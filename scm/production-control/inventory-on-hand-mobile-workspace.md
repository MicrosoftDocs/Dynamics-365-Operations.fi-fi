---
title: "Varaston käytettävissä oleva mobiili työtilaa Microsoft Dynamics-365 toiminnot app"
description: "Käytettävissä olevan varaston mobiili työtilan auttaa syventämään näkemyksiä mobiili varastoon varatun ja käytettävissä milloin tahansa ja missä tahansa."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 85058f55-e566-40e2-9234-42d3e4fe5ff6
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 2ad48765528e1d1c6e7c90417b54a248ec79f546
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Varaston käytettävissä oleva mobiili työtilaa Microsoft Dynamics-365 toiminnot app

Käytettävissä olevan varaston mobiili työtilan auttaa syventämään näkemyksiä mobiili varastoon varatun ja käytettävissä milloin tahansa ja missä tahansa. 

<a name="prerequisites"></a>Edellytykset
-------------

| Edellytys                                                         | kuvaus                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Lue Microsoft Dynamics-365 toimintojen mobiilien | [Toimintojen mobiilien Dynamics 365](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Työvaiheiden Dynamics 365                                          | Päivitä-ympäristö, joka on Microsoft Dynamics-365-version toimintoja 1611 ja toimia ympäristön Microsoft Dynamics 3 (marraskuu-2016) |
| Hotfix-korjauksen kt 3215650                                                    | Asenna hotfix-korjaus työtilat, jotka toimitetaan Microsoft Dynamics-365, toimintojen käyttöön.                                       |
| Kannettava laite, joka on asennettu toiminnot app for Dynamics-365 | Lataa mobile app myymälä toiminnot app for Dynamics-365.                                                                           |

## <a name="introduction"></a>Johdanto
Yleensä yritysten on useita toimituksia ja useita vastaanottoja varastoon joka päivä. Näiden liikkeiden muuttaa jatkuvasti käytettävissä olevan varaston tilaa. Käytettävissä olevan varaston mobiili työtilan näet yrityksen käytettävissä olevan varaston tilasta, niin, että voit käyttää valintasi mobiililaitteen tietoja varaston uusin asuun. Riippumatta siitä, onko toimi fyysisen varastoinnin, osto, myynti, tuotanto tai hallinta, tai on muita rooleja voit käyttää käytettävissä olevan varastotietoja milloin tahansa ja missä tahansa. Mobile workspace mahdollistaa käytettävissä olevan tilan instant tutkimuksen välillä tilat, ja voit tarkastella käytettävissä oleva varasto tilat, nykyiset varaukset materiaalin ja varauksettoman käytettävissä oleva varasto. Voit myös Kirjoita kyselyn käytettävissä olevan varaston nimikenumerot ja suodatetun haun varasto-tuotteita ja vaihtoehtoja. Erityisesti mobiili työtilassa on nämä ominaisuudet:

-   Voit etsiä tuotenumero tai tuotteen nimi Etsi tuotteita tarkastella käytettävissä olevan varaston tilaa.
-   Voit tarkastella valittujen tuotteiden osalta seuraavat tiedot:
    -   Käytettävissä oleva varasto per sivusto
    -   Käytettävissä olevan varastokohtaisen määrän
    -   Käytettävissä oleva varasto sijaintia kohden
    -   Käytettävissä oleva varasto per erä (erä ohjaa tuotteita varten)
    -   Varaston tilaa kohden käytettävissä oleva varasto

<!-- -->

-   Tuotteen varastosaldo näkyy seuraavilla tavoilla:
    -   Fyysinen varasto (tämä näkymä edustaa kokonaissumma).
    -   Mukaan fyysinen varattu (tämä näkymä edustaa varattu summa.)
    -   Mukaan saatavissa oleva fyysinen (tämän näkymän edustaa käytettävissä oleva summa, joka on ei varauksia.)

## <a name="get-started"></a>Aloittaminen
Matkaviestimen aloittaminen:

1.  -Mobile app myymälä Lataa ja asenna toiminnot app for Microsoft Dynamics-365.
2.  Käynnistä sovellus laitteen.
3.  Anna URL-osoitteesi Dynamics 365.
4.  Kirjoita Kirjaudu yritys. Esimerkiksi **USMF**.
5.  Ensimmäinen kerta, kun kirjaudut sisään, sinua pyydetään käyttäjänimeä ja salasanaa Microsoft Dynamics-365, tilin toimintoja varten. Anna tunnistetietosi. Kun kirjaudut sisään, näet yrityksen käytettävissä olevat työtilat.

Voit tarkastella mobiili sovellusten työtilat, haluttu työtilat on ensin julkaistava toiminnot app for Dynamics-365.

1.  Käynnistä Dynamics 365 operaatioille.
2.  Siirry **järjestelmän hallinta**&gt;**asennus**&gt;**järjestelmäparametrit**.
3.  Valitse **hallinta mobile app**.
4.  Valitse työtila julkaista mobile platform.
5.  Valitse **julkaista työtilan**.
6.  Päivitä laitteesi on julkaistu työtilat.

## <a name="view-the-onhand-inventory-for-a-product"></a>Näytä tuotteen onhand-varasto
1.  Matkaviestimessä, valitse **käytettävissä olevan varaston** työtila.
2.  Valitse **tarkistaa käytettävissä kohteelle**. Luettelo tuotteista, jotka on ladattu sovellusten offline-käyttöä varten. Oletusarvon mukaan 50 kohteet ladataan, mutta numeroa voi muuttaa. Saat lisätietoja, lue valmiiksi käsikirja.
3.  Jos kohde ei ole luettelossa, valitse **tehdä tarkempia** online-haku Dynamics 365-toimintojen suorittamiseen. Etsiä tuotteen numero tai vaihtaa tuotteen nimen mukaan etsittäessä.
4.  Valitse tuote. Jos nimikkeellä on kuvan, kuva näkyy.
5.  Valitse jokin seuraavista vaihtoehdoista, käytettävissä oleva tila:
    -   Näytä käytettävissä oleva toimipisteissä
    -   Näytä käytettävissä oleva varasto per
    -   Näytä käytettävissä oleva sijaintia kohden
    -   Näytä käytettävissä oleva per erä (erä ohjaa tuotteita varten)
    -   Näytä käytettävissä oleva varasto tilaa kohden

    Tuotteen varastosaldo näkyy seuraavilla tavoilla:
    -   Fyysinen varasto (tämä näkymä edustaa kokonaissumma).
    -   Mukaan fyysinen varattu (tämä näkymä edustaa varattu summa.)
    -   Mukaan saatavissa oleva fyysinen (tämä näkymä edustaa käytettävissä oleva summa, joka on ei varauksia.)




