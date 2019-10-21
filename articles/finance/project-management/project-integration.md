---
title: Microsoft Project -asiakasintegrointi
description: Projektin aikataulun suunnittelu ja ylläpito voi olla monimutkaista, joten projektipäälliköt tarvitsevat työkaluja tämän tehtävän hallitsemiseen. Integrointi Microsoft Project -asiakkaan kanssa tukee projektityörakenteen avaamista ja hallintaa.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 610990612d5fb38025bf39cc648d0c9572da37b6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174837"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project -asiakasintegrointi

[!include [banner](../includes/banner.md)]

Projektin aikataulun suunnittelu ja ylläpito voi olla monimutkaista, joten projektipäälliköt tarvitsevat työkaluja tämän tehtävän hallitsemiseen. Integrointi Microsoft Project -asiakkaan kanssa tukee projektityörakenteen avaamista ja hallintaa. Projektipäällikkö voi julkaista muutokset takaisin Dynamics 365 Financen projektityörakenteeseen.

> [!NOTE]
> Jos käytät heinäkuun päivitystä (versio 10.0.4), sinun täytyy asentaa KB 4054797 ja 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Microsoft Project -asiakkaan lisäosan määrittäminen
Microsoft Project -asiakkaan integrointi edellyttää Microsoft Dynamics 365 -lisäosan asentamista käyttäjän Microsoft Project -asiakassovellukseen. Asennus tehdään avaamalla **Projektinhallinta-työtila**.

•   Valitse **Määritä Project-asiakkaan lisäosa** valitsemalla työtilassa **Linkit** > **Asetukset**.

•   Valitse ensin **Avaa** ja sitten pyydettäessä **Suorita**.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Aiemmin luodun työrakenneluonnoksen avaaminen ja muokkaaminen Microsoft Project -asiakkaassa
Jos Dynamics 365 Financen projektiin on jo luotu työrakenne, se voidaan avata Microsoft Project -asiakassovelluksessa, jos työrakenne on luonnostilassa. Jos haluat avata sen **Projekti**-sivulta, napsauta **Avaa Microsoft Projectissa** -linkkiä **Suunnitelma**-välilehdessä. Tämä sivu voidaan avata myös Microsoft Project -asiakassovelluksessa valitsemalla **Avaa** **Microsoft Dynamics 365** -välilehdessä. Valitse luettelossa **Yritys** ja **Projekti**.

> [!NOTE]
> Jos käytät Internet Explorer -selainta, sinun on valittava **Tallenna** ja avattava tiedosto manuaalisesti siitä sijainnista, johon tiedosto ladattiin. Vaihtoehtoisesti voit avata tiedoston Microsoft Project -asiakkaassa valitsemalla **Tallenna ja avaa**. Älä nimeä tiedostoa uudelleen tallennuksen yhteydessä.

Sinun on kuitattava tiedosto ulos, ennen kuin voit muokata sitä Microsoft Project -asiakasohjelmassa. Valitse **Kuittaa ulos** **Microsoft Dynamics 365** -välilehdessä. Tämä estää muita käyttäjiä muokkaamasta työrakennetta Financessa samanaikaisesti. Voit julkaista työrakenteen muokkausten valmistumisen jälkeen valitsemalla **Kuittaa sisään** **Microsoft Dynamics 365** -välilehdessä.

Jos projektiryhmä on jo lisätty projektiin Financessa, ryhmän jäsenet lisätään resurssiluetteloon. Jos projektiryhmää ei ole vielä lisätty projektiin, voit valita resurssit ja muodostaa ryhmän Microsoft Project -asiakkaassa napsauttamalla **Resurssit**-painiketta **Microsoft Dynamics 365** -välilehdessä. 

Seuraavat tiedot synkronoidaan takaisin Financeen osana sisäänkuittausta:

•   Tehtävän nimi

•   Aloituspäivä

•   Valmistumispäivä

•   Edeltäjät

•   Resurssinimet

•   Luokka

•   Resurssiluokka

•   Työtunnit

•   Muistiinpanot

•   Prioriteetti

> [!NOTE]
> Jos lisäät muita sarakkeita Microsoft Project -asiakastiedostoon, niitä ei tallenneta tiedostoon eivätkä ne näy, kun tiedosto avataan seuraavan kerran.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Työrakenteen luominen aiemmin luodulle projektille Microsoft Project -asiakkaan avulla
Voit luoda uuden työrakenteen projektille Microsoft Project -asiakkaan avulla seuraavien ohjeiden avulla:


1.  Avaa Microsoft Project -asiakas.

2.  Valitse **Microsoft Dynamics 365** -välilehdessä **Avaa**.

3.  Valitse projektille **Yritys**.

4.  Valitse **Projekti**.

5.  Valitse **Kuittaa ulos** **Microsoft Dynamics 365** -välilehdessä.

6.  Kun olet valmis julkaisemaan Financeen, valitse **Kuittaa sisään** **Microsoft Dynamics 365** -välilehdessä.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Aiemmin luodun projektin aiemmin luodun työrakenteen korvaaminen Microsoft Project -asiakkaan avulla
Voit luoda uuden työrakenteen käyttämällä Microsoft Project -asiakasta ja korvata aiemmin luodun projektin aiemmin luodun työrakenteen seuraavien ohjeiden avulla:

1.  Avaa Microsoft Project -asiakas.

2.  Luo Microsoft Project -asiakkaassa aikataulu.

3.  Valitse **Microsoft Dynamics 365** -välilehdessä **Tallenna muutokset** > **Korvaa aiemmin luotu projekti**.

4.  Valitse projektille **Yritys**.

5.  Valitse **Projekti**.

6.  Napsauta **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Uuden projektin luominen Microsoft Project -asiakkaassa


1.  Avaa Microsoft Project -asiakas.

2.  Luo Microsoft Project -asiakkaassa aikataulu.

3.  Valitse **Microsoft Dynamics 365** -välilehdessä **Tallenna muutokset** > **Tallenna uuteen projektiin**.

4.  Valitse projektille **Yritys**.

5.  Anna **projektitunnus** tarvittaessa.

6.  Anna **projektin nimi**.

7.  Valitse **Projektityyppi**, **Projektiryhmä** ja **Projektisopimuksen tunnus**. Vaihtoehtoisesti voit luoda uuden projektisopimuksen valitsemalla **Uusi**.

8.  Valitse resursoinnissa käytettävä **kalenteri**.

11. Napsauta **OK**.
