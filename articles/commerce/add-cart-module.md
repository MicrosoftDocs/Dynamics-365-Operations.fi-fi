---
title: Ostoskorimoduuli
description: Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696758"
---
# <a name="cart-module"></a>Ostoskorimoduuli

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Ostoskorimoduuli on säilö, jota käytetään kaikkien niiden moduulien isännöintiin, joita tarvitaan näytettäessä ostoskorissa olevat nimikkeet. Se sisältää esimerkiksi kaikki ostoskoriin lisätyt nimikkeet, tilauksen yhteenvedon ja tarjouskoodit.

Ostoskorimoduuli hahmontaa tiedot ostoskorin tunnuksen mukaan. Ostoskorin tunnus on selaimen eväste, joka on käytettävissä koko sivustossa.

## <a name="cart-module-properties-and-slots"></a>Ostoskorimoduulin ominaisuudet ja paikat

Ostoskorimoduuli on säilö, joka ohjaa joitakin perusominaisuuksia, kuten otsikkoa ja leveyttä. Otsikko on yleensä teksti, kuten **Ostoskassi**, **Ostoskorisi** tai **Ostoskorin nimikkeet**. Leveysasetus määrittää, onko säilön sisässä olevien moduulien mahduttava säilöön vai ovatko ne näytön levyisiä.

Ostoskorisivu jaetaan useisiin alueisiin, joita ovat ostoskoririvin nimikkeet, tilauksen yhteenveto ja kassatoiminto sekä Etsi myymälästä -toiminto. Kukin alue yhdistetään ostoskorimoduulin paikkaan. Jokainen paikka hyväksyy ennalta määritetyn moduulijoukon.

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduulit, joita voidaan käyttää ostoskorimoduulissa

- **Ostoskoririvin nimikkeet** – Tässä moduulissa on kaikkien ostoskoriin lisättyjen nimikkeiden yhteenveto. Tiedot sisältävät tuotteen nimen, valitut dimensiot, hinnan, määrän ja alennukset. Tämä moduuli tukee myös toimintoja, kuten Poista ostoskorista ja Lisää toivomuslistaan. Jokaisella rivinimikkeellä on mahdollisuus toimitukseen ja myymälästä noutoon. Tämä vaihtoehto on määritettävä erikseen Nouda myymälästä -moduulissa.
- **Tilauksen yhteenveto** – Tämä moduuli näyttää tilauksen yhteenvedon. Tiedot sisältävät välisumman, toimituksen, verot ja säästöt. Tälle moduulille voidaan määrittää otsikko.
- **Kampanjakoodi** – Tämän moduulin avulla asiakas voi lunastaa tarjouskoodeja. Tarjouskoodin voi käyttää tai sen voidaan poistaa.
- **Kassalle** – Tämä moduuli käynnistää kassatoiminnon. Se ohjaa käyttäjän kassalle siirtymisen sivulle. Tälle moduulille on määritettävä kolme linkkiä:

    - **Kassalle** – Tämä linkki pakottaa asiakkaat kirjautumaan sisään, jos he eivät ole vielä tehneet sitä.
    - **Vieraan siirtyminen kassalle** – Tämän linkin avulla anonyymit asiakkaat voivat tehdä tilauksia. Se näkyy vain, kun asiakkaat eivät ole kirjautuneet sisään.
    - **Takaisin tekemään ostoksia** – Tämän linkin avulla asiakkaat siirtyvät aloitussivulle tai jollekin muulle sivulle ja jatkavat ostosten tekemistä.

