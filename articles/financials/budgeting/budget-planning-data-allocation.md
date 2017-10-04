---
title: Budjettisuunnittelun tietojen kohdistus
description: "Tässä artikkelissa on tietoja Microsoft Dynamics 365 for Finance and Operationsin, Enterprise Editionin käytettävissä olevista kohdistustavoista ja niiden käyttämisestä."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: fc85775a27a160e951593bb9d40a6294af3ca329
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# <a name="budget-planning-data-allocation"></a>Budjettisuunnittelun tietojen kohdistus

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on tietoja Microsoft Dynamics 365 for Finance and Operationsin, Enterprise Editionin käytettävissä olevista kohdistustavoista ja niiden käyttämisestä.  

Voit jakaa tiedot budjettisuunnitelmaan useilla eri tavoilla arvioitujen summien kuvaamista varten.

## <a name="allocation-methods"></a>Kohdistusmenetelmät
Kolme kohdistusmenetelmää (Kohdista kausille, Kohdista dimensioille ja Käytä kirjanpidon kohdistussääntöjä) voivat luoda budjettisuunnitelman rivejä, jotka perustuvat saman budjettisuunnitelman riveihin. Kolme muuta menetelmään (Yhdistä, Jaa ja Kopioi budjettisuunnitelmasta) voivat luoda budjettisuunnitelman rivejä muissa budjettisuunnitelmissa. Jokaiselle kuudelle kohdistusmenetelmälle voi määrittää kohdeskenaarion. Kohdeskenaario voi olla sama kuin lähdeskenaario, mutta se voi olla myös erilainen. Lisäksi voit määrittää, lisätäänkö uudet rivit budjettisuunnitelmaan vai korvataanko budjettisuunnitelman nykyiset rivit.

[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Kohdista kausille** – Kaudenkohdistusluokkaa voi käyttää kohdistettaessa lähdebudjettiskenaarion budjettisuunnitelman rivit kohdeskenaarion kausiin. Lähdesumma liitetään kohdeskenaarion useisiin riveihin kaudenkohdistusluokassa määritetyn prosenttiosuuden ja päivämäärän perusteella.         

[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Kohdista dimensioille** – Budjettisuunnitelman rivit kohdistetaan lähdebudjettisuunnittelun skenaariosta kohdeskenaarion yhteen tai useaan riviin valitussa budjetin kohdistusehdossa määritettyjen prosenttiosuuksien ja taloushallinnon dimensioiden perusteella.           

![AggregateChart](./media/aggregatechart-300x230.png)
**Yhdistä** – Budjettisuunnitelman rivit yhdistetään liittyvien (alitason) budjettisuunnitelmien lähdebudjettiskenaariosta päätason budjettisuunnitelman kohdeskenaarioon. Tämän menetelmän avulla organisaation alemmalla tasolla valmistellut budjettisummat voidaan konsolidoida korkeammalla tasolla.          

[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Jaa** – Budjettisuunnitelman rivit jaetaan päätason budjettisuunnitelman lähdebudjettisuunnittelun skenaariosta liittyvän (alitason) budjettisuunnitelmien kohdeskenaarioon liittyvien suunnitelmien organisaatioyksiköiden taloushallinnon dimensioiden perusteella. Tämän menetelmän avulla organisaation korkeammalla tasolla valmistellut budjettisummat voidaan jakaa paikallisesti tarkastelua varten.           

[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Käytä kirjanpidon kohdistussääntöjä** – Budjettisuunnitelman rivit jaetaan lähdebudjettisuunnittelun skenaariosta kohdebudjettiskenaarioon valitun kirjanpidon kohdistussäännön perusteella. 

[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopioi budjettisuunnitelmasta** – Budjettirivit luodaan jaon kohdistusmenetelmän tapaan kohteessa liittyvän budjettisuunnitelman rivien perusteella. Tässä menetelmässä lähdebudjettisuunnitelman ei kuitenkaan tarvitse olla päätaso, mutta se voi olla mikä tahansa budjettisuunnitelman hierarkian korkeampi taso. Tämä kohdistusmenetelmä on hyödyllinen, jos konsolidoidut summat on alun perin budjetoitu paljon korkeammalla tasolla, mutta jotka on siirrettävä organisaation alemmalle tasolle yksityiskohtaista tarkastelua ja oikaisua varten ennen ylemmän tason hyväksynnän saavuttamista.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Kohdistusmenetelmien käyttäminen budjettisuunnitelmassa
Voit suorittaa kohdistuksia budjettisuunnitelman sivulla, kun valitset kohdistettavat rivit ja valitset sitten **Kohdista budjetti**.

[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

Valitse seuraavaksi kohdistusmenetelmä. Tämän jälkeen määritetään jäljellä olevat kentät valitun menetelmän mukaan. Nämä kentät sisältävät budjettisuunnitelman tietojen lähteen ja kohteen sekä vaihtoehdon, joka mahdollistaa lähteen kertomisen määritetyllä kertoimella kohdesummien luomisen yhteydessä. Tämä yksinkertaistaa joukko-oikaisua. Voit määrittää myös **Liitä suunnitelmaan** -vaihtoehdon. Korvaa aiemmin luodut budjettisuunnitelman rivit valitsemalla **Ei** tai säilytä aiemmin luodut budjettisuunnitelman rivit ja lisää uusia rivejä kohdistetuille summille valitsemalla **Kyllä**.

## <a name="automating-allocations-during-a-workflow"></a>Kohdistusten automatisointi työnkulun aikana
Kohdistukset voidaan suorittaa erään tehokkaan toiminnon avulla automaattisesti budjettisuunnittelun työnkulun osana. Budjettisuunnitelman siirtyessä työnkulussa, automaattiset tehtävät voivat käynnistää kohdistuksen tietyssä budjettisuunnittelun vaiheessa. 

Voit määrittää automaattisen kohdistuksen luomalla ensin kohdistusaikataulun **Budjettisuunnittelun konfigurointi** -sivulla. Kohdistusaikataulu määrittää kohdistusmenetelmä, jota käytetään automaattisen kohdistuksen suorituksen aikana, sekä eri kohdistusvaihtoehtojen arvot (kuvaukset löytyvät edellisestä osasta). 

Seuraavaksi luodaan vaiheen kohdistus **Budjettisuunnittelun konfigurointi** -sivulla. Vaiheen kohdistuksen liittää kohdistusaikataulun budjettisuunnittelun työnkulkuun ja vaiheeseen. 

Lopuksi lisätään budjettisuunnittelun vaiheen kohdistuksen haluttuun työnkulun vaiheeseen automaattinen tehtävä. Seuraavassa esimerkissä työnkulkuun on lisätty kaksi budjettisuunnittelun vaiheen kohdistusta (näkyvät punaisina).

[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)



