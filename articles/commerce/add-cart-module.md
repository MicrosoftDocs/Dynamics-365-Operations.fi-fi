---
title: Ostoskorimoduuli
description: Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: f21268ed4cffed1d5c789f722796cdf05e965819
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621033"
---
# <a name="cart-module"></a>Ostoskorimoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskuvaus

Ostokorimoduuli näyttää ostoskoriin lisätyt nimikkeet ennen asiakkaan siirtymistä kassalle. Moduuli näyttää myös tilauksen yhteenvedon ja asiakas voi käyttää tarjouskoodeja tai poistaa niitä.

Ostoskorimoduuli tukee kirjautuneiden kassan käyttämistä kirjautuneena ja vieraana. Se tukee myös **Jatka ostoksia** -linkkejä. Voit määrittää tämän linkin reitin valitsemalla **Sivuston asetukset \> Laajennukset \> Reitit**.

Ostoskorimoduuli esittää tiedot ostoskorin tunnuksen mukaan, joka on koko sivuston käytettävissä oleva selaineväste. 

Seuraavassa kuvassa on esimerkki Fabrikam-sivuston ostoskärrysivusta.

![Esimerkki ostoskärrymoduulista](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a>Ostoskorimoduulin ominaisuudet ja paikat

Ostoskorimoduulissa on **Otsikko**-ominaisuus, jonka arvoiksi voidaan määrittää esimerkiksi **Ostoskassi** ja **Ostoskorin nimikkeet**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduulit, joita voidaan käyttää ostoskorimoduulissa

- **Tekstilohko** – Tämä moduuli tukee mukautettua viestintää ostoskorimoduulissa. Sisällönhallintajärjestelmä (CMS) ohjaa viestintää. Voit lisätä minkä tahansa viestin, esimerkiksi Jos tilauksessa on ongelmia, soita numeroon 1-800-Fabrikam.
- **Myymälän valitsin** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa. Käyttäjät voivat etsiä lähellä olevia myymälöitä antamalla sijainnin. Lisätietoja tästä moduulista on kohdassa [Kaupan valitsinmoduuli](store-selector.md).

## <a name="module-properties"></a>Moduulin ominaisuudet

Seuraavat ostoskorimoduuliasetukset voidaan määrittää valitsemalla **Sivuston asetukset \> Laajennukset**:

- **Maksimimäärä** – Tätä ominaisuutta käytetään määrittämään kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä. Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.
- **Varasto** – lisätietoja varastoasetusten ottamisesta käyttöön on kohdassa [Varastoasetusten käyttäminen](inventory-settings.md).
- **Jatka ostoksia** – Tällä ominaisuudella määritetään **Jatka ostoksia** -linkin reitti. Reitti voidaan konfiguroida sivuston tasolla, jolloin jälleenmyyjät voivat ohjata asiakkaan takaisin kotisivulle tai mille tahansa muulle sivuston sivulle.

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit -käyttö

Ostoskorimoduuli hakee tuotetiedot Commerce Scale Unitin ohjelmistorajapintojen avulla. Selaimen evästeen ostoskorin tunnusta käytetään kaikkien tuotetietojen noutamisessa Commerce Scale Unitista.

## <a name="add-a-cart-module-to-a-page"></a>Ostoskorimoduulin lisääminen sivulle

Voit lisätä ostoskorimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Sivun osat** ja **Uusi** luodaksesi uuden osan.
1. Valitse **Uusi sivun osa** -valintaikkunassa **Ostoskori**-moduuli.
1. Kirjoita **Sivun osan nimi** -kohtaan **Ostoskorin osa** ja valitse sitten **OK**.
1. Valitse **Ostoskori**-paikka.
1. Valitse oikealla olevassa ominaisuudet-ruudussa kynäsymboli, kirjoita otsikko tekstikenttään ja valitse sitten valintamerkkisymboli.
1. Valitse kolme pistettä (**...**) **Ostoskori**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Myymälävalitsin**-moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.
1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan mallin nimi.
1. Valitse jäsennyspuussa **Tekstiosa**-paikka. Valitse kolme pistettä (**...**) ja valitse sitten **Lisää osa**.
1. Valitse **Valitse sivun osa** -valintaikkunassa **Ostoskorin osa** ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Valitse **Valitse malli** -valintaikkunassa malli, jonka loit aiemmin, lisää sivun nimi ja valitse sitten **OK**.
1. Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Myymälän valitsinmoduuli](store-selector.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)

[Vähittäismyyntikanavien varaston käytettävyyden laskeminen](calculated-inventory-retail-channels.md)
