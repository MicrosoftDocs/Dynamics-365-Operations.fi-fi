---
title: Tehtävien hallinnan yleiskatsaus
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen päälliköiden ja työntekijöiden tehtävienhallinnasta.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 6fbd0ead6d73f4b032bdc3805fce87ec9c802535
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006157"
---
# <a name="task-management-overview"></a><span data-ttu-id="27616-103">Tehtävien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="27616-103">Task management overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="27616-104">Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen päälliköiden ja työntekijöiden tehtävienhallinnasta.</span><span class="sxs-lookup"><span data-stu-id="27616-104">This topic provides an overview of task management for managers and workers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="27616-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="27616-105">Overview</span></span>

<span data-ttu-id="27616-106">Vähittäismyyntiympäristössä on aina vaikeaa varmistaa, että oikea henkilö suorittaa tehtävät oikeaan aikaan.</span><span class="sxs-lookup"><span data-stu-id="27616-106">In a retail environment, it's always difficult to make sure that tasks are performed by the right person at the right time.</span></span> <span data-ttu-id="27616-107">Vähittäiskauppiaiden on pystyttävä ilmoittamaan työntekijöille tulevista tehtävistä ja tarjoamaan asiaan liittyvää liiketoimintakontekstia, jotta tehtävät voidaan suorittaa oikein ja ajallaan.</span><span class="sxs-lookup"><span data-stu-id="27616-107">Retailers must be able to notify workers about upcoming tasks and provide related business context, so that the tasks can be completed correctly and on time.</span></span>

<span data-ttu-id="27616-108">Tehtävienhallinta on tuottavuuteen liittyvä toiminto Dynamics 365 Commercessa. Sen avulla päälliköt ja työntekijät voivat luoda tehtäväluetteloita, seurata tehtävän tilaa ja integroida näitä toimintoja Commercen taustatoiminnon ja myyntipistesovellusten välillä.</span><span class="sxs-lookup"><span data-stu-id="27616-108">Task management is a productivity feature in Dynamics 365 Commerce that lets managers and workers create task lists, manage assignment criteria, track task status, and integrate these operations between Commerce back office and point of sale (POS) applications.</span></span>

<span data-ttu-id="27616-109">Headquarters-sovelluksen henkilöt voivat käyttää tehtävienhallintaa vähittäismyymälöiden tehtäväluetteloiden luomisessa ja myymälän tai työntekijän tilan seuraamisessa.</span><span class="sxs-lookup"><span data-stu-id="27616-109">Headquarters personas can use task management to create task lists for retail stores, and to track status by store or worker.</span></span> <span data-ttu-id="27616-110">Ne voivat myös luoda toistuvia tehtäviä (esimerkiksi torstai-illan loppusaldon tarkistusluettelo).</span><span class="sxs-lookup"><span data-stu-id="27616-110">They can also create recurrent tasks (for example, "Thursday night closing checklist").</span></span>

<span data-ttu-id="27616-111">Myymäläpäälliköt voivat tehtävienhallinnan avulla määrittää tehtäviä yksittäiselle työntekijälle, lähettää ilmoituksia tulevista tai erääntyvistä tehtävistä, päivittää tehtävän tilan ja luoda tehtäviä yhtä tarkoitusta varten myyntipistesovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="27616-111">Store managers can use task management to assign tasks to individual workers, send notifications about upcoming tasks or tasks that are past due, update task status, and create single-purpose tasks in the POS application.</span></span> <span data-ttu-id="27616-112">Työntekijät voivat tämän jälkeen katsella ilmoituksia, tarkastella tehtävän tietoja ja päivittää tehtävän tilan myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="27616-112">Workers can then see notifications, view task details, and update task status at the POS.</span></span>

<span data-ttu-id="27616-113">Seuraavassa kuvassa näkyy tehtävienhallinnan käsitteellinen arkkitehtuuri Commercessa.</span><span class="sxs-lookup"><span data-stu-id="27616-113">The following illustration shows the conceptual architecture of task management in Commerce.</span></span>

![Tehtävienhallinnan käsitteellinen arkkitehtuuri](media/Tasks-management-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="27616-115">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="27616-115">Additional resources</span></span>

[<span data-ttu-id="27616-116">Tehtävien hallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="27616-116">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="27616-117">Tehtäväluetteloiden luominen ja tehtävien lisääminen</span><span class="sxs-lookup"><span data-stu-id="27616-117">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="27616-118">Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille</span><span class="sxs-lookup"><span data-stu-id="27616-118">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="27616-119">Tehtävien hallinta myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="27616-119">Task management in POS</span></span>](task-mgmt-POS.md)
