# Network Cabling Basics

## Overview

This note covers basic network cabling concepts used in structured cabling, Ethernet networks, and help desk troubleshooting. These concepts are important for understanding how devices physically connect to a network and how cabling issues can affect performance.

## Copper Ethernet Cabling

Ethernet networks commonly use twisted pair copper cabling. The wires inside the cable are twisted together in pairs to help reduce interference and crosstalk.

Common copper cable categories include:

* **Cat 5e:** Supports Gigabit Ethernet up to 100 meters
* **Cat 6:** Supports higher performance than Cat 5e and can support 10 GbE over shorter distances
* **Cat 6A:** Supports 10 GbE up to 100 meters
* **Cat 8:** Used mainly in data centers for short high-speed patch cable runs

## Solid vs Stranded Cable

### Solid Cable

Solid cable uses one solid conductor per wire. It is commonly used for permanent cable runs through walls, ceilings, ducts, and patch panels.

### Stranded Cable

Stranded cable uses multiple thin wire strands per conductor. It is more flexible and is commonly used for patch cables that connect devices to wall ports or patch panels to switches.

## Patch Panels and Patch Cords

A patch panel is used to organize and terminate structured cabling from different areas of a building.

A patch cord is used to connect:

* A wall port to a computer or network device
* A patch panel port to a switch port

## T568A and T568B Termination Standards

T568A and T568B are wiring standards used to terminate Ethernet cables.

Organizations should choose one standard and stay consistent to avoid wiring mistakes and connectivity problems.

For T568A:

* Pin 1: white/green
* Pin 2: green
* Pin 3: white/orange
* Pin 4: blue
* Pin 5: white/blue
* Pin 6: orange
* Pin 7: white/brown
* Pin 8: brown

## Common Cabling Tools

### Cable Crimper

Used to attach an RJ-45 plug to the end of a cable to create a patch cord.

### Punch Down Tool

Used to terminate fixed cable into IDC terminals on patch panels, keystone jacks, or punchdown blocks.

### Wire Stripper

Used to remove the outer jacket from a cable before termination.

### Cable Tester

Used to test cables for wiring issues such as opens, shorts, reversed pairs, crossed pairs, and split pairs.

## Common Cable Issues

### Attenuation

Attenuation is signal loss over distance. Copper Ethernet cable runs are normally limited to 100 meters.

### Crosstalk

Crosstalk happens when signals from one wire pair interfere with another pair inside the cable.

### Alien Crosstalk

Alien crosstalk is interference from nearby cables or external sources.

### Electromagnetic Interference

Electromagnetic interference, or EMI, can come from electrical power cables, fluorescent lights, motors, and other electrical equipment.

## Best Practices

* Avoid running Ethernet cables too close to power cables
* Avoid sharp bends in cables
* Do not pull cable with too much force
* Keep wire pairs twisted as close to the termination point as possible
* Label both ends of cable runs
* Leave a service loop for future adjustments
* Test cable runs after installation
* Use the correct cable type for the environment

## Help Desk Connection

Understanding network cabling helps IT support technicians troubleshoot issues such as no network connection, slow speeds, intermittent connectivity, and failed cable tests. Even when a technician is not installing cable, knowing the basics helps with documentation, escalation, and communication with network teams.
