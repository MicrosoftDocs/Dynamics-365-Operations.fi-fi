---
title: Määritä pankin limiitit ja kirjausprofiilit remburssia varten
description: Tässä menettelyssä selvitetään luottokirjeiden käsittelyyn tarvittavan pankkilimiitin ja kirjausprofiilin luonti.
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
ms.openlocfilehash: bc94100461bc82e9e7cd243f198711ab61a79b0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225270"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="5951e-103">Määritä pankin limiitit ja kirjausprofiilit remburssia varten</span><span class="sxs-lookup"><span data-stu-id="5951e-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5951e-104">Tässä menettelyssä selvitetään luottokirjeiden käsittelyyn tarvittavan pankkilimiitin ja kirjausprofiilin luonti.</span><span class="sxs-lookup"><span data-stu-id="5951e-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="5951e-105">Tässä tehtävässä käytetään USMF-esittely-yritystä.</span><span class="sxs-lookup"><span data-stu-id="5951e-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="5951e-106">Kirjanpitoparametri</span><span class="sxs-lookup"><span data-stu-id="5951e-106">General ledger parameter</span></span>
1. <span data-ttu-id="5951e-107">Valitse Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot.</span><span class="sxs-lookup"><span data-stu-id="5951e-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="5951e-108">Laajenna Pankkitosite-osa.</span><span class="sxs-lookup"><span data-stu-id="5951e-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="5951e-109">Valitse Ota tuontiremburssi käyttöön -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="5951e-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="5951e-110">Valitse Ota vientiremburssi käyttöön -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="5951e-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="5951e-111">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5951e-111">Click Save.</span></span>
6. <span data-ttu-id="5951e-112">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5951e-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="5951e-113">Luo pankkilimiitti</span><span class="sxs-lookup"><span data-stu-id="5951e-113">Create Bank facility</span></span>
1. <span data-ttu-id="5951e-114">Valitse Maksuliikenteen hallinta > Asetukset > Pankin limiitit.</span><span class="sxs-lookup"><span data-stu-id="5951e-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="5951e-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5951e-115">Click New.</span></span>
3. <span data-ttu-id="5951e-116">Anna Limiittiryhmä-kenttään pankin limiittiryhmän nimi.</span><span class="sxs-lookup"><span data-stu-id="5951e-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="5951e-117">Kirjoita Kuvaus-kenttään pankin limiittiryhmän kuvaus.</span><span class="sxs-lookup"><span data-stu-id="5951e-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="5951e-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5951e-118">Click Save.</span></span>
6. <span data-ttu-id="5951e-119">Valitse Limiittityypit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="5951e-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="5951e-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5951e-120">Click New.</span></span>
8. <span data-ttu-id="5951e-121">Anna Limiittityyppi-kenttään yksilöivä koodi.</span><span class="sxs-lookup"><span data-stu-id="5951e-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="5951e-122">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5951e-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="5951e-123">Avaa haku napsauttamalla Limiittiryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="5951e-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="5951e-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5951e-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="5951e-125">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5951e-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="5951e-126">Valitse Limiitin laatu -kentästä pankkilimiitin laatu.</span><span class="sxs-lookup"><span data-stu-id="5951e-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="5951e-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5951e-127">Click Save.</span></span>
15. <span data-ttu-id="5951e-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5951e-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="5951e-129">Pankin kirjausprofiili</span><span class="sxs-lookup"><span data-stu-id="5951e-129">Bank posting profile</span></span>
1. <span data-ttu-id="5951e-130">Valitse Maksuliikenteen hallinta > Asetukset > Pankkitositteiden kirjausprofiili.</span><span class="sxs-lookup"><span data-stu-id="5951e-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="5951e-131">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5951e-131">Click New.</span></span>
3. <span data-ttu-id="5951e-132">Avaa haku napsauttamalla Tilin/ryhmän numero -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="5951e-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5951e-133">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5951e-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="5951e-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5951e-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5951e-135">Valitse tilityksen päätili.</span><span class="sxs-lookup"><span data-stu-id="5951e-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="5951e-136">Tätä tiliä käytetään laskettaessa kassavirtaennustetta.</span><span class="sxs-lookup"><span data-stu-id="5951e-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="5951e-137">Valitse Veloitustili-kentästä kulutapahtumien tili.</span><span class="sxs-lookup"><span data-stu-id="5951e-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="5951e-138">Valitse Marginaalitili-kentästä katetapahtumien tili.</span><span class="sxs-lookup"><span data-stu-id="5951e-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="5951e-139">Tätä tiliä veloitetaan, kun avaava marginaali on kirjattu ja hyvitetään, kun maksu on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="5951e-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="5951e-140">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5951e-140">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]