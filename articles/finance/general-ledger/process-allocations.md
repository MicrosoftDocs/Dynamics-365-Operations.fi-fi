---
title: Kohdistusten käsittely
description: Tässä artikkelissa on tietoja kohdistuksista, niiden käsittelyvaihtoehdoista Microsoft Dynamics 365 Financessa ja kohdistusten käyttämisestä budjettisuunnittelussa. Kohdistuksia käytetään jaettaessa summia useiden kirjanpitotiliyhdistelmien kesken. Niiden avulla varmistetaan, että kulut tai tuotot veloitetaan oikealta kohteelta kirjanpidossa.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c8216ebdd1f26601743e6b35849be0813d06b4a
ms.sourcegitcommit: 4676ea9646fa1a182103ecab93e78a69001f0b8d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/21/2020
ms.locfileid: "3612659"
---
# <a name="process-allocations"></a><span data-ttu-id="f6dcb-105">Kohdistusten käsittely</span><span class="sxs-lookup"><span data-stu-id="f6dcb-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6dcb-106">Tässä artikkelissa on tietoja kohdistuksista, niiden käsittelyvaihtoehdoista ja kohdistusten käyttämisestä budjettisuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="f6dcb-107">Kohdistuksia käytetään jaettaessa summia useiden kirjanpitotiliyhdistelmien kesken.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="f6dcb-108">Niiden avulla varmistetaan, että kulut tai tuotot veloitetaan oikealta kohteelta kirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="f6dcb-109">Seuraavat ominaisuudet tukevat tätä prosessia:</span><span class="sxs-lookup"><span data-stu-id="f6dcb-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="f6dcb-110">Kohdista tapahtumasummat manuaalisesti käyttämällä jako-toimintoa kirjanpidollisessa jaossa tai käyttämällä asiakirjan taloushallinnon dimension oletusarvomalleja.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="f6dcb-111">Lisätietoja on kohdassa [Kirjanpidolliset jaot](../accounts-payable/accounting-distributions.md)</span><span class="sxs-lookup"><span data-stu-id="f6dcb-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="f6dcb-112">Kohdista automaattisesti tapahtumien summat perustuen yksittäisen päätilin määritettyihin kohdistusehtoihin.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="f6dcb-113">Jokaiselle kirjauskansiolle, joka perustuu prosenttiosuuteen ja kohteen kirjanpitotiliin aina kun kirjaus täyttää lähteenä pidetyn kirjanpitotilin kriteerit, kun luodaan kohdistus tilitapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span> <span data-ttu-id="f6dcb-114">Lisätietoja on ohjeaiheessa [Päätilin kohdistusehdot](../general-ledger/main-account-allocation-terms.md)</span><span class="sxs-lookup"><span data-stu-id="f6dcb-114">For more information, see [Main account allocation terms](../general-ledger/main-account-allocation-terms.md)</span></span>
-   <span data-ttu-id="f6dcb-115">Kohdista automaattisesti kirjanpitosaldot tai summat, jotka perustuvat kiinteisiin kirjanpidon sääntöihin.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-115">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="f6dcb-116">Kirjanpidon kohdistussäännöt käsitellään sännöllisin väliajoin käyttäen kohdistuksen kirjauskansioita.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-116">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> <span data-ttu-id="f6dcb-117">Lisätietoja on kohdassa [Kohdistussäännöt](../general-ledger/ledger-allocation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="f6dcb-117">For more information, see [Allocation rules](../general-ledger/ledger-allocation-rules.md).</span></span>

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="f6dcb-118">Budjettisuunnittelun kohdistukset</span><span class="sxs-lookup"><span data-stu-id="f6dcb-118">Allocations in budget planning</span></span>

<span data-ttu-id="f6dcb-119">Kirjanpidon kohdistussääntöjä voidaan käyttää budjettisuunnitelmiin.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-119">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="f6dcb-120">Käytettäessä kirjanpidon kohdistussääntöjä budjettisuunnitelmassa, kohdistuksen säännöt toimivat samalla tavalla kuin tavallisessa kirjanpidossa, mutta lähdetietojen ja kohteen tiedot tulevat budjettisuunnitelmasta.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-120">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="f6dcb-121">Voit manuaalisesti valita kirjanpidon kohdistussäännöt, joita budjettisuunnitelmissa käytetään.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-121">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="f6dcb-122">Vaihtoehtoisesti voit käyttää kohdistusaikataulua, joka suoritetaan osana työnkulkuprosessia.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-122">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="f6dcb-123">Et voi käyttää konsernin sisäisen kirjanpidon kohdistussääntöjä budjettisuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-123">You can’t use intercompany ledger allocation rules for budget planning.</span></span>

