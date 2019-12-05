---
title: Työnkulun usein kysytyt kysymykset
description: Tässä ohjeaiheessa on usein kysyttyjä kysymyksiä työnkulkujärjestelmästä.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
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
ms.openlocfilehash: 0188e8ed3cbbfd7dbccd7d13cf6129e146a919ac
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772694"
---
# <a name="workflow-faq"></a><span data-ttu-id="978b9-103">Työnkulun usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="978b9-103">Workflow FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="978b9-104">Tässä ohjeaiheessa on usein kysyttyjä kysymyksiä työnkulkujärjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="978b9-104">This topic answers frequently asked questions about the workflow system.</span></span>

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="978b9-105">Miksi ilmoituksia on useita, kun työnimike hylätään?</span><span class="sxs-lookup"><span data-stu-id="978b9-105">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="978b9-106">Kun työnimike hylätään, kyseinen työnimike valmistuu hylättynä.</span><span class="sxs-lookup"><span data-stu-id="978b9-106">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="978b9-107">Toinen työnimike luodaan ja määritetään aloittajalle.</span><span class="sxs-lookup"><span data-stu-id="978b9-107">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="978b9-108">Tämä tarkoittaa, että aloittaja saa ilmoituksen hylätystä työnimikkeestä. Käyttäjä, joka on määritetty uuteen muutospyynnön työnimikkeeseen, saa erillisen ilmoituksen.</span><span class="sxs-lookup"><span data-stu-id="978b9-108">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="978b9-109">Nämä ilmoitukset on tarkoitettu eri työnimikkeelle, mutta niiden samankaltaisuus voi aiheuttaa hämmennystä.</span><span class="sxs-lookup"><span data-stu-id="978b9-109">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="978b9-110">Pyrimme parantamaan tätä myöhemmissä julkaisuissa.</span><span class="sxs-lookup"><span data-stu-id="978b9-110">We are looking at ways to improve this in a future release.</span></span>

