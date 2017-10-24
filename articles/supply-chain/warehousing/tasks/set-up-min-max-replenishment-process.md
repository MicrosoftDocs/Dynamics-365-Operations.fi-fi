--- 
title: "Määritä minimi-/maksimitäydennysprosessi"
description: "Seuraavassa menettelyssä kuvataan, miten voit määrittää uuden täydennysprosessin, joka käyttää minimi-/maksimitäydennysstrategiaa."
author: perlynne
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 02af5d1beb2d4eb6a7162b47c42854725fbdbec2
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-min-max-replenishment-process"></a><span data-ttu-id="9cbc0-103">Määritä minimi-/maksimitäydennysprosessi</span><span class="sxs-lookup"><span data-stu-id="9cbc0-103">Set up a min-max replenishment process</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9cbc0-104">Seuraavassa menettelyssä kuvataan, miten voit määrittää uuden täydennysprosessin, joka käyttää minimi-/maksimitäydennysstrategiaa.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-104">This procedure shows you how to set up a new replenishment process which uses the minimum/maximum replenishment strategy.</span></span> <span data-ttu-id="9cbc0-105">Sijainnin täydennystyö luodaan, kun varaston vähimmäistaso laskee minimitason alle.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-105">When inventory falls below the minimum level, work will be created to replenish the location.</span></span> <span data-ttu-id="9cbc0-106">Menettelyssä näytetään myös, miten kiinteitä keräilysijainteja voi käyttää sallimaan täydennys vaikka varastosaldo laskisikin minimitason alle, ja miten täydennysprosessin voi määrittää ajettavaksi säännöllisesti eräajona.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-106">The procedure also shows how to use fixed picking locations to allow restocking even if inventory falls below the minimum level, and how to enable the replenishment process to run regularly using a batch job.</span></span> <span data-ttu-id="9cbc0-107">Yleensä varastopäällikkö tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-107">These tasks would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="9cbc0-108">Voit suorittaa tämän menettelyn USMF-malliyrityksessä käyttämällä muistiinpanojen esimerkkiarvoja, tai voit suorittaa sen omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-108">You can run this procedure in the USMF demo data company using the example values in the notes, or can run it on your own data.</span></span> <span data-ttu-id="9cbc0-109">Jos käytät omia tietoja, varmista, että sinulla on varasto, jolla varastonhallintaprosessit ovat käytössä.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-109">If you’re using your own data, make sure that you have a warehouse that’s enabled for Warehouse management processes.</span></span>


## <a name="create-a-fixed-picking-location"></a><span data-ttu-id="9cbc0-110">Luo kiinteä keräilysijainti</span><span class="sxs-lookup"><span data-stu-id="9cbc0-110">Create a fixed picking location</span></span>
1. <span data-ttu-id="9cbc0-111">Valitse Varastonhallinta > Asetukset > Varasto > Kiinteät sijainnit.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-111">Go to Warehouse management > Setup > Warehouse > Fixed locations.</span></span>
    * <span data-ttu-id="9cbc0-112">Tämä on valinnainen tehtävä minimi-/maksimitäydennysprosessissa, mutta jos käytät kiinteää keräilyvarastopaikkaa, varasto voidaan täydentää vaikka se laskee alle vähimmäistason, koska järjestelmä määrittää, mitkä on täydennettävä, vaikka täydennettävää ei olisikaan.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-112">This is an optional task for min-max replenishment, but if you use fixed picking location, this allows stock to be replenished even if it falls below the minimum level, because the system can determine which items need to be replenished, even if there aren't any left.</span></span>  
2. <span data-ttu-id="9cbc0-113">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-113">Click New.</span></span>
3. <span data-ttu-id="9cbc0-114">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-114">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="9cbc0-115">Jos käytössä on USMF, voit valita nimikkeen A0001.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-115">If you’re using USMF, you can select item A0001.</span></span>  
4. <span data-ttu-id="9cbc0-116">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-116">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="9cbc0-117">Jos käytössä on USMF, valitse toimipaikka 2.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-117">If you’re using USMF, you can select site 2.</span></span>  
5. <span data-ttu-id="9cbc0-118">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-118">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="9cbc0-119">Jos käytössä on USMF, voit valita varaston 24.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-119">If you’re using USMF, you can select warehouse 24.</span></span>  
6. <span data-ttu-id="9cbc0-120">Syötä tai valitse arvo Sijainti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-120">In the Location field, enter or select a value.</span></span>
    * <span data-ttu-id="9cbc0-121">Jos käytössä on USMF, valitse CP-003.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-121">If you’re using USMF, you can select CP-003.</span></span>  
