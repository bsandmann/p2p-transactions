# Progress report

## 2022-03-30 Research and POC Planing
After a few days of CA-work, the research continued: step by step, it goes deeper into the SSI matter and new ideas are emerging. Primary focus is to dig into DID specifications and to think through possible workflows for different trust models.

Along the way, the technical design for a POC is starting. The approach is currently to provide several generic modules as a microservice: For DID-based authentication, for creating, tracing and verifying them. Above all, there is always the question of complexity in the architecture conception. How does one want to build such a system? How small-scale do you want to be with the microservices, or is a system that consists of perhaps only two or three components and is tightly coupled sufficient for a POC?

## 2022-03-17 Research & notes on the whitepaper
After the completion of the PRISM Pioneers program a few months have gone by, so I started working through some of the already visited material to get a better understanding of a few technical details. The new version (1.3.1-SP1) was integrated and some experiments completed. There are still a lot of open questions regarding the release version of the SDK and the node itself. Especially around the business model of IOG.

In addition to the technical experiments the research around trust-models, SSI and possible cryptographic solutions to the trust problem is ongoing. This will likely continue for the next weeks: mainly studying the *W3C* specifications in detail and reading *Self-Sovereign Identity* by *Alex Preukschat* and *Drummond Reed*. Meanwhile I’m taking a lot of notes which I’ll compile to a draft of the whitepaper.

A first result of the research phase is a new proposal for *Fund 8: Self-Souvereign identity* which can be found [here]( https://cardano.ideascale.com/c/idea/404879). The proposal has an overlapping with the ongoing proposal, but only regarding theoretical aspects – not technical ones. It is about the trust-building phase before a transaction even happens. In the proposal we try to find a better way to do endorsement on the web. Have a look at the proposal or visit [blocktrust.dev](http://blocktrust.dev). 

The project is schedueld to be finished until 2022-09-30 (End of September 2022)

## 2022-03-03 Received funding
The initial batch of funding was received, and the work will begin next week with the research phase.
