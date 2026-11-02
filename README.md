# SOLACE Garden Plant Database

The Plant Database (PlantDB) is a database of plants with information about growing, maintenance, pest control, scientific classification, harvesting, etc.

SOLACE Garden consumes data from PlantDB, but PlantDB doesn't depend on Garden app.

### PlantDB — Community Contributions, Moderation, and Publication

**Historical source:** Early handwritten SOLACE development notebooks, clarified during the November 2026 historical review.

**Original vision:** PlantDB was intended to be a centrally maintained, community-contributed reference database of plants. The central collection would begin with a basic dataset and expand through submissions from SOLACE participants.

**Proposed workflow:**

1. SOLACE PlantDB maintains an authoritative collection of plant records.
2. Garden and other consumers access published PlantDB data through JSON feeds.
3. Individual Garden users may create additional plant records locally for their own purposes.
4. The user may optionally submit a local plant record to the central SOLACE PlantDB.
5. Submitted records enter a moderation queue rather than becoming immediately public.
6. An authorized moderator reviews submissions and determines whether to accept them into the central dataset.
7. Approved records are incorporated into PlantDB.
8. The central dataset is republished as JSON, making approved additions available to Garden and other consumers.

**Design principles:**

- Local users retain the ability to maintain their own plant records.
- Contributing records to the central database is optional.
- Submission does not imply automatic publication.
- Moderation protects the quality of the shared reference collection.
- Published datasets are separate from submission and administrative workflows.
- PlantDB serves multiple potential applications rather than belonging exclusively to Garden.

**Historical implementation comparison:** The PHP PlantDB included database-backed administration and JSON-related functionality, but its administrative interface did not establish the full contributor-to-moderator-to-publication workflow described in the notebooks.

**Implementation status:** Partial historical administration and publishing code; proposed contribution/moderation workflow not verified as implemented.

**Future disposition:** PlantDB has been separated from Garden as an independent project. Garden v1 must provide access to PlantDB, but the integration mechanism and the future contribution/moderation architecture remain undecided.