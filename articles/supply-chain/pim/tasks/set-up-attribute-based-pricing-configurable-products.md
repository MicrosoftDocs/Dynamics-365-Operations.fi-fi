---
title: Määritä määrittäville tuotteille määritepohjainen hinnoittelu
description: Tässä aiheessa kerrotaan, miten määritepohjainen hinnoittelu määritetään.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d23030b79670e31cc237b9ca53b0b3881678786f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149823"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="ee6ae-103">Määritä määrittäville tuotteille määritepohjainen hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="ee6ae-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee6ae-104">Tässä aiheessa kerrotaan, miten määritepohjainen hinnoittelu määritetään.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="ee6ae-105">Edellytyksenä on oltava tuotemääritysmalli, jolla on yksi tai useampi osa ja määrite.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="ee6ae-106">Tämä esimerkki käyttää USMF-yrityksen demotietojen korkealaatuista kaiutinmallia.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="ee6ae-107">Tämän tehtävän suorittaa yleensä tuotepäällikkö.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="ee6ae-108">Luo uusi hintamalli</span><span class="sxs-lookup"><span data-stu-id="ee6ae-108">Create a new price model</span></span>
1. <span data-ttu-id="ee6ae-109">Valitse **Tuotevarianttimallin määritys** aloitussivulla.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="ee6ae-110">Valitse **Tuotekonfiguraation mallit** **Linkit**-osiossa.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="ee6ae-111">Valitse luettelosta **High End Speaker** -rivi, mutta älä napsauta nimen linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-111">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
4. <span data-ttu-id="ee6ae-112">Valitse toimintoruudussa **Malli**.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="ee6ae-113">Valitse **Hintamallit**.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-113">Select **Price models**.</span></span>
6. <span data-ttu-id="ee6ae-114">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-114">Select **New**.</span></span>
7. <span data-ttu-id="ee6ae-115">Kirjoita arvo **Hintamallin nimi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="ee6ae-116">Käytä nimeä, jonka avulla malli on helppo tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="ee6ae-117">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="ee6ae-118">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="ee6ae-119">Lisää hintaelementit</span><span class="sxs-lookup"><span data-stu-id="ee6ae-119">Add price elements</span></span>
1. <span data-ttu-id="ee6ae-120">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-120">Select **Edit**.</span></span> <span data-ttu-id="ee6ae-121">Kullakin tuotemallin osalla voi olla perushintaelementti ja rajaton määrä hintalausekesääntöjä.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="ee6ae-122">Voit myös lisätä hinnat eri valuutoissa.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="ee6ae-123">Syötä arvo **Perushintalauseke**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="ee6ae-124">Kirjoita esimerkiksi 100.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-124">For example, type 100.</span></span> <span data-ttu-id="ee6ae-125">Lähtöhinta-lauseke voi olla numeerinen arvo tai aritmeettinen laskutoimitus, johon liittyy vähintään yksi määrite.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="ee6ae-126">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-126">Select **Add**.</span></span>
4. <span data-ttu-id="ee6ae-127">Syötä **Nimi**-kenttään `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="ee6ae-128">Hintalausekkeen nimi auttaa tunnistamaan, mitä hintaelementti edustaa.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="ee6ae-129">Tässä esimerkissä luodaan hintaelementti kaapin viimeistelyvaihtoehdolle Ruusupuu.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="ee6ae-130">Valitse **Muokkaa ehtoa**.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-130">Select **Edit condition**.</span></span> <span data-ttu-id="ee6ae-131">Hintaehto takaa, että hintalausekkeen elementti sisältyy myyntihintaan vain, jos tietty määritteiden yhdistelmä on läsnä.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="ee6ae-132">Kirjoita **ConstraintBody**-kenttään `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="ee6ae-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-133">Select **OK**.</span></span>
8. <span data-ttu-id="ee6ae-134">Kirjoita arvo **Lauseke**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="ee6ae-135">Kirjoita esimerkiksi `50`.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="ee6ae-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ee6ae-136">Close the page.</span></span>

