---
title: Tehtävien hallinta myyntipisteessä
description: Tässä ohjeaiheessa kuvataan Microsoft Dynamics 365 Commercen myyntipistesovelluksen tehtävienhallintaa.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 38ee9db94b3b222e8c0ce5d0883f47bd5d3e7d22
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796919"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="3ce1c-103">Tehtävien hallinta myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="3ce1c-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3ce1c-104">Tässä ohjeaiheessa kuvataan Microsoft Dynamics 365 Commercen myyntipistesovelluksen tehtävienhallintaa.</span><span class="sxs-lookup"><span data-stu-id="3ce1c-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="3ce1c-105">Dynamics 365 Commercen myyntipistesovelluksessa on tehtävienhallintatoimintoja, joiden avulla myymäläpäälliköt ja työntekijät voivat hallita tehtäviä ja päivittää tehtävän tilan.</span><span class="sxs-lookup"><span data-stu-id="3ce1c-105">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="3ce1c-106">Myymälän työntekijät voivat käyttää tehtäviä valitsemalla **Tehtävät**-ruudun myyntipisteen aloitussivulla tai valitsemalla tehtävän ilmoitukset.</span><span class="sxs-lookup"><span data-stu-id="3ce1c-106">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="3ce1c-107">Oletusarvon mukaan myymälän työntekijät siirretään **Omat tehtävät** -välilehteen, jossa he voivat tarkastella heille määritettyjä tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="3ce1c-107">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="3ce1c-108">He voivat kuitenkin helposti siirtyä **Erääntyneet tehtävät**-, **Avoimet tehtävät**- ja **Tehtäväluettelot**-välilehtien välillä.</span><span class="sxs-lookup"><span data-stu-id="3ce1c-108">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="3ce1c-109">Myymäläpäälliköiden tehtävätoiminnot</span><span class="sxs-lookup"><span data-stu-id="3ce1c-109">Task operations for store managers</span></span>

<span data-ttu-id="3ce1c-110">Myymäläpäälliköt voivat tehdä seuraavia tehtävätoimintoja myyntipistesovelluksessa komentopalkin painikkeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="3ce1c-110">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="3ce1c-111">**Määritä** – Määritä valitut tehtävät myymälän työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="3ce1c-111">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="3ce1c-112">**Tehtävän tila** – Muuta valittujen tehtävien tilaa.</span><span class="sxs-lookup"><span data-stu-id="3ce1c-112">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="3ce1c-113">**Suodatin** – Oletusarvon mukaan vain aktiiviset tehtävät näytetään.</span><span class="sxs-lookup"><span data-stu-id="3ce1c-113">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="3ce1c-114">Suodattimien avulla päälliköt voivat kuitenkin tarkastella kaikkia tehtäviä, myös valmiita ja peruutettuja tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="3ce1c-114">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="3ce1c-115">**Uusi tehtävä** – Luo tehtävä aiemmin luotuun tehtäväluetteloon tai luo tehtävä yksittäistä tarkoitusta varten.</span><span class="sxs-lookup"><span data-stu-id="3ce1c-115">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="3ce1c-116">Myymälän työntekijät voivat tehdä seuraavia tehtävätoimintoja myyntipistesovelluksessa komentopalkin painikkeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="3ce1c-116">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="3ce1c-117">**Tehtävän tila** – Muuta valittujen tehtävien tilaa.</span><span class="sxs-lookup"><span data-stu-id="3ce1c-117">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="3ce1c-118">**Suodatin** – Oletusarvon mukaan vain aktiiviset tehtävät näytetään.</span><span class="sxs-lookup"><span data-stu-id="3ce1c-118">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="3ce1c-119">Suodattimien avulla työntekijät voivat kuitenkin tarkastella kaikkia tehtäviä, myös valmiita ja peruutettuja tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="3ce1c-119">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="3ce1c-120">Seuraavassa kuvassa näkyy Commercen myyntipistesovelluksen **Omat tehtävät** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="3ce1c-120">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Omat tehtävät -välilehti Commercen myyntipistesovelluksessa](media/POS-task-management.png)

<span data-ttu-id="3ce1c-122">Seuraavassa on kuvattu **Tehtäväluettelot**-välilehti</span><span class="sxs-lookup"><span data-stu-id="3ce1c-122">The following illustration shows the **Task lists** tab.</span></span>

![Tehtäväluettelot-välilehti Commercen myyntipistesovelluksessa](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="3ce1c-124">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="3ce1c-124">Additional resources</span></span>

[<span data-ttu-id="3ce1c-125">Tehtävien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="3ce1c-125">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="3ce1c-126">Tehtävien hallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3ce1c-126">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="3ce1c-127">Tehtäväluetteloiden luominen ja tehtävien lisääminen</span><span class="sxs-lookup"><span data-stu-id="3ce1c-127">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="3ce1c-128">Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille</span><span class="sxs-lookup"><span data-stu-id="3ce1c-128">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
