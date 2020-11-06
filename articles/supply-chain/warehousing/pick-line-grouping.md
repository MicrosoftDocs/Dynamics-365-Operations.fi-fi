---
title: Keräilyrivin ryhmittely
description: Tässä ohjeaiheessa on keräilyrivin yhteenveto.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b3497d43a500898207ed5154721ee0e3a327fb93
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017733"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="d9d9c-103">Keräilyrivin ryhmittely</span><span class="sxs-lookup"><span data-stu-id="d9d9c-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9d9c-104">Keräilyrivin ryhmittelyssä useita työrivejä, joilla on sama nimike ja sijainti voidaan yhdistää yhdeksi keräilyksi, joka esitetään käyttäjälle mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="d9d9c-105">Tämän vuoksi varastotyöntekijät voivat saada mahdollisimman tehokkaat ohjeet, mutta myös vaadittavien työlinjojen erottaminen järjestelmässä säilyy (esimerkiksi eri kontteihin ja tilauksiin).</span><span class="sxs-lookup"><span data-stu-id="d9d9c-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="d9d9c-106">Määritä keräilyrivin ryhmittely</span><span class="sxs-lookup"><span data-stu-id="d9d9c-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="d9d9c-107">Luo mobiililaitteen valikkovaihtoehto</span><span class="sxs-lookup"><span data-stu-id="d9d9c-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="d9d9c-108">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot** ja luo uusi valikkokohde, jonka nimi on **Myyntiryhmän keräily – käyttäjän ohjaama**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items** , and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="d9d9c-109">Määritä seuraavat arvot **Mobiililaitteen valikkovaihtoehdot** -valinnan alla:</span><span class="sxs-lookup"><span data-stu-id="d9d9c-109">Under **Mobile device menu items** , set the following values:</span></span>

    - <span data-ttu-id="d9d9c-110">Valitse **Valikkovaihtoehdon nimi** -kenttä ja syötä **Myynnin poiminta - ryhmän rivi**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="d9d9c-111">Valitse **Otsikko** -kenttä ja syötä **Myynnin keräily - ryhmän rivi**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="d9d9c-112">Valitse **Tila** -kentässä **Työ**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="d9d9c-113">Valitse **Käytä nykyistä työtä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="d9d9c-114">**Yleiset** -pikavälilehdessä voit määrittää seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="d9d9c-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="d9d9c-115">Valitse **Ohjaaja** -kentässä **Järjestelmäohjattu**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="d9d9c-116">Määritä **Luo rekisterikilpi** -valinnan asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="d9d9c-117">Määritä **Ryhmäkeräily** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="d9d9c-118">Määritä **Työluokat** -pikavälilehdessä mobiililaitteen valikkokohteelle kelvolliset työluokat noudattamalla näitä vaiheita:</span><span class="sxs-lookup"><span data-stu-id="d9d9c-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="d9d9c-119">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-119">Select **New**.</span></span>
    2. <span data-ttu-id="d9d9c-120">Valitse **Työluokan tunnus** -kentässä **Myynti** tai **Tilauksen keräily** sen mukaan, mitä varastoa käytät.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-120">In the **Work class ID** field, select **Sales** or **SO Pick** , depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="d9d9c-121">Valitse **Työtilaustyyppi** -kentässä **Myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="d9d9c-122">Määritä varaston mobiililaitteen valikko</span><span class="sxs-lookup"><span data-stu-id="d9d9c-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="d9d9c-123">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="d9d9c-124">Lisää juuri luomasi valikkokohde haluamaasi valikkoon.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="d9d9c-125">Määritä työmalli</span><span class="sxs-lookup"><span data-stu-id="d9d9c-125">Set up a work template</span></span>

1. <span data-ttu-id="d9d9c-126">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d9d9c-127">Etsi työmalli, jota käytetään tämän funktion kanssa.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="d9d9c-128">Tässä esimerkissä valitaan **Standard 51-poiminta** vaiheeseen Contoso-työmalli.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="d9d9c-129">Valitse valikosta **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="d9d9c-130">Valitse **Lajittelu** -välilehdestä **Lisää** ja määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="d9d9c-130">On the **Sorting** tab, select **Add** , and then set the following values:</span></span>

    - <span data-ttu-id="d9d9c-131">Valitse **Taulu** -kentästä **Väliaikaiset työtapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="d9d9c-132">Valitse **Johdettu taulu** -kentästä **Väliaikaiset työtapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="d9d9c-133">Valitse **Kenttä** -kentässä **Nimikkeen numero**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="d9d9c-134">Valitse **Hakusuunta** -kentässä **Laskeva**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="d9d9c-135">Jotta poimintarivin ryhmittelytoiminto toimisi, työrivit on lajiteltava nimiketunnuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="d9d9c-136">Jos rivejä, joilla on samat nimikkeet, ei ole järjestetty yksitellen, niitä ei ryhmitellä.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="d9d9c-137">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="d9d9c-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="d9d9c-138">Luo keräystyö</span><span class="sxs-lookup"><span data-stu-id="d9d9c-138">Create picking work</span></span>

