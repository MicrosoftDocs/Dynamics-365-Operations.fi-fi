---
title: Organisaatiohierarkia Common Data Servicessa
description: Tässä aiheessa kuvataan organisaation tietojen integraatiota Finance and Operationsin ja Common Data Servicen välillä.
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
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789183"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="c6e59-103">Organisaatiohierarkia Common Data Servicessa</span><span class="sxs-lookup"><span data-stu-id="c6e59-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="c6e59-104">Koska Microsoft Dynamics 365 for Finance and Operations on talousjärjestelmä, *organisaatio* on keskeinen käsite ja järjestelmän asennusohjelma alkaa organisaatiohierarkian konfiguraatiosta.</span><span class="sxs-lookup"><span data-stu-id="c6e59-104">Because Microsoft Dynamics 365 for Finance and Operations is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="c6e59-105">Yrityksen taloustoimintoja voidaan sitten seurata organisaatiotasolla ja millä tahansa organisaatiohierarkian tasolla.</span><span class="sxs-lookup"><span data-stu-id="c6e59-105">Business financials and operations can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="c6e59-106">Vaikka Common Data Servicessa ei ole käsitettä organisaatiohierarkia, siinä on joitakin käsitteitä, kuten myyntituoton kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="c6e59-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="c6e59-107">Organisaatiohierarkian tietorakenne lisätään Common Data Service -integroinnin osana Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="c6e59-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="c6e59-108">Tietojen virtaus</span><span class="sxs-lookup"><span data-stu-id="c6e59-108">Data flow</span></span>

<span data-ttu-id="c6e59-109">Liiketoiminnan ekosysteemillä, joka koostuu Finance and Operationsista ja Common Data Servicesta, tulee edelleen oelmaan organisaatiohierarkia.</span><span class="sxs-lookup"><span data-stu-id="c6e59-109">A business ecosystem that consists of Finance and Operations and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="c6e59-110">Tämä organisaatiohierarkia on rakennettu Finance and Operationsin päälle, mutta se on avattu Common Data Servicessa tiedon jakamisen ja laajennettavuuden tarkoituksia varten.</span><span class="sxs-lookup"><span data-stu-id="c6e59-110">This organization hierarchy is built on Finance and Operations, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="c6e59-111">Seuraavassa kuvassa näkyy organisaatiohierarkian tiedot, jotka ovat avattu Common Data Servicessa yksisuuntaisessa tietovirrassa Finance and Operationsista Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="c6e59-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations to Common Data Service.</span></span>

