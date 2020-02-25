---
title: Verkkokanavan määrittäminen
description: Tässä ohjeaiheessa käsitellään uuden verkkokanavan luontia Microsoft Dynamics 365 Commercessa.
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
ms.openlocfilehash: 9b7a2b8fd157df8b39e9e227d188a3802cacb4e3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002424"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="d356b-103">Verkkokanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d356b-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d356b-104">Tässä ohjeaiheessa käsitellään uuden verkkokanavan luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="d356b-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d356b-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d356b-105">Overview</span></span>

<span data-ttu-id="d356b-106">Dynamics 365 Commerce tukee useita vähittäismyynnin kanavia.</span><span class="sxs-lookup"><span data-stu-id="d356b-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="d356b-107">Vähittäismyyntikanavia ovat verkkokaupat, puhelinkeskukset ja vähittäismyymälät (eli kivijalkakaupat).</span><span class="sxs-lookup"><span data-stu-id="d356b-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="d356b-108">Verkkokaupassa asiakkaat voivat ostaa tuotteita sekä verkkokaupasta että vähittäismyymälästä.</span><span class="sxs-lookup"><span data-stu-id="d356b-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="d356b-109">Verkkokaupan luonti Commercessa edellyttää, että verkkokanava on luotava ensin.</span><span class="sxs-lookup"><span data-stu-id="d356b-109">To create an online store in Commerce, you must first create an online channel.</span></span> 

<span data-ttu-id="d356b-110">Varmista, ennen uuden verkkokanavan luontia, että [kanava-asetusten edellytykset](channels-prerequisites.md) toteutuvat.</span><span class="sxs-lookup"><span data-stu-id="d356b-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="d356b-111">Uuden verkkokanavan luominen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d356b-111">Create and configure a new online channel</span></span>

<span data-ttu-id="d356b-112">Voit luoda ja määrittää uuden verkkokanavan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d356b-112">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="d356b-113">Valitse siirtymisruudussa **Moduulit \> Kanavat \> Verkkomyymälät**.</span><span class="sxs-lookup"><span data-stu-id="d356b-113">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="d356b-114">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d356b-114">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d356b-115">Kirjoita **Nimi**-kenttään uuden kanavan nimi.</span><span class="sxs-lookup"><span data-stu-id="d356b-115">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="d356b-116">Anna sopiva yritys avattavassa **Yritys**-luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d356b-116">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="d356b-117">Anna sopiva varasto avattavassa **Varasto**-luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d356b-117">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="d356b-118">Valitse sopiva aikavyöhyke **Myymälän aikavyöhyke** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="d356b-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="d356b-119">Valitse sopiva valuutta **Valuutta**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d356b-119">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="d356b-120">Anna kelvollinen oletusasiakas **Oletusasiakas**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d356b-120">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="d356b-121">Anna kelvollinen osoitekirja **Asiakkaan osoitekirja** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="d356b-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="d356b-122">Valitse toimintoprofiili tarvittaessa **Toimintoprofiili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d356b-122">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="d356b-123">Anna kelvollinen sähköpostin ilmoitusprofiili **Sähköposti-ilmoitusprofiili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d356b-123">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="d356b-124">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d356b-124">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d356b-125">Seuraavassa kuvassa näytetään, miten uusi verkkokanava luodaan.</span><span class="sxs-lookup"><span data-stu-id="d356b-125">The following image shows the creation of a new online channel.</span></span>

![Uusi verkkokanava](media/channel-setup-online-1.png)

<span data-ttu-id="d356b-127">Seuraavassa kuvassa on esimerkki verkkokanavasta.</span><span class="sxs-lookup"><span data-stu-id="d356b-127">The following image shows an example online channel.</span></span>

