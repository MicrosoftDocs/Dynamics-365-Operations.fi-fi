---
title: Valittua kaavan numeroa ei ole hyväksytty erätilaukseen
description: Kun yrität vahvistaa suunnitellun tilauksen, näyttöön tulee virhesanoma, jossa todetaan, että valittua kaavan numeroa ei ole hyväksytty erätilauksen osalta.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294061"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="ba044-103">Valittua kaavan numeroa ei ole hyväksytty erätilaukseen</span><span class="sxs-lookup"><span data-stu-id="ba044-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="ba044-104">Virhekoodi: PRO2614</span><span class="sxs-lookup"><span data-stu-id="ba044-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="ba044-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="ba044-105">Symptoms</span></span>

<span data-ttu-id="ba044-106">Kun yrität vahvistaa suunnitellun tilauksen, näyttöön tulee seuraava virhesanoma:</span><span class="sxs-lookup"><span data-stu-id="ba044-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="ba044-107">Valittua reseptin numeroa ei ole hyväksytty erätilaukseen.</span><span class="sxs-lookup"><span data-stu-id="ba044-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="ba044-108">Syy</span><span class="sxs-lookup"><span data-stu-id="ba044-108">Cause</span></span>

<span data-ttu-id="ba044-109">Järjestelmä tarkistaa vahvistustoiminnon ja varmistaa, että aktiiviselle nimikkeelle on käytettävissä hyväksytty kaava.</span><span class="sxs-lookup"><span data-stu-id="ba044-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="ba044-110">Kaava on todennäköisesti hyväksyttävä.</span><span class="sxs-lookup"><span data-stu-id="ba044-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="ba044-111">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ba044-111">Resolution</span></span>

<span data-ttu-id="ba044-112">Voit hyväksyä kaavan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="ba044-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="ba044-113">Valitse **Tuotetietojen hallinta \> Tuoterakenteet ja kaavat \> Kaavat**.</span><span class="sxs-lookup"><span data-stu-id="ba044-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="ba044-114">Valitse haluamasi kaava.</span><span class="sxs-lookup"><span data-stu-id="ba044-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="ba044-115">Valitse toimintoruudun **Kaava**-välilehden **Ylläpidä**-ryhmässä **Hyväksy kaava**.</span><span class="sxs-lookup"><span data-stu-id="ba044-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="ba044-116">Valitse **Hyväksy tuoterakenne tai kaava** -valintaikkunassa hyväksyjä ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="ba044-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>
