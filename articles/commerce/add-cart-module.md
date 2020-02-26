---
title: Ostoskorimoduuli
description: Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025433"
---
# <a name="cart-module"></a>Ostoskorimoduuli


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Ostokorimoduulissa näytetään ostoskoriin lisätyt nimikkeet ennen asiakkaan siirtymistä kassalle. Se sisältää esimerkiksi kaikki ostoskoriin lisätyt nimikkeet ja tilauksen yhteenvedon. Lisäksi asiakas voi käyttää tai poistaa kampanjakoodeja.

Ostoskorimoduuli tukee kirjautuneiden kassan käyttämistä kirjautuneena ja vieraana. Se tukee myös **Jatka ostoksia** -linkkejä. Voit määrittää tämän linkin reitin valitsemalla **Sivuston asetukset \> Laajennukset \> Reitit**.

Ostoskorimoduuli hahmontaa tiedot ostoskorin tunnuksen mukaan. Ostoskorin tunnus on selaimen eväste, joka on käytettävissä koko sivustossa.

## <a name="cart-module-properties-and-slots"></a>Ostoskorimoduulin ominaisuudet ja paikat

Ostoskorimoduulissa on **Otsikko**-ominaisuus, jonka arvoiksi voidaan määrittää esimerkiksi **Ostoskassi** ja **Ostoskorin nimikkeet**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduulit, joita voidaan käyttää ostoskorimoduulissa

- **Tekstilohko** – Tämä moduuli tukee mukautettua viestintää ostoskorimoduulissa. Sisällönhallintajärjestelmä (CMS) ohjaa viestintää. Voit lisätä minkä tahansa viestin, esimerkiksi Jos tilauksessa on ongelmia, soita numeroon 1-800-Fabrikam.
- **Myymälän valitsin** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa. Käyttäjät voivat etsiä lähellä olevia myymälöitä antamalla sijainnin. Myymälän valitsinmoduuli on integroitu Bing Maps -geokoodauksen ohjelmointirajapintaan, jota käytetään muuntamaan sijainti leveys- ja pituusasteiksi. Bing Maps -ohjelmointirajapinnan avain on pakollinen, ja se on lisättävä Vähittäismyynnin yhteiset parametrit -sivulla Dynamics 365 Retailissa. Tämä moduuli tukee kahta ominaisuutta: **Hakusäde** ja **Käyttöehdot-linkki**. **Hakusäde**-ominaisuus määrittää myymälän hakusäteen maileina. Jos arvoa ei määritetä, käytössä on oletushakusäde 50 mailia. Jos käytössä on Bings Maps tai jokin ulkoinen palvelu, palveluehtojen linkki voidaan antaa **Käyttöehdot-linkki**-ominaisuudella. Palveluehtojen linkki on pakollinen Bing Maps -palvelussa. 

## <a name="cart-module-settings"></a>Ostoskorimoduulin asetukset

Ostoskorimoduulissa on seuraavat asetukset, jotka voidaan määrittää valitsemalla **Sivuston asetukset \> Laajennukset**:

- **Maksimimäärä** – Tätä ominaisuutta käytetään määrittämään kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä. Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.
- **Varaston tarkistus** – Kun arvoksi on asetettu **Tosi**, nimike lisätään ostoskoriin vasta, kun ostoruutumoduuli varmistaa, että nimikettä on varastossa. Tämä varaston tarkistus tehdään sekä skenaarioissa, joissa nimike toimitetaan, että skenaarioissa, joissa se noudetaan myymälästä. Jos arvoksi on määritetty **Epätosi**, varaston tarkistus tehdään vasta, kun nimike on lisätty ostoskoriin ja tilaus on tehty.
- **Varaston puskuri** – Tällä ominaisuudella määritetään varaston puskurimäärä. Varastoa ylläpidetään reaaliaikaisesti. Jos useat asiakkaat tekevät tilauksia, todellisen varastomäärän ylläpitäminen voi olla vaikeaa. Kun varaston tarkistus tehdään ja varasto on pienempi kuin puskurisumma, tuotetta käsitellään kuin se olisi loppunut varastosta. Kun myynti tapahtuu nopeasti useiden kanavien kautta eikä varastomäärä ole täysin synkronoitu, on pienempi riski siitä, että nimikettä ei ole varastossa myynnin hetkellä.
- **Jatka ostoksia** – Tällä ominaisuudella määritetään **Jatka ostoksia** -linkin reitti. Tämä reitti voidaan määrittää sivustotasolla. Tämän määrityksen ansiosta vähittäismyyjät voivat siirtää asiakkaan takaisin aloitussivulle tai jollekin muulle sivuston sivulle.

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit -käyttö

Ostoskorimoduuli hakee tuotetiedot Commerce Scale Unitin ohjelmistorajapintojen avulla. Selaimen evästeen ostoskorin tunnusta käytetään kaikkien tuotetietojen noutamisessa Commerce Scale Unitista.

## <a name="add-a-cart-module-to-a-page"></a>Ostoskorimoduulin lisääminen sivulle

Voit lisätä ostoskorimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Luo osa nimeltä **Ostoskoriosa** ja lisää siihen ostoskorimoduuli.
1. Lisää otsikko ostoskorimoduuliin.
1. Lisää myymälän valitsinmoduuli ostoskorimoduuliin.
1. Tallenna osa, lopeta sen muokkaus ja julkaise se.
1. Luo malli nimeltä **Ostoskorimalli** ja lisää siihen juuri luotu ostoskoriosa.
1. Tallenna malli, lopeta sen muokkaus ja julkaise se.
1. Luo sivu, joka käyttää uutta mallia.
1. Tallenna ja esikatsele sivu.
1. Kun sivun muokkaus on valmis, julkaise se.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)
