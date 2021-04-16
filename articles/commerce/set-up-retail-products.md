---
title: Vähittäismyyntituotteiden määrittäminen
description: Tässä artikkelissa käsitellään tuotteiden määrittämistä Dynamics 365 Commercessa.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5c8ae2f385e2e3a4d08412d9da4ab68d50496211
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795498"
---
# <a name="set-up-retail-products"></a>Vähittäismyyntituotteiden määrittäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään tuotteiden määrittämistä Dynamics 365 Commercessa.

Sinun on luotava ja määritettävä tuotteet uudelleen myytäviksi Commerce-sovelluksessa, ennen kuin tuotteita voi tarjota myytäväksi. Commerce luo organisaationlaajuiset tuotteet päätuotteessa. Voit luoda tuotteita, määrittää tuotteiden ominaisuuksia ja määritteitä sekä määrittää tuotteet kauppaluokkahierarkioihin. Jotta tuotteet olisivat käytettävissä kanavissa ja jotta ne voitaisiin lisätä aktiiviseen valikoimaan, tuotteet on vapautettava yrityksiin, jossa ne ovat saatavilla. Voit määrittää tuotteet, joita myydään kanavissa, toimimalla seuraavasti.

1. **Määritä tuotehierarkia.** Käyttämällä Commercen luokkahierarkiaominaisuuksia voit määrittää luokkahierarkiat, joiden avulla voit ryhmitellä ja luokitella kanaviin jaeltavat tuotteet. Käyttäjän määrittämät ja järjestelmän määritteet voidaan määritellä luokkatasolla. Tämän jälkeen kaikki kyseiseen luokkaan määritetyt tuotteet perivät nämä määritteet. Luokkahierarkioita voidaan määritellä useita, ja kukin tuote voidaan määrittää useaan hierarkiaan. Yhden hierarkian sisällä kukin tuote voidaan kuitenkin määrittää vain yhteen luokkaan.
2. **Lisää tuotteita ja tuotevariantteja päätuotteeseen.** Tuotteet, jotka lisätään päätuotteeseen, edustavat yleistä tuoteluetteloa. Voit lisätä tuotteita manuaalisesti yhden kerrallaan tai tuoda tuotetietoja toimittajilta.
3. **Vapauta tuotteet yrityksille.** Vain tuotteet, jotka on vapautettu yrityksille, voidaan tuoda kanavien saataville. Kun määrität jotakin tuotetta ensimmäisen kerran, voit määrittää sen organisaationlaajuiselle tasolle. Tämän jälkeen voit valita yhden tai useamman yrityksen, jolle tuote vapautetaan. Tuote on tämän jälkeen usean kanavan käytettävissä organisaatiossa. Näillä toiminnoilla voit luoda yhden tuotteen kerrallaan, lisätä ja päivittää tuotemääritteitä ja -ominaisuuksia samassa paikassa ja jaella tuotteen organisaatiossa niille kanaville, joissa se on käytettävissä.
4. **Lisää tuotteet valikoimiin.** Valikoiman edustaa kanavissa tarjottavien tuotteiden kokoelmaa. Voit määrittää yhden tai useamman valikoiman ja määrittää kunkin tuotteen yhteen tai useampaan valikoimaan. Jos haluat määrittää tuotteita kanaville, määritä valikoimat kyseisille kanaville. Luodessasi valikoimaa voit lisätä tuotteita, joita ei ole vielä vapautettu yritykselle. Tuotteet on kuitenkin julkaistava jollekin yritykselle, ennen kuin ne voidaan tuoda kanavien käyttöön.
5. **Lisää tuotteet siirtymishierarkioihin.** Ennen kuin tuotteita voidaan selata verkossa tai myyntipisteessä, ne on luokiteltava johonkin Commercen siirtymishierarkiaan.
6. **Lisää tuotteet luetteloon.** Tämä vaihe on myyntipisteiden osalta valinnainen, mutta verkkokaupat edellyttävät, että tuotteet sisältyvät vähintään yhteen luetteloon.


[!INCLUDE[footer-include](../includes/footer-banner.md)]