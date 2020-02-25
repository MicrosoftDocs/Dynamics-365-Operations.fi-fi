---
title: Sähköisen kaupankäynnin sivuston luominen
description: Tämä ohjeaihe sisältää ohjeet ja tiedot, jotka tarvitaan uuden sähköisen kaupankäynnin sivun luomiseen Dynamics 365 Commerce sivustonmuodostimessa.
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
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
ms.openlocfilehash: 3d3d8a290f06d9734be21f2d59152acac6857506
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002010"
---
# <a name="create-an-e-commerce-site"></a>Sähköisen kaupankäynnin sivuston luominen


[!include [banner](includes/banner.md)]

Tämä ohjeaihe sisältää ohjeet ja tiedot, jotka tarvitaan uuden sähköisen kaupankäynnin sivun luomiseen Dynamics 365 Commerce sivustonmuodostimessa.

Ennen kuin voit aloittaa sähköisen kaupankäynnin sivuston kehittämisen, sinun on ensin luotava uusi sivusto sivustuonmuodostimessa. 


Jos haluat aloittaa sähköisen kaupankäynnin sivuston kehittämisen, sinun on ensin luotava sivuston muokkausympäristössä uusi sivusto. Ennen kuin voit luoda uuden sivuston, Commerce-sovellukseen on luotava vähintään yksi verkkokauppa. 


## <a name="set-up-your-site"></a>Sivuston määrittäminen

Määritä sivusto seuraavasti.

1. Avaa sivustonmuodostimen ympäristö. Löydät linkin sivustonmuodostimeen Microsoft Lifecycle Servicesin (LCS) ympäristöominaisuuksien sivulta.
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

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md)

[Liitä verkkosivusto kanavaan](associate-site-online-store.md)

[Robots.txt-tiedostojen hallinta](manage-robots-txt-files.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)
