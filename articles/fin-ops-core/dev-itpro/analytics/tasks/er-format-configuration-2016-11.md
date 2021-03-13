---
title: ER Muotomääritysten luominen (marraskuu 2016)
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) muotomäärityksen luontia.
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9404d1e242c83d2103d1f24c42589c33b9f57f02
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092247"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="a0f1d-103">ER Muotomääritysten luominen (marraskuu 2016)</span><span class="sxs-lookup"><span data-stu-id="a0f1d-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0f1d-104">Tässä aiheessa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda muotokonfiguraation sähköiselle raportoinnille (ER).</span><span class="sxs-lookup"><span data-stu-id="a0f1d-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="a0f1d-105">Tämä muotokonfiguraatio määrittää maksujen käsittelyssä käytettävien sähköisten asiakirjojen muodon.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="a0f1d-106">Tässä esimerkissä luodaan muotokonfiguraatio Litware, Inc. -malliyritykselle. Voit suorittaa nämä vaiheet suoritettuasi ensin Mallin yhdistäminen valittuihin tietolähteisiin -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="a0f1d-107">Uuden muotokonfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="a0f1d-107">Create a new format configuration</span></span>
1. <span data-ttu-id="a0f1d-108">Valitse **Organisaation hallinto > Työtilat > Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="a0f1d-109">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="a0f1d-110">Valitse puussa **Maksut (yksinkertaistettu malli)**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="a0f1d-111">Avaa valintaikkuna valitsemalla **Luo konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="a0f1d-112">Jos **Luo konfigurointi** ei ole näkyvissä, suunnittelutila on otettava käyttöön **Sähköisen raportoinnin parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="a0f1d-113">Anna **Uusi**-kentässä **Muoto perustuu tietomalliin PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="a0f1d-114">Anna **Nimi**-kentässä **BACS (Iso-Britannia, kuvitteellinen)**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="a0f1d-115">Anna **Kuvaus**-kenttään **BACS - toimittajan maksumuoto (Iso-Britannia, kuvitteellinen)**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="a0f1d-116">Aktiivinen konfiguraation lähde syötetään tässä automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="a0f1d-117">Tämä lähde voi ylläpitää tätä konfiguraatiota.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="a0f1d-118">Muut lähteet voivat käyttää tätä konfiguraatiota, mutta eivät ylläpitää sitä.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="a0f1d-119">Voit määrittää sähköiselle asiakirjalle tietyn muodon.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="a0f1d-120">Jätä kenttä tyhjäksi, jos haluat valita muodon suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="a0f1d-121">Anna tai valitse **Tietomallin määritelmä** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="a0f1d-122">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-122">Click **Create configuration**.</span></span> <span data-ttu-id="a0f1d-123">Uusi konfiguraatio on luotu.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-123">A new configuration has been created.</span></span> <span data-ttu-id="a0f1d-124">Rakenteen muodon voi tallentaa luonnoksena sähköisten asiakirjojen hallintaa varten.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="a0f1d-125">Sähköisen asiakirjan muodon suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="a0f1d-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="a0f1d-126">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-126">Click **Designer**.</span></span>
2. <span data-ttu-id="a0f1d-127">Avaa valintaikkuna valitsemalla **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="a0f1d-128">Valitse puussa **Common\File**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="a0f1d-129">Anna **Nimi**-kentässä **Xml**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="a0f1d-130">Anna **Koodaus**-kentässä **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="a0f1d-131">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-131">Click **OK**.</span></span>
7. <span data-ttu-id="a0f1d-132">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-132">Click **Add**.</span></span>
8. <span data-ttu-id="a0f1d-133">Valitse puussa **XML\Elementti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="a0f1d-134">Kirjoita **Nimi**-kenttään **Viesti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="a0f1d-135">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-135">Click **OK**.</span></span>
11. <span data-ttu-id="a0f1d-136">Valitse puussa **Xml\Sanoma**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="a0f1d-137">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="a0f1d-138">Kirjoita **Nimi**-kenttään **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="a0f1d-139">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-139">Click **OK**.</span></span>
15. <span data-ttu-id="a0f1d-140">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="a0f1d-141">Kirjoita Nimi-kenttään **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="a0f1d-142">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-142">Click **OK**.</span></span>
18. <span data-ttu-id="a0f1d-143">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="a0f1d-144">Kirjoita **Nimi**-kenttään **Maksut**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="a0f1d-145">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-145">Click **OK**.</span></span>
21. <span data-ttu-id="a0f1d-146">Valitse puussa **Xml\Sanoma\Maksut**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="a0f1d-147">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="a0f1d-148">Kirjoita **Nimi**-kenttään **Nimike**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="a0f1d-149">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-149">Click **OK**.</span></span>
25. <span data-ttu-id="a0f1d-150">Valitse puussa **Xml\Sanoma\Maksut\Nimike**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="a0f1d-151">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-151">Click **Add**.</span></span>
27. <span data-ttu-id="a0f1d-152">Valitse puussa **XML\Määrite**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="a0f1d-153">Kirjoita Nimi-kenttään **Tunnus**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="a0f1d-154">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-154">Click **OK**.</span></span>
30. <span data-ttu-id="a0f1d-155">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-155">Click **Add**.</span></span>
31. <span data-ttu-id="a0f1d-156">Valitse puussa **XML\Elementti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="a0f1d-157">Kirjoita Nimi-kenttään **Toimittaja**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="a0f1d-158">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-158">Click **OK**.</span></span>
34. <span data-ttu-id="a0f1d-159">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="a0f1d-160">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="a0f1d-161">Kirjoita Nimi-kenttään **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="a0f1d-162">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-162">Click **OK**.</span></span>
38. <span data-ttu-id="a0f1d-163">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="a0f1d-164">Kirjoita **Nimi**-kenttään **Pankki**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="a0f1d-165">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-165">Click **OK**.</span></span>
41. <span data-ttu-id="a0f1d-166">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="a0f1d-167">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="a0f1d-168">Kirjoita **Nimi**-kenttään **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="a0f1d-169">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-169">Click **OK**.</span></span>
45. <span data-ttu-id="a0f1d-170">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="a0f1d-171">Kirjoita **Nimi**-kenttään **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="a0f1d-172">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-172">Click **OK**.</span></span>
48. <span data-ttu-id="a0f1d-173">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="a0f1d-174">Valitse **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-174">Click **Copy**.</span></span>
50. <span data-ttu-id="a0f1d-175">Valitse puussa **Xml\Sanoma\Maksut\Nimike**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="a0f1d-176">Valitse **Liitä**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-176">Click **Paste**.</span></span>
52. <span data-ttu-id="a0f1d-177">Kirjoita **Nimi**-kenttään **Maksaja**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="a0f1d-178">Valitse puussa **Xml\Sanoma\Maksut\Nimike**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="a0f1d-179">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="a0f1d-180">Kirjoita **Nimi**-kenttään **Valuutta**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="a0f1d-181">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-181">Click **OK**.</span></span>
57. <span data-ttu-id="a0f1d-182">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="a0f1d-183">Kirjoita **Nimi**-kenttään **Kuvaus**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="a0f1d-184">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-184">Click **OK**.</span></span>
60. <span data-ttu-id="a0f1d-185">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="a0f1d-186">Kirjoita Nimi-kenttään **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="a0f1d-187">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-187">Click **OK**.</span></span>
63. <span data-ttu-id="a0f1d-188">Valitse **Lisää elementti**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="a0f1d-189">Kirjoita Nimi-kenttään **Summa**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="a0f1d-190">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="a0f1d-191">Muotokomponenttien valmisteleminen tietomallielementtien yhdistämistä varten</span><span class="sxs-lookup"><span data-stu-id="a0f1d-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="a0f1d-192">Valitse puussa **Xml\Sanoma\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="a0f1d-193">Avaa valintaikkuna valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="a0f1d-194">Valitse puussa **Teksti\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="a0f1d-195">Kirjoita **Muoto**-kenttään **vvvv-KK-pp**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="a0f1d-196">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-196">Click **OK**.</span></span>
6. <span data-ttu-id="a0f1d-197">Valitse puussa **Xml\Sanoma\Maksut\Nimike\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="a0f1d-198">Valitse **Lisää DateTime**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="a0f1d-199">Kirjoita **Muoto**-kenttään **vvvv-KK-pp**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="a0f1d-200">Valitse **DateTime**-tyyppikentässä **Päivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="a0f1d-201">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-201">Click **OK**.</span></span>
11. <span data-ttu-id="a0f1d-202">Valitse puussa **Xml\Sanoma\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="a0f1d-203">Avaa valintaikkuna valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="a0f1d-204">Valitse puussa **Teksti\Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="a0f1d-205">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-205">Click **OK**.</span></span>
15. <span data-ttu-id="a0f1d-206">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja\Nimi**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="a0f1d-207">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-207">Click **Add String**.</span></span>
17. <span data-ttu-id="a0f1d-208">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-208">Click **OK**.</span></span>
18. <span data-ttu-id="a0f1d-209">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="a0f1d-210">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-210">Click **Add String**.</span></span>
20. <span data-ttu-id="a0f1d-211">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-211">Click **OK**.</span></span>
21. <span data-ttu-id="a0f1d-212">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="a0f1d-213">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-213">Click **Add String**.</span></span>
23. <span data-ttu-id="a0f1d-214">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-214">Click **OK**.</span></span>
24. <span data-ttu-id="a0f1d-215">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Maksaja\Nimi**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="a0f1d-216">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-216">Click **Add String**.</span></span>
26. <span data-ttu-id="a0f1d-217">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-217">Click **OK**.</span></span>
27. <span data-ttu-id="a0f1d-218">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Maksaja\Pankki\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="a0f1d-219">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-219">Click **Add String**.</span></span>
29. <span data-ttu-id="a0f1d-220">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-220">Click **OK**.</span></span>
30. <span data-ttu-id="a0f1d-221">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Maksaja\Pankki\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="a0f1d-222">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-222">Click **Add String**.</span></span>
32. <span data-ttu-id="a0f1d-223">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-223">Click **OK**.</span></span>
33. <span data-ttu-id="a0f1d-224">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Valuutta**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="a0f1d-225">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-225">Click **Add String**.</span></span>
35. <span data-ttu-id="a0f1d-226">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-226">Click **OK**.</span></span>
36. <span data-ttu-id="a0f1d-227">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Kuvaus**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="a0f1d-228">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-228">Click **Add String**.</span></span>
38. <span data-ttu-id="a0f1d-229">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-229">Click **OK**.</span></span>
39. <span data-ttu-id="a0f1d-230">Valitse puussa **Xml\Sanoma\Maksut\Nimike\Summa**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="a0f1d-231">Valitse **Lisää merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-231">Click **Add String**.</span></span>
41. <span data-ttu-id="a0f1d-232">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-232">Click **OK**.</span></span>
42. <span data-ttu-id="a0f1d-233">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-233">Click **Save**.</span></span>
43. <span data-ttu-id="a0f1d-234">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a0f1d-234">Close the page.</span></span>

