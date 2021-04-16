---
title: Määritä rinnakkaiset haarat työnkulussa
description: Rinnakkaisen haaran määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa .
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b5270660f0dbe4351f0088787468a563d2f36cf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747804"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="b906b-103">Määritä rinnakkaiset haarat työnkulussa</span><span class="sxs-lookup"><span data-stu-id="b906b-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b906b-104">Rinnakkaisen haaran määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa .</span><span class="sxs-lookup"><span data-stu-id="b906b-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="b906b-105">Rinnakkainen haara on käytännössä työnkulku, joka suoritetaan ylätason työnkulun kontekstissa.</span><span class="sxs-lookup"><span data-stu-id="b906b-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="b906b-106">Nimeä haara</span><span class="sxs-lookup"><span data-stu-id="b906b-106">Name a branch</span></span>

<span data-ttu-id="b906b-107">Kirjoita näiden ohjeiden avulla nimi rinnakkaiselle haaralle.</span><span class="sxs-lookup"><span data-stu-id="b906b-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="b906b-108">Napsauta rinnakkaista haaraa hiiren kakkospainikkeella ja valitse **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="b906b-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="b906b-109">**Ominaisuudet**-lomake tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="b906b-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="b906b-110">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="b906b-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="b906b-111">Kirjoita rinnakkaisen haaran yksilöivä nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b906b-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="b906b-112">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="b906b-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="b906b-113">Suunnittele ja konfiguroi haaran elementit</span><span class="sxs-lookup"><span data-stu-id="b906b-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="b906b-114">Voit suunnitella ja konfiguroida rinnakkaisen haaran elementtejä seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b906b-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="b906b-115">Kaksoisnapsauta rinnakkaisia haaraa.</span><span class="sxs-lookup"><span data-stu-id="b906b-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="b906b-116">Vedä työnkulkuelementit alustalle ja määritä elementit samoin kuin luotaessa muita työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="b906b-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="b906b-117">Lisätietoja on kohdassa [Työnkulujen luonnin yleiskatsaus](create-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="b906b-117">For more information, see [Create workflows overview](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b906b-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b906b-118">Additional resources</span></span>

[<span data-ttu-id="b906b-119">Työnkulkujen luonnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b906b-119">Create workflows overview</span></span>](create-workflow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]