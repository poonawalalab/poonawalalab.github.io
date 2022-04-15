---
layout: page
title: Resources
permalink: /resources/
---
Contents:
* [Introduction](#lab_introduction)
* [Lab Organization and Policies](#lab_policies)
  * [Diversity and Inclusion](#lab_divincl)
  * [Work Hours](#lab_hours)
  * [Forms](#forms)
* [Preparing Manuscripts](#lab_manuscripts)  
  * [General Planning](#lab_paperplanning)
  * [Typesetting Software](#lab_typesetting)
  * [Mathematical Equations](#lab_matheqns)
* [Creating Software](#creating_software)
  * [The Agile Method](#lab_agilesoftware)
  * [Use Version Control](#lab_versioncontrol)
  * [Comment and Document](#lab_commdoc)
* [Study Resources](#study)
  * [Math](#basicstudy)  
  * [Engineering](#enggstudy)

<h2 id = "lab_introduction">Introduction </h2>

My goal is to foster an environment of consistent research excellence and personal development that supports all lab members in achieving their goals and potential. This webpage contains information that will help you and other lab members, including me, achieve that goal together. Any suggestions and improvements are welcome.

<h2 id = "lab_policies">Lab Organization and Policies </h2>

<h3 id = "lab_divincl"> Diversity and Inclusion  </h3>
Lab membership is open to people of all backgrounds, and discrimination or prejudicial behavior will not be tolerated. If members make comments or actions that are derogatory, please bring it to my attention. You always have the right to object to such behavior.  

<h3 id = "lab_hours"> Work Hours </h3>
Lab members are not required to work on a fixed schedule. This flexibility is a prominent feature in academia. Instead, I expect that you will put in the work required to achieve research goals. Part of your training during graduate school is learn to do so within a reasonable amount of time and effort.

I highly recommend developing a framework for time management that allows you to take full advantage of opportunities both inside and outside of your role as a lab member. If you are finding it difficult to adapt to the flexibility, seek help from me or any other appropriate campus resource sooner rather than later.

[//]:<h3> Computers  </h3>

[//]:<h3> Research </h3>

[//]:<h3> Graduate Studies </h3>

[//]:<h3> Publishing </h3>

[//]: <h4> Why do we publish? </h4>
[//]: The system of peer-reviewed publication forms an organization of knowledge. This organization allows people to find and use our ideas, so that we have impact on a field. In addition, it provides a record of the valuable ideas we created, encouraging others to invest more resources in helping us develop ideas we value.
[//]: <h4> How much is enough? </h4>
[//]: Research productivity is often nonlinear and unpredictable. Instead, the focus will be on making clear plans for conducting research, and demonstrating a best effort to sticking to these plans.


<h3 id="forms">Forms</h3>
* Purchasing:
  * To facilitate purchasing, we need to provide ME department with either a link (or links) to a readily available object, or a quote.
  * For each vendor, we should also fill this [purchase order form]({{site.url}}/{{site.baseurl}}/assets/pdf/ME_purchase_order_form.pdf).
    * Fill the form as best as you can.
    * For the vendor, focus on name and website.
    * Fill in the description and justification of purchase.
  * This order form needs to be attached to an email sent to me that contains the links.
    * One order form per vendor (eg. Amazon, McMaster-Carr,Digi-Key).
    * The email must contain links to the items to be purchased, or to a shopping cart if obtaining multiple items from a single place.

<h2  id="lab_manuscripts">Preparing Manuscripts </h2>
A significant portion of your output during graduate school will consist of research articles published in conference proceedings and journals. Preparing manuscripts for submission can be straightforward or tedious, depending on the amount of planning involved from the start of the research project.
<h3 id = " lab_paperplanning"> General Planning </h3>
[Devi Parikh](https://medium.com/@deviparikh/planning-paper-writing-553f497e8839) has a good framework for planning to finish a high-quality research paper before a targeted deadline.
<h3 id="lab_typesetting"> Typesetting Software </h3>
We exclusively use <a href="https://www.ctan.org" >TeX</a> for preparing manuscripts. Your progress will require gaining competency in creating documents using TeX, and doing so efficiently.

<h3 id="lab_matheqns" > Mathematical Equations </h3>
Some good pointers on writing math well can be found in the links below.
<ul>
<li> Note by <a href = "https://math.mit.edu/~poonen/papers/writing.pdf" >Bjorn Poonen</a> </li>
<li> Note by <a href = "https://web.cs.ucdavis.edu/~amenta/w10/writingman.pdf">Kevin Lee</a> </li>
<li> Note by <a href = "http://www2.gcc.edu/dept/math/faculty/bancrofted/teaching/handouts/math_writing_rules_tips_for_discrete.pdf">Annalisa Crannell</a> </li>
</ul>

<h2 id="creating_software">Creating Software</h2>

Writing software requires a careful consideration of the objectives for that software, and an awareness of the cost-benefit tradeoff. It makes sense to invest in your code being reliable. If you anticipate using the code for a few days, you may not want to worry about extensions or modularity. If this code is going to be used repeatedly in different contexts, then it is worth thinking about how to make code chunks modular, consistent, reusable, and extensible.


<h3 id = "lab_agilesoftware"> The Agile method </h3>
Taken from  [this paper](https://arxiv.org/pdf/1506.05272.pdf) :

<p >One specific agile methodology referred to in this work is derived from ’eXtreme programming’ comprising test-driven development and pair programming. Test-driven development involves writing a failing test for a desired functionality, prior to implementing any source code. Functionality is then added to the source code until the test passes. This ensures a good degree of test coverage for the code. In this work we distinguish between unit tests and functional tests. Unit tests cover small units of the code, for example individual classes and methods, while functional tests are more involved scripts that use the code as a black box to verify correctness of a certain functionality. The latter can also be useful to identify sudden regressions in overall accuracy. Pair programming [5, 40] is a form of code review in which two developers simultaneously work on the same code, and work-station. One developer writes code and the other reviews it. This helps to capture errors efficiently and also helps less experienced developers learn the code and development practices.</p>

<h3 id = "lab_versioncontrol"> Use Version control </h3>

I use [git](https://git-scm.com) to track versions of papers and software over time. There are several tutorials online. A quick introduction can be found [here](https://rogerdudler.github.io/git-guide/), and a longer video-based lecture [here](https://missing.csail.mit.edu/2020/version-control/). Often, one does not need a remote repository. However, if a reliable server is available, why not?

<h3 id = "lab_commdoc"> Comment and Document </h3>
<p>Spend some time documenting working code: how to run it, what inputs it expects, failure cases etc. </p>

<p>Code in a research lab is often re-run long after it is created. For example, when it's time to run a slightly different version of a simulation to address reviewer's comments on a journal paper. At this point, every comment about what the next line few lines does will save you a huge amount of time. When you write those lines, it may have seemed obvious and not worth commenting upon. Therefore, comment liberally yet effectively as you create code. For example, if 20+ lines of code are trying to solve a nonlinear equation and choose one out of n expected solutions, mention the equation and the criteria for selection in a comment before these lines. </p>


<h2 id="study">Study Resources</h2>

<h3 id="basicstudy">Math</h3>
Robotics requires comfort with multiple areas, in addition to a core competency. Below are links to some resources for learning basics in these areas:

* See [these notes](https://www.user.tu-berlin.de/mtoussai/teaching/Lecture-Maths.pdf) that quickly introduces all three topics below.
* You must **master** Linear Algebra. Definitely complete Gilbert Strang's [course](https://ocw.mit.edu/courses/mathematics/18-06-linear-algebra-spring-2010/).
* Elementary real and complex analysis (barely covered in undergraduate calculus). Any interaction with theory in robotics requires comfort with these topics. Most academic libraries will have a good resource.
  * For a more complete treatment:
    * Basic: 'Introduction to Analysis', by William R. Wade. Topics:
    * Advanced: 'Introductory Real Analysis' by A. N. Komlmogorov
* Optimization.
  * There are many optimization problems and methods to solve them. Like many other roboticists, we focus on a subset for which there are reliable algorithms:
    * [Convex Optimization](https://web.stanford.edu/~boyd/cvxbook/). Read this book in detail.  

<h3 id="enggstudy">Engineering</h3>

* [Linear Systems Course by Stephen Boyd](https://stanford.edu/class/ee363/courseinfo.html)
  * Partially taught in ME 645
* Control Theory basics: ([youtube](https://www.youtube.com/watch?v=aLlbwk68-tw)) 
* ME Robotics Course ([website](https://poonawalalab.github.io/rmc-s21/))
  * If you are at UK, I also recommend Dr. Biyun Xie's course 'EE 599 Introduction to Robotics' course that focuses on kinematics of robotic mechanisms.
* Machine Learning
  * Read the **introductions** of [this book](https://mlstory.org/) and [this book](
https://web.stanford.edu/~hastie/Papers/ESLII.pdf).
  * Complete Andrew Ng's [course](https://www.coursera.org/learn/machine-learning) that introduces concepts
  * For coding skills, go through [Machine Learning with Python](https://www.coursera.org/learn/machine-learning-with-python) (copy in lab).
  * For an online course, [this intro to DL]( http://introtodeeplearning.com).
  * This [deep learning textbook](https://www.deeplearningbook.org/) is in the lab.
