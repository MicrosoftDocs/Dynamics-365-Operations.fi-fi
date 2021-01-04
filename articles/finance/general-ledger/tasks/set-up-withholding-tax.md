---
title: Määritä ennakonpidätys
description: Tässä ohjeaiheessa kuvataan ennakonpidätyksen määrittäminen.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bfa1b9e43a5745eb5b5c442998597319f196f23f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442678"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="79d0b-103">Määritä ennakonpidätys</span><span class="sxs-lookup"><span data-stu-id="79d0b-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="79d0b-104">Tässä ohjeaiheessa kuvataan ennakonpidätyksen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="79d0b-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="79d0b-105">*Ennakonpidätys* on toimittajilta perittävä vero, josta ei synny arvonlisäverotapahtumia.</span><span class="sxs-lookup"><span data-stu-id="79d0b-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="79d0b-106">Toimittajien maksuista laskettava ennakonpidätys on velkaa.</span><span class="sxs-lookup"><span data-stu-id="79d0b-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="79d0b-107">Sen vuoksi ennakonpidätyksen voi kirjata vain tase- tai velkatileille.</span><span class="sxs-lookup"><span data-stu-id="79d0b-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="79d0b-108">Tässä tehtävän ohjauksessa kerrotaan, miten ennakonpidätys määritetään.</span><span class="sxs-lookup"><span data-stu-id="79d0b-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="79d0b-109">Siirry kohtaan **Siirtymisruutu > Moduulit > Vero > Välilliset verot > Ennakonpidätys > Ennakonpidätyskoodit**.</span><span class="sxs-lookup"><span data-stu-id="79d0b-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="79d0b-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="79d0b-110">Select **New**.</span></span>
3. <span data-ttu-id="79d0b-111">Kirjoita **Ennakonpidätyskoodi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="79d0b-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="79d0b-112">Syötä **Ennakonpidätyksen nimi** -kenttään ennakonpidätyskoodin nimi.</span><span class="sxs-lookup"><span data-stu-id="79d0b-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="79d0b-113">Valitse **Päätili**-kentässä päätili ennakonpidätysvelan kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="79d0b-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="79d0b-114">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="79d0b-114">Select **Save**.</span></span>
7. <span data-ttu-id="79d0b-115">Valitse **Arvot** ja merkitse haluamasi tietue luettelossa.</span><span class="sxs-lookup"><span data-stu-id="79d0b-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="79d0b-116">Syötä **Arvo**-kenttään ennakonpidätyksen laskemisessa käytettävä prosenttiluku.</span><span class="sxs-lookup"><span data-stu-id="79d0b-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="79d0b-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="79d0b-117">Select **Save**.</span></span>
10. <span data-ttu-id="79d0b-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="79d0b-118">Close the page.</span></span>
11. <span data-ttu-id="79d0b-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="79d0b-119">Select **Save**.</span></span>
12. <span data-ttu-id="79d0b-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="79d0b-120">Close the page.</span></span>
13. <span data-ttu-id="79d0b-121">Siirry kohtaan **Siirtymisruutu > Moduulit > Vero > Välilliset verot > Ennakonpidätys > Ennakonpidätysryhmät**.</span><span class="sxs-lookup"><span data-stu-id="79d0b-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="79d0b-122">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="79d0b-122">Select **New**.</span></span>
15. <span data-ttu-id="79d0b-123">Syötä **Ennakonpidätysryhmä**-kenttään ennakonpidätysryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="79d0b-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="79d0b-124">Syötä **Kuvaus**-kenttään ennakonpidätysryhmän nimi.</span><span class="sxs-lookup"><span data-stu-id="79d0b-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="79d0b-125">Valitse **Ennakonpidätyskoodi**-kentässä ennakonpidätyskoodi.</span><span class="sxs-lookup"><span data-stu-id="79d0b-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="79d0b-126">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="79d0b-126">Select **Save**.</span></span>
19. <span data-ttu-id="79d0b-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="79d0b-127">Close the page.</span></span>

