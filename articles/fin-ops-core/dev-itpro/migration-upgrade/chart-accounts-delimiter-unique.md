---
title: Tilikartan erottimen muuttaminen yksilöiväksi
description: Tässä ohjeaiheessa selitetään, minkä vuoksi tilikartan ja dimension arvoilla ei voi olla sama erotin. Erotinarvot on muutettava päivityksen jälkeen.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 2622245c7ce7213665ab32f4020c282df28cb886
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248777"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="bb2cd-104">Tilikartan erottimen muuttaminen yksilöiväksi</span><span class="sxs-lookup"><span data-stu-id="bb2cd-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb2cd-105">Microsoft Dynamics AX 2012:ssä tilikartan ja dimension arvoissa olisi mahdollista käyttää samaa erotinta.</span><span class="sxs-lookup"><span data-stu-id="bb2cd-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="bb2cd-106">Tilikartan ja dimension arvoilla ei voi olla Finance and Operationsin nykyisissä versioissa sama erotin.</span><span class="sxs-lookup"><span data-stu-id="bb2cd-106">In current versions of Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="bb2cd-107">Jos samaa erotinta käytetään kahdesti, voit muuttaa sen päivityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="bb2cd-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="bb2cd-108">Tämä toiminto ei ole saatavana seuraavissa versioissa:</span><span class="sxs-lookup"><span data-stu-id="bb2cd-108">This feature is available in the following versions:</span></span>
- <span data-ttu-id="bb2cd-109">Finance and Operations -versio 8.0</span><span class="sxs-lookup"><span data-stu-id="bb2cd-109">Finance and Operations version 8.0</span></span>
- <span data-ttu-id="bb2cd-110">Finance and Operationsin versio 7.1, KB 4094701 Taloushallinnon dimensioita ei voi kirjata, kun dimension arvot sisältävät tilikartan erottimen</span><span class="sxs-lookup"><span data-stu-id="bb2cd-110">Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="bb2cd-111">Finance and Operationsin versio 7.2, KB 4092967 Aliprojekti ei voi valita dimensiona, kun aliprojektin muoto sisältää dimension erottimen</span><span class="sxs-lookup"><span data-stu-id="bb2cd-111">Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="bb2cd-112">Erottimen päivitys</span><span class="sxs-lookup"><span data-stu-id="bb2cd-112">Update delimiter</span></span>
<span data-ttu-id="bb2cd-113">Jos tilikartan kanssa on ristiriita, tilikartan erotin ja projektin tai aliprojektin tunnuksen muoto voidaan muuttaa.</span><span class="sxs-lookup"><span data-stu-id="bb2cd-113">If there is a conflict with the chart of accounts, the chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="bb2cd-114">Muita dimension erottimia ei voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="bb2cd-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="bb2cd-115">Voit muuttaa tilikartan erottimen tehdyn päivityksen jälkeen valitsemalla **Kirjanpitoparametrit** > **Tilikartta ja dimensiot** > **Muuta erotinta**.</span><span class="sxs-lookup"><span data-stu-id="bb2cd-115">You can change the chart of accounts delimiter after upgrade in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="bb2cd-116">Jos ainoa ristiriita on projektin tai aliprojektin tunnuksen muodon kanssa, voit vaihtaa kyseisen arvon valitsemalla **Projektinhallinnan ja kirjanpidon parametrit** > **Yleiset** > **Muuta aliprojektin muotoa**.</span><span class="sxs-lookup"><span data-stu-id="bb2cd-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="bb2cd-117">Erottimen päivitystarpeen määrittäminen ympäristössä</span><span class="sxs-lookup"><span data-stu-id="bb2cd-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="bb2cd-118">Jos päivitetyn ympäristön erottimissa on ristiriita, arvojen kirjaamisessa voi esiintyä epävakautta segmentoidussa kirjauksen hallinnassa tai dimensiomerkinnän ohjauksessa.</span><span class="sxs-lookup"><span data-stu-id="bb2cd-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="bb2cd-119">Tämä tarkoittaa sitä, sinun on aina käytettävä hakuja tai lisätietoikkunaa, kun kirjaat tili- ja dimensioyhdistelmiä.</span><span class="sxs-lookup"><span data-stu-id="bb2cd-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>
