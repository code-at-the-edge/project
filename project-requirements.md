# Code at the Edge Project Requirements and Guiding Concerns

_Last updated: December 3, 2018_

- [Who and what is this about?](#who-and-what-is-this-about)
  - [School and Classroom Setting](#school-and-classroom-setting)
  - [Stakeholders/collaborators](#stakeholderscollaborators)
- [Why are we taking this on?](#why-are-we-taking-this-on)
  - [Why does it matter?](#why-does-it-matter)
  - [What already exists in this space?](#what-already-exists-in-this-space)
    - [Code Playgrounds](#code-playgrounds)
    - [Teaching Tech Projects](#teaching-tech-projects)
- [How are we going to do it?](#how-are-we-going-to-do-it)
  - [Initial use case](#initial-use-case)
  - [Mature use case](#mature-use-case)
  - [Features and “non-functional” requirements](#features-and-non-functional-requirements)
- [Understanding (assessing) our Involvement](#understanding-assessing-our-involvement)
- [Expected Outcomes](#expected-outcomes)
- [Project Timeline and Key Dates](#project-timeline-and-key-dates)
- [Appendix: Links and Resources](#appendix-links-and-resources)

# Who and what is this about?
 
[Code at the Edge](https://code-at-the-edge.github.io/) came out of a May 2018 HTML/CSS workshop at the [Kasturba Gandhi Balika Vidyalay (KGBV)](https://en.wikipedia.org/wiki/Kasturba_Gandhi_Balika_Vidyalaya) School for Girls in [Labing, West Sikkim, India](https://goo.gl/maps/uFuVJgcRg182), that a group from a University of Toronto [research project](https://khangchendzonga.github.io/) had the great privilege to conduct. The workshop was a great success, and we would like to explore a deeper and more sustained relationship. This project is our effort to continue and deepen that collaboration.

[West Sikkim](http://www.census2011.co.in/census/district/462-west-sikkim.html) is of particular interest because of its location on what might be called "the edge of the Internet". Internet access in rural West Sikkim is currently only possible through cellular telephone signals. Because of the extremely hilly topography of Sikkim, which lies entirely within the Himalayan mountain range, cell service tends to be somewhat unreliable. However, fiberoptic cable is being laid in the district and over the next several years Internet access will expand dramatically. The district is also replete with small businesses, many in the tourism trade; a substantial fraction of these businesses have no web presence at all. There is very limited web development expertise in the region.

## School and Classroom Setting

KGBV schools are a special program of the national Government of India aimed at educating girls from poor and disadvantaged backgrounds. There are over 3,000 KGBV schools in India, but only one in the state of Sikkim. In West Sikkim, the school serves approximately 200 girls between the ages of 12 and 16, mostly from very poor backgrounds. The school itself is a group of recently-constructed concrete buildings inset on a steep hill above the main dirt road between Labang and Yuksom. Students live here full-time and the staff mostly commute by taxi from the village.

![Classroom Photo](https://www.dropbox.com/s/g93uxububan264q/IMG_0308.jpg?raw=1)
_This photo shows the clasroom setup and gives a sense of the networking hardware, the PC form factor, etc._

The computer lab is on the second floor of the building and contains 10 small form-factor desktop PCs, running an unknown version of Windows with both IE and Chrome browsers installed. For our workshop there were 50 students & we brought 5 laptops with us, so there were about 3.3 students/computer.

There's a wired-only router in the classroom (visible on wall in the image) and we brought a [cheap SIM-equipped travel router](https://www.amazon.ca/gp/product/B07712LKJM/ref=oh_aui_search_detailpage?ie=UTF8&psc=1) to connect the laptops and our Raspberry Pi (see below) to the network. We were unable to get a reliable cell signal in the classroom, and the desktop PC's appear to have been set up at another loation and never connected to the Internet _in situ_. This is not surprising given the Internet connectivity landscape described above. 

Maintenance of computer hardware appears to be the responsibility of the IT teacher, but that position seems to be a short-term part-time contract and to rotate frequently. It's unclear how, or if, software updates are applied to the PCs. One interesting question is whether and how broken hardware is repaired. 

## Stakeholders/collaborators 

At present, the following groups have some level of commitment to the project: 
- [KGBV](https://en.wikipedia.org/wiki/Kasturba_Gandhi_Balika_Vidyalaya) School for Girls in Labang.  
    - **Contacts:** Mr. Tamang (teacher), Ms. Mohra (principal)
    - **Aims:** intellectual development and economic opportunity for students (200 girls age 12-16)
- Khangchendzonga Conservation Committee (KCC)
    - **Contacts:** Uden Bhutia, Kinzong Bhutia, Pema
    - Website: [kccsikkim.org](http://kccsikkim.org/)
    - Facebook: [facebook.com/pg/kcc.sikkim/](https://www.facebook.com/pg/kcc.sikkim/about/?ref=page_internal)
    - **Aims:** sustainable eco-development of the region
- [Code at the Edge//Himalayan Borderlands Project Team](https://khangchendzonga.github.io/#team)
    - **Contacts:** [Matt](mailto:matt.price@utoronto.ca) (CatE project lead), Frances (PI), Farzad, Laila, Dawn (team members), University of Toronto (UofT), in Toronto, Ontario

Potential Collaborators:
- Steam Labs members (D, B, U) working on education+tech projects in nearby region
- Teaching Tech Together meetup 
- Code Playground developers
    - [Web-Maker](https://github.com/chinchang/web-maker/) developer has expressed interest

# Why are we taking this on?

"Sometimes you do a project, not becaue you're the best person in the world to do it, but beause you happen to be the person who's there." (Matt)

Our connection to the KGBV in Labang was made in a roundabout way, but when Matt and Frances had the opportunity to teach there in May 2018, we began to think about ways to strengthen our connection and mobilize our exprtise and skills to enhance opportunities for students enrolled there. **Frances** has spent years in and out of the Himalaya and has a strong commitment to the region. **Matt** has spent years teaching basic web development skills in non-traditional contexts in Canada, and has recently been involved in a couple of organizations ([EDGI](https://envirodatagov.org/), [Data Together](https://datatogether.org/)) with an interest in [questions of digital equity and justice](https://envirodatagov.org/environmental-data-justice/) and [the decentralized web or "dweb"](https://hacks.mozilla.org/2018/07/introducing-the-d-web/). **KGBV staff** expressed great enthusiasm about the HTML workshop we were able to put on at the school.

We wondered: could we, in this one place of Labang, help make the world of web development and the Internet itself a more just and equitable place? What might it mean if, when fiberoptic connectivity arrives there, the best-trained and most highly-skilled web devs were a group of 18-year-old girls from the very poorest backgrounds in the region? 

## Why does it matter?

- Acquiring web development skills could have substantial impact on the economic welfare of KGBV students. This likelihood on its own is enough to motivate the project. 

- The teaching process is also an opportunity to develop expertise in school teaching staff and other members of the local community. These ripple effects could be significant.

- If the project is successful, it could be replicated in other similar environments. There are lots of code teaching projects; few of them have grappled with the difficulty of working in remote offline environments. Maybe if we can move skills and knowledge into these regions before the Internet arrives in full force, we can help mitigate some of the web's worst impacts on equity and justice. 

## What already exists in this space?

To better understand the landscape of teaching web development skills, we are looking at _openly licensed_ and _open source_ projects and curriculum:

### Code Playgrounds

#### [Code Pan](https://codepan.net/) ([`codepan` GitHub](https://github.com/egoist/codepan))

Virtues:
- It runs locally and offline

Deficits:
- It does not allow for saving work without external authentication (e.g. GitHub)


#### [Web-Maker](https://webmakerapp.com/) ([`web-maker` GitHub](https://github.com/chinchang/web-maker))
An offline-first code playground designed first for personal use by an Indian developer in Delhi. Uses `localStorage` to save projects locally, while also maintaining a centralized store of project files.

[Documentation](https://webmakerapp.com/docs/#/) and [Development Instructions](https://github.com/chinchang/web-maker/blob/master/CONTRIBUTING.md).

Virtues:
- Works offline as a web-app
- We can serve it on HTTPS
- Allows saving projects into local .json file
- The developer is in reach for furthur assistance and guidance on using the platform

Deficits:
- We still do not know how to ingest material (instructor to student) for pedagogical purposes 
- No persistent URLs, so it's difficult to get assignments & exercises to students
- Database is via Google Firebase, which runs in the cloud :frowning:. So while machine-local projects and cloud-based projects, both are easy, there's no notion of a "classroom" or other middle level or organization 


#### [JSBin](http://jsbin.com/) ([`jsbin` GitHub](https://github.com/jsbin/jsbin))

This was the first tool we used. We have a very hacky fork that bends a small number of variables in order to let us run JSBin in an offline setting (only works so well, but is probably OK for our purposes at least for now).

Virtues: 
- very full-featured
- local SQL account & project data storage (no cloud required)

Deficits:
- Unclear state of development -- transitioning to a next version w/ new tooling, but work seems to have stalled this year
- installation & deployment docs not super-clear
- our changes feel pretty hacky and difficult ot maintain


#### [HTML House](https://html.house/) ([`htmlhouse` GitHub](https://github.com/writeas/htmlhouse))

Virtues:
- uses `LocalStorage` for offline editing
- permanent URL's
- project milestones
- Chrome extension version

Deficits: 
- no separate CSS and JS panes
- requires Go (it's fast, but also needs a bigger non-standard stack & does anyone know what Go is like on an Raspberry Pi?)


#### [Thimble](https://thimble.mozilla.org/) ([`thimble.mozilla.org` GitHub](https://github.com/mozilla/thimble.mozilla.org))

Thimble is a teaching tool from Mozilla's old open web promotion team, not sure how many of those old projects are still maintained, but development on Thimble seems active.

Virtues: 
- oriented towards kids, which is great
- simple interface w/ features that can be revealed one-by-one as skill level advances
- lots of curriculum-like materials already available

Deficits:
- oriented towards a [Scratch](https://scratch.mit.edu/)-like centralized community publishing model, so would probably be difficult to pull apart from the main instance.
- looks a little complicated!
- like all of these projects, no immediately obvious route to ingestion of html/js/css materials that are maintained using standard dev tools (cf. [Features and "non-functional" requirements](#Features-and-“non-functional”-requirements))
- Mozilla has recently [sunset its entire learning project](https://learning.mozilla.org/en-US/)

### Teaching Tech Projects

#### [GirlsCoding](http://girlscoding.com.ng/) Lagos, Nigeria

[GirlsCoding](http://girlscoding.com.ng) is a project of [Pearls Africa Foundation](https://pearlsafrica.org/) that is "passionate about increasing the number of females in STEM, training the girls in underserved community and improving the resourcefulness of young girls and women":

> GirlsCoding is an intense program for young girls, age range; 10-17 years, living in underserved communities in Nigeria; to train them in computer skills, robotics, programing using HTML and Java, connect them to female mentors and then connect them to Tech companies on internship. GirlsCoding make use of brain tasking puzzles from code.org and coderdojo to get our girls started and interested in the program.

See coverage: 
- [Girls Code Their Way Out of Nigeria’s Slums and Into the Tech Sector](https://www.globalcitizen.org/en/content/nigeria-lagos-girls-coding-tech-industry-computers/)

Curriculum:
- Topics include [HTML, CSS, JS, Python, Android and Microsoft](http://girlscoding.com.ng/programs.html)
- Unclear format and instructional hours
- "Short exciting courses and STEM projects"

Open(ly licensed):
- Unclear? Appears to rely on other openly available materials

#### [ReDI School of Digital Integration](https://www.redi-school.org/about-us)

ReDI School of Digital Integration is a non-profit free digital school for tech-interested newcomers in Germany. It offers multiple courses and a women-focused track on topics including frontend web development, html, js, css.

Curriculum:
- Topics include [Digital Career](https://www.redi-school.org/courses) and [Digital Women's Program](https://www.redi-school.org/digitalwomencourses) 
- Semester-based courses
- 4 hrs / week, 10-13 weeks
- 48 instructional hours / course

Open(ly licensed):
- Unclear how complete the openly available materials are
- Some materials available on GitHub: https://github.com/ReDI-School/
    - https://github.com/ReDI-School/js-munich-2018-fall
    - https://github.com/ReDI-School/html-css-munich-2018

#### [Girl Develop It](https://www.girldevelopit.com/) 

**Girl Develop It** is a nonprofit that provides "affordable and judgment-free opportunities for women interested in learning web and software development." They host in-person classes/workshops and convene a community through a chapter model to support "women of diverse backgrounds achieve their technology goals and build confidence in their careers and their every day lives."

Curriculum:
- Topics include: [Web, HTML/CSS, JS, Accessibility, etc](https://www.girldevelopit.com/materials) 
- Workshop-based
- 2 hrs/ workshop, 1-4 workshops / topic
- Up to 8 instructional hours / topic

Open(ly licensed):
- Creative Commons License
- All materials available on GitHub: http://girldevelopit.github.io/gdi-curriculum-site/

#### [Codebar](https://codebar.io/)

"Our goal is to enable underrepresented people to learn programming in a safe and collaborative environment and expand their career opportunities. To achieve this we run free regular workshops, regular one-off events and try to create opportunities for our students making technology and coding more accessible."

Curriculum:
- Topics include: [Web, HTML/CSS, JS, Ruby, Python, Mobile App Development, etc](http://tutorials.codebar.io/)
- Self-guided tutorials
- Unclear instructional hours

Open(ly licensed):
- Creative Commons License
- All materials available on GitHub: https://github.com/codebar/tutorials

#### [Building the P2P Internet](https://tomeshnet.github.io/p2p-internet-workshop/), Toronto, Ontario [`tomeshnet/p2p-internet-workshop` GitHub](https://github.com/tomeshnet/p2p-internet-workshop)

Building the P2P Internet is a six-week offline-first curriculum for learning about community networks, wireless mesh networks, distributed applications, and working with a Raspberry Pi to do networking things.

Curriculum:
- Workshop Series (Course)
- 1.5 hrs / week, 6 weeks
- 9 instructional hours

Open(ly licensed):
- Creative Commons Licensed
- GitHub: https://github.com/tomeshnet/p2p-internet-workshop

#### Free online web development and learn to code curriculum

- [Free Code Camp](https://learn.freecodecamp.org/)
- [Code.org Grade 6-12](https://code.org/student/middle-high)
- [Coderdojo](https://coderdojo.com/)
- [Codecademy](https://www.codecademy.com/)
- [The Odin Project](https://www.theodinproject.com/courses/web-development-101)
- [Khan Academy: Computer Programming](https://www.khanacademy.org/computing)
- [Hack Design: 50 design lessons/toolkit](https://hackdesign.org/lessons101)
- [Learn-JS](http://www.learn-js.org/)


# How are we going to do it?

We address this situation _with_ a package including web development curriculum and teaching materials on a pre-configured Raspberry Pi running hosted software that both teachers and students will access. Our driving goal is: **to create (or modify) and teach a web development curriculum appropriate to the West Sikkim region and the KGBV students we're working with**."

## Initial use case

We are exploring an initial **extended workshop** format to take place in February, 2019. Our emphasis will be on materials that are engaging for students with well-organized notes. This one-week session would have the following goals:
- teach students enough HTML & CSS to build a simple web page with assets &c
- introduce web literacy issues (privacy, trust, verification)
- teach staff enough about the system to enable them to replicate/expand the workshop themselves
- develop takeaways from the workshop (and interviews?) for a future iteration and structure
- Format:
    - 2.5 hours/day over 4-5 days
    - 3 phases in lesson plan
        - introduce skill
        - integrate skill into a "final project"
        - have some sort of web literacy connection
    - curriculum set up in single folder lesson structure with html, js, css file
- Questions to understand:
    - What is the scope of a useful curriculum?
        - What can we teach effectively in setting/timescale?
        - What skills will be most translatable ito opportunities?
    - What do adults in the area need?
        - e.g. Wordpress website?
    - How (critical) are, and how do we build, networks in India to connect to this work?

## Mature use case

- Questions to understand:
    - To what degree are formal CS or Computation thinking concepts required? (e.g. for, while loops, if statements, switches)
    - What is the pathway to efectively set up students to pursue and learn about these topics after we are gone?
    - What is the best pathway to develop a livelihood around web development skills (e.g., partnering with an org? connections with small businesses?)

## Features and "non-functional" requirements

*note: Non-functional Requirements or "NFRs" could include look, usability, humanity, (values), ease of use, learning, environmental/operational, maintainability, support, sustainability, security, cultural*

The system will:
- work independent of access to the web or Internet
- work in a web browser and without having to install applications locally
- allow for export and import of saved work
- provide Uniform Resource Identifiers (URIs) that are shareable and persistant over the course of a workshop and accross devices

Using the system, Students:
- can check the results of their work in realtime
- can save their work and return to it at a later date
- can view teaching materials for each specific lesson

Using the system, Teachers:
- can view instruction/facilitation material for each specific lesson, as well as an overview for all available materials
- can find documentation to support setting up the system
- can easily configure and modify/maintain the system over time
- can both use and modify curriculum materials developed elsewhere

Using the system, Developers:
- can write easily maintainable lessons using widely-available tools and processes (writing in html/css/js/markdown; using local text editors and git version control)
- can support local instructors seeking to improve the system for a given environment
- can iterate rapidly on the technical stack and on the curricular materials


# Understanding (assessing) our Involvement

We aim to assess our involvement along three (four?) facets:

- **Pedagogy**: Was the delivery of the workshop itself a success?
    - *Pre* Teachers pre-workshop interview
    - *During* Summative feedback (?)
    - *Post* Teachers post-workshop paper survey, interview
        - Reflection using...
    - Resources:
        - "Evaluation" Section of [Community Technology Handbook](https://detroitcommunitytech.org/sites/default/files/librarypdfs/TeachingCommunityTech.pdf)
- **Equity/Justice**: Does the project respond to equity needs and build justice in its approach?
    - 10 Lessons in Community Technology (PDF)
    - [Design Justice](http://designjusticenetwork.org/network-principles/) and [Digital Justice](https://www.alliedmedia.org/ddjc/principles) Principles
- **Sustainability**: Is the creation and continuation of this project sustainable?
    - *Post* Reflect on Project "Decision Gates" using those identified in "A Tale of Two Projects" from *Requirements: The key to sustainability* (Becker et al., 2016)
- **Transition/Appropriate**: Does the project bring about (or bring closer) the changes sought? Is it done in a manner 
    - *Pre* Compare against other frameworks, adjust trip protocol
    - *Post* Reflect on Project

# Expected Outcomes

- Delivery of workshop in W. Sikkim with project partners
- Re-usable curriculum package (hardware/software running on Raspberry Pi, Workshop Materials) for "offline-first" and low-connectivity environments
- Research write-up (papers/posters)
- Learn things and have fun together along the way!
    - @faraz: html/css/js basics
    - @dcwalk: curriculum development, pedagogy, esp pedagogy as change; design for appropriation & independence
    - @matt: a feeling of there being something to it, people leave having something (teachers (see this?), students (skills?)), want to make things real instead of fake 
   
# Project Timeline and Key Dates

We imagine this inital phase of the project lasting from October 2018 - May 2019

| WK# | Deadline      |
|-----|---------------|
|     | **NOVEMBER** |
| 45  | **Nov 05** Completed documenting current implementation |
| 46  | **Nov 12**   |
| 47  | **Nov 19** Project requirements and guiding concerns drafted |
| 48  | **Nov 26** <br /> **Go/No-go dec'n on Feb Delivery in Sikkim** <br /> Go/No-go dec'n on research writing venues  <br /> Dec'n on hardware/software stack, curriculum materials format |
|     | **DECEMBER** |
| 49  | **Dec 03**   |
| 50  | **Dec 15** Drafted initial lessons <br /> **Tentative** Research Writing First Draft (CHI, DIS) |
| 51  | XXX OFF! XXX |
| 52  | XXX OFF! XXX |
|**2019**| **JANUARY** |
| 1   | XXX OFF! XXX |
| 2   | **Jan 07** Recieved Curriculum Feedback <br /> **Tentative** Research Writing Submission (CHI, DIS) |
| 3   | **Jan 14** Developed Raspberry Pi prototype |
| 4   | **Jan 21** Workshop Test Run!   |
| 5   |    |
|     | **FEBRUARY** |
| 6   |    |
| 7   |    |
| 8   | **Feb 16-24** **Tentative** Project teaching in Sikkim |
| 9   |    |
|     | **MARCH** |
| 10   | Project reflection   |

Important documents:

[Code at the Edge Trip Guide](https://hackmd.io/GDr2pz-QRvqzjZxG8_C_FA?both)

# Appendix: Links and Resources

Understanding Internet/network coverage:
- [nperf maps](https://www.nperf.com/en/map/IN/-/7905.Idea-Cellular/signal/?ll=27.305282414108248&lg=88.28407287597656&zoom=12)
- [OpenSignal App](https://opensignal.com/networks)
- [Telecom Regulatory Authority of India (TRAI))](https://trai.gov.in/)
- [Bharat fiber laying project](https://en.wikipedia.org/wiki/Bharat_Broadband_Network)
- [Record of tender for cable pulling](https://www.tendertiger.com/viewtenderdetail.aspx?SrNo=29017257&tendertype=9d09819bf4266dce2eviL&Year=2016&tenders+sikkim)
- [Telecom Infrastructure Augmentation In North Eastern States Report from 2014](http://www.usof.gov.in/usof-cms/GagendaPdf/Revised%202014%2004%2009%20DPR%20North%20East%20Highway%202G%20Project.pdf)

Public information about KGBV school in Labing:
- [West Bengal Library Network on KGBV scheme](http://www.wbpublibnet.gov.in/node/292)
- [Central Board of Secondary Education (CBSE) on KGBV Labing School](http://www.icbse.com/schools/kasturba-gandhi-balika-vidalaya/11020601002)
- [Coverage of Gram Panchayat (local govt) offices](http://164.100.47.190/loksabhaquestions/annex/12/AU2965.pdf)
