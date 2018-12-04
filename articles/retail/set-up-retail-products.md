---
title: "Aseta vähittäismyyntituotteet"
description: "Tässä artikkelissa kuvataan vähittäiskaupan tuotteiden määrittäminen Microsoft Dynamics 365 for Retailissa."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0906d83ea00edcbd4c04a1f21cc0911828286607
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-retail-products"></a>Vähittäismyyntituotteiden määrittäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan vähittäiskaupan tuotteiden määrittäminen Microsoft Dynamics 365 for Retailissa.

Sinun on luotava ja määritettävä tuotteet Dynamics 365 for Retailissa, ennen kuin tuotteita voi tarjota myytäväksi vähittäismyyntikanavissa. Vähittäismyynti-osiossa päätuotteeseen voidaan luoda koko organisaatiota koskevia tuotteita käyttämällä Microsoft Dynamics 365 for Retailin tuotetoimintoja. Voit luoda tuotteet, määritellä tuotteen ominaisuudet ja määritteet ja liittää tuotteet vähittäismyynnin luokkahierarkioihin. Jos haluat tuoda tuotteet saataville vähittäismyyntikanavissa ja lisätä ne aktiiviseen valikoimaan, sinun täytyy vapauttaa tuotteet yrityksiin, joissa ne ovat käytettävissä. Voit määrittää tuotteet, joita myydään vähittäismyyntikanavissa, toimimalla seuraavasti.

1.  Määritä vähittäismyynnin tuotehierarkia. Käyttämällä Dynamics 365 for Retailin luokkahierarkiaominaisuuksia voit määrittää vähittäismyynnin luokkahierarkiat, joiden avulla voit ryhmitellä ja luokitella vähittäismyyntikanaviin jaeltavat tuotteet. Käyttäjän määrittämät ja järjestelmän määritteet voidaan määritellä luokkatasolla. Tämän jälkeen kaikki kyseiseen luokkaan määritetyt tuotteet perivät nämä määritteet. Luokkahierarkioita voidaan määritellä useita, ja kukin tuote voidaan määrittää useaan hierarkiaan. Yhden hierarkian sisällä kukin tuote voidaan kuitenkin määrittää vain yhteen luokkaan.
2.  Lisää tuotteita ja tuotevariantteja päätuotteeseen. Tuotteet, jotka lisätään päätuotteeseen, edustavat yleistä tuoteluetteloa. Voit lisätä tuotteita manuaalisesti yhden kerrallaan tai tuoda tuotetietoja toimittajilta.
3.  Vapauta tuotteet yrityksille. Vain tuotteet, jotka on vapautettu yrityksille, voidaan tuoda vähittäismyyntikanavien saataville. Kun määrität jotakin tuotetta ensimmäisen kerran, voit määrittää sen organisaationlaajuiselle tasolle. Tämän jälkeen voit valita yhden tai useamman yrityksen, jolle tuote vapautetaan. Tuote on tämän jälkeen usean vähittäismyyntikanavan käytettävissä organisaatiossa. Näillä toiminnoilla voit luoda yhden tuotteen kerrallaan, lisätä ja päivittää tuotemääritteitä ja -ominaisuuksia samassa paikassa ja jaella tuotteen organisaatiossa niille vähittäismyyntikanaville, joissa se on käytettävissä.
4.  Lisää tuotteet valikoimiin. Valikoiman edustaa vähittäismyyntikanavissa tarjottavien tuotteiden kokoelmaa. Voit määrittää yhden tai useamman valikoiman ja määrittää kunkin tuotteen yhteen tai useampaan valikoimaan. Jos haluat määrittää tuotteita vähittäismyyntikanaville, määritä valikoimat kyseisille vähittäismyyntikanaville. Luodessasi valikoimaa voit lisätä tuotteita, joita ei ole vielä vapautettu yritykselle. Tuotteet on kuitenkin julkaistava jollekin yritykselle, ennen kuin ne voidaan tuoda vähittäismyyntikanavien käyttöön.
5.  Lisää tuotteet siirtymishierarkioihin. Ennen kuin tuotteita voidaan selata verkossa tai myyntipisteessä, ne on luokiteltava johonkin vähittäismyynnin siirtymishierarkiaan.
6.  Lisää tuotteet luetteloon. Tämä vaihe on myyntipisteiden osalta valinnainen, mutta verkkokaupat edellyttävät, että tuotteet sisältyvät vähintään yhteen luetteloon.





