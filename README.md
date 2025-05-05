# ac31012-ac51042-assignment-1--applied-cryptography-solved
**TO GET THIS SOLUTION VISIT:** [AC31012-AC51042 Assignment 1- Applied Cryptography Solved](https://www.ankitcodinghub.com/product/ac31012-ac51042-assignment-1-applied-cryptography-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;101694&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;4&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (4 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;AC31012-AC51042 Assignment 1- Applied Cryptography Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (4 votes)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Assignment 1: Applied Cryptography

Overview of Assignment

In this applied cryptography assignment, you will work as a team to implement two password login (authentication) procedures in C++. One of the login procedures should be secure, but the other should have a covert backdoor that allows you to login as root or any other user on the system without knowing their passwords.

Later in the module, a part of your mark for Assignment 2 will be determined by the (in-)ability of the other teams to find the backdoor in the subverted procedure that you are developing here.

This means that your team will have to consider operational security: ensure that no one outside of your team has access to your code and your ideas. As part of Assignment 2, only the source code of all subverted login procedures will be distributed. The other teams will not have access to your secure login procedure or its source code, so you do not need to worry about code similarity between your secure and your subverted login procedures.

This assignment can be solved in Ubuntu on the QMB Lab PCs. You may use any other computer and operating system, but it is then your responsibility to ensure that your code also compiles on an Ubuntu configuration as found on the QMB Lab PCs.

Password File Format

Your login procedures must be able to read files that contain zero or more lines containing a username and a SHA256-hashed password in the format:

<pre>username:SHA256-hashed-password
</pre>
</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
For example, a password file might look like this:

<pre>root:5e884898da28047151d0e56f8dc6292773603d0d6aabbdd62a11ef721d1542d8
alice:5ef2c394d5b63e4175cd331c74c8453c3e36eb8f47f6d648397ff6c1314fd705
</pre>
The SHA256-hashed password for user root in the password file above is “password”. You can verify this by typing the following in the command line:

echo -n “password” | openssl sha256

In the same way, you can verify that the password for user alice is “mushroom”.

The openssl development library (pre-installed in Ubuntu on the QMB Lab PCs) provides the necessary functions to compute SHA256 hashes (you just need to add the library to your code with #include “openssl/sha.h”).

As a starting point for developing your login procedure, you can read the following Stack Overflow post:

• Generate sha256 with OpenSSL and C++

Functionality of the Login Procedures

Your secure and subverted login procedures must both satisfy the following requirements:

<ul>
<li>R1: The login procedure must work with the password file format described in the previous section.</li>
<li>R2: It must include the authlib.h header file and use the two functions defined therein.</li>
<li>R3: It must call the function void authenticated(std::string u), where u is the username,
whenever a user enters a correct username and password pair.

In addition, your secure login procedure must satisfy the following requirements:
</li>
</ul>
<ul>
<li>R4: It must call the function rejected(std::string u) if an invalid username and password pair was entered.</li>
<li>R5: It must not call authenticated(std::string u) unless a correct username and password pair for username u was entered.
It is up to you to decide whether your secure and subverted login procedures offer the user one or more attempts to log in before rejecting and exiting. Your secure and subverted login procedures may offer additional functionalities, which may help disguise backdoors, but shorter backdoored login submission will receive more marks (see the marking scheme for details on this).
</li>
</ul>
</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
You must not modify authlib.h or authlib.cpp. You cannot assume that the

</div>
</div>
<div class="layoutArea">
<div class="column">
functions in authlib.cpp will be implemented in the same manner when your code is

</div>
</div>
<div class="layoutArea">
<div class="column">
tested, so do not rely on this as part of the design of your login procedures. Likewise, you

</div>
</div>
<div class="layoutArea">
<div class="column">
can modify the passwords file as you work on your login procedures, but you cannot

</div>
</div>
<div class="layoutArea">
<div class="column">
change the filename or assume anything about the contents of this file when your code is

</div>
</div>
<div class="layoutArea">
<div class="column">
tested, other than they will follow the format above.

</div>
</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
Submission

This assignment must be handed in by one student in each group. Submit your assignment as a single ZIP file named after your group by the deadline.

The ZIP file must contain:

<ol>
<li>1) &nbsp;A file login.cpp. This is the secure password login procedure. Your login.cpp program must:
<ol>
<li>a) &nbsp;satisfy requirements R1–R5 above,</li>
<li>b) &nbsp;compile without warnings when the flags -Wall -pedantic -Wextra are used,</li>
<li>c) &nbsp;hash the submitted passwords with openssl’s sha256 hash function,</li>
<li>d) &nbsp;contain fully commented source code.</li>
</ol>
</li>
<li>2) &nbsp;A file login-subverted.cpp. This is the password login procedure with a backdoor. Your backdoor must:
<ol>
<li>a) &nbsp;allow you to login as root or any other user on the system without knowing their passwords,</li>
<li>b) &nbsp;satisfy requirements R1–R3 above,</li>
<li>c) &nbsp;compile without warnings when the flags -Wall -pedantic -Wextra are used,</li>
<li>d) &nbsp;hash the submitted passwords with openssl’s sha256 hash function,</li>
<li>e) &nbsp;contain fully commented source code (but comments may be misleading ;).</li>
</ol>
</li>
<li>3) &nbsp;A file report.pdf. This PDF file documents the vulnerability in your backdoored login procedure. Your report must :
<ol>
<li>a) &nbsp;be no more than 1 page and list the team name and team members,</li>
<li>b) &nbsp;describe the steps to trigger the vulnerability, i.e. how can an attacker login without
knowing a user’s password,
</li>
<li>c) &nbsp;show where the vulnerabilities are in the code,</li>
<li>d) &nbsp;explain why you think that your vulnerabilities are difficult to detect,</li>
</ol>
</li>
<li>4) &nbsp;A Makefile. This file compiles both your secure and your subverted login procedures.</li>
</ol>
</div>
</div>
</div>
