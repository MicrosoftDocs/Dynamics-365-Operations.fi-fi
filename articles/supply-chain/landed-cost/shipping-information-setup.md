---
title: Lähetystietojen asetukset
description: Tässä aiheessa kuvataan, miten kuljetustietoja määritetään Aiheutunut kustannus -moduulia varten.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 5093e42b0b5247c24c271ad50c80889516586d58
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020884"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="de9be-103">Lähetystietojen asetukset</span><span class="sxs-lookup"><span data-stu-id="de9be-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de9be-104">Tässä aiheessa kuvataan, miten kuljetustietoja määritetään **Aiheutunut kustannus** -moduulia varten.</span><span class="sxs-lookup"><span data-stu-id="de9be-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="de9be-105">Tavaroiden kuvaus</span><span class="sxs-lookup"><span data-stu-id="de9be-105">Description of goods</span></span>

<span data-ttu-id="de9be-106">Tuotteiden kuvaukset auttavat tunnistamaan tuotteiden matkan, kuljetuskontin tai pakkauksen sekä niissä olevat tuotteet.</span><span class="sxs-lookup"><span data-stu-id="de9be-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="de9be-107">Voit valita tuotekuvauksen kuljetuskontin otsikosta tai pakkauksen otsikosta.</span><span class="sxs-lookup"><span data-stu-id="de9be-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="de9be-108">Voit käyttää tuotekuvauksia valitsemalla **Aiheutunut kustannus \> Kuljetustietojen määritys \> Tuotteiden kuvaukset**.</span><span class="sxs-lookup"><span data-stu-id="de9be-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="de9be-109">Tällöin voit tarkastella, avata, luoda ja poistaa tuotekuvauksia.</span><span class="sxs-lookup"><span data-stu-id="de9be-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="de9be-110">Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.</span><span class="sxs-lookup"><span data-stu-id="de9be-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="de9be-111">Kenttä</span><span class="sxs-lookup"><span data-stu-id="de9be-111">Field</span></span> | <span data-ttu-id="de9be-112">kuvaus</span><span class="sxs-lookup"><span data-stu-id="de9be-112">Description</span></span> |
|---|---|
| <span data-ttu-id="de9be-113">Tavaroiden kuvaus</span><span class="sxs-lookup"><span data-stu-id="de9be-113">Description of goods</span></span> | <span data-ttu-id="de9be-114">Syötä niille tuotteille yksilöllinen tunnusnimi/-numero, joihin tätä kuvausta käytetään.</span><span class="sxs-lookup"><span data-stu-id="de9be-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="de9be-115">kuvaus</span><span class="sxs-lookup"><span data-stu-id="de9be-115">Description</span></span> | <span data-ttu-id="de9be-116">Syötä kuvaus tämä luokan tuotetyypille.</span><span class="sxs-lookup"><span data-stu-id="de9be-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="de9be-117">Alukset</span><span class="sxs-lookup"><span data-stu-id="de9be-117">Vessels</span></span>

