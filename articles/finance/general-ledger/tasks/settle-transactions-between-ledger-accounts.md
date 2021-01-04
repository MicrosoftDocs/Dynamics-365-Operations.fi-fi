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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb53e9fee35712343f034389f00f3d4539cc652d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442791"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="a84db-103">Tapahtumien selvitys kirjanpitotilien välillä</span><span class="sxs-lookup"><span data-stu-id="a84db-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a84db-104">Tässä menettelyssä käsitellään, miten kirjanpitotilien väliset tapahtumien tilitetään ja miten kirjanpidon tilitys peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="a84db-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="a84db-105">Menettely käyttää USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="a84db-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="a84db-106">Tilitä kirjanpitotilien välinen tapahtuma</span><span class="sxs-lookup"><span data-stu-id="a84db-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="a84db-107">Valitse Kirjanpito > Kausittaiset tehtävät > Tapahtuman selvitykset.</span><span class="sxs-lookup"><span data-stu-id="a84db-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="a84db-108">Etsi tilitettävä tapahtuma luettelosta.</span><span class="sxs-lookup"><span data-stu-id="a84db-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="a84db-109">Summan saldon on oltava nolla.</span><span class="sxs-lookup"><span data-stu-id="a84db-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="a84db-110">Valitse Sisällytä.</span><span class="sxs-lookup"><span data-stu-id="a84db-110">Click Include.</span></span>
4. <span data-ttu-id="a84db-111">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="a84db-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="a84db-112">Tapahtuman selvityksen peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="a84db-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="a84db-113">Valitse Kirjanpito > Kyselyt ja raportit > Pääkirja.</span><span class="sxs-lookup"><span data-stu-id="a84db-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="a84db-114">Avaa valintaikkuna valitsemalla Parametrit.</span><span class="sxs-lookup"><span data-stu-id="a84db-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="a84db-115">Valitse Päivitä.</span><span class="sxs-lookup"><span data-stu-id="a84db-115">Click Update.</span></span>
4. <span data-ttu-id="a84db-116">Etsi luettelosta tili, jossa on tilitetty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="a84db-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="a84db-117">Valitse Kaikki tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="a84db-117">Click All transactions.</span></span>
6. <span data-ttu-id="a84db-118">Suodattimen käyttö nopeuttaa tapahtuman etsimistä luettelosta.</span><span class="sxs-lookup"><span data-stu-id="a84db-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="a84db-119">Valitse Tapahtuman selvitykset.</span><span class="sxs-lookup"><span data-stu-id="a84db-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="a84db-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a84db-120">In the list, mark the selected row.</span></span>

