---
title: "Henkilökohtaiset kulut kuluraportissa"
description: "Tässä ohjeaiheessa käsitellään kaksi tapaa, jolla työntekijän henkilökohtaiset kulut voidaan käsitellä Microsoft Dynamics 365 for Finance and Operationsissa."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 11739c8b2979cf7ac9aad04e5be9903d6bc1837a
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="747af-103">Henkilökohtaiset kulut kuluraportissa</span><span class="sxs-lookup"><span data-stu-id="747af-103">Personal expenses on an expense report</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="747af-104">Liikematkalla työntekijät voivat joskus maksaa henkilökohtaisia kulujaan yrityksen luottokorteilla.</span><span class="sxs-lookup"><span data-stu-id="747af-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="747af-105">Jos henkilökohtaisten kulujen käsittelyä varten ei määritetä menettelyä, kuluraporttien hyväksyntäprosessi voi häiriintyä, kun työntekijä lähettää eritellyt kuluraportit.</span><span class="sxs-lookup"><span data-stu-id="747af-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="747af-106">Microsoft Dynamics 365 for Finance and Operationsissa on kaksi tapaa, jolla työntekijän henkilökohtaiset kulut voidaan käsitellä:</span><span class="sxs-lookup"><span data-stu-id="747af-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="747af-107">**Työntekijä maksaa** – Organisaatio ei maksu yrityksen luottokorttilaskussa olevia henkilökohtaisia kuluja.</span><span class="sxs-lookup"><span data-stu-id="747af-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="747af-108">Sen sijaan se luo raportin, jossa henkilökohtaiset kulut näkyvät yhdessä luottokortilla maksettujen yrityksen kulujen kanssa.</span><span class="sxs-lookup"><span data-stu-id="747af-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="747af-109">**Yritys maksaa** – Organisaatio maksaa yrityksen luottokorttilaskun kokonaisuudessaan ja veloittaa henkilökohtaiset kulut työntekijän tililtä.</span><span class="sxs-lookup"><span data-stu-id="747af-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="747af-110">Voit valita organisaation käyttämän menetelmän **Kulujenhallinnan parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="747af-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>

