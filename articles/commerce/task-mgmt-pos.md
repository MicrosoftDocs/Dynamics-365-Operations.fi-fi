---
title: Tehtävien hallinta myyntipisteessä
description: Tässä ohjeaiheessa kuvataan Microsoft Dynamics 365 Commercen myyntipistesovelluksen tehtävienhallintaa.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 889cc90b534de33ccd0e2bea367b2da42b5d72e0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006182"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="f29fa-103">Tehtävien hallinta myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="f29fa-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f29fa-104">Tässä ohjeaiheessa kuvataan Microsoft Dynamics 365 Commercen myyntipistesovelluksen tehtävienhallintaa.</span><span class="sxs-lookup"><span data-stu-id="f29fa-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="f29fa-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f29fa-105">Overview</span></span>

<span data-ttu-id="f29fa-106">Dynamics 365 Commercen myyntipistesovelluksessa on tehtävienhallintatoimintoja, joiden avulla myymäläpäälliköt ja työntekijät voivat hallita tehtäviä ja päivittää tehtävän tilan.</span><span class="sxs-lookup"><span data-stu-id="f29fa-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="f29fa-107">Myymälän työntekijät voivat käyttää tehtäviä valitsemalla **Tehtävät**-ruudun myyntipisteen aloitussivulla tai valitsemalla tehtävän ilmoitukset.</span><span class="sxs-lookup"><span data-stu-id="f29fa-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="f29fa-108">Oletusarvon mukaan myymälän työntekijät siirretään **Omat tehtävät** -välilehteen, jossa he voivat tarkastella heille määritettyjä tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="f29fa-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="f29fa-109">He voivat kuitenkin helposti siirtyä **Erääntyneet tehtävät**-, **Avoimet tehtävät**- ja **Tehtäväluettelot**-välilehtien välillä.</span><span class="sxs-lookup"><span data-stu-id="f29fa-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="f29fa-110">Myymäläpäälliköiden tehtävätoiminnot</span><span class="sxs-lookup"><span data-stu-id="f29fa-110">Task operations for store managers</span></span>

<span data-ttu-id="f29fa-111">Myymäläpäälliköt voivat tehdä seuraavia tehtävätoimintoja myyntipistesovelluksessa komentopalkin painikkeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="f29fa-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="f29fa-112">**Määritä** – Määritä valitut tehtävät myymälän työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="f29fa-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="f29fa-113">**Tehtävän tila** – Muuta valittujen tehtävien tilaa.</span><span class="sxs-lookup"><span data-stu-id="f29fa-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="f29fa-114">**Suodatin** – Oletusarvon mukaan vain aktiiviset tehtävät näytetään.</span><span class="sxs-lookup"><span data-stu-id="f29fa-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="f29fa-115">Suodattimien avulla päälliköt voivat kuitenkin tarkastella kaikkia tehtäviä, myös valmiita ja peruutettuja tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="f29fa-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="f29fa-116">**Uusi tehtävä** – Luo tehtävä aiemmin luotuun tehtäväluetteloon tai luo tehtävä yksittäistä tarkoitusta varten.</span><span class="sxs-lookup"><span data-stu-id="f29fa-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="f29fa-117">Myymälän työntekijät voivat tehdä seuraavia tehtävätoimintoja myyntipistesovelluksessa komentopalkin painikkeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="f29fa-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="f29fa-118">**Tehtävän tila** – Muuta valittujen tehtävien tilaa.</span><span class="sxs-lookup"><span data-stu-id="f29fa-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="f29fa-119">**Suodatin** – Oletusarvon mukaan vain aktiiviset tehtävät näytetään.</span><span class="sxs-lookup"><span data-stu-id="f29fa-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="f29fa-120">Suodattimien avulla työntekijät voivat kuitenkin tarkastella kaikkia tehtäviä, myös valmiita ja peruutettuja tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="f29fa-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="f29fa-121">Seuraavassa kuvassa näkyy Commercen myyntipistesovelluksen **Omat tehtävät** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="f29fa-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Omat tehtävät -välilehti Commercen myyntipistesovelluksessa](media/POS-task-management.png)

<span data-ttu-id="f29fa-123">Seuraavassa on kuvattu **Tehtäväluettelot**-välilehti</span><span class="sxs-lookup"><span data-stu-id="f29fa-123">The following illustration shows the **Task lists** tab.</span></span>

![Tehtäväluettelot-välilehti Commercen myyntipistesovelluksessa](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="f29fa-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f29fa-125">Additional resources</span></span>

[<span data-ttu-id="f29fa-126">Tehtävien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f29fa-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="f29fa-127">Tehtävien hallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f29fa-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="f29fa-128">Tehtäväluetteloiden luominen ja tehtävien lisääminen</span><span class="sxs-lookup"><span data-stu-id="f29fa-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="f29fa-129">Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille</span><span class="sxs-lookup"><span data-stu-id="f29fa-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
