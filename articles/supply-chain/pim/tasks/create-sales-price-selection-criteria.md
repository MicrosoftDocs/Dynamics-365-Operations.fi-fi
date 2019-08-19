---
title: Luo myyntihinnan valintaperusteet
description: Tässä toimintaohjeessa kuvataan, miten voit luoda myyntihinnan valintaehdon määriteperustaiselle myyntihintamallille.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72940f719baca5e8042c2f2caa8abbacb7d8264e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844486"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="c5791-103">Luo myyntihinnan valintaperusteet</span><span class="sxs-lookup"><span data-stu-id="c5791-103">Create sales price selection criteria</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5791-104">Tässä toimintaohjeessa kuvataan, miten voit luoda myyntihinnan valintaehdon määriteperustaiselle myyntihintamallille.</span><span class="sxs-lookup"><span data-stu-id="c5791-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="c5791-105">Tämän menettelyn suorittaminen edellyttää, että ainakin yksi myyntihintamalli on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="c5791-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="c5791-106">Tässä esimerkissä käytetään hintamallia esittelytietojen USMF-yrityksen Kaiutinratkaisu-hintamallissa.</span><span class="sxs-lookup"><span data-stu-id="c5791-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="c5791-107">Tämän tehtävän suorittaa yleensä tuotepäällikkö.</span><span class="sxs-lookup"><span data-stu-id="c5791-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="c5791-108">Uuden ehdon lisääminen vanhalle myyntihintamallille</span><span class="sxs-lookup"><span data-stu-id="c5791-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="c5791-109">Valitse Tuotevarianttimallin määritys.</span><span class="sxs-lookup"><span data-stu-id="c5791-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="c5791-110">Valitse Tuotekonfiguraation mallit.</span><span class="sxs-lookup"><span data-stu-id="c5791-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="c5791-111">Valitse luettelosta kaiutinratkaisun tuotemalli, mutta älä napsauta mallinimen linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c5791-111">In the list, select the row for the Speaker solution product model, but don’t click the link for the model name.</span></span>
4. <span data-ttu-id="c5791-112">Valitse toimintoruudussa Malli.</span><span class="sxs-lookup"><span data-stu-id="c5791-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="c5791-113">Valitse Hintamalliehdot.</span><span class="sxs-lookup"><span data-stu-id="c5791-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="c5791-114">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c5791-114">Click New.</span></span>
7. <span data-ttu-id="c5791-115">Syötä Nimi-kenttään "Asiakasryhmä 10".</span><span class="sxs-lookup"><span data-stu-id="c5791-115">In the Name field, type ‘Customer group 10’.</span></span>
    * <span data-ttu-id="c5791-116">Valinnan ehdot tunnistetaan hinnoittelumallin ehdon nimen avulla.</span><span class="sxs-lookup"><span data-stu-id="c5791-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="c5791-117">Syötä tai valitse arvo kentässä Hintamalli.</span><span class="sxs-lookup"><span data-stu-id="c5791-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="c5791-118">Valitse Tilaustyyppi-kenttään Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="c5791-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="c5791-119">Tilauksen tyyppi määrittää tietokannan kentät, jotka ovat saatavilla valintakyselyssä.</span><span class="sxs-lookup"><span data-stu-id="c5791-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="c5791-120">Kirjoita päivämäärä Voimassaolo alkaa -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c5791-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="c5791-121">Syötä päivämäärä Vanhentuu-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c5791-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="c5791-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c5791-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="c5791-123">Luo kysely valintaperusteilla</span><span class="sxs-lookup"><span data-stu-id="c5791-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="c5791-124">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="c5791-124">Click Edit.</span></span>
2. <span data-ttu-id="c5791-125">Valitse Asiakkaat Taulukko-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c5791-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="c5791-126">Valitse Kenttä-kentässä Asiakasryhmä.</span><span class="sxs-lookup"><span data-stu-id="c5791-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="c5791-127">Tässä esimerkissä tiettyä asiakasryhmää valintakriteerinä.</span><span class="sxs-lookup"><span data-stu-id="c5791-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="c5791-128">Valitse Ehto-kentässä Asiakasryhmä 10.</span><span class="sxs-lookup"><span data-stu-id="c5791-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="c5791-129">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c5791-129">Click OK.</span></span>

