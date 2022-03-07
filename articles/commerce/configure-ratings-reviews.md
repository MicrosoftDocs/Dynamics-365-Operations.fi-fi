---
title: Määritä luokitukset ja arvostelut
description: Tässä ohjeaiheessa kerrotaan, miten sähköisen kaupankäynnin sivusto määritetään niin, että se näyttää asiakasluokituksia ja -arvostelut Microsoft Dynamics 365 Commerce -sovelluksessa.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e3f9ff4b0654ec5fa7548ac62e16ae64f44383e7
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968099"
---
# <a name="configure-ratings-and-reviews"></a>Määritä luokitukset ja arvostelut

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten sähköisen kaupankäynnin sivusto määritetään niin, että se näyttää asiakasluokituksia ja -arvostelut Microsoft Dynamics 365 Commerce -sovelluksessa.

Sähköisen kaupankäynnin sivustojen luokitukset ja arvostelut auttavat asiakkaita saamaan tietoja tuotteista ennen ostopäätöksen tekemistä. NIiden avulla saadaan selville, mitä muut asiakkaat ajattelevat kyseisistä tuotteista. Sähköisen kaupankäynnin sivustoissa luokitukset ja arvostelut ovat myös keino, jolla kerätään asiakaspalautetta tuotteista. 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Sivuston määrittäminen niin, että se näyttää luokitukset ja arvostelut

Luokitusten ja arvostelujen määrityksen arvot, kuten vuokraajan tunnus, arvostelun tekstin pituus ja luokituksen otsikon pituus, määritetään sivustotasolla. 

Voit määrittää sivuston näyttämään luokitukset ja arvostelut seuraavasti. 

1. Siirry kohtaan **Aloitus \> Sivustot**.
1. Valitse sivuston nimi. 
1. Siirry kohtaan **Sivuston asetukset \> Laajennukset**. 
1. Syötä **Arvostelun tekstin enimmäispituus** -kenttään arvostelun tekstin merkkien enimmäismäärä (esimerkiksi **1 000**). 
1. Syötä **Arvostelun otsikon enimmäispituus** -kenttään arvostelun otsikoiden merkkien enimmäismäärä (esimerkiksi **55**). 
1. Valitse **Tallenna ja julkaise**. 

Seuraava kuva osoittaa, miltä tämä määritys näyttää Dynamics 365 Commerce -sovelluksessa.

![Sivuston määrittäminen niin, että se näyttää luokitukset ja arvostelut.](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Tuoteluokituksen linkittäminen PDP:n Arvostelut-osaan

Tuoteluokitus näkyy PDP:n yläosassa olevan tuotteen otsikon alla. Tuoteluokitus voidaan määrittää niin, että se on linkitetty saman PDP:n **Arvostelut**-osaan. 

Voit linkittää tuoteluokituksen PDP:n osan **Arvostelut**-osaan seuraavasti.

1. Avaa PDP-malli. 
1. Siirry kohtaan **Ostoruudun säilömoduulin asetukset**.
1. Valitse **Ostoruutu**-kohdassa **Tuoteluokitukset** ja valitse sitten **Linkitä napsautus täydellisten arviointien moduuliin** -valintaruutu.

Seuraava kuva osoittaa, miltä tämä määritys näyttää Dynamics 365 Commerce -sovelluksessa.

![Tuoteluokituksen linkittäminen PDP-sivun Arvostelut-osaan.](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Tietosuoja- ja käytäntösivun linkin määrittäminen

Voit määrittää tietosuoja- ja käytäntösivun linkin seuraavasti.

1. Siirry kohtaan **Aloitus \> Sivustot**.
1. Valitse sivuston nimi. 
1. Siirry kohtaan **Sivuston asetukset \> Laajennukset**.
1. Valitse **Reitit**-välilehdessä **RNR - tietosuoja ja käytäntö** -kohdassa **Lisää linkki**. Jos linkki on jo syötetty ja haluat korvata sen, valitse linkki. 
1. Valitse **Lisää linkki** -valintaikkunassa tietosuoja-ja käytäntösivun linkki ja valitse sitten **OK**. 
1. Valitse **Tallenna ja julkaise**. 

Seuraava kuva osoittaa, miltä tämä määritys näyttää Dynamics 365 Commerce -sovelluksessa.

![Tietosuoja- ja käytäntösivun linkin määrittäminen.](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>Luokitus- ja arvostelumoduulien määrittäminen tuotetietojen sivuilla

Lisätietoja luokitus- ja arvostelumoduulien määrittämisestä tuotetietojen sivuilla on kohdassa [Luokitus- ja arvostelumoduulit](ratings-reviews-modules.md).

## <a name="additional-resources"></a>Lisäresurssit

[Luokitukset ja arvostelut – yleiskatsaus](ratings-reviews-overview.md)

[Luokitusten ja arvostelujen käytön hyväksyminen](opt-in-ratings-reviews.md)

[Hallitse luokituksia ja arvosteluja](manage-reviews.md)

[Tuoteluokitusten synkronoiminen Dynamics 365 Retailissa](sync-product-ratings.md)

[Salli valvojan julkaista luokituksia ja arvosteluja manuaalisesti](manual-publish-rating-reviews.md)

[Luokitusten ja arvostelujen tuominen ja vieminen](import-export-reviews.md)

[Palvelujen välisen todennuksen määrittäminen](service-to-service-auth.md)

[Luokitusten ja arvostelujen usein kysytyt kysymykset](ratings-reviews-faq.md)

[Luokitusten ja arvosteluiden moduulit](ratings-reviews-modules.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
