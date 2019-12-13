---
title: Tuotesivun täydentäminen
description: Tässä ohjeaiheessa kerrotaan, miten tuotesivua täydennetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ef9e65b2027a41ca152afaf20ac2fb9a69cd9b96
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698139"
---
# <a name="enrich-a-product-page"></a>Tuotesivun täydentäminen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten tuotesivua täydennetään Microsoft Dynamics 365 Commerce -sovelluksessa.

## <a name="overview"></a>Yleiskatsaus

Oletusarvon mukaan sivustossa käytetään yleistä sivua tuotetietojen näyttämisessä. Tämä sivu sisältää perustiedot tuotteesta ja sen myynnissä vaadittavista ohjausobjekteista. Voit kuitenkin täydentää vähittäismyyntipalvelimen tietoja tiettyä tuotetta koskevilla kuvilla tai tekstillä. Tätä prosessia kutsutaan tuotesivun täydentämiseksi.

Usein tuotteita varten halutaan käyttää erityistä lisäsisältöä. Kun siirryt **Vähittäismyynti**-kohtaan muokkaustyökalussa, näkyviin tulee tuoteluettelo kanavasta, joka on liitetty sivustoon. Tässä luettelossa **Täydennetty**-sarake ilmaisee, onko tuotteen tuotesivua täydennetty. Jos sarakkeessa on valintamerkki, tuotteella on täydennetty tuotesivu. Jos valintamerkkiä ei ole, tuotteella käytetään oletustuotesivua ja -sisältöä. Voit esikatsella sekä täydennettyjä että muita kuin täydennettyjä tuotesivuja valitsemalla tuotteen nimen luettelosta.

## <a name="enrich-a-product-page"></a>Tuotesivun täydentäminen

Voit täydentää tuotesivua noudattamalla seuraavia ohjeita.

1. Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).
1. Valitse vasemmanpuoleisessa siirtymisruudussa **Tuotteet**.
1. Valitse mikä tahansa tuote, jolla ei ole täydennettyä tuotesivua.
1. Valitse toimintoruudussa **Täydennä tuotesivua**.
1. Valitse **PDP-malli** ja valitse sitten **OK**.
1. Laajenna sivun vasemmanpuoleisen jäsennyspuun **pääpaikka**.
1. Valitse kolmen pisteen painike (**...**) **pääpaikalle** ja valitse sitten **Lisää moduuli**.
1. Valitse **Säilö 2** ja valitse sitten **OK**.
1. Valitse paikan kolmen pisteen painike **säilölle 2** ja valitse sitten **Lisää moduuli**.
1. Valitse **Ominaisuus** ja valitse sitten **OK**.
1. Syötä oikealla olevassa ominaisuusruudussa **RTF**-kenttään tuotteen päivitetty kuvaus.
1. Syötä **Otsikko**-kenttään otsikkoteksti ja valitse sitten **OK**.
1. Valitse ensin **Tallenna** ja sitten **Kirjaa sisään**.
1. Syötä **Kommentit**-kenttään **Täydennä tuotetta** ja valitse **OK**.
1. Esikatsele täydennettyä tuotesivua valitsemalla **Esikatsele**. Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.
1. Valitse **Julkaise**.

## <a name="additional-resources"></a>Lisäresurssit

[Aiemmin luodun sivuston sivun muokkaaminen](modify-existing-page.md)

[Uuden sivuston sivun lisääminen](add-new-page.md)

[Sivun asettelujen valitseminen](select-page-layouts.md)

[SEO-metatietojen hallinta](manage-seo-metadata.md)

[Sivun tallentaminen, esikatseleminen ja julkaiseminen](save-preview-publish-page.md)

[Luokan saapumissivun täydentäminen](enrich-category-page.md)

