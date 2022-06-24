---
title: Microsoft Power Apps -portaalien käyttö osapuolen tietomallin kanssa
description: Tässä artikkelissa kuvataan Microsoft Power Apps -portaalien verkkorooleihin kaksoiskirjoituksen osapuolen tietomallin vuoksi tehdyt muutokset.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: c2e9d0f47ef90167bf84bb5b20e6a7ad2d58ffd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898943"
---
# <a name="using-microsoft-power-apps-portals-with-the-party-data-model"></a>Microsoft Power Apps -portaalien käyttö osapuolen tietomallin kanssa

[!INCLUDE[banner](../../includes/banner.md)]



Kaksoiskirjoituksen sovellusorkestrointiratkaisun versio 2.0.999.0 ja uudemmat sisältävät tietomallin muutokset Tili- ja Yhteyshenkilö-tauluihin osapuolen ja yleisessä osoitekirjassa. Muutokset mahdollistavat monta-moneen-suhteet, jotka tukevat kehittyneitä liiketoimintaskenaarioita. Näitä muutoksia eivät tue portaalin verkkoroolit, mukaan lukien asiakasportaali, jotka toimitetaan käyttövalmiina tai jotka olivat ympäristössäsi ennen kaksoiskirjoituksen asentamista. Jotta verkkoroolit toimisivat odotetulla tavalla, sinun on luotava uusia verkkorooleja uuden tietomallin avulla. 

Yhteenvetona voidaan sanoa, että taulukoiden vuorovaikutus on muuttunut, mutta asiakasportaalin taulukon käyttöoikeudet eivät ole muuttuneet. Tässä artikkelissa kerrotaan, miten luodaan uusia verkkorooleja, jotka toimivat uuden kehittyneen tietomallin kanssa.

Tässä kaaviossa esitetään taulukon yhteys **ilman** osapuolen ja yleisen osoitekirjan tietomallia:

   ![ilman osapuolimallia.](media/without-party-model.PNG)

Tässä kaaviossa esitetään taulukon yhteys osapuolen ja yleisen osoitekirjan tietomallin **kanssa**:

   ![osapuolimallin kanssa.](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Uuden taulukon käyttöoikeuden luominen

Voit luoda nämä uudet taulukon käyttöoikeudet seuraavasti:

1. Kirjaudu [Power Appsiin](https://make.powerapps.com) ja siirry sovelluksiisi.
2. Valitse Portaalin hallinta -sovellus.
3. Valitse sivupalkista **Suojaus > Taulukon käyttöoikeudet**.

    Sinun on luotava kolme uutta käyttöoikeutta:

    + **Yhteyshenkilö**- ja **Osapuoli**-taulun yhteys
    + **Osapuoli**- ja **Tili**-taulun yhteys
    + **Tili**- ja **Järjestys**-taulun yhteys

4. Luo ja tallenna Yhteyshenkilö-Osapuoli-yhteyden uusi käyttöoikeus ja määritä nämä parametrit:

    + **Nimi**: **Osapuoli**- ja **Tili**-taulun yhteys (tai valintasi)
    + **Taulukon nimi**: msdyn_contactforparty
    + **Sivusto**: Asiakasportaali
    + **Laajuus**: Yhteyshenkilö
    + **Oikeudet**: Valitse kaikki
    + **Verkkoroolit**: Todennetut käyttäjät, asiakasedustaja (tai valintasi)

5. Luo ja tallenna Osapuoli-Tili-yhteyden uusi käyttöoikeus ja määritä nämä parametrit:

    + **Nimi**: Osapuoli-Tili-yhteys (tai valintasi)
    + **Taulukon nimi**: account
    + **Sivusto**: Asiakasportaali
    + **Laajuus**: Ylätaso
    + **Oikeudet**: Valitse kaikki
    + **Ylätason taulukon oikeudet**: Yhteyshenkilö-Osapuoli-yhteys

6. Luo ja tallenna Tili-Tilaus-yhteyden uusi käyttöoikeus ja määritä nämä parametrit:

    + **Nimi**: Tili-Tilaus-yhteys (tai valintasi)
    + **Taulukon nimi**: salesorder
    + **Sivusto**: Asiakasportaali
    + **Laajuus**: Ylätaso
    + **Oikeudet**: Valitse kaikki
    + **Ylätason taulukon oikeudet**: Osapuoli-Tili-yhteys

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
