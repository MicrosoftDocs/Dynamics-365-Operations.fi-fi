---
title: Määritä määrittäville tuotteille määritepohjainen hinnoittelu
description: Tässä aiheessa kerrotaan, miten määritepohjainen hinnoittelu määritetään.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e540e0f25afa65e84cdb11fb0c56437b72891f9f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220749"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="5ae1a-103">Määritä määrittäville tuotteille määritepohjainen hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="5ae1a-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5ae1a-104">Tässä aiheessa kerrotaan, miten määritepohjainen hinnoittelu määritetään.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="5ae1a-105">Edellytyksenä on oltava tuotemääritysmalli, jolla on yksi tai useampi osa ja määrite.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="5ae1a-106">Tämä esimerkki käyttää USMF-yrityksen demotietojen korkealaatuista kaiutinmallia.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="5ae1a-107">Tämän tehtävän suorittaa yleensä tuotepäällikkö.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="5ae1a-108">Luo uusi hintamalli</span><span class="sxs-lookup"><span data-stu-id="5ae1a-108">Create a new price model</span></span>
1. <span data-ttu-id="5ae1a-109">Valitse **Tuotevarianttimallin määritys** aloitussivulla.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="5ae1a-110">Valitse **Tuotekonfiguraation mallit** **Linkit**-osiossa.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="5ae1a-111">Valitse luettelosta **High End Speaker** -rivi, mutta älä napsauta nimen linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-111">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
4. <span data-ttu-id="5ae1a-112">Valitse toimintoruudussa **Malli**.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="5ae1a-113">Valitse **Hintamallit**.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-113">Select **Price models**.</span></span>
6. <span data-ttu-id="5ae1a-114">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-114">Select **New**.</span></span>
7. <span data-ttu-id="5ae1a-115">Kirjoita arvo **Hintamallin nimi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="5ae1a-116">Käytä nimeä, jonka avulla malli on helppo tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="5ae1a-117">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="5ae1a-118">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="5ae1a-119">Lisää hintaelementit</span><span class="sxs-lookup"><span data-stu-id="5ae1a-119">Add price elements</span></span>
1. <span data-ttu-id="5ae1a-120">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-120">Select **Edit**.</span></span> <span data-ttu-id="5ae1a-121">Kullakin tuotemallin osalla voi olla perushintaelementti ja rajaton määrä hintalausekesääntöjä.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="5ae1a-122">Voit myös lisätä hinnat eri valuutoissa.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="5ae1a-123">Syötä arvo **Perushintalauseke**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="5ae1a-124">Kirjoita esimerkiksi 100.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-124">For example, type 100.</span></span> <span data-ttu-id="5ae1a-125">Lähtöhinta-lauseke voi olla numeerinen arvo tai aritmeettinen laskutoimitus, johon liittyy vähintään yksi määrite.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="5ae1a-126">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-126">Select **Add**.</span></span>
4. <span data-ttu-id="5ae1a-127">Syötä **Nimi**-kenttään `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="5ae1a-128">Hintalausekkeen nimi auttaa tunnistamaan, mitä hintaelementti edustaa.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="5ae1a-129">Tässä esimerkissä luodaan hintaelementti kaapin viimeistelyvaihtoehdolle Ruusupuu.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="5ae1a-130">Valitse **Muokkaa ehtoa**.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-130">Select **Edit condition**.</span></span> <span data-ttu-id="5ae1a-131">Hintaehto takaa, että hintalausekkeen elementti sisältyy myyntihintaan vain, jos tietty määritteiden yhdistelmä on läsnä.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="5ae1a-132">Kirjoita **ConstraintBody**-kenttään `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="5ae1a-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-133">Select **OK**.</span></span>
8. <span data-ttu-id="5ae1a-134">Kirjoita arvo **Lauseke**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="5ae1a-135">Kirjoita esimerkiksi `50`.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="5ae1a-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5ae1a-136">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]