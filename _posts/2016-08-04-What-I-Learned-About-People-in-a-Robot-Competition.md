---
categories: blog
author: anderote
---

# Engineering Physics Robot Competition

The [2016 ENPH-253 Robot competition](https://apsc.ubc.ca/news/2016/08/student-designed-robots-face-annual-competition) was overall, an amazing experience. In brief, it was a 6-week ultra-condensed course where teams of 4 competed to build fully autonomous robots that navigated a miniature city, detect passengers, pick them up, and drop them off at a specific location. Basically, 'Uber Bots.' You can see our finished robot at the [fighting Squid's Personal Homepage](https://fighting-squid.github.io/). There was tons of technical lessons learned, as one would expect, but the distinguishing feature in my mind was also observing different team dynamics. I'm greatly curious on how different social dynamics produce differing technical outcomes, and the process of teamwork which ties to the two together.Here are some of my observations (verbose mode =1).

### 1: You can't build a house out of pillars

<center>
	<img src="../../images/post-resources/pillars.jpg" alt="greek made bad robots" align="middle" width="600">
</center>

*Note: This is not a house*
{: style="text-align: center;"}

Engineering Physics is replete with talented individuals, and I'm lucky to be able to learn from them. That being said, there were teams made of individuals who certainly qualified as geniuses individually, but weren't able to collaborate effectively to tackle problems. What seems like an obvious solution to one person might be indecipherable to another.

Moreover, with a challenge that requires close integration of electrical, mechanical, and software systems, the design of each has to acknowledge the overall plan - for that reason, teams which relied on individuals hammering away at what they did best without regard to what other team members were working on often had problems with integration. 

This extends beyond simply workflow, and into the social dynamic of a team as well. Teams that are socially integrated benefit from:
- Efficient communication of ideas, less barriers to information sharing
- Increased ability of teammates to learn from one another, and extend competencies into new areas (never underestimate the ability of a naive question to challenge hidden assumptions in the design process)
- Higher morale, and with it, better uniformity in commitment, dedication, and enthhusiasm. 

### 2: Hold The Line, or, Proceed in Phases

<center>
	<img src="../../images/post-resources/hoplites.jpg" alt="greeks made bad robots" align="middle" width="600">
</center>

*Hoplites are Bronze Age warriors that pre-dated written language, as such, would likely fail this course*
{: style="text-align: center;"}

As general Maximus said in Gladiator, a team must hold the line. In the context of a small team working on a technical project, it means one section shouldn't race ahead of the others. Rather, where its feasible, teams should focus collectively on a single phase of the problem solving process before proceeding to the next phase collectively. 

Planning is everything, but the plan is nothing. In that regard it might seem reasonable that with sufficient advanced planning sections could be completed almost independently. Unfortunately, things never seem to work out that way - with an integrated project design changes in one area will propagate through the rest of the system. Working in phases, as a team, reduces this risk as obstacles and hurdles at each phase are identified as a group, communicated clearly, and other systems can be brought up to date or, even better, haven't been built or designed-in-detail yet. Phasing produces flexibility in the interfaces between phases, since you're building on top of a previous layer, not meshing two structures together.

There are a few more 'micro' reasons I'd encourage small-sized teams to 'hold the line,' i.e. work collectively on a single phase before proceeding, especially in settings where there aren't insurmountable skillset differences:

- Team leads for electrical, mechanical, and software are involved in each phase and can veto decisions in one area that will conflict in non-obvious ways with another
- Automatically improves the ability of systems to integrate with one another during assembly, reducing the likelihood of compatibility issues
- Increases the flexibility of manpower to focus on hotspots, bottlenecks, reduces 'idle' teammates when their section is 'done'. There were many teams who, after completing the mechanical design and assembly, had 'mech people' idle while software was shorthanded and under extreme pressure to deliver. 
- There's a caveat: A team must leverage special talents, not every person has to know 100% of every system, but, should have enough familiarity to attempt debugging / troubleshooting medium-sized issues, and most importantly, *has developed intuition for each system and how it **should** operate.*


### 3: Live inside the Device, or, Re-scale the Space

This is largely related to the physical / mechanical design component, and was inspired by one team that far surpassed all the others in their ability to integrate in a compact way all the electronics, motors, sensors, and circuitry in a small space. They did so by spending dozens and dozens of hours in SolidWorks, meticulously planning and fitting pieces together. It was clear they had a fundamental distinction in physical design - all the space was utilized, things fit together exactly, and it looked beautiful. 

 It easy develop a mental model of a house, and navigate it in three dimensions - the scale is familiar, there are 'person sized' objects in three dimensions. Small devices are a lot different, we are accustomed in large part to conceiving of small things in a two-dimensional context: 2-dimensional design on planar surfaces is lazy, easy, tempting, and overall wasteful. 

 SolidWorks offers a unique advantage in its ability to re-scale physical space - suddenly, that 10 cubic centimeters is as big as a house, and it becomes painfully obvious at what space is wasted and what is used. Unless you have experience as a Swiss clockmaker, its unlikely you've developed significant intuition for 3-dimensional design and thinking at very small scales. For that reason, its important to take the time and model in detail all the parts of the robot, even down to nuts and bolts. 

 Your team should be able to visualize themselves in the device, to look around from one corner and know what they'll see. This can only come from significant investment in SolidWorks or other CAD design, to the point where wasted space is glaringly obvious. 

## 4: Listen without Following

Throughout the design and construction process the TA's in the Engineering Design Course were immensely helpful as sources of knowledge and advice. Frequently they had suggestions, insights, and experiences in practical know-how that went above and beyond the call of duty. That being said, in the design process there usually isn't a single "Right Answer" that they can readily provide - indeed, it was tempting to ask "well, what should I do?" - luckily, they were wise enough not to answer that question directly.

What often did happen was they would offer a series of suggestions, or alternatives, or bring up a list of considerations. This is something I faced in previous design situations building a couple simple components to help out with the [Laboratory for Atomic Imagine Reasearch](http://lair.phas.ubc.ca/). The best answer to the question "What should I do?" is almost always: "It depends" - what's the use case, what are the limitations, what are the physical requirements in strength or durability, the list goes on. 

The difficulty is in parsing your source of advice for what's relevant to your application. They are speaking from personal experience that may or may not coincide with the application in hand, in other words, the applicability of an advisors experience is a function of the overlap between their reference knowledge and your current problem. What's particularly difficult as a junior designer is knowing just how relevant their experience is, so, probe. Probe their knowledge, if they say "spot welding is usually the easiest joining method for sheet metal" - ask, did alignment matter? did you need a clean surface afterwards? what were you spot welding for?

So, when should you take another person's design advice, well, "it depends."

## 5: A Team is All or Nothing
<center>
	<img src="../../images/post-resources/ants.jpg" alt="ants work as a team" align="middle" width="600">
</center>
*Ants' teamwork is motivated by blind adherence to pheremones, a surefire means of designing a terrible robot*
{: style="text-align: center;"}

For a team-based project, this usually goes without saying, but I'll say it anyway: Everyone needs to be a team player. Not just a team player, but there needs to be a high degree of social lubrication between team members - they should get along, genuinely enjoy each other's company, be willing to reveal doubts, insecurities, and vulnerabilities. A hostile or overbearing attitude on one person's part might scare others into not speaking up, and if a team member can't give feedback then you have an open-loop system. Anyone who's even seen a control-systems signal flow diagram can tell you, open-loop systems are not a good thing for system stability.

Effective team-playing really comes down to communication, and the mutual understanding it brings. Disagreements are inevitable, and in high stress scenarios, emotions are bound to flare. Communication is the 'pressure valve' by which disputes are resolved, personal feelings amended, and provide a means to collectively move forward. Without a clear and open means of resolving interpersonal differences, resentment is inevitable. Resentment breeds mistrust and leads team members to start discounting each other's technical suggestions or ideas, reducing the teams ability to pivot or adopt improvements. Additionally, they detract from focus on the tasks at hand - instead of debugging a circuit or designing a replacement part, team members might spend time stewing over a personal grievance, or even worse, 'balkanizing' into factions and bad-mouthing each other behind backs. 

Stifled communication channels also lead to misunderstandings between members about expectations, especially with regards to commitments and obligations. The more committed feel resentful towards those they feel are 'slackers,' while the complementary response is to feel overpressured, that you're working with 'slave drivers.' 

Perhaps the biggest risk with mis-aligned expectations of commitment is the differential skills development it leads to as the project progresses - some become subject area masters, while others increasingly fall behind. Like I mentioned earlier, the utility of person's input is a function of the overlap between their reference experience and the obstacles you face presently, and team members left behind are quickly relegated to 'non-critical roles.' In effect, differential skills acquisition induces artifical and unplanned role specialization across team members, bringing with it the inability to address hotspots or bottlenecks in mission-critical areas and leaving part of your human resource base idling during times of need. 