---
title: Ongelmien vianmääritys alkumäärityksen aikana
description: Tässä ohjeaiheessa on vianmääritystietoja, joiden avulla voit korjata ongelmat, joita voi ilmetä, kun Finance and Operations -sovellusten ja Common Data Service -ohjelmien välinen kaksoiskirjoitus integroidaan.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: e20c9c5e1250c8e65b5642a7c45d7ae859315697
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172665"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Ongelmien vianmääritys alkumäärityksen aikana

[!include [banner](../../includes/banner.md)]



Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä. Erityisesti se tarjoaa tietoa vianmääritystietoja, joiden avulla voit korjata ongelmat, joita voi ilmetä kaksoiskirjoituksen integroinnin alkuasennuksen aikana.

> [!IMPORTANT]
> Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a>Et voi linkittää Finance and Operations -sovellusta Common Data Serviceen

**Kaksoiskirjoituksen asetusten edellyttämät tunnistetiedot:** Azure AD -vuokralaisten hallinta

**Asennuslinkki Common Data Serviceen** -sivulla olevat virheet johtuvat yleensä puutteellisista määritys- tai käyttöoikeusongelmista. Varmista, että koko terveystarkistus siirtyy **Asennuslinkillä Common Data Serviceen**, kuten seuraavasta kuvasta käy ilmi. Kaksoiskirjoittamista ei voi linkittää, ellei koko terveystarkistus ole ohi.

![Onnistunut kuntotarkistus](media/health_check.png)

Sinulla on oltava Azure AD -vuokralaisen järjestelmänvalvojan käyttöoikeudet Finance and Operations- ja Common Data Service -ympäristöjen linkittämiseen. Kun olet linkittänyt ympäristöt, käyttäjät voivat kirjautua sisään käyttämällä tilinsä tunnistetietoja ja päivittää aiemmin luotua yksikön yhdistämiskarttaa.

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a>Virhe avatessasi linkin Common Data Service -sivulle

**Ongelman korjauksen edellyttämät tunnistetiedot:** Azure AD -vuokralaisten hallinta

Näyttöön saattaa tulla seuraava virhesanoma, kun avaat **Linkin Common Data Service** -sivulle Finance and Operations -sovelluksessa:

*Vastauksen tilakoodi ei tarkoita onnistumista: 404 (Ei löydetty).*

Tämä virhe ilmenee, kun suostumusvaihetta ei ole suoritettu. Voit tarkistaa, onko suostumus vaihesuoritettu, kirjautumalla kohteeseen portal.Azure.com käyttämällä Azure AD -vuokralaisen järjestelmänvalvojan tiliä ja katsomalla, näkyykö kolmannen osapuolen sovellusta, jonka tunnus **33976c19-1db5-4c02-810e-c243db79efde** Azure AD:ssa, **Yrityssovellukset**-luettelossa. Jos näin ei ole, sinun on annettava sovelluksen suostumus.

Voit antaa sovelluksen suostumuksen noudattamalla seuraavia ohjeita.

1. Avaa seuraava URL-osoite käyttämällä järjestelmänvalvojan tunnistetietoja. Sinua pyydetään antamaan suostumus.

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. Valitse **Hyväksy**, jos haluat ilmaista suostumuksesi siihen, että asennat sovelluksen, jonka tunnus **33976c19-1db5-4c02-810e-c243db79efde** on vuokralaisella.

    > [!TIP]
    > Tämä sovellus edellyttää Common Data Servicen ja Finance and Operations -sovellusten linkittämistä. Jos tässä vaiheessa ilmenee ongelmia, avaa selain incognito-tilassa (Google Chromessa) tai InPrivate-tilassa (Microsoft Edgessä).

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>Varmista, että yrityksen tiedot ja kaksoiskirjoitusryhmät on määritetty oikein linkittämisen aikana

Jos haluat varmistaa, että kaksoiskirjoitus toimii oikein, konfiguroinnin aikana valitsemasi yritykset luodaan Common Data Service -ympäristöön. Oletusarvon mukaan nämä yritykset ovat vain luku -tilassa ja **IsDualWriteEnable**-ominaisuuden arvo on **True**. Lisäksi luodaan oletusarvon mukainen liiketoimintayksiköiden omistaja ja ryhmä ja lisätään yrityksen nimi. Ennen kuin otat kartat käyttöön, varmista, että ryhmän oletusomistaja on määritetty. Voit etsiä **Yritykset (CDM\_Yritys)** -kohteen seuraavasti.

1. Valitse Dynamics 365:n mallipohjaisen sovelluksen oikeasta yläkulmasta suodatin.
2. Valitse avattavasta luettelosta **Yritys**.
3. Voit tarkastella tuloksia valitsemalla **Suorita**.
4. Valitse yritys, joka on linkitetty kaksoiskirjoituksen määrityksen yhteydessä.
5. Varmista, että **Omistavan oletusryhmän** -kentässä on arvo. Seuraavassa kuvassa **Omistavan oletusryhmän** -kentän arvoksi on asetettu **USMF-kaksoiskirjoitus**.

    ![Omistavan oletusryhmän tarkistaminen](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a>Kaksoiskirjoittamiseen liittyvien oikeussubjektien tai yritysten määrän rajoittaminen

Näyttöön saattaa tulla seuraava virhesanoma, kun yrität ottaa yhdistämismäärityksiä käyttöön:

*Kaksoiskirjoitusvirhe - Laajennuksen rekisteröiminen epäonnistui: \[(Osiokarttaa ei voitu saada projektille DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Virhe ylittää DWM-määrityksen enimmäisosiot DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], tapahtui virheitä.*

Tämänhetkinen raja-arvo, kun linkität ympäristöjä, on noin 40 oikeussubjektia. Tämä virhe ilmenee, jos yrität ottaa käyttöön yhdistämisen ja yli 40 yritystä linkitetään ympäristöjen välillä.
