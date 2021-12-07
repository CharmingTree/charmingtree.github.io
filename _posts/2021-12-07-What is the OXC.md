
---
layout: post
title: What is the OXC (Optical Cross-Connect)
hide_title: false 
bootstrap: true                                   # Add bootstrap to the page
tags: [transmission, network]
---



<H3>What is the OXC (Optical Cross-Connect)?</H3>

---

We know that the [optical network](https://www.router-switch.com/optical-network-price.html?utm_source=blog&utm_medium=blog&utm_campaign=oxc) is the cornerstone of modern communication networks.

Without the support of a powerful optical network, large bandwidth and low latency application scenarios including 8K video, VR/AR, smart factories, smart cities, and smart transportation cannot be perfectly realized. [5G](https://www.router-switch.com/5g-devices-price.html?utm_source=blog&utm_medium=blog&utm_campaign=oxc) and [F5G](https://blog.router-switch.com/2020/12/what-is-f5g-f5g-vs-5g/) will not work either.

<strong>**Why do we need the OXC?**</strong>

ROADM is one of the key technologies of all-optical networks. Its main purpose is to further realize node optical switching on the basis of line optical switching.

ROADM evolves to CDC-F ROADM, basically realizing extremely strong optical switching capabilities. However, it is still not the ultimate solution for all-optical networks.

ROADM has some problems. One of the biggest problems is the complexity of fiber connection.

ROADM usually connects optical fibers one by one according to business expansion. Over time, the plan may change, or the network needs to be adjusted, and optical fibers will continue to be added.

Over time, the fiber connecting becomes chaotic and difficult for operation and maintenance. With ROADM, the number of racks is relatively large, and it takes up a large space.

As a result, a better and more suitable all-optical switching technology was pushed to the front, that is, OXC.

<strong>**What is the OXC?**</strong>

OXC, the full name is optical cross-connect.

Like ROADM, OXC is also an optical transmission device that can exchange optical signals between different optical paths.

The concept of OXC actually existed as early as around 2000. In a sense, ROADM is a special implementation of OXC, and OXC includes ROADM.

From the perspective of traditional architecture, OXC is composed of optical cross-connect matrix, input interface, output interface, management control unit and other modules. The optical cross-connect matrix is the core of OXC. The so-called matrix is actually a “box” with any internal ports interconnected in pairs.

We will explain with the architecture of [Huawei](https://www.router-switch.com/huawei.html?utm_source=blog&utm_medium=blog&utm_campaign=oxc)‘s OXC equipment.

The OXC equipment is mainly composed of optical circuit boards, optical backplanes and optical tributary boards.

Generally speaking, each slot of the circuit board corresponds to one direction. After the optical signal enters, it is “disassembled” into N wavelength signals through WSS (Wavelength Selective Switch).

Earlier WSS switches used MEMS mechanical architecture. This structure has a high failure rate and poor reliability. Later, it evolved into the LCoS (liquid crystal on silicon) solution, which natively supports the Flexi-Grid function, supports variable channel widths and super channels, and has significantly higher reliability than MEMS.

In principle, the LCoS solution uses phase-controlled wavelength selection, no mechanical vibration, no optical amplification for upper and lower waves, and a direction dimension of up to 32 dimensions, achieving super large crossover capacity and lower power consumption.

The wavelength optical signal passes through the optical connector and enters the optical backplane from the optical circuit board.

Optical backplane is an important difference between OXC and ROADM, and has a high technical content. It is equivalent to printing many optical fibers on a piece of paper to realize optical connection.

The optical backplane provides support for large switching capacity and nanosecond delay.

After the wavelength optical signal comes out of the optical backplane, it enters the optical tributary board, and an N×M WSS is constructed by adding a level of LCoS crystal plane adjustment.



<strong>**What is the difference between OXC and ROADM?**</strong>

OXC is very similar to ROADM, except that OXC introduces hardware such as an optical backplane, which replaces the internal optical fiber box, and realizes the fiber-free connection in the rack, and “0” fiber jumper, thus avoiding human operation errors and improving system reliability.

| **Features**                          | **ROADM**                                                    | **OXC**                                                      |
| ------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Expandability**                     | Few exchange directionsPoor network scalability              | Many exchange directionsStrong network scalability           |
| **LF**                                | Occupies more space in the computer roomHigh power consumption | Occupies less space in the computer roomLess power consumption |
| **Network operation and maintenance** | There are many internal optical fiber connections, many board transfers, complex systems, many site failures, and difficult operation and maintenance. | “0” fiber jumper, high system integration, few failure points, simple maintenance |
| **Equipment cost**                    | Higher                                                       | Lower                                                        |



OXC also brings more flexible configuration capabilities. Based on OXC and its switching matrix, engineers only need to perform data configuration (wavelength configuration) through the network management, and then they can quickly open the service (minute level).

The above is the architecture and characteristics of OXC.

Today, as an all-optical crossover platform, OXC has large-dimensional non-blocking switching capabilities and extremely high cross-transfer capacity.

The role of OXC is to serve all-optical switching and all-optical scheduling.

If you have other opinions, welcome to leave your comment.





(출처 : https://blog.router-switch.com/2021/01/what-is-the-oxc-optical-cross-connect/)
