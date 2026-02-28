# Aristophia - Vocabulary Builder

I designed this application using a static-first architecture to optimize performance and simplicity for a 2000+ word dataset.

Instead of introducing a database or backend API layer, I chose to pre-compile the dataset at build time and distribute it globally through AWS CloudFront.

Edge Distribution (AWS CloudFront): Content is served via a CDN to reduce latency and improve availability.

Build-Time Data Strategy: All primary data is injected into the client bundle during the build process, eliminating runtime database queries.

HTTPS Security: Traffic is delivered securely via SSL/TLS encryption.

Client-Side Filtering: Features such as FAVS are handled through in-memory filtering to avoid unnecessary network calls.

Extensible Structure: The frontend is structured to allow future integration with a backend service (e.g., Java/Spring Boot) when user authentication or synchronization is required.

## License & Copyright

**© 2026 [Akif Acet] - All Rights Reserved.**

This repository serves strictly as a project showcase/portfolio. The source code, data sets, architectural pipelines, and proprietary content are **closed-source**. You are free to view the application via the live link, but you may not duplicate, copy, or reuse any part of the project without explicit, written permission.
