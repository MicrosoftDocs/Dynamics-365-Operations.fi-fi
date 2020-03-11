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
ms.openlocfilehash: fbf7cc33d12fb54d2ff02acc46ba2e284b2a2b3f
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019758"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="b6be0-103">Organisaatiohierarkia Common Data Servicessa</span><span class="sxs-lookup"><span data-stu-id="b6be0-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="b6be0-104">Koska Dynamics 365 Finance on talousjärjestelmä, *organisaatio* on keskeinen käsite ja järjestelmän asennusohjelma alkaa organisaatiohierarkian konfiguraatiosta.</span><span class="sxs-lookup"><span data-stu-id="b6be0-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="b6be0-105">Yrityksen taloustietoja voidaan sitten seurata organisaatiotasolla ja millä tahansa organisaatiohierarkian tasolla.</span><span class="sxs-lookup"><span data-stu-id="b6be0-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="b6be0-106">Vaikka Common Data Servicessa ei ole käsitettä organisaatiohierarkia, siinä on joitakin käsitteitä, kuten myyntituoton kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="b6be0-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="b6be0-107">Organisaatiohierarkian tietorakenne lisätään Common Data Service -integroinnin osana Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="b6be0-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="b6be0-108">Tietojen virtaus</span><span class="sxs-lookup"><span data-stu-id="b6be0-108">Data flow</span></span>

<span data-ttu-id="b6be0-109">Liiketoiminnan ekosysteemillä, joka koostuu Finance and Operations -sovelluksesta ja Common Data Servicesta, on jatkossakin organisaatiohierarkia.</span><span class="sxs-lookup"><span data-stu-id="b6be0-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="b6be0-110">Tämä organisaatiohierarkia perustuu Finance and Operations -sovelluksiin, mutta se näkyy Common Data Servicessä tiedon jakamista ja laajennettavuutta varten.</span><span class="sxs-lookup"><span data-stu-id="b6be0-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="b6be0-111">Seuraavassa kuvassa näkyy organisaatiohierarkian tiedot, jotka näkyvät Common Data Servicessä yksisuuntaisena tiedonkulkuna Finance and Operations -sovelluksista Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="b6be0-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Arkkitehtuurikuva](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="b6be0-113">Mallit</span><span class="sxs-lookup"><span data-stu-id="b6be0-113">Templates</span></span>

<span data-ttu-id="b6be0-114">Organisaatiohierarkian entiteettien yhdistämismääritykset ovat käytettävissä yksisuuntaiseen tietojen synkronointiin Finance and Operations -sovelluksista Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="b6be0-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="b6be0-115">Mallit</span><span class="sxs-lookup"><span data-stu-id="b6be0-115">Templates</span></span>

<span data-ttu-id="b6be0-116">Tuotetiedot sisältävät kaiken tuotteeseen liittyvät tiedot ja tuotteen määrityksen, kuten tuotedimensiot tai seuranta- ja varastodimensiot.</span><span class="sxs-lookup"><span data-stu-id="b6be0-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="b6be0-117">Seuraava taulukko osoittaa, miten yksikkökarttakokoelma luodaan synkronoimaan tuotteita ja liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="b6be0-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="b6be0-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b6be0-118">Finance and Operations</span></span> | <span data-ttu-id="b6be0-119">Muut Dynamics 365 -sovellukset</span><span class="sxs-lookup"><span data-stu-id="b6be0-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="b6be0-120">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="b6be0-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="b6be0-121">Organisaatiohierarkian tarkoitukset</span><span class="sxs-lookup"><span data-stu-id="b6be0-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="b6be0-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="b6be0-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="b6be0-123">Tässä mallissa on yksisuuntainen Organisaatiohierarkian tarkoitus -yksikön synkronointi.</span><span class="sxs-lookup"><span data-stu-id="b6be0-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="b6be0-124">Organisaatiohierarkian tyyppi</span><span class="sxs-lookup"><span data-stu-id="b6be0-124">Organization hierarchy type</span></span> | <span data-ttu-id="b6be0-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="b6be0-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="b6be0-126">Tässä mallissa on yksisuuntainen Organisaatiohierarkiatyyppi-yksikön synkronointi.</span><span class="sxs-lookup"><span data-stu-id="b6be0-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="b6be0-127">Organisaatiohierarkia – julkaistu</span><span class="sxs-lookup"><span data-stu-id="b6be0-127">Organization hierarchy - published</span></span> | <span data-ttu-id="b6be0-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="b6be0-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="b6be0-129">Tässä mallissa on yksisuuntainen Organisaatiohierarkia julkaistu -yksikön synkronointi.</span><span class="sxs-lookup"><span data-stu-id="b6be0-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="b6be0-130">Toimintayksikkö</span><span class="sxs-lookup"><span data-stu-id="b6be0-130">Operating unit</span></span> | <span data-ttu-id="b6be0-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="b6be0-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="b6be0-132">Oikeushenkilöt</span><span class="sxs-lookup"><span data-stu-id="b6be0-132">Legal entities</span></span> | <span data-ttu-id="b6be0-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="b6be0-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="b6be0-134">Oikeushenkilöt</span><span class="sxs-lookup"><span data-stu-id="b6be0-134">Legal entities</span></span> | <span data-ttu-id="b6be0-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="b6be0-135">cdm_companies</span></span> | <span data-ttu-id="b6be0-136">Sisältää yrityksen (yhtiön) kaksisuuntaisen synkronoinnin.</span><span class="sxs-lookup"><span data-stu-id="b6be0-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="b6be0-137">Sisäinen organisaatio</span><span class="sxs-lookup"><span data-stu-id="b6be0-137">Internal Organization</span></span>

<span data-ttu-id="b6be0-138">Sisäisen organisaation tiedot ovat Common Data Servicessa peräisin kahdesta yksiköstä: **toimintayksikkö** ja **yritykset**.</span><span class="sxs-lookup"><span data-stu-id="b6be0-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
