# Podcast Technical Measurement Guidelines

![IAB Tech Lab](https://drive.google.com/uc?id=10yoBoG5uRETSXRrnJPUDuONujvADrSG1)

The IAB Tech Lab Podcast Technical Measurement Guidelines (PTMG) provide a common technical framework for measuring podcast downloads, audiences, and advertising delivery. The guidelines are intended to promote consistent measurement and clearer communication among podcast publishers, creators, hosting providers, measurement vendors, platforms, advertisers, and agencies.

## Current Release

**Podcast Technical Measurement Guidelines v2.3** is the current published version.

[Read PTMG v2.3](./PTM-Guidelines_v2.3.md)

Version 2.3 applies to audio and video podcasts distributed through open RSS feeds or podcast applications that rely on server-side file delivery. It explains how server-log data should be filtered and aggregated to produce comparable content delivery, audience, and advertising metrics.

## What Is New in v2.3

Version 2.3 strengthens the existing download-based measurement framework by:

- Clarifying applicability to both audio and video podcasts.
- Using **podcast consumer** as the broader term for podcast listeners and viewers.
- Explaining URL-prefix measurement and the differences between redirect measurement and first-party server-log measurement.
- Adding guidance on how changes to RSS enclosure URLs can affect downloads and reporting.
- Expanding invalid traffic guidance and describing platform anti-fraud responsibilities.
- Defining calendar-day, first-touch rolling, and last-touch rolling measurement windows.
- Providing additional guidance for understanding and investigating measurement discrepancies.

## What the Guidelines Measure

PTMG v2.3 defines technical processes and metrics for:

- **Podcast content delivery**, including valid downloads.
- **Podcast audience**, using disclosed methods for identifying and aggregating unique podcast consumers.
- **Podcast ad delivery**, including Ad Delivered and Client-Confirmed Ad Play metrics.
- **Filtering and validation**, including file thresholds, duplicate removal, HTTP request handling, IPv6 treatment, invalid traffic, and technology-driven anomalies.

### Download Does Not Mean Playback

Most open podcast distribution environments do not provide publishers with consistent client-side playback signals. As a result, PTMG primarily relies on filtered server logs to determine what content or advertising was delivered to a device.

A valid download does not confirm that the podcast consumer played the episode, and an Ad Delivered metric does not necessarily confirm that the ad was heard or viewed. When a player can send a client-side tracking signal, the guidelines define **Client-Confirmed Ad Play** as a separate metric.

## Who Should Use These Guidelines

The guidelines are relevant to organizations across the podcast ecosystem, including:

- Podcast publishers and creators.
- Podcast hosting and monetization platforms.
- Measurement and analytics providers.
- Podcast applications and playback platforms.
- Advertisers, agencies, and other buyers of podcast advertising.

Organizations that generate or use podcast measurement reports should review the complete specification and clearly disclose their measurement methodology.

## Repository Contents

| Path | Description |
| --- | --- |
| [`PTM-Guidelines_v2.3.md`](./PTM-Guidelines_v2.3.md) | Published Podcast Technical Measurement Guidelines v2.3. |
| [`images/2.3/`](./images/2.3/) | Images referenced by the v2.3 specification. |

## Compliance Program

The guidelines inform the IAB Tech Lab Podcast Measurement Compliance Program, but the compliance program is administered separately from the Podcast Technical Working Group and this repository.

- [Podcast Measurement Compliance Program](https://iabtechlab.com/compliance-programs/podcast-measurement-compliance/)
- [Compliant Companies](https://iabtechlab.com/compliance-programs/compliant-companies/#podcast)

Publication of an implementation or methodology in this repository does not by itself indicate IAB Tech Lab compliance or certification.

## Working Group and Support

PTMG is developed and maintained by the IAB Tech Lab Podcast Technical Working Group in partnership with industry participants across the podcast ecosystem.

- [Podcast Technical Working Group](https://iabtechlab.com/working-groups/podcast-technical-working-group/)
- [Podcast Measurement Guidelines and Resources](https://iabtechlab.com/standards/podcast-measurement-guidelines/)
- Questions and feedback: [support@iabtechlab.com](mailto:support@iabtechlab.com)

The Working Group will continue evaluating future podcast measurement requirements, including measurement approaches that go beyond downloads as richer client-side and platform signals become available.

## About IAB Tech Lab

The IAB Technology Laboratory is a nonprofit research and development consortium that develops global technical standards and solutions for the digital advertising ecosystem. Learn more at [iabtechlab.com](https://iabtechlab.com/).

© 2026 IAB Tech Lab
