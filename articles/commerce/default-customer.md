---
title: Oletusasiakkaan luominen
description: Tässä aiheessa esitellään, miten luodaan oletusasiakas käytettäväksi, kun Microsoft Dynamics 365 Commercessa luodaan kanavaa.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: f988732549ce82919f02c87b320623d8d4218735
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477897"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="6a1e2-103">Oletusasiakkaan luominen</span><span class="sxs-lookup"><span data-stu-id="6a1e2-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a1e2-104">Tässä aiheessa esitellään, miten luodaan oletusasiakas käytettäväksi, kun Microsoft Dynamics 365 Commercessa luodaan kanavaa.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6a1e2-105">Kun luot kanavaa, sinun on määritettävä oletusasiakas.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="6a1e2-106">Oletusasiakas on helppo luoda, kun asiakasryhmä ja asiakasosoitekirja on luotu ensin.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="6a1e2-107">Asiakasryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="6a1e2-107">Create a customer group</span></span>

<span data-ttu-id="6a1e2-108">Jos asiakasryhmiä ei vielä ole, voit luoda sellaisen.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="6a1e2-109">Esimerkkejä voivat olla eri asiakasryhmiä, kuten tukkukauppa, vähittäiskauppa, internet, työntekijät jne.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="6a1e2-110">Luo asiakasryhmä noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="6a1e2-111">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Asiakkaat \> Asiakasryhmät**.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="6a1e2-112">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6a1e2-113">Kirjoita asiakkaan tunnus **Asiakasryhmä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="6a1e2-114">Kirjoita soveltuva kuvaus **Kuvaus**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="6a1e2-115">Kirjoita soveltuva arvo **Maksuehdot**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="6a1e2-116">Kirjoita soveltuva arvo **Laskun eräpäivän ja maksupäivän välinen aika** -ruutuun.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="6a1e2-117">Kirjoita tarvittaessa veroryhmä **Oletusveroryhmä**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="6a1e2-118">Valitse tarvittaessa **Hinnat sisältävät arvonlisäveron** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="6a1e2-119">Kirjoita **Poiskirjauksen oletussyy** -ruutuun tarvittaessa asianmukainen arvo.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="6a1e2-120">Seuraavassa kuvassa näkyy useista määritettyjä asiakasryhmiä.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-120">The following image shows several configured customer groups.</span></span>

![Asiakasryhmät](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="6a1e2-122">Luo uusi asiakkaan osoitekirja</span><span class="sxs-lookup"><span data-stu-id="6a1e2-122">Create a customer address book</span></span>

<span data-ttu-id="6a1e2-123">Asiakas on yhdistettävä osoitekirjaan.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="6a1e2-124">Jos sellaista ei ole vielä luotu, sinun on luotava sellainen.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="6a1e2-125">Luo osoitekirja noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="6a1e2-126">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Osoitekirja**.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="6a1e2-127">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6a1e2-128">Anna nimi **Nimi**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="6a1e2-129">Syötä **Kuvaus**-ruutuun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="6a1e2-130">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6a1e2-131">Seuraavassa kuvassa näkyy esimerkki osoitekirjasta.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-131">The following image shows an example address book.</span></span>

![Osoitekirja](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="6a1e2-133">Oletusasiakkaan luominen</span><span class="sxs-lookup"><span data-stu-id="6a1e2-133">Create a default customer</span></span>

<span data-ttu-id="6a1e2-134">Luo oletusasiakas noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-134">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="6a1e2-135">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Asiakkaat \> Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-135">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="6a1e2-136">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6a1e2-137">Valitse avattavasta **Tyyppi**-luettelosta "Henkilö".</span><span class="sxs-lookup"><span data-stu-id="6a1e2-137">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="6a1e2-138">Valitse tai syötä avattavassa **Asiakastili**-luettelossa tilinumero (esim. "100001").</span><span class="sxs-lookup"><span data-stu-id="6a1e2-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="6a1e2-139">Valitse tai syötä avattavassa **Etunimi**-valikossa nimi (esim. "Oletus").</span><span class="sxs-lookup"><span data-stu-id="6a1e2-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="6a1e2-140">Valitse tai syötä avattavassa **Toinen etunimi**-valikossa nimi (esim. "Vähittäiskauppa").</span><span class="sxs-lookup"><span data-stu-id="6a1e2-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="6a1e2-141">Valitse tai syötä avattavassa **Sukunimi**-valikossa nimi (esim. "Asiakas").</span><span class="sxs-lookup"><span data-stu-id="6a1e2-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="6a1e2-142">Valitse tai syötä avattavassa **Valuutta**-valikossa valuutta (esim. "USD").</span><span class="sxs-lookup"><span data-stu-id="6a1e2-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="6a1e2-143">Valitse avattavassa **Valuutta**-luettelossa aiemmin luotu asiakasryhmä.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="6a1e2-144">Valitse avattavasta **Osoitekirja**-valikossa olemassa oleva osoitekirja.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="6a1e2-145">Valitse **Tallenna**, jos haluat tallentaa ja palata uuden asiakkaan asiakastietonäyttöön.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="6a1e2-146">Oletusasiakkaalle ei tarvitse lisätä osoitetta.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="6a1e2-147">Seuraavassa kuvassa näkyy esimerkki asiakkaan luomisesta.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-147">The following image shows an example of customer creation.</span></span>

![Oletusasiakkaan luominen](media/default-customer-creation.png)

<span data-ttu-id="6a1e2-149">Seuraavassa kuvassa näkyy oletusarvoinen asiakasmääritys.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-149">The following image shows a default customer configuration.</span></span>

![Esimerkkiasiakkaan määritys](media/default-customer-configuration1.png)

<span data-ttu-id="6a1e2-151">Useimmat asiakastietonäytön oletusarvot voidaan säilyttää, mutta kaksi arvoa on muutettava.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="6a1e2-152">Laajenna asiakastietonäytöllä **Myyntitilauksen oletusarvot**.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="6a1e2-153">Valitse avattavassa **Sivusto**-luettelossa esimääritetty sivusto tai syötä sivusto.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="6a1e2-154">Valitse avattavassa **Varasto**-luettelossa varasto tai syötä esimääritetty varasto.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="6a1e2-155">Seuraavassa kuvassa näkyy esimerkki asiakasmäärityksestä.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-155">The following image shows an example customer configuration.</span></span>

![Esimerkkiasiakkaan määritys](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="6a1e2-157">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6a1e2-157">Additional resources</span></span>

[<span data-ttu-id="6a1e2-158">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="6a1e2-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6a1e2-159">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="6a1e2-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
