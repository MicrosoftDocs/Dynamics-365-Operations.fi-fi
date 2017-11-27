---
title: "Asiakkaiden hyvittäminen"
description: "Tässä artikkelissa kerrotaan, miten hyvitystapahtumat luodaan asiakasryhmälle. Jos asiakkaalla on maksettavien saldo, voit hyvittää asiakkaalle saldon summan."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 01c9dcebe82544624c6dd0feb3672d1c5bdfe2d1
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="reimburse-customers"></a><span data-ttu-id="197a5-104">Asiakkaiden hyvittäminen</span><span class="sxs-lookup"><span data-stu-id="197a5-104">Reimburse customers</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="197a5-105">Tässä artikkelissa kerrotaan, miten hyvitystapahtumat luodaan asiakasryhmälle.</span><span class="sxs-lookup"><span data-stu-id="197a5-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="197a5-106">Jos asiakkaalla on maksettavien saldo, voit hyvittää asiakkaalle saldon summan.</span><span class="sxs-lookup"><span data-stu-id="197a5-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="197a5-107">Seuraavassa taulukossa esitellään edellytykset, joiden on täytyttävä ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="197a5-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="197a5-108">Edellytys</span><span class="sxs-lookup"><span data-stu-id="197a5-108">Prerequisite</span></span>                                                            | <span data-ttu-id="197a5-109">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="197a5-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="197a5-110">Määritä vähimmäishyvityksen määrä yritykselle.</span><span class="sxs-lookup"><span data-stu-id="197a5-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="197a5-111">**Myyntireskontran parametrit** -sivulla **Yleiset**-alueella **Vähimmäissumma**-kentässä, syötä vähimmäissumma, joka voidaan korvata asiakkaan liikamaksuista.</span><span class="sxs-lookup"><span data-stu-id="197a5-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="197a5-112">Valinnainen: Lisää toimittajatili jokaiselle asiakkaalle, jolle voidaan hyvittää.</span><span class="sxs-lookup"><span data-stu-id="197a5-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="197a5-113">**Asiakkaiden** sivulla **Muut tiedot** -pikavälilehdessä **Toimittajatili**-kentässä, valitse toimittajatili asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="197a5-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="197a5-114">Luodessasi hyvitystapahtumia toimittajalasku luodaan maksettavan saldon määrälle.</span><span class="sxs-lookup"><span data-stu-id="197a5-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="197a5-115">Takaisinmaksuprosessi poistaa asiakastilin luottosaldon ja luo toimittajatilille erääntyvän saldon, joka vastaa asiakasta.</span><span class="sxs-lookup"><span data-stu-id="197a5-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="197a5-116">Myyntireskontrassa suorita **Hyvitys**-prosessi.</span><span class="sxs-lookup"><span data-stu-id="197a5-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="197a5-117">Noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="197a5-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="197a5-118">Jos haluat hyvittää tiettyjä asiakasnumeroita, klikkaa **Valitse**  ja määritä kyselyn asiakastilit.</span><span class="sxs-lookup"><span data-stu-id="197a5-118">To reimburse specific customer accounts, click **Select**, and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="197a5-119">Voit hyvittää kaikkia asiakasnumeroita valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="197a5-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="197a5-120">Hyvityssummat siirretään asiakkaiden toimittajanumeroille. Ne käsitellään tavallisina maksuina.</span><span class="sxs-lookup"><span data-stu-id="197a5-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="197a5-121">Jos asiakkaalla ei ole toimittajatiliä, ohjelma luo asiakkaalle automaattisesti kertatoimittajatilin.</span><span class="sxs-lookup"><span data-stu-id="197a5-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="197a5-122">Tarkastellaksesi luotuja hyvitystapahtumia, käytä **Hyvitys**-sivua.</span><span class="sxs-lookup"><span data-stu-id="197a5-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="197a5-123">Ostoreskontrassa, luo maksu toimittajan laskuille, jotka luotiin hyvitysprosessiin maksun luomisessa.</span><span class="sxs-lookup"><span data-stu-id="197a5-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>





