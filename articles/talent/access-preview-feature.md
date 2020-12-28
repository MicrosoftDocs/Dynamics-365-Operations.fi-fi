---
title: Hallitse ominaisuuksia
description: Tässä aiheessa kuvataan, kuinka järjestelmänvalvoja voi ottaa käyttöön esiversio-ominaisuudet Microsoft Dynamics 365 Talentissa. Siinä listataan myös ominaisuudet, jotka ovat tällä hetkellä käytössä esikatselua varten.
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
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461094"
---
# <a name="manage-features"></a><span data-ttu-id="60735-103">Hallitse ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="60735-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="60735-104">Parannamme jatkuvasti henkilöstöresurssien hallinnan (HCM) ominaisuuksia Microsoft Dynamics 365 Human Resourcesissa ja haluamme tarjota ne asiakkaillemme mahdollisimman pian.</span><span class="sxs-lookup"><span data-stu-id="60735-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="60735-105">Järjestelmänvalvojat voivat tarkastella ja käyttää esiversio-ominaisuuksia ympäristöissään.</span><span class="sxs-lookup"><span data-stu-id="60735-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="60735-106">Nämä ominaisuudet ovat lähes valmiita yleiseen käyttöön ja ne ovat läpäisseet laajan testauksen.</span><span class="sxs-lookup"><span data-stu-id="60735-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="60735-107">Haluamme saada vielä viimeisen asiakaspalautekierroksen, ennen kuin hyväksymme ominaisuudet yleisesti saataville.</span><span class="sxs-lookup"><span data-stu-id="60735-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="60735-108">Tässä aiheessa kuvataan, kuinka voit ottaa käyttöön esiversio-ominaisuudet. Siinä listataan myös ominaisuudet, jotka ovat tällä hetkellä saatavilla esikatselua varten.</span><span class="sxs-lookup"><span data-stu-id="60735-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="60735-109">Tätä luetteloa päivitetään sitä mukaa, kun ominaisuuksia julkaistaan yleiseen käyttöön ja uusia ominaisuuksia tuodaan esikatseltavaksi.</span><span class="sxs-lookup"><span data-stu-id="60735-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="60735-110">Erillistä ilmoitusta ei anneta, kun uusia ominaisuuksia julkaistaan esikatseluun.</span><span class="sxs-lookup"><span data-stu-id="60735-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="60735-111">Ominaisuudet tuodaan vain käyttäjien saataville.</span><span class="sxs-lookup"><span data-stu-id="60735-111">Users will just start to see the features.</span></span> <span data-ttu-id="60735-112">Lisätietoja Talentin uusista ominaisuuksista on kohdassa [Uudet tai muuttuneet ominaisuudet Dynamics 365 Talentissa](./whats-new.md)ja [Dynamics 365- ja Power Platform -julkaisutiedot](https://docs.microsoft.com/business-applications-release-notes) -kohdissa.</span><span class="sxs-lookup"><span data-stu-id="60735-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="60735-113">Esiversio-ominaisuuksien ottaminen käyttöön tai poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="60735-113">Enable or disable preview features</span></span>

<span data-ttu-id="60735-114">Jos haluat käyttää esikatselutoimintoja, sinun on ensin otettava ne käyttöön omassa ympäristössäsi.</span><span class="sxs-lookup"><span data-stu-id="60735-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="60735-115">Esiversio-ominaisuuksien käyttöönotto on ympäristökohtainen.</span><span class="sxs-lookup"><span data-stu-id="60735-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60735-116">Kun otat **Esiversio-ominaisuudet**-asetuksen käyttöön sallit esiversio-ominaisuudet organisaation kaikille käyttäjille kyseisessä ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="60735-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="60735-117">Kun poistat asetuksen käytöstä, esiversio-ominaisuudet eivät ole käyttäjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="60735-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="60735-118">Esiversio-ominaisuuksilla on Talentissa rajoitettu tuki.</span><span class="sxs-lookup"><span data-stu-id="60735-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="60735-119">Niissä voi olla tavallista vähemmän tietosuoja- ja suojausominaisuuksia, eivätkä ne sisälly Talentin palvelutasosopimukseen (SLA).</span><span class="sxs-lookup"><span data-stu-id="60735-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="60735-120">Älä käytä esiversio-ominaisuuksia henkilötietojen (eli henkilökohtaisesti tunnistettavien tietojen) käsittelyyn tai muiden sellaisten tietojen käsittelyyn, jotka edellyttävät lain- tai säädöstenmukaista suojelua.</span><span class="sxs-lookup"><span data-stu-id="60735-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="60735-121">Kerätä</span><span class="sxs-lookup"><span data-stu-id="60735-121">Attract</span></span>

