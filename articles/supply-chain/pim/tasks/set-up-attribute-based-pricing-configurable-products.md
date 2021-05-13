---
title: Määritä määrittäville tuotteille määritepohjainen hinnoittelu
description: Tässä aiheessa kerrotaan, miten määritepohjainen hinnoittelu määritetään.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921238"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="d387f-103">Määritä määrittäville tuotteille määritepohjainen hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="d387f-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d387f-104">Tässä aiheessa kerrotaan, miten määritepohjainen hinnoittelu määritetään.</span><span class="sxs-lookup"><span data-stu-id="d387f-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="d387f-105">Edellytyksenä on oltava tuotemääritysmalli, jolla on yksi tai useampi osa ja määrite.</span><span class="sxs-lookup"><span data-stu-id="d387f-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="d387f-106">Tämä esimerkki käyttää USMF-yrityksen demotietojen korkealaatuista kaiutinmallia.</span><span class="sxs-lookup"><span data-stu-id="d387f-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="d387f-107">Tämän tehtävän suorittaa yleensä tuotepäällikkö.</span><span class="sxs-lookup"><span data-stu-id="d387f-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="d387f-108">Luo uusi hintamalli</span><span class="sxs-lookup"><span data-stu-id="d387f-108">Create a new price model</span></span>

1. <span data-ttu-id="d387f-109">Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.</span><span class="sxs-lookup"><span data-stu-id="d387f-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="d387f-110">Valitse luettelosta **High End Speaker** -rivi, mutta älä napsauta nimen linkkiä.</span><span class="sxs-lookup"><span data-stu-id="d387f-110">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
1. <span data-ttu-id="d387f-111">Valitse toimintoruudussa **Malli**.</span><span class="sxs-lookup"><span data-stu-id="d387f-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="d387f-112">Valitse **Hintamallit**.</span><span class="sxs-lookup"><span data-stu-id="d387f-112">Select **Price models**.</span></span>
1. <span data-ttu-id="d387f-113">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d387f-113">Select **New**.</span></span>
1. <span data-ttu-id="d387f-114">Kirjoita arvo **Hintamallin nimi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="d387f-114">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="d387f-115">Käytä nimeä, jonka avulla malli on helppo tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="d387f-115">Use a name that makes the model easy to identify.</span></span>  
1. <span data-ttu-id="d387f-116">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d387f-116">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="d387f-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d387f-117">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="d387f-118">Lisää hintaelementit</span><span class="sxs-lookup"><span data-stu-id="d387f-118">Add price elements</span></span>

1. <span data-ttu-id="d387f-119">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="d387f-119">Select **Edit**.</span></span> <span data-ttu-id="d387f-120">Kullakin tuotemallin osalla voi olla perushintaelementti ja rajaton määrä hintalausekesääntöjä.</span><span class="sxs-lookup"><span data-stu-id="d387f-120">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="d387f-121">Voit myös lisätä hinnat eri valuutoissa.</span><span class="sxs-lookup"><span data-stu-id="d387f-121">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="d387f-122">Syötä arvo **Perushintalauseke**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d387f-122">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="d387f-123">Kirjoita esimerkiksi 100.</span><span class="sxs-lookup"><span data-stu-id="d387f-123">For example, type 100.</span></span> <span data-ttu-id="d387f-124">Lähtöhinta-lauseke voi olla numeerinen arvo tai aritmeettinen laskutoimitus, johon liittyy vähintään yksi määrite.</span><span class="sxs-lookup"><span data-stu-id="d387f-124">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="d387f-125">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="d387f-125">Select **Add**.</span></span>
4. <span data-ttu-id="d387f-126">Syötä **Nimi**-kenttään `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="d387f-126">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="d387f-127">Hintalausekkeen nimi auttaa tunnistamaan, mitä hintaelementti edustaa.</span><span class="sxs-lookup"><span data-stu-id="d387f-127">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="d387f-128">Tässä esimerkissä luodaan hintaelementti kaapin viimeistelyvaihtoehdolle Ruusupuu.</span><span class="sxs-lookup"><span data-stu-id="d387f-128">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="d387f-129">Valitse **Muokkaa ehtoa**.</span><span class="sxs-lookup"><span data-stu-id="d387f-129">Select **Edit condition**.</span></span> <span data-ttu-id="d387f-130">Hintaehto takaa, että hintalausekkeen elementti sisältyy myyntihintaan vain, jos tietty määritteiden yhdistelmä on läsnä.</span><span class="sxs-lookup"><span data-stu-id="d387f-130">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="d387f-131">Kirjoita **ConstraintBody**-kenttään `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="d387f-131">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="d387f-132">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="d387f-132">Select **OK**.</span></span>
8. <span data-ttu-id="d387f-133">Kirjoita arvo **Lauseke**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d387f-133">In the **Expression** field, type a value.</span></span> <span data-ttu-id="d387f-134">Kirjoita esimerkiksi `50`.</span><span class="sxs-lookup"><span data-stu-id="d387f-134">For example, type `50`.</span></span> 
9. <span data-ttu-id="d387f-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d387f-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]