7. <span data-ttu-id="9cbc0-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-122">Close the page.</span></span>

## <a name="create-a-replenishment-location-directive"></a><span data-ttu-id="9cbc0-123">Luo täydennyssijainnin direktiivi</span><span class="sxs-lookup"><span data-stu-id="9cbc0-123">Create a replenishment location directive</span></span>
1. <span data-ttu-id="9cbc0-124">Valitse Varastonhallinta > Asetukset > Sijaintidirektiivit.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-124">Go to Warehouse management > Setup > Location directives.</span></span>
    * <span data-ttu-id="9cbc0-125">Sijaintidirektiivejä käytetään määrittämään, mistä nimikkeet tulee keräillä täydennysprosessissa.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-125">Location directives are used to determine where items should be picked from in the replenishment process.</span></span>  
2. <span data-ttu-id="9cbc0-126">Valitse Työtilauksen tyyppi -kentässä Täydennys.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-126">In the Work order type field, select 'Replenishment'.</span></span>
3. <span data-ttu-id="9cbc0-127">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-127">Click New.</span></span>
4. <span data-ttu-id="9cbc0-128">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-128">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9cbc0-129">Valitse Työtyyppi-kentässä Keräilyt.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-129">In the Work type field, select 'Pick'.</span></span>
6. <span data-ttu-id="9cbc0-130">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-130">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="9cbc0-131">Jos käytössä on USMF, valitse toimipaikka 2.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-131">If you’re using USMF, you can select site 2.</span></span>  
7. <span data-ttu-id="9cbc0-132">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-132">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="9cbc0-133">Jos käytössä on USMF, voit valita varaston 24.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-133">If you’re using USMF, you can select warehouse 24.</span></span>  
8. <span data-ttu-id="9cbc0-134">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-134">Click Save.</span></span>
9. <span data-ttu-id="9cbc0-135">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-135">Click New.</span></span>
10. <span data-ttu-id="9cbc0-136">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-136">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="9cbc0-137">Lisää Määrään-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-137">In the To quantity field, enter a number.</span></span>
    * <span data-ttu-id="9cbc0-138">Voit esimerkiksi asettaa sen arvoon 9999.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-138">For example, you can set it to 9999.</span></span>  
12. <span data-ttu-id="9cbc0-139">Merkitse Salli jakaminen -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-139">Select the Allow split check box.</span></span>
    * <span data-ttu-id="9cbc0-140">Jos valitset tämän vaihtoehdon, töiden luontiprosessi sallii työrivien määrien jakamisen useille sijainneille.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-140">If you select this option, the work creation process will allow work line quantities to be split across multiple locations.</span></span>  
13. <span data-ttu-id="9cbc0-141">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-141">Click Save.</span></span>
14. <span data-ttu-id="9cbc0-142">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-142">Click New.</span></span>
15. <span data-ttu-id="9cbc0-143">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-143">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="9cbc0-144">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-144">In the Name field, type a value.</span></span>
17. <span data-ttu-id="9cbc0-145">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-145">Click Save.</span></span>
18. <span data-ttu-id="9cbc0-146">Valitse Muokkaa kyselyä.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-146">Click Edit query.</span></span>
    * <span data-ttu-id="9cbc0-147">Voit muokata tätä kyselyä lisätäksesi rajoituksia varaston valintasijainnille täydennysprosessissa.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-147">You can edit this query to add restrictions where inventory can be selected from in the replenishment process.</span></span> <span data-ttu-id="9cbc0-148">On esimerkiksi mahdollista, että varastoa tulisi käyttää ainoastaan irtotavara-alueelta.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-148">For example, it could be that inventory should only be used from the Bulk area of the warehouse.</span></span>  
19. <span data-ttu-id="9cbc0-149">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-149">Click OK.</span></span>
20. <span data-ttu-id="9cbc0-150">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-150">Close the page.</span></span>

