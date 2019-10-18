---
title: ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 1 – Tietomallin suunnittelu)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvoja tai sähköisen raportoinnin kehittäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca295d651838f34106c9b91a53efc1f4faad4e4a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182482"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1-design-data-model"></a><span data-ttu-id="fc5ac-103">ER Taloushallinnon dimensioiden käyttö tietolähteenä (osa 1: tietomallin suunnittelu)</span><span class="sxs-lookup"><span data-stu-id="fc5ac-103">ER Use financial dimensions as a data source (Part 1: Design data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc5ac-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvoja tai sähköisen raportoinnin kehittäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="fc5ac-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="fc5ac-106">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="fc5ac-107">Luo uusi tietomalli</span><span class="sxs-lookup"><span data-stu-id="fc5ac-107">Create a new data model</span></span>
1. <span data-ttu-id="fc5ac-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="fc5ac-109">Varmista, että Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="fc5ac-110">-lähde on käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="fc5ac-111">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="fc5ac-112">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="fc5ac-113">Syötä Nimi-kenttään "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="fc5ac-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="fc5ac-114">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-114">Click Create configuration.</span></span>
6. <span data-ttu-id="fc5ac-115">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-115">Click Designer.</span></span>
7. <span data-ttu-id="fc5ac-116">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="fc5ac-117">Kirjoita Nimi-kenttään "Kirjaus".</span><span class="sxs-lookup"><span data-stu-id="fc5ac-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="fc5ac-118">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-118">Click Add.</span></span>
10. <span data-ttu-id="fc5ac-119">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="fc5ac-120">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="fc5ac-121">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-121">Click Add.</span></span>
    * <span data-ttu-id="fc5ac-122">Malliin ei lisätä uutta tietueluetteloa.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-122">We will add to our model a new record list.</span></span> <span data-ttu-id="fc5ac-123">Tässä luettelossa näytetään valittujen taloushallinnon dimensioiden asetukset (kaikille tätä mallia tietolähteenä käyttäville ER-raporteille).</span><span class="sxs-lookup"><span data-stu-id="fc5ac-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="fc5ac-124">Jokainen taloushallinnon dimensio esitetään tässä luettelossa tietueena, jonka asianmukaiset kentät edustavat dimension asetuksia.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="fc5ac-125">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="fc5ac-126">Kirjoita Nimi-kenttään "Dimensioiden asetus".</span><span class="sxs-lookup"><span data-stu-id="fc5ac-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="fc5ac-127">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="fc5ac-128">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-128">Click Add.</span></span>
17. <span data-ttu-id="fc5ac-129">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="fc5ac-130">Kirjoita Nimi-kenttään "Koodi".</span><span class="sxs-lookup"><span data-stu-id="fc5ac-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="fc5ac-131">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="fc5ac-132">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-132">Click Add.</span></span>
21. <span data-ttu-id="fc5ac-133">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="fc5ac-134">Syötä Nimi-kenttään Nimi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="fc5ac-135">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-135">Click Add.</span></span>
24. <span data-ttu-id="fc5ac-136">Valitse puussa "Entry".</span><span class="sxs-lookup"><span data-stu-id="fc5ac-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="fc5ac-137">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="fc5ac-138">Kirjoita Nimi-kenttään "Kirjauskansio".</span><span class="sxs-lookup"><span data-stu-id="fc5ac-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="fc5ac-139">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="fc5ac-140">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-140">Click Add.</span></span>
29. <span data-ttu-id="fc5ac-141">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="fc5ac-142">Kirjoita Nimi-kenttään "Erä".</span><span class="sxs-lookup"><span data-stu-id="fc5ac-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="fc5ac-143">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="fc5ac-144">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-144">Click Add.</span></span>
33. <span data-ttu-id="fc5ac-145">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="fc5ac-146">Kirjoita Nimi-kenttään "Tapahtuma".</span><span class="sxs-lookup"><span data-stu-id="fc5ac-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="fc5ac-147">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="fc5ac-148">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-148">Click Add.</span></span>
37. <span data-ttu-id="fc5ac-149">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="fc5ac-150">Kirjoita Nimi-kenttään "Päivämäärä".</span><span class="sxs-lookup"><span data-stu-id="fc5ac-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="fc5ac-151">Valitse Nimiketyyppi-kentässä Päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="fc5ac-152">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-152">Click Add.</span></span>
41. <span data-ttu-id="fc5ac-153">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="fc5ac-154">Kirjoita Nimi -kenttään "Veloitus".</span><span class="sxs-lookup"><span data-stu-id="fc5ac-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="fc5ac-155">Valitse Nimiketyyppi-kentässä Reaaliluku.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="fc5ac-156">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-156">Click Add.</span></span>
45. <span data-ttu-id="fc5ac-157">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="fc5ac-158">Syötä Nimi-kenttään "Hyvitys".</span><span class="sxs-lookup"><span data-stu-id="fc5ac-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="fc5ac-159">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-159">Click Add.</span></span>
48. <span data-ttu-id="fc5ac-160">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="fc5ac-161">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="fc5ac-162">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="fc5ac-163">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-163">Click Add.</span></span>
52. <span data-ttu-id="fc5ac-164">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="fc5ac-165">Kirjoita Nimi-kenttään "Tosite".</span><span class="sxs-lookup"><span data-stu-id="fc5ac-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="fc5ac-166">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-166">Click Add.</span></span>
55. <span data-ttu-id="fc5ac-167">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="fc5ac-168">Kirjoita Nimi-kenttään "Dimensioiden tiedot".</span><span class="sxs-lookup"><span data-stu-id="fc5ac-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="fc5ac-169">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="fc5ac-170">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-170">Click Add.</span></span>
    * <span data-ttu-id="fc5ac-171">Malliin on lisätty uusi tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-171">We added to our model a new record list.</span></span> <span data-ttu-id="fc5ac-172">Tässä luettelossa näytetään valittujen taloushallinnon dimensioiden arvot (kaikille tätä mallia tietolähteenä käyttäville ER-raporteille).</span><span class="sxs-lookup"><span data-stu-id="fc5ac-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="fc5ac-173">Jokainen taloushallinnon dimensio esitetään tässä luettelossa tietueena, jonka asianmukaiset kentät edustavat dimension arvoja.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="fc5ac-174">Dimension nimi esitetään myös tässä tietueessa käytettävänä kenttänä valintatoimintoa varten tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="fc5ac-175">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="fc5ac-176">Kirjoita Nimi-kenttään "Koodi".</span><span class="sxs-lookup"><span data-stu-id="fc5ac-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="fc5ac-177">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="fc5ac-178">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-178">Click Add.</span></span>
63. <span data-ttu-id="fc5ac-179">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="fc5ac-180">Syötä Nimi-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="fc5ac-181">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-181">Click Add.</span></span>
66. <span data-ttu-id="fc5ac-182">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="fc5ac-183">Syötä Nimi-kenttään Nimi.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="fc5ac-184">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-184">Click Add.</span></span>
69. <span data-ttu-id="fc5ac-185">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-185">Click Save.</span></span>
70. <span data-ttu-id="fc5ac-186">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fc5ac-186">Close the page.</span></span>
