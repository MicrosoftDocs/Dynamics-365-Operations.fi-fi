---
title: Määritä syykoodit
description: Dynamics 365 Human Resources käyttää syykoodeja selittääkseen, miksi työntekijän edut muuttuvat.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6fc641233a1bd217de5b9eb6e06560b989f91c7b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056345"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="66bfc-103">Määritä syykoodit</span><span class="sxs-lookup"><span data-stu-id="66bfc-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="66bfc-104">Dynamics 365 Human Resources käyttää syykoodeja selittääkseen, miksi työntekijän edut muuttuvat.</span><span class="sxs-lookup"><span data-stu-id="66bfc-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="66bfc-105">Tammikuussa 2021 syykoodit siirretään **Etujen hallinta** -työtilan sijaan **Henkilöstöhallinto**-työtilaan.</span><span class="sxs-lookup"><span data-stu-id="66bfc-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="66bfc-106">Lisätietoja on ohjeaiheessa [Syykoodien manuaalinen siirtäminen henkilöstöhallintaan](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="66bfc-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="66bfc-107">Syykoodien luominen</span><span class="sxs-lookup"><span data-stu-id="66bfc-107">Create reason codes</span></span>

1. <span data-ttu-id="66bfc-108">Valitse **Henkilöstönhallinta**-työtilassa (tai **Etujen hallinta** -työtilassa, jos syykoodit eivät ole vielä siirtyneet), valitse **Linkit** ja valitse sitten **Syykoodit**.</span><span class="sxs-lookup"><span data-stu-id="66bfc-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="66bfc-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="66bfc-109">Select **New**.</span></span>

3. <span data-ttu-id="66bfc-110">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="66bfc-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="66bfc-111">Kenttä</span><span class="sxs-lookup"><span data-stu-id="66bfc-111">Field</span></span> | <span data-ttu-id="66bfc-112">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="66bfc-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="66bfc-113">**Syykoodi**</span><span class="sxs-lookup"><span data-stu-id="66bfc-113">**Reason code**</span></span> | <span data-ttu-id="66bfc-114">Yksilöivä nimi, joka ilmaisee syyn, jonka vuoksi työntekijä muuttaisi etuussuunnitelman rekisteröimisen.</span><span class="sxs-lookup"><span data-stu-id="66bfc-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="66bfc-115">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="66bfc-115">**Description**</span></span> | <span data-ttu-id="66bfc-116">Syykoodin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="66bfc-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="66bfc-117">Määritä **Soveltuvat skenaariot** -kohdassa **Etujen hallinta** -arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="66bfc-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="66bfc-118">(Ei käytössä, jos syykoodit eivät ole vielä siirtyneet **Henkilöstöhallinta**-työtilaan.)</span><span class="sxs-lookup"><span data-stu-id="66bfc-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="66bfc-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="66bfc-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="66bfc-120">Syykoodien manuaalinen siirtäminen henkilöstöhallintaan</span><span class="sxs-lookup"><span data-stu-id="66bfc-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="66bfc-121">Tammikuussa 2021 syykoodit siirretään **Etujen hallinta** -työtilan sijaan **Henkilöstöhallinto**-työtilaan.</span><span class="sxs-lookup"><span data-stu-id="66bfc-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="66bfc-122">Useimmat syykooditiedot siirtyvät automaattisesti ympäristössäsi.</span><span class="sxs-lookup"><span data-stu-id="66bfc-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="66bfc-123">Joitakin syykooditietoja ei ehkä siirretä.</span><span class="sxs-lookup"><span data-stu-id="66bfc-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="66bfc-124">Esimerkiksi syykoodien enimmäispituus on 15 merkkiä, joten yli 15 merkin pituiset syykoodit eivät siirry automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="66bfc-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="66bfc-125">**Etujen hallinta** -työtilan **Linkit**-sivulla näet palkissa ilmoituksen siirrosta sekä siitä, eivätkö kaikki syykoodit siirry.</span><span class="sxs-lookup"><span data-stu-id="66bfc-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="66bfc-126">Valitsemalla **Syykoodit** saat lisätietoja siirron tilasta.</span><span class="sxs-lookup"><span data-stu-id="66bfc-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="66bfc-127">[![Syykoodit](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="66bfc-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="66bfc-128">Valitse syykoodi, joka ei siirtynyt.</span><span class="sxs-lookup"><span data-stu-id="66bfc-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="66bfc-129">[![Syykoodin siirron tila](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="66bfc-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="66bfc-130">Valitse **Siirrä syykoodi**.</span><span class="sxs-lookup"><span data-stu-id="66bfc-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="66bfc-131">[![Siirrä syykoodi](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="66bfc-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="66bfc-132">**Edun syykoodin siirto** -ruudussa on kaksi vaihtoehtoa, joissa voit tehdä määrityksen henkilöstöhallinnan syykoodiin:</span><span class="sxs-lookup"><span data-stu-id="66bfc-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="66bfc-133">Jos haluat käyttää aiemmin luotua syykoodia henkilöstöhallinnassa, valitse syykoodi avattavasta **Käytä aiemmin luotua syykoodia** -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="66bfc-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="66bfc-134">Voit käyttää henkilöstöhallinnassa aiemmin luotua syykoodia vain, jos siihen ei ole vielä siirtynyt toista etujen hallinnan syykoodia.</span><span class="sxs-lookup"><span data-stu-id="66bfc-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="66bfc-135">Voit luoda uuden syykoodin henkilöstöhallinnassa kirjoittamalla uuden syykoodin **Uusi syykoodi** -kenttään ja kirjoittamalla sitten kuvauksen kohtaan **Uusi kuvaus**.</span><span class="sxs-lookup"><span data-stu-id="66bfc-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="66bfc-136">[![Yhdistä henkilöstönhallinnan syykoodiin](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="66bfc-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="66bfc-137">Kun syykoodit siirtyvät henkilöstöhallintaan, niiden käytön asetus etujen hallinnassa on automaattisesti **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="66bfc-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="66bfc-138">[![Syykoodin käyttö Etujen hallinnassa](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="66bfc-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]