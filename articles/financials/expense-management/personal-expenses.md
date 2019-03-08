---
title: Henkilökohtaiset kulut kuluraportissa
description: Tässä ohjeaiheessa käsitellään kaksi tapaa, jolla työntekijän henkilökohtaisia kuluja käsitellään Microsoft Dynamics 365 for Finance and Operationsissa.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a6b6c505e7dc5e6544658b00d9f59e6062353608
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "344889"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="33cfa-103">Henkilökohtaiset kulut kuluraportissa</span><span class="sxs-lookup"><span data-stu-id="33cfa-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33cfa-104">Liikematkalla työntekijät voivat joskus maksaa henkilökohtaisia kulujaan yrityksen luottokorteilla.</span><span class="sxs-lookup"><span data-stu-id="33cfa-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="33cfa-105">Jos henkilökohtaisten kulujen käsittelyä varten ei määritetä menettelyä, kuluraporttien hyväksyntäprosessi voi häiriintyä, kun työntekijä lähettää eritellyt kuluraportit.</span><span class="sxs-lookup"><span data-stu-id="33cfa-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="33cfa-106">Microsoft Dynamics 365 for Finance and Operationsissa on kaksi tapaa, jolla työntekijän henkilökohtaisia kuluja käsitellään:</span><span class="sxs-lookup"><span data-stu-id="33cfa-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="33cfa-107">**Työntekijä maksaa** – Organisaatio ei maksu yrityksen luottokorttilaskussa olevia henkilökohtaisia kuluja.</span><span class="sxs-lookup"><span data-stu-id="33cfa-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="33cfa-108">Sen sijaan se luo raportin, jossa henkilökohtaiset kulut näkyvät yhdessä luottokortilla maksettujen yrityksen kulujen kanssa.</span><span class="sxs-lookup"><span data-stu-id="33cfa-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="33cfa-109">**Yritys maksaa** – Organisaatio maksaa yrityksen luottokorttilaskun kokonaisuudessaan ja veloittaa henkilökohtaiset kulut työntekijän tililtä.</span><span class="sxs-lookup"><span data-stu-id="33cfa-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="33cfa-110">Voit valita organisaation käyttämän menetelmän **Kulujenhallinnan parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="33cfa-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
