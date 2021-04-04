---
title: Kanta-asiakaskortit ja palkkiopisteet
description: Tässä ohjeaiheessa käsitellään asiakkaan kanta-asiakaskorttien ja palkkiopisteiden tietojen integrointia kaksoiskirjoituksella.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 39e1d5b0a73b198b164e51a18222dbd985192070
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568025"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="9bb77-103">Kanta-asiakaskortit ja palkkiopisteet</span><span class="sxs-lookup"><span data-stu-id="9bb77-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9bb77-104">Yritykset luokittelevat asiakkaat ja tarjoavat kehittyneitä palveluita asiakkaan ostosten ja kulutustottumusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="9bb77-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="9bb77-105">Esimeriksi Dynamics 365 Commerce sisältää infrastruktuurin ja toiminnot, jotka helpottavat ja käsittelevät asiakkaan kanta-asiakaskortteja, palkkiopisteitä, kanta-asiakashinnoittelun ja palkkiopohjaisia ostoskokemuksia.</span><span class="sxs-lookup"><span data-stu-id="9bb77-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="9bb77-106">Kun asiakkaan kanta-asiakaskorttien ja palkkiopisteiden tiedot synkronoidaan Dataverseen, Customer Engagement -sovellukset voivat käyttää näitä tietoja.</span><span class="sxs-lookup"><span data-stu-id="9bb77-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="9bb77-107">Esimerkiksi Dynamics 365 Customer Servicen käyttäjät voivat käyttää tietoja tarjotakseen samoja kehittyneitä palveluita tukipalvelun kautta.</span><span class="sxs-lookup"><span data-stu-id="9bb77-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="9bb77-108">Mallipohjat</span><span class="sxs-lookup"><span data-stu-id="9bb77-108">Templates</span></span>

| <span data-ttu-id="9bb77-109">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="9bb77-109">Finance and Operations apps</span></span> | <span data-ttu-id="9bb77-110">Dynamics 365:n mallipohjaiset sovellukset</span><span class="sxs-lookup"><span data-stu-id="9bb77-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="9bb77-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="9bb77-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="9bb77-112">Kanta-asiakaskortti</span><span class="sxs-lookup"><span data-stu-id="9bb77-112">Loyalty card</span></span>                | <span data-ttu-id="9bb77-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="9bb77-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="9bb77-114">Tämä malli synkronoi tietoja asiakkaan kanta-asiakaskorteista.</span><span class="sxs-lookup"><span data-stu-id="9bb77-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="9bb77-115">Kanta-asiakkaan palkkiopisteet</span><span class="sxs-lookup"><span data-stu-id="9bb77-115">Loyalty reward points</span></span>       | <span data-ttu-id="9bb77-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="9bb77-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="9bb77-117">Tämä malli synkronoi tietoja asiakkaan palkkiopisteistä.</span><span class="sxs-lookup"><span data-stu-id="9bb77-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]