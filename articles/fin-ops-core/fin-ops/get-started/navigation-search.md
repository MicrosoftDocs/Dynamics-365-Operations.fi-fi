---
title: Siirtymishaku
description: Tässä artikkelissa kerrotaan, miten sivujen välillä voi siirtyä hakutoiminnon avulla.
author: jasongre
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.openlocfilehash: 4c362e4cd83f926e7e21d775abd24ae6ddfcbbed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292334"
---
# <a name="navigation-search"></a>Siirtymishaku

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Tässä artikkelissa kerrotaan, miten sivujen välillä voi siirtyä hakutoiminnon avulla.

Sovellus sisältää useita alueita ja sivuja erilaisten tehtävien suorittamista varten. Siirtymishakutoiminnon avulla tehtävien suorittamisessa tarvittavat sivut löytyvät helposti.

Kun haluat käyttää tätä toimintoa, valitse **hakukuvake**, jolloin **hakukenttä** tukee näkyviin. Tämän jälkeen voit kirjoittaa hakukenttään yhden sanan tai useita sanoja. Järjestelmä hakee heti syöttämiäsi sanoja vastaavat sivut sovelluksesta. Jos syötä esimerkiksi sanat toimittajan lasku, järjestelmä näyttää sanoja vastaavat tulokset.

> [!NOTE]
> **Hakukentän** avulla voit etsiä sivut ja siirtyä niille. Sen avulla ei voi etsiä tiettyjä tietoja tai toimintoja.

![hakuruutu](media/navigation-search.png "Hakuruutu")

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
