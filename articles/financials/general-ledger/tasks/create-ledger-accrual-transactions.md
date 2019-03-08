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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a65bec066bdcb01ce8acf8cfbf2d31611104921
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "330468"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="ad157-103">Kirjanpidon jaksotustapahtumien luominen</span><span class="sxs-lookup"><span data-stu-id="ad157-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad157-104">Tässä tehtäväopastuksessa käsitellään jaksotusmalleihin perustuvien kirjanpidon jaksotustapahtumien luontia</span><span class="sxs-lookup"><span data-stu-id="ad157-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="ad157-105">Siirry kohtaan Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="ad157-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="ad157-106">Etsi ja valitse kirjauskansio luettelosta tai luo uusi kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="ad157-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="ad157-107">Avaa Kirjauskansion eränumero -kentän linkki napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="ad157-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="ad157-108">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ad157-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="ad157-109">Määritä Tili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="ad157-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="ad157-110">Tässä esimerkissä on määritetään vakuutuksen kulu.</span><span class="sxs-lookup"><span data-stu-id="ad157-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="ad157-111">Siitä tulee kausittainen kulusumma.</span><span class="sxs-lookup"><span data-stu-id="ad157-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="ad157-112">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ad157-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="ad157-113">Syötä Debet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ad157-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="ad157-114">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="ad157-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="ad157-115">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="ad157-115">Click Functions.</span></span>
10. <span data-ttu-id="ad157-116">Valitse Kirjanpidon jaksotukset.</span><span class="sxs-lookup"><span data-stu-id="ad157-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="ad157-117">Avaa haku napsauttamalla Jaksotustunnus-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="ad157-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="ad157-118">Etsi ja valitse luettelosta käytettävä jaksotusmalli.</span><span class="sxs-lookup"><span data-stu-id="ad157-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="ad157-119">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ad157-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="ad157-120">Syötä päivämäärä Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ad157-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="ad157-121">Valitse Tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="ad157-121">Click Transactions.</span></span>
16. <span data-ttu-id="ad157-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ad157-122">Close the page.</span></span>
17. <span data-ttu-id="ad157-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ad157-123">Click OK.</span></span>
18. <span data-ttu-id="ad157-124">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="ad157-124">Click Post.</span></span>

