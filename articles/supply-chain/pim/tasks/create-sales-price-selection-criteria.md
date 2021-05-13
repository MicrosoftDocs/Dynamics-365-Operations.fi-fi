---
title: Luo myyntihinnan valintaperusteet
description: Tässä toimintaohjeessa kuvataan, miten voit luoda myyntihinnan valintaehdon määriteperustaiselle myyntihintamallille.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920528"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="71cf1-103">Luo myyntihinnan valintaperusteet</span><span class="sxs-lookup"><span data-stu-id="71cf1-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71cf1-104">Tässä toimintaohjeessa kuvataan, miten voit luoda myyntihinnan valintaehdon määriteperustaiselle myyntihintamallille.</span><span class="sxs-lookup"><span data-stu-id="71cf1-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="71cf1-105">Tämän menettelyn suorittaminen edellyttää, että ainakin yksi myyntihintamalli on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="71cf1-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="71cf1-106">Tässä esimerkissä käytetään hintamallia esittelytietojen USMF-yrityksen Kaiutinratkaisu-hintamallissa.</span><span class="sxs-lookup"><span data-stu-id="71cf1-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="71cf1-107">Tämän tehtävän suorittaa yleensä tuotepäällikkö.</span><span class="sxs-lookup"><span data-stu-id="71cf1-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="71cf1-108">Uuden ehdon lisääminen vanhalle myyntihintamallille</span><span class="sxs-lookup"><span data-stu-id="71cf1-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="71cf1-109">Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.</span><span class="sxs-lookup"><span data-stu-id="71cf1-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="71cf1-110">Valitse luettelosta kaiutinratkaisun tuotemalli, mutta älä valitse mallinimen linkkiä.</span><span class="sxs-lookup"><span data-stu-id="71cf1-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="71cf1-111">Valitse toimintoruudussa **Malli**.</span><span class="sxs-lookup"><span data-stu-id="71cf1-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="71cf1-112">Valitse **Hintamalliehdot**.</span><span class="sxs-lookup"><span data-stu-id="71cf1-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="71cf1-113">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="71cf1-113">Select **New**.</span></span>
1. <span data-ttu-id="71cf1-114">Syötä **Nimi**-kenttään "Asiakasryhmä 10".</span><span class="sxs-lookup"><span data-stu-id="71cf1-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="71cf1-115">Valinnan ehdot tunnistetaan hinnoittelumallin ehdon nimen avulla.</span><span class="sxs-lookup"><span data-stu-id="71cf1-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="71cf1-116">Syötä tai valitse arvo kentässä **Hintamalli**.</span><span class="sxs-lookup"><span data-stu-id="71cf1-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="71cf1-117">Valitse **Tilaustyyppi**-kenttään *Myyntitilaus*.</span><span class="sxs-lookup"><span data-stu-id="71cf1-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="71cf1-118">Tilauksen tyyppi määrittää tietokannan kentät, jotka ovat saatavilla valintakyselyssä.</span><span class="sxs-lookup"><span data-stu-id="71cf1-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="71cf1-119">Kirjoita päivämäärä **Voimassaolo alkaa** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="71cf1-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="71cf1-120">Syötä päivämäärä **Vanhentuu**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="71cf1-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="71cf1-121">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="71cf1-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="71cf1-122">Luo kysely valintaperusteilla</span><span class="sxs-lookup"><span data-stu-id="71cf1-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="71cf1-123">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="71cf1-123">Select **Edit**.</span></span>
2. <span data-ttu-id="71cf1-124">Valitse *Asiakkaat* **Taulukko**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="71cf1-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="71cf1-125">Valitse **Kenttä**-kentässä *Asiakasryhmä*.</span><span class="sxs-lookup"><span data-stu-id="71cf1-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="71cf1-126">Tässä esimerkissä tiettyä asiakasryhmää valintakriteerinä.</span><span class="sxs-lookup"><span data-stu-id="71cf1-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="71cf1-127">Valitse **Ehto**-kentässä *Asiakasryhmä 10*.</span><span class="sxs-lookup"><span data-stu-id="71cf1-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="71cf1-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="71cf1-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]