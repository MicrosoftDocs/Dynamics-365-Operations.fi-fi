---
title: Ota tuotesuositukset käyttöön
description: Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten.
author: bebeale
ms.date: 08/18/2020
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 873266405638cd277eb748ad7e966ba8a4976b13
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019856"
---
# <a name="enable-product-recommendations"></a>Ota tuotesuositukset käyttöön

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten. Lisätietoja tuotesuositusten luetteloista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Suositusten esitarkistus

Ota huomioon ennen käyttöönottoa, että tuotesuosituksia tuetaan vain Commerce-asiakkaille, jotka ovat siirtäneet tallennustilansa Azure Data Lake Storagea käyttäen. 

Seuraavat kokoonpanot on otettava käyttöön taustajärjestelmässä ennen suositusten käyttöönottoa:

1. Varmista, että Azure Data Lake Storage on ostettu ja todennettu onnistuneesti ympäristössä. Katso lisätietoja kohdasta [Varmista, että Azure Data Lake Storage on ostettu ja todennettu onnistuneesti ympäristössä](enable-ADLS-environment.md).
2. Varmista, että yksikkösäilön päivitys on automatisoitu. Lisätietoja on kohdassa [Varmista, että yksikkösäilön päivitys on automatisoitu](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
3. Vahvista, että Azure AD -käyttäjätietojen määritys sisältää suositusten merkinnän. Lisätietoja tästä toiminnosta alla.

Varmista myös, että RetailSale-mittarit on otettu käyttöön. Lisätietoja tästä määritysprosessista on kohdassa [Mittayksiköiden käsitteleminen](/dynamics365/ai/customer-insights/pm-measures).

## <a name="azure-ad-identity-configuration"></a>Azure AD -tunnisteen konfiguraatio

Tämä vaihe on pakollinen kaikille asiakkaille, jotka käyttävät infrastruktuuria palvelun (IaaS) määrityksenä. Jos asiakas käyttää Service fabric (SF) -palvelua, tämän vaiheen tulisi olla automaattinen ja suosittelemme, että asetus määritetään odotetulla tavalla.

### <a name="setup"></a>Määritys

1. Etsi taustaohjelmistosta **Azure Active Directory -sovellukset** -sivu.
2. Tarkista, onko "RecommendationSystemApplication-1"-merkintää olemassa.

Jos tapahtumaa ei ole olemassa, lisää uusi tietue, jossa on seuraavat tiedot:

- **Asiakastunnus** - d37b07e8-dd1c-4514-835d-8b918e6f9727
- **Nimi** - RecommendationSystemApplication-1
- **Käyttäjätunnus** - RetailServiceAccount

Tallenna ja sulje sivu. 

## <a name="turn-on-recommendations"></a>Suositusten ottaminen käyttöön

Voit ottaa tuotesuositukset käyttöön noudattamalla seuraavia ohjeita.

1. Hae **Ominaisuuksien hallinta** Commercen pääkonttoriversiossa.
1. Avaa käytettävissä olevien ominaisuuksien luettelo valitsemalla **Kaikki**. 
1. Kirjoita hakuruutuun **Suositukset**.
1. Valitse **Tuotesuositukset** -ominaisuus.
1. Valitse **Tuotesuositukset** -ominaisuusruudussa **Ota käyttöön nyt**.

![Suositusten ottaminen käyttöön](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> Tämä menettely käynnistää tuotesuositusluetteloiden luontiprosessin. Luetteloiden luominen, niiden saaminen käyttöön ja näkyminen myyntipisteessä tai Dynamics 365 Commerce -sovelluksessa voi kestää useita tunteja.

## <a name="configure-recommendation-list-parameters"></a>Suositusluettelon parametrien määrittäminen

Oletusarvoisesti tekoälyyn perustuva tuotesuositusluettelo sisältää ehdotetut arvot. Voit muuttaa ehdotettuja oletusarvoja haluamallasi tavalla. Lisätietoja oletusparametrien muuttamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvan tuotesuositusluettelon hallinta](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Suositusten näyttäminen myyntipistelaitteissa

Kun suositukset on otettu käyttöön Commercen taustatoiminnossa, suosituspaneeli on lisättävä ohjausobjektin myyntipistenäyttöön asettelutyökalun avulla. Lisä tietoja tästä prosessista on kohdassa [Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Kohdennettujen suositusten ottaminen käyttöön

Dynamics 365 Commerce -ohjelmassa jälleenmyyjät voivat tehdä mukautettuja tuotesuosituksia (eli personointeja). Näin henkilökohtaiset suositukset voidaan sisällyttää asiakaskokemukseen verkossa ja myyntipisteessä. Kun mukautustoiminto on käytössä, järjestelmä voi liittää käyttäjän osto- ja tuotetiedot ja luoda yksilöllisiä tuotesuosituksia.

Lisätietoja mukautetuista suosituksista on kohdassa [Mukautettujen suositusten ottaminen käyttöön](personalized-recommendations.md).

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä](enable-adls-environment.md)

[Kohdennettujen suositusten ottaminen käyttöön](personalized-recommendations.md)

["Osta samankaltaisia tyylejä" -suositusten käyttöönotto](shop-similar-looks.md)

[Kohdennetuista tuotesuosituksista kieltäytyminen](personalization-gdpr.md)

[Tuotesuositusten lisääminen myyntipisteessä](product.md)

[Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Kuratoitujen suositusten manuaalinen luominen](create-editorial-recommendation-lists.md)

[Suositusten luominen esittelytietojen avulla](product-recommendations-demo-data.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]