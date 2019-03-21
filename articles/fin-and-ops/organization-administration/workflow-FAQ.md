---
title: Työnkulun usein kysytyt kysymykset
description: Tässä ohjeaiheessa on usein kysyttyjä kysymyksiä Microsoft Dynamics 365 for Finance and Operationsin työnkulkujärjestelmässä.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
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
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/01/2019
ms.locfileid: "773207"
---
# <a name="workflow-system"></a><span data-ttu-id="4c49b-103">Työnkulkujärjestelmä</span><span class="sxs-lookup"><span data-stu-id="4c49b-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c49b-104">Tässä ohjeaiheessa on usein kysyttyjä kysymyksiä Microsoft Dynamics 365 for Finance and Operationsin työnkulkujärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="4c49b-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="4c49b-105">Ilmoitukset</span><span class="sxs-lookup"><span data-stu-id="4c49b-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="4c49b-106">Miksi ilmoituksia on useita, kun työnimike hylätään?</span><span class="sxs-lookup"><span data-stu-id="4c49b-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="4c49b-107">Kun työnimike hylätään, kyseinen työnimike valmistuu hylättynä.</span><span class="sxs-lookup"><span data-stu-id="4c49b-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="4c49b-108">Toinen työnimike luodaan ja määritetään aloittajalle.</span><span class="sxs-lookup"><span data-stu-id="4c49b-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="4c49b-109">Tämä tarkoittaa, että aloittaja saa ilmoituksen hylätystä työnimikkeestä. Käyttäjä, joka on määritetty uuteen muutospyynnön työnimikkeeseen, saa erillisen ilmoituksen.</span><span class="sxs-lookup"><span data-stu-id="4c49b-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="4c49b-110">Nämä ilmoitukset on tarkoitettu eri työnimikkeelle, mutta niiden samankaltaisuus voi aiheuttaa hämmennystä.</span><span class="sxs-lookup"><span data-stu-id="4c49b-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="4c49b-111">Pyrimme parantamaan tätä myöhemmissä julkaisuissa.</span><span class="sxs-lookup"><span data-stu-id="4c49b-111">We are looking at ways to improve this in a future release.</span></span>
