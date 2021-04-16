---
title: Käyttöomaisuusryhmien jälleenhankintahintojen ja vakuutusarvojen uudelleenlaskenta
description: Tässä artikkelissa on selostettu prosessia, jolla päivitetään käyttöomaisuuden jälleenhankintahinnat ja vakuutusarvot.
author: ShylaThompson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0509c0ea2fe6e4d04aeec451969a81eb33b1d19
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826296"
---
# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Käyttöomaisuusryhmien jälleenhankintahintojen ja vakuutusarvojen uudelleenlaskenta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on selostettu prosessia, jolla päivitetään käyttöomaisuuden jälleenhankintahinnat ja vakuutusarvot.

Tiettyjen käyttöomaisuuserien jälleenhankintahinta tai vakuutusarvo voi toisinaan muuttua. Esimies voi esimerkiksi ilmoittaa, että inflaatio on ollut viime vuonna 3 prosenttia, joten kaikkien käyttöomaisuuserien jälleenhankintahintaa täytyy korottaa 3 prosenttia. 

Vaikka yksittäisten käyttöomaisuuserien jälleenhankintahintaa ja vakuutusarvoa voikin muokata **Käyttöomaisuudet**-sivulla, kokonaisen käyttöomaisuusryhmän arvot voi päivittää kerralla **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivulla. Tässä ohjeessa kuvataan käyttöomaisuusryhmien tai tiettyjen ryhmän käyttöomaisuuksien arvojen päivittäminen.

## <a name="how-values-are-updated"></a> Tietoja arvojen päivittämisestä
Jos haluat laskea käyttöomaisuusryhmien jälleenhankintahinnan ja vakuutusarvon uudelleen, määritä ensin prosenttiosuus, jonka mukaisesti aiempia jälleenhankintahintoja ja vakuutusarvoja muutetaan, ja laske sitten varsinaiset arvot uudelleen suorittamalla kausittainen päivitys. Prosenttiosuus määritetään **Jälleenhankintahinnan kerroin**- ja **Vakuutusarvon kerroin** -kenttiin **Käyttöomaisuusryhmät**-sivulla. Vaikka nämä muutosluvut voikin määrittää koko käyttöomaisuusryhmälle, **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivua käyttäessäsi voit valita, että jälleenhankintahinta ja vakuutusarvo lasketaan uudelleen vain ryhmän tietyille käyttöomaisuuserille. 

Kun käyttöomaisuuserien jälleenhankintahinta ja vakuutusarvo lasketaan uudelleen **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivulla, järjestelmä käyttää seuraavia kaavoja:

-   \[(Käyttöomaisuusryhmän jälleenhankintahinnan muutos / 100) + 1\] \* Käyttöomaisuuserän nykyinen jälleenhankintahinta
-   \[(Käyttöomaisuusryhmän vakuutusarvon muutos / 100) + 1\] \* Käyttöomaisuuserän nykyinen vakuutusarvo

> [!NOTE] 
> Kun käytät **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivulla, valittujen käyttöomaisuuserien jälleenhankintahinta ja vakuutusarvo päivitetään; vain jommankumman arvon päivittäminen ei ole mahdollista. Jos haluat jättää yhden arvon ennalleen ja päivittää toisen arvon, lisää muutosluvuksi 0 (nolla) **Käyttöomaisuusryhmät**-sivulla. Jos kertoimen arvoksi määritetään nolla tai tyhjä, laskenta ohitetaan päivityksessä. Kausittainen päivitys ei vaikuta käyttöomaisuuserien kirjanpitoarvoon ja nettokirjanpitoarvoon. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a> Tietoja päivitettävien nimikkeiden valitsemisesta päivämäärän perusteella
Oletusarvon mukaan päivityskäsittely päivittää valitut käyttöomaisuuserät, joita ei ole päivitetty kuluvana päivämääränä, mutta jotka on voitu päivittää edeltäneinä päivämäärinä. Esimerkiksi &lt; kuluva päivämäärä merkitsee "aiemmin kuin tänään". Voit muuttaa päivämäärää **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivun **Valitse**-painikkeella. Määrittämääsi päivämääräehtoa verrataan käyttöomaisuuserän edellisen kausittaisen päivityksen päivämäärään (**Käyttöomaisuudet**-sivun **Edellinen kausittainen arvon/hinnan päivitys** -kenttään). Aina kun käyttöomaisuuserän jälleenhankintahinta tai vakuutusarvo päivitetään onnistuneesti, järjestelmä päivittää kuluvan päivämäärän automaattisesti **Edellinen kausittainen arvon/hinnan päivitys** -kenttään. 

