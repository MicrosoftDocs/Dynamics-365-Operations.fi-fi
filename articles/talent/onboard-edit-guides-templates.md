---
title: Perehdytysoppaiden ja mallien mukaaminen Dynamics 365 for Talent - Onboardissa
description: Tässä ohjeaiheessa käsitellään tehtävien ja muiden tietojen lisäämistä Microsoft Dynamics 365 for Talent - Onboardin perehdytysoppaisiin ja malleihin.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
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
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 68afc5d789d1f4af67cd2ec73eb0e073efad0761
ms.sourcegitcommit: 4ff8c2c2f3705d8045df66f2c4393253e05b49ed
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864390"
---
# <a name="edit-onboarding-guides-and-templates-in-dynamics-365-for-talent-onboard"></a><span data-ttu-id="b1a7d-103">Perehdytysoppaiden ja mallien muokkaaminen Dynamics 365 for Talent: Onboardissa</span><span class="sxs-lookup"><span data-stu-id="b1a7d-103">Edit onboarding guides and templates in Dynamics 365 for Talent: Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b1a7d-104">Kun olet luonut perehdytysoppaan tai mallin Microsoft Dynamics 365 for Talent: Onboard, sinun on lisättävä johdanto, tehtävät, yhteyshenkilöt ja resurssit.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-104">After you create an onboarding guide or template in Microsoft Dynamics 365 for Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="b1a7d-105">Voit lisätä Onboardin perehdytysoppaisiin monipuolista sisältöä, kuten seuraavat:</span><span class="sxs-lookup"><span data-stu-id="b1a7d-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="b1a7d-106">YouTube-videot</span><span class="sxs-lookup"><span data-stu-id="b1a7d-106">YouTube videos</span></span>
- <span data-ttu-id="b1a7d-107">Microsoft Sway -esitykset</span><span class="sxs-lookup"><span data-stu-id="b1a7d-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="b1a7d-108">Microsoft PowerApps -sovellukset</span><span class="sxs-lookup"><span data-stu-id="b1a7d-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="b1a7d-109">Microsoft Stream -videot</span><span class="sxs-lookup"><span data-stu-id="b1a7d-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="b1a7d-110">Microsoft Forms -lomakkeet</span><span class="sxs-lookup"><span data-stu-id="b1a7d-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="b1a7d-111">Verkkosisältöä sisältävät iFrame-kehykset</span><span class="sxs-lookup"><span data-stu-id="b1a7d-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="b1a7d-112">Mallista tuotujen johdantojen tai tehtävien muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="b1a7d-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="b1a7d-113">Jos luot perehdytysoppaan mallista tai tuot tehtäviä mallista toiseen malliin, tuoduissa tehtävissä on **Lukitus**-painike.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="b1a7d-114">Näitä tehtäviä kutsutaan *hallituiksi tehtäviksi*.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-114">These are called *managed activities*.</span></span>

