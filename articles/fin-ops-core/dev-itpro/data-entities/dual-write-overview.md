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
ms.openlocfilehash: 072564446b74318ffc8e8e6ad4fd16f4421e7854
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853903"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="a831a-103">Lähes reaaliaikainen tietojen integrointi Common Data Servicen kanssa</span><span class="sxs-lookup"><span data-stu-id="a831a-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a831a-104">Nykyisessä digitaalisessa maailmassa liiketoiminnan ekosysteemit käyttävät Microsoft Dynamics 365 -sovelluksia kokonaisuutena.</span><span class="sxs-lookup"><span data-stu-id="a831a-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="a831a-105">Koska henkilöiden, asiakkaiden, operaatioiden ja esineiden internetin (IoT) laitteiden tiedot virtaavat yhteen lähteeseen, on mahdollista, että digitaaliset palautesilmukat ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="a831a-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="a831a-106">Tämän kokemuksen saavuttamiseksi Finance and Operations -sovellusten ja Dynamics 365 -sovellusten välinen integrointi on välttämätöntä.</span><span class="sxs-lookup"><span data-stu-id="a831a-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="a831a-107">Jotkin sovellukset perustuvat Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="a831a-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="a831a-108">Finance and Operations -sovellusten tietojen ja Common Data Servicen integrointi antaa muille sovelluksille mahdollisuuden viestiä johdonmukaisesti ja sujuvasti Finance and Operationsin kanssa.</span><span class="sxs-lookup"><span data-stu-id="a831a-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="a831a-109">Finance and Operations -sovellukset ja Common Data Service mahdollistavat lähes reaaliaikaista tietojen synkronointia Finance and Operations -sovellusten ja muiden Dynamics 365 -sovellusten välillä kaksoiskirjoituskehyksen avulla.</span><span class="sxs-lookup"><span data-stu-id="a831a-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="a831a-110">Kattavuus on laaja ja kattaa 28 sovelluksen osa-aluetta.</span><span class="sxs-lookup"><span data-stu-id="a831a-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="a831a-111">Tavoitteena on tarjota yksi yhdenmukainen Dynamics 365 -käyttäjäkokemus saumattomien tietovirtojen kautta, jotka yhdistävät liiketoimintaprosesseja eri sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="a831a-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Arkkitehtuurin yleiskuvauskaavio](media/dual-write-overview.jpg)

<span data-ttu-id="a831a-113">Käytössä on seuraavat arvoehdotukset:</span><span class="sxs-lookup"><span data-stu-id="a831a-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="a831a-114">Organisaatiohierarkia Common Data Servicessa</span><span class="sxs-lookup"><span data-stu-id="a831a-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="a831a-115">Yrityksen käsite Common Data Servicessa</span><span class="sxs-lookup"><span data-stu-id="a831a-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="a831a-116">Integroidut asiakkaiden päätiedot</span><span class="sxs-lookup"><span data-stu-id="a831a-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="a831a-117">Integroitu kirjanpito</span><span class="sxs-lookup"><span data-stu-id="a831a-117">Integrated ledger</span></span>](dual-write-ledger.md)
+ [<span data-ttu-id="a831a-118">Yhtenäinen tuotekokemus</span><span class="sxs-lookup"><span data-stu-id="a831a-118">Unified product experience</span></span>](dual-write-product.md)
+ [<span data-ttu-id="a831a-119">Integroidut toimittajien päätiedot</span><span class="sxs-lookup"><span data-stu-id="a831a-119">Integrated vendor master</span></span>](dual-write-vendor.md)
+ [<span data-ttu-id="a831a-120">Integroidut toimipaikat ja varastot</span><span class="sxs-lookup"><span data-stu-id="a831a-120">Integrated sites and warehouses</span></span>](dual-write-sites-and-warehouses.md)
+ [<span data-ttu-id="a831a-121">Integroidut veron päätiedot</span><span class="sxs-lookup"><span data-stu-id="a831a-121">Integrated tax master</span></span>](dual-write-tax.md)

## <a name="system-requirements"></a><span data-ttu-id="a831a-122">Järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="a831a-122">System requirements</span></span>

<span data-ttu-id="a831a-123">Synkroniset, kaksisuuntaiset, lähes reaaliaikaiset tietovirrat vaativat seuraavat versiot:</span><span class="sxs-lookup"><span data-stu-id="a831a-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="a831a-124">Microsoft Dynamics 365 for Finance and Operationsin versio 10.0.4 (heinäkuu 2019) ja Platform update 28 tai uudempi</span><span class="sxs-lookup"><span data-stu-id="a831a-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="a831a-125">Microsoft Dynamics 365 for Customer Engagement, Platform -versio 9.1 (4.2) tai uudempi</span><span class="sxs-lookup"><span data-stu-id="a831a-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="a831a-126">Määritysohjeet</span><span class="sxs-lookup"><span data-stu-id="a831a-126">Setup instructions</span></span>

<span data-ttu-id="a831a-127">Määritä Finance and Operations -sovellusten ja Common Data Servicen integrointi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a831a-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="a831a-128">Kaksoiskirjoitusjärjestelmän asennusta varten katso [vaiheittainen opas](https://aka.ms/dualwrite-docs) kaksoiskirjoituksen esiversion julkistamisessa.</span><span class="sxs-lookup"><span data-stu-id="a831a-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="a831a-129">Lataa ja asenna ratkaisu [FIN Ops- ja CDS/CE-integraatiosta kaksoiskirjoitus-](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer-ryhmän kautta.</span><span class="sxs-lookup"><span data-stu-id="a831a-129">Download and install the solution from the [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="a831a-130">Paketti sisältää viisi ratkaisua:</span><span class="sxs-lookup"><span data-stu-id="a831a-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="a831a-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="a831a-131">Dynamics365Company</span></span>
    + <span data-ttu-id="a831a-132">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="a831a-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="a831a-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="a831a-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="a831a-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="a831a-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="a831a-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="a831a-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="a831a-136">Noudata suoritusjärjestystä [alkuperäisten viitetietojen synkronoinnissa](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="a831a-136">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="a831a-137">Jos kohtaat kaksoiskirjoitussynkronoinnin ongelmia, katso [tietojen integroinnin vianetsintäopas](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="a831a-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a831a-138">Et voi suorittaa kaksoiskirjoitusta ja [Prospektista käteiseksi -prosessia](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="a831a-138">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="a831a-139">Jos käytössäsi on Prospektista käteiseksi -ratkaisu, sinun on poistettava sen asennus.</span><span class="sxs-lookup"><span data-stu-id="a831a-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="a831a-140">Sinun on myös poistettava käytöstä asiakkaan ja toimittajan kaksoiskirjoitusmallit, jotka ovat osa Prospektista käteiseksi -ratkaisua.</span><span class="sxs-lookup"><span data-stu-id="a831a-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
