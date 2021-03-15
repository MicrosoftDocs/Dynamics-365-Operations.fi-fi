---
title: Siirtymishaku
description: Tässä ohjeaiheessa kerrotaan, miten sivujen välillä voi siirtyä hakutoiminnon avulla.
author: aneesmsft
manager: AnnBe
ms.date: 04/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43fa263bcbb6f5a6465af59ffb744aa865d66239
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/19/2020
ms.locfileid: "4799095"
---
# <a name="navigation-search"></a>Siirtymishaku

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten sivujen välillä voi siirtyä hakutoiminnon avulla.

Sovellus sisältää useita alueita ja sivuja erilaisten tehtävien suorittamista varten. Siirtymishakutoiminnon avulla tehtävien suorittamisessa tarvittavat sivut löytyvät helposti.

Kun haluat käyttää tätä toimintoa, valitse **hakukuvake**, jolloin **hakukenttä** tukee näkyviin. Tämän jälkeen voit kirjoittaa hakukenttään yhden sanan tai useita sanoja. Järjestelmä hakee heti syöttämiäsi sanoja vastaavat sivut sovelluksesta. Jos syötä esimerkiksi sanat toimittajan lasku, järjestelmä näyttää sanoja vastaavat tulokset.

> [!NOTE]
> **Hakukentän** avulla voit etsiä sivut ja siirtyä niille. Sen avulla ei voi etsiä tiettyjä tietoja tai toimintoja.

[![hakuruutu](media/navigation-search.png "Hakuruutu")

## <a name="quickly-navigate-to-a-particular-page"></a>Siirry nopeasti tietylle sivulle

Siirtymishakutoiminnon avulla on helppo siirtyä tietylle sivulle. Esimerkiksi ostoreskontran käsittelijä, joka käyttää **Maksukirjauskansio**-sivua säännöllisesti, voi kirjoittaa **hakukenttään** maksukirjauskansio. Koska syöte on sivun otsikon tarkka vastine, sivu näkyy hakutulosten kärjessä. Näin sivulle siirtyminen tapahtuu nopeasti.

Hakutulosten luettelo sisältää sekä sivun otsikon että siirtymispolun. Tämä näyttää sivun sijainnin sovelluksessa. Toiminnon avulla pystytään myös määrittämään kahden tai useamman tulosluettelossa olevan sivun erot.

Kun sivua haetaan, syötettä ja sivun otsikkoa sekä sivun siirtymispolkua verrataan toisiinsa. Jos **hakukenttään** syötetään sana myyntireskontra, tuloksissa näkyvät myyntireskontra-alueen sivut, vaikka näiden sivujen otsikossa ei olisi sanaa myyntireskontra.

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Siirry nopeasti sivulle lomakkeen teknisen nimen perusteella

Siirtymishakutoiminto sisältää myös käyttäjien toivoman tehokäyttäjille tarkoitetun toiminnon, joka on mahdollisuus siirtyä sivulle nopeasti teknisen lomakkeen nimen avulla. Monet käyttäjät tuntevat järjestelmän ja käsittelemiensä lomakkeiden tarkat nimet hyvin. Jos olet tällainen käyttäjä, voit syöttää hakukenttään **lomake:** ja tämän jälkeen etsittävän lomakkeen nimen. Jos syötät esimerkiksi **lomake: vendinvoice**, hakutuloksissa näkyvät kaikki sivut, joiden lomakkeen nimi alkaa sanalla **vendinvoice**.

## <a name="administration-and-security"></a>Hallinta ja suojaus

Siirtymishakutoiminto esittelee hallinnan ja suojauksen näkökulmasta seuraavat sivut:

- sivut, jotka ovat käytössä nykyisessä konfiguraatiossa (konfigurointiavainten kautta)
- sivut, joiden käyttöoikeus käyttäjällä on käyttäjäroolin perusteella.

Hakutulosluettelo sisältää 10 kohdetta. Jos tuloksissa ei ole hakemaasi sivua, yritä tarkentaa tai päivittää syötettä.

## <a name="development"></a>Kehitys

Siirtymishakutoimintoa on helppo kehittää, sillä valikon vaihtoehtojen käyttöönoton ja niiden hakutuloksissa näkymisen välillä ei käytännössä ole viivettä. Valikon vaihtoehdot ovat automaattisesti haettavissa, jos ne on linkitetty siirtymisruudusta tai koontinäytöstä.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]