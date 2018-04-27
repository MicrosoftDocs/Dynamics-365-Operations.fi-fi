---
title: "Varaston työkäytännöt"
description: "Varaston työkäytännöt määrittävät, onko varastotyö luotu varastoprosessia varten valmistuksessa työtilaustyypin, varaston sijainnin ja tuotteen perusteella."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c2d72509b0dc4d0cea5b4f2478ae7f8fc163e78c
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="warehouse-work-policies"></a><span data-ttu-id="64e6d-103">Varaston työkäytännöt</span><span class="sxs-lookup"><span data-stu-id="64e6d-103">Warehouse work policies</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="64e6d-104">Varaston työkäytännöt Microsoft Dynamics 365 for Finance and Operationsissa määrittävät, onko varastotyö luotu valmistuksen varastoprosessia varten työtilaustyypin, varaston sijainnin ja tuotteen perusteella.</span><span class="sxs-lookup"><span data-stu-id="64e6d-104">Warehouse work policies in Microsoft Dynamics 365 for Finance and Operations control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="64e6d-105">Tämä työkäytäntö määrittää, onko varastotyö luotu varastoprosessia varten valmistuksessa.</span><span class="sxs-lookup"><span data-stu-id="64e6d-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="64e6d-106">Voit määrittää työkäytännön käyttämällä yhdistelmää **työtilaustyypit**, **varastosijainti** ja **tuote**.</span><span class="sxs-lookup"><span data-stu-id="64e6d-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="64e6d-107">Esimerkiksi tuote L0101 ilmoitetaan valmiiksi tuotossijaintiin 001.</span><span class="sxs-lookup"><span data-stu-id="64e6d-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="64e6d-108">Valmis tuote käytetään myöhemmin toisessa tuotantotilauksessa tuotossijainnissa 001.</span><span class="sxs-lookup"><span data-stu-id="64e6d-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="64e6d-109">Tässä tapauksessa voit määrittää työkäytännön, joka estää luomasta työtä, jossa käytetään valmiita sivuun siirrettyjä tuotteita, kun raportoit tuotteen L0101 valmiiksi tuotossijaintiin 001.</span><span class="sxs-lookup"><span data-stu-id="64e6d-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="64e6d-110">Työkäytäntö on yksittäinen yksikkö, jota voidaan kuvata seuraavien tietojen avulla:</span><span class="sxs-lookup"><span data-stu-id="64e6d-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="64e6d-111">**Työkäytännön nimi**(työkäytännön yksilöivä tunnus)</span><span class="sxs-lookup"><span data-stu-id="64e6d-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="64e6d-112">**Työtilaustyypit** ja **Työn luontimenetelmä**</span><span class="sxs-lookup"><span data-stu-id="64e6d-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="64e6d-113">**Varastosijainnit**</span><span class="sxs-lookup"><span data-stu-id="64e6d-113">**Inventory locations**</span></span>
-   <span data-ttu-id="64e6d-114">**Tuotteet**</span><span class="sxs-lookup"><span data-stu-id="64e6d-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="64e6d-115">Työtilaustyypit</span><span class="sxs-lookup"><span data-stu-id="64e6d-115">Work order types</span></span>
<span data-ttu-id="64e6d-116">Voit valita seuraavista työtilaustyypeistä:</span><span class="sxs-lookup"><span data-stu-id="64e6d-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="64e6d-117">Valmiiden tuotteiden poispano</span><span class="sxs-lookup"><span data-stu-id="64e6d-117">Finished goods put away</span></span>
-   <span data-ttu-id="64e6d-118">Rinnakkaistuotteen ja sivutuotteen poispano</span><span class="sxs-lookup"><span data-stu-id="64e6d-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="64e6d-119">Raaka-aineiden keräily</span><span class="sxs-lookup"><span data-stu-id="64e6d-119">Raw material picking</span></span>

