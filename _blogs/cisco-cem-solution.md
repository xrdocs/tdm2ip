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

MPLS OAM supports provisioning and maintenance of MPLS bidirectional LSPs. Generic Associated Channel (G-Ach) is the control mechanism associated with MPLS LSPs. G-ACh Label (GAL) (Label 13) is taken from the reserved MPLS label space.

G-ACH: is used by MPLS-TP to carry management, OAM and potentially other traffic across MPLS-TP LSP
Channel Type value for fault OAM is 0x58
GAL: Label value 13 is used for indicating to the device that packet contains G-ACH and that the contents should be processed by the local device
GAL is not used for forwarding decision such as QoS
TTL of GAL is not examined when processing GAL
TTL will be set 255 in XR implementation at ingress
BFD and OAM packets can be encapsulated with GAL/G-ACH


The OAM messages are used for fault management, connection verification, continuity check and other functions.
Fault OAM messages are encapsulated with GAL/G-ACH, and are inserted in bidirectional LSPs and sent in the direction away from the fault
Transmission of any OAM messages:
Initially 3 messages are transmitted at an interval of 1 sec 
Subsequent messages are transmitted at the refresh interval specified in the message
A fault is assumed to be cleared either of when:
OAM message times out after waiting for 3.5 * refresh interval
Fault message are received with R-bit is set to 1