<span data-ttu-id="de9be-118">Alus on rahdinkuljettajan tai huolintaliikkeen käyttämä laivan tai aluksen yksilöllinen nimi.</span><span class="sxs-lookup"><span data-stu-id="de9be-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="de9be-119">Kun luot matkan, sinun on joko valittava tai syötettävä sille alus.</span><span class="sxs-lookup"><span data-stu-id="de9be-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="de9be-120">Jos käytät usein samoja aluksia, voit nopeuttaa ja helpottaa uuden matkan luomista luomalla kyseisille aluksille alustietueen. Tällöin käyttäjät voivat valita aluksen luettelosta eikä heidän tarvitse syöttää numeroa manuaalisesti joka kerta.</span><span class="sxs-lookup"><span data-stu-id="de9be-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="de9be-121">Aluksia voit käsitellä valitsemalla **Aiheutunut kustannus \> Kuljetustietojen määritys \> Alukset**.</span><span class="sxs-lookup"><span data-stu-id="de9be-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="de9be-122">Tällöin voit tarkastella, avata, luoda ja poistaa alusten tietueita.</span><span class="sxs-lookup"><span data-stu-id="de9be-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="de9be-123">Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.</span><span class="sxs-lookup"><span data-stu-id="de9be-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="de9be-124">Kenttä</span><span class="sxs-lookup"><span data-stu-id="de9be-124">Field</span></span> | <span data-ttu-id="de9be-125">kuvaus</span><span class="sxs-lookup"><span data-stu-id="de9be-125">Description</span></span> |
|---|---|
| <span data-ttu-id="de9be-126">Alus</span><span class="sxs-lookup"><span data-stu-id="de9be-126">Vessel</span></span> | <span data-ttu-id="de9be-127">Syötä sille laivalle yksilöllinen tunnusnimi/-numero, jota käytetään tuotteiden kuljettamiseen matkalla.</span><span class="sxs-lookup"><span data-stu-id="de9be-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="de9be-128">kuvaus</span><span class="sxs-lookup"><span data-stu-id="de9be-128">Description</span></span> | <span data-ttu-id="de9be-129">Syötä aluksen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="de9be-129">Enter a description of the vessel.</span></span> <span data-ttu-id="de9be-130">Yleensä tämä kuvaus sisältää laivan sekä rahdinkuljettajan/huolintaliikkeen nimet.</span><span class="sxs-lookup"><span data-stu-id="de9be-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="de9be-131">Toimitustapa</span><span class="sxs-lookup"><span data-stu-id="de9be-131">Mode of delivery</span></span> | <span data-ttu-id="de9be-132">Valitse aluksen käyttämä toimitustapa (kuten _Ilma_, _Meri_ tai _Juna_).</span><span class="sxs-lookup"><span data-stu-id="de9be-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="de9be-133">Viejät</span><span class="sxs-lookup"><span data-stu-id="de9be-133">Exporters</span></span>

<span data-ttu-id="de9be-134">Kussakin viejätietuessa määritetään toimittaja tai viejä, joka voidaan määrittää matkan toimittajaksi.</span><span class="sxs-lookup"><span data-stu-id="de9be-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="de9be-135">Viejä voidaan liittää matkaan ja viejää voidaan käyttää raportointiin.</span><span class="sxs-lookup"><span data-stu-id="de9be-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="de9be-136">Viejiä voit käsitellä valitsemalla **Aiheutunut kustannus \> Kuljetustietojen määritys \> Viejät**.</span><span class="sxs-lookup"><span data-stu-id="de9be-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="de9be-137">Tällöin voit tarkastella, avata, luoda ja poistaa viejien tietueita.</span><span class="sxs-lookup"><span data-stu-id="de9be-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="de9be-138">Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.</span><span class="sxs-lookup"><span data-stu-id="de9be-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="de9be-139">Kenttä</span><span class="sxs-lookup"><span data-stu-id="de9be-139">Field</span></span> | <span data-ttu-id="de9be-140">kuvaus</span><span class="sxs-lookup"><span data-stu-id="de9be-140">Description</span></span> |
|---|---|
| <span data-ttu-id="de9be-141">Viejä</span><span class="sxs-lookup"><span data-stu-id="de9be-141">Exporter</span></span> | <span data-ttu-id="de9be-142">Syötä sille tuotteiden viejälle yksilöllinen tunnusnimi/-numero, jonka tuotteita kuljetetaan matkalla.</span><span class="sxs-lookup"><span data-stu-id="de9be-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="de9be-143">kuvaus</span><span class="sxs-lookup"><span data-stu-id="de9be-143">Description</span></span> | <span data-ttu-id="de9be-144">Syötä viejän kuvaus.</span><span class="sxs-lookup"><span data-stu-id="de9be-144">Enter a description of the exporter.</span></span> <span data-ttu-id="de9be-145">Yleensä tämä kuvaus sisältää rahdinkuljettajan/huolintaliikkeen täyden nimen.</span><span class="sxs-lookup"><span data-stu-id="de9be-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="de9be-146">Kauppatavarakoodit</span><span class="sxs-lookup"><span data-stu-id="de9be-146">Commodity codes</span></span>