<span data-ttu-id="64e6d-120">**Työn luontimenetelmä** -kentän arvo on **Ei koskaan**.</span><span class="sxs-lookup"><span data-stu-id="64e6d-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="64e6d-121">Tämä arvo ilmaisee, että työkäytäntö estää työn varastotyön luomisen valitulle työtilaustyypille.</span><span class="sxs-lookup"><span data-stu-id="64e6d-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="64e6d-122">Varastosijainnit</span><span class="sxs-lookup"><span data-stu-id="64e6d-122">Inventory locations</span></span>
<span data-ttu-id="64e6d-123">Voit valita sijainnin, johon työkäytäntö sopii.</span><span class="sxs-lookup"><span data-stu-id="64e6d-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="64e6d-124">Jos sijaintia ei ole liitetty työkäytäntöön, työkäytäntö ei koske mitään prosessia.</span><span class="sxs-lookup"><span data-stu-id="64e6d-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="64e6d-125">**Sijainnit**-sivulla voidaan valita tai peruuttaa työkäytännön valinta määrätyssä sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="64e6d-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="64e6d-126">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="64e6d-126">Products</span></span>
<span data-ttu-id="64e6d-127">Voit valita tuotteen, johon työkäytäntö sopii.</span><span class="sxs-lookup"><span data-stu-id="64e6d-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="64e6d-128">Voi soveltaa työkäytäntöä joko kaikkiin tai valittuihin tuotteisiin.</span><span class="sxs-lookup"><span data-stu-id="64e6d-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="64e6d-129">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="64e6d-129">Example</span></span>
<span data-ttu-id="64e6d-130">Seuraavassa esimerkissä on kaksi tuotantotilausta RD-001 ja PRD-00*2*.</span><span class="sxs-lookup"><span data-stu-id="64e6d-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="64e6d-131">Tuotantotilaus PRD-001 sisältää **Kokoonpano**-työvaiheen, jolla tuote SC1 raportoidaan valmiiksi sijainnissa O1.</span><span class="sxs-lookup"><span data-stu-id="64e6d-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="64e6d-132">Tuotantotilaus PRD-002 sisältää **maalaus**-työvaiheen ja käyttää tuotetta SC1 sijainnista O1.</span><span class="sxs-lookup"><span data-stu-id="64e6d-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="64e6d-133">Tuotantotilaus PRD-002 käyttää myös raaka-ainetta RM1 sijainnissa O1.</span><span class="sxs-lookup"><span data-stu-id="64e6d-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="64e6d-134">RM1 varastoidaan varastosijaintiin BULK-001, josta raaka-ainekeräilyn varastotyö kerää sen sijaintiin O1.</span><span class="sxs-lookup"><span data-stu-id="64e6d-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="64e6d-135">Keräilytyö luodaan, kun tuotanto PRD 002 vapautetaan.</span><span class="sxs-lookup"><span data-stu-id="64e6d-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="64e6d-136">[![Varaston työkäytännöt](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="64e6d-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="64e6d-137">Kun suunnittelet tämän skenaarion mukaista varastotyön konfigurointia, ota huomioon seuraava:</span><span class="sxs-lookup"><span data-stu-id="64e6d-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="64e6d-138">Valmiiden tuotteiden poispanon varastotyötä ei tarvita, kun raportoit tuotteen SC1 valmiiksi tuotantotilauksesta PRD 001 sijainnissa O1.</span><span class="sxs-lookup"><span data-stu-id="64e6d-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="64e6d-139">Tämä johtuu siitä, että **Maalaus**-työvaihe tuotantotilauksessa PRD-002 käyttää SC1:n samassa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="64e6d-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="64e6d-140">Raaka-aineen keräilyn varastotyö vaaditaan, jotta raaka-aine RM1 siirretään varastosijainnista BULK-001 sijaintiin O1.</span><span class="sxs-lookup"><span data-stu-id="64e6d-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="64e6d-141">Seuraavassa on esimerkki työmenettelystä jonka voit määrittää näiden havaintojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="64e6d-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="64e6d-142"><strong>Työkäytännön nimi</strong></span><span class="sxs-lookup"><span data-stu-id="64e6d-142"><strong>Work policy name</strong></span></span><br> | <span data-ttu-id="64e6d-143"><strong>Työtilaustyypit</strong></span><span class="sxs-lookup"><span data-stu-id="64e6d-143"><strong>Work order types</strong></span></span><br> |
|         <span data-ttu-id="64e6d-144">Ei pantu pois 01     \`</span><span class="sxs-lookup"><span data-stu-id="64e6d-144">No put away 01     \`</span></span>          |     <span data-ttu-id="64e6d-145">- Valmiiden tuotteiden poispano</span><span class="sxs-lookup"><span data-stu-id="64e6d-145">- Finished good put away</span></span><br>      |
|                                       |    <span data-ttu-id="64e6d-146"><strong>Sijaintipaikat</strong></span><span class="sxs-lookup"><span data-stu-id="64e6d-146"><strong>Locations</strong></span></span><br>     |
|                                       |                 <span data-ttu-id="64e6d-147">- O1</span><span class="sxs-lookup"><span data-stu-id="64e6d-147">- O1</span></span>                  |
|                                       |    <span data-ttu-id="64e6d-148"><strong>Tuotteet</strong></span><span class="sxs-lookup"><span data-stu-id="64e6d-148"><strong>Products</strong></span></span> <br>     |
|                                       |                 <span data-ttu-id="64e6d-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="64e6d-149">- SC1</span></span>                 |

<span data-ttu-id="64e6d-150">Seuraavissa menettelyissä saadaan vaiheittaiset ohjeet varastotyökäytännön määrittämiseksi tässä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="64e6d-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="64e6d-151">Esimerkkiasetuksissa kuvataan myös, miten tuotantotilaus raportoidaan valmiiksi tiettyyn sijaintiin, jossa ei ole varastorekisterinumero-ohjausta.</span><span class="sxs-lookup"><span data-stu-id="64e6d-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="64e6d-152">Määritä varaston työkäytäntö</span><span class="sxs-lookup"><span data-stu-id="64e6d-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="64e6d-153">Varastointiprosessit eivät aina sisällä varastotyötä.</span><span class="sxs-lookup"><span data-stu-id="64e6d-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="64e6d-154">Voit määrittää työn käytännön, joka estää raaka-aineen keräilytyön ja valmiiden tuotteiden poispanotöiden luonnin tietyille tuotejoukoille tietyissä sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="64e6d-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="64e6d-155">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="64e6d-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="64e6d-156">STEPS (21)</span><span class="sxs-lookup"><span data-stu-id="64e6d-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="64e6d-157">1.</span><span class="sxs-lookup"><span data-stu-id="64e6d-157">1.</span></span>  | <span data-ttu-id="64e6d-158">Valitse Varastonhallinta &gt; Asetukset &gt; Työ &gt; Työkäytännöt.</span><span class="sxs-lookup"><span data-stu-id="64e6d-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="64e6d-159">2.</span><span class="sxs-lookup"><span data-stu-id="64e6d-159">2.</span></span>  | <span data-ttu-id="64e6d-160">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="64e6d-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="64e6d-161">3.</span><span class="sxs-lookup"><span data-stu-id="64e6d-161">3.</span></span>  | <span data-ttu-id="64e6d-162">Kirjoita Työkäytännön nimi -kenttään Ei poispanotyötä.</span><span class="sxs-lookup"><span data-stu-id="64e6d-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="64e6d-163">4.</span><span class="sxs-lookup"><span data-stu-id="64e6d-163">4.</span></span>  | <span data-ttu-id="64e6d-164">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="64e6d-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="64e6d-165">5.</span><span class="sxs-lookup"><span data-stu-id="64e6d-165">5.</span></span>  | <span data-ttu-id="64e6d-166">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="64e6d-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="64e6d-167">6.</span><span class="sxs-lookup"><span data-stu-id="64e6d-167">6.</span></span>  | <span data-ttu-id="64e6d-168">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="64e6d-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="64e6d-169">7.</span><span class="sxs-lookup"><span data-stu-id="64e6d-169">7.</span></span>  | <span data-ttu-id="64e6d-170">Valitse Työtilauksen tyyppi -kentässä Valmiiden tuotteiden poispano.</span><span class="sxs-lookup"><span data-stu-id="64e6d-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="64e6d-171">8.</span><span class="sxs-lookup"><span data-stu-id="64e6d-171">8.</span></span>  | <span data-ttu-id="64e6d-172">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="64e6d-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="64e6d-173">9.</span><span class="sxs-lookup"><span data-stu-id="64e6d-173">9.</span></span>  | <span data-ttu-id="64e6d-174">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="64e6d-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="64e6d-175">10.</span><span class="sxs-lookup"><span data-stu-id="64e6d-175">10.</span></span> | <span data-ttu-id="64e6d-176">Valitse Työtilauksen tyyppi -kenttään Rinnakkaistuotteen ja sivutuotteen poispano.</span><span class="sxs-lookup"><span data-stu-id="64e6d-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="64e6d-177">11.</span><span class="sxs-lookup"><span data-stu-id="64e6d-177">11.</span></span> | <span data-ttu-id="64e6d-178">Laajenna Varastosijainnit-osa.</span><span class="sxs-lookup"><span data-stu-id="64e6d-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="64e6d-179">12.</span><span class="sxs-lookup"><span data-stu-id="64e6d-179">12.</span></span> | <span data-ttu-id="64e6d-180">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="64e6d-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="64e6d-181">13.</span><span class="sxs-lookup"><span data-stu-id="64e6d-181">13.</span></span> | <span data-ttu-id="64e6d-182">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="64e6d-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="64e6d-183">14.</span><span class="sxs-lookup"><span data-stu-id="64e6d-183">14.</span></span> | <span data-ttu-id="64e6d-184">Kirjoita varasto-luetteloon arvo 51.</span><span class="sxs-lookup"><span data-stu-id="64e6d-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="64e6d-185">15.</span><span class="sxs-lookup"><span data-stu-id="64e6d-185">15.</span></span> | <span data-ttu-id="64e6d-186">Syötä tai valitse Sijainti-kentän arvoksi 001.</span><span class="sxs-lookup"><span data-stu-id="64e6d-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="64e6d-187">16.</span><span class="sxs-lookup"><span data-stu-id="64e6d-187">16.</span></span> | <span data-ttu-id="64e6d-188">Laajenna Tuotteet-osa.</span><span class="sxs-lookup"><span data-stu-id="64e6d-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="64e6d-189">17.</span><span class="sxs-lookup"><span data-stu-id="64e6d-189">17.</span></span> | <span data-ttu-id="64e6d-190">Valitse Tuotteen valinta -kentän arvoksi Valittu.</span><span class="sxs-lookup"><span data-stu-id="64e6d-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="64e6d-191">18.</span><span class="sxs-lookup"><span data-stu-id="64e6d-191">18.</span></span> | <span data-ttu-id="64e6d-192">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="64e6d-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="64e6d-193">19.</span><span class="sxs-lookup"><span data-stu-id="64e6d-193">19.</span></span> | <span data-ttu-id="64e6d-194">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="64e6d-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="64e6d-195">20.</span><span class="sxs-lookup"><span data-stu-id="64e6d-195">20.</span></span> | <span data-ttu-id="64e6d-196">Syötä tai valitse Nimiketunnus-kentän arvoksi L0101.</span><span class="sxs-lookup"><span data-stu-id="64e6d-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="64e6d-197">21.</span><span class="sxs-lookup"><span data-stu-id="64e6d-197">21.</span></span> | <span data-ttu-id="64e6d-198">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="64e6d-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="64e6d-199">Raportoi tuotantotilaus valmistuneeksi sijaintiin, jossa ei ole varastorekisterinumero-ohjausta</span><span class="sxs-lookup"><span data-stu-id="64e6d-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="64e6d-200">Tässä menettelyssä näytetään esimerkki valmiiksi ilmoittamisesta sijaintiin, jota ei ohjata rekisterikilvellä.</span><span class="sxs-lookup"><span data-stu-id="64e6d-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="64e6d-201">Tehtävä edellyttää käytettävää työkäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="64e6d-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="64e6d-202">Työkäytännön määrittäminen on esitelty edellisessä menettelyssä.</span><span class="sxs-lookup"><span data-stu-id="64e6d-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="64e6d-203">STEPS (25)</span><span class="sxs-lookup"><span data-stu-id="64e6d-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="64e6d-204"><strong>Alitehtävä: Määritä tulostussijainti.</strong></span><span class="sxs-lookup"><span data-stu-id="64e6d-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="64e6d-205">Valitse Organisaation hallinto &gt; Resurssit &gt; Resurssiryhmät.</span><span class="sxs-lookup"><span data-stu-id="64e6d-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="64e6d-206">Valitse luettelosta resurssiryhmä 5102.</span><span class="sxs-lookup"><span data-stu-id="64e6d-206">In the list, select resource group &#39;5102&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="64e6d-207">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="64e6d-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="64e6d-208">Kirjoita Tulostusvarasto-kenttään arvo 51.</span><span class="sxs-lookup"><span data-stu-id="64e6d-208">In the Output warehouse field, enter &#39;51&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="64e6d-209">Kirjoita Tulostussijainti-kenttään arvo 001.</span><span class="sxs-lookup"><span data-stu-id="64e6d-209">In the Output location field, enter &#39;001&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="64e6d-210">Sijainti 001 ei ole rekisterikilven mukaan ohjattu sijainti.</span><span class="sxs-lookup"><span data-stu-id="64e6d-210">Location 001 isn&#39;t a license plate–controlled location.</span></span> <span data-ttu-id="64e6d-211">Voit määrittää rekisterikilven mukaan ohjaamattoman sijainnin ainoastaan, jos sijainnille on olemassa soveltuva työkäytäntö.</span><span class="sxs-lookup"><span data-stu-id="64e6d-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="64e6d-212"><strong>Alitehtävä: Luo tuotantotilaus ja ilmoita se valmiiksi.</strong></span><span class="sxs-lookup"><span data-stu-id="64e6d-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="64e6d-213">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="64e6d-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="64e6d-214">Siirry kohtaan Tuotannonhallinta &gt; Tuotantotilaukset &gt; Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="64e6d-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="64e6d-215">Valitse Uusi tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="64e6d-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="64e6d-216">Kirjoita Nimiketunnus-kenttään arvo L0101.</span><span class="sxs-lookup"><span data-stu-id="64e6d-216">In the Item number field, enter &#39;L0101&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="64e6d-217">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="64e6d-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="64e6d-218">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="64e6d-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="64e6d-219">Valitse Arvio.</span><span class="sxs-lookup"><span data-stu-id="64e6d-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="64e6d-220">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="64e6d-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="64e6d-221">Valitse Käynnistys.</span><span class="sxs-lookup"><span data-stu-id="64e6d-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="64e6d-222">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="64e6d-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="64e6d-223">Valitse Automaattinen tuoterakennekulutus -kentässä Ei koskaan.</span><span class="sxs-lookup"><span data-stu-id="64e6d-223">In the Automatic BOM consumption field, select &#39;Never&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="64e6d-224">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="64e6d-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="64e6d-225">Valitse Ilmoita automaattisesti valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="64e6d-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="64e6d-226">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="64e6d-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="64e6d-227">Valitse Hyväksy virhe -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="64e6d-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="64e6d-228">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="64e6d-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="64e6d-229">Valitse toimintoruudussa Varasto.</span><span class="sxs-lookup"><span data-stu-id="64e6d-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="64e6d-230">Valitse Työn tiedot.</span><span class="sxs-lookup"><span data-stu-id="64e6d-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="64e6d-231">Kun tuotantotilaus on raportoitu päättyneeksi, poispanotöitä ei luotu.</span><span class="sxs-lookup"><span data-stu-id="64e6d-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="64e6d-232">Tämä johtuu siitä, että määritettynä on työn käytäntö, joka estää töiden luonnin, kun tuote L0101 ilmoitetaan valmiiksi sijaintiin 001.</span><span class="sxs-lookup"><span data-stu-id="64e6d-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>




