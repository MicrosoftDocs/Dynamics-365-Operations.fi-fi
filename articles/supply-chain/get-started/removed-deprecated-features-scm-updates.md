---
title: Poistetut tai vanhentuneet Dynamics 365 Supply Chain Management -ominaisuudet
description: Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Supply Chain Managementsta.
author: kamaybac
manager: AnnBe
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7502cd16129431d41d152508fb3b49ff85a5a9f8
ms.sourcegitcommit: f1db998ecfccca660eb15cc2739b12c8463fa54d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331245"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="2a6ed-103">Poistetut tai vanhentuneet Dynamics 365 Supply Chain Management -ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="2a6ed-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a6ed-104">Tämä ohjeaihe päivitetään, koska Dynamics 365 Supply Chain Managementissa on uusia poistettuja tai vanhentuneita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="2a6ed-105">*Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="2a6ed-106">*Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="2a6ed-107">Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="2a6ed-108">Seuraavissa raporteissa on tarkempia tietoja Finance and Operations -sovellusten objekteista: [Teknisten tietojen raportit](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="2a6ed-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="2a6ed-109">Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin Finance and Operations -sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="2a6ed-110">Supply Chain Managementin version 10.0.11 poistetut tai vanhentuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="2a6ed-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="2a6ed-111">Supply Chain Managementin sisäisen pääsuunnittelumoduulin käyttö jakeluskenaarioissa</span><span class="sxs-lookup"><span data-stu-id="2a6ed-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="2a6ed-112">**Poiston tai vanhentumisen syy**</span><span class="sxs-lookup"><span data-stu-id="2a6ed-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="2a6ed-113">Jotta suorituskyky paranisi ja SQL-tietokannan kuormitus pienenisi pääsuunnittelun aikana, sisäinen Supply Chain Managementin pääsuunnittelumoduuli korvataan suunnittelun optimoinnilla.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="2a6ed-114">Suunnittelun optimointi mahdollistaa nopeat suunnitteluajot, jotka voidaan suorittaa myös toimiston aukioloaikoina.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="2a6ed-115">Tämän ansiosta suunnittelijat voivat reagoida välittömästi kysynnän muutoksiin tai suunnitteluparametreihin.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="2a6ed-116">**Onko toinen ominaisuus korvannut?**</span><span class="sxs-lookup"><span data-stu-id="2a6ed-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="2a6ed-117">Kyllä, suunnittelun optimointi tulee jossain vaiheessa korvaamaan nykyisen Supply Chain Managementin sisäisen pääsuunnittelumoduulin.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="2a6ed-118">**Tuotealueet, joihin vaikutetaan**</span><span class="sxs-lookup"><span data-stu-id="2a6ed-118">**Product areas affected**</span></span>         | <span data-ttu-id="2a6ed-119">Supply Chain Management – Pääsuunnittelu</span><span class="sxs-lookup"><span data-stu-id="2a6ed-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="2a6ed-120">**Käytön asetukset**</span><span class="sxs-lookup"><span data-stu-id="2a6ed-120">**Deployment option**</span></span>              | <span data-ttu-id="2a6ed-121">Vain pilvipalvelussa.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-121">Cloud only.</span></span> <span data-ttu-id="2a6ed-122">Suunnittelun optimointia ei tueta paikallisilla käyttöönotoilla.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="2a6ed-123">**Tila**</span><span class="sxs-lookup"><span data-stu-id="2a6ed-123">**Status**</span></span>                         | <span data-ttu-id="2a6ed-124">Vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-124">Deprecated.</span></span> <span data-ttu-id="2a6ed-125">Huhtikuussa 2021 jakelu skenaarioita ei enää tueta Dynamics 365 Supply Chain Managementin sisäisellä pääsuunnittelumoduulilla.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="2a6ed-126">Jakeluskenaarioiden osalta asiakkaiden on käytettävä suunnittelun optimointia pääsuunnittelun laskennoissa.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="2a6ed-127">Lisätietoja on kohdassa [Suunnittelun optimoinnin dokumentointi](https://go.microsoft.com/fwlink/?linkid=2105830).</span><span class="sxs-lookup"><span data-stu-id="2a6ed-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="2a6ed-128">Asiakkaat, joilla on käytössä paikalliset Dynamics 365 Supply Chain Management -käyttöönotot, voivat edelleen käyttää toimitusketjun hallinnan pääsuunnittelumoduulia jakeluskenaarioissa huhtikuun 2021 jälkeen.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="2a6ed-129">Muita ominaisuuksien parannuksia ei kuitenkaan ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="2a6ed-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="2a6ed-130">Poistettujen tai vanhentuneiden toimintojen aiemmat ilmoitukset</span><span class="sxs-lookup"><span data-stu-id="2a6ed-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="2a6ed-131">Lisätietoja poistetuista tai vanhentuneista toiminnoista aiemmissa versioissa on kohdassa [Poistetut tai vanhentuneet toiminnot edellisissä versioissa](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="2a6ed-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
