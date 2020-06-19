---
title: Puhelinkeskuskanavan määrittäminen
description: Tässä ohjeaiheessa käsitellään uuden puhelinkeskuskanavan luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
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
ms.openlocfilehash: bdaabad39484cb12537bc5f94c34dcb2575a5b2f
ms.sourcegitcommit: ef27189efc15ce79c3c31ce2e41ef8a606fc5429
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410410"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="231d8-103">Puhelinkeskuskanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="231d8-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="231d8-104">Tässä ohjeaiheessa käsitellään uuden puhelinkeskuskanavan luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="231d8-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="231d8-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="231d8-105">Overview</span></span>


<span data-ttu-id="231d8-106">Dynamics 365 Commerceissa puhelinpalvelukeskus on Commerce-tyyppinen kanava, joka voidaan määrittää sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="231d8-106">In Dynamics 365 Commerce, a call center is a type of Commerce channel that can be defined in the application.</span></span> <span data-ttu-id="231d8-107">Kun puhelinkeskusentiteeteille määritetään kanava, järjestelmä voi sitoa tietyt tiedot ja tilausten käsittelyn oletukset myyntitilauksiin.</span><span class="sxs-lookup"><span data-stu-id="231d8-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="231d8-108">Yritys voi määrittää useita puhelinkeskuskanavia Commercessa. On kuitenkin tärkeää huomata, että yksittäinen käyttäjä voidaan linkittää vain yhteen puhelinkeskuskanavaan.</span><span class="sxs-lookup"><span data-stu-id="231d8-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="231d8-109">Varmista ennen uuden puhelinkeskuskanavan luomista, että olet tehnyt valmiiksi [kanavan määrityksen edellytykset](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="231d8-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="231d8-110">Uuden puhelinkeskuskanavan luominen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="231d8-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="231d8-111">Voit luoda ja määrittää uuden puhelinkeskuskanavan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="231d8-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="231d8-112">Siirry navigointiruudussa kohtaan **Vähittäismyynti ja kauppa \> Kanavat \> Puhelinkeskukset \> Kaikki puhelinkeskukset**.</span><span class="sxs-lookup"><span data-stu-id="231d8-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="231d8-113">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="231d8-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="231d8-114">Kirjoita **Nimi**-kenttään uuden kanavan nimi.</span><span class="sxs-lookup"><span data-stu-id="231d8-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="231d8-115">Valitse avattavasta luettelosta sopiva **Yritys**.</span><span class="sxs-lookup"><span data-stu-id="231d8-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="231d8-116">Valitse avattavasta luettelosta sopiva **Varasto**-sijainti.</span><span class="sxs-lookup"><span data-stu-id="231d8-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="231d8-117">Tätä sijaintia käytetään tälle puhelinkeskuskanavalle luotujen myyntitilausten oletusarvona, jos muita oletusarvoja ei ole määritetty asiakas- tai nimiketasolla.</span><span class="sxs-lookup"><span data-stu-id="231d8-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="231d8-118">Anna kelvollinen oletusasiakas **Oletusasiakas**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="231d8-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="231d8-119">Näitä tietoja käytetään automaattisen täytön oletusarvoissa, kun luodaan uusia asiakastietueita.</span><span class="sxs-lookup"><span data-stu-id="231d8-119">This data is used to assist in auto-populating defaults when new customer records are created.</span></span> <span data-ttu-id="231d8-120">Kun luodaan puhelinkeskuksen tilauksia, ei kannata luoda tilauksia oletusasiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="231d8-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="231d8-121">Anna kelvollinen sähköpostin ilmoitusprofiili **Sähköposti-ilmoitusprofiili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="231d8-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="231d8-122">Puhelinkeskustilausten luomisessa ja käsittelyssä käytetään sähköposti-ilmoituksen profiilia automaattisten sähköposti-ilmoitusten käynnistämisessä. Ne ilmoittavat asiakkaille tilauksen tilan.</span><span class="sxs-lookup"><span data-stu-id="231d8-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="231d8-123">Anna **Hinnan ohitus** -tietokoodi.</span><span class="sxs-lookup"><span data-stu-id="231d8-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="231d8-124">Tämä tietokoodi on ehkä luotava ensin.</span><span class="sxs-lookup"><span data-stu-id="231d8-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="231d8-125">Tämä tietokoodi sisältää niiden syykoodien joukon, joiden avulla käyttäjää pyydetään määrittämään hinnan ohituksen toiminto puhelinkeskustilauksessa.</span><span class="sxs-lookup"><span data-stu-id="231d8-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="231d8-126">Anna **Pitokoodi**-tietokoodi.</span><span class="sxs-lookup"><span data-stu-id="231d8-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="231d8-127">Tämä tietokoodi on ehkä luotava ensin.</span><span class="sxs-lookup"><span data-stu-id="231d8-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="231d8-128">Tämä tietokoodi sisältää niiden valinnaisten syykoodien joukon, joiden avulla käyttäjää pyydetään määrittämään tilauksen pitoon asettaminen.</span><span class="sxs-lookup"><span data-stu-id="231d8-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="231d8-129">Anna **Luotto**-tietokoodi.</span><span class="sxs-lookup"><span data-stu-id="231d8-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="231d8-130">Tämä tietokoodi on ehkä luotava ensin.</span><span class="sxs-lookup"><span data-stu-id="231d8-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="231d8-131">Tämä tietokoodi sisältää niiden syykoodien joukon, joiden avulla käyttäjä voi valita tilauksen kredit-toiminnon puhelinkeskuksesta muiden kuin hyvitysten antamiseksi asiakkaalle asiakaspalvelullisista syistä.</span><span class="sxs-lookup"><span data-stu-id="231d8-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="231d8-132">Valinnainen: Määritä taloushallinnon dimensiot **Taloushallinnon dimensiot** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="231d8-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="231d8-133">Tässä annetut dimensiot ovat oletusarvoja kaikissa tässä puhelinkeskuskanavassa luoduissa myyntitilauksissa.</span><span class="sxs-lookup"><span data-stu-id="231d8-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="231d8-134">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="231d8-134">Click **Save**.</span></span>

<span data-ttu-id="231d8-135">Seuraavassa kuvassa näytetään, miten uusi puhelinkeskuskanava luodaan.</span><span class="sxs-lookup"><span data-stu-id="231d8-135">The following image shows the creation of a new call center channel.</span></span>

![Uusi puhelinkeskuskanava](media/channel-setup-callcenter-1.png)

<span data-ttu-id="231d8-137">Seuraavassa kuvassa on esimerkki puhelinkeskuskanavasta.</span><span class="sxs-lookup"><span data-stu-id="231d8-137">The following image shows an example call center channel.</span></span>

![Esimerkki puhelinkeskuskanavasta](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="231d8-139">Lisäkanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="231d8-139">Additional channel setup</span></span>

<span data-ttu-id="231d8-140">Puhelinkeskuskanavan asetuksia varten tarvittavia tehtäviä, kuten maksutapojen ja toimitustapojen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="231d8-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="231d8-141">Seuraavassa kuvassa on **Asetukset**-välilehden **Toimitustavat**- ja **Maksutavat**-asetusvaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="231d8-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![Puhelinkeskuskanavan lisämääritykset](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="231d8-143">Maksutapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="231d8-143">Set up payment methods</span></span>

<span data-ttu-id="231d8-144">Voit määrittää maksutavan kullekin tässä kanavassa tuetulle maksutyypille seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="231d8-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="231d8-145">Käyttäjien on valittava ennalta määritetyistä maksutavoista. Maksutapa linkitetään heille puhelinkeskuskanavassa.</span><span class="sxs-lookup"><span data-stu-id="231d8-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="231d8-146">Ennen kuin määrität puhelinkeskuksen maksutavat, määritä päämaksutapa kohdassa **Vähittäismyynti ja kauppa \> Kanavan asetukset \> Maksutavat \> Maksutavat**.</span><span class="sxs-lookup"><span data-stu-id="231d8-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="231d8-147">Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Maksutavat**.</span><span class="sxs-lookup"><span data-stu-id="231d8-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="231d8-148">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="231d8-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="231d8-149">Valitse siirtymisruudussa maksutapa käytettävissä olevista ennalta määritetyistä maksuista.</span><span class="sxs-lookup"><span data-stu-id="231d8-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="231d8-150">Määritä tarvittaessa maksutyypin mahdolliset lisäasetukset.</span><span class="sxs-lookup"><span data-stu-id="231d8-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="231d8-151">Luottokorteille, lahjakorteille ja kanta-asiakkuuskorteille vaaditaan lisäasetukset. Valitse **Kortin asetukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="231d8-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="231d8-152">Määritä soveltuvat kirjaustilit maksutyypille **Kirjaus**-osassa.</span><span class="sxs-lookup"><span data-stu-id="231d8-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="231d8-153">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="231d8-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="231d8-154">Seuraavassa kuvassa näkyy esimerkki käteismaksutavasta.</span><span class="sxs-lookup"><span data-stu-id="231d8-154">The following image shows an example of a cash payment method.</span></span>

![Esimerkki maksutavasta](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="231d8-156">Määritä toimitustavat</span><span class="sxs-lookup"><span data-stu-id="231d8-156">Set up modes of delivery</span></span>

<span data-ttu-id="231d8-157">Määritetyt toimitustavat saadaan näkyviin valitsemalla **Toimitustapa** **toimintoruudun** **Asetukset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="231d8-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="231d8-158">Voit muuttaa toimitustapaa tai lisätä sen ja liittää puhelinkeskuskanavaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="231d8-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="231d8-159">Valitse puhelinkeskuksen toimitustapojen lomakkeessa **Hallitse toimitustapoja**</span><span class="sxs-lookup"><span data-stu-id="231d8-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="231d8-160">Luo uusi toimitustapa valitsemalla toimintoruudussa **Uusi** tai valitse aiemmin luotu tapa.</span><span class="sxs-lookup"><span data-stu-id="231d8-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="231d8-161">Lisää puhelinkeskuskanava valitsemalla **Vähittäismyyntikanava**-osassa **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="231d8-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="231d8-162">Kanavien lisäämistä voi yksinkertaistaa käyttämällä organisaatiosolmua sen sijaan, että kukin kanava lisättäisiin erikseen.</span><span class="sxs-lookup"><span data-stu-id="231d8-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="231d8-163">Varmista, että toimitustapa on määritetty **Tuotteet**-pikavälilehden ja **Osoitteet**-pikavälilehden tietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="231d8-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="231d8-164">Jos tuotteet tai toimitusosoitteet eivät ole sallittuja toimitustavalle, sen valitseminen tilauksen syöttämisen aikana päättyy virheeseen.</span><span class="sxs-lookup"><span data-stu-id="231d8-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="231d8-165">Kun muutokset puhelikeskuksen toimitustilan määrityksiin on tehty muutokset, **Käsittele toimitustilat** -työ on suoritettava muutosmatriisi hajoittamiseksi.</span><span class="sxs-lookup"><span data-stu-id="231d8-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="231d8-166">Tämä työ löytyy siirtymällä kohtaan **Vähittäismyynti ja kauppa \> Vähittäismyynnin ja kaupan IT \> Käsittele toimitustilat**.</span><span class="sxs-lookup"><span data-stu-id="231d8-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="231d8-167">Seuraavassa kuvassa on esimerkki toimitustavasta.</span><span class="sxs-lookup"><span data-stu-id="231d8-167">The following image shows an example of a mode of delivery.</span></span>

![Määritä toimitustavat](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="231d8-169">Kanavan käyttäjien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="231d8-169">Set up channel users</span></span>

<span data-ttu-id="231d8-170">Voit luoda myyntitilauksen, joka on linkitetty puhelinkeskuskanavaan Commerce Headquarters -sovelluksesta, jos myyntitilauksen luonut käyttäjä on linkitetty puhelinkeskuskanavaan.</span><span class="sxs-lookup"><span data-stu-id="231d8-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="231d8-171">Käyttäjä ei voi linkittää Commerce Headquarters -sovelluksessa luotua myyntitilausta manuaalisesti puhelinkeskuskanavaan.</span><span class="sxs-lookup"><span data-stu-id="231d8-171">The user can not manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="231d8-172">Linkki on systemaattinen. Se perustuu käyttäjään ja käyttäjän sekä puhelinkeskuskanavan suhteeseen.</span><span class="sxs-lookup"><span data-stu-id="231d8-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="231d8-173">Käyttäjä voidaan linkittää vain yhteen puhelinkeskuskanavaan.</span><span class="sxs-lookup"><span data-stu-id="231d8-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="231d8-174">Valitse toimintoruudussa ensin **Kanava**-välilehti ja sitten **Kanavan käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="231d8-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="231d8-175">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="231d8-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="231d8-176">Valitse olemassa oleva **Käyttäjän tunnus** avattavasta valintaluettelosta ja linkitä tämä käyttäjä puhelinkeskuskanavaan</span><span class="sxs-lookup"><span data-stu-id="231d8-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="231d8-177">Kun kanavan käyttäjän määritys on valmis ja käyttäjä luo uuden myyntitilauksen Commerce Headquarters -sovelluksessa, myyntitilaus linkitetään liitettyyn puhelinkeskuskanavaan.</span><span class="sxs-lookup"><span data-stu-id="231d8-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="231d8-178">Kaikki tämän kanavan määritykset kohdistetaan systemaattisesti myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="231d8-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="231d8-179">Käyttäjä voi vahvistaa, mihin puhelinkeskuskanavaan myyntitilaus linkitetään, katsomalla kanavan nimen viitteen myyntitilauksen otsikosta.</span><span class="sxs-lookup"><span data-stu-id="231d8-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="231d8-180">Hintaryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="231d8-180">Set up price groups</span></span>

<span data-ttu-id="231d8-181">Hintaryhmät ovat valinnaisia. Jos niitä käytetään, voidaan hallinnoida asiakkaille tilauksissa tarjottavia myyntihintoja puhelinkeskuskanavassa.</span><span class="sxs-lookup"><span data-stu-id="231d8-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="231d8-182">Jos hintaryhmää ei ole määritetty asiakkaalle tai jos luettelon hintaryhmiä ei ole kohdistettu myyntitilaukseen (käyttämällä **Lähdekoodin tunnus** -kenttää puhelinkeskuksen tilauksen otsikossa), nimikkeiden hinnat määritetään käyttämällä kanavan hintaryhmää.</span><span class="sxs-lookup"><span data-stu-id="231d8-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="231d8-183">Jos hintaryhmää ei löydy puhelinkeskuskanavasta, käytetään oletusnimikkeen päähintoja.</span><span class="sxs-lookup"><span data-stu-id="231d8-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="231d8-184">Voit määrittää hintaryhmän seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="231d8-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="231d8-185">Valitse toimintoruudussa ensin **Kanava**-välilehti ja sitten **Hintaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="231d8-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="231d8-186">Napsauta Toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="231d8-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="231d8-187">Valitse **Vähittäismyynnin hintaryhmä** avattavasta valintaluettelosta.</span><span class="sxs-lookup"><span data-stu-id="231d8-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="231d8-188">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="231d8-188">Additional resources</span></span>

[<span data-ttu-id="231d8-189">Kanavan määrittämisen edellytykset</span><span class="sxs-lookup"><span data-stu-id="231d8-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="231d8-190">Puhelinkeskuksen myyntitoiminnot</span><span class="sxs-lookup"><span data-stu-id="231d8-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="231d8-191">Puhelinkeskuksen tilaustenkäsittelyasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="231d8-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="231d8-192">Puhelinpalvelukeskuksen luettelot</span><span class="sxs-lookup"><span data-stu-id="231d8-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="231d8-193">Petoshälytysten määrittäminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="231d8-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="231d8-194">Jatkuvuusohjelmien määrittäminen puhelinkeskuksille</span><span class="sxs-lookup"><span data-stu-id="231d8-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
