= CODAPPS: The Cookie Clicker
Clément Levallois <levallois@em-lyon.com>
last modified: {docdate}
:icons: font
:iconsfont: font-awesome
:source-highlighter: rouge
:revnumber: 1.0
:docinfo: shared
:example-caption!:
:sourcedir: ../../../../main/java


:title-logo-image: EMLyon_logo_corp.png[width="242" align="center"]

image::EMLyon_logo_corp.png[width="242" align="center"]
{nbsp} +



//ST: 'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes

== 1. The Cookie Clicker: an addictive game on the web
//ST: 1. The Cookie Clicker: an addictive game on the web

//ST: !
==== a. The game

//ST: !
image::cookie-brand.jpg[align="center",title="The cookie clicker"]
{nbsp} +

//ST: !
We are going to create an app which replicates a game called http://orteil.dashnet.org/cookieclicker/["The Cookie Clicker"].

//ST: !
It is an addictive game where you try to produce as many cookies as you can. For this, you can:

1. mouse click on the cookie itself.
2. spend cookies you produced to buy devices which will increase your cookie production.

The more cookies you produce, the more options become available to speed up your cookie production.

//ST: !
==== b. Why is it so addictive?

//ST: !
This game offers periodic gratifications (sounds, pics, new game features) which reward the player for its continuous engagement.

//ST: !
This pushes the player to continue playing, to receive new gratifications.
This is a well established mechanism in psychology and game design:

//ST: !
video::tWtvrPTbQ_c[youtube, width=100%, height=400px]

//ST: !
Players can easily play an hour (on and off) on it, and some seem to have played weeks or months (check the number of cookies):

//ST: !
video::sIsA9U4EXrA[youtube,width=100%, height=400px]

//ST: !
==== c. Why replicating this game as a mobile app?

//ST: !
Mobile app development is a never ending experience.
When you will continue coding lessons after this introductory course, you will realize that there is so much to learn:

//ST: !
1. how can I make my mobile app share something to Facebook?
2. how can I display maps in my app?
3. how can my app send push notifications?
4. how can I animate the app / make it react to the user's actions?

Etc...

//ST: !
It is hard to say which of these features is more important than the other.

*So in this course, we replicate a game, because we will learn something essential from this list, AND we will have some fun.*

//ST: !
Choosing a game will put the focus on the feature number 4. in the list above:

 4. How can I animate the app / make it react to the user's actions?

//ST: !
Let's see the essential steps we are going to follow:

== 2. The steps in making the Cookie clicker app
//ST: 2. The steps in making the Cookie clicker app

//ST: !
=== a. Creating the interface (the screen)

//ST: !
The end result should look like this:

//ST: !
image::The-design-of-the-cookie-clicker-mobile-app.png[align="center",title="The design of the cookie clicker mobile app"]
{nbsp} +

//ST: !
We will *not* use the GUI Builder to create this interface.

Indeed, now that you covered the basics of coding, we will be able to create the Form, the Labels, Buttons... directly with some lines of code, and the layout ("how to place things where I want?) will be also managed by writing code.

//ST: !
We could have used the GUIBuilder for this, but the process of creating containers and placing things inside them (Buttons, Labels, ScaledLabels...) is too slow and annoying for an app of this complexity.

//ST: !
=== b. Coding the "logic" of the game.

//ST: !
- Clicking on the cookie should increase the score!
- Whe should be able to buy grandmas, farms, etc... with cookies!
- the score should take into account everything we have (grandmas bake more cookies!), and every expense the player make (buying a grandma should decrease the score).

//ST: !
We will define these differents functions of the game with some lines of code.

//ST: !
=== c. Polishing the design

//ST: !
Even with all the buttons and pictures on screen, working correctly, we'll need to make the app more beautiful and cleanly designed.

//ST: !
For this, you will refer to the lesson on "styling" in Module 3 (the talents of this lecturer are quite limited in terms of designing a beautiful interface, you'll surely do better than him).

== 3. Let' start
//ST: 3. Let' start

//ST: !
Note: you must have worked and understood the content of Module 5 about coding before you can follow the next lessons.

//ST: !
A last word, as we start: creating an app takes some time.

[INFO]
====
Companies typically invest in a *team* of 2 to 5 developers working several months to create an app.

Not because it is complicated, but because there are so many features to create in an app.
====

//ST: !
So in comparison to the apps you download and use on your phones, our cookie clicker app will be much simpler (yet impressive!)

-> it doesn't mean we can't do better, just that with more time, we could have achieved much more :-)

//ST: !
Let's dive in with the next lesson of this Module!

== The end
//ST: The end

//ST: !
Questions? Want to open a discussion on this lesson? Visit the forum https://github.com/emlyon/codapps/issues[here] (need a free Github account).

//ST: !
Find references for this lesson, and other lessons, https://seinecle.github.io/codapps/[here].

//ST: !
Licence: Creative Commons, https://creativecommons.org/licenses/by/4.0/legalcode[Attribution 4.0 International] (CC BY 4.0).
You are free to:

- copy and redistribute the material in any medium or format
- Adapt — remix, transform, and build upon the material

=> for any purpose, even commercially.

//ST: !
image:round_portrait_mini_150.png[align="center", role="right"]
This course is designed by Clement Levallois.

Discover my other courses in data / tech for business: http://www.clementlevallois.net

Or get in touch via Twitter: https://www.twitter.com/seinecle[@seinecle]
