---
title: Ajan ja läsnäolon hallinta Retailissa
description: Tässä aiheessa on kuvaus Dynamics 365 Commercein ajan ja työajan hallinnassa tuettavista skenaarioista.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: e28df09ecb592ae7df360d1b2d0bf06339c1410d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989374"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="71071-103">Ajan ja läsnäolon hallinta Retailissa</span><span class="sxs-lookup"><span data-stu-id="71071-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="71071-104">Tässä aiheessa on kuvaus Dynamics 365 Commercein ajan ja työajan hallinnassa tuettavista skenaarioista.</span><span class="sxs-lookup"><span data-stu-id="71071-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Commerce.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="71071-105">Työntekijän asetusten ja ajoituksen hallinta</span><span class="sxs-lookup"><span data-stu-id="71071-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="71071-106"> - alkukokoonpano</span><span class="sxs-lookup"><span data-stu-id="71071-106">Initial configuration</span></span>

- <span data-ttu-id="71071-107">Suorita ohjattu konfigurointitoiminto.</span><span class="sxs-lookup"><span data-stu-id="71071-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="71071-108">Rekisteröi työntekijät aikakirjausten työntekijöiksi.</span><span class="sxs-lookup"><span data-stu-id="71071-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="71071-109">Suunnittele työntekijöiden aikatauluja</span><span class="sxs-lookup"><span data-stu-id="71071-109">Plan worker schedules</span></span>

