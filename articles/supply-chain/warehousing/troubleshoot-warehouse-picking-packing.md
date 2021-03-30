---
title: Keräyksen ja pakkauksen vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä kerättäessä ja pakattaessa Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 01e33b63e09a035f5243bd57faf53b522737c987
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223239"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="f3eee-103">Keräyksen ja pakkauksen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="f3eee-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3eee-104">Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä kerättäessä ja pakattaessa Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="f3eee-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="f3eee-105">Seuraava virhesanoma avautuu: Dimension sijaintia ei voi jättää tyhjäksi, jos dimension sarjanumero on määritetty.</span><span class="sxs-lookup"><span data-stu-id="f3eee-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f3eee-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="f3eee-106">Issue description</span></span>

<span data-ttu-id="f3eee-107">Tämä virhesanoma avautuu, jos sarjanimikkeelle luodaan siirtotilaus käyttämällä varastoa, jossa on otettu käyttöön edistyksellinen varastonhallinta, ja kun lähetystä yritetään vahvistaa työn valmistumisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="f3eee-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f3eee-108">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f3eee-108">Issue resolution</span></span>

<span data-ttu-id="f3eee-109">Lähtövaraston kuljetusvaraston **Oletusvastaanottosijainti** -kenttä on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="f3eee-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="f3eee-110">Korjaa ongelma määrittämällä oletusvastaanottosijainti kuljetusvarastossa.</span><span class="sxs-lookup"><span data-stu-id="f3eee-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="f3eee-111">Varmista, että tämä sijainti on rekisterikilpiohjattu.</span><span class="sxs-lookup"><span data-stu-id="f3eee-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="f3eee-112">Seuraava virhesanoma avautuu: Virheellinen rekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="f3eee-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f3eee-113">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="f3eee-113">Issue description</span></span>

<span data-ttu-id="f3eee-114">Tämä virhesanoma avautuu varastosovelluksessa, kun rekisterikilven tunnus skannataan.</span><span class="sxs-lookup"><span data-stu-id="f3eee-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f3eee-115">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f3eee-115">Issue resolution</span></span>

<span data-ttu-id="f3eee-116">Varmista, että rekisterikilven tunnus on rekisterikilpitaulukossa ja että rekisterikilven nimikkeet ja määrät ovat käytettävissä (eli niitä ei ole estetty).</span><span class="sxs-lookup"><span data-stu-id="f3eee-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="f3eee-117">Seuraava virhesanoma avautuu: Kenttä Kuorman paino(=-%1) voi sisältää vain positiivisia lukuja.</span><span class="sxs-lookup"><span data-stu-id="f3eee-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="f3eee-118">Päivitys on keskeytetty.</span><span class="sxs-lookup"><span data-stu-id="f3eee-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f3eee-119">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="f3eee-119">Issue description</span></span>

<span data-ttu-id="f3eee-120">Tämä virhesanoma avautuu, jos työ on avoin, kun työ käsitellään pakkaussijainneista valmistelusijainteihin tai valmistelusijainneista laiturisijainteihin.</span><span class="sxs-lookup"><span data-stu-id="f3eee-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f3eee-121">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f3eee-121">Issue resolution</span></span>

<span data-ttu-id="f3eee-122">Voit korjata ongelman valitsemalla **Järjestelmänhallinta \> Kausittaiset tehtävät \> Tietokanta \> Yhdenmukaisuustarkistus** ja suorittamalla **Varaston kuorman painon yhdenmukaisuustarkistus** -prosessin.</span><span class="sxs-lookup"><span data-stu-id="f3eee-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="f3eee-123">Seuraava virhesanoma avautuu: Yksikön %1 määrä ei kelpaa.</span><span class="sxs-lookup"><span data-stu-id="f3eee-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f3eee-124">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="f3eee-124">Issue description</span></span>

<span data-ttu-id="f3eee-125">Tämä virhesanoma avautuu, kun yrität suorittaa *jaetun keräilyn* useissa erissä.</span><span class="sxs-lookup"><span data-stu-id="f3eee-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f3eee-126">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f3eee-126">Issue resolution</span></span>

<span data-ttu-id="f3eee-127">Varastotyöntekijän on käytettävä *Lyhyt keräily* -prosessia varastosovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f3eee-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="f3eee-128">Jos yrität kerätä useita eriä samasta sijainnista, voit käyttää myös varastosovelluksen **Täysi**-vaihtoehdolla.</span><span class="sxs-lookup"><span data-stu-id="f3eee-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="f3eee-129">Varastoa ei voi siirtää rekisterikilpiohjattuun sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="f3eee-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f3eee-130">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="f3eee-130">Issue description</span></span>

<span data-ttu-id="f3eee-131">Kuormituksen kerättyjä määriä ei voi vähentää.</span><span class="sxs-lookup"><span data-stu-id="f3eee-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f3eee-132">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f3eee-132">Issue resolution</span></span>

