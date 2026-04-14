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

Adeptus supports nine document types, each with its own metadata schema defined in YAML frontmatter. All types share common fields (`id`, `type`, `title`, `description`, `status`, `language`, `creationDate`, `updateDate`, `accessLevel`, `tags`, `files`) and add type-specific fields as described below.

### 1. Release Items (Atomic)

Individual changes, fixes, or features that can be independently referenced and aggregated into release notes.

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique identifier (issued by Adeptus API) |
| `type` | string | `"release_item"` |
| `title` | string | Short description of the change |
| `status` | string | `draft` / `review` / `published` / `archived` |
| `language` | string | Language-country code, e.g. `"en-us"` |
| `creationDate` | date | When the item was created |
| `updateDate` | date | When the item was last modified |
| `tickets` | string[] | Internal ticket references, e.g. `["ENG-1423", "ENG-1458"]` |
| `tags` | string[] | Categories, e.g. `["bugfix", "firmware", "power-system"]` |
| `accessLevel` | string[] | SSO groups with read access |
| `files` | object[] | Local or external file references |

### 2. Known Issues (Atomic)

Documented bugs, limitations, or problems -- the complement of release items.

Extends the release item schema with:

| Field | Type | Description |
|-------|------|-------------|
| `severity` | string | `critical` / `high` / `medium` / `low` / `cosmetic` |
| `affectedVersions` | string[] | Software versions affected |
| `resolvedInVersion` | string | Version where the issue is fixed (empty if unresolved) |
| `workarounds` | string[] | Workaround identifiers or descriptions |
| `relatedIssues` | string[] | IDs of related known issues |
| `discoveredDate` | date | When the issue was first observed |
| `resolvedDate` | date | When the issue was resolved |

### 3. Release Notes

Version-based aggregations of release items. Not atomic themselves -- they compose items by reference.

| Field | Type | Description |
|-------|------|-------------|
| `title` | string | Release note title |
| `description` | string | Brief description |
| `version` | string | Release version, e.g. `"1.5.0"` |
| `status` | string | `draft` / `review` / `published` / `archived` |
| `items` | string[] | Array of release item IDs to include |
| `releaseDate` | date | When the release was published |

### 4. Manuals (Composed)

Comprehensive user or service manuals. Always composed documents with an `index.markdoc` entry point referencing chapters and partials.

| Field | Type | Description |
|-------|------|-------------|
| `title` | string | Manual title |
| `description` | string | Brief description |
| `category` | string | Category path, e.g. `"installation-manuals/power-supplies"` |
| `version` | string | Document version |
| `chapters` | string[] | Ordered array of chapter file paths |
| `partials` | string[] | Reusable partial file paths |
| `relatedDocuments` | object[] | Related document IDs with relationship type (`related`, `references`, `supersedes`) |

### 5. Service Notes

Technical service bulletins and maintenance notices targeting field service technicians and engineering.

| Field | Type | Description |
|-------|------|-------------|
| `title` | string | Service note title |
| `description` | string | Description |
| `severity` | string | `info` / `warning` / `critical` |
| `affectedProducts` | string[] | Product identifiers |
| `affectedSerialRanges` | object[] | Serial number ranges (optional) |
| `expiryDate` | date | When the note becomes obsolete |

### 6. Safety Notes

Safety warnings and regulatory compliance information. Rarely archived.

| Field | Type | Description |
|-------|------|-------------|
| `title` | string | Safety note title |
| `description` | string | Description |
| `severity` | string | `caution` / `warning` / `danger` |
| `regulatoryStandards` | string[] | Standards, e.g. `["IEC 61010-1", "UL 61010-1"]` |
| `affectedProducts` | string[] | Product identifiers |
| `affectedSerialRanges` | object[] | Serial number ranges (optional) |

### 7. Product Notes

Product announcements, transitions, end-of-life notices.

| Field | Type | Description |
|-------|------|-------------|
| `title` | string | Product note title |
| `description` | string | Description |
| `noteType` | string | `new_product` / `update` / `replacement` / `retired` / `eol` |
| `affectedProducts` | string[] | Products being changed |
| `replacementProducts` | string[] | Replacement product identifiers (if applicable) |
| `effectiveDate` | date | When the change takes effect |

### 8. Guides (Atomic or Composed)

How-to guides, tutorials, and quickstart documentation. Simple guides are single files; comprehensive guides use the composed document structure.

| Field | Type | Description |
|-------|------|-------------|
| `difficulty` | string | `beginner` / `intermediate` / `advanced` |
| `estimatedTime` | number | Estimated completion time in minutes |
| `sections` | string[] | Section file paths (for composed guides, optional) |
| `partials` | string[] | Reusable partial file paths (optional) |

### 9. FAQs (Atomic)

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
status: "published"
language: "en-us"
creationDate: "2025-11-04"
updateDate: ""
tickets: ["ENG-1423", "ENG-1458"]
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

### Template Functions

Release notes use template functions to reference and render release items:

```markdoc
{# Include a specific release item by ID #}
{{ releaseItem("item-2025-11-04-001") }}

{# Render all items listed in the frontmatter items[] array #}
{{ renderReleaseItems() }}
```

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
{% callout type="danger" %}
**HIGH VOLTAGE**: Installation must be performed by qualified personnel only.
{% /callout %}

{% callout type="warning" %}
Do not interrupt the firmware update process.
{% /callout %}

{% callout type="note" %}
Current limiting is a safety feature, not a fault condition.
{% /callout %}

