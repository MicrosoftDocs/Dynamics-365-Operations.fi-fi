---
title: Integroitu kirjanpito
description: Tässä ohjeaiheessa käsitellään kirjanpitotietojen integraatiota Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä Dataversen avulla.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
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
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f8095b0a755e40e5665d951d33ea4ce60e749165
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567693"
---
# <a name="integrated-ledger"></a><span data-ttu-id="b9cfd-103">Integroitu kirjanpito</span><span class="sxs-lookup"><span data-stu-id="b9cfd-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="b9cfd-104">Yrityssovelluksen kirjanpitotiedot määrittävät perusasetukset sille, miten yritys harjoittaa liiketoimintaa.</span><span class="sxs-lookup"><span data-stu-id="b9cfd-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="b9cfd-105">Kirjanpitotiedot esimerkiksi kuvaavat, mitä tilikautta noudattaa sekä mitä valuuttoja ja tilejä se käyttää.</span><span class="sxs-lookup"><span data-stu-id="b9cfd-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="b9cfd-106">Tässä ohjeaiheessa käsitellään näiden perustaloustietojen integrointia.</span><span class="sxs-lookup"><span data-stu-id="b9cfd-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="b9cfd-107">Mallit</span><span class="sxs-lookup"><span data-stu-id="b9cfd-107">Templates</span></span>

<span data-ttu-id="b9cfd-108">Kirjanpitotiedot sisältävät perustaloushallinnon taulukarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b9cfd-108">Ledger data includes a collection of core financial table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="b9cfd-109">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="b9cfd-109">Finance and Operations apps</span></span>      | <span data-ttu-id="b9cfd-110">Dynamics 365:n mallipohjainen sovellus</span><span class="sxs-lookup"><span data-stu-id="b9cfd-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="b9cfd-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="b9cfd-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="b9cfd-112">Valuutat</span><span class="sxs-lookup"><span data-stu-id="b9cfd-112">Currencies</span></span>                       | <span data-ttu-id="b9cfd-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="b9cfd-113">transactioncurrencies</span></span>            |
<span data-ttu-id="b9cfd-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="b9cfd-114">FiscalCalendar</span></span>                   | <span data-ttu-id="b9cfd-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="b9cfd-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="b9cfd-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="b9cfd-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="b9cfd-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="b9cfd-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="b9cfd-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="b9cfd-118">ExchRateType</span></span>                     | <span data-ttu-id="b9cfd-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="b9cfd-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="b9cfd-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="b9cfd-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="b9cfd-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="b9cfd-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="b9cfd-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="b9cfd-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="b9cfd-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="b9cfd-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="b9cfd-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="b9cfd-124">MainAccountCategory</span></span>              | <span data-ttu-id="b9cfd-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="b9cfd-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="b9cfd-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="b9cfd-126">MainAccount</span></span>                      | <span data-ttu-id="b9cfd-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="b9cfd-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="b9cfd-128">Kirjanpito</span><span class="sxs-lookup"><span data-stu-id="b9cfd-128">Ledger</span></span>                           | <span data-ttu-id="b9cfd-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="b9cfd-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="b9cfd-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="b9cfd-130">ExchangeRates</span></span>                    | <span data-ttu-id="b9cfd-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="b9cfd-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="b9cfd-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="b9cfd-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="b9cfd-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="b9cfd-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="b9cfd-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="b9cfd-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="b9cfd-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="b9cfd-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="b9cfd-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="b9cfd-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="b9cfd-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="b9cfd-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="b9cfd-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="b9cfd-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="b9cfd-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="b9cfd-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]