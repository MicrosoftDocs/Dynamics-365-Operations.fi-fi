---
title: Kanta-asiakaskortit ja palkkiopisteet
description: Tässä ohjeaiheessa käsitellään asiakkaan kanta-asiakaskorttien ja palkkiopisteiden tietojen integrointia Finance and Operations -sovellusten ja Common Data Servicen välillä.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172966"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="e63ea-103">Kanta-asiakaskortit ja palkkiopisteet</span><span class="sxs-lookup"><span data-stu-id="e63ea-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e63ea-104">Yritykset luokittelevat asiakkaat ja tarjoavat kehittyneitä palveluita asiakkaan ostosten ja kulutustottumusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="e63ea-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="e63ea-105">Microsoft Dynamics 365 -ohjelmistopaketissa Dynamics 365 Commerce sisältää infrastruktuurin ja toiminnot, jotka helpottavat ja käsittelevät asiakkaan kanta-asiakaskortteja, palkkiopisteitä, kanta-asiakashinnoittelun ja palkkiopohjaisia ostoskokemuksia.</span><span class="sxs-lookup"><span data-stu-id="e63ea-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="e63ea-106">Kun asiakkaan kanta-asiakaskorttien ja palkkiopisteiden tiedot synkronoidaan Common Data serviceen, Dynamics 365 -järjestelmän mallipohjaiset sovellukset voivat käyttää näitä tietoja.</span><span class="sxs-lookup"><span data-stu-id="e63ea-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="e63ea-107">Esimerkiksi Dynamics 365 Customer Servicen käyttäjät voivat käyttää tietoja tarjotakseen samoja kehittyneitä palveluita tukipalvelun kautta.</span><span class="sxs-lookup"><span data-stu-id="e63ea-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="e63ea-108">Mallipohjat</span><span class="sxs-lookup"><span data-stu-id="e63ea-108">Templates</span></span>

| <span data-ttu-id="e63ea-109">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="e63ea-109">Finance and Operations apps</span></span> | <span data-ttu-id="e63ea-110">Dynamics 365:n mallipohjaiset sovellukset</span><span class="sxs-lookup"><span data-stu-id="e63ea-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="e63ea-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="e63ea-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="e63ea-112">Kanta-asiakaskortti</span><span class="sxs-lookup"><span data-stu-id="e63ea-112">Loyalty card</span></span>                | <span data-ttu-id="e63ea-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="e63ea-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="e63ea-114">Tämä malli synkronoi tietoja asiakkaan kanta-asiakaskorteista.</span><span class="sxs-lookup"><span data-stu-id="e63ea-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="e63ea-115">Kanta-asiakkaan palkkiopisteet</span><span class="sxs-lookup"><span data-stu-id="e63ea-115">Loyalty reward points</span></span>       | <span data-ttu-id="e63ea-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="e63ea-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="e63ea-117">Tämä malli synkronoi tietoja asiakkaan palkkiopisteistä.</span><span class="sxs-lookup"><span data-stu-id="e63ea-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
