---
title: 'Dynamics 365 Talent: Onboard -sovelluksen hankkiminen'
description: 'Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent: Onboard -sovelluksen itsenäisen version tai kattavan työhönottolaajennuksen sisältävän version hankkimista.'
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: 1b59fdbdd9ed46f42afd3e7310d2cd3f076edd95
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461092"
---
# <a name="get-the-onboard-app"></a><span data-ttu-id="6bebd-103">Onboard-sovelluksen hankkiminen</span><span class="sxs-lookup"><span data-stu-id="6bebd-103">Get the Onboard app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6bebd-104">Voit katsoa demon ja kokeilla Microsoft Dynamics 365 Talent: Onboard -sovellusta maksutta [Onboard-tuotesivulta](https://dynamics.microsoft.com/talent/onboard/).</span><span class="sxs-lookup"><span data-stu-id="6bebd-104">You can view a demo and try the Microsoft Dynamics 365 Talent: Onboard app for free from the [Onboard product page](https://dynamics.microsoft.com/talent/onboard/).</span></span>

> [!NOTE]
> <span data-ttu-id="6bebd-105">Maksuton kokeilu edellyttää yrityssähköpostitiliä.</span><span class="sxs-lookup"><span data-stu-id="6bebd-105">The free trial requires a business email account.</span></span>

