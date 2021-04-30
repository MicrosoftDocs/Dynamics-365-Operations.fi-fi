---
title: Numerosarjojen määrittäminen
description: Tässä ohjeaiheessa selitetään, miten vuokratunnuksille luodaan numerosarjat. Siinä kerrotaan myös, miten indeksin uudelleenarvostusprosessissa käytettäviä yksilöiviä tunnuksia luodaan.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 331542811b2ba9399185478b6d25d1a57fce3a05
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881081"
---
# <a name="assign-number-sequences"></a><span data-ttu-id="72488-104">Numerosarjojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="72488-104">Assign number sequences</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="72488-105">Tässä ohjeaiheessa selitetään, miten vuokratunnuksille luodaan numerosarjat.</span><span class="sxs-lookup"><span data-stu-id="72488-105">This topic explains how to create number sequences for lease IDs.</span></span> <span data-ttu-id="72488-106">Siinä kerrotaan myös, miten indeksin uudelleenarvostusprosessissa käytettäviä yksilöiviä tunnuksia luodaan.</span><span class="sxs-lookup"><span data-stu-id="72488-106">It also explains how to create unique IDs that are used in the index revaluation process.</span></span>

1. <span data-ttu-id="72488-107">Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Resurssin vuokrausparametrit**.</span><span class="sxs-lookup"><span data-stu-id="72488-107">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="72488-108">Valitse **Numerosarjat**-sivuvälilehti.</span><span class="sxs-lookup"><span data-stu-id="72488-108">Select the **Number sequences** side tab.</span></span>
3. <span data-ttu-id="72488-109">Valitse **Numerosarjat** sivupalkissa.</span><span class="sxs-lookup"><span data-stu-id="72488-109">Select **Number sequences** in the side bar.</span></span>
4. <span data-ttu-id="72488-110">Valitse numerosarja **vuokratunnuksen** viitteelle.</span><span class="sxs-lookup"><span data-stu-id="72488-110">Select the number sequence for the **Lease ID** reference.</span></span> <span data-ttu-id="72488-111">Tämän numerosarjan avulla luodaan kunkin vuokrauksen yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="72488-111">This number sequence will be used to generate the unique identifier for each lease.</span></span>
5. <span data-ttu-id="72488-112">Valitse numerosarja **prosessitunnuksen** viitteelle.</span><span class="sxs-lookup"><span data-stu-id="72488-112">Select the number sequence for the **Process ID** reference.</span></span> <span data-ttu-id="72488-113">Tämän numerosarjan avulla luodaan kunkin indeksin uudelleenarvostusprosessin yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="72488-113">This number sequence will be used to generate the unique identifier for each index revaluation process.</span></span>
6. <span data-ttu-id="72488-114">Valitse numerosarja **Irtisanomisehdotuksen tunnus** -viitteelle.</span><span class="sxs-lookup"><span data-stu-id="72488-114">Select the number sequence for the **Termination Proposal ID** reference.</span></span> <span data-ttu-id="72488-115">Tämän numerosarjan avulla luodaan kunkin irtisanomisehdotuksen yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="72488-115">This number sequence will be used to generate the unique identifier for each termination proposal.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
