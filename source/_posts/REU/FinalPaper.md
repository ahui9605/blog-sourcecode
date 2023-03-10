---
title: Closed Interpreting Accessibility
date: July 21, 2022
tags:
  - Articles
  - Web Development
  - REU
categories: Accessibility Research
keywords: Accessibility, CIA, Able Player
description: An advanced accessiblity feature enables users to access the media player without communicating barriers

#阅读模式，右下角开启
readmode: true

#封面
cover: /images/REU_CIA/CIA,cover.jpg

#版权
copyright_author: Bridget Lam, Zehui Liu
copyright_url: https://sites.google.com/gallaudet.edu/reuaict/
---

### Abstract

Sign language in the media, either on-site or remotely (video interpreting) is provided to people who are Deaf and hard of hearing (DHH) to be informed about critical information (e.g. COVID-19 briefings) and other critical information in their daily lives. Access to Sign Language on TV or online media is not a requirement outlined within the American Disability Act. It is known that the DHH community relies primarily on closed captions as the most accessible option available on all media platforms. There is an increasing trend that sign language interpreting is provided exclusively in news outlets during COVID-19 lockdown (NAD vlogs, 2020) and it will continue to grow in the near future. To promote quality accessibility, we came up with a tool called AblePlayer, an accessible tool similar to closed captioning that will be displayed with an MP4 video that can be toggled on and off. The closed interpreting tool is user-adjustable. It contains settings such as: interpreter size, transparency, and location. All of which can be adjusted by the user. This study aims to evaluate and understand the current practice of media in the US and abroad. We want to eliminate all the barriers of closed captions (CC), picture in picture (PIP), and live interpreting. We hypothesize that having closed interpreting would affect the Deaf viewer’s comprehension positively. We collected feedback from 10 deaf, hearing, and hard of hearing sign language users through observational study, followed by an end-user survey. The addition of captions had a favorable effect on the participants' comprehension rate. The most noticeable variations in understanding between viewing a sign language interpreter with no background color preference, as well as the draggable window and resize features, garnered good responses from a majority of our participants. The findings led to recommendations for the uniform usage of certified sign interpreters with no background color, draggable windows, and resize options in subtitles video across multiple media platforms.

### Introduction

The utilization of sign language interpreter videos has grown as a result of the fast development of high-speed data transmission and video compression technology. Deaf and hard of hearing people are increasingly adapting to acquire information from television shows, films, and websites. Thus, sign language interpreter films are intended for the deaf and hard of hearing who rely on sign language as a valuable tool for translating spoken and/or written words. Despite the fact that little study has been conducted on how deaf individuals perceive a recording of a sign language interpreter when watching web films, several issues are clear.

Accessibility is ‘ad-hoc’ with traditional picture in picture sign language on TV because the media tends to crop out the screen of the interpreter if it is even available to all, which prevents the sign language viewer from getting full access to information. Providing PIP on a few channels or sources achieves critical mass, albeit with limited success. If not properly set up, it might be difficult for the signing audience to see what is being spoken, resulting in incomplete communication. It only caters to the DHH community on a limited level, therefore this issue may be difficult for DHH individuals because the media is hearing-centric, and they have little experience with sign language translating on TV.
Captions are an alternative option to replace aural information that many deaf viewers find difficult to follow because the speed of verbatim captioning is likely to exceed their reading abilities. Even after controlling for reading level, deaf students learned less from on-screen text than hearing peers, apparently based on differences in background knowledge and information processing strategies. They prefer ASL interpreters over closed captions, partially because they find captions difficult to understand and partly because they receive less information. There are still concerns with video interpreters that must be solved.

We have outlined a few of the proposed study's objectives. Our initial goal is to understand and learn what features help deaf, hard of hearing, and hearing sign language users. Next, we will examine how closed interpreting will assist society in including these accessibility features in mainstream accessibility standards such as closed captions. Following preliminary research, we aim to evaluate and analyze the collected data to determine how the complexity of supportive accessibility can be applied to general users, both signers and non-signers. Then we will determine which accessibility functions are the most helpful and desirable, as well as how we might improve the experience for a certain group of users.

### Research Questions/Objectives

- In terms of design (preferred signer, signing style, background color) are these options enough for accessibility of the Deaf community?
- What are the ‘new’ minimum features to be included?

### Lit Review/Background

