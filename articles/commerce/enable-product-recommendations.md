---
title: Ota tuotesuositukset käyttöön
description: Tässä artikkelissa kerrotaan, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten.
author: bebeale
ms.date: 08/31/2021
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
ms.openlocfilehash: 3dceec9e8e994a81b43cd5d1bd13970f2d246f40
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892068"
---
# <a name="enable-product-recommendations"></a>Ota tuotesuositukset käyttöön

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten. Lisätietoja tuotesuositusten luetteloista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Suositusten esitarkistus

1. Varmista, että sinulla on voimassa oleva Dynamics 365 Commerce -suositusten käyttöoikeus.
1. Varmista, että yksikkösäilö on yhteydessä asiakkaan omistamaan Azure Data Lake Storage Gen 2 -tiliin. Katso lisätietoja kohdasta [Varmista, että Azure Data Lake Storage on ostettu ja todennettu onnistuneesti ympäristössä](enable-ADLS-environment.md).
1. Vahvista, että Azure AD -käyttäjätietojen määritys sisältää suositusten merkinnän. Lisätietoja tästä toiminnosta alla.
1. Varmista, että yksikkösäilön päivittäinen päivitys Azure Data Lake Storage Gen 2:een on ajoitettu. Lisätietoja on kohdassa [Varmista, että yksikkösäilön päivitys on automatisoitu](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
1. Ota RetailSale-mittaukset käyttöön yksikkösäilössä. Lisätietoja tämän prosessin määrittämisestä: [Mittayksiköiden käsitteleminen](/dynamics365/ai/customer-insights/pm-measures).

Kun edellä mainitut vaiheet on suoritettu, olet valmis ottamaan suositukset käyttöön.

## <a name="azure-ad-identity-configuration"></a>Azure AD -tunnisteen konfiguraatio

Tämä vaihe on pakollinen vain asiakkaille, jotka käyttävät infrastruktuuria palvelun (IaaS) määrityksenä. Azure AD:n käyttäjätietojen määritys on automaattinen asiakkaille, jotka käyttävät Azure Service Fabricia, mutta on suoriteltavaa varmistaa, että asetus on määritetty odotetulla tavalla.

### <a name="setup"></a>Asetusten määrittäminen

1. Etsi Commerce-pääkonttorissa **Azure Active Directory -sovellukset** -sivua
1. Tarkista, että **RecommendationSystemApplication-1**-merkintä on olemassa. Jos merkintää ei ole, luo sellainen käyttäen seuraavia tietoja:

    - **Asiakastunnus**: d37b07e8-dd1c-4514-835d-8b918e6f9727
    - **Nimi**: RecommendationSystemApplication-1
    - **Käyttäjätunnus**: RetailServiceAccount

1. Tallenna ja sulje sivu. 

## <a name="turn-on-recommendations"></a>Suositusten ottaminen käyttöön

Voit ottaa tuotesuositukset käyttöön noudattamalla seuraavia ohjeita.

1. Hae **Ominaisuuksien hallinta** Commercen pääkonttoriversiossa.
1. Avaa käytettävissä olevien ominaisuuksien luettelo valitsemalla **Kaikki**. 
1. Kirjoita hakuruutuun **Suositukset**.
1. Valitse **Tuotesuositukset** -ominaisuus.
1. Valitse **Tuotesuositukset** -ominaisuusruudussa **Ota käyttöön nyt**.

![Suositusten ottaminen käyttöön.](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> - Edellä mainittu menettely käynnistää tuotesuositusluetteloiden luontiprosessin. Luetteloiden luominen, niiden saaminen käyttöön ja näkyminen myyntipisteessä tai Dynamics 365 Commerce -sovelluksessa voi kestää useita tunteja.
> - Tämä määritys ei ota käyttöön kaikkia suositusominaisuuksia. Erilliset ominaisuuksienhallinnan merkinnät ohjaavat edistyneitä ominaisuuksia, kuten yksilöllisiä suosituksia, kuten "osta samankaltaiselta näyttäviä" tai "osta samankaltaisen kuvauksen perusteella". Lisätietoja näiden ominaisuuksien käyttöönotosta Commerce-pääkonttorista: [Yksilöllisten suositusten käyttöönotto](personalized-recommendations.md), [Osta samankaltaisia näyttäviä -suositusten käyttöönotto](shop-similar-looks.md) ja [Osta samankaltaisen kuvauksen perusteella -suositusten käyttöönotto](shop-similar-description.md).

## <a name="configure-recommendation-list-parameters"></a>Suositusluettelon parametrien määrittäminen

Oletusarvoisesti tekoälyyn perustuva tuotesuositusluettelo sisältää ehdotetut arvot. Voit muuttaa ehdotettuja oletusarvoja haluamallasi tavalla. Lisätietoja oletusparametrien muuttamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvan tuotesuositusluettelon hallinta](modify-product-recommendation-results.md).

## <a name="include-recommendations-in-e-commerce-experiences"></a>Suositusten sisällyttäminen sähköisen kaupankäynnin kokemuksiin

Kun suositukset on otettu käyttöön Commerce-pääkonttorissa, sähköisen kaupankäynnin kokemuksia koskevien suositustulosten näyttämiseen käytettävät Commerce-moduulit ovat valmiina määritettäväksi. Lisätietoja: [Tuotteiden keräilymoduulit](product-collection-module-overview.md).

## <a name="show-recommendations-on-pos-devices"></a>Suositusten näyttäminen myyntipistelaitteissa

Kun suositukset on otettu käyttöön Commerce-pääkonttorissa, suosituspaneeli on lisättävä ohjausobjektin myyntipistenäyttöön asettelutyökalun avulla. Lisä tietoja tästä prosessista on kohdassa [Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle](add-recommendations-control-pos-screen.md). 

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
