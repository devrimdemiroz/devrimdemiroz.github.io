---
layout: post
title:  Tracing "Contact Tracing"
category: home
comments_id: 1
---

_Last Update: Sat April 2 20:00:00 CET 2020_  
Just documenting COVID-19 related contact trace softwares..  


Chasing “Contact Trace” Softwares around the world brought me here as I was not able to find a consolidated listing of what is available. 
I hope it helps others… Please feel free to contribute. 

Product      | Country      | URL          | Opensource
------------ | -------------|--------------|-------------
WHO App|World Health Organization     |[WHO App](https://docs.google.com/document/d/1isNMLpwI2iUY92KPwJHfY7kQnpN3oCuUl6c94J7Qmhs/edit)|[sources](https://github.com/WorldHealthOrganization/app)
tracetogether|Singapore     |[tracetogether](https://www.tracetogether.gov.sg/)|In future
hamagen|Israel     |[hamagen](https://govextra.gov.il/ministry-of-health/hamagen-app/download-en/)|[sources](https://govextra.gov.il/ministry-of-health/hamagen-app/download-en/)
COVID360|Israel     |<a href="https://youtu.be/z84MfjI1Dp0" target="_blank">COVID360</a>|No
safepaths|USA     |[safepaths](http://safepaths.mit.edu/)|[sources](https://github.com/tripleblindmarket/)
covid-watch|USA     |[covid-watch](https://www.covid-watch.org/collaborate.html)|Unknown
diAry|Italy     |[diAry](https://covid19app.uniurb.it/)|In April
geoHealthApp|Germany     |[geoHealthApp](https://www.geohealthapp.de/)|No
Smart quarantine|Czech     |[Smart quarantine](https://medium.com/@pabu01/covid19cz-update-bb7e12e71d9e)|No
coronapp |Turkey     |[coronapp](https://coronapp.tech/)|No
coronawarner |Turkey     |[coronawarner](https://www.linkedin.com/posts/geodotech_corowarner-hackcorona-coronathontaesrkiye-activity-6648915397267476480-TT4N)|No
N/A |Russia     |<a href="https://www.bbc.com/news/technology-52121264" target="_blank">BBC news</a>|No
Alipay |China     |N/A|No
WeChat |China     |<a href="https://www.wechat.com/en/" target="_blank">wechat</a> |No
Corona 100m (Co100) |Korea     |N/A|No
N/A |Taiwan     |N/A|No
CoviID |South Africa     |<a href="https://coviid.me/" target="_blank">CoviID</a>|No


Details ahead

## World Health Organization
### `WHO App`

- <a href="https://www.who.int/mediacentre/multimedia/app/en/" target="_blank">https://www.who.int/mediacentre/multimedia/app/en/</a>
- **Opensource**: <a href="https://github.com/WorldHealthOrganization/app" target="_blank">https://github.com/WorldHealthOrganization/app</a>
- Contact Tracing is one of the five key goals of app stated in 
<a href="https://docs.google.com/document/d/1isNMLpwI2iUY92KPwJHfY7kQnpN3oCuUl6c94J7Qmhs/edit?usp=sharing" target="_blank">WHO COVID-19 App For Location Based Containment, Triage & Response</a>
- Same infrastructure addressed in safepaths app. "The plan is to leverage the PrivateKit technology from MIT."

***


## Singapore
### `tracetogether`

- <https://www.tracetogether.gov.sg/>
- **Opensource**: Announced to be opensource but when? Related news: <https://str.sg/Jfup>
- Almost the most pouplar, 735K users
- Bluetooth based, no location information collected. As stated in their official site “The app doesn't identify “where” the exposure to COVID-19 cases may have occurred. It only seeks to establish “who” else might have been exposed to the virus.”
- A technical look: <https://medium.com/@meshead/tracetogether-a-technical-look-e48360d4a4a9>
- Under-the-hood: <https://medium.com/@frankvolkel/tracetogether-under-the-hood-7d5e509aeb5d>
***

## Israel 
### `Hamagen (The Shield)`

- <https://govextra.gov.il/ministry-of-health/hamagen-app/download-en/>
- **Opensource**: https://github.com/MohGovIL/hamagen-react-native
- Israel's Ministry of Health's COVID-19 Exposure Prevention App 
- **Architecture**: <https://proferopublic.s3-eu-west-1.amazonaws.com/5f72cff6-0fb5-4517-9941-99331819b5a0/profero_infographic_01_en.jpg>
- React-native based Android and IOS clients , .ts typescript mostly
- Location and wifi based
***  

### `COVID360`
- "_The full Corona treatment solution for patients and citizens at risk. 
COVID360 built by Deloitte Israel, based on Salesforce Health-Cloud, and “Diagnostics Robotics” 
AI triage and clinical predictions platform._"  from link:
<a href="https://youtu.be/z84MfjI1Dp0" target="_blank">COVID360 - End to end centralized solution for Corona treatment</a>
- **Opensource**: NO
- Apart from general solutions outlined here within, this one brings backend server side into picture. 
- Contact trace is not the main focus for COVID360 yet as an important feature of solution.

## USA
### `safepaths`

- <http://safepaths.mit.edu/> 
- **Opensource**: <https://github.com/tripleblindmarket/>
- Based on Private Kit by MIT, core code is ready but still in early stages
- React-native based Android and IOS clients, .js javascript mostly
- Location and bluetooth based

### `covid-watch`

- <https://www.covid-watch.org/collaborate.html>
- Notihng developed so far, in organization/establishment phase
***



## Italy 
### `diAry`

- <https://covid19app.uniurb.it/>
- **Opensource**: Announced to be opensource by April'20
- Additional feature worth to mention is reward system
***


## Germany 
### `geoHealthApp`
- <https://www.geohealthapp.de/>
- **Opensource**: NO
***


## Czech
### `Smart quarantine`
- <https://medium.com/@pabu01/covid19cz-update-bb7e12e71d9e>
- **Opensource**: NO
- Based on Telco data
***

## Turkey
### `coronapp`
- <https://coronapp.tech/>
- **Opensource**: NO

### `corowarner`
- <a href="https://www.linkedin.com/posts/geodotech_corowarner-hackcorona-coronathontaesrkiye-activity-6648915397267476480-TT4N" target="_blank">geodotech_corowarner-hackcorona-coronathontaesrkiye-activit</a>
- **Opensource**: NO
- More information(In Turkish) on youtube <a href="https://youtu.be/KwuWcTp2ZnQ" target="_blank">CoroWarner telefon uygulaması koronavirüs salgınının Türkiye'deki yayılım hızını düşürmeyi amaçlıyor</a> 
  
***

## Russia
### ``
- Related news: <a href="https://www.bbc.com/news/technology-52121264" target="_blank">Coronavirus: Moscow rolls out 
patient-tracking app</a>
- Application details(In russian, use a translator on browser) 
<a href="https://echo.msk.ru/programs/razvorot-morning/2616757-echo/" target="_blank">About the application for 
monitoring quarantined Muscovites</a>

***

## China
- "_Alibaba and Tencent are working with local governments. They have created health QR codes. 
Users get different colors depending on travel history and health. 
The agreement over health code 'passports' between localities underscores China's urgency in getting people back to work._".
 You might want to have a quick look at short video <a href="https://youtu.be/Sp-TaoPdrWo" target="_blank">Chinese cities cooperating on health code systems</a>.
   
- Contact tracing features provided inside Alipay and WeChat applications is not just informing people, but as well acts as clarance by color. 
Three colors. Red, yellow, green. Only Green can drive, tracel or even get into a market.
- **Opensource**: NO
### `Alipay` 
### `WeChat`
- <a href="https://www.wechat.com/en/" target="_blank">https://www.wechat.com/en/</a> by Tencent

***

## Korea
### `Corona 100m (Co100)` 
***

## Taiwan
### TBD
***

## South Africa
### CoviID
- <a href="https://coviid.me/" target="_blank">https://coviid.me/</a>
- <a href="https://www.news.uct.ac.za/news/research-office/-article/2020-03-27-coviid-new-app-to-avoid-future-lockdowns"
 target="_blank">CoviID: new app to avoid future lockdowns</a>

[Trends](https://devrimdemiroz.github.io/contactTracing/trends.html)

<div >
    <script type="text/javascript" src="https://ssl.gstatic.com/trends_nrtr/2152_RC02/embed_loader.js"></script> <script type="text/javascript"> trends.embed.renderExploreWidget("TIMESERIES", {"comparisonItem":[{"keyword":"geoHealthApp","geo":"","time":"now 7-d"},{"keyword":"tracetogether","geo":"","time":"now 7-d"},{"keyword":"hamagen","geo":"","time":"now 7-d"},{"keyword":"diAry app","geo":"","time":"now 7-d"},{"keyword":"safepaths","geo":"","time":"now 7-d"}],"category":0,"property":""}, {"exploreQuery":"date=now%207-d&q=geoHealthApp,tracetogether,hamagen,diAry%20app,safepaths","guestPath":"https://trends.google.com:443/trends/embed/"}); </script>
</div>
