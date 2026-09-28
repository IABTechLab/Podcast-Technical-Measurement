![IAB Tech Lab](https://drive.google.com/uc?id=10yoBoG5uRETSXRrnJPUDuONujvADrSG1)
# Podcast Technical Measurement Guidelines

Version 2.3

© 2026 IAB Tech Lab

## About This Document

The IAB Tech Lab Podcast Technical Measurement Guidelines was developed to address measurement of downloaded media and the ads included in those downloads. Companies can apply for compliance with these guidelines, but compliance details are defined separately. Visit https://iabtechlab.com/compliance-programs/ to learn more.

## About IAB Tech Lab

The IAB Technology Laboratory is a nonprofit research and development consortium charged with producing and helping companies implement global industry technical standards and solutions. The goal of the Tech Lab is to reduce friction associated with the digital advertising and marketing supply chain while contributing to the safe growth of an industry. The IAB Tech Lab spearheads the development of technical standards, creates and maintains a code library to assist in rapid, cost-effective implementation of IAB standards, and establishes a test platform for companies to evaluate the compatibility of their technology solutions with IAB standards, which for 18 years have been the foundation for interoperability and profitable growth in the digital advertising supply chain. Further details about the IAB Technology Lab can be found at https://iabtechlab.com.

### IAB Tech Lab lead

Brad Pipkin, Director of Product - Advanced TV

### Disclaimer

IAB TECHNOLOGY LABORATORY, INC. (“IAB TECH LAB”) PROVIDES THESE GUIDELINES AS A PRACTICAL GUIDE AND RESOURCE FOR GENERAL INFORMATION.  PLEASE BE AWARE THAT THESE GUIDELINES DO NOT CONSTITUTE LEGAL ADVICE, AND IF YOU HAVE ANY LEGAL QUESTIONS, PLEASE CONSULT YOUR ATTORNEY.  WHILE IAB TECH LAB HAS MADE EFFORTS TO ASSURE THE ACCURACY OF THE MATERIAL IN THESE GUIDELINES, THEY SHOULD NOT BE TREATED AS A BASIS FOR FORMULATING BUSINESS AND LEGAL DECISIONS WITHOUT INDIVIDUALIZED LEGAL ADVICE.

IAB TECH LAB MAKES NO REPRESENTATIONS OR WARRANTIES, EXPRESS OR IMPLIED, AS TO THE COMPLETENESS, CORRECTNESS, OR UTILITY OF THE INFORMATION CONTAINED IN THESE GUIDELINES AND ASSUMES NO LIABILITY OF ANY KIND WHATSOEVER RESULTING FROM THE USE OR RELIANCE UPON THEIR CONTENTS.  PLEASE BE ADVISED THAT: (I) ONE OR MORE OF THE MEASUREMENT PROCESSES DESCRIBED HEREIN MAY BE SUBJECT TO PATENTS; (II) IAB TECH LAB HAS PERFORMED NO DILIGENCE AND HAS NOT ANALYZED THE VALIDITY OF ANY OF THESE PATENTS; (III) IAB TECH LAB IS NOT PROMULGATING ANY STANDARDS OR SPECIFICATIONS UNDER THESE GUIDELINES; AND (IV) PRIOR TO IMPLEMENTING ANY MEASUREMENT PROCESSES DESCRIBED HEREIN, YOU ARE SOLELY RESPONSIBLE FOR CONDUCTING ANY SUCH DILIGENCE AND ANALYSES AND/OR LICENSING ANY NECESSARY PATENTS.

Please contact support@iabtechlab.com if you have any questions or comments about this document. This document and other related resources can be found on the IAB Tech Lab website at:  https://iabtechlab.com/standards/podcast-measurement-guidelines/

## Contributing Member Companies

The IAB Podcast Measurement Technical Guidelines document was developed by the IAB Tech Lab Podcast Technical Working Group, in partnership with the IAB Audio Committee. The following IAB Tech Lab member companies contributed to the update of this document:

- A+E Networks
- Acast
- ACPM
- Ad Results Media
- Adelaide
- AdLarge Media
- AdsWizz
- Algorix
- ART19
- Audacy
- Audio Alliance GmbH
- Audion
- Audit Bureau of Circulations (ABC) UK
- Barometer
- Barstool Sports
- CBC Radio Canada
- Centillion
- Chartable
- Dailymotion
- Doceree
- DoubleVerify
- Epsilon
- ESPN
- Experian Marketing Services
- Extreme Reach
- Global Media & Entertainment
- Google LLC
- GroupM US
- Hearst
- Hubhopper
- IAB Germany
- IAB Tech Lab
- IAB UK
- iHeartMedia
- Julep Media GmbH
- Jun Group
- SIFO Fifty5Blue
- Katz Media Group
- Kinesso
- Libsyn
- Lucid
- Magellan AI
- Media.net Advertising FZ LLC
- National Public Media
- NBCUniversal
- New York Public Radio
- News UK
- Nexxen
- Nielsen
- Nova Entertainment
- NPR
- Omny Studio
- Oracle Advertising & Customer Experience
- Paramount
- Podigee GmbH
- Podscribe
- Podtrac
- Protected Media
- Publicis Media
- Pyler Co., Ltd
- RawVoice
- Rebel Base Media
- Remixd
- ResponsiveAds
- SiriusXM Media
- Slate
- Sony Music Entertainment
- Sounder
- Sounds Profitable
- Soundstack
- Spotify
- Spreaker
- StackAdapt
- The Daily Wire
- The Inquirer
- The New York Times Company
- The Trade Desk
- TripleLift
- Triton Digital
- Veritonic
- VRTCAL
- Warner Bros. Discovery
- Westwood One
- WideOrbit
- Xaxis

A list of current members subscribed to the Podcast Technical Working Group can be found at https://iabtechlab.com/working-groups/podcast-technical-working-group/

## Table of Contents

- [1. Executive Summary](#1-executive-summary)
  - [1.1 About Compliance](#11-about-compliance)
  - [1.2 Who Should Read These Guidelines?](#12-who-should-read-these-guidelines)
  - [1.3 About this Version](#13-about-this-version)
- [2. Overview](#2-overview)
  - [2.1 The Advantage of Podcast Syndication](#21-the-advantage-of-podcast-syndication)
  - [2.2 Scope](#22-scope)
  - [2.3 Out-of-Scope](#23-out-of-scope)
- [3. The Podcast Medium - Content Delivery](#3-the-podcast-medium--content-delivery)
  - [3.1 Downloaded Podcasts](#31-downloaded-podcasts)
  - [3.2 Progressively Downloaded Podcasts](#32-progressively-downloaded-podcasts)
    - [3.2.1 Raw Server Logs for Progressive Downloads](#321-raw-server-logs-for-progressive-downloads)
- [4. The Podcast Medium - Ad Delivery](#4-the-podcast-medium--ad-delivery)
  - [4.2 Integrated Ads](#42-integrated-ads)
  - [4.3 Dynamically Inserted Ads](#43-dynamically-inserted-ads)
  - [4.4 Sponsorship Ads](#44-sponsorship-ads)
- [5. Podcast Measurement Process](#5-podcast-measurement-process)
  - [5.1 Measurement with Server Logs](#51-measurement-with-server-logs)
  - [5.2 Measurement Using a URL Prefix](#52-measurement-using-a-url-prefix)
  - [5.3 Enclosure URLs and Measurement](#53-enclosure-urls-and-measurement)
  - [5.4 Invalid Traffic](#54-invalid-traffic)
    - [5.4.1 Valid Traffic Mistaken for IVT](#541-valid-traffic-mistaken-for-ivt)
    - [5.4.2 Verification and Platform Anti-Fraud Responsibilities](#542-verification-and-platform-anti-fraud-responsibilities)
  - [5.5 Recommended Process for Measurement](#55-recommended-process-for-measurement)
    - [5.5.1 Measurement Windows](#551-measurement-windows)
    - [5.5.2 Step 1: Filtering](#552-step-1-filtering)
    - [5.5.3 Step 2: Apply File Threshold Levels](#553-step-2-apply-file-threshold-levels)
    - [5.5.4 Step 3: Identify and Aggregate Uniques](#554-step-3-identify-and-aggregate-uniques)
    - [5.5.5 Step 4: Generate Metrics](#555-step-4-generate-metrics)
    - [5.5.6 Step 5: Audit the Process](#556-step-5-audit-the-process)
  - [5.6 Understanding Discrepancies](#56-understanding-discrepancies)
- [6. Podcast Metric Definitions](#6-podcast-metric-definitions)
  - [6.1 Podcast Content Delivery Metric Definitions](#61-podcast-content-delivery-metric-definitions)
  - [6.2 Podcast Audience Metric Definitions](#62-podcast-audience-metric-definitions)
  - [6.3 Podcast Ad Metric Definitions](#63-podcast-ad-metric-definitions)
  - [6.4 Higher Level or Advanced Metrics](#64-higher-level-or-advanced-metrics)
- [7. Podcast Player Recommendations](#7-podcast-player-recommendations)
  - [7.1 Agent Structure](#71-agent-structure)
- [8. A Use Case in Changing Technology](#8-a-use-case-in-changing-technology)
  - [8.1 Apple watchOS Duplicate Downloads](#81-apple-watchos-duplicate-downloads)
  - [8.2 Accounting for Changes in Technology](#82-accounting-for-changes-in-technology)
- [9. In Closing](#9-in-closing)

## 1. Executive Summary

Podcast audiences represent a growing segment of effective marketable media. Podcast ad revenues were expected to reach over $4 Billion in 2025—more than double posted revenues in 2022--according to the IAB Podcast Advertising Revenue Study conducted by PwC US and posted May 2023. Podcasts offer advertisers hyper-focused audiences that remain attentive even during ads. Podcast consumers have been shown to be the most loyal and engaged audience of any digital medium.

The stakes for revenue in podcasting are growing, and the need to attract buyers will become more competitive over time. To foster a fair market for podcast businesses, IAB Tech Lab and the Podcast Technical Measurement Working Group developed and maintains guidelines for metrics used in podcasting.

Measuring performance in podcast advertising is unique in the market of digital advertising. Podcast episodes, traditionally released as audio files but increasingly as both audio and video files, are downloaded by podcast consumers for consumption and measurement is based on server logs. This is in contrast to other digital mediums that typically maintain an open connection between a consumer’s device and the content server. This nuance produces different metrics in podcast advertising.

The challenge for podcast producers and distributors is to offer buyers a set of metrics that is consistently defined and measured equally across the podcast medium. This document provides an overview of ad delivery in podcasting and describes the technical process for measuring: downloads, audience, and ad delivery. IAB Tech Lab also offers a compliance program for companies who wish to signal to buyers their adherence to these guidelines.

With a consistent set of podcast advertising metrics, buyers and sellers can engage in a conversation about campaign strategy with confidence.

### 1.1 About Compliance

This document informs the Podcast Compliance Program provided by IAB Tech Lab. However, because the Podcast Technical Measurement Working Group defines these guidelines, and because many of the member companies go through the compliance process, the Compliance Program must be defined separately to gain the trust of buyers and meet basic expectations for third-party certification.

To learn more about Tech Lab’s Compliance Program, visit: https://iabtechlab.com/compliance-programs/podcast-measurement-compliance/

For a list of compliant podcast companies, visit: https://iabtechlab.com/compliance-programs/compliant-companies/#podcast

### 1.2 Who Should Read These Guidelines?

While all professionals in the podcast supply chain can benefit by being familiar with this document, metric definitions are primarily intended for podcast producers and distributors who provide measurement services. Specifically, account managers should be familiar with and use metrics as defined in this document when negotiating ad packages with buyers. Additionally, publishers and podcast hosting platforms should use the metric definitions in this document to design or adjust the ad measurement technology they use to analyze server logs for podcast ad measurement. Podcast creator organizations should also familiarize themselves with these guidelines to understand how ad measurement for their content is accomplished when they partner with a compliant podcast publishing service.

Buyers should also reference this document to better understand how ads placed in podcast content are counted. This document offers a set of metrics that establish a mutual understanding in podcast advertising negotiations.

### 1.3 About this Version

The first version of this document was released in September 2016. Additional significant updates were made with version 2.0 released in December 2017. Updates in version 2.1, released in 2021, included language edits for more clarity, a new section with guidance on user agent structure, recommendations for IPv6 IP addresses, filtering guidance for Apple watchOS user agents, and a number of additional podcast player recommendations.

#### Updates in version 2.3 (this version)

- Clarified this document covers video when distributed via open RSS feeds or podcast applications that rely on server-side file delivery
- Replace the term “listener” with “podcast consumer” to describe both listeners (audio) and viewers (video) of podcasts
- Describes prefix URL redirect method in section 5.2 to help understand discrepancies
- Section 5.2 describes Enclosure URLs in RSS feed servers and their impact on measurement
- Section 5.4 describes common fraudulent activity types and existing standards to further assess anomalies which may be legitimate activities
- Section 5.5.1 describes three measurement window types used in counting downloads and demonstrates with examples how they are applied for measurement

## 2. Overview

Podcast content is an on-demand audio or video format that consumers either stream progressively or download to consume online or later. Unlike the streaming format more common in video, podcasts continue to be downloadable because of the convenience offered by existing platform and application functionality.

Despite the use of the word “streaming” in podcasting, "streamed" podcast files are progressively downloaded via the standard HTTP protocol.

The delivery of a streamed podcast is logged the same way as a downloaded file in the server logs. This important distinction impacts the ability to measure content and ad delivery in real-time without access to client-side analytics. Podcast publishers must work around this limitation and track metrics using server log data.

### 2.1 The Advantage of Podcast Syndication

Podcast consumption relies on and benefits from a fragmented ecosystem. This fragmentation allows consumers to access podcasts wherever they want - with any podcast app or on websites offering podcasts. Podcast creators and advertisers benefit by being able to reach a larger audience compared to an ecosystem limited to only one place of consumption.

The ability to track podcast content and ad playback largely depends on the player requesting the episode. Podcast aggregator apps, like Apple Podcasts and Spotify, typically do not send playback data to publishers. Host-branded players (players owned by the podcast producers) can provide playback data for podcasts consumed using their branded app; however, this playback data represents limited reach because the majority of podcast consumers prefer aggregator apps over host-branded ones.

Despite the limitations, podcast audiences are growing and offer valuable exposure for marketers. In order to offer this value to buyers, metrics must be consistently defined across the industry. IAB Tech Lab collaborates with the podcasting community to establish and maintain metric definitions that can be used consistently in the podcast marketplace.

Establishing consensus and clarity for podcast reporting metrics improves communication and establishes trust and accountability with buyers.

### 2.2 Scope

This document defines content, ad, and audience metrics in the context of downloaded podcasts whether saved for later consumption or consumed while being downloaded. In this context, both formats are typically pre-recorded and available on demand whenever the podcast consumer is ready to access the files.

For the sake of establishing common ground in tracking podcast performance, the definitions presented in this document focus on counting ad delivery in downloaded and progressively downloaded podcast episodes. This count comes from analyzing server logs to determine what was actually delivered.

#### Video Podcast Applicability

For the avoidance of doubt, the guidelines defined in this document apply to **both audio and video podcast episodes** when distributed via open RSS feeds or podcast applications that rely on server-side file delivery.

Video podcasts delivered as MP4 files or via segmented streaming formats (e.g., HTTP Live Streaming/HLS) through podcast distribution mechanisms are subject to the same measurement principles, filtering requirements, and metric definitions described herein, unless explicitly stated otherwise.

### 2.3 Out-of-Scope

Podcasts using true streaming technology can provide real-time or near real-time tracking through client-confirmed ad delivery. While these implementations generally do not support impression-level viewability metrics, they do enable validated counting of consumer activity, including podcast consumption sessions and downloads generated through true streaming. As adoption of true streaming continues to grow, we expect to address measurement standards for these delivery methods more directly in future versions of the Podcast Technical Measurement Guidelines.

Additional Measurement guidance for true streaming audio is covered in the MRC [Audio Measurement Guidelines](https://www.mediaratingcouncil.org/sites/default/files/Standards/Digital%20Audio%20Measurement%20Standards%20-%20Final%20Version%201.0.pdf) released January 2018. The percentage of market share for true streaming apps may be changing and a well-rounded analysis of podcast measurement includes metrics for ad delivery in a medium with limited client-confirmed playback data.

## 3. The Podcast Medium – Content Delivery

Podcast consumers acquire podcast episodes in one of two ways: either by downloading the episode for later consumption (downloaded), or by consuming the podcast while the episode is downloaded (progressively downloaded). Note that Video or Audio delivery via HLS is also a form of progressive download and is therefore covered by these guidelines.

Delivery methods for downloaded episodes, whether consumed later or during download, offer valuable inventory to advertisers, but content and ad delivery are handled differently in both environments. An overview of each format is explained in the following paragraphs. Despite different tracking capabilities in each environment, a few baseline metrics are able to offer similar reports for both podcast types.

### 3.1 Downloaded Podcasts

Audio or Video Podcast downloading allows podcast consumers to download full episodes of content that can be played at a later date and time. Podcast consumers may subscribe to select programs, and platforms like Apple Podcasts continue to support full downloads to a personal library for consumption offline at any time in the future. The convenience of this system makes downloaded podcasts a continued preference among podcast consumers.

### 3.2 Progressively Downloaded Podcasts

These podcasts appear to be streamed, but the episode is actually being downloaded whilst it is being consumed. The downloaded episode is stored in a temporary location rather than to a library as with a downloaded podcast. Since progressively downloaded episodes are typically downloaded the same way as the episodes stored for later listening, delivery for these two formats is recorded the same way in the server logs. The only difference between the two is whether the podcast consumer is actively playing the episode as it is downloaded, or it is being saved for later consumption. This distinction can typically only be discerned by the player. Note that this is valid for any formats, inclusive of video podcasts consumed via HLS.

#### 3.2.1 Raw Server Logs for Progressive Downloads

In a downloaded episode, segments of each file associated with that episode are collected on the podcast consumer’s device, or progressively downloaded. These progressively downloaded files result in a server log with several requests to the server, which must then be analyzed and filtered from other server requests in order to represent how many individual episodes were downloaded and to what audiences. When podcast publishers use a consistent process, metrics can be reported and trusted with a high level of confidence.

## 4. The Podcast Medium – Ad Delivery

Podcast ads can be delivered and tracked in a variety of different ways, but in general two different methods are used with variations on each.

### 4.2 Integrated Ads

Historically, podcast ad campaigns often involved ads that were read by the podcast host or a familiar voice. A static ad or jingle may also be included as part of the episode. These ads are part of the content and included, or “baked-in,” with the episode that is downloaded. Targeting is limited because everyone who downloads the episode gets the same ads.

### 4.3 Dynamically Inserted Ads

Ad technology allows for ads to be targeted and dynamically inserted at the time of episode request (rather than recorded directly into the audio or video file). The ad server determines the best ad to serve to the podcast consumer at the time of request. In a podcast consumed online, ads may be inserted into a file that is being progressively downloaded at designated times (ad breaks).

### 4.4 Sponsorship Ads

Ads that directly sponsor a podcast episode have typically been host-read, or integrated as described in 4.2 above. However, with today’s ad technology and business models, sponsorships can be dynamically inserted as described in 4.3.

## 5. Podcast Measurement Process[^1]

Most players that initiate a podcast download (client) send no information about playback, which is in contrast to other IP-connected mediums that rely on client signals to confirm the ad was received. In these podcast measurement guidelines, an ad play is calculated based on server logs that provide information about what was served.

### 5.1 Measurement with Server Logs

In order to produce accurate counts for podcast downloads and ads, podcast hosting, measurement, and monetization, companies must analyze server logs. These server logs may include file requests for a combination of downloaded podcast episodes/files, dynamically inserted ads, and any content requested by the web page or application hosting the player. HTTP GET requests usually contain the following data:

- **IP Address** - The IP address is one of the factors that may be used to determine if the request is unique or a duplicate, except when the IP address is of known corporate offices, dorms, and other IP-connected setups that have a large number of people sharing one IP address. The IP address is also used to determine geographical information on where the podcast is downloaded. Both IPv4 and IPv6 IP formats are accounted for in measurement data outlined in this guidance.
- **Time Stamp** - The date and time is used to define a measurement window (as described in the Measurement Windows section of  this document) in which downloads are filtered for duplicates.
- **HTTP Status Code** - The appropriate HTTP status code is examined to determine if the request should be counted.
- **Bytes Served** - only available in native server logs, the bytes served value may be used to determine how much of the podcast was downloaded.
- **Referrer** - The origin of the download, if available.
- **User Agent** - The identifier for the app or service consuming the media, which helps to determine if the download request is unique.
- **Byte Range** - The range of bytes requested in a given request, used to determine what portion of the media is requested. A low byte range may signal a pre-download which is excluded from valid counts.

When analyzed across multiple requests, filtered log data offers statistics that represent podcast downloads, audience and ad delivery. Since media technology is always changing, no specific combination of factors or techniques will offer the most accurate count indefinitely. However, meeting some minimum requirements and following some best practices will help produce more consistent results across providers and platforms.

This guidance outlines best practices for filtering server logs for measurement and defines specific metrics for podcast content measurement, audience measurement, and ad measurement. Podcast producers and distributors may include additional metrics beyond the ones defined here, but such additional metrics should be labeled separately from the core list of IAB Tech Lab metrics.

### 5.2 Measurement Using a URL Prefix

Measurement can be done by appending a prefix to the download URL, collecting most of the data elements listed above for the GET requests, and counting how many times that prefix was used to trigger a download. This method of measurement tracks the download request, but not the server response.

For example, a prefix measurement vendor may not be able to discern how much of the file was downloaded because it can’t directly gather data on how many bytes were consumed. The vendor may be able to obtain this information from other sources, but the results will vary from measurement using filtered server log data that include bytes served.

Validation of this measurement method is distinct from working with podcast hosting platform server logs. For example, partial download removal might be accomplished by comparing prefix measurement counts to server log data from either the vendor’s own first-party server logs or a partner’s first-party server logs.

The diagram below maps out how prefix measurement is executed. While each third-party measurement vendor may handle their process a little differently, the diagram below represents how a download request moves from a user’s device through the two platforms. Each step holds the potential for recording slightly different details.

[IMAGE: URL Prefix Measurement Process Diagram]

1. **Initial Request to Redirect Measurement Platform:**

When a podcast episode is requested, the initial download request is routed through a measurement server using a prefix on the URL for the media file. This redirect server logs the request for analytics purposes but typically does not access the actual media file. A download URL may contain multiple prefixes which sends the request to multiple servers.

2. **Redirect Platform records request details:**

The redirect platform logs the request. Since the redirect server doesn’t store the media files, it estimates details about the file to be downloaded using other methods.

3. **Redirect instructions sent to user device:**

After logging the request, the measurement server redirects the user device to the host server where the media file is stored.   From this point, depending on device/player behavior, subsequent partial requests may bypass the prefix and request the remainder of the file directly from the hosting platform.  In these cases, the Redirect Measurement Platform will not have access to the remaining requests, or the bytes requested.  This creates a challenge in consistently confirming that the first minute of content has been requested.

4. **Device sends request to Host Platform:**

The device now sends a request to the host server for the media file. If the original request that included the prefix was only a partial download, the user device may bypass the redirect service to complete the download. The rest of this process happens the same way a direct request to the host server works.

5. **Download details recorded:**

The host platform then records details about the request and the file sent.

6. **Requested file sent to user device:**

The host platform then facilitates the download of the media file to the end-user's device. The host server only knows details about what is sent to the device. No confirmation is sent to the host server about how the file was used.

### 5.3 Enclosure URLs and Measurement

In the podcast ecosystem, the enclosure URL in an RSS feed serves as a key pointer to the episode’s media file. Changes to the URL—such as adding, modifying, or removing a prefix—can unintentionally disrupt measurement.

#### Common Impacts

- **Duplicated Downloads:** Some podcast players interpret a changed URL as a new episode, prompting a re-download—even if the content hasn't changed. For example, switching from `//hostingplatform.com/123.mp3` to `//prefixplatform.com/123.mp3` can trigger a new download.
- **Inflated Metrics:** Re-downloads result in duplicated download events across both the prefix and hosting platforms, potentially skewing campaign reporting.
- **Recurring Re-downloads:** Each subsequent URL change (e.g., changing prefixes again or reverting) can trigger another download, amplifying the issue.

While most publishers maintain consistent URL structures, any variation can propagate unintended effects through the ecosystem.

**Best Practice:** Avoid changing episode GUIDs during hosting changes. If possible, also avoid changing episode titles and publication dates, as different podcatchers use different heuristics for determining if an episode is the same as one previously encountered.

### 5.4 Invalid Traffic

In podcasting, downloads generated by bots or other systems that will not be consumed by a human are considered invalid traffic. In all advertising mediums, invalid traffic (IVT) can be broken down into two categories: General Invalid Traffic (GIVT) and Sophisticated Invalid Traffic (SIVT).

GIVT is generated by crawlers (bots, spiders, etc.), known data centers, pre-fetching, and other general routine practices that can be easily filtered from logged data using common practices and technology that identifies this.

SIVT, on the other hand, is intended to look like human traffic. This kind of traffic is generated using hijacked devices, bots designed to mimic human traffic, by manipulating data, or using other technology and tactics to generate false audiences for advertising. The public version of this guideline will not offer specific guidance on what to filter because the organizations generating this kind of IVT might use it to adjust their strategies. That said, measurement organizations should implement practices that look for anomalies in the data and address them as appropriate.

Valid measurement outlined in this document includes filtering recommendations aimed at minimizing invalid traffic. While more data is needed to set specific thresholds for measurement compliance, the filtering guidance offered here will catch most GIVT and some of the more obvious SIVT. Companies trying to catch more SIVT can look to additional resources and services for a higher level of accountability to their customers and partners.

Operations set up to fabricate traffic sell inventory that is never exposed to humans. This intentional act is fraudulent, regardless of how it’s implemented.

One key indicator for campaigns that run through any kind of fabricated traffic is that they're almost completely ineffective. Measured on reach alone, effectiveness might look promising, but measuring on conversions or ROI will produce little to no results, likely leading to advertisers abandoning the show.

#### 5.4.1 Valid Traffic Mistaken for IVT

Not all anomalies are fraudulent. Some legitimate podcast consumer behavior or platform-specific quirks can be mistaken for invalid traffic (IVT), resulting in undercounting and inconsistent audience metrics. The podcast medium - unlike streaming or web-based media - relies heavily on download behavior with limited visibility into client-side playback. This nature limits what can be measured in terms of playback. Verify if your IVT system accommodates podcasts.

#### 5.4.2 Verification and Platform Anti-Fraud Responsibilities

Podcast verification depends on cooperation across the supply chain, but podcast player platforms are often best positioned to support anti-fraud practices because they control the environment where podcast files are requested, downloaded, cached, and consumed.

Podcast publishers, hosting providers, measurement vendors, and buyers should work directly with podcast player platforms to understand which verification signals and IAB Tech Lab anti-fraud practices are supported. Platform support may vary by app, device, playback model, and business relationship.

Common practices include **ads.txt/app-ads.txt** for authorized seller transparency and **Open Measurement** for supported client-side ad verification environments. Readers should refer to the IAB Tech Lab website for current guidance, specifications, and compliance resources for each standard.

- ads.txt/app-ads.txt -  https://iabtechlab.com/ads.txt/
- Open Measurement - https://iabtechlab.com/standards/open-measurement-sdk/

### 5.5 Recommended Process for Measurement

While we have made the effort to be specific with our guidance on filtering server log data for measurement, publishers and distributors will have to consider best practices to align with their circumstances. For certification, metrics providers must support the process outlined in this document to the best of their ability, or follow a process with a similar or more stringent level of analysis, disclose the options selected, disclose where they diverge from the guidance in this document, and provide the rationale or explain the circumstances that drove those decisions.

https://iabtechlab.com/compliance-programs/compliant-companies/#podcast

We recommend a 5-step process to generating metrics using server-side log analysis.

1. Apply filtering logic
2. Apply file threshold logic
3. Identify and aggregate uniques
4. Generate metrics
5. Audit the process (feedback loop)

#### 5.5.1 Measurement Windows

The previous version of the Podcast Measurement Guidelines (v2.2) made reference to a rolling 24 hr window as compared to a calendar day (fixed) window; however, the difference between these options is not stated clearly, and there are two interpretations of “rolling”. In this appendix, we offer the following explanation.

A **calendar day (fixed) measurement window** resets at a fixed time (e.g., 12:00am UTC) each day. Download requests which fall on the same calendar day are **not** counted as a new download. A subsequent download request on the next calendar day should be counted as unique.

A **“first touch” rolling measurement window** is a time period (typically a 24 hr period) that begins at the timestamp of a qualifying download request (based on IP address and user agent) and is used to evaluate whether subsequent download requests from the same source should be counted as unique.

A **“last touch” rolling measurement window** is a time period that extends and resets the measurement window based on subsequent requests. Thus, when a subsequent download occurs within the time period, the measurement window is extended. If the subsequent download occurs after the time period, it is counted as unique.

#### Example

- A podcast consumer downloads an episode **at 10:00 PM on** Monday.
- A second download of the same episode from the same IP and user agent at **3:00 AM** on Tuesday counts as a download for the calendar window because it’s on a different day. A download is not counted for either rolling window. For the “last touch”  window, it begins a new 24-hr period.
- A third download from the same IP and user agent at **10:15 PM** Tuesday does not count as another download for the calendar window. It counts as a download for the “first touch” rolling window as it’s over 24 hours from the initial 10:00 PM Monday download. For the “last touch” window, a download **would NOT be counted,** as it occurs within the 24-hour window that reset at 3:00 AM Tuesday. This also resets a new window beginning at **10:15 PM** on Tuesday.
- A fourth download from the same IP and user agent at **11:15 PM** Wednesday **would be counted,** in all cases as it occurs outside the latest 24-hour window.

| Request Time | Calendar | Rolling | Extending |
| --- | ---: | ---: | ---: |
| 1) 10:00 PM Monday | 1 | 1 | 1 |
| 2) 3:00 AM Tuesday | 1 | 0 | 0 |
| 3) 10:15 PM Tuesday | 0 | 1 | 0 |
| 4) 11:15 PM Wednesday | 1 | 1 | 1 |

Choice of windowing algorithm provides flexibility in measurement and can be useful for systems that do not align with fixed calendar boundaries. Implementers must consistently apply the rolling window logic to ensure accurate and comparable measurement results.

#### 5.5.2 Step 1: Filtering

All requests that should not be counted for any reason should be filtered out up front. The criteria we have identified for filtering are listed below.

#### Step 1.1: Eliminate Pre-Load Requests

Pre-loading of podcasts directly results in podcast downloads being counted when they should not. There are two possible solutions to handle this.

- Policy put in place to not allow preloading in players and on websites (e.g. preload=none for HTML5)
- Use a download threshold based on one minute of content, excluding any data used for headers or other information, to eliminate downloads that were more likely caused by pre-loading or accidental plays.  (see Step 2 **“Apply file threshold levels”** below)

Look for evidence of pre-loading in the logfile data. If found, try to identify the source of the pre-loading, then contact the business responsible and ask them to correct the behavior.

#### Step 1.2: Eliminate Potential Bots and Bogus Requests

A number of scenarios include requests that should not be counted because they likely come from bots or from systems designed to mimic human behavior for downloads. This step is a first defense against general invalid traffic.

Metrics providers must filter out the following:

1. IP addresses that account for a large number of downloads in the measurement window used by the metrics provider. Large numbers of downloads that represent an unrealistic number of downloads for a single podcast consumer should be examined for potential fraud. (But also look at the safe IP addresses note below.)
2. IP addresses that are identified from sources that are not actual podcast consumers, such as requests that come from known bots, data centers, VPN traffic, or other non-human sources.
3. Erroneous referrer data. Referrer data is rarely available, but it provides valuable information when it is. For example, accurate referrer data can imply that certain sources are not actual podcast consumers. Check for accuracy on any available referrer data.
4. Malformed user agents. For example, a legitimate Firefox version number is 55.0.2. However, a bogus user agent could use the device label “Firefox 55.02” which only lacks a period “.” separator between 0 and 2 and therefore looks like a legitimate user agent. This could be an error or intentional. Be wary of malformed user agents, which prevent proper filtering. If simply malformed, then correct, and if intentionally false, filter them out.
5. User Agents that identify to be from sources that are not actual podcast consumers (e.g. bots that self identify as being bots)
6. Some apps perform a 2 byte range request (Range: 0-1) to check if the media file can be downloaded using byte range requests. This kind of request is often immediately followed by one or more additional range requests. Disregard any 2 byte (0-1 byte) range requests. These requests don’t represent a valid download.
7. Duplicates on paired Apple Watch devices indicated by UA’s that begin with atc/ and include watchOS (/for example atc/1.0 watchOS/), or UA’s that contain (null)/(null) watchOS

**Note:** Known “safe” IP Addresses (dorms, corporations, etc.) should be maintained in an inclusion-list and be allowed for counting. These inclusion lists must be re-validated at least every 90 days since IP addresses may not be static. Keep a record of list re-validation to share with customers and partners to indicate efforts for combating invalid traffic.

#### Step 1.3: Handling HTTP Requests

Different types of HTTP requests indicate different kinds of behavior in the server logs. HTTP requests in the server logs should be handled as follows:

1. HEAD requests: typically used to check for changes. No data is transferred in a HEAD request, so these requests should be excluded.
2. GET requests:
   - a. 200 (ok request) in a non-HLS context: valid count for downloads
   - b. 206 (partial request) or 200 (ok request) in a HLS context: only count if the download covers the 1-minute rule defined in 1.2 above, and de-duplication based on IP Address/UA to cover cases where the podcast consumer might be skipping ahead. Determining whether the requests cover the 1-minute requirement might require reassembling requests.
   - c. 304 (not modified request) - signal that the user has an existing file and wants to see if it changed. These should not be counted.
3. There may also be platform specific quirks to watch for. For example, Akamai uses a HTTP code of 000 for 206 requests that ended prematurely.  These requests can only be counted if they pass all measurement filters.

#### 5.5.3 Step 2: Apply File Threshold Levels

Downloads below a certain size are unlikely to result in human consumption because too little of the file was received to listen to any content. The following rules help eliminate the downloads that are too small to be counted.

1. To count as a valid download, the header information plus **_enough of the podcast content to play for 1 minute_** should have been downloaded.
2. ID3 size recommendation – since the ID3 file size can vary quite significantly, each publisher should measure the ID3 tag file size for each podcast. To be more efficient in cases where the ID3 size doesn’t change, the publisher could set a size for the show/program and whenever the artwork changes, re-calculate the size.
3. Content size recommendation – the size of the download for 1 minute of content will vary based on the bitrate used and the amount of bytes ID3 headers consume. The publisher must calculate this size for each episode.

This step requires a continuous monitoring of the podcasts as each episode gets served.

**Alternatively,** if the podcast episode is shorter than 1 minute or if it isn’t possible to compute the file and ID3 sizes regularly, **_complete file downloads_** (100% of the file, including the ID3 tag or other header information) should be used.

**Note:** One minute was chosen as a conservative minimum size since other mediums use similar or smaller thresholds.

**Note:** When byte range request data is not available, more advanced algorithms that factor in a correction for partially downloaded content may be used. Such a system must disclose how their system overcomes not having the byte range data.

#### 5.5.4 Step 3: Identify and aggregate uniques

Once filtering is completed, requests should be aggregated to identify uniques in the following two scenarios.

**Scenario 1: Identifying Uniques (for Downloads & Podcast Consumers):** Identifying unique requests is important in counting downloads for an episode and in counting audience size. The standard way to sort downloads and remove duplicates is to match on IP address and user agent (UA); however, additional metadata may be available for the download and may help further reduce duplicate downloads. Details for all methods should be made transparent.

First, filter using IP address + user agent (UA); then filter using additional metadata if available.

Filter for **IP Address + UA** with the following considerations:

- A combination of IP Address + UA is used to identify unique podcast consumers and downloads. For example, if the same episode is downloaded 10 times by 6 user agents behind one IP address within a 24 hour window, that would count as 6 podcast consumers and 6 downloads.
- This method requires some technique to constrain counts for a maintained exclusion-list for blocking IP addresses that excessively download/play at a rate that is not feasible.
- To better support known high density IP Addresses (dorms, corporations, etc.), an inclusion-list of IP Addresses may also be maintained. For these IP Addresses, different filtering rules may be needed to account for a concentration of similar devices.

#### Filter for Additional Metadata

Companies can filter using additional metadata if available. When using additional sources of data, these companies must be transparent about what metadata is being used.

Examples of additional metadata may include:

- UserId
- Cookie or similar identifier
- X-playback sessionID

#### Scenario 2: Play-Pause-Play Scenarios

If a unique download is divided into multiple file requests, for example if a podcast consumer plays the first half of an episode using a website audio player, clicks pause, and then resumes an hour later, that counts as one unique download.

Regardless of the use case and the metadata used to filter for uniques, companies must be transparent in their methods by communicating their methods in a corporate description of methodology (DOM).

#### Working with IPv6 Addresses

The members of the Podcast Technical Working Group recognize that measuring unique devices assigned with IPv6 addresses poses certain challenges. IPv6 addresses are not static, and multiple new addresses are cycled on a single device in a short time period. Without special consideration, this feature of IPv6 addresses could result in inflated metrics, and could also impact frequency capping of ad campaigns.

The Podcast Technical Working Group has researched methods to address potential discrepancies attributed to IPv6 measurements to define the following treatment for IPv6 based measurements.

The best way to handle IPv6 addresses is to truncate it to its first 64 bits before calculating. The IP addresses used in calculating metrics is a combination of full IPv4 IP addresses along with partial IPv6 addresses truncated to 64 bits.

**Note:** IPv4 or partial IPv6 addresses can be hashed for privacy reasons without affecting the above formulas. Truncating IPv6 addresses to 64 bits may result in a few duplicated podcast consumers; however, our research has shown that results are comparable to the results for non-truncated IPv4 calculations. Ultimately, metrics providers must be transparent about the methodology used.

#### 5.5.5 Step 4: Generate Metrics

Once the requests have gone through the filtering process above and uniques have been identified, generate the metrics defined in section 6, as well as any additional / custom metrics supported. The metrics should be formatted, and delivered according to each company’s process and policy, using their choice of analytics technology.

#### 5.5.6 Step 5. Audit the Process

Regular audits allow for adjustments to metrics generation. Measurement platforms must watch for behavior that indicates diminished quality of the metrics, and investigate the source of potential errors or fraud.

The entire process must be self-audited and reported in a corporate document of methodology at least twice a year. Anomalies, such as uncharacteristic spikes or drops in data, should be identified and metrics adjusted based on deeper investigation.

Future cycles of metrics generation should factor in any learnings from each run. For example, if certain IP addresses are identified as generating downloads not intended for human consumption, downloads from those IP addresses must be removed from current metric generation, and the IP address must be added to an exclusion list for future metrics generation.

### 5.6 Understanding Discrepancies

Multiple third-party measurement vendors can collect data independently of the host platform. Even when multiple parties are certified, slight discrepancies in download metrics are expected due to different access points and methodologies. Differences within ±5% - assuming alignment on date range, geography, and show selection - are generally considered acceptable. Larger gaps may warrant investigation.

## 6. Podcast Metric Definitions

Since podcast ads are so closely integrated with podcast content, metrics that measure content are vital to ad measurement in podcasting.

Show producers, executives, marketing, and digital product teams are interested in the following questions:

- **Audience:** How many people are downloading my network/show/episode?
- **Downloads:** How many times is my network/show/episode downloaded/progressively downloaded and therefore potentially consumed, at least in part?

Podcast metrics are broken down into 4 categories:

1. Podcast Content Delivery
2. Podcast Audience

3. Podcast Ad Delivery
4. Higher Level or Advanced

The metrics for each category are defined in the following sections.

### 6.1 Podcast Content Delivery Metric Definitions

The following metric is used to describe content downloads. Server log analysis for content delivery must filter data to produce metrics as defined below.

1. **Download:** a unique episode request that results in an episode being delivered to the podcast consumer’s device. This includes complete episode downloads as well as partial downloads in accordance with the rules described in section 5, which outlines the filtering process for measurement. The download metrics can apply for audio and video podcasts in either MP3, MP4 or HLS or other file formats.

### 6.2 Podcast Audience Metric Definitions

Podcast consumers often download more than one episode and often from more than one podcast.  A measure of how many podcast consumers downloaded episodes can be used to describe the reach of the podcast or group of podcasts.

HTTP requests include the IP address of the client device receiving the file and usually include a user agent that, while not unique to the podcast consumer, provides some ability to distinguish multiple consumers behind one IP address.

2. **Podcast Consumer/Listener:** data that represents a single user who downloads content (for immediate or delayed consumption). Podcast consumers/listeners are represented by the unique combination of IP address and User Agent as described in section 5, step 3. Podcast consumers/listeners must be specified within a stated time frame (day, week, month, etc.).

**Note:** The nature of podcast consumption involves consumers on mobile devices, which means that the IP addresses change frequently for each consumer, or what we call “IP-hopping.” IP-hopping can result in double counting consumers, but IP addresses can also be recycled, resulting in undercounting podcast consumers/listeners. These factors can be difficult to account for.

Shorter time frames can produce better results while longer time frames exacerbate the issue. The time frame within which counts are provided should be disclosed to customers.

#### Podcast Consumer/Listener Metric using IPv6 Addresses

The best way to handle IPv6 addresses is to truncate it to its first 64 bits before calculating the _podcast consumer/listener_ metric, which is a combination of IP + UA. Please see Working with IPv6 Addresses under Step 3 of the filtering process for details.

**Podcast Consumer/Listener** = Count of Unique (IP* + UA)

*Either the full IPv4 or a partial IPv6 (prefix 64 bits).

### 6.3 Podcast Ad Metric Definitions

The following metrics represent the first step toward improved ad measurement in podcast advertising. These metrics are derived using the content metrics defined above. As these metrics become adopted in the industry, additional steps can be made toward an improved podcasting ecosystem.

3. **Ad Delivered:** an ad that was delivered as determined by filtered server logs for validated downloads that show either all bytes of the ad file were sent or the bytes representing the portion of the podcast file containing the ad file were downloaded.

For example, if an ad was included within the first 25% of a podcast and at least 25% of the podcast episode was downloaded, then the ad can be counted as delivered.

When ads are dynamically inserted into the podcast episode or within an ad break within the podcast, 100% of the ad content (all bytes) must be downloaded before it may be counted as delivered.

**Note:** An ad can only ever be counted as “ad delivered” if the download it belongs to is determined to be valid. For example, if a 30 second pre-roll ad was included in a download that never got 1 full min downloaded, the ad cannot be counted as valid even if the ad itself was fully downloaded.

4. **Client-Confirmed Ad Play:** counts an ad that was able to prompt a tracking beacon from the client device when the file was played. Whenever possible, this metric should include information about how much of the ad was played. Sufficient granularity might be markers indicating: ad start, first quartile (25%), midpoint (50%), third quartile (75%), and complete (100%).

While the client-confirmed ad play metric represents the most accurate count for ad plays in a podcast, it requires client-side tracking. As discussed earlier, the platforms used to download, store, and play podcast files often lack or prevent the availability of client-confirmed metrics. The IAB Tech Lab will continue working with player platforms to get more access to client-side signals.

### 6.4 Higher Level or Advanced Metrics

All the metrics described in previous sections were written with a focus on episode level analysis. The _content_ and _ad delivered_ metrics described above could be applied at 3 levels: publisher, show, and episode.

Client-side tracking or access to some sort of podcast consumer ID - for example using cookies or using an Identifier For Advertising (IFA) - would be ideal for tracking audiences over time, but this isn’t provided by any major podcatchers. It can be approximated using analytical methods as described below.

If metrics providers have the ability to identify the podcast consumer, they should indicate the mechanism used and provide metrics (downloads, podcast consumers and any other additional metrics supported) at the publisher and show level, in order to provide a better picture of that podcast's reach.

Lacking a podcast consumer ID, building metrics can be done using one of the following options:

1. **Sum the metrics across podcast episodes.**

Acceptable if the goal is to just count the total number of unique downloads, but does not provide a view of the podcast consumer base due to audience overlap.

**2. Use the IP Address & User Agent (UA) to identify and track podcast consumers.**

Provides a better view of the podcast consumer base, with certain limitations:

- The IP Address for a podcast consumer could change – especially in the case of a mobile podcast consumer – at which point there is no way to correlate the 2 IP addresses
- Using UA helps differentiate multiple podcast consumers from an IP address, but breaks down when multiple consumers from an IP have the same kind of device/UA (as is somewhat common in corporate and educational settings)

The above two negatives likely counteract each other over time, but any innovations to better handle these limitations are welcome.

## 7. Podcast Player Recommendations

Companies that provide a player for downloaded podcast episodes can impact server logs used for determining metrics. We recommend the following guidelines for player set up and operations to minimize any impact on podcast measurement.

1. Do not implement auto-play except where podcast consumer intent is implied. For example, if a podcast consumer initiates play for an episode in their podcast player, the expectation is that the next episode will auto-play when the selected episode is complete. In contrast, when a set-up that initiates auto-play upon a page visit or opening an app without any other actions to indicate intent, the result is a bad experience for the podcast consumer and inflates measurement metrics to include unwanted audio play.
2. Similarly, do not preload podcast episodes unless the intent was clearly to play the podcast. This wastes publisher hosting bandwidth and artificially inflates stats.
3. Use header information located at the start of the podcast to prevent a full download when not needed.
4. For a full download, ask for the entire file at once. For a progressive download, ask for the file in slices at a byte range that is more than 2 bytes at a time. This way a full download can be distinguished from a progressive download.
5. Do not modify the enclosure URL or add extra parameters when requesting media.
6. Do not cache podcast episodes on your servers. Always download the latest episode from the enclosure URL for every app podcast consumer initiating a download.
7. Use the GUID - as opposed to episode URL, title, publication date, etc. - to identify new episodes in the RSS feed that should be automatically downloaded to a podcast consumer’s device. The GUID is designed to be persistent regardless of changes to hosting environments, titles, or other details.
8. Employ an “automatic download unsubscribe” behavior. For example, after a number of inactive downloads (episodes never played), stop auto downloading additional episodes.
9. Do not automatically download all episodes (e.g. back catalog episodes) by default. This behavior creates unnecessary drain on the publishers’ servers as well as burning through podcast consumers’ bandwidth. It also creates spikes in downloads on server logs that require resources for troubleshooting, explaining, and addressing.
10. Provide enough details in the user-agent header to allow it to be consistently differentiated from the user agent of other devices. See “User Agent Structure” below.

In addition to podcast consumer experience issues and slowing down the websites, if these guidelines are not followed, measurement companies may decide to discount ALL the traffic from these apps/sites because they cannot discern true downloads or plays.

### 7.1 Agent Structure

Device platform providers and app developers used to play podcast episodes should provide enough details in the user-agent header so that it can be consistently differentiated from the user agent of other devices. Using the following pattern to build the user-agent will offer a consistent structure for all parties who consume the details:

```text
<app name>/<app version> <device info> <os name>/<os version><other info>
```

For example:

```text
AppName/1.2.3 DeviceBrand DeviceModel OSName/1.2.3 LibName/1.2.3
```

Whenever possible the above user agent structure should be applied to both RSS feeds and audio files.

We recommend that OS hosts should allow the user agent to be modifiable when using their libraries. Player platforms should be conservative about adding unnecessary information to the user-agent string and as part of their encoding practices. For example, refrain from injecting user or session IDs into the user-agent string.

We also recommend that platforms submit their user-agent header value to the IAB Tech Lab Spiders and Bots inclusion list so that it is not considered a bot, enabling the signal to be used for determining device information. If the app or platform uses bots to index content, the user-agent should be specified in a way that is distinct from the application user-agent and should also include the word “bot” to clearly identify its use case.

## 8. A Use Case in Changing Technology

Certified companies put practices in place to watch for anomalous changes that impact measurement. The Podcast Technical Measurement Working Group with IAB Tech Lab includes companies that look at podcast download measurement on a daily basis. When they see a significant anomaly in their reports, they bring it to the attention of the Working Group and enter a process for discovering what is causing the anomaly and what to do about it.

The below use case demonstrates an example of a shift in technology and how the Working Group addressed the issue.

### 8.1 Apple watchOS Duplicate Downloads

Podcast server logs can be impacted when podcast player apps introduce new behaviors or updates. For example, wearable computing devices, such as a smart watch, may duplicate downloads for the paired phone device. Filtering for the known user agent helps metric providers remove the duplicate downloads. However, an update that changes how that user agent is made known may cause a spike in downloads. This exact case happened when Apple changed how it labeled the User Agent for Apple Watch.

In 2020, Apple Watch changed metadata conventions for its user agent that impacted metric providers’ ability to filter out duplicate downloads. The spike in downloads was obvious to some of Tech Lab’s compliant companies and made known to IAB Tech Lab. Once the source of the spike was identified as a change in metadata for Apple Watch downloads, an addendum was issued to highlight the change so that metrics providers could adjust their process.

The addendum required filtering out:

- UA’s that begin with **atc/** and include **watchOS** ( _for example atc/1.0 watchOS_ )

That label was changed again and the addendum was updated to include filtering out:

- UA’s that contain **(null)/(null) watchOS***

And yet again in recent years, Apple Watch became capable of downloading episodes independent of its paired device. The result of these changes is that companies seeking certification in Tech Lab’s compliance program are required to filter out UAs for Apple Watch while today, some of those downloads may be a download that is unique and not duplicated on a paired device. However, detecting whether the download on a paired device is a duplicate or unique could be a challenge, and as of the release of this document, Apple Watch downloads still represent a significant amount of duplication. For now, Tech Lab’s guidance still requires filtering out Apple Watch downloads. Should the counting methodology change, a new addendum will be issued.

### 8.2 Accounting for Changes in Technology

The above use case was specific to Apple Watch and likely caught because of the higher market share for Apple devices. However, changes that impact podcast measurement happen on more devices and with more frequency than our version update cycle for podcast measurement guidelines.

Moving forward, compliant podcast measurement companies should have practices in place to account for mass market technology changes in their measurement reports. Such practices might include setting reasonable data thresholds to trigger warnings about anomalies in the data, a course of action when anomalous data occurs, a subscription to common development sites that report known issues or updates.

Measurement practices for your company depend on your business model and strategy. When seeking certification for compliance against these guidelines, be sure to share how your company accounts for changes in technology and what you might be doing to address any known issues or data spikes occurring in the market at the time of audit.

## 9. In Closing

Podcast syndication offers an attractive selection of inventory for audiences that are more attentive and more loyal to their podcast shows. Measuring podcast advertising performance is dependent on server-side counts and can offer sound data provided that podcast measurement providers adhere to the recommendations outlined in this guidance document.

The recommendations we provide help to define a fair market for podcast inventory because it reduces inflated counts that result from duplicate downloads, general invalid traffic (GIVT) such as known bots, some of the more obvious sophisticated invalid traffic (SIVT), and temporary anomalies in the data produced by changing technology or other significant events.

IAB Tech Lab’s Podcast Technical Measurement Working Group will continue to deliberate over how to bring more clarity and fairness in measurement practices as well as ways to offer support for this growing and lucrative market. Continue to check in on our site at iabtechlab.com, or send your questions and suggestions to support@iabtechlab.com.

[^1]: Please be advised that: (i) one or more of the measurement processes described herein may be subject to patents; (ii) IAB Tech Lab has performed no diligence and has not analyzed the validity of any of these patents; (iii) IAB Tech Lab is not promulgating any standards or specifications under these guidelines; and (iv) prior to implementing any measurement processes described herein, you are solely responsible for conducting any such diligence and analyses and/or licensing any necessary patents.
