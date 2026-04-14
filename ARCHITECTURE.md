```
┌──────────────────────────────────────────────────────────────┐
│                   Tech Writers (Git)                         │
│  ┌─────────────┐   ┌─────────────┐   ┌─────────────┐         │
│  │  Manuals    │   │  Releases   │   │Service Notes│         │
│  │   Repo      │   │    Repo     │   │    Repo     │  ...    │
│  └──────┬──────┘   └──────┬──────┘   └──────┬──────┘         │
└─────────┼─────────────────┼─────────────────┼────────────────┘
          │                 │                 │
          │   ┌─────────────▼─────────────────┴─┐
          │   │      CI/CD Pipeline             │
          │   │  - Validate Markdoc             │
          │   │  - Parse frontmatter            │
          └───►  - Upload to Adeptus            │
              │  - Push assets to CDN           │
              └────────────┬────────────────────┘
                           │
          ┌────────────────▼────────────────────────────┐
          │         Adeptus Backend (Rust)              │
          ├─────────────────────────────────────────────┤
          │  API Layer                                  │
          │  ├── GraphQL (primary)                      │
          │  └── REST (files, PDF generation)           │
          ├─────────────────────────────────────────────┤
          │  Core Services                              │
          │  ├── DocumentService                        │
          │  ├── ReleaseService (specialized)           │
          │  ├── GlossaryService                        │
          │  ├── FileService                            │
          │  └── PdfService                             │
          ├─────────────────────────────────────────────┤
          │  Storage & Search                           │
          │  ├── PostgreSQL (structured data)           │
          │  ├── Meilisearch (full-text search)         │
          │  └── CDN (files with access control)        │
          ├─────────────────────────────────────────────┤
          │  Infrastructure                             │
          │  ├── OpenConnect ID (SSO auth)              │
          │  ├── OpenTelemetry (observability)          │
          │  └── Audit logging                          │
          └────────────┬────────────────────────────────┘
                       │
          ┌────────────▼─────────────────────────────┐
          │      Dioxus Frontend (Multi-backend)     │
          │  ┌───────────────────────────────────┐   │
          │  │  Content Rendering                │   │
          │  │  ├── Markdoc → HTML               │   │
          │  │  ├── Search UI                    │   │
          │  │  └── Component library            │   │
          │  └───────────────────────────────────┘   │
          │  ┌───────────────────────────────────┐   │
          │  │  Backend Integration              │   │
          │  │  ├── Adeptus (docs - primary)     │   │
          │  │  ├── Sparta (spare parts)         │   │
          │  │  └── Artemis (software artifacts) │   │
          │  └───────────────────────────────────┘   │
          └──────────────────────────────────────────┘
```
