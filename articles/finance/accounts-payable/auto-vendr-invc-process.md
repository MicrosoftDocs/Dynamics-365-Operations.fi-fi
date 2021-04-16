---
title: Automaattisten toimittajan laskutusprosessien yleiskuvaus
description: Tässä ohjeaiheessa käsitellään toimittajan laskujen käsittelyn automatisointiominaisuutta ja automatisoidun prosessin etuja.
author: abruer
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 37dd76773abb69819bfd32bb2813bb8b42b2a375
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820832"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Automaattisten toimittajan laskutusprosessien yleiskuvaus

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään toimittajan laskujen käsittelyn automatisointiominaisuutta ja automatisoidun prosessin etuja. Tässä ominaisuudessa on toimintoja, jotka otetaan käyttöön ominaisuuksien hallinnassa. Nämä toiminnot koskevat vain toimittajan laskuja; ne eivät siis koske laskuja, jotka käsitellään **Laskukirjauskansio**- tai **Laskurekisterikirjauskansio**-sivulla.

Organisaatiot käyttävät usein kolmansia osapuolia paperilaskujen käsittelyssä hyödyntämällä OCR-tekstintunnistuspalvelua. Tällainen palvelu palauttaa koneellisesti luettavat laskun metatiedot. Ostoreskontran automaatiotoiminnot edistävät automatisointia, sillä näitä artefakteja voidaan käyttää ostoreskontrasta.

Tietyt ostoreskontran toimittajan laskutusprosessit voidaan automatisoida. Näitä prosesseja ovat esimerkiksi tuotujen toimittajan laskujen lähettämisen työnkulkujärjestelmään ja kirjattujen tuotteen vastaanottorivien täsmäyttäminen odottaviin toimittajan laskuriveihin. Automatisoitu prosessi näyttää tietoja toimittajan laskun etenemisestä prosessin kussakin vaiheessa. Tämän ominaisuuden avulla ostoreskontran käsittelijät ja esimiehet voivat käsitellä toimittajan laskuja entistä tehokkaammin. Lisäksi se auttaa vähentämään virheitä ja tehottomuuksia, joita voi esiintyä, kun tietoja syötetään ja käsitellään manuaalisesti.

Automatisoiduilla prosesseilla voidaan suorittaa seuraavia tehtäviä:

- Tuotujen laskujen lähettäminen automaattisesti työnkulkujärjestelmään.
- Tuotteen vastaanottojen täsmäyttäminen odottaviin toimittajan laskuriveihin.
- Kirjauksen simuloiminen ennen toimittajan laskun kirjaamista.
- Työnkulkuhistorian näyttäminen nopeasti ja tehokkaasti.
- Toimittajan laskun käsittelyn automatisoinnin tulosten näyttäminen ja analysoiminen.
- Jatka useiden laskujen automaattista käsittelyä.

## <a name="submit-imported-vendor-invoices-to-the-workflow-system"></a>Tuotujen toimittajalaskujen lähettäminen työnkulkujärjestelmään

Ilman käyttäjän toimia tehtävän ostoreskontraprosessin osana on mahdollista määrittää, että järjestelmä lähettää tuodun laskun automaattisesti työnkulkujärjestelmään. Prosessi suoritetaan taustalla määritetyin toistovälein (joko kerran tunnissa tai kerran päivässä). Mahdollisuus lähettää tuodut laskut automaattisesti työnkulkujärjestelmään edellyttää, että prosessi alkaa tuodulla laskulla. Työnkulkumääritykseen on sisällytettävä automaattinen kirjaustehtävä, sillä näin voidaan varmistaa, että lasku voidaan käsitellä alusta loppuun ilman manuaalisia toimia.


Ostotilauksiin liittyvät laskut sekä ei-ostotilauksellisen hankintaluokan ja varastossa olemattomia rivejä sisältävät laskut voidaan lähettää automaattisesti työnkulkujärjestelmään. Manuaalisesti syötetyt ja **Toimittajayhteistyön laskutus** -työtilassa luodut laskut on lähetettävä manuaalisesti työnkulkujärjestelmään. Tuoduille laskuille on suoritettava manuaalisesti ennakkomaksujen sovelluskäsittely. Voit kohdistaa ennakkomaksut manuaalisesti ennen tuodun laskun kirjaamista tai sen jälkeen. Voit kohdistaa ennakkomaksuja kirjaamattomiin vakiolaskuihin manuaalisesti **Toimittajan laskut** -sivulla. Kirjauksen jälkeen selvitetty ennakkomaksu on käytettävissä manuaalisesti muiden tämän toimittajan laskujen kohdistamiseen **Toimittajat**-sivulla (**Ostoreskontra \> Yhteiset \> Toimittajat \> Kaikki toimittajat \> Lasku-väliehti \> Kohdista**).

Automatisointitoiminto on joustava kehys, jossa voi määrittää yrityskohtaisia sääntöjä tuotujen toimittajan laskujen lähettämiseen työnkulkujärjestelmään ja kirjatun tuotteen vastaanottorivien täsmäyttämiseen odottaviin toimittajan laskuriveihin.

## <a name="match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Tuotteen vastaanottojen täsmäyttäminen laskuriveille, joilla on kolmisuuntainen vastaavuuskäytäntö

