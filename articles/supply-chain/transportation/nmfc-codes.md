---
title: National Motor Freight Classification (NMFC) -koodit
description: Tässä aiheessa kuvataan, miten National Motor Freight Classification (NMFC) -koodeja käsitellään Microsoft Dynamics 365 Supply Chain Managementissa
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941879"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="478a4-103">National Motor Freight Classification (NMFC) -koodit</span><span class="sxs-lookup"><span data-stu-id="478a4-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="478a4-104">National Motor Freight Classification (NMFC) -koodit auttavat sinua luokittelemaan toimitettavat nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="478a4-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="478a4-105">NMFC-koodi on merkintä, jota käytetään kauppatavaran ryhmittelemisessä.</span><span class="sxs-lookup"><span data-stu-id="478a4-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="478a4-106">Kuljetusyritysten on sen avulla mahdollista arvioida toimitettavat tavarat luokittelemalla nimikkeet eri näkökohdat, kuten kuorma-autoon sopivat, lastausongelmat, käsittelyongelmat ja käytettävyys huomioon ottaen.</span><span class="sxs-lookup"><span data-stu-id="478a4-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="478a4-107">Kauppatavarat ryhmitellään yhteen 18 rahtiluokasta käyttämällä lukuja 50–500.</span><span class="sxs-lookup"><span data-stu-id="478a4-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="478a4-108">Luokka, jonne kauppatavara on ryhmitelty, perustuu neljään kuljetusominaisuudesta, jotka ovat tiheys, säilytettävyys, käsittely ja velka.</span><span class="sxs-lookup"><span data-stu-id="478a4-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="478a4-109">Yhdessä nämä ominaisuudet muodostavat kauppatavaran kuljetettavuuden.</span><span class="sxs-lookup"><span data-stu-id="478a4-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="478a4-110">NMFC-koodi on liitetty kuorma-autokuormaa pienempiin (LTL) lähetysnimikkeisiin.</span><span class="sxs-lookup"><span data-stu-id="478a4-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="478a4-111">Esimerkiksi kannettavalle tietokoneelle voidaan määrittää NMFC-luokka 2.5, kun taas sähköjohdoille määritetään NMFC-luokka 65.</span><span class="sxs-lookup"><span data-stu-id="478a4-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="478a4-112">Tämän ominaisuuden avulla työntekijät voivat luokitella LTL-lähetysnimikkeet NMFC-koodien avulla.</span><span class="sxs-lookup"><span data-stu-id="478a4-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="478a4-113">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="478a4-113">Here are some examples:</span></span>

- <span data-ttu-id="478a4-114">Jos yrityksesi sisällyttää rahtikirjaan rahtikuvauksen, operaattori saa käsityksen rahdista.</span><span class="sxs-lookup"><span data-stu-id="478a4-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="478a4-115">Rahti on tärkeä luokitus, koska monet kuljetusyritykset perustavat koko liiketoimintamallinsa rahtityyppeihin.</span><span class="sxs-lookup"><span data-stu-id="478a4-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="478a4-116">Luokitus voi olla tärkeä yrityksellesi, koska sitä käytetään tietyn kuormituksen kustannusten määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="478a4-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="478a4-117">Yrityksesi voi tunnistaa LTL-logistiikka- ja kuljetusyrityksen kannattavuuden.</span><span class="sxs-lookup"><span data-stu-id="478a4-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="478a4-118">Tässä ohjeaiheessa käsitellään NMFC-koodien käsittelemistä Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="478a4-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="478a4-119">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="478a4-119">Prerequisites</span></span>

