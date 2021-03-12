---
title: Varastohaku myyntipisteessä (POS)
description: Tässä ohjeaiheessa käsitellään asetuksia, joilla voi tarkastella varastotietoja myyntipisteessä.
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: f08906c14f80b07368d88d820acae83cf1157e6c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969948"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a><span data-ttu-id="28e59-103">Varastohaku myyntipisteessä (POS)</span><span class="sxs-lookup"><span data-stu-id="28e59-103">Inventory lookup in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="28e59-104">Myyntipisteen varastohaku auttaa jälleenmyyjiä tehostamaan toimintaa reaaliaikaisesti. Samalla myymälöiden, myyntipisteen ja taustatoimintojen yhdistäminen antaa analyysitietoja.</span><span class="sxs-lookup"><span data-stu-id="28e59-104">Inventory lookup in the point of sale (POS) helps retailers achieve real-time operational excellence and gain insights by connecting stores, the POS, and the back office.</span></span> <span data-ttu-id="28e59-105">Tällä toiminnolla saa tarkan reaaliaikaisen näkymän eri myymälöiden ja jakelukeskusten tuotevarastoon.</span><span class="sxs-lookup"><span data-stu-id="28e59-105">This functionality provides an accurate real-time view of product inventory across stores and distribution centers.</span></span> <span data-ttu-id="28e59-106">Sen avulla jälleenmyyjät voivat myös tehostaa toimintaa ja kustannussäästöjä, sillä reaaliaikainen varastosuunnittelu paranee.</span><span class="sxs-lookup"><span data-stu-id="28e59-106">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="28e59-107">Tarkka reaaliaikainen koko organisaation kattava varastonäkymä auttaa myyntiedustajia tarjoamaan nopeaa ja erinomaista asiakaspalvelua.</span><span class="sxs-lookup"><span data-stu-id="28e59-107">An accurate real-time view of inventory across an organization helps store associates provide timely, superior customer service.</span></span> <span data-ttu-id="28e59-108">Tärkein hetki on se hetki, jolloin asiakas on valmis tekemään ostopäätöksen.</span><span class="sxs-lookup"><span data-stu-id="28e59-108">The moment that matters most is the moment when the customer is ready to make a purchase decision.</span></span> <span data-ttu-id="28e59-109">On tärkeää, että myymälän kassojen käytettävissä on reaaliaikaiset varastotiedot, jotta he voivat luvata tuotteen toimituksen ja noudon tarkasti.</span><span class="sxs-lookup"><span data-stu-id="28e59-109">It's important that cashiers in the store have real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="28e59-110">Voit avata **Varastohaku**-sivun **Retail Modern POS**- tai **Retail Cloud POS** -työtilasta.</span><span class="sxs-lookup"><span data-stu-id="28e59-110">You can open the **Inventory lookup** page from the **Retail Modern POS** workspace or the **Retail Cloud POS** workspace.</span></span>

![Myyntipisteen aloitussivun varastohakuruutu](media/POSHomepage.png)

<span data-ttu-id="28e59-112">Voit antaa tuotteen numeron **Varastohaku**-sivulla numeronäppäimistöllä.</span><span class="sxs-lookup"><span data-stu-id="28e59-112">On the **Inventory lookup** page, you can use the numeric keyboard to enter a product number.</span></span> <span data-ttu-id="28e59-113">Voit sitten tarkastella useiden myymälöiden ja varastojen käytettävissä olevaa määrää.</span><span class="sxs-lookup"><span data-stu-id="28e59-113">You can then view the on-hand quantity for multiple stores and warehouses.</span></span>

![Vakiovarastohaku-sivu](media/InventoryLookUp.png)

<span data-ttu-id="28e59-115">Kullekin sijainnille näytetään myös **Varattu**- ja **Tilattu**-määrät.</span><span class="sxs-lookup"><span data-stu-id="28e59-115">**Reserved** and **Ordered** quantities are also shown for each location.</span></span>

