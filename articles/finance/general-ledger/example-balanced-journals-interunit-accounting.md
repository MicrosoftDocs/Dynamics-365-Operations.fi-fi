---
title: Tasapainotetut kirjauskansiot yksiköiden väliselle kirjanpidolle
description: Tässä artikkelissa esitellään, kuinka kirjauskansio täsmäytetään automaattisesti, kun täsmäyttävä taloushallinnon dimensio on valittu Kirjanpito-sivulla.
author: ShylaThompson
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5a926adcc631ec286f37796713466eb0144494c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818389"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="702a5-103">Tasapainotetut kirjauskansiot yksiköiden väliselle kirjanpidolle</span><span class="sxs-lookup"><span data-stu-id="702a5-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="702a5-104">Tässä artikkelissa esitellään, kuinka kirjauskansio täsmäytetään automaattisesti, kun täsmäyttävä taloushallinnon dimensio on valittu Kirjanpito-sivulla.</span><span class="sxs-lookup"><span data-stu-id="702a5-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="702a5-105">Jos kirjanpitomerkinnät eivät täsmää taloushallinnon dimension arvojen tasolla, kirjauskansion tasapainottamiseksi luodaan automaattisesti lisäkirjanpitomerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="702a5-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="702a5-106">Nämä kirjanpitomerkinnät käyttävät **Automaattisten tapahtumien tilit** -sivulla olevia **Yksiköiden välinen – debet**- ja **Yksiköiden välinen – kredit** -kirjaustyyppejä päätilin määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="702a5-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="702a5-107">Esimerkki: Liiketoimintayksikkö, joka on kirjanpitotilin toinen segmentti, valitaan täsmäyttäväksi taloushallinnon dimensioksi, ja seuraavat kirjanpitomerkinnät on tarkoitus luoda.</span><span class="sxs-lookup"><span data-stu-id="702a5-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

| &nbsp;               | &nbsp;    |
|----------------------|-----------|
| <span data-ttu-id="702a5-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="702a5-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="702a5-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="702a5-109">100.00 DR</span></span> |
| <span data-ttu-id="702a5-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="702a5-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="702a5-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="702a5-111">100.00 DR</span></span> |
| <span data-ttu-id="702a5-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="702a5-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="702a5-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="702a5-113">200.00 CR</span></span> |

<span data-ttu-id="702a5-114">Tässä tapauksessa määritetään seuraavat saldot:</span><span class="sxs-lookup"><span data-stu-id="702a5-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="702a5-115">Liiketoimintayksikön MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="702a5-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="702a5-116">Liiketoimintayksikön NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="702a5-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="702a5-117">Tällöin seuraavat kirjanpitomerkinnät luodaan automaattisesti, jotta kirjauskansio täsmää taloushallinnon dimensioiden arvojen tasolla.</span><span class="sxs-lookup"><span data-stu-id="702a5-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

| &nbsp;                            | &nbsp;    |
|-----------------------------------|-----------|
| <span data-ttu-id="702a5-118">(Yksiköiden välinen – debet) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="702a5-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="702a5-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="702a5-119">100.00 DR</span></span> |
| <span data-ttu-id="702a5-120">(Yksiköiden välinen – kredit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="702a5-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="702a5-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="702a5-121">100.00 CR</span></span> |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]