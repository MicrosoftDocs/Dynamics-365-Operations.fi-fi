---
title: Tuotteita ja luokkia puuttuu ympäristön kopioinnin jälkeen
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun tuotteet ja luokat puuttuvat, kun sivusto on kopioitu eri ympäristöstä tai samassa ympäristössä.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35f2cbd98a91149395f40bf821c1d5d7e58eaf77
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585311"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="5e452-103">Tuotteita ja luokkia puuttuu ympäristön kopioinnin jälkeen</span><span class="sxs-lookup"><span data-stu-id="5e452-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5e452-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun tuotteet ja luokat puuttuvat, kun sivusto on kopioitu eri ympäristöstä tai samassa ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="5e452-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="5e452-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="5e452-105">Description</span></span>

<span data-ttu-id="5e452-106">Kun sivusto on kopioitu ympäristöstä toiseen tai samassa ympäristössä, tuotteet ja luokat puuttuvat sivustosta.</span><span class="sxs-lookup"><span data-stu-id="5e452-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="5e452-107">Tuotteet ja luokat puuttuvat verkkokaupasta ja Commercen sivuston luontiohjelman **Tuotteet**-välilehdestä.</span><span class="sxs-lookup"><span data-stu-id="5e452-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="5e452-108">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="5e452-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="5e452-109">Kanavan toimintayksikkönumeron määritys juuri kopioituun sivustoon Commercen sivuston luontiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="5e452-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="5e452-110">Voit määrittää kanavan toimintayksikkönumeron (OUN) juuri kopioituun sivustoon Commercen sivuston luontiohjelmassa toimimalla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5e452-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5e452-111">Valitse juuri kopioitu sivusto.</span><span class="sxs-lookup"><span data-stu-id="5e452-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="5e452-112">Valitse **Sivuston asetukset** -kohdassa **Kanavat**.</span><span class="sxs-lookup"><span data-stu-id="5e452-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="5e452-113">Valitse kanavan nimen vieressä kolme pistettä (**...**) ja valitse sitten **Vaihda verkkokaupan kanava**.</span><span class="sxs-lookup"><span data-stu-id="5e452-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="5e452-114">Valitse **Vaihda verkkokaupan kanava** -valintaikkunassa kanava, johon haluat yhdistää juuri kopioidun sivuston, ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e452-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="5e452-115">Valitse **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="5e452-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e452-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5e452-116">Additional resources</span></span>

[<span data-ttu-id="5e452-117">Dynamics 365 Commerce -sivuston liittäminen online-kanavaan</span><span class="sxs-lookup"><span data-stu-id="5e452-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)
