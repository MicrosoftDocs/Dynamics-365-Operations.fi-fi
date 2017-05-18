---
title: "Luottokorttien määritys, varmennus ja sieppaaminen"
description: "Tässä artikkelissa on yhteenveto luottokortin varmennuksesta Microsoft Dynamics AX:ssä. Artikkeli sisältää tietoja maksupalvelun määrittämisestä, luottokortin lisäämisestä myyntitilaukseen ja varmennuksen mitätöinnistä."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 82cc16189bc8d57788711d8ba36070826271e3a9
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="credit-card-setup-authorization-and-capture"></a>Luottokorttien määritys, varmennus ja sieppaaminen

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on yhteenveto luottokortin varmennuksesta Microsoft Dynamics AX:ssä. Artikkeli sisältää tietoja maksupalvelun määrittämisestä, luottokortin lisäämisestä myyntitilaukseen ja varmennuksen mitätöinnistä.

<a name="setting-up-the-credit-card-payment-service"></a>Luottokorttien maksupalvelun määrittäminen
------------------------------------------

Jos haluat käyttää luottokortteja, sinun on määritettävä ja aktivoitava maksupalvelu Maksupalvelut-sivulla. Maksupalvelu toimii välittäjänä yrityksesi ja asiakkaan korttimaksut käsittelevän pankin välillä. Sinun on käytettävä luottokorttimaksun tarjoajaa, joka on saatavilla Maksuyhdistin-kentässä ja määrittää tili kyseiselle palveluntarjoajalle. Sinun on sitten määritettävä muut asetukset Maksupalvelut-sivulla, määritettävä luottokorttityypit American Express, Discover, MasterCard ja Visa -korteille Luottokorttityypit-sivulla ja aktivoitava palveluntarjoaja oletuspalveluntarjoajaksi. Sinun on myös noudatettava seuraavia vaiheita:
-   Määritä luottokortin varmennuksessa käytettävät parametrit Myyntireskontran parametrit -sivulla.
-   Määritä luottokorttien maksuehdot Maksuehdot-sivulla. Valitse Luottokortti Maksutyyppi-kentässä.
-   Syötä asiakkaan luottokorttitiedot Asiakkaan luottokortit -sivulla.

## <a name="adding-a-new-credit-card"></a>Uuden luottokortin lisääminen
Voit luoda uudet luottokorttitietueet Asiakkaat-sivulla kohdasta Asiakas > Määritä > Luottokortti. Voit myös luoda luottokorttitietueita kirjatessasi myyntitilauksia Myyntitilaus-sivulla kohdasta Hallinta > Asiakas > Luottokortti > Rekisteröi.
Luottokortin lisääminen myyntitilaukseen
-------------------------------------

Voit lisätä luottokortin myyntitilaukseen valitsemalla luottokortin Myyntitilaus-sivun Hinnat ja alennukset -pikavälilehden luottokorttihausta. Varmennusprosessin voit aloittaa valitsemalla toimintoruudun Hallinta-välilehdestä kohdan Luottokortti ja Varmenna.
Luottokortin varmennus
-------------------------

Kun luottokortti varmennetaan, kortin numero ja kortin haltijan henkilöllisyys varmennetaan ja käytettävissä oleva luottosaldo tarkistetaan. Voit myös tarkistaa kortin tarkistusnumeron ja kortinhaltijan osoitteen. Laskun summa vähennetään tämän jälkeen asiakkaan käytettävissä olevasta luottosaldosta. Maksupalvelu lähettää tiedon luottokortin hyväksymisestä tai hylkäämisestä. Kun myyntitilaus laskutetaan, laskun summa veloitetaan (siepataan) luottokortilta.

### <a name="card-verification-value"></a>Kortin tarkistusnumero

Voit vaatia kortin tarkistusarvon käyttöä, jota kutsutaan toisinaan myös turvakoodiksi. American Express -korteilla tämä luku on nelinumeroinen. Discover, MasterCard ja Visa -korteilla luku on kolminumeroinen.

### <a name="address-verification"></a>Osoitteen tarkistus

Osoitteen varmennustiedot lähetetään aina maksupalvelulle. Voit päättää, kuinka paljon tietoja tarvitaan tapahtuman hyväksymiseksi. Muista varmistaa palveluntarjoajaltasi, voiko se hyväksyä näitä tietoja. Nämä ovat osoitetietojen varmennuksen vaihtoehdot:
-   **Hyväksy tapahtuma aina** – Hyväksy tapahtuma riippumatta osoitteen tarkistustuloksista.
-   **Tilin omistaja** – Vertaa kortinhaltijan nimeä tapahtumasta luottokorttiyhtiön tietoihin.
-   **Laskutusosoite** – Vertaa kortinhaltijan nimeä ja laskutusosoitetta tapahtumasta luottokorttiyhtiön tietoihin.
-   **Laskutusosoitteen postinumero** – Vertaa kortinhaltijan nimeä, laskutusosoitetta ja postinumeroa tapahtumasta luottokorttiyhtiön tietoihin.

## <a name="data-support"></a>Tietotuki
Voit määrittää kullekin tukemallesi luottokorttityypille tuetun tiedon tason. Taso määrittää, kuinka paljon tietoja tapahtumasta siirretään maksupalvelulle. Muista varmistaa palveluntarjoajaltasi, voiko se tarjota näitä tietoja. Nämä ovat tietotuen tasoasetukset:
-   **Taso 1** – Siirrä tapahtuman päivämäärä, summa ja kuvaus.
-   **Taso 2** – Siirrä kaikki tason 1 tiedot sekä toimitusosoite, myyjän osoite ja verotiedot.
-   **Taso 3** – Siirrä kaikki tason 2 tiedot sekä tilausrivin tiedot.

## <a name="partial-payments"></a>Osamaksut
Jos toimitat vain osan tilauksesta, osatilauksen määrä siepataan ja koko tilauksen määrälle tarkoitettu varmennus suljetaan. Toimittamattomalle tilausmäärälle luodaan sitten uusi varmennus.

## <a name="voiding-an-authorization"></a>Varmennuksen mitätöinti 
Luottokortin varmennuksen voit mitätöidä vaihtamalla maksutavan sellaiseksi, jolla ei ole Luottokortti-tyyppiä.






