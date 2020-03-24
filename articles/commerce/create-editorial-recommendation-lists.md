---
title: Kuratoitujen suositusten manuaalinen luominen
description: Tässä ohje aiheessa kerrotaan, miten jälleenmyyjät voivat luoda ja hallita tuoteluetteloita Microsoft Dynamics 365 Commerce -sovelluksen asiakkaita varten.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b39ef61e7dabdd8a53d5666926a95cb7b9e6b9a5
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127718"
---
# <a name="manually-create-curated-recommendations"></a>Kuratoitujen suositusten manuaalinen luominen

[!include [banner](includes/banner.md)]

Tässä ohje aiheessa kerrotaan, miten jälleenmyyjät voivat luoda ja hallita tuotesuositusluetteloita Microsoft Dynamics 365 Commerce -sovelluksen asiakkaita varten.

Kuratoidut luettelot ovat yksittäisen sellaisen sisällön kokoelmia, jonka ihmiset ovat luoneet ja jota he kuratoivat.  

## <a name="create-a-new-list"></a>Uuden luettelon luominen

Voit luoda uuden kuratoidun tuotesuositusluettelon seuraavasti.

1. Siirry kohtaan **Retail ja Commerce &gt; Tuotesuositukset &gt; Suositusluettelot**.
1. Valitse **Uusi**.
1. Anna **Luettelon tunnus** -kenttään arvo.
1. Anna **Luettelon nimi** -kenttään arvo.
    - **Luettelon nimi** on sen luettelon otsikko, joka näkyy kuratoitujen luetteloiden osassa **Tuotekokoelma**-moduulissa.
1. Voit lisätä tuotteita luetteloon valitsemalla **Lisää tuotteita**.
1. Jos haluat muuttaa tuotteiden järjestystä luettelossa, kirjoita arvo **Näyttöjärjestys**-sarakkeeseen.
    - Jos kahdella tuotteilla on sama näyttöjärjestyksen arvo, näiden kahden tuloksen lopullinen järjestys voi poiketa taustasovelluksen järjestyksestä.
1. Tallenna luettelo valitsemalla **Tallenna**.

## <a name="example-list"></a>Esimerkkiluettelo

![Esimerkki kuratoidusta luettelosta taustatoiminnossa](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[ADLS:n käyttöönotto Dynamics 365 Commerce -ympäristössä](enable-adls-environment.md)

[Ota tuotesuositukset käyttöön](enable-product-recommendations.md)

[Ota kohdennetut suositukset käyttöön](personalized-recommendations.md)

[Kohdennetuista tuotesuosituksista kieltäytyminen](personalization-gdpr.md)

[Suositusluettelojen lisääminen sähköisen kaupankäynnin sivustoon](add-reco-list-to-page.md)

[Tuotesuositusten lisääminen myyntipisteessä](product.md)

[Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Suositusten luominen esittelytietojen avulla](product-recommendations-demo-data.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)
