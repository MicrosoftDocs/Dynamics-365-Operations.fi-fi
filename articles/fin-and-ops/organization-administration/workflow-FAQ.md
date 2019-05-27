---
title: Työnkulun usein kysytyt kysymykset
description: Tässä ohjeaiheessa on usein kysyttyjä kysymyksiä Microsoft Dynamics 365 for Finance and Operationsin työnkulkujärjestelmässä.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509288"
---
# <a name="workflow-system"></a><span data-ttu-id="6ed31-103">Työnkulkujärjestelmä</span><span class="sxs-lookup"><span data-stu-id="6ed31-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ed31-104">Tässä ohjeaiheessa on usein kysyttyjä kysymyksiä Microsoft Dynamics 365 for Finance and Operationsin työnkulkujärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="6ed31-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="6ed31-105">Ilmoitukset</span><span class="sxs-lookup"><span data-stu-id="6ed31-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="6ed31-106">Miksi ilmoituksia on useita, kun työnimike hylätään?</span><span class="sxs-lookup"><span data-stu-id="6ed31-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="6ed31-107">Kun työnimike hylätään, kyseinen työnimike valmistuu hylättynä.</span><span class="sxs-lookup"><span data-stu-id="6ed31-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="6ed31-108">Toinen työnimike luodaan ja määritetään aloittajalle.</span><span class="sxs-lookup"><span data-stu-id="6ed31-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="6ed31-109">Tämä tarkoittaa, että aloittaja saa ilmoituksen hylätystä työnimikkeestä. Käyttäjä, joka on määritetty uuteen muutospyynnön työnimikkeeseen, saa erillisen ilmoituksen.</span><span class="sxs-lookup"><span data-stu-id="6ed31-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="6ed31-110">Nämä ilmoitukset on tarkoitettu eri työnimikkeelle, mutta niiden samankaltaisuus voi aiheuttaa hämmennystä.</span><span class="sxs-lookup"><span data-stu-id="6ed31-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="6ed31-111">Pyrimme parantamaan tätä myöhemmissä julkaisuissa.</span><span class="sxs-lookup"><span data-stu-id="6ed31-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="6ed31-112">Miksi työnkulun vienti ei ole mahdollista?</span><span class="sxs-lookup"><span data-stu-id="6ed31-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="6ed31-113">Työnkulun viennissä on tällä hetkellä rajoitus, joka estää työnkulkujen nimiä ylittämästä 48 merkkiä.</span><span class="sxs-lookup"><span data-stu-id="6ed31-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="6ed31-114">Jos nimi on pidempi kuin 48 merkkiä, palvelin ei voi todentaa pyyntöä ja / tai estää tiedoston viemisen ilman tiedostotyyppiä.</span><span class="sxs-lookup"><span data-stu-id="6ed31-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="6ed31-115">Seuraava blogikirjoitus sisältää lisätietoja [Työnkulun viennin vian määrityksestä](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="6ed31-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>
