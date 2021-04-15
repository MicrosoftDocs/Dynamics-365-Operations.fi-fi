---
title: Asiakkaiden hyvittäminen
description: Tässä artikkelissa kerrotaan, miten hyvitystapahtumat luodaan asiakasryhmälle. Jos asiakkaalla on maksettavien saldo, voit hyvittää asiakkaalle saldon summan.
author: JodiChristiansen
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd8b32e04743fdde3cc339e1535f8ae58c518aed
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816289"
---
# <a name="reimburse-customers"></a><span data-ttu-id="461f8-104">Asiakkaiden hyvittäminen</span><span class="sxs-lookup"><span data-stu-id="461f8-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="461f8-105">Tässä artikkelissa kerrotaan, miten hyvitystapahtumat luodaan asiakasryhmälle.</span><span class="sxs-lookup"><span data-stu-id="461f8-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="461f8-106">Jos asiakkaalla on maksettavien saldo, voit hyvittää asiakkaalle saldon summan.</span><span class="sxs-lookup"><span data-stu-id="461f8-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="461f8-107">Seuraavassa taulukossa esitellään edellytykset, joiden on täytyttävä ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="461f8-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="461f8-108">Edellytys</span><span class="sxs-lookup"><span data-stu-id="461f8-108">Prerequisite</span></span>                                                            | <span data-ttu-id="461f8-109">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="461f8-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="461f8-110">Määritä vähimmäishyvityksen määrä yritykselle.</span><span class="sxs-lookup"><span data-stu-id="461f8-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="461f8-111">**Myyntireskontran parametrit** -sivulla **Yleiset**-alueella **Vähimmäissumma**-kentässä, syötä vähimmäissumma, joka voidaan korvata asiakkaan liikamaksuista.</span><span class="sxs-lookup"><span data-stu-id="461f8-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="461f8-112">Valinnainen: Lisää toimittajatili jokaiselle asiakkaalle, jolle voidaan hyvittää.</span><span class="sxs-lookup"><span data-stu-id="461f8-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="461f8-113">**Asiakkaiden** sivulla **Muut tiedot** -pikavälilehdessä **Toimittajatili**-kentässä, valitse toimittajatili asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="461f8-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="461f8-114">Luodessasi hyvitystapahtumia toimittajalasku luodaan maksettavan saldon määrälle.</span><span class="sxs-lookup"><span data-stu-id="461f8-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="461f8-115">Takaisinmaksuprosessi poistaa asiakastilin luottosaldon ja luo toimittajatilille erääntyvän saldon, joka vastaa asiakasta.</span><span class="sxs-lookup"><span data-stu-id="461f8-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="461f8-116">Suorita myyntireskontrassa **Hyvitys**-prosessi (**Myyntireskontra \> Kausittaiset tehtävät \> Hyvitys**).</span><span class="sxs-lookup"><span data-stu-id="461f8-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="461f8-117">Jos haluat ryhmitellä kaikki tapahtumat kirjauskansion dimensioista huolimatta, määritä **Asiakasyhteenveto**-vaihtoehdon arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="461f8-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="461f8-118">Voit ryhmitellä vain sellaisia tapahtumia, joilla on samanlaiset kirjanpitodimensiot, määrittämällä arvoksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="461f8-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="461f8-119">Valitse **Sisällytä asiakkaat, joilla on avoimia veloitustapahtumia**, jos haluat valita asiakkaat, joilla on selvittämättömiä veloitussummia.</span><span class="sxs-lookup"><span data-stu-id="461f8-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="461f8-120">Jos haluat hyvittää tiettyjä asiakastilejä, valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** ja määritä sitten asiakastilit kyselyssä.</span><span class="sxs-lookup"><span data-stu-id="461f8-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="461f8-121">Hyvityssummat siirretään asiakkaiden toimittajanumeroille. Ne käsitellään tavallisina maksuina.</span><span class="sxs-lookup"><span data-stu-id="461f8-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="461f8-122">Jos asiakkaalla ei ole toimittajatiliä, ohjelma luo asiakkaalle automaattisesti kertatoimittajatilin.</span><span class="sxs-lookup"><span data-stu-id="461f8-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="461f8-123">Voit tarkastella luotuja hyvitystapahtumia käyttämällä **Hyvitys**-raporttia (**Myyntireskontra \> Kyselyt ja raportit \> Hyvitys-raportti**).</span><span class="sxs-lookup"><span data-stu-id="461f8-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="461f8-124">Ostoreskontrassa, luo maksu toimittajan laskuille, jotka luotiin hyvitysprosessiin maksun luomisessa.</span><span class="sxs-lookup"><span data-stu-id="461f8-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="461f8-125">Lisätietoja toimittajille maksamisesta on kohdassa [Toimittajan maksun yhteenveto](../accounts-payable/Vendor-payments-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="461f8-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]