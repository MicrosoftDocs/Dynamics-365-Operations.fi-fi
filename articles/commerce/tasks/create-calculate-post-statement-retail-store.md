---
title: Laskelmien luonti, laskenta ja kirjaaminen vähittäismyymälälle
description: Tässä aiheessa kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet.
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
ms.openlocfilehash: 3b26ea5c816339eef88bfdd9ac59701dcaa31fe4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022391"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="f8ca0-103">Laskelmien luonti, laskenta ja kirjaaminen vähittäismyymälälle</span><span class="sxs-lookup"><span data-stu-id="f8ca0-103">Create, calculate, and post statements for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f8ca0-104">Tässä aiheessa kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="f8ca0-105">Samalle tehtävälle voidaan määrittää myös erätöitä.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="f8ca0-106">Erätöiden määrittämisen ja suorittamisen vaiheet löytyvät myös muista aiheista.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="f8ca0-107">Tämän menettelyn suorittaminen edellyttää myyntipisteellä tehtyjä ja Dynamics 365 Commerceiin siirrettyjä tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Commerce.</span></span> <span data-ttu-id="f8ca0-108">Tämä tallenne käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="f8ca0-109">Valitse kotisivulla **Myymälän myyntitiedot**.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-109">Select **Store financials** from the home page.</span></span>
2. <span data-ttu-id="f8ca0-110">Valitse **Uusi laskelma**.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-110">Select **New statement**.</span></span>
3. <span data-ttu-id="f8ca0-111">Valitse **Myymälän numero** -kentästä vaihtoehto avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="f8ca0-112">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-112">Select **OK**.</span></span>
5. <span data-ttu-id="f8ca0-113">**Asetus**-ryhmässä on asetuksia, jotka ohjaavat laskelmaan sisällytettävien tapahtumien valintaa sekä tapahtumien laskentariveiksi ryhmittelyä.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="f8ca0-114">Voit avata **Asetus**-ryhmän ja muuttaa asetuksia tai käyttää oletusarvoja.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="f8ca0-115">**Laskelmatapa**-kentässä määritetään, miten laskelmarivit ryhmitellään.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="f8ca0-116">Valitse henkilökunnan jäsen tai kassakone **Henkilöstö/kassakone**-kentässä, jos haluat tehdä laskelman vain tietylle henkilökunnan jäsenelle tai kassakoneelle.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="f8ca0-117">Valitse vaihtoehto **Sulkemistapa**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="f8ca0-118">Valitse toimintoruudusta **Laske laskelma**.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="f8ca0-119">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-119">Select **Yes**.</span></span>
    - <span data-ttu-id="f8ca0-120">Kun laskelma on tehty, jokaiselle käytetylle maksu- ja laskelmatavalle on luotu rivejä, jotka sisältävät kokonaissummat.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="f8ca0-121">Voit syöttää kullekin riville lasketun summan, jos summia on syötettävä tai päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="f8ca0-122">Laskettuun kenttää siirretään myyntipisteellä kassan maksuvälineittäin tehtyjen laskemistapahtumien summat.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="f8ca0-123">Valitse toimintoruudusta **Kirjaa laskelma**.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="f8ca0-124">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-124">Select **Close**.</span></span>
11. <span data-ttu-id="f8ca0-125">Sulje ruutu.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-125">Close the pane.</span></span>
12. <span data-ttu-id="f8ca0-126">Valitse kotisivulla **Myymälän myyntitiedot**.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-126">At the home page, select **Store financials**.</span></span>
13. <span data-ttu-id="f8ca0-127">Valitse **Kirjatut laskelmat** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="f8ca0-127">Select the **Posted statements** tab.</span></span>
