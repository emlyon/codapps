= CODAPPS: Essential notions of code
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

== 1. The interactive tool we are using to learn the basics of code
//ST: 1. The interactive  we are using to learn the basics of code



//ST: !
It is useful to learn about coding by reading a lesson like this one, but it is more efficient if you can *practice while you read*.

Indeed, a key competency in coding is to learn the simple discipline of writing text carefully:

//ST: !
- not forgetting a `;` at the end of the line
- not forgetting to put a capitalized letter when it is necessary
- learning how to spot opening accolades `{` and closing accolades `}`
- not confusing when to use commas `,` and semi-colons `;`, knowning wen to put double quotes `""` or not...

//ST: !
It is all very trivial, right?

*And yet this is what needs the most practice, at the start.*

//ST: !
So in this lesson, you will see plenty of interactive screens like this one:

++++
<iframe src="https://repl.exploreyourdata.com/ui/console.html" style="width: 500px; height: 150px; border: 0px"></iframe>
++++

//ST: !
"Interactive screen" means that *you can write directly on it* and see your code in action - yes, right here: click next to "java", a cursor will blink to show that you can write:

//ST: !
image::How-to-use-the-interactive-tool.png[align="Center" title="How to use the interactive tool"]
{nbsp} +

//ST: !
Last note before we start: this lesson is on the [underline]#essentials# of coding, so we go fast and discuss just the most important notions of coding.

If you are interested in (much) longer, more thorough approaches, you can have a look at these two interactive courses:

//ST: !
- https://books.trinket.io/thinkjava/index.html["Think Java"] by Tinklet (Java is the same programmming language as the one we use here)
- https://books.trinket.io/pfe/index.html["Python for Everybody"] also by Tinklet (Python is the most popular programming language for data science)

== 1. Variables
//ST: 1. Variables

//ST: !
If we compare coding to cooking, you could say that `variables` are the ingredients of the recipe.

-> variables are a way to create, define and store all the information we need in our mobile app.

What kind of information do we need to store?

//ST: !
- if you create a *gaming app*, you might need to store the name of the player, the score, the energy level, etc...
- if you create an *app selling a service*, you might need to store a login name, a password, a list of products and their prices...

//ST: !
As you see, variables can be of different types: text, numbers, numbers with decimals, ...

//ST: !
[TIP]
====
You can create all the kinds of variables you want, but to help you, a number of them are already predefined because they are so common:
====

//ST: !
==== a. *String* variables: to store text

//ST: !
A variable of type "String" specializes in storing textual information. It is created and defined this way:

//ST: !
[[string]]
.Creating a String variable and giving it a value
[source,java]
----
String playerName; //<1>
playerName = "Bernard B"; //<2>
----

What does all this mean? Let's decompose each line:

//ST: !
<1> We create the variable (this needs to be *done just once*)

- `String` The capital *S* is mandatory. It means this variable specializes in storing *text*. This is the *type* of the variable.
- `playerName` this is the name I chose for the variable, it could have been anything else. By convention it always starts *without* a capitalized letter and it has *no space* in it.
- The `;` shows the end of this instruction and *is mandatory* (if you don't put it, the program tries to read the next line as the direct continuation of this one, and it gets confused).

//ST: !
<2> A value is assigned to the variable (this can be done as many times as we need)

- `playerName`: our variable, created just above.
- `=`: the right of the equal sign will be the value of the variable.
- `"Bernard B"`: this is the value I store in the variable `playerName`. *Textual values should be put between quotes " "*.
- The `;` shows the end of this instruction and *is mandatory*.

//ST: !
There is a shortcut if you want to create a variable and give it a value, just in one line of code:

//ST: !
[[string-shortcut]]
.A shortcut
[source,java]
----
String playerName = "Bernard B";
----

*So this single line of code creates a variable called `playerName`, and I immediately give it a value: `Bernard B`.*

//ST: !
This will be handy when we need to show the player's name on the screen of the app: we will just use the variable `player`, and what ever value in it (the player's name) will be shown.