This study aims to investigate the accessibility of media contents through sign language interpreting, which is still not widely adopted in the US. There have been several studies in the past few years (Yi, J. H. et al, 2020, Baliarda, M. B. et al. 2020, Debevc, M. et al. 2015) in Asia and Europe that have investigated the best practice of sign language interpreting in the media using PIP, and other customized features. The findings show that the PIP is essential to comprehending Sign Language users as their primary language. Additionally, those studies pursued further examination of the individual preference with the features such as sizing, placement, video backgrounds, etc). The current technology allows us to make this possible, but we do not know what the preferences are for DHH in the US. This study intends to duplicate other international studies from the DHH community to improve a better understanding of accessibility content so that DHH can conveniently access sign language in the media. The study will be designed to mainly focus on the group of participants whose primary language is American Sign Language (ASL). We call this research project ‘Closed Interpreting Accessibility’ (CIA.)

One study conducted in Korea, researched their Interpreting service among 30 Deaf and hard of hearing individuals over the age of 19. This study conducted a survey and had a selection of different types of interpreting services. Most users preferred the closed interpreting option (no background and reasonably sized). The worst screen clip out of all of the options are similar to what is currently shown on TV programs today (PIP). The experiment consisted of a total of three people: a subject, a sign language interpreter to help guide the experiment progress, and an investigator. Tobii Nano, an eye tracker, was attached to a 27-inch monitor to collect gaze information from the subject during the experiment. (Yi, J. H. et al 2020).

