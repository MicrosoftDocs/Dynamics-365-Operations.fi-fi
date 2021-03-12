---
title: Prosessivalmistuksen vianmääritys
description: Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita prosessivalmistuksen käytössä voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d999c91aa1cc14f29ebfa6be8e456e45ef0d3fa4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966177"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="2a7dc-103">Prosessivalmistuksen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="2a7dc-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="2a7dc-104">Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita prosessivalmistuksen käytössä voi esiintyä.</span><span class="sxs-lookup"><span data-stu-id="2a7dc-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="2a7dc-105">Kun työkorttilaitetta käytetään raportoimaan osittainen määrä tuotantotilauksen viimeisessä työssä, kaikki kyseisen tilauksen aiemmat työt, joiden tilana on keskeneräinen, päättyvät automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="2a7dc-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="2a7dc-106">Tämä on suunniteltu ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="2a7dc-106">This behavior is by design.</span></span> <span data-ttu-id="2a7dc-107">**Ilmoita valmiiksi** -välilehden **Tuotantotilauksen oletusarvot** -sivulla on **Tee reitityksen loppumerkintä** -niminen vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="2a7dc-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="2a7dc-108">Jos tämän aiheen asetuksena on *Kyllä*, reittikortin kirjauskansio kirjataan kun työntekijä käyttää työkorttilaitetta ja työkorttipäätettä viimeisimmän toiminnon ilmoittamiseen.</span><span class="sxs-lookup"><span data-stu-id="2a7dc-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="2a7dc-109">Tämä kirjauskansio kirjaa kaikki toiminnot valmiiksi ja lopettaa kaikki tuotantotyöt.</span><span class="sxs-lookup"><span data-stu-id="2a7dc-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="2a7dc-110">Kun **Tee reitityksen loppumerkintä** -asetuksena on *Kyllä*, järjestelmä ei ota huomioon työn tilaa, jonka työntekijä valitsi, kun tämä ilmoitti viimeisimmän toiminnon.</span><span class="sxs-lookup"><span data-stu-id="2a7dc-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="2a7dc-111">Järjestelmä ei myöskään ota huomioon, ilmoittaako työntekijä täyden vai osittaisen määrän.</span><span class="sxs-lookup"><span data-stu-id="2a7dc-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="2a7dc-112">Kun varaston sulkemista yritetään, seurauksena on seuraava varoitussanoma: Jälkikustannuslaskentaa ei suoriteta päivämäärällä %1, jolla kohdistuskauden loppu on rekisteröity.</span><span class="sxs-lookup"><span data-stu-id="2a7dc-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="2a7dc-113">Jos versiota 10.0.13 edeltävissä versioissa ei käytetä lean-tuotannon kustannuslaskentaan, seuraava virheellinen varoitussanoma annetaan varastoa suljettaessa:</span><span class="sxs-lookup"><span data-stu-id="2a7dc-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="2a7dc-114">Olet sulkemassa varaston päivämäärällä %1.</span><span class="sxs-lookup"><span data-stu-id="2a7dc-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="2a7dc-115">Jälkikustannuslaskentaa ei suoriteta päivämäärällä %1, jolla kohdistuskauden loppu on rekisteröity.</span><span class="sxs-lookup"><span data-stu-id="2a7dc-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="2a7dc-116">Muista suorittaa jälkikustannuslaskentaa päivämäärällä %1, jolla kohdistuskausi päättyy.</span><span class="sxs-lookup"><span data-stu-id="2a7dc-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="2a7dc-117">Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes tämä on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="2a7dc-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="2a7dc-118">Tämä ongelma on korjattu versiosta 10.0.13 alkaen.</span><span class="sxs-lookup"><span data-stu-id="2a7dc-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="2a7dc-119">Lisätietoja on artikkelissa [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span><span class="sxs-lookup"><span data-stu-id="2a7dc-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>
