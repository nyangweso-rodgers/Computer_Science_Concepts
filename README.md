# Introduction to Computer Science
## Computer Science Concepts

## 1. Definition of Terms
### 1.1 Payload
When data is sent over the Internet, each unit transmitted includes both header information and the actual data being sent. The header identifies the source and destination of the packet, while the actual data is referred to as the __payload__. Because header information, or overhead data, is only used in the transmission process, it is stripped from the packet when it reaches its destination. Therefore, the __payload__ is the only data received by the destination system.

#### References
_https://techterms.com/definition/payload_

### 1.2 Cookies
By example. __cookies__ are something that bring you back to your Twitter account after you have signed in with _Remember me checkbox_ checked. By definition, _small chunk of information (4KB) that browser stores on behalf of Web server_.

#### Mechanism Behind Cookies
* server asks the browser to store this using a _Set-Cookie_ header.
* browser and server pass this info to and fro as part of request and response headers
* stores a name value pair and attributes like Expires, Domain, Path.
* Cookie in the header when communicating from Browser to server.
* Set-Cookie in the header when communicating from server to browser.
* These HTTP Cookies are used to store the name value pair that identify you. So, the next time you visit, your session is restored.
* It is used by numerous websites to track your online activities

#### Types of Cookies
1. Session Cookies
2. Persistent/Permanent Cookies
3. Third Party Cookies

#### Cookies vs. Session
__Session__ is a period with all the parameters that suggest you are active on the website. __Cookies__ help in recognising and managing the session.Cookies are primarily used to create session and related info for web application. They get deleted when the session expires. 

_Note_: not all cookies are related wit session, some remain persistent


### 1.3 IP Addresses
The __IP address__ is a fascinating product of modern computer technology designed to allow one connected computer (or “smart” device) to communicate with another device over the Internet. Because, in the same way you to need a mailing address to recieve a letter in the mail from a friend, a remote computer needs your __IP address__ to communicate with your computer.

#### 1.3.1 The IPv4 Address.
The common type of __IP address__ (is known as __IPv4__, for “__version 4__”). Here’s an example of what an __IP address__ might look like: __66.171.248.170__

An __IPv4__ address consists of __four numbers__, each of which contains one to three digits, with a single dot (.) separating each number or set of digits. Each of the four numbers can range from 0 to 255. This versatile group of segmented numbers create the addresses that lets you and everyone around the globe to send and retrieve data over our Internet connections. Without this numeric protocol, sending and receiving data over the World Wide Web would be impossible.

#### 1.3.2 IPv6 (Internet Protocol Version 6)
It’s called __IPv6__ and it offers a maximum number of __IP address__ for today and for the future. Whereas __IPv4__ supports a maximum of approximately 4.3 billion unique IP addresses, __IPv6__ supports, in theory, a maximum number that will never run out. An __IPv6__ address consists of __eight groups__ of four hexadecimal digits. If a group consists of four zeros, the notation can be shortened using a colon to replace the zeros. Here’s an example IPv6 address: __2001:0db8:85a3:0000:0000:8a2e:0370:7334__

__REMARK:__ _Your IP address is your passport to the Internet. But it also gives away your location and is used to profile your individual online activity. That’s why you might consider hiding it._

A main advantage of __IPv6__ is increased address space. The 128-bit length of IPv6 addresses is a significant gain over the 32-bit length of IPv4 addresses, allowing for an almost limitless number of unique IP addresses. The size of the IPv6 address space makes it less vulnerable to malicious activities such as IP scanning. IPv6 packets can support a larger payload than IPv4 packets resulting in increased throughput and transport efficiency.

#### References
__https://whatismyipaddress.com/ip-address_

### 1.4 Caching
__Caching__ is a common practice in different layers of technology to _improve application performance_. A __cache__ is a high speed data store which stores a part or the complete dataset so that future requests to the data are served faster. The data in a cache is stored on a fast access hardware like __RAM__. Caching allows us to _efficiently reuse previously retrieved data_. 

__Caching__ is leveraged at different layers of technology like:
* Operating systems
* CDN(Content Delivery Network)
* DNS(Domain Name Systems)
* Web Applications(APIs)
* Databases e.t.c.

__Caching__ information includes:
* database query results
* computationally intensive caclculations
* API requests/responses
* data files like HTML, images or
* any application data in general e.t.c

In _distributed applications_ there are various caching _strategies_:
* write-through
* write-around
* write-back

#### 1.4.1 write-through cache
in this policy, data is written to both the cache and the underlying data source. The order in which it is written is not important. The main idea is that the I/O operation is considered complete when the data is written to both the cache and the DB.

#### 1.4.2 write-around cache
in this policy, data is directly written to the underlying data source without disturbing the cache.

#### 1.4.3 write-back cache
in this policy, data is written only to the cache and the I/O operation is considered complete. Typically, data is written  to the underlying data source as well, but it is done asynchronously using a worker process.

#### Benefits of caching
1. improves application performance
2. reduced load on servers
3. reduced load on databases
4. eliminates database hotspots
5. increases Read Throughput(IOPS)
6. reduces bandwidth consumption


### 5. LocalHost
__localhost__ refers to “_this computer_” or even more accurately “_the computer I’m working on_.”

#### References
_https://whatismyipaddress.com/localhost_

### 6. Collection Concurrency
__Concurrency__ is when multiple instructions execute at the same time(concurrently)

#### 6.1 Situations for Concurrency
##### 6.1.1 Multiple Threads
* multiple threads executing within a single process
* _Example_: Multi-threaded .NET application accessing a shared collection

##### 6.1.2 Multiple Processes
* Several processes executing on a single computer system
* _Example_: Multiple applications accessing a common file

##### 6.1.3 Multiple Systems
* Several systems, each accessing a common resource
* _Example_: Multiple processes accessing a common database table.