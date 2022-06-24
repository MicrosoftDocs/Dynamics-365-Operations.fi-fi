---
title: Palvelujen välisen todennuksen määrittäminen
description: Tässä artikkelissa kuvataan, kuinka määritetään huollon todennuksen määrittäminen Microsoft Dynamics 365 Commercessa niin, että luokitukset ja arviot kutsuvat palvelun sovellusliittymiä suojatusti.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: acb3a6220d146d32bbeb5bd8169033bc897ec3fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871604"
---
# <a name="configure-service-to-service-authentication"></a>Palvelujen välisen todennuksen määrittäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka sivustojen välinen (S2S) -todennus määritetään Microsoft Dynamics 365 Commercessa kutsumaan turvallisesti palvelusovellusohjelmointirajapintoja (API) arvioita ja arvosteluja varten.

Dynamics 365 Commerce tarjoaa [luokitukset ja arvostelut](ratings-reviews-overview.md) monikanavaratkaisuna. Tämä ratkaisu mahdollistaa huollon API:n käytön Commercen ulkopuolelta, jotta erilaisia tehtäviä voidaan suorittaa. Näitä tehtäviä ovat luokitusten ja arviointien tuominen ulkoisesta järjestelmästä Commerceen sekä luokitusten ja arviointien vieminen Commerce-järjestelmästä. Jotta Commerce voi kutsua luokitus- ja arvostelupalvelusovellusliittymiä turvallisesti, sinun on ensin määritettävä S2S-todennus suorittamalla tämän artikkelin toimenpiteet.

## <a name="add-a-new-app-registration"></a>Lisää uusi sovelluksen rekisteröinti

Ennen uuden sovellusrekisteröinnin lisäystä sinun on luotava sovellus, jossa voit käyttää [Azure Portalia](https://portal.azure.com). Rekisteröi sovellus Azure Active Directoryssä (Azure AD) ja ota todennus käyttöön noudattamalla kohdan [Käytä Azure Active Directoryn mukautettua liitintä Power Automate -sovelluksessa](/connectors/custom-connectors/azure-active-directory-authentication) ohjeita.

Kerää seuraavat tunnukset Azure-portaalista. Näitä tunnuksia tarvitaan seuraavien vaiheiden mukaisesti.

- Asiakassovelluksen tunnus
- Asiakashakemiston (vuokraajan) tunnus

Uuden sovelluksen rekisteröinti lisätään sivulle Commercen sivustonmuodostimessa seuraavasti.

1. Siirry kohtaan **Aloitus \> Arvostelut \> Asetukset**.
1. Valitse **Sivustojen välisen yhteyden (S2S) -todennus** -kohdasta **Hallinnoi**.

    ![Commercen sivustonmuodostimen sivustojen välisen yhteyden (S2S) -todennuksen osan Hallinta-painike.](media/Ratings-reviews-settings-service-to-service-authentication.png)

1. Valitse oikealla kentässä näkyvästä **S2S-sovelluksen merkinnät** -ruudusta **Lisää uusi S2S-sovelluksen rekisteröinti**.
1. Anna seuraavat vaaditut tiedot **Lisää S2S-sovelluksen merkintä** -valintaikkunassa. Käytä Azure-sovellusrekisteröinnin arvoja.

    - **Nimi** – Syötä sovelluksen nimi (esimerkiksi **Fabrikam-sovellus**).
    - **Asiakassovelluksen tunnus** – Syötä sovelluksen tunnus (esimerkiksi **00000000-0000-0000-0000-000000000000**).
    - **Hakemistotunnus (Vuokraaja)** – Kirjoita hakemiston tunnus (esimerkiksi **00000000-0000-0000-0000-000000000000**).

    ![Lisää S2S-sovelluksen merkintä -valintaikkuna Commerce-sivuston luontiohjelmassa.](media/Ratings-reviews-settings-S2S-APP-entry.png)

1. Valitse **Lähetä**. Sovelluksesi nimi tulisi nyt näkyä luettelossa **S2S-sovelluksen merkinnät** -ruudussa.
1. Sulje **S2S-sovelluksen merkintä** -ruutu.
1. Valitse **Tallenna**.

## <a name="edit-an-existing-app-registration"></a>Aiemmin luodun sovellusrekisteröinnin muokkaaminen

Olemassa olevan sovelluksen rekisteröintiä muokataan Commercen sivustonmuodostimessa seuraavasti.

1. Siirry kohtaan **Aloitus \> Arvostelut \> Asetukset**.
1. Valitse **Sivustojen välisen yhteyden (S2S) -todennus** -kohdasta **Hallinnoi**.
1. Valitse **S2S App Entries** -ruudussa kynäsymboli muokattavan merkinnän vieressä.
1. Päivitä **Nimi**-, **Asiakassovellustunnus**- ja **Hakemiston (Tenant) tunnus** -kenttien arvot tarpeen mukaan.
1. Valitse **Lähetä**.
1. Sulje **S2S-sovelluksen merkintä** -ruutu.
1. Valitse **Tallenna**.

## <a name="remove-an-existing-app-registration"></a>Aiemmin luodun sovellusrekisteröinnin poistaminen

Olemassa olevan sovelluksen rekisteröinti poistetaan Commercen sivustonmuodostimessa seuraavasti.

1. Siirry kohtaan **Aloitus \> Arvostelut \> Asetukset**.
1. Valitse **Sivustojen välisen yhteyden (S2S) -todennus** -kohdasta **Hallinnoi**.
1. Valitse **S2S App Entries** -ruudussa roskakorisymboli poistettavan merkinnän vieressä. Merkintä poistetaan luettelosta.
1. Sulje **S2S-sovelluksen merkintä** -ruutu.
1. Valitse **Tallenna**.

## <a name="additional-resources"></a>Lisäresurssit

[Luokitukset ja arvostelut – yleiskatsaus](ratings-reviews-overview.md)

[Luokitusten ja arvostelujen käytön hyväksyminen](opt-in-ratings-reviews.md)

[Hallitse luokituksia ja arvosteluja](manage-reviews.md)

[Määritä luokitukset ja arvostelut](configure-ratings-reviews.md)

[Synkronoi tuoteluokitukset](sync-product-ratings.md)

[Salli valvojan julkaista luokituksia ja arvosteluja manuaalisesti](manual-publish-rating-reviews.md)

[Luokitusten ja arvostelujen tuominen ja vieminen](import-export-reviews.md)

[Luokitusten ja arvostelujen usein kysytyt kysymykset](ratings-reviews-faq.md) 
