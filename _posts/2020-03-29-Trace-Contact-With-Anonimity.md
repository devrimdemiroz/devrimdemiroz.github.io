---
layout: post
title:  "Contact Trace Identity Angle"
comments_id: 2
---


Approximately a week ago, decided to be a part of a solution about covid-19.
After chasing myself to a practical fit, attached to "Contact Trace" Softwares. 
Did a preliminary current analysis, can be found in  <a href="{% post_url 2020-03-28-Tracing-Contact-Tracing %}" target="_blank"> this </a>  post. 

However, ended up chasing usual "Identity Crisis" as an Identity and Access Management specialist in very same context.  

Please consider this article as a "draft log". Currently just stuffing with possibilities yet with intention to refine later.

Eventhough many of the listed products listed in post 
<a href="{% post_url 2020-03-28-Tracing-Contact-Tracing %}" target="_blank"> Tracing "Contact Tracing"  </a>  claims to  
comply with GDPR or equivalent, respecting user's anonymity etc. , still there are a number of open points regarding 
Identity as a concept itself.  

Not only bounded with privacy issues, while ensuring end to end coverage in terms of 
"Verifiable Sovereign Identity", also respect human values, evaluate future, be fast , be efficient , think practical ...

The need for a Global Identity coupled with COVID-19 credentials is crucial to return to our "new normal" lives. 
Just to state an example, after pandemic gets controlled, suppose I would like travel to a country. Now my medical 
COVID-19 history is a part of my VISA. May be not only for the country I am going, as well for the airlines I have choose. 
Moreover,  when I arrive there , foreign country authorities might want to keep track me as risk factor. And so on...  
You may find well defined use cases  in "<a href="https://github.com/disposableidentities/healthcrisis/blob/master/usecases.md"
 target="_blank">5 use-cases of Health Status Sharing for Social Recovery with HygienGap</a> ".

Any case, in terms of global economic and social recovery , today we are desperately in need see some light from the end of the tunnel. 

**What do we have in hand?** 

#### Current Identity Implementations in Contact Trace Software's

Not all apps listed in <a href="{% post_url 2020-03-28-Tracing-Contact-Tracing %}" target="_blank"> this post </a> has been published to market yet.

- **WHO** app is not featuring contact trace yet and when you install the application you just see a mobile version of their official web page.

***

- **tracetogether** application requires an OTP authentication send to a number starting with +65 XXXXXXXXX , 
which initially means the main/central "verifiable identity" link is established using telco infrastructure. 
The collected bluetooth identities around that particular device is the "temporary ID" created on device. 
The "temporary ID" exchanged between devices is linked to telephone numbers are stored centrally and can only be accessed by authorities.  
One leaking point in terms of coverage lies here within. Suppose you are a tourist trapped in Singapore with your SIM card from your home country.
You would not be able to participate the system meanwhile system will not able to aware of your disease. 
Situation links to a "Sovereign Identity" need for coverage.

***

#### Verifiable credentials (VCs)

You might want to check <a href="https://www.wikiwand.com/en/Verifiable_credentials" target="_blank">Verifiable credentials</a> 
on wikipedia before going further. From their definition:  
 
"_**Verifiable credentials (VCs)** are the electronic equivalent of the physical credentials that we all possess today, 
such as: plastic cards, passports, driving licences, qualifications and awards, etc._"
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/51/VC_triangle_of_Trust.svg/640px-VC_triangle_of_Trust.svg.png?1585827350750" 
alt="Verifiable credentials" 
class="responsiveImage" >

Having said so, Disposable Identities mentioned in 
<a href="https://github.com/disposableidentities/healthcrisis" target="_blank">Disposable Identities for Health Crisis</a>
is quite interesting as well. Still trying to figure out the intersection set and discrete sides. 

### Blockchain Footprints
`sovrin`  
- Foresight of following article is [Responding to the COVID-19 Challenge with Verifiable Credentials](https://www.evernym.com/covid19-creds/)  
is very valuable.
- Self-sovereign Identity

***

`Aries-DID`
- <a href="https://github.com/OpenMined/Aries-DiD" target="_blank">https://github.com/OpenMined/Aries-DiD</a>
- From the link above , "_We'd like users to be able to prove they are eligible for COVID screening 
without the service provider knowing the identity of the user. 
We can do this using DID documents, Verifiable Credentials (VCs) and some distributed identity concepts._"
- Has a very simple and clear diagram how identity and clinical data should be handled in COVID-19 context. 
<img src="https://raw.githubusercontent.com/OpenMined/Aries-DID/demo-finish/images/step0.png" alt="Building a Credential Eco-System for Anonymous Verification " class="responsiveImage" >

***

`uport`
- Self-sovereign Identity

***

`ShoCard`
- ShoCard has been acquired by Ping Identity.
- Decentralised Trusted Identity

***

`OneName`
- Self-sovereign Identity


***
### Non-Blockchain 

`IRMA`

 
 ***
 
### References
 
- <a href="https://arxiv.org/pdf/1801.03294.pdf" target="_blank">A First Look at Identity Management Schemes on the Blockchain</a>
 by Paul Dunphy and Fabien A. P. Petitcolas
- 