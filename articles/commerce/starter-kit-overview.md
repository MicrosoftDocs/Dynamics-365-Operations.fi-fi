---
title: Aloituspakkauksen yleiskatsaus
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen aloituspakkauksesta.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1960e1354744fe1034783177ba331f5877d0bee7
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025899"
---
# <a name="starter-kit-overview"></a>Aloituspakkauksen yleiskatsaus


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen aloituspakkauksesta.

## <a name="overview"></a>Yleiskatsaus

Dynamics 365 Commercen aloituspakkaus on moduulikokoelma, jota voi käyttää sähköisen kaupankäynnin sivuston luomisessa. Moduuleilla on sekä käyttöliittymänäkökulmat että toiminnalliset näkökulmat.

Aloituspakkauksen moduuleihin voi kohdistaa teemoja ja muuttaa niiden ulkoasua. Teemat käyttävät CSS-tyylisivuja (CSS). Kuvitteellisen verkkokauppasivuston, jonka nimi on Fabrikam, teema on mukana aloitus pakkauksen osana ja sitä voidaan käyttää viitteenä.

## <a name="starter-kit-modules"></a>Aloituspakkausmoduulit

Seuraavat moduulit ovat mukana aloituspakkauksessa:

- **Säilömoduuli** – Säilömoduuli on yksinkertainen moduuli, joka toimii isäntänä muille moduuleille. Se ohjaa sen sisällään olevien moduulien asettelua.
- **Markkinointimoduulit** – Markkinointimoduulit sisältävät sisältölohkon, tekstilohkon, videotoistimen ja karusellimoduulit. Kaikkia näitä moduuleja voidaan käyttää sisällön esittelyyn. Ne voidaan asettaa mille tahansa sivulle. Niitä ohjaavat sisällönhallintajärjestelmän (CMS) tiedot.
- **Ylä- ja alatunnistemoduulit** Ylä- ja alatunnistemoduulit näkyvät kaikkien sivuston sivujen ylä- ja alatunnisteessa. Nämä moduulit voidaan määrittää tarpeen mukaan ominaisuuksien avulla.
- **Hakumoduulit** – Tuotteet voidaan löytää käyttämällä ylätunnisteen hakumoduulia. Hakutulokset näkyvät hakutulossivulla. Tuotteita voi etsiä myös luokkasivuilta. Ne ovat kullekin kanavan siirtymishierarkiassa tuetuille luokalle varattuja sivuja. Lisäksi muokkaajamoduuleja voi käyttää hakutulosten ja luokkasivujen lisäsuodatuksessa.
- **Tuotetietosivumoduulit** – Tuotetietosivut käyttävät useita moduuleja tuotetietojen näyttämisessä. Ostoruutumoduulin avulla asiakkaat voivat tarkastella tuotteita ja lisätä niitä ostoskoriin. Muut moduulit, kuten teknisten tietojen moduuli, näyttävät tuotetietoja. Luokitusten ja arvostelujen moduulin avulla voidaan tarkastella arvosteluja ja syöttää niitä.
- **Osta verkosta, nouda myymälästä -moduuli** – Osta verkosta, nouda myymälästä -moduuli on integroitu Bing Maps -sovelluksen kanssa. Sitä voi käyttää lähellä olevien myymälöiden etsimisessä. Asiakkaat voivat noutaa niistä ostamiaan tuotteita.
- **Ostomoduulit** – Ostomoduulit sisältävät ostoskorimoduulin, jota voi käyttää nimikkeiden lisäämisessä ostoskoriin. Kassamoduuli kerää toimitusosoitteen, toimitusvaihtoehdot ja lahjakortin, kanta-asiakasohjelman ja luottokortin tiedot tilauksen käsittelemistä varten. Kun tilaus on tehty, vahvistustiedot voidaan näyttää tilauksen vahvistuksen moduulin avulla.
- **Tilinhallintamoduulit** – Sisäänkirjautumismoduulin avulla asiakkaat voivat kirjautua sisään olemassa olevalle tilille ja rekisteröitymismoduulin avulla he voivat luoda uuden tilin. Kun tili on luotu, viimeaikaisia tilauksia voi tarkastella tilaushistoriamoduulin avulla. Tilauksen tietoja voi tarkastella tilaustietojen moduulin avulla.
- **Suositusten moduuli** – Suositukset näytetään tuotteensijoittelumoduulin avulla. Tämä moduuli tukee algoritmiluetteloita ja toimituksellisia luetteloita, jotka voidaan esitellä millä tahansa sivulla.

## <a name="additional-resources"></a>Lisäresurssit

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)
