# [Binding] HIP-8: Accept 352 pixels as minimum dimension in video submissions
**Simple summary**
Make clear that the definition of 360p does not literally mean 360 pixels, and that certain codecs crop 4 pixel columns from each side of the image. Submissions with 352 pixels wide should not be considered in violation with submission rules.

**Abstract**
This amendment proposal is a fast, immediate solution to issues related to a widespread method of video submission… It moves the minimum dimension of the width or height of videos from 360 to 352 to match what is currently capable in the most widespread technology available. The 8 pixels removed cropped by the codec due to ancient PAL analogue norm is not moving the line too much and it fits the technical capability of current widespread technology. It is not realistic to challenge a person because 8 pixel columns are removed from the side of the picture (in the case that is background that is removed from the frame and not actual image). This amendment is final and it is not intended to serve precedent of moving the minimum any further than this.

**Motivation**
The most common and easy way for a lay user to submit and transfer a video without additional installations or knowledge is sending it via WhatsApp and downloading it through WhatsApp web. In order to avoid opportunistic challengers that predate in these submissions, that would otherwise be a good-faith submission, an urgent amendment to this policy should be put in place. It would also lift some artificial and clunky methods that current new users are using that degrades the platform in order to meet the requirements (re-encoding video, padding to sides of it, etc.).

**Specification**
Minimum video dimensions is a square of 352 pixels by 352 pixels. Videos with equal or higher size than stated should not be considered a violation to the rule #4 of submission guidelines. Videos equaling 351 pixels or lower in size in any of their dimensions will violate rule #4.

This is an interim resolution until more precise video quality submission guidelines are approved.

**Implementation**
Change the text of rule number #4, replacing this block of text:

    The video quality should be at least 360p, at most 2 minutes long, and in the video/webm, video/MP4, video/avi or video/mov format.

With this block of text:

    Video submissions must follow all of the following requirements:

       * at most 2 minutes long,
       * in the video/webm, video/MP4, video/avi or video/mov format,
       * vertical (portrait), horizontal (landscape) or square,

    and follow these minimum size requirements:

       * Minimum height: equal to or higher than 352 pixels
       * Minimum width: equal to or higher than 352 pixels



**Rationale**
Refer to [Imprecise rule regarding video quality of submissions ](https://gov.proofofhumanity.id/t/imprecise-rule-regarding-video-quality-of-submissions/443)

**Supplementary information**
See also forum discussion in https://gov.proofofhumanity.id/t/hip-8-phase-3-accept-352-as-minimum-dimension-in-video-submissions/536

[Link a versión en español](https://gov.proofofhumanity.id/t/hip-8-phase-3-accept-352-as-minimum-dimension-in-video-submissions/536/22?u=ludovico)
