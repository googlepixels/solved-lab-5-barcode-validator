Download Link: https://assignmentchef.com/product/solved-lab-5-barcode-validator
<br>
<h1></h1>

Objectives

<ul>

 <li>Learn how to use 1D arrays</li>

 <li>Practice converting an algorithm to code</li>

 <li>Practice self guided program design</li>

</ul>

<h3>Overview</h3>

For this lab, you will write a program that prompts the user to enter the 12 digits of a UPC barcode, which you will store in an array. Using the algorithm described below, you will determine if the barcode is valid or invalid.

<h3>Algorithm</h3>

A barcode scanner for Universal Product Codes (UPC) verifies the 12-digit code scanned by comparing the code’s last digit (called a <em>check digit</em>) to its own computation of the check digit from the first 11 digits. The process of validating a barcode is described below.

<ol>

 <li>Calculate the sum of the digits in the odd-numbered position (first, third, …, eleventh). Multiply this sum by three.

  <blockquote>

   <strong>NOTE:</strong> In C arrays, we count array indices starting at 0. Therefore, the “first” digit of the barcode will be stored in the 0th position of your array. Be careful to manage your array indices correctly.

  </blockquote></li>

 <li>Calculate the sum of the digits in the even numbered positions (second, fourth, …, tenth) of the barcode.

  <blockquote>

   <strong>NOTE:</strong> Remember, the 12th digit of the barcode is the checksum. Make sure not to include it in your sum of even indices.

  </blockquote></li>

 <li>Add these two sums together.</li>

 <li>From this combined sum, extact the last digit. If the last digit is a 0, then 0 is the check digit. Otherwise, subtract the last digit from 10 to calculate the check digit.

  <blockquote>

   <strong>NOTE:</strong> To extract an individual digit from a number, use the <code>%</code> modulus operator

  </blockquote></li>

 <li>If the check digit matches the final digit of the 12-digit UPC, the UPC is valid. If not, the UPC is invalid.</li>

</ol>

<h3>Program</h3>

Write a program that prompts the user to enter the 12 digits of a barcode, separated by spaces. Your program will store the digits in an integer array, calculate the check digit, and compare your calculated check digit to the final barcode digit (the true check digit). If the digits match, the barcode is valid. Otherwise the barcode is invalid. You will print out your intermediate calculations for each step (1-5). See the Example Execution section to determine how to format your results.

<blockquote>

 <em>TIP:</em> Practice good program design by splitting your program into subtasks and write a functoin to solve each subtask. Do not write all of your code in your <code>main</code> function.

</blockquote>

<h3>Example Execution</h3>

<pre><code>    [esus] $ ./lab5    Enter a bar code to check. Separate digits with a space &gt;    0 7 9 4 0 0 8 0 4 5 0 1    You entered the code: 0 7 9 4 0 0 8 0 4 5 0 1    STEP 1: Sum of odds times 3 is 63    STEP 2: Sum of the even digits is 16    STEP 3: Total sum is 79    STEP 4: Calculated check digit is 1    STEP 5: Check digit and last digit match    Barcode is VALID.    [esus] $ ./lab5    Enter a bar code to check. Separate digits with a space &gt;    0 2 4 0 0 0 1 6 2 8 6 0    You entered the code: 0 2 4 0 0 0 1 6 2 8 6 0    STEP 1: Sum of odds times 3 is 39    STEP 2: Sum of the even digits is 16    STEP 3: Total sum is 55    STEP 4: Calculated check digit is 5    STEP 5: Check digit and last digit do not match    Barcode is INVALID.</code></pre>

<h3>Compile &amp; Test</h3>

Compile your program using this <code>gcc</code> command. <code>c99</code> is a shortcut for running <code>gcc -std=c99</code>, which uses the C99 standard instead of the default C89 standard.

<pre><code>$ c99 -Wall lab5.c -o lab5</code></pre>

<h3>Self Check</h3>

One you finish, you can test out your program with the following barcodes.

<pre><code>    0 7 9 4 0 0 8 0 4 5 0 1     Valid    0 1 1 1 1 0 8 5 6 8 0 7     Valid    0 5 1 0 0 0 1 3 8 1 0 1     Valid    0 2 4 0 0 0 1 6 2 8 6 0     Invalid</code></pre>

These barcodes are provided to allow you to verify that your program is working correctly.

<h3>Resources</h3>

<ul>

 <li>You should attend the Friday Lab session to seek assistance from the TAs and CAs.</li>

 <li>For specific questions, attend the weekly lab session or attend the TA’s office hours.</li>

 <li>You are encouraged to use resources or tutorials on the internet to learn unix or C. Check the <a href="http://www.cs.montana.edu/~marissa.joehler/csci-112/otherresources.html">class resource list</a> for some links to resources.</li>

</ul>

<h3>Submission</h3>

<strong>Assigned:</strong> February 29th<strong>Lab Day:</strong> March 4th<strong>Due Date:</strong> March 7th, 8:00am

<ol>

 <li>Make sure you included ample and informative comments – it is 20% of your grade!</li>

 <li>Rename your C file to <code>last_first_lab5.c</code> and substitute your last and first name.

  <blockquote>

   <strong>NOTE:</strong> If you fail to follow the above file naming conventions, your program cannot be graded automatically and you will lose significant points.

  </blockquote></li>

 <li>Submit your .c file to the D2L Dropbox for Lab 5.

  <blockquote>

   <strong>NOTE:</strong> Submit only your C file to D2L. Do not submit your object file or executable program. Do not archive (e.g. <code>zip</code>) your file.

  </blockquote></li>

</ol>

Each student will complete and submit this assignment individually. Submit your work on or before the deadline as late work will receive a 50% penalty. Labs submitted more than 24 hours late will not be accepted.


