---
title: Resurssin kapasiteetin synkronointi
description: Tässä aiheessa on tietoja resurssikapasiteetin synkronoinnista kalenterien ja projektien välillä.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760532"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="ab87c-103">Resurssin kapasiteetin synkronointi</span><span class="sxs-lookup"><span data-stu-id="ab87c-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab87c-104">Resurssin synkronointiprosessi auttaa varmistamaan, että kalenterin ja peruskalenterin tiedot siirtyvät projektiresurssien ajoitukseen.</span><span class="sxs-lookup"><span data-stu-id="ab87c-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="ab87c-105">Jos kalenteria muutetaan, prosessit tekevät projektiresurssien ajoitukseen tarvittavat päivitykset.</span><span class="sxs-lookup"><span data-stu-id="ab87c-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="ab87c-106">Prosessit parantavat myös suorituskykyä, koska resurssin kalenteritiedot synkronoidaan etukäteen.</span><span class="sxs-lookup"><span data-stu-id="ab87c-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="ab87c-107">Näin päivitykset resurssien ajoitustietoihin tapahtuvat entistä nopeammin.</span><span class="sxs-lookup"><span data-stu-id="ab87c-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="ab87c-108">Prosessit kannattaa ajoittaa eräajona, ei yksitellen.</span><span class="sxs-lookup"><span data-stu-id="ab87c-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="ab87c-109">Muussa tapauksessa riskinä on, että edelliseen synkronointiin sisällytettävät päivämäärät unohtuvat.</span><span class="sxs-lookup"><span data-stu-id="ab87c-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="ab87c-110">Jos sisällytettäviä päivämääriä ei käytetä, päivämäärien synkronointiin voi jäädä aukkoja.</span><span class="sxs-lookup"><span data-stu-id="ab87c-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalenterin synkronointi](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="ab87c-112">Synkronoi resurssin kapasiteetin koonnit</span><span class="sxs-lookup"><span data-stu-id="ab87c-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="ab87c-113">Synkronointiprosessin tarkoituksena on synkronoida kaikki resurssin kalenteritiedot.</span><span class="sxs-lookup"><span data-stu-id="ab87c-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="ab87c-114">Näihin tietoihin sisältyvät peruskalenterin tiedot kaikista muutoksista, jotka tehdään projektin resurssikalenterin kapasiteettitaulukkoon.</span><span class="sxs-lookup"><span data-stu-id="ab87c-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="ab87c-115">Jos projektiin lisätään uusia resursseja, synkronoinnin avulla voidaan varmistaa, että päivitetyt kalenteritiedot ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="ab87c-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="ab87c-116">Synkronoinnin voi tehdä milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="ab87c-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="ab87c-117">Ne kannattaa tehdä eräajona.</span><span class="sxs-lookup"><span data-stu-id="ab87c-117">We recommend that you use a batch.</span></span> <span data-ttu-id="ab87c-118">Vaihtoehdot ovat käytettävissä kapasiteettivarauksia synkronoitaessa.</span><span class="sxs-lookup"><span data-stu-id="ab87c-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="ab87c-119">Valitse **Projektinhallinta ja kirjanpito** &gt; **Kausittainen** &gt; **Kapasiteetin synkronointi** &gt; **Synkronoi resurssin kapasiteetin koonnit**.</span><span class="sxs-lookup"><span data-stu-id="ab87c-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="ab87c-120">Määritä asetukset seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="ab87c-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="ab87c-121">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="ab87c-121">Option</span></span>      | <span data-ttu-id="ab87c-122">kuvaus</span><span class="sxs-lookup"><span data-stu-id="ab87c-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="ab87c-123">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="ab87c-123">Period code</span></span> | <span data-ttu-id="ab87c-124">Voit myös valita pääkirjanpidon päivämäärävälin koodin, jolla asetetaan resurssin kapasiteetin koontien synkronointiprosessin aloitus- ja lopetuspäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="ab87c-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="ab87c-125">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab87c-125">Start date</span></span>  | <span data-ttu-id="ab87c-126">Anna resurssin kapasiteetin koontien synkronointiprosessin aloituspäivä.</span><span class="sxs-lookup"><span data-stu-id="ab87c-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="ab87c-127">Päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab87c-127">End date</span></span>    | <span data-ttu-id="ab87c-128">Anna resurssin kapasiteetin koontien synkronointiprosessin päättymispäivä.</span><span class="sxs-lookup"><span data-stu-id="ab87c-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="ab87c-129">[![Synkronointiprosessi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="ab87c-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
