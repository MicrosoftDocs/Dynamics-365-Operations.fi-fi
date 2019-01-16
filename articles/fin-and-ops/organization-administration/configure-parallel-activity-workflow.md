---
title: "Rinnakkaisten tehtävien määrittäminen työnkulussa"
description: "Rinnakkaisen tehtävän määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa ."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 01c1fa876dd66ba6f0e1cdcecff56f424e117bd9
ms.contentlocale: fi-fi
ms.lasthandoff: 12/18/2018

---

# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="1f29a-103">Rinnakkaisten tehtävien määrittäminen työnkulussa</span><span class="sxs-lookup"><span data-stu-id="1f29a-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f29a-104">Rinnakkaisen tehtävän määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa .</span><span class="sxs-lookup"><span data-stu-id="1f29a-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="1f29a-105">Rinnakkainen tehtävä sisältää työnkulun haarat, jotka suoritetaan samaan aikaan.</span><span class="sxs-lookup"><span data-stu-id="1f29a-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="1f29a-106">Nimeä rinnakkainen tehtävä</span><span class="sxs-lookup"><span data-stu-id="1f29a-106">Name a parallel activity</span></span>

<span data-ttu-id="1f29a-107">Kirjoita näiden ohjeiden avulla nimi rinnakkaiselle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="1f29a-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="1f29a-108">Napsauta rinnakkaista tehtävää hiiren kakkospainikkeella ja valitse sitten **Ominaisuudet**, joka avaa **Ominaisuudet** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="1f29a-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="1f29a-109">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="1f29a-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="1f29a-110">Kirjoita rinnakkaisen tehtävän yksilöivä nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1f29a-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="1f29a-111">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="1f29a-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="1f29a-112">Määritä rinnakkaisen tehtävän haarat</span><span class="sxs-lookup"><span data-stu-id="1f29a-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="1f29a-113">Voit lisätä ja konfiguroida rinnakkaisen tehtävän haaroja seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="1f29a-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="1f29a-114">Kaksoisnapsauttamalla rinnakkaista tehtävää saat näkyviin sen haarat.</span><span class="sxs-lookup"><span data-stu-id="1f29a-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="1f29a-115">Lisää haara vetämällä **haara**-elementti **Työnkulkuelementit** alueesta alustan lisäyspisteeseen.</span><span class="sxs-lookup"><span data-stu-id="1f29a-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="1f29a-116">Lisäyspiste näkyy seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="1f29a-116">The following figure shows an insertion point.</span></span>

    ![Lisäyspiste](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="1f29a-118">Haarojen järjestyksellä ei ole merkitystä, koska rinnakkaisen tehtävän haarat suoritetaan samaan aikaan.</span><span class="sxs-lookup"><span data-stu-id="1f29a-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="1f29a-119">Lisätietoja haarojen määrittämisestä on kohdassa [Määritä rinnakkaishaara](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="1f29a-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>

