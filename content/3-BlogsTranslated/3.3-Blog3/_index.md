---

title: "Blog 3: MasterClass enhances video quality and reduces costs with AWS Media Services"
date: "2025-09-15"
weight: 1
chapter: false
pre: " <b> 3.3 </b> "
----------------------

# MasterClass enhances video quality and reduces costs with AWS Media Services

by Dan Gehred and Matt Carter on 25 MAR 2025 in Amazon CloudFront, AWS Elemental MediaConvert, Direct-to-Consumer & Streaming, Industries, Media & Entertainment, Media Services, Networking & Content Delivery

For many, cooking alongside Gordon Ramsay or writing with Shonda Rhimes may seem like pure fantasy, but streaming platform MasterClass makes these experiences a reality. The streaming platform offers more than 200 classes, delivered by the world’s best instructors. With video at the core of the MasterClass experience, the company looked to Amazon Web Services (AWS) Media Services to help support its continued growth.

The company now uses AWS Elemental MediaConvert and Amazon CloudFront to support video transcoding and delivery, with AWS Partner Nomad Media as an orchestration layer. After migrating to AWS, including the transfer of its archive content, MasterClass saw significant video infrastructure improvements, including enhanced video quality; it also reduced video costs by more than half.

“AWS provides a flexible solution that we can build on, so that we can create our own technology and IP around our media space,” said Paul Phipps, Senior Staff Software Engineer at MasterClass. “With MediaConvert and CloudFront specifically, we’ve dramatically reduced costs while improving streaming quality. We’ve also seen a reduction in buffering times and faster streaming across a variety of devices.”

![Masterclass](/images/Blog/Blog3.jpg)

## Improved transcoding efficiency with AWS Elemental MediaConvert

When MasterClass launched in 2015, the company used a turnkey video solution to develop the platform. While that setup served them well for many years, the company’s needs grew as its content library expanded. Making more video classes available to subscribers required a more flexible and scalable solution, which it found in the file-based transcoding service AWS Elemental MediaConvert.

Today, MasterClass relies heavily on the Quality-Defined Variable Bitrate (QVBR) feature in MediaConvert. QVBR automatically allocates bits to maintain consistent video quality, confirming viewers enjoy an optimized experience, whether watching on a smart TV, computer, or mobile device. Previously, MasterClass had to first process files with FFmpeg, resulting in two compression steps. With its new setup, MasterClass sends native files directly into MediaConvert, leading to noticeably improved video quality, reduced artifacts, and faster content delivery for users.


## Seamless migration and enhanced content delivery

Along with providing the orchestration layer, Nomad Media proved essential to a smooth transition, providing tools that enabled MasterClass to parallelize workflows with minimal disruption.

“We re-transcoded all of our content onto the cloud, so we could improve the quality of our legacy content with QVBR,” explained Phipps. “One of the great things about AWS is that every service is supported by a large infrastructure and serverless applications. Backed by that support, we were able to transcode most of our library in just a couple of days.”

Nomad’s direct integration with the content delivery network (CDN) Amazon CloudFront also influenced MasterClass while mapping out its migration. After evaluating several third-party CDNs, MasterClass determined that Amazon CloudFront provided the best fit.

“We found that Amazon CloudFront performed better or as well as the other CDNs we assessed, and it was much easier to implement in our workflow since we were already using AWS,” noted Phipps. “Also, there isn’t an associated storage consumption cost, which is a huge benefit.”

MasterClass was interested in a system that allowed for a high rate of cache reuse. Using CloudFront with Lambda@Edge, the company optimized its token authentication process. With this setup, its team can refresh tokens without changing the content path, enabling secure access and maintaining cache stability.

## Looking ahead with AWS

With full autonomy over its media stack, MasterClass can now customize its video workflows and explore new feature implementations like content analysis powered by artificial intelligence (AI) or live streaming with real-time interactivity. As MasterClass continues to innovate and expand, AWS provides them with robust and flexible infrastructure that supports both their present needs and future ambitions.

“Having control over our own tech stack is essential for scaling our offerings and continuing to innovate,” concluded Phipps. “AWS gives us the flexibility we need to build a future-proof solution that supports our continued growth.”