Another study researched how sign language users responded to a screen composition including a larger screen for the content and a smaller screen for the sign language interpreter. 32 deaf users participated in this experiment, watching four similar clips with four different screen compositions through focus group style research and surveys. The study registered the pattern of screen exploration with Eye Tracker, and assessed content recall with two questionnaires. Results show that sign language users mainly look at the sign language interpreter screen. This survey clarified the relevance of some parameters (type of on-screen insertion (picture-in-picture / half screen (split screen) / Chroma key); shot size (long shot / medium long shot / mid shot / medium close-up; interpreter’s clothing color (plain light color / plain dark color / patterned or multi- coloured); size of the interpreter’s screen (small / medium / large); on-screen positioning of the interpreter (right / left, top / center / bottom); position of the interpreter (standing / seated).) Others were considered irrelevant in terms of usability and quality of the SLI access service. For example, users considered gender, age, appearance and position of the interpreter to be of least importance. Whereas speed, size and color com- binations were the parameters that had a greater impact on screen legibility. The participants tend to look more often and for a longer time at the SLI side closer to the main screen. Results were interpreted in terms of perceptual strategies developed by Sign Language users. All participants considered that the most important on-screen parameter to grant accessibility was the size of the interpreter’s window. Most of them agreed that taking roughly a third of the split screen and using a medium shot or a medium-large shot would be ideal for news broadcasts. However, they acknowledged that it would not be appropriate for other television programs, such as interviews, films or documentaries where a larger scene screen was preferred (Baliarda, M. B. et al. 2020).

Finally, the main aim of a study conducted in Europe was to find out what the increment in comprehension of the content of sign language interpreter videos was, when captions were included. To be more specific, we compared the comprehension scores of sign language interpreter videos with or without captions. Additionally, we aimed to investigate the differences in comprehension scores between different topics (sport, hiking, shopping, and culture) presented in sign language interpreter videos with, or without, captions. Fifty-one deaf and hard of hearing sign language users alternately watched the sign language interpreter videos with, and without, captions. Afterwards, they answered ten questions. Participants were required to have the ability to read and actively understand basic written text and to have basic experience in using information and communication technology. The results showed that the presence of captions positively affected their rates of comprehension, which increased by 24% among deaf viewers and 42% among hard of hearing viewers. The results led to suggestions for the consistent use of captions in sign language interpreter videos in various media (Debevc, M. et al. 2015).

### Development/Setup

_Survey Setup:_
We employed a screening survey at the early testing stage to qualify or exclude respondents, allowing us to ensure that respondents fit the criteria within our targeted participation group. To obtain valuable high-level responses, in-depth insights via an exit survey and interview at the end of the testing stage were conducted. This step is to obtain additional clarification information, answer participants' confusing questions, and receive any feedback related to our research. The survey questions are based on the SUS (System Usability Scale), and participants will rank each question from 1 to 5 based on how much they agree with the statement they are reading. There are English and ASL versions available for use. Both surveys are done through Google form.

_Able Player Setup:_
We used Ableplayer as our priority supportive tool to implement the sign language interpreters and closed captions for all disability audiences. The original purpose of creating Ableplayer is to allow the front-end/full-stack developer to set up the accessible media player on the website, followed by WCAG (Web Content Accessibility Guideline) accessibility checker. The contributor AccessComputing developed this professional development of the Ableplayer project at the University of Washington with financial support from NSF. Ableplayer is an open-source tool that anyone can use, modify, and add. We removed the redundant transcripts and chapter descriptions that are the built-in features in the original code source. We are mainly focused on the sign interpreters and closed captions only. Researcher Zehui Liu developed some new features that were more accessible by using JavaScript and jQuery during the methodology development stage. The current available of the following features can be used:

- The media controller's essential functions included: a timeline bar, play/pause, rewind/forward, slow/fast speed.
- Built-in closed captions with user preferences provided, such as font size, text/background color, opacity, with newly added features: draggable captions in the media player.
- Added features of the drop-down menu to be allowed to select multiple interpreters with various background colors. Also, an alternative option of transparency from 0% to 100% is available to interact with.

The transparency option is not available all the time except the user enables interpreters features with no background. It is considered unintuitive for some users to interact with the transparency icons, but a tooltip will pop up when the user hovers that icon; it will provide a brief explanation of how to enable the transparency in some specific situation. Since this research is focused on the sign interpreters and closed captions, there is only minimum HCI of eight golden rules of the interface designed in Ableplayer.

![](/images/REU_CIA/CIA,figure1.png "Figure 1: Example of Two Sign Interpreters and Closed Captions on Able Player Media")

To provide the highest quality sample videos, the two Deaf ASL interpreters pictured above, are official certified interpreters on a professional level and are actively involved in Gallaudet University's activities for the association of sign language interpreters. The purpose for having two interpreters of different skin tones served visual contrast purposes as the DHH community heavily relies on their vision to obtain information. The interpreters were filmed in front of a chroma key background at the Kellogg Hotel Lab to illuminate the interpreters in multiple positions from the waist up and lit by using four separate lighting positions while also controlling (or eliminating entirely) the shading and shadows produced by direct lighting. The videos were captured in the high-definition resolution of 3480 x 2160 at a 29.97fps camera. Due to the lack of support for the alpha channel (the interpreting video with no background only) in MP4 format, For each interpreter's video, Ableplayer embeds an alternate format WebM in 1280x720 resolution with no background color. Nevertheless, the original video content itself is still in MP4 with 3480 x 2160 quality for optimal message delivery.

The interpreter window is designed with size placement and other customization options on Ableplayer in mind, along with a focus on the visibility of the sign language interpreter delivering the content. We chose essential information converting economic news, interviews, and visual graphic affairs. We aimed to include other forms of entertainment to simulate our daily basis of using accessibility to see if it is possible for all forms of media to be well fit for users. The order of videos was randomized to eliminate bias that can arise out of the order in which a participant sees stimuli. The sequence of the interpreters was likewise randomized; each video topic is designated with Interpreter A or Interpreter B as a video title.

_Testing Room Setup:_
Our participants tested the tool in a research lab at Gallaudet University. A 4K monitor is connected to a laptop where all equipment is already set up for participants. A camera to film the participants and their immediate reaction, thoughts, and feedback during the usability portion of the study. This process is coined as ‘Think Aloud Protocol’ (TAP). There is also screen recording to review which functions were clicked on the most and drew the most attention to. The researchers observed the participants and provided any help and support needed with technological problems and ASL clarification. Researchers made note not to impose help in effort to not tamper with the feedback given to us.

### Evaluation/Study

1. The investigator met the participant and explained the Informed Consent and Video Release form in ASL or spoken English. A general explanation of the study purpose was to be shared as follows: “At REU AICT, we are conducting studies of different people’s user experience and feedback on closed interpreting services to promote accessibility for the Deaf and hard of hearing community.”
2. The participants will sit in a room with a computer provided by Gallaudet along with a camera for recording feedback.
3. The research assistant will explain the process on how to perform the TAP during the study by providing a video example. Additionally, they will be expected to complete a survey of Net Promoter Scale (NPS) and System Usability Scale (SUS) questions.
4. Before starting the study, a video camera will start recording the participant's immediate reaction as well as a screen recording of the desktop screen that the participant will be using. The participants will be directed to the Ableplayer webpage. During the process, the participant will have access to 4 videos of different media content and 2 different signers. The different tone of the skin for vision and contrast evaluation purposes. They will spend approximately 4-5 minutes on each video. Each window will have the same accessibility functions supplied and will be permitted to access each video.

![](/images/REU_CIA/CIA,figure2.png "Figure 2: The  the Concept of the Participant Viewing the Able Player. ")

The illustrated figure is an example of one video the participants watched and attempted to apply accessibility functions that they were most comfortable with and tested its effectiveness. There were a total of 4 videos, each video content was used from the public site platform YouTube. The footage was extracted and edited for length and uploaded in our private study webpage. Each video was played twice, once with one signer, next with the other. The participants will be asked to perform the Think Aloud Protocol (TAP) while using the platform. They are asked to describe their navigation, decision-making, and opinions during and throughout the process. The participants will fill out an end-user survey that entails a likert scale inspired by the System Usability Scale (SUS) and Net Promoter Score (NPS) followed by a short open-ended discussion.

Each participant was compensated for their time during the usability study with $25. All participants' responses to both the usability study and survey remained confidential and was only to be shared among investigators and co-investigators of this study.

### Results

Overall, feedback was mostly positive. There were mixed responses about the consistency and complexity of the tool. Results from the end user survey and recordings of the participants served to examine each of their reactions to each function, such as ease of use and how quickly they can manage each function. We employ surveys and open-ended discussions for feedback on user satisfaction, comprehension of video contents, and how simple it was to see each content video and interpreter videos.
Participants were asked to complete the questionnaire through Google Form immediately following each usability session. With a total of ten participants in our study, we used the same survey for each round of usability testing. We used an Excel chart generation tool to visualize each participant's responses in order to evaluate and present the data. The SUS result of each participant was processed in accordance with the SUS calculations in Figure 3.1 and the scores for individual participants and different hearing status groups of participants were examined.

![](/images/REU_CIA/CIA,figure3.1.png "Figure 3.1: A Bar Chart of SUS Calculations by Score")

We gathered and documented each participant's responses in order to create complete bar charts of SUS calculations. Combining these two dimensions produced a heat-map with positive and negative ratings, as illustrated in Figure 3.2.

![](/images/REU_CIA/CIA,figure3.2.png "Figure 3.2: Detailed Diagram of SUS Calculations by a Heatmap Matrix")

The formula we used to get the SUS score (Brooke and John, 2013) per participant begins by adding the total scores for all odd-numbered survey questions (highest number, 5, to mean positive feedback). Then subtract 5 from the total to get (X). For example in Participant B:

<table>
    <tr>
        <td><div align="center"> <b>X=(4+4+4+3+5)-5</b></div></td>
    </tr>
</table>

Then we add up the total score for all even-numbered questions (lowest number, 1, to mean positive feedback) and subtract it from 25 to get (Y).

<table>
    <tr>
        <td><div align="center"> <b>Y=25–(1+1+2+1+1)</b></div></td>
    </tr>
</table>

Finally, we multiply the total score of the new values (X+Y) by 2.5.

<table>
    <tr>
        <td><div align="center"> <b><i>Participant B SUS score</i> = X+Y*2.5</b></div></td>
    </tr>
</table>

There is only one participant score computed above; When all of our (10) participants' scores are aggregated, the average SUS score is 82.2, followed by the System Usability Acceptability Score, which is in the acceptable range but close to the excellent rating for good design. It is worth noting that all of the participants fully agree with the system and are quite confident in using it frequently. Both the SUS and System Usability Acceptability, received 49 points out of a possible 50 on survey questions 1 and 9, accounting for 98 percent of the highest rate in the study.

In the open-ended discussion portion of the study, the majority of the participants agreed with the statement that Ableplayer was a useful tool and can be applied to our real life on a daily basis on each media player. Only a small number of respondents indicated that they would still prefer to use traditional PIP (Picture in Picture) or live captions similar to Youtube auto captions for their satisfaction of accessibility. There are some negative feedbacks about the buggy, unreachable functions are not consistent to interact with is their major concern and providing several suggestions such as providing a professional team to develop with more UI and UX testing.  
When asked about the customization of captions preference, half of our participants unanimously agreed that it is necessary to exist for more flexibility. Comments entailed:

<table>
    <tr>
        <td><i>“I see why your tool needs to offer captions preferences, and it is sometimes necessary for … colorblind viewers, who have difficulty seeing a specific color and must alter their best color for watching experience.”</i></td>
    </tr>
</table>

<table>
    <tr>
        <td><i>“I like the captions preference options… (but I) don't like the white font with black background, so I simply change the background to green, now it works much better for me.”</i></td>
    </tr>
</table>

The customizable implementation of sign interpreter window had more positive response than the closed captions preference. One participant commented:

<table>
    <tr>
        <td><i>“The draggable signer window is fantastic…However, I believe the drop-down choice is worded incorrectly…(and) you mixed in the signer enable options and background color…(So) consider separating them and giving them their own icons and functions on the media controller.”</i></td>
    </tr>
</table>

Taken together, these findings suggest that there is an association between the complexity of the user interface as well as its unfriendliness to inexperienced computer users. Some participants took longer than others to figure out how the tool worked and needed further guidance and explanation for the research itself. Eventually they managed to figure it out on their own. The sign interpreter window received far more positive feedback, but it required further testing and tweaking on the drop-down menu to provide the optimal message to the user.

The next section of the open-ended discussion is the transparency function. We noticed that it might not have been the most functional part of the software on specific areas of certain videos. When the transparency of sign interpreter windows with no background color were mentioned, two third of our participants gave it a thumbs down to the transparency because of the busy background that made it hard for the user to see. Furthermore, when clicking on a background screen color for the interpreter, transparency was not available to serve that function.

![](/images/REU_CIA/CIA,figure3.3.png "Figure 3.3: 50% of Transparency of Each Sign Interpreter ")

In the figure 3.3 above where the interpreter on the left is mixed with white font, it is difficult to see what the sign interpreter is signing. Additionally, the interpreter on the right with a dark busy background, is just as very difficult to decipher. Another participant, when asked for the transparency function, said:

<table>
    <tr>
        <td><i>“It (transparency) looks cool at first, but when I enter Fullscreen mode and activate it with 50% opacity to apply the Oscar video and another one with gas prices in Los Angeles, it is difficult to view. So, in my perspective, I do not recommend providing transparency.”</i></td>
    </tr>
</table>

### Conclusion

A new form of media accessibility for the Deaf and hard of hearing community has been necessary and crucial. We hoped to have not only reached that new form, but created a new standard of the needs of the community. For a long time, the DHH community has been left out of information and communication in the media. Ableplayer aims to give the community better access to information and communication from a variety of media beyond news programs and give the user control and options to accommodate best to their language needs.

We found that many people did indeed like the customizable closed interpreting implementation over the traditional interpreting service. However, there were several survey results and feedback that contradicted each other. In general, there was a noticeable and significant increase in satisfaction, understanding and ease of viewing from participant’s feedback. Participants also preferred the interpreting features that allow for resizing and relocating the interpreter video in the customizable implementation, but the transparency feature was not well-received.

There will always be more that can be achieved when it comes to accessibility for the Deaf and hard of hearing community, the solution is not one-size fits all. Our tool brought something new to the table and was able to create discourse on how it can improve to achieve greater quality accessibility.

### Future Work

Some limitations to consider for future work, the data we obtained contains only 10 participants for the time being, all of who were Deaf, hard of hearing or hearing and ages 18-34 years. There is a need to obtain a larger sample size and demographic variability so that the data can be generalizable. Some survey questions were difficult for participants to comprehend, and only a few Deaf people responded without asking for explanation in ASL. Led to nonsensical answers such as repeatedly choosing the answer ‘5’ to mean, strongly agree for all questions. We had originally planned to provide an ASL version on each survey question, however due to the time constraint, we were only able to provide in-person clarification given that the participant asked for it. There was potential researcher bias in that explanation of the testing process to each participant slightly differed as some participants asked for more clarification even though the research was aimed to study effectiveness and understanding of the tool independent from guidance.

Some participants were curious as to why there was a need for two interpreters of different races. The intention mainly served visual contrast purposes particularly for Deaf-blind users as well as the DHH community as a whole, due to the fact that the Deaf community in general is largely visually reliant in receiving information. It was taken into consideration that all of the participants more than likely understood the function to serve as a cultural representation purpose as both signers had different signing styles and dialects. For this reason, the demand for more diversity in this function was mentioned frequently and brought more questions. It would be necessary to have a variety of certified trained sign interpreters to record in order to add diverse signers of different nationalities, colors, and genders solely for representation purposes.

It is important to note some people found it hard to catch all the information from videos that had two people speaking. There was only one interpreter provided, switching back and forth between speakers and interpreting for two people. In the future we should work towards having more than one interpreter ready to ease communication and information delivery.

In the tool, the sign interpreter with no background color is achieved by exporting an alpha channel with WebM video format using the Premiere Pro video editor. It is possible to automate the conversion of video to no background by uploading the video clip to the ableplayer website. This is the most ideal solution in order to save more time and less workload. There were technological concerns that necessitated the assistance of additional UI and UX professional consultants and specialists, such as incorporating a new design style on a dropdown menu. A professional can provide far more beneficial recommendations. While working on this enormous project since 2014, more than three or four individuals are also encouraged to contribute to the future development of Ableplayer.

### Resources Availability

All research data (including paper and electronic) will be treated with the utmost respect and confidentiality. All data collected and downloaded will be securely stored in the cloud drive with password protection and will not be shared with others who aren’t listed in this IRB study approved, the principal co-investigators are (Bridget Lam, Zehui Liu) and program mentors are (Dr. Boudreault, Dr. Vogler and Dr. Kushalngaer) All of the sensitive data will be appropriately disposed of after the content is no longer needed or up to 7 years. There will be no identifying data that will be discussed about the participants in reporting the results.

The Ableplayer tool is available on [GitHub](https://github.com/ahui9605/ableplayer-example), but only the source code for it is provided; the video footages, sign interpreters, and captions that we use are not available at this time
Please see the manul on how to set up the Able Player tool for educational purposes: [Click here](https://github.com/ahui9605/ableplayer-example)

### Acknowledgements

This work has been generously supported by NSF REU Site Grants (#1757836 and #2150429) awarded to Dr. Raja Kushalnagar, PI and Dr. Christian Vogler, Co-PI.
Special thanks to Lizzie from RIT with many supports and ideas on Ableplayer
Special thanks to Afzal with technical assistance on jQuery and JavaScript during the development stage of Ableplayer

### References

<table>
    <tr>
        <td>Bosch-Baliarda, M., Soler-Vilageliu, O., & Orero, P. (2020). Sign language interpreting on TV: A reception study of visual screen exploration in deaf signing users. MonTI. Monografías De Traducción e Interpretación, (12), 108–143. https://doi.org/10.6035/monti.2020.12.04
        </td>
    </tr>
        <tr>
        <td>Debevc, M., Milošević, D., & Kožuh, I. (2015). A comparison of comprehension processes in sign language interpreter videos with or without captions. PLOS ONE, 10(5). https://doi.org/10.1371/journal.pone.0127577
        </td>
    </tr>
        <tr>
        <td>Cronin, B. J. (2013, April 22). Chapter 14: Closed-caption television: Today and Tomorrow. American Annals of the Deaf. Retrieved June 7, 2022, from https://muse.jhu.edu/article/386799/pdf
        </td>
    </tr>
        <tr>
        <td>Huang, C.-wei. (2003). Automatic Closed Caption Alignment Based on Speech Recognition Transcript. CiteSeerX. Retrieved June 7, 2022, from http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.233.419
        </td>
    </tr>
            <tr>
        <td>Yi, J. H., et al. (2021). Design Proposal for Sign Language Services in TV Broadcasting from the Perspective of People Who Are Deaf or Hard of Hearing. Applied Sciences, 11(23), 11211. https://doi.org/10.3390/app112311211
        </td>
    </tr>
            <tr>
        <td>Brooke, John. (2013). SUS: a retrospective. Journal of Usability Studies. 8. 29-40.
        </td>
    </tr>
            <tr>
        <td>Brooke, J. (1986). “SUS: a “quick and dirty” usability scale”. In P. W. Jordan, B. Thomas, B. A. Weerdmeester, & A. L. McClelland (eds.). Usability Evaluation in Industry. London: Taylor and Francis.
        </td>
    </tr>
            <tr>
        <td>https://www.youtube.com/watch?v=Z2O3mYNxjHM. (2022). [Youtube Video].
        </td>
    </tr>
</table>
