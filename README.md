# Flux - Document Format Specification for Adeptus

Flux is the document format specification and example library for the [Adeptus](../adeptus/) documentation platform. It defines the content structure, YAML frontmatter metadata schemas, Markdoc authoring patterns, and CI/CD ingestion rules that govern how technical documentation is authored, validated, and published through Adeptus.

Flux is **not** a runtime service. There is no source code, no `Cargo.toml`, and nothing to compile or deploy. It is a specification with worked examples.

Originally conceived as a separate system for software release notes ("Flux"), the concept was unified into the broader Adeptus platform. This directory preserves the name and serves as the canonical reference for all document types that Adeptus supports.

## Contents

| Path | Description |
|------|-------------|
| `ARCHITECTURE.md` | Architectural diagram |
| `EXAMPLES/` | Sample Markdoc documents for every supported document type, including a complete multi-file composed manual |

## Document Types

Adeptus supports nine document types, each with its own metadata schema defined in YAML frontmatter. All types share common fields (`id`, `type`, `title`, `print`, `status`, `language`, `creationDate`, `updateDate`, `accessLevel`, `tags`, `files`) and add type-specific fields as described below.

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | automatically assigned |
| `type` | string | see list |
| `title` | sting | document title |
| `documentNumber` | int | Document number for all items that are printed (optional and triggers automated PDF generation in pipeline) |
| `status` | string | `draft` / `review` / `published` / `archived` |
| `version` | string | document version. default to 1.0 |
| `language` | string | en-US |
| `firstReleaseDate` | date | When the release was first published (auto filled by PR) |
| `updateDate` | date | When the release was updated (auto filled by PR) |
| `accessLevel` | string | SSO |
| `tags` | string[] | array of tags to help categorize and search for articles |
| `files` | string[] | associated download files |
| `documentHistory` | object[ date , string] | array of entry objects that contain date of change and description of change |



### 1. Release Notes (Atomic - but with automated component)

Version-based aggregations of release items. Not atomic themselves -- they compose items by reference to JIRA tickets and include any custom texts or instructions that accompany the release

| Field | Type | Description |
|-------|------|-------------|
| `swVersion` | string | Release version, e.g. `"1.5.0"` |
| `swAccess` | string | `standard` / `beta` / `<specific_customer>`|

### 2. Manuals (Composed)

Comprehensive user or service manuals. Always composed documents with an `index.markdoc` entry point referencing chapters and partials.

| Field | Type | Description |
|-------|------|-------------|
| `hwVersionRobot`| string | (Optional) robot HW version |
| `hwVersionTM`| string | (Optional) top module HW version |
| `swVersion`| string | (Optional) SW version |
| `products`| string[] | (Optional) the product the guide is relevant for |
| `configFile` | string | Path to applicable config file |
| `sections` | string[] | Ordered array of chapter file paths |

### 3. Notice (atomic)

Technical service/safety bulletins and maintenance notices targeting field service technicians and engineering.

| Field | Type | Description |
|-------|------|-------------|
| `category` | string | `product` / `safety` |
| `affectedProducts` | string[] | Product identifiers |
| `affectedHwRanges` | object[] | Serial number ranges (optional) |
| `expiryDate` | date | When the note becomes obsolete |


### 4. Product Notes

Product announcements, transitions, end-of-life notices.

| Field | Type | Description |
|-------|------|-------------|
| `title` | string | Product note title |
| `description` | string | Description |
| `noteType` | string | `new_product` / `hw_update` / `replacement` / `retired` / `eol` |
| `affectedProducts` | string[] | Products being changed |
| `replacementProducts` | string[] | Replacement product identifiers (if applicable) |
| `effectiveDate` | date | When the change takes effect |

### 5. Article (Atomic)

How-to guides, tutorials, and feature documentation that are collected on one page

| Field | Type | Description |
|-------|------|-------------|
| `hwVersionRobot`| string | (Optional) robot HW version |
| `hwVersionTM`| string | (Optional) top module HW version |
| `swVersion`| string | (Optional) SW version |
| `products`| string[] | (Optional) the product the guide is relevant for |
| `orderNumber` | int | (optional) for spare part guides |

### 6. FAQs (Atomic)

Frequently asked questions, individually authored and independently searchable.

| Field | Type | Description |
|-------|------|-------------|
| `question` | string | The question text |
| `category` | string | Category for organisation, e.g. `"troubleshooting/power-supplies"` |
| `popularity` | number | View/interaction count (tracked by Adeptus) |

## Content Format

