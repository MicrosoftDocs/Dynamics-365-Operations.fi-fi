---
title: Ostoskorimoduuli
description: Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154014"
---
# <a name="cart-module"></a>Ostoskorimoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskuvaus

Ostokorimoduuli näyttää ostoskoriin lisätyt nimikkeet ennen asiakkaan siirtymistä kassalle. Moduuli näyttää myös tilauksen yhteenvedon ja asiakas voi käyttää tarjouskoodeja tai poistaa niitä.

Ostoskorimoduuli tukee kirjautuneiden kassan käyttämistä kirjautuneena ja vieraana. Se tukee myös **Jatka ostoksia** -linkkejä. Voit määrittää tämän linkin reitin valitsemalla **Sivuston asetukset \> Laajennukset \> Reitit**.

Ostoskorimoduuli esittää tiedot ostoskorin tunnuksen mukaan, joka on koko sivuston käytettävissä oleva selaineväste.

## <a name="cart-module-properties-and-slots"></a>Ostoskorimoduulin ominaisuudet ja paikat

Ostoskorimoduulissa on **Otsikko**-ominaisuus, jonka arvoiksi voidaan määrittää esimerkiksi **Ostoskassi** ja **Ostoskorin nimikkeet**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduulit, joita voidaan käyttää ostoskorimoduulissa

- **Tekstilohko** – Tämä moduuli tukee mukautettua viestintää ostoskorimoduulissa. Sisällönhallintajärjestelmä (CMS) ohjaa viestintää. Voit lisätä minkä tahansa viestin, esimerkiksi Jos tilauksessa on ongelmia, soita numeroon 1-800-Fabrikam.
- **Myymälän valitsin** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa. Käyttäjät voivat etsiä lähellä olevia myymälöitä antamalla sijainnin. Lisätietoja tästä moduulista on kohdassa [Kaupan valitsinmoduuli](store-selector.md).

## <a name="cart-module-settings"></a>Ostoskorimoduulin asetukset

Ostoskorimoduulissa on seuraavat asetukset, jotka voidaan määrittää valitsemalla **Sivuston asetukset \> Laajennukset**:

- **Maksimimäärä** – Tätä ominaisuutta käytetään määrittämään kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä. Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.
- **Varaston tarkistus** – Kun arvoksi on asetettu **Tosi**, nimike lisätään ostoskoriin vasta, kun ostoruutumoduuli varmistaa, että nimikettä on varastossa. Tämä varaston tarkistus tehdään skenaarioissa, joissa nimike toimitetaan, että skenaarioissa, joissa se noudetaan myymälästä. Jos arvoksi on määritetty **Epätosi**, varaston tarkistus tehdään vasta, kun nimike on lisätty ostoskoriin ja tilaus on tehty.
- **Varaston puskuri** – Tällä ominaisuudella määritetään varaston puskurimäärä. Varastoa ylläpidetään reaaliaikaisesti. Jos useat asiakkaat tekevät tilauksia, todellisen varastomäärän ylläpitäminen voi olla vaikeaa. Kun varaston tarkistus tehdään ja varasto on pienempi kuin puskurisumma, tuotetta käsitellään kuin se olisi loppunut varastosta. Kun myynti tapahtuu nopeasti useiden kanavien kautta eikä varastomäärä ole täysin synkronoitu, on pienempi riski siitä, että nimikettä ei ole varastossa myynnin hetkellä.
- **Jatka ostoksia** – Tällä ominaisuudella määritetään **Jatka ostoksia** -linkin reitti. Reitti voidaan konfiguroida sivuston tasolla, jolloin jälleenmyyjät voivat ohjata asiakkaan takaisin kotisivulle tai mille tahansa muulle sivuston sivulle.

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit -käyttö

Ostoskorimoduuli hakee tuotetiedot Commerce Scale Unitin ohjelmistorajapintojen avulla. Selaimen evästeen ostoskorin tunnusta käytetään kaikkien tuotetietojen noutamisessa Commerce Scale Unitista.

## <a name="add-a-cart-module-to-a-page"></a>Ostoskorimoduulin lisääminen sivulle

Voit lisätä ostoskorimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Luo osa nimeltä **Ostoskoriosa** ja lisää uuteen osaan ostoskorimoduuli.
1. Lisää otsikko ostoskorimoduuliin.
1. Lisää myymälän valitsinmoduuli ostoskorimoduuliin.
1. Tallenna osa, lopeta sen muokkaus ja sitten julkaise osa.
1. Luo malli nimeltä **Ostoskorimalli** ja lisää juuri luotu ostoskoriosa.
1. Tallenna malli, lopeta sen muokkaus ja sitten julkaise malli.
1. Luo sivu, joka käyttää uutta mallia.
1. Tallenna ja esikatsele sivu.
1. Lopeta sivun muokkaus ja sitten julkaise sivu.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Myymälän valitsinmoduuli](store-selector.md)

[Ostoruutumoduuli](add-buy-box.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)
