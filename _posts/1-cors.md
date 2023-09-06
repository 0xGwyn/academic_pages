---
title: 'Cross Origin Resource Sharing misconfiguration fuzzer'
date: 2023-09-6
permalink: /posts/1-cors/
tags:
  - tools
---

This is a sample blog post. Lorem ipsum I can't remember the rest of lorem ipsum and don't have an internet connection right now. Testing testing testing this blog post. Blog posts are cool.

Summary
======
Browsers employ various mechanisms to facilitate requests for resources from different origins, including the postMessage feature, JSONP (JSON with Padding), and CORS (Cross-Origin Resource Sharing) which is the most widely used among them. Misconfiguring CORS can have severe implications. One common misconfiguration involves granting unauthorized access to resources from another origin. For instance, if a bank website has a misconfigured CORS policy in its "/credentials" path, an attacker can exploit this vulnerability by creating a malicious webpage. When unsuspecting victims click on a link leading to the attacker's webpage, they unknowingly send a request to the bank's "/credentials" path. The attacker's code can then read and extract the victims' credentials, which are sent to the attacker's server. These misconfigurations often occur due to inadequate enforcement measures, such as flawed regex patterns used for whitelisting or blacklisting. 

This tool tests a list of URLs for CORS misconfigurations. It does this by manipulating the "Origin" header in requests using a curated list of origins that can potentially bypass regex patterns. By analyzing the CORS-related headers in the responses, the tool identifies any potential vulnerabilities.

I have to thank Mr. Reza Sarvani for his idea regarding this fuzzer.