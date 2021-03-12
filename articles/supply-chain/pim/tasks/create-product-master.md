---
title: Luo päätuote
description: Luo ennalta määritetyille varianteille päätuotteen.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 612f83f2df0ca3e66aa38defa27ec34315b4b2ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001721"
---
# <a name="create-a-product-master"></a><span data-ttu-id="cdf37-103">Luo päätuote</span><span class="sxs-lookup"><span data-stu-id="cdf37-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cdf37-104">Luo ennalta määritetyille varianteille päätuotteen.</span><span class="sxs-lookup"><span data-stu-id="cdf37-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="cdf37-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="cdf37-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="cdf37-106">Tämä menettely on tarkoitettu tuotesuunnittelijalle.</span><span class="sxs-lookup"><span data-stu-id="cdf37-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="cdf37-107">Luo uusi päätuote</span><span class="sxs-lookup"><span data-stu-id="cdf37-107">Create a new product master</span></span>
1. <span data-ttu-id="cdf37-108">Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Päätuotteet**.</span><span class="sxs-lookup"><span data-stu-id="cdf37-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="cdf37-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="cdf37-109">Click **New**.</span></span>
3. <span data-ttu-id="cdf37-110">Kirjoita arvo **Tuotenumero**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cdf37-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="cdf37-111">Numeron tulee olla yksilöivä.</span><span class="sxs-lookup"><span data-stu-id="cdf37-111">The number must be unique.</span></span> <span data-ttu-id="cdf37-112">**Tuotetunnus**-kenttään voidaan määrittää numerojärjestys.</span><span class="sxs-lookup"><span data-stu-id="cdf37-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="cdf37-113">Tällöin käyttäjän ei tarvitse syöttää arvoa.</span><span class="sxs-lookup"><span data-stu-id="cdf37-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="cdf37-114">Kirjoita arvo **Tuotteen nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cdf37-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="cdf37-115">Syötä kuvaava tuotteen nimi.</span><span class="sxs-lookup"><span data-stu-id="cdf37-115">Enter a descriptive product name.</span></span> <span data-ttu-id="cdf37-116">Arvo saa oletusarvon haun nimestä, mutta käyttäjä voi muuttaa arvon.</span><span class="sxs-lookup"><span data-stu-id="cdf37-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="cdf37-117">Avaa haku valitsemalla **Tuotedimensioryhmä**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="cdf37-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="cdf37-118">Tuotedimensioryhmä määrittää, mitä neljää tuotedimensiota tuotevarianttien luomisessa voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="cdf37-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="cdf37-119">Tässä esimerkissä käytetään ryhmää, joka sisältää värin ja koon.</span><span class="sxs-lookup"><span data-stu-id="cdf37-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="cdf37-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="cdf37-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="cdf37-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cdf37-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="cdf37-122">Oletusmääritysmenetelmä on **Ennalta määritetty variantti**.</span><span class="sxs-lookup"><span data-stu-id="cdf37-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="cdf37-123">Tässä esimerkissä käytetään sitä.</span><span class="sxs-lookup"><span data-stu-id="cdf37-123">This will be used for this example.</span></span>
8. <span data-ttu-id="cdf37-124">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="cdf37-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="cdf37-125">Tuotedimensioryhmien valitseminen</span><span class="sxs-lookup"><span data-stu-id="cdf37-125">Select product dimension groups</span></span>
1. <span data-ttu-id="cdf37-126">Avaa haku valitsemalla **Väriryhmä**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="cdf37-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="cdf37-127">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="cdf37-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cdf37-128">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cdf37-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="cdf37-129">Avaa haku valitsemalla **Kokoryhmä**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="cdf37-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="cdf37-130">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="cdf37-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="cdf37-131">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cdf37-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="cdf37-132">Lisää dimensioryhmät</span><span class="sxs-lookup"><span data-stu-id="cdf37-132">Add dimension groups</span></span>
1. <span data-ttu-id="cdf37-133">Valitse **toimintoruudusta** **Tuote**.</span><span class="sxs-lookup"><span data-stu-id="cdf37-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="cdf37-134">Avaa valintaikkuna valitsemalla **Dimensioryhmät**.</span><span class="sxs-lookup"><span data-stu-id="cdf37-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="cdf37-135">Avaa haku valitsemalla **Varastodimensioryhmä**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="cdf37-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="cdf37-136">Varastodimensioilla hallitaan nimikkeiden tallentamista varastoon ja ottamista sieltä.</span><span class="sxs-lookup"><span data-stu-id="cdf37-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="cdf37-137">Varastodimensio voi sisältää esimerkiksi toimipisteen ja varaston.</span><span class="sxs-lookup"><span data-stu-id="cdf37-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="cdf37-138">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="cdf37-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cdf37-139">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cdf37-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cdf37-140">Avaa haku valitsemalla **Seurantadimensioryhmä**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="cdf37-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="cdf37-141">Seurantadimensioryhmä määrittää, mitkä seurantadimensiot voit tuotteelle määrittää.</span><span class="sxs-lookup"><span data-stu-id="cdf37-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="cdf37-142">Esimerkiksi eränumeroa ja sarjanumeroa voidaan käyttää varastonimikkeiden seurantaan.</span><span class="sxs-lookup"><span data-stu-id="cdf37-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="cdf37-143">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="cdf37-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="cdf37-144">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cdf37-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cdf37-145">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="cdf37-145">Click **OK**.</span></span>
10. <span data-ttu-id="cdf37-146">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="cdf37-146">Click **Save**.</span></span>
11. <span data-ttu-id="cdf37-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="cdf37-147">Close the page.</span></span>

