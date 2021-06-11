---
title: Henkilökohtaisen yhteyshenkilön kelpoisuusasetusten määrittäminen
description: Määritä henkilökohtaisten yhteyshenkilöiden kelpoisuusasetuksia Microsoft Dynamics 365 Human Resourcesissa. Henkilökohtaiset yhteyshenkilöt voivat olla edunsaajia tai huollettavia.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d85677973f67f0c68de6c5ede62c142524939833
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054401"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="64cdd-104">Henkilökohtaisen yhteyshenkilön kelpoisuusasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="64cdd-104">Configure personal contact eligibility options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="64cdd-105">Tässä artikkelissa kerrotaan, miten voit määrittää henkilökohtaisten yhteyshenkilöiden tyyppejä käytettäväksi Microsoft Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="64cdd-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="64cdd-106">Henkilökohtaiset yhteyshenkilöt voivat olla edunsaajia tai huollettavia.</span><span class="sxs-lookup"><span data-stu-id="64cdd-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="64cdd-107">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Henkilökohtaisen yhteyshenkilön kelpoisuusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="64cdd-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="64cdd-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="64cdd-108">Select **New**.</span></span>

3. <span data-ttu-id="64cdd-109">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="64cdd-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="64cdd-110">Kenttä</span><span class="sxs-lookup"><span data-stu-id="64cdd-110">Field</span></span> | <span data-ttu-id="64cdd-111">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="64cdd-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="64cdd-112">**Kelpoisuusvaihtoehto**</span><span class="sxs-lookup"><span data-stu-id="64cdd-112">**Eligibility option**</span></span> | <span data-ttu-id="64cdd-113">Yksilöllinen kelpoisuusasetuksen nimi tai koodi kelpoisuusasetuksen tunnistamista varten.</span><span class="sxs-lookup"><span data-stu-id="64cdd-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="64cdd-114">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="64cdd-114">**Description**</span></span> | <span data-ttu-id="64cdd-115">Kelpoisuusasetuksen lyhyt kuvaus.</span><span class="sxs-lookup"><span data-stu-id="64cdd-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="64cdd-116">**Yhteyshenkilön kelpoisuuskoodi**</span><span class="sxs-lookup"><span data-stu-id="64cdd-116">**Contact eligibility code**</span></span> | <span data-ttu-id="64cdd-117">Järjestelmäkoodi, joka kuvaa parhaiten henkilökohtaista kelpoisuusvaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="64cdd-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="64cdd-118">Voit valita jonkin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="64cdd-118">You can choose from:</span></span> <ul><li><span data-ttu-id="64cdd-119">Suhde</span><span class="sxs-lookup"><span data-stu-id="64cdd-119">Relationship</span></span></li><li><span data-ttu-id="64cdd-120">Opiskelija</span><span class="sxs-lookup"><span data-stu-id="64cdd-120">Student</span></span></li><li><span data-ttu-id="64cdd-121">Ylitys - huollettava</span><span class="sxs-lookup"><span data-stu-id="64cdd-121">Overage dependent</span></span></li><li><span data-ttu-id="64cdd-122">Yli-ikäinen vammainen huollettava</span><span class="sxs-lookup"><span data-stu-id="64cdd-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="64cdd-123">**Tila**</span><span class="sxs-lookup"><span data-stu-id="64cdd-123">**Status**</span></span> | <span data-ttu-id="64cdd-124">Kelpoisuusasetuksen tila.</span><span class="sxs-lookup"><span data-stu-id="64cdd-124">The status of the eligibility option.</span></span> <span data-ttu-id="64cdd-125">Jos kelpoisuusasetuksen tilaksi on määritetty passiivinen, et voi valita kyseistä henkilökohtaisen yhteyshenkilön kelpoisuusasetusta henkilökohtaisille yhteyshenkilöille.</span><span class="sxs-lookup"><span data-stu-id="64cdd-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="64cdd-126">**Suhde**</span><span class="sxs-lookup"><span data-stu-id="64cdd-126">**Relationship**</span></span> | <span data-ttu-id="64cdd-127">Määrittää suhteen henkilökohtaisen yhteyshenkilön ja työntekijän välillä.</span><span class="sxs-lookup"><span data-stu-id="64cdd-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="64cdd-128">Tämä kenttä on käytettävissä vain, jos yhteyshenkilön kelpoisuuskoodiksi on määritetty Suhde.</span><span class="sxs-lookup"><span data-stu-id="64cdd-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="64cdd-129">**Ikä**</span><span class="sxs-lookup"><span data-stu-id="64cdd-129">**Age**</span></span> | <span data-ttu-id="64cdd-130">Kelvollisen henkilökohtaisen yhteyshenkilön yläikäraja etuussuunnitelmassa.</span><span class="sxs-lookup"><span data-stu-id="64cdd-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="64cdd-131">Tämä kenttä on käytettävissä vain, jos valitset suhteen.</span><span class="sxs-lookup"><span data-stu-id="64cdd-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="64cdd-132">Tätä ikää verrataan henkilökohtaisen yhteyshenkilön laskettuun ikään.</span><span class="sxs-lookup"><span data-stu-id="64cdd-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="64cdd-133">Laskettu ikä on: (kattavuuspäivämäärä – henkilökohtaisen yhteyshenkilön syntymäaika / 365).</span><span class="sxs-lookup"><span data-stu-id="64cdd-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="64cdd-134">Tämä luku on aina kokonaisluku.</span><span class="sxs-lookup"><span data-stu-id="64cdd-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="64cdd-135">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="64cdd-135">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]