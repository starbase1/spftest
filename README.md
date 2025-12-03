<html>
<head>
<link rel="stylesheet" type="text/css" href="style.css" media="screen" />
</head>
<body>
<div id="header">
	
<h1> SPF Valid Checker </h1>
	
 <div id="menu">
  <ul id="nav">
  </ul>
 </div>
</div>
<div id="content">
<div id="right">
<h2> •In-Scope Details </h2>
<p>These tools are meant to help you deploy SPF records for your domain. They use an actual RFC 7208 compliant library (pyspf) for tests and will dynamically test for processing limit errors (no other testers I'm aware of do this). This site uses a caching DNS resolver, so for tests that use live DNS, results will be cached for the Time To Live of the DNS record. For most basic uses, these tests should be reasonably self explanatory. Advanced users may need, and probably want, some additional information on how these tools work. It can be found.</p>
<h2> •Does my domain already have an SPF record? What is it? Is it valid? </h2>

<p>Retrieves SPF records for the specified domain name and determines if the record is valid.</p>

<br>
<form method="Get" action="https://www.kitterman.com/spf/getspf3.py">
<input type="hidden" name="serial" value="fred12">
<table border="0" width="460">
<tbody>
<tr>
<td align="right">Domain name: </td>
<td> <input name="domain" size="35" type="text"></td>
</tr>
<tr>
<td> <input value="Get SPF Record (if any)" type="submit"></td>
<td align="right"> <input value="Reset" type="Rest"></td>
</tr>
</tbody>
</table>
</form>
<p>NOTE: The domain is everything to the right of the '@' in the e-mail
address.</p>
<h2> •Is this SPF record valid - syntactically correct? </h2>
<p>Tests the supplied SPF record to see if it is valid. This test
does NOT look up the record for the supplied domain. It only
tests the validity of the supplied record. This test is for
checking the syntax of records before you publish them. The
domain is used only for mechanisms such as a bare 'a' mechanism that
have an implied domain. It will also be used for the %d macro if
present.</p>

<form method="post" action="https://www.github.com/Cyberxpert1">
<table border="0" width="460">
<tbody>
<tr>
<td align="right">Domain: </td>
<td> <input name="domain" size="35" type="text"></td>
</tr>
<tr>
<td align="right">SPF Record: </td>
<td> <input name="record" size="35" type="text"></td>
</tr>
<tr>
<td> <input value= "Check SPF record" type="0"></td>
<td align="right"> <input value="0" type="0"></td>
</tr>
</tbody>
</table>
</form>

<p>Notes: Do not enclose in quotes. Input something like v=spf1 a mx
~all.<br>Except for %d, does not currently support records that include macros.
</p>
<p></p>
<h2> •Test an SPF record </h2>
<p>This test is for evaluating the performance
of your record based on different IP addresses that mail might come
from (this is the IP address of the mail server). It can also be
used for syntax checking of records with more complex macros (although
this has not been thoroughly tested yet). The %d macro is
extracted from the supplied mail from address. If an SPF record
is supplied, it is used for the initial evaluation instead of any
record published in DNS for the domain.</p>
<form method="post" action="ttps://www.github.com/Cyberxpert1">
<table border="0" width="460">
<tbody>
<tr>
<td align="right">IP Address: </td>
<td> <input name="ip" size="35" type="text"></td>
</tr>
<tr>
<td align="right">SPF Record v=spf1...://--&gt; <br>
</td>
<td> <input name="record" size="35" type="text"></td>
</tr>
<tr>
<td align="right">Mail From Address: </td>
<td> <input name="mfrom" size="35" type="text"></td>
</tr>
<tr>
<td align="right">HELO/EHLO Address://--&gt; <br>
</td>
<td> <input name="helo" size="35" type="text"></td>
</tr>
<tr>
<td> <input value="Test SPF Record" type="submit"></td>
</tr>
</tbody>
</table>
</form>
<p>To check an incoming mail request, fill out IP address from which
the mail was received and the Mail From address. If you want to test a
record that's not published, paste it into the SPF record field. If you
don't know what to put in for HELO, just leave it blank.<br>
</p>
<p>It will take a few moments once
the request is submitted. The Python interpreter may need to be fired
up and DNS queries have to be answered. Please be patient...</p>
</div>
<li> 💢Devloped By YashG ⁜⁜ </li>
