---
title: "Tasapainotetut kirjauskansiot yksiköiden väliselle kirjanpidolle"
description: "Tässä artikkelissa esitellään, kuinka kirjauskansio täsmäytetään automaattisesti, kun täsmäyttävä taloushallinnon dimensio on valittu Kirjanpito-sivulla."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="b49bd-103">Tasapainotetut kirjauskansiot yksiköiden väliselle kirjanpidolle</span><span class="sxs-lookup"><span data-stu-id="b49bd-103">Balanced journals for interunit accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b49bd-104">Tässä artikkelissa esitellään, kuinka kirjauskansio täsmäytetään automaattisesti, kun täsmäyttävä taloushallinnon dimensio on valittu Kirjanpito-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b49bd-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="b49bd-105">Jos kirjanpitomerkinnät eivät täsmää taloushallinnon dimension arvojen tasolla, kirjauskansion tasapainottamiseksi luodaan automaattisesti lisäkirjanpitomerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="b49bd-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="b49bd-106">Nämä kirjanpitomerkinnät käyttävät **Automaattisten tapahtumien tilit** -sivulla olevia **Yksiköiden välinen – debet**- ja **Yksiköiden välinen – kredit** -kirjaustyyppejä päätilin määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="b49bd-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="b49bd-107">Esimerkki: Haara, joka on kirjanpitotilin toinen segmentti, valitaan täsmäyttäväksi taloushallinnon dimensioksi, ja seuraavat kirjanpitomerkinnät on tarkoitus luoda.</span><span class="sxs-lookup"><span data-stu-id="b49bd-107">For example, Branch, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="b49bd-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="b49bd-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="b49bd-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="b49bd-109">100.00 DR</span></span> |
| <span data-ttu-id="b49bd-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="b49bd-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="b49bd-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="b49bd-111">100.00 DR</span></span> |
| <span data-ttu-id="b49bd-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="b49bd-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="b49bd-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="b49bd-113">200.00 CR</span></span> |

<span data-ttu-id="b49bd-114">Tässä tapauksessa määritetään seuraavat saldot:</span><span class="sxs-lookup"><span data-stu-id="b49bd-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="b49bd-115">Haara MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="b49bd-115">For Branch MSP = 100.00 CR</span></span>
-   <span data-ttu-id="b49bd-116">Haara NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="b49bd-116">For Branch NY = 100.00 DR</span></span>

<span data-ttu-id="b49bd-117">Tällöin seuraavat kirjanpitomerkinnät luodaan automaattisesti, jotta kirjauskansio täsmää taloushallinnon dimensioiden arvojen tasolla.</span><span class="sxs-lookup"><span data-stu-id="b49bd-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="b49bd-118">(Yksiköiden välinen – debet) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="b49bd-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="b49bd-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="b49bd-119">100.00 DR</span></span> |
| <span data-ttu-id="b49bd-120">(Yksiköiden välinen – kredit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="b49bd-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="b49bd-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="b49bd-121">100.00 CR</span></span> |






