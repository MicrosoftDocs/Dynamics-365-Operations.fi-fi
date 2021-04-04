---
title: Työntekijän loman hallinta
description: Hallinnoi työntekijän lomia Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42d51ffe14442e076bafc99035dbd68a555e5b92
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468056"
---
# <a name="manage-employee-leave"></a><span data-ttu-id="42d57-103">Työntekijän loman hallinta</span><span class="sxs-lookup"><span data-stu-id="42d57-103">Manage employee leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="42d57-104">Voit hallita työntekijän lomaa lomatyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="42d57-104">You can manage an employee's leave by leave type.</span></span> <span data-ttu-id="42d57-105">Tämä koskee vanhentuvia lomailmoituksia ja lomatyypin saldojen säätämistä.</span><span class="sxs-lookup"><span data-stu-id="42d57-105">This includes expiring leave enrollment and adjusting leave type balances.</span></span> 

## <a name="adjust-leave-balances"></a><span data-ttu-id="42d57-106">Loma saldojen säätäminen</span><span class="sxs-lookup"><span data-stu-id="42d57-106">Adjust leave balances</span></span>

1. <span data-ttu-id="42d57-107">Valitse työntekijän tietueesta **Loma**.</span><span class="sxs-lookup"><span data-stu-id="42d57-107">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="42d57-108">Valitse **Lomien ja poissaolojen asettaminen**.</span><span class="sxs-lookup"><span data-stu-id="42d57-108">Select **Leave and absence setup**.</span></span>

3. <span data-ttu-id="42d57-109">Valitse **Muuta saldoa**.</span><span class="sxs-lookup"><span data-stu-id="42d57-109">Select **Adjust balance**.</span></span>

4. <span data-ttu-id="42d57-110">Valitse **Poissaolon tyyppi**.</span><span class="sxs-lookup"><span data-stu-id="42d57-110">Select the **Leave type**.</span></span>

5. <span data-ttu-id="42d57-111">Syötä **Muutoksen määrä**.</span><span class="sxs-lookup"><span data-stu-id="42d57-111">Enter an **Adjustment amount**.</span></span> 

6. <span data-ttu-id="42d57-112">Vaihtoehtoisesti voit valita **Päivämäärän**.</span><span class="sxs-lookup"><span data-stu-id="42d57-112">Optionally, you can select a **Date**.</span></span> 

<span data-ttu-id="42d57-113">Voit sisällyttää syykoodin ja kommentin, kun säädät työntekijän lomasaldoa.</span><span class="sxs-lookup"><span data-stu-id="42d57-113">You can include a reason code and comment when adjusting an employee's leave balance.</span></span> 

>[!IMPORTANT]
><span data-ttu-id="42d57-114">Lomasaldojen lisätietojen tarkasteleminen esikatselussa.</span><span class="sxs-lookup"><span data-stu-id="42d57-114">Viewing additional information about leave balances is in preview.</span></span> <span data-ttu-id="42d57-115">Se on otettava käyttöön **eristysympäristössä**.</span><span class="sxs-lookup"><span data-stu-id="42d57-115">You'll need to enable it in your **Sandbox** environment.</span></span> <span data-ttu-id="42d57-116">Lisätietoja esiversio-ominaisuuksien ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="42d57-116">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br>
><span data-ttu-id="42d57-117">Kun mikä tahansa lomasaldo valitaan osoittamalla, näkyvissä ovat nyt seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="42d57-117">When hovering over any leave balance, you will now see:</span></span><br>
>- <span data-ttu-id="42d57-118">**Saatavilla**: Yhteensä tänä vuonna - Otto tänä vuonna</span><span class="sxs-lookup"><span data-stu-id="42d57-118">**Available**: Total this year - Take this year</span></span>
>- <span data-ttu-id="42d57-119">**Yhteensä tänä vuonna**: Kaikki tämän vuoden kertymät, oikaisut ja siirtokirjaukset</span><span class="sxs-lookup"><span data-stu-id="42d57-119">**Total this year**: All accruals, adjustments, and carry forward for the year</span></span>
>- <span data-ttu-id="42d57-120">**Otetut tänä vuonna**: Hyväksytyt poissaolot yhteensä</span><span class="sxs-lookup"><span data-stu-id="42d57-120">**Taken this year**: All approved time off</span></span>

## <a name="see-also"></a><span data-ttu-id="42d57-121">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="42d57-121">See also</span></span>

- [<span data-ttu-id="42d57-122">Lomien ja poissaolojen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="42d57-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="42d57-123">Loma- ja poissaolopyyntöjen hallinta</span><span class="sxs-lookup"><span data-stu-id="42d57-123">Manage leave and absence requests</span></span>](hr-employee-self-service-manage-requests.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]