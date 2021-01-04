---
title: Ratkaisujen käyttäjien osaamistasoon liittyvien ongelmien vianmääritys
description: Tässä ohjeaiheessa on vianmääritys tietoja, joiden avulla voit korjata ratkaisutietoisuuteen liittyviä ongelmia.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 79b2920b80ce4a8b419c2a146e15babc061cf64d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683558"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="4a8b4-103">Ratkaisujen käyttäjien osaamistasoon liittyvien ongelmien vianmääritys</span><span class="sxs-lookup"><span data-stu-id="4a8b4-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="4a8b4-104">Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Dataversen välillä.</span><span class="sxs-lookup"><span data-stu-id="4a8b4-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="4a8b4-105">Erityisesti se tarjoaa tietoja, joiden avulla voit korjata ratkaisutietoisuuteen liittyviä ongelmia.</span><span class="sxs-lookup"><span data-stu-id="4a8b4-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a8b4-106">Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia.</span><span class="sxs-lookup"><span data-stu-id="4a8b4-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="4a8b4-107">Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="4a8b4-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="4a8b4-108">Virhe kaksoiskirjoitussivulla</span><span class="sxs-lookup"><span data-stu-id="4a8b4-108">Error on the Dual-write page</span></span>

<span data-ttu-id="4a8b4-109">**Kaksoiskirjoitussivulla** näyttöön saattaa tulla seuraavan kaltainen virhesanoma:</span><span class="sxs-lookup"><span data-stu-id="4a8b4-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="4a8b4-110">*Yksikköä, jonka nimi on msdyn\_dualwriteentitymap' with namemapping='Logical', ei löytynyt kohteesta MetadataCache.*</span><span class="sxs-lookup"><span data-stu-id="4a8b4-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="4a8b4-111">Voit korjata ongelman varmistamalla, että kaksoiskirjoitusydinratkaisu on asennettu Dataverse -järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="4a8b4-111">To fix the issue, make sure that the dual-write core solution is installed in Dataverse.</span></span> <span data-ttu-id="4a8b4-112">Kaksoiskirjoitusydinratkaisu on ratkaisutietoisuuden edellytys.</span><span class="sxs-lookup"><span data-stu-id="4a8b4-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>
