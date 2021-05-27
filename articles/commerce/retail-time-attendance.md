---
title: Ajan ja läsnäolon hallinta Retailissa
description: Tässä aiheessa on kuvaus Dynamics 365 Commercen ajan ja työajan hallinnassa tuettavista skenaarioista.
author: aamirallaqaband
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7ac7eec69bda7ad2fa41a7311a71a969eddeafb6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021485"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="e374e-103">Ajan ja läsnäolon hallinta Retailissa</span><span class="sxs-lookup"><span data-stu-id="e374e-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e374e-104">Tässä aiheessa on kuvaus Dynamics 365 Commercen ajan ja työajan hallinnassa tuettavista skenaarioista.</span><span class="sxs-lookup"><span data-stu-id="e374e-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Commerce.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="e374e-105">Työntekijän asetusten ja ajoituksen hallinta</span><span class="sxs-lookup"><span data-stu-id="e374e-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="e374e-106"> - alkukokoonpano</span><span class="sxs-lookup"><span data-stu-id="e374e-106">Initial configuration</span></span>

- <span data-ttu-id="e374e-107">Suorita ohjattu konfigurointitoiminto.</span><span class="sxs-lookup"><span data-stu-id="e374e-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="e374e-108">Rekisteröi työntekijät aikakirjausten työntekijöiksi.</span><span class="sxs-lookup"><span data-stu-id="e374e-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="e374e-109">Suunnittele työntekijöiden aikatauluja</span><span class="sxs-lookup"><span data-stu-id="e374e-109">Plan worker schedules</span></span>

- <span data-ttu-id="e374e-110">Liitä profiileita työn suunnittelutoiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="e374e-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="e374e-111">Lisätietoja on kohdassa [Profiilien käyttäminen työn suunnittelun avulla](/dynamicsax-2012/appuser-itpro/apply-profiles-using-work-planner).</span><span class="sxs-lookup"><span data-stu-id="e374e-111">For more information, see [Apply profiles using work planner](/dynamicsax-2012/appuser-itpro/apply-profiles-using-work-planner).</span></span>

<span data-ttu-id="e374e-112">Lisätietoja määritysvaiheista on kohdassa [Työajan seurannan määrittäminen](/dynamicsax-2012/appuser-itpro/setting-up-time-and-attendance).</span><span class="sxs-lookup"><span data-stu-id="e374e-112">For information about the configuration steps, see [Setting up time and attendance](/dynamicsax-2012/appuser-itpro/setting-up-time-and-attendance).</span></span>

### <a name="commerce-specific-configuration"></a><span data-ttu-id="e374e-113">Commerce-kohtainen konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="e374e-113">Commerce-specific configuration</span></span>

