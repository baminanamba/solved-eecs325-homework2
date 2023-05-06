Download Link: https://assignmentchef.com/product/solved-eecs325-homework2
<br>
<ol>

 <li> Consider a web page whose base file is of size <em>S</em><sub>1 </sub>= 10 KB. Assume that the web page consists of <em>N </em>= 20 inline objects each of size <em>S</em><sub>2 </sub>= 100 KB. Assume that the round-trip time to the web server is <em>T </em>= 100 ms and the bottleneck capacity is <em>C </em>= 10 Mbps. Ignore any packetization delays and header overhead.

  <ol>

   <li> Assuming non-persistent HTTP is used with a single TCP connection, how</li>

  </ol></li>

</ol>

long does it take to download the web page?

<ol>

 <li> Assuming non-persistent HTTP is used with 4 parallel TCP connections,</li>

</ol>

how long does it take to download the web page?

<ol>

 <li> Assuming pipelined, persistent HTTP is used, how long does it take to</li>

</ol>

download the web page? ”Pipelined” means requests for multiple objects can be sent back-to-back on the same connection.

<ol>

 <li> Assuming non-pipelined, persistent HTTP with 2 parallel TCP connections</li>

</ol>

is used, how long does it take to download the web page? Assume that the 2 parallel connections equally share the total available bandwidth C.

<ol start="2">

 <li> Consider the figure used to illustrate Web caching below. Suppose that the access link capacity is <strong>C </strong>bits/sec and the average object size is <strong>S </strong>bits and that the average request rate from the institution’s browsers to the origin servers is <strong>A </strong>requests/sec. Also suppose that the amount of time it takes from when the router on the Internet side of the access link forwards an HTTP request until it receives the response is <strong>T </strong>seconds on average. Model the total average response time perceived by the institutional users as the sum of the average access delay (that is, the delay from the Internet router to institution router) and the average Internet delay. For the average access delay, use</li>

</ol>

, where <strong>D </strong>is the average time required to transmit an object over the access lnik and <strong>B </strong>is the arrival rate of objects to the access link. Note that this access delay includes both the transmission and queuing delays. (Note also that B = A if there is no caching.) Ignore the details of persistent or non-persistent HTTP in this question as well as any LAN delays.

<ol>

 <li>What is the total average response time <em>T</em><sub>1</sub>?</li>

 <li> Now suppose a cache is installed in the institutional LAN and its hit rate is</li>

 <li><em>p</em>. What is the total average response time <em>T</em><sub>2</sub>?</li>

 <li>We didn’t model DNS delays above. Suppose the root, TLD, and authoritative name servers are located at round-trip latencies of <em>R</em><sub>1</sub>, <em>R</em><sub>2</sub>, <em>R</em><sub>3 </sub>seconds respectively.</li>

</ol>

What is the additional delay introduced by DNS if

<ol>

 <li> the institution maintains a local name server internally in its LAN</li>

 <li> the local name server in maintained by the institution’s ISP at a round-trip distance of <em>R</em><sub>0</sub></li>

 <li>a.  The DNS root hints file is a file that all DNS resolvers have to be able to bootstrap their resolution abilities. It is located at http://www.internic.net/domain/named.root, and it has entries for each root server as such:</li>

</ol>

<table width="517">

 <tbody>

  <tr>

   <td width="205">.</td>

   <td width="107">3600000</td>

   <td width="205">NS          A.ROOT-SERVERS.NET.</td>

  </tr>

  <tr>

   <td width="205">A.ROOT-SERVERS.NET.</td>

   <td width="107">3600000</td>

   <td width="205">A            198.41.0.4</td>

  </tr>

  <tr>

   <td width="205">A.ROOT-SERVERS.NET.;</td>

   <td width="107">3600000</td>

   <td width="205">AAAA 2001:503:ba3e::2:30</td>

  </tr>

  <tr>

   <td width="205">.</td>

   <td width="107">3600000</td>

   <td width="205">NS          B.ROOT-SERVERS.NET.</td>

  </tr>

  <tr>

   <td width="205">B.ROOT-SERVERS.NET.</td>

   <td width="107">3600000</td>

   <td width="205">A            199.9.14.201</td>

  </tr>

  <tr>

   <td width="205">B.ROOT-SERVERS.NET.</td>

   <td width="107">3600000</td>

   <td width="205">AAAA 2001:500:200::b</td>

  </tr>

 </tbody>

</table>

If you have only this file, how can you use the information in it, and dig, to look up www.facebook.com? List the steps you need to take (along with the answer you might get), using the syntax dig &lt;name&gt; @&lt;server&gt; &lt;record type&gt; +norecursive. b. Suppose you run a website at www.foo.net:

iWhich name servers need to change their databases if you decide to change the name to www.foo.com? ii (1pt) To web.foo.net?

iii  What needs to change if you decide to keep the name www.foo.net, but change the IP address?

<ol>

 <li>Explain why using a DNS resolver out on the Internet (i.e., open resolver) can result in poor choice of CDN servers.</li>

</ol>