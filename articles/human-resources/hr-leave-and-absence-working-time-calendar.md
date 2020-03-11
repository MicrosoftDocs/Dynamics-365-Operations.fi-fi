---
title: Työaikakalenterin luominen
description: Määritä työaikakalenteri, vapaapäivät ja muut kuin työajat Dynamics 365 Human Resources -järjestelmässä.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 641f66c75875cfba51af3753223a070d7cb7dc50
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008921"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="63e04-103">Työaikakalenterin luominen</span><span class="sxs-lookup"><span data-stu-id="63e04-103">Create a working time calendar</span></span>

<span data-ttu-id="63e04-104">Dynamics 365 Human Resourcesin työaikakalenterissa näkyvät työntekijöiden työpäivät ja -tunnit organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="63e04-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="63e04-105">Kun työntekijä lähettää lomapyynnön, hänen ei tarvitse huolehtia juhlapäivistä ja sulkemisista.</span><span class="sxs-lookup"><span data-stu-id="63e04-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="63e04-106">Jos haluat tehostaa lomapyyntöjä, määritä nämä nimikkeet organisaatiollesi:</span><span class="sxs-lookup"><span data-stu-id="63e04-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="63e04-107">Työaikakalenteri</span><span class="sxs-lookup"><span data-stu-id="63e04-107">Working time calendar</span></span>
- <span data-ttu-id="63e04-108">Lomat ja sulkemiset</span><span class="sxs-lookup"><span data-stu-id="63e04-108">Holidays and closures</span></span>
- <span data-ttu-id="63e04-109">Muu kuin työaika</span><span class="sxs-lookup"><span data-stu-id="63e04-109">Non-work time</span></span>

<span data-ttu-id="63e04-110">Voit lisätä kaksi viimeistä nimikettä työaikakalenteria määrittäessäsi.</span><span class="sxs-lookup"><span data-stu-id="63e04-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="63e04-111">Voit myös määrittää tai päivittää ne erikseen.</span><span class="sxs-lookup"><span data-stu-id="63e04-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="63e04-112">Määritä työaikakalenteri</span><span class="sxs-lookup"><span data-stu-id="63e04-112">Set up a working time calendar</span></span>

<span data-ttu-id="63e04-113">Määritä vähintään yksi työaikakalenteri, joka näyttää päivät ja työtunnit.</span><span class="sxs-lookup"><span data-stu-id="63e04-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="63e04-114">Jos sinulla on sijainteja useissa maissa ja tietyillä alueilla, haluat ehkä määrittää kullekin alueelle työaikakalenterin.</span><span class="sxs-lookup"><span data-stu-id="63e04-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="63e04-115">Valitse **Organisaation hallinto** -sivulta **Kalenterit**.</span><span class="sxs-lookup"><span data-stu-id="63e04-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="63e04-116">Valitse **Uusi** ja kirjoita kalenterisi nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="63e04-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="63e04-117">Valitse **Luonnin asetukset**-kohdasta organisaation työpäivät ja määritä työajat.</span><span class="sxs-lookup"><span data-stu-id="63e04-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="63e04-118">Jos haluat lisätä loman tai sulkemisen, valitse **Lomien ja sulkemisten** vieressä oleva **Lisää**-painike.</span><span class="sxs-lookup"><span data-stu-id="63e04-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="63e04-119">Jos haluat lisätä muun kuin työajan, kuten lounaan tai tauon, valitse **Lisää** **Muu kuin työaika** -kohdassa ja kirjoita nimi ja aikaväli.</span><span class="sxs-lookup"><span data-stu-id="63e04-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="63e04-120">Valitse **Päivät**-kohdassa **Luo** päivien luomiseksi kalenteriin.</span><span class="sxs-lookup"><span data-stu-id="63e04-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="63e04-121">Kirjoita kalenterin päivämääräväli ja valitse **Luo päiviä**.</span><span class="sxs-lookup"><span data-stu-id="63e04-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="63e04-122">Jos haluat lisätä työaikatauluja, valitse **Työaikataulu**-kohdasta **Lisää** ja kirjoita sitten kunkin työaikataulun ajat.</span><span class="sxs-lookup"><span data-stu-id="63e04-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="63e04-123">Määritä lomat ja sulkemiset</span><span class="sxs-lookup"><span data-stu-id="63e04-123">Configure holidays and closures</span></span>

<span data-ttu-id="63e04-124">Voit lisätä tai muuttaa lomia ja sulkemisia erillään työaikakalenterista.</span><span class="sxs-lookup"><span data-stu-id="63e04-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="63e04-125">Valitse **Organisaation hallinto** -sivulta **Lomat ja sulkemiset**.</span><span class="sxs-lookup"><span data-stu-id="63e04-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="63e04-126">Valitse **Uusi** ja kirjoita loman tai sulkemisen nimi ja päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="63e04-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="63e04-127">Määritä muu kuin työaika</span><span class="sxs-lookup"><span data-stu-id="63e04-127">Configure non-work time</span></span>

<span data-ttu-id="63e04-128">Voit lisätä tai muuttaa muita kuin työaikoja erillään työaikakalenterista.</span><span class="sxs-lookup"><span data-stu-id="63e04-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="63e04-129">Valitse **Organisaation hallinto** -sivulta **Muu kuin työaika**.</span><span class="sxs-lookup"><span data-stu-id="63e04-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="63e04-130">Valitse **Uusi** ja kirjoita vapaa-ajan nimi ja aika-alue.</span><span class="sxs-lookup"><span data-stu-id="63e04-130">Select **New** and enter a name and time range for the non-work time.</span></span>

## <a name="leave-and-absence-preview-feature"></a><span data-ttu-id="63e04-131">Lomien ja poissaolojen esikatseluominaisuus</span><span class="sxs-lookup"><span data-stu-id="63e04-131">Leave and absence preview feature</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

<span data-ttu-id="63e04-132">Jos olet ottanut loma- ja poissaolopäivän korjausten esikatselutoiminnon käyttöön, henkilöstöhallinto käyttää loma- ja sulkemispäiviä määrittääkseen päivien määrän, jota mukautetaan kalenteriin ilmoitettujen työntekijöiden osalta.</span><span class="sxs-lookup"><span data-stu-id="63e04-132">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="63e04-133">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="63e04-133">See also</span></span>

- [<span data-ttu-id="63e04-134">Lomien ja poissaolojen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="63e04-134">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="63e04-135">Määritä loman ja poissaolon tyypit</span><span class="sxs-lookup"><span data-stu-id="63e04-135">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)