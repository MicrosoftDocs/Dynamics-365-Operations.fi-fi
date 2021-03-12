---
title: Määritä pankin limiitit ja kirjausprofiilit takauskirjoja varten
description: Tämä tehtävä pankkilimiitin ja kirjausprofiilin, joita tarvitaan takausasiakirjan käsittelemiseen.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6da3b9358192997de1d0231e5c9c8eaba92a23b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976263"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="2d0d6-103">Määritä pankin limiitit ja kirjausprofiilit takauskirjoja varten</span><span class="sxs-lookup"><span data-stu-id="2d0d6-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2d0d6-104">Tämä tehtävä pankkilimiitin ja kirjausprofiilin, joita tarvitaan takausasiakirjan käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="2d0d6-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="2d0d6-106">Kirjanpitoparametri</span><span class="sxs-lookup"><span data-stu-id="2d0d6-106">General ledger parameter</span></span>
1. <span data-ttu-id="2d0d6-107">Valitse Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="2d0d6-108">Laajenna Pankkitosite-osa.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="2d0d6-109">Valitse Ota takausasiakirja käyttöön -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="2d0d6-110">Avaa haku napsauttamalla Tapahtumakirjauskansio-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2d0d6-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="2d0d6-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2d0d6-113">Valitse Numerojärjestykset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="2d0d6-114">Määritä takausasiakirjan numeron ja takausasiakirjan tapahtumaviitteiden numerosarjakoodi</span><span class="sxs-lookup"><span data-stu-id="2d0d6-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="2d0d6-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-115">Click Save.</span></span>
9. <span data-ttu-id="2d0d6-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="2d0d6-117">Luo pankkilimiitti</span><span class="sxs-lookup"><span data-stu-id="2d0d6-117">Create Bank facility</span></span>
1. <span data-ttu-id="2d0d6-118">Valitse Maksuliikenteen hallinta > Asetukset > Pankin limiitit.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="2d0d6-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-119">Click New.</span></span>
3. <span data-ttu-id="2d0d6-120">Kirjoita Limiittiryhmä-kenttään takausasiakirjatapahtuman pankin limiittiryhmän nimi.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="2d0d6-121">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2d0d6-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-122">Click Save.</span></span>
6. <span data-ttu-id="2d0d6-123">Valitse Limiittityypit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="2d0d6-124">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-124">Click New.</span></span>
8. <span data-ttu-id="2d0d6-125">Kirjoita Limiittityyppi-kenttään pankin limiittisopimukseen liittyvä pankin limiittityyppi.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="2d0d6-126">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="2d0d6-127">Avaa haku napsauttamalla Limiittiryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2d0d6-128">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="2d0d6-129">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="2d0d6-130">Valitse Limiitin laatu -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="2d0d6-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-131">Click Save.</span></span>
15. <span data-ttu-id="2d0d6-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="2d0d6-133">Pankin kirjausprofiili</span><span class="sxs-lookup"><span data-stu-id="2d0d6-133">Bank posting profile</span></span>
1. <span data-ttu-id="2d0d6-134">Valitse Maksuliikenteen hallinta > Asetukset > Pankkitositteiden kirjausprofiili.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="2d0d6-135">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-135">Click New.</span></span>
3. <span data-ttu-id="2d0d6-136">Avaa haku napsauttamalla Tilin/ryhmän numero -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2d0d6-137">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2d0d6-138">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2d0d6-139">Valitse Selvitystili-kentässä päätili tilitystä varten.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="2d0d6-140">Valitse Veloitustili-kentästä kulutapahtumien tili.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="2d0d6-141">Valitse Marginaalitili-kentästä katetapahtumien tili.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="2d0d6-142">Valitse Selvitystili-kentässä takausasiakirjatapahtuman selvitystili.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="2d0d6-143">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-143">Click Save.</span></span>
11. <span data-ttu-id="2d0d6-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2d0d6-144">Close the page.</span></span>

