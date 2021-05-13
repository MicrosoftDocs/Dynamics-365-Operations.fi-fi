---
title: Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön
description: Tässä aiheessa on yhteenveto laadun ja määrityksistä poikkeamisen hallinnan ominaisuuksien määritys- ja konfigurointiprosessista Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956251"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="df576-103">Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="df576-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df576-104">Tässä aiheessa on yhteenveto laadun ja määrityksistä poikkeamisen hallinnan ominaisuuksien määritys- ja konfigurointiprosessista Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="df576-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a><span data-ttu-id="df576-105">Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="df576-105">Enable quality and nonconformance management</span></span>

<span data-ttu-id="df576-106">Ota laadunhallinta käyttöön järjestelmässä noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="df576-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="df576-107">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto ja varastonhallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="df576-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="df576-108">Määritä **Laadunhallinta**-välilehdessä **Käytä laadunhallintaa** -asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="df576-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="df576-109">Syötä työn hinta paikallisena valuuttana **Tuntihinta**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="df576-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="df576-110">Tuntihintaa käytetään määrityksistä poikkeavien toimintojen kustannusten laskentaan.</span><span class="sxs-lookup"><span data-stu-id="df576-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="df576-111">Tuntihinta ja lasketut kustannukset ovat määrityksistä poikkeamisen viitetietoja.</span><span class="sxs-lookup"><span data-stu-id="df576-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="df576-112">Ne eivät vaikuta muihin toimintoihin.</span><span class="sxs-lookup"><span data-stu-id="df576-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="df576-113">Valitse **Raportin asetukset**.</span><span class="sxs-lookup"><span data-stu-id="df576-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="df576-114">Lisää eri raporttityypeille uusia rivejä ja valitse kussakin raportissa käytettävä asiakirjatyyppi.</span><span class="sxs-lookup"><span data-stu-id="df576-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="df576-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="df576-115">Close the page.</span></span>
1. <span data-ttu-id="df576-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="df576-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="df576-117">Laadunhallinnan määritysprosessi</span><span class="sxs-lookup"><span data-stu-id="df576-117">Quality management configuration process</span></span>

<span data-ttu-id="df576-118">Ennen kuin voit aloittaa laadunhallintaominaisuuksien käytön ja luoda laatutilauksia, sinun on määritettävä järjestelmä ja edellytykset.</span><span class="sxs-lookup"><span data-stu-id="df576-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="df576-119">Tässä on luettelo vaiheista, joita tarvitaan laadunhallinnan konfiguroinnissa.</span><span class="sxs-lookup"><span data-stu-id="df576-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="df576-120">[Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="df576-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="df576-121">Valinnainen: [Testin mittavälineiden määrittäminen](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="df576-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="df576-122">[Testien määrittäminen](quality-tests.md).</span><span class="sxs-lookup"><span data-stu-id="df576-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="df576-123">[Testimuuttujien ja tulosten määrittäminen](quality-test-variables.md).</span><span class="sxs-lookup"><span data-stu-id="df576-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="df576-124">[Testiryhmien määrittäminen](quality-test-groups.md).</span><span class="sxs-lookup"><span data-stu-id="df576-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="df576-125">Valinnainen: [Laaturyhmien määrittäminen ja linkittäminen tuotteisiin](quality-groups.md).</span><span class="sxs-lookup"><span data-stu-id="df576-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="df576-126">Valinnainen: [Laatuliitosten määrittäminen](quality-associations.md).</span><span class="sxs-lookup"><span data-stu-id="df576-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="df576-127">Kun määrittäminen on valmis, voit aloittaa laatutilausten luomisen ja käsittelemisen.</span><span class="sxs-lookup"><span data-stu-id="df576-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="df576-128">Lisätietoja laatutilausten luomisesta ja käyttämisestä on kohdassa [Laatutilaukset](quality-orders.md).</span><span class="sxs-lookup"><span data-stu-id="df576-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="df576-129">Määrityksistä poikkeamisen hallinnan määritysprosessi</span><span class="sxs-lookup"><span data-stu-id="df576-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="df576-130">Ennen kuin voit aloittaa määrityksistä poikkeamisen hallinnan ominaisuuksien käytön ja luoda määrityksistä poikkeamisia, sinun on määritettävä järjestelmä ja edellytykset.</span><span class="sxs-lookup"><span data-stu-id="df576-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="df576-131">Tässä on luettelo vaiheista, joita tarvitaan määrityksistä poikkeamisen hallinnan konfiguroinnissa.</span><span class="sxs-lookup"><span data-stu-id="df576-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="df576-132">[Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="df576-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="df576-133">[Määrityksistä poikkeamisia hyväksyvien työntekijöiden määrittäminen](quality-responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="df576-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="df576-134">[Ongelmatyyppien määrittäminen](quality-problem-types.md).</span><span class="sxs-lookup"><span data-stu-id="df576-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="df576-135">[Karanteenivyöhykkeiden määrittäminen](quality-quarantine-zones.md).</span><span class="sxs-lookup"><span data-stu-id="df576-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="df576-136">[Diagnostiikkatyyppien määrittäminen](quality-diagnostic-types.md).</span><span class="sxs-lookup"><span data-stu-id="df576-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="df576-137">[Operaatioiden määrittäminen](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="df576-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="df576-138">Valinnainen: [Laatukulujen määrittäminen](quality-charges.md).</span><span class="sxs-lookup"><span data-stu-id="df576-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="df576-139">Kun määrittäminen on valmis, voit aloittaa määrityksistä poikkeamisten luomisen ja käsittelemisen.</span><span class="sxs-lookup"><span data-stu-id="df576-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="df576-140">Lisätietoja määrityksistä poikkeamisten luonnista ja käyttämisestä on kohdassa [Määrityksistä poikkeamisten luonti ja käsittely](tasks/create-process-non-conformance.md).</span><span class="sxs-lookup"><span data-stu-id="df576-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df576-141">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="df576-141">Additional resources</span></span>

- [<span data-ttu-id="df576-142">Laadunhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="df576-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="df576-143">Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="df576-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="df576-144">Laadunhallinta varastoprosesseja varten</span><span class="sxs-lookup"><span data-stu-id="df576-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
