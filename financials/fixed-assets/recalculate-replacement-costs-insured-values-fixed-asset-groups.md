---
title: "Käyttöomaisuusryhmien korvaavan jälleenhankintahinnat ja vakuutusarvot arvot lasketaan uudelleen"
description: "Tässä artikkelissa on selostettu prosessia, jolla päivitetään käyttöomaisuuden jälleenhankintahinnat ja vakuutusarvot."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: 38f779274da370d436509e021cabf5b90ab08475
ms.lasthandoff: 03/31/2017


---

# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Käyttöomaisuusryhmien korvaavan jälleenhankintahinnat ja vakuutusarvot arvot lasketaan uudelleen

Tässä artikkelissa on selostettu prosessia, jolla päivitetään käyttöomaisuuden jälleenhankintahinnat ja vakuutusarvot.

Tiettyjen käyttöomaisuuserien jälleenhankintahinta tai vakuutusarvo voi toisinaan muuttua. Esimies voi esimerkiksi ilmoittaa, että inflaatio on ollut viime vuonna 3 prosenttia, joten kaikkien käyttöomaisuuserien jälleenhankintahintaa täytyy korottaa 3 prosenttia. 

Vaikka yksittäisten käyttöomaisuuserien jälleenhankintahintaa ja vakuutusarvoa voikin muokata Käyttöomaisuudet-lomakkeessa, kokonaisen käyttöomaisuusryhmän arvot voi päivittää kerralla Päivitä jälleenhankintahinnat ja vakuutusarvot -lomaketta käyttäen. Tässä ohjeessa kuvataan käyttöomaisuusryhmien tai tiettyjen ryhmän käyttöomaisuuksien arvojen päivittäminen.

## <a name="how-values-are-updated"></a> Tietoja arvojen päivittämisestä
Jos haluat laskea käyttöomaisuusryhmien jälleenhankintahinnan ja vakuutusarvon uudelleen, määritä ensin prosenttiosuus, jonka mukaisesti aiempia jälleenhankintahintoja ja vakuutusarvoja muutetaan, ja laske sitten varsinaiset arvot uudelleen suorittamalla kausittainen päivitys. Prosenttiosuus määritetään Jälleenhankintahinnan kerroin- ja Vakuutusarvon kerroin -kenttiin Käyttöomaisuusryhmät-lomakkeessa. Vaikka nämä muutosluvut voikin määrittää koko käyttöomaisuusryhmälle, Päivitä jälleenhankintahinnat ja vakuutusarvot -lomaketta käyttäessäsi voit valita, että jälleenhankintahinta ja vakuutusarvo lasketaan uudelleen vain ryhmän tietyille käyttöomaisuuserille. 

Kun käyttöomaisuuserien jälleenhankintahinta ja vakuutusarvo lasketaan uudelleen Päivitä jälleenhankintahinnat ja vakuutusarvot -lomakkeen avulla, järjestelmä käyttää seuraavia kaavoja:

-   \[(Käyttöomaisuusryhmän jälleenhankintahinnan muutos / 100) + 1\]\* käyttöomaisuuserän nykyinen jälleenhankintahinta
-   \[(Ryhmän käyttöomaisuuserän vakuutusarvon muutos / 100) + 1\]\* käyttöomaisuuserän nykyinen Vakuutusarvo

> [!NOTE] 
> Kun käytät Päivitä jälleenhankintahinnat ja vakuutusarvot -lomaketta, valittujen käyttöomaisuuserien jälleenhankintahinta ja vakuutusarvo päivitetään; vain jommankumman arvon päivittäminen ei ole mahdollista. Jos haluat jättää yhden arvon ennalleen ja päivittää toisen arvon, lisää muutosluvuksi 0 (nolla) Käyttöomaisuusryhmät-lomakkeeseen. Jos kertoimen arvoksi määritetään nolla tai tyhjä, laskenta ohitetaan päivityksessä. Kausittainen päivitys ei vaikuta käyttöomaisuuserien kirjanpitoarvoon ja nettokirjanpitoarvoon. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a> Tietoja päivitettävien nimikkeiden valitsemisesta päivämäärän perusteella
Oletusarvon mukaan päivityskäsittely päivittää valitut käyttöomaisuuserät, joita ei ole päivitetty kuluvana päivämääränä, mutta jotka on voitu päivittää edeltäneinä päivämäärinä. Esimerkiksi &lt;nykyinen päivämäärä tarkoittaa "ennen tätä päivää." Voit muuttaa päivämäärää päivitys korvaavan jälleenhankintahinnat ja vakuutusarvot arvoja-lomakkeessa napsauttamalla Valitse-painiketta. Määrittämääsi päivämääräkriteeriä verrataan käyttöomaisuuserän edellisen kausittaisen päivityksen päivämäärään (Käyttöomaisuudet-lomakkeen Edellinen kausittainen arvon/hinnan päivitys -kenttään). Aina kun käyttöomaisuuserän jälleenhankintahinta tai vakuutusarvo päivitetään onnistuneesti, järjestelmä päivittää kuluvan päivämäärän automaattisesti Edellinen kausittainen arvon/hinnan päivitys -kenttään. 

