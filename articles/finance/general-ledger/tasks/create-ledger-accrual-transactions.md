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
ms.openlocfilehash: 2112336045086d0eb3b2fb0018f33631528a05ec
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145096"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="1097a-103">Kirjanpidon jaksotustapahtumien luominen</span><span class="sxs-lookup"><span data-stu-id="1097a-103">Create ledger accrual transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1097a-104">Tässä tehtäväopastuksessa käsitellään jaksotusmalleihin perustuvien kirjanpidon jaksotustapahtumien luontia</span><span class="sxs-lookup"><span data-stu-id="1097a-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="1097a-105">Siirry kohtaan Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="1097a-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="1097a-106">Etsi ja valitse kirjauskansio luettelosta tai luo uusi kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="1097a-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="1097a-107">Avaa Kirjauskansion eränumero -kentän linkki napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="1097a-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="1097a-108">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="1097a-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="1097a-109">Määritä Tili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="1097a-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="1097a-110">Tässä esimerkissä on määritetään vakuutuksen kulu.</span><span class="sxs-lookup"><span data-stu-id="1097a-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="1097a-111">Siitä tulee kausittainen kulusumma.</span><span class="sxs-lookup"><span data-stu-id="1097a-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="1097a-112">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1097a-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="1097a-113">Syötä Debet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="1097a-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="1097a-114">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="1097a-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="1097a-115">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="1097a-115">Click Functions.</span></span>
10. <span data-ttu-id="1097a-116">Valitse Kirjanpidon jaksotukset.</span><span class="sxs-lookup"><span data-stu-id="1097a-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="1097a-117">Avaa haku napsauttamalla Jaksotustunnus-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="1097a-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="1097a-118">Etsi ja valitse luettelosta käytettävä jaksotusmalli.</span><span class="sxs-lookup"><span data-stu-id="1097a-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="1097a-119">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1097a-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="1097a-120">Syötä päivämäärä Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1097a-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="1097a-121">Valitse Tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="1097a-121">Click Transactions.</span></span>
16. <span data-ttu-id="1097a-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1097a-122">Close the page.</span></span>
17. <span data-ttu-id="1097a-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1097a-123">Click OK.</span></span>
18. <span data-ttu-id="1097a-124">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="1097a-124">Click Post.</span></span>

