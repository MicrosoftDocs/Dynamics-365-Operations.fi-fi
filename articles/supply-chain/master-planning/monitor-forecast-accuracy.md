---
title: Ennusteen tarkkuuden valvonta
description: Tässä artikkelissa kuvataan ennusteen tarkkuuden tyyppejä, joita Microsoft Dynamics 365 for Finance and Operations laskee ja ilmoittaa, miten voit tarkastella näitä tarkkuusarvoja.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7070c15f9ee23cfdba871af68d1fc5954735651
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "356412"
---
# <a name="monitor-forecast-accuracy"></a>Ennusteen tarkkuuden valvonta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan ennusteen tarkkuuden tyyppejä, joita Microsoft Dynamics 365 for Finance and Operations laskee ja ilmoittaa, miten voit tarkastella näitä tarkkuusarvoja.

Finance and Operations laskee seuraavia ennusteen tarkkuuden tyyppejä:

-   Historiallinen ennusteen tarkkuus vertaamalla historiallista ennustetta, jota pääsuunnittelu käyttää historiallisen kysynnän kanssa. Jos haluat tarkastella historiallisen tarkkuuden arvoja (sekä absoluuttisia että prosentuaalisia arvoja), valitse **Näytä tarkkuus** **Kysynnän ennusteen tiedot** -sivulla.
-   Ennustemallin arvioitua tarkkuutta käytetään ennusteiden luonnissa. Voit tarkastella tarkkuusprosenttia kohdassa **Mallin tiedot - MAPE** **Kysynnän ennusteen tiedot** -sivulla. 

**Huomautus:** Jos käytät Finance and Operationsin kysynnän ennusteiden Microsoft Azuren automaattianalyysipalvelua, sisäisen mallin tarkkuuden laskenta perustuu testitietojen joukkoon. Voit määrittää testitietojoukon koon määrittämällä **TEST\_SET\_SIZE\_PERCENT** (Testijoukon koon prosenttiosuus) -parametrin **Kysynnän ennusteen parametrit** -sivulla. Jos esimerkiksi määrität arvoksi **20**, historiallisten tietojen viimeistä 20 prosenttia käytetään sisäisen mallin tarkkuuden laskemiseen.


<a name="additional-resources"></a>Lisäresurssit
--------

[Oikaistun kysynnän ennusteen valtuuttaminen](authorize-adjusted-forecast.md)

[Poista poikkeavat tiedot aiemmista tapahtumatiedoista laskettaessa ennustetarvetta](remove-historical-outliers-calculating-demand-forecast.md)



