---
title: Sähköisen kaupankäynnin sivuston luominen
description: Tässä ohje aiheessa kuvataan tehtävät, jotka liittyvät uuden sähköisen kaupankäynnin sivuston luomiseen Dynamics 365 Commercessa.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697126"
---
# <a name="create-an-e-commerce-site"></a>Sähköisen kaupankäynnin sivuston luominen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohje aiheessa kuvataan tehtävät, jotka liittyvät uuden sähköisen kaupankäynnin sivuston luomiseen Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Jos haluat aloittaa sähköisen kaupankäynnin sivuston kehittämisen, sinun on ensin luotava sivuston muokkausympäristössä uusi sivusto. Ennen kuin voit luoda uuden sivuston, Dynamics 365 Retail -sovellukseen on luotava vähintään yksi verkkokauppa. 

## <a name="set-up-your-site"></a>Sivuston määrittäminen

Määritä sivusto seuraavasti.

1. Valitse Microsoft Lifecycle Services (LCS) -palvelussa sivuston muokkausympäristön linkki. 
1. Valitse sivuston muokkausympäristön aloitussivulla **Uusi sivusto**.
1. Anna seuraavat tiedot **Uusi sivusto** -valintaikkunaan.

| Kenttä                               | Kuvaus |
|-------------------------------------|-------------|
| Sivuston nimi                           | Anna näyttönimi, jota käytetään sivuston muokkausympäristön sivustossa. Tämä nimi näkyy vain muokkausympäristössä. Se ei näy asiakkaille. |
| Sivuston järjestelmänvalvojan käyttöoikeusryhmä | Määritä Microsoft Azure Active Directory (Azure AD) -käyttöoikeusryhmä. Se hallitsee käyttäjiä, joilla on tämän sivuston järjestelmänvalvojan rooli. |
| Oletuskanava (toimintayksikön numero) | Valitse verkkomyymälä, jonka verkkomyymälä tämä sivusto on. Jos haluat, että sähköisen kaupankäynnin sivusto tukee useita verkkomyymälöitä, liitä myymälät sivustoon **Sivuston asetukset** -kohdassa sivuston määrityksen jälkeen. |
| Oletuskieli                            | Määritä tämän verkkomyymälän ja -markkinan oletuskieli. Verkkomyymälä voi tukea useita kieliä. Jos haluat, että tämä verkkomyymälä tai toinen verkkomyymälä tukee useita kieliä, määritä tuki **Sivuston asetukset** -kohdassa sivuston määrityksen jälkeen.  |
| Toimialue                              | Valitse toimialueen nimi, joka toimii tämän verkkomyymälän toimialueena. Jos et ole määrittänyt toimialueita LCS:ssä, voit jättää tämän kentän tyhjäksi. Kun toimialue on määritetty LCS:ssä, lisää se verkkomyymälään **Sivuston asetukset** -kohdassa.  |
| Polku                              | Kun sivusto tukee useita kieliä tietyssä toimialueessa, käytä polkukenttää ja luo yksilöivä sivuston URL-osoite kyseiselle toimialueelle ja kielen yhdistelmälle. Jos **Oletuskieli**-kentässä määritetty kieli on ainoa kieli, jota tuetaan tässä toimialueessa, tai jos se on oletuskieli sen jälkeen kun sivusto on lokalisoitu muille kielille, suosittelemme, että tämä kenttä jätetään tyhjäksi. |


Kun sivusto on luotu, voit varmistaa, että se on liitetty verkkomyymälään, valitsemalla **Tuotteet**-välilehden. Näkyvissä on tuotevalikoima, joka on määritetty verkkomyymälälle. Voit käyttää avattavaa valikkoa sivun vasemmassa yläosassa, jos haluat käyttää kohdistettuja tuotteita luokan mukaan.

## <a name="additional-resources"></a>Lisäresurssit

[Verkkokaupan yleiskatsaus](online-store-overview.md)

[Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md)

[Liitä verkkosivusto kanavaan](associate-site-online-store.md)

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)

[Muokkauksen aloitussivun yleiskatsaus](authoring-home-overview.md)

[Uuden sivuston sivun lisääminen](add-new-page.md)
