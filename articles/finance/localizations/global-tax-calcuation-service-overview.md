---
title: Verolaskentapalvelu (esiversio)
description: Tässä ohjeaiheessa selitetään verolaskentapalvelun yleinen laajuus ja ominaisuudet.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818221"
---
# <a name="tax-calculation-service-preview"></a>Verolaskentapalvelu (esiversio)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Verolaskentapalvelu on hyperskaalautuva monivuokaajapalvelu, jonka avulla Global Tax Engine voi automatisoida ja yksinkertaistaa verotuksen määritys- ja laskentaprosessia. Veromoduuli on täysin konfiguroitavissa. Määritettäviä elementtejä ovat muun muassa verotettava tietomalli, verokoodi, verojen kohdistuksen matriisi ja verolaskelmakaava. Veromoduuli toimii Microsoft Azure -ydinpalvelualustalla ja tarjoaa modernia teknologiaa ja eksponentiaalisen skaalautuvuuden.

Verolaskentapalvelu integroituu Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin kanssa. Lopulta se tulee integroitumaan myös Dynamics 365 Project Operationsiin, Dynamics 365 Commerceen ja muihin ensimmäisen ja kolmannen osapuolen sovelluksiin.

Verolaskentapalvelu on Microsoft-pohjainen veromoduuli, joka tarjoaa eksponentiaalisen skaalautuvuuden. Sen avulla voit suorittaa seuraavia tehtäviä:

- Määritä verolaskentapalvelu RCS:n (Regulatory Configuration Service) kautta. RCS on parannettu versio sähköisen raportoinnin (ER) suunnittelijasta, ja se on saatavana erillisenä palveluna.
- Määritä veromatriisi määrittämään automaattisesti verokoodit ja -prosentit.
- Määritä veromatriisi määrittämään automaattisesti verorekisteröintinumerot.
- Määritä verolaskelman suunnittelija määrittämään kaavoja ja ehtoja.
- Jaa verotuksen määritys- ja laskentaratkaisu yritysten välillä.

Jos haluat käyttää verolaskentapalvelua, asenna verolaskentapalvelun apuohjelma Microsoft Dynamics Lifecycle Services (LCS) -palvelun projektista. Viimeistele sitten RCS:n asetukset ja ota käyttöön verolaskentapalvelu Financessa ja Supply Chain Managementissa. Lisätietoja on kohdassa [Veroaplvelun käytön aloittaminen](https://go.microsoft.com/fwlink/?linkid=2138482).

## <a name="availability"></a>Käytettävyys

Veronlaskentapalvelu on käytettävissä vain eristysympäristöissä ja valituille asiakkaille julkisen esiversio-ohjelman kautta. Lopulta se tulee yleisesti kaikkien asiakkaiden saataville ja tuotantoympäristöihin.

Verolaskentapalveluun toimitetaan uusia ominaisuuksia jatkossakin. Muista siksi tarkistaa ajan tasalla oleva dokumentaatio usein, jotta opit tuettujen ominaisuuksien kattavuudesta ja laajuudesta.

Verolaskentapalvelu otetaan käyttöön seuraavilla Azuren maantieteellisillä alueilla. Se otetaan käyttöön myös useammilla Azuren maantieteellisillä alueilla asiakkaiden tarpeiden mukaan:

- Yhdysvallat
- Eurooppa
- Ranska
- Iso-Britannia

> [!NOTE]
> Veronlaskentapalvelu ei tue Dynamics 365:n paikallista käyttöönottoa. Se ei myöskään tue aiempia versioita, kuten Dynamics AX 2012 -versiota.

## <a name="feature-highlights"></a>Toiminnon tärkeimmät ominaisuudet

- Määritettävä veromatriisi, jonka avulla määritetään ja lasketaan vero automaattisesti
- Useiden arvonlisäveron rekisteröintinumeroiden tukeminen
- Siirtotilausten tuki verojen määritystä ja laskentaa varten
- Siirtotilausten tuki useiden ALV-rekisterinumeroiden määrittämiseksi

## <a name="supported-transactions"></a>Tuetut tapahtumat

Verolaskentapalvelu voidaan ottaa käyttöön yritys- ja tapahtumakohtaisesti. Seuraavia tapahtumia tuetaan:

- Myyntiprosessi

    - Myyntitarjous
    - Myyntitilaus
    - Vahvistus
    - Materiaaliluettelo
    - Pakkausluettelo
    - Myyntilasku
    - Hyvityslasku
    - Palautustilaus
    - Otsikon muu kulu
    - Rivin muu kulu

- Ostoprosessi

    - Ostotilaus
    - Vahvistus
    - Saapumisluettelo
    - Tuotteen vastaanotto
    - Ostolasku
    - Otsikon muu kulu
    - Rivin muu kulu
    - Hyvityslasku
    - Palautustilaus
    - Ostoehdotus
    - Ostoehdotuksen rivin muu kulu
    - Tarjouspyyntö
    - Tarjouspyynnön otsikon muu kulu
    - Tarjouspyynnön rivin muu kulu

- Varastoprosessi

    - Siirtotilaus – lähetä
    - Siirtotilaus – vastaanota

## <a name="related-resources"></a>Liittyvät resurssit

[Veroapalvelun käytön aloittaminen](https://go.microsoft.com/fwlink/?linkid=2138482)

[Useita ALV-rekisterinumeroita](https://go.microsoft.com/fwlink/?linkid=2153387)

[Siirtotilauksen verotoiminnon tuki](https://go.microsoft.com/fwlink/?linkid=2153388)

[Näin rakennat laajennuksen veropalveluun](https://go.microsoft.com/fwlink/?linkid=2138483)
