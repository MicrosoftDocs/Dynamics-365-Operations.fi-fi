---
title: "Määritä klusterikeräily"
description: "Tässä ohjeaiheessa käsitellään klusterikeräilyn määrittämistä ja nimikevahvistuksen käyttämistä klusterikeräilyssä."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2ec0890963b2b01407acac8003453faf370894b4
ms.openlocfilehash: 1c23421ddfda8c5f6fa27a31831a00ead6094db9
ms.contentlocale: fi-fi
ms.lasthandoff: 04/11/2018

---

[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a><span data-ttu-id="bf435-103">Määritä klusterikeräily</span><span class="sxs-lookup"><span data-stu-id="bf435-103">Set up cluster picking</span></span>

<span data-ttu-id="bf435-104">Tässä ohjeaiheessa kuvataan, kuinka työntekijät voivat käyttää mobiililaitteitaan ryhmittelemään työn keräilyn klustereihin, jotta he voivat keräillä nimikkeet yhdestä sijainnista useille työtilauksille samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="bf435-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="bf435-105">Tätä kutsutaan nimellä *klusterin keräys*.</span><span class="sxs-lookup"><span data-stu-id="bf435-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="bf435-106">Tietoja klusterin keräilystä</span><span class="sxs-lookup"><span data-stu-id="bf435-106">About cluster picking</span></span>

<span data-ttu-id="bf435-107">Kun työtilaukset on vapautettu varastoon, työntekijä voi määrittää tilaukset klusteriin mobiililaitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="bf435-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="bf435-108">Klusteri järjestää keräilytyön työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="bf435-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="bf435-109">Kun työtilaus liitetään klusteriin, työntekijän on käytettävä klusterikeräilyä kyseisen tilauksen keräilytyöhön.</span><span class="sxs-lookup"><span data-stu-id="bf435-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="bf435-110">Työntekijä ei voi käyttää muita keräilymenetelmiä.</span><span class="sxs-lookup"><span data-stu-id="bf435-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="bf435-111">Jos työjärjestys määritetään klusteriin vahingossa, työntekijän on pidettävä tauko rikkoakseen klusterin ja luodakseen sen sitten uudelleen.</span><span class="sxs-lookup"><span data-stu-id="bf435-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="bf435-112">Tarvittaessa työntekijä voi siirtää klusterin toiselle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="bf435-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="bf435-113">Tämä muuttaa klusterin tilaksi Hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="bf435-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="bf435-114">Kun työntekijä käyttää mobiililaitetta ja ilmoittaa, että keräily ja hyllytys on valmis, lähetys tai kuorma on vahvistettava Dynamics 365 for Finance and Operations -asiakasohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="bf435-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the Dynamics 365 for Finance and Operations client.</span></span>

## <a name="set-up-cluster-picking"></a><span data-ttu-id="bf435-115">Määritä klusterikeräily</span><span class="sxs-lookup"><span data-stu-id="bf435-115">Set up cluster picking</span></span>

<span data-ttu-id="bf435-116">Jos haluat ottaa klusterin keräilyn käyttöön, sinun on määritettävä seuraavat:</span><span class="sxs-lookup"><span data-stu-id="bf435-116">To enable cluster picking, you must set up the following:</span></span>

-   <span data-ttu-id="bf435-117">**Klusteriprofiilit** – Määritä, luodaanko klusterin tunnukset, käytettävien sijaintien määrä ja klusterien keskeytyskohta automaattisesti. Määritä myös, miten keräilytyö jaksotetaan ja vahvistetaan.</span><span class="sxs-lookup"><span data-stu-id="bf435-117">**Cluster profiles** – Specify whether to automatically generate cluster IDs, the number of positions to use, when to break clusters, and how to sequence and verify the picking work.</span></span>

-   <span data-ttu-id="bf435-118">**Työmallit** – Määritä, miten klusterikeräilyn keräilytyö luodaan.</span><span class="sxs-lookup"><span data-stu-id="bf435-118">**Work templates** – Define how to create the picking work for cluster picking.</span></span>

-   <span data-ttu-id="bf435-119">**Sijaintidirektiivit** – Määritä, mistä nimikkeet kerätään ja mihin ne laitetaan.</span><span class="sxs-lookup"><span data-stu-id="bf435-119">**Location directives** – Specify where to pick items from, and where to put them.</span></span>

-   <span data-ttu-id="bf435-120">**Mobiililaitteen valikkovaihtoehdot** – Määritä mobiililaitteen valikkovaihtoehto käyttämään klusterikeräilyn ohjaamaa työtä.</span><span class="sxs-lookup"><span data-stu-id="bf435-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="bf435-121">Sinun on lisättävä valikkokohde mobiililaitteen valikkoon, jotta se näkyy mobiililaitteilla.</span><span class="sxs-lookup"><span data-stu-id="bf435-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

-   <span data-ttu-id="bf435-122">**Varastonhallinnan parametrit** – Määritä numerosarja, jota haluat käyttää klustereiden tunnisteiden luontiin.</span><span class="sxs-lookup"><span data-stu-id="bf435-122">**Warehouse management parameters** – Specify the number sequence to use if you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="bf435-123">Klusteriprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bf435-123">Set up a cluster profile</span></span>

<span data-ttu-id="bf435-124">Määritä klusteriprofiili noudattamalla seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="bf435-124">To set up a cluster profile, follow these steps:</span></span>

1.  <span data-ttu-id="bf435-125">Valitse **Varastonhallinta** \> **Asetukset** \> **Mobiililaite** \> **Klusteriprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="bf435-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \> **Cluster profiles**.</span></span>

2.  <span data-ttu-id="bf435-126">Luo uusi profiili valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bf435-126">Click **New** to create a new profile.</span></span>

3.  <span data-ttu-id="bf435-127">Määritä klusterin lajitteluperuste valitsemalla ensin **Luo klusteri** ja sitten **Klusterin lajittelu** -kohdassa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bf435-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="bf435-128">Lajitteluehto hallitsee järjestystä, jonka perusteella työntekijä suorittaa keräilytyön.</span><span class="sxs-lookup"><span data-stu-id="bf435-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="bf435-129">Voit luoda tarvitsemasi määrän kriteereitä.</span><span class="sxs-lookup"><span data-stu-id="bf435-129">You can add as many criteria as needed.</span></span>

4.  <span data-ttu-id="bf435-130">Anna **Järjestysnumero**-kentässä numero, joka määrittää lajitteluehtojen käsittelyjärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="bf435-130">In the **Sequence number** field, enter a number to define the order in which the sorting criteria are processed.</span></span>

5.  <span data-ttu-id="bf435-131">Valitse **Kentän nimi** -kentässä kenttä, joka määrittää lajitteluun.</span><span class="sxs-lookup"><span data-stu-id="bf435-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="bf435-132">Esimerkiksi jos valitset **WMSLocationId**-kentän, työ lajitellaan sijainnin mukaan.</span><span class="sxs-lookup"><span data-stu-id="bf435-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

6.  <span data-ttu-id="bf435-133">Valitse **Lajittelu**-kentässä jokin seuraavista vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="bf435-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="bf435-134">**Vaihtoehto**</span><span class="sxs-lookup"><span data-stu-id="bf435-134">**Option**</span></span>     | <span data-ttu-id="bf435-135">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="bf435-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf435-136">**Nouseva**</span><span class="sxs-lookup"><span data-stu-id="bf435-136">**Ascending**</span></span>  | <span data-ttu-id="bf435-137">Keräystyö järjestetään nousevassa järjestyksessä lajitteluehtojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="bf435-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="bf435-138">Jos käytät **WMSLocationId**-kenttää lajitteluehtona ja sijaintitunnuksesi ovat 1, 2, 3 ja 4, keräät sijainnista 4 ensin.</span><span class="sxs-lookup"><span data-stu-id="bf435-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="bf435-139">**Laskeva**</span><span class="sxs-lookup"><span data-stu-id="bf435-139">**Descending**</span></span> | <span data-ttu-id="bf435-140">Keräystyö järjestetään laskevassa järjestyksessä lajitteluehtojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="bf435-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="bf435-141">Jos käytät **WMSLocationId**-kenttää lajitteluehtona ja sijaintitunnuksesi ovat 1, 2, 3 ja 4, keräät sijainnista 1 ensin.</span><span class="sxs-lookup"><span data-stu-id="bf435-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="bf435-142">Nimikkeen vahvistus</span><span class="sxs-lookup"><span data-stu-id="bf435-142">Item confirmation</span></span>

<span data-ttu-id="bf435-143">Kun klusterikeräily on käytössä, nimikkeen vahvistaminen on ehdottoman tärkeää, jotta klustereihin lisättävät nimikkeet voidaan tarkistaa.</span><span class="sxs-lookup"><span data-stu-id="bf435-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="bf435-144">Voit tarkistaa klusterikeräilyn nimikkeet klusterikeräilyn aikana.</span><span class="sxs-lookup"><span data-stu-id="bf435-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="bf435-145">Määritys perustuu tuotteen viivakoodin asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="bf435-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="bf435-146">Nimiketarkistuksen määrittäminen klusterikeräilyssä</span><span class="sxs-lookup"><span data-stu-id="bf435-146">Set up item verification with cluster picking</span></span>

1.  <span data-ttu-id="bf435-147">Avaa mobiililaitteen valikossa työn vahvistuksen määrityslomake: **Varastonhallinta** \> **Varastonhallinta** \> **Asetukset** \> **Mobiililaite** \> **Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="bf435-147">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** \> **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>

2.  <span data-ttu-id="bf435-148">Avaa mobiililaitteen valikossa **Työn vahvistusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="bf435-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="bf435-149">**Tuotteen vahvistus** -asetuksella voi tarkistaa kunkin varastokappaleen mobiililaitteessa skannauksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="bf435-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>
