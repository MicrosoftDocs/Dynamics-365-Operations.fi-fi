---
title: "Luottokorttien määritys, varmennus ja sieppaaminen"
description: "Tässä artikkelissa on Microsoft Dynamics 365 for Finance and Operationsissa tehtävän luottokortin varmennuksen yleiskatsaus. Artikkeli sisältää tietoja maksupalvelun määrittämisestä, luottokortin lisäämisestä myyntitilaukseen ja varmennuksen mitätöinnistä."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4a6354563fdebff901498f1cd6caed3aedae668b
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="credit-card-setup-authorization-and-capture"></a>Luottokorttien määritys, varmennus ja sieppaaminen

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Tässä artikkelissa on Microsoft Dynamics 365 for Finance and Operationsissa tehtävän luottokortin varmennuksen yleiskatsaus. Artikkeli sisältää tietoja maksupalvelun määrittämisestä, luottokortin lisäämisestä myyntitilaukseen ja varmennuksen mitätöinnistä.

<a name="setting-up-the-credit-card-payment-service"></a>Luottokorttien maksupalvelun määrittäminen
------------------------------------------

Jos haluat käyttää luottokortteja, sinun on määritettävä ja aktivoitava maksupalvelu Maksupalvelut-sivulla. Maksupalvelu toimii välittäjänä yrityksesi ja asiakkaan korttimaksut käsittelevän pankin välillä. Sinun on käytettävä luottokorttimaksun tarjoajaa, joka on saatavilla Maksuyhdistin-kentässä ja määrittää tili kyseiselle palveluntarjoajalle. Sinun on sitten määritettävä muut asetukset Maksupalvelut-sivulla, määritettävä luottokorttityypit American Express, Discover, MasterCard ja Visa -korteille Luottokorttityypit-sivulla ja aktivoitava palveluntarjoaja oletuspalveluntarjoajaksi. Sinun on myös noudatettava seuraavia vaiheita:
-   Määritä luottokortin varmennuksessa käytettävät parametrit Myyntireskontran parametrit -sivulla.
-   Määritä luottokorttien maksuehdot Maksuehdot-sivulla. Valitse Luottokortti Maksutyyppi-kentässä.
-   Syötä asiakkaan luottokorttitiedot Asiakkaan luottokortit -sivulla.

## <a name="adding-a-new-credit-card"></a>Uuden luottokortin lisääminen
Voit luoda uudet luottokorttitietueet Asiakkaat-sivulla kohdasta Asiakas > Määritä > Luottokortti. Voit myös luoda luottokorttitietueita kirjatessasi myyntitilauksia Myyntitilaus-sivulla kohdasta Hallinta > Asiakas > Luottokortti > Rekisteröi.

<a name="adding-a-credit-card-to-a-sales-order"></a>Luottokortin lisääminen myyntitilaukseen
-------------------------------------

Voit lisätä luottokortin myyntitilaukseen valitsemalla luottokortin Myyntitilaus-sivun Hinnat ja alennukset -pikavälilehden luottokorttihausta. Varmennusprosessin voit aloittaa valitsemalla toimintoruudun Hallinta-välilehdestä kohdan Luottokortti ja Varmenna.

<a name="authorizing-a-credit-card"></a>Luottokortin varmennus
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






