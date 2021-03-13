---
title: ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 1 – Tietomallin suunnittelu)
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) mallin määrittämistä käyttämään taloushallinnon dimensioita ER-raporttien tietolähteenä. (Osa 1)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92d29d954debddd509eaba6b710f39b218da2c77
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092172"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="0a618-104">ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 1 – Tietomallin suunnittelu)</span><span class="sxs-lookup"><span data-stu-id="0a618-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a618-105">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvoja tai sähköisen raportoinnin kehittäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.</span><span class="sxs-lookup"><span data-stu-id="0a618-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="0a618-106">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="0a618-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="0a618-107">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="0a618-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="0a618-108">Luo uusi tietomalli</span><span class="sxs-lookup"><span data-stu-id="0a618-108">Create a new data model</span></span>
1. <span data-ttu-id="0a618-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="0a618-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="0a618-110">Varmista, että Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="0a618-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="0a618-111">-lähde on käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="0a618-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="0a618-112">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="0a618-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="0a618-113">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="0a618-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="0a618-114">Syötä Nimi-kenttään "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="0a618-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="0a618-115">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="0a618-115">Click Create configuration.</span></span>
6. <span data-ttu-id="0a618-116">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="0a618-116">Click Designer.</span></span>
7. <span data-ttu-id="0a618-117">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="0a618-118">Kirjoita Nimi-kenttään "Kirjaus".</span><span class="sxs-lookup"><span data-stu-id="0a618-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="0a618-119">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-119">Click Add.</span></span>
10. <span data-ttu-id="0a618-120">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="0a618-121">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="0a618-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="0a618-122">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-122">Click Add.</span></span>
    * <span data-ttu-id="0a618-123">Malliin ei lisätä uutta tietueluetteloa.</span><span class="sxs-lookup"><span data-stu-id="0a618-123">We will add to our model a new record list.</span></span> <span data-ttu-id="0a618-124">Tässä luettelossa näytetään valittujen taloushallinnon dimensioiden asetukset (kaikille tätä mallia tietolähteenä käyttäville ER-raporteille).</span><span class="sxs-lookup"><span data-stu-id="0a618-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="0a618-125">Jokainen taloushallinnon dimensio esitetään tässä luettelossa tietueena, jonka asianmukaiset kentät edustavat dimension asetuksia.</span><span class="sxs-lookup"><span data-stu-id="0a618-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="0a618-126">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="0a618-127">Kirjoita Nimi-kenttään "Dimensioiden asetus".</span><span class="sxs-lookup"><span data-stu-id="0a618-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="0a618-128">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="0a618-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="0a618-129">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-129">Click Add.</span></span>
17. <span data-ttu-id="0a618-130">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="0a618-131">Kirjoita Nimi-kenttään "Koodi".</span><span class="sxs-lookup"><span data-stu-id="0a618-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="0a618-132">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="0a618-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="0a618-133">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-133">Click Add.</span></span>
21. <span data-ttu-id="0a618-134">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="0a618-135">Syötä Nimi-kenttään Nimi.</span><span class="sxs-lookup"><span data-stu-id="0a618-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="0a618-136">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-136">Click Add.</span></span>
24. <span data-ttu-id="0a618-137">Valitse puussa "Entry".</span><span class="sxs-lookup"><span data-stu-id="0a618-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="0a618-138">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="0a618-139">Kirjoita Nimi-kenttään "Kirjauskansio".</span><span class="sxs-lookup"><span data-stu-id="0a618-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="0a618-140">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="0a618-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="0a618-141">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-141">Click Add.</span></span>
29. <span data-ttu-id="0a618-142">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="0a618-143">Kirjoita Nimi-kenttään "Erä".</span><span class="sxs-lookup"><span data-stu-id="0a618-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="0a618-144">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="0a618-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="0a618-145">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-145">Click Add.</span></span>
33. <span data-ttu-id="0a618-146">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="0a618-147">Kirjoita Nimi-kenttään "Tapahtuma".</span><span class="sxs-lookup"><span data-stu-id="0a618-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="0a618-148">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="0a618-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="0a618-149">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-149">Click Add.</span></span>
37. <span data-ttu-id="0a618-150">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="0a618-151">Kirjoita Nimi-kenttään "Päivämäärä".</span><span class="sxs-lookup"><span data-stu-id="0a618-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="0a618-152">Valitse Nimiketyyppi-kentässä Päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="0a618-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="0a618-153">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-153">Click Add.</span></span>
41. <span data-ttu-id="0a618-154">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="0a618-155">Kirjoita Nimi -kenttään "Veloitus".</span><span class="sxs-lookup"><span data-stu-id="0a618-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="0a618-156">Valitse Nimiketyyppi-kentässä Reaaliluku.</span><span class="sxs-lookup"><span data-stu-id="0a618-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="0a618-157">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-157">Click Add.</span></span>
45. <span data-ttu-id="0a618-158">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="0a618-159">Syötä Nimi-kenttään "Hyvitys".</span><span class="sxs-lookup"><span data-stu-id="0a618-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="0a618-160">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-160">Click Add.</span></span>
48. <span data-ttu-id="0a618-161">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="0a618-162">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="0a618-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="0a618-163">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="0a618-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="0a618-164">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-164">Click Add.</span></span>
52. <span data-ttu-id="0a618-165">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="0a618-166">Kirjoita Nimi-kenttään "Tosite".</span><span class="sxs-lookup"><span data-stu-id="0a618-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="0a618-167">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-167">Click Add.</span></span>
55. <span data-ttu-id="0a618-168">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="0a618-169">Kirjoita Nimi-kenttään "Dimensioiden tiedot".</span><span class="sxs-lookup"><span data-stu-id="0a618-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="0a618-170">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="0a618-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="0a618-171">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-171">Click Add.</span></span>
    * <span data-ttu-id="0a618-172">Malliin on lisätty uusi tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="0a618-172">We added to our model a new record list.</span></span> <span data-ttu-id="0a618-173">Tässä luettelossa näytetään valittujen taloushallinnon dimensioiden arvot (kaikille tätä mallia tietolähteenä käyttäville ER-raporteille).</span><span class="sxs-lookup"><span data-stu-id="0a618-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="0a618-174">Jokainen taloushallinnon dimensio esitetään tässä luettelossa tietueena, jonka asianmukaiset kentät edustavat dimension arvoja.</span><span class="sxs-lookup"><span data-stu-id="0a618-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="0a618-175">Dimension nimi esitetään myös tässä tietueessa käytettävänä kenttänä valintatoimintoa varten tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="0a618-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="0a618-176">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="0a618-177">Kirjoita Nimi-kenttään "Koodi".</span><span class="sxs-lookup"><span data-stu-id="0a618-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="0a618-178">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="0a618-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="0a618-179">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-179">Click Add.</span></span>
63. <span data-ttu-id="0a618-180">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="0a618-181">Syötä Nimi-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="0a618-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="0a618-182">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-182">Click Add.</span></span>
66. <span data-ttu-id="0a618-183">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0a618-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="0a618-184">Syötä Nimi-kenttään Nimi.</span><span class="sxs-lookup"><span data-stu-id="0a618-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="0a618-185">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a618-185">Click Add.</span></span>
69. <span data-ttu-id="0a618-186">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0a618-186">Click Save.</span></span>
70. <span data-ttu-id="0a618-187">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0a618-187">Close the page.</span></span>

![ER-tietomallin suunnittelutoiminnon sivu](../media/er-financial-dimensions-guides-data-model.png)