{% callout type="info" %}
Remote sensing compensates for voltage drop in output cables.
{% /callout %}

{% callout type="success" %}
Your PSU-5000 is now powering your load.
{% /callout %}
```

Supported types: `danger`, `warning`, `note`, `info`, `success`.

### Template Variables

Frontmatter values are accessible within the document body:

```markdoc
**Version:** {% $markdoc.frontmatter.version %}
**Last Updated:** {% $markdoc.frontmatter.updateDate %}
**Severity:** {% $markdoc.frontmatter.severity.toUpperCase() %}
```

### File References

Documents reference local or external files declared in frontmatter. Within the document body, CDN URLs for local files are resolved using expression syntax:

```markdoc
![Front Panel]({{ files.find(f => f.path && f.path.includes('front-panel')).cdnUrl }})

See the [design specification]({{ files.find(f => f.description.includes('design specification')).url }}).
```

## Atomic vs Composed Documents

Flux defines two fundamental document structures.

### Atomic Documents

A single `.markdoc` file containing all content and metadata. No external file dependencies beyond optional media assets.

**Types that are always atomic:** Release Items, Known Issues, FAQs, Product Notes.

**Types that may be atomic:** Service Notes, Safety Notes, Guides.

```
release-items/
    item-2025-11-04-001.markdoc
```

### Composed Documents

A directory containing an `index.markdoc` entry point that declares chapters, partials, and assets. The entry point's frontmatter includes `chapters[]` and `partials[]` arrays listing the constituent files. The body uses `{% partial %}` tags to assemble the full document.

**Types that are always composed:** Manuals.

**Types that may be composed:** Guides (when sufficiently complex).

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

## Examples Directory Guide

The `EXAMPLES/` directory contains working samples for every supported document type.

### Atomic Document Examples

| File | Type | Description |
|------|------|-------------|
| `release_item.markdoc` | Release Item | Voltage regulator bug fix -- minimal frontmatter example |
| `release_item_with_files.markdoc` | Release Item | Web UI power graphs -- demonstrates local and external file references, CDN URL expressions, and rich content |
| `known_issue.markdoc` | Known Issue | Graph rendering failure with >10,000 data points -- severity, affected versions, workarounds, related issues |
| `release_note.markdoc` | Release Note | v1.5.0 release using `{{ releaseItem("id") }}` to include individual items |
| `release_note-alt_format.markdoc` | Release Note | v1.5.0 release using `{{ renderReleaseItems() }}` with an `items[]` array in frontmatter |
| `service_note.markdoc` | Service Note | Critical firmware update bulletin -- severity, affected serial ranges, expiry date |
| `safety_note.markdoc` | Safety Note | High-voltage safety and regulatory compliance -- danger severity, regulatory standards array |
| `product_note.markdoc` | Product Note | PSU-3000 to PSU-3000-X replacement transition -- replacement products, effective date, timeline |
| `guide.markdoc` | Guide | PSU-5000 quick start guide -- difficulty, estimated time, step-by-step instructions |
| `faq.markdoc` | FAQ | Voltage drop troubleshooting -- question, category, popularity counter |

### Single-File Manual Example

| File | Type | Description |
|------|------|-------------|
| `manual.markdoc` | Manual (atomic) | PSU-5000 installation manual -- a complete manual in a single file with callouts, file references, and related document links |

### Composed Manual Example

The `manual-composed/` directory demonstrates the multi-file manual structure:

```
EXAMPLES/manual-composed/
    index.markdoc                          # Entry point: metadata, chapter/partial declarations
    chapters/
        01-introduction.markdoc            # Chapter 1: welcome, manual organisation, safety callout
        03-basic-operation.markdoc         # Chapter 3: front panel controls, operating modes, output enable
    partials/
        safety-banner.markdoc              # Reusable danger callout for high-voltage warning
        front-panel-ref.markdoc            # Front panel controls and display reference table
        specs-table.markdoc                # PSU-5000/HV/LV specification comparison table
        footer.markdoc                     # Document information, support contacts, legal notice
```

The `index.markdoc` frontmatter declares all eight chapters and four partials (only a subset of chapters are included as examples). Chapters reference partials themselves -- for instance, `03-basic-operation.markdoc` includes `front-panel-ref.markdoc` via a `{% partial %}` tag.

## CI/CD Integration

Tech writers author documents in Git repositories. On commit, a CI/CD pipeline validates content against the Flux specification and pushes it to the Adeptus backend. The pipeline performs these steps:

### 1. Change Detection

The pipeline monitors paths for `.markdoc` file changes. For composed documents, any file change within the document directory triggers reprocessing of the entire document. Changes to shared partials trigger reprocessing of all documents that include them.

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

### Release Items

```
draft --> review --> published --> archived
```

| State | Description |
|-------|-------------|
| `draft` | Work in progress, not ready for inclusion in releases |
| `review` | Complete and ready for technical/editorial review |
| `published` | Approved and available for inclusion in releases |
| `archived` | Superseded or no longer relevant |

### Known Issues

```
open --> investigating --> workaround_available --> planned_fix --> resolved
                                                               \-> wont_fix
```

| State | Description |
|-------|-------------|
| `open` | Issue reported but not yet triaged |
| `investigating` | Engineering is analysing the root cause |
| `workaround_available` | A workaround has been documented |
| `planned_fix` | A fix is scheduled for a future release |
| `resolved` | The issue has been fixed |
| `wont_fix` | The issue will not be addressed |

### Documents (All Other Types)

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