//ST: !
====
icon:child[3x] Your turn!

__Create a variable called "favoriteMovie" and store the name of your favorite movie in it__
====

//ST: !
++++
<iframe src="https://repl.exploreyourdata.com/ui/console.html" style="width: 500px; height: 150px; border: 0px"></iframe>
++++

//ST: !
Here is the solution:

//ST: !
image::Creating-a-variable-for-a-textual-information.png[align="center", title="Creating a variable for a textual information"]
{nbsp} +

//ST: !
==== b. *Integer* variables: to store round numbers

//ST: !
A variable of type "Integer" specializes in storing round numbers (like 1, 2, 3...). It is created and defined this way:

//ST: !
[[integer]]
.Creating an Integer variable and giving it a value
[source,java]
----
Integer playerAge; //<1>
playerAge = 22; //<2>
----

__Note that we did not put double quotes around 22__! Let's decompose each line:


//ST: !
<1> We create the variable (this needs to be *done just once*)

- `Integer` The capital *I* is mandatory. It means this variable specializes in storing *round numbers*. This is the *type* of the variable.
- `playerAge` this is the name I chose for the variable, it could have been anything else. By convention it always starts *without* a capitalized letter and it has *no space* in it.
- The `;` shows the end of this instruction and *is mandatory* (if you don't put it, the program tries to read the next line as the direct continuation of this one, and it gets confused).

//ST: !
<2> A value is assigned to the variable (this can be done as many times as we need)

- `playerAge`: our variable, created just above.
- `=`: the right of the equal sign will be the value of the variable.
- `22`: this is the value I store in the variable `playerAge`. *Don't use double quote around the value*.
- The `;` shows the end of this instruction and *is mandatory*.

//ST: !
There is the same shortcut as usual if you want to create a variable and give it a value, just in one line of code:

//ST: !
[[integer-shortcut]]
.A shortcut
[source,java]
----
Integer playerName = 18;
----

*So this single line of code creates a variable called `playerAge`, and I immediately give it a value: `22`.*

//ST: !
There is another way to use variables for round numbers:

//ST: !
[[int-primitive]]
.Another way
[source,java]
----
int playerName = 18;
----

`Integer` has been replaced by `int`. Both are the same, except that `int` takes *even less space in the memory of your program*.

//ST: !
====
icon:child[3x] Your turn!

1. __Create an Integer variable called `score` and store `999999` in it. __
2. __Create a variable called `purchasedItems`, using `int` instead of `Integer`. Store `4` in it.__
====

//ST: !
++++
<iframe src="https://repl.exploreyourdata.com/ui/console.html" style="width: 500px; height: 150px; border: 0px"></iframe>
++++

//ST: !
Here is the solution:

//ST: !
image::java-repl-3.png[align="center", title="Creating 2 variables to store numbers"]
{nbsp} +

//ST: !
==== c. *Float*, *Double* and *Long* variables: to store decimal numbers and big numbers

//ST: !
Variables of type "Float" and "Double" specialize in storing decimal numbers (like 1.4533).

The difference between Float and Double? Double can store even more decimals than Float.

Variable of type "Long" specializes in storing loooong numbers (like 9395353439449039035353). It is useful when you need to count milliseconds, for example.

These are created and defined this way:

//ST: !
[[float-double-long]]
.Using Float, Double and Long variables
[source,java]
----
Float averagePrice;
averagePrice = 15.34f; //<1>
Double piValue;
piValue = 3.14159265358979323846d; //<2>
Long timeOfPlayinMilliSeconds;
timeOfPlayinMilliSeconds = 72585335350535l; //<3>
----

Let's notice a few things:

//ST: !
<1> We added the letter `f` at the end of our number, to signal that this is a *Float*.
<2> We added the letter `d` at the end of our number, to signal that this is a *Double*.
<3> We added the letter `l` at the end of our number, to signal that this is a *Long*.

//ST: !
There is the same shortcut as usual if you want to create a variable and give it a value, just in one line of code:

//ST: !
[[float-double-long-shortcuts]]
.A shortcut
[source,java]
----
Float averagePrice = 15.34f;
Double piValue = 3.14159265358979323846d;
Long timeOfPlayinMilliSeconds = 72585335350535l;
----

//ST: !
There is another way to use these types of variables, again for a gain in memory:

//ST: !
[[float-double-long-primitive]]
.Another way
[source,java]
----
float averagePrice = 15.34f;
double piValue = 3.14159265358979323846d;
long timeOfPlayinMilliSeconds = 72585335350535l;
----

//ST: !
`Float` is replaced by `float`, `Double` is replaced by `double`, and `Long` is replaced by `long`.

This looks like just a small change, but the smaller cap version takes *even less space in the memory of your program*.

//ST: !
====
icon:child[3x] Your turn!

1. __Create a variable called `discountPercentage` and store `0.33` in it. __
2. __Create a variable called `dollarToEuro`, using `double`. Store `0.80240500000000003` in it.__
3. __Create a variable called `milliseconds`, using `long`. Store `25343353530285753` in it.__

====

//ST: !
++++
<iframe src="https://repl.exploreyourdata.com/ui/console.html" style="width: 500px; height: 150px; border: 0px"></iframe>
++++

//ST: !
[#open-solution]
Here is the solution:

//ST: !
[#solution]
image::java-repl-4.png[align="center", title="Creating 3 variables to store decimal or long numbers"]
{nbsp} +


//ST: !
==== d. *Boolean* variables: to store true / false information

//ST: !
If you have never programmed before, this type of variable might be surprising to you.
Why do we need a type of variable that would just store 2 possible values: `true` or `false`?

After all, we could just use a `String` type of variable for that:

//ST: !
[[string-for-boolean]]
.Using a String variable to store a "true" value
[source,java]
----
String customerLoggedIn = "true";
String customerSubscribedToNewsletter= "false";

----

//ST: !
That would work very well, but in practice these true / false values are so common that a special type of variable called `Boolean` has been created just for them:


//ST: !
[[boolean]]
.Using Boolean variables
[source,java]
----
Boolean hasSuperPowers = true;
Boolean isAClubMember = false;
----

Let's notice that *we did not put double quotes around the value `true` or `false`*.

//ST: !
Just like before, there is another way to use these type of variables, again for a gain in memory:

//ST: !
[[boolean-primitive]]
.Another way
[source,java]
----
boolean hasSuperPowers = true;
boolean isAClubMember = false;
----

Notice that `Boolean` has been replaced by `boolean`.

//ST: !
====
icon:child[3x] Your turn!

1. __Create a variable called `isPremiumMember` and store a `true` value in it. __
2. __Create a variable called `isReturningVisitor` and store a `false` value in it__

====

//ST: !
++++
<iframe src="https://repl.exploreyourdata.com/ui/console.html" style="width: 500px; height: 150px; border: 0px"></iframe>
++++


//ST: !
Here is the solution:

//ST: !
image::java-repl-5.png[align="center", title="Creating 3 variables to store true false values"]
{nbsp} +




== The end
//ST: The end

//ST: !
Questions? Want to open a discussion on this lesson? Visit the forum https://github.com/seinecle/codapps/issues[here] (need a free Github account).

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
pass:[    <!-- Start of StatCounter Code for Default Guide -->
    <script type="text/javascript">
        var sc_project = 11592657;
        var sc_invisible = 1;
        var sc_security = "5154b75d";
        var scJsHost = (("https:" == document.location.protocol) ?
            "https://secure." : "http://www.");
        document.write("<sc" + "ript type='text/javascript' src='" +
            scJsHost +
            "statcounter.com/counter/counter.js'></" + "script>");
    </script>
    <noscript><div class="statcounter"><a title="site stats"
    href="http://statcounter.com/" target="_blank"><img
    class="statcounter"
    src="//c.statcounter.com/11592657/0/5154b75d/1/" alt="site
    stats"></a></div></noscript>
    <!-- End of StatCounter Code for Default Guide -->]
