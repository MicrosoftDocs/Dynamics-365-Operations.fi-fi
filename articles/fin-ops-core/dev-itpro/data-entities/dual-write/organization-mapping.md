---
title: Organisaatiohierarkia Dataversessa
description: Tässä aiheessa kuvataan organisaation tietojen integraatiota Finance and Operations -sovellusten ja Dataversen välillä.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: e2b652f11db62eb58ffc2ec2fc4322149e7d45d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680069"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="a573c-103">Organisaatiohierarkia Dataversessa</span><span class="sxs-lookup"><span data-stu-id="a573c-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a573c-104">Koska Dynamics 365 Finance on talousjärjestelmä, *organisaatio* on keskeinen käsite ja järjestelmän asennusohjelma alkaa organisaatiohierarkian konfiguraatiosta.</span><span class="sxs-lookup"><span data-stu-id="a573c-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="a573c-105">Yrityksen taloustietoja voidaan sitten seurata organisaatiotasolla ja millä tahansa organisaatiohierarkian tasolla.</span><span class="sxs-lookup"><span data-stu-id="a573c-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="a573c-106">Vaikka Dataversessa ei ole käsitettä organisaatiohierarkia, siinä on joitakin käsitteitä, kuten myyntituoton kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="a573c-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="a573c-107">Organisaatiohierarkian tietorakenne lisätään Dataverse -integroinnin osana Dataverseen.</span><span class="sxs-lookup"><span data-stu-id="a573c-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="a573c-108">Tietojen virtaus</span><span class="sxs-lookup"><span data-stu-id="a573c-108">Data flow</span></span>

<span data-ttu-id="a573c-109">Liiketoiminnan ekosysteemillä, joka koostuu Finance and Operations -sovelluksesta ja Dataversesta, on jatkossakin organisaatiohierarkia.</span><span class="sxs-lookup"><span data-stu-id="a573c-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="a573c-110">Tämä organisaatiohierarkia perustuu Finance and Operations -sovelluksiin, mutta se näkyy Dataversessä tiedon jakamista ja laajennettavuutta varten.</span><span class="sxs-lookup"><span data-stu-id="a573c-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="a573c-111">Seuraavassa kuvassa näkyy organisaatiohierarkian tiedot, jotka näkyvät Dataversessä yksisuuntaisena tiedonkulkuna Finance and Operations -sovelluksista Dataverseen.</span><span class="sxs-lookup"><span data-stu-id="a573c-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Arkkitehtuurikuva](media/dual-write-data-flow.png)

<span data-ttu-id="a573c-113">Organisaatiohierarkian taulujen yhdistämismääritykset ovat käytettävissä yksisuuntaiseen tietojen synkronointiin Finance and Operations -sovelluksista Dataverseen.</span><span class="sxs-lookup"><span data-stu-id="a573c-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="a573c-114">Mallit</span><span class="sxs-lookup"><span data-stu-id="a573c-114">Templates</span></span>

<span data-ttu-id="a573c-115">Tuotetiedot sisältävät kaiken tuotteeseen liittyvät tiedot ja tuotteen määrityksen, kuten tuotedimensiot tai seuranta- ja varastodimensiot.</span><span class="sxs-lookup"><span data-stu-id="a573c-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="a573c-116">Seuraava taulukko osoittaa, miten taulukarttakokoelma luodaan synkronoimaan tuotteita ja liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="a573c-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="a573c-117">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="a573c-117">Finance and Operations apps</span></span> | <span data-ttu-id="a573c-118">Muut Dynamics 365 -sovellukset</span><span class="sxs-lookup"><span data-stu-id="a573c-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="a573c-119">kuvaus</span><span class="sxs-lookup"><span data-stu-id="a573c-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="a573c-120">Organisaatiohierarkian tarkoitukset</span><span class="sxs-lookup"><span data-stu-id="a573c-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="a573c-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="a573c-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="a573c-122">Tässä mallissa on yksisuuntainen Organisaatiohierarkian tarkoitus -yksikön synkronointi.</span><span class="sxs-lookup"><span data-stu-id="a573c-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="a573c-123">Organisaatiohierarkian tyyppi</span><span class="sxs-lookup"><span data-stu-id="a573c-123">Organization hierarchy type</span></span> | <span data-ttu-id="a573c-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="a573c-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="a573c-125">Tässä mallissa on yksisuuntainen Organisaatiohierarkiatyyppi-yksikön synkronointi.</span><span class="sxs-lookup"><span data-stu-id="a573c-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="a573c-126">Organisaatiohierarkia – julkaistu</span><span class="sxs-lookup"><span data-stu-id="a573c-126">Organization hierarchy - published</span></span> | <span data-ttu-id="a573c-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="a573c-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="a573c-128">Tässä mallissa on yksisuuntainen Organisaatiohierarkia julkaistu -yksikön synkronointi.</span><span class="sxs-lookup"><span data-stu-id="a573c-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="a573c-129">Toimintayksikkö</span><span class="sxs-lookup"><span data-stu-id="a573c-129">Operating unit</span></span> | <span data-ttu-id="a573c-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="a573c-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="a573c-131">Oikeushenkilöt</span><span class="sxs-lookup"><span data-stu-id="a573c-131">Legal entities</span></span> | <span data-ttu-id="a573c-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="a573c-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="a573c-133">Oikeushenkilöt</span><span class="sxs-lookup"><span data-stu-id="a573c-133">Legal entities</span></span> | <span data-ttu-id="a573c-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="a573c-134">cdm_companies</span></span> | <span data-ttu-id="a573c-135">Sisältää yrityksen (yhtiön) kaksisuuntaisen synkronoinnin.</span><span class="sxs-lookup"><span data-stu-id="a573c-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="a573c-136">Sisäinen organisaatio</span><span class="sxs-lookup"><span data-stu-id="a573c-136">Internal Organization</span></span>

<span data-ttu-id="a573c-137">Sisäisen organisaation tiedot ovat Dataversessa peräisin kahdesta taulusta: **toimintayksikkö** ja **yritykset**.</span><span class="sxs-lookup"><span data-stu-id="a573c-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
