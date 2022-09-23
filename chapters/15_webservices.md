# Web Services

An essential component to all services is the ability to communicate at a distance. This is the entire principle of networking and the internet, to be able to send messages at a distance of various lengths, and receive them on another machine connected on the same network through a system of cables, and wifi, light, or infrared signals. Communicating between systems requires sockets, and servers. A typical communication of this sort is the communication we use in development often. We spin up servers on our local machines using a loopback address to view our content as we develop on our local system. Two of the most common web servers we see today are Apache and Nginx, if you work in development it is very likely you will be using either one, or sometimes both, of these web servers, though there are also many others out there.

We can encrypt the communication between browser and the web server (`mod_ssl`), use as a proxy server (`mod_proxy`), or perform complex manipulations of `HTTP` header data (`mod_headers`) and `URLs` (`mod_rewrite`). Here we will focus specifically on `Apache`. 

___

<div align="right">

[<< prev](./13_masking.md.md) | [next >>]()
</div>