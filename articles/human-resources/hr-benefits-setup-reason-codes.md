---
title: Määritä syykoodit
description: Dynamics 365 Human Resources käyttää syykoodeja selittääkseen, miksi työntekijän edut muuttuvat.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c799a81f38a5dbd5996afbda9529fa83d7fe5cf9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468392"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="c8190-103">Määritä syykoodit</span><span class="sxs-lookup"><span data-stu-id="c8190-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c8190-104">Dynamics 365 Human Resources käyttää syykoodeja selittääkseen, miksi työntekijän edut muuttuvat.</span><span class="sxs-lookup"><span data-stu-id="c8190-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="c8190-105">Tammikuussa 2021 syykoodit siirretään **Etujen hallinta** -työtilan sijaan **Henkilöstöhallinto**-työtilaan.</span><span class="sxs-lookup"><span data-stu-id="c8190-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="c8190-106">Lisätietoja on ohjeaiheessa [Syykoodien manuaalinen siirtäminen henkilöstöhallintaan](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="c8190-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="c8190-107">Syykoodien luominen</span><span class="sxs-lookup"><span data-stu-id="c8190-107">Create reason codes</span></span>

1. <span data-ttu-id="c8190-108">Valitse **Henkilöstönhallinta**-työtilassa (tai **Etujen hallinta** -työtilassa, jos syykoodit eivät ole vielä siirtyneet), valitse **Linkit** ja valitse sitten **Syykoodit**.</span><span class="sxs-lookup"><span data-stu-id="c8190-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="c8190-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="c8190-109">Select **New**.</span></span>

3. <span data-ttu-id="c8190-110">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="c8190-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c8190-111">Kenttä</span><span class="sxs-lookup"><span data-stu-id="c8190-111">Field</span></span> | <span data-ttu-id="c8190-112">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="c8190-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c8190-113">**Syykoodi**</span><span class="sxs-lookup"><span data-stu-id="c8190-113">**Reason code**</span></span> | <span data-ttu-id="c8190-114">Yksilöivä nimi, joka ilmaisee syyn, jonka vuoksi työntekijä muuttaisi etuussuunnitelman rekisteröimisen.</span><span class="sxs-lookup"><span data-stu-id="c8190-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="c8190-115">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="c8190-115">**Description**</span></span> | <span data-ttu-id="c8190-116">Syykoodin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="c8190-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="c8190-117">Määritä **Soveltuvat skenaariot** -kohdassa **Etujen hallinta** -arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="c8190-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="c8190-118">(Ei käytössä, jos syykoodit eivät ole vielä siirtyneet **Henkilöstöhallinta**-työtilaan.)</span><span class="sxs-lookup"><span data-stu-id="c8190-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="c8190-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="c8190-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="c8190-120">Syykoodien manuaalinen siirtäminen henkilöstöhallintaan</span><span class="sxs-lookup"><span data-stu-id="c8190-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="c8190-121">Tammikuussa 2021 syykoodit siirretään **Etujen hallinta** -työtilan sijaan **Henkilöstöhallinto**-työtilaan.</span><span class="sxs-lookup"><span data-stu-id="c8190-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="c8190-122">Useimmat syykooditiedot siirtyvät automaattisesti ympäristössäsi.</span><span class="sxs-lookup"><span data-stu-id="c8190-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="c8190-123">Joitakin syykooditietoja ei ehkä siirretä.</span><span class="sxs-lookup"><span data-stu-id="c8190-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="c8190-124">Esimerkiksi syykoodien enimmäispituus on 15 merkkiä, joten yli 15 merkin pituiset syykoodit eivät siirry automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="c8190-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="c8190-125">**Etujen hallinta** -työtilan **Linkit**-sivulla näet palkissa ilmoituksen siirrosta sekä siitä, eivätkö kaikki syykoodit siirry.</span><span class="sxs-lookup"><span data-stu-id="c8190-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="c8190-126">Valitsemalla **Syykoodit** saat lisätietoja siirron tilasta.</span><span class="sxs-lookup"><span data-stu-id="c8190-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="c8190-127">[![Syykoodit](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="c8190-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="c8190-128">Valitse syykoodi, joka ei siirtynyt.</span><span class="sxs-lookup"><span data-stu-id="c8190-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="c8190-129">[![Syykoodin siirron tila](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="c8190-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="c8190-130">Valitse **Siirrä syykoodi**.</span><span class="sxs-lookup"><span data-stu-id="c8190-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="c8190-131">[![Siirrä syykoodi](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="c8190-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="c8190-132">**Edun syykoodin siirto** -ruudussa on kaksi vaihtoehtoa, joissa voit tehdä määrityksen henkilöstöhallinnan syykoodiin:</span><span class="sxs-lookup"><span data-stu-id="c8190-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="c8190-133">Jos haluat käyttää aiemmin luotua syykoodia henkilöstöhallinnassa, valitse syykoodi avattavasta **Käytä aiemmin luotua syykoodia** -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="c8190-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="c8190-134">Voit käyttää henkilöstöhallinnassa aiemmin luotua syykoodia vain, jos siihen ei ole vielä siirtynyt toista etujen hallinnan syykoodia.</span><span class="sxs-lookup"><span data-stu-id="c8190-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="c8190-135">Voit luoda uuden syykoodin henkilöstöhallinnassa kirjoittamalla uuden syykoodin **Uusi syykoodi** -kenttään ja kirjoittamalla sitten kuvauksen kohtaan **Uusi kuvaus**.</span><span class="sxs-lookup"><span data-stu-id="c8190-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="c8190-136">[![Yhdistä henkilöstönhallinnan syykoodiin](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="c8190-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="c8190-137">Kun syykoodit siirtyvät henkilöstöhallintaan, niiden käytön asetus etujen hallinnassa on automaattisesti **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="c8190-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="c8190-138">[![Syykoodin käyttö Etujen hallinnassa](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="c8190-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]