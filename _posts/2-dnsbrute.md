---
title: 'A custom DNS brute forcing flow'
date: 2023-09-6
permalink: /posts/2/
tags:
  - tools
  - presentations
---

This is a sample blog post. Lorem ipsum I can't remember the rest of lorem ipsum and don't have an internet connection right now. Testing testing testing this blog post. Blog posts are cool.

A a custom DNS brute forcing flow
======
Maximizing subdomain discovery is crucial for effective reconnaissance. DNS brute-forcing is a powerful technique used to identify live subdomains by querying multiple subdomains through DNS. To increase the chances of discovering as many subdomains as possible, a custom and intelligent approach is employed.

The approach involves two phases. In the first phase, subdomains are passively gathered from various providers like Shodan, Common Crawl, or SecurityTrails and many others using the Subfinder tool developed by the ProjectDiscovery team. A list of subdomains is then generated based on a pre-prepared wordlist, and these generated subdomains are merged with the passively obtained ones. This merged list is then given to shuffleDNS which is a wrapper around MassDNS, a high-performance DNS stub resolver. 

In the second phase, a smart subdomain generator like AlterX or DNSgen is used to generate subdomain names based on specific patterns provided by the resolved subdomains from the first phase. The output of AlterX or DNSgen is then given to shuffleDNS. The final result is the resolved subdomains from both phases that are sorted, and deduplicated.

By leveraging this approach, which combines passive gathering, wordlist-based generation, and smart pattern utilization, DNS brute-forcing becomes more effective in discovering a comprehensive list of subdomains associated with the target company.

Github link: https://github.com/0xGwyn/ResolveRaptor