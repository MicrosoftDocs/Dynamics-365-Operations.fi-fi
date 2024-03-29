---
title: Tuotesivun täydentäminen
description: Tässä artikkelissa kerrotaan, miten tuotesivua täydennetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: josaw1
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: f01dcc2518fe861339b4984522582ed3de7aa6ad
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282131"
---
# <a name="enrich-a-product-page"></a>Tuotesivun täydentäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten tuotesivua täydennetään Microsoft Dynamics 365 Commerce -sovelluksessa.

Oletusarvon mukaan sivustossa käytetään yleistä sivua tuotetietojen näyttämisessä. Tämä sivu sisältää perustiedot tuotteesta ja sen myynnissä vaadittavista ohjausobjekteista. Voit kuitenkin täydentää Commerce Scale Unitin tietoja tiettyä tuotetta koskevilla kuvilla tai tekstillä. Tätä prosessia kutsutaan tuotesivun täydentämiseksi.

Usein tuotteita varten halutaan käyttää erityistä lisäsisältöä. Kun siirryt **Retail ja Commerce**-kohtaan muokkaustyökalussa, näkyviin tulee tuoteluettelo kanavasta, joka on liitetty sivustoon. Tässä luettelossa **Täydennetty**-sarake ilmaisee, onko tuotteen tuotesivua täydennetty. Jos sarakkeessa on valintamerkki, tuotteella on täydennetty tuotesivu. Jos valintamerkkiä ei ole, tuotteella käytetään oletustuotesivua ja -sisältöä. Voit esikatsella sekä täydennettyjä että muita kuin täydennettyjä tuotesivuja valitsemalla tuotteen nimen luettelosta.

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
1. Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.
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

[Sivun sisällön helppokäyttöisyyden tarkistaminen](verify-accessibility.md)

[Dynaamisten verkkokauppasivujen luominen URL-parametrien perusteella](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
