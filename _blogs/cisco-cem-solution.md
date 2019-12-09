---
published: false
date: '2019-12-09 12:15 +0530'
title: Cisco CEM Solution
author: Tejas Lad
excerpt: >-
  This Blog describes the Cisco CEM solution based on MPLS FleX LSP and the
  benefits of using MPLS FLeX LSP as the transport networ
---
# Introduction

In the previous [blog](https://xrdocs.io/tdm2ip/blogs/network-modernization/ "blog"), we discussed the business challenges the operators are facing and how moving away from the legacy networks can benefit them. In this blog, we will look into Cisco CEM Solution and how it can benefit the operators.

# Cisco CEM Solution

![cisco-cem-soln.png]({{site.baseurl}}/images/cisco-cem-soln.png)

As shown above, Cisco CEM solution is a cost effective migration path for operators with ongoing TDM service requirements. Supported by industry standards, the solution enables the operators to drastically reduce the OpeEX and scale the network for future growth. With CEM technology, operators can modernize their transport network without service disruption or changing the CPE (customer premise equipment).

# MPLS Flex LSP

Cisco CEM solution is based on MPLS Flex LSP which is also known as Associated Bidirectional LSP.

![Screenshot 2019-12-09 at 1.50.30 PM.png]({{site.baseurl}}/images/Screenshot 2019-12-09 at 1.50.30 PM.png)

As shown in Figure 2, it provides bidirectional label switched paths (LSPs). The LSPs are set up dynamically through Resource Reservation Protocol–Traffic Engineering (RSVP-TE). Flex LSP is a combination of static bidirectional MPLS-TP (MPLS Traffic Profile) and dynamic MPLS-TE (MPLS Traffic Engineering).

In Flex LSPs, the forward and the reverse direction paths are setup, monitored and protected independently and associated together during signaling. RSVP Association object is used to bind the two forward and reverse LSPs together to form a co-routed associated bidirectional TE tunnel.
Tunnel is configured with matching association ID, association source, optional global association source. The working LSP is the primary LSP backed up by the protecting LSP. When a working LSP goes down, the protecting LSP is automatically activated. 


# Comparison of MPLS TP, MPLS-TE and MPLS Flex LSP

![comparison of mpls.png]({{site.baseurl}}/images/comparison of mpls.png)

# MPLS OAM


