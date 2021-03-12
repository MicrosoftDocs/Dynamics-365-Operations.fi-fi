---
title: Työkäytännöt
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää työkäytännöt.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 530abffb4c80a2d2f0e58e0c5a34294f7cba0b1a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998450"
---
# <a name="work-policies"></a><span data-ttu-id="4429e-103">Työkäytännöt</span><span class="sxs-lookup"><span data-stu-id="4429e-103">Work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4429e-104">Tässä ohjeaiheessa kerrotaan, miten järjestelmä ja varastosovellus määritetään niin, että ne tukevat työkäytäntöjä.</span><span class="sxs-lookup"><span data-stu-id="4429e-104">This topic explains how to set up the system and the warehouse app so that they support work policies.</span></span> <span data-ttu-id="4429e-105">Tämän toiminnon avulla voit rekisteröidä varaston nopeasti ilman hyllytystyön luomista silloin, kun vastaanotat osto- ja siirtotilauksia ja kun viimeistelet valmistusprosesseja.</span><span class="sxs-lookup"><span data-stu-id="4429e-105">You can use this functionality to quickly register inventory without creating putaway work when you receive purchase or transfer orders, or when you complete manufacturing processes.</span></span> <span data-ttu-id="4429e-106">Tämä ohjeaihe sisältää yleistietoja.</span><span class="sxs-lookup"><span data-stu-id="4429e-106">This topic provides general information.</span></span> <span data-ttu-id="4429e-107">Saat yksityiskohtaisia tietoja rekisterikilven vastaanotosta kohdassa [Rekisterikilven vastaanotto varastosovelluksen kautta](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="4429e-107">For detailed information that is related to license plate receiving, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="4429e-108">Työkäytäntö määrittää, luodaanko varastotyö valmistetun nimikkeen valmiiksi raportoinnin yhteydessä vai silloin, kun tavarat vastaanotetaan käyttämällä varastosovellusta.</span><span class="sxs-lookup"><span data-stu-id="4429e-108">A work policy controls whether warehouse work is created when a manufactured item is reported as finished, or when goods are received by using the warehouse app.</span></span> <span data-ttu-id="4429e-109">Voit määrittää kunkin työkäytännön määrittämällä sen ehdot: työtilaustyypit ja -prosessit, varaston sijainnin ja (vaihtoehtoisesti) tuotteet.</span><span class="sxs-lookup"><span data-stu-id="4429e-109">You set up each work policy by defining the conditions where it applies: the work order types and processes, the inventory location, and (optionally) the products.</span></span> <span data-ttu-id="4429e-110">Esimerkiksi ostotilaus tuotteelle *A0001* on vastaanotettava sijainnissa *RECV* varastossa *24*.</span><span class="sxs-lookup"><span data-stu-id="4429e-110">For example, a purchase order for product *A0001* must be received in location *RECV* in warehouse *24*.</span></span> <span data-ttu-id="4429e-111">Myöhemmin tuotetta kulutetaan toisessa prosessissa sijainnissa *RECV*.</span><span class="sxs-lookup"><span data-stu-id="4429e-111">Later, the product is consumed in another process at location *RECV*.</span></span> <span data-ttu-id="4429e-112">Tässä tapauksessa määrität työkäytännön, joka estää hyllytystyön luomisen, kun työntekijä raportoi tuotteen *A0001* vastaanotetuksi sijainnissa *RECV*.</span><span class="sxs-lookup"><span data-stu-id="4429e-112">In this case, you can set up a work policy to prevent putaway work from being created when a worker reports product *A0001* as received in location *RECV*.</span></span>

> [!NOTE]
> - <span data-ttu-id="4429e-113">Jotta työkäytäntö olisi aktiivinen, määritä sille ensin vähintään yksi sijainti **Varastosijainnit**-pikavälilehdessä **Työkäytännöt**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="4429e-113">For a work policy to be active, you must define at least one location for it on the **Inventory locations** FastTab of the **Work policies** page.</span></span> 
> - <span data-ttu-id="4429e-114">Et voi määrittää samaa sijaintia useille työkäytännöille.</span><span class="sxs-lookup"><span data-stu-id="4429e-114">You can't specify the same location for multiple work policies.</span></span>
> - <span data-ttu-id="4429e-115">Mobiililaitteen valikon vaihtoehtojen **Tulosta tarra** -asetus ei tulosta rekisterikilven otsikkoa, jos työtä ei ole luotu.</span><span class="sxs-lookup"><span data-stu-id="4429e-115">The **Print label** option for mobile device menu items won't print a license plate label unless work was created.</span></span>

## <a name="activate-the-features-in-your-system"></a><span data-ttu-id="4429e-116">Järjestelmän ominaisuuksien aktivoiminen</span><span class="sxs-lookup"><span data-stu-id="4429e-116">Activate the features in your system</span></span>

<span data-ttu-id="4429e-117">Voit ottaa tämän ohjeaiheen kaikki toiminnot käyttöön järjestelmässä ottamalla seuraavat kaksi ominaisuutta käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span><span class="sxs-lookup"><span data-stu-id="4429e-117">To make all the functionality that is described in this topic available in your system, turn on the following two features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span></span>

- <span data-ttu-id="4429e-118">Rekisterikilven vastaanoton parannukset</span><span class="sxs-lookup"><span data-stu-id="4429e-118">License plate receiving enhancements</span></span>
- <span data-ttu-id="4429e-119">Saapuvan työn työkäytäntöjen parannukset</span><span class="sxs-lookup"><span data-stu-id="4429e-119">Work policy enhancements for inbound work</span></span>

## <a name="the-work-policies-page"></a><span data-ttu-id="4429e-120">Työkäytännöt-sivu</span><span class="sxs-lookup"><span data-stu-id="4429e-120">The Work policies page</span></span>

<span data-ttu-id="4429e-121">Voit määrittää työkäytännöt siirtymällä kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työkäytännöt**.</span><span class="sxs-lookup"><span data-stu-id="4429e-121">To set up work policies, go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span> <span data-ttu-id="4429e-122">Määritä sitten kunkin pikavälilehden kentät seuraavien aliosien mukaan.</span><span class="sxs-lookup"><span data-stu-id="4429e-122">Then, on each FastTab, set the fields as described in the following subsections.</span></span>

### <a name="the-work-order-types-fasttab"></a><span data-ttu-id="4429e-123">Työtilaustyypit-pikavälilehti</span><span class="sxs-lookup"><span data-stu-id="4429e-123">The Work order types FastTab</span></span>

