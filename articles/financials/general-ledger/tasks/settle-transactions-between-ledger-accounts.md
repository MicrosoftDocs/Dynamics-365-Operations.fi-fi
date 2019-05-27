---
title: Tapahtumien selvitys kirjanpitotilien välillä
description: Tässä menettelyssä käsitellään, miten kirjanpitotilien väliset tapahtumien tilitetään ja miten kirjanpidon tilitys peruutetaan.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4aff64fa1c017f295752e913de7fb320f0662ef8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568117"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="85f59-103">Tapahtumien selvitys kirjanpitotilien välillä</span><span class="sxs-lookup"><span data-stu-id="85f59-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85f59-104">Tässä menettelyssä käsitellään, miten kirjanpitotilien väliset tapahtumien tilitetään ja miten kirjanpidon tilitys peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="85f59-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="85f59-105">Menettely käyttää USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="85f59-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="85f59-106">Tilitä kirjanpitotilien välinen tapahtuma</span><span class="sxs-lookup"><span data-stu-id="85f59-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="85f59-107">Valitse Kirjanpito > Kausittaiset tehtävät > Tapahtuman selvitykset.</span><span class="sxs-lookup"><span data-stu-id="85f59-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="85f59-108">Etsi tilitettävä tapahtuma luettelosta.</span><span class="sxs-lookup"><span data-stu-id="85f59-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="85f59-109">Summan saldon on oltava nolla.</span><span class="sxs-lookup"><span data-stu-id="85f59-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="85f59-110">Valitse Sisällytä.</span><span class="sxs-lookup"><span data-stu-id="85f59-110">Click Include.</span></span>
4. <span data-ttu-id="85f59-111">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="85f59-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="85f59-112">Tapahtuman selvityksen peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="85f59-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="85f59-113">Valitse Kirjanpito > Kyselyt ja raportit > Pääkirja.</span><span class="sxs-lookup"><span data-stu-id="85f59-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="85f59-114">Avaa valintaikkuna valitsemalla Parametrit.</span><span class="sxs-lookup"><span data-stu-id="85f59-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="85f59-115">Valitse Päivitä.</span><span class="sxs-lookup"><span data-stu-id="85f59-115">Click Update.</span></span>
4. <span data-ttu-id="85f59-116">Etsi luettelosta tili, jossa on tilitetty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="85f59-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="85f59-117">Valitse Kaikki tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="85f59-117">Click All transactions.</span></span>
6. <span data-ttu-id="85f59-118">Suodattimen käyttö nopeuttaa tapahtuman etsimistä luettelosta.</span><span class="sxs-lookup"><span data-stu-id="85f59-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="85f59-119">Valitse Tapahtuman selvitykset.</span><span class="sxs-lookup"><span data-stu-id="85f59-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="85f59-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="85f59-120">In the list, mark the selected row.</span></span>