- <span data-ttu-id="e374e-114">Ota toimintoprofiili käyttöön aikamerkinnöissä työntekijöille, joille haluat ottaa käyttöön aikakirjaukset.</span><span class="sxs-lookup"><span data-stu-id="e374e-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="e374e-115">Valitse **Myyntipisteen toimintoprofiilit** &gt; **Toiminnot** &gt; **Myyntipisteen aikakirjaukset** &gt; **Ota käyttöön aikakirjaukset**.</span><span class="sxs-lookup"><span data-stu-id="e374e-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="e374e-116">Määritä myyntipisteen käyttöoikeudet ottaaksesi käyttöön aikamerkintöjen tarkasteluluvat.</span><span class="sxs-lookup"><span data-stu-id="e374e-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="e374e-117">Tämä lupa antaa käyttäjälle oikeuden tarkastella muiden saman myymälän työntekijöiden aikakirjauksia, ja lisäksi osoitekirjan kautta muiden myymälöiden, joihin käyttäjä on liitetty.</span><span class="sxs-lookup"><span data-stu-id="e374e-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="e374e-118">Haluat ehkä myöntää tämän oikeuden päällikköroolille mutta ei kassanhoitajan roolille.</span><span class="sxs-lookup"><span data-stu-id="e374e-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="e374e-119">Valitse **Myyntipisteen käyttöoikeusryhmät** &gt; **Näytä aikamerkinnät**.</span><span class="sxs-lookup"><span data-stu-id="e374e-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="e374e-120">Rekisteröi aika</span><span class="sxs-lookup"><span data-stu-id="e374e-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="e374e-121">Kassanhoitajien ja muiden kuin kassanhoitajien kirjaukset</span><span class="sxs-lookup"><span data-stu-id="e374e-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="e374e-122">Myyntipisteellä:</span><span class="sxs-lookup"><span data-stu-id="e374e-122">On POS:</span></span>

    - <span data-ttu-id="e374e-123">Saapumistoiminnot:</span><span class="sxs-lookup"><span data-stu-id="e374e-123">Clock-in operations:</span></span>

        - <span data-ttu-id="e374e-124">Kirjaudu sisään muulla kuin kassatoiminnolla tai Uusi vuoro -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="e374e-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="e374e-125">Valitse aikamerkintätoiminto.</span><span class="sxs-lookup"><span data-stu-id="e374e-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="e374e-126">Valitse haluttu toiminto:</span><span class="sxs-lookup"><span data-stu-id="e374e-126">Select a desired operation:</span></span>

            - <span data-ttu-id="e374e-127">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="e374e-127">Clock-in</span></span>
            - <span data-ttu-id="e374e-128">Työtauko</span><span class="sxs-lookup"><span data-stu-id="e374e-128">Break for Work</span></span>
            - <span data-ttu-id="e374e-129">Lounastauko</span><span class="sxs-lookup"><span data-stu-id="e374e-129">Break for Lunch</span></span>
            - <span data-ttu-id="e374e-130">Poistuminen</span><span class="sxs-lookup"><span data-stu-id="e374e-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="e374e-131">Nykyinen tila:</span><span class="sxs-lookup"><span data-stu-id="e374e-131">Current state</span></span></th>
        <th><span data-ttu-id="e374e-132">Käytettävissä olevat toiminnot</span><span class="sxs-lookup"><span data-stu-id="e374e-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="e374e-133">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="e374e-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="e374e-134">Työtauko</span><span class="sxs-lookup"><span data-stu-id="e374e-134">Break for Work</span></span></li>
        <li><span data-ttu-id="e374e-135">Lounastauko</span><span class="sxs-lookup"><span data-stu-id="e374e-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="e374e-136">Poistuminen</span><span class="sxs-lookup"><span data-stu-id="e374e-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="e374e-137">Työtauko</span><span class="sxs-lookup"><span data-stu-id="e374e-137">Break for Work</span></span></td>
        <td><span data-ttu-id="e374e-138">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="e374e-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="e374e-139">Lounastauko</span><span class="sxs-lookup"><span data-stu-id="e374e-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="e374e-140">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="e374e-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="e374e-141">Poistuminen</span><span class="sxs-lookup"><span data-stu-id="e374e-141">Clock-out</span></span></td>
        <td><span data-ttu-id="e374e-142">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="e374e-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="e374e-143">[![Aikatilat](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="e374e-143">[![Time Clock States](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="e374e-144">Tarkastele vahvistussanomaa ja vahvista, että nykyinen merkinnän aika on oikea.</span><span class="sxs-lookup"><span data-stu-id="e374e-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="e374e-145">Lokikirja:</span><span class="sxs-lookup"><span data-stu-id="e374e-145">Logbook:</span></span>

    - <span data-ttu-id="e374e-146">Valitse **Lokikirja** tarkastellaksesi aikamerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="e374e-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="e374e-147">Käytä ajan suodattimia eri aikaikkunoiden valitsemiseen.</span><span class="sxs-lookup"><span data-stu-id="e374e-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="e374e-148">Jos työskentelet useissa myymäläsijainneissa, näet aikakirjauksesi kaikista myymälöistä, joihin sinulle on kirjattu aikaa.</span><span class="sxs-lookup"><span data-stu-id="e374e-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="e374e-149">Voit käyttää myymäläsuodatinta tarkastellaksesi valitun myymälän aikakirjauksia.</span><span class="sxs-lookup"><span data-stu-id="e374e-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="e374e-150">Eri aikavyöhykkeet:</span><span class="sxs-lookup"><span data-stu-id="e374e-150">Different time zones:</span></span>

    - <span data-ttu-id="e374e-151">Jos tarkastelet aikoja eri sijainnista (kassan lokikirjaa varten tai käyttämällä **Näytä aikamerkinnät** -toimintoa päällikköskenaariossa), ja kyseinen sijainti on eri aikavyöhykkeellä, näkemäsi aikamerkinnät muunnetaan paikalliseen aikavyöhykkeeseesi.</span><span class="sxs-lookup"><span data-stu-id="e374e-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="e374e-152">Ajatellaan, että olet kahden myymälän päällikkö, joista toinen sijaitsee Arizonassa ja toinen Nevadassa.</span><span class="sxs-lookup"><span data-stu-id="e374e-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="e374e-153">Kassa kirjaa saapumisen klo 9:00</span><span class="sxs-lookup"><span data-stu-id="e374e-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="e374e-154">Arizonassa.</span><span class="sxs-lookup"><span data-stu-id="e374e-154">in Arizona.</span></span> <span data-ttu-id="e374e-155">Tuolla hetkellä kello on Nevadassa 8.00.</span><span class="sxs-lookup"><span data-stu-id="e374e-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="e374e-156">Näin ollen, jos olet Nevadan liikkeessä ja katsot aikakirjaustietueita, kirjaus on merkitty klo 8.00:ksi.</span><span class="sxs-lookup"><span data-stu-id="e374e-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="e374e-157">Työntekijän aikarekisteröintien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="e374e-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="e374e-158">Näytä työntekijän aikakirjaukset ja suodata myymälän tai tapahtumatyypin perusteella.</span><span class="sxs-lookup"><span data-stu-id="e374e-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="e374e-159">Myyntipisteellä:</span><span class="sxs-lookup"><span data-stu-id="e374e-159">On POS:</span></span>

