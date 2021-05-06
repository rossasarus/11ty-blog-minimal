---
title: "Threat modeling 101"
date: "2021-05-05"
published: true
tags:
- threat modeling
- l33t h4x0r
---
I was lucky this week to be able to attend 2 days of threat modeling training. I didn't even know all that much about it before volunteering but I knew the company doing it also does penetration tests so I was IN. 

Ultimately it was really cool, taught me a lot, and gave me so many more things that I want to learn about now!


<!-- excerpt -->
# What is threat modeling?
Threat modeling is the concept of analyzing an application and breaking it down into small chunks that each can have their dependencies and 'threats' listed out. Looking at a giant wall from a distance makes it look massive, but when you get closer you can start to see the cracks. Once those threats have been identified they can be modeled, mitigated, and tested. It was repeatedly stressed that a perfect threat model is an impossibility, so start with what you have, make it better, and then repeat.

## What is the output of a threat modeling session?
Most people represent threat models visually with a data flow diagram. The diagrams use different shapes to represent different entities. One example of a diagram 'key' is:
- External Entities - square
- Process - circle
- Data store - disk shape
- Data Flow - arrow
- Trust Boundary - dotted line

Those shapes can be combined into a diagram that looks like this to represent a service.
{% asset_img 'threat_model.png' 'example threat model' %}

There is also an acronym called STRIDE that's either the bad guys in GI JOE, or something that represents the types of attacks and the tasks needed in order to remove them from your application.

## ...that's it?
Yeah - but it's not as easy as it looks. This is a process where you look at an application and carefully consider all of the api calls, processes, data storage services and more. Looking at each one and listing out the ways in which it could be broken (or even just listing how bad it would be if it was broken) can teach you a TON about how fragile your app actually is.

## What did I learn?
Ah, this is the cool part. All of the above would be pretty simple (and easy if, and worthless) you didn't know how sites get hacked. No one intentionally designs software so that it can later on be hacked! Part of knowing how things can be broken is breaking them yourselves. Even though I'm (probably) not going to get paid to break web apps anytime soon it is SUPER helpful to have a passing knowledge of how people do that. In this class we covered the [OWASP top 10](https://owasp.org/www-project-top-ten/) which is the top 10 most common web vulnerabilities.
## Top 10 Web Application Security Risks
- Injection 
- Broken Authentication
- Sensitive Data Exposure
- XML External Entities (XXE)
- Broken Access Control
- Security Misconfiguration
- Cross-Site Scripting XSS
- Insecure Deserialization
- Using Components with Known Vulnerabilities
- Insufficient Logging & Monitoring

We also played a game of Capture the Flag (CTF) where you attack a server with known vulnerabilities and collect 'flags' to increase your score. That was a fun structure to hold the lessons in mind.

Lastly we needed to learn about a few tools that enable this kind of testing. We covered Zap, nmap, SQLmap, and got a brief overview of [BeEF on Kali linux](https://linuxhint.com/hacking_beef/)

## Final thoughts
I'm definitely not a good hacker, and (I hope) I'm not a terrible software developer. This training mostly helps me understand the benefit of having thoughtful conversations about software vulnerabilities, stressing the importance of buttoning up every last TODO before committing, and also keeping attacks in mind whenever implementing any new features. Even if I don't try my hand at another SQL injection vuln this class will have been worth the time. I'm thankful I was offered the chance to do this at work, and I recommend it to any software engineer.