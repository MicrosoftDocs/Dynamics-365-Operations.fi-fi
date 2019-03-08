---
title: Standardikustannusten päivittäminen valmistusympäristössä
description: Tämä artikkeli sisältää ohjeita vakiokustannusten päivittämiseen tuotantoympäristössä.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fccfcec3d74bd13aa1b6511ebd37ee1454d1b47b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "332354"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="b563a-103">Standardikustannusten päivittäminen valmistusympäristössä</span><span class="sxs-lookup"><span data-stu-id="b563a-103">Update standard costs in a manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b563a-104">Tämä artikkeli sisältää ohjeita vakiokustannusten päivittämiseen tuotantoympäristössä.</span><span class="sxs-lookup"><span data-stu-id="b563a-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="b563a-105">Päivitykset voivat johtua uusista nimikkeistä, kustannusluokista tai epäsuorien kustannusten laskentakaavoista.</span><span class="sxs-lookup"><span data-stu-id="b563a-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="b563a-106">Ne voivat johtua myös korjauksista ja kustannusmuutoksista.</span><span class="sxs-lookup"><span data-stu-id="b563a-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="b563a-107">Kuten seuraavista esimerkkitapauksista selviää, päivityksen tyyppi vaikuttaa siihen, mitä toimia standardikustannusten päivittäminen edellyttää.</span><span class="sxs-lookup"><span data-stu-id="b563a-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="b563a-108">Lisää ostettujen nimikkeiden odotetut standardikustannusten muutokset ja muuta sitten nimikkeen kustannustietueiden tila **aktiiviseksi** asianmukaisena päivämääränä.</span><span class="sxs-lookup"><span data-stu-id="b563a-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="b563a-109">Älä kuitenkaan laske ostettuja nimikkeitä käyttävien valmistettujen nimikkeiden kustannuksia uudelleen.</span><span class="sxs-lookup"><span data-stu-id="b563a-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="b563a-110">Lisää uuden ostetun nimikkeen standardikustannukset, mutta älä laske sellaisten valmistettujen nimikkeiden kustannuksia uudelleen, joiden tuoterakenneversiossa on uusi ostettu nimike komponenttina.</span><span class="sxs-lookup"><span data-stu-id="b563a-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="b563a-111">Korjaa tai muuta ostetun nimikkeen kustannuksia tai muuta ostettuun nimikkeeseen määritettyä kustannusryhmää. Laske myös kaikkien sellaisten valmistettujen nimikkeiden kustannukset, joiden tuoterakenneversiossa on ostettu nimike komponenttina.</span><span class="sxs-lookup"><span data-stu-id="b563a-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="b563a-112">Muuta kustannusluokan kustannusta ja laske kaikkien sellaisten valmistettujen nimikkeiden kustannukset, joiden reititysversiossa on kustannusluokkaa käyttäviä reitityksen työvaiheita.</span><span class="sxs-lookup"><span data-stu-id="b563a-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="b563a-113">Muuta kustannusluokkia, jotka on määritetty reitityksen työvaiheisiin, tai kustannusryhmää, joka on määritetty kustannusluokkiin.</span><span class="sxs-lookup"><span data-stu-id="b563a-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="b563a-114">Laske sitten kaikkien sellaisten valmistettujen nimikkeiden kustannukset, joiden reititysversiossa on kustannusluokkaa käyttäviä reitityksen työvaiheita.</span><span class="sxs-lookup"><span data-stu-id="b563a-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="b563a-115">Muuta epäsuorien kustannusten laskentakaavaa ja laske kaikkien sellaisten valmistettujen nimikkeiden kustannukset, joihin muutos vaikuttaa.</span><span class="sxs-lookup"><span data-stu-id="b563a-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="b563a-116">Muuta tai lisää valmistetulle nimikkeelle valmistustoimipaikka ja laske nimikkeen toimipaikkakohtaiset valmistuskustannukset.</span><span class="sxs-lookup"><span data-stu-id="b563a-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="b563a-117">Laske valmistetun nimikkeen kustannukset tai laske ne uudelleen. Laske sitten kaikkien sellaisten valmistettujen nimikkeiden kustannukset uudelleen, joiden tuoterakenneversiossa on valmistettu nimike komponenttina.</span><span class="sxs-lookup"><span data-stu-id="b563a-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="b563a-118">Laske uuden valmistetun nimikkeen kustannukset sen määritettyjen, hyväksyttyjen ja aktiivisten tuoterakenne- ja reititystietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="b563a-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="b563a-119">Jokainen tilanne vaatii tarkkaa harkintaa siitä, kuinka vakiokustannukset pitäisi päivittää.</span><span class="sxs-lookup"><span data-stu-id="b563a-119">Each case requires careful consideration about how to update standard costs.</span></span>



