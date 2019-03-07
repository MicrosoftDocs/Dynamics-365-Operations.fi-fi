---
title: Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (31. tammikuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 1/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5c9449e2bdec8c17cc2cf659ed68ac1d713a26ad
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2019
ms.locfileid: "374731"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a><span data-ttu-id="33e5f-103">Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (31. tammikuuta 2019)</span><span class="sxs-lookup"><span data-stu-id="33e5f-103">What's new or changed in Dynamics 365 for Talent (January 31, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33e5f-104">Tässä ohjeaiheessa käsitellään Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="33e5f-104">This topic describes features that are either new or changed in Dynamics 365 for Talent</span></span>

<span data-ttu-id="33e5f-105">**Koontiversio 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="33e5f-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="33e5f-106">Core HR:n muutokset</span><span class="sxs-lookup"><span data-stu-id="33e5f-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="33e5f-107">Käytetty poissaolo lomalla olevan kortissa ei ota huomioon lomasuunnitelman päivämääriä</span><span class="sxs-lookup"><span data-stu-id="33e5f-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="33e5f-108">Niiden henkilöiden **Otettu**-kortti näyttää nyt suunnitelman määrittämänä lomavuonna käytetyt poissaolot, joiden lomasuunnitelmat eivät ole kalenterivuoden mukaisia.</span><span class="sxs-lookup"><span data-stu-id="33e5f-108">For those that have leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="33e5f-109">Jos organisaation lomavuosi on esimerkiksi 1.6.–30.5. ja työntekijä on ollut poissa kolme päivää joulukuussa, 15.1. **Otettu**-kortissa näkyy 3 päivää.</span><span class="sxs-lookup"><span data-stu-id="33e5f-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken 3 days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="33e5f-110">Jaksotussummat eivät vastaa tasopäivämääräperustetta</span><span class="sxs-lookup"><span data-stu-id="33e5f-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="33e5f-111">Lomiin ja poissaoloihin on lisätty uusia asetuksia (**Henkilöstöhallinto**-parametrit), joiden avulla asiakkaat voivat määrittää, milloin työntekijöiden työkuukausipäivämäärät ovat voimassa.</span><span class="sxs-lookup"><span data-stu-id="33e5f-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="33e5f-112">Joissakin organisaatioissa päivämäärä on kuukauden lopussa, kun taas toisessa se voi olla kuukauden alussa.</span><span class="sxs-lookup"><span data-stu-id="33e5f-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="33e5f-113">Yksi organisaatio voi esimerkiksi myöntää poissaolon 31.12., kun taas toisen tekee sen 1.1.</span><span class="sxs-lookup"><span data-stu-id="33e5f-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="33e5f-114">Tällä asetuksella voi valita, milloin myöntämisen tapahtuu.</span><span class="sxs-lookup"><span data-stu-id="33e5f-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="33e5f-115">Työntekijän työhönottotoiminnot ovat juuttuneet Työnkulku valmis -tilaan</span><span class="sxs-lookup"><span data-stu-id="33e5f-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="33e5f-116">Tehdyillä muutoksilla on korjattu ongelma, jossa pieni määrä työnkulkuja päättyi Työnkulku valmis -tilaan.</span><span class="sxs-lookup"><span data-stu-id="33e5f-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="33e5f-117">Uusien työnkulkujen pitäisi nyt siirtyä Valmis- tilaan, kun työnkulku päättyy.</span><span class="sxs-lookup"><span data-stu-id="33e5f-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="33e5f-118">Jos työnkulku on Työnkulku valmis -tilassa, se siirretään virhetilaan, jotta se voidaan tarvittaessa päivittää tai poistaa.</span><span class="sxs-lookup"><span data-stu-id="33e5f-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
