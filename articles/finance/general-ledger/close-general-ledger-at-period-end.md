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
ms.reviewer: roschlom
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fe90e29e5ae71492519d9ab0d4cab2d12765cf4b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212370"
---
# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="f03aa-103">Sulje kirjanpito kauden lopussa</span><span class="sxs-lookup"><span data-stu-id="f03aa-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f03aa-104">Tässä aiheessa käsitellään tehtäviä, jotka yleensä viimeistellään, kun suoritetaan kirjanpidon kauden sulkemista.</span><span class="sxs-lookup"><span data-stu-id="f03aa-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="f03aa-105">Kirjanpidossa voit tehdä päätöstoimenpiteet jakson tai vuoden lopussa.</span><span class="sxs-lookup"><span data-stu-id="f03aa-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="f03aa-106">Lopetusprosessit valmistavat järjestelmän uudelle jaksolle.</span><span class="sxs-lookup"><span data-stu-id="f03aa-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="f03aa-107">Valmistellaksesi järjestelmän uudelle vuodelle, sinun on suoritettava "Vuoden loppu" -sulkemisprosessi.</span><span class="sxs-lookup"><span data-stu-id="f03aa-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="f03aa-108">Kussakin organisaatiossa on eri prosessit ja vaiheet, jotka se tekee kauden lopussa.</span><span class="sxs-lookup"><span data-stu-id="f03aa-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="f03aa-109">Seuraavassa on joitakin valinnaisia vaiheita kauden loppuun:</span><span class="sxs-lookup"><span data-stu-id="f03aa-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="f03aa-110">Suorita valmiiksi kaikki tehtävät kaikissa muissa moduuleissa, esimerkiksi Myyntireskontra, Ostoreskontra ja Varasto.</span><span class="sxs-lookup"><span data-stu-id="f03aa-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="f03aa-111">Varmista, että kaikki kirjauskansiot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="f03aa-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="f03aa-112">Suorita ulkomaanvaluutan uudelleenarvostus tuottaaksesi kaikki toteutumattomat voitto- tai tappiosummat.</span><span class="sxs-lookup"><span data-stu-id="f03aa-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="f03aa-113">Päätä tapahtumat jokaiselle kirjanpitotilille.</span><span class="sxs-lookup"><span data-stu-id="f03aa-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="f03aa-114">Käsittele kaikki pyydettävät kohdistukset.</span><span class="sxs-lookup"><span data-stu-id="f03aa-114">Process any required allocations.</span></span>
-   <span data-ttu-id="f03aa-115">Kirjaa manuaalisesti kauden opun muutokset.</span><span class="sxs-lookup"><span data-stu-id="f03aa-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="f03aa-116">Kirjaa tapahtumat ja tarkista **kirjanpidon kirjauskansion** raportti.</span><span class="sxs-lookup"><span data-stu-id="f03aa-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="f03aa-117">Voit suorittaa konsolidoinnin käyttämälä konsolidointiyrityksiä tai taloushallinnon raportteja.</span><span class="sxs-lookup"><span data-stu-id="f03aa-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="f03aa-118">Luo kauden lopun tilinpäätöksiä käyttämällä taloushallinnon raportointia.</span><span class="sxs-lookup"><span data-stu-id="f03aa-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="f03aa-119">Määritä kirjanpitokaudet asentoon **Pidossa** niin, ettei muita kirjauksia tule.</span><span class="sxs-lookup"><span data-stu-id="f03aa-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="f03aa-120">Voit myös rajoittaa kauden tietylle käyttäjäryhmälle, loppukauden tehtävien aikana, paremman hallinnan takia.</span><span class="sxs-lookup"><span data-stu-id="f03aa-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="f03aa-121">Se ei ole suositeltavaa määrittää jaksoja asentoon **Suljettu pysyvästi**, koska kun kausi on suljettu, sitä ei voi avata uudelleen.</span><span class="sxs-lookup"><span data-stu-id="f03aa-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="f03aa-122">Tilikauden työtilan sulkemista voidaan käyttää järjestämään ja seuraamaan erilaisia kauden lopun prosessien edellyttämiä tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="f03aa-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="f03aa-123">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="f03aa-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="f03aa-124">Tilikauden sulkemisen työtila</span><span class="sxs-lookup"><span data-stu-id="f03aa-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="f03aa-125">Tilikauden lopetus</span><span class="sxs-lookup"><span data-stu-id="f03aa-125">Year-end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="f03aa-126">Tilikauden joukkosulkeminen</span><span class="sxs-lookup"><span data-stu-id="f03aa-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]