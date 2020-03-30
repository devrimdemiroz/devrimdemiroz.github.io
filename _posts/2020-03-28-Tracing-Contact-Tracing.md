---
layout: post
title:  Tracing "Contact Tracing"
category: home
comments_id: 1
---

_Last Update:Sat Mar 28 13:41:22 CET 2020_  
Just documenting covid-19 related contact trace softwares..  


Chasing “Contact Trace” Softwares around the world brought me here as I was not able to find a consolidated listing of what is available. 
I hope it helps others… Please feel free to contribute. 

Product      | Country      | URL          | Opensource
------------ | -------------|--------------|-------------
WHO App|World Health Organization     |[WHO App](https://docs.google.com/document/d/1isNMLpwI2iUY92KPwJHfY7kQnpN3oCuUl6c94J7Qmhs/edit)|[sources](https://github.com/WorldHealthOrganization/app)
tracetogether|Singapore     |[tracetogether](https://www.tracetogether.gov.sg/)|In future
hamagen|Israel     |[hamagen](https://govextra.gov.il/ministry-of-health/hamagen-app/download-en/)|[sources](https://govextra.gov.il/ministry-of-health/hamagen-app/download-en/)
safepaths|USA     |[safepaths](http://safepaths.mit.edu/)|[sources](https://github.com/tripleblindmarket/)
covid-watch|USA     |[covid-watch](https://www.covid-watch.org/collaborate.html)|Unknown
diAry|Italy     |[diAry](https://covid19app.uniurb.it/)|In April
geoHealthApp|Germany     |[geoHealthApp](https://www.geohealthapp.de/)|No
Smart quarantine|Czech     |[Smart quarantine](https://medium.com/@pabu01/covid19cz-update-bb7e12e71d9e)|No
coronapp |Turkey     |[coronapp](https://coronapp.tech/)|No
coronawarner |Turkey     |[coronawarner](https://www.linkedin.com/posts/geodotech_corowarner-hackcorona-coronathontaesrkiye-activity-6648915397267476480-TT4N)|No
Alipay |China     |N/A|No
WeChat |China     |N/A|No
Corona 100m (Co100) |Korea     |N/A|No
N/A |Taiwan     |N/A|No

Scroll down for details

## World Health Organization
### `WHO App`

- <https://www.who.int/mediacentre/multimedia/app/en/>
- **Opensource**: <https://github.com/WorldHealthOrganization/app>
- Contact Tracing is one of the five key goals of app stated in <https://docs.google.com/document/d/1isNMLpwI2iUY92KPwJHfY7kQnpN3oCuUl6c94J7Qmhs/edit>
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
- <https://www.linkedin.com/posts/geodotech_corowarner-hackcorona-coronathontaesrkiye-activity-6648915397267476480-TT4N>
- **Opensource**: NO
***



## China
### `Alipay` 
### `WeChat`
***

## Korea
### `Corona 100m (Co100)` 
***

## Taiwan
### ``
***
[Trends](https://devrimdemiroz.github.io/contactTracing/trends.html)

<div >
    <script type="text/javascript" src="https://ssl.gstatic.com/trends_nrtr/2152_RC02/embed_loader.js"></script> <script type="text/javascript"> trends.embed.renderExploreWidget("TIMESERIES", {"comparisonItem":[{"keyword":"geoHealthApp","geo":"","time":"now 7-d"},{"keyword":"tracetogether","geo":"","time":"now 7-d"},{"keyword":"hamagen","geo":"","time":"now 7-d"},{"keyword":"diAry app","geo":"","time":"now 7-d"},{"keyword":"safepaths","geo":"","time":"now 7-d"}],"category":0,"property":""}, {"exploreQuery":"date=now%207-d&q=geoHealthApp,tracetogether,hamagen,diAry%20app,safepaths","guestPath":"https://trends.google.com:443/trends/embed/"}); </script>
</div>
