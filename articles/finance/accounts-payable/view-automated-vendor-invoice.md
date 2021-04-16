---
title: Toimittajan laskun automatisoinnin tulosten näyttäminen (esiversio)
description: Tässä ohjeaiheessa käsitellään niiden toimittajan laskujen tilan näyttämistä, jotka ovat automatisoidussa työnkulkuun lähettämisprosessissa.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 872ec404da0cce41c4ea0f882a3fa8af56316ce3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837222"
---
# <a name="view-vendor-invoice-automation-results"></a>Toimittajan laskujen automaatiotulosten tarkasteleminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään niiden toimittajan laskujen tilan näyttämistä, jotka ovat automatisoidussa työnkulkuun lähettämisprosessissa. Kunkin tuodun toimittajan laskun automatisoinnin historiatiedot säilytetään. Automatisoidun prosessin mukaan **Odottavat toimittajan laskut** -sivulla näkyy **Automatisoidun vastaanoton täsmäytyksen tila**- ja **Automatisoidun työnkulkuun lähettämisen tila** -arvot. Voit tarkastella tietoja ja päättää suunnitelmasta, joka keskittyy automatisointivaiheessa epäonnistuneisiin laskuihin. Sen jälkeen kun ongelma on korjattu, voit jatkaa tuotujen laskujen automatisointiprosessia.

Ennen kuin lähetettyä laskua voi muokata, automatisoitu käsittely on keskeytettävä. Jos automatisoidussa työnkulkuun lähetysprosessissa oleva lasku on keskeytettävä, määritä **Sisällytä automatisoituun käsittelyyn** -kentän arvoksi **Ei** **Toimittajan laskut** -sivulla. Automatisointia ei sitten suoriteta, ennen kuin **Sisällytä automatisoituun käsittelyyn** -arvoksi on määritetty **Kyllä**. Laskun lisäautomatisointi voidaan keskeyttää, jos se ei ole vielä työnkulkujärjestelmässä ja jos automatisoitu prosessi ei käytä sitä.

Jos tuotu lasku on työnkulkuun lähettämisprosessissa, sen **Automatisoinnin tila** -arvon voi tarkistaa **Toimittajan laskut** -sivulla. Seuraavat tiloja seurataan:

- **Sisällytetty** – **Ostoreskontran parametrit** -sivulla määritetyt automatisoidut prosessit ovat käynnissä, mutta ne eivät ole vielä valmiita.
- **Keskeytetty** – **Ostoreskontran parametrit** -sivulla määritetyt automatisoidut prosessit on suoritettu, mutta ainakin yksi prosessin vaihe epäonnistui. **Keskeytetty**-tila on käytössä myös silloin, jos **Sisällytä automatisoituun käsittelyyn** -kentän arvo on **Ei**. Voit tarkastella epäonnistuneita vaiheita valitsemalla **Näytä viimeisimmät tulokset**.
- **Työnkulussa** – tuotu lasku on lähetetty työnkulkujärjestelmään joko automatisoidussa työnkulkuun lähettämisprosessissa tai manuaalisesti.
- **Työnkulku valmis** – tuodun laskun työnkulkuprosessi on valmis.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]