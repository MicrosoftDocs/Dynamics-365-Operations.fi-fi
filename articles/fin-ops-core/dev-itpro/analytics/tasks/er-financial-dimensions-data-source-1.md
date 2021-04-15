---
title: ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 1 – Tietomallin suunnittelu)
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) mallin määrittämistä käyttämään taloushallinnon dimensioita ER-raporttien tietolähteenä. (Osa 1)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92b44532dfae70f03d6686ca1d2f8b6f74345ee6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752457"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="09244-104">ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 1 – Tietomallin suunnittelu)</span><span class="sxs-lookup"><span data-stu-id="09244-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09244-105">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvoja tai sähköisen raportoinnin kehittäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.</span><span class="sxs-lookup"><span data-stu-id="09244-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="09244-106">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="09244-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="09244-107">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="09244-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="09244-108">Luo uusi tietomalli</span><span class="sxs-lookup"><span data-stu-id="09244-108">Create a new data model</span></span>
1. <span data-ttu-id="09244-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="09244-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="09244-110">Varmista, että Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="09244-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="09244-111">-lähde on käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="09244-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="09244-112">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="09244-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="09244-113">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="09244-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="09244-114">Syötä Nimi-kenttään "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="09244-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="09244-115">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="09244-115">Click Create configuration.</span></span>
6. <span data-ttu-id="09244-116">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="09244-116">Click Designer.</span></span>
7. <span data-ttu-id="09244-117">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="09244-118">Kirjoita Nimi-kenttään "Kirjaus".</span><span class="sxs-lookup"><span data-stu-id="09244-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="09244-119">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-119">Click Add.</span></span>
10. <span data-ttu-id="09244-120">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="09244-121">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="09244-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="09244-122">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-122">Click Add.</span></span>
    * <span data-ttu-id="09244-123">Malliin ei lisätä uutta tietueluetteloa.</span><span class="sxs-lookup"><span data-stu-id="09244-123">We will add to our model a new record list.</span></span> <span data-ttu-id="09244-124">Tässä luettelossa näytetään valittujen taloushallinnon dimensioiden asetukset (kaikille tätä mallia tietolähteenä käyttäville ER-raporteille).</span><span class="sxs-lookup"><span data-stu-id="09244-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="09244-125">Jokainen taloushallinnon dimensio esitetään tässä luettelossa tietueena, jonka asianmukaiset kentät edustavat dimension asetuksia.</span><span class="sxs-lookup"><span data-stu-id="09244-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="09244-126">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="09244-127">Kirjoita Nimi-kenttään "Dimensioiden asetus".</span><span class="sxs-lookup"><span data-stu-id="09244-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="09244-128">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="09244-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="09244-129">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-129">Click Add.</span></span>
17. <span data-ttu-id="09244-130">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="09244-131">Kirjoita Nimi-kenttään "Koodi".</span><span class="sxs-lookup"><span data-stu-id="09244-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="09244-132">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="09244-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="09244-133">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-133">Click Add.</span></span>
21. <span data-ttu-id="09244-134">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="09244-135">Syötä Nimi-kenttään Nimi.</span><span class="sxs-lookup"><span data-stu-id="09244-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="09244-136">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-136">Click Add.</span></span>
24. <span data-ttu-id="09244-137">Valitse puussa "Entry".</span><span class="sxs-lookup"><span data-stu-id="09244-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="09244-138">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="09244-139">Kirjoita Nimi-kenttään "Kirjauskansio".</span><span class="sxs-lookup"><span data-stu-id="09244-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="09244-140">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="09244-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="09244-141">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-141">Click Add.</span></span>
29. <span data-ttu-id="09244-142">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="09244-143">Kirjoita Nimi-kenttään "Erä".</span><span class="sxs-lookup"><span data-stu-id="09244-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="09244-144">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="09244-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="09244-145">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-145">Click Add.</span></span>
33. <span data-ttu-id="09244-146">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="09244-147">Kirjoita Nimi-kenttään "Tapahtuma".</span><span class="sxs-lookup"><span data-stu-id="09244-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="09244-148">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="09244-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="09244-149">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-149">Click Add.</span></span>
37. <span data-ttu-id="09244-150">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="09244-151">Kirjoita Nimi-kenttään "Päivämäärä".</span><span class="sxs-lookup"><span data-stu-id="09244-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="09244-152">Valitse Nimiketyyppi-kentässä Päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="09244-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="09244-153">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-153">Click Add.</span></span>
41. <span data-ttu-id="09244-154">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="09244-155">Kirjoita Nimi -kenttään "Veloitus".</span><span class="sxs-lookup"><span data-stu-id="09244-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="09244-156">Valitse Nimiketyyppi-kentässä Reaaliluku.</span><span class="sxs-lookup"><span data-stu-id="09244-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="09244-157">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-157">Click Add.</span></span>
45. <span data-ttu-id="09244-158">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="09244-159">Syötä Nimi-kenttään "Hyvitys".</span><span class="sxs-lookup"><span data-stu-id="09244-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="09244-160">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-160">Click Add.</span></span>
48. <span data-ttu-id="09244-161">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="09244-162">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="09244-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="09244-163">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="09244-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="09244-164">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-164">Click Add.</span></span>
52. <span data-ttu-id="09244-165">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="09244-166">Kirjoita Nimi-kenttään "Tosite".</span><span class="sxs-lookup"><span data-stu-id="09244-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="09244-167">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-167">Click Add.</span></span>
55. <span data-ttu-id="09244-168">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="09244-169">Kirjoita Nimi-kenttään "Dimensioiden tiedot".</span><span class="sxs-lookup"><span data-stu-id="09244-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="09244-170">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="09244-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="09244-171">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-171">Click Add.</span></span>
    * <span data-ttu-id="09244-172">Malliin on lisätty uusi tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="09244-172">We added to our model a new record list.</span></span> <span data-ttu-id="09244-173">Tässä luettelossa näytetään valittujen taloushallinnon dimensioiden arvot (kaikille tätä mallia tietolähteenä käyttäville ER-raporteille).</span><span class="sxs-lookup"><span data-stu-id="09244-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="09244-174">Jokainen taloushallinnon dimensio esitetään tässä luettelossa tietueena, jonka asianmukaiset kentät edustavat dimension arvoja.</span><span class="sxs-lookup"><span data-stu-id="09244-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="09244-175">Dimension nimi esitetään myös tässä tietueessa käytettävänä kenttänä valintatoimintoa varten tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="09244-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="09244-176">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="09244-177">Kirjoita Nimi-kenttään "Koodi".</span><span class="sxs-lookup"><span data-stu-id="09244-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="09244-178">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="09244-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="09244-179">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-179">Click Add.</span></span>
63. <span data-ttu-id="09244-180">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="09244-181">Syötä Nimi-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="09244-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="09244-182">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-182">Click Add.</span></span>
66. <span data-ttu-id="09244-183">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="09244-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="09244-184">Syötä Nimi-kenttään Nimi.</span><span class="sxs-lookup"><span data-stu-id="09244-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="09244-185">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="09244-185">Click Add.</span></span>
69. <span data-ttu-id="09244-186">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="09244-186">Click Save.</span></span>
70. <span data-ttu-id="09244-187">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="09244-187">Close the page.</span></span>

![ER-tietomallin suunnittelutoiminnon sivu](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]