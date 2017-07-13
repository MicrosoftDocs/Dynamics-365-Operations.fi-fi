---
title: "Luottokorttien määritys, varmennus ja sieppaaminen"
description: "Tässä artikkelissa on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin tehtävän luottokortin varmennuksen yleiskatsaus. Artikkeli sisältää tietoja maksupalvelun määrittämisestä, luottokortin lisäämisestä myyntitilaukseen ja varmennuksen mitätöinnistä."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a5b3dc7710ebbce50366ca9299bfb30dffc03187
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Luottokorttien määritys, varmennus ja sieppaaminen
<a id="credit-card-setup-authorization-and-capture" class="xliff"></a>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Tässä artikkelissa on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin tehtävän luottokortin varmennuksen yleiskatsaus. Artikkeli sisältää tietoja maksupalvelun määrittämisestä, luottokortin lisäämisestä myyntitilaukseen ja varmennuksen mitätöinnistä.

Luottokorttien maksupalvelun määrittäminen
<a id="setting-up-the-credit-card-payment-service" class="xliff"></a>
------------------------------------------

Jos haluat käyttää luottokortteja, sinun on määritettävä ja aktivoitava maksupalvelu Maksupalvelut-sivulla. Maksupalvelu toimii välittäjänä yrityksesi ja asiakkaan korttimaksut käsittelevän pankin välillä. Sinun on käytettävä luottokorttimaksun tarjoajaa, joka on saatavilla Maksuyhdistin-kentässä ja määrittää tili kyseiselle palveluntarjoajalle. Sinun on sitten määritettävä muut asetukset Maksupalvelut-sivulla, määritettävä luottokorttityypit American Express, Discover, MasterCard ja Visa -korteille Luottokorttityypit-sivulla ja aktivoitava palveluntarjoaja oletuspalveluntarjoajaksi. Sinun on myös noudatettava seuraavia vaiheita:
-   Määritä luottokortin varmennuksessa käytettävät parametrit Myyntireskontran parametrit -sivulla.
-   Määritä luottokorttien maksuehdot Maksuehdot-sivulla. Valitse Luottokortti Maksutyyppi-kentässä.
-   Syötä asiakkaan luottokorttitiedot Asiakkaan luottokortit -sivulla.

## Uuden luottokortin lisääminen
<a id="adding-a-new-credit-card" class="xliff"></a>
Voit luoda uudet luottokorttitietueet Asiakkaat-sivulla kohdasta Asiakas > Määritä > Luottokortti. Voit myös luoda luottokorttitietueita kirjatessasi myyntitilauksia Myyntitilaus-sivulla kohdasta Hallinta > Asiakas > Luottokortti > Rekisteröi.
Luottokortin lisääminen myyntitilaukseen
-------------------------------------

Voit lisätä luottokortin myyntitilaukseen valitsemalla luottokortin Myyntitilaus-sivun Hinnat ja alennukset -pikavälilehden luottokorttihausta. Varmennusprosessin voit aloittaa valitsemalla toimintoruudun Hallinta-välilehdestä kohdan Luottokortti ja Varmenna.
Luottokortin varmennus
-------------------------

Kun luottokortti varmennetaan, kortin numero ja kortin haltijan henkilöllisyys varmennetaan ja käytettävissä oleva luottosaldo tarkistetaan. Voit myös tarkistaa kortin tarkistusnumeron ja kortinhaltijan osoitteen. Laskun summa vähennetään tämän jälkeen asiakkaan käytettävissä olevasta luottosaldosta. Maksupalvelu lähettää tiedon luottokortin hyväksymisestä tai hylkäämisestä. Kun myyntitilaus laskutetaan, laskun summa veloitetaan (siepataan) luottokortilta.

### Kortin tarkistusnumero
<a id="card-verification-value" class="xliff"></a>

Voit vaatia kortin tarkistusarvon käyttöä, jota kutsutaan toisinaan myös turvakoodiksi. American Express -korteilla tämä luku on nelinumeroinen. Discover, MasterCard ja Visa -korteilla luku on kolminumeroinen.

### Osoitteen tarkistus
<a id="address-verification" class="xliff"></a>

Osoitteen varmennustiedot lähetetään aina maksupalvelulle. Voit päättää, kuinka paljon tietoja tarvitaan tapahtuman hyväksymiseksi. Muista varmistaa palveluntarjoajaltasi, voiko se hyväksyä näitä tietoja. Nämä ovat osoitetietojen varmennuksen vaihtoehdot:
-   **Hyväksy tapahtuma aina** – Hyväksy tapahtuma riippumatta osoitteen tarkistustuloksista.
-   **Tilin omistaja** – Vertaa kortinhaltijan nimeä tapahtumasta luottokorttiyhtiön tietoihin.
-   **Laskutusosoite** – Vertaa kortinhaltijan nimeä ja laskutusosoitetta tapahtumasta luottokorttiyhtiön tietoihin.
-   **Laskutusosoitteen postinumero** – Vertaa kortinhaltijan nimeä, laskutusosoitetta ja postinumeroa tapahtumasta luottokorttiyhtiön tietoihin.

## Tietotuki
<a id="data-support" class="xliff"></a>
Voit määrittää kullekin tukemallesi luottokorttityypille tuetun tiedon tason. Taso määrittää, kuinka paljon tietoja tapahtumasta siirretään maksupalvelulle. Muista varmistaa palveluntarjoajaltasi, voiko se tarjota näitä tietoja. Nämä ovat tietotuen tasoasetukset:
-   **Taso 1** – Siirrä tapahtuman päivämäärä, summa ja kuvaus.
-   **Taso 2** – Siirrä kaikki tason 1 tiedot sekä toimitusosoite, myyjän osoite ja verotiedot.
-   **Taso 3** – Siirrä kaikki tason 2 tiedot sekä tilausrivin tiedot.

## Osamaksut
<a id="partial-payments" class="xliff"></a>
Jos toimitat vain osan tilauksesta, osatilauksen määrä siepataan ja koko tilauksen määrälle tarkoitettu varmennus suljetaan. Toimittamattomalle tilausmäärälle luodaan sitten uusi varmennus.

## Varmennuksen mitätöinti 
<a id="voiding-an-authorization" class="xliff"></a>
Luottokortin varmennuksen voit mitätöidä vaihtamalla maksutavan sellaiseksi, jolla ei ole Luottokortti-tyyppiä.