![Esimerkki verkkokanavasta](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="d356b-129">Kielien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d356b-129">Set up languages</span></span>

<span data-ttu-id="d356b-130">Jos sähköinen kaupankäyntisivusto tukee useita kieliä, laajenna **Kielet**-osa ja lisää uusia kieliä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="d356b-130">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="d356b-131">Maksutilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d356b-131">Set up payment account</span></span>

<span data-ttu-id="d356b-132">Voit lisätä **Maksutili**-osassa kolmannen osapuolen maksupalvelun.</span><span class="sxs-lookup"><span data-stu-id="d356b-132">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="d356b-133">Lisätietoja Adyen-maksuyhdistimen määrittämisestä on kohdassa [Dynamics 365:n Adyen-maksuyhdistin](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="d356b-133">For information on settting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-set-up"></a><span data-ttu-id="d356b-134">Lisäkanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d356b-134">Additional channel set up</span></span>

<span data-ttu-id="d356b-135">Verkkokanavan asetuksia varten tarvittavia tehtäviä, kuten maksutapojen, toimitustapojen ja täytäntöönpanoryhmään määrityksen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="d356b-135">Additional tasks required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="d356b-136">Seuraavassa kuvassa on **Asetukset**-välilehden **Toimitustavat**-, **Maksutavat**- ja **Täytäntöönpanoryhmän määritys** -asetusvaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="d356b-136">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Verkkokanavan lisämääritykset](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="d356b-138">Maksutapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d356b-138">Set up payment methods</span></span>

<span data-ttu-id="d356b-139">Voit määrittää maksutavan kullekin tässä kanavassa tuetulle maksutyypille seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="d356b-139">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="d356b-140">Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Maksutavat**.</span><span class="sxs-lookup"><span data-stu-id="d356b-140">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="d356b-141">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d356b-141">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d356b-142">Valitse maksutapa siirtymisruudussa.</span><span class="sxs-lookup"><span data-stu-id="d356b-142">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="d356b-143">Anna **Yleiset**-osassa **Toiminnon nimi** ja määritä muut mahdolliset asetukset.</span><span class="sxs-lookup"><span data-stu-id="d356b-143">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="d356b-144">Määritä tarvittaessa maksutyypin mahdolliset lisäasetukset.</span><span class="sxs-lookup"><span data-stu-id="d356b-144">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="d356b-145">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d356b-145">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d356b-146">Seuraavassa kuvassa näkyy esimerkki käteismaksutavasta.</span><span class="sxs-lookup"><span data-stu-id="d356b-146">The following image shows an example of a cash payment method.</span></span>

![Esimerkki maksutavasta](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="d356b-148">Määritä toimitustavat</span><span class="sxs-lookup"><span data-stu-id="d356b-148">Set up modes of delivery</span></span>

<span data-ttu-id="d356b-149">Määritetyt toimitustavat saadaan näkyviin valitsemalla **Toimitustapa** **toimintoruudun** **Asetukset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="d356b-149">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="d356b-150">Voit muuttaa toimitustapaa tai lisätä sen seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="d356b-150">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="d356b-151">Valitse siirtymisruudussa **Moduulit \> Varastonhallinta \> Toimitustavat**.</span><span class="sxs-lookup"><span data-stu-id="d356b-151">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="d356b-152">Luo uusi toimitustapa valitsemalla toimintoruudussa **Uusi** tai valitse aiemmin luotu tapa.</span><span class="sxs-lookup"><span data-stu-id="d356b-152">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="d356b-153">Lisää kanava valitsemalla **Vähittäismyyntikanava**-osassa **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="d356b-153">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="d356b-154">Kanavien lisäämistä voi yksinkertaistaa käyttämällä organisaatiosolmua sen sijaan, että kukin kanava lisättäisiin erikseen.</span><span class="sxs-lookup"><span data-stu-id="d356b-154">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="d356b-155">Seuraavassa kuvassa on esimerkki toimitustavasta.</span><span class="sxs-lookup"><span data-stu-id="d356b-155">The following image shows an example of a mode of delivery.</span></span>

![Määritä toimitustavat](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="d356b-157">Täytäntöönpanoryhmän määrityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d356b-157">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="d356b-158">Voit määrittää täytäntöönpanoryhmän määrityksen noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="d356b-158">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="d356b-159">Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Täytäntöönpanoryhmän määritys**.</span><span class="sxs-lookup"><span data-stu-id="d356b-159">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="d356b-160">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d356b-160">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d356b-161">Valitse täytäntöönpanoryhmä avattavassa **Täytäntöönpanoryhmä**-luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d356b-161">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="d356b-162">Anna kuvaus avattavassa **Kuvaus**-luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d356b-162">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="d356b-163">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d356b-163">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d356b-164">Seuraavassa kuvassa on esimerkki täytäntöönpanoryhmän määrityksen määrittämisestä.</span><span class="sxs-lookup"><span data-stu-id="d356b-164">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Täytäntöönpanoryhmän määrityksen määrittäminen](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="d356b-166">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d356b-166">Additional resources</span></span>

[<span data-ttu-id="d356b-167">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d356b-167">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d356b-168">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="d356b-168">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="d356b-169">Vähittäismyyntikanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d356b-169">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="d356b-170">Puhelinkeskuskanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d356b-170">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="d356b-171">Dynamics 365 -maksuyhdistin Adyenia varten</span><span class="sxs-lookup"><span data-stu-id="d356b-171">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