<span data-ttu-id="f3eee-133">Aiemmissa versioissa kuormituksen kerättyjä määriä ei voi vähentää.</span><span class="sxs-lookup"><span data-stu-id="f3eee-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="f3eee-134">Voit nyt kumota keräyksen rekisterikilpiohjattuun sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="f3eee-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="f3eee-135">Sekä **Sijainti**- että **Rekisterikilpi**-arvo on määritettävä kuormariville **Vähennä keräiltyä määrää** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f3eee-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="f3eee-136">Voidaanko toimitusilmoitus tai pakkaussisältö tulostaa varastokohtaisesti?</span><span class="sxs-lookup"><span data-stu-id="f3eee-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="f3eee-137">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="f3eee-137">Issue description</span></span>

<span data-ttu-id="f3eee-138">Haluat tulostaa toimitusilmoituksen tai pakkaussisällön varasto- tai sivustokohtaisesti **Työn tarkistusmallin rivien päivitys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f3eee-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f3eee-139">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f3eee-139">Issue resolution</span></span>

<span data-ttu-id="f3eee-140">Kun asiakirja tulostetaan tulostuksen hallinta-asetuksilla, rajoita laajuus (toimipaikka tai varasto) tulostuksen hallinnassa sen sijaan, että valitsisit **Muokkaa tulostusasetuksia** **Työn tarkistusmallin rivien päivitys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f3eee-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="f3eee-141">Pakkausluetteloa ei voi peruuttaa sen jälkeen, kun se on kirjattu myyntitilauksesta</span><span class="sxs-lookup"><span data-stu-id="f3eee-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f3eee-142">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="f3eee-142">Issue description</span></span>

<span data-ttu-id="f3eee-143">Kun keräily- ja lähetysprosessit on otettu käyttöön varastonhallintajärjestelmässä, pakkausluettelo ei voi peruuttaa, kun se on kirjattu myyntitilauksesta.</span><span class="sxs-lookup"><span data-stu-id="f3eee-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f3eee-144">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f3eee-144">Issue resolution</span></span>

<span data-ttu-id="f3eee-145">Varastonhallintajärjestelmää käyttävien nimikkeiden kirjattujen pakkausluetteloiden korjaaminen edellyttää, että kirjaaminen tehdään kuormasta eikä tilauksesta.</span><span class="sxs-lookup"><span data-stu-id="f3eee-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="f3eee-146">Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus.</span><span class="sxs-lookup"><span data-stu-id="f3eee-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="f3eee-147">Yleisesti ottaen myyntitilauksen, joka on kerätty ja lähetetty varastonhallintaprosesseilla, pakkausluettelopäivitys voidaan tehdä kuormituksesta tai lähetyksestä ja itse myyntitilausasiakirjasta.</span><span class="sxs-lookup"><span data-stu-id="f3eee-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="f3eee-148">Jos myyntitilauksen pakkausluettelopäivitys kuitenkin tehdään myyntitilausasiakirjasta, pakkausluettelon palautusta ei voi edelläänkään tehdä kuormasta tai myyntitilauksesta.</span><span class="sxs-lookup"><span data-stu-id="f3eee-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="f3eee-149">Tämän vuoksi kannattaa käyttää pakkausluettelon kirjaamista kuormasta.</span><span class="sxs-lookup"><span data-stu-id="f3eee-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="f3eee-150">Siinä tapauksessa kuormasta tehtävä peruutus otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="f3eee-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="f3eee-151">Seuraava virhesanoma avautuu: Klusterille ei löydy tarpeeksi työtä.</span><span class="sxs-lookup"><span data-stu-id="f3eee-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f3eee-152">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="f3eee-152">Issue description</span></span>

<span data-ttu-id="f3eee-153">Jos määrität *Järjestelmäohjattu klusterikeräily* -prosessia käytettäessä klusteriprofiilin, jossa voidaan kerätä esimerkiksi 10 paikkaa, prosessi toimii suunnitellusti, kun töitä on riittävästi 10 paikkaan keräilyyn.</span><span class="sxs-lookup"><span data-stu-id="f3eee-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="f3eee-154">Jos keräilyyn on kuitenkin vain kahdeksan paikkaa, tämä virhesanoma avautuu, koska työtä ei ole riittävästi yhdelle klusterille.</span><span class="sxs-lookup"><span data-stu-id="f3eee-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f3eee-155">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f3eee-155">Issue resolution</span></span>

<span data-ttu-id="f3eee-156">Korjaa tämä ongelma muokkaamalla klusteriprofiilia ja määrittämällä **Aktivoi toimet** -asetukseksi *Ei*.</span><span class="sxs-lookup"><span data-stu-id="f3eee-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]