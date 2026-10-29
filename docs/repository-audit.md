# Repository audit — preliminary public-source pass

**Status:** Partial audit, not a completed source-code audit. This document distinguishes facts visible on public repository pages from items that still require file-by-file inspection. Local working copies were not available in this session. No claims below imply tests were run or applications were executed.

## Summary of verified access

| Repository | Public URL | What is currently verified | Status / next step |
|---|---|---|---|
| TradLingo | https://github.com/riahiali/tradlingo | README describes Python/Streamlit, Hugging Face Inference Providers, Helsinki-NLP models, SQLite local auth, PBKDF2-SHA256 password hashing, in-memory translation cache, `.txt` upload, and pytest tests using mocks. | README reviewed; source-level implementation and test execution still required. |
| Nexor Application | https://github.com/riahiali/nexor-application | Public page lists `docs`, `nexor-backend`, `nexor-rn`, and `package.json`. | Directory-level inspection only; open manifests and source files. |
| Filmi Gestion Film | https://github.com/riahiali/Filmi-gestion-film | Public repository page resolves. | README and source details not yet verified in this pass. |
| Filmi | https://github.com/riahiali/filmi | Public repository page resolves. | README and source details not yet verified in this pass. |
| Nexor Framework | https://github.com/riahiali/nexorFW | Public repository page resolves. | README and source details not yet verified in this pass. |
| ETL Data Pipeline System | https://github.com/riahiali/ETL-Data-pipeline-system | Public repository page resolves. | README, dependencies, pipeline steps and tests still need inspection. |
| UIB | https://github.com/riahiali/UIB | Public page lists `api`, `frontend`, and `nlp` directories. | Structure supports targeted investigation; no model, API provider, accuracy, or working flow is verified yet. |
| Mobile Backend | https://github.com/riahiali/mobile-backend | Public repository page resolves. | README and source details not yet verified in this pass. |
| E-commerce Backend | https://github.com/riahiali/e-commerce-backend | Public repository page resolves. | README and source details not yet verified in this pass. |
| SaaS Multi-tenant | https://github.com/riahiali/Saas-Multi-tenant | Public page resolves and has repository content. | Need inspect implementation, tenant isolation, auth, tests and deployment claims. |
| CXAI | https://github.com/riahiali/CXAI | GitHub currently reports the repository is empty. | Do not feature as an implemented AI product unless local source is found. |
| Campini | https://github.com/riahiali/campini | GitHub currently reports the repository is empty. | Local counterpart may contain code; otherwise mark inaccessible/empty. |
| Replanto | https://github.com/riahiali/replanto | Public repository page resolves and has repository content. | README, manifests and actual features still need inspection. |
| Nexor Firmware | https://github.com/riahiali/Nexor-Firmware | Supplied URL returned 404 during this pass. | Check capitalization/name or local counterpart; do not infer absence of project. |
| Nexor Web | https://github.com/riahiali/Nexor-web | Supplied URL returned 404 during this pass. | Check capitalization/name or local counterpart; do not infer absence of project. |
| Sarraj Harmony Hub | https://github.com/riahiali/sarraj-harmony-hub | Supplied URL returned 404 during this pass. | Check spelling/access/local counterpart. |
| Mizora | https://github.com/riahiali/mizora | Public repository page resolves and has repository content. | README, manifests and actual features still need inspection. |
| Vehicle Navigator App | https://github.com/riahiali/vehicle-navigator-app | Supplied URL returned 404 during this pass. | Check URL/access/local counterpart. |

## AI integration evidence

### Confirmed from public README: TradLingo
- README describes Hugging Face Inference Providers and Helsinki-NLP translation models.
- The README names configuration variables for the Hugging Face token, inference URL, and directional model choices.
- It describes translation from French/English/Arabic, with French↔Arabic routed through English, plus an in-memory cache.
- It describes SQLite-based local accounts and PBKDF2-SHA256 password hashing.
- The README says tests use mocks and can run without an API key. Tests have not been executed in this audit.

### UIB — investigation required
The public repository has `api`, `frontend`, and `nlp` directories. This is not enough to confirm which model or provider was used, whether training actually occurs, or the end-to-end architecture. Inspect NLP source, API routes, dependency files, environment variables and README before writing the case study.

### CXAI — no public source currently available
The public repository page says the repository is empty. No AI capability should be attributed to it without local code or other evidence.

## Resume-grounded facts supplied for portfolio draft

The following information comes from the project instructions and is not independently verified against the original French PDF in this workspace:
- Professional title: Junior Backend Software Engineer & Database Administration Engineer.
- Capgemini Engineering / BMW project: Embedded Software Testing Engineer, June–September 2025.
- UIB: AI & Backend Developer, February–May 2024.
- Wattnow: Embedded Software Developer, Summer 2023.
- Linedata: Software Engineering Intern, Summer 2022.
- Freelance Backend & Full-Stack Developer, 2023–present.
- Education, skills, language levels and association leadership should be reconciled against the actual original CV before publication.

## Blocking limitations
1. The original `CV-RiahiAli_updated.pdf` was referenced in the instructions but was not included among the files available for this pass. Therefore a faithful *complete* résumé translation cannot yet be certified.
2. Local project folders on the user's Windows machine are not mounted in this environment.
3. GitHub source pages were accessible selectively, but this pass did not inspect all source files, run projects, execute tests, capture real screenshots, or deploy.
4. The portfolio starter includes clearly labeled conceptual graphics; they are not represented as genuine screenshots.

## Next audit procedure
For every accessible repository: inspect README, directory tree, dependency manifests, application entry points, API routes, model clients/prompts, tests, screenshots, CI configuration, deployment files and commit history. Then run tests/builds where practical and update each row with exact file paths and verification outcomes.
