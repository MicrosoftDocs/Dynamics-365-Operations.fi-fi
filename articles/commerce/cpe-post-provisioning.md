---
title: Dynamics 365 Commercen esikatseluympäristön määrittäminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää Microsoft Dynamics 365 Commercen esikatseluympäristön, kun se on valmisteltu.
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.openlocfilehash: d72caee25c03e8167b94dd387c7861f98bd0f4cb
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057714"
---
# <a name="configure-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="09cd8-103">Dynamics 365 Commercen esikatseluympäristön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="09cd8-103">Configure a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="09cd8-104">Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää Microsoft Dynamics 365 Commercen esikatseluympäristön, kun se on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="09cd8-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="09cd8-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="09cd8-105">Overview</span></span>

<span data-ttu-id="09cd8-106">Suorita tämän ohjeaiheen toimet vasta, kun Commercen esikatseluympäristö on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="09cd8-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="09cd8-107">Katso lisätietoja Commercen esikatseluympäristön valmistelusta kohdasta [Commercen esikatseluympäristön valmisteleminen](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="09cd8-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="09cd8-108">Kun Commercen esikatseluympäristö on valmisteltu loppuun, lisävalmistelun jälkeiset määritysvaiheet on suoritettava, ennen kuin voit aloittaa ympäristön arvioinnin.</span><span class="sxs-lookup"><span data-stu-id="09cd8-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="09cd8-109">Näiden vaiheiden suorittaminen edellyttää, että käytössä ovat Microsoft Dynamics Lifecycle Services (LCS) ja Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="09cd8-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="09cd8-110">Ennen aloittamista</span><span class="sxs-lookup"><span data-stu-id="09cd8-110">Before you start</span></span>

