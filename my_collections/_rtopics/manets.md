---
title: Control of Dynamic Multi-Robot Networks
layout: rtopic
thumb: manet.png
date: 2013-09-01
status: preuk
---
<h2>Control of Dynamic Networks</h2>
<ul>
<li><p>When the mobile robot network is directed, how do you identify which links need to be preserved to maintain properties like strong connectivity of the network?</p>
</li>
<li><p>Is there a smooth control law that can guarantee that desired edges are preserved in the presence of disturbances? Can this control law be designed to interfere as little as possible with other control goals?</p>
</li>
</ul>
<p>Prior to my work, most techniques preserved all existing edges, which restricts the possible topologies that the network can exhibit in the future. Furthermore, most control laws were based on potential functions which typically resulted in discontinuous control commands when new edges were created.</p>
<div align="center"><img src="{{site.url}}/{{site.baseurl}}/assets/img/manet.png" alt="" width="255px" height="205px" /><p text-align="center"> Heterogenous Mobile Robot Communication Network. </p></div>

<h3>Experimental validation:</h3>
<p>We evaluated the influence of the additional connectivity controller on the closed-loop behavior of a team of wheeled mobile robots. For example, we command five mobile robots to move to a location, while a sixth mobile robot has no task assigned to it. Under the influence of the connectivity control, it moves towards the remaining robots only when they begin to move outside of its simulated communication range.</p>
<div align="center"><iframe  width="420" height="315" src = "http://www.youtube.com/embed/8VoW_5Lb-00" frameborder="0" allowfullscreen></iframe></div>
