---
title: Tuotesuositusten yleiskatsaus
description: Tässä aiheessa on yleisiä tietoja tuotesuosituksista. Tuotesuositusten avulla asiakkaat löytävät helposti ja nopeasti tuotteita, joita he haluavat. He löytävät jopa tuotteita, joita he eivät alun perin aikoneet ostaa.
author: Moonma
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: abeeb3c35c21f6d7a6ec24a84522033f9a5367f3
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127856"
---
# <a name="product-recommendations-overview"></a>Tuotesuositusten yleiskatsaus

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce -sovelluksen avulla voidaan näyttää tuotesuosituksia sähköisen kaupankäynnin sivustossa ja myyntipistelaitteessa. Tuotesuositukset ovat nimikkeitä, joista asiakas voi olla kiinnostunut. Suositukset perustuvat muiden asiakkaiden ostotrendeihin verkko- ja kivijalkamyymälöissä.

Tuotesuositusten avulla asiakkaat löytävät helposti ja nopeasti tuotteita, joita he haluavat. Samalla he saavat kokemuksen hyvin toimivasta sovelluksesta. Ristiinmyyntiä ja lisämyyntiä voidaan käyttää myös autettaessa asiakkaita löytämään tuotteita, joita he eivät alun perin aikoneet ostaa. Suositusten käyttäminen tuotteiden etsimisessä voi luoda lisää muuntomahdollisuuksia, auttaa myyntituoton lisäämisessä ja jopa parantaa asiakastyytyväisyyttä ja asiakkaiden säilyttämistä.

Sähköisessä kaupankäynnissä tuotesuositukset perustuvat Microsoftin koneoppimisen teknologian perusteella laatimiin suosituksiin.

## <a name="recommendation-service"></a>Suosituspalvelu

Tuotesuositukset-palvelu hyödyntää tekoäly-ja kone opiskelu tekniikoita (AI-ML) seuraavalla tavalla:

- Tiedot muodossa, jota suosituspalvelu vaatii, saadaan Commercen toiminnallisesta tietokannasta. Tiedot lähetetään Azure Data Lake Storage -ratkaisuun (ADLS) tai yksikkösäiliöön.
- Suosituspalvelu käyttää tallennettuja tietoja suositusmallien opettamisessa **Ihmiset pitävät myös**-, **Ostetaan usein yhdessä**-, **Uudet**-, **Myydyimmät**- ja **Suositut**-luetteloissa.

## <a name="scenarios"></a>Skenaariot

Tuotesuositukset ovat käytettävissä seuraavissa skenaarioissa:

- **Millä tahansa sähköisen kaupankäynnin selaus- tai saapumissivulla:** Jos asiakkaat tai myyjät käyvät myymälän sivulla, suositusohjelma ehdottaa tuotteita **Uudet**-, **Myydyimmät**- ja **Suositut**-luetteloissa.
- **Tuotetietosivu:** Jos asiakkaat tai myyjät käyvät **tuotetietosivulla**, suositusohjelma ehdottaa lisänimikkeitä, joita saatetaan haluta ostaa. Nämä nimikkeet näkyvät myös **Ihmiset pitävät myös** -luettelossa.
- **Tapahtuma-sivu tai Kassasivu** Suositusohjelma ehdottaa nimikkeitä korin kaikkien nimikkeiden luettelon perusteella. Nämä nimikkeet näkyvät **Ostetaan usein yhdessä** -luettelossa.
- **Henkilökohtaiset suositukset:** Jälleenmyyjät voivat tarjota kirjautuneille asiakkaille henkilökohtaisen **Poimintoja sinulle** -luettelon lisäksi uusia toimintoja, jotka mahdollistavat nykyisten luetteloskenaarioiden mukauttamisen asiakkaaseen perustuen. Saat lisätietoja kohdasta [Ota kohdennetut suositukset käyttöön](personalized-recommendations.md).

### <a name="types-of-product-recommendations"></a>Tuotesuositusten tyypit

Seuraavassa taulussa on automaattisten tuotesuositusten eri tyypit, jotka ovat vähittäismyyjien käytettävissä Dynamics 365 Commerce -ratkaisun käyttöönottoa varten [tuotteen keräilymoduulissa](product-collection-module-overview.md). Vähittäismyyjät voivat myös näyttää mukautettuja tuloksia kirjautuneesta käyttäjästä, jos sivuston tekijä valitsee kyseisen vaihtoehdon.

| Tuotekokoelmamoduuli  | Laji | kuvaus |
|----------------------------|------|-------------|
| Uusi                        | Algoritmi | Tämä moduuli näyttää luettelon uusimmista tuotteista, jotka on lajiteltu kanaviin ja luetteloihin viime aikoina. |
| Myydyin               | Algoritmi | Tämä moduuli näyttää luettelon tuotteista, jotka on järjestetty suurimman myyntimäärän mukaan. |
| Suosittu                   | Algoritmi | Tämä moduuli näyttää luettelon annetun ajanjakson parhaiten menestyvistä tuotteista parhaan myynnin mukaan lajiteltuina.  |
| Ostetaan usein yhdessä | AI-ML | Tämä moduuli suosittelee luetteloa tuotteista, jotka ostetaan yleisesti yhdessä kuluttajien nykyisen ostoskorin sisällön kanssa. |
| Ihmiset pitävät myös seuraavista           | AI-ML | Tämä moduuli suosittelee tietyn alkutuotteen tuotteita kuluttajien ostotottumusten perusteella. |
| Valinnat sinulle              | AI-ML | Tämä moduuli suosittelee räätälöityjen tuotteiden luetteloa, joka perustuu kirjautuneen käyttäjän ostomalleihin. Vieraskäyttäjän luettelo on kutistettu. |

## <a name="additional-resources"></a>Lisäresurssit

[ADLS:n käyttöönotto Dynamics 365 Commerce -ympäristössä](enable-adls-environment.md)

[Ota tuotesuositukset käyttöön](enable-product-recommendations.md)

[Ota kohdennetut suositukset käyttöön](personalized-recommendations.md)

[Kohdennetuista tuotesuosituksista kieltäytyminen](personalization-gdpr.md)

[Suositusluettelojen lisääminen sähköisen kaupankäynnin sivustoon](add-reco-list-to-page.md)

[Tuotesuositusten lisääminen myyntipisteessä](product.md)

[Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Kuratoitujen suositusten manuaalinen luominen](create-editorial-recommendation-lists.md)

[Suositusten luominen esittelytietojen avulla](product-recommendations-demo-data.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)
