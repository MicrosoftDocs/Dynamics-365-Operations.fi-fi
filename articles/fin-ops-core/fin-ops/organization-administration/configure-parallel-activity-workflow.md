---
title: Rinnakkaisten tehtävien määrittäminen työnkulussa
description: Rinnakkaisen tehtävän määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa .
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11b541c3e159b2c38e4dd2fa9f2ad08e4c1e4500
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177627"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="01cc4-103">Rinnakkaisten tehtävien määrittäminen työnkulussa</span><span class="sxs-lookup"><span data-stu-id="01cc4-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01cc4-104">Rinnakkaisen tehtävän määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa .</span><span class="sxs-lookup"><span data-stu-id="01cc4-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="01cc4-105">Rinnakkainen tehtävä sisältää työnkulun haarat, jotka suoritetaan samaan aikaan.</span><span class="sxs-lookup"><span data-stu-id="01cc4-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="01cc4-106">Nimeä rinnakkainen tehtävä</span><span class="sxs-lookup"><span data-stu-id="01cc4-106">Name a parallel activity</span></span>

<span data-ttu-id="01cc4-107">Kirjoita näiden ohjeiden avulla nimi rinnakkaiselle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="01cc4-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="01cc4-108">Napsauta rinnakkaista tehtävää hiiren kakkospainikkeella ja valitse sitten **Ominaisuudet**, joka avaa **Ominaisuudet** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="01cc4-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="01cc4-109">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="01cc4-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="01cc4-110">Kirjoita rinnakkaisen tehtävän yksilöivä nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="01cc4-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="01cc4-111">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="01cc4-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="01cc4-112">Määritä rinnakkaisen tehtävän haarat</span><span class="sxs-lookup"><span data-stu-id="01cc4-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="01cc4-113">Voit lisätä ja konfiguroida rinnakkaisen tehtävän haaroja seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="01cc4-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="01cc4-114">Kaksoisnapsauttamalla rinnakkaista tehtävää saat näkyviin sen haarat.</span><span class="sxs-lookup"><span data-stu-id="01cc4-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="01cc4-115">Lisää haara vetämällä **haara**-elementti **Työnkulkuelementit** alueesta alustan lisäyspisteeseen.</span><span class="sxs-lookup"><span data-stu-id="01cc4-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="01cc4-116">Lisäyspiste näkyy seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="01cc4-116">The following figure shows an insertion point.</span></span>

    ![Lisäyspiste](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="01cc4-118">Haarojen järjestyksellä ei ole merkitystä, koska rinnakkaisen tehtävän haarat suoritetaan samaan aikaan.</span><span class="sxs-lookup"><span data-stu-id="01cc4-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="01cc4-119">Lisätietoja haarojen määrittämisestä on kohdassa [Määritä rinnakkaishaara](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="01cc4-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>
