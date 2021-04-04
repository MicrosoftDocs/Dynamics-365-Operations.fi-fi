---
title: Ongelmien vianmääritys alkumäärityksen aikana
description: Tässä ohjeaiheessa on tietoja, joiden avulla voidaan korjata kaksoiskirjoituksen integroinnin alkuasennuksen aikana esiintyviä ongelmia.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f6ff9a304de8a94b86e6866d6d2cb65fbfdfb02f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561175"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Ongelmien vianmääritys alkumäärityksen aikana

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Dataversen välillä. Erityisesti se tarjoaa tietoa vianmääritystietoja, joiden avulla voit korjata ongelmat, joita voi ilmetä kaksoiskirjoituksen integroinnin alkuasennuksen aikana.

> [!IMPORTANT]
> Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Et voi linkittää Finance and Operations -sovellusta Dataverseen

**Kaksoiskirjoituksen asettamiseen vaadittava rooli:** Järjestelmän ylläpitäjä Finance and Operations -sovelluksissa ja Dataversessä.

**Asennuslinkki Dataverseen** -sivulla olevat virheet johtuvat yleensä puutteellisista määritys- tai käyttöoikeusongelmista. Varmista, että koko terveystarkistus siirtyy **Asennuslinkillä Dataverseen**, kuten seuraavasta kuvasta käy ilmi. Kaksoiskirjoittamista ei voi linkittää, ellei koko terveystarkistus ole ohi.

![Onnistunut kuntotarkistus](media/health_check.png)

Sinulla on oltava Azure AD -vuokralaisen järjestelmänvalvojan käyttöoikeudet Finance and Operations- ja Dataverse -ympäristöjen linkittämiseen. Kun olet linkittänyt ympäristöt, käyttäjät voivat kirjautua sisään käyttämällä tilinsä tunnistetietoja ja päivittää aiemmin luotua taulujen yhdistämiskarttaa.

## <a name="error-when-you-open-the-link-to-dataverse-page"></a>Virhe avatessasi linkin Dataverse -sivulle

**Ongelman korjauksen edellyttämät tunnistetiedot:** Azure AD -vuokralaisten hallinta

Näyttöön saattaa tulla seuraava virhesanoma, kun avaat **Linkin Dataverse** -sivulle Finance and Operations -sovelluksessa:

*Vastauksen tilakoodi ei tarkoita onnistumista: 404 (Ei löydetty).*

Tämä virhe ilmenee, kun suostumusvaihetta ei ole suoritettu. Voit tarkistaa, onko suostumus vaihesuoritettu, kirjautumalla kohteeseen portal.Azure.com käyttämällä Azure AD -vuokralaisen järjestelmänvalvojan tiliä ja katsomalla, näkyykö kolmannen osapuolen sovellusta, jonka tunnus **33976c19-1db5-4c02-810e-c243db79efde** Azure AD:ssa, **Yrityssovellukset**-luettelossa. Jos näin ei ole, sinun on annettava sovelluksen suostumus.

Voit antaa sovelluksen suostumuksen noudattamalla seuraavia ohjeita.

1. Avaa seuraava URL-osoite käyttämällä järjestelmänvalvojan tunnistetietoja. Sinua pyydetään antamaan suostumus.

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. Valitse **Hyväksy**, jos haluat ilmaista suostumuksesi siihen, että asennat sovelluksen, jonka tunnus **33976c19-1db5-4c02-810e-c243db79efde** on vuokralaisella.

    > [!TIP]
    > Tämä sovellus edellyttää Dataversen ja Finance and Operations -sovellusten linkittämistä. Jos tässä vaiheessa ilmenee ongelmia, avaa selain incognito-tilassa (Google Chromessa) tai InPrivate-tilassa (Microsoft Edgessä).

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>Varmista, että yrityksen tiedot ja kaksoiskirjoitusryhmät on määritetty oikein linkittämisen aikana

Jos haluat varmistaa, että kaksoiskirjoitus toimii oikein, konfiguroinnin aikana valitsemasi yritykset luodaan Dataverse -ympäristöön. Oletusarvon mukaan nämä yritykset ovat vain luku -tilassa ja **IsDualWriteEnable**-ominaisuuden arvo on **True**. Lisäksi luodaan oletusarvon mukainen liiketoimintayksiköiden omistaja ja ryhmä ja lisätään yrityksen nimi. Ennen kuin otat kartat käyttöön, varmista, että ryhmän oletusomistaja on määritetty. Voit etsiä **Yritykset (CDM\_Yritys)** -taulukon seuraavasti.

1. Valitse Dynamics 365:n mallipohjaisen sovelluksen oikeasta yläkulmasta suodatin.
2. Valitse avattavasta luettelosta **Yritys**.
3. Voit tarkastella tuloksia valitsemalla **Suorita**.
4. Valitse yritys, joka on linkitetty kaksoiskirjoituksen määrityksen yhteydessä.
5. Varmista, että **Omistavan oletusryhmän** -sarakkeessa on arvo. Seuraavassa kuvassa **Omistavan oletusryhmän** -sarakkeen arvoksi on määritetty **USMF-kaksoiskirjoitus**.

    ![Omistavan oletusryhmän tarkistaminen](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Kaksoiskirjoittamiseen liittyvien lakitaulujen tai yritysten määrän rajoittaminen

Näyttöön saattaa tulla seuraava virhesanoma, kun yrität ottaa yhdistämismäärityksiä käyttöön:

*Kaksoiskirjoitusvirhe - Laajennuksen rekisteröiminen epäonnistui: \[(Osiokarttaa ei voitu saada projektille DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Virhe ylittää DWM-määrityksen enimmäisosiot DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], tapahtui virheitä.*

Tämänhetkinen raja-arvo, kun linkität ympäristöjä, on noin 40 lakitaulua. Tämä virhe ilmenee, jos yrität ottaa käyttöön yhdistämisen ja yli 40 taulua linkitetään ympäristöjen välillä.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]