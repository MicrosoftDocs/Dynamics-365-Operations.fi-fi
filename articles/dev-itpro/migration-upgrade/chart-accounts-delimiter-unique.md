---
title: "Tilikartan erottimen on oltava yksilöivä"
description: "Tilikartan ja dimension arvoilla ei voi olla Dynamics 365 for Finance and Operationsissa sama erotin. Erotinarvot on muutettava päivityksen jälkeen."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c9728714944b54f3bff1e2a8b43c7adcf5200f08
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="chart-of-accounts-delimiter-must-be-unique"></a><span data-ttu-id="a6392-104">Tilikartan erottimen on oltava yksilöivä</span><span class="sxs-lookup"><span data-stu-id="a6392-104">Chart of accounts delimiter must be unique</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="a6392-105">Microsoft Dynamics AX 2012:ssä tilikartan ja dimension arvoissa olisi mahdollista käyttää samaa erotinta.</span><span class="sxs-lookup"><span data-stu-id="a6392-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="a6392-106">Tilikartan ja dimension arvoilla ei voi olla Dynamics 365 for Finance and Operationsissa sama erotin.</span><span class="sxs-lookup"><span data-stu-id="a6392-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="a6392-107">Jos samaa erotinta käytetään kahdesti, voit muuttaa sen päivityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="a6392-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="a6392-108">Ominaisuuden käytettävyys:</span><span class="sxs-lookup"><span data-stu-id="a6392-108">This feature is available in:</span></span>
- <span data-ttu-id="a6392-109">Dynamics 365 for Finance and Operations versio 8.0</span><span class="sxs-lookup"><span data-stu-id="a6392-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="a6392-110">Dynamics 365 for Finance and Operations versio 7.1, KB 4094701 Taloushallinnon dimensioita ei voi kirjata, kun dimension arvot sisältävät tilikartan erottimen</span><span class="sxs-lookup"><span data-stu-id="a6392-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="a6392-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Aliprojekti ei voi valita dimensiona, kun aliprojektin muoto sisältää dimension erottimen</span><span class="sxs-lookup"><span data-stu-id="a6392-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="a6392-112">Erottimen päivitys</span><span class="sxs-lookup"><span data-stu-id="a6392-112">Update delimiter</span></span>
<span data-ttu-id="a6392-113">Jos tilikartan kanssa on ristiriita, tilikartan erotin ja projektin tai aliprojektin tunnuksen muoto voidaan muuttaa.</span><span class="sxs-lookup"><span data-stu-id="a6392-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="a6392-114">Muita dimension erottimia ei voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="a6392-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="a6392-115">Voit muuttaa tilikartan erottimen Finance and Operationsiin tehdyn päivityksen jälkeen valitsemalla **Kirjanpitoparametrit** > **Tilikartta ja dimensiot** > **Muuta erotinta**.</span><span class="sxs-lookup"><span data-stu-id="a6392-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="a6392-116">Jos ainoa ristiriita on projektin tai aliprojektin tunnuksen muodon kanssa, voit vaihtaa kyseisen arvon valitsemalla **Projektinhallinnan ja kirjanpidon parametrit** > **Yleiset** > **Muuta aliprojektin muotoa**.</span><span class="sxs-lookup"><span data-stu-id="a6392-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="a6392-117">Erottimen päivitystarpeen määrittäminen ympäristössä</span><span class="sxs-lookup"><span data-stu-id="a6392-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="a6392-118">Jos päivitetyn ympäristön erottimissa on ristiriita, arvojen kirjaamisessa voi esiintyä epävakautta segmentoidussa kirjauksen hallinnassa tai dimensiomerkinnän ohjauksessa.</span><span class="sxs-lookup"><span data-stu-id="a6392-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="a6392-119">Tämä tarkoittaa sitä, sinun on aina käytettävä hakuja tai lisätietoikkunaa, kun kirjaat tili- ja dimensioyhdistelmiä.</span><span class="sxs-lookup"><span data-stu-id="a6392-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>

