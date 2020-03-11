---
title: Puhelinkeskuskanavan määrittäminen
description: Tässä ohjeaiheessa käsitellään uuden puhelinkeskuskanavan luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 42448bd54c00b8642b158f422e17d2b46ee25579
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057876"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="de751-103">Puhelinkeskuskanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="de751-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="de751-104">Tässä ohjeaiheessa käsitellään uuden puhelinkeskuskanavan luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="de751-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="de751-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="de751-105">Overview</span></span>

<span data-ttu-id="de751-106">Dynamics 365 Commercessa puhelinpalvelukeskus on vähittäismyynnin kanava, joka voidaan määrittää sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="de751-106">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="de751-107">Kun puhelinkeskusentiteeteille määritetään kanava, järjestelmä voi sitoa tietyt tiedot ja tilausten käsittelyn oletukset myyntitilauksiin.</span><span class="sxs-lookup"><span data-stu-id="de751-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="de751-108">Yritys voi määrittää useita puhelinkeskuskanavia Commercessa.</span><span class="sxs-lookup"><span data-stu-id="de751-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="de751-109">Varmista, ennen uuden puhelinkeskuskanavan luontia, että [kanava-asetusten edellytykset](channels-prerequisites.md) toteutuvat.</span><span class="sxs-lookup"><span data-stu-id="de751-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="de751-110">Uuden puhelinkeskuskanavan luominen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="de751-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="de751-111">Voit luoda ja määrittää uuden puhelinkeskuskanavan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="de751-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="de751-112">Valitse siirtymisruudussa **Moduulit \> Kanavat \> Puhelinkeskukset \> Kaikki puhelinkeskukset**.</span><span class="sxs-lookup"><span data-stu-id="de751-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="de751-113">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="de751-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="de751-114">Kirjoita **Nimi**-kenttään uuden kanavan nimi.</span><span class="sxs-lookup"><span data-stu-id="de751-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="de751-115">Valitse avattavasta luettelosta sopiva **Yritys**.</span><span class="sxs-lookup"><span data-stu-id="de751-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="de751-116">Valitse avattavasta luettelosta sopiva **Varasto**-sijainti.</span><span class="sxs-lookup"><span data-stu-id="de751-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="de751-117">Anna kelvollinen oletusasiakas **Oletusasiakas**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="de751-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="de751-118">Anna kelvollinen sähköpostin ilmoitusprofiili **Sähköposti-ilmoitusprofiili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="de751-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="de751-119">Anna **Hinnan ohitus** -tietokoodi.</span><span class="sxs-lookup"><span data-stu-id="de751-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="de751-120">Huomaa, että tämä tietokoodi on luotava ensin.</span><span class="sxs-lookup"><span data-stu-id="de751-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="de751-121">Anna **Pitokoodi**-tietokoodi.</span><span class="sxs-lookup"><span data-stu-id="de751-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="de751-122">Huomaa, että tämä tietokoodi on luotava ensin.</span><span class="sxs-lookup"><span data-stu-id="de751-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="de751-123">Anna **Luotto**-tietokoodi.</span><span class="sxs-lookup"><span data-stu-id="de751-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="de751-124">Huomaa, että tämä tietokoodi on luotava ensin.</span><span class="sxs-lookup"><span data-stu-id="de751-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="de751-125">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="de751-125">Select **Save**.</span></span>

<span data-ttu-id="de751-126">Seuraavassa kuvassa näytetään, miten uusi puhelinkeskuskanava luodaan.</span><span class="sxs-lookup"><span data-stu-id="de751-126">The following image shows the creation of a new call center channel.</span></span>

![Uusi puhelinkeskuskanava](media/channel-setup-callcenter-1.png)

<span data-ttu-id="de751-128">Seuraavassa kuvassa on esimerkki puhelinkeskuskanavasta.</span><span class="sxs-lookup"><span data-stu-id="de751-128">The following image shows an example call center channel.</span></span>

![Esimerkki puhelinkeskuskanavasta](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="de751-130">Lisäkanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="de751-130">Additional channel setup</span></span>

<span data-ttu-id="de751-131">Puhelinkeskuskanavan asetuksia varten tarvittavia tehtäviä, kuten maksutapojen ja toimitustapojen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="de751-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="de751-132">Seuraavassa kuvassa on **Asetukset**-välilehden **Toimitustavat**- ja **Maksutavat**-asetusvaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="de751-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![Puhelinkeskuskanavan lisämääritykset](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="de751-134">Maksutapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="de751-134">Set up payment methods</span></span>

<span data-ttu-id="de751-135">Voit määrittää maksutavan kullekin tässä kanavassa tuetulle maksutyypille seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="de751-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="de751-136">Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Maksutavat**.</span><span class="sxs-lookup"><span data-stu-id="de751-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="de751-137">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="de751-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="de751-138">Valitse maksutapa siirtymisruudussa.</span><span class="sxs-lookup"><span data-stu-id="de751-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="de751-139">Anna **Yleiset**-osassa **Toiminnon nimi** ja määritä muut mahdolliset asetukset.</span><span class="sxs-lookup"><span data-stu-id="de751-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="de751-140">Määritä tarvittaessa maksutyypin mahdolliset lisäasetukset.</span><span class="sxs-lookup"><span data-stu-id="de751-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="de751-141">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="de751-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="de751-142">Seuraavassa kuvassa näkyy esimerkki käteismaksutavasta.</span><span class="sxs-lookup"><span data-stu-id="de751-142">The following image shows an example of a cash payment method.</span></span>

![Esimerkki maksutavasta](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="de751-144">Määritä toimitustavat</span><span class="sxs-lookup"><span data-stu-id="de751-144">Set up modes of delivery</span></span>

<span data-ttu-id="de751-145">Määritetyt toimitustavat saadaan näkyviin valitsemalla **Toimitustapa** **toimintoruudun** **Asetukset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="de751-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="de751-146">Voit muuttaa toimitustapaa tai lisätä sen seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="de751-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="de751-147">Valitse siirtymisruudussa **Moduulit \> Varastonhallinta \> Toimitustavat**.</span><span class="sxs-lookup"><span data-stu-id="de751-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="de751-148">Luo uusi toimitustapa valitsemalla toimintoruudussa **Uusi** tai valitse aiemmin luotu tapa.</span><span class="sxs-lookup"><span data-stu-id="de751-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="de751-149">Lisää kanava valitsemalla **Vähittäismyyntikanava**-osassa **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="de751-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="de751-150">Kanavien lisäämistä voi yksinkertaistaa käyttämällä organisaatiosolmua sen sijaan, että kukin kanava lisättäisiin erikseen.</span><span class="sxs-lookup"><span data-stu-id="de751-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="de751-151">Seuraavassa kuvassa on esimerkki toimitustavasta.</span><span class="sxs-lookup"><span data-stu-id="de751-151">The following image shows an example of a mode of delivery.</span></span>

![Määritä toimitustavat](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="de751-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="de751-153">Additional resources</span></span>

[<span data-ttu-id="de751-154">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="de751-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="de751-155">Puhelupalvelukeskuksen myyntitoiminnot</span><span class="sxs-lookup"><span data-stu-id="de751-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="de751-156">Puhelinkeskuksen tilaustenkäsittelyasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="de751-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="de751-157">Puhelinpalvelukeskuksen luettelot</span><span class="sxs-lookup"><span data-stu-id="de751-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="de751-158">Petoshälytysten määrittäminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="de751-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="de751-159">Jatkuvuusohjelmien määrittäminen puhelinkeskuksille</span><span class="sxs-lookup"><span data-stu-id="de751-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
