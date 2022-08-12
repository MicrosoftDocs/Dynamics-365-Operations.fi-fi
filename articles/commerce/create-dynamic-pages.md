---
title: Dynaamisten sähköisen kaupankäynnin sivujen luominen URL-parametrien perusteella
description: Tässä artikkelissa kuvataan, kuinka määritetään Microsoft Dynamics 365 Commerce -verkkokauppasivu, joka voi tuottaa URL-parametreihin perustuvaa dynaamista sisältöä.
author: StuHarg
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.openlocfilehash: 83e20d9fc655a474a11521ec61d0b64d30603181
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169127"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>Dynaamisten sähköisen kaupankäynnin sivujen luominen URL-parametrien perusteella

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka määritetään Microsoft Dynamics 365 Commerce -verkkokauppasivu, joka voi tuottaa URL-parametreihin perustuvaa dynaamista sisältöä.

Sähköisen kaupankäyntisivun voi konfiguroida käyttämään erilaista sisältöä URL-polun segmentin perusteella. Näin ollen sivu tunnetaan dynaamisena sivuna. Segmenttiä käytetään sivun sisällön noutamisen parametrina. Esimerkiksi sivuston muodostimessa luotava sivu, jonka nimeksi tulee **blog\_viewer** siirretään URL-osoitteeksi `https://fabrikam.com/blog`. Tämän sivun avulla voidaan sitten näyttää eri sisältöä URL-polun viimeisen segmentin perusteella. Esimerkiksi URL-osoitteen `https://fabrikam.com/blog/article-1` viimeinen segmentti on **article-1**.

Voit myös ohittaa parametrisoidun URL-segmentin sivustonmuodostajasivulla. Esimerkiksi sivuston muodostimessa luotava sivu, jonka nimeksi tulee **blog\_summary** voidaan yhdistää URL-osoitteeseen `https://fabrikam.com/blog/about-this-blog`. Kun URL-osoitetta `https://fabrikam.com/blog`, jonka lopussa on segmentti `/about-this-blog`, pyydetään **blog\_summary** -sivun sisältö palautetaan sen sijaan, että `/about-this-blog`-segmentti tulkittaisiin `https://fabrikam.com/blog`-sivun käyttämäksi parametriksi. 

Kun dynaamiselle sivulle välitetyille parametreille valitaan nimiä, dynaamisen sivun nimeä, joka näkyy URL-osoitteessa (`/blog` yllä olevassa esimerkissä), ei voi käyttää parametrin nimenä tai parametrin nimen alimerkkijonona. 

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

Kun reititys on konfiguroitu, kaikki parametrisoidun URL-polun pyynnöt palauttavat tähän URL-osoitteeseen liittyvän sivun. Jos pyynnöt sisältävät lisäsegmentin, siihen liittyvä sivu palautetaan ja sivun sisältö haetaan käyttämällä segmenttiä parametrina. Esimerkiksi `https://fabrikam.com/blog/article-1` palauttaa esimerkiksi `https://fabrikam.com/blog` -sivun, jossa näkyy sisältö, joka haettiin käyttäen **/article-1**-parametria.

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
