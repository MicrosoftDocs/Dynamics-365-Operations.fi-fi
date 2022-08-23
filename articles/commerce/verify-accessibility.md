---
title: Sivun sisällön helppokäyttöisyyden tarkistaminen
description: Tässä artikkelissa kerrotaan, miten voit varmistaa sivun sisällön helppokäyttöisyyden Microsoft Dynamics 365 Commercella.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: 686ec37f24cf68902c4dd918c0ca8aea7612e1a9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291970"
---
# <a name="verify-page-content-accessibility"></a>Sivun sisällön helppokäyttöisyyden tarkistaminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten voit varmistaa sivun sisällön helppokäyttöisyyden Microsoft Dynamics 365 Commercella.

Kun olet lopettanut sivun muuttamisen, varmista, että sisältö on kaikkien Web-sivustojen käytettävissä. Commercen luontityökalujen avulla voit helposti tarkistaa sivun sisällön helppokäyttöisyyden käyttämällä integroitua [Microsoft Accessibility Insights](https://accessibilityinsights.io/) -palvelua. Tämä palvelu varmistaa sivusi sisällön uusimpien [World Wide Web Consortium (W3C) -helppokäyttöisyysohjeiden](https://www.w3.org/standards/webdesign/accessibility) mukaisesti.

[Microsoft Accessibility Insights](https://accessibilityinsights.io/) -integroinnin on oltava käytössä vuokraajassa tai sivustotasolla, ennen kuin sitä voi käyttää.

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>Microsoftin helppokäyttöisyystietojen ottaminen käyttöön kaikissa vuokraajan sivustoissa

Voit ottaa [Microsoft helppokäyttöisyystietojen](https://accessibilityinsights.io/) -integroinnin käyttöön kaikissa vuokraajasi Commerce-sivustoissa noudattamalla seuraavia ohjeita.

> [!NOTE]
> Jotta voit käyttää vuokraajan asetuksia, sinun on oltava kirjautuneena sisään Commercen järjestelmänvalvojana.

1. Kirjaudu Commerce-järjestelmään järjestelmänvalvojana.
1. Laajenna vasemmanpuoleisessa siirtymisruudussa **vuokraajan asetukset** (hammasratassymbolin vieressä).
1. Valitse **Vuokraajan asetukset** -kohdasta **Ominaisuudet**.
1. Määritä **Helppokäyttötoiminnon tarkistus** -asetukseksi **Käytössä**.

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>Microsoftin helppokäyttötoimintotietojen ottaminen käyttöön yksittäisessä sivustossa

Voit ottaa [Microsoft helppokäyttöisyystietojen](https://accessibilityinsights.io/) -integroinnin käyttöön yhdessä Commerce-sivustossa noudattamalla seuraavia ohjeita.

1. Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).
1. Laajenna se valitsemalla vasemmasta siirtymisruudusta **Sivuston asetukset**.
1. Valitse **Sivuston asetukset** -kohdasta **Ominaisuudet**.
1. Määritä **Helppokäyttötoiminnon tarkistus** -asetukseksi **Käytössä**.

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>Kotisivun sisällön helppokäyttöisyyden tarkistaminen

Jos haluat käyttää integroitua [Microsoft helppokäyttöisyystiedot](https://accessibilityinsights.io/) -palvelua kotisivusi sisällön skannaukseen ja vahvistamiseen kaupankäynnin aikana, toimi seuraavasti.

1. Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).
1. Valitse vasemmanpuoleisessa siirtymisruudussa **Sivut**.
1. Etsi ja valitse aloitussivu, joka avataan sivueditorissa.
1. Valitse komentopalkissa **Tarkista helppokäyttöisyys**. **Tarkista helppokäyttöisyys** -sivu tulee näkyviin.
1. Kun tarkistus on valmis, tarkista raportin sisältö.
1. Jos jokin tarkistus epäonnistui, valitse jokainen epäonnistunut tarkistuskohde laajentaaksesi sitä, jotta voit nähdä lisätietoja.
1. Jos haluat sulkea raportin sen jälkeen, kun olet tarkistanut sen, vieritä **Tarkista Helppokäyttötoiminnot** -sivun alareunaan ja valitse **OK**.

## <a name="additional-resources"></a>Lisäresurssit

[Aiemmin luodun sivuston sivun muokkaaminen](modify-existing-page.md)

[Uuden sivuston sivun lisääminen](add-new-page.md)

[Sivun asettelujen valitseminen](select-page-layouts.md)

[SEO-metatietojen hallinta](manage-seo-metadata.md)

[Sivun tallentaminen, esikatseleminen ja julkaiseminen](save-preview-publish-page.md)

[Tuotesivun täydentäminen](enrich-product-page.md)

[Luokan saapumissivun täydentäminen](enrich-category-page.md)

[Dynaamisten verkkokauppasivujen luominen URL-parametrien perusteella](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
