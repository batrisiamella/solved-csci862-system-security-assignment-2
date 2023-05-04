Download Link: https://assignmentchef.com/product/solved-csci862-system-security-assignment-2
<br>
<h1>Part One: Short Answer                                                                         13 Marks</h1>

For questions where you are referencing material outside the lecture notes, you should provide appropriate referencing.

<ol>

 <li>Consider that you have two puzzles</li>

</ol>

Puzzle A: One sub–puzzles. <em>k </em>= 8.

Puzzle B: Four sub–puzzles. <em>k </em>= 6.

For each puzzle provide

<ul>

 <li>A graph of the distribution of the number of hashes needed. <strong>1 Mark</strong></li>

 <li>The average number of hashes needed. <strong>75 Mark</strong></li>

 <li>The standard deviation for the distribution of the number of hashes needed. <strong>2 Marks</strong></li>

 <li>Describe the method you used to obtain your solutions to (c). Don’t go into too many detailsor show working, it’s more “I wrote a C++ program to … and then using … I …”.<strong>25 Mark</strong></li>

</ul>

You should assume that if there are <em>N </em>possible solutions you check the <em>N<sup>th </sup></em>by hashing even if all others have failed and there has to be a solution.

<ol start="2">

 <li>Using a TCP SYN spoofing attack, the attacker aims to flood the table of TCP connection requestson a system so that it is unable to respond to legitimate connection requests. Consider a server system with a table for 1024 connection requests. This system will retry sending the SYN-ACK packet five times when it fails to receive an ACK packet in response, at 45 second intervals, before purging the request from its table. Assume that no additional countermeasures are used against this attack and that the attacker has filled this table with an initial flood of connection requests. At what rate (per minute) must the attacker continue to send TCP connection requests to this system in order to ensure that the table remains full? Assuming that the TCP SYN packet is 50 bytes in size (ignoring framing overhead). How much bandwidth does the attacker consume to continue this attack? <strong>1 Mark</strong></li>

 <li>What is a password mangler and why would we use one? <strong>1 Mark</strong></li>

 <li>What is a Cinderella attack? In particular, describe the target, the vulnerability being exploited,and the likely effect. <strong>1 Mark</strong></li>

 <li>Every hour the malware <strong>X </strong>spreads from each infected computer to two previously uninfected computers. In answering these questions you should explain how you determined your answers.

  <ul>

   <li>Give a table showing the number of infected computers at each hour across a 24 hour period.</li>

  </ul></li>

</ol>

At time <em>t </em>= 0 the number of <strong>X </strong>infected computers is <em>N </em>= 1.                                          <strong>0.5 Mark</strong>

<ul>

 <li>By time <em>t </em>= 10<em>.</em>5 a counter worm <strong>W </strong>has been developed and it is deployed on one infected computer. <strong>W </strong>removes malware <strong>X </strong>from any host <strong>W </strong>is on. The counter worm <strong>W </strong>spreads slightly more quickly than <strong>X</strong>, with each <strong>W </strong>spreading to three <strong>X </strong>infected hosts each hour, provided such hosts are available.</li>

</ul>

Provide another table showing the spread of <strong>W </strong>and the impact on <strong>X </strong>across a relevant time frame, starting from <em>t </em>= 0 again.

Note the offset in time means that at <em>t </em>= 10<em>.</em>5 the number of <strong>X </strong>infected computers reduces by

1, so the spread of <em>t </em>= 11 will be slightly smaller than before. <strong>1.5 Marks </strong>(c) Graph the two cases against each other, clearly indicating on it where <em>N </em>= 0. <strong>0.5 Mark</strong>

(d) Assume that at time <em>t </em>= 12, <strong>X </strong>evolves to spread to three uninfected computers each hour.

What subsequently happens?                                                                                            <strong>0.5 Mark</strong>

<ol start="6">

 <li>In the context of phishing, list 8 points that can be used in checking the legitimacy of an email.Justify why each is appropriate as an indicator. Note that some points could relate to characteristics of legitimate messages, and others could be indicators of a phishing message. <strong>2 Marks</strong></li>

 <li>What protection is provided at the memory level by using the private access specifier in declaring aclass in C++? Is it possible to overflow into private variables? <strong>1 Mark</strong></li>

</ol>

<h1>Part Two: Buffer overflow                                                                       3 Marks</h1>

The Windows executable overIT.exe is given. The corresponding C/C++ code was compiled with Dev– C++ and is executable on PC’s only. It should work happily in the lab. It can be used as follows:

overIT your student id Additional input

where your student id is your UOW student number, possibly with an additional digit (or more) appended (see below), and Additional input is an arbitrary string that will, in a normal run of the program, be echoed.

overIT.exe consists of some functions including a set of “bar” functions. Your task is to invoke it by altering the return address of a given function that improperly uses a C/C++ function that could allow a buffer overflow. When bar is invoked, it will print out a message: “I have been hacked!”.

You need to find out the return address of the given function. Do not try to compare it with other students since it is dependent on your student ID. However, if you cannot alter the return address because the address contains unalterable numbers (such as a space, etc.), then you are allowed to append an additional digit or digits to your student number to make a different stack. Provide the number in your report.

When overIT.exe is executed, it will provide you with the address of bar and a list of addresses on the associated memory stack. This is the only information you have. You then hack the code in terms of your own inputs in the command line. To do so, you need to create a Perl file that contains your input.

Your solution must include the following information:

<ol>

 <li>Your name and student ID.</li>

 <li>The additional digit if you used it.</li>

 <li>The stack contents before hacking and the memory address of bar, which will be printed out if youhave used the code properly. Mark the location of the return address that you attempt to overwrite.</li>

 <li>The output when you launch your successful buffer overflow. Remember there should be a message“I have been hacked!”.</li>

</ol>

You should also submit the perl script attack.pl used in your successful attack.


