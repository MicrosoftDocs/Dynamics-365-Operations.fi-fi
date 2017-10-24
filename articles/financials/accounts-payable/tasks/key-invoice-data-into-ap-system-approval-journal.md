--- 
title: "Laskun keskeiset tiedot ostoreskontraan hyväksymiskirjauskansion avulla"
description: "Tässä ohjauksessa opastetaan luomaan laskuja laskurekisterin avulla ja käyttämään hyväksymiskirjauskansiota kulutilien päivittämisessä."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 604345d357e5019e334017b2b6d0413f40818acc
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="e1fe0-103">Laskun keskeiset tiedot ostoreskontraan hyväksymiskirjauskansion avulla</span><span class="sxs-lookup"><span data-stu-id="e1fe0-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e1fe0-104">Tässä ohjauksessa opastetaan luomaan laskuja laskurekisterin avulla ja käyttämään hyväksymiskirjauskansiota kulutilien päivittämisessä.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="e1fe0-105">Luominen, kirjaaminen ja laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="e1fe0-105">Create and post and invoice</span></span>
1. <span data-ttu-id="e1fe0-106">Siirry kohtaan Ostoreskontra > Laskut > Laskurekisteri.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="e1fe0-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-107">Click New.</span></span>
3. <span data-ttu-id="e1fe0-108">Valitse sen laskurekisterin nimi, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="e1fe0-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e1fe0-110">Valitse Rivit, kun haluat avata rekisterin ja syöttää kulurivejä.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="e1fe0-111">Valitse toimittaja.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-111">Select a vendor.</span></span> <span data-ttu-id="e1fe0-112">Voit esimerkiksi syöttää tai valita arvoksi US-104</span><span class="sxs-lookup"><span data-stu-id="e1fe0-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="e1fe0-113">Kirjoita Lasku-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="e1fe0-114">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="e1fe0-115">Syötä Kredit-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="e1fe0-116">Avaa haku valitsemalla Hyväksynyt-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e1fe0-117">Korosta hyväksyjä ja valitse hyväksyjä valitsemalla Valitse.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="e1fe0-118">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-118">Click Post.</span></span>
13. <span data-ttu-id="e1fe0-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-119">Close the page.</span></span>
14. <span data-ttu-id="e1fe0-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="e1fe0-121">Laskun hyväksyminen</span><span class="sxs-lookup"><span data-stu-id="e1fe0-121">Approve an invoice</span></span>
1. <span data-ttu-id="e1fe0-122">Siirry kohtaan Ostoreskontra > Laskut > Laskun hyväksyntä.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="e1fe0-123">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-123">Click New.</span></span>
3. <span data-ttu-id="e1fe0-124">Valitse sen laskun hyväksymiskirjauskansion nimi, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="e1fe0-125">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e1fe0-126">Valitse sivulla näytettävät rivit. Sivulla voit valita hyväksyttäviä laskuja.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="e1fe0-127">Valitse Etsi tositteet, kun haluat näyttää kaikki laskut, jotka ovat valmiita hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="e1fe0-128">Merkitse luomasi lasku.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="e1fe0-129">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-129">Click Select.</span></span>
    * <span data-ttu-id="e1fe0-130">Yllä valitut tositteet siirretään tähän luetteloon sen jälkeen, kun tositteet on valittu.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="e1fe0-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-131">Click OK.</span></span>
10. <span data-ttu-id="e1fe0-132">Valitse Tilinumero-kenttä, kun haluat lisätä laskuun kulutilin.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="e1fe0-133">Syötä tilinumero ja siirry pois kentästä sarkainnäppäimellä.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="e1fe0-134">Syötä arvoksi esimerkiksi 600120.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="e1fe0-135">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-135">Click Post.</span></span>
13. <span data-ttu-id="e1fe0-136">Valitse Tosite, kun haluat tarkastella kirjattuja syöttöjä.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="e1fe0-137">Hyväksyntää odottavien laskujen tili peruutetaan ja korvataan toteutuneella kulutilillä.</span><span class="sxs-lookup"><span data-stu-id="e1fe0-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  


