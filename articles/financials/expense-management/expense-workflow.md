---
title: "Kulujen työnkulku"
description: "Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin työnkulkujärjestelmää käytetään kuluraporttien tarkastusprosessien luomiseen kulujenhallinnassa."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d60d2f462a1fd27d4655e68aab7f96fb28a34b77
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="expense-workflow"></a><span data-ttu-id="3f5da-103">Kulujen työnkulku</span><span class="sxs-lookup"><span data-stu-id="3f5da-103">Expense workflow</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3f5da-104">Voit käyttää Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin työnkulkujärjestelmää kuluraporttien tarkastusprosessien luomiseen kulujenhallinnassa.</span><span class="sxs-lookup"><span data-stu-id="3f5da-104">You can use the workflow system in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="3f5da-105">Voit määrittää työnkulun, joka määrittelee kuluraporttien hyväksyjät seuraavien ehtojen perusteella:</span><span class="sxs-lookup"><span data-stu-id="3f5da-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="3f5da-106">Työntekijän raportointihierarkia ja ennalta määritellyt hyväksyntärajat</span><span class="sxs-lookup"><span data-stu-id="3f5da-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="3f5da-107">Monitasoinen hyväksyntä, joka tukee väliaikaisia hyväksyjiä ja lopullista hyväksyjää</span><span class="sxs-lookup"><span data-stu-id="3f5da-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="3f5da-108">Taloushallinnon dimensiot ja projektin vastuualueet</span><span class="sxs-lookup"><span data-stu-id="3f5da-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="3f5da-109">Määrittäminen tietyille käyttäjille tai käyttäjäryhmille</span><span class="sxs-lookup"><span data-stu-id="3f5da-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="3f5da-110">Työnkulun hyväksynnät voidaan luoda kuluraporteille, matkustusehdotuksille, käteisennakoille ja arvonlisäveron (ALV) palautuksille.</span><span class="sxs-lookup"><span data-stu-id="3f5da-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="3f5da-111">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="3f5da-111">**Example**</span></span>

<span data-ttu-id="3f5da-112">Seuraava prosessi on esimerkki kulujenhallinnan työnkulusta kuluraporttia varten.</span><span class="sxs-lookup"><span data-stu-id="3f5da-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="3f5da-113">Työntekijä luo ja tallentaa kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="3f5da-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="3f5da-114">Työntekijä lähettää kuluraportin toiselle työntekijälle hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="3f5da-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="3f5da-115">Hyväksyjä päätetään työnkulkua määritellessä luotujen sääntöjen mukaan.</span><span class="sxs-lookup"><span data-stu-id="3f5da-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="3f5da-116">Hyväksyjä saa ilmoituksen kuluraportista, joka on valmis hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="3f5da-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="3f5da-117">Hyväksyjä tarkistaa kuluraportin ja varmistaa, että seuraavat ehdot täyttyvät:</span><span class="sxs-lookup"><span data-stu-id="3f5da-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="3f5da-118">Kulut eivät riko mitään kulukäytäntöjä.</span><span class="sxs-lookup"><span data-stu-id="3f5da-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="3f5da-119">Jos kulu rikkoo käytäntöä, hyväksyjä varmistaa, että kuluraportissa on hyväksyttävä liiketoiminnallinen peruste.</span><span class="sxs-lookup"><span data-stu-id="3f5da-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="3f5da-120">Kuluraporttiin on liitetty sähköisiä kuitteja.</span><span class="sxs-lookup"><span data-stu-id="3f5da-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="3f5da-121">Hyväksyjä hyväksyy kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="3f5da-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="3f5da-122">Kuluraportti annetaan ostoreskontran koordinaattorille kirjattavaksi.</span><span class="sxs-lookup"><span data-stu-id="3f5da-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="3f5da-123">Jokin seuraavista vaiheista toteutuu, riippuen siitä, onko automaattinen kirjaus määritetty:</span><span class="sxs-lookup"><span data-stu-id="3f5da-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="3f5da-124">Jos automaattinen kirjaus on määritetty, kuluraportti käsitellään maksettavaksi ja kuluraportin tila päivitetään.</span><span class="sxs-lookup"><span data-stu-id="3f5da-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="3f5da-125">Jos automaattista kirjausta ei ole määritetty, jos ostoreskontran koodrinaattori varmistaa, että alkuperäiset kuitit on lähetetty ja että kuitit on kohdistettu kuluraportin kuluihin.</span><span class="sxs-lookup"><span data-stu-id="3f5da-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="3f5da-126">Kaikki kuluraportille kirjatut verokoodit on myös varmistettava.</span><span class="sxs-lookup"><span data-stu-id="3f5da-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="3f5da-127">Kun nämä vaatimukset on varmistettu, kuluraportti kirjataan.</span><span class="sxs-lookup"><span data-stu-id="3f5da-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="3f5da-128">Kun kuluraportti on kirjattu, sen maksaminen hyväksytään ja työntekijää hyvitetään.</span><span class="sxs-lookup"><span data-stu-id="3f5da-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>

