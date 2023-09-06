---
title: 'Dynamic URL Query Modifier for Discovering Reflection and Abnormal Behavior'
date: 2023-09-6
permalink: /posts/3/
tags:
  - tools
---

This is a sample blog post. Lorem ipsum I can't remember the rest of lorem ipsum and don't have an internet connection right now. Testing testing testing this blog post. Blog posts are cool.

Summary
======
One of my favorite web application vulnerabilities is XSS (Cross-Site Scripting), often referred to as a low hanging fruit bug. Among the types of XSS vulnerabilities, there is the reflected type, where the value of a parameter in the URL's query part or sometimes in the body of a POST request is reflected on the page. 

This tool manipulates a list of URLs to modify the query parameters or values, generating a list of modified URLs based on different strategies. These modified URLs can be used in other applications like Nuclei to test for reflections with the right template. It is particularly useful for mass hunting, where we aim to test a large number of targets to uncover reflections. If any reflections are found, we can manually work on them to exploit or escalate the impact and finally report it responsibly to the corresponding company.

Github link: https://github.com/0xGwyn/x9