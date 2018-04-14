--- 
title: "Määritä puhelinkeskuksen kanava ja kanavamääritteet"
description: "Tässä menettelyssä kerrotaan, miten uusi vähittäismyyntikanava luodaan ja miten kanavamääritteet määritetään."
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bfccbaab5b4d0b4d84d1bf344521b22b7a5e6efc
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="define-call-center-channel-and-channel-attributes"></a><span data-ttu-id="f94fe-103">Määritä puhelinkeskuksen kanava ja kanavamääritteet</span><span class="sxs-lookup"><span data-stu-id="f94fe-103">Define call center channel and channel attributes</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f94fe-104">Tässä menettelyssä kerrotaan, miten uusi vähittäismyyntikanava luodaan ja miten kanavamääritteet määritetään.</span><span class="sxs-lookup"><span data-stu-id="f94fe-104">This procedure walks through creating a new retail channel and defining channel attributes.</span></span> <span data-ttu-id="f94fe-105">Tämän tehtävän luomisessa käytetty USRT-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="f94fe-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="f94fe-106">Tämä menettely on tarkoitettu vähittäismyymälän IT-osaston roolille.</span><span class="sxs-lookup"><span data-stu-id="f94fe-106">This procedure is intended for the Retail IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="f94fe-107">Uuden myymälän luominen</span><span class="sxs-lookup"><span data-stu-id="f94fe-107">Create new store</span></span>
1. <span data-ttu-id="f94fe-108">Siirry Kaikki työtiloja > Kanavan käyttöönotto.</span><span class="sxs-lookup"><span data-stu-id="f94fe-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="f94fe-109">Valitse Uusi kanava.</span><span class="sxs-lookup"><span data-stu-id="f94fe-109">Click New channel.</span></span>
3. <span data-ttu-id="f94fe-110">Valitse Myymälä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-110">Click Store.</span></span>
4. <span data-ttu-id="f94fe-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f94fe-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f94fe-112">Kirjoita arvo Myymälän numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f94fe-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="f94fe-113">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f94fe-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f94fe-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f94fe-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f94fe-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f94fe-116">Valitse vaihtoehto Varaston aikavyöhyke -kentässä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="f94fe-117">Avaa haku valitsemalla Kanavaprofiili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f94fe-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="f94fe-118">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="f94fe-119">Avaa haku valitsemalla Kieli-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f94fe-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="f94fe-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f94fe-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="f94fe-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="f94fe-122">Avaa haku valitsemalla Arvonlisäveroryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f94fe-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="f94fe-123">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f94fe-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="f94fe-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="f94fe-125">Avaa haku valitsemalla Asiakkaan osoitekirja -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f94fe-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f94fe-126">Valitse osoitekirja, johon tämän myymälän asiakkaat linkitetään.</span><span class="sxs-lookup"><span data-stu-id="f94fe-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="f94fe-127">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f94fe-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="f94fe-128">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="f94fe-129">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="f94fe-129">Click Select.</span></span>
22. <span data-ttu-id="f94fe-130">Avaa haku valitsemalla Työntekijän osoitekirja -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f94fe-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f94fe-131">Valitse osoitekirja, johon tämän kanavan kassat linkitetään.</span><span class="sxs-lookup"><span data-stu-id="f94fe-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="f94fe-132">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f94fe-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="f94fe-133">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="f94fe-134">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="f94fe-134">Click Select.</span></span>
26. <span data-ttu-id="f94fe-135">Avaa haku valitsemalla Oletusasiakas-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f94fe-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="f94fe-136">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="f94fe-137">Laajenna tai tiivistä Näytön asettelu -osa.</span><span class="sxs-lookup"><span data-stu-id="f94fe-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="f94fe-138">Avaa haku valitsemalla Näytön asettelun tunnus -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f94fe-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f94fe-139">Valitse tämän myymälän myyntipisteen näytön oletusasettelu.</span><span class="sxs-lookup"><span data-stu-id="f94fe-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="f94fe-140">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f94fe-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="f94fe-141">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="f94fe-142">Valitse toimintoruudussa Määritä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="f94fe-143">Valitse Kanavamääritteet.</span><span class="sxs-lookup"><span data-stu-id="f94fe-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="f94fe-144">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f94fe-144">Click New.</span></span>
35. <span data-ttu-id="f94fe-145">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f94fe-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="f94fe-146">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f94fe-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="f94fe-147">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="f94fe-148">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f94fe-148">Click Save.</span></span>
39. <span data-ttu-id="f94fe-149">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f94fe-149">Close the page.</span></span>
40. <span data-ttu-id="f94fe-150">Valitse toimintoruudussa Määritä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="f94fe-151">Valitse Maksutavat.</span><span class="sxs-lookup"><span data-stu-id="f94fe-151">Click Payment methods.</span></span>
42. <span data-ttu-id="f94fe-152">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f94fe-152">Click New.</span></span>
43. <span data-ttu-id="f94fe-153">Avaa haku valitsemalla Maksutapa-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f94fe-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="f94fe-154">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="f94fe-155">Laajenna tai tiivistä Kirjaus-osa.</span><span class="sxs-lookup"><span data-stu-id="f94fe-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="f94fe-156">Määritä Tilinumero-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="f94fe-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="f94fe-157">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f94fe-157">Click Save.</span></span>
48. <span data-ttu-id="f94fe-158">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f94fe-158">Close the page.</span></span>
49. <span data-ttu-id="f94fe-159">Valitse toimintoruudussa Määritä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="f94fe-160">Valitse Kassatilitys.</span><span class="sxs-lookup"><span data-stu-id="f94fe-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="f94fe-161">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f94fe-161">Click New.</span></span>
52. <span data-ttu-id="f94fe-162">Syötä luku Summa tapahtuman valuuttana -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f94fe-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="f94fe-163">Avaa haku valitsemalla Valuutta-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f94fe-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="f94fe-164">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f94fe-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="f94fe-165">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="f94fe-166">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f94fe-166">Click Save.</span></span>
57. <span data-ttu-id="f94fe-167">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f94fe-167">Close the page.</span></span>
58. <span data-ttu-id="f94fe-168">Valitse toimintoruudussa Määritä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="f94fe-169">Valitse Myymäläpaikantimen ryhmämääritys.</span><span class="sxs-lookup"><span data-stu-id="f94fe-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="f94fe-170">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f94fe-170">Click New.</span></span>
61. <span data-ttu-id="f94fe-171">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f94fe-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="f94fe-172">Avaa haku valitsemalla Paikanninryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f94fe-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="f94fe-173">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f94fe-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="f94fe-174">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f94fe-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="f94fe-175">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f94fe-175">Click Save.</span></span>
66. <span data-ttu-id="f94fe-176">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f94fe-176">Close the page.</span></span>


