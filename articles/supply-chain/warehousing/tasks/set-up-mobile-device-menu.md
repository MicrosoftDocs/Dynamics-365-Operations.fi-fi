--- 
title: "Määritä mobiililaitteen valikkokohde Ostotilaus-tyypin työn valmistumiselle"
description: "Seuraavassa menettelyssä kuvataan, miten määrität Mobiililaite-valikkovaihtoehdon."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 326a0039d2769ee5f459a87c302c93604d2379aa
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a><span data-ttu-id="d09a0-103">Määritä mobiililaitteen valikkokohde Ostotilaus-tyypin työn valmistumiselle</span><span class="sxs-lookup"><span data-stu-id="d09a0-103">Set up a mobile device menu item for completing work of type Purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d09a0-104">Seuraavassa menettelyssä kuvataan, miten määrität Mobiililaite-valikkovaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="d09a0-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="d09a0-105">Tässä esimerkissä valikkovaihtoehdolla suoritetaan Ostotilaus-tyypin työ.</span><span class="sxs-lookup"><span data-stu-id="d09a0-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="d09a0-106">Työn voimassaolo määritetään valikkokohteeseen liitetyn työluokan perusteella.</span><span class="sxs-lookup"><span data-stu-id="d09a0-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="d09a0-107">Voit käyttää tätä opastusta USMF-yrityksen demotiedoissa.</span><span class="sxs-lookup"><span data-stu-id="d09a0-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="d09a0-108">Tämän menettelyn suorittaa yleensä varastopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="d09a0-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="d09a0-109">Luo mobiililaitteen valikkovaihtoehto</span><span class="sxs-lookup"><span data-stu-id="d09a0-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="d09a0-110">Valitse Mobiililaitteen valikkovaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="d09a0-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="d09a0-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d09a0-111">Click New.</span></span>
3. <span data-ttu-id="d09a0-112">Kirjoita arvo Valikkovaihtoehdon nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="d09a0-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="d09a0-113">Anna yksilöivä arvo.</span><span class="sxs-lookup"><span data-stu-id="d09a0-113">Enter a unique value.</span></span> <span data-ttu-id="d09a0-114">Voit esimerkiksi kirjoittaa Ostotilaussiirto.</span><span class="sxs-lookup"><span data-stu-id="d09a0-114">For example, you could type POMove.</span></span> <span data-ttu-id="d09a0-115">Kirjoita arvo muistiin, sillä sitä tarvitaan myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="d09a0-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="d09a0-116">Kirjoita Otsikko-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d09a0-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="d09a0-117">Tämä on mobiililaitteessa näkyvä otsikko.</span><span class="sxs-lookup"><span data-stu-id="d09a0-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="d09a0-118">Voit esimerkiksi kirjoittaa Ostotilauksen siirto.</span><span class="sxs-lookup"><span data-stu-id="d09a0-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="d09a0-119">Valitse Tila-kentässä Työ.</span><span class="sxs-lookup"><span data-stu-id="d09a0-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="d09a0-120">Valitse Käytä nykyistä työtä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d09a0-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="d09a0-121">Tällä mobiililaitteen valikkovaihtoehdolla suoritetaan aiemmin luotu työ.</span><span class="sxs-lookup"><span data-stu-id="d09a0-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="d09a0-122">Niinpä arvoksi on valittava Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d09a0-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="d09a0-123">Näytä varaston tila -kenttä määrittää, näytetäänkö varastosaldon varaston tila mobiililaitteessa varastotyöntekijälle.</span><span class="sxs-lookup"><span data-stu-id="d09a0-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="d09a0-124">Valitse Ohjaaja-kentässä Järjestelmän ryhmittely.</span><span class="sxs-lookup"><span data-stu-id="d09a0-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="d09a0-125">Kun valitset arvon Ohjaaja-kentässä, tämän sivun Yleinen-osaan tulee näkyviin lisäkenttiä.</span><span class="sxs-lookup"><span data-stu-id="d09a0-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="d09a0-126">Näkyvät kentät määräytyvät sen mukaan, mitä olet valinnut.</span><span class="sxs-lookup"><span data-stu-id="d09a0-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="d09a0-127">Kun valitset Järjestelmän ryhmittelyn, kaksi uutta kenttää lisätään.</span><span class="sxs-lookup"><span data-stu-id="d09a0-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="d09a0-128">Ne käsitellään seuraavaksi.</span><span class="sxs-lookup"><span data-stu-id="d09a0-128">These are explained below.</span></span>  
8. <span data-ttu-id="d09a0-129">Kirjoita Järjestelmän ryhmittely -kenttään WorkPoolId.</span><span class="sxs-lookup"><span data-stu-id="d09a0-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="d09a0-130">Kun varastotyöntekijät avaavat tämän valikkovaihtoehdon, heitä pyydetään skannaamaan työpoolin tunnus.</span><span class="sxs-lookup"><span data-stu-id="d09a0-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="d09a0-131">Käyttäjälle lähetetään kaikki työtilaukset, joilla on tämä työpoolin tunnus, sekä kaikki avoimet työtilausrivit, joissa on yksi tähän valikkovaihtoehtoon lisätty työluokka.</span><span class="sxs-lookup"><span data-stu-id="d09a0-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="d09a0-132">Kirjoita Järjestelmän ryhmittelyotsikko -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d09a0-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="d09a0-133">Tämä teksti näkyy mobiililaitteen käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="d09a0-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="d09a0-134">Voit esimerkiksi kirjoittaa Työpooli.</span><span class="sxs-lookup"><span data-stu-id="d09a0-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="d09a0-135">Valitse Ohita rekisterikilpi määrityksen aikana -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d09a0-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="d09a0-136">Varastotyöntekijät voivat ohittaa tällä asetuksella kohderekisterikilven, kun nimikkeet on laskettu alas rekisterikilpiohjattuun sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="d09a0-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="d09a0-137">Valitse Ryhmä pantu pois -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d09a0-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="d09a0-138">Jos kaikilla työtilauksen Määritä-riveillä on sama sijainti, käyttäjä vastaanottaa kaikille riveille yhden yhdistetyn Määritä-ohjeen.</span><span class="sxs-lookup"><span data-stu-id="d09a0-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="d09a0-139">Tarkistusmallin tunnus: Voit määrittää työntarkistusmallin avulla, että valikkovaihtoehdon työprosessi on keskeytettävä, jotta toisen työvaihe voidaan suorittaa.</span><span class="sxs-lookup"><span data-stu-id="d09a0-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="d09a0-140">Jos tämä valikkovaihtoehto on esimerkiksi saapuvalle työlle, tarkistusmalli saattaa edellyttää, että työntekijä tarkistaa lämpötilan.</span><span class="sxs-lookup"><span data-stu-id="d09a0-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="d09a0-141">Prosessin keskeytyskohta määritetään tarkistusmallissa ja se voi olla esimerkiksi työn aloitus, valmistuminen tai tilan muutos.</span><span class="sxs-lookup"><span data-stu-id="d09a0-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="d09a0-142">Laajenna Työluokat-osa.</span><span class="sxs-lookup"><span data-stu-id="d09a0-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="d09a0-143">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d09a0-143">Click New.</span></span>
14. <span data-ttu-id="d09a0-144">Kirjoita Työluokan tunnus -kenttään Osto.</span><span class="sxs-lookup"><span data-stu-id="d09a0-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="d09a0-145">Työpooli rajoittaa työn, johon valikkovaihtoehtoa voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="d09a0-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="d09a0-146">Tässä tapauksessa sitä käytetään avoimilla työtilausriveillä, joilla ostotyöluokan tunnus.</span><span class="sxs-lookup"><span data-stu-id="d09a0-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="d09a0-147">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d09a0-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="d09a0-148">Määritä työn vahvistus</span><span class="sxs-lookup"><span data-stu-id="d09a0-148">Set up work confirmation</span></span>
1. <span data-ttu-id="d09a0-149">Valitse Työn vahvistusasetukset.</span><span class="sxs-lookup"><span data-stu-id="d09a0-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="d09a0-150">Valitse Työtyyppi-kentässä Keräilyt.</span><span class="sxs-lookup"><span data-stu-id="d09a0-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="d09a0-151">Valitse Vahvista automaattisesti -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="d09a0-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="d09a0-152">Jos työn tyyppi on Keräily, sen työohjeet vahvistetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="d09a0-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="d09a0-153">Tätä ohjetta ei näytetä käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="d09a0-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="d09a0-154">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d09a0-154">Click New.</span></span>
5. <span data-ttu-id="d09a0-155">Valitse Työtyyppi-kentässä Määritä.</span><span class="sxs-lookup"><span data-stu-id="d09a0-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="d09a0-156">Valitse Sijainnin vahvistus -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="d09a0-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="d09a0-157">Varastotyöntekijää pyydetään vahvistamaan skannaamalla sijainti, johon nimike on laskettu alas.</span><span class="sxs-lookup"><span data-stu-id="d09a0-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="d09a0-158">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d09a0-158">Click Save.</span></span>
8. <span data-ttu-id="d09a0-159">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d09a0-159">Close the page.</span></span>
9. <span data-ttu-id="d09a0-160">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d09a0-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="d09a0-161">Lisää valikkovaihtoehto mobiililaitteen valikkoon</span><span class="sxs-lookup"><span data-stu-id="d09a0-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="d09a0-162">Valitse Mobiililaitevalikko.</span><span class="sxs-lookup"><span data-stu-id="d09a0-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="d09a0-163">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="d09a0-163">Click Edit.</span></span>
3. <span data-ttu-id="d09a0-164">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="d09a0-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d09a0-165">Voit esimerkiksi suodattaa Nimi-kenttää arvolla inbound.</span><span class="sxs-lookup"><span data-stu-id="d09a0-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="d09a0-166">Haluat etsi valikon, jota käytät saapuville valikkovaihtoehdoille.</span><span class="sxs-lookup"><span data-stu-id="d09a0-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="d09a0-167">USMF:ssä sen nimenä on Saapuva.</span><span class="sxs-lookup"><span data-stu-id="d09a0-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="d09a0-168">Valitse puussa a value.</span><span class="sxs-lookup"><span data-stu-id="d09a0-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="d09a0-169">Napsauttamalla oikealle osoittavaa työtä.</span><span class="sxs-lookup"><span data-stu-id="d09a0-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="d09a0-170">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d09a0-170">Click Save.</span></span>
7. <span data-ttu-id="d09a0-171">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d09a0-171">Close the page.</span></span>


