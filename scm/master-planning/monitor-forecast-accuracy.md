---
title: Ennusteen tarkkuuden valvonta
description: "Tässä artikkelissa kuvataan ennusteen tarkkuuden tyyppejä, joita Microsoft Dynamics 365 for Operations laskee ja kertoo, miten voit tarkastella näitä tarkkuusarvoja."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 580b45263b45e6ef730b0fac32575fcdd9c358b6
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="monitor-forecast-accuracy"></a>Ennusteen tarkkuuden valvonta

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan ennusteen tarkkuuden tyyppejä, joita Microsoft Dynamics 365 for Operations laskee ja kertoo, miten voit tarkastella näitä tarkkuusarvoja.

Dynamics 365 for Operations laskee seuraavia ennusteen tarkkuuden tyyppejä:

-   Historiallinen ennusteen tarkkuus vertaamalla historiallista ennustetta, jota pääsuunnittelu käyttää historiallisen kysynnän kanssa. Jos haluat tarkastella historiallisen tarkkuuden arvoja (sekä absoluuttisia että prosentuaalisia arvoja), valitse **Näytä tarkkuus****Kysynnän ennusteen tiedot** -sivulla.
-   Ennustemallin arvioitua tarkkuutta käytetään ennusteiden luonnissa. Voit tarkastella tarkkuusprosenttia kohdassa **Mallin tiedot - MAPE** **Kysynnän ennusteen tiedot** -sivulla. 

**Huomautus:** Jos käytät Dynamics 365 for Operationsin kysynnän ennustamisen Microsoft Azuren automaattianalyysipalvelua, sisäisen mallin tarkkuuden laskenta perustuu testitietojen joukkoon. Voit määrittää testitietojoukon koon määrittämällä **TEST\_SET\_SIZE\_PERCENT** (Testijoukon koon prosenttiosuus) -parametrin **Kysynnän ennusteen parametrit** -sivulla. Jos esimerkiksi määrität arvoksi **20**, historiallisten tietojen viimeistä 20 prosenttia käytetään sisäisen mallin tarkkuuden laskemiseen.


<a name="see-also"></a>Lisätietoja
--------

[Oikaistun kysynnän ennusteen valtuuttaminen](authorize-adjusted-forecast.md)

[Poista poikkeavat tiedot aiemmista tapahtumatiedoista laskettaessa ennustetarvetta](remove-historical-outliers-calculating-demand-forecast.md)




