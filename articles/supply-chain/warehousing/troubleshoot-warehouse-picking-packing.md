---
title: Keräyksen ja pakkauksen vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä kerättäessä ja pakattaessa Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 1a54fa9dc21fb1691d74905a1215f4dfea31f136
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828127"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="9d9c2-103">Keräyksen ja pakkauksen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="9d9c2-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d9c2-104">Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä kerättäessä ja pakattaessa Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="9d9c2-105">Seuraava virhesanoma avautuu: Dimension sijaintia ei voi jättää tyhjäksi, jos dimension sarjanumero on määritetty.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9d9c2-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="9d9c2-106">Issue description</span></span>

<span data-ttu-id="9d9c2-107">Tämä virhesanoma avautuu, jos sarjanimikkeelle luodaan siirtotilaus käyttämällä varastoa, jossa on otettu käyttöön edistyksellinen varastonhallinta, ja kun lähetystä yritetään vahvistaa työn valmistumisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9d9c2-108">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="9d9c2-108">Issue resolution</span></span>

<span data-ttu-id="9d9c2-109">Lähtövaraston kuljetusvaraston **Oletusvastaanottosijainti** -kenttä on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="9d9c2-110">Korjaa ongelma määrittämällä oletusvastaanottosijainti kuljetusvarastossa.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="9d9c2-111">Varmista, että tämä sijainti on rekisterikilpiohjattu.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="9d9c2-112">Seuraava virhesanoma avautuu: Virheellinen rekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9d9c2-113">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="9d9c2-113">Issue description</span></span>

<span data-ttu-id="9d9c2-114">Tämä virhesanoma avautuu varastonhallinnan mobiilisovelluksessa, kun rekisterikilven tunnus skannataan.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-114">You receive this error message in the Warehouse Management mobile app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9d9c2-115">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="9d9c2-115">Issue resolution</span></span>

<span data-ttu-id="9d9c2-116">Varmista, että rekisterikilven tunnus on rekisterikilpitaulukossa ja että rekisterikilven nimikkeet ja määrät ovat käytettävissä (eli niitä ei ole estetty).</span><span class="sxs-lookup"><span data-stu-id="9d9c2-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="9d9c2-117">Seuraava virhesanoma avautuu: Kenttä Kuorman paino(=-%1) voi sisältää vain positiivisia lukuja.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="9d9c2-118">Päivitys on keskeytetty.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9d9c2-119">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="9d9c2-119">Issue description</span></span>

<span data-ttu-id="9d9c2-120">Tämä virhesanoma avautuu, jos työ on avoin, kun työ käsitellään pakkaussijainneista valmistelusijainteihin tai valmistelusijainneista laiturisijainteihin.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9d9c2-121">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="9d9c2-121">Issue resolution</span></span>

<span data-ttu-id="9d9c2-122">Voit korjata ongelman valitsemalla **Järjestelmänhallinta \> Kausittaiset tehtävät \> Tietokanta \> Yhdenmukaisuustarkistus** ja suorittamalla **Varaston kuorman painon yhdenmukaisuustarkistus** -prosessin.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="9d9c2-123">Seuraava virhesanoma avautuu: Yksikön %1 määrä ei kelpaa.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9d9c2-124">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="9d9c2-124">Issue description</span></span>

<span data-ttu-id="9d9c2-125">Tämä virhesanoma avautuu, kun yrität suorittaa *jaetun keräilyn* useissa erissä.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9d9c2-126">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="9d9c2-126">Issue resolution</span></span>

<span data-ttu-id="9d9c2-127">Varastotyöntekijän on käytettävä *Lyhyt keräily* -prosessia varastonhallinnan mobiilisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-127">The warehouse worker must use the *Short picking* process in the Warehouse Management mobile app.</span></span> <span data-ttu-id="9d9c2-128">Jos yrität kerätä useita eriä samasta sijainnista, voit käyttää myös sovelluksen **Täysi**-vaihtoehdolla.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="9d9c2-129">Varastoa ei voi siirtää rekisterikilpiohjattuun sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9d9c2-130">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="9d9c2-130">Issue description</span></span>

