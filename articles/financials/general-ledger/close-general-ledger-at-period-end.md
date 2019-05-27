---
title: Sulje kirjanpito kauden lopussa
description: Tässä aiheessa käsitellään tehtäviä, jotka yleensä viimeistellään, kun suoritetaan kirjanpidon kauden sulkemista.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 23d4b9b070a48e1964ecd6896afe071b564d1194
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567257"
---
# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="2619c-103">Sulje kirjanpito kauden lopussa</span><span class="sxs-lookup"><span data-stu-id="2619c-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2619c-104">Tässä aiheessa käsitellään tehtäviä, jotka yleensä viimeistellään, kun suoritetaan kirjanpidon kauden sulkemista.</span><span class="sxs-lookup"><span data-stu-id="2619c-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="2619c-105">Kirjanpidossa voit tehdä päätöstoimenpiteet jakson tai vuoden lopussa.</span><span class="sxs-lookup"><span data-stu-id="2619c-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="2619c-106">Lopetusprosessit valmistavat järjestelmän uudelle jaksolle.</span><span class="sxs-lookup"><span data-stu-id="2619c-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="2619c-107">Valmistellaksesi järjestelmän uudelle vuodelle, sinun on suoritettava "Vuoden loppu" -sulkemisprosessi.</span><span class="sxs-lookup"><span data-stu-id="2619c-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="2619c-108">Kussakin organisaatiossa on eri prosessit ja vaiheet, jotka se tekee kauden lopussa.</span><span class="sxs-lookup"><span data-stu-id="2619c-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="2619c-109">Seuraavassa on joitakin valinnaisia vaiheita kauden loppuun:</span><span class="sxs-lookup"><span data-stu-id="2619c-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="2619c-110">Suorita valmiiksi kaikki tehtävät kaikissa muissa moduuleissa, esimerkiksi Myyntireskontra, Ostoreskontra ja Varasto.</span><span class="sxs-lookup"><span data-stu-id="2619c-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="2619c-111">Varmista, että kaikki kirjauskansiot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="2619c-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="2619c-112">Suorita ulkomaanvaluutan uudelleenarvostus tuottaaksesi kaikki toteutumattomat voitto- tai tappiosummat.</span><span class="sxs-lookup"><span data-stu-id="2619c-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="2619c-113">Päätä tapahtumat jokaiselle kirjanpitotilille.</span><span class="sxs-lookup"><span data-stu-id="2619c-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="2619c-114">Käsittele kaikki pyydettävät kohdistukset.</span><span class="sxs-lookup"><span data-stu-id="2619c-114">Process any required allocations.</span></span>
-   <span data-ttu-id="2619c-115">Kirjaa manuaalisesti kauden opun muutokset.</span><span class="sxs-lookup"><span data-stu-id="2619c-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="2619c-116">Kirjaa tapahtumat ja tarkista **kirjanpidon kirjauskansion** raportti.</span><span class="sxs-lookup"><span data-stu-id="2619c-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="2619c-117">Voit suorittaa konsolidoinnin käyttämälä konsolidointiyrityksiä tai taloushallinnon raportteja.</span><span class="sxs-lookup"><span data-stu-id="2619c-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="2619c-118">Luo kauden lopun tilinpäätöksiä käyttämällä taloushallinnon raportointia.</span><span class="sxs-lookup"><span data-stu-id="2619c-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="2619c-119">Määritä kirjanpitokaudet asentoon **Pidossa** niin, ettei muita kirjauksia tule.</span><span class="sxs-lookup"><span data-stu-id="2619c-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="2619c-120">Voit myös rajoittaa kauden tietylle käyttäjäryhmälle, loppukauden tehtävien aikana, paremman hallinnan takia.</span><span class="sxs-lookup"><span data-stu-id="2619c-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="2619c-121">Se ei ole suositeltavaa määrittää jaksoja asentoon **Suljettu pysyvästi**, koska kun kausi on suljettu, sitä ei voi avata uudelleen.</span><span class="sxs-lookup"><span data-stu-id="2619c-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="2619c-122">Tilikauden työtilan sulkemista voidaan käyttää järjestämään ja seuraamaan erilaisia kauden lopun prosessien edellyttämiä tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="2619c-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="2619c-123">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="2619c-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="2619c-124">Tilikauden sulkemisen työtila</span><span class="sxs-lookup"><span data-stu-id="2619c-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="2619c-125">Tilikauden lopetus</span><span class="sxs-lookup"><span data-stu-id="2619c-125">Year end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="2619c-126">Tilikauden joukkosulkeminen</span><span class="sxs-lookup"><span data-stu-id="2619c-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)