<span data-ttu-id="6bebd-106">Voit ostaa Onboard-tilauksen joko itsenäisenä sovelluksena tai Dynamics 365 Talentin osana.</span><span class="sxs-lookup"><span data-stu-id="6bebd-106">You can purchase a subscription to Onboard as either a stand-alone app or part of Dynamics 365 Talent.</span></span> <span data-ttu-id="6bebd-107">Lisätietoja Onboardin ostamisesta on [Onboard-tuotesivulla](https://dynamics.microsoft.com/talent/onboard/).</span><span class="sxs-lookup"><span data-stu-id="6bebd-107">For more information about how to purchase Onboard, see the [Onboard product page](https://dynamics.microsoft.com/talent/onboard/).</span></span>

<span data-ttu-id="6bebd-108">Microsoft 365:n sähköpostiosoite ja salasana määritetään kokeilu- tai ostoprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="6bebd-108">During the trial or purchase process, you will set up your Microsoft 365 email address and password.</span></span> <span data-ttu-id="6bebd-109">Muista kirjoittaa nämä arvot muistiin.</span><span class="sxs-lookup"><span data-stu-id="6bebd-109">Be sure to make a note of these values.</span></span>

> [!WARNING]
> <span data-ttu-id="6bebd-110">Et voi siirtää kokeiluversiosta maksettuun tilausympäristöön.</span><span class="sxs-lookup"><span data-stu-id="6bebd-110">You can't migrate data from your trial to your paid subscription environment.</span></span> <!--Reviewers: please verify.-->

<span data-ttu-id="6bebd-111">Lisätietoja Talentin uusista ominaisuuksista on kohdassa [Uudet tai muuttuneet ominaisuudet Dynamics 365 Talentissa](./whats-new.md)ja [Dynamics 365- ja Power Platform -julkaisutiedot](https://docs.microsoft.com/business-applications-release-notes/index).</span><span class="sxs-lookup"><span data-stu-id="6bebd-111">To find out about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform release notes](https://docs.microsoft.com/business-applications-release-notes/index).</span></span> <span data-ttu-id="6bebd-112">Jos haluat Onboardin uusien toimintojen esiversion, lisätietoja on kohdassa [Microsoft Dynamics 365 Talentin esiversiotoimintojen käyttäminen](./access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="6bebd-112">If you want to preview new features in Onboard, see [Access preview features in Microsoft Dynamics 365 Talent](./access-preview-feature.md).</span></span>

<span data-ttu-id="6bebd-113">Jos olet IT-ammattilainen ja haluat lisätietoja Onboard-sovelluksen kahden version valmistelemisesta, lisätietoja on kohdassa [Dynamics 365 Talent – Onboard -sovelluksen valmisteleminen](./modular-app-tech-faq.md).</span><span class="sxs-lookup"><span data-stu-id="6bebd-113">If you're an IT professional and want to learn more about how the two versions of the Onboard app are provisioned, see [Provisioning for the Dynamics 365 Talent - Onboard app](./modular-app-tech-faq.md).</span></span>

## <a name="get-started-with-onboard"></a><span data-ttu-id="6bebd-114">Onboardin käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="6bebd-114">Get started with Onboard</span></span>

<span data-ttu-id="6bebd-115">Kun avaat Onboardin ensimmäistä kertaa, sinua pyydetään aloittamaan Microsoft 365 -hallintakeskuksen esittelyohjelma.</span><span class="sxs-lookup"><span data-stu-id="6bebd-115">When you open Onboard for the first time, you're invited to start a tour of the Microsoft 365 admin center.</span></span> <span data-ttu-id="6bebd-116">Hallintakeskuksessa määritetään organisaatio, hallitaan käyttäjiä ja hallitaan tilauksia.</span><span class="sxs-lookup"><span data-stu-id="6bebd-116">The admin center is where you set up your organization, manage users, and manage your subscriptions.</span></span> <span data-ttu-id="6bebd-117">(Yksi näistä tilauksista on Onboard-tilaus.) Lisätietoja Microsoft 365 -hallintakeskuksesta on kohdassa [Tietoja Microsoft 365 -hallintakeskuksessa](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="6bebd-117">(One of those subscriptions is your Onboard subscription.) For more information about the Microsoft 365 admin center, see [About the Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

<span data-ttu-id="6bebd-118">Siirry Onboard-sovellukseen seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="6bebd-118">To get to the Onboard app, follow these steps.</span></span>

1. <span data-ttu-id="6bebd-119">Avaa [Microsoftin kirjautumissivu](https://portal.office.com/).</span><span class="sxs-lookup"><span data-stu-id="6bebd-119">Open the [Microsoft sign-in page](https://portal.office.com/).</span></span>
2. <span data-ttu-id="6bebd-120">Anna pyydettäessä Microsoft 365:n sähköpostiosoite ja salasana.</span><span class="sxs-lookup"><span data-stu-id="6bebd-120">When you're prompted, enter your Microsoft 365 email address and password.</span></span>
3. <span data-ttu-id="6bebd-121">Valitse vasemmassa yläkulmassa sovelluksen käynnistys ja valitse **Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="6bebd-121">Select the app launcher in the upper left, and then select **Dynamics 365**.</span></span>

    <span data-ttu-id="6bebd-122">[![Dynamics 365:n käyttäminen](./media/onboard-start-dynamics365.png)](./media/onboard-start-dynamics365.png)</span><span class="sxs-lookup"><span data-stu-id="6bebd-122">[![Accessing Dynamics 365](./media/onboard-start-dynamics365.png)](./media/onboard-start-dynamics365.png)</span></span>

4. <span data-ttu-id="6bebd-123">Valitse **Talent: Onboard** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="6bebd-123">Select the **Talent: Onboard** tile.</span></span>

    <span data-ttu-id="6bebd-124">[![Onboardin avaaminen](./media/onboard-start-onboard.png)](./media/onboard-start-onboard.png)</span><span class="sxs-lookup"><span data-stu-id="6bebd-124">[![Opening Onboard](./media/onboard-start-onboard.png)](./media/onboard-start-onboard.png)</span></span>

<span data-ttu-id="6bebd-125">Ensimmäinen kirjautuminen voi kestää muutaman minuutin, koska ympäristö on alustettava.</span><span class="sxs-lookup"><span data-stu-id="6bebd-125">Your first sign-in might take a few minutes, because the environment must be initialized.</span></span>

## <a name="try-the-walkthrough"></a><span data-ttu-id="6bebd-126">Esittelyn kokeileminen</span><span class="sxs-lookup"><span data-stu-id="6bebd-126">Try the walkthrough</span></span>

<span data-ttu-id="6bebd-127">Kun avaat Onboardin ensimmäinen kerran, voit aloittaa mallin käyttämisen valitsemalla **Aloita esittely**.</span><span class="sxs-lookup"><span data-stu-id="6bebd-127">When you first open Onboard, you can select **Start the walkthrough** to get started with a working template.</span></span>

<span data-ttu-id="6bebd-128">Jos ohitat esittelyn, voit siirtyä siihen myöhemmin valitsemalla ensin **Ohje**-painikkeen (**?**) ja sitten **Aloittaminen**.</span><span class="sxs-lookup"><span data-stu-id="6bebd-128">If you skip the walkthrough, you can access it later by selecting the **Help** button (**?**) and then selecting **Get started**.</span></span>

![[<span data-ttu-id="6bebd-129">Onboardingin läpikäymisen aloittaminen</span><span class="sxs-lookup"><span data-stu-id="6bebd-129">Starting the Onboard walkthrough</span></span>](./media/onboard-start-walkthrough.png)](./media/onboard-start-walkthrough.png)

## <a name="change-the-domain-name"></a><span data-ttu-id="6bebd-130">Toimialueen nimen muuttaminen</span><span class="sxs-lookup"><span data-stu-id="6bebd-130">Change the domain name</span></span>

<span data-ttu-id="6bebd-131">Jos hyväksyit oletustoimialuenimen, kun kirjauduit Onboardiin, voit vaihtaa sen toiseen toimialueeseen myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="6bebd-131">If you accepted the default domain name when you signed up with Onboard, you can change it to another domain later.</span></span> <span data-ttu-id="6bebd-132">(Oletustoimialuenimen lopussa on **onmicrosoft.com**.)</span><span class="sxs-lookup"><span data-stu-id="6bebd-132">(The default domain name ends in **onmicrosoft.com**.)</span></span>

1. <span data-ttu-id="6bebd-133">Avaa [Microsoftin kirjautumissivu](https://portal.office.com/).</span><span class="sxs-lookup"><span data-stu-id="6bebd-133">Open the [Microsoft sign-in page](https://portal.office.com/).</span></span>
2. <span data-ttu-id="6bebd-134">Anna pyydettäessä Microsoft 365:n sähköpostiosoite ja salasana.</span><span class="sxs-lookup"><span data-stu-id="6bebd-134">When you're prompted, enter your Microsoft 365 email address and password.</span></span>
3. <span data-ttu-id="6bebd-135">Jos suositus toimialueen lisäämisestä ei näy **Suositellaan sinulle** -kohdassa, valitse **Näytä suositus** ja toimi kehotteiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="6bebd-135">If you see a recommendation to add your own domain under **Recommended for you**, select **View recommendation**, and follow the prompts.</span></span> <span data-ttu-id="6bebd-136">Jos et näe suositusta, valitse vasemmassa valikossa ensin **Näytä kaikki**, sitten **Asetukset**, seuraavaksi **Toimialueet** ja lopuksi joko **Lisää toimialue** tai **Osta toimialue**.</span><span class="sxs-lookup"><span data-stu-id="6bebd-136">If you don't see the recommendation, select **Show all** on the menu on the left, select **Setup**, select **Domains**, and then select either **Add domain** or **Buy domain**.</span></span> <span data-ttu-id="6bebd-137">Toimi sitten kehotteiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="6bebd-137">Then follow the prompts.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6bebd-138">Seuraavat vaiheet</span><span class="sxs-lookup"><span data-stu-id="6bebd-138">Next steps</span></span>

- [<span data-ttu-id="6bebd-139">Perehdytysoppaan luominen</span><span class="sxs-lookup"><span data-stu-id="6bebd-139">Create an onboarding guide</span></span>](./onboard-create-guide.md)
- [<span data-ttu-id="6bebd-140">Perehdytysmallin luominen</span><span class="sxs-lookup"><span data-stu-id="6bebd-140">Create an onboarding template</span></span>](./onboard-create-template.md)
- [<span data-ttu-id="6bebd-141">Perehdytysoppaiden ja mallien muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="6bebd-141">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="6bebd-142">Sisällön jakaminen muiden osallisten kanssa</span><span class="sxs-lookup"><span data-stu-id="6bebd-142">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="6bebd-143">Työntekijöiden tehtävien ja perehdyttämisen tilan näyttäminen</span><span class="sxs-lookup"><span data-stu-id="6bebd-143">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="6bebd-144">Työhönottoryhmien luominen Onboardissa</span><span class="sxs-lookup"><span data-stu-id="6bebd-144">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="6bebd-145">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="6bebd-145">See also</span></span>

- [<span data-ttu-id="6bebd-146">Onboard-sovelluksen kokeileminen tai ostaminen</span><span class="sxs-lookup"><span data-stu-id="6bebd-146">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="6bebd-147">Dynamics 365 Talentin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="6bebd-147">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="6bebd-148">Julkaisusuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="6bebd-148">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="6bebd-149">Microsoft iDynamics 365 Talentin tuki</span><span class="sxs-lookup"><span data-stu-id="6bebd-149">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
