---
title: Avaintiedot ostoreskontrajärjestelmään hyväksymiskirjauskansiota käyttämällä
description: Tässä ohjauksessa opastetaan luomaan laskuja laskurekisterin avulla ja käyttämään hyväksymiskirjauskansiota kulutilien päivittämisessä.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 048eda77064b6aa3f666e998a8e551d2f7adc385
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "363519"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a><span data-ttu-id="616ad-103">Avaintiedot ostoreskontrajärjestelmään hyväksymiskirjauskansiota käyttämällä</span><span class="sxs-lookup"><span data-stu-id="616ad-103">Key invoice data into AP system using approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="616ad-104">Tässä ohjauksessa opastetaan luomaan laskuja laskurekisterin avulla ja käyttämään hyväksymiskirjauskansiota kulutilien päivittämisessä.</span><span class="sxs-lookup"><span data-stu-id="616ad-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="616ad-105">Luominen, kirjaaminen ja laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="616ad-105">Create and post and invoice</span></span>
1. <span data-ttu-id="616ad-106">Siirry kohtaan Ostoreskontra > Laskut > Laskurekisteri.</span><span class="sxs-lookup"><span data-stu-id="616ad-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="616ad-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="616ad-107">Click New.</span></span>
3. <span data-ttu-id="616ad-108">Valitse sen laskurekisterin nimi, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="616ad-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="616ad-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="616ad-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="616ad-110">Valitse Rivit, kun haluat avata rekisterin ja syöttää kulurivejä.</span><span class="sxs-lookup"><span data-stu-id="616ad-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="616ad-111">Valitse toimittaja.</span><span class="sxs-lookup"><span data-stu-id="616ad-111">Select a vendor.</span></span> <span data-ttu-id="616ad-112">Voit esimerkiksi syöttää tai valita arvoksi US-104</span><span class="sxs-lookup"><span data-stu-id="616ad-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="616ad-113">Kirjoita Lasku-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="616ad-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="616ad-114">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="616ad-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="616ad-115">Syötä Kredit-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="616ad-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="616ad-116">Avaa haku valitsemalla Hyväksynyt-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="616ad-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="616ad-117">Korosta hyväksyjä ja valitse hyväksyjä valitsemalla Valitse.</span><span class="sxs-lookup"><span data-stu-id="616ad-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="616ad-118">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="616ad-118">Click Post.</span></span>
13. <span data-ttu-id="616ad-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="616ad-119">Close the page.</span></span>
14. <span data-ttu-id="616ad-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="616ad-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="616ad-121">Laskun hyväksyminen</span><span class="sxs-lookup"><span data-stu-id="616ad-121">Approve an invoice</span></span>
1. <span data-ttu-id="616ad-122">Siirry kohtaan Ostoreskontra > Laskut > Laskun hyväksyntä.</span><span class="sxs-lookup"><span data-stu-id="616ad-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="616ad-123">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="616ad-123">Click New.</span></span>
3. <span data-ttu-id="616ad-124">Valitse sen laskun hyväksymiskirjauskansion nimi, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="616ad-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="616ad-125">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="616ad-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="616ad-126">Valitse sivulla näytettävät rivit. Sivulla voit valita hyväksyttäviä laskuja.</span><span class="sxs-lookup"><span data-stu-id="616ad-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="616ad-127">Valitse Etsi tositteet, kun haluat näyttää kaikki laskut, jotka ovat valmiita hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="616ad-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="616ad-128">Merkitse luomasi lasku.</span><span class="sxs-lookup"><span data-stu-id="616ad-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="616ad-129">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="616ad-129">Click Select.</span></span>
    * <span data-ttu-id="616ad-130">Yllä valitut tositteet siirretään tähän luetteloon sen jälkeen, kun tositteet on valittu.</span><span class="sxs-lookup"><span data-stu-id="616ad-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="616ad-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="616ad-131">Click OK.</span></span>
10. <span data-ttu-id="616ad-132">Valitse Tilinumero-kenttä, kun haluat lisätä laskuun kulutilin.</span><span class="sxs-lookup"><span data-stu-id="616ad-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="616ad-133">Syötä tilinumero ja siirry pois kentästä sarkainnäppäimellä.</span><span class="sxs-lookup"><span data-stu-id="616ad-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="616ad-134">Syötä arvoksi esimerkiksi 600120.</span><span class="sxs-lookup"><span data-stu-id="616ad-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="616ad-135">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="616ad-135">Click Post.</span></span>
13. <span data-ttu-id="616ad-136">Valitse Tosite, kun haluat tarkastella kirjattuja syöttöjä.</span><span class="sxs-lookup"><span data-stu-id="616ad-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="616ad-137">Hyväksyntää odottavien laskujen tili peruutetaan ja korvataan toteutuneella kulutilillä.</span><span class="sxs-lookup"><span data-stu-id="616ad-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

