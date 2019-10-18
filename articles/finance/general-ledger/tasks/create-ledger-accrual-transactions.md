---
title: Kirjanpidon jaksotustapahtumien luominen
description: Tässä tehtäväopastuksessa käsitellään jaksotusmalleihin perustuvien kirjanpidon jaksotustapahtumien luontia.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06743ca3ed13906e3f65d3783db7a7f74fb53e3f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186184"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="f7604-103">Kirjanpidon jaksotustapahtumien luominen</span><span class="sxs-lookup"><span data-stu-id="f7604-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7604-104">Tässä tehtäväopastuksessa käsitellään jaksotusmalleihin perustuvien kirjanpidon jaksotustapahtumien luontia</span><span class="sxs-lookup"><span data-stu-id="f7604-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="f7604-105">Siirry kohtaan Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="f7604-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="f7604-106">Etsi ja valitse kirjauskansio luettelosta tai luo uusi kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="f7604-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="f7604-107">Avaa Kirjauskansion eränumero -kentän linkki napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="f7604-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="f7604-108">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f7604-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="f7604-109">Määritä Tili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="f7604-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="f7604-110">Tässä esimerkissä on määritetään vakuutuksen kulu.</span><span class="sxs-lookup"><span data-stu-id="f7604-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="f7604-111">Siitä tulee kausittainen kulusumma.</span><span class="sxs-lookup"><span data-stu-id="f7604-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="f7604-112">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f7604-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="f7604-113">Syötä Debet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="f7604-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="f7604-114">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="f7604-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="f7604-115">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="f7604-115">Click Functions.</span></span>
10. <span data-ttu-id="f7604-116">Valitse Kirjanpidon jaksotukset.</span><span class="sxs-lookup"><span data-stu-id="f7604-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="f7604-117">Avaa haku napsauttamalla Jaksotustunnus-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="f7604-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="f7604-118">Etsi ja valitse luettelosta käytettävä jaksotusmalli.</span><span class="sxs-lookup"><span data-stu-id="f7604-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="f7604-119">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f7604-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f7604-120">Syötä päivämäärä Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f7604-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="f7604-121">Valitse Tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="f7604-121">Click Transactions.</span></span>
16. <span data-ttu-id="f7604-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f7604-122">Close the page.</span></span>
17. <span data-ttu-id="f7604-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f7604-123">Click OK.</span></span>
18. <span data-ttu-id="f7604-124">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="f7604-124">Click Post.</span></span>
