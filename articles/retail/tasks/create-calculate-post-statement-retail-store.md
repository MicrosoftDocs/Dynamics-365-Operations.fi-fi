---
title: Luo, laske ja kirjaa laskelma vähittäismyymälälle
description: Tässä menettelyssä kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9ea30e7e008bfcce77a7ee2f4d7d01a6cf1ababc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "354388"
---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="ea9ff-103">Luo, laske ja kirjaa laskelma vähittäismyymälälle</span><span class="sxs-lookup"><span data-stu-id="ea9ff-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ea9ff-104">Tässä menettelyssä kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="ea9ff-105">Samalle tehtävälle voidaan määrittää myös erätöitä.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="ea9ff-106">Erätöiden määrittämisen ja suorittamisen vaiheet löytyvät myös muista aiheista.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="ea9ff-107">Tämän menettelyn suorittaminen edellyttää myyntipisteellä tehtyjä ja Dynamics AX:ään siirrettyjä tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="ea9ff-108">Tämä tallenne käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="ea9ff-109">Tämä ohje voi viitata Microsoft Dynamics AX:ään.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="ea9ff-110">Huomaa, että Dynamics AX:n nimi on nyt Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="ea9ff-111">Valitse Kaikki työtilat > ..</span><span class="sxs-lookup"><span data-stu-id="ea9ff-111">Go to All workspaces > ..</span></span> <span data-ttu-id="ea9ff-112">> Vähittäismyymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-112">> Retail store financials.</span></span>
2. <span data-ttu-id="ea9ff-113">Valitse Uusi laskelma.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-113">Click New statement.</span></span>
3. <span data-ttu-id="ea9ff-114">Avaa haku valitsemalla Myymälä numero -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ea9ff-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ea9ff-116">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-116">Click OK.</span></span>
    * <span data-ttu-id="ea9ff-117">Asetusryhmässä on asetuksia, jotka ohjaavat laskelmaan sisällytettävien tapahtumien valintaa sekä tapahtumien laskentariveiksi ryhmittelyä.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="ea9ff-118">Voit avata asetusryhmän ja muuttaa asetuksia tai käyttää oletusarvoja.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="ea9ff-119">Laskelmatapa-kentässä määritetään, miten laskelmarivit ryhmitellään.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="ea9ff-120">Valitse henkilökunnan jäsen tai kassakone, jos haluat tehdä laskelman vain tietylle henkilökunnan jäsenelle tai kassakoneelle.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="ea9ff-121">Valitse vaihtoehto Sulkemistapa-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="ea9ff-122">Valitse Laske laskelma.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="ea9ff-123">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-123">Click Yes.</span></span>
    * <span data-ttu-id="ea9ff-124">Kun laskelma on tehty, jokaiselle käytetylle maksu- ja laskelmatavalle on luotu rivejä, jotka sisältävät kokonaissummat.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="ea9ff-125">Voit syöttää kullekin riville lasketun summan, jos summia on syötettävä tai päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="ea9ff-126">Laskettuun kenttää siirretään myyntipisteellä kassan maksuvälineittäin tehtyjen laskemistapahtumien summat.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="ea9ff-127">Valitse Kirjaa laskelma.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-127">Click Post statement.</span></span>
10. <span data-ttu-id="ea9ff-128">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-128">Click Close.</span></span>
11. <span data-ttu-id="ea9ff-129">Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="ea9ff-130">Valitse Kirjatut laskelmat -välilehti.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-130">Click the Posted statements tab.</span></span>

