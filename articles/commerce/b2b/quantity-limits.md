---
title: Tuotemäärän rajojen asettaminen B2B-verkkokauppasivustoille
description: Tässä aiheessa kuvataan, kuinka määritetään tuotemäärän rajat yritysten (B2B) verkkokauppasivustoissa.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e70648da2cc1c526625b6e34fd0867d40abb5a85
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035902"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="7ecc3-103">Tuotemäärän rajojen asettaminen B2B-verkkokauppasivustoille</span><span class="sxs-lookup"><span data-stu-id="7ecc3-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7ecc3-104">Tässä aiheessa kuvataan, kuinka määritetään tuotemäärän rajat yritysten (B2B) verkkokauppasivustoissa.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="7ecc3-105">Useimmilla tuotteilla on ryhmittelyn määrittävä mittayksikkö.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="7ecc3-106">Ryhmittely vaikuttaa siihen, miten tuotteita voidaan myydä.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="7ecc3-107">Joillakin tuotteilla saattaa olla määrille lisäryhmittelyitä.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="7ecc3-108">Tämä ryhmittely määrittää, voidaanko tuotteet myydä yksittäisinä yksikköinä vai ryhminä, ja se, onko olemassa vähimmäis- tai enimmäistilausmäärän raja, jota on noudatettava.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="7ecc3-109">Määrän rajaustoiminnon avulla voidaan varmistaa, että Microsoft Dynamics 365 Commercessa (oletustilausasetuksissa tai Commercen sivuston muodostintyökalun sivuston asetuksissa) konfiguroituja vähimmäis-, enimmäis-, moni- ja vakiomääriä sovelletaan asiakastilauksiin, jotka tehdään verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="7ecc3-110">Tuotemäärän rajoja ei tueta myyntipisteissä ja soittokeskuksissa.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="7ecc3-111">Monet vähittäiskauppiaat tarjoavat asiakastilausten (eli erikoistilausten) mahdollisuuden täyttääkseen erilaisia eri tuote- ja palveluvaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="7ecc3-112">Seuraavassa on joitakin tyypillisiä skenaarioita:</span><span class="sxs-lookup"><span data-stu-id="7ecc3-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="7ecc3-113">Asiakas haluaa, että tietyt tuotteet tai variantit myydään muutaman kappaleen erissä.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="7ecc3-114">Asiakas haluaa noutaa tuotteet myymälästä tai sijainnista, joka on eri kuin myymälä tai sijainti, josta asiakas osti nämä tuotteet.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="7ecc3-115">Myymälöiden pakkausstandardit eroavat kuitenkin online-myynnin jakelun pakkausstandardeista.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="7ecc3-116">Asiakas haluaa ostaa rajoitetun painoksen tuotteen, jolla on suurin mahdollinen määrä ostettavalle nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="7ecc3-117">Oletusarvoisten tilausasetusten ominaisuuden käyttöönottaminen Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="7ecc3-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="7ecc3-118">Ennen kuin tuotemäärän rajat voidaan määrittää, tilausten oletusasetusten ominaisuus on otettava käyttöön Commerce headquartersissa.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="7ecc3-119">Noudata seuraavia ohjeita ottaaksesi oletusarvoisten tilausasetusten ominaisuuden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="7ecc3-120">Valitse **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="7ecc3-121">Etsi ja valitse **Tue sivuston ja oletusarvoisia tilausasetuksia asiakastilauksessa** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="7ecc3-122">Valitse oikeanpuoleisen ruudun alareunasta **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="7ecc3-123">Määräasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7ecc3-123">Define quantity settings</span></span> 

<span data-ttu-id="7ecc3-124">Voit määrittää määrän asetukset **Tilauksen oletusasetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="7ecc3-125">Voit määrittää määrän asetukset noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="7ecc3-126">Siirry kohtaan **Retail ja Commerce \> Tuotteet ja luokat \> Vapautetut tuotteet luokittain**.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="7ecc3-127">Valitse vapautettu tuote.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-127">Select a released product.</span></span>
1. <span data-ttu-id="7ecc3-128">Valitse toimintoruudussa **Hallitse varastoa** -välilehden **Tilauksen asetukset** -ryhmästä **Tilauksen oletusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="7ecc3-129">Määritä **Tilauksen oletusasetukset** -sivun **Myyntitilaus**-pikavälilehden **Myyntimäärä** -osassa uotteetn myyntimäärät:</span><span class="sxs-lookup"><span data-stu-id="7ecc3-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="7ecc3-130">**Kerrannainen** – Määrä, jonka mukaan tuotteen voi ostaa.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="7ecc3-131">**Tilauksen vähimmäismäärä** – Ostettavan tuotteen vähimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="7ecc3-132">**Tilauksen enimmäismäärä** – Ostettavan tuotteen enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="7ecc3-133">**Tilauksen vakiomäärä** – Oletusmäärä, joka syötetään automaattisesti, kun tuote valitaan.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="7ecc3-134">Ota B2B-tilauksen määrärajatoiminto käyttöön Commercen sivustonmuodostimessa</span><span class="sxs-lookup"><span data-stu-id="7ecc3-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="7ecc3-135">Ota B2B-tilauksen määrärajatoiminto käyttöön Commercen sivustonmuodostimessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="7ecc3-136">Siirry kohtaan **Sivuston asetukset \> Laajennukset**.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="7ecc3-137">Valitse kohdan **Ota käyttöön tilausten määrärajat** avattavasta valikosta **Käytössä B2B-asiakkaille**.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="7ecc3-138">Päivitetyt sivustonmuodostajan asetukset tulevat voimaan vasta, kun app.settings.json-tiedosto on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="7ecc3-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="7ecc3-139">Lisätietoja on ohjeaiheessa [SDK:n ja moduulikirjaston päivitykset](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="7ecc3-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7ecc3-140">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7ecc3-140">Additional resources</span></span>

[<span data-ttu-id="7ecc3-141">B2B-verkkokauppasivuston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7ecc3-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="7ecc3-142">Organisaation mallinnushierarkioiden luominen B2B-organisaatioille</span><span class="sxs-lookup"><span data-stu-id="7ecc3-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="7ecc3-143">Liikekumppanikäyttäjien hallinta B2B-verkkokauppasivustoissa</span><span class="sxs-lookup"><span data-stu-id="7ecc3-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="7ecc3-144">Asiakastilin maksutavan määrittäminen B2B-verkkokauppasivustoille</span><span class="sxs-lookup"><span data-stu-id="7ecc3-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)