- <span data-ttu-id="28e59-116">**Varattu** – tämä määrä viittaa sijainnissa tietyn tuotenumeron taustatoimintojen **Fyysiset varatut** -arvoon.</span><span class="sxs-lookup"><span data-stu-id="28e59-116">**Reserved** – This quantity refers to the **Physical reserved** value from the back office for the specified product number at the location.</span></span>
- <span data-ttu-id="28e59-117">**Tilattu** – tämä määrä viittaa sijainnissa tietyn tuotenumeron taustatoimintojen **Tilattu yhteensä** -arvoon.</span><span class="sxs-lookup"><span data-stu-id="28e59-117">**Ordered** – This quantity refers to the **Ordered in total** value from the back office for the specified product number at the location.</span></span>

## <a name="locations-that-inventory-availability-information-is-shown-for"></a><span data-ttu-id="28e59-118">Sijainnit, joiden varastosaatavuustiedot näytetään</span><span class="sxs-lookup"><span data-stu-id="28e59-118">Locations that inventory availability information is shown for</span></span>

<span data-ttu-id="28e59-119">Sijaintiluettelossa on kahden tyyppisiä yksiköitä:</span><span class="sxs-lookup"><span data-stu-id="28e59-119">The list of locations includes two types of entities:</span></span>

- <span data-ttu-id="28e59-120">**Myymälät** – luettelo sisältää myymälät, jotka on määritetty käyttämällä nykyisen myymälän myymälän paikanninryhmää Headquartersissa.</span><span class="sxs-lookup"><span data-stu-id="28e59-120">**Stores** – The list shows stores that are configured by using the store locator group for the current store in the Headquarters.</span></span>
- <span data-ttu-id="28e59-121">**Jakelukeskukset** – Commercessa voidaan määrittää useita erilaisia jakelukeskuksia (kuten varastoja).</span><span class="sxs-lookup"><span data-stu-id="28e59-121">**Distribution centers** – Various types of distribution centers (such as warehouses) can be configured in Commerce.</span></span> <span data-ttu-id="28e59-122">Luettelossa näkyy kuitenkin vain **Vakio**-oletustyyppisten jakelukeskusten varaston saatavuustiedot.</span><span class="sxs-lookup"><span data-stu-id="28e59-122">However, the list shows inventory availability information only for distribution centers of the **Standard** default type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="28e59-123">Varaston saatavuustietoja ei näytetä myyntipisteellä seuraaville varastotyypeille: **Kuljetus**, **Karanteeni** ja **Tavarat matkalla**.</span><span class="sxs-lookup"><span data-stu-id="28e59-123">Inventory availability information isn't shown for warehouses of the **Transit**, **Quarantine**, and **Goods in Route** types for the POS.</span></span>

<span data-ttu-id="28e59-124">Voit tarkastella **Varastohaku**-sivulla kunkin myymälän luvattavissa olevaa määrää (ATP) nykyisten käytettävissä olevan määrän, varattujen määrien ja tilattujen määrien lisäksi.</span><span class="sxs-lookup"><span data-stu-id="28e59-124">On the **Inventory lookup** page, you can view available to promise (ATP) quantities for each store, in addition to the current on-hand quantities, reserved quantities, and ordered quantities.</span></span> <span data-ttu-id="28e59-125">Valitse myymälä, jonka ATP-tietoja haluat tarkastella, ja valitse sitten myymälä **Näytä myymälän käytettävyys**.</span><span class="sxs-lookup"><span data-stu-id="28e59-125">Select the store to view the ATP information for, and then select **Show store availability**.</span></span>

