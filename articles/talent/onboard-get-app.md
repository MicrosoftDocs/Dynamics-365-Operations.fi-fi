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
ms.openlocfilehash: 28ed12bd8cf2df7c25e14a25465cad1229676cfd
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551976"
---
# <a name="get-the-dynamics-365-talent---onboard-app"></a><span data-ttu-id="7d3d7-103">Dynamics 365 Talent: Onboard -sovelluksen hankkiminen</span><span class="sxs-lookup"><span data-stu-id="7d3d7-103">Get the Dynamics 365 Talent - Onboard app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7d3d7-104">Voit katsoa demon ja kokeilla Microsoft Dynamics 365 Talent: Onboard -sovellusta maksutta [Onboard-tuotesivulta](https://dynamics.microsoft.com/talent/onboard/).</span><span class="sxs-lookup"><span data-stu-id="7d3d7-104">You can view a demo and try the Microsoft Dynamics 365 Talent: Onboard app for free from the [Onboard product page](https://dynamics.microsoft.com/talent/onboard/).</span></span>

> [!NOTE]
> <span data-ttu-id="7d3d7-105">Maksuton kokeilu edellyttää yrityssähköpostitiliä.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-105">The free trial requires a business email account.</span></span>

<span data-ttu-id="7d3d7-106">Voit ostaa Onboard-tilauksen joko itsenäisenä sovelluksena tai Dynamics 365 Talentin osana.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-106">You can purchase a subscription to Onboard as either a stand-alone app or part of Dynamics 365 Talent.</span></span> <span data-ttu-id="7d3d7-107">Talent on kattava henkilöstöresurssien hallintajärjestelmä, joka sisältää Dynamics 365 Talent: Attractin, Onboardin ja Core HR:n.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-107">Talent is a comprehensive human capital management (HCM) system that includes Dynamics 365 Talent: Attract, Onboard, and Core HR.</span></span> <span data-ttu-id="7d3d7-108">Lisätietoja Onboardin ostamisesta on [Onboard-tuotesivulla](https://dynamics.microsoft.com/talent/onboard/).</span><span class="sxs-lookup"><span data-stu-id="7d3d7-108">For more information about how to purchase Onboard, see the [Onboard product page](https://dynamics.microsoft.com/talent/onboard/).</span></span>

<span data-ttu-id="7d3d7-109">Microsoft 365:n sähköpostiosoite ja salasana määritetään kokeilu- tai ostoprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-109">During the trial or purchase process, you will set up your Microsoft 365 email address and password.</span></span> <span data-ttu-id="7d3d7-110">Muista kirjoittaa nämä arvot muistiin.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-110">Be sure to make a note of these values.</span></span>

> [!WARNING]
> <span data-ttu-id="7d3d7-111">Et voi siirtää kokeiluversiosta maksettuun tilausympäristöön.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-111">You can't migrate data from your trial to your paid subscription environment.</span></span> <!--Reviewers: please verify.-->

<span data-ttu-id="7d3d7-112">Lisätietoja Talentin uusista ominaisuuksista on kohdassa [Uudet tai muuttuneet ominaisuudet Dynamics 365 Talentissa](./whats-new.md)ja [Dynamics 365- ja Power Platform -julkaisutiedot](https://docs.microsoft.com/business-applications-release-notes/index).</span><span class="sxs-lookup"><span data-stu-id="7d3d7-112">To find out about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform release notes](https://docs.microsoft.com/business-applications-release-notes/index).</span></span> <span data-ttu-id="7d3d7-113">Jos haluat Onboardin uusien toimintojen esiversion, lisätietoja on kohdassa [Talentin esiversiotoimintojen käyttäminen](./access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="7d3d7-113">If you want to preview new features in Onboard, see [Access preview features in Talent](./access-preview-feature.md).</span></span>

<span data-ttu-id="7d3d7-114">Jos olet IT-ammattilainen ja haluat lisätietoja Onboard-sovelluksen kahden version valmistelemisesta, lisätietoja on kohdassa [Onboard-sovelluksen valmisteleminen](./modular-app-tech-faq.md).</span><span class="sxs-lookup"><span data-stu-id="7d3d7-114">If you're an IT professional and want to learn more about how the two versions of the Onboard app are provisioned, see [Provisioning for the Onboard app](./modular-app-tech-faq.md).</span></span>

## <a name="get-started-with-onboard"></a><span data-ttu-id="7d3d7-115">Onboardin käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="7d3d7-115">Get started with Onboard</span></span>

<span data-ttu-id="7d3d7-116">Kun avaat Onboardin ensimmäistä kertaa, sinua pyydetään aloittamaan Microsoft 365 -hallintakeskuksen esittelyohjelma.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-116">When you open Onboard for the first time, you're invited to start a tour of the Microsoft 365 admin center.</span></span> <span data-ttu-id="7d3d7-117">Hallintakeskuksessa määritetään organisaatio, hallitaan käyttäjiä ja hallitaan tilauksia.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-117">The admin center is where you set up your organization, manage users, and manage your subscriptions.</span></span> <span data-ttu-id="7d3d7-118">(Yksi näistä tilauksista on Onboard-tilaus.) Lisätietoja Microsoft 365 -hallintakeskuksesta on kohdassa [Tietoja Microsoft 365 -hallintakeskuksessa](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="7d3d7-118">(One of those subscriptions is your Onboard subscription.) For more information about the Microsoft 365 admin center, see [About the Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

<span data-ttu-id="7d3d7-119">Siirry Onboard-sovellukseen seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-119">To get to the Onboard app, follow these steps.</span></span>

1. <span data-ttu-id="7d3d7-120">Avaa [Microsoftin kirjautumissivu](https://portal.office.com/).</span><span class="sxs-lookup"><span data-stu-id="7d3d7-120">Open the [Microsoft sign-in page](https://portal.office.com/).</span></span>
2. <span data-ttu-id="7d3d7-121">Anna pyydettäessä Microsoft 365:n sähköpostiosoite ja salasana.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-121">When you're prompted, enter your Microsoft 365 email address and password.</span></span>
3. <span data-ttu-id="7d3d7-122">Valitse vasemmassa yläkulmassa sovelluksen käynnistys ja valitse **Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-122">Select the app launcher in the upper left, and then select **Dynamics 365**.</span></span>

    <span data-ttu-id="7d3d7-123">[![Dynamics 365:n käyttäminen](./media/onboard-start-dynamics365.png)](./media/onboard-start-dynamics365.png)</span><span class="sxs-lookup"><span data-stu-id="7d3d7-123">[![Accessing Dynamics 365](./media/onboard-start-dynamics365.png)](./media/onboard-start-dynamics365.png)</span></span>

4. <span data-ttu-id="7d3d7-124">Valitse **Talent: Onboard** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-124">Select the **Talent: Onboard** tile.</span></span>

    <span data-ttu-id="7d3d7-125">[![Onboardin avaaminen](./media/onboard-start-onboard.png)](./media/onboard-start-onboard.png)</span><span class="sxs-lookup"><span data-stu-id="7d3d7-125">[![Opening Onboard](./media/onboard-start-onboard.png)](./media/onboard-start-onboard.png)</span></span>

<span data-ttu-id="7d3d7-126">Ensimmäinen kirjautuminen voi kestää muutaman minuutin, koska ympäristö on alustettava.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-126">Your first sign-in might take a few minutes, because the environment must be initialized.</span></span>

## <a name="try-the-walkthrough"></a><span data-ttu-id="7d3d7-127">Esittelyn kokeileminen</span><span class="sxs-lookup"><span data-stu-id="7d3d7-127">Try the walkthrough</span></span>

<span data-ttu-id="7d3d7-128">Kun avaat Onboardin ensimmäinen kerran, voit aloittaa mallin käyttämisen valitsemalla **Aloita esittely**.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-128">When you first open Onboard, you can select **Start the walkthrough** to get started with a working template.</span></span>

<span data-ttu-id="7d3d7-129">Jos ohitat esittelyn, voit siirtyä siihen myöhemmin valitsemalla ensin **Ohje**-painikkeen (**?**) ja sitten **Aloittaminen**.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-129">If you skip the walkthrough, you can access it later by selecting the **Help** button (**?**) and then selecting **Get started**.</span></span>

![[<span data-ttu-id="7d3d7-130">Onboard-esittelyn käynnistäminen</span><span class="sxs-lookup"><span data-stu-id="7d3d7-130">Starting the Onboard walkthrough</span></span>](./media/onboard-start-walkthrough.png)](./media/onboard-start-walkthrough.png)

## <a name="change-the-domain-name"></a><span data-ttu-id="7d3d7-131">Toimialueen nimen muuttaminen</span><span class="sxs-lookup"><span data-stu-id="7d3d7-131">Change the domain name</span></span>

<span data-ttu-id="7d3d7-132">Jos hyväksyit oletustoimialuenimen, kun kirjauduit Onboardiin, voit vaihtaa sen toiseen toimialueeseen myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-132">If you accepted the default domain name when you signed up with Onboard, you can change it to another domain later.</span></span> <span data-ttu-id="7d3d7-133">(Oletustoimialuenimen lopussa on **onmicrosoft.com**.)</span><span class="sxs-lookup"><span data-stu-id="7d3d7-133">(The default domain name ends in **onmicrosoft.com**.)</span></span>

1. <span data-ttu-id="7d3d7-134">Avaa [Microsoftin kirjautumissivu](https://portal.office.com/).</span><span class="sxs-lookup"><span data-stu-id="7d3d7-134">Open the [Microsoft sign-in page](https://portal.office.com/).</span></span>
2. <span data-ttu-id="7d3d7-135">Anna pyydettäessä Microsoft 365:n sähköpostiosoite ja salasana.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-135">When you're prompted, enter your Microsoft 365 email address and password.</span></span>
3. <span data-ttu-id="7d3d7-136">Jos suositus toimialueen lisäämisestä ei näy **Suositellaan sinulle** -kohdassa, valitse **Näytä suositus** ja toimi kehotteiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-136">If you see a recommendation to add your own domain under **Recommended for you**, select **View recommendation**, and follow the prompts.</span></span> <span data-ttu-id="7d3d7-137">Jos et näe suositusta, valitse vasemmassa valikossa ensin **Näytä kaikki**, sitten **Asetukset**, seuraavaksi **Toimialueet** ja lopuksi joko **Lisää toimialue** tai **Osta toimialue**.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-137">If you don't see the recommendation, select **Show all** on the menu on the left, select **Setup**, select **Domains**, and then select either **Add domain** or **Buy domain**.</span></span> <span data-ttu-id="7d3d7-138">Toimi sitten kehotteiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="7d3d7-138">Then follow the prompts.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7d3d7-139">Seuraavat vaiheet</span><span class="sxs-lookup"><span data-stu-id="7d3d7-139">Next steps</span></span>

- [<span data-ttu-id="7d3d7-140">Perehdytysoppaan luominen</span><span class="sxs-lookup"><span data-stu-id="7d3d7-140">Create an onboarding guide</span></span>](./onboard-create-guide.md)
- [<span data-ttu-id="7d3d7-141">Perehdytysmallin luominen</span><span class="sxs-lookup"><span data-stu-id="7d3d7-141">Create an onboarding template</span></span>](./onboard-create-template.md)
- [<span data-ttu-id="7d3d7-142">Perehdytysoppaiden ja mallien muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="7d3d7-142">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="7d3d7-143">Sisällön jakaminen muiden osallisten kanssa</span><span class="sxs-lookup"><span data-stu-id="7d3d7-143">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="7d3d7-144">Työntekijöiden tehtävien ja perehdyttämisen tilan näyttäminen</span><span class="sxs-lookup"><span data-stu-id="7d3d7-144">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="7d3d7-145">Työhönottoryhmien luominen Onboardissa</span><span class="sxs-lookup"><span data-stu-id="7d3d7-145">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="7d3d7-146">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="7d3d7-146">See also</span></span>

- [<span data-ttu-id="7d3d7-147">Onboard-sovelluksen kokeileminen tai ostaminen</span><span class="sxs-lookup"><span data-stu-id="7d3d7-147">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="7d3d7-148">Uutta</span><span class="sxs-lookup"><span data-stu-id="7d3d7-148">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="7d3d7-149">Julkaisutiedot</span><span class="sxs-lookup"><span data-stu-id="7d3d7-149">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="7d3d7-150">Tuen saaminen</span><span class="sxs-lookup"><span data-stu-id="7d3d7-150">Get support</span></span>](./talent-support.md)
