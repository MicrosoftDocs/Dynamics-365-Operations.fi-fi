---
title: "Kuluraportit ja useita hyväksyjiä"
description: "Tässä ohjeaiheessa on tietoja kuluraportteja, joissa tarvitaan useita hyväksyjiä."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7cd2e56dab48ad8f2380dcaa72e3317250b5b2f0
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="e492c-103">Kuluraportit ja useita hyväksyjiä</span><span class="sxs-lookup"><span data-stu-id="e492c-103">Expense reports and multiple approvers</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="e492c-104">Organisaation kulujen hyväksyntäkäytäntöjen mukaan useat henkilöt voivat hyväksyä työntekijän lähettämän kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="e492c-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="e492c-105">Kun määritä kuluraportin hyväksyntätyönkulun, voit lisätä työnkulkuelementtejä, jotka sisältävät vaiheita vähintään yhdelle kuluraportin hyväksyjälle.</span><span class="sxs-lookup"><span data-stu-id="e492c-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="e492c-106">Voit esimerkiksi edellyttää, että kaikki kuluraportit on ensin hyväksytettävä raportin lähettäneen työntekijän esimiehellä ja sitten ostoreskontran koordinaattorilla.</span><span class="sxs-lookup"><span data-stu-id="e492c-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="e492c-107">Jos päätät edellyttää useita kuluraportin hyväksyjiä, voit lisätä työnkulun elementtejä seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="e492c-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="e492c-108">Lisää hyväksyntäelementti, jossa on yksi vaihe.</span><span class="sxs-lookup"><span data-stu-id="e492c-108">Add one approval element that has one step.</span></span> <span data-ttu-id="e492c-109">Vaihe voi esimerkiksi edellyttää, että kuluraportti määritetään käyttäjäryhmälle ja että 50 % ryhmän jäsenistä on hyväksyttävä se.</span><span class="sxs-lookup"><span data-stu-id="e492c-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="e492c-110">Lisää hyväksyntäelementti, jossa on useita vaiheita.</span><span class="sxs-lookup"><span data-stu-id="e492c-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="e492c-111">Hyväksyntäelementissä voi olla esimerkiksi seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="e492c-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="e492c-112">Kuluraportin lähettäneen työntekijän esimies hyväksyy raportin.</span><span class="sxs-lookup"><span data-stu-id="e492c-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="e492c-113">Ostoreskontra-assistentti varmistaa kuitit ja kuluraportin nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="e492c-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="e492c-114">Budjetin omistaja hyväksyy kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="e492c-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="e492c-115">Lisää useita hyväksyntäelementtejä, joista jokaisella on yksi vaihe.</span><span class="sxs-lookup"><span data-stu-id="e492c-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="e492c-116">Voit esimerkiksi lisätä erillisen hyväksyntäelementin kullekin seuraavista vaiheista:</span><span class="sxs-lookup"><span data-stu-id="e492c-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="e492c-117">Työntekijän esimies hyväksyy kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="e492c-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="e492c-118">Budjetin omistaja hyväksyy kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="e492c-118">The budget owner approves the expense report.</span></span>

