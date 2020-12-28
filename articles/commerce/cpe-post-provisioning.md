---
title: Dynamics 365 Commerce -arviointiympäristön määritykset
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää Microsoft Dynamics 365 Commercen arviointiympäristön, kun se on valmisteltu.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6a1ae960f0f530104af7bdea9a8fcb78b01571f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411864"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="e9ad2-103">Dynamics 365 Commerce -arviointiympäristön määritykset</span><span class="sxs-lookup"><span data-stu-id="e9ad2-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e9ad2-104">Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää Microsoft Dynamics 365 Commercen arviointiympäristön, kun se on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="e9ad2-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="e9ad2-105">Overview</span></span>

<span data-ttu-id="e9ad2-106">Suorita tämän ohjeaiheen toimet vasta, kun Commercen arviointiympäristö on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="e9ad2-107">Lisätietoja Commercen arviointiympäristön valmistelusta on kohdasta [Commercen arviointiympäristön valmisteleminen](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="e9ad2-107">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="e9ad2-108">Kun Commercen arviointiympäristö on valmisteltu kokonaisuudessaan, valmistelun jälkeiset lisämääritysvaiheet on suoritettava, ennen kuin voit aloittaa ympäristön arvioinnin.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-108">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="e9ad2-109">Näiden vaiheiden suorittaminen edellyttää, että käytössä ovat Microsoft Dynamics Lifecycle Services (LCS) ja Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="e9ad2-110">Ennen aloittamista</span><span class="sxs-lookup"><span data-stu-id="e9ad2-110">Before you start</span></span>

1. <span data-ttu-id="e9ad2-111">Kirjaudu [LSC-portaaliin](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="e9ad2-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="e9ad2-112">Siirry projektiisi.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-112">Go to your project.</span></span>
1. <span data-ttu-id="e9ad2-113">Valitse päävalikosta **Pilvipalveluympäristöt**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="e9ad2-114">Valitse ympäristö luettelosta.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="e9ad2-115">Valitse oikealla ympäristön tiedoista **Kirjaudu ympäristöön**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-115">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="e9ad2-116">Siirryt Commercen pääkonttorisovellukseen.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-116">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="e9ad2-117">Varmista, että valittuna on **USRT**-yritys oikealla yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="e9ad2-118">Varmista Commercen pääkonttorissa tehtävien valmistelun jälkeisten toimintojen aikana, että **USRT**-yritys on koko ajan valittuna.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-118">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="e9ad2-119">Myyntipisteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e9ad2-119">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="e9ad2-120">Työntekijän liittäminen tunnukseen</span><span class="sxs-lookup"><span data-stu-id="e9ad2-120">Associate a worker with your identity</span></span>

<span data-ttu-id="e9ad2-121">Voit liittää työntekijän käyttäjätietoihin seuraavien ohjeiden avulla Commercen pääkonttorissa.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-121">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="e9ad2-122">Valitse vasemmalla olevasta valikosta **Moduulit \> Vähittäismyynti ja kauppa \> Työntekijät \> Työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-122">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="e9ad2-123">Etsi ja valitse luettelosta seuraava tietue: **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-123">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="e9ad2-124">Valitse toimintoruudussa **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-124">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="e9ad2-125">Valitse **Liitä aiemmin luotu tunnus**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-125">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="e9ad2-126">Syötä **Sähköposti**-kenttään **Hae sähköpostiosoitteen avulla** -kohdan oikealla puolelle sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-126">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="e9ad2-127">Valitse **Haku**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-127">Select **Search**.</span></span>
1. <span data-ttu-id="e9ad2-128">Valitse tietue, joka sisältää nimesi.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-128">Select the record that has your name.</span></span>
1. <span data-ttu-id="e9ad2-129">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-129">Select **OK**.</span></span>
1. <span data-ttu-id="e9ad2-130">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-130">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="e9ad2-131">Pilvipalvelun myyntipisteen aktivoiminen</span><span class="sxs-lookup"><span data-stu-id="e9ad2-131">Activate Cloud POS</span></span>

<span data-ttu-id="e9ad2-132">Jos haluat aktivoida pilvimyyntipisteen LCS:ssä, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-132">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="e9ad2-133">Valitse päävalikosta **Pilvipalveluympäristöt**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-133">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="e9ad2-134">Valitse ympäristö luettelosta.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-134">Select your environment in the list.</span></span>
1. <span data-ttu-id="e9ad2-135">Valitse oikealla ympäristön tiedoista **Kirjaudu pilvimyyntipisteeseen**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-135">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="e9ad2-136">Avaa **Ennen aloittamista** -valintaikkunassa **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-136">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="e9ad2-137">Älä tee muutoksia **Palvelimen URL-osoite** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-137">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="e9ad2-138">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-138">Select **Next**.</span></span>
1. <span data-ttu-id="e9ad2-139">Kirjaudu sisään käyttämällä Microsoft Azure Active Directory (Azure AD) -tiliäsi.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-139">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="e9ad2-140">Valitse **Myymälän nimi** -kentässä **San Francisco** ja valitse sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-140">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="e9ad2-141">Valitse **Kassakone ja laite** -kohdassa **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-141">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="e9ad2-142">Valitse **Aktivoi**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-142">Select **Activate**.</span></span> <span data-ttu-id="e9ad2-143">Olet kirjautunut ulos ja sinut on ohjattu POS-kirjautumissivulle.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-143">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="e9ad2-144">Voit nyt kirjautua pilvimyyntipistekokemukseen käyttämällä operaattorin tunnusta **000713** ja salasanaa **123**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-144">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="e9ad2-145">Urasivuston määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="e9ad2-145">Set up your site in Commerce</span></span>

<span data-ttu-id="e9ad2-146">Voit aloittaa arviointisivuston määrittämisen Commercessa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-146">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="e9ad2-147">Kirjaudu sivustonmuodostimeen käyttämällä URL-osoitetta, josta kirjoitit muistiin sähköisen kaupankäyntiä alustettaessa valmistelun aikana (katso [Sähköisen kaupankäynnin alustaminen](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="e9ad2-147">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="e9ad2-148">Avaa sivuston asetusvalintaikkuna valitsemalla **Fabrikam**-sivusto.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-148">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="e9ad2-149">Valitse verkkotunnus, jonka syötit sähköistä kaupankäyntiä alustettaessa.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-149">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="e9ad2-150">Valitse **Fabrikamin laajennettu verkkokauppa** oletuskanavaksi.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-150">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="e9ad2-151">(Huomautus: Varmista, että valitset **laajennetun** verkkokaupan.)</span><span class="sxs-lookup"><span data-stu-id="e9ad2-151">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="e9ad2-152">Valitse **en-us** oletuskieleksi.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-152">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="e9ad2-153">Jätä **polku** -kentän arvo sellaiseksi kuin se on.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-153">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="e9ad2-154">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-154">Select **OK**.</span></span> <span data-ttu-id="e9ad2-155">Sivuston sivuluettelo tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-155">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="e9ad2-156">Töiden ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e9ad2-156">Enable jobs</span></span>

<span data-ttu-id="e9ad2-157">Voit ottaa käyttöön työt Commercessa seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-157">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="e9ad2-158">Kirjaudu sisään ympäristöön (pääkonttori).</span><span class="sxs-lookup"><span data-stu-id="e9ad2-158">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="e9ad2-159">Siirry vasemmalla olevan valikon avulla kohtaan **Vähittäismyynti ja kauppa \> Kyselyt ja raportit \> Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-159">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="e9ad2-160">Tämän menettelyn jäljellä olevat vaiheet on täytettävä kunkin seuraavan työn osalta:</span><span class="sxs-lookup"><span data-stu-id="e9ad2-160">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="e9ad2-161">Vähittäismyyntitilauksen sähköposti-ilmoituksen käsittely</span><span class="sxs-lookup"><span data-stu-id="e9ad2-161">Process retail order email notification</span></span>
    * <span data-ttu-id="e9ad2-162">Tuotteen saatavuus</span><span class="sxs-lookup"><span data-stu-id="e9ad2-162">Product availability</span></span>
    * <span data-ttu-id="e9ad2-163">P-0001</span><span class="sxs-lookup"><span data-stu-id="e9ad2-163">P-0001</span></span>
    * <span data-ttu-id="e9ad2-164">Synkronoi tilaukset -työ</span><span class="sxs-lookup"><span data-stu-id="e9ad2-164">Synchronize orders job</span></span>

1. <span data-ttu-id="e9ad2-165">Hae työ pikasuodattimen avulla nimen perusteella.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-165">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="e9ad2-166">Jos työn tila on **Suoritetaan**, toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e9ad2-166">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="e9ad2-167">Valitse tietue.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-167">Select the record.</span></span>
    1. <span data-ttu-id="e9ad2-168">Valitse toimintoruudussa **Erätyö**-välilehdellä **Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-168">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="e9ad2-169">Valitse ensin **Peruuttaminen** ja sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-169">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="e9ad2-170">Vaihtoehtoisesti voit määrittää toistuvuusvälin yhteen (1) minuuttiin seuraavissa töissä:</span><span class="sxs-lookup"><span data-stu-id="e9ad2-170">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="e9ad2-171">Vähittäismyyntitilauksen sähköposti-ilmoitustyön käsittely</span><span class="sxs-lookup"><span data-stu-id="e9ad2-171">Process retail order email notification job</span></span>
* <span data-ttu-id="e9ad2-172">P-0001 työ</span><span class="sxs-lookup"><span data-stu-id="e9ad2-172">P-0001 job</span></span>
* <span data-ttu-id="e9ad2-173">Synkronoi tilaukset -työ</span><span class="sxs-lookup"><span data-stu-id="e9ad2-173">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="e9ad2-174">Suorita täydellinen tietojen synkronointi</span><span class="sxs-lookup"><span data-stu-id="e9ad2-174">Run full data synchronization</span></span>

<span data-ttu-id="e9ad2-175">Suorita täydellinen tietojen synkronointi Commercessa, toimi seuraavasti Commercen pääkonttorissa.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-175">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="e9ad2-176">Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Headquarters-asetukset \> Commerce-ajastus \> Kanavan tietokanta**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-176">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="e9ad2-177">Valitse kanava, jonka nimi on **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-177">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="e9ad2-178">Valitse toimintoruudusta **Tietojen täydellinen synkronointi**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-178">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="e9ad2-179">Syötä jakeluaikatauluksi **9999**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-179">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="e9ad2-180">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-180">Select **OK**.</span></span>
1. <span data-ttu-id="e9ad2-181">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-181">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="e9ad2-182">Luottokortin testitiedot testiostojen tekemistä varten</span><span class="sxs-lookup"><span data-stu-id="e9ad2-182">Test credit card information to do test purchases</span></span>

<span data-ttu-id="e9ad2-183">Voit käyttää seuraavia luottokortin testitietoja sivuston testitapahtumien suorittamisessa:</span><span class="sxs-lookup"><span data-stu-id="e9ad2-183">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="e9ad2-184">**Kortin numero:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="e9ad2-184">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="e9ad2-185">**Vanhentumispäivä:** 10/20</span><span class="sxs-lookup"><span data-stu-id="e9ad2-185">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="e9ad2-186">**Kortin tarkistusnumero (CVV) -koodi:** 737</span><span class="sxs-lookup"><span data-stu-id="e9ad2-186">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9ad2-187">Älä milloinkaan, missään tapauksessa yritä käyttää testisivustossa todellisia luottokortin tietoja.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-187">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e9ad2-188">Seuraavat vaiheet</span><span class="sxs-lookup"><span data-stu-id="e9ad2-188">Next steps</span></span>

<span data-ttu-id="e9ad2-189">Kun valmistelu- ja määritysvaiheet on suoritettu, voit aloittaa arviointiympäristön käytön.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-189">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="e9ad2-190">Siirry sisällönluontikokemukseen Commercen sivustonmuodostimen URL-osoitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-190">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="e9ad2-191">Siirry vähittäismyynnin asiakassivustokokemukseen Commercen sivuston URL-osoitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="e9ad2-191">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="e9ad2-192">Lisätietoja Commercen arviointiympäristön valinnaisten ominaisuuksien määrittämisestä on kohdassa [Commercen arviointiympäristön valinnaisten ominaisuuksien määrittäminen](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="e9ad2-192">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9ad2-193">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e9ad2-193">Additional resources</span></span>

[<span data-ttu-id="e9ad2-194">Dynamics 365 Commerce -arviointiympäristön yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="e9ad2-194">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="e9ad2-195">Dynamics 365 Commerce -arviointiympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="e9ad2-195">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="e9ad2-196">Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset</span><span class="sxs-lookup"><span data-stu-id="e9ad2-196">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="e9ad2-197">BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä</span><span class="sxs-lookup"><span data-stu-id="e9ad2-197">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="e9ad2-198">Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="e9ad2-198">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="e9ad2-199">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="e9ad2-199">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="e9ad2-200">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="e9ad2-200">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="e9ad2-201">Microsoft Azure -portaali</span><span class="sxs-lookup"><span data-stu-id="e9ad2-201">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="e9ad2-202">Dynamics 365 Commerce -sivusto</span><span class="sxs-lookup"><span data-stu-id="e9ad2-202">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
