---
title: Määritä määrittäville tuotteille määritepohjainen hinnoittelu
description: Tässä menettelyssä kerrotaan, miten määritepohjainen hinnoittelu määritetään.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8568b5f4933ae58bc2d55a169c798668e03bed2a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "333780"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="8d743-103">Määritä määrittäville tuotteille määritepohjainen hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="8d743-103">Set up attribute-based pricing for configurable products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8d743-104">Tässä menettelyssä kerrotaan, miten määritepohjainen hinnoittelu määritetään.</span><span class="sxs-lookup"><span data-stu-id="8d743-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="8d743-105">Edellytyksenä on oltava tuotemääritysmalli, jolla on yksi tai useampi osa ja määrite.</span><span class="sxs-lookup"><span data-stu-id="8d743-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="8d743-106">Tämä esimerkki käyttää USMF-yrityksen demotietojen korkealaatuista kaiutinmallia.</span><span class="sxs-lookup"><span data-stu-id="8d743-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="8d743-107">Tämän tehtävän suorittaa yleensä tuotepäällikkö.</span><span class="sxs-lookup"><span data-stu-id="8d743-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="8d743-108">Luo uusi hintamalli</span><span class="sxs-lookup"><span data-stu-id="8d743-108">Create a new price model</span></span>
1. <span data-ttu-id="8d743-109">Valitse Tuotevarianttimallin määritys.</span><span class="sxs-lookup"><span data-stu-id="8d743-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="8d743-110">Valitse Tuotekonfiguraation mallit.</span><span class="sxs-lookup"><span data-stu-id="8d743-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="8d743-111">Valitse luettelosta korkealaatuisen kaiuttimen rivi, mutta älä napsauta nimen linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8d743-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="8d743-112">Valitse toimintoruudussa Malli.</span><span class="sxs-lookup"><span data-stu-id="8d743-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="8d743-113">Valitse Hintamallit.</span><span class="sxs-lookup"><span data-stu-id="8d743-113">Click Price models.</span></span>
6. <span data-ttu-id="8d743-114">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8d743-114">Click New.</span></span>
7. <span data-ttu-id="8d743-115">Kirjoita arvo Hintamalli-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8d743-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="8d743-116">Käytä nimeä, jonka avulla malli on helppo tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="8d743-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="8d743-117">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8d743-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="8d743-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8d743-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="8d743-119">Lisää hintaelementit</span><span class="sxs-lookup"><span data-stu-id="8d743-119">Add price elements</span></span>
1. <span data-ttu-id="8d743-120">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="8d743-120">Click Edit.</span></span>
    * <span data-ttu-id="8d743-121">Kullakin tuotemallin osalla voi olla perushintaelementti ja rajaton määrä hintalausekesääntöjä.</span><span class="sxs-lookup"><span data-stu-id="8d743-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="8d743-122">Voit myös lisätä hinnat eri valuutoissa.</span><span class="sxs-lookup"><span data-stu-id="8d743-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="8d743-123">Syötä arvo Perushintalauseke-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8d743-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="8d743-124">Kirjoita esimerkiksi 100.</span><span class="sxs-lookup"><span data-stu-id="8d743-124">For example, type 100.</span></span>   <span data-ttu-id="8d743-125">Lähtöhinta-lauseke voi olla numeerinen arvo tai aritmeettinen laskutoimitus, johon liittyy vähintään yksi määrite.</span><span class="sxs-lookup"><span data-stu-id="8d743-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="8d743-126">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="8d743-126">Click Add.</span></span>
4. <span data-ttu-id="8d743-127">Kirjoita Nimi-kenttään Ruusupuu.</span><span class="sxs-lookup"><span data-stu-id="8d743-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="8d743-128">Hintalausekkeen nimi auttaa tunnistamaan, mitä hintaelementti edustaa.</span><span class="sxs-lookup"><span data-stu-id="8d743-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="8d743-129">Tässä esimerkissä luodaan hintaelementti kaapin viimeistelyvaihtoehdolle Ruusupuu.</span><span class="sxs-lookup"><span data-stu-id="8d743-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="8d743-130">Valitse Muokkaa ehtoa.</span><span class="sxs-lookup"><span data-stu-id="8d743-130">Click Edit condition.</span></span>
    * <span data-ttu-id="8d743-131">Hintaehto takaa, että hintalausekkeen elementti sisältyy myyntihintaan vain, jos tietty määritteiden yhdistelmä on läsnä.</span><span class="sxs-lookup"><span data-stu-id="8d743-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="8d743-132">Lisää ConstraintBody-kenttään CabinetFinish=="Rosewood".</span><span class="sxs-lookup"><span data-stu-id="8d743-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="8d743-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d743-133">Click OK.</span></span>
8. <span data-ttu-id="8d743-134">Kirjoita arvo Lauseke-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8d743-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="8d743-135">Kirjoita esimerkiksi 50.</span><span class="sxs-lookup"><span data-stu-id="8d743-135">For example, type 50.</span></span>  
9. <span data-ttu-id="8d743-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8d743-136">Close the page.</span></span>
10. <span data-ttu-id="8d743-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8d743-137">Close the page.</span></span>

