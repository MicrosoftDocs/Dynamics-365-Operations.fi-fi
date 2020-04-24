---
title: Ylläpitopyyntöraportit
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpitopyyntöraportit luodaan resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5abb62e7f92f62d4635309625d765e1c081052eb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205135"
---
# <a name="maintenance-request-reports"></a><span data-ttu-id="83cc1-103">Ylläpitopyyntöraportit</span><span class="sxs-lookup"><span data-stu-id="83cc1-103">Maintenance request reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="83cc1-104">Resurssien hallinnassa voit luoda kaksi raporttia, jotka liittyvät ylläpitopyyntöihin.</span><span class="sxs-lookup"><span data-stu-id="83cc1-104">In Asset Management, you can generate two reports that are related to maintenance requests.</span></span> <span data-ttu-id="83cc1-105">Yhdessä raportissa näkyy tietoja, ja toisessa raportissa on luettelo, jota voidaan käyttää suunnitteluun ja seurantaan.</span><span class="sxs-lookup"><span data-stu-id="83cc1-105">One report shows details, and the other report provides a list that can be used for planning and follow-up.</span></span>

## <a name="create-a-maintenance-request-details-report"></a><span data-ttu-id="83cc1-106">Ylläpitopyyntöjen tietoraportin luominen</span><span class="sxs-lookup"><span data-stu-id="83cc1-106">Create a Maintenance request details report</span></span>

<span data-ttu-id="83cc1-107">**Ylläpitopyynnön tiedot** -raportissa näkyy erilaisia ylläpitopyyntöihin liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="83cc1-107">The **Maintenance request details** report shows various information that is related to maintenance requests.</span></span>

1. <span data-ttu-id="83cc1-108">Valitse **Resurssien hallinta** \> **Raportit** \> **Ylläpitopyynnöt** \> **Ylläpitopyynnön tiedot**.</span><span class="sxs-lookup"><span data-stu-id="83cc1-108">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request details**.</span></span>
2. <span data-ttu-id="83cc1-109">**Sisällytettävät tietueet** -pikavälilehdessä voit valita raporttiin sisällytettävät tietyt ylläpitopyynnöt.</span><span class="sxs-lookup"><span data-stu-id="83cc1-109">On the **Records to include** FastTab, you can select specific maintenance requests to include on the report.</span></span>
3. <span data-ttu-id="83cc1-110">**Suorita taustalla** -pikavälilehdessä voit määrittää raportin luonnin erätyönä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="83cc1-110">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="83cc1-111">Luo raportti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="83cc1-111">Select **OK** to generate the report.</span></span>

<span data-ttu-id="83cc1-112">Seuraavassa kuvassa on esimerkki **Ylläpitopyynnön tiedot** -raportista.</span><span class="sxs-lookup"><span data-stu-id="83cc1-112">The following illustration shows an example of the **Maintenance request details** report.</span></span>

![Ylläpitopyynnön tietoraportti](media/09-manage-maintenance-requests.png)

## <a name="create-a-maintenance-request-list-report"></a><span data-ttu-id="83cc1-114">Ylläpitopyyntöjen luetteloraportin luominen</span><span class="sxs-lookup"><span data-stu-id="83cc1-114">Create a Maintenance request list report</span></span>

<span data-ttu-id="83cc1-115">**Ylläpitopyyntöluettelo**-raportissa on luettelo kaikista saman pyyntötyypin ylläpitopyynnöistä.</span><span class="sxs-lookup"><span data-stu-id="83cc1-115">The **Maintenance request list** report shows a list of all maintenance requests of the same request type.</span></span>

1. <span data-ttu-id="83cc1-116">Valitse **Resurssien hallinta** \> **Raportit** \> **Ylläpitopyynnöt** \> **Ylläpitopyyntöluettelo**.</span><span class="sxs-lookup"><span data-stu-id="83cc1-116">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request list**.</span></span>
2. <span data-ttu-id="83cc1-117">**Sisällytettävät tietueet** -pikavälilehdessä voit tehdä valintoja raporttiin sisällytettävistä ylläpitopyynnöistä.</span><span class="sxs-lookup"><span data-stu-id="83cc1-117">On the **Records to include** FastTab, you can make selections to define which maintenance requests are included on the report.</span></span>
3. <span data-ttu-id="83cc1-118">**Suorita taustalla** -pikavälilehdessä voit määrittää raportin luonnin erätyönä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="83cc1-118">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="83cc1-119">Luo raportti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="83cc1-119">Select **OK** to generate the report.</span></span>

<span data-ttu-id="83cc1-120">Seuraavassa kuvassa on esimerkki **Ylläpitopyyntöluettelo** -raportista kaikille aktiivisille yläpitopyynnöille.</span><span class="sxs-lookup"><span data-stu-id="83cc1-120">The following illustration shows an example of the **Maintenance request list** report for all active maintenance requests.</span></span>

![Ylläpitopyynnön luetteloraportti](media/10-manage-maintenance-requests.png)
