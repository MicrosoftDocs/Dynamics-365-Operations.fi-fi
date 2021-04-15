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
ms.openlocfilehash: f1a086f1b710de9bad898abc740286c174ae3be7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797982"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="0ed35-103">Power Apps-hallintakeskuksessa ei voi luoda ympäristöä</span><span class="sxs-lookup"><span data-stu-id="0ed35-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0ed35-104">**Lähetä**</span><span class="sxs-lookup"><span data-stu-id="0ed35-104">**Issue**</span></span>

- <span data-ttu-id="0ed35-105">Vuokraajan tai ympäristön järjestelmänvalvoja ei voi luoda ympäristöä Microsoft Power Appsin hallintakeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="0ed35-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="0ed35-106">Käyttäjällä ei ole käyttöoikeutta luoda ympäristöjä.</span><span class="sxs-lookup"><span data-stu-id="0ed35-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="0ed35-107">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="0ed35-107">**Solution**</span></span>

<span data-ttu-id="0ed35-108">Varmista, että vuokraajan järjestelmänvalvoja on määrittänyt ympäristöä luovalle käyttäjälle kelvollisen Power Apps P2 -käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="0ed35-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="0ed35-109">Seuraavissa Microsoft Dynamics -palvelusuunnitelmissa on mukana oikeudet luoda ympäristöjä:</span><span class="sxs-lookup"><span data-stu-id="0ed35-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="0ed35-110">Tuotteen varastointiyksikkö (SKU)</span><span class="sxs-lookup"><span data-stu-id="0ed35-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="0ed35-111">Power Apps P2 -huoltosuunnitelma</span><span class="sxs-lookup"><span data-stu-id="0ed35-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="0ed35-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="0ed35-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="0ed35-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="0ed35-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="0ed35-114">Microsoft Dynamics 365 Enterprise Edition -palvelupaketti</span><span class="sxs-lookup"><span data-stu-id="0ed35-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="0ed35-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="0ed35-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="0ed35-116">Huomaa, että myös monet Microsoft Officen varastointiyksiköt sisältävät tämän oikeuden itsenäisen Power Apps-palvelupaketin 2 varastointiyksiköiden lisäksi.</span><span class="sxs-lookup"><span data-stu-id="0ed35-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="0ed35-117">Olennaista on, että jokin näistä varastointiyksiköistä on käytössä.</span><span class="sxs-lookup"><span data-stu-id="0ed35-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="0ed35-118">Siirry osoitteeseen [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="0ed35-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="0ed35-119">Luo ympäristöjä noudattamalla ohjeita kohdassa [Human Resourcesin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="0ed35-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]