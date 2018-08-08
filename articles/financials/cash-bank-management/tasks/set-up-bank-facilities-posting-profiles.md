--- 
title: "Määritä pankin limiitit ja kirjausprofiilit takauskirjoja varten"
description: "Tämä tehtävä pankkilimiitin ja kirjausprofiilin, joita tarvitaan takausasiakirjan käsittelemiseen."
author: kweekley
manager: AnnBe
ms.date: 02/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 4c36d938000fdb70fd4fbedb1e05b0c8a5350fac
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="f2196-103">Määritä pankin limiitit ja kirjausprofiilit takauskirjoja varten</span><span class="sxs-lookup"><span data-stu-id="f2196-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2196-104">Tämä tehtävä pankkilimiitin ja kirjausprofiilin, joita tarvitaan takausasiakirjan käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="f2196-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="f2196-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="f2196-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="f2196-106">Kirjanpitoparametri</span><span class="sxs-lookup"><span data-stu-id="f2196-106">General ledger parameter</span></span>
1. <span data-ttu-id="f2196-107">Valitse Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot.</span><span class="sxs-lookup"><span data-stu-id="f2196-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="f2196-108">Laajenna Pankkitosite-osa.</span><span class="sxs-lookup"><span data-stu-id="f2196-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="f2196-109">Valitse Ota takausasiakirja käyttöön -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="f2196-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="f2196-110">Avaa haku napsauttamalla Tapahtumakirjauskansio-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="f2196-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f2196-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f2196-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="f2196-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f2196-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f2196-113">Valitse Numerojärjestykset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f2196-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="f2196-114">Määritä takausasiakirjan numeron ja takausasiakirjan tapahtumaviitteiden numerosarjakoodi</span><span class="sxs-lookup"><span data-stu-id="f2196-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="f2196-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f2196-115">Click Save.</span></span>
9. <span data-ttu-id="f2196-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2196-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="f2196-117">Luo pankkilimiitti</span><span class="sxs-lookup"><span data-stu-id="f2196-117">Create Bank facility</span></span>
1. <span data-ttu-id="f2196-118">Valitse Maksuliikenteen hallinta > Asetukset > Pankin limiitit.</span><span class="sxs-lookup"><span data-stu-id="f2196-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="f2196-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f2196-119">Click New.</span></span>
3. <span data-ttu-id="f2196-120">Kirjoita Limiittiryhmä-kenttään takausasiakirjatapahtuman pankin limiittiryhmän nimi.</span><span class="sxs-lookup"><span data-stu-id="f2196-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="f2196-121">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f2196-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f2196-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f2196-122">Click Save.</span></span>
6. <span data-ttu-id="f2196-123">Valitse Limiittityypit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f2196-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="f2196-124">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f2196-124">Click New.</span></span>
8. <span data-ttu-id="f2196-125">Kirjoita Limiittityyppi-kenttään pankin limiittisopimukseen liittyvä pankin limiittityyppi.</span><span class="sxs-lookup"><span data-stu-id="f2196-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="f2196-126">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f2196-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="f2196-127">Avaa haku napsauttamalla Limiittiryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="f2196-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="f2196-128">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f2196-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="f2196-129">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f2196-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="f2196-130">Valitse Limiitin laatu -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="f2196-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="f2196-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f2196-131">Click Save.</span></span>
15. <span data-ttu-id="f2196-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2196-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="f2196-133">Pankin kirjausprofiili</span><span class="sxs-lookup"><span data-stu-id="f2196-133">Bank posting profile</span></span>
1. <span data-ttu-id="f2196-134">Valitse Maksuliikenteen hallinta > Asetukset > Pankkitositteiden kirjausprofiili.</span><span class="sxs-lookup"><span data-stu-id="f2196-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="f2196-135">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f2196-135">Click New.</span></span>
3. <span data-ttu-id="f2196-136">Avaa haku napsauttamalla Tilin/ryhmän numero -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="f2196-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f2196-137">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f2196-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f2196-138">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f2196-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f2196-139">Valitse Selvitystili-kentässä päätili tilitystä varten.</span><span class="sxs-lookup"><span data-stu-id="f2196-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="f2196-140">Valitse Veloitustili-kentästä kulutapahtumien tili.</span><span class="sxs-lookup"><span data-stu-id="f2196-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="f2196-141">Valitse Marginaalitili-kentästä katetapahtumien tili.</span><span class="sxs-lookup"><span data-stu-id="f2196-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="f2196-142">Valitse Selvitystili-kentässä takausasiakirjatapahtuman selvitystili.</span><span class="sxs-lookup"><span data-stu-id="f2196-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="f2196-143">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f2196-143">Click Save.</span></span>
11. <span data-ttu-id="f2196-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2196-144">Close the page.</span></span>


