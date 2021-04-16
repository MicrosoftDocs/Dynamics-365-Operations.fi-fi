---
title: Arvonlisäveron erittely kirjanpitotapahtuman mukaan -raportti
description: Tässä aiheessa selitetään, kuinka Arvonlisäveron erittely kirjanpitotapahtuman mukaan -raporttia voidaan käyttää sellaisten kirjanpitotapahtumien tietojen tarkastelemiseen ja tulostamiseen, joille on laskettu arvonlisävero.
author: ericwang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 75913edcbac0151d5d27d866ff5430b194c62738
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815257"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="4d03e-103">Arvonlisäveron erittely kirjanpitotapahtuman mukaan -raportti</span><span class="sxs-lookup"><span data-stu-id="4d03e-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d03e-104">Tässä aiheessa selitetään, kuinka **Arvonlisäveron erittely kirjanpitotapahtuman mukaan** -raporttia voidaan käyttää sellaisten kirjanpitotapahtumien tietojen tarkastelemiseen ja tulostamiseen, joille on laskettu arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="4d03e-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="4d03e-105">Verotilit vs. muut kuin verotilit</span><span class="sxs-lookup"><span data-stu-id="4d03e-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="4d03e-106">**Arvonlisäveron erittely kirjanpitotapahtuman mukaan** -raportti näyttää sekä verotilien että muiden kuin verotilien verotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="4d03e-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="4d03e-107">Nämä tilit on luokiteltu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="4d03e-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="4d03e-108">**Verotili** – Tiliä pidetään verotilinä, kun verotapahtuma kirjataan ja **Arvonlisävero**-kirjauskansiorivin päätili on verotili, kuten maksettavan arvonlisäveron tili tai saatava arvonlisäveron tili.</span><span class="sxs-lookup"><span data-stu-id="4d03e-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="4d03e-109">**Muu kuin verotili** –Tiliä pidetään muuna kuin verotilinä, kun verotapahtuma kirjataan ja alkuperäisen tapahtuman päätili on muu kuin verotili, kuten tuottotili tai kulutili.</span><span class="sxs-lookup"><span data-stu-id="4d03e-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="4d03e-110">Verotilien **Alkuperä**-, **Saatava arvonlisävero**- ja **Maksettava arvonlisävero** -sarakkeissa näytetään **0** (nolla).</span><span class="sxs-lookup"><span data-stu-id="4d03e-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="4d03e-111">Muissa kuin verotileissä näissä sarakkeissa näytetään summat.</span><span class="sxs-lookup"><span data-stu-id="4d03e-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="4d03e-112">Raportin tietojen suodattaminen</span><span class="sxs-lookup"><span data-stu-id="4d03e-112">Filtering the data on the report</span></span>

<span data-ttu-id="4d03e-113">Kun luot raportin, seuraavat oletuskentät ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="4d03e-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="4d03e-114">Voit käyttää näitä kenttiä suodattaaksesi raportissa näytettäviä tietoa.</span><span class="sxs-lookup"><span data-stu-id="4d03e-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="4d03e-115">Kenttä</span><span class="sxs-lookup"><span data-stu-id="4d03e-115">Field</span></span>                      | <span data-ttu-id="4d03e-116">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="4d03e-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="4d03e-117">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="4d03e-117">Date</span></span>                       | <span data-ttu-id="4d03e-118">Määritä verotapahtumien ajanjakso käyttämällä **Alkamispäivä**- ja **Päättymispäivä**-osioiden kenttiä.</span><span class="sxs-lookup"><span data-stu-id="4d03e-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="4d03e-119">Päätili</span><span class="sxs-lookup"><span data-stu-id="4d03e-119">Main account</span></span>               | <span data-ttu-id="4d03e-120">Määritä päätilien ajanjakso käyttämällä **Alkamispäivä**- ja **Päättymispäivä**-osioiden kenttiä.</span><span class="sxs-lookup"><span data-stu-id="4d03e-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="4d03e-121">Arvonlisäverokoodi</span><span class="sxs-lookup"><span data-stu-id="4d03e-121">Sales tax code</span></span>             | <span data-ttu-id="4d03e-122">Määritä arvonlisäverokoodien ajanjakso käyttämällä **Alkamispäivä**- ja **Päättymispäivä**-osioiden kenttiä.</span><span class="sxs-lookup"><span data-stu-id="4d03e-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="4d03e-123">Ryhmittely</span><span class="sxs-lookup"><span data-stu-id="4d03e-123">Grouping</span></span>                   | <span data-ttu-id="4d03e-124">Valitse, ryhmitetäänkö raportti kirjanpitotilin vai arvonlisäverokoodin mukaan.</span><span class="sxs-lookup"><span data-stu-id="4d03e-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="4d03e-125">Välisumma arvonlisäverokoodeittain</span><span class="sxs-lookup"><span data-stu-id="4d03e-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="4d03e-126">Määritä täksi asetukseksi **Kyllä**, jos haluat näyttää välisummat arvonlisäverokoodin mukaan.</span><span class="sxs-lookup"><span data-stu-id="4d03e-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="4d03e-127">Vain kokonaissummat</span><span class="sxs-lookup"><span data-stu-id="4d03e-127">Totals only</span></span>                | <span data-ttu-id="4d03e-128">Määritä täksi asetukseksi **Kyllä**, jos haluat näyttää vain kokonaissummat.</span><span class="sxs-lookup"><span data-stu-id="4d03e-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="4d03e-129">Vain päätilit</span><span class="sxs-lookup"><span data-stu-id="4d03e-129">Main accounts only</span></span>         | <span data-ttu-id="4d03e-130">Valitse täksi asetukseksi **Kyllä**, jos haluat sisällyttää raporttiin vain päätilit.</span><span class="sxs-lookup"><span data-stu-id="4d03e-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="4d03e-131">Vain muiden kuin verotilien näyttäminen raportissa</span><span class="sxs-lookup"><span data-stu-id="4d03e-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="4d03e-132">Jos haluat näyttää raportissa vain muut kuin verotilit, määritä suodatusehto, kuten tähtimerkki (\*), seuraavan kuvan osoittamalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="4d03e-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![Raportti, joka näyttää muut kuin verotilit](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]