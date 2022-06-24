---
title: Kuratoitujen suositusten manuaalinen luominen
description: Tässä artikkelissa kerrotaan, miten jälleenmyyjät voivat luoda ja hallita tuoteluetteloita Microsoft Dynamics 365 Commerce -sovelluksen asiakkaita varten.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e1a1b402165c5cb35696cf1cf6630770ad07508a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892675"
---
# <a name="manually-create-curated-recommendations"></a>Kuratoitujen suositusten manuaalinen luominen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten jälleenmyyjät voivat luoda ja hallita tuotesuosituksia Microsoft Dynamics 365 Commerce -sovelluksen asiakkaita varten.

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

![Esimerkki kuratoidusta luettelosta taustajärjestelmässä.](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä](enable-adls-environment.md)

[Tuotesuositusten ottaminen käyttöön](enable-product-recommendations.md)

[Kohdennettujen suositusten ottaminen käyttöön](personalized-recommendations.md)

[Kohdennetuista tuotesuosituksista kieltäytyminen](personalization-gdpr.md)

["Osta samankaltaisia tyylejä" -suositusten käyttöönotto](shop-similar-looks.md)

[Tuotesuositusten lisääminen myyntipisteessä](product.md)

[Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Suositusten luominen esittelytietojen avulla](product-recommendations-demo-data.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]