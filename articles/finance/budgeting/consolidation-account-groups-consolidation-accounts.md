---
title: Konsolidointitiliryhmät ja lisäkonsolidointitilit
description: Tässä ohjeaiheessa on tietoja konsolidointitiliryhmistä ja lisäkonsolidointitileistä ja siinä kerrotaan, kuinka niitä käytetään Microsoft Dynamics 365 Financessa.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8db7a60656434aafd8114b08c2c0e9493140f27b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177569"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="3859d-103">Konsolidointitiliryhmät ja lisäkonsolidointitilit</span><span class="sxs-lookup"><span data-stu-id="3859d-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3859d-104">Tässä ohjeaiheessa on tietoja konsolidointitiliryhmistä ja lisäkonsolidointitileistä ja siinä kerrotaan, kuinka niitä käytetään Microsoft Dynamics 365 Financessa.</span><span class="sxs-lookup"><span data-stu-id="3859d-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 Finance.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="3859d-105">Konsolidointitiliryhmät</span><span class="sxs-lookup"><span data-stu-id="3859d-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="3859d-106">Konsolidointitiliryhmien avulla voit luoda tiliryhmiä, joita haluat käyttää tietojen konsolidointiin.</span><span class="sxs-lookup"><span data-stu-id="3859d-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="3859d-107">Useimmiten konsolidointitiliryhmä vastaa hallituksen määräämää tilikarttaa tai yhdistää tilit ryhmään, joka on määritetty yrityksen pääkonttorissa.</span><span class="sxs-lookup"><span data-stu-id="3859d-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="3859d-108">Löydät konsolidoinnin tiliryhmät **Konsolidoinnit**-moduulin **Määritys**-alueelta.</span><span class="sxs-lookup"><span data-stu-id="3859d-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="3859d-109">Kun lisäät uuden ryhmän, kirjoita tiliryhmän yksilöivä tunnus sekä nimi.</span><span class="sxs-lookup"><span data-stu-id="3859d-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="3859d-110">Lisäkonsolidointitilit</span><span class="sxs-lookup"><span data-stu-id="3859d-110">Additional consolidation accounts</span></span>
<span data-ttu-id="3859d-111">Lisäkonsolidointitilien avulla voit liittää tilin aiemmin luodusta tilikartasta konsolidoinnin tiliryhmään.</span><span class="sxs-lookup"><span data-stu-id="3859d-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="3859d-112">Sitten voit määrittää konsolidointitilin arvon ja nimen.</span><span class="sxs-lookup"><span data-stu-id="3859d-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="3859d-113">Löydät konsolidoinnin lisätiliryhmät **Konsolidoinnit**-moduulin **Määritys**-alueelta.</span><span class="sxs-lookup"><span data-stu-id="3859d-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="3859d-114">Kun luot uuden konsolidointitilin, sinun on määritettävä seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="3859d-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="3859d-115">**Päätili** – kenttä on valinta, joka näyttää kaikki päätilit, jotka perustuvat tilikarttaan, jonka valitsit sivulla.</span><span class="sxs-lookup"><span data-stu-id="3859d-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="3859d-116">Kun valitset tilin, sen nimi syötetään automaattisesti **Päätilin nimi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3859d-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="3859d-117">**Konsolidointitiliryhmä** – Tämän kentän avulla voit määrittää ryhmän, johon tili määritetään.</span><span class="sxs-lookup"><span data-stu-id="3859d-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="3859d-118">Jos konsolidoit kahdella eri tavalla, sama tili pitää lisätä kaikkiin neljään konsolidointitiliryhmään.</span><span class="sxs-lookup"><span data-stu-id="3859d-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="3859d-119">**Konsolidointitili** – Anna konsolidointitilin arvo.</span><span class="sxs-lookup"><span data-stu-id="3859d-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="3859d-120">Tämän arvon ei tarvitse olla tilikartan tili.</span><span class="sxs-lookup"><span data-stu-id="3859d-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="3859d-121">Se voi olla mikä tahansa arvo, jota tarvitset.</span><span class="sxs-lookup"><span data-stu-id="3859d-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="3859d-122">**Konsolidointitilin nimi** – Kirjoita tilin nimi muodossa, jossa haluat sen näkyvän kyselyissä ja raporteissa.</span><span class="sxs-lookup"><span data-stu-id="3859d-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="3859d-123">**SAT-taso** – tätä kenttää käytetään ilmoittamaan tiliotteet Meksikon veroviranomaisille.</span><span class="sxs-lookup"><span data-stu-id="3859d-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="3859d-124">Kun olet luonut konsolidointitiliryhmät ja lisäkonsolidointilit, voit valita ryhmän Konsolidoi verkossa -prosessissa.</span><span class="sxs-lookup"><span data-stu-id="3859d-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="3859d-125">Lisätietoja on ohjeaiheessa [Konsolidaatioryhmien ja lisäkonsolidaatiotilien luominen](../general-ledger/tasks/create-consolidation-groups.md)</span><span class="sxs-lookup"><span data-stu-id="3859d-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 


