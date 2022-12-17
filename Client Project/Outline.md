# Greenhouse Generative AI Project
Greenhouse didn't give us a very clear objective, instead only asking us to investigate potential applications. While a bit daunting, this was also very exciting: it meant we had a lot of freedom to give a personal touch to the project. Generative AI has incredible potential, and is currently at the point where it is relatively accessible, which meant we had a lot of options. Initial brainstorming quickly showed that we were all interested in helping out Greenhouse employees somehow, and our project was born from there.

## Project Details
Our mission goal is to use generative AI to empower Greenhouse employees. Empower is a key word here: to us, it means that we not only inspire employees, but also help them be more creative by positively influencing their mood and state of mind.

To do this, we want to create a place where employees can go to find inspiration for a project they're working on. They'll enter a room, where they can provide any prompt they want, and based on their input AI generated images and text will be projected on the walls, accompanied by AI generated music. Our goal is not only to provide direct ideas through the AI images, but to also serve as a space that helps employees relax or be more productive.

## Project Progress

### Sprint 1: Initial Exploration, Ideation, and Research
Much of our early work was based on casting a wide net around the subject of generative AI. While I knew about it and had been following its progress, none of our group had worked with the technology before, so much of our early reading was into what generative AI can do and how we could potentially use it.
We also tried to consider the future - where would AI be headed, and how could we prepare for that. In the end, we discovered that AI is very good at generating images, text, and to a lesser extend music and sound, but as of right now there is no AI capable of automatically combining those. This served our purposes well enough however, as we could manually generate and combine the different elements.

![AI Directions]()

I also researched training our own custom image model; this could potentially be very powerful, because we would have a lot more control over what our output would be, but this proved more difficult than I'd hoped. Model training is definitely more accessible than it used to be, but is still a significant challenge, and unfortunately outside of the scope of this project. Besides, when it comes to inspiring people having a very large range of potential output isn't necessarily a disadvantage.

During all this, we also spent time brainstorming about what we wanted to actually accomplish with the generative AI. Initially we were looking at the assignment from a lot of different angles - directly generating personalised advertising, prototyping, even collaborative art projects - but eventually settled on our current course, trying to empower Greenhouse employees.

![Heart vs Mind]()

To help shape our ideas, we performed our first user tests, investigating whether or not people were able to distinguish AI generated and human art, and whether or not it could influence their emotions.

We also built our first prototype, a model of the room out of wood - this wasn't meant to be an exact model of what the end result would look like, but more to visualise our intentions, for which I think it served our purposes quite well.

![Room Prototype](https://user-images.githubusercontent.com/9715331/208252726-ebe8cb02-339e-47b4-bf88-9f0d01fa54b3.png)
_The room prototype_

### Sprint 2: Research, First Software Prototype, and Adjustments
We had honed in on what we wanted to do, but before we could truly start working on our first prototype we needed to do a lot more research. This round was much more focused: we had decided we wanted to empower Greenhouse employees, so we needed to investigate how best to do that, which we did in three ways.

First, we held interviews with Greenhouse employees. We set up interviews and crafted a list of questions we wanted to ask which went through many revisions, eventually we decided our main focus with the questions would be their current workflow, to see how we could best fit in. The results were very positive, not only getting enthousiastic reactions from the interviewees, but also getting some data that required some alterations to our concept. For example, we realised that the employees do almost everything in groups, which meant that we needed to find ways to make our concept work in a cooperative setting instead of the more solitary setup we envisioned before.

We also performed user tests to test the exact emotional impact AI generated images could have. This test was even more successful than expected, showing that it was absolutely a possibility, but there are still challenges when it comes to this angle. First, figuring out exactly what emotions would have a positive impact on creativity and productivity will probably require deeper research, and second, having an AI generate images that specifically evoke those emotions could prove quite difficult, since simply asking it to generate something 'happy' does not work.

![Creativity User Testing](https://user-images.githubusercontent.com/9715331/208252819-58bb1129-13d4-47db-a09d-72c5bfbae7ca.jpg)
_The creativity user test_

I personally headed a user test into if, and how exactly, we could positively influence people's creativity with AI art. For me this was an incredibly important question to answer, because the results would largely determine what exact prompts we would use to generate our images. The results were very positive, and gave us a lot to work with: based on the results I plan to implement adjustments in art style, and try to generate a wider array of images closely related to users' initial prompt. For a full research report including results see [Creativity Research](Research/Creativity%20Research.md), and for an evaluation of the results and how exactly we plan to use them to adjust our prototype see [Evaluation](Research/Evaluation.md).

We also set up our very first prototype using React. Luckily, there were a host of publicly available speech-to-text libraries, which meant setting up the basics was very easy. This gave us the opportunity to create a foundation for future improvements, and investigate the specifics of the DALL-E API.

![Prototype Gif](https://user-images.githubusercontent.com/9715331/208179089-80004b7b-3c19-47ed-8b29-12215d0bf62b.gif)
_First software prototype with an updated UI_
