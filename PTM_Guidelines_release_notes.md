![](https://drive.google.com/uc?id=1MStOYYaZDqrvuOwlmecX0iayL0Jt_eAN)
# Podcast Technical Measurement Guidelines (PTMG) — Release Notes

This document records the published history of the IAB Tech Lab Podcast Technical Measurement Guidelines (PTMG), including final releases and identifiable public-comment or maintenance milestones.

The history below concerns the measurement guidelines themselves. The separate [Podcast Measurement Compliance Program](https://iabtechlab.com/compliance-programs/podcast-measurement-compliance/) maintains its own program requirements, audit procedures, and certification records.

## Current release

**PTMG v2.3**, finalized September 29, 2026, is the current published version.

- [Read PTMG v2.3](PTM-Guidelines_v2.3.md)
- [IAB Tech Lab PTMG resources](https://iabtechlab.com/standards/podcast-measurement-guidelines/)

## Release history at a glance

| Version or milestone | Date | Status |
| --- | --- | --- |
| v3.0 | In development; public comment planned for mid-2027 | Unreleased |
| v2.3 | September 29, 2026 | Final |
| v2.3 public-comment draft | July 21–August 19, 2026 | Superseded draft |
| v2.2 | May 2, 2024 | Final |
| v2.2 public-comment draft | February 22–March 23, 2024 | Superseded draft |
| v2.1 annual maintenance update | October 11, 2022 | Maintenance update recorded in the published change log |
| v2.1 | March 2021 | Final document date; see the date note below |
| v2.1 revised draft | January 11, 2021 | Superseded draft |
| v2.1 public-comment period | December 2–31, 2020 | Superseded draft |
| v2.1 initial draft | November 2, 2020 | Superseded draft |
| v2.0 | December 20, 2017 | Final |
| v2.0 public-comment period | July 12–August 11, 2017; subsequently extended through September 8, 2017 | Superseded draft |
| v1.0 | September 6, 2016 | Final |

> **v2.1 date note:** The [IAB Tech Lab version-history page](https://iabtechlab.com/standards/podcast-measurement-guidelines/) lists the v2.1 release as February 2021. The [published v2.1 PDF](https://iabtechlab.com/wp-content/uploads/2021/03/PodcastMeasurement_v2.1.pdf) states “Released March 2021.” This release history uses March 2021 as the document-level release date while retaining the February 2021 listing for transparency.

---

## Unreleased — v3.0

### Status

In development. IAB Tech Lab has publicly described v3.0 as planned for public comment in the middle of 2027.

### Direction under consideration

- Move podcast measurement beyond a download-only framework.
- Address the next generation of podcast measurement, including streaming video podcasts.
- Examine richer client-side and platform signals while preserving clear distinctions between delivery, playback, exposure, audience, and outcome claims.
- Continue supporting open podcast distribution while addressing measurement differences across RSS, streaming, and platform-hosted environments.

No v3.0 requirement is final until the working group approves a public-comment draft and completes the applicable review process.

Sources:

- [Clarifying Today’s Podcast Measurement and Preparing for What Comes Next](https://iabtechlab.com/clarifying-todays-podcast-measurement-and-preparing-for-what-comes-next/)
- [Podcast Measurement Technical Guidelines](https://iabtechlab.com/standards/podcast-measurement-guidelines/)

---

## v2.3 — September 29, 2026

### Status

Final. The final version was published on September 29, 2026, following a 30-day public-comment period. IAB Tech Lab reported that no public comments required changes to the public-comment draft.

### Added

- Explicit applicability to audio and video podcasts distributed through open RSS feeds or podcast applications that rely on server-side file delivery.
- A section addressing enclosure URLs and their effect on measurement.
- Expanded invalid-traffic guidance, including examples of legitimate behavior that may be mistaken for invalid traffic.
- Guidance on verification and platform anti-fraud responsibilities.
- Three measurement-window approaches with examples:
  - Calendar-day window
  - First-touch rolling window
  - Last-touch rolling window
- Guidance for understanding and investigating measurement discrepancies.
- Sponsorship ads as a separately described advertising form.

### Changed

- Replaced general use of **listener** with **podcast consumer** where a broader term is needed to include both podcast listeners and viewers.
- Clarified the URL-prefix redirect method and how it differs from measurement based on complete first-party server logs.
- Clarified how open-RSS video formats, including HLS where applicable, fit within the server-side delivery framework.
- Expanded descriptions of common fraudulent-activity types and the standards that may be used when assessing anomalies.

### Important measurement clarification

v2.3 remains principally a server-log-based measurement framework. A valid download describes delivery to a device; it does not by itself confirm playback, listening, viewing, or advertising exposure. Client-Confirmed Ad Play remains a separate metric requiring a client-side signal.

### Publication milestones

- **July 21, 2026:** Public-comment draft released.
- **August 19, 2026:** Public-comment period closed.
- **September 29, 2026:** Final v2.3 published and moved to GitHub for easier discovery and change management.

Sources:

- [PTMG v2.3](PTM-Guidelines_v2.3.md)
- [v2.3 final publication page](https://iabtechlab.com/standards/advanced-tv/podcast-technical-measurement-guidelines-v2-3/)
- [v2.3 public-comment announcement](https://iabtechlab.com/press-releases/iab-tech-lab-releases-podcast-technical-measurement-guidelines-v2-3/)
- [Clarifying Today’s Podcast Measurement and Preparing for What Comes Next](https://iabtechlab.com/clarifying-todays-podcast-measurement-and-preparing-for-what-comes-next/)

---

## v2.2 — May 2, 2024

### Status

Final. The final PDF identifies the release as May 2024; IAB Tech Lab’s implementation announcement was published May 2, 2024.

### Added

- Patent and due-diligence disclaimer language.
- Guidance distinguishing general invalid traffic (GIVT) from sophisticated invalid traffic (SIVT).
- Documentation-of-methodology expectations for relevant measurement and anomaly-resolution practices.
- A description of fixed and rolling measurement windows and a requirement to disclose the method used.
- More formal section numbering to make requirements easier to reference.
- Broader guidance for accounting for changes in platform and device technology.

### Changed

- Clarified the difference between download measurement using a redirect or URL prefix and measurement using complete server logs at the delivery origin.
- Clarified that an advertisement may be counted as valid only when it is associated with a valid download.
- Divided the podcast measurement material into measurement-process and metric-definition sections.
- Moved podcast-player recommendations from an appendix into the main document.
- Replaced the draft’s more general Apple watchOS case-study treatment with an explicit requirement to filter duplicate Apple Watch downloads in the final version.

### Publication milestones

- **February 22, 2024:** v2.2 public-comment draft released.
- **March 23, 2024:** Public-comment period closed.
- **May 2, 2024:** Final-release implementation announcement published.
- **May 2024:** Final v2.2 PDF release date.

Sources:

- [Final PTMG v2.2 PDF](https://iabtechlab.com/wp-content/uploads/2024/02/PodcastMeasurement_v2.2_final.pdf)
- [v2.2 public-comment announcement](https://iabtechlab.com/press-releases/iab-tech-labs-podcast-technical-working-group-announces-podcast-measurement-updates-for-public-comment/)
- [Podcast Measurement v2.2 Is Ready for Implementation](https://iabtechlab.com/podcast-measurement-v2-2-is-ready-for-implementation/)

---

## v2.1 — March 2021

### Status

Final. The final PDF states “Released March 2021.” IAB Tech Lab’s current version-history page lists February 2021; see the date note in the summary table.

### Added

- Guidance for constructing useful and distinguishable user-agent strings.
- Recommendations for working with IPv6 addresses when calculating audience metrics.
- Filtering guidance for Apple watchOS user agents and automatically triggered downloads.
- Additional recommendations for podcast players and applications.

### Changed

- Clarified language throughout the guidelines.
- Replaced whitelist/blacklist terminology.
- Updated the Podcast Player Market Share section.
- Improved the IPv6 metric-calculation methodology.

### Defined metrics

v2.1 continued the common measurement vocabulary around four principal metrics:

- Download
- Listener
- Ad Delivered
- Client-Confirmed Ad Play

### Publication and maintenance milestones

- **November 2, 2020:** Initial v2.1 draft recorded in the published change log.
- **December 2, 2020:** Public-comment period opened.
- **December 31, 2020:** Public-comment period closed.
- **January 11, 2021:** Updated draft recorded, including terminology, player-market-share, and IPv6 changes.
- **February 2021:** Release month listed on the current IAB Tech Lab version-history page.
- **March 2021:** Release month printed on the final v2.1 PDF.
- **October 11, 2022:** v2.1 maintenance update recorded for yearly cadence and minor cleanup.

Sources:

- [Final PTMG v2.1 PDF](https://iabtechlab.com/wp-content/uploads/2021/03/PodcastMeasurement_v2.1.pdf)
- [v2.1 public-comment announcement](https://iabtechlab.com/press-releases/tech-lab-releases-podcast-measurement-technical-guidelines-2-1-for-public-comment/)
- [Published change log in the October 2022 compliance guide](https://iabtechlab.com/wp-content/uploads/2022/10/Podcast-Measurement-Validation-Compliance-v2.1-Oct-2022.pdf)

---

## v2.0 — December 20, 2017

### Status

Final. The final document was released in December 2017; the published change log identifies December 20, 2017.

### Added

- A four-step process for improving the accuracy of podcast measurement:
  1. Filter requests.
  2. Apply file-threshold levels.
  3. Identify and aggregate unique activity.
  4. Generate metrics.
- Expanded podcast content, audience, delivery, and advertising metric definitions.
- A minimum download threshold based on the ID3 header plus enough media to represent one minute of content, with a complete-file alternative when the threshold cannot be calculated.
- Guidance for handling HTTP requests, byte ranges, duplicate requests, bots, preloads, and play-pause-play behavior.
- Publisher-player recommendations.
- Higher-level reporting considerations at publisher, show, and episode levels.

### Changed

- Improved content-metric definitions from the initial 2016 guidelines.
- Introduced a more structured process for accurately capturing and reconciling server-log-based metrics.
- More clearly separated file delivery from confirmed playback.

### Publication milestones

- **July 12, 2017:** v2.0 public-comment draft announced.
- **August 11, 2017:** Original public-comment deadline.
- **September 8, 2017:** Extended public-comment deadline shown in the published draft.
- **December 20, 2017:** Final v2.0 release recorded in the change log.

Sources:

- [Final PTMG v2.0 PDF](https://iabtechlab.com/wp-content/uploads/2017/12/Podcast_Measurement_v2-Dec-20-2017.pdf)
- [v2.0 public-comment announcement](https://www.iab.com/news/podcast-measurement-release/)
- [v2.0 public-comment draft](https://iabtechlab.com/wp-content/uploads/2016/07/Podcast-Measurementv2.0.pdf)

---

## v1.0 — September 6, 2016

### Status

Final. Originally published as the **IAB Podcast Ad Metrics Guidelines**.

### Initial scope

- Introduced common practices for measuring podcast content and advertising delivery using server logs.
- Described downloaded and progressively downloaded podcast delivery.
- Described integrated and dynamically inserted podcast advertisements.
- Introduced filtering concepts for server-log analysis.
- Defined foundational content, advertising, and audience metrics.
- Included example formulas for unique media-file requests, partial downloads, and completed downloads.
- Established a shared measurement vocabulary intended to reduce discrepancies among podcast publishers, distributors, advertisers, and agencies.

### Publication milestone

- **September 6, 2016:** Initial guidelines released.

Source:

- [IAB Podcast Ad Metrics Guidelines — September 2016 PDF](https://www.iab.com/wp-content/uploads/2016/09/Podcast-Metrics_September_2016.pdf)

---

## Maintaining this file

For future releases:

1. Add the new version above the previous final release.
2. Record public-comment opening and closing dates separately from the final publication date.
3. Summarize normative additions, changes, clarifications, and removals.
4. Link to the specification, announcement, and final publication page when available.
5. Preserve known date discrepancies with an explanatory note instead of silently selecting one source.
6. Keep compliance-program changes separate unless they directly change the published measurement guidelines.

## Historical source index

- [Current PTMG repository](https://github.com/IABTechLab/Podcast-Technical-Measurement)
- [IAB Tech Lab PTMG resources and version history](https://iabtechlab.com/standards/podcast-measurement-guidelines/)
- [PTMG v2.3 final](PTM-Guidelines_v2.3.md)
- [PTMG v2.2 final PDF](https://iabtechlab.com/wp-content/uploads/2024/02/PodcastMeasurement_v2.2_final.pdf)
- [PTMG v2.1 final PDF](https://iabtechlab.com/wp-content/uploads/2021/03/PodcastMeasurement_v2.1.pdf)
- [PTMG v2.0 final PDF](https://iabtechlab.com/wp-content/uploads/2017/12/Podcast_Measurement_v2-Dec-20-2017.pdf)
- [PTMG v1.0 final PDF](https://www.iab.com/wp-content/uploads/2016/09/Podcast-Metrics_September_2016.pdf)

