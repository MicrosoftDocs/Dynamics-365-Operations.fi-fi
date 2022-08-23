---
title: Moduulikirjaston yleiskatsaus
description: Tässä artikkelissa on yleiskatsaus Microsoft Dynamics 365 Commercen moduulikirjastosta.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d9dc07b3f6417c7e284c6555c2818c2a782d7683
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268943"
---
# <a name="module-library-overview"></a>Moduulikirjaston yleiskatsaus

[!include [banner](includes/banner.md)]

Tässä artikkelissa on yleiskatsaus Microsoft Dynamics 365 Commercen moduulikirjastosta.

Dynamics 365 Commercen moduulikirjasto on moduulikokoelma, jota voi käyttää sähköisen kaupankäynnin sivuston luomisessa. Moduuleilla on sekä käyttöliittymänäkökulmat että toiminnalliset näkökulmat.

Moduulikirjaston moduuleihin voi kohdistaa teemoja ja muuttaa niiden ulkoasua. Teemat käyttävät CSS-tyylisivuja (CSS). Kuvitteellisen verkkokauppasivuston, jonka nimi on Fabrikam, teema on mukana moduulikirjaston osana ja sitä voidaan käyttää viitteenä.

## <a name="module-library-modules"></a>Moduulikirjaston moduulit

Seuraavat moduulit ovat mukana moduulikirjastossa:

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
