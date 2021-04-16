---
title: Rinnakkaisten tehtävien määrittäminen työnkulussa
description: Rinnakkaisen tehtävän määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa .
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1a47857cbe65c00ad678b2b0372c642abf01b41
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747828"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="75e53-103">Rinnakkaisten tehtävien määrittäminen työnkulussa</span><span class="sxs-lookup"><span data-stu-id="75e53-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75e53-104">Rinnakkaisen tehtävän määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa .</span><span class="sxs-lookup"><span data-stu-id="75e53-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="75e53-105">Rinnakkainen tehtävä sisältää työnkulun haarat, jotka suoritetaan samaan aikaan.</span><span class="sxs-lookup"><span data-stu-id="75e53-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="75e53-106">Nimeä rinnakkainen tehtävä</span><span class="sxs-lookup"><span data-stu-id="75e53-106">Name a parallel activity</span></span>

<span data-ttu-id="75e53-107">Kirjoita näiden ohjeiden avulla nimi rinnakkaiselle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="75e53-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="75e53-108">Napsauta rinnakkaista tehtävää hiiren kakkospainikkeella ja valitse sitten **Ominaisuudet**, joka avaa **Ominaisuudet** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="75e53-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="75e53-109">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="75e53-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="75e53-110">Kirjoita rinnakkaisen tehtävän yksilöivä nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="75e53-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="75e53-111">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="75e53-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="75e53-112">Määritä rinnakkaisen tehtävän haarat</span><span class="sxs-lookup"><span data-stu-id="75e53-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="75e53-113">Voit lisätä ja konfiguroida rinnakkaisen tehtävän haaroja seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="75e53-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="75e53-114">Kaksoisnapsauttamalla rinnakkaista tehtävää saat näkyviin sen haarat.</span><span class="sxs-lookup"><span data-stu-id="75e53-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="75e53-115">Lisää haara vetämällä **haara**-elementti **Työnkulkuelementit** alueesta alustan lisäyspisteeseen.</span><span class="sxs-lookup"><span data-stu-id="75e53-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="75e53-116">Lisäyspiste näkyy seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="75e53-116">The following figure shows an insertion point.</span></span>

    ![Lisäyspiste](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="75e53-118">Haarojen järjestyksellä ei ole merkitystä, koska rinnakkaisen tehtävän haarat suoritetaan samaan aikaan.</span><span class="sxs-lookup"><span data-stu-id="75e53-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="75e53-119">Lisätietoja haarojen määrittämisestä on kohdassa [Työnkulun rinnakkaishaarojen määrittäminen](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="75e53-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]