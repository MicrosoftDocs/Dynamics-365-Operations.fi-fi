---
title: "Työajan seuranta vähittäismyynnissä"
description: "Tässä aiheessa on kuvaus vähittäismyynnin ajan ja työajan hallinnassa tuettavista skenaarioista Microsoft Dynamics 365 for Retailissa."
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ebbf3c72b4c34cba95ecd2fb3ce506af393acc34
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="retail-time-and-attendance"></a><span data-ttu-id="5d4ac-103">Vähittäismyynnin työajan seuranta</span><span class="sxs-lookup"><span data-stu-id="5d4ac-103">Retail time and attendance</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="5d4ac-104">Tässä aiheessa on kuvaus vähittäismyynnin ajan ja työajan hallinnassa tuettavista skenaarioista Microsoft Dynamics 365 for Retailissa.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-104">This topic describes the scenarios that are supported for time and attendance management in Microsoft Dynamics 365 for Retail.</span></span> 

<a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="5d4ac-105">Työntekijän asetusten ja ajoituksen hallinta</span><span class="sxs-lookup"><span data-stu-id="5d4ac-105">Manage worker setup and scheduling</span></span>
----------------------------------

### <a name="initial-configuration"></a><span data-ttu-id="5d4ac-106"> - alkukokoonpano</span><span class="sxs-lookup"><span data-stu-id="5d4ac-106">Initial configuration</span></span>

-   <span data-ttu-id="5d4ac-107">Suorita ohjattu konfigurointitoiminto.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-107">Run the configuration wizard.</span></span>
-   <span data-ttu-id="5d4ac-108">Rekisteröi työntekijät aikakirjausten työntekijöiksi.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="5d4ac-109">Suunnittele työntekijöiden aikatauluja</span><span class="sxs-lookup"><span data-stu-id="5d4ac-109">Plan worker schedules</span></span>

-   <span data-ttu-id="5d4ac-110">Liitä profiileita työn suunnittelutoiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="5d4ac-111">Lisätietoja on kohdassa <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-111">For more information, see <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span></span>

<span data-ttu-id="5d4ac-112">Tietoja määritysten vaiheista on kohdassa<https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-112">For information about the configuration steps, see <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="5d4ac-113">Vähittäismyynnille ominaiset määritykset</span><span class="sxs-lookup"><span data-stu-id="5d4ac-113">Retail-specific configuration</span></span>

-   <span data-ttu-id="5d4ac-114">Ota toimintoprofiili käyttöön aikamerkinnöissä työntekijöille, joille haluat ottaa käyttöön aikakirjaukset.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="5d4ac-115">Valitse **Myyntipisteen toimintoprofiilit** &gt; **Toiminnot** &gt; **Myyntipisteen aikakirjaukset** &gt; **Ota käyttöön aikakirjaukset**.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
-   <span data-ttu-id="5d4ac-116">Määritä myyntipisteen käyttöoikeudet ottaaksesi käyttöön aikamerkintöjen tarkasteluluvat.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="5d4ac-117">Tämä lupa antaa käyttäjälle oikeuden tarkastella muiden saman myymälän työntekijöiden aikakirjauksia, ja lisäksi osoitekirjan kautta muiden myymälöiden, joihin käyttäjä on liitetty.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="5d4ac-118">Haluat ehkä myöntää tämän oikeuden päällikköroolille mutta ei kassanhoitajan roolille.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="5d4ac-119">Valitse **Myyntipisteen käyttöoikeusryhmät** &gt; **Näytä aikamerkinnät**.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="5d4ac-120">Rekisteröi aika</span><span class="sxs-lookup"><span data-stu-id="5d4ac-120">Register time</span></span>
### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="5d4ac-121">Kassanhoitajien ja muiden kuin kassanhoitajien kirjaukset</span><span class="sxs-lookup"><span data-stu-id="5d4ac-121">Cashier and non-cashier time registrations</span></span>

