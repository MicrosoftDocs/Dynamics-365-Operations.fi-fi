---
title: Odotuskausien määrittäminen
description: Microsoft Dynamics 365 Human Resources -ohjelmassa odotuspäivät muodostavat tavoitteen, jota käytetään etuussuunnitelmissa.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 58d96469fc953c1bbabe8e29bf9df7a8fb4a0589
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092505"
---
# <a name="configure-waiting-periods"></a><span data-ttu-id="a2c1f-103">Odotuskausien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a2c1f-103">Configure waiting periods</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a2c1f-104">Microsoft Dynamics 365 Human Resources -ohjelmassa odotuspäivät muodostavat tavoitteen, jota käytetään etuussuunnitelmissa.</span><span class="sxs-lookup"><span data-stu-id="a2c1f-104">In Microsoft Dynamics 365 Human Resources, waiting days establish a milestone to use for benefit plans.</span></span> <span data-ttu-id="a2c1f-105">Esimerkiksi kolme kuukautta työhönottopäivästä, kunkin kuukauden ensimmäinen kuukausi tai kuusi kuukautta.</span><span class="sxs-lookup"><span data-stu-id="a2c1f-105">For example, three months from hire date, the first of each month, or six months.</span></span>   

1. <span data-ttu-id="a2c1f-106">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Odotuskaudet**.</span><span class="sxs-lookup"><span data-stu-id="a2c1f-106">In the **Benefits management** workspace, under **Setup**, select **Waiting periods**.</span></span>

2. <span data-ttu-id="a2c1f-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a2c1f-107">Select **New**.</span></span>

3. <span data-ttu-id="a2c1f-108">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="a2c1f-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="a2c1f-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="a2c1f-109">Field</span></span> | <span data-ttu-id="a2c1f-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="a2c1f-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a2c1f-111">Odotuskoodi</span><span class="sxs-lookup"><span data-stu-id="a2c1f-111">Waiting code</span></span> | <span data-ttu-id="a2c1f-112">Odotuskauden yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="a2c1f-112">A unique identifier for the waiting period.</span></span> |
   | <span data-ttu-id="a2c1f-113">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="a2c1f-113">Description</span></span> | <span data-ttu-id="a2c1f-114">Odotuskauden kuvaus.</span><span class="sxs-lookup"><span data-stu-id="a2c1f-114">A description of the waiting period.</span></span> |
   | <span data-ttu-id="a2c1f-115">Odotusmenetelmä</span><span class="sxs-lookup"><span data-stu-id="a2c1f-115">Waiting method</span></span> | <span data-ttu-id="a2c1f-116">Valitse haluamasi odotusmenetelmä arvojen pudotusvalikosta.</span><span class="sxs-lookup"><span data-stu-id="a2c1f-116">Select the appropriate waiting method from the drop down list of values.</span></span> <span data-ttu-id="a2c1f-117">Vaihtoehdot ovat netto, kuluva kuukausi, kuluva vuosineljännes, kuluva vuosi ja kuluva viikko.</span><span class="sxs-lookup"><span data-stu-id="a2c1f-117">Options are Net, Current month, Current quarter, Current year, and Current week.</span></span> |
   | <span data-ttu-id="a2c1f-118">Kuukautta</span><span class="sxs-lookup"><span data-stu-id="a2c1f-118">Months</span></span> | <span data-ttu-id="a2c1f-119">Anna odotusmenetelmään odotuspäivän laskemiseksi lisättävä kuukausien määrä.</span><span class="sxs-lookup"><span data-stu-id="a2c1f-119">Enter the number of months to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="a2c1f-120">Days</span><span class="sxs-lookup"><span data-stu-id="a2c1f-120">Days</span></span> | <span data-ttu-id="a2c1f-121">Anna odotusmenetelmään odotuspäivän laskemiseksi lisättävä päivien määrä.</span><span class="sxs-lookup"><span data-stu-id="a2c1f-121">Enter the number of days to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="a2c1f-122">Odotuspäivä</span><span class="sxs-lookup"><span data-stu-id="a2c1f-122">Waiting day</span></span> | <span data-ttu-id="a2c1f-123">Valitse odotuspäivän laskemisessa käytettävä odotuspäivä.</span><span class="sxs-lookup"><span data-stu-id="a2c1f-123">Select the waiting day to use to calculate the waiting date.</span></span> |

4. <span data-ttu-id="a2c1f-124">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a2c1f-124">Select **Save**.</span></span>
