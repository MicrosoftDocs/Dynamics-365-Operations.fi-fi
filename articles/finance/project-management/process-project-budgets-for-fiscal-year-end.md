---
title: Projektibudjettien siirtäminen tilikauden lopussa
description: Tässä artikkelissa annetaan tietoja jäljellä olevien budjettisummien siirtämisestä tuleville vuosille ja budjettirekisteritietojen luomisesta.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172327"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Projektibudjettien siirtäminen tilikauden lopussa

[!include [banner](../includes/banner.md)]

Kun työskentelet usean vuoden projektissa, sinulla voi olla jäljellä olevaa budjettia tilikauden lopussa. Voit siirtää jäljellä olevat budjettimäärät tulevaan vuoteen ja luoda budjettirekisteritiedot niihin liittyvien pääkirjatilien summille. Tarkista ja analysoi jäljellä olevat budjettisummat ennen jäljellä olevien summien eteenpäin suorittamista.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Jäljellä olevien budjettisummien tarkasteleminen ja analysoiminen

Suorita seuraavat toimet tarkastaaksesi projektien tilinpäätöksen budjettisummat, mutta älä siirrä summia eteenpäin.

1. Siirry kohtaan **Projektinhallinta- ja kirjanpito** > **Kausittainen** > **Budjetit** > **Siirrettävät budjetit**. 
2. Tarkista **Projektibudjetin siirtoprosessi** -sivun **Vuoden lopun asetukset** -välilehdessä, että**Siirrettävät jäljellä olevat projektibudjetin summat** -vaihtoehto ei ole käytössä.
3. Valitse **Parametrit**-ryhmän **Projektin budjettivuosi** -kentästä se tilikausi, jonka projektien jäljellä olevaa budjettisummaa haluat tarkastella. 
4. Valitse **Avaa tilikausi** -kentästä sen tilikauden alku, jonka jäljellä olevaa budjettisummaa haluat tarkastella. 
5. Valitse **Ennustemallista**-kentästä **Jäljellä oleva budjetti**. 
6. Jos haluat sisällyttää projektit, jotka vastaavat valittuja ehtoja ja joilla ei ole jäljellä olevaa budjettia, valitse **Näytä nolla jäljellä**.  
7. Valitse **Valitse budjetit** -välilehdestä**Hae kaikki budjetit**, jos haluat ladata kaikki valittuja ehtoja vastaavat budjetit, ja valitse sitten **Prosessi**. 
8. Suunnitellaksesi tietokantakyselyn, joka lataa ruutuun tietyn joukon projektibudjetteja, napsauta **Hae valitut budjetit**.

Lisätietoja tietystä ruudun rivistä saat valitsemalla rivin ja valitsemalla sitten **Näytä budjetin tiedot** tai **Näytä tilit**.

## <a name="carry-forward-remaining-budget-amounts"></a>Tee siirtokirjaus jäljellä olevista budjettisummista 

