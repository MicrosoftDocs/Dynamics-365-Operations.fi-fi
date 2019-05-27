---
title: Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (10. syyskuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talent Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: 6682e4d013f006696b45e644b7b4861b34faa9bf
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517917"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a><span data-ttu-id="b9019-103">Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (10. syyskuuta 2018)</span><span class="sxs-lookup"><span data-stu-id="b9019-103">What's new or changed in Dynamics 365 for Talent Core HR (September 10, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b9019-104">**Koontiversio 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="b9019-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="b9019-105">Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talent Core HR:n uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="b9019-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Talent Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="b9019-106">Salli poissaolopyyntöjä koskeva erityinen kellonaika (puoli päivää)</span><span class="sxs-lookup"><span data-stu-id="b9019-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="b9019-107">Jos lomat ja poissaolot on määritetty siten, että poissaolo merkitään päivinä, voit nyt myös ottaa käyttöön puolen päivän määrityksen.</span><span class="sxs-lookup"><span data-stu-id="b9019-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="b9019-108">Kun käyttäjä sitten lähettää poissaolopyynnön, hän voi määrittää, pyytääkö hän poissaoloa päivän ensimmäiselle vai toiselle puoliskolle.</span><span class="sxs-lookup"><span data-stu-id="b9019-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="b9019-109">Oletusarvon mukaan tämä asetus on pois käytöstä.</span><span class="sxs-lookup"><span data-stu-id="b9019-109">By default, this option is turned off.</span></span> <span data-ttu-id="b9019-110">Jos työntekijät ovat pyytäneet poissaoloa päivän ensimmäiselle tai toiselle puoliskolle, sinun on otettava tämä asetus käyttöön henkilöstöhallinnon parametrien **Lomat ja poissaolot** -alueella.</span><span class="sxs-lookup"><span data-stu-id="b9019-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="b9019-111">Tämän toiminnon suojausoikeus on henkilöstöhallinnon parametrien ylläpitäminen.</span><span class="sxs-lookup"><span data-stu-id="b9019-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="b9019-112">Lomien ja poissaolojen syötteiden oikeellisuustarkistus</span><span class="sxs-lookup"><span data-stu-id="b9019-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="b9019-113">Loman määrityksestä riippuen työntekijät, jotka yrittävät lähettää työpäivää pidemmän poissaolopyynnön, saavat varoitusviestin.</span><span class="sxs-lookup"><span data-stu-id="b9019-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="b9019-114">Toisin sanoen heitä varoitetaan, jos he yrittävät ottaa vapaaksi enemmän kuin yhden kokonaisen päivän jonakin tiettynä päivämääränä.</span><span class="sxs-lookup"><span data-stu-id="b9019-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="b9019-115">Tämä oikeellisuustarkistus on aina käytössä.</span><span class="sxs-lookup"><span data-stu-id="b9019-115">This validation is always turned on.</span></span> <span data-ttu-id="b9019-116">Aina kun työntekijät ylittävät määritetyn päivärajan, he saavat varoituksen poissaolopyyntönsä yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="b9019-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="b9019-117">Lisäkenttiä ehdollisille selvityksille työnkuluissa</span><span class="sxs-lookup"><span data-stu-id="b9019-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="b9019-118">Core HR:n useisiin työnkulkuihin on lisätty kenttiä ehdollisille selvityksille ja paikkamerkeille.</span><span class="sxs-lookup"><span data-stu-id="b9019-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="b9019-119">Seuraavat kentät on lisätty kompensaation, irtisanomisen ja siirron työnkulkuihin:</span><span class="sxs-lookup"><span data-stu-id="b9019-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="b9019-120">Työsuhteen tyyppi</span><span class="sxs-lookup"><span data-stu-id="b9019-120">EmploymentType</span></span>
- <span data-ttu-id="b9019-121">Oikeushenkilö</span><span class="sxs-lookup"><span data-stu-id="b9019-121">LegalEntity</span></span>
- <span data-ttu-id="b9019-122">Korjattu työntekijän aloituspäivä</span><span class="sxs-lookup"><span data-stu-id="b9019-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="b9019-123">Työnantajan ilmoituksen summa</span><span class="sxs-lookup"><span data-stu-id="b9019-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="b9019-124">Työnantajan ilmoitusyksikkö</span><span class="sxs-lookup"><span data-stu-id="b9019-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="b9019-125">Siirtopäivämäärä</span><span class="sxs-lookup"><span data-stu-id="b9019-125">TransitionDate</span></span>
- <span data-ttu-id="b9019-126">Työntekijän ilmoituksen summa</span><span class="sxs-lookup"><span data-stu-id="b9019-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="b9019-127">Työntekijän aloituspäivä</span><span class="sxs-lookup"><span data-stu-id="b9019-127">WorkerStartDate</span></span>
- <span data-ttu-id="b9019-128">Työntekijän ilmoitusyksikkö</span><span class="sxs-lookup"><span data-stu-id="b9019-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="b9019-129">Koeajan lopetuspäivä</span><span class="sxs-lookup"><span data-stu-id="b9019-129">ProbationEndDate</span></span>
- <span data-ttu-id="b9019-130">Toimi</span><span class="sxs-lookup"><span data-stu-id="b9019-130">Position</span></span>
- <span data-ttu-id="b9019-131">Unioni</span><span class="sxs-lookup"><span data-stu-id="b9019-131">Union</span></span>
- <span data-ttu-id="b9019-132">Osasto</span><span class="sxs-lookup"><span data-stu-id="b9019-132">Department</span></span>
- <span data-ttu-id="b9019-133">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="b9019-133">PositionType</span></span>
- <span data-ttu-id="b9019-134">Yrityksen sijainti</span><span class="sxs-lookup"><span data-stu-id="b9019-134">CompLocation</span></span>
- <span data-ttu-id="b9019-135">Tehtävänimike</span><span class="sxs-lookup"><span data-stu-id="b9019-135">Title</span></span>
- <span data-ttu-id="b9019-136">Työ</span><span class="sxs-lookup"><span data-stu-id="b9019-136">Job</span></span>
- <span data-ttu-id="b9019-137">Työtyyppi</span><span class="sxs-lookup"><span data-stu-id="b9019-137">JobType</span></span>
- <span data-ttu-id="b9019-138">Työluokka</span><span class="sxs-lookup"><span data-stu-id="b9019-138">JobFamily</span></span>
- <span data-ttu-id="b9019-139">Työtehtävä</span><span class="sxs-lookup"><span data-stu-id="b9019-139">JobFunction</span></span>

<span data-ttu-id="b9019-140">Seuraavat kentät on lisätty toimen työnkulkuun:</span><span class="sxs-lookup"><span data-stu-id="b9019-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="b9019-141">Toimi</span><span class="sxs-lookup"><span data-stu-id="b9019-141">Position</span></span>
- <span data-ttu-id="b9019-142">Unioni</span><span class="sxs-lookup"><span data-stu-id="b9019-142">Union</span></span>
- <span data-ttu-id="b9019-143">Osasto</span><span class="sxs-lookup"><span data-stu-id="b9019-143">Department</span></span>
- <span data-ttu-id="b9019-144">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="b9019-144">PositionType</span></span>
- <span data-ttu-id="b9019-145">Yrityksen sijainti</span><span class="sxs-lookup"><span data-stu-id="b9019-145">CompLocation</span></span>
- <span data-ttu-id="b9019-146">Tehtävänimike</span><span class="sxs-lookup"><span data-stu-id="b9019-146">Title</span></span>
- <span data-ttu-id="b9019-147">Työ</span><span class="sxs-lookup"><span data-stu-id="b9019-147">Job</span></span>
- <span data-ttu-id="b9019-148">Työtyyppi</span><span class="sxs-lookup"><span data-stu-id="b9019-148">JobType</span></span>
- <span data-ttu-id="b9019-149">Työluokka</span><span class="sxs-lookup"><span data-stu-id="b9019-149">JobFamily</span></span>
- <span data-ttu-id="b9019-150">Työtehtävä</span><span class="sxs-lookup"><span data-stu-id="b9019-150">JobFunction</span></span>

<span data-ttu-id="b9019-151">Ehdollisten selvitysten ja paikkamerkkien kenttiä voivat käyttää kaikki käyttäjät, jotka voivat määrittää edellä mainittuja työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="b9019-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="b9019-152">Siirtyminen Attractiin henkilöstöhallinnosta</span><span class="sxs-lookup"><span data-stu-id="b9019-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="b9019-153">Jos Attractia ei ole määritetty henkilöstöhallinnossa, **Palkattavat ehdokkaat** -osiossa käyttäjiä kehotetaan aloittamaan Attractin käyttö sen sijaan, että näytettäisiin viesti "Emme löytäneet mitään näytettävää tähän”.</span><span class="sxs-lookup"><span data-stu-id="b9019-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="b9019-154">Muut muutokset</span><span class="sxs-lookup"><span data-stu-id="b9019-154">Other changes</span></span>

<span data-ttu-id="b9019-155">Tämä versio sisältää useita muita ohjelmavirhekorjauksia:</span><span class="sxs-lookup"><span data-stu-id="b9019-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="b9019-156">Kun palkataan alihankkija, **Kompensaatio**-välilehden ei pitäisi olla saatavilla pyyntö-/toimintosivulla.</span><span class="sxs-lookup"><span data-stu-id="b9019-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="b9019-157">Pyynnön päättymisprosessin aikana et voi jatkaa, ennen kuin kaikki vaaditut kentät sisältävät tietoja.</span><span class="sxs-lookup"><span data-stu-id="b9019-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="b9019-158">Lajittelujärjestyksen ja päivämäärän näyttöongelmat on korjattu henkilöstöhallinnon analyysissa.</span><span class="sxs-lookup"><span data-stu-id="b9019-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
