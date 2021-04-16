---
title: Dynamics 365 Commerce -arviointiympäristön määritykset
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää Microsoft Dynamics 365 Commercen arviointiympäristön, kun se on valmisteltu.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e80830a1cb0864c7eef19857b91e36ad27cdef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795856"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="304ce-103">Dynamics 365 Commerce -arviointiympäristön määritykset</span><span class="sxs-lookup"><span data-stu-id="304ce-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="304ce-104">Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää Microsoft Dynamics 365 Commercen arviointiympäristön, kun se on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="304ce-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

<span data-ttu-id="304ce-105">Suorita tämän ohjeaiheen toimet vasta, kun Commercen arviointiympäristö on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="304ce-105">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="304ce-106">Lisätietoja Commercen arviointiympäristön valmistelusta on kohdasta [Commercen arviointiympäristön valmisteleminen](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="304ce-106">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="304ce-107">Kun Commercen arviointiympäristö on valmisteltu kokonaisuudessaan, valmistelun jälkeiset lisämääritysvaiheet on suoritettava, ennen kuin voit aloittaa ympäristön arvioinnin.</span><span class="sxs-lookup"><span data-stu-id="304ce-107">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="304ce-108">Näiden vaiheiden suorittaminen edellyttää, että käytössä ovat Microsoft Dynamics Lifecycle Services (LCS) ja Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="304ce-108">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="304ce-109">Ennen aloittamista</span><span class="sxs-lookup"><span data-stu-id="304ce-109">Before you start</span></span>

1. <span data-ttu-id="304ce-110">Kirjaudu [LSC-portaaliin](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="304ce-110">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="304ce-111">Siirry projektiisi.</span><span class="sxs-lookup"><span data-stu-id="304ce-111">Go to your project.</span></span>
1. <span data-ttu-id="304ce-112">Valitse päävalikosta **Pilvipalveluympäristöt**.</span><span class="sxs-lookup"><span data-stu-id="304ce-112">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="304ce-113">Valitse ympäristö luettelosta.</span><span class="sxs-lookup"><span data-stu-id="304ce-113">Select your environment in the list.</span></span>
1. <span data-ttu-id="304ce-114">Valitse oikealla ympäristön tiedoista **Kirjaudu ympäristöön**.</span><span class="sxs-lookup"><span data-stu-id="304ce-114">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="304ce-115">Siirryt Commercen pääkonttorisovellukseen.</span><span class="sxs-lookup"><span data-stu-id="304ce-115">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="304ce-116">Varmista, että valittuna on **USRT**-yritys oikealla yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="304ce-116">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="304ce-117">Varmista Commercen pääkonttorissa tehtävien valmistelun jälkeisten toimintojen aikana, että **USRT**-yritys on koko ajan valittuna.</span><span class="sxs-lookup"><span data-stu-id="304ce-117">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="304ce-118">Myyntipisteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="304ce-118">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="304ce-119">Työntekijän liittäminen tunnukseen</span><span class="sxs-lookup"><span data-stu-id="304ce-119">Associate a worker with your identity</span></span>

<span data-ttu-id="304ce-120">Voit liittää työntekijän käyttäjätietoihin seuraavien ohjeiden avulla Commercen pääkonttorissa.</span><span class="sxs-lookup"><span data-stu-id="304ce-120">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="304ce-121">Valitse vasemmalla olevasta valikosta **Moduulit \> Vähittäismyynti ja kauppa \> Työntekijät \> Työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="304ce-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="304ce-122">Etsi ja valitse luettelosta seuraava tietue: **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="304ce-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="304ce-123">Valitse toimintoruudussa **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="304ce-123">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="304ce-124">Valitse **Liitä aiemmin luotu tunnus**.</span><span class="sxs-lookup"><span data-stu-id="304ce-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="304ce-125">Syötä **Sähköposti**-kenttään **Hae sähköpostiosoitteen avulla** -kohdan oikealla puolelle sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="304ce-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="304ce-126">Valitse **Haku**.</span><span class="sxs-lookup"><span data-stu-id="304ce-126">Select **Search**.</span></span>
1. <span data-ttu-id="304ce-127">Valitse tietue, joka sisältää nimesi.</span><span class="sxs-lookup"><span data-stu-id="304ce-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="304ce-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="304ce-128">Select **OK**.</span></span>
1. <span data-ttu-id="304ce-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="304ce-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="304ce-130">Pilvipalvelun myyntipisteen aktivoiminen</span><span class="sxs-lookup"><span data-stu-id="304ce-130">Activate Cloud POS</span></span>

<span data-ttu-id="304ce-131">Jos haluat aktivoida pilvimyyntipisteen LCS:ssä, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="304ce-131">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="304ce-132">Valitse päävalikosta **Pilvipalveluympäristöt**.</span><span class="sxs-lookup"><span data-stu-id="304ce-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="304ce-133">Valitse ympäristö luettelosta.</span><span class="sxs-lookup"><span data-stu-id="304ce-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="304ce-134">Valitse oikealla ympäristön tiedoista **Kirjaudu pilvimyyntipisteeseen**.</span><span class="sxs-lookup"><span data-stu-id="304ce-134">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="304ce-135">Avaa **Ennen aloittamista** -valintaikkunassa **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="304ce-135">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="304ce-136">Älä tee muutoksia **Palvelimen URL-osoite** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="304ce-136">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="304ce-137">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="304ce-137">Select **Next**.</span></span>
1. <span data-ttu-id="304ce-138">Kirjaudu sisään käyttämällä Microsoft Azure Active Directory (Azure AD) -tiliäsi.</span><span class="sxs-lookup"><span data-stu-id="304ce-138">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="304ce-139">Valitse **Myymälän nimi** -kentässä **San Francisco** ja valitse sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="304ce-139">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="304ce-140">Valitse **Kassakone ja laite** -kohdassa **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="304ce-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="304ce-141">Valitse **Aktivoi**.</span><span class="sxs-lookup"><span data-stu-id="304ce-141">Select **Activate**.</span></span> <span data-ttu-id="304ce-142">Olet kirjautunut ulos ja sinut on ohjattu POS-kirjautumissivulle.</span><span class="sxs-lookup"><span data-stu-id="304ce-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="304ce-143">Voit nyt kirjautua pilvimyyntipistekokemukseen käyttämällä operaattorin tunnusta **000713** ja salasanaa **123**.</span><span class="sxs-lookup"><span data-stu-id="304ce-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="304ce-144">Urasivuston määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="304ce-144">Set up your site in Commerce</span></span>

<span data-ttu-id="304ce-145">Voit aloittaa arviointisivuston määrittämisen Commercessa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="304ce-145">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="304ce-146">Kirjaudu sivustonmuodostimeen käyttämällä URL-osoitetta, josta kirjoitit muistiin sähköisen kaupankäyntiä alustettaessa valmistelun aikana (katso [Sähköisen kaupankäynnin alustaminen](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="304ce-146">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="304ce-147">Avaa sivuston asetusvalintaikkuna valitsemalla **Fabrikam**-sivusto.</span><span class="sxs-lookup"><span data-stu-id="304ce-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="304ce-148">Valitse verkkotunnus, jonka syötit sähköistä kaupankäyntiä alustettaessa.</span><span class="sxs-lookup"><span data-stu-id="304ce-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="304ce-149">Valitse **Fabrikamin laajennettu verkkokauppa** oletuskanavaksi.</span><span class="sxs-lookup"><span data-stu-id="304ce-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="304ce-150">(Huomautus: Varmista, että valitset **laajennetun** verkkokaupan.)</span><span class="sxs-lookup"><span data-stu-id="304ce-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="304ce-151">Valitse **en-us** oletuskieleksi.</span><span class="sxs-lookup"><span data-stu-id="304ce-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="304ce-152">Jätä **polku** -kentän arvo sellaiseksi kuin se on.</span><span class="sxs-lookup"><span data-stu-id="304ce-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="304ce-153">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="304ce-153">Select **OK**.</span></span> <span data-ttu-id="304ce-154">Sivuston sivuluettelo tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="304ce-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="304ce-155">Töiden ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="304ce-155">Enable jobs</span></span>

<span data-ttu-id="304ce-156">Voit ottaa käyttöön työt Commercessa seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="304ce-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="304ce-157">Kirjaudu sisään ympäristöön (pääkonttori).</span><span class="sxs-lookup"><span data-stu-id="304ce-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="304ce-158">Siirry vasemmalla olevan valikon avulla kohtaan **Vähittäismyynti ja kauppa \> Kyselyt ja raportit \> Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="304ce-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="304ce-159">Tämän menettelyn jäljellä olevat vaiheet on täytettävä kunkin seuraavan työn osalta:</span><span class="sxs-lookup"><span data-stu-id="304ce-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="304ce-160">Vähittäismyyntitilauksen sähköposti-ilmoituksen käsittely</span><span class="sxs-lookup"><span data-stu-id="304ce-160">Process retail order email notification</span></span>
    * <span data-ttu-id="304ce-161">Tuotteen saatavuus</span><span class="sxs-lookup"><span data-stu-id="304ce-161">Product availability</span></span>
    * <span data-ttu-id="304ce-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="304ce-162">P-0001</span></span>
    * <span data-ttu-id="304ce-163">Synkronoi tilaukset -työ</span><span class="sxs-lookup"><span data-stu-id="304ce-163">Synchronize orders job</span></span>

1. <span data-ttu-id="304ce-164">Hae työ pikasuodattimen avulla nimen perusteella.</span><span class="sxs-lookup"><span data-stu-id="304ce-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="304ce-165">Jos työn tila on **Suoritetaan**, toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="304ce-165">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="304ce-166">Valitse tietue.</span><span class="sxs-lookup"><span data-stu-id="304ce-166">Select the record.</span></span>
    1. <span data-ttu-id="304ce-167">Valitse toimintoruudussa **Erätyö**-välilehdellä **Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="304ce-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="304ce-168">Valitse ensin **Peruuttaminen** ja sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="304ce-168">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="304ce-169">Vaihtoehtoisesti voit määrittää toistuvuusvälin yhteen (1) minuuttiin seuraavissa töissä:</span><span class="sxs-lookup"><span data-stu-id="304ce-169">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="304ce-170">Vähittäismyyntitilauksen sähköposti-ilmoitustyön käsittely</span><span class="sxs-lookup"><span data-stu-id="304ce-170">Process retail order email notification job</span></span>
* <span data-ttu-id="304ce-171">P-0001 työ</span><span class="sxs-lookup"><span data-stu-id="304ce-171">P-0001 job</span></span>
* <span data-ttu-id="304ce-172">Synkronoi tilaukset -työ</span><span class="sxs-lookup"><span data-stu-id="304ce-172">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="304ce-173">Suorita täydellinen tietojen synkronointi</span><span class="sxs-lookup"><span data-stu-id="304ce-173">Run full data synchronization</span></span>

<span data-ttu-id="304ce-174">Suorita täydellinen tietojen synkronointi Commercessa, toimi seuraavasti Commercen pääkonttorissa.</span><span class="sxs-lookup"><span data-stu-id="304ce-174">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="304ce-175">Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Headquarters-asetukset \> Commerce-ajastus \> Kanavan tietokanta**.</span><span class="sxs-lookup"><span data-stu-id="304ce-175">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="304ce-176">Valitse kanava, jonka nimi on **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="304ce-176">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="304ce-177">Valitse toimintoruudusta **Tietojen täydellinen synkronointi**.</span><span class="sxs-lookup"><span data-stu-id="304ce-177">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="304ce-178">Syötä jakeluaikatauluksi **9999**.</span><span class="sxs-lookup"><span data-stu-id="304ce-178">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="304ce-179">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="304ce-179">Select **OK**.</span></span>
1. <span data-ttu-id="304ce-180">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="304ce-180">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="304ce-181">Luottokortin testitiedot testiostojen tekemistä varten</span><span class="sxs-lookup"><span data-stu-id="304ce-181">Test credit card information to do test purchases</span></span>

<span data-ttu-id="304ce-182">Voit käyttää seuraavia luottokortin testitietoja sivuston testitapahtumien suorittamisessa:</span><span class="sxs-lookup"><span data-stu-id="304ce-182">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="304ce-183">**Kortin numero:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="304ce-183">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="304ce-184">**Vanhentumispäivä:** 10/20</span><span class="sxs-lookup"><span data-stu-id="304ce-184">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="304ce-185">**Kortin tarkistusnumero (CVV) -koodi:** 737</span><span class="sxs-lookup"><span data-stu-id="304ce-185">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="304ce-186">Älä milloinkaan, missään tapauksessa yritä käyttää testisivustossa todellisia luottokortin tietoja.</span><span class="sxs-lookup"><span data-stu-id="304ce-186">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="304ce-187">Seuraavat vaiheet</span><span class="sxs-lookup"><span data-stu-id="304ce-187">Next steps</span></span>

<span data-ttu-id="304ce-188">Kun valmistelu- ja määritysvaiheet on suoritettu, voit aloittaa arviointiympäristön käytön.</span><span class="sxs-lookup"><span data-stu-id="304ce-188">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="304ce-189">Siirry sisällönluontikokemukseen Commercen sivustonmuodostimen URL-osoitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="304ce-189">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="304ce-190">Siirry vähittäismyynnin asiakassivustokokemukseen Commercen sivuston URL-osoitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="304ce-190">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="304ce-191">Lisätietoja Commercen arviointiympäristön valinnaisten ominaisuuksien määrittämisestä on kohdassa [Commercen arviointiympäristön valinnaisten ominaisuuksien määrittäminen](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="304ce-191">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="304ce-192">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="304ce-192">Additional resources</span></span>

[<span data-ttu-id="304ce-193">Dynamics 365 Commerce -arviointiympäristön yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="304ce-193">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="304ce-194">Dynamics 365 Commerce -arviointiympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="304ce-194">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="304ce-195">Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset</span><span class="sxs-lookup"><span data-stu-id="304ce-195">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="304ce-196">BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä</span><span class="sxs-lookup"><span data-stu-id="304ce-196">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="304ce-197">Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="304ce-197">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="304ce-198">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="304ce-198">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="304ce-199">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="304ce-199">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="304ce-200">Microsoft Azure -portaali</span><span class="sxs-lookup"><span data-stu-id="304ce-200">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="304ce-201">Dynamics 365 Commerce -sivusto</span><span class="sxs-lookup"><span data-stu-id="304ce-201">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
