---
title: Tuotesuositusten yleiskatsaus
description: Tässä aiheessa on yleisiä tietoja tuotesuosituksista. Tuotesuositusten avulla asiakkaat löytävät helposti ja nopeasti tuotteita, joita he haluavat. He löytävät jopa tuotteita, joita he eivät alun perin aikoneet ostaa.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024976"
---
# <a name="product-recommendations-overview"></a>Tuotesuositusten yleiskatsaus

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce -sovelluksen avulla voidaan näyttää tuotesuosituksia sähköisen kaupankäynnin sivustossa ja myyntipistelaitteessa. Tuotesuositukset ovat nimikkeitä, joista asiakas voi olla kiinnostunut. Suositukset perustuvat muiden asiakkaiden ostotrendeihin verkko- ja kivijalkamyymälöissä.

Tuotesuositusten avulla asiakkaat löytävät helposti ja nopeasti tuotteita, joita he haluavat. Samalla he saavat kokemuksen hyvin toimivasta sovelluksesta. Ristiinmyyntiä ja lisämyyntiä voidaan käyttää myös autettaessa asiakkaita löytämään tuotteita, joita he eivät alun perin aikoneet ostaa. Suositusten käyttäminen tuotteiden etsimisessä voi luoda lisää muuntomahdollisuuksia, auttaa myyntituoton lisäämisessä ja jopa parantaa asiakastyytyväisyyttä ja asiakkaiden säilyttämistä.

Commercessa tuotesuositukset perustuvat Microsoftin koneoppimisen teknologian perusteella laatimiin suosituksiin.


## <a name="scenarios"></a>Skenaariot

Tuotesuositukset ovat käytettävissä seuraavissa skenaarioissa:

- **Millä tahansa sähköisen kaupankäynnin selaus- tai saapumissivulla:** Jos asiakkaat tai myyjät käyvät myymälän sivulla, suositusohjelma ehdottaa tuotteita **Uudet**-, **Myydyimmät**- ja **Suositut**-luetteloissa.
- **Tuotetietosivu:** Jos asiakkaat tai myyjät käyvät **tuotetietosivulla**, suositusohjelma ehdottaa lisänimikkeitä, joita saatetaan haluta ostaa. Nämä nimikkeet näkyvät myös **Ihmiset pitävät myös** -luettelossa.
- **Tapahtuma-sivu tai Kassasivu** Suositusohjelma ehdottaa nimikkeitä korin kaikkien nimikkeiden luettelon perusteella. Nämä nimikkeet näkyvät **Ostetaan usein yhdessä** -luettelossa.
- **Henkilökohtaiset suositukset:** Jälleenmyyjät voivat tarjota kirjautuneille asiakkaille henkilökohtaisen **Poimintoja sinulle** -luettelon lisäksi uusia toimintoja, jotka mahdollistavat nykyisten luetteloskenaarioiden mukauttamisen asiakkaaseen perustuen. Lisätietoja on kohdassa ominaisuusdokumentaatio: [Ota käyttöön mukautetut suositukset.](personalized-recommendations.md)

## <a name="recommendation-service"></a>Suosituspalvelu

Tuotesuositukset käyttävät Suositukset-koneoppimisteknologiaa seuraavasti:

- Tiedot muodossa, jota suosituspalvelu vaatii, saadaan Commercen toiminnallisesta tietokannasta. Tiedot lähetetään entiteettimyymälään.
- Suosituspalvelu käyttää tietoja suositusmallien opettamisessa **Ihmiset pitävät myös**-, **Ostetaan usein yhdessä**-, **Uudet**-, **Myydyimmät**- ja **Suositut**-luetteloissa.

## <a name="additional-resources"></a>Lisäresurssit

[Ota tuotesuositukset käyttöön](enable-product-recommendations.md)

[Ota käyttöön kohdennetut tuotesuositukset](personalized-recommendations.md)

[Tuotekokoelmamoduulin yleiskuvaus](product-collection-module-overview.md)

[Luo kuratoituja tuotesuositusluetteloita](create-editorial-recommendation-lists.md)

[Hallitse AI-ML-pohjaisia tuotesuositustuloksia](modify-product-recommendation-results.md)

[Tuotesuositusluetteloiden lisääminen sivuille](add-reco-list-to-page.md)
