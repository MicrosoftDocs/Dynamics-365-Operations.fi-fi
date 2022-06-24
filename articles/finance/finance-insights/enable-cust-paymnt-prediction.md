---
title: Asiakkaan maksuennusteiden ottaminen käyttöön
description: Tässä artikkelissa kerrotaan, miten Asiakkaan maksuennusteet -toiminto otetaan käyttöön ja määritetään Finance Insightsissa.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f04ee9db5efe3595dea30d641c5097d6b90c0d77
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898204"
---
# <a name="enable-customer-payment-predictions"></a>Asiakkaan maksuennusteiden ottaminen käyttöön

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten Asiakkaan maksuennusteet -toiminto otetaan käyttöön ja määritetään Finance Insightsissa. Toiminto otetaan käyttöön **Ominaisuuksien hallinta** -työtilassa ja määritysasetukset annetaan **Finance Insights -määritykset** -sivulla. Tämä artikkeli sisältää tietoja, joiden avulla voit käyttää toimintoa tehokkaasti.

> [!NOTE]
> Ennen kuin suoritat seuraavat vaiheet, varmista, että olet suorittanut ennalta suoritettavat vaiheet [Määritykset Finance Insightsia varten](configure-for-fin-insites.md) -artikkelista.

1. Asiakkaan maksuennusteet -toiminnon ottaminen käyttöön:

    1. Avaa **Ominaisuuksien hallinta** -työtila.
    2. Valitse **Tarkista päivitysten saatavuus**.
    3. Käytä **Kaikki**-välilehdessä hakusanaa **Asiakkaan maksuennusteet**. Jos toimintoa ei löydy, käytä hakusanaa **(Esiversio) Asiakkaan maksuennusteet**. 
    4. Ota toiminto käyttöön.

    Asiakkaan maksuennusteet -toiminto on nyt käytössä ja valmis määritettäväksi.

2. Määritä Asiakasmaksun tiedot -toiminto:

    1. Valitse **Luotonvalvonta \> Asetukset \> Finance Insights \> Asiakkaan maksuennusteet**.
    2. Valitse **Finance Insights -määritykset** -sivun **Asiakkaan maksuennusteet** -välilehdessä **Ennustemallissa käytettyjen tietokenttien tarkasteleminen** -linkki ja avaa **Ennustemallin tietokentät** -sivu. Siellä voit tarkastella oletusluetteloa kentistä, joita käytetään asiakkaan maksuennusteiden tekoälyennustemallissa.

        Jos haluat käyttää kenttien oletusluetteloa ja luoda ennustemallin, sulje **Ennustemallin tietokentät** -sivu ja määritä sitten **Finance Insights -määritykset** -sivu ja **Ota toiminto käyttöön** -vaihtoehdon arvoksi **Kyllä**.
        
   > [!NOTE]
   > **Asiakkaan maksuennusteet**-toiminto edellyttää yli 100 tapahtumaa 6–9 edellisen kuukauden ajalta. Tapahtumia voivat olla esimerkiksi vapaatekstilaskut, myyntitilauksia ja asiakasmaksut. Tietojen on oltava jaettuna asetusten **Ajoissa**, **Myöhässä** ja **Paljon myöhässä** kesken.    
     

    3. Määrtä erittäin paljon myöhässä -tapahtumakausi, jotta voit määrittää, mitä **Erittäin paljon myöhässä** -ennustesäilö tarkoittaa yrityksessä.

        Järjestelmä ennustaa avoimen laskun maksun todennäköisyyden kolmen säilön avulla: **Ajoissa**, **Myöhässä** ja **Erittäin paljon myöhässä**.

        - **Ajoissa** – Tämä säilö sisältää maksut, jotka on ennustettu maksettavaksi ajoissa tai ennen tapahtuman eräpäivää.
        - **Myöhässä** – Tämä säilö sisältää maksut, jotka on ennustettu maksettavaksi tapahtuman eräpäivän jälkeen, mutta ennen Erittäin paljon myöhässä -tapahtumakautta.
        - **Erittäin paljon myöhässä** – Tämä säilö sisältää maksut, jotka on ennustettu maksettavaksi Erittäin paljon myöhässä -tapahtumakauden alun jälkeen.

        > [!NOTE]
        > Jos muutat Erittäin paljon myöhässä -tapahtumakautta ja valitset **Muuta myöhäistä rajaa** -arvoa asiakasmaksujen tekoälyennustemallin luomisen jälkeen, olemassa oleva ennustemalli poistetaan ja uusi luodaan. Uusi ennustemalli siirtää tapahtumat Erittäin paljon myöhässä -kauteen määritettyjen asetusten perusteella.

    4. Kun Erittäin paljon myöhässä -tapahtumakausi on määritetty, valitse **Luo ennustemalli** ja luo ennustemalli. **Finance Insights -määritykset** -sivun **Ennustemalli**-osassa näkyy ennustemallin tila.

        > [!NOTE]
        > Kun ennustemallia luodaan, voit käynnistää prosessin uudelleen valitsemalla **Nollaa mallin luominen**.

    Toiminto on nyt määritetty ja valmis käytettäväksi.

Kun toiminto on otettu käyttöön ja määritetty sekä ennustemalli luotu ja toiminnassa, **Finance Insights -parametrit** -sivun **Ennustemalli**-osa näyttää mallin tarkkuuden seuraavan kuvan mukaisesti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
