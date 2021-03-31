---
title: Laskun keskeiset tiedot ostoreskontraan hyväksymiskirjauskansion avulla
description: Tässä ohjeaiheessa kerrotaan, miten luodaan laskuja laskurekisterin avulla ja käytetään hyväksymiskirjauskansiota kulutilien päivittämisessä.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0fee32d9fd1ab89b1a8cedb2e1965674586d4e7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227181"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="7da64-103">Laskun keskeiset tiedot ostoreskontraan hyväksymiskirjauskansion avulla</span><span class="sxs-lookup"><span data-stu-id="7da64-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7da64-104">Tässä ohjeaiheessa kerrotaan, miten luodaan laskuja laskurekisterin avulla ja käytetään hyväksymiskirjauskansiota kulutilien päivittämisessä.</span><span class="sxs-lookup"><span data-stu-id="7da64-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="7da64-105">Luominen, kirjaaminen ja laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="7da64-105">Create and post and invoice</span></span>
1. <span data-ttu-id="7da64-106">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Laskut > Laskurekisteri**.</span><span class="sxs-lookup"><span data-stu-id="7da64-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="7da64-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7da64-107">Select **New**.</span></span>
3. <span data-ttu-id="7da64-108">Valitse sen laskurekisterin nimi, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="7da64-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="7da64-109">Valitse **Rivit**, kun haluat avata rekisterin ja syöttää kulurivejä.</span><span class="sxs-lookup"><span data-stu-id="7da64-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="7da64-110">Valitse toimittaja.</span><span class="sxs-lookup"><span data-stu-id="7da64-110">Select a vendor.</span></span> <span data-ttu-id="7da64-111">Voit esimerkiksi syöttää tai valita arvoksi `US-104`.</span><span class="sxs-lookup"><span data-stu-id="7da64-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="7da64-112">Kirjoita **Lasku**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7da64-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="7da64-113">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7da64-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="7da64-114">Syötä **Kredit**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="7da64-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="7da64-115">Valitse **Hyväksynyt**-kentästä hyväksyjä avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="7da64-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="7da64-116">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="7da64-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="7da64-117">Laskun hyväksyminen</span><span class="sxs-lookup"><span data-stu-id="7da64-117">Approve an invoice</span></span>
1. <span data-ttu-id="7da64-118">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Laskut > Laskun hyväksyntä**.</span><span class="sxs-lookup"><span data-stu-id="7da64-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="7da64-119">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7da64-119">Select **New**.</span></span>
3. <span data-ttu-id="7da64-120">Valitse sen laskun hyväksymiskirjauskansion nimi, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="7da64-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="7da64-121">Valitse sivulla näytettävät **Rivit**. Sivulla voit valita hyväksyttäviä laskuja.</span><span class="sxs-lookup"><span data-stu-id="7da64-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="7da64-122">Valitse **Etsi tositteet**, kun haluat näyttää kaikki laskut, jotka ovat valmiita hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="7da64-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="7da64-123">Merkitse luomasi lasku ja valitse sitten **Valitse.**</span><span class="sxs-lookup"><span data-stu-id="7da64-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="7da64-124">Yllä valitut tositteet siirretään tähän luetteloon sen jälkeen, kun tositteet on valittu.</span><span class="sxs-lookup"><span data-stu-id="7da64-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="7da64-125">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7da64-125">Select **OK**.</span></span>
8. <span data-ttu-id="7da64-126">Valitse **Tilinumero**-kenttä, kun haluat lisätä laskuun kulutilin.</span><span class="sxs-lookup"><span data-stu-id="7da64-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="7da64-127">Syötä tilinumero ja siirry pois kentästä sarkainnäppäimellä.</span><span class="sxs-lookup"><span data-stu-id="7da64-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="7da64-128">Syötä arvoksi esimerkiksi `600120`.</span><span class="sxs-lookup"><span data-stu-id="7da64-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="7da64-129">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="7da64-129">Select **Post**.</span></span>
11. <span data-ttu-id="7da64-130">Valitse **Tosite**, kun haluat tarkastella kirjattuja syöttöjä.</span><span class="sxs-lookup"><span data-stu-id="7da64-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="7da64-131">Hyväksyntää odottavien laskujen tili peruutetaan ja korvataan toteutuneella kulutilillä.</span><span class="sxs-lookup"><span data-stu-id="7da64-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]