<span data-ttu-id="4429e-124">Lisää **Työtilaustyypit**-pikavälilehteen kaikki työtilaustyypit ja liittyvät työprosessit, joita työkäytäntö koskee.</span><span class="sxs-lookup"><span data-stu-id="4429e-124">On the **Work order types** FastTab, add all the work order types, and the related work processes, that the work policy applies to.</span></span> <span data-ttu-id="4429e-125">Työkäytännöt tukevat seuraavia työtilaustyyppejä ja liittyviä työprosesseja.</span><span class="sxs-lookup"><span data-stu-id="4429e-125">The following work order types and related work processes are supported for work policies.</span></span>

| <span data-ttu-id="4429e-126">Työtilaustyyppi</span><span class="sxs-lookup"><span data-stu-id="4429e-126">Work order type</span></span> | <span data-ttu-id="4429e-127">Työprosessi</span><span class="sxs-lookup"><span data-stu-id="4429e-127">Work process</span></span> |
|---|---|
| <span data-ttu-id="4429e-128">Raaka-aineiden keräily</span><span class="sxs-lookup"><span data-stu-id="4429e-128">Raw material picking</span></span>| <span data-ttu-id="4429e-129">Kaikki liittyvät prosessit</span><span class="sxs-lookup"><span data-stu-id="4429e-129">All related processes</span></span> |
| <span data-ttu-id="4429e-130">Rinnakkaistuotteen ja sivutuotteen poispano</span><span class="sxs-lookup"><span data-stu-id="4429e-130">Co-product and by-product put away</span></span> | <span data-ttu-id="4429e-131">Kaikki liittyvät prosessit</span><span class="sxs-lookup"><span data-stu-id="4429e-131">All related processes</span></span> |
| <span data-ttu-id="4429e-132">Valmiiden tuotteiden hyllytys</span><span class="sxs-lookup"><span data-stu-id="4429e-132">Finished goods putaway</span></span> | <span data-ttu-id="4429e-133">Kaikki liittyvät prosessit</span><span class="sxs-lookup"><span data-stu-id="4429e-133">All related processes</span></span> |
| <span data-ttu-id="4429e-134">Siirron vastaanotto</span><span class="sxs-lookup"><span data-stu-id="4429e-134">Transfer receipt</span></span> | <span data-ttu-id="4429e-135">Rekisterikilven vastaanotto (ja hyllytys)</span><span class="sxs-lookup"><span data-stu-id="4429e-135">License plate receiving (and putaway)</span></span> |
| <span data-ttu-id="4429e-136">Ostotilaukset</span><span class="sxs-lookup"><span data-stu-id="4429e-136">Purchase orders</span></span> | <ul><li><span data-ttu-id="4429e-137">Rekisterikilven vastaanotto (ja hyllytys)</span><span class="sxs-lookup"><span data-stu-id="4429e-137">License plate receiving (and putaway)</span></span></li><li><span data-ttu-id="4429e-138">Kuorman nimikkeen vastaanotto (ja hyllytys)</span><span class="sxs-lookup"><span data-stu-id="4429e-138">Load item receiving (and putaway)</span></span></li><li><span data-ttu-id="4429e-139">Ostotilausrivin vastaanotto (ja hyllytys)</span><span class="sxs-lookup"><span data-stu-id="4429e-139">Purchase order line receiving (and putaway)</span></span></li><li><span data-ttu-id="4429e-140">Ostotilausnimikkeen vastaanotto (ja hyllytys)</span><span class="sxs-lookup"><span data-stu-id="4429e-140">Purchase order item receiving (and putaway)</span></span></li></ul> |

<span data-ttu-id="4429e-141">Jos haluat määrittää työkäytännön niin, että se koskee saman työtilaustyypin useita työprosesseja, lisää erillinen rivi jokaiselle ruudukon työprosessille.</span><span class="sxs-lookup"><span data-stu-id="4429e-141">To set up a work policy so that it applies to several work processes of the same work order type, add a separate line for each work process to the grid.</span></span>

<span data-ttu-id="4429e-142">Määritä ruudukon jokaisen rivin **Työn luontimenetelmä** -kenttään jokin seuraavista arvoista:</span><span class="sxs-lookup"><span data-stu-id="4429e-142">For each line in the grid, set the **Work creation method** field to one of the following values:</span></span>

- <span data-ttu-id="4429e-143">**Ei koskaan** – Työkäytäntö estää varastotyön luomisen valitulle työtilaustyypille ja liittyvälle työprosessille.</span><span class="sxs-lookup"><span data-stu-id="4429e-143">**Never** – The work policy will prevent warehouse work from being created for the selected work order type and related work process.</span></span>
- <span data-ttu-id="4429e-144">**Cross-docking** – Työkäytäntö luo cross-docking-työn käyttämällä **Cross-docking-käytännön nimi** -kentässä valittua käytäntöä.</span><span class="sxs-lookup"><span data-stu-id="4429e-144">**Cross docking** – The work policy will create cross-docking work by using the policy that you select in the **Cross docking policy name** field.</span></span>

### <a name="the-inventory-locations-fasttab"></a><span data-ttu-id="4429e-145">Varastosijainnit-pikavälilehti</span><span class="sxs-lookup"><span data-stu-id="4429e-145">The Inventory locations FastTab</span></span>

<span data-ttu-id="4429e-146">Lisää **Varastosijainnit**-pikavälilehteen kaikki sijainnit, joihin tämä työkäytäntö tulee kohdistaa.</span><span class="sxs-lookup"><span data-stu-id="4429e-146">On the **Inventory locations** FastTab, add all the locations where this work policy should be applied.</span></span> <span data-ttu-id="4429e-147">Jos sijaintia ei ole liitetty työkäytäntöön, työkäytäntöä ei käytetä missään prosessissa.</span><span class="sxs-lookup"><span data-stu-id="4429e-147">If no location is associated with a work policy, the work policy won't be applied to any process.</span></span>

<span data-ttu-id="4429e-148">Et voi määrittää samaa sijaintia useille työkäytännöille.</span><span class="sxs-lookup"><span data-stu-id="4429e-148">You can't specify the same location for multiple work policies.</span></span>

<span data-ttu-id="4429e-149">Voit käyttää sijaintiprofiiliin määritettyä varastopaikkaa, jonka **rekisterikilven seuranta** on poistettu käytöstä.</span><span class="sxs-lookup"><span data-stu-id="4429e-149">You can use a warehouse location that is assigned to a location profile where the **Use license plate tracking** option is turned off.</span></span> <span data-ttu-id="4429e-150">Tällöin työntekijät rekisteröivät käytettävissä olevan varaston suoraan.</span><span class="sxs-lookup"><span data-stu-id="4429e-150">In this case, workers will directly register the on-hand inventory.</span></span>

