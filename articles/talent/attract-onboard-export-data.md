---
title: Tietojen vienti Attractista ja Onboardista
description: Tietojen vienti Dynamics 365 Talent – Attractista ja Onboardista.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
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
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: acdd93637385246f9c5c652cccdf2cbfb263cc33
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/23/2020
ms.locfileid: "2975931"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="a2aaa-103">Tietojen vienti Attractista ja Onboardista</span><span class="sxs-lookup"><span data-stu-id="a2aaa-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a2aaa-104">Kuten kohdassa [Dynamics 365 Talent: Attract- ja Dynamics 365 Talent: Onboard -sovellusten poistaminen käytöstä](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps) ilmoitettiin, Dynamics 365 Talent: Attract ja Dynamics 365 Talent: Onboard poistetaan käytöstä 1.2.2022.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="a2aaa-105">Kummassakin sovelluksessa on nyt tietojen vientiominaisuus, mikä helpottaa siirtymistä toiseen tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="a2aaa-106">Tietojen vienti Attractista</span><span class="sxs-lookup"><span data-stu-id="a2aaa-106">Export data from Attract</span></span>

<span data-ttu-id="a2aaa-107">Voit viedä tietoja ilman, että ympäristön käyttöoikeutta on rajoitettava.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="a2aaa-108">Se kannattaa ehkä tehdä testauksen vuoksi tai tietorakenteen selvittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="a2aaa-109">Kun olet valmis siirtoon, rajoita Attract-ympäristön käyttöä tämän menettelyn jälkeen annettujen ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="a2aaa-110">Muista viedä tiedot uudelleen.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="a2aaa-111">Siirry osoitteeseen [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="a2aaa-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="a2aaa-112">Valitse **Pyydä tietojen vientiä** **Tietojen vienti** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="a2aaa-113">Tietojen viennin pyytäminen Attractista</span><span class="sxs-lookup"><span data-stu-id="a2aaa-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="a2aaa-114">Kun **Pyyntöä käsitellään** -sanomaruutu avautuu, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="a2aaa-115">Tietojen vienti voi kestää 20 minuuttia viennin koon mukaan.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="a2aaa-116">Kun vienti valmistuu, valitse vieressä oleva **Lataa**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="a2aaa-117">Kaikki tietojen viennit ovat käytettävissä seitsemän päivää, jonka jälkeen **Lataa**-linkki vanhenee.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="a2aaa-118">Latauksen .zip-tiedostossa on Attract-tietoja, mukaan lukien seuraavat kansiot:</span><span class="sxs-lookup"><span data-stu-id="a2aaa-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="a2aaa-119">Kansion nimi</span><span class="sxs-lookup"><span data-stu-id="a2aaa-119">Folder name</span></span> | <span data-ttu-id="a2aaa-120">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="a2aaa-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="a2aaa-121">Järjestelmänvalvojan asetukset</span><span class="sxs-lookup"><span data-stu-id="a2aaa-121">Admin settings</span></span> | <span data-ttu-id="a2aaa-122">Attract-hallintakeskuksen määritykset.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="a2aaa-123">Ehdokkaat</span><span class="sxs-lookup"><span data-stu-id="a2aaa-123">Candidates</span></span> | <span data-ttu-id="a2aaa-124">Kaikki töihin tai kykypooleihin lisätyt ehdokkaat.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="a2aaa-125">Sähköpostimallit</span><span class="sxs-lookup"><span data-stu-id="a2aaa-125">Email templates</span></span> | <span data-ttu-id="a2aaa-126">Kaikki ympäristöön määritetyt sähköpostimallit.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="a2aaa-127">Työntarjouspakettien mallit</span><span class="sxs-lookup"><span data-stu-id="a2aaa-127">Job offer package templates</span></span> | <span data-ttu-id="a2aaa-128">Kaikki luodut työtarjouspakettien mallit sekä niihin liitetyt määritykset.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="a2aaa-129">Työtarjouksen sääntöjoukot</span><span class="sxs-lookup"><span data-stu-id="a2aaa-129">Job offer rule sets</span></span> |  <span data-ttu-id="a2aaa-130">Kaikki tarjouksenhallintaa ladatut sääntöjoukkotiedostot.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="a2aaa-131">Työntarjousmallit</span><span class="sxs-lookup"><span data-stu-id="a2aaa-131">Job offer templates</span></span> | <span data-ttu-id="a2aaa-132">Kaikki ympäristöön luodut työtarjouksen asiakirjamallit.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="a2aaa-133">Avoimet työpaikat</span><span class="sxs-lookup"><span data-stu-id="a2aaa-133">Job openings</span></span> | <span data-ttu-id="a2aaa-134">Kaikki luodut työt.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-134">All created jobs.</span></span> <span data-ttu-id="a2aaa-135">Poistettuja töitä ei viedä.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="a2aaa-136">Alikansiot sisältävät ehdokkaiden hakemukset. Lisäksi hakemusten liitteille ja tarjouspaketeille on tarvittaessa omat alikansiot.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="a2aaa-137">Avoimien työpaikkojen mallit</span><span class="sxs-lookup"><span data-stu-id="a2aaa-137">Job opening templates</span></span> | <span data-ttu-id="a2aaa-138">Ympäristössä määritetyt töiden käsittelymallit.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="a2aaa-139">Kykypoolit</span><span class="sxs-lookup"><span data-stu-id="a2aaa-139">Talent pools</span></span> | <span data-ttu-id="a2aaa-140">Kaikki luodut kykypoolit, niiden osallistujaluettelot ja kykypoolien ehdokasluettelot.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="a2aaa-141">Työntekijät</span><span class="sxs-lookup"><span data-stu-id="a2aaa-141">Workers</span></span> | <span data-ttu-id="a2aaa-142">Luettelo kaikista ympäristössä olevista työntekijöistä sekä heidän rooleistaan.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="a2aaa-143">(pääkansio)</span><span class="sxs-lookup"><span data-stu-id="a2aaa-143">(root folder)</span></span> | <span data-ttu-id="a2aaa-144">Tietorakennekenttiä kuvaava JSON-rakennetiedosto.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="a2aaa-145">Attractin käytön rajoittaminen</span><span class="sxs-lookup"><span data-stu-id="a2aaa-145">Restrict access to Attract</span></span>

<span data-ttu-id="a2aaa-146">Kun olet valmis siirtoon, rajoita muiden kuin järjestelmänvalvojien Attract-ympäristön käyttöoikeutta ja vie tiedot.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="a2aaa-147">Attract-ympäristön käyttöoikeus rajoitetaan pysyvästi, eikä rajoitusta voi peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="a2aaa-148">Jos haluat, että muut kuin järjestelmänvalvojat voivat jatkaa ympäristön käyttöä, ohita tämä vaihe.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="a2aaa-149">Siirry osoitteeseen [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="a2aaa-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="a2aaa-150">Voit rajoittaa muiden kuin järjestelmänvalvojien Attract-ympäristön käyttöä valitsemalla **Rajoita käyttö nyt** **Rajoita tämän sovelluksen käyttöä** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="a2aaa-151">Käytön rajoittaminen aiheuttaa myös kaikkien julkaistujen aktiivisten työpaikkojen julkaisujen poistaminen.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="a2aaa-152">Muiden kuin järjestelmänvalvojien Attractin käytön rajoittaminen</span><span class="sxs-lookup"><span data-stu-id="a2aaa-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="a2aaa-153">Kun varoitus **Tämä on pysyvä muutos** tulee näkyviin, valitse **Rajoita käyttöä**, jonka jälkeen muut kuin järjestelmänvalvojat eivät voi enää käyttää tätä ympäristöä.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="a2aaa-154">Jos et ole valmis tekemään tätä vaihetta, valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="a2aaa-155">Varoitus siitä, että käytön rajoittaminen on pysyvä muutos</span><span class="sxs-lookup"><span data-stu-id="a2aaa-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="a2aaa-156">Järjestelmänvalvojat voivat jatkaa tietojen viennin ja henkilöraporttisivujen käyttöä sen jälkeen, kun Attract-ympäristön käyttöä on rajoitettu.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="a2aaa-157">Tietojen vienti Onboardista</span><span class="sxs-lookup"><span data-stu-id="a2aaa-157">Export data from Onboard</span></span>

<span data-ttu-id="a2aaa-158">Kun olet valmis, voit ladata mallit, oppaat ja ehdokastiedot Onboardista.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="a2aaa-159">Siirry osoitteeseen [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span><span class="sxs-lookup"><span data-stu-id="a2aaa-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="a2aaa-160">Valitse **Pyydä tietojen vientiä** **Tietojen vienti** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="a2aaa-161">Tietojen viennin pyytäminen Onboardista</span><span class="sxs-lookup"><span data-stu-id="a2aaa-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="a2aaa-162">Kun **Pyyntöä käsitellään** -sanomaruutu avautuu, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="a2aaa-163">Tietojen vienti voi kestää 20 minuuttia viennin koon mukaan.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="a2aaa-164">Kun vienti valmistuu, valitse vieressä oleva **Lataa**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="a2aaa-165">Tietojen viennin lataaminen Onboardista</span><span class="sxs-lookup"><span data-stu-id="a2aaa-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="a2aaa-166">Tietojen vienti on käytettävissä seitsemän päivän ajan.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-166">Your data export is available for seven days.</span></span> <span data-ttu-id="a2aaa-167">**Lataa**-linkki vanhenee seitsemän päivän kuluttua, jonka jälkeen on pyydettävä uusi vienti, jos tiedot on ladattava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="a2aaa-168">Kun aloitat uuden tietojen viennin, aiemmin tehdyt lataukset vanhentuvat, kun uusi vienti on valmis.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="a2aaa-169">Ladattavan .zip-tiedoston sisältö:</span><span class="sxs-lookup"><span data-stu-id="a2aaa-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="a2aaa-170">**Mallit**-kansio, joka sisältää Word-muotoiset Onboard-mallit.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="a2aaa-171">**Opas**-kansio, joka sisältää Word-muotoiset Onboard-oppaat.</span><span class="sxs-lookup"><span data-stu-id="a2aaa-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2aaa-172">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="a2aaa-172">See also</span></span>

[<span data-ttu-id="a2aaa-173">Dynamics 365 Talent: Attract- ja Dynamics 365 Talent: Onboard -sovellusten poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="a2aaa-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)