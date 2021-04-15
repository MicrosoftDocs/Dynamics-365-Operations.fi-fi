---
title: Määritä ennakonpidätys
description: Tässä ohjeaiheessa kuvataan ennakonpidätyksen määrittäminen.
author: twheeloc
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 592afb7542fa44dcb1bf3f7354937d3c21fb1a87
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813465"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="28ae8-103">Määritä ennakonpidätys</span><span class="sxs-lookup"><span data-stu-id="28ae8-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28ae8-104">Tässä ohjeaiheessa kuvataan ennakonpidätyksen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="28ae8-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="28ae8-105">*Ennakonpidätys* on toimittajilta perittävä vero, josta ei synny arvonlisäverotapahtumia.</span><span class="sxs-lookup"><span data-stu-id="28ae8-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="28ae8-106">Toimittajien maksuista laskettava ennakonpidätys on velkaa.</span><span class="sxs-lookup"><span data-stu-id="28ae8-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="28ae8-107">Sen vuoksi ennakonpidätyksen voi kirjata vain tase- tai velkatileille.</span><span class="sxs-lookup"><span data-stu-id="28ae8-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="28ae8-108">Tässä tehtävän ohjauksessa kerrotaan, miten ennakonpidätys määritetään.</span><span class="sxs-lookup"><span data-stu-id="28ae8-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="28ae8-109">Siirry kohtaan **Siirtymisruutu > Moduulit > Vero > Välilliset verot > Ennakonpidätys > Ennakonpidätyskoodit**.</span><span class="sxs-lookup"><span data-stu-id="28ae8-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="28ae8-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="28ae8-110">Select **New**.</span></span>
3. <span data-ttu-id="28ae8-111">Kirjoita **Ennakonpidätyskoodi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="28ae8-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="28ae8-112">Syötä **Ennakonpidätyksen nimi** -kenttään ennakonpidätyskoodin nimi.</span><span class="sxs-lookup"><span data-stu-id="28ae8-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="28ae8-113">Valitse **Päätili**-kentässä päätili ennakonpidätysvelan kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="28ae8-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="28ae8-114">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="28ae8-114">Select **Save**.</span></span>
7. <span data-ttu-id="28ae8-115">Valitse **Arvot** ja merkitse haluamasi tietue luettelossa.</span><span class="sxs-lookup"><span data-stu-id="28ae8-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="28ae8-116">Syötä **Arvo**-kenttään ennakonpidätyksen laskemisessa käytettävä prosenttiluku.</span><span class="sxs-lookup"><span data-stu-id="28ae8-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="28ae8-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="28ae8-117">Select **Save**.</span></span>
10. <span data-ttu-id="28ae8-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="28ae8-118">Close the page.</span></span>
11. <span data-ttu-id="28ae8-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="28ae8-119">Select **Save**.</span></span>
12. <span data-ttu-id="28ae8-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="28ae8-120">Close the page.</span></span>
13. <span data-ttu-id="28ae8-121">Siirry kohtaan **Siirtymisruutu > Moduulit > Vero > Välilliset verot > Ennakonpidätys > Ennakonpidätysryhmät**.</span><span class="sxs-lookup"><span data-stu-id="28ae8-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="28ae8-122">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="28ae8-122">Select **New**.</span></span>
15. <span data-ttu-id="28ae8-123">Syötä **Ennakonpidätysryhmä**-kenttään ennakonpidätysryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="28ae8-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="28ae8-124">Syötä **Kuvaus**-kenttään ennakonpidätysryhmän nimi.</span><span class="sxs-lookup"><span data-stu-id="28ae8-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="28ae8-125">Valitse **Ennakonpidätyskoodi**-kentässä ennakonpidätyskoodi.</span><span class="sxs-lookup"><span data-stu-id="28ae8-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="28ae8-126">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="28ae8-126">Select **Save**.</span></span>
19. <span data-ttu-id="28ae8-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="28ae8-127">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]