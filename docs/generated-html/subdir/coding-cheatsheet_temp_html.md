= CODAPPS: Coding Cheatsheet
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

== Variables and objects

General rules:

- The type of the variable (String, Long, Boolean...) start [underline]#with# a capital letter.
- variable names start [underline]#without# a capital letter.

==== *String* variables store *text*

[[string]]
.Creating a String variable and giving it a value
[source,java]
----
String title = "Welcome to my app"; //<1>
----
<1> Don't forget the double quotes `" "`!

==== *Integer* variables store *round numbers*

[[integer]]
.Creating an Integer variable and giving it a value
[source,java]
----
Integer classSize = 32;
int anotherClassSize = 25; // <1>
----
<1> `int` is like `Integer`. It takes less memory but is sometimes less convenient to use.
Also, note: [underline]#no# double quote!! Double quotes are just for `String`.

==== *Float* and *Double* variables store *decimals*

__ *Double* is like *Float* but can store *decimals with a lot more precision* __

[[Float-and-Double]]
.Creating Float and Double variables
[source,java]
----
Float pi = 3.14f; //<1>
Double piVeryPrecise = 3.141592653589793238462643383279502884197169d; // <2>
----
<1> Don't forget the `f` letter at the end of your number. `float` or `Float` can be used, `float` takes less memory than `Float`.
<2> Don't forget the `d` letter at the end of your number. `double` or `Double` can be used, `double` takes less memory than `Double`.

==== *Long* stores *big round numbers*

__ *Long* is like *Integer* but can store *bigger numbers* __

[[Long]]
.Creating a Long variable
[source,java]
----
Long millisecondsSinceLastMonth = 364434030430414l; //<1>
----
<1> Don't forget the `l` letter at the end of your number. `long` or `Long` can be used, `long` takes less memory than Long but can be inconvenient to use.

==== *Boolean* stores *true / false values*

__ This seems not very useful but actually we use it quite often __

[[Boolean]]
.Creating a Boolean variable
[source,java]
----
Boolean hasAStudentCard = true; //<1>
----
<1> A classic mistake is to write `"true"` (with double quotes, which is incorrect). Boolean values are `true` or `false` [underline]#without double quotes " "#.
`boolean` can be used instead of `Boolean`: less memory but also less convenient to use in some cases.

==== `Objects`: to create and store a variety of things

__ A variety of objects exist - use them to create and store things __

[[object]]
.Creating an Object storing a Date
[source,java]
----
Date dateStartOfTheGame;  //<1>
dateStartOfTheGame = new Date(); //<2>
Date dateEndOfTheGame = new Date();  //<3>

----
<1> An object `dateStartOfTheGame` of type `Date` is [underline]#declared#. It is `null` at the moment.
<2> `dateStartOfTheGame` is [underline]#instantiated#: an instance of it is created.
<3> Shortcut: a variable can be [underline]#declared# and [underline]#instantiated# in one line of code.

== Methods

==== Creating (defining) a method

//ST: !
[[method-creation]]
.Creating a method adding the VAT to a price
[source,java]
----
private Float addFrenchVAT(Float priceWithoutVAT) { // <1>
   Float priceWithVAT; // <2>
   //the regular rate of the VAT in France is 20% so we multiply the price by 1.20 to find the new price <3>
   priceWithVAT = priceWithoutVAT * 1.20; // <2>
   return priceWithVAT; // <2>
}// <4>
----
<1> title of the method you create, then the method start at the opening curly brace `{`.
<2> the method itself
<3> an explanation, not some code! The line starts with `//` to show this is some explanations for humans like you and me, not some code in our app.
<4> this closing curly brace signals the end of the definition of the method.

[[creating-a-method-without-return]]
.Creating a method which returns nothing
[source,java]
----
Float price = 5.99f;  // <1>
private void addFrenchVAT() {  // <2>
   price = price * 1.20; // <3>
} // <4>
----
<1> we have created a variable named `price`
<2> now we define a method like the one before in this lesson, except that:

- `Float` has been replaced by `void`, which is an English term meaning "nothing"
- it has no parameter: there is nothing in the parenthesis `(  )`

<3> the method does one thing: it multiplies the value of the variable `price` by 1.20
<4> this is the end of the method. There is no "return" statement.

== Classes

A class is just a file in your app.
It contains the variables and the methods that you want.
It looks like:

[[class-example]]
.A simple example of what a class looks like
[source,java]
----
package net.clementlevallois.codapps.myfirstapp // <1>

public class Form1 { // <2>

Integer scorePlayer; // <3>

  public void addOneToScore() {
    scorePlayer = scorePlayer + 1;
  }

}  // <4>
----
<1> a class always starts with the name of the package where it belongs
<2> the name of the class (`Form1`) should have the same name as your file where it is writte (here the file would be Form1.java)
<3> this is a variable which can be used anywhere in the class.
<4> don't forget the closing curly brace of the class!


