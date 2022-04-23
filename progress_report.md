# Progress report

## 2022-04-23 Continued POC and questions regarding the SDK
In addition to the continued immersion in SSI specific topics, the POC was the central topic of the last weeks. The white paper was postponed somewhat in favor of practical experience with the SDK. In the course of this, various problems in the architecture of the SDK were revealed: For example, the SDK always assumes that the private keys are known within the SDK. Signing credentials via a browser wallet is not natively supported. To implement such capabilities, new functions had to be written, which required some code duplication. In other places, too, one gets the impression that the SDK was written only for an Atala-specific application purpose and not from a perspective that is open to alternative application use cases.

As far as the release of the SDK is concerned, there is still some uncertainty: It has not yet been communicated to what extent the node will be released, who will be allowed to run the node, how the accounting-model on the node will work, if there will be node-as-service operators, etc. The questions primarily concern the business model of Atala PRISM and less the implementation of the proposal. Nevertheless, they are critical to the way forward and the underlying structure of the implementation of the proposal. At the heart of this is the question: who will pay for the costs of issuing credentials and how can they be paid? Regardless of the costs themselves (and their amount), this has architectural implications and questions the philosophy behind P2P transactions: In addition to the transactions for issuing a transaction token, does there need to be a transaction for payment? One is a transaction against the PRISM node, the other is a transaction against the Cardano blockchain. How would an integrated wallet look like to consolidate this whole process into one user action in a user-friendly way? Or does one use a centralized service where there is a settlement account? The most convenient solution from the user's point of view, but not necessarily in the spirit of the very idea of creating a decentralized solution. Unfortunately, all these questions cannot be answered yet, because IOG does not release any information about this at the moment.

In a conversation with Tony Rose (product manager for PRSIM) I was able to raise these points personally. The result was also only that the business model on the part of IOG is not yet definitely determined. Regardless of the unclear strategy regarding the SDK, the support on the part of PRISM is very good.
Besides these developments, there were two weeks of Easter vacation for me, so that work will resume regularly at the end of April. 

## 2022-03-30 Research and POC Planing
After a few days of CA-work, the research continued: step by step, it goes deeper into the SSI material and new ideas are emerging. Primary focus is to dig into DID specifications and to think through possible workflows for different trust models.

Along the way, the technical design for a POC is starting. The approach is currently to provide several generic modules as a microservice: For DID-based authentication, for creating, tracing and verifying them. Above all, there is always the question of complexity in the architecture conception. How does one want to build such a system? How small-scale do you want to be with the microservices, or is a system that consists of perhaps only two or three components and is tightly coupled sufficient for a POC?

## 2022-03-17 Research & notes on the whitepaper
After the completion of the PRISM Pioneers program a few months have gone by, so I started working through some of the already visited material to get a better understanding of a few technical details. The new version (1.3.1-SP1) was integrated and some experiments completed. There are still a lot of open questions regarding the release version of the SDK and the node itself. Especially around the business model of IOG.

In addition to the technical experiments the research around trust-models, SSI and possible cryptographic solutions to the trust problem is ongoing. This will likely continue for the next weeks: mainly studying the *W3C* specifications in detail and reading *Self-Sovereign Identity* by *Alex Preukschat* and *Drummond Reed*. Meanwhile I’m taking a lot of notes which I’ll compile to a draft of the whitepaper.

A first result of the research phase is a new proposal for *Fund 8: Self-Souvereign identity* which can be found [here]( https://cardano.ideascale.com/c/idea/404879). The proposal has an overlapping with the ongoing proposal, but only regarding theoretical aspects – not technical ones. It is about the trust-building phase before a transaction even happens. In the proposal we try to find a better way to do endorsement on the web. Have a look at the proposal or visit [blocktrust.dev](http://blocktrust.dev). 

The project is schedueld to be finished until 2022-09-30 (End of September 2022)

## 2022-03-03 Received funding
The initial batch of funding was received, and the work will begin next week with the research phase.
