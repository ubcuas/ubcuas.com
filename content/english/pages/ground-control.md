---
title: "Ground Control"
# meta title
meta_title: "Ground Control"
# meta description
description: "Projects pertaining to our ground control systems and services."
# save as draft
draft: false
---

<!-- TODO: add more software stuff here -->

{{< columns >}}
{{% markdown class="text-center" %}}

## GCATS

The GCATS (Ground Control Antenna Tracking Station) family of projects are custom-developed, long-range data transfer solutions capable of automatically relaying images and videos from drones flying at long ranges back to the ground control station.

Their job is to autonomously track our aircraft in flight and point a directional antenna in that exact direction. This allows the team to use higher gain antennas as opposed to less optimal omnidirectional options. Additionally, the ability to modify the height of the antenna tracker counters the Fresnel effect’s impact on our operations.

{{% /markdown %}}

<--->

{{< slider dir="images/gcs/gcats" class="max-w-lg" height="" width="" webp="true" command="Fit" option="" zoomable="true" >}}

{{< /columns >}}

<hr>

{{< columns >}}

{{< image src="images/gcs/map.png" caption="" alt="Ground control station map and controls" height="" width="600" position="center" command="Fit" class="" title="" >}}

<br>

{{< image src="images/gcs/odlc.png" caption="" alt="Object detection and classification software" height="" width="600" position="center" command="Fit" class="" title="" >}}

<--->

{{% markdown class="text-center" %}}

<!-- TODO: update this -->
## GCOM

Over the past years UBC UAS has been working on the next generation ground command software (GCOM). A single suit that acts as a data consolidation platform, it gathers information about the UAS from multiple sources (e.g. Mavlink) and provides the following functionality:

{{% /markdown %}}

- Antenna tracker control
- Drone communication and control
- Collision avoidance
- Reliable Image download
- Image object detection
- Image geotagging
- Analytics on processed images
- Autonomously report generation

{{% markdown class="text-center" %}}

In addition to the above functionalities, GCOM was designed with reliability and modularity in mind. This allows UBC UAS to achieve higher reliability standards since each module can be independently tested against all possible inputs. Additionally, GCOM operates using a fully reliable communication protocol developed to transmit variable length data between any two devices (UAS Message) that utilize serial, TCP, or UDP communications.

{{% /markdown %}}
{{< /columns >}}