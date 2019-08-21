# ch34x
Clone of the CH34x library, which is commonly used in serial connections with Arduino boards

This product has been derived from the CH341_LINUX.ZIP source code from url [http://www.wch.cn/products/CH340.html]
The code in the above library however is faulty, and does not compile.  Corrections to the product have been made to address these issues.

To compile run:
- make

To install into an Ubuntu 19.04 operating system (elevation to administrator required):
- sudo make load

Note: Ubuntu comes with an existing CH341 driver, however it isn't particularly polished.

It is worth blacklisting the original kernel module by adding it to the following file:\s\s
**/etc/modprobe.d/blacklist**

The record to add should read something like:\s\s
**#Blacklist of CH341 kernel module to prevent collision with new ch34X driver**\s\s
**blacklist ch341**