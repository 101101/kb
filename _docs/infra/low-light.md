---
title: low-light
permalink: /docs/infra/low-light/
tags: 
 - infra
 - low-light
 - network
category: infra
description: What do do when a low-light alert is received  
---

## Low Light

> what to do when low light is identified on your fiber  

---

[![](https://101101.github.io/optical-test-points.png #Optical Test Points)  

**Steps**  
  1. Swap the two fiber jumpers at the switch (or server). One of them should be sending light to the switch. It’s possible that it’s connected to the transmitter instead of the receiver. The connectors on the duplex jumper are usually connected together. If they are connected, you may need to gently remove them from the connector and then swap the connectors  
  1. If swapping the fibers did not resolve the issue, I would get my light meter to look for the fiber stand with the light  
     1. It really does not matter what side of the link you start at, in this scenario, I’m going to start at the server, Test Point #1  
     1. Pull the fiber out of the server and look for light on either jumper. If you have a light level within the specifications of your optic that optical module may be bad  
     1. Repeat this same process at the switch (Test Point #6). If you have good light levels at the switch, one of your optical modules may have a bad receiver
  1. If the light levels are low, or not there at all you need to start eliminating segments of the fiber run. For this scenario, we have good light at the server from the switch, but low light at the switch from the server  
     1. I like to start at the source. Start at Test Point #1, I would use a known good fiber jumper to connect my light meter to the optical transmitter and get a light level reading. If there is low light, then your optical module may be bad. If you have a good light level, continue testing  
     1. Reconnect the original jumper to the server. Disconnect the jumper from the patch panel and test the light from there (Test Point #2). If the light is low, use your fiber scope to see if either side of the jumper is damaged or dirty. If the connector is dirty, use your fiber cleaner to clean it and then use the scope again to make sure it’s clean. If the connectors are clean with no damage to them, replace the jumper  
     1. If the light levels are good, repeat this process all of the way through Test Point #6. At each Test Point, make sure all connectors are firmly connected and clean  

---