Järjestelmä voi automaattisesti täsmäyttää kirjatut tuotteen vastaanotot laskuriveillä, joille on määritetty kolmisuuntainen vastaavuuskäytäntö. Prosessia suoritetaan siihen saakka, että täsmäytetty tuotteen vastaanottomäärä on sama kuin laskun määrä. Tämän prosessin osana määritetään, kuinka monta kertaa järjestelmä enintään yrittää täsmäyttää tuotteen vastaanotot laskuriviin, ennen kuin se päättää prosessin epäonnistuneena. Prosessi suoritetaan taustalla joko kerran tunnissa tai kerran päivässä. Automatisoitu täsmäytysprosessi voidaan suorittaa osana laskujen työnkulkujärjestelmään lähettämisprosessia. Vaihtoehtoisesti se voidaan suorittaa erillisenä prosessina.

## <a name="pre-validate-vendor-invoice-posting"></a>Toimittajan laskun kirjaamisen ennakkotarkistus

Kirjauksen simulointi suorittaa toimittajan laskujen kirjausprosessin aikana tehtävät vahvistusvaiheet, mutta mitään tilejä ei päivitetä. Prosessi suoritetaan valitsemalla joko yksi lasku tai useita laskuja **Odottavat toimittajan laskut** -sivulla.

## <a name="enhanced-experience-for-viewing-workflow-and-automation-historical-information-for-vendor-invoices"></a>Parannettu toimittajan laskujen työnkulun ja automaation historiatietojen katselukokemus

Käytettävissä on helppolukuinen toimittajan laskun työnkulkuhistorianäkymä. Toimittajan laskun työnkulkuhistoriaan voidaan siirtyä suoraan toimittajan laskusta. Näiden tietojen saamiseen tarvitaan siis vähemmän napsautuksia. Jos organisaatiosi on mahdollistanut tuotujen toimittajan laskujen automaattisen lähettämisen työnkulkuun, tuotujen laskujen automaatiohistoria on käytettävissä. Automaatiohistorian avulla voit tunnistaa nykyisen prosessivaiheen sekä vaiheet, jotka on jo suoritettu. Kun vaihe epäonnistuu, järjestelmä antaa yksityiskohtaisia tietoja virheen syystä.

## <a name="analytics-and-metrics"></a>Analytiikka ja mittarit

**Toimittajan laskutapahtuma** -työtilassa voi keskittyä toimittajan laskuihin, joita ei voitu käsitellä automatisoidussa prosessissa. Työtilan ruuduissa on tietoja toimittajan laskuista, joiden lähettäminen työnkulkujärjestelmään, tuominen tai täsmäyttäminen tuotteen vastaanottoihin ei onnistunut. Ostoreskontran esimiehet puolestaan saavat Microsoft Power BI -mittareiden avulla merkityksellistä tietoa toimittajan laskun automatisoinnin tehokkuudesta.


## <a name="resume-automation-processing-for-multiple-invoices"></a>Jatka useiden laskujen automaattista käsittelyä

Kun tuodun laskun lähettäminen ei onnistu työnkulkuun automatisoidun prosessin avulla, järjestelmä poistaa sen automaattisesta käsittelystä. Ostoreskontran käsittelijä voi tarkastella ja muokata laskua, ennen kuin automaattinen prosessi lähettää sen uudelleen työnkulkuun. Vian syy voidaan ratkaista saman korjauksen avulla useita laskuja varten. Voit käynnistää automaattisen prosessin uudelleen **Jatka automaattista laskujen käsittelyä** -sivulla. 

## <a name="tracking-the-invoice-received-date-value"></a>Laskun vastaanottopäivämäärän arvon seuraaminen

**Laskun vastaanottopäivämäärä** -arvo ilmaisee päivämäärän, jolloin yritys vastaanotti laskun toimittajalta. Sen avulla voidaan seurata laskun etenemistä automaatioprosessien läpi. Tämä arvo voidaan sisällyttää toimittajan laskun tuotuihin tietoihin. Voit määrittää päivämäärän manuaalisesti luoduille laskuille. Jos arvoa ei ole määritetty, oletusarvon mukaan käytetään kuluvaa päivää.


## <a name="tracking-the-imported-invoice-amount-and-imported-sales-tax-amount-values"></a>Tuodun laskun summan ja tuodun arvonlisäveron summan arvojen seuranta

Toimittajan laskujen tuontitiedostossa voi määrittää **tuodun laskun summan** ja **tuodun arvonlisäveron summan** arvot. Tavallisesti arvot ovat peräisin laskusta, jonka ulkopuolinen palveluntarjoaja on skannannut ja sisällyttänyt tuontitiedostoon. Kun laskua käsitellään ostoreskontrassa, järjestelmä laskee arvot laskutietojen perusteella. Laskun voi kirjata vain, jos tuodut arvot vastaavat laskettuja arvoja. Täsmäytysarvojen avulla varmistetaan, että lasku vastaa tarkasti toimittajalle maksettavaa summaa. Jos organisaatio sallii tuotujen laskujen lähettämisen työnkulkujärjestelmään automaattisesti, voit halutessasi edellyttää, että tuodut summat vastaavat laskettuja kokonaissummia, ennen kuin lasku voidaan lähettää työnkulkujärjestelmään.

## <a name="vendor-invoice-automation---resume-automation-processing-for-multiple-invoices"></a>Toimittajan laskun automaatio - useiden laskujen automaattisen käsittelyn jatkaminen
Kun tuodun laskun lähettäminen ei onnistu työnkulkuun automatisoidun prosessin kautta, järjestelmä poistaa sen automaattisesta käsittelystä. Ostoreskontran käsittelijä voi tarkastella ja muokata laskua, ennen kuin automaattinen prosessi lähettää sen uudelleen työnkulkuun. Vian syy voidaan ratkaista saman korjauksen avulla useita laskuja varten. Voit käynnistää automaattisen prosessin uudelleen **Jatka automaattista laskujen käsittelyä** -sivulla. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