Esimerkki 

Voit päivittää ajoneuvoja, Toimistokalusteet ja rakennukset-ryhmien jälleenhankintahintaa eilen 5 prosenttia, ja nyt harkita omaisuuden jälleenhankintahintaa päivitettiin. Voit jättää nämä varat, kun kaikki muut käyttöomaisuuserät päivitetään tänään, kirjoittamalla päivämäärän viime Kausittainen arvon/hinnan päivitys-kenttä, joka on ennen eilisen (&lt; eilisen päivän päivämäärän), ajoneuvojen ja rakennusten toimistokalusteiden ryhmien viimeisen päivityksen vuoksi kirjoittamasi päivämäärän ehtojen ulkopuolelle.

## <a name="cumulative-effect-of-each-update"></a> Kunkin päivityksen kumulatiivinen vaikutus
Kullakin päivityksellä on kumulatiivinen vaikutus. Siksi päivitykset kannattaa suunnitella tarkkaan. Jos esimerkiksi teet kaikkiin käyttöomaisuuseriin kolmen prosentin korotuksen tiistaina ja toimistokalusteisiin neljä prosentin korotuksen perjantaina, toimistokalusteiden kumulatiivinen kokonaiskorotus on tällöin 7,12 prosenttia.

## <a name="scenario"></a>Skenaario
Esimies ilmoittaa seuraavista käyttöomaisuuseriin tulevista muutoksista:
-   Kaikkien käyttöomaisuuserien jälleenhankintahintaan tehdään 3,25 prosentin korotus tietokoneita lukuun ottamatta.
-   Kaikkien toimistokalusteiden jälleenhankintahintaan tehdään 1 prosentin lisäkorotus.
-   Kaikkien tietokoneiden jälleenhankintahintaa ja vakuutusarvoa pienennetään 10 prosenttia.

Teet seuraavat muutokset:
1.  Kirjoitat Käyttöomaisuusryhmät-lomakkeessa Jälleenhankintahinnan kerroin -kenttään 3,25 ja Vakuutusarvon kerroin -kenttään 0 kaikille käyttöomaisuusryhmille Toimistokalusteet- ja Tietokoneet-ryhmiä lukuun ottamatta.
2.  Toimistokalusteet-ryhmän Jälleenhankintahinnan kerroin -kenttään kirjoitat 4,25 ja Vakuutusarvon kerroin -kenttään 0.
3.  Tietokoneet-ryhmän Jälleenhankintahinnan kerroin -kenttään kirjoitat -10 ja Vakuutusarvon kerroin -kenttään -10.
4.  Suoritat kaikkien käyttöomaisuuserien uudelleenlaskennan napsauttamalla OK Päivitä jälleenhankintahinnat ja vakuutusarvot -lomakkeessa.

Seuraavana päivänä esimies ilmoittaa, että tietokoneiden pienennyksen oli tarkoitus olla 8 prosenttia 10 prosentin asemesta, joten jälleenhankintahintoihin ja vakuutusarvoihin täytyy tehdä oikaisu. Voit korjata virheen seuraavilla tavoilla:
-   Muokkaa Tietokoneet-käyttöomaisuusryhmän jokaista käyttöomaisuuserää manuaalisesti Käyttöomaisuudet-lomakkeen Jälleenhankintahinta- ja Vakuutusarvo-kentissä. Laske ja lisää arvot manuaalisesti niin kuin olisit alun perin pienentänyt alkuperäistä summaa 8 prosenttia. Tässä menetelmässä et käytä Päivitä jälleenhankintahinnat ja vakuutusarvot -lomaketta.
-   Kirjoita jälleenhankintahinnan ja vakuutusarvon kertoimet Tietokoneet-ryhmän Jälleenhankintahinnan kerroin- ja Vakuutusarvon kerroin -kenttiin Käyttöomaisuusryhmät-lomakkeessa. Tämä tarkoittaa, että käyttöomaisuuserät palautetaan (10 prosentin vähennystä edeltävien) alkuperäisten arvojen mukaisiksi ja alkuperäistä arvoa pienennetään 8 prosenttia. Laske sitten arvot uudelleen Päivitä jälleenhankintahinnat ja vakuutusarvot -lomakkeella kirjoittamiesi arvojen mukaisesti.

> [!NOTE]  
> Muutoslukua -10 ei voi peruuttaa lisäämällä positiivinen muutosluku 10 (tai kertoimella 2, joka on lukujen -10 ja -8 erotus), koska summat lasketaan tällöin eri tavalla kuin käyttäjä on tarkoittanut. 




