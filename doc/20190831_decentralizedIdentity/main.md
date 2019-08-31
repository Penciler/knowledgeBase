#Decentralized Identity

There are several problem of current identity system. First, identity data were spread across numerous providers. For example, your identity as a citizen is provided by the government while your bachelor diploma is given by your college. Second, user can’t control what information to disclose. If you need to prove that you are old enough to buy alcohol, one way is to show your ID card. But you also disclose your date of birth and other information. And the worse is security breach. Our identities are stored and managed by large, trusted organization. No matter how much effort is invested in security. Leaking of personal data happens time to time. Because those organization are big target and attacking them is profitable. In the 2017 EQUIFAX security breach (2017/05~06), 143 million Americans’ names, address and social security numbers were stolen. To solve above problems, the concept of decentralized identity were proposed.  

##Solution-Decentralized identity
So, let’s talk about the topic of today: decentralized identity. We’ll go through four key concepts below. And in conclusion we’ll explain how those concepts return the control of identity back to users, realize partial disclosure and achieve privacy and security.  
-Decentralized identifier (DID)  
-Registry  
-Resolver  
-Identity hub  

##Decentralized identifier (DID)  
Decentralized identifier is the index pointing to the DID document (DDO). DDO includes DID (index), public key and a pointer to identity hub. The identity hub is a private repository to store personal information. And users possess a private key that paired with the public key in DDO. So user can provide signature by private key to prove that the identity hub pointed by DDO belongs to him/her.  
![alt text](ref/Figure01.png?raw=true)  
Figure 1. Structure of DDO.

![alt text](ref/Figure02.png?raw=true)  
Figure 2. Structure of DDO in JSON format.  

##Registry  
Traditionally, Registry is in charge of mediating the creation or verification of subject identifiers. (College-graduation certificate…) In today’s topic, Registry is distributed ledgers to store DID and DDO. Such as blockchain.  
![alt text](ref/Figure03.png?raw=true)  
Figure 3. How registry works, details will be explained later.  

##Resolver
Resolver is a software that look up the DDO on registry (blockchain) using DID.  
![alt text](ref/Figure04.png?raw=true)  
Figure 4. Universal resolver use DID to find DDO on blockchain.  

##Identity hub  
We mentioned that identity hub is a private repository which stores personal information. And the personal information is in the form of Verifiable claim (VC). Let’s go back to the example of buying alcohol. Instead of showing your ID card, Pat can send a VC to the clerk to prove his age is over 21. In this case, VC will includes issuer (the government), claim (is older than 21) and proof (an Rsa signature).  
![alt text](ref/Figure05.png?raw=true)  
Figure 5. Prove Pat’s age is over 21. 

![alt text](ref/Figure06.png?raw=true)  
Figure 6. Structure of VC.  

![alt text](ref/Figure07.png?raw=true)  
Figure 7. Structure of VC in JSON format.  

![alt text](ref/Figure08.png?raw=true)  
Figure 8. The roles in buying alcohol example.  

##An example  
Finally, we use the example of Alice apply for college to show how above key concepts work together. In this example, Alice has to prove that her age, high school grade….etc is qualified for the college. Please check out below diagram, the “Alice hub” is Alice’s identity hub.  
![alt text](ref/Figure09.png?raw=true)  
Figure 9. Alice apply for college.  

##Conclusions  
To sum up, there are three advantages in decentralized identity system. First, personal informations (VCs) are stored in identity hubs, no central authority is required. So there is no big target to be attacked. Second, it bundle different DID with different VCs to achieve partial disclosure. Third, DID are managed by users them self, rather than managed by multiple organizations.  
![alt text](ref/Figure10.png?raw=true)  

##References  
[Decentralized Digital Identities and Blockchain](https://www.microsoft.com/en-us/microsoft-365/blog/2018/02/12/decentralized-digital-identities-and-blockchain-the-future-as-we-see-it/)  
[Can Blockchain & Verifiable Claims Eliminate the Next Equifax-Level Breach?](https://www.linkedin.com/pulse/can-blockchain-verifiable-claims-eliminate-next-breach-gary-rowe)  
[Equifax](https://en.wikipedia.org/wiki/Equifax)  
[Sovrin-Protocol-and-Token-White-Paper](https://sovrin.org/wp-content/uploads/2018/03/Sovrin-Protocol-and-Token-White-Paper.pdf)  
[Distributed Digital Identity](http://blogchain.space/entries/blockchain/distributed-digital-identity)  
[Decentralized Identifiers (DIDs) v0.11](https://w3c-ccg.github.io/did-spec/)  
[Verifiable Credentials Data Model 1.0](https://w3c.github.io/vc-data-model/)  
[A Universal Resolver for self-sovereign identifiers](https://medium.com/decentralized-identity/a-universal-resolver-for-self-sovereign-identifiers-48e6b4a5cc3c)  
[Identity Hub Attestation Flows and Components](https://github.com/WebOfTrustInfo/rwot6-santabarbara/blob/master/draft-documents/Identity%20Hub%20Attestation%20Handling.md)  
[A gentle introduction to self-sovereign identity](https://bitsonblocks.net/2017/05/17/gentle-introduction-self-sovereign-identity/)  