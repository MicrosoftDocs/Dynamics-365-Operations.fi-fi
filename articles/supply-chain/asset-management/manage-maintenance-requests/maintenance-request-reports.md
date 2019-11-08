---
title: Ylläpitopyyntöraportit
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpitopyyntöraportit luodaan resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0734416eccf149330b390cce897d2c254f6c698b
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571619"
---
# <a name="maintenance-request-reports"></a><span data-ttu-id="3d39a-103">Ylläpitopyyntöraportit</span><span class="sxs-lookup"><span data-stu-id="3d39a-103">Maintenance request reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3d39a-104">Resurssien hallinnassa voit luoda kaksi raporttia, jotka liittyvät ylläpitopyyntöihin.</span><span class="sxs-lookup"><span data-stu-id="3d39a-104">In Asset Management, you can generate two reports that are related to maintenance requests.</span></span> <span data-ttu-id="3d39a-105">Yhdessä raportissa näkyy tietoja, ja toisessa raportissa on luettelo, jota voidaan käyttää suunnitteluun ja seurantaan.</span><span class="sxs-lookup"><span data-stu-id="3d39a-105">One report shows details, and the other report provides a list that can be used for planning and follow-up.</span></span>

## <a name="create-a-maintenance-request-details-report"></a><span data-ttu-id="3d39a-106">Ylläpitopyyntöjen tietoraportin luominen</span><span class="sxs-lookup"><span data-stu-id="3d39a-106">Create a Maintenance request details report</span></span>

<span data-ttu-id="3d39a-107">**Ylläpitopyynnön tiedot** -raportissa näkyy erilaisia ylläpitopyyntöihin liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="3d39a-107">The **Maintenance request details** report shows various information that is related to maintenance requests.</span></span>

1. <span data-ttu-id="3d39a-108">Valitse **Resurssien hallinta** \> **Raportit** \> **Ylläpitopyynnöt** \> **Ylläpitopyynnön tiedot**.</span><span class="sxs-lookup"><span data-stu-id="3d39a-108">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request details**.</span></span>
2. <span data-ttu-id="3d39a-109">**Sisällytettävät tietueet** -pikavälilehdessä voit valita raporttiin sisällytettävät tietyt ylläpitopyynnöt.</span><span class="sxs-lookup"><span data-stu-id="3d39a-109">On the **Records to include** FastTab, you can select specific maintenance requests to include on the report.</span></span>
3. <span data-ttu-id="3d39a-110">**Suorita taustalla** -pikavälilehdessä voit määrittää raportin luonnin erätyönä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="3d39a-110">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="3d39a-111">Luo raportti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d39a-111">Select **OK** to generate the report.</span></span>

<span data-ttu-id="3d39a-112">Seuraavassa kuvassa on esimerkki **Ylläpitopyynnön tiedot** -raportista.</span><span class="sxs-lookup"><span data-stu-id="3d39a-112">The following illustration shows an example of the **Maintenance request details** report.</span></span>

![Ylläpitopyynnön tietoraportti](media/09-manage-maintenance-requests.png)

## <a name="create-a-maintenance-request-list-report"></a><span data-ttu-id="3d39a-114">Ylläpitopyyntöjen luetteloraportin luominen</span><span class="sxs-lookup"><span data-stu-id="3d39a-114">Create a Maintenance request list report</span></span>

<span data-ttu-id="3d39a-115">**Ylläpitopyyntöluettelo**-raportissa on luettelo kaikista saman pyyntötyypin ylläpitopyynnöistä.</span><span class="sxs-lookup"><span data-stu-id="3d39a-115">The **Maintenance request list** report shows a list of all maintenance requests of the same request type.</span></span>

1. <span data-ttu-id="3d39a-116">Valitse **Resurssien hallinta** \> **Raportit** \> **Ylläpitopyynnöt** \> **Ylläpitopyyntöluettelo**.</span><span class="sxs-lookup"><span data-stu-id="3d39a-116">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request list**.</span></span>
2. <span data-ttu-id="3d39a-117">**Sisällytettävät tietueet** -pikavälilehdessä voit tehdä valintoja raporttiin sisällytettävistä ylläpitopyynnöistä.</span><span class="sxs-lookup"><span data-stu-id="3d39a-117">On the **Records to include** FastTab, you can make selections to define which maintenance requests are included on the report.</span></span>
3. <span data-ttu-id="3d39a-118">**Suorita taustalla** -pikavälilehdessä voit määrittää raportin luonnin erätyönä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="3d39a-118">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="3d39a-119">Luo raportti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d39a-119">Select **OK** to generate the report.</span></span>

<span data-ttu-id="3d39a-120">Seuraavassa kuvassa on esimerkki **Ylläpitopyyntöluettelo** -raportista kaikille aktiivisille yläpitopyynnöille.</span><span class="sxs-lookup"><span data-stu-id="3d39a-120">The following illustration shows an example of the **Maintenance request list** report for all active maintenance requests.</span></span>

![Ylläpitopyynnön luetteloraportti](media/10-manage-maintenance-requests.png)
