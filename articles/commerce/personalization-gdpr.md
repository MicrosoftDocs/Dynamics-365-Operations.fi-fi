---
title: Kohdennetuista tuotesuosituksista kieltäytyminen
description: Tässä artikkelissa kerrotaan, miten voit antaa asiakkaiden kieltäytyä vastaanottamasta mukautettuja Microsoft Dynamics 365 Commerce -suosituksia.
author: bebeale
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 5d75f1ae4ec8fbccd00635d3c245a5ae7c1e1dff
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283665"
---
# <a name="opt-out-of-personalized-recommendations"></a>Kohdennetuista tuotesuosituksista kieltäytyminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten voit antaa asiakkaiden kieltäytyä vastaanottamasta mukautettuja Microsoft Dynamics 365 Commerce -suosituksia.

Tilin luonnin yhteydessä uudet asiakkaat määritetään automaattisesti vastaanottamaan mukautettuja suosituksia. Dynamics 365 Commerce tarjoaa kuitenkin useita tapoja, joilla jälleenmyyjät voivat antaa käyttäjien kieltäytyä vastaanottamasta näitä suosituksia ja rajoittaa henkilökohtaisten tietojen käsittelyä. Todennetut käyttäjät, jotka eivät halua saada mukautettuja suosituksia, eivät heti näe mukautettuja luetteloita. Lisäksi kaikki personointia varten kerätyt henkilökohtaiset tiedot poistetaan mukautetuista suositusmalleista.

Lisätietoja mukautetuista tuotesuosituksista on kohdassa [Mukautettujen suositusten ottaminen käyttöön](personalized-recommendations.md).

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a>Tapoja, joilla jälleenmyyjät voivat toteuttaa opt-out-kokemuksen

Jälleenmyyjillä on kolme tapaa toteuttaa opt-out-kokemus.

### <a name="opting-out-on-behalf-of-users"></a>Käytöstä poistaminen käyttäjien puolesta

Commerce Back Office -tilien hallinnassa jälleenmyyjät voivat jättäytyä pois käyttäjien puolesta.

1. Hae Back Office -kotisivulta **kaikki asiakkaat**.
1. Hae ja valitse asiakas ja valitse sitten **Retail**-pikavälilehti.

    ![Retail-pikavälilehti.](./media/Disablepersonalizationpart1.png)

1. Valitse **Yksityisyys**-kohdassa **Poista mukautus käytöstä** -asetukseksi **Kyllä**.

    ![Tietosuoja-asetukset.](./media/Disablepersonalizationpart2.png)

1. Valitse **Tallenna** ja sulje sivu.

### <a name="module-based-opt-out-experience"></a>Moduulipohjainen opt-out-kokemus

Vähittäiskauppiaat voivat antaa todennettujen käyttäjien jättäytyä pois yksilöllisten suositusten mukaan itse. Voit antaa tämän opt-out-käyttökokemuksen lisäämällä käyttäjän opt-out-moduulin asiakastilin profiilisivuille.

### <a name="custom-extensions"></a>Mukautetut laajennukset

Jälleenmyyjät voivat luoda omia laajennuksia, joilla hallitaan käyttäjien käyttöoikeustietoja. Lisätietoja on kohdassa [Soita Retail-palvelimen ohjelmointirajapinnalle](e-commerce-extensibility/call-retail-server-apis.md) ja [Online-kanavan laajennettavuus](e-commerce-extensibility/overview.md).

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a>Digitaalisen kopion hankkiminen yksilöllisten suositusten tiedoista todennetun käyttäjän puolesta

Asiakkaat voivat halutessaan hankkia digitaalisen kopion henkilötiedoistaan ja nähdä myös viedyn näkymän niiden suositusten tuloksista. Jos asiakas pyytää näitä tietoja, vähittäismyyjän on luotava mukautettu laajennus, joka kutsuu Retail Server -sovellusohjelmointiliittymää (API), ja kyselyt, jotka koskevat **poimintoja sinulle** -luettelon kaikkia tuloksia asiakkaan asiakastunnuksen perusteella. Tämän jälkeen tulokset voidaan viedä CSV-muodossa ja jakaa asiakkaan kanssa.

Seuraavassa esimerkissä näkyy, miten jälleenmyyjä voi suorittaa tämän tehtävän.

1. Vähittäiskauppias luo mukautetun laajennuksen henkilökohtaisten suositusten tietojen vastaanottamista varten käyttäjän puolesta. Lisätietoja moduulien luomisesta, aiemmin luotujen moduulien kloonaamiseksi, Retail Serverin API-liittymien käyttämisestä ja tietojen kutsumisesta on ohjeaiheessa [Online-kanavan laajennettavuus](e-commerce-extensibility/overview.md).
2. Mukautettu laajennus soittaa **hanki-suositukset**-ydintietotoimenpiteeseen ja välittää tarvittavat tiedot luettelon vaatimusten mukaisesti. Kun kyseessä on **poiminnat sinulle** -luettelo, tunnisteen on läpäistävä oikea luettelonimi ja asiakastunnus tietotoiminnossa.

    Yksi tapa luoda mukautettu tunniste on kloonata aiemmin luotu tuotekokoelmamoduuli, jota käytetään suositustulosten palauttamiseen. Kloonaamalla tämän olemassa olevan moduulin jälleenmyyjä voi muokata olemassa olevaa koodia ja lisätä uuden painikkeen, joka vie suositustulokset CSV-tiedostoon. Lisätietoja on kohdassa [moduulikirjaston moduulin](e-commerce-extensibility/clone-starter-module.md) ja [tuotekokoelmamoduulien](product-collection-module-overview.md) kloonaaminen.

    Lisä tietoja Retail Serverin API-kirjaston täydestä näkymästä on kohdassa [Retail Server-asiakas- ja kuluttajasovellusliittymät](dev-itpro/retail-server-customer-consumer-api.md).

3. Kun mukautettu laajennus on tehty, jälleenmyyjä voi viedä CSV-tiedoston kaikista suositusten tuloksista todennetun käyttäjän yksilöllisen asiakastunnuksen perusteella.
4. Jälleenmyyjä voi jakaa viedyn CSV-tiedoston, joka sisältää täyden mukautetun luettelon suositelluista tuotteista todennetun käyttäjän kanssa.

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä](enable-adls-environment.md)

[Ota tuotesuositukset käyttöön](enable-product-recommendations.md)

[Kohdennettujen suositusten ottaminen käyttöön](personalized-recommendations.md)

["Osta samankaltaisia tyylejä" -suositusten käyttöönotto](shop-similar-looks.md)

[Tuotesuositusten lisääminen myyntipisteessä](product.md)

[Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Kuratoitujen suositusten manuaalinen luominen](create-editorial-recommendation-lists.md)

[Suositusten luominen esittelytietojen avulla](product-recommendations-demo-data.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
