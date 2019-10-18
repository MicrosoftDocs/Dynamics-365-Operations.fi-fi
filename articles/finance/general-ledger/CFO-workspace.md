---
title: Taloushallinnon dimensioiden lisääminen talousjohtajan työtilaan
description: Tässä ohjeaiheessa kerrotaan, miten taloushallinnon dimensiot lisätään talousjohtajan työtilaan siten, että niitä voi käyttää kirjapito- ja budjettiraporteissa.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 3817c6688339735c7478e85786efe15bd2372c91
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177504"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="b8d42-103">Taloushallinnon dimensioiden lisääminen talousjohtajan työtilaan</span><span class="sxs-lookup"><span data-stu-id="b8d42-103">Add financial dimensions to the CFO workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8d42-104">Tässä ohjeaiheessa kerrotaan, miten taloushallinnon dimensiot lisätään talousjohtajan työtilaan siten, että niitä voi käyttää kirjapito- ja budjettiraporteissa.</span><span class="sxs-lookup"><span data-stu-id="b8d42-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="b8d42-105">Talousjohtajan työtilassa on **Yleiskatsaus**- ja **Taloushallinto**-välilehdet. Näiden välilehtien raportit perustuvat kahteen mittaan: LedgerActivityMeasure ja BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="b8d42-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="b8d42-106">Näiden kahden mitan ja DimensionCombinationEntity-yksikön välillä on suhde.</span><span class="sxs-lookup"><span data-stu-id="b8d42-106">There is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="b8d42-107">Tämän vuoksi dimensiot voidaan valita.</span><span class="sxs-lookup"><span data-stu-id="b8d42-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="b8d42-108">Päivitä Financen **Yksikkösäilö**-sivulla **LedgerActivityMeasure**- ja **BudgetActivityMeasure**-mitat.</span><span class="sxs-lookup"><span data-stu-id="b8d42-108">In Finance, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="b8d42-109">Avaa Microsoft Visual Studiossa Application Explorer ja tee haku hakusanalla **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="b8d42-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="b8d42-110">Avaa **Resurssit**-kohdassa **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="b8d42-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="b8d42-111">Kun resurssi avautuu Microsoft Power BI desktopissa, valitse ensin **Nouda tiedot**, sitten **SQL Server -tietokanta** ja lopuksi **Yhdistä**.</span><span class="sxs-lookup"><span data-stu-id="b8d42-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="b8d42-112">Anna ensin palvelimen nimi ja sitten tietokannaksi **AxDW**.</span><span class="sxs-lookup"><span data-stu-id="b8d42-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="b8d42-113">Valitse ensin **DirectQuery** ja sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8d42-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="b8d42-114">Etsi ja valitse **LedgerActivityMeasure\_DimensionCombination** ja valitse sitten **Lataa**.</span><span class="sxs-lookup"><span data-stu-id="b8d42-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="b8d42-115">Vaihda taulun nimeksi **Kentät**-luettelossa **Taloushallinnon dimensiot**, jotta se on helppo tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="b8d42-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="b8d42-116">Valitse ensin **Suhteiden hallinta** ja sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b8d42-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="b8d42-117">Valitse ensin ensimmäisessä kentässä **Kirjanpitotehtävät** ja sitten **LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="b8d42-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="b8d42-118">Valitse toisessa kentässä **LedgerActivityMeasure\_DimensionCombination** (tai **Taloushallinnon dimensiot**, jos muutit kentän nimen).</span><span class="sxs-lookup"><span data-stu-id="b8d42-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="b8d42-119">Valitse **DimensionCombinationRECID**-otsikko.</span><span class="sxs-lookup"><span data-stu-id="b8d42-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="b8d42-120">Valitse **Kardinaliteetti**-kentässä **Monta yhteen**.</span><span class="sxs-lookup"><span data-stu-id="b8d42-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="b8d42-121">Vaihda **Ristisuodatus**-arvoksi **Yksittäinen**.</span><span class="sxs-lookup"><span data-stu-id="b8d42-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="b8d42-122">Valitse ensin sekä **Tee tästä suhteesta aktiivinen** että **Oleta viite-eheys**, sitten **OK** ja lopuksi **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="b8d42-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="b8d42-123">[![Suhteen luominen](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="b8d42-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="b8d42-124">**Kentät**-luettelossa pitäisi olla taulu ja käytettävissä olevat taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="b8d42-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="b8d42-125">Vedä sopivat taloushallinnon dimensiot raporttitason suodattimiin.</span><span class="sxs-lookup"><span data-stu-id="b8d42-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="b8d42-126">Tallenna muutokset.</span><span class="sxs-lookup"><span data-stu-id="b8d42-126">Save your changes.</span></span>
15. <span data-ttu-id="b8d42-127">Napsauta sovellusobjektipuussa (AOT) hiiren kakkospainikkeella projektia ja valitse sitten **Synkronoi**.</span><span class="sxs-lookup"><span data-stu-id="b8d42-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="b8d42-128">Luo projekti ja tarkastele sitten tuloksia avaamalla sovellus.</span><span class="sxs-lookup"><span data-stu-id="b8d42-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="b8d42-129">[![Valmis työtila](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="b8d42-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>