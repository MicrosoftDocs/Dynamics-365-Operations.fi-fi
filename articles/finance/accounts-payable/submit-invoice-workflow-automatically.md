---
title: Laskujen lähettäminen työnkulkujärjestelmään ja tuotteen vastaanottorivien täsmäyttäminen
description: Tässä ohjeaiheessa käsitellään toimittajan laskujen lähettämisprosessia työnkulkujärjestelmään ja kirjattujen tuotteen vastaanottorivien täsmäyttämistä automaattisesti toimittajan laskuihin.
author: abruer
manager: AnnBe
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 03c9f6752a0bb9641f67d65580aca18276e43e9a
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115653"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a>Laskujen lähettäminen työnkulkujärjestelmään ja tuotteen vastaanottorivien täsmäyttäminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään toimittajan laskujen lähettämisprosessia työnkulkujärjestelmään ja kirjattujen tuotteen vastaanottorivien täsmäyttämistä automaattisesti toimittajan laskuihin.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Toimittajan laskujen lähettäminen työnkulkujärjestelmään ja kirjattujen tuotteen vastaanottorivien täsmäyttäminen odottaviin toimittajan laskuriveihin.

Ilman käyttäjän toimia tehtävän ostoreskontraprosessin osana on mahdollista määrittää, että järjestelmä lähettää tuodun laskun automaattisesti työnkulkujärjestelmään. Voit määrittää tuotujen laskujen lähettämisen työnkulkujärjestelmään valitsemalla **Toimittajan laskujen automatisointi** -välilehden **Ostoreskontran parametrit** -sivulla (**Ostoreskontra \> Asetukset \> Ostoreskontran parametrit**). Työnkulkuun lähettämisprosessi suoritetaan taustalla määritetyin toistovälein (joko kerran tunnissa tai kerran päivässä).

Kun laskujen lähetetään automaattisesti työnkulkujärjestelmään, lähtökohtana on oltava tuotu lasku. Työnkulkumääritykseen on sisällytettävä automaattinen kirjaustehtävä, sillä näin voidaan varmistaa, että lasku voidaan käsitellä alusta loppuun ilman manuaalisia toimia. Ostotilauksiin liittyvät laskut sekä ei-ostotilauksellisen hankintaluokan ja varastossa olemattomia rivejä sisältävät laskut voidaan lähettää automaattisesti työnkulkujärjestelmään. Manuaalisesti annetut laskut on lähetettävä manuaalisesti työnkulkujärjestelmään.

Työnkulun **Lähettäjä**-arvo on se käyttäjätunnus, joka annettiin **Lähetä toimittajan laskut työnkulkuun** -taustatehtävässä **Prosessin automatisointi** -sivulla. Käyttäjä, jolla on kyseinen käyttäjätunnus, voi tarvittaessa peruuttaa työnkulussa olevan laskun.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Tuotteen vastaanottojen täsmäyttäminen laskuriveille, joilla on kolmisuuntainen vastaavuuskäytäntö

Järjestelmä voi automaattisesti täsmäyttää kirjatut tuotteen vastaanotot laskuriveille osana ilman käyttäjän toimia suoritettavaa ostoreskontran laskutusprosessia. Tälle tehtävälle on määritettävä kolmisuuntainen vastaavuuskäytäntö. Tämä toiminto on käytettävissä, jos **Toimittajan laskun automatisointi** -toiminto on otettu käyttöön **Ominaisuuksien hallinta** -sivulla.

Prosessia suoritetaan siihen saakka, että täsmäytetty tuotteen vastaanottomäärä on sama kuin laskun määrä. Tämän prosessin osana määritetään, kuinka monta kertaa järjestelmä enintään yrittää täsmäyttää tuotteen vastaanotot laskuriviin, ennen kuin se päättää prosessin epäonnistuneena. Prosessi suoritetaan taustalla joko kerran tunnissa tai kerran päivässä. Automatisoitu täsmäytysprosessi voidaan suorittaa osana laskujen työnkulkujärjestelmään lähettämisprosessia. Vaihtoehtoisesti se voidaan suorittaa erillisenä prosessina. Tuotteen vastaanottojen laskuriveille täsmäyttämisprosessin asetukset määritetään valitsemalla **Toimittajan laskujen automatisointi** -välilehden **Ostoreskontran parametrit** -sivulla (**Ostoreskontra \> Asetukset \> Ostoreskontran parametrit**).

Automaattiseen tuotteen vastaanoton täsmäyttämisprosessiin sisällytetään laskurivit, joiden kolmisuuntaisen vastaavuuskäytännön vastaanotettu määrä on pienempi kuin laskun määrä.

Voit tarkastella niiden laskujen **Viimeisen täsmäytyksen tilaa**, jotka eivät sisälly automaattiseen työnkulkuun lähettämisprosessiin, avaamalla laskun **Toimittajan laskut** -sivulla. Täsmäytyksen vahvistustiedot päivitetään, kun tarkastelet laskua. **Viimeisen täsmäytyksen** tila voidaan päivittää automaattisesti käyttämällä **Vahvista laskun täsmäytys** -taustatehtävää. Voit määrittää **viimeisen täsmäytyksen** tilan automaattisen päivityksen **Taustaprosessit**-välilehdessä **Prosessin automatisoinnit** -sivulla (**Järjestelmän hallinta\> Asetukset\> Prosessin automatisoinnit**).

Laskurivi jätetään automaattisen käsittelyn ulkopuolelle seuraavissa tilanteissa:

- Laskurivin **Automatisoidun vastaanoton täsmäytyksen tila** -arvo on **Epäonnistui**.
- Laskua käytetään.
- Lasku on työnkulkujärjestelmässä.
