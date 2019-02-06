--- 
title: "ER Muotomääritysten luominen (marraskuu 2016)"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda muotokonfiguraation sähköiselle raportoinnille (ER)."
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f004451a260b5be6c15c3975cd9e63ba9c1a7a2e
ms.openlocfilehash: 6fa5023a29c95ab9f10d8aacd51edc1a06c3c152
ms.contentlocale: fi-fi
ms.lasthandoff: 02/06/2019

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="a2dca-103">ER Muotomääritysten luominen (marraskuu 2016)</span><span class="sxs-lookup"><span data-stu-id="a2dca-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a2dca-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda muotokonfiguraation sähköiselle raportoinnille (ER).</span><span class="sxs-lookup"><span data-stu-id="a2dca-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="a2dca-105">Tämä muotokonfiguraatio määrittää maksujen käsittelyssä käytettävien sähköisten asiakirjojen muodon.</span><span class="sxs-lookup"><span data-stu-id="a2dca-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="a2dca-106">Tässä esimerkissä luodaan muotokonfiguraatio Litware, Inc. -malliyritykselle. Voit suorittaa nämä vaiheet suoritettuasi ensin Mallin yhdistäminen valittuihin tietolähteisiin -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="a2dca-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="a2dca-107">Uuden muotokonfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="a2dca-107">Create a new format configuration</span></span>
1. <span data-ttu-id="a2dca-108">Valitse **Organisaation hallinto > Työtilat > Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="a2dca-109">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="a2dca-110">Valitse puussa **Maksut (yksinkertaistettu malli)**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="a2dca-111">Avaa valintaikkuna valitsemalla **Luo konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="a2dca-112">Jos **Luo konfigurointi** ei ole näkyvissä, suunnittelutila on otettava käyttöön **Sähköisen raportoinnin parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="a2dca-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="a2dca-113">Anna **Uusi**-kentässä **Muoto perustuu tietomalliin PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="a2dca-114">Anna **Nimi**-kentässä **BACS (Iso-Britannia, kuvitteellinen)**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="a2dca-115">Anna **Kuvaus**-kenttään **BACS - toimittajan maksumuoto (Iso-Britannia, kuvitteellinen)**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="a2dca-116">Aktiivinen konfiguraation lähde syötetään tässä automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="a2dca-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="a2dca-117">Tämä lähde voi ylläpitää tätä konfiguraatiota.</span><span class="sxs-lookup"><span data-stu-id="a2dca-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="a2dca-118">Muut lähteet voivat käyttää tätä konfiguraatiota, mutta eivät ylläpitää sitä.</span><span class="sxs-lookup"><span data-stu-id="a2dca-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="a2dca-119">Voit määrittää sähköiselle asiakirjalle tietyn muodon.</span><span class="sxs-lookup"><span data-stu-id="a2dca-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="a2dca-120">Jätä kenttä tyhjäksi, jos haluat valita muodon suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="a2dca-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="a2dca-121">Anna tai valitse **Tietomallin määritelmä** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="a2dca-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="a2dca-122">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-122">Click **Create configuration**.</span></span> <span data-ttu-id="a2dca-123">Uusi konfiguraatio on luotu.</span><span class="sxs-lookup"><span data-stu-id="a2dca-123">A new configuration has been created.</span></span> <span data-ttu-id="a2dca-124">Rakenteen muodon voi tallentaa luonnoksena sähköisten asiakirjojen hallintaa varten.</span><span class="sxs-lookup"><span data-stu-id="a2dca-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

 > [!NOTE]
 > <span data-ttu-id="a2dca-125">Jos **Luo konfigurointi** ei ole näkyvissä, suunnittelutila on otettava käyttöön **Sähköisen raportoinnin parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="a2dca-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="a2dca-126">Sähköisen asiakirjan muodon suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="a2dca-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="a2dca-127">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-127">Click **Designer**.</span></span>
