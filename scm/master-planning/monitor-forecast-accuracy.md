---
title: "Näytön tarkkuus ennuste"
description: "Tässä artikkelissa kuvataan Microsoft Dynamics-365 työvaiheiden laskee ja kerrotaan, kuinka voit tarkastella tarkkuus arvot ennusteen tarkkuus tyypit."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>Näytön tarkkuus ennuste

Tässä artikkelissa kuvataan Microsoft Dynamics-365 työvaiheiden laskee ja kerrotaan, kuinka voit tarkastella tarkkuus arvot ennusteen tarkkuus tyypit.

Työvaiheiden 365 Dynamics laskee ennusteen tarkkuus seuraavanlaisia:

-   Historiallinen ennusteen tarkkuus vertaamalla historiallista ennustetta, jota pääsuunnittelu käyttää historiallisen kysynnän kanssa. Jos haluat tarkastella historiallisen tarkkuuden arvoja (sekä absoluuttisia että prosentuaalisia arvoja), valitse **Näytä tarkkuus****Kysynnän ennusteen tiedot** -sivulla.
-   Ennustemallin arvioitua tarkkuutta käytetään ennusteiden luonnissa. Voit tarkastella tarkkuusprosenttia kohdassa **Mallin tiedot - MAPE** **Kysynnän ennusteen tiedot** -sivulla. 

**Huomautus:** Jos toimia kysynnän ennusteet Microsoftin Azure Machine Learning-palvelu käyttää Dynamics 365, sisäisen mallin tarkkuutta laskenta perustuu testi tietojoukon. Tietojoukon testin kokoa, aseta **TESTATA\_MÄÄRITTÄÄ\_kokoa\_PROSENTTIA** -parametrin **kysynnän ennusteet parametrit** sivun. Jos esimerkiksi määrität arvoksi **20**, historiallisten tietojen viimeistä 20 prosenttia käytetään sisäisen mallin tarkkuuden laskemiseen.


<a name="see-also"></a>Lisätietoja
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