![ATP-määrät](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a><span data-ttu-id="28e59-127">Kaikkien varianttien näyttäminen avaamalla dimensioon perustuva matriisi</span><span class="sxs-lookup"><span data-stu-id="28e59-127">Opening the Dimension based matrix view to show all variants</span></span>

<span data-ttu-id="28e59-128">Valitse päätuotteen **Tuotteen tiedot** -sivulla tai **Varastohaku**-sivulla **Näytä kaikki variantit** sivun alaosassa olevasta sovelluspalkista.</span><span class="sxs-lookup"><span data-stu-id="28e59-128">On the **Product details** page of a product master, or on the **Inventory lookup** page, select **View all variants** from the app-bar at bottom of the page.</span></span> <span data-ttu-id="28e59-129">Näillä sivulla aluksi avautuva **Dimensioon perustuva matriisi** -näkymä näyttää nykyisen myymälän kaikkien tuotevarianttien varaston saatavuustiedot.</span><span class="sxs-lookup"><span data-stu-id="28e59-129">The **Dimension based matrix** view for the initial launch from these pages shows the inventory availability information for all variants of a product for the current store.</span></span>

> [!NOTE]
> <span data-ttu-id="28e59-130">**Näytä kaikki variantit** -painike on käytettävissä niillä nimikkeen päätuotteilla, joilla on tuotevariantteja.</span><span class="sxs-lookup"><span data-stu-id="28e59-130">The **View all variants** button is available only for item product masters that have product variants.</span></span> <span data-ttu-id="28e59-131">Se ei ole käytettävissä erillisissä tuotteissa tai myyntirakenteissa.</span><span class="sxs-lookup"><span data-stu-id="28e59-131">It isn't available for standalone products or kits.</span></span>

![Näytä kaikki variantit -painike Varastohaku-sivulla](media/StandardToMatrix.png)

<span data-ttu-id="28e59-133">Valitse **Näytä kaikki variantit** päätuotteen **Tuotteen tiedot** -sivulla tai **Varastohaku**-sivulla sijaintia valitsematta. Siirry sitten **Dimensioon perustuva matriisi** -näkymään, jossa voit tarkastella nykyisen myymälän kaikkien tuotevarianttien varaston saatavuustietoja.</span><span class="sxs-lookup"><span data-stu-id="28e59-133">Select **View all variants** on the **Product details** page of a product master, or on the **Inventory lookup** page, without selecting a location, to go to the **Dimension based matrix** view to view the inventory availability information for all variants of a product for the current store.</span></span>

![Varastohaku-sivun Dimensioon perustuva matriisi -näkymä](media/Matrix.png)

> [!NOTE]
> <span data-ttu-id="28e59-135">Edellisessä kuvassa dimensioiden näytetään aakkosjärjestyksessä, koska valitun tuotteen dimensioiden näyttöjärjestystä ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="28e59-135">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="28e59-136">**Dimensioon perustuva matriisi** -näkymässä tuotevarianttien solujen oikeassa alakulmassa on käytettävissä oleva arvo.</span><span class="sxs-lookup"><span data-stu-id="28e59-136">In the **Dimension based matrix** view, the cells for the product variants include an on-hand value in the lower-right corner.</span></span> <span data-ttu-id="28e59-137">Seuraavassa taulukossa selitetään eri arvojen merkitykset.</span><span class="sxs-lookup"><span data-stu-id="28e59-137">The following table explains the meaning of the various values.</span></span>

| <span data-ttu-id="28e59-138">Käytettävissä olevan varaston arvo</span><span class="sxs-lookup"><span data-stu-id="28e59-138">On-hand value</span></span>                            | <span data-ttu-id="28e59-139">kuvaus</span><span class="sxs-lookup"><span data-stu-id="28e59-139">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="28e59-140">Numeerinen arvo, joka on suurempi kuin 0 (nolla)</span><span class="sxs-lookup"><span data-stu-id="28e59-140">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="28e59-141">Variantti on vapautettu valittuun sijaintiin, ja voit tehdä solussa lisätoimintoja.</span><span class="sxs-lookup"><span data-stu-id="28e59-141">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> <span data-ttu-id="28e59-142">(Näitä toimintoja käsitellään tarkemmin jäljempänä tässä ohjeaiheessa.)</span><span class="sxs-lookup"><span data-stu-id="28e59-142">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="28e59-143">**0** (nolla)</span><span class="sxs-lookup"><span data-stu-id="28e59-143">**0** (zero)</span></span>                             | <span data-ttu-id="28e59-144">Variantti on vapautettu valittuun sijaintiin mutta nimike ei käytettävissä valitussa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="28e59-144">A variant has been released to the selected location, but the item isn't available in selected location.</span></span> <span data-ttu-id="28e59-145">Voit kuitenkin tehdä solussa muita toimia.</span><span class="sxs-lookup"><span data-stu-id="28e59-145">However, you can perform additional actions in the cell.</span></span> <span data-ttu-id="28e59-146">(Näitä toimintoja käsitellään tarkemmin jäljempänä tässä ohjeaiheessa.)</span><span class="sxs-lookup"><span data-stu-id="28e59-146">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="28e59-147">**–** tai passiivinen solu</span><span class="sxs-lookup"><span data-stu-id="28e59-147">**n/a** or an inactive cell</span></span>              | <span data-ttu-id="28e59-148">Varianttia ei ole vapautettu valittuun sijaintiin etkä voi tehdä solussa lisätoimintoja.</span><span class="sxs-lookup"><span data-stu-id="28e59-148">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="28e59-149">Voit myös muuttaa pivot-dimensiota valitsemalla uuden käytettävän dimension.</span><span class="sxs-lookup"><span data-stu-id="28e59-149">You can also change the pivot for dimensions by selecting the new dimension to use.</span></span>

![Pivot-dimension muuttaminen](media/ChangePivot.png)

![Pivot-dimensio muutettu](media/PivotChanged.png)

> [!NOTE]
> <span data-ttu-id="28e59-152">Edellisissä kuvissa valitun tuotteen dimensioiden näyttöjärjestys on mukautettu (ei aakkosellinen).</span><span class="sxs-lookup"><span data-stu-id="28e59-152">In the preceding illustrations, the display order of the dimensions for the selected product is custom (non-alphabetic).</span></span> <span data-ttu-id="28e59-153">Se perustuu taustatoiminnossa määritettyyn dimension näyttöjärjestykseen.</span><span class="sxs-lookup"><span data-stu-id="28e59-153">It's based on the dimension display order that is set in the back office.</span></span>

<span data-ttu-id="28e59-154">**Dimensioon perustuva matriisi** -näkymässä voidaan suorittaa myös muita toimintoja, jotka tehostavat myymälän myyjien tuottavuutta.</span><span class="sxs-lookup"><span data-stu-id="28e59-154">Additionally, in the **Dimension based matrix** view, more actions can be performed to help boost a store associate's productivity.</span></span> <span data-ttu-id="28e59-155">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="28e59-155">Here are some examples:</span></span>

- <span data-ttu-id="28e59-156">Muuttamalla myymälän sijaintia voit hakea kaikkien tuotevarianttien varastosaatavuuden muissa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="28e59-156">Change the store location to look up the inventory availability of all product variants at other locations.</span></span> <span data-ttu-id="28e59-157">Näitä sijainteja ovat muut myymälän paikannin ryhmät myymälät ja **Vakio**-oletustyypin jakelukeskukset.</span><span class="sxs-lookup"><span data-stu-id="28e59-157">These locations include other stores in the store locator group and distribution centers of the **Standard** default type.</span></span>
- <span data-ttu-id="28e59-158">Myy yksittäinen tuotevariantti asiakkaalle käyttämällä itsepalvelutukkua, noutoa myymälästä tai lähetystä osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="28e59-158">Sell an individual product variant to a customer by using cash and carry, in-store pickup, or shipment to an address.</span></span>
- <span data-ttu-id="28e59-159">Anna asiakkaalle yksittäisen tuotevariantin ATP-tiedot tietyssä sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="28e59-159">Provide the customer with ATP information for an individual product variant at a specific location.</span></span>

![Varianttiruutujen muut toiminnot](media/VariantActions.png)

> [!NOTE]
> <span data-ttu-id="28e59-161">Edellisessä kuvassa dimensioiden näytetään aakkosjärjestyksessä, koska valitun tuotteen dimensioiden näyttöjärjestystä ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="28e59-161">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="28e59-162">Seuraavassa taulukossa on lisätietoja käytettävissä olevista toiminnoista.</span><span class="sxs-lookup"><span data-stu-id="28e59-162">The following table provides more information about the additional actions that are available.</span></span>

| <span data-ttu-id="28e59-163">Toimenpide</span><span class="sxs-lookup"><span data-stu-id="28e59-163">Action</span></span>               | <span data-ttu-id="28e59-164">kuvaus</span><span class="sxs-lookup"><span data-stu-id="28e59-164">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="28e59-165">Myy nyt</span><span class="sxs-lookup"><span data-stu-id="28e59-165">Sell now</span></span>             | <span data-ttu-id="28e59-166">Lisää tapahtumaan valittu nimikevariantti ja ohjaa käyttäjä tapahtumanäyttöön.</span><span class="sxs-lookup"><span data-stu-id="28e59-166">Add the selected item variant to the transaction, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="28e59-167">(Tämä toiminto ei ole käytettävissä, kun valittu sijainti on jakelukeskus.)</span><span class="sxs-lookup"><span data-stu-id="28e59-167">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="28e59-168">Nouto myymälästä</span><span class="sxs-lookup"><span data-stu-id="28e59-168">Pick up in store</span></span>     | <span data-ttu-id="28e59-169">Luo tuotevariantille asiakastilaus, joka noudetaan valitusta sijainnista, ja ohjaa käyttäjä tapahtumanäyttöön.</span><span class="sxs-lookup"><span data-stu-id="28e59-169">Create a customer order for the product variant that will be picked up from the selected location, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="28e59-170">(Tämä toiminto ei ole käytettävissä, kun valittu sijainti on jakelukeskus.)</span><span class="sxs-lookup"><span data-stu-id="28e59-170">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="28e59-171">Lähetä tuote</span><span class="sxs-lookup"><span data-stu-id="28e59-171">Ship product</span></span>         | <span data-ttu-id="28e59-172">Luo tuotevariantille asiakastilaus, joka lähetetään valitusta sijainnista, ja ohjaa käyttäjä tapahtumanäyttöön.</span><span class="sxs-lookup"><span data-stu-id="28e59-172">Create a customer order for the product variant that will be shipped from the selected location, and redirect the user to the transaction screen.</span></span> |
| <span data-ttu-id="28e59-173">Käytettävyys</span><span class="sxs-lookup"><span data-stu-id="28e59-173">Availability</span></span>         | <span data-ttu-id="28e59-174">Näytä valitun sijainnin valitun varianttiyhdistelmän ATP-tiedot.</span><span class="sxs-lookup"><span data-stu-id="28e59-174">Show the ATP information for the selected variant combination for the selected location.</span></span> |
| <span data-ttu-id="28e59-175">Näytä kaikki sijainnit</span><span class="sxs-lookup"><span data-stu-id="28e59-175">Show all locations</span></span>   | <span data-ttu-id="28e59-176">Vaihda varastohaun vakionäkymään ja korosta nimikevariantiin varaston saatavuustiedot kaikissa myymälän paikanninryhmän myymälöissä sekä **vakio- tai oletustyypin** jakelukeskuksissa.</span><span class="sxs-lookup"><span data-stu-id="28e59-176">Switch to the standard inventory lookup view, and highlight inventory availability information for the item variant across all stores in the store locator group, and also in distribution centers of the **Standard/Default** type.</span></span> |
| <span data-ttu-id="28e59-177">Näytä tuotteen tiedot</span><span class="sxs-lookup"><span data-stu-id="28e59-177">View product details</span></span> | <span data-ttu-id="28e59-178">Ohjaa käyttäjä liitetyn päätuotteen **Tuotteen tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="28e59-178">Redirect the user to the **Product details** page of the associated product master.</span></span> |