<span data-ttu-id="d9d9c-139">Ennen kuin voit määrittää keräilyrivin ryhmittelyn, sinun on luotava joitakin tukikelpoisia lähteviä töitä.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="d9d9c-140">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="d9d9c-141">Luo uusi myyntitilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="d9d9c-142">Valitse **Asiakastili** -kentässä mikä tahansa asiakas.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="d9d9c-143">Valitse **Yleinen** -pikavälilehden **Varasto** -kentässä **51**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="d9d9c-144">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-144">Then select **OK**.</span></span>
5. <span data-ttu-id="d9d9c-145">Lisää seuraavat kuusi riviä **myyntitilausriveille** :</span><span class="sxs-lookup"><span data-stu-id="d9d9c-145">Under **Sales order lines** , add the following six lines:</span></span>

    - <span data-ttu-id="d9d9c-146">Valitse **Rivi 1:** **Nimikkeen numero** -kentässä **M9200**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="d9d9c-147">Kirjoita **Määrä** -kenttään **3**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="d9d9c-148">Valitse **Rivi 2:** **Nimikkeen numero** -kentässä **M9201**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="d9d9c-149">Kirjoita **Määrä** -kenttään **3**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="d9d9c-150">Valitse **Rivi 3:** **Nimikkeen numero** -kentässä **M9202**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="d9d9c-151">Kirjoita **Määrä** -kenttään **2**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="d9d9c-152">Valitse **Rivi 4:** **Nimikkeen numero** -kentässä **M9200**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="d9d9c-153">Kirjoita **Määrä** -kenttään **1**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="d9d9c-154">Valitse **Rivi 5:** **Nimikkeen numero** -kentässä **M9200**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="d9d9c-155">Kirjoita **Määrä** -kenttään **3**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="d9d9c-156">Valitse **Rivi 6:** **Nimikkeen numero** -kentässä **M9202**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="d9d9c-157">Kirjoita **Määrä** -kenttään **7**.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="d9d9c-158">Tässä on yhteenveto kunkin nimikkeen kokonaismääristä:</span><span class="sxs-lookup"><span data-stu-id="d9d9c-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="d9d9c-159">**Nimike M9200:** 7 kukin</span><span class="sxs-lookup"><span data-stu-id="d9d9c-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="d9d9c-160">**Nimike M9201:** 3 kukin</span><span class="sxs-lookup"><span data-stu-id="d9d9c-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="d9d9c-161">**Nimike M9202:** 9 kukin</span><span class="sxs-lookup"><span data-stu-id="d9d9c-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="d9d9c-162">Ennen kuin vapautat tilaukset varastoon, varmista, että poiminnan sijainneissa on tarpeeksi varastoa kaikkien tilausten kaikille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="d9d9c-163">Tarkista **Toimipaikkadirektiivin** asetus ja määritä, mitä keräilysijainteja myyntitilausten keräilyyn käytetään.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="d9d9c-164">Varaa varasto ja vapauta se varastoon.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="d9d9c-165">Työtunnus, jossa on kuusi riviä on luotu.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="d9d9c-166">Rivit lajitellaan nimiketunnuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="d9d9c-167">Suorita mobiililaitteen virtaus</span><span class="sxs-lookup"><span data-stu-id="d9d9c-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="d9d9c-168">Valitse mobiililaitteessa valikko, joka sisältää uuden mobiililaitteen valikkovaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="d9d9c-169">Valitse **Myynnin poiminta – ryhmärivi** -valikkonimike ja aloita poiminta.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="d9d9c-170">Kun olet valinnut valikon ja kirjoitat työn tunnuksen, näet poimintavaiheen, jossa kaikki nimikkeen M9200 poimintarivit ryhmitellään.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="d9d9c-171">Saat ohjeen, jossa voit valita 7 kutakin nimikettä M9200.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="d9d9c-172">Vahvista ensimmäinen vaihe.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="d9d9c-173">Siirry keskeneräisen työn asiakasnäyttöön ja huomaa, että kohteen M9200 kaikki kolme poimintariviä suljettiin samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="d9d9c-174">Työlinja 4 on esitetty.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="d9d9c-175">Vahvista ensimmäinen vaihe.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-175">Confirm the pick step.</span></span>

    <span data-ttu-id="d9d9c-176">Matkaviestimen viimeinen poimintavaihe kokoaa yhteen kaksi viimeistä poimintariviä työtilauksesta.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="d9d9c-177">Täytä poiminnan vaihe 9 jokaiselle nimikkeelle M9202.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="d9d9c-178">Vahvista laittovaihe ja mahdolliset muut poiminta-/laittovaiheet töiden suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="d9d9c-179">Työrivit voidaan ryhmitellä vain, jos ne ovat järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="d9d9c-180">Seuraavaa toimintoa ei tueta:</span><span class="sxs-lookup"><span data-stu-id="d9d9c-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="d9d9c-181">Todellisen painon nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-181">Catch-weight items.</span></span> <span data-ttu-id="d9d9c-182">Jos työssä on mitään todellisen painon nimikkeitä, näyttöön tulee virhesanoma, ennen kuin aloitat poiminnan.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="d9d9c-183">Kappaleen keräily.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-183">Piece picking.</span></span>
>    - <span data-ttu-id="d9d9c-184">Työrivit, joilla on keskeneräinen täydennystyö.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="d9d9c-185">Ylikeräily.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-185">Over-picking.</span></span>
>    - <span data-ttu-id="d9d9c-186">Nimikkeen uudelleenkohdistaminen lyhyen keräilyn avulla</span><span class="sxs-lookup"><span data-stu-id="d9d9c-186">Short picking with item reallocation</span></span>