<span data-ttu-id="9d9c2-131">Kuormituksen kerättyjä määriä ei voi vähentää.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9d9c2-132">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="9d9c2-132">Issue resolution</span></span>

<span data-ttu-id="9d9c2-133">Aiemmissa versioissa kuormituksen kerättyjä määriä ei voi vähentää.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="9d9c2-134">Voit nyt kumota keräyksen rekisterikilpiohjattuun sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="9d9c2-135">Sekä **Sijainti**- että **Rekisterikilpi**-arvo on määritettävä kuormariville **Vähennä keräiltyä määrää** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="9d9c2-136">Voidaanko toimitusilmoitus tai pakkaussisältö tulostaa varastokohtaisesti?</span><span class="sxs-lookup"><span data-stu-id="9d9c2-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="9d9c2-137">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="9d9c2-137">Issue description</span></span>

<span data-ttu-id="9d9c2-138">Haluat tulostaa toimitusilmoituksen tai pakkaussisällön varasto- tai sivustokohtaisesti **Työn tarkistusmallin rivien päivitys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9d9c2-139">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="9d9c2-139">Issue resolution</span></span>

<span data-ttu-id="9d9c2-140">Kun asiakirja tulostetaan tulostuksen hallinta-asetuksilla, rajoita laajuus (toimipaikka tai varasto) tulostuksen hallinnassa sen sijaan, että valitsisit **Muokkaa tulostusasetuksia** **Työn tarkistusmallin rivien päivitys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="9d9c2-141">Pakkausluetteloa ei voi peruuttaa sen jälkeen, kun se on kirjattu myyntitilauksesta</span><span class="sxs-lookup"><span data-stu-id="9d9c2-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9d9c2-142">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="9d9c2-142">Issue description</span></span>

<span data-ttu-id="9d9c2-143">Kun keräily- ja lähetysprosessit on otettu käyttöön varastonhallintajärjestelmässä, pakkausluettelo ei voi peruuttaa, kun se on kirjattu myyntitilauksesta.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9d9c2-144">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="9d9c2-144">Issue resolution</span></span>

<span data-ttu-id="9d9c2-145">Varastonhallintajärjestelmää käyttävien nimikkeiden kirjattujen pakkausluetteloiden korjaaminen edellyttää, että kirjaaminen tehdään kuormasta eikä tilauksesta.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="9d9c2-146">Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="9d9c2-147">Yleisesti ottaen myyntitilauksen, joka on kerätty ja lähetetty varastonhallintaprosesseilla, pakkausluettelopäivitys voidaan tehdä kuormituksesta tai lähetyksestä ja itse myyntitilausasiakirjasta.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="9d9c2-148">Jos myyntitilauksen pakkausluettelopäivitys kuitenkin tehdään myyntitilausasiakirjasta, pakkausluettelon palautusta ei voi edelläänkään tehdä kuormasta tai myyntitilauksesta.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="9d9c2-149">Tämän vuoksi kannattaa käyttää pakkausluettelon kirjaamista kuormasta.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="9d9c2-150">Siinä tapauksessa kuormasta tehtävä peruutus otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="9d9c2-151">Seuraava virhesanoma avautuu: Klusterille ei löydy tarpeeksi työtä.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9d9c2-152">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="9d9c2-152">Issue description</span></span>

<span data-ttu-id="9d9c2-153">Jos määrität *Järjestelmäohjattu klusterikeräily* -prosessia käytettäessä klusteriprofiilin, jossa voidaan kerätä esimerkiksi 10 paikkaa, prosessi toimii suunnitellusti, kun töitä on riittävästi 10 paikkaan keräilyyn.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="9d9c2-154">Jos keräilyyn on kuitenkin vain kahdeksan paikkaa, tämä virhesanoma avautuu, koska työtä ei ole riittävästi yhdelle klusterille.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9d9c2-155">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="9d9c2-155">Issue resolution</span></span>

<span data-ttu-id="9d9c2-156">Korjaa tämä ongelma muokkaamalla klusteriprofiilia ja määrittämällä **Aktivoi toimet** -asetukseksi *Ei*.</span><span class="sxs-lookup"><span data-stu-id="9d9c2-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]