- <span data-ttu-id="e374e-160">Valitse **Näytä aikamerkinnät**.</span><span class="sxs-lookup"><span data-stu-id="e374e-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="e374e-161">Näet kaikkien niiden työntekijöiden aikakirjaustapahtumat, jotka on määritetty samoihin myymälöihin kuin sinä.</span><span class="sxs-lookup"><span data-stu-id="e374e-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="e374e-162">Voit käyttää tehtävätyyppiä ja myymälän suodattimia suodattamaan aikamerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="e374e-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="e374e-163">Aikarekisteröintien käsitteleminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="e374e-163">Process and manage time registrations</span></span>

<span data-ttu-id="e374e-164">Commerce-käyttäjä noudattaa työnkulkua aikakirjausten laskemiseen, hyväksymiseen ja palkanlaskentaan siirtämiseen.</span><span class="sxs-lookup"><span data-stu-id="e374e-164">A Commerce user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="e374e-165">Tärkeimmät työvaiheet</span><span class="sxs-lookup"><span data-stu-id="e374e-165">Primary operations</span></span>

- <span data-ttu-id="e374e-166">Laske</span><span class="sxs-lookup"><span data-stu-id="e374e-166">Calculate</span></span>
- <span data-ttu-id="e374e-167">Hyväksy</span><span class="sxs-lookup"><span data-stu-id="e374e-167">Approve</span></span>
- <span data-ttu-id="e374e-168">Lähetä palkanlaskentaan</span><span class="sxs-lookup"><span data-stu-id="e374e-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="e374e-169">Muut yleiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="e374e-169">Other common operations</span></span>

- <span data-ttu-id="e374e-170">Joukkopoistuminen</span><span class="sxs-lookup"><span data-stu-id="e374e-170">Bulk Clock-out</span></span>
- <span data-ttu-id="e374e-171">Poissaolon kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="e374e-171">Register Absence</span></span>

<span data-ttu-id="e374e-172">Lisätietoja työajan seurannan rekisteröintien käsittelystä on kohdassa [Työajan seurannan rekisteröintien käsittely](/dynamicsax-2012/appuser-itpro/process-time-and-attendance-registrations).</span><span class="sxs-lookup"><span data-stu-id="e374e-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](/dynamicsax-2012/appuser-itpro/process-time-and-attendance-registrations).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]