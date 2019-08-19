---
title: Luo päätuote
description: Luo ennalta määritetyille varianteille päätuotteen.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21cfc2699fdcd6024286ee16bb60c3cd6dda5b67
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844704"
---
# <a name="create-a-product-master"></a><span data-ttu-id="59920-103">Luo päätuote</span><span class="sxs-lookup"><span data-stu-id="59920-103">Create a product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="59920-104">Luo ennalta määritetyille varianteille päätuotteen.</span><span class="sxs-lookup"><span data-stu-id="59920-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="59920-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="59920-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="59920-106">Tämä menettely on tarkoitettu tuotesuunnittelijalle.</span><span class="sxs-lookup"><span data-stu-id="59920-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="59920-107">Luo uusi päätuote</span><span class="sxs-lookup"><span data-stu-id="59920-107">Create a new product master</span></span>
1. <span data-ttu-id="59920-108">Siirry kohtaan Tuotetietojen hallinta > Tuotteet > Päätuotteet.</span><span class="sxs-lookup"><span data-stu-id="59920-108">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="59920-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="59920-109">Click New.</span></span>
3. <span data-ttu-id="59920-110">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="59920-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="59920-111">Numeron tulee olla yksilöivä.</span><span class="sxs-lookup"><span data-stu-id="59920-111">The number must be unique.</span></span> <span data-ttu-id="59920-112">Tuotetunnus-kentälle voidaan määrittää numerojärjestys.</span><span class="sxs-lookup"><span data-stu-id="59920-112">A number sequence can be set for the Product number field.</span></span> <span data-ttu-id="59920-113">Tällöin käyttäjän ei tarvitse syöttää arvoa.</span><span class="sxs-lookup"><span data-stu-id="59920-113">In this case, the user doesn't have to enter a value.</span></span>  
4. <span data-ttu-id="59920-114">Kirjoita arvo Tuotteen nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="59920-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="59920-115">Syötä kuvaava tuotteen nimi.</span><span class="sxs-lookup"><span data-stu-id="59920-115">Enter a descriptive product name.</span></span> <span data-ttu-id="59920-116">Arvo saa oletusarvon haun nimestä, mutta käyttäjä voi muuttaa arvon.</span><span class="sxs-lookup"><span data-stu-id="59920-116">The value defaults to the search name, but this can be changed by the user.</span></span>  
5. <span data-ttu-id="59920-117">Avaa haku valitsemalla Tuotedimensioryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="59920-117">In the Product dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="59920-118">Tuotedimensioryhmä määrittää, mitä neljää tuotedimensiota tuotevarianttien luomisessa voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="59920-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="59920-119">Tässä esimerkissä käytetään ryhmää, joka sisältää värin ja koon.</span><span class="sxs-lookup"><span data-stu-id="59920-119">This example uses a group with color and size.</span></span>  
6. <span data-ttu-id="59920-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="59920-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="59920-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="59920-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="59920-122">Oletusmääritysmenetelmä on Ennalta määritetty variantti.</span><span class="sxs-lookup"><span data-stu-id="59920-122">The default configuration technology is Predefined variant.</span></span> <span data-ttu-id="59920-123">Tässä esimerkissä käytetään sitä.</span><span class="sxs-lookup"><span data-stu-id="59920-123">This will be used for this example.</span></span>  
8. <span data-ttu-id="59920-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="59920-124">Click OK.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="59920-125">Tuotedimensioryhmien valitseminen</span><span class="sxs-lookup"><span data-stu-id="59920-125">Select product dimension groups</span></span>
1. <span data-ttu-id="59920-126">Avaa haku valitsemalla Väriryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="59920-126">In the Color group field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="59920-127">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="59920-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="59920-128">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="59920-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="59920-129">Avaa haku valitsemalla Kokoryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="59920-129">In the Size group field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="59920-130">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="59920-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="59920-131">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="59920-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="59920-132">Lisää dimensioryhmät</span><span class="sxs-lookup"><span data-stu-id="59920-132">Add dimension groups</span></span>
1. <span data-ttu-id="59920-133">Valitse toimintoruudussa Tuote.</span><span class="sxs-lookup"><span data-stu-id="59920-133">On the Action Pane, click Product.</span></span>
2. <span data-ttu-id="59920-134">Avaa valintaikkunalomake valitsemalla Dimensioryhmät.</span><span class="sxs-lookup"><span data-stu-id="59920-134">Click Dimension groups to open the drop dialog.</span></span>
3. <span data-ttu-id="59920-135">Avaa haku valitsemalla Varastodimensioryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="59920-135">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="59920-136">Varastodimensioilla hallitaan nimikkeiden tallentamista varastoon ja ottamista sieltä.</span><span class="sxs-lookup"><span data-stu-id="59920-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="59920-137">Varastodimensio voi sisältää esimerkiksi toimipisteen ja varaston.</span><span class="sxs-lookup"><span data-stu-id="59920-137">For example, a storage dimension can include Site and Warehouse.</span></span>  
4. <span data-ttu-id="59920-138">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="59920-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="59920-139">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="59920-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="59920-140">Avaa haku valitsemalla Seurantadimensioryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="59920-140">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="59920-141">Seurantadimensioryhmä määrittää, mitkä seurantadimensiot voit tuotteelle määrittää.</span><span class="sxs-lookup"><span data-stu-id="59920-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="59920-142">Esimerkiksi eränumeroa ja sarjanumeroa voidaan käyttää varastonimikkeiden seurantaan.</span><span class="sxs-lookup"><span data-stu-id="59920-142">For example, the batch number and serial number are used to track inventory items.</span></span>  
7. <span data-ttu-id="59920-143">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="59920-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="59920-144">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="59920-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="59920-145">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="59920-145">Click OK.</span></span>
10. <span data-ttu-id="59920-146">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="59920-146">Click Save.</span></span>
11. <span data-ttu-id="59920-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="59920-147">Close the page.</span></span>