### <a name="the-products-fasttab"></a><span data-ttu-id="4429e-151">Tuotteet-pikavälilehti</span><span class="sxs-lookup"><span data-stu-id="4429e-151">The Products FastTab</span></span>

<span data-ttu-id="4429e-152">Määritä **Tuotteet**-välilehdessä **Tuotevalinta**-kenttä niin, että se ohjaa käytäntöjen kohdistamista tuotteisiin seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4429e-152">On the **Products** tab, set the **Product selection** field to control which products the policy should apply to:</span></span>

- <span data-ttu-id="4429e-153">**Kaikki** – Käytäntö kohdistetaan kaikkiin tuotteisiin.</span><span class="sxs-lookup"><span data-stu-id="4429e-153">**All** – The policy should apply to all products.</span></span>
- <span data-ttu-id="4429e-154">**Valittu** – Käytäntö kohdistetaan vain tuotteisiin, jotka ovat ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="4429e-154">**Selected** – The policy should apply only to products that are listed in the grid.</span></span> <span data-ttu-id="4429e-155">Käytä **Tuotteet**-pikavälilehden työkaluriviä, jos haluat lisätä tuotteita ruudukkoon tai poistaa niitä ruudukosta.</span><span class="sxs-lookup"><span data-stu-id="4429e-155">Use the toolbar on the **Products** FastTab to add products to the grid or remove them from the grid.</span></span>

## <a name="default-and-custom-to-locations"></a><span data-ttu-id="4429e-156">Oletus- ja mukautetut kohdesijainnit</span><span class="sxs-lookup"><span data-stu-id="4429e-156">Default and custom "to" locations</span></span>