## <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="978b9-111">Miksi työnkulun vienti ei ole mahdollista?</span><span class="sxs-lookup"><span data-stu-id="978b9-111">Why are my workflow exports failing?</span></span>
<span data-ttu-id="978b9-112">Työnkulun viennissä on tällä hetkellä rajoitus, joka estää työnkulkujen nimiä ylittämästä 48 merkkiä.</span><span class="sxs-lookup"><span data-stu-id="978b9-112">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="978b9-113">Jos nimi on pidempi kuin 48 merkkiä, palvelin ei voi todentaa pyyntöä ja / tai estää tiedoston viemisen ilman tiedostotyyppiä.</span><span class="sxs-lookup"><span data-stu-id="978b9-113">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="978b9-114">Seuraava blogikirjoitus sisältää lisätietoja [Työnkulun viennin vian määrityksestä](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="978b9-114">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a><span data-ttu-id="978b9-115">Voiko työnkulun lähettäjä myös hyväksyä työnkulun?</span><span class="sxs-lookup"><span data-stu-id="978b9-115">Can the submitter of a workflow also approve the workflow?</span></span>
<span data-ttu-id="978b9-116">Kyllä, Työnkulun lähettäjä voi myös hyväksyä työnkulun, jos määritys sen sallii.</span><span class="sxs-lookup"><span data-stu-id="978b9-116">Yes, a submitter of a workflow can also approve the workflow if it is configured that way.</span></span> <span data-ttu-id="978b9-117">Voit estää tämän valitsemalla kohdassa **Työnkulkuparametrit > Yleiset > Hyväksyjä > Estä lähettäjän hyväksyntä** **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="978b9-117">To prevent this behavior, set **Workflow parameters > General > Approver > Disallow approval by submitter** to **Yes**.</span></span>

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a><span data-ttu-id="978b9-118">Voinko lisätä työnkulkuihin hälytyksiä toimittamaan ilmoituksia käyttäjille?</span><span class="sxs-lookup"><span data-stu-id="978b9-118">Can I add alerts to workflows to provide notifications to users?</span></span>
<span data-ttu-id="978b9-119">Seuraavat seikat on otettava huomioon, kun työnkulkuihin lisätään hälytyksiä toimittamaan ilmoituksia:</span><span class="sxs-lookup"><span data-stu-id="978b9-119">Here are a few key areas to note about adding alerts to workflows to provide notifications:</span></span>
- <span data-ttu-id="978b9-120">Hälytys- ja työnkulkuilmoitusmekanismien vertailu</span><span class="sxs-lookup"><span data-stu-id="978b9-120">Alerts versus workflow notification mechanisms</span></span>
    - <span data-ttu-id="978b9-121">Tietueiden muutoksille voidaan määrittää hälytyksiä.</span><span class="sxs-lookup"><span data-stu-id="978b9-121">Alerts can be set up for record changes.</span></span> <span data-ttu-id="978b9-122">Työnkulut muuttavat tietueita, joten työnkulun aiheuttamaan tietuemuutokseen voi määrittää hälytyksen.</span><span class="sxs-lookup"><span data-stu-id="978b9-122">Workflows change records, so it's possible to set up an alert related to a record change caused by a workflow.</span></span> <span data-ttu-id="978b9-123">Koska työnkuluissa on erilaisia sisäisiä ilmoitusasetuksia, hälytysten käyttäminen ei ole paras mahdollinen vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="978b9-123">However, because workflows have different built-in notification options, using alerts isn’t ideal.</span></span>
- <span data-ttu-id="978b9-124">Työnkulkujen vakioilmoitukset</span><span class="sxs-lookup"><span data-stu-id="978b9-124">Standard notifications from workflows</span></span> 
    - <span data-ttu-id="978b9-125">Työnkulut sisältävät valmiita sähköposti-ilmoituksia.</span><span class="sxs-lookup"><span data-stu-id="978b9-125">Workflows have built in email notifications.</span></span> <span data-ttu-id="978b9-126">Asiakas voi määrittää ilmoitukset lähettämään käyttäjille sähköpostiviestejä.</span><span class="sxs-lookup"><span data-stu-id="978b9-126">A customer can configure the notifications so that the users are sent emails.</span></span> <span data-ttu-id="978b9-127">Nämä ilmoitukset eivät aiheuta toimintokeskuksen sanomien lähettämistä käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="978b9-127">Those notifications don’t result in Action Center messages for users.</span></span>
    - <span data-ttu-id="978b9-128">Tulevaan päivitykseen lisätään toimintokeskuksen sanoma, jotta työnkulun työnimike määritetään käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="978b9-128">In a future update we will be adding an Action Center message so a user is assigned a workflow work item.</span></span> 
- <span data-ttu-id="978b9-129">Ilmoitusten lisääminen työnkulkuihin</span><span class="sxs-lookup"><span data-stu-id="978b9-129">Adding notifications to workflows</span></span>
    - <span data-ttu-id="978b9-130">Toimintokeskuksen sanomat voidaan luoda tietyille käyttäjille, kuten työnkulusta luotu sanoma X++-kielessä.</span><span class="sxs-lookup"><span data-stu-id="978b9-130">Action Center messages can be created for specific users, such as a message created from a workflow in X++.</span></span>
    - <span data-ttu-id="978b9-131">[Työnkuluissa on liiketoimintatapahtumia](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow), joilla asiakas voi käynnistää työnkulut, joissa on heidän etsimänsä ilmoitukset.</span><span class="sxs-lookup"><span data-stu-id="978b9-131">[Workflows have Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) that the customer could use to trigger Flows have the notifications that they are looking for.</span></span>   

<span data-ttu-id="978b9-132">Tiivistäen voi todeta, että jos käyttäjä ei saa oikeaa ilmoitusta toimintokeskuksesta, kun heille määritetään työnkulun työnimike, he voivat muodostaa lisäilmoituksia tai toisia ilmoituksia käyttämällä [työnkulun liiketoimintatapahtumia](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) yhdessä Microsoft Power Automaten kanssa.</span><span class="sxs-lookup"><span data-stu-id="978b9-132">In summary, if a user does not get the proper notification from the Action Center when they are assigned a workflow work item, then leverage [Workflow Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) with Microsoft Power Automate to provide additional or different notifications.</span></span>
