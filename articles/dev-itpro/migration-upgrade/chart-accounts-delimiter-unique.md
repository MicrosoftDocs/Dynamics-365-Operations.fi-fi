---
title: "Tee tilikartan erottimista yksilöiviä"
description: "Tilikartan ja dimension arvoilla ei voi olla Dynamics 365 for Finance and Operationsissa sama erotin. Erotinarvot on muutettava päivityksen jälkeen."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="b81b8-104">Tee tilikartan erottimista yksilöiviä</span><span class="sxs-lookup"><span data-stu-id="b81b8-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b81b8-105">Microsoft Dynamics AX 2012:ssä tilikartan ja dimension arvoissa olisi mahdollista käyttää samaa erotinta.</span><span class="sxs-lookup"><span data-stu-id="b81b8-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="b81b8-106">Tilikartan ja dimension arvoilla ei voi olla Dynamics 365 for Finance and Operationsissa sama erotin.</span><span class="sxs-lookup"><span data-stu-id="b81b8-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="b81b8-107">Jos samaa erotinta käytetään kahdesti, voit muuttaa sen päivityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="b81b8-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="b81b8-108">Ominaisuuden käytettävyys:</span><span class="sxs-lookup"><span data-stu-id="b81b8-108">This feature is available in:</span></span>
- <span data-ttu-id="b81b8-109">Dynamics 365 for Finance and Operations versio 8.0</span><span class="sxs-lookup"><span data-stu-id="b81b8-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="b81b8-110">Dynamics 365 for Finance and Operations versio 7.1, KB 4094701 Taloushallinnon dimensioita ei voi kirjata, kun dimension arvot sisältävät tilikartan erottimen</span><span class="sxs-lookup"><span data-stu-id="b81b8-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="b81b8-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Aliprojekti ei voi valita dimensiona, kun aliprojektin muoto sisältää dimension erottimen</span><span class="sxs-lookup"><span data-stu-id="b81b8-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="b81b8-112">Erottimen päivitys</span><span class="sxs-lookup"><span data-stu-id="b81b8-112">Update delimiter</span></span>
<span data-ttu-id="b81b8-113">Jos tilikartan kanssa on ristiriita, tilikartan erotin ja projektin tai aliprojektin tunnuksen muoto voidaan muuttaa.</span><span class="sxs-lookup"><span data-stu-id="b81b8-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="b81b8-114">Muita dimension erottimia ei voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="b81b8-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="b81b8-115">Voit muuttaa tilikartan erottimen Finance and Operationsiin tehdyn päivityksen jälkeen valitsemalla **Kirjanpitoparametrit** > **Tilikartta ja dimensiot** > **Muuta erotinta**.</span><span class="sxs-lookup"><span data-stu-id="b81b8-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="b81b8-116">Jos ainoa ristiriita on projektin tai aliprojektin tunnuksen muodon kanssa, voit vaihtaa kyseisen arvon valitsemalla **Projektinhallinnan ja kirjanpidon parametrit** > **Yleiset** > **Muuta aliprojektin muotoa**.</span><span class="sxs-lookup"><span data-stu-id="b81b8-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="b81b8-117">Erottimen päivitystarpeen määrittäminen ympäristössä</span><span class="sxs-lookup"><span data-stu-id="b81b8-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="b81b8-118">Jos päivitetyn ympäristön erottimissa on ristiriita, arvojen kirjaamisessa voi esiintyä epävakautta segmentoidussa kirjauksen hallinnassa tai dimensiomerkinnän ohjauksessa.</span><span class="sxs-lookup"><span data-stu-id="b81b8-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="b81b8-119">Tämä tarkoittaa sitä, sinun on aina käytettävä hakuja tai lisätietoikkunaa, kun kirjaat tili- ja dimensioyhdistelmiä.</span><span class="sxs-lookup"><span data-stu-id="b81b8-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>

