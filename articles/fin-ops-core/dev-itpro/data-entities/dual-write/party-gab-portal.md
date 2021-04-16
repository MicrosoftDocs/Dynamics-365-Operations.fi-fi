---
title: Power Portalin käyttö osapuolen tietomallin kanssa
description: Tässä ohjeaiheessa kuvataan Power Portalin verkkorooleihin kaksoiskirjoituksen osapuolen tietomallin vuoksi tehdyt muutokset.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833087"
---
# <a name="using-power-portal-with-the-party-data-model"></a>Power Portalin käyttö osapuolen tietomallin kanssa

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

Kaksoiskirjoituksen sovellusorkestrointiratkaisun versio 2.0.999.0 ja uudemmat sisältävät tietomallin muutokset Tili- ja Yhteyshenkilö-tauluihin osapuolen ja yleisessä osoitekirjassa. Muutokset mahdollistavat monta-moneen-suhteet, jotka tukevat kehittyneitä liiketoimintaskenaarioita. Näitä muutoksia eivät tue portaalin verkkoroolit, mukaan lukien asiakasportaali, jotka toimitetaan käyttövalmiina tai jotka olivat ympäristössäsi ennen kaksoiskirjoituksen asentamista. Jotta verkkoroolit toimisivat odotetulla tavalla, sinun on luotava uusia verkkorooleja uuden tietomallin avulla. 

Yhteenvetona voidaan sanoa, että taulukoiden vuorovaikutus on muuttunut, mutta asiakasportaalin taulukon käyttöoikeudet eivät ole muuttuneet. Tässä ohjeaiheessa kerrotaan, miten luodaan uusia verkkorooleja, jotka toimivat uuden kehittyneen tietomallin kanssa.

Tässä kaaviossa esitetään taulukon yhteys **ilman** osapuolen ja yleisen osoitekirjan tietomallia:

   ![ilman osapuolimallia](media/without-party-model.PNG)

Tässä kaaviossa esitetään taulukon yhteys osapuolen ja yleisen osoitekirjan tietomallin **kanssa**:

   ![osapuolimallin kanssa](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Uuden taulukon käyttöoikeuden luominen

Voit luoda nämä uudet taulukon käyttöoikeudet seuraavasti:

1. Kirjaudu [Power Appsiin](https://make.powerapps.com) ja siirry sovelluksiisi.
2. Valitse Portaalin hallinta -sovellus.
3. Valitse sivupalkista **Suojaus > Taulukon käyttöoikeudet**.

    Sinun on luotava kolme uutta käyttöoikeutta:

    + Yhteyshenkilö-Osapuoli-yhteys
    + Osapuoli-Tili-yhteys
    + Tili-Tilaus-yhteys

4. Luo ja tallenna Yhteyshenkilö-Osapuoli-yhteyden uusi käyttöoikeus ja määritä nämä parametrit:

    + **Nimi**: Osapuoli-Tili-yhteys (tai valintasi)
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
