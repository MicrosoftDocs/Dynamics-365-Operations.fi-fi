---
title: Kuluraportin kirjaaminen
description: "Tässä ohjeaiheessa kerrotaan, miten kuluraportti kirjataan kirjanpitoon."
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: cc3aae061038202ec4f314654d9149c31e2575bb
ms.contentlocale: fi-fi
ms.lasthandoff: 03/13/2018

---

# <a name="post-an-expense-report"></a><span data-ttu-id="341ba-103">Kuluraportin kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="341ba-103">Post an expense report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="341ba-104">Kun kuluraportti on hyväksytty ja siirretty yleiseen kirjauskansioon, se voidaan kirjata kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="341ba-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="341ba-105">Kun kirjaat kuluraporttia, ALV:n palautukseen oikeuttavat kulut tunnistetaan.</span><span class="sxs-lookup"><span data-stu-id="341ba-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="341ba-106">ALV-maksujen varmistaminen ja palauttaminen on määritetty työntekijöille, joka vastaa kuluraportin varmistamisesta.</span><span class="sxs-lookup"><span data-stu-id="341ba-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="341ba-107">Jos kuluraportin kulut veloitetaan jollekin muulle yritykselle kuin yritykselle, joka on työntekijän työnantaja, sinun on vahvistettava yritys, jolle kulut ollaan velkaa, ja yritys, joka on kulut velkaa.</span><span class="sxs-lookup"><span data-stu-id="341ba-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="341ba-108">Kuluraportin lähettänyt työntekijä esimerkiksi on töissä DAT-yrityksessä mutta veloitti kulut DIR-yritykselle.</span><span class="sxs-lookup"><span data-stu-id="341ba-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="341ba-109">Tässä tapauksessa DAT on yritys, jolle kulu ollaan velkaa, ja DIR on yritys, joka on kulun velkaa.</span><span class="sxs-lookup"><span data-stu-id="341ba-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="341ba-110">Kun nämä kirjauskansion rivit on varmistettu, kulurivit voidaan kirjata kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="341ba-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="341ba-111">Kuluraportti kirjataan valitsemalla **Hyväksytyt kuluraportit** -sivulla ensin kuluraportin ja sitten toimintoruudussa **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="341ba-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="341ba-112">Voit kirjata luettelon kaikki kuluraportit myös yhdellä kertaa.</span><span class="sxs-lookup"><span data-stu-id="341ba-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="341ba-113">Valitse ensin kaikki kuluraportit ja sitten **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="341ba-113">Select all the expense reports, and then select **Post**.</span></span>