<span data-ttu-id="de9be-147">Kauppatavarakoodeja käytetään yksilöintiin tullia varten sekä matkan tuotteiden tullimaksujen laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="de9be-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="de9be-148">Voit valita kauppatavarakoodeja **Vapautetut tuotteet** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="de9be-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="de9be-149">Kauppatavarakoodeja voit käsitellä valitsemalla **Aiheutunut kustannus \> Kuljetustietojen määritys \> Kauppatavarakoodit**.</span><span class="sxs-lookup"><span data-stu-id="de9be-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="de9be-150">Tällöin voit tarkastella, avata, luoda ja poistaa kauppatavarakoodien tietueita.</span><span class="sxs-lookup"><span data-stu-id="de9be-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="de9be-151">Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.</span><span class="sxs-lookup"><span data-stu-id="de9be-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="de9be-152">Kenttä</span><span class="sxs-lookup"><span data-stu-id="de9be-152">Field</span></span> | <span data-ttu-id="de9be-153">kuvaus</span><span class="sxs-lookup"><span data-stu-id="de9be-153">Description</span></span> |
|---|---|
| <span data-ttu-id="de9be-154">Kauppatavarakoodi</span><span class="sxs-lookup"><span data-stu-id="de9be-154">Commodity code</span></span> | <span data-ttu-id="de9be-155">Syötä tämäntyyppiselle kauppatavaralle yksilöllinen koodi.</span><span class="sxs-lookup"><span data-stu-id="de9be-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="de9be-156">kuvaus</span><span class="sxs-lookup"><span data-stu-id="de9be-156">Description</span></span> | <span data-ttu-id="de9be-157">Syötä kauppatavaratyypille kuvaus.</span><span class="sxs-lookup"><span data-stu-id="de9be-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="de9be-158">Tullin kuvaus</span><span class="sxs-lookup"><span data-stu-id="de9be-158">Customs description</span></span>

<span data-ttu-id="de9be-159">Tullin kuvaukset auttavat tunnistamaan tuotteet tullaustarkoituksia varten.</span><span class="sxs-lookup"><span data-stu-id="de9be-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="de9be-160">Voit valita tullin kuvauksen **Vapautetut tuotteet** -sivulta tai ostotilauksen riveiltä.</span><span class="sxs-lookup"><span data-stu-id="de9be-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="de9be-161">Voit käyttää tullin kuvauksia valitsemalla **Aiheutunut kustannus \> Kuljetustietojen määritys \> Tullin kuvaukset**.</span><span class="sxs-lookup"><span data-stu-id="de9be-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="de9be-162">Tällöin voit tarkastella, avata, luoda ja poistaa tullin kuvauksia.</span><span class="sxs-lookup"><span data-stu-id="de9be-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="de9be-163">Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.</span><span class="sxs-lookup"><span data-stu-id="de9be-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="de9be-164">Kenttä</span><span class="sxs-lookup"><span data-stu-id="de9be-164">Field</span></span> | <span data-ttu-id="de9be-165">kuvaus</span><span class="sxs-lookup"><span data-stu-id="de9be-165">Description</span></span> |
|---|---|
| <span data-ttu-id="de9be-166">Tullin kuvaus</span><span class="sxs-lookup"><span data-stu-id="de9be-166">Customs description</span></span> | <span data-ttu-id="de9be-167">Syötä tämäntyyppiselle tulliluokitukselle yksilöllinen koodi.</span><span class="sxs-lookup"><span data-stu-id="de9be-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="de9be-168">Tätä koodia käytetään usein tulliviranomaisen tuotteiden kuvausta ja laadullista arvoa varten antamana virallisena kuvauksena.</span><span class="sxs-lookup"><span data-stu-id="de9be-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="de9be-169">kuvaus</span><span class="sxs-lookup"><span data-stu-id="de9be-169">Description</span></span> | <span data-ttu-id="de9be-170">Syötä tulliluokittelun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="de9be-170">Enter a description of the customs classification.</span></span> |
