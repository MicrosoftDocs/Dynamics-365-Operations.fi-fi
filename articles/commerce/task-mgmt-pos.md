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
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cc685fcd584fe2ab5cd9282e8fbefbd284d5b2a2
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036783"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="4de2e-103">Tehtävien hallinta myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="4de2e-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4de2e-104">Tässä ohjeaiheessa kuvataan Microsoft Dynamics 365 Commercen myyntipistesovelluksen tehtävienhallintaa.</span><span class="sxs-lookup"><span data-stu-id="4de2e-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="4de2e-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4de2e-105">Overview</span></span>

<span data-ttu-id="4de2e-106">Dynamics 365 Commercen myyntipistesovelluksessa on tehtävienhallintatoimintoja, joiden avulla myymäläpäälliköt ja työntekijät voivat hallita tehtäviä ja päivittää tehtävän tilan.</span><span class="sxs-lookup"><span data-stu-id="4de2e-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="4de2e-107">Myymälän työntekijät voivat käyttää tehtäviä valitsemalla **Tehtävät**-ruudun myyntipisteen aloitussivulla tai valitsemalla tehtävän ilmoitukset.</span><span class="sxs-lookup"><span data-stu-id="4de2e-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="4de2e-108">Oletusarvon mukaan myymälän työntekijät siirretään **Omat tehtävät** -välilehteen, jossa he voivat tarkastella heille määritettyjä tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="4de2e-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="4de2e-109">He voivat kuitenkin helposti siirtyä **Erääntyneet tehtävät**-, **Avoimet tehtävät**- ja **Tehtäväluettelot**-välilehtien välillä.</span><span class="sxs-lookup"><span data-stu-id="4de2e-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="4de2e-110">Myymäläpäälliköiden tehtävätoiminnot</span><span class="sxs-lookup"><span data-stu-id="4de2e-110">Task operations for store managers</span></span>

<span data-ttu-id="4de2e-111">Myymäläpäälliköt voivat tehdä seuraavia tehtävätoimintoja myyntipistesovelluksessa komentopalkin painikkeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="4de2e-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="4de2e-112">**Määritä** – Määritä valitut tehtävät myymälän työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="4de2e-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="4de2e-113">**Tehtävän tila** – Muuta valittujen tehtävien tilaa.</span><span class="sxs-lookup"><span data-stu-id="4de2e-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="4de2e-114">**Suodatin** – Oletusarvon mukaan vain aktiiviset tehtävät näytetään.</span><span class="sxs-lookup"><span data-stu-id="4de2e-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="4de2e-115">Suodattimien avulla päälliköt voivat kuitenkin tarkastella kaikkia tehtäviä, myös valmiita ja peruutettuja tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="4de2e-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="4de2e-116">**Uusi tehtävä** – Luo tehtävä aiemmin luotuun tehtäväluetteloon tai luo tehtävä yksittäistä tarkoitusta varten.</span><span class="sxs-lookup"><span data-stu-id="4de2e-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="4de2e-117">Myymälän työntekijät voivat tehdä seuraavia tehtävätoimintoja myyntipistesovelluksessa komentopalkin painikkeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="4de2e-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="4de2e-118">**Tehtävän tila** – Muuta valittujen tehtävien tilaa.</span><span class="sxs-lookup"><span data-stu-id="4de2e-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="4de2e-119">**Suodatin** – Oletusarvon mukaan vain aktiiviset tehtävät näytetään.</span><span class="sxs-lookup"><span data-stu-id="4de2e-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="4de2e-120">Suodattimien avulla työntekijät voivat kuitenkin tarkastella kaikkia tehtäviä, myös valmiita ja peruutettuja tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="4de2e-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="4de2e-121">Seuraavassa kuvassa näkyy Commercen myyntipistesovelluksen **Omat tehtävät** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="4de2e-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Omat tehtävät -välilehti Commercen myyntipistesovelluksessa](media/POS-task-management.png)

<span data-ttu-id="4de2e-123">Seuraavassa on kuvattu **Tehtäväluettelot**-välilehti</span><span class="sxs-lookup"><span data-stu-id="4de2e-123">The following illustration shows the **Task lists** tab.</span></span>

![Tehtäväluettelot-välilehti Commercen myyntipistesovelluksessa](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="4de2e-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4de2e-125">Additional resources</span></span>

[<span data-ttu-id="4de2e-126">Tehtävien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4de2e-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="4de2e-127">Tehtävien hallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4de2e-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="4de2e-128">Tehtäväluetteloiden luominen ja tehtävien lisääminen</span><span class="sxs-lookup"><span data-stu-id="4de2e-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="4de2e-129">Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille</span><span class="sxs-lookup"><span data-stu-id="4de2e-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