> [!NOTE]
> <span data-ttu-id="4429e-157">Jos haluat määrittää tässä osassa kuvaillun toiminnon käytettäväksi järjestelmässä, ota käyttöön *Rekisterikilven vastaanoton parannukset*- ja *Työkäytännön parannukset saapuvalle työlle* -toiminnot [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="4429e-157">To make the functionality that is described in this section available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="4429e-158">Aiemmin järjestelmä tuki vain kullekin varastolle määritettyä oletussijaintia.</span><span class="sxs-lookup"><span data-stu-id="4429e-158">Previously, the system supported receiving only at the default location that is defined for each warehouse.</span></span> <span data-ttu-id="4429e-159">Seuraavia työn luontiprosesseja käyttävät mobiililaitteen valikon vaihtoehdot sisältävät nyt kuitenkin **Käytä oletustietoja** -vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="4429e-159">However, mobile device menu items that use the following work creation processes now provide the **Use default data** option.</span></span> <span data-ttu-id="4429e-160">Tämän vaihtoehdon avulla voit määrittää kohdesijainnin yhdelle tai usealle valikon vaihtoehdolle.</span><span class="sxs-lookup"><span data-stu-id="4429e-160">This option lets you assign a custom "to" location to one or more menu items.</span></span> <span data-ttu-id="4429e-161">(Tämä vaihtoehto on jo käytettävissä joidenkin muun tyyppisten valikkovaihtoehtojen yhteydessä.)</span><span class="sxs-lookup"><span data-stu-id="4429e-161">(This option was already available for some other types of menu items.)</span></span>

- <span data-ttu-id="4429e-162">Rekisterikilven vastaanotto (ja hyllytys)</span><span class="sxs-lookup"><span data-stu-id="4429e-162">License plate receiving (and putaway)</span></span>
- <span data-ttu-id="4429e-163">Kuorman nimikkeen vastaanotto (ja hyllytys)</span><span class="sxs-lookup"><span data-stu-id="4429e-163">Load item receiving (and putaway)</span></span>
- <span data-ttu-id="4429e-164">Ostotilausrivin vastaanotto (ja hyllytys)</span><span class="sxs-lookup"><span data-stu-id="4429e-164">Purchase order line receiving (and putaway)</span></span>
- <span data-ttu-id="4429e-165">Ostotilausnimikkeen vastaanotto (ja hyllytys)</span><span class="sxs-lookup"><span data-stu-id="4429e-165">Purchase order item receiving (and putaway)</span></span>

<span data-ttu-id="4429e-166">Valikon vaihtoehdon **Kohdesijainti**-asetus korvaa varaston oletusvastaanottosijainnin kaikissa tilauksissa, jotka on käsitelty kyseisen valikon vaihtoehdon avulla.</span><span class="sxs-lookup"><span data-stu-id="4429e-166">The **To location** setting for a menu item overrides the default receiving location for the warehouse, for all orders that are processed by using that menu item.</span></span>

<span data-ttu-id="4429e-167">Voit määrittää mobiililaitteen valikon vaihtoehdon tukemaan vastaanottoa mukautetussa sijainnissa alla olevien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="4429e-167">To set up a mobile device menu item to support receiving at a custom location, follow these steps.</span></span>

1. <span data-ttu-id="4429e-168">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="4429e-168">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="4429e-169">Valitse valikon vaihtoehto, joka käyttää jotain aiemmin tässä osassa mainittua työn luontiprosessia, tai luo valikon vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="4429e-169">Select or create a menu item that uses one of the work creation processes that are listed earlier in this section.</span></span>
1. <span data-ttu-id="4429e-170">Määritä **Yleinen**-pikavälilehdessä **Käytä oletustietoja** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4429e-170">On the **General** FastTab, set the **Use default data** option to **Yes**.</span></span>
1. <span data-ttu-id="4429e-171">Valitse toimintoruudusta **Oletustiedot**.</span><span class="sxs-lookup"><span data-stu-id="4429e-171">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="4429e-172">Määritä **Oletustiedot**-sivulla seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="4429e-172">On the **Default data** page, set the following values:</span></span>

    - <span data-ttu-id="4429e-173">**Oletustietokenttä:** Määritä tämän kentän arvoksi *Kohdesijainti*.</span><span class="sxs-lookup"><span data-stu-id="4429e-173">**Default data field:** Set this field to *To location*.</span></span>
    - <span data-ttu-id="4429e-174">**Varasto:** Valitse tämän valikon vaihtoehdon yhteydessä käytettävä kohdevarasto.</span><span class="sxs-lookup"><span data-stu-id="4429e-174">**Warehouse:** Select the destination warehouse to use with this menu item.</span></span>
    - <span data-ttu-id="4429e-175">**Sijainti:** Tässä kentässä ovat kaikki sijaintien tunnukset, jotka ovat käytettävissä valitussa varastossa.</span><span class="sxs-lookup"><span data-stu-id="4429e-175">**Location:** This field lists all the location IDs that are available for the selected warehouse.</span></span> <span data-ttu-id="4429e-176">Tämän kentän määrittäminen ei kuitenkaan muuta tilannetta.</span><span class="sxs-lookup"><span data-stu-id="4429e-176">However, the setting of this field doesn't actually have any effect.</span></span> <span data-ttu-id="4429e-177">Tämän vuoksi kenttä voidaan jättää tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="4429e-177">Therefore, you can leave it blank.</span></span> <span data-ttu-id="4429e-178">Voit silti käyttää luetteloa, jos haluat varmistaa **Kovakoodattu arvo** -kenttään annettavan tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="4429e-178">Nevertheless, you can use the list to confirm the ID that you must enter in the **Hardcoded value** field.</span></span>
    - <span data-ttu-id="4429e-179">**Kovakoodattu arvo:** Anna sijainnin tunnus vastaanottosijainnille, joka koskee tätä valikon vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="4429e-179">**Hardcoded value:** Enter the location ID for the receiving location that applies to this menu item.</span></span>

> [!TIP]
> <span data-ttu-id="4429e-180">Työkäytäntö voidaan kohdistaa vain, jos kaikki vastaanottosijainnit on luetteloitu liittyvän työkäytännön asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="4429e-180">A work policy can be applied only if all the receiving locations are listed in the relevant work policy setup.</span></span> <span data-ttu-id="4429e-181">Tämä vaatimus on voimassa siitä huolimatta, onko käytössä varaston oletusvastaanottopaikka vai mukautettu kohdesijainti.</span><span class="sxs-lookup"><span data-stu-id="4429e-181">This requirement applies regardless of whether you're using the default warehouse receiving location or a custom "to" location.</span></span>

## <a name="example-scenario-warehouse-receiving"></a><span data-ttu-id="4429e-182">Esimerkkiskenaario: Varaston vastaanotto</span><span class="sxs-lookup"><span data-stu-id="4429e-182">Example scenario: Warehouse receiving</span></span>

<span data-ttu-id="4429e-183">Kaikki tuotteet, jotka on vastaanotettu *Ostotilausnimikkeen vastaanotto (ja hyllytys)* -prosessin avulla, on rekisteröitävä sijainnissa *FL-001*. Niiden on myös oltava käytettävissä varastossa *24*.</span><span class="sxs-lookup"><span data-stu-id="4429e-183">All products that are received by the *Purchase order item receiving (and putaway)* process must be registered in location *FL-001*, and they must be available in warehouse *24*.</span></span> <span data-ttu-id="4429e-184">Työtä ei kuitenkaan tule luoda.</span><span class="sxs-lookup"><span data-stu-id="4429e-184">However, work should not be created.</span></span> <span data-ttu-id="4429e-185">Tuotteet, jotka vastaanotetaan jonkin muun prosessin avulla (käyttämällä muita mobiililaitteen valikon vaihtoehtoja), on rekisteröitävä varaston oletusvastaanottosijaintiin (*RECV*). Työ tulee luoda normaaliin tapaan.</span><span class="sxs-lookup"><span data-stu-id="4429e-185">Products that are received by any other process (that is, by using other mobile device menu items) should be registered at the default warehouse receiving location (*RECV*), and work should be created as usual.</span></span> <span data-ttu-id="4429e-186">(Tässä skenaariossa ei näytetä vastaanoton oletusasetuksia.)</span><span class="sxs-lookup"><span data-stu-id="4429e-186">(This scenario doesn't show the default receiving setup.)</span></span>

<span data-ttu-id="4429e-187">Tämä skenaario edellyttää seuraavia elementtejä:</span><span class="sxs-lookup"><span data-stu-id="4429e-187">This scenario requires the following elements:</span></span>

- <span data-ttu-id="4429e-188">*Ostotilausnimikkeen vastaanotto (ja hyllytys)* -prosessin työkäytäntö sijainnissa *FL-001* kaikille tuotteille</span><span class="sxs-lookup"><span data-stu-id="4429e-188">A work policy for the *Purchase order item receiving (and putaway)* process in location *FL-001*, for all products</span></span>
- <span data-ttu-id="4429e-189">Mobiililaitteen valikon vaihtoehto, jolla on oletustiedot ja joka määrittää **Kohdesijainti**-kentän arvoksi *FL-001*</span><span class="sxs-lookup"><span data-stu-id="4429e-189">A mobile device menu item that has default data, and that sets the **To location** field to *FL-001*</span></span>

### <a name="prerequisites"></a><span data-ttu-id="4429e-190">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="4429e-190">Prerequisites</span></span>

<span data-ttu-id="4429e-191">Jos haluat määrittää tässä skenaariossa kuvaillun toiminnon käytettäväksi järjestelmässä, ota käyttöön *Rekisterikilven vastaanoton parannukset*- ja *Työkäytännön parannukset saapuvalle työlle* -toiminnot [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="4429e-191">To make the functionality that is described in this scenario available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="4429e-192">Tässä skenaariossa käytetään vakioesittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="4429e-192">This scenario uses the standard demo data.</span></span> <span data-ttu-id="4429e-193">Jos siis haluat käsitellä tätä skenaariota käyttämällä tässä annettuja arvoja, sinun on työskenneltävä järjestelmässä, johon on asennettu esittelytiedot.</span><span class="sxs-lookup"><span data-stu-id="4429e-193">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="4429e-194">Sinun on myös valittava **USMF**-yritys.</span><span class="sxs-lookup"><span data-stu-id="4429e-194">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-work-policy"></a><span data-ttu-id="4429e-195">Määritä työkäytäntö</span><span class="sxs-lookup"><span data-stu-id="4429e-195">Set up a work policy</span></span>

1. <span data-ttu-id="4429e-196">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työkäytännöt**.</span><span class="sxs-lookup"><span data-stu-id="4429e-196">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="4429e-197">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4429e-197">Select **New**.</span></span>
1. <span data-ttu-id="4429e-198">Anna **Työkäytännön nimi** -kenttään *Ei ostonimikkeen hyllytystyötä*.</span><span class="sxs-lookup"><span data-stu-id="4429e-198">In the **Work policy name** field, enter *No purchase item putaway work*.</span></span>
1. <span data-ttu-id="4429e-199">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4429e-199">Select **Save**.</span></span>
1. <span data-ttu-id="4429e-200">Valitse **Työtilaustyypit**-pikavälilehdessä **Lisää**, jos haluat lisätä rivin ruudukkoon. Määritä sitten uuden rivin seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="4429e-200">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="4429e-201">**Työtilaustyyppi:** *Ostotilaukset*</span><span class="sxs-lookup"><span data-stu-id="4429e-201">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="4429e-202">**Työprosessi:** *Ostotilausnimikkeen vastaanotto (ja hyllytys)*</span><span class="sxs-lookup"><span data-stu-id="4429e-202">**Work process:** *Purchase order item receiving (and putaway)*</span></span>
    - <span data-ttu-id="4429e-203">**Työn luontimenetelmä:** *Ei koskaan*</span><span class="sxs-lookup"><span data-stu-id="4429e-203">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="4429e-204">**Cross-docking-käytännön nimi:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="4429e-204">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="4429e-205">Valitse **Varastosijainnit**-pikavälilehdessä **Lisää**, jos haluat lisätä rivin ruudukkoon. Määritä sitten uuden rivin seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="4429e-205">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="4429e-206">**Varasto**: *24*</span><span class="sxs-lookup"><span data-stu-id="4429e-206">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="4429e-207">**Sijainti:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="4429e-207">**Location:** *FL-001*</span></span>

1. <span data-ttu-id="4429e-208">Määritä **Tuotteet**-pikavälilehdessä **Tuotteen valinta** -kentän arvoksi *Kaikki*.</span><span class="sxs-lookup"><span data-stu-id="4429e-208">On the **Products** FastTab, set the **Product selection** field to *All*.</span></span>
1. <span data-ttu-id="4429e-209">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4429e-209">Select **Save**.</span></span>

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a><span data-ttu-id="4429e-210">Määritä mobiililaitteen valikon vaihtoehto, jos haluat muuttaa vastaanottosijaintia</span><span class="sxs-lookup"><span data-stu-id="4429e-210">Set up a mobile device menu item to change the receiving location</span></span>

1. <span data-ttu-id="4429e-211">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="4429e-211">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="4429e-212">Valitse vasemmanpuoleisessa ruudussa olemassa oleva valikon **Oston vastaanotto** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="4429e-212">In the left pane, select the existing **Purchase receive** menu item.</span></span>
1. <span data-ttu-id="4429e-213">Määritä **Yleinen**-pikavälilehdessä **Käytä oletustietoja** -asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="4429e-213">On the **General** FastTab, set the **Use default data** option to *Yes*.</span></span>
1. <span data-ttu-id="4429e-214">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4429e-214">Select **Save**.</span></span>
1. <span data-ttu-id="4429e-215">Valitse toimintoruudusta **Oletustiedot**.</span><span class="sxs-lookup"><span data-stu-id="4429e-215">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="4429e-216">Valitse **Oletustiedot**-sivun toimintoruudussa **Uusi**, jos haluat lisätä rivin ruudukkoon. Määritä sitten uuden rivin seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="4429e-216">On the **Default data** page, on the Action Pane, select **New** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="4429e-217">**Oletustietokenttä:** *Kohdesijainti*</span><span class="sxs-lookup"><span data-stu-id="4429e-217">**Default data field:** *To location*</span></span>
    - <span data-ttu-id="4429e-218">**Varasto**: *24*</span><span class="sxs-lookup"><span data-stu-id="4429e-218">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="4429e-219">**SIjainti:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="4429e-219">**Location:** Leave this field blank.</span></span>
    - <span data-ttu-id="4429e-220">**Kovakoodattu arvo:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="4429e-220">**Hardcoded value:** *FL-001*</span></span>

1. <span data-ttu-id="4429e-221">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4429e-221">Select **Save**.</span></span>

### <a name="receive-a-purchase-order-without-creating-work"></a><span data-ttu-id="4429e-222">Ostotilauksen vastaanottaminen ilman työn luomista</span><span class="sxs-lookup"><span data-stu-id="4429e-222">Receive a purchase order without creating work</span></span>

<span data-ttu-id="4429e-223">Tämä osan esimerkki osoittaa, miten ostotilausnimike vastaanotetaan ilman työn luomista sijainnissa, joka on eri kuin tälle varastolle määritetty oletusvastaanottosijainti.</span><span class="sxs-lookup"><span data-stu-id="4429e-223">The example in this section shows how to receive a purchase order item, but without creating work, at a location that differs from the default receiving location that is set up for the warehouse.</span></span> <span data-ttu-id="4429e-224">Tässä esimerkissä käytetään työkäytäntöä ja mobiililaitenimikettä, jotka luotiin aiemmin tässä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="4429e-224">This example uses the work policy and mobile device item that you created earlier in this scenario.</span></span>

#### <a name="create-a-purchase-order"></a><span data-ttu-id="4429e-225">Ostotilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="4429e-225">Create a purchase order</span></span>

1. <span data-ttu-id="4429e-226">Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="4429e-226">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="4429e-227">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4429e-227">Select **New**.</span></span>
1. <span data-ttu-id="4429e-228">Aseta **Luo ostotilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="4429e-228">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4429e-229">**Toimittajan tili:** *US-101*</span><span class="sxs-lookup"><span data-stu-id="4429e-229">**Vendor account:** *US-101*</span></span>
    - <span data-ttu-id="4429e-230">**Toimipaikka:** *2*</span><span class="sxs-lookup"><span data-stu-id="4429e-230">**Site:** *2*</span></span>
    - <span data-ttu-id="4429e-231">**Varasto**: *24*</span><span class="sxs-lookup"><span data-stu-id="4429e-231">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="4429e-232">Valitse **OK**, jos haluat sulkea valintaikkunan ja avata uuden ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="4429e-232">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="4429e-233">Määritä **Ostotilausrivit**-pikavälilehdessä seuraavat arvot tyhjälle riville:</span><span class="sxs-lookup"><span data-stu-id="4429e-233">On the **Purchase order lines** FastTab, set the following values for the empty row:</span></span>

    - <span data-ttu-id="4429e-234">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="4429e-234">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="4429e-235">**Määrä** *1*</span><span class="sxs-lookup"><span data-stu-id="4429e-235">**Quantity:** *1*</span></span>

1. <span data-ttu-id="4429e-236">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4429e-236">Select **Save**.</span></span>
1. <span data-ttu-id="4429e-237">Kirjoita ostotilauksen numero muistiin.</span><span class="sxs-lookup"><span data-stu-id="4429e-237">Make a note of the purchase order number.</span></span>

#### <a name="receive-a-purchase-order"></a><span data-ttu-id="4429e-238">Ostotilauksen vastaanottaminen</span><span class="sxs-lookup"><span data-stu-id="4429e-238">Receive a purchase order</span></span>

1. <span data-ttu-id="4429e-239">Kirjaudu mobiililaitteella varastoon *24* käyttämällä käyttäjätunnusta *24* ja salasanaa *1*.</span><span class="sxs-lookup"><span data-stu-id="4429e-239">On the mobile device, sign in to warehouse *24* by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="4429e-240">Valitse **Saapuva**.</span><span class="sxs-lookup"><span data-stu-id="4429e-240">Select **Inbound**.</span></span>
1. <span data-ttu-id="4429e-241">Valitse **Oston vastaanotto**.</span><span class="sxs-lookup"><span data-stu-id="4429e-241">Select **Purchase receive**.</span></span> <span data-ttu-id="4429e-242">**Sijainti**-kentän arvoksi tulee määrittää *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="4429e-242">The **Location** field should be set to *FL-001*.</span></span>
1. <span data-ttu-id="4429e-243">Anna edellisessä proseduurissa luodun ostotilauksen ostotilausnumero.</span><span class="sxs-lookup"><span data-stu-id="4429e-243">Enter the purchase order number for the purchase order that you created in the previous procedure.</span></span>
1. <span data-ttu-id="4429e-244">Anna **Nimiketunnus**-kenttään arvo *A0001*.</span><span class="sxs-lookup"><span data-stu-id="4429e-244">In the **Item number** field, enter *A0001*.</span></span>
1. <span data-ttu-id="4429e-245">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="4429e-245">Select **OK**.</span></span>
1. <span data-ttu-id="4429e-246">Kirjoita **Määrä**-kenttään *1*.</span><span class="sxs-lookup"><span data-stu-id="4429e-246">In the **Quantity** field, enter *1*.</span></span>
1. <span data-ttu-id="4429e-247">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="4429e-247">Select **OK**.</span></span>

<span data-ttu-id="4429e-248">Ostotilaus on nyt vastaanotettu, mutta siihen ei ole liitetty työtä.</span><span class="sxs-lookup"><span data-stu-id="4429e-248">The purchase order is now received, but no work is associated with it.</span></span> <span data-ttu-id="4429e-249">Käytettävissä oleva varasto on päivitetty. Määrä *1* nimikettä *A0001* on nyt käytettävissä sijainnissa *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="4429e-249">The on-hand inventory has been updated, and a quantity of *1* of item *A0001* is now available at location *FL-001*.</span></span>

## <a name="example-scenario-manufacturing"></a><span data-ttu-id="4429e-250">Esimerkkiskenaario: Valmistus</span><span class="sxs-lookup"><span data-stu-id="4429e-250">Example scenario: Manufacturing</span></span>

<span data-ttu-id="4429e-251">Seuraavassa esimerkissä on kaksi tuotantotilausta, jotka ovat *PRD-001* ja *PRD-002*.</span><span class="sxs-lookup"><span data-stu-id="4429e-251">In the following example, there are two production orders, *PRD-001* and *PRD-002*.</span></span> <span data-ttu-id="4429e-252">Tuotantotilaus *PRD-001* sisältää *Kokoonpano*-työvaiheen, jolla tuote *SC1* raportoidaan valmiiksi sijainnissa *001*.</span><span class="sxs-lookup"><span data-stu-id="4429e-252">Production order *PRD-001* has an operation that is named *Assembly*, where product *SC1* is being reported as finished to location *001*.</span></span> <span data-ttu-id="4429e-253">Tuotantotilaus *PRD-002* sisältää *Maalaus*-työvaiheen ja käyttää tuotetta *SC1* sijainnista *001*.</span><span class="sxs-lookup"><span data-stu-id="4429e-253">Production order *PRD-002* has an operation that is named *Painting* and consumes product *SC1* from location *001*.</span></span> <span data-ttu-id="4429e-254">Tuotantotilaus *PRD-002* käyttää myös raaka-ainetta *RM1* sijainnissa *001*.</span><span class="sxs-lookup"><span data-stu-id="4429e-254">Production order *PRD-002* also consumes raw material *RM1* from location *001*.</span></span> <span data-ttu-id="4429e-255">Raaka-ainetta *RM1* varastoidaan varastosijaintiin *BULK-001*, josta raaka-ainekeräilyn varastotyö kerää sen sijaintiin *001*.</span><span class="sxs-lookup"><span data-stu-id="4429e-255">Raw material *RM1* is stored in warehouse location *BULK-001* and will be picked to location *001* by warehouse work for raw material picking.</span></span> <span data-ttu-id="4429e-256">Keräilytyö luodaan, kun tuotanto *PRD-002* vapautetaan.</span><span class="sxs-lookup"><span data-stu-id="4429e-256">The picking work is generated when production *PRD-002* is released.</span></span>

<span data-ttu-id="4429e-257">[![Varaston työkäytännöt](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="4429e-257">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span>

<span data-ttu-id="4429e-258">Kun suunnittelet tämän skenaarion mukaista varastotyön konfigurointia, ota huomioon seuraavat seikat:</span><span class="sxs-lookup"><span data-stu-id="4429e-258">When you're planning to configure a warehouse work policy for this scenario, you should consider the following points:</span></span>

- <span data-ttu-id="4429e-259">Valmiiden tuotteiden hyllytyksen varastotyötä ei tarvita, kun raportoit tuotteen *SC1* valmiiksi tuotantotilauksesta *PRD-001* sijainnissa *001*.</span><span class="sxs-lookup"><span data-stu-id="4429e-259">Warehouse work for putaway of finished goods isn't required when you report product *SC1* as finished from production order *PRD-001* to location *001*.</span></span> <span data-ttu-id="4429e-260">Tämä johtuu siitä, että *Maalaus*-työvaihe tuotantotilauksessa *PRD-002* käyttää *SC1*:n samassa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="4429e-260">The reason is that the *Painting* operation for production order *PRD-002* consumes product *SC1* at the same location.</span></span>
- <span data-ttu-id="4429e-261">Raaka-aineen keräilyn varastotyö vaaditaan, jotta raaka-aine *RM1* siirretään varastosijainnista *BULK-001* sijaintiin *001*.</span><span class="sxs-lookup"><span data-stu-id="4429e-261">Warehouse work for raw material picking is required to move raw material *RM1* from warehouse location *BULK-001* to location *001*.</span></span>

<span data-ttu-id="4429e-262">Seuraavassa on esimerkki työmenettelystä, jonka voit määrittää näiden havaintojen perusteella:</span><span class="sxs-lookup"><span data-stu-id="4429e-262">Here is an example of a work policy that you can set up, based on these considerations:</span></span>

- <span data-ttu-id="4429e-263">**Työkäytännön nimi:** *Ei hyllytystyötä*</span><span class="sxs-lookup"><span data-stu-id="4429e-263">**Work policy name:** *No putaway work*</span></span>
- <span data-ttu-id="4429e-264">**Työtilaustyypit:** *Valmiiden tuotteiden hyllytys* ja *Rinnakkais- ja sivutuotteen hyllytys*</span><span class="sxs-lookup"><span data-stu-id="4429e-264">**Work order types:** *Finished goods put away* and *Co-product and by-product put away*</span></span>
- <span data-ttu-id="4429e-265">**Varastosijainnit:** Varasto *51* ja sijainti *001*</span><span class="sxs-lookup"><span data-stu-id="4429e-265">**Inventory locations:** Warehouse *51* and location *001*</span></span>
- <span data-ttu-id="4429e-266">**Tuotteet:** *SC1*</span><span class="sxs-lookup"><span data-stu-id="4429e-266">**Products:** *SC1*</span></span>

<span data-ttu-id="4429e-267">Seuraavassa esimerkkiskenaariossa on vaiheittaiset ohjeet varastotyökäytännön määrittämiseksi tässä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="4429e-267">The following example scenario provides step-by-step instructions for setting up the warehouse work policy for this scenario.</span></span>

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="4429e-268">Esimerkkiskenaario: Raportoi valmistuneeksi sijaintiin, jossa ei ole varastorekisterinumero-ohjausta</span><span class="sxs-lookup"><span data-stu-id="4429e-268">Example scenario: Report as finished to a location that isn't license plate–controlled</span></span>

<span data-ttu-id="4429e-269">Tässä skenaariossa on esimerkki, jossa tuotantotilaus raportoidaan valmiiksi tiettyyn sijaintiin, jossa ei ole varastorekisterinumero-ohjausta.</span><span class="sxs-lookup"><span data-stu-id="4429e-269">This scenario shows an example where a production order is reported as finished to a location that isn't license plate–controlled.</span></span>

<span data-ttu-id="4429e-270">Tässä skenaariossa käytetään vakioesittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="4429e-270">This scenario uses the standard demo data.</span></span> <span data-ttu-id="4429e-271">Jos siis haluat käsitellä tätä skenaariota käyttämällä tässä annettuja arvoja, sinun on työskenneltävä järjestelmässä, johon on asennettu esittelytiedot.</span><span class="sxs-lookup"><span data-stu-id="4429e-271">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="4429e-272">Sinun on myös valittava **USMF**-yritys.</span><span class="sxs-lookup"><span data-stu-id="4429e-272">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="4429e-273">Määritä varaston työkäytäntö</span><span class="sxs-lookup"><span data-stu-id="4429e-273">Set up a warehouse work policy</span></span>

<span data-ttu-id="4429e-274">Varastointiprosessit eivät aina sisällä varastotyötä.</span><span class="sxs-lookup"><span data-stu-id="4429e-274">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="4429e-275">Voit määrittää työn käytännön, joka estää raaka-aineen keräilytyön ja valmiiden tuotteiden hyllytystöiden luonnin tietyille tuotejoukoille tietyissä sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="4429e-275">By defining a work policy, you can prevent the creation of work for raw material picking and putaway of finished goods for a set of products at specific locations.</span></span>

1. <span data-ttu-id="4429e-276">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työkäytännöt**.</span><span class="sxs-lookup"><span data-stu-id="4429e-276">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="4429e-277">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4429e-277">Select **New**.</span></span>
1. <span data-ttu-id="4429e-278">Anna **Työkäytännön nimi** -kenttään *Ei hyllytystyötä*.</span><span class="sxs-lookup"><span data-stu-id="4429e-278">In the **Work policy name** field, enter *No putaway work*.</span></span>
1. <span data-ttu-id="4429e-279">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4429e-279">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="4429e-280">Valitse **Työtilaustyypit**-pikavälilehdessä **Lisää**, jos haluat lisätä rivin ruudukkoon. Määritä sitten uuden rivin seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="4429e-280">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="4429e-281">**Työtilaustyyppi:** *Valmiiden tuotteiden hyllytys*</span><span class="sxs-lookup"><span data-stu-id="4429e-281">**Work order type:** *Finished goods put away*</span></span>
    - <span data-ttu-id="4429e-282">**Työprosessi:** *Kaikki liittyvät työprosessit*</span><span class="sxs-lookup"><span data-stu-id="4429e-282">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="4429e-283">**Työn luontimenetelmä:** *Ei koskaan*</span><span class="sxs-lookup"><span data-stu-id="4429e-283">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="4429e-284">**Cross-docking-käytännön nimi:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="4429e-284">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="4429e-285">Valitse **Lisää** uudelleen, jos haluat lisätä toisen rivin ruudukkoon. Määritä sitten uuden rivin seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="4429e-285">Select **Add** again to add a second row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="4429e-286">**Työtilauksen tyyppi:** *Rinnakkais- ja sivutuotteen hyllytys*</span><span class="sxs-lookup"><span data-stu-id="4429e-286">**Work order type:** *Co-product and by-product put away*</span></span>
    - <span data-ttu-id="4429e-287">**Työprosessi:** *Kaikki liittyvät työprosessit*</span><span class="sxs-lookup"><span data-stu-id="4429e-287">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="4429e-288">**Työn luontimenetelmä:** *Ei koskaan*</span><span class="sxs-lookup"><span data-stu-id="4429e-288">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="4429e-289">**Cross-docking-käytännön nimi:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="4429e-289">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="4429e-290">Valitse **Varastosijainnit**-pikavälilehdessä **Lisää**, jos haluat lisätä rivin ruudukkoon. Määritä sitten uuden rivin seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="4429e-290">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="4429e-291">**Varasto**: *51*</span><span class="sxs-lookup"><span data-stu-id="4429e-291">**Warehouse:** *51*</span></span>
    - <span data-ttu-id="4429e-292">**Sijainti:** *001*</span><span class="sxs-lookup"><span data-stu-id="4429e-292">**Location:** *001*</span></span>

1. <span data-ttu-id="4429e-293">Määritä **Tuotteet**-pikavälilehdessä **Tuotteen valinta** -kentän arvoksi *Valittu*.</span><span class="sxs-lookup"><span data-stu-id="4429e-293">On the **Products** FastTab, set the **Product selection** field to *Selected*.</span></span>
1. <span data-ttu-id="4429e-294">Valitse **Tuotteet**-pikavälilehdessä **Lisää**, jos haluat lisätä uuden rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="4429e-294">On the **Products** FastTab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="4429e-295">Määritä uuden rivin **Nimiketunnus**-kentän arvoksi *L0101*.</span><span class="sxs-lookup"><span data-stu-id="4429e-295">In the new row, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="4429e-296">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4429e-296">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-an-output-location"></a><span data-ttu-id="4429e-297">Määritä tulostussijainti</span><span class="sxs-lookup"><span data-stu-id="4429e-297">Set up an output location</span></span>

1. <span data-ttu-id="4429e-298">Siirry kohtaan **Organisaation hallinto \> Resurssit \> Resurssiryhmät**.</span><span class="sxs-lookup"><span data-stu-id="4429e-298">Go to **Organization administration \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="4429e-299">Valitse vasemmasta ruudusta resurssiryhmä **5102**.</span><span class="sxs-lookup"><span data-stu-id="4429e-299">In the left pane, select resource group **5102**.</span></span>
1. <span data-ttu-id="4429e-300">Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="4429e-300">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="4429e-301">**Tulostusvarasto:** *51*</span><span class="sxs-lookup"><span data-stu-id="4429e-301">**Output warehouse:** *51*</span></span>
    - <span data-ttu-id="4429e-302">**Tulostussijainti:** *001*</span><span class="sxs-lookup"><span data-stu-id="4429e-302">**Output location:** *001*</span></span>

1. <span data-ttu-id="4429e-303">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4429e-303">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="4429e-304">Sijainti *001* ei ole rekisterikilven mukaan ohjattu sijainti.</span><span class="sxs-lookup"><span data-stu-id="4429e-304">Location *001* isn't a license plate–controlled location.</span></span> <span data-ttu-id="4429e-305">Voit määrittää rekisterikilven mukaan ohjaamattoman tulostussijainnin ainoastaan, jos sijainnille on olemassa soveltuva työkäytäntö.</span><span class="sxs-lookup"><span data-stu-id="4429e-305">You can set up an output location that isn't license plate–controlled only if an applicable work policy exists for the location.</span></span>

### <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="4429e-306">Luo tuotantotilaus ja ilmoita se valmiiksi</span><span class="sxs-lookup"><span data-stu-id="4429e-306">Create a production order and report it as finished</span></span>

1. <span data-ttu-id="4429e-307">Siirry kohtaan **Tuotannonhallinta \> Tuotantotilaukset \> Kaikki tuotantotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="4429e-307">Go to **Production control \> Production orders \> All production orders**.</span></span>
1. <span data-ttu-id="4429e-308">Valitse toimintoruudussa **Uusi tuotantotilaus**.</span><span class="sxs-lookup"><span data-stu-id="4429e-308">On the Action Pane, select **New production order**.</span></span>
1. <span data-ttu-id="4429e-309">Määritä **Luo tuotantotilaus** -valintaikkunassa **Nimiketunnus**-kentän arvoksi *L0101*.</span><span class="sxs-lookup"><span data-stu-id="4429e-309">In the **Create production order** dialog box, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="4429e-310">Valitse **Luo** luodaksesi tilauksen. Sulje sitten valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="4429e-310">Select **Create** to create the order and close the dialog box.</span></span>

    <span data-ttu-id="4429e-311">Uusi tuotantotilaus lisätään ruudukkoon **Kaikki tuotantotilaukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4429e-311">A new production order is added to the grid on the **All production orders** page.</span></span>

    <span data-ttu-id="4429e-312">Pidä uusi tuotantotilaus valittuna.</span><span class="sxs-lookup"><span data-stu-id="4429e-312">Keep the new production order selected.</span></span>

1. <span data-ttu-id="4429e-313">Valitse toimintoruudun **Tuotantotilaus**-välilehden **Käsittely**-ryhmässä **Arvio**.</span><span class="sxs-lookup"><span data-stu-id="4429e-313">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Estimate**.</span></span>
1. <span data-ttu-id="4429e-314">Katso arvio **Arvio**-valintaikkunasta ja sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="4429e-314">In the **Estimate** dialog box, read the estimate, and then select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="4429e-315">Valitse toimintoruudun **Tuotantotilaus**-välilehden **Käsittely**-ryhmässä **Käynnistä**.</span><span class="sxs-lookup"><span data-stu-id="4429e-315">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Start**.</span></span>
1. <span data-ttu-id="4429e-316">Määritä **Käynnistä**-valintaikkunan **Yleistä**-välilehdessä **Automaattinen tuoterakennekulutus** -kentän arvoksi *Ei koskaan*.</span><span class="sxs-lookup"><span data-stu-id="4429e-316">In the **Start** dialog box, on the **General** tab, set the **Automatic BOM consumption** field to *Never*.</span></span>
1. <span data-ttu-id="4429e-317">Valitse **OK** tallentaaksesi asetuksen. Sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="4429e-317">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="4429e-318">Valitse toimintoruudun **Tuotantotilaus**-välilehden **Käsittely**-ryhmässä **Ilmoita valmistuneeksi**.</span><span class="sxs-lookup"><span data-stu-id="4429e-318">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Report as finished**.</span></span>
1. <span data-ttu-id="4429e-319">Määritä **Ilmoita valmistuneeksi** -valintaikkunan **Yleistä**-välilehdessä **Hyväksy virhe** -valinnan arvoksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="4429e-319">In the **Report as finished** dialog box, on the **General** tab, set the **Accept error** option to *Yes*.</span></span>
1. <span data-ttu-id="4429e-320">Valitse **OK** tallentaaksesi asetuksen. Sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="4429e-320">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="4429e-321">Valitse toimintoruudun **Varasto**-välilehden **Yleinen**-ryhmässä **Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="4429e-321">On the Action Pane, on the **Warehouse** tab, in the **General** group, select **Work details**.</span></span>

<span data-ttu-id="4429e-322">Kun tuotantotilaus on ilmoitettu valmistuneeksi, hyllytystyötä ei luoda.</span><span class="sxs-lookup"><span data-stu-id="4429e-322">When the production order is reported as finished, no work is generated for putaway.</span></span> <span data-ttu-id="4429e-323">Tämä toiminta johtuu siitä, että määritettynä on työkäytäntö, joka estää töiden luonnin, kun tuote *L0101* ilmoitetaan valmiiksi sijainnissa *001*.</span><span class="sxs-lookup"><span data-stu-id="4429e-323">This behavior occurs because a work policy is defined that prevents work from being generated when product *L0101* is reported as finished to location *001*.</span></span>

## <a name="more-information"></a><span data-ttu-id="4429e-324">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="4429e-324">More information</span></span>

<span data-ttu-id="4429e-325">Lisätietoja mobiililaitteiden valikkokohteista on kohdassa [Mobiililaitteiden määrittäminen varastotyötä varten](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="4429e-325">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

<span data-ttu-id="4429e-326">Lisätietoja rekisterikilven vastaanotosta ja työkäytännöistä on kohdassa [Rekisterikilven vastaanotto varastosovelluksen kautta](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="4429e-326">For more information about license plate receiving and work policies, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="4429e-327">Lisätietoja saapuvien kuormien hallinnasta on kohdassa [Ostotilausten saapuvien kuormien varastokäsittely](inbound-load-handling.md).</span><span class="sxs-lookup"><span data-stu-id="4429e-327">For more information about inbound load management, see [Warehouse handling of inbound loads for purchase orders](inbound-load-handling.md).</span></span>
