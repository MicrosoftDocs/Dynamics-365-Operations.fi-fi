---
title: Verolaskenta (esiversio)
description: Tässä ohjeaiheessa selitetään verolaskentamahdollisuuden yleinen laajuus ja ominaisuudet.
author: wangchen
ms.date: 04/12/2021
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
ms.openlocfilehash: 3df952e0632807e55f176e63dc2047be5e622ec2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892346"
---
# <a name="tax-calculation-preview"></a>Verolaskenta (esiversio)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Verolaskenta on hyperskaalautuva monivuokaajapalvelu, jonka avulla Global Tax Engine voi automatisoida ja yksinkertaistaa verotuksen määritys- ja laskentaprosessia. Veromoduuli on täysin konfiguroitavissa. Määritettäviä elementtejä ovat muun muassa verotettava tietomalli, verokoodi, verojen kohdistuksen matriisi ja verolaskelmakaava. Veromoduuli toimii Microsoft Azure -ydinpalvelualustalla ja tarjoaa modernia teknologiaa ja eksponentiaalisen skaalautuvuuden.

Verolaskenta integroituu Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin kanssa. Lopulta se tulee integroitumaan myös Dynamics 365 Project Operationsiin, Dynamics 365 Commerceen ja muihin ensimmäisen ja kolmannen osapuolen sovelluksiin.

Verolaskenta on mikropalvelupohjainen veromoduuli, joka tarjoaa eksponentiaalisen skaalautuvuuden. Sen avulla voit suorittaa seuraavia tehtäviä:

- Määritä verolaskenta RCS:n (Regulatory Configuration Service) kautta. RCS on parannettu versio sähköisen raportoinnin (ER) suunnittelijasta, ja se on saatavana erillisenä palveluna.
- Määritä veromatriisi määrittämään automaattisesti verokoodit ja -prosentit.
- Määritä veromatriisi määrittämään automaattisesti verorekisteröintinumerot.
- Määritä verolaskelman suunnittelija määrittämään kaavoja ja ehtoja.
- Jaa verotuksen määritys- ja laskentaratkaisu yritysten välillä.

Jos haluat käyttää verolaskentapalvelua, asenna verolaskentapalvelun apuohjelma Microsoft Dynamics Lifecycle Services (LCS) -palvelun projektista. Viimeistele sitten RCS:n asetukset ja ota käyttöön verolaskentapalvelu Financessa ja Supply Chain Managementissa. Lisätietoja on kohdassa [Veroaplvelun käytön aloittaminen](./global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Käytettävyys

Verolaskenta on käytettävissä vain eristysympäristöissä ja valituille asiakkaille julkisen esiversio-ohjelman kautta. Lopulta se tulee yleisesti kaikkien asiakkaiden saataville ja tuotantoympäristöihin.

Uusia ominaisuuksia julkaistaan jatkuvasti, joten tarkista ajan tasalla oleva dokumentaatio usein, jotta opit tuettujen ominaisuuksien kattavuudesta ja laajuudesta.

Verolaskenta otetaan käyttöön seuraavilla Azuren maantieteellisillä alueilla. Se otetaan käyttöön myös useammilla Azuren maantieteellisillä alueilla asiakkaiden tarpeiden mukaan:

- Yhdysvallat
- Eurooppa

> [!NOTE]
> Veronlaskenta ei tue Dynamics 365:n paikallista käyttöönottoa. Se ei myöskään tue aiempia versioita, kuten Dynamics AX 2012 -versiota.

## <a name="feature-highlights"></a>Toiminnon tärkeimmät ominaisuudet

- Määritettävä veromatriisi, jonka avulla määritetään ja lasketaan vero automaattisesti
- Useiden veron rekisteröintinumeroiden tukeminen
- Siirtotilausten tuki verojen määritystä ja laskentaa varten
- Siirtotilausten tuki useiden verorekisterinumeroiden määrittämiseksi

## <a name="supported-transactions"></a>Tuetut tapahtumat

Verolaskenta voidaan ottaa käyttöön yritys- ja tapahtumakohtaisesti. Seuraavia tapahtumia tuetaan:

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

[Veroapalvelun käytön aloittaminen](./global-get-started-with-tax-calculation-service.md)

[Useita ALV-rekisterinumeroita](./emea-multiple-vat-registration-numbers.md)

[Siirtotilauksen verotoiminnon tuki](./tasks/tax-feature-support-for-transfer-order.md)

[Näin rakennat laajennuksen veropalveluun](./tax-service-add-data-fields-tax-integration-by-extension.md)