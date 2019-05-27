---
title: Hakijan profiilien ja sovellusten lähteiden seuraaminen
description: Tässä ohjeaiheessa kerrotaan hakijaprofiilien ja -sovellusten lähteiden seurannasta.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ebc82ada31d2803800358cd9aecfe389ada8f0dc
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517928"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a><span data-ttu-id="f8da1-103">Hakijan profiilien ja sovellusten lähteiden seuraaminen</span><span class="sxs-lookup"><span data-stu-id="f8da1-103">Track sources for candidate profiles and applications</span></span> 

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> <span data-ttu-id="f8da1-104">Tässä ohjeaiheessa mainitut toiminnot ovat saatavilla ennakkoversion osana.</span><span class="sxs-lookup"><span data-stu-id="f8da1-104">Functionality noted in this topic is available as part of a preview review release.</span></span> <span data-ttu-id="f8da1-105">Sisältö ja toiminnot voivat muuttua.</span><span class="sxs-lookup"><span data-stu-id="f8da1-105">The content and the functionality are subject to change.</span></span> <span data-ttu-id="f8da1-106">Voit käyttää tätä toimintoa pyytämällä järjestelmänvalvojaa ottamaan sen käyttöön Attractin **järjestelmänvalvojan asetuksissa**.</span><span class="sxs-lookup"><span data-stu-id="f8da1-106">To use this feature, ask an administrator to enable it using the **Admin settings** in Attract.</span></span> <span data-ttu-id="f8da1-107">Tuleva julkaisu tarjoaa lähdeseurantaraportteja.</span><span class="sxs-lookup"><span data-stu-id="f8da1-107">A future release will provide source tracking reports.</span></span> <span data-ttu-id="f8da1-108">Lisätietoja on kohdassa [Talentin esiversiotoimintojen käyttö](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="f8da1-108">For more information, see [Access preview features in Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

<span data-ttu-id="f8da1-109">Kun hakijat hakevat työtä, Attract seuraa automaattisesti sovellustensa lähdettä ja antaa sinulle arvokasta tietoa, jonka avulla voit kohdistaa rekrytointityösi.</span><span class="sxs-lookup"><span data-stu-id="f8da1-109">When candidates apply for a job, Attract automatically tracks the source of their applications, providing you with valuable information to help you target your recruiting efforts.</span></span> <span data-ttu-id="f8da1-110">Rekrytoijat ja rekrytointipäälliköt voivat myös valita sovelluslähteen samalla, kun lisäät hakijan manuaalisesti työ- tai lahjakkuusalueelle.</span><span class="sxs-lookup"><span data-stu-id="f8da1-110">Recruiters and hiring managers can also select an application source while manually adding a candidate to a job or talent pool.</span></span>

<span data-ttu-id="f8da1-111">Voit tarkastella sovelluksen lähdettä sovelluksen toiminnan yksityiskohdissa **Tehtävä**-välilehdellä samoin kuin sovellushistoria kohdassa **Profiili** kykypooleissa.</span><span class="sxs-lookup"><span data-stu-id="f8da1-111">You can view the application source in the application activity details under the **Activity** tab, as well as in the application history available under **Profile** in talent pools.</span></span> <span data-ttu-id="f8da1-112">Löydät hakijan profiililähteen hakijan tiedoista kohdasta **Profiili** sekä sovellusten ja kykypoolien välilehdeltä.</span><span class="sxs-lookup"><span data-stu-id="f8da1-112">You can find a candidate's profile source in the candidate details under the **Profile** tab in both applications and talent pools.</span></span>

> [!NOTE] 
> <span data-ttu-id="f8da1-113">Prosessimallit löytyvät kohdasta [Kattava työhönottolaajennus](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="f8da1-113">You can find process templates in the [Comprehensive hiring add-on](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>

## <a name="pre-configured-sources"></a><span data-ttu-id="f8da1-114">Ennalta määritetyt lähteet</span><span class="sxs-lookup"><span data-stu-id="f8da1-114">Pre-configured sources</span></span>

<span data-ttu-id="f8da1-115">Oletuslähteiden luettelo sisältää yleisiä sovelluslähteitä.</span><span class="sxs-lookup"><span data-stu-id="f8da1-115">The default source list contains common application sources.</span></span> <span data-ttu-id="f8da1-116">Joillakin lähdetyypeillä, kuten **Työtaulu** ja **Sosiaalinen verkko**, on ylimääräisiä lähdetietoja.</span><span class="sxs-lookup"><span data-stu-id="f8da1-116">Some source types, like **Job board** and **Social Network**, have additional source details.</span></span> <span data-ttu-id="f8da1-117">Esimerkiksi **Sosiaalinen verkko** sisältää Facebookin ja Twitterin.</span><span class="sxs-lookup"><span data-stu-id="f8da1-117">For example, **Social Network** includes Facebook and Twitter.</span></span> <span data-ttu-id="f8da1-118">**Viittauksen** lähdetyypin avulla voit määrittää sisäisen työntekijän viittaajaksi.</span><span class="sxs-lookup"><span data-stu-id="f8da1-118">The **Referral** source type allows you to specify an internal employee as the referrer.</span></span> <span data-ttu-id="f8da1-119">Oletuslähteiden luettelo sisältää seuraavat ennalta määritetyt lähteet:</span><span class="sxs-lookup"><span data-stu-id="f8da1-119">The default source list includes the following pre-configured sources:</span></span>

-   <span data-ttu-id="f8da1-120">Attract-urasivusto</span><span class="sxs-lookup"><span data-stu-id="f8da1-120">Attract career site</span></span>

-   <span data-ttu-id="f8da1-121">Virasto</span><span class="sxs-lookup"><span data-stu-id="f8da1-121">Agency</span></span>

-   <span data-ttu-id="f8da1-122">Uramessut</span><span class="sxs-lookup"><span data-stu-id="f8da1-122">Career Fair</span></span>

-   <span data-ttu-id="f8da1-123">Yrityksen markkinointi</span><span class="sxs-lookup"><span data-stu-id="f8da1-123">Company Marketing</span></span>

-   <span data-ttu-id="f8da1-124">Konferenssit ja messut</span><span class="sxs-lookup"><span data-stu-id="f8da1-124">Conferences & Trade shows</span></span>

-   <span data-ttu-id="f8da1-125">Asiantuntijayhteisö</span><span class="sxs-lookup"><span data-stu-id="f8da1-125">Professional Association</span></span>

-   <span data-ttu-id="f8da1-126">Työtaulu</span><span class="sxs-lookup"><span data-stu-id="f8da1-126">Job board</span></span>

    -   <span data-ttu-id="f8da1-127">Itse asiassa</span><span class="sxs-lookup"><span data-stu-id="f8da1-127">Indeed</span></span>

    -   <span data-ttu-id="f8da1-128">Haku</span><span class="sxs-lookup"><span data-stu-id="f8da1-128">Seek</span></span>

    -   <span data-ttu-id="f8da1-129">CareerBuilder</span><span class="sxs-lookup"><span data-stu-id="f8da1-129">CareerBuilder</span></span>

    -   <span data-ttu-id="f8da1-130">Google työt</span><span class="sxs-lookup"><span data-stu-id="f8da1-130">Google Jobs</span></span>

    -   <span data-ttu-id="f8da1-131">Xing</span><span class="sxs-lookup"><span data-stu-id="f8da1-131">Xing</span></span>

    -   <span data-ttu-id="f8da1-132">Glassdoor</span><span class="sxs-lookup"><span data-stu-id="f8da1-132">Glassdoor</span></span>

    -   <span data-ttu-id="f8da1-133">Monster Jobs</span><span class="sxs-lookup"><span data-stu-id="f8da1-133">Monster Jobs</span></span>

-   <span data-ttu-id="f8da1-134">Aikakauslehdet ja julkaisut</span><span class="sxs-lookup"><span data-stu-id="f8da1-134">Magazines & Publications</span></span>

-   <span data-ttu-id="f8da1-135">Sosiaalinen verkko</span><span class="sxs-lookup"><span data-stu-id="f8da1-135">Social Network</span></span>

    -   <span data-ttu-id="f8da1-136">Facebook</span><span class="sxs-lookup"><span data-stu-id="f8da1-136">Facebook</span></span>

    -   <span data-ttu-id="f8da1-137">Twitter</span><span class="sxs-lookup"><span data-stu-id="f8da1-137">Twitter</span></span>

-   <span data-ttu-id="f8da1-138">Yliopiston rekrytointi</span><span class="sxs-lookup"><span data-stu-id="f8da1-138">University Recruiting</span></span>

-   <span data-ttu-id="f8da1-139">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="f8da1-139">LinkedIn</span></span>

-   <span data-ttu-id="f8da1-140">Luokittelemattomat</span><span class="sxs-lookup"><span data-stu-id="f8da1-140">Classifieds</span></span>

-   <span data-ttu-id="f8da1-141">Viite</span><span class="sxs-lookup"><span data-stu-id="f8da1-141">Referral</span></span>

-   <span data-ttu-id="f8da1-142">Rekrytoijan lisäämä</span><span class="sxs-lookup"><span data-stu-id="f8da1-142">Added by Recruiter</span></span>

-   <span data-ttu-id="f8da1-143">Muu</span><span class="sxs-lookup"><span data-stu-id="f8da1-143">Other</span></span>

## <a name="customize-the-source-list"></a><span data-ttu-id="f8da1-144">Lähdeluettelon mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="f8da1-144">Customize the source list</span></span> 

<span data-ttu-id="f8da1-145">Voit laajentaa lähdeluetteloa lisäämällä muita sovelluslähteitä.</span><span class="sxs-lookup"><span data-stu-id="f8da1-145">You can extend the source list to include additional application sources.</span></span> <span data-ttu-id="f8da1-146">Voit mukauttaa tätä luetteloa noudattamalla ohjeita kohdassa [Vaihtoehtoasetusten määrittäminen Attractissa](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span><span class="sxs-lookup"><span data-stu-id="f8da1-146">To customize this list, follow the instructions in [Extending Option Sets in Attract](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span></span> <span data-ttu-id="f8da1-147">Muokkaa **TalentSource**-yksikköä sisällyttääksesi muita lähteitä.</span><span class="sxs-lookup"><span data-stu-id="f8da1-147">Edit the **TalentSource** entity to include additional sources.</span></span> 

<span data-ttu-id="f8da1-148">Voit välttää käyttöliittymän (UI) negatiivista vaikutusta muokkaamalla tai poistamalla **TalentCategory** valintalistojen arvoja (ei nimiä) seuraaviin tarkoituksiin:</span><span class="sxs-lookup"><span data-stu-id="f8da1-148">To avoid negatively impacting the user interface (UI), don't edit or delete the **TalentCategory** enum values (not names) for the following:</span></span>

- <span data-ttu-id="f8da1-149">**Viite**</span><span class="sxs-lookup"><span data-stu-id="f8da1-149">**Referral**</span></span>
- <span data-ttu-id="f8da1-150">**LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="f8da1-150">**LinkedIn**</span></span>
- <span data-ttu-id="f8da1-151">**Muu**</span><span class="sxs-lookup"><span data-stu-id="f8da1-151">**Other**</span></span>

<span data-ttu-id="f8da1-152">Voit laajentaa sen sijaan **TalentSource**-valintalistaa lisätäksesi muita lähdetyyppejä.</span><span class="sxs-lookup"><span data-stu-id="f8da1-152">Instead, you can extend the **TalentSource** enum to add other types of sources.</span></span>
