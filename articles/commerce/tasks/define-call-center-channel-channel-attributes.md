---
title: Puhelinkeskuskanavien luominen ja kanavamääritteiden määrittäminen
description: Tässä menettelyssä kerrotaan, miten uusi kanavaa luodaan ja miten kanavamääritteet määritetään.
author: mugunthanm
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b053ea3a5792d016cfe4850f07c65de97fbfc9e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802692"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="5aa90-103">Puhelinkeskuskanavien luominen ja kanavamääritteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5aa90-103">Create call center channels and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5aa90-104">Tässä menettelyssä kerrotaan, miten uusi kaupankäyntikanava luodaan ja miten kanavamääritteet määritetään.</span><span class="sxs-lookup"><span data-stu-id="5aa90-104">This procedure walks through creating a new commerce channel and defining channel attributes.</span></span> <span data-ttu-id="5aa90-105">Tämän tehtävän luomisessa käytetty USRT-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="5aa90-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="5aa90-106">Tämä menettely on tarkoitettu kaupan IT-osaston roolille.</span><span class="sxs-lookup"><span data-stu-id="5aa90-106">This procedure is intended for the Commerce IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="5aa90-107">Uuden myymälän luominen</span><span class="sxs-lookup"><span data-stu-id="5aa90-107">Create new store</span></span>
1. <span data-ttu-id="5aa90-108">Siirry Kaikki työtiloja > Kanavan käyttöönotto.</span><span class="sxs-lookup"><span data-stu-id="5aa90-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="5aa90-109">Valitse Uusi kanava.</span><span class="sxs-lookup"><span data-stu-id="5aa90-109">Click New channel.</span></span>
3. <span data-ttu-id="5aa90-110">Valitse Myymälä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-110">Click Store.</span></span>
4. <span data-ttu-id="5aa90-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5aa90-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="5aa90-112">Kirjoita arvo Myymälän numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="5aa90-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="5aa90-113">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5aa90-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5aa90-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5aa90-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="5aa90-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5aa90-116">Valitse vaihtoehto Varaston aikavyöhyke -kentässä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="5aa90-117">Avaa haku valitsemalla Kanavaprofiili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5aa90-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="5aa90-118">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="5aa90-119">Avaa haku valitsemalla Kieli-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5aa90-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="5aa90-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5aa90-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="5aa90-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="5aa90-122">Avaa haku valitsemalla Arvonlisäveroryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5aa90-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="5aa90-123">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5aa90-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="5aa90-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="5aa90-125">Avaa haku valitsemalla Asiakkaan osoitekirja -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5aa90-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5aa90-126">Valitse osoitekirja, johon tämän myymälän asiakkaat linkitetään.</span><span class="sxs-lookup"><span data-stu-id="5aa90-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="5aa90-127">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5aa90-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="5aa90-128">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="5aa90-129">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="5aa90-129">Click Select.</span></span>
22. <span data-ttu-id="5aa90-130">Avaa haku valitsemalla Työntekijän osoitekirja -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5aa90-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5aa90-131">Valitse osoitekirja, johon tämän kanavan kassat linkitetään.</span><span class="sxs-lookup"><span data-stu-id="5aa90-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="5aa90-132">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5aa90-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="5aa90-133">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="5aa90-134">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="5aa90-134">Click Select.</span></span>
26. <span data-ttu-id="5aa90-135">Avaa haku valitsemalla Oletusasiakas-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5aa90-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="5aa90-136">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="5aa90-137">Laajenna tai tiivistä Näytön asettelu -osa.</span><span class="sxs-lookup"><span data-stu-id="5aa90-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="5aa90-138">Avaa haku valitsemalla Näytön asettelun tunnus -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5aa90-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5aa90-139">Valitse tämän myymälän myyntipisteen näytön oletusasettelu.</span><span class="sxs-lookup"><span data-stu-id="5aa90-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="5aa90-140">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5aa90-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="5aa90-141">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="5aa90-142">Valitse toimintoruudussa Määritä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="5aa90-143">Valitse Kanavamääritteet.</span><span class="sxs-lookup"><span data-stu-id="5aa90-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="5aa90-144">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5aa90-144">Click New.</span></span>
35. <span data-ttu-id="5aa90-145">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5aa90-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="5aa90-146">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5aa90-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="5aa90-147">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="5aa90-148">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5aa90-148">Click Save.</span></span>
39. <span data-ttu-id="5aa90-149">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5aa90-149">Close the page.</span></span>
40. <span data-ttu-id="5aa90-150">Valitse toimintoruudussa Määritä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="5aa90-151">Valitse Maksutavat.</span><span class="sxs-lookup"><span data-stu-id="5aa90-151">Click Payment methods.</span></span>
42. <span data-ttu-id="5aa90-152">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5aa90-152">Click New.</span></span>
43. <span data-ttu-id="5aa90-153">Avaa haku valitsemalla Maksutapa-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5aa90-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="5aa90-154">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="5aa90-155">Laajenna tai tiivistä Kirjaus-osa.</span><span class="sxs-lookup"><span data-stu-id="5aa90-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="5aa90-156">Määritä Tilinumero-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="5aa90-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="5aa90-157">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5aa90-157">Click Save.</span></span>
48. <span data-ttu-id="5aa90-158">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5aa90-158">Close the page.</span></span>
49. <span data-ttu-id="5aa90-159">Valitse toimintoruudussa Määritä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="5aa90-160">Valitse Kassatilitys.</span><span class="sxs-lookup"><span data-stu-id="5aa90-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="5aa90-161">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5aa90-161">Click New.</span></span>
52. <span data-ttu-id="5aa90-162">Syötä luku Summa tapahtuman valuuttana -kenttään.</span><span class="sxs-lookup"><span data-stu-id="5aa90-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="5aa90-163">Avaa haku valitsemalla Valuutta-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5aa90-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="5aa90-164">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5aa90-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="5aa90-165">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="5aa90-166">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5aa90-166">Click Save.</span></span>
57. <span data-ttu-id="5aa90-167">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5aa90-167">Close the page.</span></span>
58. <span data-ttu-id="5aa90-168">Valitse toimintoruudussa Määritä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="5aa90-169">Valitse Myymäläpaikantimen ryhmämääritys.</span><span class="sxs-lookup"><span data-stu-id="5aa90-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="5aa90-170">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5aa90-170">Click New.</span></span>
61. <span data-ttu-id="5aa90-171">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="5aa90-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="5aa90-172">Avaa haku valitsemalla Paikanninryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5aa90-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="5aa90-173">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5aa90-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="5aa90-174">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5aa90-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="5aa90-175">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5aa90-175">Click Save.</span></span>
66. <span data-ttu-id="5aa90-176">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5aa90-176">Close the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]