1. <span data-ttu-id="60735-122">Kirjaudu Microsoft Dynamics 365 Talent: Attractiin.</span><span class="sxs-lookup"><span data-stu-id="60735-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="60735-123">Valitse **Asetukset**-valikossa (hammasrataskuvake) oikeassa alakulmassa **Hallintakeskus**.</span><span class="sxs-lookup"><span data-stu-id="60735-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="60735-124">Valitse **Ominaisuuksien hallinta** -välilehdestä kohdan **Esiversio-ominaisuudet** vieressä oleva vaihtoehto siten, että se muuttuu siniseksi ja siinä lukee **Päällä**.</span><span class="sxs-lookup"><span data-stu-id="60735-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![Ota esiversio-ominaisuudet käyttöön Attractissa](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="60735-126">Valitse tai Peruuta henkilökohtaisten esikatseluominaisuuksien valinta.</span><span class="sxs-lookup"><span data-stu-id="60735-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="60735-127">Jos et tee mitään, kaikki käytettävissä olevat esikatseluominaisuudet ovat käytössä.</span><span class="sxs-lookup"><span data-stu-id="60735-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="60735-128">Päivitä selaimesi ikkuna nähdäksesi uudet ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="60735-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="60735-129">Käyttäjät, jotka ovat jo kirjautuneet sisään, näkevät ominaisuudet seuraavan sisäänkirjautumiskerran yhteydessä tai päivittäessään selaimen ikkunan.</span><span class="sxs-lookup"><span data-stu-id="60735-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="60735-130">Jotkin esikatseluominaisuudet saattavat edellyttää lisämääritystä.</span><span class="sxs-lookup"><span data-stu-id="60735-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="60735-131">Viimeistele sen määritys seuraamalla esikatselutoiminnon vieressä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="60735-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="60735-132">Palaute</span><span class="sxs-lookup"><span data-stu-id="60735-132">Feedback</span></span>

<span data-ttu-id="60735-133">Haluamme kuulla kokemuksistasi näistä esikatseluominaisuuksista.</span><span class="sxs-lookup"><span data-stu-id="60735-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="60735-134">Kannustamme sinua antamaan säännöllisesti palautetta, kun käytät näitä sivustoja tai muita ominaisuuksia:</span><span class="sxs-lookup"><span data-stu-id="60735-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="60735-135">[Yhteisö](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Tämä sivusto on erinomainen resurssi, jossa käyttäjät voivat keskustella tapauksista, esittää kysymyksiä ja saada ohjeita yhteisöltä.</span><span class="sxs-lookup"><span data-stu-id="60735-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="60735-136">Ilmoita meille, mitä ominaisuuksia haluaisit tuotteeseen ja kerro, mitä muutoksia nykyisiin ominaisuuksiin pitäisi mielestäsi tehdä.</span><span class="sxs-lookup"><span data-stu-id="60735-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="60735-137">Ehdota tuoteideoita seuraavilla sivustoilla:</span><span class="sxs-lookup"><span data-stu-id="60735-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="60735-138">Attract-ideat</span><span class="sxs-lookup"><span data-stu-id="60735-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="60735-139">Onboard-ideat</span><span class="sxs-lookup"><span data-stu-id="60735-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="60735-140">Varmista, että et sisällytä mitään henkilötietoja (eli henkilökohtaisesti tunnistettavia tietoja) palautteeseesi tai tuotearvioihisi.</span><span class="sxs-lookup"><span data-stu-id="60735-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="60735-141">Kerättyjä tietoja voidaan analysoida tarkemmin, eikä niitä käytetä pyyntöihin vastaamiseen tietosuojalakien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="60735-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="60735-142">Henkilökohtaisiin tietoihin, jotka kerätään erillään näistä ohjelmista, sovelletaan [Microsoftin tietosuojalausuntoa](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="60735-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="60735-143">Lisää kirjanmerkki tähän aiheeseen ja käy säännöllisesti katsomassa tietoa uusista julkaistuista esiversio-ominaisuuksista.</span><span class="sxs-lookup"><span data-stu-id="60735-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="60735-144">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="60735-144">See also</span></span>

- [<span data-ttu-id="60735-145">Kokeile tai osta Talent-sovelluksia</span><span class="sxs-lookup"><span data-stu-id="60735-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="60735-146">Dynamics 365 Talentin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="60735-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="60735-147">Julkaisusuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="60735-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="60735-148">Microsoft iDynamics 365 Talentin tuki</span><span class="sxs-lookup"><span data-stu-id="60735-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
