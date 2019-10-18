---
title: Organisaatiohierarkia Common Data Servicessa
description: Tässä aiheessa kuvataan organisaation tietojen integraatiota Finance and Operations -sovellusten ja Common Data Servicen välillä.
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
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182022"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="9a1f5-103">Organisaatiohierarkia Common Data Servicessa</span><span class="sxs-lookup"><span data-stu-id="9a1f5-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="9a1f5-104">Koska Dynamics 365 Finance on talousjärjestelmä, *organisaatio* on keskeinen käsite ja järjestelmän asennusohjelma alkaa organisaatiohierarkian konfiguraatiosta.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="9a1f5-105">Yrityksen taloustietoja voidaan sitten seurata organisaatiotasolla ja millä tahansa organisaatiohierarkian tasolla.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="9a1f5-106">Vaikka Common Data Servicessa ei ole käsitettä organisaatiohierarkia, siinä on joitakin käsitteitä, kuten myyntituoton kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="9a1f5-107">Organisaatiohierarkian tietorakenne lisätään Common Data Service -integroinnin osana Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="9a1f5-108">Tietojen virtaus</span><span class="sxs-lookup"><span data-stu-id="9a1f5-108">Data flow</span></span>

<span data-ttu-id="9a1f5-109">Liiketoiminnan ekosysteemillä, joka koostuu Finance and Operations -sovelluksesta ja Common Data Servicesta, on jatkossakin organisaatiohierarkia.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="9a1f5-110">Tämä organisaatiohierarkia perustuu Finance and Operations -sovelluksiin, mutta se näkyy Common Data Servicessa tiedon jakamista ja laajennettavuutta varten.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="9a1f5-111">Seuraavassa kuvassa näkyy organisaatiohierarkian tiedot, jotka näkyvät Common Data Servicessa yksisuuntaisena tiedonkulkuna Finance and Operations- sovelluksista Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Arkkitehtuurikuva](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="9a1f5-113">Mallit</span><span class="sxs-lookup"><span data-stu-id="9a1f5-113">Templates</span></span>

<span data-ttu-id="9a1f5-114">Organisaatiohierarkian entiteettien yhdistämismääritykset ovat käytettävissä yksisuuntaiseen tietojen synkronointiin Finance and Operations -sovelluksista Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="9a1f5-115">Sisäinen organisaatiohierarkian tarkoitus</span><span class="sxs-lookup"><span data-stu-id="9a1f5-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="9a1f5-116">Tässä mallissa on yksisuuntainen Organisaatiohierarkian tarkoitus -yksikön synkronointi Finance and Operationsista muihin Dynamics 365 -sovelluksiin.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="9a1f5-117">Lähdetaulu</span><span class="sxs-lookup"><span data-stu-id="9a1f5-117">Source field</span></span> | <span data-ttu-id="9a1f5-118">Määritystyyppi</span><span class="sxs-lookup"><span data-stu-id="9a1f5-118">Map type</span></span> | <span data-ttu-id="9a1f5-119">Kohdekenttä</span><span class="sxs-lookup"><span data-stu-id="9a1f5-119">Destination field</span></span>
---|---|---
<span data-ttu-id="9a1f5-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="9a1f5-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="9a1f5-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="9a1f5-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="9a1f5-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="9a1f5-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="9a1f5-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="9a1f5-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="9a1f5-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="9a1f5-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="9a1f5-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="9a1f5-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="9a1f5-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="9a1f5-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="9a1f5-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="9a1f5-127">msdyn\_immutable</span></span>
<span data-ttu-id="9a1f5-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="9a1f5-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="9a1f5-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="9a1f5-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="9a1f5-130">Sisäinen organisaatiohierarkian tyyppi</span><span class="sxs-lookup"><span data-stu-id="9a1f5-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="9a1f5-131">Tässä mallissa on yksisuuntainen Organisaatiohierarkian tyyppi -yksikön synkronointi Finance and Operationsista muihin Dynamics 365 -sovelluksiin.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="9a1f5-132">Lähdetaulu</span><span class="sxs-lookup"><span data-stu-id="9a1f5-132">Source field</span></span> | <span data-ttu-id="9a1f5-133">Määritystyyppi</span><span class="sxs-lookup"><span data-stu-id="9a1f5-133">Map type</span></span> | <span data-ttu-id="9a1f5-134">Kohdekenttä</span><span class="sxs-lookup"><span data-stu-id="9a1f5-134">Destination field</span></span>
---|---|---
<span data-ttu-id="9a1f5-135">NIMI</span><span class="sxs-lookup"><span data-stu-id="9a1f5-135">NAME</span></span> | \> | <span data-ttu-id="9a1f5-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="9a1f5-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="9a1f5-137">Sisäinen organisaatiohierarkia</span><span class="sxs-lookup"><span data-stu-id="9a1f5-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="9a1f5-138">Tässä mallissa on yksisuuntainen Julkaistu organisaatiohierarkia -yksikön synkronointi Finance and Operationsista muihin Dynamics 365 -sovelluksiin.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="9a1f5-139">Lähdetaulu</span><span class="sxs-lookup"><span data-stu-id="9a1f5-139">Source field</span></span> | <span data-ttu-id="9a1f5-140">Määritystyyppi</span><span class="sxs-lookup"><span data-stu-id="9a1f5-140">Map type</span></span> | <span data-ttu-id="9a1f5-141">Kohdekenttä</span><span class="sxs-lookup"><span data-stu-id="9a1f5-141">Destination field</span></span>
---|---|---
<span data-ttu-id="9a1f5-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="9a1f5-142">VALIDTO</span></span> | \> | <span data-ttu-id="9a1f5-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="9a1f5-143">msdyn\_validto</span></span>
<span data-ttu-id="9a1f5-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="9a1f5-144">VALIDFROM</span></span> | \> | <span data-ttu-id="9a1f5-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="9a1f5-145">msdyn\_validfrom</span></span>
<span data-ttu-id="9a1f5-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="9a1f5-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="9a1f5-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="9a1f5-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="9a1f5-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="9a1f5-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="9a1f5-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="9a1f5-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="9a1f5-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="9a1f5-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="9a1f5-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="9a1f5-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="9a1f5-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="9a1f5-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="9a1f5-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="9a1f5-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="9a1f5-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="9a1f5-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="9a1f5-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="9a1f5-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="9a1f5-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="9a1f5-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="9a1f5-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="9a1f5-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="9a1f5-158">Sisäinen organisaatio</span><span class="sxs-lookup"><span data-stu-id="9a1f5-158">Internal Organization</span></span>

<span data-ttu-id="9a1f5-159">Sisäisen organisaation tiedot ovat Common Data Servicessa peräisin kahdesta yksiköstä: **toimintayksikkö** ja **yritykset**.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="9a1f5-160">Toimintayksikkö</span><span class="sxs-lookup"><span data-stu-id="9a1f5-160">Operating unit</span></span>

<span data-ttu-id="9a1f5-161">Lähdetaulu</span><span class="sxs-lookup"><span data-stu-id="9a1f5-161">Source field</span></span> | <span data-ttu-id="9a1f5-162">Määritystyyppi</span><span class="sxs-lookup"><span data-stu-id="9a1f5-162">Map type</span></span> | <span data-ttu-id="9a1f5-163">Kohdekenttä</span><span class="sxs-lookup"><span data-stu-id="9a1f5-163">Destination field</span></span>
---|---|---
<span data-ttu-id="9a1f5-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="9a1f5-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="9a1f5-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="9a1f5-165">msdyn\_languageid</span></span>
<span data-ttu-id="9a1f5-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="9a1f5-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="9a1f5-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="9a1f5-167">msdyn\_namealias</span></span>
<span data-ttu-id="9a1f5-168">NIMI</span><span class="sxs-lookup"><span data-stu-id="9a1f5-168">NAME</span></span> | \> | <span data-ttu-id="9a1f5-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="9a1f5-169">msdyn\_name</span></span>
<span data-ttu-id="9a1f5-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="9a1f5-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="9a1f5-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="9a1f5-171">msdyn\_partynumber</span></span>
<span data-ttu-id="9a1f5-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="9a1f5-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="9a1f5-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="9a1f5-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="9a1f5-174">Oikeushenkilö</span><span class="sxs-lookup"><span data-stu-id="9a1f5-174">Legal entity</span></span>

<span data-ttu-id="9a1f5-175">Lähdetaulu</span><span class="sxs-lookup"><span data-stu-id="9a1f5-175">Source field</span></span> | <span data-ttu-id="9a1f5-176">Määritystyyppi</span><span class="sxs-lookup"><span data-stu-id="9a1f5-176">Map type</span></span> | <span data-ttu-id="9a1f5-177">Kohdekenttä</span><span class="sxs-lookup"><span data-stu-id="9a1f5-177">Destination field</span></span>
---|---|---
<span data-ttu-id="9a1f5-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="9a1f5-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="9a1f5-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="9a1f5-179">msdyn\_namealias</span></span>
<span data-ttu-id="9a1f5-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="9a1f5-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="9a1f5-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="9a1f5-181">msdyn\_languageid</span></span>
<span data-ttu-id="9a1f5-182">NIMI</span><span class="sxs-lookup"><span data-stu-id="9a1f5-182">NAME</span></span> | \> | <span data-ttu-id="9a1f5-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="9a1f5-183">msdyn\_name</span></span>
<span data-ttu-id="9a1f5-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="9a1f5-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="9a1f5-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="9a1f5-185">msdyn\_partynumber</span></span>
<span data-ttu-id="9a1f5-186">none</span><span class="sxs-lookup"><span data-stu-id="9a1f5-186">none</span></span> | \>\> | <span data-ttu-id="9a1f5-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="9a1f5-187">msdyn\_type</span></span>
<span data-ttu-id="9a1f5-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="9a1f5-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="9a1f5-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="9a1f5-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="9a1f5-190">Yritys </span><span class="sxs-lookup"><span data-stu-id="9a1f5-190">Company</span></span>

<span data-ttu-id="9a1f5-191">Sisältää oikeushenkilön (yrityksen) kaksisuuntaisen synkronoinnin Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="9a1f5-192">Lähdetaulu</span><span class="sxs-lookup"><span data-stu-id="9a1f5-192">Source field</span></span> | <span data-ttu-id="9a1f5-193">Määritystyyppi</span><span class="sxs-lookup"><span data-stu-id="9a1f5-193">Map type</span></span> | <span data-ttu-id="9a1f5-194">Kohdekenttä</span><span class="sxs-lookup"><span data-stu-id="9a1f5-194">Destination field</span></span>
---|---|---
<span data-ttu-id="9a1f5-195">NIMI</span><span class="sxs-lookup"><span data-stu-id="9a1f5-195">NAME</span></span> | = | <span data-ttu-id="9a1f5-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="9a1f5-196">cdm\_name</span></span>
<span data-ttu-id="9a1f5-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="9a1f5-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="9a1f5-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="9a1f5-198">cdm\_companycode</span></span>
