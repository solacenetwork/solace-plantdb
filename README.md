# SOLACE Garden Plant Database (PlantDB)

PlantDB is a separate project for maintaining, administering and publishing reference information about plants, including growing, maintenance, pest control, scientific classification and harvesting. Its intended output includes JSON data that applications such as SOLACE Garden can consume.

## Current Garden V1 boundary

**Garden V1 does not depend on building the PlantDB administration or publishing application.** Garden currently has a generated reference artifact at `public/assets/data/plants.json` in the `solacenetwork/solace-garden` repository. Garden V1 will consume that JSON artifact and integrate plant browsing, searching, selection and plant-related Garden workflows on the application side.

How the plant reference catalog is browsed and selected, how gardeners add local plant records, and how catalog references behave across updates are **not yet finalized**. They will be designed in Garden's later plant-integration milestone, using early prototypes as references. The Garden roadmap is authoritative for V1 scope and milestone order: [SOLACE Garden roadmap](https://github.com/solacenetwork/solace-garden/blob/main/docs/ROADMAP.md).

## PlantDB backend — future work

The independent PlantDB administration/publishing tool is a **potential V2/V3 project**, not a V1 blocker. Future work may include managing an authoritative plant dataset, validating submissions, moderation and generating published JSON artifacts. No specific backend implementation or community submission workflow is committed for Garden V1.

Garden may continue using a generated/static `plants.json` artifact before the full publishing tool exists. The reference artifact and its Garden-side consumption are separate concerns from how the artifact is produced.

## Historical vision (deferred, not current V1 requirements)

Early SOLACE development notes envisioned a centrally maintained, community-contributed plant reference database:

1. PlantDB maintains an authoritative collection of plant records.
2. Applications consume published JSON datasets.
3. Gardeners may create local plant records.
4. Gardeners may optionally submit records to the central collection.
5. Submissions enter a moderation queue.
6. Authorized moderators review proposed additions.
7. Approved records are incorporated and the dataset is republished.

The historical PHP implementation included some database-backed administration and JSON-related functionality, but completion of that contribution/moderation workflow was never verified.

These ideas remain possible future directions, **not requirements for Garden V1 or evidence that the backend has already been implemented**. Local plant support and the exact Garden integration interface are still subject to Garden-side design decisions.
