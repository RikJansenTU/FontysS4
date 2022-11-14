# Fontys S4 Portfolio
By Rik Jansen

# Table of Contents
- [Personal Project](#personal-project-criticmatic)
  * [Project Details](#project-details)
  * [Evaluation](#evaluation)
- [Duo Project](#duo-project)
  * [Concepting](#concepting)
  * [Technical Challenges](#technical-challenges)
  * [Presentation](#presentation)
  * [Evaluation](#evaluation)
  
# Personal Project: Criticmatic
Most of us find it hard to make time in our busy schedules to read, so when we finally get around to opening the book that’s been gathering dust on our shelf it’s important to make sure we’re reading something worthwhile; you don’t want to spend hours reading some worthless drivel, but you want something that you can use to impress on your friends how well-read and sophisticated you are.

Finding something with literary value can be difficult however: if you walk into your local bookstore it’s easy to get overwhelmed by the vast quantity of reading material available, and separating the wheat from the chaff can be an impossible task. Sure, many books have reviews, but those are often lengthy themselves. I offer an alternative: a simple device that can determine whether or not a book will be worth your time based on only a couple of sentences. Simply pick a book, dictate a few lines, and you will immediately be notified of the work’s most important characteristics.

With this revolutionary technology, you’ll be able to contribute to any conversation your pretentious friends are having, while still having plenty of time to catch up on your favorite Netflix series.
## Project Details
Criticmatic is a device that rates literature based on a few sentences: you dictate them into a microphone, the device will evaluate them using speech-to-text, and return a verdict by lighting up one (or several) LED lights corresponding to a variety of characteristics, like ‘derivative’ or ‘worthwhile’.

Obviously it’s impossible to evaluate the value of a piece of literature based on a couple of sentences, let alone using software. The project is intended as satire, attempting to highlight the futility of trying to rate a piece of art, especially with something as reliant on personal experience as reading books.

This is the postcard based on the Criticmatic concept:

![Postcard.png](https://user-images.githubusercontent.com/9715331/201684174-067d69df-b298-4c7c-9196-b3629fabf228.png)

The Arduino has a microphone, activated by pressing a button, linked to a PC with a small speech recognition program, which will evaluate the resulting text on arbitrary parameters like average word length, alliteration, usage of specific words, and others. Based on those parameters it will light up a LED light corresponding to one or more of the following terms:

- Derivative
- Worthwhile
- Groundbreaking
- Simplistic
- Amateurish

## Evaluation
Unfortunately I was sick for almost all of the project’s duration, which meant I was unable to get much further than the concept stage. I was able to do research into the technology that would be required, mostly the speech recognition software, but couldn’t implement much of it. I did however, work out as much of the concept and its intended impact, satirical as it may be, as I could.

Afterwards, I decided to focus on the duo project instead of trying to catch up on my personal one.


# Duo Project
For our Duo Project, Ruben and I created the A.L.N.D.. A.L.N.D. stands for Automatic Long distance Nut Dispenser, a useful device that ensures you never have to get up to eat cocktail nuts ever again. This device will automatically measure the distance to your mouth, and when you open your it the A.L.N.D. will shoot a nut right at you so you can keep doing what you're doing and have a snack at the same time.

![ALND Instruction Men](https://user-images.githubusercontent.com/9715331/201686098-ae1538c8-7919-4174-ad34-7c680a77fb67.png)

## Concepting
We didn’t go into the project with a clear concept of what we wanted to do, so we spent much of the first week coming up with potential ideas. We weren’t looking to create something inherently useful, but instead wanted to create a seemingly useless device that would make people think about some aspect of their lives, akin to an art project. We tried not to get too constricted in technical details immediately, instead throwing out ideas we thought were fun, and worrying about their practical implementation later.

Some of the ideas we ended up rejecting were:

- A device to forcibly remove you from your bed in the morning
- A staircase that could turn into a slide automatically
- A robot that allows you to practice your dating skills
- A drone that follows you around and streams your activities 24/7

Eventually we chose the ALND due to the manageable size of the project, and the fact that it made a funny point about the way advanced technology is being used for more and more mundane tasks, slowly creating a world where we have to do less and less ourselves.

## Technical Challenges
We decided to quickly design a low-fi prototype using rubber bands - we were pretty sure rubber bands would not be used in a final product, but it did allow us to create something that could fire cocktail nuts (albeit inaccurately) and show off our concept. This prototype highlighted initial design flaws and served as a catalyst for new ideas, for example when it came to the shape of the device's 'barrel'.

After an adjusted rubber band-based prototype, we moved on to a spring launching mechanism, which would allow for much greater firing consistency and accuracy. This is where we really started to attempt to dig into the automatic firing mechanism - it would need to be able to pull back the spring a specific amount, and then immediately release it, reloading afterwards. This proved to be a much greater challenge than expected, and while we did do a lot of research into similar devices, we never managed to get a working prototype built.

![All of the prototypes](https://user-images.githubusercontent.com/9715331/201690742-2c0c27a6-0902-40de-b9d3-4efbb83db8cd.jpg)

## Presentation
When we showed our very first prototype, feedback indicated that the satirical nature of the project wasn’t clear, and instead it seemed like our only end goal was to make a functional cocktail nut launcher.

For our final presentation, we wanted to ensure people understood our intentions better, and hopefully make them think about the increasingly large role of technology in our lives. We decided to pretend to ‘sell’ our product, marketing it as a must-have and a truly great use of modern science. We very quickly landed on framing it as an 80s-style Telsel commercial, known for its enthusiastic overselling of incredibly niche or nearly useless items.

We created an advertising poster in this same style, exaggerating the product’s features and framing it as a must-have item, and gave a sales pitch trying to convince the audience to purchase it. We had to make sure to strike a balance between making it straight-faced, but ridiculous enough that people would be able to understand the underlying meaning.

Alongside we set up a demo overselling the complexity of grabbing a cocktail nut for yourself, and offering the A.L.N.D. as a superior alternative, both to mimic the demonstrations often given on Telsel commercials and to make the presentation more hands-on and enjoyable. 

Overall, the presentation seemed to have its intended effect; while it might have been a bit on the nose at times, people understood that the project was intended as satire, and the subsequent discussions weren’t about our own device as much as the increasingly minor ‘problems’ in our lives we try to solve with gadgets.

![ALND A3 Poster](https://user-images.githubusercontent.com/9715331/201691189-b2fad071-0c97-4875-a5a9-f79a91742491.png)

## Evaluation
Unfortunately, I don't think the end result of the project was quite as advanced as we hoped or planned it to be. I think this can mainly be contributed to two factors: my inexperience handling projects like these, and our excessive focus on the firing mechanism.
Speaking for myself, I am used to creating software projects, and while there are definitely similarities, the fact that the A.L.N.D. had much more hardware engineering involved made it much more difficult to get a grasp on. Problems that I thought would be easy to solve turned out to be much bigger stumbling blocks than expected, and required a lot of research - this was most apparent in the firing mechanism, which took up a lot of our time and energy to try and develop.

I do think there was a bigger hurdle in the project however, and it was one we placed in front of ourselves; the fact that we spent way too much time trying to get the automatic firing mechanism working. It's something we got stuck on for quite a while, and we didn't even end up solving the problem.
Instead, we could've started working on other aspects, like adding a camera to the A.L.N.D. and setting up automatic face detection; even if there was no working mechanism to control, it could still measure distances or detect a mouth opening, adding some much-needed tech to our project.
I realise I do this getting lost in details in a lot of my projects, either for study or personal, so I think the lesson of sometimes needing to take a step back and get a better overview of what you're doing, and maybe look at a problem from a different angle, is a very valuable one, and something I'll definitely try to take with me in future projects.

I did really enjoy the presentation aspect of the project - I'd never really tackled a 'marketing' challenge like this one, and really enjoyed thinking about ways to sell our product, while still keeping in mind the satirical aspect. In this way, I do think we achieved at least part of our impact - while the end product wasn't automatic in any way, it did function well enough to set up a demo and convey our intended message. I learned that a well-made presentation can do a lot to sell a project, and I'm excited to explore the 'media' side of technology more in the future.