- <span data-ttu-id="71071-110">Liitä profiileita työn suunnittelutoiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="71071-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="71071-111">Lisätietoja on kohdassa [Profiilien käyttäminen työn suunnittelun avulla](https://technet.microsoft.com/library/aa551234.aspx).</span><span class="sxs-lookup"><span data-stu-id="71071-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="71071-112">Lisätietoja määritysvaiheista on kohdassa [Työajan seurannan määrittäminen](https://technet.microsoft.com/library/aa496971.aspx).</span><span class="sxs-lookup"><span data-stu-id="71071-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="commerce-specific-configuration"></a><span data-ttu-id="71071-113">Commerce-kohtainen konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="71071-113">Commerce-specific configuration</span></span>

- <span data-ttu-id="71071-114">Ota toimintoprofiili käyttöön aikamerkinnöissä työntekijöille, joille haluat ottaa käyttöön aikakirjaukset.</span><span class="sxs-lookup"><span data-stu-id="71071-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="71071-115">Valitse **Myyntipisteen toimintoprofiilit** &gt; **Toiminnot** &gt; **Myyntipisteen aikakirjaukset** &gt; **Ota käyttöön aikakirjaukset**.</span><span class="sxs-lookup"><span data-stu-id="71071-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="71071-116">Määritä myyntipisteen käyttöoikeudet ottaaksesi käyttöön aikamerkintöjen tarkasteluluvat.</span><span class="sxs-lookup"><span data-stu-id="71071-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="71071-117">Tämä lupa antaa käyttäjälle oikeuden tarkastella muiden saman myymälän työntekijöiden aikakirjauksia, ja lisäksi osoitekirjan kautta muiden myymälöiden, joihin käyttäjä on liitetty.</span><span class="sxs-lookup"><span data-stu-id="71071-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="71071-118">Haluat ehkä myöntää tämän oikeuden päällikköroolille mutta ei kassanhoitajan roolille.</span><span class="sxs-lookup"><span data-stu-id="71071-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="71071-119">Valitse **Myyntipisteen käyttöoikeusryhmät** &gt; **Näytä aikamerkinnät**.</span><span class="sxs-lookup"><span data-stu-id="71071-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="71071-120">Rekisteröi aika</span><span class="sxs-lookup"><span data-stu-id="71071-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="71071-121">Kassanhoitajien ja muiden kuin kassanhoitajien kirjaukset</span><span class="sxs-lookup"><span data-stu-id="71071-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="71071-122">Myyntipisteellä:</span><span class="sxs-lookup"><span data-stu-id="71071-122">On POS:</span></span>

    - <span data-ttu-id="71071-123">Saapumistoiminnot:</span><span class="sxs-lookup"><span data-stu-id="71071-123">Clock-in operations:</span></span>

        - <span data-ttu-id="71071-124">Kirjaudu sisään muulla kuin kassatoiminnolla tai Uusi vuoro -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="71071-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="71071-125">Valitse aikamerkintätoiminto.</span><span class="sxs-lookup"><span data-stu-id="71071-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="71071-126">Valitse haluttu toiminto:</span><span class="sxs-lookup"><span data-stu-id="71071-126">Select a desired operation:</span></span>

            - <span data-ttu-id="71071-127">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="71071-127">Clock-in</span></span>
            - <span data-ttu-id="71071-128">Työtauko</span><span class="sxs-lookup"><span data-stu-id="71071-128">Break for Work</span></span>
            - <span data-ttu-id="71071-129">Lounastauko</span><span class="sxs-lookup"><span data-stu-id="71071-129">Break for Lunch</span></span>
            - <span data-ttu-id="71071-130">Poistuminen</span><span class="sxs-lookup"><span data-stu-id="71071-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="71071-131">Nykyinen tila:</span><span class="sxs-lookup"><span data-stu-id="71071-131">Current state</span></span></th>
        <th><span data-ttu-id="71071-132">Käytettävissä olevat toiminnot</span><span class="sxs-lookup"><span data-stu-id="71071-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="71071-133">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="71071-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="71071-134">Työtauko</span><span class="sxs-lookup"><span data-stu-id="71071-134">Break for Work</span></span></li>
        <li><span data-ttu-id="71071-135">Lounastauko</span><span class="sxs-lookup"><span data-stu-id="71071-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="71071-136">Poistuminen</span><span class="sxs-lookup"><span data-stu-id="71071-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="71071-137">Työtauko</span><span class="sxs-lookup"><span data-stu-id="71071-137">Break for Work</span></span></td>
        <td><span data-ttu-id="71071-138">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="71071-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="71071-139">Lounastauko</span><span class="sxs-lookup"><span data-stu-id="71071-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="71071-140">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="71071-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="71071-141">Poistuminen</span><span class="sxs-lookup"><span data-stu-id="71071-141">Clock-out</span></span></td>
        <td><span data-ttu-id="71071-142">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="71071-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="71071-143">[![Aikatilat](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="71071-143">[![Time Clock States](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="71071-144">Tarkastele vahvistussanomaa ja vahvista, että nykyinen merkinnän aika on oikea.</span><span class="sxs-lookup"><span data-stu-id="71071-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="71071-145">Lokikirja:</span><span class="sxs-lookup"><span data-stu-id="71071-145">Logbook:</span></span>

    - <span data-ttu-id="71071-146">Valitse **Lokikirja** tarkastellaksesi aikamerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="71071-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="71071-147">Käytä ajan suodattimia eri aikaikkunoiden valitsemiseen.</span><span class="sxs-lookup"><span data-stu-id="71071-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="71071-148">Jos työskentelet useissa myymäläsijainneissa, näet aikakirjauksesi kaikista myymälöistä, joihin sinulle on kirjattu aikaa.</span><span class="sxs-lookup"><span data-stu-id="71071-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="71071-149">Voit käyttää myymäläsuodatinta tarkastellaksesi valitun myymälän aikakirjauksia.</span><span class="sxs-lookup"><span data-stu-id="71071-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="71071-150">Eri aikavyöhykkeet:</span><span class="sxs-lookup"><span data-stu-id="71071-150">Different time zones:</span></span>

    - <span data-ttu-id="71071-151">Jos tarkastelet aikoja eri sijainnista (kassan lokikirjaa varten tai käyttämällä **Näytä aikamerkinnät** -toimintoa päällikköskenaariossa), ja kyseinen sijainti on eri aikavyöhykkeellä, näkemäsi aikamerkinnät muunnetaan paikalliseen aikavyöhykkeeseesi.</span><span class="sxs-lookup"><span data-stu-id="71071-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="71071-152">Ajatellaan, että olet kahden myymälän päällikkö, joista toinen sijaitsee Arizonassa ja toinen Nevadassa.</span><span class="sxs-lookup"><span data-stu-id="71071-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="71071-153">Kassa kirjaa saapumisen klo 9:00</span><span class="sxs-lookup"><span data-stu-id="71071-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="71071-154">Arizonassa.</span><span class="sxs-lookup"><span data-stu-id="71071-154">in Arizona.</span></span> <span data-ttu-id="71071-155">Tuolla hetkellä kello on Nevadassa 8.00.</span><span class="sxs-lookup"><span data-stu-id="71071-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="71071-156">Näin ollen, jos olet Nevadan liikkeessä ja katsot aikakirjaustietueita, kirjaus on merkitty klo 8.00:ksi.</span><span class="sxs-lookup"><span data-stu-id="71071-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="71071-157">Työntekijän aikarekisteröintien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="71071-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="71071-158">Näytä työntekijän aikakirjaukset ja suodata myymälän tai tapahtumatyypin perusteella.</span><span class="sxs-lookup"><span data-stu-id="71071-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="71071-159">Myyntipisteellä:</span><span class="sxs-lookup"><span data-stu-id="71071-159">On POS:</span></span>

- <span data-ttu-id="71071-160">Valitse **Näytä aikamerkinnät**.</span><span class="sxs-lookup"><span data-stu-id="71071-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="71071-161">Näet kaikkien niiden työntekijöiden aikakirjaustapahtumat, jotka on määritetty samoihin myymälöihin kuin sinä.</span><span class="sxs-lookup"><span data-stu-id="71071-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="71071-162">Voit käyttää tehtävätyyppiä ja myymälän suodattimia suodattamaan aikamerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="71071-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="71071-163">Aikarekisteröintien käsitteleminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="71071-163">Process and manage time registrations</span></span>

<span data-ttu-id="71071-164">Commerce-käyttäjä noudattaa työnkulkua aikakirjausten laskemiseen, hyväksymiseen ja palkanlaskentaan siirtämiseen.</span><span class="sxs-lookup"><span data-stu-id="71071-164">A Commerce user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="71071-165">Tärkeimmät työvaiheet</span><span class="sxs-lookup"><span data-stu-id="71071-165">Primary operations</span></span>

- <span data-ttu-id="71071-166">Laske</span><span class="sxs-lookup"><span data-stu-id="71071-166">Calculate</span></span>
- <span data-ttu-id="71071-167">Hyväksy</span><span class="sxs-lookup"><span data-stu-id="71071-167">Approve</span></span>
- <span data-ttu-id="71071-168">Lähetä palkanlaskentaan</span><span class="sxs-lookup"><span data-stu-id="71071-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="71071-169">Muut yleiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="71071-169">Other common operations</span></span>

- <span data-ttu-id="71071-170">Joukkopoistuminen</span><span class="sxs-lookup"><span data-stu-id="71071-170">Bulk Clock-out</span></span>
- <span data-ttu-id="71071-171">Poissaolon kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="71071-171">Register Absence</span></span>

<span data-ttu-id="71071-172">Lisätietoja työajan seurannan rekisteröintien käsittelystä on kohdassa [Työajan seurannan rekisteröintien käsittely](https://technet.microsoft.com/library/aa573180.aspx).</span><span class="sxs-lookup"><span data-stu-id="71071-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>