All documents are authored in [Markdoc](https://markdoc.dev/) -- a Markdown superset with structured extensions. Metadata is expressed as YAML frontmatter at the top of each `.markdoc` file.

### Frontmatter

Every document begins with a YAML frontmatter block:

```yaml
---
id: "item-2025-11-04-001"
type: "release_item"
title: "Fix voltage regulator instability"
documentNumber : 12345678
status: "published"
version: 1.0
language: "en-us"
firstReleaseDate: "2025-11-04"
updateDate: ""
tags: ["bugfix", "firmware", "power-system"]
accessLevel: ["engineering", "public"]
files:
  - path: "assets/power-graph-screenshot.png"
    type: "image"
    description: "Screenshot of new interactive power graph"
  - url: "https://design.example.com/specs/power-graph-v2"
    type: "link"
    description: "Complete UI/UX design specification"
---
```
### JIRA ticket component

Release notes use JIRA ticket component that fetches JIRA tickets with selected filtering

{{ renderReleaseTickets("fixVersion"="x.x.x", "ReleaseNote"="Published") }}


### Partials

Reusable content fragments are included with the `partial` tag:

```markdoc
{% partial file="partials/safety-banner.markdoc" /%}
{% partial file="chapters/01-introduction.markdoc" /%}
```

Partials can themselves include other partials. The CI/CD pipeline resolves them recursively.

### Callouts

Structured callout blocks for warnings, notes, and other highlighted content:

```markdoc
{% callout type="warning" %}
**HIGH VOLTAGE**: Installation must be performed by qualified personnel only.
{% /callout %}

{% callout type="caution" %}
Do not interrupt the firmware update process.
{% /callout %}

{% callout type="note" %}
Current limiting is a safety feature, not a fault condition.
{% /callout %}

{% callout type="info" %}
Remote sensing compensates for voltage drop in output cables.
{% /callout %}

```

Supported types: `caution`, `warning`, `note`, `info`

### Template Variables

Frontmatter values are accessible within the document body:

```markdoc
**Version:** {% $markdoc.frontmatter.version %}
**Last Updated:** {% $markdoc.frontmatter.updateDate %}
**Severity:** {% $markdoc.frontmatter.severity.toUpperCase() %}
```

Global variables are also accessible

{% $global.mir100 %}
{% $global.companyName %}


Config variables are also accessible and can be used in conditional statements and image paths

{% $config.modelName %}
{% if $config.isForklift %}
{% img src="img/path/file_name_{$config.model}.png" %}

### File References

Documents reference local or external files declared in frontmatter. Within the document body, CDN URLs for local files are resolved using expression syntax:

```markdoc
![Front Panel]({{ files.find(f => f.path && f.path.includes('front-panel')).cdnUrl }})

See the [design specification]({{ files.find(f => f.description.includes('design specification')).url }}).
```


Documents reference to other tags within the project. In the case the same tag is used (e.g. if used in a partial and is used several places) the reference should use the tag with "shortest folder distance". 
```markdoc
# Header 1 {% tag id="header1"%}

 ...

For more info see {% tagref id="header1" %}

```

## Atomic vs Composed Documents

Flux defines two fundamental document structures.

### Atomic Documents

A single `.markdoc` file containing all content and metadata. No external file dependencies beyond optional media assets and partials.

**Types that are always atomic:** Everything except manuals

```
release-items/
    item-2025-11-04-001.markdoc
```

### Composed Documents

A directory containing an `index.markdoc` entry point that declares chapters, partials, and assets. The entry point's frontmatter includes `chapters[]` and `partials[]` arrays listing the constituent files. The body uses `{% partial %}` tags to assemble the full document.

**Types that are always composed:** Manuals.

```
manual-composed/
    index.markdoc                          # Metadata + chapter/partial assembly
    chapters/
        01-introduction.markdoc
        03-basic-operation.markdoc
    partials/
        safety-banner.markdoc
        front-panel-ref.markdoc
        specs-table.markdoc
        footer.markdoc
    assets/
        front-panel-diagram.svg
        rear-panel-diagram.svg
```

The `index.markdoc` body typically looks like:

```markdoc
{% partial file="partials/safety-banner.markdoc" /%}

{% partial file="chapters/01-introduction.markdoc" /%}
{% partial file="chapters/03-basic-operation.markdoc" /%}

{% partial file="partials/footer.markdoc" /%}
```

During CI/CD processing, all partials are resolved recursively and merged into a single document before upload to Adeptus.

## CI/CD Integration

Tech writers author documents in Git repositories. On commit, a CI/CD pipeline validates content against the Flux specification and pushes it to the Adeptus backend. The pipeline performs these steps:

### 1. Change Detection

The pipeline monitors paths for `.markdoc` file changes. For composed documents, any file change within the document directory triggers reprocessing of the entire document. Changes to shared partials trigger reprocessing of all documents that include them. (Ideally this should also chekc for changes in images... not sure if this is too much to ask)

If a file change is detected: 
* The `updatedDate` is updated to the current date
* The user is displayed a list of affected documents and is prompted to describe what has been changed in each.
* The provided description is logged in the file's document history 

### 2. Document Resolution

For composed documents, the pipeline reads `index.markdoc` to obtain metadata and file references, then resolves all `{% partial %}` tags by reading the referenced files recursively. The result is a single merged document.

### 3. Partial Resolution

Partials are resolved recursively:

1. Read the main document content.
2. Identify all `{% partial file="..." /%}` tags.
3. Read each referenced file.
4. If that file contains its own `{% partial %}` tags, resolve those first.
5. Substitute partial content in place of the tag.

Circular dependencies are detected and rejected during validation.

### 4. Asset Collection

All files referenced in frontmatter `files[]` arrays and inline image syntax are collected. Local files (paths relative to the document) are packaged for upload. External URLs are recorded as references without download.

### 5. Validation

Before upload, the pipeline validates:

- **Metadata completeness**: All required fields present, valid values for enums (status, severity, etc.), valid language-country codes.
- **Chapter/partial resolution**: All referenced files exist, no circular dependencies, valid Markdoc syntax.
- **Asset validation**: All referenced local files exist, file sizes within limits, supported MIME types.
- **Content validation**: Valid Markdoc syntax, no broken internal links, all document ID references resolve.
- **Tag validation**: All refTags point to a valid tag that is accessible within the scope of a composed document and no conflicts between folder levels.

### 6. Upload to Adeptus

The merged document, metadata, and assets are sent to the Adeptus ingestion API. Adeptus then stores metadata in PostgreSQL, uploads assets to CDN with access control, indexes content in Meilisearch, and records a revision entry.

### Git Repository Organisation

The specification recommends separate repositories for different content families:

- **Atomic documents** (release items, known issues, FAQs, service notes): Grouped in a single repository by type.
- **Composed documents** (manuals, comprehensive guides): Separate repositories per product or manual family to keep repository size manageable and permissions independent.

```
# Atomic documents repository
docs-repo/
    release-items/
        item-2025-11-04-001.markdoc
        item-2025-11-04-002.markdoc
    known-issues/
        issue-2025-10-15-003.markdoc
    faqs/
        faq-psu-5000-output-issues.markdoc
    service-notes/
        sn-2025-11-004.markdoc

# Composed documents repository (per product family)
docs-manuals-psu-5000/
    installation/
        index.markdoc
        chapters/
        partials/
        assets/
    user-guide/
        index.markdoc
        chapters/
        partials/
        assets/
```

## Frontmatter Filtering

When Adeptus serves documents to frontends via GraphQL, it strips internal-only metadata fields from the frontmatter. This separation ensures frontends receive only the fields relevant to rendering and navigation, while operational fields remain accessible through a separate authenticated `_internal` query path.

**Fields stripped before serving to frontends:**

| Field | Reason |
|-------|--------|
| `status` | Internal workflow state |
| `effectiveStatus` | Computed field |
| `creationDate` | Internal tracking (frontends use `publishDate`) |
| `expiryDate` | Internal lifecycle management |
| `supersededBy` | Exposed via API relationships, not raw frontmatter |
| `gitCommitSha` | Internal tracking |
| `ingestedAt` | Internal tracking |
| `requiresAttention` | Internal flag for editorial workflow |
| `attentionReason` | Internal flag |
| `daysUntilExpiry` | Computed field |
| `accessLevel` | Used for authorisation checks, not needed by frontend rendering |

**Fields included for frontends:**

`id`, `type`, `title`, `version`, `publishDate`, `updateDate`, `language`, `files` (enhanced with CDN URLs and GUIDs), `relatedDocuments`.

## Conditional Rendering

Markdoc documents can include content blocks that are conditionally rendered based on the consuming frontend's type and context. Adeptus stores the raw Markdoc with all conditional blocks intact. Each frontend evaluates the conditionals and renders only the matching blocks.

### Syntax

```markdoc
{% if $frontendType === "web" %}
## Web-Specific Instructions
Use your mouse to click the buttons shown in the screenshots below.
{% /if %}

{% if $frontendType === "pdf" %}
## PDF Note
This is a static PDF version. For interactive features, use the web interface.
{% /if %}

{% if $deviceType === "mobile" %}
{% callout type="note" %}
Rotate your device to landscape mode for better graph visibility.
{% /callout %}
{% /if %}
```

### Available Variables

| Variable | Values | Description |
|----------|--------|-------------|
| `$frontendType` | `web`, `tablet`, `mobile`, `pdf`, `embedded` | Which frontend is rendering |
| `$deviceType` | `desktop`, `tablet`, `mobile` | Physical device class |
| `$platform` | `browser`, `ios`, `android`, `windows` | Operating environment |
| `$language` | e.g. `"en-us"` | User's selected language |
| `$accessLevel` | string[] | User's SSO groups (enables role-based content) |

And variables defined in config or frontmatter.

### Advanced Example

Variables can be combined for fine-grained conditional content:

```markdoc
{% if $frontendType === "web" && $accessLevel.includes("engineering") %}
## Engineering-Only Web Content
This section is only visible to engineers viewing in the web frontend.
{% /if %}
```

## File Management

Documents reference media and attachments through the frontmatter `files[]` array. Files are either local (committed alongside the Markdoc document in Git) or external (URLs to resources hosted elsewhere).

### Local Files

```yaml
files:
  - path: "assets/power-graph-screenshot.png"
    type: "image"
    description: "Screenshot of new interactive power graph"
```

On commit, the CI/CD pipeline uploads local files to Adeptus. Adeptus then:

1. Computes a BLAKE3 content hash.
2. Checks for an existing file with the same hash (deduplication).
3. If new, assigns a GUID and uploads to CDN with access control derived from the document's `accessLevel`.
4. If the file already exists, reuses the existing CDN entry and increments the reference count.
5. Replaces the local path in the stored Markdoc with the CDN URL or GUID reference.

### External Files

```yaml
files:
  - url: "https://www.chartjs.org/docs/latest/"
    type: "link"
    description: "Chart.js documentation (external library)"
```

External references are stored as-is. No download, hashing, or CDN upload occurs.

### Access Control on Files

Files inherit their document's `accessLevel` by default. A file can override this with its own `accessLevel` field:

```yaml
files:
  - path: "assets/internal-diagram.svg"
    type: "image"
    description: "Internal circuit diagram"
    accessLevel: ["engineering"]       # More restrictive than the document

  - path: "assets/front-panel.jpg"
    type: "image"
    description: "Front panel photograph"
    accessLevel: ["public"]            # Public marketing image
```

Public files are served directly from CDN. Restricted files require signed URLs generated by Adeptus after verifying the requester's permissions through Ory Keto.

### Deduplication

Files are deduplicated by BLAKE3 hash. If two documents reference the same binary content (even under different filenames), only one copy is stored on the CDN. The `document_files` junction table tracks which documents reference which files, and a `reference_count` on each file record enables garbage collection of orphaned assets.

## Lifecycle States

```
draft --> review --> published --> archived --> unpublished
```

| State | Description |
|-------|-------------|
| `draft` | Document being authored, not visible to end users |
| `review` | Complete, awaiting final approval |
| `published` | Visible to authorised users |
| `archived` | Historical, no longer actively maintained but still queryable |
| `unpublished` | Fully retired, no longer queryable by end users. Only accessible to administrators for audit purposes |

The Adeptus GraphQL API supports filtering by status on all queries. Frontends typically request only `published` documents. Unpublished documents are excluded from all standard queries and only accessible through an authenticated administrative query path.

## Platform Integration

Flux defines the format; the rest of the platform consumes it.

```
  Tech Writers (Git)
        |
        |  Author .markdoc files with Flux metadata schemas
        v
  CI/CD Pipeline
        |
        |  Validate against Flux spec
        |  Resolve partials, collect assets
        v
  Adeptus Backend (Rust)
        |
        |  Store metadata in PostgreSQL
        |  Upload assets to DAM + CDN
        |  Index in Meilisearch
        |  Serve raw Markdoc via GraphQL
        v
  Frontends (Dioxus web, tablet, mobile, PDF generator)
        |
        |  Receive raw Markdoc
        |  Evaluate conditional blocks
        |  Render to HTML or PDF client-side
        v
  End Users
```

### Key integration points

- **Adeptus** ingests and serves content authored in Flux format. It stores raw Markdoc (not pre-rendered HTML) and delegates rendering to frontends.
- **Frontends** receive raw Markdoc from the Adeptus GraphQL API and render it locally, enabling conditional content based on device type, user role, and platform.
- **Media** referenced in documents is delegated to a Digital Asset Management system (DAM) and served through a CDN. Adeptus stores references (GUIDs, hashes, CDN URLs) but does not host binary media itself.
- **Access control** in frontmatter maps to Ory Keto permission tuples. Adeptus queries Keto on every document and file access request.
- **PDF generation** is handled by a separate microservice that acts as a specialised frontend -- it receives Markdoc, evaluates conditionals with `$frontendType = "pdf"`, renders to HTML, generates a PDF via headless Chromium, and injects version-check JavaScript.
- **Search** is powered by Meilisearch. Adeptus extracts plain text from Markdoc (stripping syntax) and indexes it for full-text, typo-tolerant search with faceted filtering by document type, tags, language, and status.

### Related services

Flux and Adeptus are part of a larger enterprise platform. See the [platform README](../README.md) for the full architecture including:

- **Sparta** -- Spare parts tracking
- **Artemis** -- Software artifact distribution
- **Genesis** -- Unit lifecycle and traceability
- **Ory ecosystem** -- Authentication and authorisation (Kratos, Hydra, Keto, Oathkeeper)
