---
title: Dynaamisten sähköisen kaupankäynnin sivujen luominen URL-parametrien perusteella
description: Tässä aiheessa kuvataan, kuinka määritetään Microsoft Dynamics 365 Commerce -verkkokauppasivu, joka voi tuottaa URL-parametreihin perustuvaa dynaamista sisältöä.
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d6b4756fc81dc99786da251d5d9a575a71ccc49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208012"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>Dynaamisten sähköisen kaupankäynnin sivujen luominen URL-parametrien perusteella

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä aiheessa kuvataan, kuinka määritetään Microsoft Dynamics 365 Commerce -verkkokauppasivu, joka voi tuottaa URL-parametreihin perustuvaa dynaamista sisältöä.

Sähköisen kaupankäyntisivun voi konfiguroida käyttämään erilaista sisältöä URL-polun segmentin perusteella. Näin ollen sivu tunnetaan dynaamisena sivuna. Segmenttiä käytetään sivun sisällön noutamisen parametrina. Voit luoda esimerkiksi sivun, jonka nimi on **blog\_viewer**, ja se liitetään URL-osoitteeseen `https://fabrikam.com/blog`. Tämän sivun avulla voidaan sitten näyttää eri sisältöä URL-polun viimeisen segmentin perusteella. Esimerkiksi URL-osoitteen `https://fabrikam.com/blog/article-1` viimeinen segmentti on **article-1**.

Erilliset dynaamisen sivun ohittavat mukautetut sivut voidaan liittää myös URL-polun segmentteihin. Voit luoda esimerkiksi sivun, jonka nimi on **blog\_summary**, ja se liitetään URL-osoitteeseen `https://fabrikam.com/blog/about-this-blog`. Kun tämä URL-osoite on pyydetty, palautetaan **blog\_summary** -sivu, joka liittyy **/about-this-blog** -parametriin, sen sijaan että palautettaisiin **blog\_viewer** -sivu.

> [!NOTE]
> Dynaamisen sivusisällön isännöinti-, noutaminen- ja näyttämistoiminnot toteutetaan mukautetulla moduulilla. Lisätietoja on ohjeaiheessa [Online-kanavan laajennettavuus](e-commerce-extensibility/overview.md).

## <a name="set-up-a-dynamic-e-commerce-page"></a>Dynaamisen verkkokauppasivun määrittäminen

Voit määrittää dynaamisen sähköisen kaupankäynnin sivun luomalla dynaamisen sivun, luomalla perus-URL-osoitteen ja määrittämällä reitityksen dynaamiselle sivulle.

### <a name="create-the-page-that-will-serve-dynamic-content"></a>Dynaamista sisältöä tarjoavan sivun luominen

Voit luoda dynaamista sisältöä tuottavan sivun noudattamalla ohjeita: [Uuden sivuston sivun lisääminen](add-new-page.md). Luotava sivu edellyttää, että käytössä on moduuli, joka käyttää URL-polun viimeistä segmenttiä ulkoisen tietolähteen sisällön hakemiseen. Lisätietoja mukautetusta moduulien kehittämisestä on kohdassa [Online-kanavan laajennettavuus](e-commerce-extensibility/overview.md).

### <a name="create-the-base-url-for-the-dynamic-page"></a>Luo dynaamisen sivun perus-URL-osoite

Luo dynaamiselle sivulle perus-URL-osoite Commercen sivustonmuodostimessa noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **URL-osoitteet** ja valitse **Uusi \> Uusi URL-osoite**.
1. Valitse **Luo uusi URL-osoite** -valintaikkunasta **Sisäinen sivu**. Kirjoita **URL-polku**-kohdassa polku, jota käytetään dynaamisen sivun juuripolkuna (tässä esimerkissä **/blog**). Valitse sitten **Seuraava**.
1. Valitse **Valitse sivu** -valintaikkunassa sivu, jonka loit aiemmin dynaamiseksi sivuksi ja valitse sitten **Tallenna**.
1. Valitse **Julkaise**.

### <a name="configure-the-route-to-the-dynamic-page"></a>Reitityksen konfiguroiminen dynaamiselle sivulle

Määritä dynaamiselle sivulle reititys Commercen sivustonmuodostimessa noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Sivuston asetukset \> Laajennukset**.
1. Valitse kohdassa **Parametrisoidut URL-polut** **Lisää** ja kirjoita sitten URL-osoitteen luomisen yhteydessä syötetty URL-polku (tässä esimerkissä **/blog**).
1. Valitse **Tallenna ja julkaise**.

Kun reititys on konfiguroitu, kaikki parametrisoidun URL-polun pyynnöt palauttavat tähän URL-osoitteeseen liittyvän sivun. Jos pyynnöt sisältävät lisäsegmentin, siihen liittyvä sivu palautetaan ja sivun sisältö haetaan käyttämällä segmenttiä parametrina. Esimerkiksi `https://fabrikam.com/blog/article-1` palauttaa esimerkiksi **blog\_summary** -sivun ja sivun sisältö haetaan käyttämällä **/article-1**-parametria.

## <a name="override-a-parameterized-url-with-a-custom-page"></a>Parametriswoidun URL-osoitteen ohittaminen mukautetulla sivulla

Noudattamalla seuraavia ohjeita voit ohittaa parametrisoidun URL-osoitteen mukautetulla sivulla Commercen sivustonmuodostimen avulla.

1. Siirry kohtaan **URL-osoitteet** ja valitse **Uusi \> Uusi URL-osoite**.
1. Valitse **Luo uusi URL-osoite** -valintaikkunasta **Sisäinen sivu**. Kirjoita **URL-polku**-kohdassa polku, joka sisältää ohitettavan segmentin (tässä esimerkissä **/blog/about-this-blog**). Valitse sitten **Seuraava**.
1. Valitse mukautettu sivu **Valitse sivu** -valintaikkunasta ja valitse sitten **Tallenna**.
1. Valitse **Julkaise**.
1. Jos mukautettua sivua ei ole vielä julkaisuttu, siirry kohtaan **Sivut**, valitse mukautettu sivu ja valitse sitten **Julkaise**.

Kun mukautettu sivu on julkaistu, se tarjotaan sen sijaan, että tarjottaisiin dynaaminen sivu, jolla on parametrisoitua sisältöä.

## <a name="additional-resources"></a>Lisäresurssit

[Aiemmin luodun sivuston sivun muokkaaminen](modify-existing-page.md)

[Uuden sivuston sivun lisääminen](add-new-page.md)

[Sivun asettelujen valitseminen](select-page-layouts.md)

[SEO-metatietojen hallinta](manage-seo-metadata.md)

[Sivun tallentaminen, esikatseleminen ja julkaiseminen](save-preview-publish-page.md)

[Tuotesivun täydentäminen](enrich-product-page.md)

[Luokan saapumissivun täydentäminen](enrich-category-page.md)

[Sivun sisällön helppokäyttöisyyden tarkistaminen](verify-accessibility.md)

[Online-kanavan laajennettavuus](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]