---
title: Lähes reaaliaikainen tietojen integrointi Common Data Servicen kanssa
description: Tässä ohjeaiheessa on yleiskatsaus Finance and Operationsin ja Common Data Servicen integroinnista.
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
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019762"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="b983e-103">Lähes reaaliaikainen tietojen integrointi Common Data Servicen kanssa</span><span class="sxs-lookup"><span data-stu-id="b983e-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="b983e-104">Nykyisessä digitaalisessa maailmassa liiketoiminnan ekosysteemit käyttävät Microsoft Dynamics 365 -sovelluksia kokonaisuutena.</span><span class="sxs-lookup"><span data-stu-id="b983e-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="b983e-105">Koska henkilöiden, asiakkaiden, operaatioiden ja esineiden internetin (IoT) laitteiden tiedot virtaavat yhteen lähteeseen, on mahdollista, että digitaaliset palautesilmukat ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b983e-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="b983e-106">Tämän kokemuksen saavuttamiseksi Finance and Operations -sovellusten ja Dynamics 365 -sovellusten välinen integrointi on välttämätöntä.</span><span class="sxs-lookup"><span data-stu-id="b983e-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="b983e-107">Jotkin sovellukset perustuvat Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="b983e-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="b983e-108">Finance and Operations -sovellusten tietojen integrointi Common Data Serviceen sallii muiden sovellusten johdonmukaisen ja sujuvan tietojenvaihdon Finance and Operationsin kanssa.</span><span class="sxs-lookup"><span data-stu-id="b983e-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="b983e-109">Finance and Operations -sovellukset ja Common Data Service mahdollistavat lähes reaaliaikaista tietojen synkronointia Finance and Operations -sovellusten ja muiden Dynamics 365 -sovellusten välillä kaksoiskirjoituskehyksen avulla.</span><span class="sxs-lookup"><span data-stu-id="b983e-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="b983e-110">Kattavuus on laaja ja kattaa 28 sovelluksen osa-aluetta.</span><span class="sxs-lookup"><span data-stu-id="b983e-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="b983e-111">Tavoitteena on tarjota yksi yhdenmukainen Dynamics 365 -käyttäjäkokemus saumattomien tietovirtojen kautta, jotka yhdistävät liiketoimintaprosesseja eri sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="b983e-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Arkkitehtuurin yleiskuvauskaavio](media/dual-write-overview.jpg)

<span data-ttu-id="b983e-113">Käytössä on seuraavat arvoehdotukset:</span><span class="sxs-lookup"><span data-stu-id="b983e-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="b983e-114">Organisaatiohierarkia Common Data Servicessa</span><span class="sxs-lookup"><span data-stu-id="b983e-114">Organization hierarchy in Common Data Service</span></span>](organization-mapping.md)
+ [<span data-ttu-id="b983e-115">Yrityksen käsite Common Data Servicessa</span><span class="sxs-lookup"><span data-stu-id="b983e-115">Company concept in Common Data Service</span></span>](company-data.md)
+ [<span data-ttu-id="b983e-116">Integroidut asiakkaiden päätiedot</span><span class="sxs-lookup"><span data-stu-id="b983e-116">Integrated customer master</span></span>](customer-mapping.md)
+ [<span data-ttu-id="b983e-117">Integroitu kirjanpito</span><span class="sxs-lookup"><span data-stu-id="b983e-117">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="b983e-118">Yhtenäinen tuotekokemus</span><span class="sxs-lookup"><span data-stu-id="b983e-118">Unified product experience</span></span>](product-mapping.md)
+ [<span data-ttu-id="b983e-119">Integroidut toimittajien päätiedot</span><span class="sxs-lookup"><span data-stu-id="b983e-119">Integrated vendor master</span></span>](vendor-mapping.md)
+ [<span data-ttu-id="b983e-120">Integroidut toimipaikat ja varastot</span><span class="sxs-lookup"><span data-stu-id="b983e-120">Integrated sites and warehouses</span></span>](sites-warehouses-mapping.md)
+ [<span data-ttu-id="b983e-121">Integroidut veron päätiedot</span><span class="sxs-lookup"><span data-stu-id="b983e-121">Integrated tax master</span></span>](tax-mapping.md)

## <a name="system-requirements"></a><span data-ttu-id="b983e-122">Järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="b983e-122">System requirements</span></span>

<span data-ttu-id="b983e-123">Synkroniset, kaksisuuntaiset, lähes reaaliaikaiset tietovirrat vaativat seuraavat versiot:</span><span class="sxs-lookup"><span data-stu-id="b983e-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="b983e-124">Microsoft Dynamics 365 for Finance and Operationsin versio 10.0.4 (heinäkuu 2019) ja Platform update 28 tai uudempi</span><span class="sxs-lookup"><span data-stu-id="b983e-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="b983e-125">Microsoft Dynamics 365 for Customer Engagement, Platform -versio 9.1 (4.2) tai uudempi</span><span class="sxs-lookup"><span data-stu-id="b983e-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="b983e-126">Määritysohjeet</span><span class="sxs-lookup"><span data-stu-id="b983e-126">Setup instructions</span></span>

<span data-ttu-id="b983e-127">Määritä Finance and Operations -sovellusten ja Common Data Servicen välinen integrointi noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b983e-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="b983e-128">Kaksoiskirjoitusjärjestelmän asennusta varten katso [vaiheittainen opas](https://aka.ms/dualwrite-docs) kaksoiskirjoituksen esiversion julkistamisessa.</span><span class="sxs-lookup"><span data-stu-id="b983e-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="b983e-129">Lataa ja asenna ratkaisu [FIN Ops- ja CDS/CE-integraatiosta kaksoiskirjoitus-](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer-ryhmän kautta.</span><span class="sxs-lookup"><span data-stu-id="b983e-129">Download and install the solution from the [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="b983e-130">Paketti sisältää viisi ratkaisua:</span><span class="sxs-lookup"><span data-stu-id="b983e-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="b983e-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="b983e-131">Dynamics365Company</span></span>
    + <span data-ttu-id="b983e-132">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="b983e-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="b983e-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="b983e-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="b983e-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="b983e-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="b983e-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="b983e-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="b983e-136">Noudata suoritusjärjestystä [alkuperäisten viitetietojen synkronoinnissa](initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="b983e-136">Follow the execution order for [synchronizing initial reference data](initial-sync.md).</span></span>
4. <span data-ttu-id="b983e-137">Jos kohtaat kaksoiskirjoitussynkronoinnin ongelmia, katso [tietojen integroinnin vianetsintäopas](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="b983e-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b983e-138">Et voi suorittaa kaksoiskirjoitusta ja [Prospektista käteiseksi -prosessia](../../../../supply-chain/sales-marketing/prospect-to-cash.md) rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="b983e-138">You can’t run dual-write and [Prospect to cash](../../../../supply-chain/sales-marketing/prospect-to-cash.md) side-by-side.</span></span> <span data-ttu-id="b983e-139">Jos käytössäsi on Prospektista käteiseksi -ratkaisu, sinun on poistettava sen asennus.</span><span class="sxs-lookup"><span data-stu-id="b983e-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="b983e-140">Sinun on myös poistettava käytöstä asiakkaan ja toimittajan kaksoiskirjoitusmallit, jotka ovat osa Prospektista käteiseksi -ratkaisua.</span><span class="sxs-lookup"><span data-stu-id="b983e-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
