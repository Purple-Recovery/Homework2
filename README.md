# Homework 2: Designing a Solution
**Purple Recovery**

## Problem

Right now, the University of Washington’s official statistics, resources, and other responses are scattered (via department, college, unit, etc). After conducting internal user research, our organization found it difficult to navigate the FAQs and resources meant to make UW Seattle student lives easier during this time of uncertainty. This poses problems to students as they might need to do a lot of searching and jumping around different webpages, emails, and social media posts. 

The [UW's “COVID-19 Landing Page”](https://www.washington.edu/coronavirus/) currently aims to provide a one-stop, although it is not as comprehensive as it could be. This seems to be missing: university buildings’ hours, resources that are staying open, lack of RSO information, and where to turn for academic support. 

### Literary Research

According to researchers at [Cambridge University](https://www.cambridge.org/core/journals/disaster-medicine-and-public-health-preparedness/article/do-pandemic-preparedness-planning-systems-ignore-critical-community-and-locallevel-operational-challenges/D472C569D002A2525F941B537D1E9064), “pandemic preparedness planning systems ignore the critical community and local-level operational challenges”. It is clear that the University of Washington, its students, and its local community are directly affected by a swirl of information that became immediately available, but not necessarily easy to navigate in a single space. The current information system does a disservice in the lack of additional resources for community members who are still in the area as well during this pandemic. 

### Heuristic Evaluation

The UW COVID-19 page is quite text-heavy and scroll-reliant, and the interface for the FAQs is in a list view, making browsing a challenge. To get a clearer view of this, we performed a heuristic evaluation of the following metrics, adapted from [Nielsen and Molich’s 10 UI Design Heuristics](https://www.interaction-design.org/literature/article/heuristic-evaluation-how-to-conduct-a-heuristic-evaluation):

**Visibility of system status** 

* While a fairly simple system, there is an italicized subtitle under the main header that displays the last date and time that the page was updated. 

**Match between system and the real world**
 
* The “system” is a web page with lots of text, divided into a traditional two-column layout: 
	* Left column has most of the information 
		* A top text-based nav, each one leading to a different FAQ section (three out of the five hyperlinked options do NOT match FAQ title, e.g. “What to do if you feel sick” leads to “Health, wellness, and prevention”, but does match the first question in the section
		* Paragraphs
		* Expandable FAQs
	* Right column is more narrow
		* “Spring Quarter Resources” + hyperlinked button
		* Messages and Updates (list view of hyperlinks and dates to various “official statements” and past blog posts from Ana Mari)
		* Testing Results + hyperlinked button
		* Resources + hyperlinked button

**User control and freedom**

* Backward steps are only possible via scrolling back to specific section

**Consistency and standards**

* Webpage has graphic elements and terminology that are maintained across similar platforms/i.e. UW branding is very clear

**Recognition rather than recall; flexibility and efficiency of use**

* Navigating the page relies a lot on user’s cognitive load
* Very reliant on scrolling; no clear markers/indicators on how to jump between sections, aside from expandable individual FAQs
* FAQ section has 11 sections; the biggest section has 17 questions (all in a list view)
* Only has a top text-based nav for FAQs (seem to be quick links) and a more comprehensive FAQs table of contents; both are non-sticky/disappear after one-page scroll

**Aesthetic and minimalist design**

* While no “unnecessary” information, interface comes across as cluttered because there is a lot of information

### Competitive Analysis

We also started working on a competitive analysis of other university COVID-19 information portals and usability testing on UW's COVID-19 page. Specifically, we took a look at the University of California Berkeley's portal for student accessible information on the Corona virus outbreak. It is broken up between resource categories and dates of updates. The header also contains a banner relaying the most recent update to university operations and resource posts. Like UW's own page, when each section is expanded in the Berkeley site it creates a large drop down of explanations and also helpful links. We hope to implement findings from both in later iterations of our solution.

### Usability Tests

We were able to conduct 5 usability tests. Here are our main findings:

![usability test findings](img/usability_tests.png)

Out of 6 basic tasks, 3 had a struggle or failure rate of 50% (info on study abroad, what to do if showing COVID-19 symptoms, Odegaard status), 1 had 75% (navigate to COVID-19 page from UW home page), and 2 had 100% (navigate to UW COVID-19 cases dashboard, finding online tutoring). 
 
## Solution

We envision a section-based dashboard for our solution.

![main dashboard](img/main_dashboard.png)	
Upon opening the portal, users are greeted with UW COVID-19 Information organized into categories in a card-view: UW Resources (Official UW Resources), UW Messages (Official UW Messages), Responses (Student/staff pieces, opinion or otherwise), Statistics (Data sources), and Community (Resources and activities meant to  help others connect during self isolation). Each section will have a "more" button bringing the user to a dedicated page for that specific section. (These "more" butons will be more semantically named later in our design process.) Further, there will also be a top banner displaying the most recently posted UW official message. 

![section view](img/section_view.png)

When clicking the “More” buttons, the user will be taken to that section’s own page, which would have more detailed links. Under each section header there will be "breadcrumbs" of where the user currenlty is in the web app, to ensure a sense of system location. There is then also a side pseudo-navigation just in case the user needs to view another section. This side nav will be sticky and always available to the user regardless of their scroll position. 

![submit a resource form](img/submit_form.png)

Users can also submit resources that may not be available on our web app. We hope that by including this feature, that the UW community would be more compelled to share virtual events that may happening. These events are usually on Facebook or segregated from each department. In these isolating times, it would be beneficial for the community to gather together even if it is on a virtual plane.


