---
title: Automaattisten toimittajan laskutusprosessien yleiskuvaus
description: Tässä ohjeaiheessa käsitellään toimittajan laskujen käsittelyn automatisointiominaisuutta ja automatisoidun prosessin etuja.
author: abruer
manager: AnnBe
ms.date: 08/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 187b3c4f1a8b2c9ec6df95c19b261756ec4562dc
ms.sourcegitcommit: 6ffbae02de2eee1f3be9bab2da37a3771aae8bec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2020
ms.locfileid: "3905009"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Automaattisten toimittajan laskutusprosessien yleiskuvaus

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa käsitellään toimittajan laskujen käsittelyn automatisointiominaisuutta ja automatisoidun prosessin etuja. Tässä ominaisuudessa on toimintoja, jotka otetaan käyttöön ominaisuuksien hallinnassa. Nämä toiminnot koskevat vain toimittajan laskuja; ne eivät siis koske laskuja, jotka käsitellään **Laskukirjauskansio**- tai **Laskurekisterikirjauskansio**-sivulla.

Organisaatiot käyttävät usein kolmansia osapuolia paperilaskujen käsittelyssä hyödyntämällä OCR-tekstintunnistuspalvelua. Tällainen palvelu palauttaa koneellisesti luettavat laskun metatiedot. Ostoreskontran automaatiotoiminnot edistävät automatisointia, sillä näitä artefakteja voidaan käyttää ostoreskontrasta.

Tietyt ostoreskontran toimittajan laskutusprosessit voidaan automatisoida. Näitä prosesseja ovat esimerkiksi tuotujen toimittajan laskujen lähettämisen työnkulkujärjestelmään ja kirjattujen tuotteen vastaanottorivien täsmäyttäminen odottaviin toimittajan laskuriveihin. Automatisoitu prosessi näyttää tietoja toimittajan laskun etenemisestä prosessin kussakin vaiheessa. Tämän ominaisuuden avulla ostoreskontran käsittelijät ja esimiehet voivat käsitellä toimittajan laskuja entistä tehokkaammin. Lisäksi se auttaa vähentämään virheitä ja tehottomuuksia, joita voi esiintyä, kun tietoja syötetään ja käsitellään manuaalisesti.

Automatisoiduilla prosesseilla voidaan suorittaa seuraavia tehtäviä:

- Tuotujen laskujen lähettäminen automaattisesti työnkulkujärjestelmään.
- Tuotteen vastaanottojen täsmäyttäminen odottaviin toimittajan laskuriveihin.
- Kirjauksen simuloiminen ennen toimittajan laskun kirjaamista.
- Työnkulkuhistorian näyttäminen nopeasti ja tehokkaasti.
- Toimittajan laskun käsittelyn automatisoinnin tulosten näyttäminen ja analysoiminen.

## <a name="vendor-invoice-automation--submit-imported-vendor-invoices-to-the-workflow-system"></a>Toimittajan laskun automatisointi – tuotujen toimittajan laskujen lähettäminen työnkulkujärjestelmään.

Ilman käyttäjän toimia tehtävän ostoreskontraprosessin osana on mahdollista määrittää, että järjestelmä lähettää tuodun laskun automaattisesti työnkulkujärjestelmään. Prosessi suoritetaan taustalla määritetyin toistovälein (joko kerran tunnissa tai kerran päivässä). Mahdollisuus lähettää tuodut laskut automaattisesti työnkulkujärjestelmään edellyttää, että prosessi alkaa tuodulla laskulla. Työnkulkumääritykseen on sisällytettävä automaattinen kirjaustehtävä, sillä näin voidaan varmistaa, että lasku voidaan käsitellä alusta loppuun ilman manuaalisia toimia.

'Ostotilauksiin liittyvät laskut sekä ei-ostotilauksellisen hankitaluokan ja varastossa olemattomia rivejä sisältävät laskut voidaan lähettää automaattisesti työnkulkujärjestelmään. Manuaalisesti syötetyt ja **Toimittajayhteistyön laskutus** -työtilassa luodut laskut on lähetettävä manuaalisesti työnkulkujärjestelmään.

Automatisointitoiminto on joustava kehys, jossa voi määrittää yrityskohtaisia sääntöjä tuotujen toimittajan laskujen lähettämiseen työnkulkujärjestelmään ja kirjatun tuotteen vastaanottorivien täsmäyttämiseen odottaviin toimittajan laskuriveihin.

## <a name="vendor-invoice-automation--match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Toimittajan laskun automatisointi – tuotteen vastaanottojen täsmäyttäminen laskuriveille, joilla on kolmisuuntainen vastaavuuskäytäntö

Järjestelmä voi automaattisesti täsmäyttää kirjatut tuotteen vastaanotot laskuriveillä, joille on määritetty kolmisuuntainen vastaavuuskäytäntö. Prosessia suoritetaan siihen saakka, että täsmäytetty tuotteen vastaanottomäärä on sama kuin laskun määrä. Tämän prosessin osana määritetään, kuinka monta kertaa järjestelmä enintään yrittää täsmäyttää tuotteen vastaanotot laskuriviin, ennen kuin se päättää prosessin epäonnistuneena. Prosessi suoritetaan taustalla joko kerran tunnissa tai kerran päivässä. Automatisoitu täsmäytysprosessi voidaan suorittaa osana laskujen työnkulkujärjestelmään lähettämisprosessia. Vaihtoehtoisesti se voidaan suorittaa erillisenä prosessina.

## <a name="vendor-invoice-automation--pre-validate-vendor-invoice-posting"></a>Toimittajan laskun automatisointi – toimittajan laskun kirjauksen esivahvistus

Kirjauksen simulointi suorittaa toimittajan laskujen kirjausprosessin aikana tehtävät vahvistusvaiheet, mutta mitään tilejä ei päivitetä. Prosessi suoritetaan valitsemalla joko yksi lasku tai useita laskuja **Odottavat toimittajan laskut** -sivulla.

## <a name="vendor-invoice-automation--enhanced-experience-for-viewing-workflow-historical-information-for-vendor-invoices"></a>Toimittajan laskun automatisointi – parannettu toimittajan laskujen työnkulun historiatietojen katselukokemus

Käytettävissä on helppolukuinen toimittajan laskun työnkulkuhistorianäkymä. Toimittajan laskun työnkulkuhistoriaan voidaan siirtyä suoraan toimittajan laskusta. Näiden tietojen saamiseen tarvitaan siis vähemmän napsautuksia.

## <a name="vendor-invoice-automation--analytics-and-metrics"></a>Toimittajan laskun automatisointi – analytiikka ja mittarit

**Toimittajan laskutapahtuma** -työtilassa voi keskittyä toimittajan laskuihin, joita ei voitu käsitellä automatisoidussa prosessissa. Työtilan ruuduissa on tietoja toimittajan laskuista, joiden lähettäminen työnkulkujärjestelmään, tuominen tai täsmäyttäminen tuotteen vastaanottoihin ei onnistunut. Ostoreskontran esimiehet puolestaan saavat Microsoft Power BI -mittareiden avulla merkityksellistä tietoa toimittajan laskun automatisoinnin tehokkuudesta.
