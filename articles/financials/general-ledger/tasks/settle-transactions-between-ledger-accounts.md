--- 
title: "Tapahtumien selvitys kirjanpitotilien välillä"
description: "Tässä menettelyssä käsitellään, miten kirjanpitotilien väliset tapahtumien tilitetään ja miten kirjanpidon tilitys peruutetaan."
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: cf82898b6ff731433bad100b12ba48a8f42ee11b
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="51bd3-103">Tapahtumien selvitys kirjanpitotilien välillä</span><span class="sxs-lookup"><span data-stu-id="51bd3-103">Settle transactions between ledger accounts</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51bd3-104">Tässä menettelyssä käsitellään, miten kirjanpitotilien väliset tapahtumien tilitetään ja miten kirjanpidon tilitys peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="51bd3-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="51bd3-105">Menettely käyttää USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="51bd3-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="51bd3-106">Tilitä kirjanpitotilien välinen tapahtuma</span><span class="sxs-lookup"><span data-stu-id="51bd3-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="51bd3-107">Valitse Kirjanpito > Kausittaiset tehtävät > Tapahtuman selvitykset.</span><span class="sxs-lookup"><span data-stu-id="51bd3-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="51bd3-108">Etsi tilitettävä tapahtuma luettelosta.</span><span class="sxs-lookup"><span data-stu-id="51bd3-108">In the list, find the transaction that you want to settle.</span></span>
    * <span data-ttu-id="51bd3-109">Summan saldon on oltava nolla.</span><span class="sxs-lookup"><span data-stu-id="51bd3-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="51bd3-110">Valitse Sisällytä.</span><span class="sxs-lookup"><span data-stu-id="51bd3-110">Click Include.</span></span>
4. <span data-ttu-id="51bd3-111">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="51bd3-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="51bd3-112">Tapahtuman selvityksen peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="51bd3-112">Cancel a ledger settlement</span></span>
1. <span data-ttu-id="51bd3-113">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="51bd3-113">Close the page.</span></span>
2. <span data-ttu-id="51bd3-114">Valitse Kirjanpito > Kyselyt ja raportit > Pääkirja.</span><span class="sxs-lookup"><span data-stu-id="51bd3-114">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
3. <span data-ttu-id="51bd3-115">Avaa valintaikkuna valitsemalla Parametrit.</span><span class="sxs-lookup"><span data-stu-id="51bd3-115">Click Parameters to open the drop dialog.</span></span>
4. <span data-ttu-id="51bd3-116">Valitse Päivitä.</span><span class="sxs-lookup"><span data-stu-id="51bd3-116">Click Update.</span></span>
5. <span data-ttu-id="51bd3-117">Etsi luettelosta tili, jossa on tilitetty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="51bd3-117">In the list, find the account that has the settled transaction.</span></span>
6. <span data-ttu-id="51bd3-118">Valitse Kaikki tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="51bd3-118">Click All transactions.</span></span>
7. <span data-ttu-id="51bd3-119">Suodattimen käyttö nopeuttaa tapahtuman etsimistä luettelosta.</span><span class="sxs-lookup"><span data-stu-id="51bd3-119">Use a filter to easily find the transaction in the list.</span></span>
8. <span data-ttu-id="51bd3-120">Valitse Tapahtuman selvitykset.</span><span class="sxs-lookup"><span data-stu-id="51bd3-120">Click Ledger settlements.</span></span>
9. <span data-ttu-id="51bd3-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="51bd3-121">In the list, mark the selected row.</span></span>