//ST: !
[[example-instantiation]]
.Instantiating a Form in MyApplication.java
[source,java]
----
public void start() {
    Form1 myForm1 = new Form1(); // <1>
    myForm1.show(); // <2>
}
----
<1> We instantiate our Form1
<2> *And now we can use methods of this Form1*. Here, we use the method `show()` which has for effect to display the `Form` on screen.

Another common way to instantiate an object is this one:

//ST: !
[[example-instantiaton-with-static-method]]
.Getting the present time and storing it in a variable
[source,java]
----
public void start() {
  LocalTime timeNow = LocalTime.now(); //<1>
}
----
<1> This stores the time at the moment when this line of code is executed, in the variable `timeNow`

== If... conditional statements

==== conditional statements for numbers

[[if-example]]
.Different kinds of conditional statements about numbers
[source,java]
----
Float priceItemInEuros;
priceItemInEuros = 5.99f;
Label productLabel = new Label();
if (priceItemInEuros < 6) {
  productLabel.setText("cheap product!");
}
if (priceItemInEuros == 5.99) { //<1>
  productLabel.setText("the price is exactly 5.99");
}
if (priceItemInEuros != 5.99) { //<2>
  productLabel.setText("the price is different from 5.99");
}
if (priceItemInEuros =< 6) {
  productLabel.setText("the price is under or equal to 6!");
}
if (priceItemInEuros >= 7) {
  productLabel.setText("the price is above or equal to 6!");
}
----

==== conditional statements about text

It would be a *mistake* to write:

[[if-text-example-mistake]]
.Mistake! Don't do this!
[source,java]
----
String playerName1 = "Tristan";
String playerName2 = "Tristan";

if (playerName1 == playerName2) { //<1>
  messageLabel.setText("the two players have the same name!");
}
----
<1> Using `==` to compare two Strings is incorrect.
- Your build will not fail, but even if the two players have the same name it might say it's false!
- when comparing two String, you should do like below:

[[if-text-example]]
.Different kinds of conditional statements about text
[source,java]
----
String playerName1 = "Tristan";
String playerName2 = "Touni";

if (playerName1.equals(playerName2)) {
  messageLabel.setText("the two players have the same name!");
}
if (!playerName1.equals(playerName2)) { //<1>
  messageLabel.setText("the two players have different names!");
}
----
<1> note the `!` in front

==== conditional statements about several items

[[several-and-conditionals-example]]
.A statement with two conditions which need both to be true
[source,java]
----
Float priceItemInEuros;
priceItemInEuros = 5.99f;
Label productLabel = new Label();
if (priceItemInEuros < 6 & priceItem > 2) { // <1>
  productLabel.setText("relatively cheap product!");
}
----
<1> the `&` means "and". The two conditions: `priceItemInEuros < 6` *and* `priceItem > 2` both need to be true for the statement `productLabel.setText("relatively cheap product!");` to be executed.

[[several-and-conditionals-example]]
.A statement with two conditions where just either one of the two needs to be true
[source,java]
----
Float priceItemInEuros;
priceItemInEuros = 5.99f;
Label productLabel = new Label();
if (priceItemInEuros < 6 | priceItem > 2) { // <1>
  productLabel.setText("relatively cheap product!");
}
----
<1> the `|` means "or". Just one of the two conditions: `priceItemInEuros < 6` *or* `priceItem > 2` needs to be true for the statement `productLabel.setText("relatively cheap product!");` to be executed.

== Loops

[[loop]]
.Writing a loop
[source,java]
----
for (int i = 0; i<100; i = i+1){
  System.out.println("I looped " + i) +" times.";
}
----

//ST: !
[[using-loop-with-if]]
.A loop with several ifs inside
[source,java]
----
for (int i = 0; i<100; i = i+1){
  System.out.println("I looped " + i + " times.");
  if (i == 0) {
    System.out.println("We just started the loops. This is going to be a long journey.");
  }
  if (i == 50) {
    System.out.println("Half way already!");
  }
  if (i == 99) {
    System.out.println("This was the last loop. Bye!");
  }
}
----

== ArrayLists

[[lists]]
.Creating a list and adding objects to it
[source,java]
----
ArrayList<Balloon> balloons = new ArrayList();
for (int i = 0; i<20000;i = i+1){
  Balloon myBalloon = new Balloon();
  balloons.add(myBalloon);
}
----

//ST: !
[[using-ArrayLists]]
.Looping through a list to show the names of all players
[source,java]
----
for (String player: playerNames) { //<1>
  Label myLabel = new Label();
  myLabel.setText(player);
  myForm.add(myLabel)
}
----
<1> here we assume that we had created before an ArrayList of player names.
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
