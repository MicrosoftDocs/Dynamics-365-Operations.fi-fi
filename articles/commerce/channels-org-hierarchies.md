---
title: Organisaatiohierarkioiden määrittäminen
description: Tässä ohjeaiheessa käsitellään organisaatiohierarkioiden määrittämistä Microsoft Dynamics 365 Commercessa.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 490d466c10cfe0640f8fbcf8fe2298536e499d9b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477993"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="a5041-103">Organisaatiohierarkioiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a5041-103">Set up organization hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a5041-104">Tässä ohjeaiheessa käsitellään organisaatiohierarkioiden määrittämistä Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="a5041-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a5041-105">Ennen kanavien luontia on varmistettava, että organisaatiohierarkiat on määritetty.</span><span class="sxs-lookup"><span data-stu-id="a5041-105">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="a5041-106">Voit käyttää organisaatiohierarkioita liiketoiminnan tarkastelemiseen ja raportointiin eri näkökulmista.</span><span class="sxs-lookup"><span data-stu-id="a5041-106">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="a5041-107">Voit esimerkiksi määrittää yhden hierarkian veroraportteja tai oikeudellista tai lakisääteistä raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="a5041-107">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="a5041-108">Voit määrittää toisen hierarkian raportoimaan sellaiset taloustiedot, joiden raportointia lainsäädäntö ei edellytä mutta joita käytetään sisäisessä raportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="a5041-108">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="a5041-109">Ennen organisaatiohierarkian luomista sinun on luotava organisaatiot.</span><span class="sxs-lookup"><span data-stu-id="a5041-109">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="a5041-110">Lisätietoja on kohdassa [Yritysten luominen](channels-legal-entities.md) tai [Toimintayksiköiden luominen](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="a5041-110">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="a5041-111">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="a5041-111">For more information, see the following topics.</span></span>
- [<span data-ttu-id="a5041-112">Organisaatiot ja organisaatiohierarkiat – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a5041-112">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="a5041-113">Organisaatiohierarkian suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="a5041-113">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="a5041-114">Organisaation hierarkian luominen</span><span class="sxs-lookup"><span data-stu-id="a5041-114">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="a5041-115">Organisaatiohierarkian luominen</span><span class="sxs-lookup"><span data-stu-id="a5041-115">Create an organizational hierarchy</span></span>

<span data-ttu-id="a5041-116">Luo organisaatiohierarkia seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="a5041-116">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="a5041-117">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan asetukset \> Organisaatiohierarkiat**.</span><span class="sxs-lookup"><span data-stu-id="a5041-117">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="a5041-118">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a5041-118">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a5041-119">Anna **Nimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a5041-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="a5041-120">Valitse **Tarkoitus**-osassa **Määritä tarkoitus**.</span><span class="sxs-lookup"><span data-stu-id="a5041-120">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="a5041-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a5041-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="a5041-122">Valitse tarkoitus määritettäväksi organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="a5041-122">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="a5041-123">Valitse **Määritetyt hierarkiat** -kohdassa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a5041-123">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="a5041-124">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a5041-124">In the list, mark the selected row.</span></span> <span data-ttu-id="a5041-125">Etsi juuri luomasi hierarkia.</span><span class="sxs-lookup"><span data-stu-id="a5041-125">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="a5041-126">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a5041-126">Select **OK**.</span></span>

<span data-ttu-id="a5041-127">Seuraavassa kuvassa on esimerkki organisaatiohierarkiasta, joka luotu kuvitteelliselle Adventure Works -myymäläketjulle.</span><span class="sxs-lookup"><span data-stu-id="a5041-127">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Esimerkki organisaatiohierarkiasta](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="a5041-129">Organisaatioiden lisääminen hierarkiaan</span><span class="sxs-lookup"><span data-stu-id="a5041-129">Add organizations to a hierarchy</span></span>

<span data-ttu-id="a5041-130">Lisää organisaatiot hierarkiaan seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="a5041-130">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="a5041-131">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a5041-131">In the list, find and select the desired record.</span></span> <span data-ttu-id="a5041-132">Valitse hierarkia.</span><span class="sxs-lookup"><span data-stu-id="a5041-132">Select your hierarchy.</span></span>
1. <span data-ttu-id="a5041-133">Valitse toimintoruudussa **Näytä**.</span><span class="sxs-lookup"><span data-stu-id="a5041-133">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="a5041-134">Lisää organisaatioita tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="a5041-134">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="a5041-135">Lisää organisaatio valitsemalla ensin **Muokkaa** ja sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a5041-135">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="a5041-136">Kun olet tehnyt haluamasi muutokset, voit tallentaa luonnoksen ja julkaista muutokset.</span><span class="sxs-lookup"><span data-stu-id="a5041-136">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="a5041-137">Seuraavassa kuvassa on hierarkian juureen lisätty yritys ja neljä kustannuspaikkaa: ostoskeskus-, outlet-, verkko- ja puhelinkeskuskanavat.</span><span class="sxs-lookup"><span data-stu-id="a5041-137">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="a5041-138">Kuhunkin voidaan sitten lisätä erilaisia vähittäismyynti-, puhelinkeskus- ja verkkokanavia.</span><span class="sxs-lookup"><span data-stu-id="a5041-138">Various retail, call center and online channels can then be added to each.</span></span>

![Esimerkki hierarkian suunnittelutoiminnosta](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="a5041-140">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a5041-140">Additional resources</span></span>

[<span data-ttu-id="a5041-141">Organisaatiot ja organisaatiohierarkiat – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a5041-141">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="a5041-142">Organisaatiohierarkian suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="a5041-142">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="a5041-143">Yritysten luominen</span><span class="sxs-lookup"><span data-stu-id="a5041-143">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="a5041-144">Toimintayksiköiden luominen</span><span class="sxs-lookup"><span data-stu-id="a5041-144">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="a5041-145">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a5041-145">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="a5041-146">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="a5041-146">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
