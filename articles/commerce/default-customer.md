---
title: Oletusasiakkaan luominen
description: Tässä aiheessa esitellään, miten luodaan oletusasiakas käytettäväksi, kun Dynamics 365 Commercessa luodaan kanavaa.
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
ms.openlocfilehash: ba1d10a897f349703737068d772423f7d0292944
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411885"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="2ed2c-103">Oletusasiakkaan luominen</span><span class="sxs-lookup"><span data-stu-id="2ed2c-103">Create a default customer</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2ed2c-104">Tässä aiheessa esitellään, miten luodaan oletusasiakas käytettäväksi, kun Dynamics 365 Commercessa luodaan kanavaa.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2ed2c-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2ed2c-105">Overview</span></span>

<span data-ttu-id="2ed2c-106">Kun luot kanavaa, sinun on määritettävä oletusasiakas.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-106">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="2ed2c-107">Oletusasiakas on helppo luoda, kun asiakasryhmä ja asiakasosoitekirja on luotu ensin.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-107">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="2ed2c-108">Asiakasryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="2ed2c-108">Create a customer group</span></span>

<span data-ttu-id="2ed2c-109">Jos asiakasryhmiä ei vielä ole, voit luoda sellaisen.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-109">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="2ed2c-110">Esimerkkejä voivat olla eri asiakasryhmiä, kuten tukkukauppa, vähittäiskauppa, internet, työntekijät jne.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-110">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="2ed2c-111">Luo asiakasryhmä noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-111">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="2ed2c-112">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Asiakkaat \> Asiakasryhmät**.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-112">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="2ed2c-113">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="2ed2c-114">Kirjoita asiakkaan tunnus **Asiakasryhmä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-114">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="2ed2c-115">Kirjoita soveltuva kuvaus **Kuvaus**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-115">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="2ed2c-116">Kirjoita soveltuva arvo **Maksuehdot**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-116">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="2ed2c-117">Kirjoita soveltuva arvo **Laskun eräpäivän ja maksupäivän välinen aika** -ruutuun.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-117">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="2ed2c-118">Kirjoita tarvittaessa veroryhmä **Oletusveroryhmä**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-118">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="2ed2c-119">Valitse tarvittaessa **Hinnat sisältävät arvonlisäveron** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-119">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="2ed2c-120">Kirjoita **Poiskirjauksen oletussyy** -ruutuun tarvittaessa asianmukainen arvo.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-120">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="2ed2c-121">Seuraavassa kuvassa näkyy useista määritettyjä asiakasryhmiä.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-121">The following image shows several configured customer groups.</span></span>

![Asiakasryhmät](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="2ed2c-123">Luo uusi asiakkaan osoitekirja</span><span class="sxs-lookup"><span data-stu-id="2ed2c-123">Create a customer address book</span></span>

<span data-ttu-id="2ed2c-124">Asiakas on yhdistettävä osoitekirjaan.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-124">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="2ed2c-125">Jos sellaista ei ole vielä luotu, sinun on luotava sellainen.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-125">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="2ed2c-126">Luo osoitekirja noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-126">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="2ed2c-127">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Osoitekirja**.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-127">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="2ed2c-128">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-128">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="2ed2c-129">Anna nimi **Nimi**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-129">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="2ed2c-130">Syötä **Kuvaus**-ruutuun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-130">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="2ed2c-131">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-131">On the action pane, select **Save**.</span></span>

<span data-ttu-id="2ed2c-132">Seuraavassa kuvassa näkyy esimerkki osoitekirjasta.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-132">The following image shows an example address book.</span></span>

![Osoitekirja](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="2ed2c-134">Oletusasiakkaan luominen</span><span class="sxs-lookup"><span data-stu-id="2ed2c-134">Create a default customer</span></span>

<span data-ttu-id="2ed2c-135">Luo oletusasiakas noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-135">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="2ed2c-136">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Asiakkaat \> Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-136">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="2ed2c-137">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="2ed2c-138">Valitse avattavasta **Tyyppi**-luettelosta "Henkilö".</span><span class="sxs-lookup"><span data-stu-id="2ed2c-138">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="2ed2c-139">Valitse tai syötä avattavassa **Asiakastili**-luettelossa tilinumero (esim. "100001").</span><span class="sxs-lookup"><span data-stu-id="2ed2c-139">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="2ed2c-140">Valitse tai syötä avattavassa **Etunimi**-valikossa nimi (esim. "Oletus").</span><span class="sxs-lookup"><span data-stu-id="2ed2c-140">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="2ed2c-141">Valitse tai syötä avattavassa **Toinen etunimi**-valikossa nimi (esim. "Vähittäiskauppa").</span><span class="sxs-lookup"><span data-stu-id="2ed2c-141">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="2ed2c-142">Valitse tai syötä avattavassa **Sukunimi**-valikossa nimi (esim. "Asiakas").</span><span class="sxs-lookup"><span data-stu-id="2ed2c-142">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="2ed2c-143">Valitse tai syötä avattavassa **Valuutta**-valikossa valuutta (esim. "USD").</span><span class="sxs-lookup"><span data-stu-id="2ed2c-143">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="2ed2c-144">Valitse avattavassa **Valuutta**-luettelossa aiemmin luotu asiakasryhmä.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-144">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="2ed2c-145">Valitse avattavasta **Osoitekirja**-valikossa olemassa oleva osoitekirja.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-145">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="2ed2c-146">Valitse **Tallenna**, jos haluat tallentaa ja palata uuden asiakkaan asiakastietonäyttöön.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-146">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="2ed2c-147">Oletusasiakkaalle ei tarvitse lisätä osoitetta.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-147">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="2ed2c-148">Seuraavassa kuvassa näkyy esimerkki asiakkaan luomisesta.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-148">The following image shows an example of customer creation.</span></span>

![Oletusasiakkaan luominen](media/default-customer-creation.png)

<span data-ttu-id="2ed2c-150">Seuraavassa kuvassa näkyy oletusarvoinen asiakasmääritys.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-150">The following image shows a default customer configuration.</span></span>

![Esimerkkiasiakkaan määritys](media/default-customer-configuration1.png)

<span data-ttu-id="2ed2c-152">Useimmat asiakastietonäytön oletusarvot voidaan säilyttää, mutta kaksi arvoa on muutettava.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-152">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="2ed2c-153">Laajenna asiakastietonäytöllä **Myyntitilauksen oletusarvot**.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-153">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="2ed2c-154">Valitse avattavassa **Sivusto**-luettelossa esimääritetty sivusto tai syötä sivusto.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-154">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="2ed2c-155">Valitse avattavassa **Varasto**-luettelossa varasto tai syötä esimääritetty varasto.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-155">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="2ed2c-156">Seuraavassa kuvassa näkyy esimerkki asiakasmäärityksestä.</span><span class="sxs-lookup"><span data-stu-id="2ed2c-156">The following image shows an example customer configuration.</span></span>

![Esimerkkiasiakkaan määritys](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="2ed2c-158">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2ed2c-158">Additional resources</span></span>

[<span data-ttu-id="2ed2c-159">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2ed2c-159">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="2ed2c-160">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="2ed2c-160">Channel setup prerequisites</span></span>](channels-prerequisites.md)
