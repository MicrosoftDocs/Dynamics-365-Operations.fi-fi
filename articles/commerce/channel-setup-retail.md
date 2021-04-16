---
title: Vähittäismyyntikanavan määrittäminen
description: Tässä ohjeaiheessa käsitellään uuden vähittäismyyntikanavan luomisesta Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 713cbe68c151b6893519843611089941cabf0e70
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800588"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="a75a1-103">Vähittäismyyntikanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a75a1-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a75a1-104">Tässä ohjeaiheessa käsitellään uuden vähittäismyyntikanavan luomisesta Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="a75a1-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a75a1-105">Dynamics 365 Commerce tukee useita vähittäismyynnin kanavia.</span><span class="sxs-lookup"><span data-stu-id="a75a1-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="a75a1-106">Vähittäismyyntikanavia ovat verkkokaupat, puhelinkeskukset ja vähittäismyymälät (eli kivijalkakaupat).</span><span class="sxs-lookup"><span data-stu-id="a75a1-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="a75a1-107">Jokaisella vähittäismyymäläkanavalla voi olla omat maksuvälineet, hintaryhmät, kassakoneet, tulo- ja kulutilit sekä oma henkilökunta.</span><span class="sxs-lookup"><span data-stu-id="a75a1-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="a75a1-108">Sinun on määritettävä kaikki nämä elementit, ennen kuin voit luoda vähittäismyymäläkanavan.</span><span class="sxs-lookup"><span data-stu-id="a75a1-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="a75a1-109">Varmista ennen vähittäismyyntikanavan luontia, että [kanavan edellytykset](channels-prerequisites.md) toteutuvat.</span><span class="sxs-lookup"><span data-stu-id="a75a1-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="a75a1-110">Uuden vähittäismyyntikanavan luominen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a75a1-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="a75a1-111">Valitse siirtymisruudussa **Moduulit \> Kanavat \> Myymälät \> Kaikki myymälät**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="a75a1-112">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a75a1-113">Kirjoita **Nimi**-kenttään uuden kanavan nimi.</span><span class="sxs-lookup"><span data-stu-id="a75a1-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="a75a1-114">Anna yksilöivä myymälän numero **Myymälän numero** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="a75a1-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="a75a1-115">Numero voi olla aakkosnumeerinen, ja siinä saa olla enintään 10 merkkiä.</span><span class="sxs-lookup"><span data-stu-id="a75a1-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="a75a1-116">Anna sopiva yritys avattavassa **Yritys**-luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a75a1-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="a75a1-117">Anna sopiva varasto avattavassa **Varasto**-luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a75a1-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="a75a1-118">Valitse sopiva aikavyöhyke **Myymälän aikavyöhyke** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="a75a1-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="a75a1-119">Valitse myymälään sopiva arvonlisäveroryhmä avattavassa **Arvonlisäveroryhmä**-luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a75a1-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="a75a1-120">Valitse sopiva valuutta **Valuutta**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a75a1-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="a75a1-121">Anna kelvollinen osoitekirja **Asiakkaan osoitekirja** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="a75a1-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="a75a1-122">Anna kelvollinen oletusasiakas **Oletusasiakas**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a75a1-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="a75a1-123">Valitse toimintoprofiili tarvittaessa **Toimintoprofiili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a75a1-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="a75a1-124">Anna kelvollinen sähköpostin ilmoitusprofiili **Sähköposti-ilmoitusprofiili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a75a1-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="a75a1-125">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-125">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a75a1-126">Seuraavassa kuvassa näytetään, miten uusi vähittäismyyntikanava luodaan.</span><span class="sxs-lookup"><span data-stu-id="a75a1-126">The following image shows the creation of a new retail channel.</span></span>

![Uusi vähittäismyyntikanava](media/channel-setup-retail-1.png)

<span data-ttu-id="a75a1-128">Seuraavassa kuvassa on esimerkki vähittäismyyntikanavasta.</span><span class="sxs-lookup"><span data-stu-id="a75a1-128">The following image shows an example retail channel.</span></span>

