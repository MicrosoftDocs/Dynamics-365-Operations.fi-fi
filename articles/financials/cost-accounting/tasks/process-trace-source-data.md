--- 
title: "Lähdetietojen käsittely ja seuranta"
description: "Kaikki tiedot käsitellään töiden avulla."
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e476416420875ba0f2401cf251d34977ae84b8f5
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="4b952-103">Lähdetietojen käsittely ja seuranta</span><span class="sxs-lookup"><span data-stu-id="4b952-103">Process and trace source data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4b952-104">Kaikki tiedot käsitellään töiden avulla.</span><span class="sxs-lookup"><span data-stu-id="4b952-104">All data processing is run by jobs.</span></span> <span data-ttu-id="4b952-105">Jokaiselle työlle ja tietopalvelulle luodaan kirjauskansio asiakirjaan, jolle prosessi on suoritettu ja jonka merkinnät on käsitelty nykyisessä työssä.</span><span class="sxs-lookup"><span data-stu-id="4b952-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="4b952-106">Tämän menettelyn avulla määritetään tietolähde ja jäljitetään sitten määritetyn kustannusmerkinnän alkuperä.</span><span class="sxs-lookup"><span data-stu-id="4b952-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="4b952-107">Tämä tallenne käyttää esittelytietojen USP2-yritystä.</span><span class="sxs-lookup"><span data-stu-id="4b952-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="4b952-108">Toista ennen tämän tehtävän suorittamista seuraavat tehtäväoppaat: Kustannuslaskennan kirjanpidon luominen, Kustannusseurantayksiköiden määrittäminen ja Kustannuslaskennan kirjanpidon tietolähteen hallinta.</span><span class="sxs-lookup"><span data-stu-id="4b952-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="4b952-109">Valitse Kustannuslaskenta > Kirjanpidon asetukset > Kustannuslaskennan kirjanpidot.</span><span class="sxs-lookup"><span data-stu-id="4b952-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="4b952-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="4b952-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4b952-111">Valitse aiemmin luotu kustannuslaskennan kirjanpito.</span><span class="sxs-lookup"><span data-stu-id="4b952-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="4b952-112">Valitse Toteutuneet versiot.</span><span class="sxs-lookup"><span data-stu-id="4b952-112">Click Actual versions.</span></span>
4. <span data-ttu-id="4b952-113">Valitse toimintoruudussa Lähdetietojen käsittely.</span><span class="sxs-lookup"><span data-stu-id="4b952-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="4b952-114">Valitse Kirjanpitomerkintöjen siirron kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="4b952-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="4b952-115">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="4b952-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="4b952-116">Valitse Kirjauskansioviennit.</span><span class="sxs-lookup"><span data-stu-id="4b952-116">Click Journal entries.</span></span>
8. <span data-ttu-id="4b952-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="4b952-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="4b952-118">Valitse Kustannusmerkinnät.</span><span class="sxs-lookup"><span data-stu-id="4b952-118">Click Cost entries.</span></span>
10. <span data-ttu-id="4b952-119">Valitse Lähdemerkintä.</span><span class="sxs-lookup"><span data-stu-id="4b952-119">Click Source entry.</span></span>
11. <span data-ttu-id="4b952-120">Valitse toimintoruudussa Lähdetietojen käsittely.</span><span class="sxs-lookup"><span data-stu-id="4b952-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="4b952-121">Valitse Kirjanpito.</span><span class="sxs-lookup"><span data-stu-id="4b952-121">Click General ledger.</span></span>
13. <span data-ttu-id="4b952-122">Syötä tai valitse arvo Kirjanpidon vuosikalenterin kausi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4b952-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="4b952-123">Valitse tässä esimerkissä Tilivuosi 2017, kausi 9.</span><span class="sxs-lookup"><span data-stu-id="4b952-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="4b952-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4b952-124">Click OK.</span></span>


