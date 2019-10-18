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
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e7018c79e54841d0729636b08ad475a94d20d5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185954"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="7dff0-103">Määritä ennakonpidätys</span><span class="sxs-lookup"><span data-stu-id="7dff0-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7dff0-104">Tässä ohjeaiheessa kuvataan ennakonpidätyksen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="7dff0-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="7dff0-105">*Ennakonpidätys* on toimittajilta perittävä vero, josta ei synny arvonlisäverotapahtumia.</span><span class="sxs-lookup"><span data-stu-id="7dff0-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="7dff0-106">Toimittajien maksuista laskettava ennakonpidätys on velkaa.</span><span class="sxs-lookup"><span data-stu-id="7dff0-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="7dff0-107">Sen vuoksi ennakonpidätyksen voi kirjata vain tase- tai velkatileille.</span><span class="sxs-lookup"><span data-stu-id="7dff0-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="7dff0-108">Tässä tehtävän ohjauksessa kerrotaan, miten ennakonpidätys määritetään.</span><span class="sxs-lookup"><span data-stu-id="7dff0-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="7dff0-109">Siirry kohtaan **Siirtymisruutu > Moduulit > Vero > Välilliset verot > Ennakonpidätys > Ennakonpidätyskoodit**.</span><span class="sxs-lookup"><span data-stu-id="7dff0-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="7dff0-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7dff0-110">Select **New**.</span></span>
3. <span data-ttu-id="7dff0-111">Kirjoita **Ennakonpidätyskoodi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7dff0-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="7dff0-112">Syötä **Ennakonpidätyksen nimi** -kenttään ennakonpidätyskoodin nimi.</span><span class="sxs-lookup"><span data-stu-id="7dff0-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="7dff0-113">Valitse **Päätili**-kentässä päätili ennakonpidätysvelan kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="7dff0-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="7dff0-114">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7dff0-114">Select **Save**.</span></span>
7. <span data-ttu-id="7dff0-115">Valitse **Arvot** ja merkitse haluamasi tietue luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7dff0-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="7dff0-116">Syötä **Arvo**-kenttään ennakonpidätyksen laskemisessa käytettävä prosenttiluku.</span><span class="sxs-lookup"><span data-stu-id="7dff0-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="7dff0-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7dff0-117">Select **Save**.</span></span>
10. <span data-ttu-id="7dff0-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7dff0-118">Close the page.</span></span>
11. <span data-ttu-id="7dff0-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7dff0-119">Select **Save**.</span></span>
12. <span data-ttu-id="7dff0-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7dff0-120">Close the page.</span></span>
13. <span data-ttu-id="7dff0-121">Siirry kohtaan **Siirtymisruutu > Moduulit > Vero > Välilliset verot > Ennakonpidätys > Ennakonpidätysryhmät**.</span><span class="sxs-lookup"><span data-stu-id="7dff0-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="7dff0-122">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7dff0-122">Select **New**.</span></span>
15. <span data-ttu-id="7dff0-123">Syötä **Ennakonpidätysryhmä**-kenttään ennakonpidätysryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="7dff0-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="7dff0-124">Syötä **Kuvaus**-kenttään ennakonpidätysryhmän nimi.</span><span class="sxs-lookup"><span data-stu-id="7dff0-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="7dff0-125">Valitse **Ennakonpidätyskoodi**-kentässä ennakonpidätyskoodi.</span><span class="sxs-lookup"><span data-stu-id="7dff0-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="7dff0-126">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7dff0-126">Select **Save**.</span></span>
19. <span data-ttu-id="7dff0-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7dff0-127">Close the page.</span></span>

