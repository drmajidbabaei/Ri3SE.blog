---
layout: post
title: "Increasing the Dependability of Internet-of-Things Systems in the context of End-User Development Environments"
categories: [research, engineering, software, iot]
tags: [research, phd, engineering, software, iot]
thumbnail: /images/phd/phd.png
description: "Abstract of my PhD thesis in Informatics Engineering."
---

Today, 1 April of 2022, I have successfully defended my [PhD thesis](https://hdl.handle.net/10216/140853) work on Software Engineering and Internet-of-Things entitled "Increasing the Dependability of Internet-of-Things Systems in the context of End-User Development Environments". Here follows the abstract.

<!--more-->

## Abstract

The ubiquitousness of computing, known as Internet-of-Things (IoT), has reshaped the way people interact with the physical world. However, the scale, distribution --- both logical and geographical ---, density, heterogeneity, interdependence, and {quality-of-service} requirements of these systems make them complex, posing several challenges from both operational and development viewpoints.

While there is a consensus that the widely used software engineering practices are inadequate for IoT development, they remain the go-to solutions for most practitioners. This aspect has severely compromised their dependability, centralizing most of the computation of these (soft) real-time systems in cloud infrastructure. Likewise, as these systems scale in terms of devices and applications, it outreaches existing technical resources to manage and operate them, becoming of paramount importance, making them as most self-managed as possible while empowering the ability of system operators (including end-users) to configure and understand them --- mainly using solutions that do not require high technical expertise, _viz_ low-code development solutions --- including the configuration of fail-safe measures.

This dissertation's primary focus is to research how to improve the current status quo on the dependability of IoT. However, this is a manifold endeavor: (1) what are the best practices for developing IoT dependably, and what is their scientific soundness, (2) do the current solutions give the fundamental building blocks that allow to design and construct dependable systems, and, if not, what contributions are needed to overcome the existing limitations, and, lastly, (3) giving that these systems are operated by humans with limited technical expertise, it is required that their users can use and configure them without compromising their correct operation. As we set ourselves to tackle these challenges, we claim that:

> It is possible to enrich IoT-focused end-user development environments in such a way that the resulting systems have a higher dependability degree, with the lowest impact on the know-how of the (end-)users.

As preliminary research, to understand what end-users want to automate and how they wish to perform such automations, a study was carried to collect automation scenarios. These scenarios showcased the complexity of the automations that some end-users want to perform and the interdependencies between different information sources, devices, and persons. It also supported the view that some of the appliances that end-users want to automate can have nefarious effects if a malfunction happens or a misconfiguration is performed.

We followed extensive literature research and experimental process to _mine_ a set of patterns that can be used to improve IoT systems by making them more dependable, documenting them as _patlets_, which summarily describe solutions that address some particular problem within a specific context. We further studied a subset of these patterns as a _self-healing_ pattern language that contemplates the use of more than one pattern in tandem to address systems' operational concerns autonomically.

Adopting these patterns depends on supporting foundations, which include architectural and functional aspects of the target systems. A key aspect is that most of the current solutions do not provide any features to readjust their intrinsic behaviors during runtime --- with the software that runs on edge devices being mostly set on stone, delegating all the computational needs to cloud-based services. The research on fog and edge computing attempt to mitigate this by leveraging computational resources across architectural tiers, making the resulting systems more dependable and improving their scalability. Taking on these foundations, we explored and asserted the feasibility of using serverless functions in the IoT context, optimizing the choice of execution contexts according to a priori preferences, constraints, and latencies.

To understand how these paradigms can be leveraged in widely used solutions, we select the open-source Node-RED solution as the experimental base, given its popularity. It provides a visual programming interface that increases its target user base across different expertise levels. Like other available solutions, Node-RED does not provide any feature that allows it to orchestrate tasks across devices or deal with system parts' failures, limiting the dependability of systems built with it. Nonetheless, given its open-source and extensible nature, we proceed to address some of its limitations. We proceed to evaluate empirically, both in virtual and physical setups, the feasibility of using Node-RED as an orchestrator, where computational tasks are allocated to the available resources, and failures are mitigated by re-orchestrating as devices fail and recover. We also implemented a set of extensions for Node-RED that allows one to enrich the existing programs (_i.e._, flows) with self-healing capabilities --- allowing the detection errors of different parts during runtime, and readjust its behavior to keep delivering correct service by recovering to normal operation, or, at least, maintain its operation within acceptable Quality-of-Service levels.

As IoT users have different expertise levels, we also attempt to improve the interaction with these systems in a way that the users can understand what the configured automations are (_viz_ inspection), how it is behaving (_viz_ observability and feedback), and increase their capability to know what was the possible cause behind certain events (_viz_ causality). In the first study, we extended the visual notations and functionalities of Node-RED to improve the development process using it. We proceed to empirically evaluate the performance of our solution against a non-modified version of Node-RED, observing statistically significant improvements in the users' ability to evolve existing IoT deploys. Lastly, we explored the use of voice assistants as an alternative way of configuring, understanding, and interacting with IoT-enriched environments, with a particular focus on the ability of a user to understand the cause behind some events. We assert the feasibility of our solution by covering all the different automation possibilities that Node-RED supports, with a considerable extension of the interaction possibilities due to multi-message dialogs support. We proceeded to empirically validate the feasibility of users using the voice assistant to complete different tasks, and all the users were able to finish the tasks. While some valid sentences were incorrectly recognized, forcing the user to repeat their intent, participants expressed a preference for voice interfaces over visual ones in terms of subjective perception.

These contributions materialize into a core set of building blocks that, in assemble, can be used to improve the dependability of IoT systems while leveraging abstractions that do not hinder the (end-)user capability to configure, use, and evolve them. The experimental counterparts of the contributions provide empirical supporting evidence for the plausibility of the hypothesis.

## Presentation

<script async class="speakerdeck-embed" data-id="18b538f15d3d4213981406270b2662ab" data-ratio="1.77966101694915" src="//speakerdeck.com/assets/embed.js"></script>

### References

- Open Repository: [https://hdl.handle.net/10216/140853](https://hdl.handle.net/10216/140853)
- PDF File: [https://repositorio-aberto.up.pt/bitstream/10216/140853/2/553182.pdf](https://repositorio-aberto.up.pt/bitstream/10216/140853/2/553182.pdf)
- Bibtex: [phdthesis.bib](/assets/bibtex/phdthesis.bib)