1. <span data-ttu-id="09cd8-111">Kirjaudu [LSC-portaaliin](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="09cd8-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="09cd8-112">Siirry projektiisi.</span><span class="sxs-lookup"><span data-stu-id="09cd8-112">Go to your project.</span></span>
1. <span data-ttu-id="09cd8-113">Valitse päävalikosta **Pilvipalveluympäristöt**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="09cd8-114">Valitse ympäristö luettelosta.</span><span class="sxs-lookup"><span data-stu-id="09cd8-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="09cd8-115">Valitse oikealla olevista ympäristön tiedoista **Täydet tiedot**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="09cd8-116">Valitse **Kirjaudu sisään** avataksesi valikon ja valitse sitten **Kirjaudu ympäristöön**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="09cd8-117">Varmista, että valittuna on **USRT**-yritys oikealla yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="09cd8-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="09cd8-118">Määritä myyntipiste LCS:ssä</span><span class="sxs-lookup"><span data-stu-id="09cd8-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="09cd8-119">Työntekijän liittäminen tunnukseen</span><span class="sxs-lookup"><span data-stu-id="09cd8-119">Associate a worker with your identity</span></span>

<span data-ttu-id="09cd8-120">Voit liittää työntekijän identiteettisi LCS:iin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="09cd8-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="09cd8-121">Valitse vasemmalla olevasta valikosta **Moduulit \> Vähittäismyynti ja kauppa \> Työntekijät \> Työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="09cd8-122">Etsi ja valitse luettelosta seuraava tietue: **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="09cd8-123">Valitse toimintoruudussa **Vähittäismyynti**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="09cd8-124">Valitse **Liitä aiemmin luotu tunnus**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="09cd8-125">Syötä **Sähköposti**-kenttään **Hae sähköpostiosoitteen avulla** -kohdan oikealla puolelle sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="09cd8-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="09cd8-126">Valitse **Haku**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-126">Select **Search**.</span></span>
1. <span data-ttu-id="09cd8-127">Valitse tietue, joka sisältää nimesi.</span><span class="sxs-lookup"><span data-stu-id="09cd8-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="09cd8-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-128">Select **OK**.</span></span>
1. <span data-ttu-id="09cd8-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="09cd8-130">Pilvipalvelun myyntipisteen aktivoiminen</span><span class="sxs-lookup"><span data-stu-id="09cd8-130">Activate Cloud POS</span></span>

<span data-ttu-id="09cd8-131">Jos haluat aktivoida pilvimyyntipisteen LCS:ssä, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="09cd8-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="09cd8-132">Valitse päävalikosta **Pilvipalveluympäristöt**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="09cd8-133">Valitse ympäristö luettelosta.</span><span class="sxs-lookup"><span data-stu-id="09cd8-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="09cd8-134">Valitse oikealla olevista ympäristön tiedoista **Täydet tiedot**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="09cd8-135">Avaa valikko valitsemalla **Kirjaudu** ja avaa sitten myyntipiste (POS) valitsemalla **Kirjaudu pilvimyyntipisteeseen**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="09cd8-136">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-136">Select **Next**.</span></span>
1. <span data-ttu-id="09cd8-137">Kirjaudu sisään käyttämällä Microsoft Azure Active Directory (Azure AD) -tiliäsi.</span><span class="sxs-lookup"><span data-stu-id="09cd8-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="09cd8-138">Valitse **Myymälän nimi** -kohdassa **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="09cd8-139">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-139">Select **Next**.</span></span>
1. <span data-ttu-id="09cd8-140">Valitse **Kassakone ja laite** -kohdassa **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="09cd8-141">Valitse **Aktivoi**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-141">Select **Activate**.</span></span> <span data-ttu-id="09cd8-142">Olet kirjautunut ulos ja sinut on ohjattu POS-kirjautumissivulle.</span><span class="sxs-lookup"><span data-stu-id="09cd8-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="09cd8-143">Voit nyt kirjautua pilvimyyntipistekokemukseen käyttämällä operaattorin tunnusta **000713** ja salasanaa **123**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="09cd8-144">Urasivuston määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="09cd8-144">Set up your site in Commerce</span></span>

<span data-ttu-id="09cd8-145">Voit aloittaa esikatseluruudun määrittämisen Commerce-sivustossa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="09cd8-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="09cd8-146">Kirjaudu sivustonhallintatyökaluun käyttämällä URL-osoitetta, johon olet tehnyt huomautuksen verkkokaupan valmistelusta valmistelun aikana (katso [verkkokaupan alustaminen](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="09cd8-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="09cd8-147">Avaa sivuston asetusvalintaikkuna valitsemalla **Fabrikam**-sivusto.</span><span class="sxs-lookup"><span data-stu-id="09cd8-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="09cd8-148">Valitse verkkotunnus, jonka syötit sähköistä kaupankäyntiä alustettaessa.</span><span class="sxs-lookup"><span data-stu-id="09cd8-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="09cd8-149">Valitse **Fabrikamin laajennettu verkkokauppa** oletuskanavaksi.</span><span class="sxs-lookup"><span data-stu-id="09cd8-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="09cd8-150">(Huomautus: Varmista, että valitset **laajennetun** verkkokaupan.)</span><span class="sxs-lookup"><span data-stu-id="09cd8-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="09cd8-151">Valitse **en-us** oletuskieleksi.</span><span class="sxs-lookup"><span data-stu-id="09cd8-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="09cd8-152">Jätä **polku** -kentän arvo sellaiseksi kuin se on.</span><span class="sxs-lookup"><span data-stu-id="09cd8-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="09cd8-153">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-153">Select **OK**.</span></span> <span data-ttu-id="09cd8-154">Sivuston sivuluettelo tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="09cd8-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="09cd8-155">Töiden ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="09cd8-155">Enable jobs</span></span>

<span data-ttu-id="09cd8-156">Voit ottaa käyttöön työt Commercessa seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="09cd8-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="09cd8-157">Kirjaudu sisään ympäristöön (pääkonttori).</span><span class="sxs-lookup"><span data-stu-id="09cd8-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="09cd8-158">Siirry vasemmalla olevan valikon avulla kohtaan **Vähittäismyynti ja kauppa \> Kyselyt ja raportit \> Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="09cd8-159">Tämän menettelyn jäljellä olevat vaiheet on täytettävä kunkin seuraavan työn osalta:</span><span class="sxs-lookup"><span data-stu-id="09cd8-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="09cd8-160">Vähittäismyyntitilauksen sähköposti-ilmoituksen käsittely</span><span class="sxs-lookup"><span data-stu-id="09cd8-160">Process retail order email notification</span></span>
    * <span data-ttu-id="09cd8-161">Tuotteen saatavuus</span><span class="sxs-lookup"><span data-stu-id="09cd8-161">Product availability</span></span>
    * <span data-ttu-id="09cd8-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="09cd8-162">P-0001</span></span>
    * <span data-ttu-id="09cd8-163">Synkronoi tilaukset -työ</span><span class="sxs-lookup"><span data-stu-id="09cd8-163">Synchronize orders job</span></span>

1. <span data-ttu-id="09cd8-164">Hae työ pikasuodattimen avulla nimen perusteella.</span><span class="sxs-lookup"><span data-stu-id="09cd8-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="09cd8-165">Jos työn tila on **Pidätä**, seuraa näitä vaiheita:</span><span class="sxs-lookup"><span data-stu-id="09cd8-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="09cd8-166">Valitse tietue.</span><span class="sxs-lookup"><span data-stu-id="09cd8-166">Select the record.</span></span>
    1. <span data-ttu-id="09cd8-167">Valitse toimintoruudussa **Erätyö**-välilehdellä **Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="09cd8-168">Valitse **Odottaa** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="09cd8-169">Suorita täydellinen tietojen synkronointi</span><span class="sxs-lookup"><span data-stu-id="09cd8-169">Run full data synchronization</span></span>

<span data-ttu-id="09cd8-170">Jos haluat suorittaa täyden tietojen synkronoinnin Commercessa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="09cd8-170">To run full data synchronization in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="09cd8-171">Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Headquarters-asetukset \> Retail-ajastus \> Kanavan tietokanta**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-171">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="09cd8-172">Vasemmalla olevasta luettelosta valitaan **oletuskanava**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="09cd8-173">Valitse toinen käytettävissä oleva kanava.</span><span class="sxs-lookup"><span data-stu-id="09cd8-173">Select the other available channel.</span></span> <span data-ttu-id="09cd8-174">Tämä kanava on nimeltään **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="09cd8-175">Valitse toimintoruudusta **Tietojen täydellinen synkronointi**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="09cd8-176">Syötä jakeluaikatauluksi **9999**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="09cd8-177">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-177">Select **OK**.</span></span>
1. <span data-ttu-id="09cd8-178">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="09cd8-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="09cd8-179">Luottokortin testitiedot testiostojen tekemistä varten</span><span class="sxs-lookup"><span data-stu-id="09cd8-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="09cd8-180">Voit käyttää seuraavia luottokortin testitietoja sivuston testitapahtumien suorittamisessa:</span><span class="sxs-lookup"><span data-stu-id="09cd8-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="09cd8-181">**Kortin numero:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="09cd8-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="09cd8-182">**Vanhentumispäivä:** 10/20</span><span class="sxs-lookup"><span data-stu-id="09cd8-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="09cd8-183">**Kortin tarkistusnumero (CVV) -koodi:** 737</span><span class="sxs-lookup"><span data-stu-id="09cd8-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09cd8-184">Älä milloinkaan, missään tapauksessa yritä käyttää testisivustossa todellisia luottokortin tietoja.</span><span class="sxs-lookup"><span data-stu-id="09cd8-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="09cd8-185">Seuraavat vaiheet</span><span class="sxs-lookup"><span data-stu-id="09cd8-185">Next steps</span></span>

<span data-ttu-id="09cd8-186">Kun valmistelu- ja konfigurointivaiheet on suoritettu, olet valmis arvioimaan esikatseluympäristön.</span><span class="sxs-lookup"><span data-stu-id="09cd8-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="09cd8-187">Siirry sisällönluontikokemukseen Commercen sivustonhallintatyökalun URL-osoitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="09cd8-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="09cd8-188">Siirry Retail-asiakassivustokokemukseen Commercen sivuston URL-osoitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="09cd8-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="09cd8-189">Jos haluat määrittää valinnaiset ominaisuudet Commercen esikatseluympäristöön, katso [Lisäominaisuuksien määrittäminen Commercen esikatseluympäristöä varten](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="09cd8-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09cd8-190">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="09cd8-190">Additional resources</span></span>

[<span data-ttu-id="09cd8-191">Dynamics 365 Commercen esikatseluympäristön yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="09cd8-191">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="09cd8-192">Dynamics 365 Commercen esiversioympäristön valmistelu</span><span class="sxs-lookup"><span data-stu-id="09cd8-192">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="09cd8-193">Valinnaisten ominaisuuksien määrittäminen Dynamics 365 Commercen esikatseluympäristöä varten</span><span class="sxs-lookup"><span data-stu-id="09cd8-193">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="09cd8-194">Dynamics 365 Commerce -esikatseluympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="09cd8-194">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="09cd8-195">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="09cd8-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="09cd8-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="09cd8-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="09cd8-197">Microsoft Azure -portaali</span><span class="sxs-lookup"><span data-stu-id="09cd8-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="09cd8-198">Dynamics 365 Commerce -sivusto</span><span class="sxs-lookup"><span data-stu-id="09cd8-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
