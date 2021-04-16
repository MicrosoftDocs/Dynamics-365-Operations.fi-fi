---
title: Tuotannon suunnittelu
description: Tässä aiheessa käsitellään tuotannon suunnittelua ja suunniteltujen tuotantotilausten muokkaamista tuotannon optimoinnin avulla.
author: ChristianRytt
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 22b78f44940f71097ca8b1cdb74edb06274bba75
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839220"
---
# <a name="production-planning"></a>Tuotannon suunnittelu

Suunnittelun optimointi tukee useita tuotantoskenaarioita. Jos siirtyminen tapahtuu nykyisestä sisäisestä pääsuunnittelumoduulista, on tärkeää ottaa huomioon tietyt toiminnasta tapahtuneet muutokset.

Seuraavassa videossa esitetään lyhyt johdanto joihinkin tässä aiheessa käsiteltyihin käsitteisiin: [Dynamics 365 Supply Chain Management: Suunnitteluoptimoinnin parannukset](https://youtu.be/u1pcmZuZBTw).

## <a name="turn-on-this-feature-for-your-system"></a>Tämän ominaisuuden ottaminen käyttöön järjestelmällesi

Jos järjestelmäsi ei vielä sisällä tässä aiheessa kuvattuja ominaisuuksia, avaa [Ominaisuuksien hallinta](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota *Suunnitellut tuotantotilaukset tuotannon optimoinnille* -ominaisuus käyttöön.

## <a name="planned-production-orders"></a>Suunnitellut tuotantotilaukset

Kun pääsuunnittelu täyttää tarpeita luomalla suunniteltuja tilauksia, tilauksen tyyppi määritetään **Suunniteltu tilaustyyppi** -kentän arvon perusteella. Jos **Suunniteltu tilaustyyppi** -kentän asetuksena on *Tuotanto*, luodaan suunniteltuja tuotantotilauksia. Näissä suunnitelluissa tuotantotilauksissa on tietoja aktiivisista tuoterakenteista ja liittyvän tuotantomäärityksen reititystunnus.

## <a name="requirements-from-boms"></a>Tuoterakenteiden tarpeet

Tuoterakennetiedot otetaan huomioon pääsuunnittelun aikana. Suunnittelutulos sisältää materiaalin oston, joka kattaa tuotantoon liittyvän materiaalin kysynnän.

Pääsuunnittelun aikana nykyisen aktiivisen tuoterakenteen avulla määritetään tuotantoa varten tarvittavat materiaalit. Tämä vaihe tehdään kaikilla tarvittavaan tuotantotilaukseen liittyvillä tuoterakenteen tasoilla. Materiaalitarve täytetään käyttämällä käytettävissä olevaa varastoa, nykyistä tilausvarastoa ja hyväksyttyjä suunniteltuja tilauksia. Jos jossakin tarvitaan lisämateriaalia, kysyntää varten luodaan suunniteltu tilaus.

## <a name="scheduling-during-firming"></a>Aikatauluttaminen vahvistuksen aikana

Suunnitellut tuotantotilaukset sisältävä reititystunnuksen, jota tarvitaan tuotannon aikatauluttamiseen. Suunniteltujen tilausten aikataulutuksen tukea suunnitteluajon aikana odotetaan. Reititystunnusta käytetään suunniteltujen tuotantotilausten aikatauluttamiseen vahvistuksen aikana. Tämän vuoksi suunniteltujen tuotantotilausten läpimenoaika voi olla erilainen kuin niistä luotujen liittyvien aikataulutettujen ja vahvistettujen tuotantotilausten läpimenoaika. Selitys:

- **Suunniteltu tuotantotilaus** – läpimenoaika perustuu vapautetun tuotteen staattiseen läpimenoaikaan.
- **Vahvistettu tuotantotilaus** – läpimenoaika perustuu reititystietoja ja liittyviä resurssirajoituksia käyttävään aikataulutukseen.

Lisätietoja toiminnon odotetusta saatavuudesta on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md).

Jos tarvitset sellaista tuotannon toimintoa, joka ei ole vielä saatavana tuotannon optimoinnissa, voit jatkaa sisäisen pääsuunnittelumoduulin käyttöä. Mitään poikkeusta ei tarvita.

## <a name="delays"></a>Viiveet

Jos tarvittavan materiaalin läpimenoaika on pidempi kuin kuluvan päivän ja materiaalin tarvepäivän väliin jäävä jakso, tarvittavan materiaalin ja liittyvän tuotantotilauksen suunniteltu tilaus viivästyy. Viive lasketaan suunnitelluissa tilauksissa vapautetun tuotteen läpimenoajan perusteella. Tämän jälkeen viivetiedot leviävät sitten kaikille tuoterakenteen tasoille. Tällä tavoin viivästyneen raaka-aineen vaikutusta voidaan seurata asiakkaan myyntitilaukseen saakka.

## <a name="modifying-planned-orders"></a>Suunniteltujen tilausten muokkaaminen

Suunnitellun tilauksen tietojen muuttaminen aiheuttaa seuraavan sanoman: Huomaa, että suunniteltujen tilausten manuaaliset muutokset näkyvät muualla suunnitelmassa vasta seuraavan pääsuunnitteluajon jälkeen.

Suunniteltuun tilaukseen tehdyn muutoksen vaikutus liittyviin materiaalitarpeisiin saadaan näkyviin seuraavasti:

1. Päivitä suunniteltu tilaus.
2. Hyväksy suunniteltu tilaus.
3. Suorita pääsuunnittelu.

Jos suunnitellut tuotantotilaukset sisältyvät suoritettavaan pääsuunnitteluun, suodattimia ei voi käyttää. Lisätietoja on myöhemmin tässä aiheessa kohdassa [Suodattimet](#filters).

> [!NOTE]
> Jos suunnitellun tilauksen toimituspäivä muutetaan myöhempään ajankohtaan, tarvekohdistus saatetaan tehdä uuden suunnitellun tilauksen perusteella. Näin tapahtuu, jos uusi tarjontapäivä viivästyttää tarvekohdistusta mutta läpimenoasetusten perusteella viive voidaan välttää.

## <a name="explosion-page"></a>Hajotussivu

**Hajotus**-sivulla voidaan analysoida tietyn tuotantotilauksen tai suunnitellun tuotantotilauksen, liittyvän kattavuuden ja tarvekohdistustietojen kysyntää. **Hajotus**-sivun tiedot päivitetään pääsuunnittelun aikana. Tietoja ei voi päivittää suoraan **Hajotus**-sivulta.

## <a name="filters"></a><a name="filters"></a>Suodattimet

Tuotannon sisältävissä suunnitteluskenaarioissa ei kannata käyttää suodatettuja pääsuunnitteluajoja, Jotta suunnittelun optimoinnilla on varmasti kaikki tiedot, joita tarvitaan oikean tuloksen laskemiseen, siihen on sisällyttävä kaikki tuotteet, jotka liittyvät jollain tavoin koko suunnitellun tilauksen tuoterakenteeseen.

Vaikka riippuvaiset alikohteet havaitaan automaattisesti ja sisällytetään pääsuunnitteluajoihin sisäistä pääsuunnittelumoduulia käytettäessä, niin ei tapahdu suunnittelun optimoinnissa.

Jos esimerkiksi yhtä tuotteen A tuoterakenteen pulttia käytetään myös tuotteen B tuottamiseen, kaikkien tuotteiden A ja B tuoterakenteiden tuotteiden on sisällyttävä suodattimeen. Koska voi olla erittäin monimutkaista varmistaa, että kaikki tuotteet sisältyvät suodattimeen, suodatettuja pääsuunnitteluajoja kannattaa välttää, jos kyse on tuotantotilauksesta.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]