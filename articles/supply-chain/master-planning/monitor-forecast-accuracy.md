---
title: Ennusteen tarkkuuden valvonta
description: Tässä artikkelissa kuvataan ennusteen tarkkuuden tyyppejä, joita Dynamics 365 Supply Chain Management laskee ja ilmoittaa, miten voit tarkastella näitä tarkkuusarvoja.
author: t-benebo
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76248d87533fd233b255060aa278c76e13719700
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740736"
---
# <a name="monitor-forecast-accuracy"></a>Ennusteen tarkkuuden valvonta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan ennusteen tarkkuuden tyyppejä, joita Microsoft Dynamics 365 Supply Chain Management laskee ja ilmoittaa, miten voit tarkastella näitä tarkkuusarvoja.

Supply Chain Management laskee seuraavia ennusteen tarkkuuden tyyppejä:

-   Historiallinen ennusteen tarkkuus vertaamalla historiallista ennustetta, jota pääsuunnittelu käyttää historiallisen kysynnän kanssa. Jos haluat tarkastella historiallisen tarkkuuden arvoja (sekä absoluuttisia että prosentuaalisia arvoja), valitse **Näytä tarkkuus** **Kysynnän ennusteen tiedot** -sivulla.
-   Ennustemallin arvioitua tarkkuutta käytetään ennusteiden luonnissa. Voit tarkastella tarkkuusprosenttia kohdassa **Mallin tiedot - MAPE** **Kysynnän ennusteen tiedot** -sivulla. 

> [!NOTE]
> Jos käytät kysynnän ennusteiden Microsoft Azuren automaattianalyysiä, sisäisen mallin tarkkuuden laskenta perustuu testitietojen joukkoon. Voit määrittää testitietojoukon koon määrittämällä **TEST\_SET\_SIZE\_PERCENT** (Testijoukon koon prosenttiosuus) -parametrin **Kysynnän ennusteen parametrit** -sivulla. Jos esimerkiksi määrität arvoksi **20**, historiallisten tietojen viimeistä 20 prosenttia käytetään sisäisen mallin tarkkuuden laskemiseen.


## <a name="additional-resources"></a>Lisäresurssit

- [Oikaistun ennusteen valtuuttaminen](authorize-adjusted-forecast.md)
- [Poista poikkeavat tiedot aiemmista tapahtumatiedoista laskettaessa ennustetarvetta](remove-historical-outliers-calculating-demand-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]