<span data-ttu-id="b1a7d-115">[![Hallitut tehtävät](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="b1a7d-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="b1a7d-116">Kun valitset hallitun tehtävän, lähdemalli näkyy tehtävän yläosassa.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="b1a7d-117">[![Hallitun tehtävän lähde](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="b1a7d-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="b1a7d-118">Jos muokkaat tehtävää mallissa, Onboard siirtää muutokset kaikkiin malleihin ja kyseiseen malliin perustuviin lähettämättömiin oppaisiin.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="b1a7d-119">Jos valitset lähettämättömän oppaan muokkaamasi mallin perusteella ja valitset sitten oppaassa **Tehtävät**-välilehden, huomaat, että opas on muuttunut.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="b1a7d-120">Voit hylätä ilmoituksen valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="b1a7d-121">[![Muutosilmoitus](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="b1a7d-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="b1a7d-122">Päivitettyjen tehtävien vieressä on musta piste.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="b1a7d-123">[![Muutettu tehtävä](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="b1a7d-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="b1a7d-124">Hallittuja tehtäviä ei voi muokata alkuperäisen mallin ulkopuolella lukuun ottamatta vastuunhenkilön, määräpäivän tai muiden tehtävän oikeanpuolisessa olevien tietojen lisäämistä.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="b1a7d-125">Jos haluat muokata hallittua tehtävää tai jos et halua, että tehtävä saa päivityksiä alkuperäisestä mallista, valitse kyseisen tehtävän **Lukitus**-painike.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="b1a7d-126">**Lukitus**-painike häviää.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="b1a7d-127">Alkuperäinen malli ei enää hallitse tehtävää eikä se enää vastaanota päivityksiä kyseisestä mallista.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="b1a7d-128">Tehtävään tehdyt päivitykset eivät vaikuta alkuperäiseen malliin.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="b1a7d-129">Jos poistat tehtävän oppaasta ja siirrät kyseisen oppaan mallin muutokset, tehtävät jää poistetuksi oppaassa.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="b1a7d-130">Mallit eivät hallitse yhteyshenkilöitä ja resursseja.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="b1a7d-131">Myöskään osat eivät ole hallittuja, joten jos lisäät osan tai muokkaat sitä mallissa, muutoksia ei siirretä muihin kyseistä mallia käyttäviin oppaisiin tai malleihin.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="b1a7d-132">Jos lisäät uusia tehtäviä malliin, uudet tehtävät siirretään kyseiseen malliin perustuviin oppaisiin ja malleihin. Nämä uudet tehtävät näkyvät kyseisen mallin yläosassa.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="b1a7d-133">Tehtävien tuominen toisesta mallista</span><span class="sxs-lookup"><span data-stu-id="b1a7d-133">Import activities from another template</span></span>

<span data-ttu-id="b1a7d-134">Voit tuoda tehtäviä oppaaseen tai malliin yhdestä tai useasta mallista.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="b1a7d-135">Valitse muokattava opas tai malli.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="b1a7d-136">Valitse **Tehtävät**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="b1a7d-137">Valitse oikealla **Tuo**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="b1a7d-138">[![Tehtävien tuominen](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="b1a7d-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="b1a7d-139">Voit esikatsella tehtäviä uudessa selaimen välilehdessä valitsemalla mallissa **Avaa uudessa välilehdessä** -painike.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="b1a7d-140">[![Tehtävien tuominen](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="b1a7d-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="b1a7d-141">Vedä ja pudota sopiva malli siihen ohjemallin kohtaan, jossa haluat tehtävien näkyvän.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="b1a7d-142">Jatka oppaan tai mallin muokkaamista.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="b1a7d-143">Tuoduissa tehtävissä on **Lukitus**-painike, joka ilmaisee, että se malli hallitsee kyseisiä tehtäviä, josta ne tuotiin.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="b1a7d-144">Kun teet muutoksia tuotuun malliin, nämä tehtävät päivitetään mallissa, johon ne tuotiin.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="b1a7d-145">Muutoksia ei kuitenkaan voi siirretä automaattisesti kaikkiin siitä mallista luotuihin oppaisiin, joihin tuonti tapahtui.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="b1a7d-146">Muutosten siirtäminen mallista toiseen malliin tai oppaaseen.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="b1a7d-147">Jos muokkaat muissa malleissa tai oppaissa käytettyjä tehtäviä, muutokset on siirrettävä, jos haluat niiden näkyvän muissa malleissa tai oppaissa.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="b1a7d-148">Jos et ole varma, käytetäänkö mallin tehtäviä muissa malleissa tai oppaissa, valitse **Käytössä**-välilehti ja tarkista, missä kyseiset tehtävät näkyvät.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="b1a7d-149">[![Niiden oppaiden ja mallien näyttäminen, joissa tehtäviä käytetään](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="b1a7d-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="b1a7d-150">Muutosten siirtäminen:</span><span class="sxs-lookup"><span data-stu-id="b1a7d-150">To push your changes:</span></span>

1. <span data-ttu-id="b1a7d-151">Tallenna muutokset valitsemalla **Tallenna**-painike.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="b1a7d-152">Jos et toimi näin, sinua pyydetään tallentamaan muutokset seuraavassa vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="b1a7d-153">Valitse **Siirrä nämä muutokset**.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="b1a7d-154">Johdannon lisääminen tai muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="b1a7d-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="b1a7d-155">Kirjoita oppaalle otsikko ja avausviesti **Johdanto**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="b1a7d-156">Voit käyttää näytetekstiä valitsemalla **Käytä tätä viestiä**.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="b1a7d-157">[![Onboard-mallin Johdanto-välilehti](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="b1a7d-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="b1a7d-158">Käytä muotoilupainikkeita tarpeen mukaan tekstin hakemiseen tai kuvien tai linkkien lisäämiseen.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="b1a7d-159">Tallenna työsi valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="b1a7d-160">Tehtävien lisääminen tai muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="b1a7d-160">Add or edit activities</span></span>

1. <span data-ttu-id="b1a7d-161">Vedä kohteita **Tehtävät**-välilehdessä oikealta muokkausalueelle.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="b1a7d-162">Järjestä opas osiin vetämällä **Uusi osa** -kohde muokkausalueelle ja anna osalle nimi ja valinnainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[<span data-ttu-id="b1a7d-163">Uuden osan lisääminen perehdytysoppaaseen tai malliin</span><span class="sxs-lookup"><span data-stu-id="b1a7d-163">Adding a new section to an onboarding guide or template</span></span>](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="b1a7d-164">Lisää tehtäviä uudelle työntekijälle tehtäväksi vetämällä **Uusi tehtävä** -kohde muokkausalueelle ja anna tehtävälle nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="b1a7d-165">Uuden tehtävän lisääminen perehdytysoppaaseen tai malliin</span><span class="sxs-lookup"><span data-stu-id="b1a7d-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="b1a7d-166">Monipuolisen sisällön lisääminen perehdytysoppaaseen:</span><span class="sxs-lookup"><span data-stu-id="b1a7d-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="b1a7d-167">Lisää YouTube-video vetämällä **YouTube**-kohde muokkausalueelle, anna tehtävälle nimi ja kuvaus ja anna YouTube-videon URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="b1a7d-168">Lisää Sway-esitys tai -uutiskirje vetämällä **Sway**-kohde muokkausalueelle, anna tehtävälle nimi ja kuvaus ja anna Sway-esityksen tai -uutiskirjeen upotettu URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="b1a7d-169">Lisää PowerApps-sovellus vetämällä **PowerApps**-kohde muokkausalueelle, anna tehtävän nimi ja kuvaus ja joko valitse PowerApps-sovellus tai anna PowerApps-sovelluksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-169">To add a PowerApps app, drag the **PowerApps** item to the editing area, enter a name and description for the activity, and either select the PowerApps app or enter the PowerApps app ID.</span></span>
    - <span data-ttu-id="b1a7d-170">Lisää Microsoft Stream -video vetämällä **Microsoft Stream** -kohde muokkausalueelle, anna tehtävälle nimi ja kuvaus ja anna Microsoft Stream -videon URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="b1a7d-171">Lisää Microsoft Forms -lomake vetämällä **Microsoft Forms** -kohde muokkausalueelle, anna tehtävän nimi ja kuvaus, anna Microsoft Forms -lomakkeen URL-osoite ja määritä näyttöalueen koko.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="b1a7d-172">Lisää verkkosisältöä sisältävä iframe vetämällä **Internet-sisältö (iframe)** -kohde muokkausalueelle, anna tehtävän nimi ja kuvaus, anna verkkosisällön URL-osoite ja määritä näyttöalueen koko.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="b1a7d-173">Monipuolisen sisällön lisääminen perehdytysoppaaseen tai malliin</span><span class="sxs-lookup"><span data-stu-id="b1a7d-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-add-rieha-Content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="b1a7d-174">Valinnainen: määritä kunkin tehtävän oikealla puolella olevalla alueella tehtävä tietylle henkilölle tai tiettyyn rooliin, lisää määräpäivä ja yhteyshenkilö ja määritä luokan väri.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="b1a7d-175">Kun määrität tehtävän henkilölle tai rooliin, tehtävä luodaan kullekin henkilölle.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="b1a7d-176">Tämä tehtävä näkyy Onboardin **tehtävät**-valikossa.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="b1a7d-177">[![Tehtävän määrittäminen perehdytysoppaassa tai mallissa](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="b1a7d-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="b1a7d-178">Tallenna työsi valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="b1a7d-179">Poista tehtävä tai osa valitsemalla **Poista**-painike (roskakorisymboli) tehtävän tai osan oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="b1a7d-180">Muuta tehtävien tai osien järjestystä vetämällä ne uuteen sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="b1a7d-181">Yhteyshenkilöiden lisääminen tai muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="b1a7d-181">Add or edit contacts</span></span>

<span data-ttu-id="b1a7d-182">Voit lisätä yhteyshenkilöitä, jotka voivat auttaa uutta työntekijää menestymään ensimmäistä työpäivästä alkaen.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="b1a7d-183">Nämä yhteyshenkilöt voivat olla työhönottajia, ryhmän jäseniä, perehdyttäjiä, mentoreita, järjestelmänvalvojia ja IT-tuen henkilöitä.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="b1a7d-184">Valitse **Yhteyshenkilöt**-välilehdessä **Uusi yhteyshenkilö**.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="b1a7d-185">Anna **Lisää ryhmän jäsen** -valintaikkunassa yhteyshenkilön nimi tai sähköpostiosoite, lisää sitten lyhyt kuvaus, joka selittää, miten yhteyshenkilö voi auttaa uutta työntekijää, ja valitse lopuksi **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="b1a7d-186">Yhteyshenkilöiden sisällön lisääminen perehdytysoppaaseen tai malliin</span><span class="sxs-lookup"><span data-stu-id="b1a7d-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="b1a7d-187">Vaihtoehtoisesti voit valita vähintään yhden yhteyshenkilön **Ehdotukset**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="b1a7d-188">Tallenna työsi valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="b1a7d-189">Poista yhteyshenkilö valitsemalla **Poista**-painike (roskakorisymboli) yhteyshenkilön oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="b1a7d-190">Muokkaa yhteyshenkilöä valitsemalla **Muokkaa**-painike (kynäsymboli) yhteyshenkilön oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="b1a7d-191">Resurssien lisääminen tai muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="b1a7d-191">Add or edit resources</span></span>

<span data-ttu-id="b1a7d-192">Voit lisätä hyödyllisiä tiedostoja, karttoja ja linkkejä perehdytysoppaan **Resurssit**-osaan.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="b1a7d-193">Valitse **Resurssit**-välilehdessä **Uusi resurssi**.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="b1a7d-194">Noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="b1a7d-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="b1a7d-195">Lisää tiedosto valitsemalla **Tiedosto**-välilehti ja vetämällä tiedosto määritetylle alueelle.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="b1a7d-196">(Vaihtoehtoisesti voit napsauttaa kyseistä aluetta ja siirtymällä tiedostoon tietokoneessa tai valitse **Selaa OneDrive**.) Anna tiedostolle nimi ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="b1a7d-197">Lisää linkki valitsemalla **Linkki**-välilehti, anna linkille nimi ja osoite ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="b1a7d-198">Lisää kartta valitsemalla **Kartta**-välilehti, anna kartta nimi ja osoite ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="b1a7d-199">Onboard sisällyttää määritetyn osoitteen kartan.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="b1a7d-200">Resurssin lisääminen perehdytysoppaaseen tai malliin</span><span class="sxs-lookup"><span data-stu-id="b1a7d-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="b1a7d-201">Tallenna työsi valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="b1a7d-202">Poista resurssi valitsemalla **Poista**-painike (roskakorisymboli) resurssin oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="b1a7d-203">Muokkaa yhteyshenkilöä valitsemalla **Muokkaa**-painike (kynäsymboli) resurssin oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="b1a7d-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b1a7d-204">Seuraavat vaiheet</span><span class="sxs-lookup"><span data-stu-id="b1a7d-204">Next steps</span></span>

- [<span data-ttu-id="b1a7d-205">Sisällön jakaminen muiden osallisten kanssa</span><span class="sxs-lookup"><span data-stu-id="b1a7d-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="b1a7d-206">Työntekijöiden tehtävien ja perehdyttämisen tilan näyttäminen</span><span class="sxs-lookup"><span data-stu-id="b1a7d-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="b1a7d-207">Työhönottoryhmien luominen Onboardissa</span><span class="sxs-lookup"><span data-stu-id="b1a7d-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="b1a7d-208">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="b1a7d-208">See also</span></span>

- [<span data-ttu-id="b1a7d-209">Onboard-sovelluksen kokeileminen tai ostaminen</span><span class="sxs-lookup"><span data-stu-id="b1a7d-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="b1a7d-210">Uutta</span><span class="sxs-lookup"><span data-stu-id="b1a7d-210">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="b1a7d-211">Julkaisutiedot</span><span class="sxs-lookup"><span data-stu-id="b1a7d-211">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="b1a7d-212">Tuen saaminen</span><span class="sxs-lookup"><span data-stu-id="b1a7d-212">Get support</span></span>](./talent-support.md)