-   <span data-ttu-id="5d4ac-122">Myyntipisteellä:</span><span class="sxs-lookup"><span data-stu-id="5d4ac-122">On POS:</span></span>
    -   <span data-ttu-id="5d4ac-123">Saapumistoiminnot:</span><span class="sxs-lookup"><span data-stu-id="5d4ac-123">Clock-in operations:</span></span>
        -   <span data-ttu-id="5d4ac-124">Kirjaudu sisään muulla kuin kassatoiminnolla tai Uusi vuoro -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-124">Log on with a non-drawer operation or New shift.</span></span>
        -   <span data-ttu-id="5d4ac-125">Valitse aikamerkintätoiminto.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-125">Select a Time Clock operation.</span></span>
        -   <span data-ttu-id="5d4ac-126">Valitse haluttu toiminto:</span><span class="sxs-lookup"><span data-stu-id="5d4ac-126">Select a desired operation:</span></span>
            -   <span data-ttu-id="5d4ac-127">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="5d4ac-127">Clock-in</span></span>
            -   <span data-ttu-id="5d4ac-128">Työtauko</span><span class="sxs-lookup"><span data-stu-id="5d4ac-128">Break for Work</span></span>
            -   <span data-ttu-id="5d4ac-129">Lounastauko</span><span class="sxs-lookup"><span data-stu-id="5d4ac-129">Break for Lunch</span></span>
            -   <span data-ttu-id="5d4ac-130">Poistuminen</span><span class="sxs-lookup"><span data-stu-id="5d4ac-130">Clock-out</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="5d4ac-131">Nykyinen tila:</span><span class="sxs-lookup"><span data-stu-id="5d4ac-131">Current state</span></span></th>
    <th><span data-ttu-id="5d4ac-132">Käytettävissä olevat toiminnot</span><span class="sxs-lookup"><span data-stu-id="5d4ac-132">Available operations</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="5d4ac-133">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="5d4ac-133">Clock-in</span></span></td>
    <td><ul>
    <li><span data-ttu-id="5d4ac-134">Työtauko</span><span class="sxs-lookup"><span data-stu-id="5d4ac-134">Break for Work</span></span></li>
    <li><span data-ttu-id="5d4ac-135">Lounastauko</span><span class="sxs-lookup"><span data-stu-id="5d4ac-135">Break for Lunch</span></span></li>
    <li><span data-ttu-id="5d4ac-136">Poistuminen</span><span class="sxs-lookup"><span data-stu-id="5d4ac-136">Clock-out</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="5d4ac-137">Työtauko</span><span class="sxs-lookup"><span data-stu-id="5d4ac-137">Break for Work</span></span></td>
    <td><span data-ttu-id="5d4ac-138">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="5d4ac-138">Clock-in</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="5d4ac-139">Lounastauko</span><span class="sxs-lookup"><span data-stu-id="5d4ac-139">Break for Lunch</span></span></td>
    <td><span data-ttu-id="5d4ac-140">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="5d4ac-140">Clock-in</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="5d4ac-141">Poistuminen</span><span class="sxs-lookup"><span data-stu-id="5d4ac-141">Clock-out</span></span></td>
    <td><span data-ttu-id="5d4ac-142">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="5d4ac-142">Clock-in</span></span></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="5d4ac-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="5d4ac-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>
-   <span data-ttu-id="5d4ac-144">Tarkastele vahvistussanomaa ja vahvista, että nykyinen merkinnän aika on oikea.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
-   <span data-ttu-id="5d4ac-145">Lokikirja:</span><span class="sxs-lookup"><span data-stu-id="5d4ac-145">Logbook:</span></span>
    -   <span data-ttu-id="5d4ac-146">Valitse **Lokikirja** tarkastellaksesi aikamerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-146">Click **Logbook** to view time clock activity.</span></span>
    -   <span data-ttu-id="5d4ac-147">Käytä ajan suodattimia eri aikaikkunoiden valitsemiseen.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-147">Use time filters to select different time windows.</span></span>
    -   <span data-ttu-id="5d4ac-148">Jos työskentelet useissa myymäläsijainneissa, näet aikakirjauksesi kaikista myymälöistä, joihin sinulle on kirjattu aikaa.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="5d4ac-149">Voit käyttää myymäläsuodatinta tarkastellaksesi valitun myymälän aikakirjauksia.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-149">You can use the store filter to view time registrations from a selected store.</span></span>