![Vähittäismyyntikanavan esimerkki](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="a75a1-130">Muut asetukset</span><span class="sxs-lookup"><span data-stu-id="a75a1-130">Other settings</span></span>

<span data-ttu-id="a75a1-131">**Laskelma/sulkeminen**- ja **Muut**-osissa on monia määritettäviä valinnaisia asetuksia. Nämä määritykset voidaan tehdä vähittäismyymälän tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="a75a1-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="a75a1-132">Lisätietoja näytön oletusasettelun määrittämisestä **Näytön asettelu** -osassa on kohdassa [Näytön asettelut myyntipisteeseen (POS)](pos-screen-layouts.md) ja **Laiteasema**-osan määritystiedoista on kohdassa [Retail Hardware Stationin määrittäminen ja asentaminen](retail-hardware-station-configuration-installation.md).</span><span class="sxs-lookup"><span data-stu-id="a75a1-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="a75a1-133">Seuraavassa kuvassa on esimerkki vähittäismyyntikanavan asetusten määrityksistä.</span><span class="sxs-lookup"><span data-stu-id="a75a1-133">The following image shows an example retail channel setup configuration.</span></span>

![Vähittäismyyntikanavan määritysesimerkki](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="a75a1-135">Lisäkanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a75a1-135">Additional channel set up</span></span>

<span data-ttu-id="a75a1-136">Muita kanavaan määritettäviä kohteita on **Asetukset**-osan **toimintoruudussa**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-136">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="a75a1-137">Verkkokanavan asetuksia varten tarvittavia tehtäviä, kuten maksutapojen, kassatilityksen, toimitustapojen, tulo- ja kulutilin, osien, täytäntöönpanoryhmään määrityksen ja säilöjen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="a75a1-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="a75a1-138">Seuraavassa kuvassa on erilaisia vähittäismyyntikanavan määritysvaihtoehtoja **Asetukset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="a75a1-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanavan määrittäminen](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="a75a1-140">Maksutapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a75a1-140">Set up payment methods</span></span>

<span data-ttu-id="a75a1-141">Voit määrittää maksutavan kullekin tässä kanavassa tuetulle maksutyypille seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a75a1-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="a75a1-142">Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Maksutavat**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="a75a1-143">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a75a1-144">Valitse maksutapa siirtymisruudussa.</span><span class="sxs-lookup"><span data-stu-id="a75a1-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="a75a1-145">Anna **Yleiset**-osassa **Toiminnon nimi** ja määritä muut mahdolliset asetukset.</span><span class="sxs-lookup"><span data-stu-id="a75a1-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="a75a1-146">Määritä tarvittaessa maksutyypin mahdolliset lisäasetukset.</span><span class="sxs-lookup"><span data-stu-id="a75a1-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="a75a1-147">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a75a1-148">Seuraavassa kuvassa näkyy esimerkki käteismaksutavasta.</span><span class="sxs-lookup"><span data-stu-id="a75a1-148">The following image shows an example of a cash payment method.</span></span>

![Esimerkki maksutavasta](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="a75a1-150">Kassatilityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a75a1-150">Set up cash declaration</span></span>

1. <span data-ttu-id="a75a1-151">Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Kassatilitys**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-151">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="a75a1-152">Valitse toimintoruudussa **Uusi** ja luo sitten kaikki tarvittavat **Kolikko**- ja **Seteli**-arvot.</span><span class="sxs-lookup"><span data-stu-id="a75a1-152">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="a75a1-153">Seuraavassa kuvassa näkyy esimerkki kassatilityksestä.</span><span class="sxs-lookup"><span data-stu-id="a75a1-153">The following image shows an example of a cash declaration.</span></span>

![Kassatilitysten määrittäminen](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="a75a1-155">Määritä toimitustavat</span><span class="sxs-lookup"><span data-stu-id="a75a1-155">Set up modes of delivery</span></span>

<span data-ttu-id="a75a1-156">Määritetyt toimitustavat saadaan näkyviin valitsemalla **Toimitustapa** **toimintoruudun** **Asetukset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="a75a1-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="a75a1-157">Voit muuttaa toimitustapaa tai lisätä sen seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a75a1-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="a75a1-158">Valitse siirtymisruudussa **Moduulit \> Varastonhallinta \> Toimitustavat**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="a75a1-159">Luo uusi toimitustapa valitsemalla toimintoruudussa **Uusi** tai valitse aiemmin luotu tapa.</span><span class="sxs-lookup"><span data-stu-id="a75a1-159">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="a75a1-160">Lisää kanava valitsemalla **Vähittäismyyntikanava**-osassa **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="a75a1-161">Kanavien lisäämistä voi yksinkertaistaa käyttämällä organisaatiosolmua sen sijaan, että kukin kanava lisättäisiin erikseen.</span><span class="sxs-lookup"><span data-stu-id="a75a1-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="a75a1-162">Seuraavassa kuvassa on esimerkki toimitustavasta.</span><span class="sxs-lookup"><span data-stu-id="a75a1-162">The following image shows an example of a mode of delivery.</span></span>

![Määritä toimitustavat](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="a75a1-164">Tulo- ja kulutilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a75a1-164">Set up income/expense account</span></span>

<span data-ttu-id="a75a1-165">Voit määrittää tulo- ja kulutilin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="a75a1-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="a75a1-166">Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Tulo- ja kulutili**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-166">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="a75a1-167">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-167">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a75a1-168">Anna nimi **Nimi**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="a75a1-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="a75a1-169">Anna hakunimi **Hakunimi**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="a75a1-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="a75a1-170">Anna tilityyppi **Tilityyppi**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="a75a1-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="a75a1-171">Kirjoita tarpeen mukaan tekstiä seuraaviin kohtiin: **Sanomarivi 1**, **Sanomarivi 2**, **Luetteloteksti 1** ja **Luetteloteksti 2**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="a75a1-172">Anna kirjauksen tiedot **Kirjaus**-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="a75a1-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="a75a1-173">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-173">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a75a1-174">Seuraavassa kuvassa on esimerkki tulo- ja kulutilistä.</span><span class="sxs-lookup"><span data-stu-id="a75a1-174">The following image shows an example of an income/expense account.</span></span>

![Tulo- ja kulutilien määrittäminen](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="a75a1-176">Osien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a75a1-176">Set up sections</span></span>

<span data-ttu-id="a75a1-177">Voit määrittää osia noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="a75a1-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="a75a1-178">Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Osat**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-178">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="a75a1-179">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-179">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a75a1-180">Anna osan numero **Osan numero** -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="a75a1-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="a75a1-181">Anna kuvaus **Kuvaus**-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="a75a1-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="a75a1-182">Anna osan koko **Osan koko** -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="a75a1-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="a75a1-183">Määritä tarpeen mukaan **Yleiset**- ja **Myyntitilastot**-asetukset.</span><span class="sxs-lookup"><span data-stu-id="a75a1-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="a75a1-184">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-184">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="a75a1-185">Täytäntöönpanoryhmän määrityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a75a1-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="a75a1-186">Voit määrittää täytäntöönpanoryhmän määrityksen noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="a75a1-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="a75a1-187">Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Täytäntöönpanoryhmän määritys**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-187">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="a75a1-188">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-188">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a75a1-189">Valitse täytäntöönpanoryhmä avattavassa **Täytäntöönpanoryhmä**-luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a75a1-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="a75a1-190">Anna kuvaus avattavassa **Kuvaus**-luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a75a1-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="a75a1-191">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-191">On the action pane, select **Save**</span></span>

<span data-ttu-id="a75a1-192">Seuraavassa kuvassa on esimerkki täytäntöönpanoryhmän määrityksen määrittämisestä.</span><span class="sxs-lookup"><span data-stu-id="a75a1-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Täytäntöönpanoryhmän määritysten määrittäminen](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="a75a1-194">Säilöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a75a1-194">Set up safes</span></span>

<span data-ttu-id="a75a1-195">Voit määrittää säilöjä noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="a75a1-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="a75a1-196">Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-196">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="a75a1-197">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-197">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a75a1-198">Anna säilön nimi.</span><span class="sxs-lookup"><span data-stu-id="a75a1-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="a75a1-199">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a75a1-199">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a75a1-200">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a75a1-200">Additional resources</span></span>

[<span data-ttu-id="a75a1-201">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a75a1-201">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="a75a1-202">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="a75a1-202">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="a75a1-203">Verkkokanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a75a1-203">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="a75a1-204">Puhelinkeskuskanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a75a1-204">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
