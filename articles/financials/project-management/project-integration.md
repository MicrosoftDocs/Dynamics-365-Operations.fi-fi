---
title: Microsoft Project -asiakasintegrointi
description: "Projektin aikataulun suunnittelu ja ylläpito voi olla monimutkaista, joten projektipäälliköt tarvitsevat työkaluja tämän tehtävän hallitsemiseen. Integrointi Microsoft Project -asiakkaan kanssa tukee projektityörakenteen avaamista ja hallintaa."
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4a3445417d5ae88e2ff3676962a82921a7ab475d
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="microsoft-project-client-integration"></a>Microsoft Project -asiakasintegrointi

[!include [banner](../includes/banner.md)]

Projektin aikataulun suunnittelu ja ylläpito voi olla monimutkaista, joten projektipäälliköt tarvitsevat työkaluja tämän tehtävän hallitsemiseen. Integrointi Microsoft Project -asiakkaan kanssa tukee projektityörakenteen avaamista ja hallintaa. Projektipäällikkö voi julkaista muutokset takaisin Finance and Operationsin projektityörakenteeseen.

> [!NOTE]
> Jos käytössä on Microsoft Dynamics 365 for Finance and Operations -sovelluksen heinäkuun 2017 päivitys, KB 4054797 ja 4055884 on asennettava.

## <a name="configure-the-microsoft-project-client-add-in"></a>Microsoft Project -asiakkaan lisäosan määrittäminen
Microsoft Project -asiakkaan integrointi edellyttää Microsoft Dynamics 365 -lisäosan asentamista käyttäjän Microsoft Project -asiakassovellukseen. Asennus tehdään avaamalla **Projektinhallinta-työtila**.

•   Valitse **Määritä Project-asiakkaan lisäosa** valitsemalla työtilassa **Linkit** > **Asetukset**.

•   Valitse ensin **Avaa** ja sitten pyydettäessä **Suorita**.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Aiemmin luodun työrakenneluonnoksen avaaminen ja muokkaaminen Microsoft Project -asiakkaassa
Jos Finance and Operationsin projektiin on jo luotu työrakenne, se voidaan avata Microsoft Project -asiakassovelluksessa, jos työrakenne on luonnostilassa. Jos haluat avata sen **Projekti**-sivulta, napsauta **Avaa Microsoft Projectissa** -linkkiä **Suunnitelma**-välilehdessä. Tämä sivu voidaan avata myös Microsoft Project -asiakassovelluksessa valitsemalla **Avaa** **Microsoft Dynamics 365** -välilehdessä. Valitse luettelossa **Yritys** ja **Projekti**.

> [!NOTE]
> Jos käytät Internet Explorer -selainta, sinun on valittava **Tallenna** ja avattava tiedosto manuaalisesti siitä sijainnista, johon tiedosto ladattiin. Vaihtoehtoisesti voit avata tiedoston Microsoft Project -asiakkaassa valitsemalla **Tallenna ja avaa**. Älä nimeä tiedostoa uudelleen tallennuksen yhteydessä.

Sinun on kuitattava tiedosto ulos, ennen kuin voit muokata sitä Microsoft Project -asiakkaassa. Valitse **Kuittaa ulos** **Microsoft Dynamics 365** -välilehdessä. Muut käyttäjät eivät voi nyt muokata työrakennetta Finance and Operationsissa samanaikaisesti. Voit julkaista työrakenteen muokkausten valmistumisen jälkeen valitsemalla **Kuittaa sisään** **Microsoft Dynamics 365** -välilehdessä.

Jos projektiryhmä on jo lisätty projektiin Finance and Operationsissa, ryhmän jäsenet lisätään resurssiluetteloon. Jos projektiryhmää ei ole vielä lisätty projektiin, voit valita resurssit ja muodostaa ryhmän Microsoft Project -asiakkaassa napsauttamalla **Resurssit**-painiketta **Microsoft Dynamics 365** -välilehdessä. 

Seuraavat tiedot synkronoidaan takaisin Finance and Operationsin osana sisäänkuittausta:

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

6.  Kun olet valmis julkaisemaan Finance and Operationsiin, valitse **Kuittaa sisään** **Microsoft Dynamics 365** -välilehdessä.

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

