---
title: Ympäristöä ei voi luoda PowerAppsin hallintakeskuksessa
description: Tässä ohjeaiheessa kerrotaan, mitä voidaan tehdä, jos järjestelmänvalvoja ei voi luoda ympäristöä Microsoft PowerAppsin hallintakeskuksessa.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 96119ca869cbbb15ed8d8d5d0fe3b0f94b5f36cc
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742839"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="0ad6d-103">PowerApps-hallintakeskuksessa ei voi luoda ympäristöä</span><span class="sxs-lookup"><span data-stu-id="0ad6d-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0ad6d-104">**Ongelma**</span><span class="sxs-lookup"><span data-stu-id="0ad6d-104">**Issue**</span></span>

- <span data-ttu-id="0ad6d-105">Vuokraajan tai ympäristön järjestelmänvalvoja ei voi luoda ympäristöä Microsoft PowerAppsin hallintakeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="0ad6d-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="0ad6d-106">Tätä vaihetta suorittavalle käyttäjälle ei ole määritetty suoraan käyttöoikeutta, jonka antaa käyttäjille oikeuden suorittaa ympäristön luontivaiheen.</span><span class="sxs-lookup"><span data-stu-id="0ad6d-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="0ad6d-107">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="0ad6d-107">**Solution**</span></span>

<span data-ttu-id="0ad6d-108">Varmista, että vuokraajan järjestelmänvalvoja on määrittänyt kelvollisen PowerApps P2 -käyttöoikeuden käyttäjälle, joka suorittaa ympäristön luontivaiheen.</span><span class="sxs-lookup"><span data-stu-id="0ad6d-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="0ad6d-109">Tämä oikeus on seuraavissa Microsoft Dynamics -palvelusopimuksissa.</span><span class="sxs-lookup"><span data-stu-id="0ad6d-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="0ad6d-110">Tuotteen varastointiyksikkö (SKU)</span><span class="sxs-lookup"><span data-stu-id="0ad6d-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="0ad6d-111">PowerApps P2 -palvelusopimus</span><span class="sxs-lookup"><span data-stu-id="0ad6d-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="0ad6d-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="0ad6d-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="0ad6d-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="0ad6d-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="0ad6d-114">Microsoft Dynamics 365 Enterprise Edition -palvelupaketti</span><span class="sxs-lookup"><span data-stu-id="0ad6d-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="0ad6d-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="0ad6d-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="0ad6d-116">Huomaa, että myös monet Microsoft Officen varastointiyksiköt sisältävät tämän oikeuden itsenäisen PowerApps-palvelupaketin 2 varastointiyksiköiden lisäksi.</span><span class="sxs-lookup"><span data-stu-id="0ad6d-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="0ad6d-117">Olennaista on, että jokin näistä varastointiyksiköistä on käytössä.</span><span class="sxs-lookup"><span data-stu-id="0ad6d-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="0ad6d-118">Siirry osoitteeseen [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="0ad6d-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="0ad6d-119">Luo ympäristöjä noudattamalla ohjeita kohdassa [Talentin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="0ad6d-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
