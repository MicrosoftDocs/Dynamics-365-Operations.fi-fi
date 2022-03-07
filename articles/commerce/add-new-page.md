---
title: Uuden sivuston sivun lisääminen
description: Tässä ohjeaiheessa kerrotaan, miten uusi sivu lisätään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: psimolin
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e0c2a73ae9e85cb299e7cb6fc70562659cdfadc5
ms.sourcegitcommit: 1eef00796f7c5511f432b01800cdf8920992d7d5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2022
ms.locfileid: "8090716"
---
# <a name="add-a-new-site-page"></a>Uuden sivuston sivun lisääminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten uusi sivu lisätään Microsoft Dynamics 365 Commerce -sovelluksessa.

Kun olet luonut sivustoon malleja ja osia, seuraava vaihe on luoda sivuja, jotka käyttävät malleja ja osia. Valitse ensin malli tai asettelu, sivun nimi ja sivun URL-osoite.

## <a name="template-or-layout"></a>Malli tai asettelu

Voit käyttää uudella sivulla mallia tai asettelua. Lisätietoja on kohdassa [Mallien ja asettelujen yleiskatsaus](templates-layouts-overview.md).

## <a name="specify-the-page-name"></a>Määritä sivun nimi

Sivun nimen on oltava yksilöllinen sivustossa ja sen on oltava kuvaava, jotta voit löytää sen helposti ja muut tietävät, mitä varten sivu on tarkoitettu. Voit nimetä sivun myöhemmin uudelleen muokkaamalla sivua ja valitsemalla sitten kynäsymbolin ominaisuusruudussa sivun nimen vierestä.

## <a name="specify-the-page-url"></a>Määritä sivun URL-osoite

Voit määrittää uuden sivun URL-osoitteen. Kun luot sivun, voit kirjoittaa merkkijonon, jota käytetään täydellisen URL-osoitteen määrittämiseen. Tämä merkkijono on suhteellinen URL-osoite tai URL-osoitteen kuvaava osa. Koko URL-osoite muodostetaan URL-osoitteen kuvaavan osan perusteella. Uusi sivu liitetään siihen. Voit muuttaa URL-osoitteen kuvaavaa osaa myöhemmin ennen sivun julkaisemista. Lisätietoja on kohdassa [Sivun URL-osoitteen luominen](create-page-URL.md).

> [!NOTE]
> Dynamics 365 Commerce irrottaa URL-osoitteet ja sisällön. Toisin sanoen voidaan luoda situ, jota ei ole liitetty URL-osoitteeseen. Samoin voidaan luoda URL-osoite, jota ei ole liitetty sivuun. Tämän vuoksi sisällön vaihtamisen voi tehdä URL-osoitteelle, eikä siitä seuraa käyttökatkoksia. Uudelleenohjauksia on myös helppo hallita.

## <a name="add-a-new-page"></a>Uuden sivun lisääminen

Voit lisätä sivustoon uuden sivuston sivun seuraavasti.

1. Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).
1. Valitse **Uusi sivu**.
1. Valitse **Uusi sivu** -valintaikkunassa malli ja valitse sitten **OK**.
1. Anna **Sivun nimi** -kenttään sivun nimi (esimerkiksi **Oma uusi sivu**).
1. Anna **URL-osoite**-kenttään merkkijono (URL-osoitteen kuvaava osa) ja tee URL-osoite valmiiksi (esimerkiksi **omauusisivu**).
1. Valitse **OK**. Sivueditori avautuu. Huomaa, että ylä- ja alatunniste lisätään sivulle automaattisesti valitsemasi mallin perusteella.
1. Valitse sivun jäsennyksessä **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Säilö** ja valitse sitten **OK**
1. Valitse **Nestesäilö**. Valitse kolmen pisteen painike ja valitse sitten **Lisää moduuli**.
1. Valitse **Sisällöntäyteinen lohko** ja valitse sitten **OK**.
1. Valitse **Sisällöntäyteinen lohko**. Valitse kolmen pisteen painike ja valitse sitten **Lisää moduuli**.
1. Valitse **Sisällöntäyteinen lohkonimike** ja valitse sitten **OK**.
1. Valitse oikeanpuoleisessa ominaisuusruudussa **Kappale** ja kirjoita kenttään **Oma tekstiteksti**.
1. Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.
1. Syötä **Kommentit**-kenttään **Lisätty uusi sivu** ja valitse **OK**.
1. Esikatsele sivua valitsemalla **Esikatsele**. Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.
1. Valitse **Julkaise**.
1. Valitse siirtymispolussa (navigointilinkit) **Fabrikam** (tai sivuston nimi).
1. Valitse vasemmanpuoleisessa siirtymisruudussa **URL-osoitteet**.
1. Etsi ja valitse oma URL-osoite (**omauusisivu**) luettelosta.
1. Valitse **Julkaise**.

## <a name="additional-resources"></a>Lisäresurssit

[Aiemmin luodun sivuston sivun muokkaaminen](modify-existing-page.md)

[Sivun asettelujen valitseminen](select-page-layouts.md)

[SEO-metatietojen hallinta](manage-seo-metadata.md)

[Sivun tallentaminen, esikatseleminen ja julkaiseminen](save-preview-publish-page.md)

[Tuotesivun täydentäminen](enrich-product-page.md)

[Luokan saapumissivun täydentäminen](enrich-category-page.md)

[Sivun sisällön helppokäyttöisyyden tarkistaminen](verify-accessibility.md)

[Dynaamisten verkkokauppasivujen luominen URL-parametrien perusteella](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
