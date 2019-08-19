---
title: Finance and Operationsin ja Common Data Servicen lähes reaaliaikainen integrointi
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 for Finance and Operationsin ja Common Data Servicen integroinnista.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797225"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a><span data-ttu-id="6210c-103">Finance and Operationsin ja Common Data Servicen lähes reaaliaikainen integrointi</span><span class="sxs-lookup"><span data-stu-id="6210c-103">Near-real-time data integration between Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="6210c-104">Nykyisessä digitaalisessa maailmassa liiketoiminnan ekosysteemit käyttävät Microsoft Dynamics 365 -sovelluspakettia kokonaisuutena.</span><span class="sxs-lookup"><span data-stu-id="6210c-104">In the current digital world, business ecosystems use the Microsoft Dynamics 365 suite as a whole.</span></span> <span data-ttu-id="6210c-105">Koska henkilöiden, asiakkaiden, operaatioiden ja esineiden internetin (IoT) laitteiden tiedot virtaavat yhteen lähteeseen, on mahdollista, että digitaaliset palautesilmukat ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6210c-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="6210c-106">Tämän kokemuksen saavuttamiseksi Dynamics 365 for Finance and Operationsin ja Dynamics 365 for Customer Engagement -sovelluksen välinen integrointi on oleellinen.</span><span class="sxs-lookup"><span data-stu-id="6210c-106">To achieve this experience, integration between Dynamics 365 for Finance and Operations and Dynamics 365 for Customer Engagement applications is essential.</span></span> <span data-ttu-id="6210c-107">Customer Engagement -sovellukset on rakennettu Common Data Servicen päälle.</span><span class="sxs-lookup"><span data-stu-id="6210c-107">Customer Engagement applications are built on top of Common Data Service.</span></span> <span data-ttu-id="6210c-108">Finance and Operationsin tietojen integrointi Common Data Servicen kanssa antaa Customer Engagement -sovelluksille mahdollisuuden kommunikoida johdonmukaisesti ja sujuvasti Finance and Operationsin kanssa.</span><span class="sxs-lookup"><span data-stu-id="6210c-108">Integration between Finance and Operations data with Common Data Service lets Customer Engagement applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="6210c-109">Finance and Operations ja Common Data Service tarjoavat lähes reaaliaikaista tietojen synkronointia Finance and Operationsin ja Customer Engagement -sovellusten välillä kaksoiskirjoituskehyksen avulla.</span><span class="sxs-lookup"><span data-stu-id="6210c-109">Finance and Operations and Common Data Service provide near-real-time data synchronization between Finance and Operations and Customer Engagement applications via a dual-write framework.</span></span> <span data-ttu-id="6210c-110">Kattavuus on laaja ja kattaa 28 Finance and Operationsin osa-aluetta.</span><span class="sxs-lookup"><span data-stu-id="6210c-110">The coverage is broad and spans 28 surface areas of Finance and Operations.</span></span> <span data-ttu-id="6210c-111">Tavoitteena on tarjota yksi yhdenmukainen Dynamics 365 -käyttäjäkokemus saumattomien tietovirtojen kautta, jotka yhdistävät liiketoimintaprosesseja eri sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="6210c-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Arkkitehtuurin yleiskuvauskaavio](media/dual-write-overview.jpg)

<span data-ttu-id="6210c-113">Asiakkaille on tarjolla seuraavat arvoehdotukset:</span><span class="sxs-lookup"><span data-stu-id="6210c-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="6210c-114">Organisaatiohierarkia Common Data Servicessa</span><span class="sxs-lookup"><span data-stu-id="6210c-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="6210c-115">Yrityksen käsite Common Data Servicessa</span><span class="sxs-lookup"><span data-stu-id="6210c-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="6210c-116">Integroidut asiakkaiden päätiedot</span><span class="sxs-lookup"><span data-stu-id="6210c-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="6210c-117">Integroidut toimittajien päätiedot</span><span class="sxs-lookup"><span data-stu-id="6210c-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="6210c-118">Yhdistetty päätuote</span><span class="sxs-lookup"><span data-stu-id="6210c-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="6210c-119">Järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="6210c-119">System requirements</span></span>

<span data-ttu-id="6210c-120">Synkroniset, kaksisuuntaiset, lähes reaaliaikaiset tietovirrat vaativat seuraavat versiot:</span><span class="sxs-lookup"><span data-stu-id="6210c-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="6210c-121">Microsoft Dynamics 365 for Finance and Operationsin versio 10.0.4 (heinäkuu 2019) ja Platform update 28 tai uudempi</span><span class="sxs-lookup"><span data-stu-id="6210c-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="6210c-122">Microsoft Dynamics 365 for Customer Engagement, Platform -versio 9.1 (4.2) tai uudempi</span><span class="sxs-lookup"><span data-stu-id="6210c-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="6210c-123">Määritysohjeet</span><span class="sxs-lookup"><span data-stu-id="6210c-123">Setup instructions</span></span>

<span data-ttu-id="6210c-124">Määritä Finance and Operationsin ja Common Data Service:n integrointi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6210c-124">Follow these steps to set up integration between Finance and Operations and Common Data Service.</span></span>
    
1. <span data-ttu-id="6210c-125">Kaksoiskirjoitusjärjestelmän asennusta varten katso [vaiheittainen opas](https://aka.ms/dualwrite-docs) kaksoiskirjoituksen esiversion julkistamisessa.</span><span class="sxs-lookup"><span data-stu-id="6210c-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="6210c-126">Lataa ja asenna ratkaisu Yammer-ryhmästä [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096).</span><span class="sxs-lookup"><span data-stu-id="6210c-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="6210c-127">Paketti sisältää viisi ratkaisua:</span><span class="sxs-lookup"><span data-stu-id="6210c-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="6210c-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="6210c-128">Dynamics365Company</span></span>
    + <span data-ttu-id="6210c-129">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="6210c-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="6210c-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="6210c-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="6210c-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="6210c-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="6210c-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="6210c-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="6210c-133">Noudata suoritusjärjestystä [alkuperäisten viitetietojen synkronoinnissa](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="6210c-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="6210c-134">Jos kohtaat kaksoiskirjoitussynkronoinnin ongelmia, katso [tietojen integroinnin vianetsintäopas](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="6210c-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6210c-135">Et voi suorittaa kaksoiskirjoitusta ja [Prospektista käteiseksi -prosessia](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="6210c-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="6210c-136">Jos käytössäsi on Prospektista käteiseksi -ratkaisu, sinun on poistettava sen asennus.</span><span class="sxs-lookup"><span data-stu-id="6210c-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="6210c-137">Sinun on myös poistettava käytöstä asiakkaan ja toimittajan kaksoiskirjoitusmallit, jotka ovat osa Prospektista käteiseksi -ratkaisua.</span><span class="sxs-lookup"><span data-stu-id="6210c-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