## <a name="create-a-replenishment-work-template"></a><span data-ttu-id="9cbc0-151">Luo täydennystyömalli</span><span class="sxs-lookup"><span data-stu-id="9cbc0-151">Create a replenishment work template</span></span>
1. <span data-ttu-id="9cbc0-152">Valitse Varastonhallinta > Asetukset > Työ > Työmallit.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-152">Go to Warehouse management > Setup > Work > Work templates.</span></span>
    * <span data-ttu-id="9cbc0-153">Työmallin avulla järjestelmää ohjataan minimi-/maksimitäydennysprosessin luomisessa.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-153">The work template is use to guide the system as to how the min/max replenishment work must be created.</span></span> <span data-ttu-id="9cbc0-154">Työmallissa on oltava rivi vähintään keräilylle ja asettamiselle.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-154">As a minimum, there must be a work template line for a pick and a put.</span></span> <span data-ttu-id="9cbc0-155">Työmallin ilmoitetaan olevan virheellinen, kunnes kaikki tarpeellinen tieto on täytetty.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-155">The work template will say that it’s Invalid until all the necessary information has been filled in.</span></span>  
2. <span data-ttu-id="9cbc0-156">Valitse Työtilauksen tyyppi -kentässä Täydennys.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-156">In the Work order type field, select 'Replenishment'.</span></span>
3. <span data-ttu-id="9cbc0-157">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-157">Click New.</span></span>
4. <span data-ttu-id="9cbc0-158">Kirjoita Työmalli-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-158">In the Work template field, type a value.</span></span>
5. <span data-ttu-id="9cbc0-159">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-159">Click Save.</span></span>
6. <span data-ttu-id="9cbc0-160">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-160">Click New.</span></span>
7. <span data-ttu-id="9cbc0-161">Valitse Työtyyppi-kentässä Keräilyt.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-161">In the Work type field, select 'Pick'.</span></span>
8. <span data-ttu-id="9cbc0-162">Syötä tai valitse arvo Työluokan tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-162">In the Work class ID field, enter or select a value.</span></span>
    * <span data-ttu-id="9cbc0-163">Tämän tulisi olla täydentämiseen liittyvä työn luokka.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-163">This should be a work class related to replenishment.</span></span> <span data-ttu-id="9cbc0-164">Jos USMF on käytössä, valitse Täydennys.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-164">If you’re using USMF, select Replenish.</span></span>  
9. <span data-ttu-id="9cbc0-165">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-165">Click New.</span></span>
10. <span data-ttu-id="9cbc0-166">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-166">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="9cbc0-167">Valitse Työtyyppi-kentässä Määritä.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-167">In the Work type field, select 'Put'.</span></span>
12. <span data-ttu-id="9cbc0-168">Syötä tai valitse arvo Työluokan tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-168">In the Work class ID field, enter or select a value.</span></span>
13. <span data-ttu-id="9cbc0-169">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-169">Click Save.</span></span>
14. <span data-ttu-id="9cbc0-170">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-170">Close the page.</span></span>

## <a name="create-a-new-replenishment-template"></a><span data-ttu-id="9cbc0-171">Luo uusi täydennysmalli</span><span class="sxs-lookup"><span data-stu-id="9cbc0-171">Create a new replenishment template</span></span>
1. <span data-ttu-id="9cbc0-172">Valitse Varastonhallinta > Asetukset > Täydennys > Täydennysmallit.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-172">Go to Warehouse management > Setup > Replenishment > Replenishment templates.</span></span>
    * <span data-ttu-id="9cbc0-173">Täydennysmallilla määritetään täydennettävät nimikkeet ja määrät sekä täydennettävä sijainti.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-173">The replenishment template is used to define the items and quantities, and the location to replenish.</span></span>  
2. <span data-ttu-id="9cbc0-174">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-174">Click New.</span></span>
3. <span data-ttu-id="9cbc0-175">Kirjoita Täydennysmalli-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-175">In the Replenish template field, type a value.</span></span>
    * <span data-ttu-id="9cbc0-176">Anna mallille nimi, joka osoittaa, että se on minimi-/maksimitäydennysprosessia varten.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-176">Give the template a name to indicate that it’s for min/max replenishment.</span></span>  
4. <span data-ttu-id="9cbc0-177">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-177">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9cbc0-178">Merkitse Salli aallon kysynnän käyttää varaamattomia määriä -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-178">Select the Allow wave demand to use unreserved quantities check box.</span></span>
    * <span data-ttu-id="9cbc0-179">Jos valitset tämän vaihtoehdon, se ottaa käyttöön aaltokysynnän täydennyksen kuluttamaan määriä, jotka liittyvät minimi-/maksimitäydennysprosessiin.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-179">If you select this option, it enables wave demand replenishment to consume quantities that are related to min/max replenishment.</span></span> <span data-ttu-id="9cbc0-180">Tästä voi esimerkiksi olla hyötyä, jos minimi-/maksimitäydennystyötä ei ole käsitelty heti, jotta tarpeettomien kysyntää vastaavien täydennystöiden luonti voidaan välttää.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-180">For example, this might be useful if the min/max replenishment work isn’t processed immediately, to avoid unnecessary demand replenishment work from being created.</span></span>  
