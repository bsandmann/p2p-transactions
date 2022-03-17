# p2p-transactions
## A Cardano-Catalyst projekt to build a library to enable trustful and private P2P market transaction by Atala PRISM DIDs.

This page provides essential information about the project process of the project funded by Cardano-Catalyst.
All development of the white paper and code base is happening publicly on this site.

Feel free to contact me:
Björn Sandmann

sandmann@codedata.solutions
or via Catalyst @bsandmann

# Progress-report
The progress-report can be found [here](progress_report.md)



# Project description 

In existing centralized marketplace solutions (amazon, eBay, ...) the platform providers take the role of all-powerful gatekeepers. This centralized authority can remove certain products due to "moral concerns", block users or vendors or highlight their own products and make competing vendors difficult to reach. In some cases, they can also intervene in the trust-building process itself: Inappropriate reviews are removed on a whim, bad reviews are hidden or are cumbersome to submit or find. Trust relationships built up over a long period of time are always dependent on the goodwill of the platform operator and ultimately also on the lifetime of the technical platform itself.

For many types of transactions, however, there is no central platform with a reliable rating system in the first place and one is at the mercy of one's gut feeling. Even in industrialized countries, this applies not only to transactions in moral gray areas, but to most transactions between two parties who are selling something privately and are not primarily acting as traders. If we go to third world countries, these transactions make up the majority of all transactions and the possibilities to assess the degree of trust of the counterpart are often reduced to knowledge of human nature and hearsay.

Therefore, there are a number of reasons to look for alternative solutions, one of which is presented here in the form of a platform and payment service provider independent decentralized Peer-To-Peer (P2P) solution. This technical solution enables trust-based trading of goods and services between parties based on a history of "certificates of trust" using Atala PRISM. By means of an app (with integrated wallet), two parties can prove their trustworthiness to each other and thus come to a trade agreement. The establishment of trust is completely independent of the marketplace (where the offer is presented) and the method of payment (cash, EC, Ada, ...) and can therefore be used anywhere. 

*Concept*

Instead of "certificates", credentials of trust are issued by both parties upon successful transactions. In the following, these credentials will be referred to as "Trust Tokens" to move away from the PRISM/SSI terminology (but technically this is identical). For example: a seller issues a "Trust Token" to the buyer. This "Trust Token" certifies to the buyer, the successful payment. At the same time, the seller receives a "Trust Token" for the successful delivery of a good or service.

The seller-buyer relationship represents the simplest conceivable case. Other scenarios are, for example, the request for services (requester-fulfiller) and the interchange of goods without payment. The procedure is essentially the same and independent of the traded goods/services or the payment for them.

Using PRISM/SSI terminology, each of the two participants in a transaction is always both an "issuer" and a "holder". In the ideal case (happy path), each participant certifies the other to be a good transaction partner. The third party in the trust triangle, the "verifier", using this terminology, represents e.g. another potential buyer who asks the seller to show "trust tokens" of past transactions. If the seller can show enough tokens, the seller can be considered trustworthy. At the same time, a seller can also ask the buyer to show trust tokens from past transactions to ensure that the payment will be made.

Over a certain period, this creates a history of verifiably successful transactions for all participants, which creates trust and gradually enables transactions with higher volumes. A network of trust is created. The proposed model becomes interesting in the presence of fraudsters, suppliers of inferior goods, non-paying customers or transaction participants who do not issue mutual trust tokens.

*Fraud*

The decentralized system proposed here lacks a central authority to turn to when transactions do not produce the desired result for one or both participants. To replace this central authority, it requires an extension of the presented concept:

First, the trust tokens mentioned above are extended by a textual description and issued in three (possibly more) tiers: 1 - Successful transaction "Good customer" / "Good seller". 2 - Successful transaction with restrictions "Poor payment record" , "Goods with defective..." 3 - Unsuccessful transaction: fraud. The issuance of a certificate from the Issuer to the Holder cannot be prevented in Atala PRISM. Consequently, a Seller can be issued a "Trust Token" of the "Fraud" type to a Buyer in case of non-payment of a delivered good. However, this alone is not enough, because the recipient (Holder) of these bad tokens can simply ignore it and does not have to show it to new potential sellers (whom he also wants to defraud). He would just always show the "good" Trust Token.

The problem can be solved by issuing a start-of-transaction token for both the seller and the buyer to a central location before each trade. This token contains no information other than the Id of the participant in the transaction. The central entity is thus a holder of all start-of-transaction tokens, but does not issue any certificates/tokens itself and can be used by all parties as a target of a verification process.

In the case of the above fraudster, who has now collected e.g. 3 "good" "trust tokens" and 10 "bad" ones (which he would like to ignore) there would thus be 13 start-of-transaction tokens in the central registry. Before starting a new trade with this fraudster, a potential buyer (verifier) can compare the number of transactions recorded in the registry with the presented tokens. However, if this person deliberately shows only his 3 "good" tokens, there is an obvious mismatch here and the participant is not transparent/not trustworthy.

*Bad ratings and collateral*

In the previous example it was assumed that the good or bad rating is justified. I.e. in case of objectively good delivery of goods or complete receipt of money a good rating was given and in case of missing delivery or insufficient quality a bad rating was given. An additional extension of the concept becomes necessary if the issuance of a "Trust Token" does not take place or is deliberately done with a negative evaluation, although the delivery of goods objectively complied with the terms of the agreement. In these and other cases, it may be necessary to involve a neutral third party to look at and judge the circumstance at hand. In a decentralized system, this may be randomly selected participants of the same transaction platform who decide on the case based on the facts presented by the disagreeing parties. Collateral deposited by both parties prior to the start of the transaction can ensure that both compensation can be given and the independent third parties are paid for their efforts. In this case, similar to a court case, the losing party has to bear the costs. There are already a number of game-theoretically well thought-out (in some cases multi-level) models for this, which an implementation could be based on.

*Privacy*

The central point of Atala PRISM's considerations is not only to create trust, but above all not to reveal too much information to interested parties.Before a transcation, the primary concern is to ensure that the counterpart is reliable and has already handled a certain number of transactions satisfactorily. Details about previous customers and their purchases should remain hidden. In the presented system, no data from previous transactions is disclosed to third parties. Only the number of transactions is transparent. The proposed platform also does not specify the payment method: whether payments are made in cash or ADA is irrelevant to the trust relationship.

Similarly, the way in which the parties come together for the purchase is basically independent of the trust relationship. Consequently, making the offer, making the payment, and building trust are three distinct aspects: The focus of this proposal is on implementing the latter, as it is the main innovation.
