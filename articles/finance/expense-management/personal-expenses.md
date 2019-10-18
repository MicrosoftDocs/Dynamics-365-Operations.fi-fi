---
title: Henkilökohtaiset kulut kuluraportissa
description: Tässä ohjeaiheessa käsitellään kaksi tapaa, jolla työntekijän henkilökohtaisia kuluja käsitellään MicrosoftDynamics 365 Financessa.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177530"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="b5523-103">Henkilökohtaiset kulut kuluraportissa</span><span class="sxs-lookup"><span data-stu-id="b5523-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5523-104">Liikematkalla työntekijät voivat joskus maksaa henkilökohtaisia kulujaan yrityksen luottokorteilla.</span><span class="sxs-lookup"><span data-stu-id="b5523-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="b5523-105">Jos henkilökohtaisten kulujen käsittelyä varten ei määritetä menettelyä, kuluraporttien hyväksyntäprosessi voi häiriintyä, kun työntekijä lähettää eritellyt kuluraportit.</span><span class="sxs-lookup"><span data-stu-id="b5523-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="b5523-106">On kaksi tapaa, jolla työntekijän henkilökohtaisia kuluja käsitellään:</span><span class="sxs-lookup"><span data-stu-id="b5523-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="b5523-107">**Työntekijä maksaa** – Organisaatio ei maksu yrityksen luottokorttilaskussa olevia henkilökohtaisia kuluja.</span><span class="sxs-lookup"><span data-stu-id="b5523-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="b5523-108">Sen sijaan se luo raportin, jossa henkilökohtaiset kulut näkyvät yhdessä luottokortilla maksettujen yrityksen kulujen kanssa.</span><span class="sxs-lookup"><span data-stu-id="b5523-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="b5523-109">**Yritys maksaa** – Organisaatio maksaa yrityksen luottokorttilaskun kokonaisuudessaan ja veloittaa henkilökohtaiset kulut työntekijän tililtä.</span><span class="sxs-lookup"><span data-stu-id="b5523-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="b5523-110">Voit valita organisaation käyttämän menetelmän **Kulujenhallinnan parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b5523-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