- **Sisällöntäyteinen lohko** – Tämä moduuli tukee mukautettua viestintää ostoskorimoduulissa. Sisällönhallintajärjestelmä (CMS) ohjaa viestintää. Voit lisätä minkä tahansa viestin, esimerkiksi Jos tilauksessa on ongelmia, soita numeroon 1-800-Fabrikam.
- **Nouda myymälästä** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa. Oletusarvon mukaan tämä moduuli näyttää myymälät, jotka sijaitsevat 50 mailin päässä asiakkaasta. Arvoa voi kuitenkin muuttaa moduulissa. Kunkin myymälän varasto tarkistetaan, jos varaston tarkistustoiminto on käytössä, ja näkyvissä on soveltuva varastossa- tai varasto tyhjä -viesti.
- **Myymälän haku Bing Mapsin avulla** – Tätä moduulia voi käyttää Nouda myymälästä -moduulin sisässä. Sen avulla asiakkaat voivat hakea myymälöitä syöttämällä sijainnin. Bing Maps -geokoodauksen ohjelmointirajapintaa käytetään asiakkaan syöttämän sijainnin muuntamisessa leveys- ja pituusasteiksi. Jos tätä moduulia ei käytetä, vain asiakkaan nykyisen sijainnin lähellä olevat myymälät näytetään, eikä asiakas voi hakea toista sijaintia.

## <a name="cart-module-settings"></a>Ostoskorimoduulin asetukset

Ostoskorimoduuleilla on seuraavat kolme määritettävää asetusta:

- **Maksimimäärä** – Kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä. Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.
- **Varaston tarkistus** – Kun arvoksi on asetettu **Tosi**, nimike lisätään ostoskoriin vasta, kun ostoruutumoduuli varmistaa, että nimikettä on varastossa. Tämä varaston tarkistus tehdään sekä skenaarioissa, joissa nimike toimitetaan, että skenaarioissa, joissa se noudetaan myymälästä. Jos arvoksi on määritetty **Epätosi**, varaston tarkistus tehdään vasta, kun nimike on lisätty ostoskoriin ja tilaus on tehty.
- **Varaston puskuri** – Varastoa ylläpidetään reaaliaikaisesti. Jos useat asiakkaat tekevät tilauksia, todellisen varastomäärän ylläpitäminen voi olla vaikeaa. Tämän vuoksi varastolle voidaan määrittää puskuri. Kun varaston tarkistus tehdään ja varasto on pienempi kuin puskurisumma, tuotetta käsitellään kuin se olisi loppunut varastosta. Kun myynti tapahtuu nopeasti useiden kanavien kautta eikä varastomäärää ole täysin synkronoitu, on pienempi riski sille, että nimikettä ei ole varastossa myynnin hetkellä.

## <a name="retail-server-interaction"></a>Vähittäismyynnin palvelimen vuorovaikutus

Ostoskorimoduuli hakee tuotetiedot vähittäismyynnin palvelimen ohjelmistorajapintojen avulla. Selaimen evästeen ostoskorin tunnusta käytetään kaikkien tuotetietojen noutamisessa vähittäismyynnin palvelimelta.

## <a name="add-a-cart-module-to-a-page"></a>Ostoskorimoduulin lisääminen sivulle

Voit lisätä ostoskorimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Luo osa nimeltä **Ostoskoriosa** ja lisää siihen ostoskorimoduuli.
1. Lisää ostoskoririvin nimikkeiden moduuli ostoskorimoduulin **Ostoskoririvin nimikkeet** -paikkaan.
1. Lisää **Tilauksen yhteenveto** -paikkaan tilauksen yhteenvedon moduuli.
1. Lisää **Kampanjakoodi**-paikkaan kampanjakoodimoduuli.
1. Lisää **Kassalle**-paikkaan kassamoduuli.
1. Lisää **Etsi myymälästä** -paikkaan Nouda myymälästä -moduuli.
1. Valitse Nouda myymälästä -moduulissa **Myymälähaku**-paikka ja lisää myymälän haku Bing Mapsin avulla -moduuli.
1. Kirjaa osa sisään ja julkaise se.
1. Luo malli nimeltä **Ostoskorimalli** ja lisää siihen juuri luotu ostoskoriosa.
1. Tallenna malli, kirjaa se sisään ja julkaise se.
1. Luo sivu, joka käyttää uutta mallia.
1. Tallenna ja esikatsele sivu.
1. Kirjaa sivu sisään ja julkaise se.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)
