---
title: Poistetut tai vanhentuneet Platform-ominaisuudet
description: Tässä ohjeaiheessa käsitellään toimintoja, jotka on poistettu tai joiden poistoa suunnitellaan Finance and Operations -sovellusten ympäristöpäivityksissä.
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087880"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="2952c-103">Poistetut tai vanhentuneet Platform-ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="2952c-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2952c-104">Tässä ohjeaiheessa käsitellään toimintoja, jotka on poistettu tai joiden poistoa suunnitellaan Finance and Operations -sovellusten ympäristöpäivityksissä.</span><span class="sxs-lookup"><span data-stu-id="2952c-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="2952c-105">*Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.</span><span class="sxs-lookup"><span data-stu-id="2952c-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="2952c-106">*Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.</span><span class="sxs-lookup"><span data-stu-id="2952c-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="2952c-107">Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi.</span><span class="sxs-lookup"><span data-stu-id="2952c-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="2952c-108">Seuraavissa raporteissa on tarkempia tietoja Finance and Operations -sovellusten objekteista: [Teknisten tietojen raportit](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="2952c-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="2952c-109">Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin Finance and Operations -sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="2952c-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="2952c-110">Ympäristön update 32 -päivitys</span><span class="sxs-lookup"><span data-stu-id="2952c-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="2952c-111">Työnkulun pyynnön muutoksen valintaikkuna ei enää sisällä käyttäjän valinnan avattavaa luetteloa</span><span class="sxs-lookup"><span data-stu-id="2952c-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="2952c-112">**Poiston tai vanhentumisen syy**</span><span class="sxs-lookup"><span data-stu-id="2952c-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="2952c-113">Tämä oli tietoturvaongelma, koska muutospyyntö voitiin lähettää väärälle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="2952c-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="2952c-114">Tämä oli myös käytettävyysongelma, koska se pakotti käyttäjän määrittämään, kuka työnkulun aloittaja on, ja manuaalisesti valitsemaan tämän.</span><span class="sxs-lookup"><span data-stu-id="2952c-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="2952c-115">**Onko toinen ominaisuus korvannut?**</span><span class="sxs-lookup"><span data-stu-id="2952c-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="2952c-116">Ei</span><span class="sxs-lookup"><span data-stu-id="2952c-116">No</span></span> |
| <span data-ttu-id="2952c-117">**Tuotealueet, joihin vaikutetaan**</span><span class="sxs-lookup"><span data-stu-id="2952c-117">**Product areas affected**</span></span>         | <span data-ttu-id="2952c-118">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="2952c-118">Workflow</span></span> |
| <span data-ttu-id="2952c-119">**Käytön asetukset**</span><span class="sxs-lookup"><span data-stu-id="2952c-119">**Deployment option**</span></span>              | <span data-ttu-id="2952c-120">Kaikki</span><span class="sxs-lookup"><span data-stu-id="2952c-120">All</span></span> |
| <span data-ttu-id="2952c-121">**Tila**</span><span class="sxs-lookup"><span data-stu-id="2952c-121">**Status**</span></span>                         | <span data-ttu-id="2952c-122">Käyttäjän valinnan avattava luettelo poistettiin pyynnön muutoksen valintaikkunasta Platform update 32 -päivityksessä.</span><span class="sxs-lookup"><span data-stu-id="2952c-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="2952c-123">Pyynnön muutospyynnöt lähetetään automaattisesti aloittajalle aiemmin määritetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="2952c-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="2952c-124">Lisätietoja tästä toiminnosta on kohdassa [Toiminnot työnkulun hyväksyntäprosesseissa](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span><span class="sxs-lookup"><span data-stu-id="2952c-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="2952c-125">Poistettujen tai vanhentuneiden toimintojen aiemmat ilmoitukset</span><span class="sxs-lookup"><span data-stu-id="2952c-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="2952c-126">Lisätietoja poistetuista tai vanhentuneista toiminnoista aiemmissa versioissa on kohdassa [Poistetut tai vanhentuneet toiminnot edellisissä versioissa](../migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="2952c-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

