---
title: Kuorma-autokuormaa pienemmät (LTL) luokat
description: Tässä aiheessa selitetään, mitkä ovat kuorma-autokuormaa pienemmät (LTL) luokat ja miten ne määritetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941807"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="d4419-103">Kuorma-autokuormaa pienemmät (LTL) luokat</span><span class="sxs-lookup"><span data-stu-id="d4419-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4419-104">Kuorma-autokuormaa pienempi luokka on rahdin lähetysluokka, jota käytetään toimitettavissa olevien nimikkeiden luokittamiseen.</span><span class="sxs-lookup"><span data-stu-id="d4419-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="d4419-105">Yleensä jokaisella tuote- tai kauppatavaratyypillä on National Motor Freight Classification (NMFC) -koodi, joka vastaa LTL-lähetysten tiettyä rahtiluokan numeroa.</span><span class="sxs-lookup"><span data-stu-id="d4419-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="d4419-106">LTL-rahtiluokat edustavat nimikeluokkia, kun taas NMFC-koodit liittyvät kunkin 18 rahtiluokan tiettyihin kauppatavaroihin.</span><span class="sxs-lookup"><span data-stu-id="d4419-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="d4419-107">Toiminnolla voi suorittaa seuraavia tehtäviä järjestelmää käyttämällä:</span><span class="sxs-lookup"><span data-stu-id="d4419-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="d4419-108">Määritä yrityksessä käytettävät LTL-rahtiluokat.</span><span class="sxs-lookup"><span data-stu-id="d4419-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="d4419-109">Määritä jokainen LTL-luokka NMFC-koodiin **NMFC-koodit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d4419-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="d4419-110">Lisätietoja on kohdassa [National Motor Freight Classification (NMFC) -koodit](nmfc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d4419-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="d4419-111">Määritä NMFC-koodi (ja siten siihen liittyvä LTL-koodi) jokaiselle tuotteelle **Tuotteet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d4419-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="d4419-112">Arvioi tarkasti kaikkien niiden tuotteiden LTL-luokka, joihin on liitetty NMFC-koodi.</span><span class="sxs-lookup"><span data-stu-id="d4419-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="d4419-113">Voit määrittää kunkin LTL-luokan pakkausvaatimukset tarkistamalla kansainväliset LTL-standardit.</span><span class="sxs-lookup"><span data-stu-id="d4419-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="d4419-114">Näin varmistat, että tuotteesi suojataan ja toimitetaan varmasti.</span><span class="sxs-lookup"><span data-stu-id="d4419-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="d4419-115">Hae tarkat lähetysarviot kunkin tuotteen LTL-rahtiluokan perusteella.</span><span class="sxs-lookup"><span data-stu-id="d4419-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="d4419-116">Tässä ohjeaiheessa käsitellään LTL-luokkien luontia Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="d4419-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="d4419-117">Luo LTL-luokka</span><span class="sxs-lookup"><span data-stu-id="d4419-117">Create an LTL class</span></span>

<span data-ttu-id="d4419-118">Luo LTL-luokka seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="d4419-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="d4419-119">Noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="d4419-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="d4419-120">Valitse **Varastonhallinta \> Asetukset \> Varasto \> LTL-luokat**.</span><span class="sxs-lookup"><span data-stu-id="d4419-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="d4419-121">Valitse **Kuljetustenhallinta \> Asetukset \> Kuljetusstandardit \> LTL-luokat**.</span><span class="sxs-lookup"><span data-stu-id="d4419-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="d4419-122">Valitse toimintoruudussa **Uusi** ja luo LTL-luokka.</span><span class="sxs-lookup"><span data-stu-id="d4419-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="d4419-123">Määritä sitten seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="d4419-123">Then set the following fields:</span></span>

    - <span data-ttu-id="d4419-124">**LTL-luokka** – Kirjoita yrityksen sisäinen LTL-luokkatunnus kauppatavaran tyypille.</span><span class="sxs-lookup"><span data-stu-id="d4419-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="d4419-125">Useimmat yritykset käyttävät kansainvälistä standardia.</span><span class="sxs-lookup"><span data-stu-id="d4419-125">Most companies use the international standard.</span></span> <span data-ttu-id="d4419-126">Tässä tapauksessa tämän kentän arvo vastaa **Luokka**-kentän arvoa.</span><span class="sxs-lookup"><span data-stu-id="d4419-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="d4419-127">Jos yrityksesi käyttää kuitenkin omaa standardia, kirjoita sen mukainen koodi.</span><span class="sxs-lookup"><span data-stu-id="d4419-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="d4419-128">**Nimi** – Kirjoita kuvaava nimi, joka auttaa sinua ja muita käyttäjiä valitsemaan oikean LTL-luokan jokaiselle NMFC-koodille.</span><span class="sxs-lookup"><span data-stu-id="d4419-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="d4419-129">**Luokka** – Syötä kauppatavaratyypin kansainvälinen LTL-vakioluokan tunnus.</span><span class="sxs-lookup"><span data-stu-id="d4419-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="d4419-130">Tähän kirjoitettavan koodin on vastattava virallista standardia.</span><span class="sxs-lookup"><span data-stu-id="d4419-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="d4419-131">Esimerkki: LTL-luokkien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d4419-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="d4419-132">Seuraavassa esimerkissä kerrotaan, miten määritetään kaksi erilaista LTL-luokkaa, joita voit käyttää erityyppisten tuotteiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="d4419-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="d4419-133">Valitse **Varastonhallinta \> Asetukset \> Varasto \> LTL-luokat**.</span><span class="sxs-lookup"><span data-stu-id="d4419-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="d4419-134">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d4419-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d4419-135">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="d4419-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d4419-136">**LTL-luokka:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="d4419-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="d4419-137">**Nimi:** *Tietokoneet, näytöt, jäähdytyskoneet*</span><span class="sxs-lookup"><span data-stu-id="d4419-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="d4419-138">**Luokka:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="d4419-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="d4419-139">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d4419-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="d4419-140">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d4419-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d4419-141">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="d4419-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d4419-142">**LTL-luokka:** *125*</span><span class="sxs-lookup"><span data-stu-id="d4419-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="d4419-143">**Nimi:** *Pienet kodinkoneet*</span><span class="sxs-lookup"><span data-stu-id="d4419-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="d4419-144">**Luokka:** *125*</span><span class="sxs-lookup"><span data-stu-id="d4419-144">**Class:** *125*</span></span>

1. <span data-ttu-id="d4419-145">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d4419-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4419-146">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d4419-146">Additional resources</span></span>

- [<span data-ttu-id="d4419-147">National Motor Freight Classification (NMFC) -koodit</span><span class="sxs-lookup"><span data-stu-id="d4419-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="d4419-148">Rahtikirjan luominen</span><span class="sxs-lookup"><span data-stu-id="d4419-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