6. <span data-ttu-id="9cbc0-181">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-181">Click New.</span></span>
7. <span data-ttu-id="9cbc0-182">Syötä Järjestysnumero-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-182">In the Sequence number field, enter a number.</span></span>
8. <span data-ttu-id="9cbc0-183">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-183">In the Description field, type a value.</span></span>
9. <span data-ttu-id="9cbc0-184">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-184">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="9cbc0-185">Syötä tai valitse arvo Täydennysyksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-185">In the Replenishment unit field, enter or select a value.</span></span>
    * <span data-ttu-id="9cbc0-186">Valitse esimerkiksi arvo pcs.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-186">For example, select pcs.</span></span> <span data-ttu-id="9cbc0-187">Tämä asetus on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-187">This setting is mandatory.</span></span> <span data-ttu-id="9cbc0-188">Voit määrittää eri mittayksikön täydennystyölle verrattuna mallissa määritettyihin minimi- ja maksimivaraston tasoihin.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-188">It allows you to specify a different unit of measurement for replenishment work compared to the unit specified for the minimum and maximum stock levels in this template.</span></span>  
11. <span data-ttu-id="9cbc0-189">Anna tai valitse Työmalli-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-189">In the Work template field, enter or select a value.</span></span>
    * <span data-ttu-id="9cbc0-190">Valitse aiemmin luomasi työmalli.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-190">Choose the work template that you created earlier.</span></span>  
12. <span data-ttu-id="9cbc0-191">Syötä numero Vähimmäismäärä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-191">In the Minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="9cbc0-192">Valitse vähimmäismäärä, joka käynnistää täydennyksen.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-192">Select the minimum quantity that should trigger the replenishment.</span></span> <span data-ttu-id="9cbc0-193">Määritä arvoksi esimerkiksi 50.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-193">For example, set this to 50.</span></span> <span data-ttu-id="9cbc0-194">Voit jättää tämän kentän arvoksi nollan, jos täydennät kiinteään sijaintiin ja Täydennä tyhjät kiinteät sijainnit -asetuksen arvo on Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-194">It is possible to leave this set to zero, if you’re replenishing a fixed location and the Replenish empty fixed locations option is set to Yes.</span></span> <span data-ttu-id="9cbc0-195">Suosittelemme myös, että käytät Täydennä vain kiinteät sijainnit -asetusta suorituskyvyn parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-195">We also recommend that you select the Replenish only fixed locations option for performance reasons.</span></span>  
13. <span data-ttu-id="9cbc0-196">Syötä numero Enimmäismäärä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-196">In the Maximum quantity field, enter a number.</span></span>
    * <span data-ttu-id="9cbc0-197">Määritä arvoksi esimerkiksi 100.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-197">For example, set this to 100.</span></span>  
14. <span data-ttu-id="9cbc0-198">Syötä tai valitse arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-198">In the Unit field, enter or select a value.</span></span>
    * <span data-ttu-id="9cbc0-199">Määritä vähimmäis- ja enimmäismäärien yksikkö.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-199">Assign the unit for the minimum and maximum quantities.</span></span> <span data-ttu-id="9cbc0-200">Määritä arvoksi esimerkiksi pcs.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-200">For example, set this to pcs.</span></span>  
15. <span data-ttu-id="9cbc0-201">Merkitse Täydennä tyhjät kiinteät sijainnit -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-201">Select the Replenish empty fixed locations check box.</span></span>
    * <span data-ttu-id="9cbc0-202">Valitse tämä valintaruutu, kun haluat täydentää kiinteät sijainnit, kun ne ovat tyhjät.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-202">Select this check box to replenish fixed locations when they are empty.</span></span> <span data-ttu-id="9cbc0-203">Muussa tapauksessa vain sijainnit, jossa määrä on käytettävissä, täydennetään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-203">Otherwise, only the locations where there is a quantity on hand will be replenished.</span></span>  
