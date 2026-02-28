# Aristophia - Vocabulary Builder

(https://aristophia.com)


**Aristophia** is a high-performance, single-page (SPA) vocabulary learning application optimized for academic exams like TOEFL and IELTS. It provides reliable pronunciations, categorized definitions, and example sentences for over 2000 highly-probable English words, designed with an offline-first approach.

### Architecture & Backend Philosophy

As a backend-focused developer, I architected this application prioritizing raw performance, data decoupling, and future scalability. Instead of making constant database queries or API calls for 2000+ words, the architecture resolves around **Pre-rendering and Aggressive In-Memory Caching**:

- **Pre-compiled Data Delivery:** The massive word dataset is securely processed and injected into the client bundle at build time. This completely eliminates server latency, connection drops, and API loading times.
- **In-Memory Filtering (FAVS):** Queries and data filtering (like fetching users' favorite words) are handled instantly via smart DOM-level caching rather than making server requests.
- **Future-Proof Scalability:** The current decoupled frontend logic can easily be integrated into a RESTful API or a microservice architecture (e.g., a Spring Boot backend) when features like cross-device user synchronization are needed in the future.
- **Zero-Dependency Frontend:** Built entirely with Vanilla JavaScript and CSS to minimize payload size and achieve maximum efficiency, especially on lower-end mobile devices.

---

## License & Copyright

**© 2026 [Akif Acet] - All Rights Reserved.**

This repository serves strictly as a project showcase/portfolio. The source code, data sets, architectural pipelines, and proprietary content are **closed-source**. You are free to view the application via the live link, but you may not duplicate, copy, or reuse any part of the project without explicit, written permission.