<span data-ttu-id="478a4-120">Ennen kuin voit luoda NMFC-koodit, sinun on määritettävä kaikki LTL-rahtiluokat, jotka on määritettävä niihin.</span><span class="sxs-lookup"><span data-stu-id="478a4-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="478a4-121">LTL-rahtiluokat edustavat nimikeluokkia, kun taas NMFC-koodit liittyvät kunkin 18 rahtiluokan tiettyihin kauppatavaroihin.</span><span class="sxs-lookup"><span data-stu-id="478a4-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="478a4-122">Lisätietoja LTL-luokkien kanssa työskentelystä on kohdassa [Kuorma-autokuormaa pienemmät (LTL) luokat](ltl-class.md).</span><span class="sxs-lookup"><span data-stu-id="478a4-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="478a4-123">Luo NMFC-koodi</span><span class="sxs-lookup"><span data-stu-id="478a4-123">Create an NMFC code</span></span>

<span data-ttu-id="478a4-124">Luo NMFC-koodi seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="478a4-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="478a4-125">Noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="478a4-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="478a4-126">Valitse **Varastonhallinta \> Asetukset \> Varasto \> NMFC-koodit**.</span><span class="sxs-lookup"><span data-stu-id="478a4-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="478a4-127">Valitse **Kuljetustenhallinta \> Asetukset \> Kuljetusstandardit \> NMFC-koodit**.</span><span class="sxs-lookup"><span data-stu-id="478a4-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="478a4-128">Luo uusi NMFC-koodi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="478a4-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="478a4-129">Määritä sitten seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="478a4-129">Then set the following fields:</span></span>

    - <span data-ttu-id="478a4-130">**NMFC-koodi** – Kirjoita kauppatavaran tyypin NMFC-koodi.</span><span class="sxs-lookup"><span data-stu-id="478a4-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="478a4-131">**Nimi** – Kirjoita NMFC-koodin nimi.</span><span class="sxs-lookup"><span data-stu-id="478a4-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="478a4-132">**LTL-luokka** – Valitse LTL-luokka, joka on liitetty NMFC-koodiin.</span><span class="sxs-lookup"><span data-stu-id="478a4-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="478a4-133">**BOL materiaalin käsittely-yksikkö** – Määritä lähetyksen oletuskäsittelytyyppi.</span><span class="sxs-lookup"><span data-stu-id="478a4-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="478a4-134">Esimerkki: NMFC-koodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="478a4-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="478a4-135">Seuraavassa esimerkissä kerrotaan, miten määritetään kaksi erilaista NMFC-koodia, joita voit käyttää erityyppisten tuotteiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="478a4-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="478a4-136">Valitse **Varastonhallinta \> Asetukset \> Varasto \> NMFC-koodit**.</span><span class="sxs-lookup"><span data-stu-id="478a4-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="478a4-137">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="478a4-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="478a4-138">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="478a4-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="478a4-139">**NMFC-koodi:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="478a4-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="478a4-140">**Nimi:** *Tietokoneet*</span><span class="sxs-lookup"><span data-stu-id="478a4-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="478a4-141">**LTL-luokka:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="478a4-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="478a4-142">**BOL materiaalin käsittely-yksikkö:** *Yksikkö*</span><span class="sxs-lookup"><span data-stu-id="478a4-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="478a4-143">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="478a4-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="478a4-144">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="478a4-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="478a4-145">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="478a4-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="478a4-146">**NMFC-koodi:** *125*</span><span class="sxs-lookup"><span data-stu-id="478a4-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="478a4-147">**Nimi:** *Puhelimet*</span><span class="sxs-lookup"><span data-stu-id="478a4-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="478a4-148">**LTL-luokka:** *125*</span><span class="sxs-lookup"><span data-stu-id="478a4-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="478a4-149">**BOL materiaalin käsittely-yksikkö:** *Yksikkö*</span><span class="sxs-lookup"><span data-stu-id="478a4-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="478a4-150">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="478a4-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="478a4-151">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="478a4-151">Additional resources</span></span>

- [<span data-ttu-id="478a4-152">Kuorma-autokuormaa pienemmät (LTL) luokat</span><span class="sxs-lookup"><span data-stu-id="478a4-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="478a4-153">Rahtikirjan luominen</span><span class="sxs-lookup"><span data-stu-id="478a4-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