Kun käsittelet jäljellä olevat budjettisummat, voit luoda kirjanpitoon tapahtuman siirtokirjatuista summista. Jos haluat luoda kirjanpidon tapahtumia, täytä osan vaiheet, [Siirrä budjettisummat ja luo kirjanpidon tapahtumat](#carry-forward). 

> [!NOTE]
> Siirtokirjatut budjettisummat siirretään ennustemalliin, joka valitaan siirtokirjausmalliksi **Ennustemallit** -sivulla.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Budjettisummien siirtokirjaaminen ja kirjanpitotapahtumien luonti

1.  Valitse **Projektinhallinta- ja kirjanpito** > **Kausittainen** > **Budjetit** > **Siirrettävät budjetit**. 
2. Valitse **projektibudjetin siirtoprosessi** -sivulla **Vuoden loppu** ja ota sitten **Siirrä jäljellä olevat projektin budjettisummat** käyttöön ja **Luo budjettirekisterimerkinnät kirjanpitoon**. 
3. Valitse **Parametrit**-välilehden **Projektin parametrit** -kenttäryhmästä seuraavat asiat:

   - **Projektibudjetin vuosi**: Valitse sen tilikauden alku, jonka jäljellä olevia budjettisummia haluat tarkastella. 
   - **Voitto ja tappio**: Luo voitto- ja tappiotapahtumat kirjanpitoon. 
   -  **KET**: Luo keskeneräisten töiden (KET) tapahtumia kirjanpitoon.
   -  **Palkanlaskenta**: Luo palkanlaskennan tapahtumat kirjanpitoon. 

5. Anna seuraavat tiedot **Kirjanpito**-kenttärymässä: 

   - Valitse **Tilikauden avaus**-kentästä se tilikausi, jolle haluat siirtää projektien jäljellä olevat budjettisummat. Oletusarvo on vuoden kuluttua **Projektibudjetin vuosi** -kentän arvosta.
   -  Valitse **Siirtokirjausjakso** -kentässä ajanjakso, johon haluat luoda kirjanpidon budjettirekisteritiedot. Tämä on yleensä uuden tilikauden ensimmäinen jakso.

6. Anna seuraavat tiedot **Kopioi jostakin/johonkin** -kenttäryhmässä:

   - Valitse **Ennustemallista** -kentässä projektibudjetin ennustemalli, joka liittyy jäljellä oleviin budjettisummiin, jotka haluat siirtää projekteille. 
   - Valitse **Kirjanpidon budjettimalli** -kentässä kirjanpidon budjettimalli, joka liittyy jäljellä kirjanpitoon siirrettäviin budjettisummiin. 
   -  Jos haluat käyttää projektin myyntivaluuttaa niihin kirjanpidon tapahtumiin, jotka luodaan, kun siirrät budjettisummat projekteille, valitse **Siirrä myyntivaluutta** -valintaruutu. Kun vaihtoehto ei ole valittuna, tapahtumat käyttävät kirjanpitovaluuttaa. 
   -  Valitse **Näytä nolla jäljellä** jos haluat sisällyttää projektit, joilla ei ole jäljellä olevia budjettimääriä, mutta jotka täyttävät muut perusteet, jotka valitsit alaruudussa näkyvissä projekteissa.

7. Valitse **Valitse budjetit** -välilehdestä **Hae kaikki budjetit**, jos haluat ladata kaikki valittuja ehtoja vastaavat budjetit. Jos haluat suunnitella tietokantakyselyn, joka lataa ruutuun tietyn joukon projektibudjetteja, napsauta **Hae valitut budjetit**.
8. Valitse kunkin haluamasi projektin kohdalla projektirivin alussa oleva vaihtoehto.

    > [!TIP]
    > Jos haluat valita kaikki projektit tai useimmat niistä, valitse vasemmassa yläkulmassa oleva valintamerkki. Jos haluat jättää minkä tahansa projektin käsittelyn pois, poista kyseisen projektin valintamerkki.

9. Jos haluat siirtää valittujen projektien jäljellä olevat budjettimäärät valitulle tilikaudelle ja luoda budjettirekisteritiedot pääkirjaan, valitse **Prosessi**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Budjettisummien siirtokirjaaminen ilman kirjanpitotapahtumien luontia

1. Siirry kohtaan **Projektinhallinta- ja kirjanpito** > **Kausittainen** > **Budjetit** > **Siirrettävät budjetit**.
2. Valitse **Projektibudjetin siirtoprosessi** -sivun **Vuoden lopun asetukset** -välilehdessä **Siirrettävät jäljellä olevat projektibudjetin summat**.
3. Valitse **Parametrit**-ryhmän **Projektin budjettivuosi** -kentästä se tilikausi, jonka projektien jäljellä olevaa budjettisummaa haluat tarkastella.
4. Anna seuraavat tiedot **Kopioi jostakin/johonkin** -ryhmässä:

   - Valitse **Ennustemallista** -kentässä projektibudjetin ennustemalli, joka liittyy jäljellä oleviin budjettisummiin, jotka haluat siirtää projekteille. 
   - Valitse **Näytä nolla jäljellä**, jos haluat sisällyttää projektit, jotka vastaavat valittuja ehtoja ja joilla ei ole jäljellä olevaa budjettia.
   - Valitse **Valitse budjetit** -ryhmästä **Hae kaikki budjetit**, jos haluat ladata kaikki valittuja ehtoja vastaavat budjetit. Suunnitellaksesi tietokantakyselyn, joka lataa ruutuun tietyn joukon projektibudjetteja, napsauta **Hae valitut budjetit**.

5. Valitse kunkin haluamasi projektin kohdalla projektirivin alussa oleva vaihtoehto. 
6. Valitse **Prosessi** siirtääksesi valittujen hankkeiden jäljellä olevat budjettisummat valitulle tilikaudelle.