Esimerkki 

Ajoneuvot-, Toimistokalusteet- ja Rakennuksen-ryhmien jälleenhankintahintaa päivitettiin eilen 5 prosenttia, ja ko. käyttöomaisuuksien päivitystä voidaan pitää oikeana. Nämä käyttöomaisuuserät voi jättää pois tämänpäiväisestä päivityksestä, jossa kaikki muut käyttöomaisuuserät päivitetään. Tämä tehdään lisäämällä eilistä päivää edeltävä päivämäärä (&lt; eilisen päivämäärä) **Edellinen kausittainen arvon/hinnan päivitys** -kenttään, koska **ajoneuvojen**, **toimistokalusteiden** ja **rakennusten** edellinen päivitys tapahtui määritettyjen päivämääräkriteerien ulkopuolella.

## <a name="cumulative-effect-of-each-update"></a> Kunkin päivityksen kumulatiivinen vaikutus
Kullakin päivityksellä on kumulatiivinen vaikutus. Siksi päivitykset kannattaa suunnitella tarkkaan. Jos esimerkiksi teet kaikkiin käyttöomaisuuseriin kolmen prosentin korotuksen tiistaina ja toimistokalusteisiin neljä prosentin korotuksen perjantaina, toimistokalusteiden kumulatiivinen kokonaiskorotus on tällöin 7,12 prosenttia.

## <a name="scenario"></a>Skenaario
Esimies ilmoittaa seuraavista käyttöomaisuuseriin tulevista muutoksista:
-   Kaikkien käyttöomaisuuserien jälleenhankintahintaan tehdään 3,25 prosentin korotus tietokoneita lukuun ottamatta.
-   Kaikkien toimistokalusteiden jälleenhankintahintaan tehdään 1 prosentin lisäkorotus.
-   Kaikkien tietokoneiden jälleenhankintahintaa ja vakuutusarvoa pienennetään 10 prosenttia.

Teet seuraavat muutokset:
1.  Kirjoita **Käyttöomaisuusryhmät**-sivulla **Jälleenhankintahinnan kerroin** -kenttään 3,25 ja **Vakuutusarvon kerroin** -kenttään 0 kaikille käyttöomaisuusryhmille **Toimistokalusteet**- ja **Tietokoneet**-ryhmiä lukuun ottamatta.
2.  **Toimistokalusteet**-ryhmän **Jälleenhankintahinnan kerroin** -kenttään kirjoitat 4,25 ja **Vakuutusarvon kerroin** -kenttään 0.
3.  **Tietokoneet**-ryhmän **Jälleenhankintahinnan kerroin** -kenttään kirjoitat -10 ja **Vakuutusarvon kerroin** -kenttään -10.
4.  Suorita kaikkien käyttöomaisuuserien uudelleenlaskenta valitsemalla **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivulla **OK**.

Seuraavana päivänä esimies ilmoittaa, että tietokoneiden pienennyksen oli tarkoitus olla 8 prosenttia 10 prosentin asemesta, joten jälleenhankintahintoihin ja vakuutusarvoihin täytyy tehdä oikaisu. Voit korjata virheen seuraavilla tavoilla:
-   Muokkaa **Tietokoneet**-käyttöomaisuusryhmän jokaista käyttöomaisuuserää manuaalisesti **Käyttöomaisuudet**-sivun **Jälleenhankintahinta**- ja **Vakuutusarvo**-kentissä. Laske ja lisää arvot manuaalisesti niin kuin olisit alun perin pienentänyt alkuperäistä summaa 8 prosenttia. Tässä menetelmässä ei käytetä **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivua.
-   Kirjoita jälleenhankintahinnan ja vakuutusarvon kertoimet **Tietokoneet**-ryhmän **Jälleenhankintahinnan kerroin**- ja **Vakuutusarvon kerroin** -kenttiin **Käyttöomaisuusryhmät**-sivulla. Tämä tarkoittaa, että käyttöomaisuuserät palautetaan (10 prosentin vähennystä edeltävien) alkuperäisten arvojen mukaisiksi ja alkuperäistä arvoa pienennetään 8 prosenttia. Laske sitten arvot uudelleen **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivulla ilmoitettujen arvojen mukaisesti.

> [!NOTE]  
> Muutoslukua -10 ei voi peruuttaa lisäämällä positiivinen muutosluku 10 (tai kertoimella 2, joka on lukujen -10 ja -8 erotus), koska summat lasketaan tällöin eri tavalla kuin käyttäjä on tarkoittanut. 







[!INCLUDE[footer-include](../../includes/footer-banner.md)]