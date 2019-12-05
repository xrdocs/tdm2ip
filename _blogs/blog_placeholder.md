---
published: false
date: '2019-12-05 09:37 +0530'
title: 'A look into Business Benefits of Network Modernisation '
---
# Introduction

Legacy Infrastructure has reached a stage where operators who have invested in PDH, SONET, and/or SDH networks and services must decide on when and how to migrate these legacy networks to next-generation architectures.Transitioning from TDM to IP is no longer a question of “why” but rather “when”. Replacing the legacy PDH/SONET/SDH gears has become a priority for Enterprise, Public Sector Organisations, Utilities or Service Providers. Operators need to get away from deploying, supporting and maintaining multiple separate networks and instead move towards consolidating all services onto a single network in order to reduce the cost of running their network.


# Figure 1: Legacy Metro Network

![Screenshot 2019-11-28 at 10.08.39 AM.png]({{site.baseurl}}/images/legacy_network.png)

# Business Challenges

Figure 1, shows snapshot of a typical Legacy TDM network. Along with the older gears like Add/Drop Multiplexers (ADM), Digital cross connects etc, it has separate network to cater the packet switching. These networks have served well for several years but operators are now facing challenges to maintain them. Below are some of the influx points for TDM to IP Migration:

- **Equipment has reached end-of-life (EOL)**: For many customers, the SONET/SDH installed base is already exceeding the lifespan for which it was intended. Most of the gears are already obsolete and parts are increasingly difficult to find.
- **Increasing operational costs**: Operators face increasing operational costs running legacy networks due to several factors like higher faults and time taken to resolve it causing increased service degradation.
- **Automation**: Lack of automated processes make maintenance activities longer, increasing costs.
- **Power Saving**: Legacy gears has large footprints and high-power consumption compared to today's packet-optical technologies, leading to wasted space and excessive and unnecessary power and cooling costs.
- **Network Simplicity**: Maintaining separate networks for TDM and packet adds to operational and organizational costs.
- **Lack of Vendor Support**: Vendors have reduced or stopped supporting legacy equipment because the market has dropped 95 percent from its peak. Some legacy suppliers are actually no longer in the business. Vendors are not able to provide software patches on time during failure of equipments causing security concerns.
- **Lack of qualified personnel**: As equipment ages, fewer qualified technicians are available to support it. This leads to higher operational costs and increased risk of service outages.


Customers have 3 options in front of them:

![Screenshot 2019-11-28 at 11.30.46 AM.png]({{site.baseurl}}/images/options.png)


As shown in Figure 2 , annual global SONET/SDH equipment spending has dropped drastically year over year.

# Figure 2: Global SONET/SDH Equipment Spending Trend

![Screenshot 2019-11-26 at 12.07.49 PM.png]({{site.baseurl}}/images/trend.png)

# Circuit Emulation for TDM to IP Migration

It is absolutely clear that operators around the geography face a big challenge: How do they move away from the Legacy infrastructure in their own networks without losing end customers? How do they move from a complex architecture to a more simplified one? Due to lack of a strategic plan, most operators have simply either delayed the decision or ignoring the risks of not migrating. However, the problem has now become so severe that doing nothing is no longer an option. 

Fortunately, Circuit Emulation (CEM) has emerged as a means of circuit-to-packet migration, though many customers may not yet be aware of its scalability or its benefits. 

Today, there are three major IETF-defined CEM standards addressing different data rates over a packet-switched network.

- **Structure-Agnostic TDM over Packet (SAToP)**: SAToP defines pseudowire en-capsulation for T1/E1 and T3/E3 bitstreams over packet-switched networks. See RFC 4553.
- **Circuit Emulation Service over Packet Switched Net-work (CESoPSN)**: CESoPSN defines pseudowire encapsulation of lower bit-rate nxDS-0 streams over packet-switched networks. See RFC 5086.
- **Circuit Emulation over Packet (CEP)**: CEP defines pseudowire en-capsulation for emulating SONET/SDH circuits over packet-switched networks. See RFC 4842.


# Figure 3: Circuit Emulation for TDM2IP Migration

![Screenshot 2019-11-27 at 11.21.58 AM.png]({{site.baseurl}}/images/cem.png)

As shown in above figure, the CEM router receives the raw TDM frame, adds on CEM encapsulation, and then transmits the frame towards the packet core. (Cisco CEM solution has MPLS Bidirectional LSP in the packet core).The MPLS core label-switches the frame based on the LSP. The receiving CEM router receives the frame, removes the CEM encapsulation and serializes the frame from the dejitter buffer towards the TDM endpoint.

CEM is designed to closely resemble the service characteristics of a circuit switching technology over a packet network. Critical circuit characteristics include operations, administration and management (OA&M) functions, predictable and deterministic transmission, and sub-50 ms resiliency in failures, achievable using packet network protection technology such as MPLS Traffic Engineering (Bidirectional MPLS Tunnels).


# Key Benefits of Migration

- **Measured Migration for Operators and their Customers**: Migration to modernized transport allows operators to swap their aging equipment without service changes to their customers. Customer end points remains untouched over end-end Packet Switched Network.
- **Immediate Operational Benefit**: Migration with Circuit Emulation does not require full network overhaul. Power and maintenance costs goes down, while central office floor space can be opened for new opportunities.
- **Path to automated network operations**: Much better architecture to enable automation.Easier software upgrades and proactive identification of problems before they impact services.
- **Maintaining 50ms resiliency**: Use MPLS transport with RSVP protocol provides pre defined bandwidth and guaranteed sub milliseconds protection.
- **Retaining SONET-like OA&M**: Circuit Emulation provides OA&M functions which closely matches the legacy SONET/SDH infrastructure.
- **Scalability & Operational Simplicity with MPLS**: Pseudowires’s mapped with traffic engineering tunnels provide bi-directional path, protection & co-routing just like TDM networks


## Conclusion

The problem due to aging infrastructure has reached such a critical point that operators can no longer ignore it. Migrating to the modernized packet network is the most viable solution. Operators should move away from legacy gears in their network, without disrupting their customers that require the private line functionality. Circuit Emulation has matured to provide the most efficient solution to the problem, enabling a measured migration for operators and their customers while retaining reliability (including 50 ms resiliency) and SONET-like OA&M. With CEM, operators can reap the operational benefits of a modern packet-switched network while retaining existing private line service revenue.