![Arkkitehtuurikuva](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="c6e59-113">Mallit</span><span class="sxs-lookup"><span data-stu-id="c6e59-113">Templates</span></span>

<span data-ttu-id="c6e59-114">Organisaatiohierarkian entiteettien yhdistämismäärirtykset ovat käytettävissä yksisuuntaiseen tietojen synkronointiin Finance and Operationsista Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="c6e59-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="c6e59-115">Sisäinen organisaatiohierarkian tarkoitus</span><span class="sxs-lookup"><span data-stu-id="c6e59-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="c6e59-116">Tässä mallissa on yksisuuntainen Organisaatiohierarkian tarkoitus -entiteetin synkronointi Finance and Operationsista Dynamics 365 for Customer Engagementiin.</span><span class="sxs-lookup"><span data-stu-id="c6e59-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to Dynamics 365 for Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="c6e59-117">Lähdetaulu</span><span class="sxs-lookup"><span data-stu-id="c6e59-117">Source field</span></span> | <span data-ttu-id="c6e59-118">Määritystyyppi</span><span class="sxs-lookup"><span data-stu-id="c6e59-118">Map type</span></span> | <span data-ttu-id="c6e59-119">Kohdekenttä</span><span class="sxs-lookup"><span data-stu-id="c6e59-119">Destination field</span></span>
---|---|---
<span data-ttu-id="c6e59-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="c6e59-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="c6e59-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="c6e59-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="c6e59-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="c6e59-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="c6e59-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="c6e59-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="c6e59-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="c6e59-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="c6e59-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="c6e59-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="c6e59-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="c6e59-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="c6e59-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="c6e59-127">msdyn\_immutable</span></span>
<span data-ttu-id="c6e59-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="c6e59-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="c6e59-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="c6e59-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="c6e59-130">Sisäinen organisaatiohierarkian tyyppi</span><span class="sxs-lookup"><span data-stu-id="c6e59-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="c6e59-131">Tässä mallissa on yksisuuntainen Organisaatiohierarkian tyyppi -entiteetin synkronointi Finance and Operationsista Customer Engagementiin.</span><span class="sxs-lookup"><span data-stu-id="c6e59-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="c6e59-132">Lähdetaulu</span><span class="sxs-lookup"><span data-stu-id="c6e59-132">Source field</span></span> | <span data-ttu-id="c6e59-133">Määritystyyppi</span><span class="sxs-lookup"><span data-stu-id="c6e59-133">Map type</span></span> | <span data-ttu-id="c6e59-134">Kohdekenttä</span><span class="sxs-lookup"><span data-stu-id="c6e59-134">Destination field</span></span>
---|---|---
<span data-ttu-id="c6e59-135">NIMI</span><span class="sxs-lookup"><span data-stu-id="c6e59-135">NAME</span></span> | \> | <span data-ttu-id="c6e59-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="c6e59-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="c6e59-137">Sisäinen organisaatiohierarkia</span><span class="sxs-lookup"><span data-stu-id="c6e59-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="c6e59-138">Tässä mallissa on yksisuuntainen Julkaistu organisaatiohierarkia -entiteetin synkronointi Finance and Operationsista Customer Engagementiin.</span><span class="sxs-lookup"><span data-stu-id="c6e59-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="c6e59-139">Lähdetaulu</span><span class="sxs-lookup"><span data-stu-id="c6e59-139">Source field</span></span> | <span data-ttu-id="c6e59-140">Määritystyyppi</span><span class="sxs-lookup"><span data-stu-id="c6e59-140">Map type</span></span> | <span data-ttu-id="c6e59-141">Kohdekenttä</span><span class="sxs-lookup"><span data-stu-id="c6e59-141">Destination field</span></span>
---|---|---
<span data-ttu-id="c6e59-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="c6e59-142">VALIDTO</span></span> | \> | <span data-ttu-id="c6e59-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="c6e59-143">msdyn\_validto</span></span>
<span data-ttu-id="c6e59-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="c6e59-144">VALIDFROM</span></span> | \> | <span data-ttu-id="c6e59-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="c6e59-145">msdyn\_validfrom</span></span>
<span data-ttu-id="c6e59-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="c6e59-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="c6e59-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="c6e59-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="c6e59-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="c6e59-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="c6e59-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="c6e59-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="c6e59-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="c6e59-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="c6e59-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="c6e59-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="c6e59-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="c6e59-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="c6e59-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="c6e59-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="c6e59-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="c6e59-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="c6e59-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="c6e59-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="c6e59-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="c6e59-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="c6e59-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="c6e59-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="c6e59-158">Sisäinen organisaatio</span><span class="sxs-lookup"><span data-stu-id="c6e59-158">Internal Organization</span></span>

<span data-ttu-id="c6e59-159">Sisäisen organisaation tiedot ovat Common Data Servicessa peräisin kahdesta Finance and Operations -entiteetistä: **Toimintayksikkö** ja **Oikeushenkilöt**.</span><span class="sxs-lookup"><span data-stu-id="c6e59-159">Internal organization information in Common Data Service comes from two Finance and Operations entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="c6e59-160">Toimintayksikkö</span><span class="sxs-lookup"><span data-stu-id="c6e59-160">Operating unit</span></span>

<span data-ttu-id="c6e59-161">Lähdetaulu</span><span class="sxs-lookup"><span data-stu-id="c6e59-161">Source field</span></span> | <span data-ttu-id="c6e59-162">Määritystyyppi</span><span class="sxs-lookup"><span data-stu-id="c6e59-162">Map type</span></span> | <span data-ttu-id="c6e59-163">Kohdekenttä</span><span class="sxs-lookup"><span data-stu-id="c6e59-163">Destination field</span></span>
---|---|---
<span data-ttu-id="c6e59-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="c6e59-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="c6e59-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="c6e59-165">msdyn\_languageid</span></span>
<span data-ttu-id="c6e59-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="c6e59-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="c6e59-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="c6e59-167">msdyn\_namealias</span></span>
<span data-ttu-id="c6e59-168">NIMI</span><span class="sxs-lookup"><span data-stu-id="c6e59-168">NAME</span></span> | \> | <span data-ttu-id="c6e59-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="c6e59-169">msdyn\_name</span></span>
<span data-ttu-id="c6e59-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="c6e59-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="c6e59-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="c6e59-171">msdyn\_partynumber</span></span>
<span data-ttu-id="c6e59-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="c6e59-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="c6e59-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="c6e59-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="c6e59-174">Oikeushenkilö</span><span class="sxs-lookup"><span data-stu-id="c6e59-174">Legal entity</span></span>

<span data-ttu-id="c6e59-175">Lähdetaulu</span><span class="sxs-lookup"><span data-stu-id="c6e59-175">Source field</span></span> | <span data-ttu-id="c6e59-176">Määritystyyppi</span><span class="sxs-lookup"><span data-stu-id="c6e59-176">Map type</span></span> | <span data-ttu-id="c6e59-177">Kohdekenttä</span><span class="sxs-lookup"><span data-stu-id="c6e59-177">Destination field</span></span>
---|---|---
<span data-ttu-id="c6e59-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="c6e59-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="c6e59-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="c6e59-179">msdyn\_namealias</span></span>
<span data-ttu-id="c6e59-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="c6e59-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="c6e59-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="c6e59-181">msdyn\_languageid</span></span>
<span data-ttu-id="c6e59-182">NIMI</span><span class="sxs-lookup"><span data-stu-id="c6e59-182">NAME</span></span> | \> | <span data-ttu-id="c6e59-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="c6e59-183">msdyn\_name</span></span>
<span data-ttu-id="c6e59-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="c6e59-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="c6e59-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="c6e59-185">msdyn\_partynumber</span></span>
<span data-ttu-id="c6e59-186">none</span><span class="sxs-lookup"><span data-stu-id="c6e59-186">none</span></span> | \>\> | <span data-ttu-id="c6e59-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="c6e59-187">msdyn\_type</span></span>
<span data-ttu-id="c6e59-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="c6e59-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="c6e59-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="c6e59-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="c6e59-190">Yritys </span><span class="sxs-lookup"><span data-stu-id="c6e59-190">Company</span></span>

<span data-ttu-id="c6e59-191">Sisältää oikeushenkilön (yrityksen) kaksisuuntaisen synkronoinnin Finance and Operationsin ja Customer Engagementin välillä.</span><span class="sxs-lookup"><span data-stu-id="c6e59-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="c6e59-192">Lähdetaulu</span><span class="sxs-lookup"><span data-stu-id="c6e59-192">Source field</span></span> | <span data-ttu-id="c6e59-193">Määritystyyppi</span><span class="sxs-lookup"><span data-stu-id="c6e59-193">Map type</span></span> | <span data-ttu-id="c6e59-194">Kohdekenttä</span><span class="sxs-lookup"><span data-stu-id="c6e59-194">Destination field</span></span>
---|---|---
<span data-ttu-id="c6e59-195">NIMI</span><span class="sxs-lookup"><span data-stu-id="c6e59-195">NAME</span></span> | = | <span data-ttu-id="c6e59-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="c6e59-196">cdm\_name</span></span>
<span data-ttu-id="c6e59-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="c6e59-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="c6e59-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="c6e59-198">cdm\_companycode</span></span>