16. <span data-ttu-id="9cbc0-204">Merkitse Täydennä vain kiinteät sijainnit -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-204">Select the Replenish only fixed locations check box.</span></span>
17. <span data-ttu-id="9cbc0-205">Napsauta Valitse tuotteet -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-205">Click Select products.</span></span>
    * <span data-ttu-id="9cbc0-206">Tässä voit määrittää, mitkä tuotteet tulee täydentää.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-206">This is the place to define which products should be replenished.</span></span> <span data-ttu-id="9cbc0-207">Jos Kiinteät keräilysijainnit -asetus on valittuna, sijainnit on myös määritettävä tähän kyselyyn.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-207">If the Fixed picking locations option is selected, you also need to define the locations in this query.</span></span> <span data-ttu-id="9cbc0-208">Saatavilla on sekä variantti- että tuotekohtaisia kyselyitä.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-208">Variant-specific queries are available as well product-specific queries.</span></span>  
18. <span data-ttu-id="9cbc0-209">Valitse Nimikkeet-rivi.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-209">Select the Items row.</span></span>
19. <span data-ttu-id="9cbc0-210">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-210">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="9cbc0-211">Valitse kiinteisiin sijainteihin täydennettävät nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-211">Select the items that should be replenished at the fixed locations.</span></span> <span data-ttu-id="9cbc0-212">Kirjoita esimerkiksi A* valitaksesi kaikki nimiketunnukset, jotka alkavat A:lla.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-212">For example, type A* to select all item numbers beginning with A.</span></span>  
20. <span data-ttu-id="9cbc0-213">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-213">Click Add.</span></span>
    * <span data-ttu-id="9cbc0-214">Lisää sijainnin entiteetti (jos se on jo olemassa) rajataksesi täydennystyön kiinteisiin keräilysijainteihin varaston tietyllä alueella.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-214">Add the Location entity (unless it already exists) to be able to restrict the replenishment work to the fixed picking locations within a specific area of the warehouse.</span></span>  
21. <span data-ttu-id="9cbc0-215">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-215">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="9cbc0-216">Aseta Taulukko-kentän arvoksi Sijainnit.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-216">Set the Table field to Locations.</span></span>
23. <span data-ttu-id="9cbc0-217">Valitse Kenttä-kenttään Sijainnin profiilitunnus.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-217">In the Field field, select Location profile ID.</span></span>
24. <span data-ttu-id="9cbc0-218">Syötä tai valitse arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-218">In the Criteria field, enter or select a value.</span></span>
25. <span data-ttu-id="9cbc0-219">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-219">Click OK.</span></span>
26. <span data-ttu-id="9cbc0-220">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-220">Close the page.</span></span>

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a><span data-ttu-id="9cbc0-221">Aseta täydennysprosessi ajettavaksi eräajona</span><span class="sxs-lookup"><span data-stu-id="9cbc0-221">Set the replenishment process to run as a batch job</span></span>
1. <span data-ttu-id="9cbc0-222">Valitse Varastonhallinta > Täydennys > Täydennykset. </span><span class="sxs-lookup"><span data-stu-id="9cbc0-222">Go to Warehouse management > Replenishment > Replenishments.</span></span>
    * <span data-ttu-id="9cbc0-223">Täydennykset-sivulla voit asettaa täydennykset ajettavaksi eräajona tai vaatia, että ne käynnistetään manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-223">The Replenishments page allows you to set up replenishment to run as a batch job, or to require that it’s started manually.</span></span>  
2. <span data-ttu-id="9cbc0-224">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-224">Click Filter.</span></span>
3. <span data-ttu-id="9cbc0-225">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-225">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="9cbc0-226">Syötä tai valitse arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-226">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="9cbc0-227">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-227">Click OK.</span></span>
6. <span data-ttu-id="9cbc0-228">Laajenna Suorita taustalla -osa.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-228">Expand the Run in the background section.</span></span>
7. <span data-ttu-id="9cbc0-229">Aseta Eräkäsittely-asetuksen arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-229">Set the Batch processing option to Yes.</span></span>
8. <span data-ttu-id="9cbc0-230">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-230">Click Recurrence.</span></span>
9. <span data-ttu-id="9cbc0-231">Valitse päättymispäivämääräasetuksen arvoksi Ei.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-231">Select the No end date option.</span></span>
10. <span data-ttu-id="9cbc0-232">Aseta toistumismalli.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-232">Set the Recurrance pattern.</span></span>
    * <span data-ttu-id="9cbc0-233">Valitse esimerkiksi Päivää.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-233">For example, select Days.</span></span>  
11. <span data-ttu-id="9cbc0-234">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-234">Click OK.</span></span>
12. <span data-ttu-id="9cbc0-235">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9cbc0-235">Click OK.</span></span>


