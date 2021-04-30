---
title: Power Apps-hallintakeskuksessa ei voi luoda ympäristöä
description: Tässä artikkelissa kerrotaan, mitä voidaan tehdä, jos järjestelmänvalvoja ei voi luoda ympäristöä Microsoft Power Appsin hallintakeskuksessa.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 26a228229a09e74809a048675a3ff90025f2a26c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892224"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="3f2d0-103">Power Apps-hallintakeskuksessa ei voi luoda ympäristöä</span><span class="sxs-lookup"><span data-stu-id="3f2d0-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3f2d0-104">**Lähetä**</span><span class="sxs-lookup"><span data-stu-id="3f2d0-104">**Issue**</span></span>

- <span data-ttu-id="3f2d0-105">Vuokraajan tai ympäristön järjestelmänvalvoja ei voi luoda ympäristöä Microsoft Power Appsin hallintakeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="3f2d0-106">Käyttäjällä ei ole käyttöoikeutta luoda ympäristöjä.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="3f2d0-107">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="3f2d0-107">**Solution**</span></span>

<span data-ttu-id="3f2d0-108">Varmista, että vuokraajan järjestelmänvalvoja on määrittänyt ympäristöä luovalle käyttäjälle kelvollisen Power Apps P2 -käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="3f2d0-109">Seuraavissa Microsoft Dynamics -palvelusuunnitelmissa on mukana oikeudet luoda ympäristöjä:</span><span class="sxs-lookup"><span data-stu-id="3f2d0-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="3f2d0-110">Tuotteen varastointiyksikkö (SKU)</span><span class="sxs-lookup"><span data-stu-id="3f2d0-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="3f2d0-111">Power Apps P2 -huoltosuunnitelma</span><span class="sxs-lookup"><span data-stu-id="3f2d0-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="3f2d0-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="3f2d0-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="3f2d0-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3f2d0-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="3f2d0-114">Microsoft Dynamics 365 Enterprise Edition -palvelupaketti</span><span class="sxs-lookup"><span data-stu-id="3f2d0-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="3f2d0-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3f2d0-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="3f2d0-116">Huomaa, että myös monet Microsoft Officen varastointiyksiköt sisältävät tämän oikeuden itsenäisen Power Apps-palvelupaketin 2 varastointiyksiköiden lisäksi.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="3f2d0-117">Olennaista on, että jokin näistä varastointiyksiköistä on käytössä.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="3f2d0-118">Siirry osoitteeseen [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="3f2d0-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="3f2d0-119">Luo ympäristöjä noudattamalla ohjeita kohdassa [Human Resourcesin valmistelu](/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="3f2d0-119">Create the environments by following the instructions in [Provision Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]