2. <span data-ttu-id="a2dca-128">Avaa valintaikkuna valitsemalla **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="a2dca-129">Valitse puussa **Common\File**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="a2dca-130">Anna **Nimi**-kentässä **Xml**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="a2dca-131">Anna **Koodaus**-kentässä **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="a2dca-132">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-132">Click **OK**.</span></span>
7. <span data-ttu-id="a2dca-133">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-133">Click **Add**.</span></span>
8. <span data-ttu-id="a2dca-134">Valitse puussa **XML\Elementti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="a2dca-135">Kirjoita **Nimi**-kenttään **Viesti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="a2dca-136">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-136">Click **OK**.</span></span>
11. <span data-ttu-id="a2dca-137">Valitse puussa **Xml\Sanoma**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="a2dca-138">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="a2dca-139">Kirjoita **Nimi**-kenttään **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="a2dca-140">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-140">Click **OK**.</span></span>
15. <span data-ttu-id="a2dca-141">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="a2dca-142">Kirjoita Nimi-kenttään **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="a2dca-143">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-143">Click **OK**.</span></span>
18. <span data-ttu-id="a2dca-144">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="a2dca-145">Kirjoita **Nimi**-kenttään **Maksut**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="a2dca-146">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-146">Click **OK**.</span></span>
21. <span data-ttu-id="a2dca-147">Valitse puussa **Xml\Sanoma\Maksut**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="a2dca-148">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="a2dca-149">Kirjoita **Nimi**-kenttään **Nimike**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="a2dca-150">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-150">Click **OK**.</span></span>
25. <span data-ttu-id="a2dca-151">Valitse puussa **Xml\Sanoma\Maksut\Nimike**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="a2dca-152">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-152">Click **Add**.</span></span>
27. <span data-ttu-id="a2dca-153">Valitse puussa **XML\Määrite**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="a2dca-154">Kirjoita Nimi-kenttään **Tunnus**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="a2dca-155">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-155">Click **OK**.</span></span>
30. <span data-ttu-id="a2dca-156">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-156">Click **Add**.</span></span>
31. <span data-ttu-id="a2dca-157">Valitse puussa **XML\Elementti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="a2dca-158">Kirjoita Nimi-kenttään **Toimittaja**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="a2dca-159">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-159">Click **OK**.</span></span>
34. <span data-ttu-id="a2dca-160">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="a2dca-161">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="a2dca-162">Kirjoita Nimi-kenttään **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="a2dca-163">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-163">Click **OK**.</span></span>
38. <span data-ttu-id="a2dca-164">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="a2dca-165">Kirjoita **Nimi**-kenttään **Pankki**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="a2dca-166">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-166">Click **OK**.</span></span>
41. <span data-ttu-id="a2dca-167">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="a2dca-168">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="a2dca-169">Kirjoita **Nimi**-kenttään **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="a2dca-170">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-170">Click **OK**.</span></span>
45. <span data-ttu-id="a2dca-171">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="a2dca-172">Kirjoita **Nimi**-kenttään **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="a2dca-173">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-173">Click **OK**.</span></span>
48. <span data-ttu-id="a2dca-174">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="a2dca-175">Valitse **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-175">Click **Copy**.</span></span>
50. <span data-ttu-id="a2dca-176">Valitse puussa **Xml\Sanoma\Maksut\Nimike**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="a2dca-177">Valitse **Liitä**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-177">Click **Paste**.</span></span>
52. <span data-ttu-id="a2dca-178">Kirjoita **Nimi**-kenttään **Maksaja**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="a2dca-179">Valitse puussa **Xml\Sanoma\Maksut\Nimike**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="a2dca-180">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="a2dca-181">Kirjoita **Nimi**-kenttään **Valuutta**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="a2dca-182">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-182">Click **OK**.</span></span>
57. <span data-ttu-id="a2dca-183">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="a2dca-184">Kirjoita **Nimi**-kenttään **Kuvaus**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="a2dca-185">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-185">Click **OK**.</span></span>
60. <span data-ttu-id="a2dca-186">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="a2dca-187">Kirjoita Nimi-kenttään **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="a2dca-188">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-188">Click **OK**.</span></span>
63. <span data-ttu-id="a2dca-189">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="a2dca-190">Kirjoita Nimi-kenttään **Summa**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="a2dca-191">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="a2dca-192">Muotokomponenttien valmisteleminen tietomallielementtien yhdistämistä varten</span><span class="sxs-lookup"><span data-stu-id="a2dca-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="a2dca-193">Valitse puussa **Xml\Sanoma\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="a2dca-194">Avaa valintaikkuna valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="a2dca-195">Valitse puussa **Teksti\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="a2dca-196">Kirjoita **Muoto**-kenttään **vvvv-KK-pp**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="a2dca-197">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-197">Click **OK**.</span></span>
6. <span data-ttu-id="a2dca-198">Valitse puussa **Xml\Sanoma\Maksut\Nimike\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="a2dca-199">Valitse **Lisää DateTime**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="a2dca-200">Kirjoita **Muoto**-kenttään **vvvv-KK-pp**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="a2dca-201">Valitse **DateTime**-tyyppikentässä **Päivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="a2dca-202">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-202">Click **OK**.</span></span>
11. <span data-ttu-id="a2dca-203">Valitse puussa **Xml\Sanoma\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="a2dca-204">Avaa valintaikkuna valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="a2dca-205">Valitse puussa **Teksti\Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="a2dca-206">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-206">Click **OK**.</span></span>
15. <span data-ttu-id="a2dca-207">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja\Nimi**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="a2dca-208">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-208">Click **Add String**.</span></span>
17. <span data-ttu-id="a2dca-209">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-209">Click **OK**.</span></span>
18. <span data-ttu-id="a2dca-210">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="a2dca-211">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-211">Click **Add String**.</span></span>
20. <span data-ttu-id="a2dca-212">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-212">Click **OK**.</span></span>
21. <span data-ttu-id="a2dca-213">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="a2dca-214">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-214">Click **Add String**.</span></span>
23. <span data-ttu-id="a2dca-215">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-215">Click **OK**.</span></span>
24. <span data-ttu-id="a2dca-216">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Maksaja\Nimi**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="a2dca-217">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-217">Click **Add String**.</span></span>
26. <span data-ttu-id="a2dca-218">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-218">Click **OK**.</span></span>
27. <span data-ttu-id="a2dca-219">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Maksaja\Pankki\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="a2dca-220">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-220">Click **Add String**.</span></span>
29. <span data-ttu-id="a2dca-221">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-221">Click **OK**.</span></span>
30. <span data-ttu-id="a2dca-222">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Maksaja\Pankki\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="a2dca-223">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-223">Click **Add String**.</span></span>
32. <span data-ttu-id="a2dca-224">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-224">Click **OK**.</span></span>
33. <span data-ttu-id="a2dca-225">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Valuutta**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="a2dca-226">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-226">Click **Add String**.</span></span>
35. <span data-ttu-id="a2dca-227">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-227">Click **OK**.</span></span>
36. <span data-ttu-id="a2dca-228">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Kuvaus**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="a2dca-229">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-229">Click **Add String**.</span></span>
38. <span data-ttu-id="a2dca-230">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-230">Click **OK**.</span></span>
39. <span data-ttu-id="a2dca-231">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Summa**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="a2dca-232">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-232">Click **Add String**.</span></span>
41. <span data-ttu-id="a2dca-233">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-233">Click **OK**.</span></span>
42. <span data-ttu-id="a2dca-234">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a2dca-234">Click **Save**.</span></span>
43. <span data-ttu-id="a2dca-235">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a2dca-235">Close the page.</span></span>