<!-- -->

-   <span data-ttu-id="5d4ac-150">Eri aikavyöhykkeet:</span><span class="sxs-lookup"><span data-stu-id="5d4ac-150">Different time zones:</span></span>
    -   <span data-ttu-id="5d4ac-151">Jos tarkastelet aikoja eri sijainnista (kassan lokikirjaa varten tai käyttämällä **Näytä aikamerkinnät** -toimintoa päällikköskenaariossa), ja kyseinen sijainti on eri aikavyöhykkeellä, näkemäsi aikamerkinnät muunnetaan paikalliseen aikavyöhykkeeseesi.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="5d4ac-152">Ajatellaan, että olet kahden myymälän päällikkö, joista toinen sijaitsee Arizonassa ja toinen Nevadassa.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="5d4ac-153">Kassa kirjaa saapumisen klo 9:00</span><span class="sxs-lookup"><span data-stu-id="5d4ac-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="5d4ac-154">Arizonassa.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-154">in Arizona.</span></span> <span data-ttu-id="5d4ac-155">Tuolla hetkellä kello on Nevadassa 8.00.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="5d4ac-156">Näin ollen, jos olet Nevadan liikkeessä ja katsot aikakirjaustietueita, kirjaus on merkitty klo 8.00:ksi.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="5d4ac-157">Työntekijän aikarekisteröintien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="5d4ac-157">View worker time registrations</span></span>
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="5d4ac-158">Näytä työntekijän aikakirjaukset ja suodata myymälän tai tapahtumatyypin perusteella.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="5d4ac-159">Myyntipisteellä:</span><span class="sxs-lookup"><span data-stu-id="5d4ac-159">On POS:</span></span>

-   <span data-ttu-id="5d4ac-160">Valitse **Näytä aikamerkinnät**.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-160">Select **View timeclock entries**.</span></span>
-   <span data-ttu-id="5d4ac-161">Näet kaikkien niiden työntekijöiden aikakirjaustapahtumat, jotka on määritetty samoihin myymälöihin kuin sinä.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
-   <span data-ttu-id="5d4ac-162">Voit käyttää tehtävätyyppiä ja myymälän suodattimia suodattamaan aikamerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="5d4ac-163">Aikarekisteröintien käsitteleminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="5d4ac-163">Process and manage time registrations</span></span>
<span data-ttu-id="5d4ac-164">A Dynamics 365 for Retail -käyttäjä noudattaa työnkulkua aikakirjausten laskemiseen, hyväksymiseen ja palkanlaskentaan siirtämiseen.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-164">A Dynamics 365 for Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="5d4ac-165">Tärkeimmät työvaiheet</span><span class="sxs-lookup"><span data-stu-id="5d4ac-165">Primary operations</span></span>

-   <span data-ttu-id="5d4ac-166">Laske</span><span class="sxs-lookup"><span data-stu-id="5d4ac-166">Calculate</span></span>
-   <span data-ttu-id="5d4ac-167">Hyväksy</span><span class="sxs-lookup"><span data-stu-id="5d4ac-167">Approve</span></span>
-   <span data-ttu-id="5d4ac-168">Lähetä palkanlaskentaan</span><span class="sxs-lookup"><span data-stu-id="5d4ac-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="5d4ac-169">Muut yleiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="5d4ac-169">Other common operations</span></span>

-   <span data-ttu-id="5d4ac-170">Joukkopoistuminen</span><span class="sxs-lookup"><span data-stu-id="5d4ac-170">Bulk Clock-out</span></span>
-   <span data-ttu-id="5d4ac-171">Poissaolon kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="5d4ac-171">Register Absence</span></span>

<span data-ttu-id="5d4ac-172">Saat lisätietoja työajan seurannan kirjausten käsittelystä kohdassa <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span><span class="sxs-lookup"><span data-stu-id="5d4ac-172">For more information about how to process time and attendance registrations, see <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span></span>




