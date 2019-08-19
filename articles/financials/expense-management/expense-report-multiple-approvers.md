---
title: Kuluraportit ja useita hyväksyjiä
description: Tässä ohjeaiheessa on tietoja kuluraportteja, joissa tarvitaan useita hyväksyjiä.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d83a473e2e894856c12b36b4d005c6cb06b765a
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795121"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="46e46-103">Kuluraportit ja useita hyväksyjiä</span><span class="sxs-lookup"><span data-stu-id="46e46-103">Expense reports and multiple approvers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46e46-104">Organisaation kulujen hyväksyntäkäytäntöjen mukaan useat henkilöt voivat hyväksyä työntekijän lähettämän kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="46e46-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="46e46-105">Kun määritä kuluraportin hyväksyntätyönkulun, voit lisätä työnkulkuelementtejä, jotka sisältävät vaiheita vähintään yhdelle kuluraportin hyväksyjälle.</span><span class="sxs-lookup"><span data-stu-id="46e46-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="46e46-106">Voit esimerkiksi edellyttää, että kaikki kuluraportit on ensin hyväksytettävä raportin lähettäneen työntekijän esimiehellä ja sitten ostoreskontran koordinaattorilla.</span><span class="sxs-lookup"><span data-stu-id="46e46-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="46e46-107">Jos päätät edellyttää useita kuluraportin hyväksyjiä, voit lisätä työnkulun elementtejä seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="46e46-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="46e46-108">Lisää hyväksyntäelementti, jossa on yksi vaihe.</span><span class="sxs-lookup"><span data-stu-id="46e46-108">Add one approval element that has one step.</span></span> <span data-ttu-id="46e46-109">Vaihe voi esimerkiksi edellyttää, että kuluraportti määritetään käyttäjäryhmälle ja että 50 % ryhmän jäsenistä on hyväksyttävä se.</span><span class="sxs-lookup"><span data-stu-id="46e46-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="46e46-110">Lisää hyväksyntäelementti, jossa on useita vaiheita.</span><span class="sxs-lookup"><span data-stu-id="46e46-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="46e46-111">Hyväksyntäelementissä voi olla esimerkiksi seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="46e46-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="46e46-112">Kuluraportin lähettäneen työntekijän esimies hyväksyy raportin.</span><span class="sxs-lookup"><span data-stu-id="46e46-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="46e46-113">Ostoreskontra-assistentti varmistaa kuitit ja kuluraportin nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="46e46-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="46e46-114">Budjetin omistaja hyväksyy kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="46e46-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="46e46-115">Lisää useita hyväksyntäelementtejä, joista jokaisella on yksi vaihe.</span><span class="sxs-lookup"><span data-stu-id="46e46-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="46e46-116">Voit esimerkiksi lisätä erillisen hyväksyntäelementin kullekin seuraavista vaiheista:</span><span class="sxs-lookup"><span data-stu-id="46e46-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="46e46-117">Työntekijän esimies hyväksyy kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="46e46-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="46e46-118">Budjetin omistaja hyväksyy kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="46e46-118">The budget owner approves the expense report.</span></span>
