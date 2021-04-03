---
title: Henkilökohtaisen yhteyshenkilön kelpoisuusasetusten määrittäminen
description: Määritä henkilökohtaisten yhteyshenkilöiden kelpoisuusasetuksia Microsoft Dynamics 365 Human Resourcesissa. Henkilökohtaiset yhteyshenkilöt voivat olla edunsaajia tai huollettavia.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f300ac917ac21db9fffbffcc6eb8589357c0a3e
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466203"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="48619-104">Henkilökohtaisen yhteyshenkilön kelpoisuusasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="48619-104">Configure personal contact eligibility options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="48619-105">Tässä artikkelissa kerrotaan, miten voit määrittää henkilökohtaisten yhteyshenkilöiden tyyppejä käytettäväksi Microsoft Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="48619-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="48619-106">Henkilökohtaiset yhteyshenkilöt voivat olla edunsaajia tai huollettavia.</span><span class="sxs-lookup"><span data-stu-id="48619-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="48619-107">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Henkilökohtaisen yhteyshenkilön kelpoisuusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="48619-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="48619-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="48619-108">Select **New**.</span></span>

3. <span data-ttu-id="48619-109">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="48619-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="48619-110">Kenttä</span><span class="sxs-lookup"><span data-stu-id="48619-110">Field</span></span> | <span data-ttu-id="48619-111">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="48619-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="48619-112">**Kelpoisuusvaihtoehto**</span><span class="sxs-lookup"><span data-stu-id="48619-112">**Eligibility option**</span></span> | <span data-ttu-id="48619-113">Yksilöllinen kelpoisuusasetuksen nimi tai koodi kelpoisuusasetuksen tunnistamista varten.</span><span class="sxs-lookup"><span data-stu-id="48619-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="48619-114">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="48619-114">**Description**</span></span> | <span data-ttu-id="48619-115">Kelpoisuusasetuksen lyhyt kuvaus.</span><span class="sxs-lookup"><span data-stu-id="48619-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="48619-116">**Yhteyshenkilön kelpoisuuskoodi**</span><span class="sxs-lookup"><span data-stu-id="48619-116">**Contact eligibility code**</span></span> | <span data-ttu-id="48619-117">Järjestelmäkoodi, joka kuvaa parhaiten henkilökohtaista kelpoisuusvaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="48619-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="48619-118">Voit valita jonkin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="48619-118">You can choose from:</span></span> <ul><li><span data-ttu-id="48619-119">Suhde</span><span class="sxs-lookup"><span data-stu-id="48619-119">Relationship</span></span></li><li><span data-ttu-id="48619-120">Opiskelija</span><span class="sxs-lookup"><span data-stu-id="48619-120">Student</span></span></li><li><span data-ttu-id="48619-121">Ylitys - huollettava</span><span class="sxs-lookup"><span data-stu-id="48619-121">Overage dependent</span></span></li><li><span data-ttu-id="48619-122">Yli-ikäinen vammainen huollettava</span><span class="sxs-lookup"><span data-stu-id="48619-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="48619-123">**Tila**</span><span class="sxs-lookup"><span data-stu-id="48619-123">**Status**</span></span> | <span data-ttu-id="48619-124">Kelpoisuusasetuksen tila.</span><span class="sxs-lookup"><span data-stu-id="48619-124">The status of the eligibility option.</span></span> <span data-ttu-id="48619-125">Jos kelpoisuusasetuksen tilaksi on määritetty passiivinen, et voi valita kyseistä henkilökohtaisen yhteyshenkilön kelpoisuusasetusta henkilökohtaisille yhteyshenkilöille.</span><span class="sxs-lookup"><span data-stu-id="48619-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="48619-126">**Suhde**</span><span class="sxs-lookup"><span data-stu-id="48619-126">**Relationship**</span></span> | <span data-ttu-id="48619-127">Määrittää suhteen henkilökohtaisen yhteyshenkilön ja työntekijän välillä.</span><span class="sxs-lookup"><span data-stu-id="48619-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="48619-128">Tämä kenttä on käytettävissä vain, jos yhteyshenkilön kelpoisuuskoodiksi on määritetty Suhde.</span><span class="sxs-lookup"><span data-stu-id="48619-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="48619-129">**Ikä**</span><span class="sxs-lookup"><span data-stu-id="48619-129">**Age**</span></span> | <span data-ttu-id="48619-130">Kelvollisen henkilökohtaisen yhteyshenkilön yläikäraja etuussuunnitelmassa.</span><span class="sxs-lookup"><span data-stu-id="48619-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="48619-131">Tämä kenttä on käytettävissä vain, jos valitset suhteen.</span><span class="sxs-lookup"><span data-stu-id="48619-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="48619-132">Tätä ikää verrataan henkilökohtaisen yhteyshenkilön laskettuun ikään.</span><span class="sxs-lookup"><span data-stu-id="48619-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="48619-133">Laskettu ikä on: (kattavuuspäivämäärä – henkilökohtaisen yhteyshenkilön syntymäaika / 365).</span><span class="sxs-lookup"><span data-stu-id="48619-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="48619-134">Tämä luku on aina kokonaisluku.</span><span class="sxs-lookup"><span data-stu-id="48619-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="48619-135">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="48619-135">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]