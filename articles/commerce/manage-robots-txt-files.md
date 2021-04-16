---
title: Robots.txt-tiedostojen hallinta
description: Tässä ohjeaiheessa kerrotaan, miten robots.txt-tiedostoja hallitaan Microsoft Dynamics 365 Commercella.
author: BrianShook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9b832d6714447f8957095c8c87d48527087f12d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794232"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="2bf1a-103">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="2bf1a-103">Manage robots.txt files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2bf1a-104">Tässä ohjeaiheessa kerrotaan, miten robots.txt-tiedostoja hallitaan Microsoft Dynamics 365 Commercella.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2bf1a-105">Robottien poissulkemisstandardi tai robots.txt on standardi, jonka avulla sivustot kommunikoivat Web-robottien kanssa.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-105">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="2bf1a-106">Se ohjeistaa Web-robotteja kaikista verkkosivuston alueista, joilla ei pitäisi käydä.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-106">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="2bf1a-107">Hakukoneet käyttävät usein robotteja indeksoidakseen verkkosivustoja.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-107">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="2bf1a-108">Jos haluat sulkea robotit pois palvelimelta, luo tiedosto palvelimelle.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-108">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="2bf1a-109">Tässä tiedostossa määritetään robots-sovelluksen käyttöoikeuskäytäntö.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-109">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="2bf1a-110">Tiedoston on oltava käytettävissä HTTP-protokollan kautta paikallisessa URL-osoitteessa **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-110">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="2bf1a-111">Robots.txt-tiedosto auttaa hakukoneita indeksoimaan sivustosi sisällön.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-111">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="2bf1a-112">Dynamics 365 Commerce auttaa sinua lataamaan robots.txt-tiedoston toimialueellesi.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-112">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="2bf1a-113">Voit ladata kullekin Commerce Environment -verkkotunnukselle yhden robots.txt-tiedoston ja liittää sen toimialueeseen.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-113">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="2bf1a-114">Lisä tietoja robots.txt-tiedostosta on [Web Robots-sivuilla](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="2bf1a-114">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="2bf1a-115">Robots.txt-tiedoston lataaminen</span><span class="sxs-lookup"><span data-stu-id="2bf1a-115">Upload a robots.txt file</span></span>

<span data-ttu-id="2bf1a-116">Kun olet luonut ja muokannut robots.txt-tiedostoasi [robottien poissulkemisstandardin](https://www.robotstxt.org/orig.html) mukaisesti, varmista, että tiedosto on käytettävissä tietokoneessa, jossa käytät Commercen luontityökaluja.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-116">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="2bf1a-117">Tiedoston on oltava nimeltään **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-117">The file must be named **robots.txt**.</span></span> <span data-ttu-id="2bf1a-118">Parhaan tuloksen saamiseksi sen on oltava standardissa mainitussa muodossa.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-118">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="2bf1a-119">Jokainen Commerce-asiakas on vastuussa robots.txt-tiedoston sisällön validoinnista ja ylläpitämisestä.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-119">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="2bf1a-120">Ladataksesi robots.txt -tiedoston, sinun on oltava kirjautuneena sisään Commercen järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-120">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="2bf1a-121">Jos haluat ladata robots.txt-tiedoston sivustoon Commerce-sivustossa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-121">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="2bf1a-122">Kirjaudu Commerce-järjestelmään järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-122">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="2bf1a-123">Laajenna vasemmanpuoleisessa siirtymisruudussa **vuokraajan asetukset** (hammasratassymbolin vieressä).</span><span class="sxs-lookup"><span data-stu-id="2bf1a-123">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="2bf1a-124">Valitse **Vuokraajan asetukset** -kohdasta **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-124">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="2bf1a-125">Luettelo kaikista ympäristöön liittyvistä toimialueista näkyy ikkunan pääosassa.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-125">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="2bf1a-126">Valitse **Hallitse**, jos haluat ladata robots. txt-tiedoston ympäristösi toimialueelle.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-126">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="2bf1a-127">Valitse oikealla olevasta valikosta robots.txt-tiedostoon liitetyn toimialueen viereinen **lähetys**-painike (ylöspäin osoittava nuoli).</span><span class="sxs-lookup"><span data-stu-id="2bf1a-127">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="2bf1a-128">Näyttöön tulee tiedostoselainvalintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-128">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="2bf1a-129">Etsi ja valitse valintaikkunassa robots.txt-tiedosto, jonka haluat ladata liitettyä toimialuetta varten, ja valitse sitten **Avaa**, niin lataus on valmis.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-129">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="2bf1a-130">Latauksen aikana Commerce tarkistaa, että tiedosto on tekstitiedosto, mutta se ei vahvista tiedoston sisältöä.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-130">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="2bf1a-131">Robots.txt-tiedoston lataaminen</span><span class="sxs-lookup"><span data-stu-id="2bf1a-131">Download a robots.txt file</span></span>

<span data-ttu-id="2bf1a-132">Jos haluat ladata robots.txt-tiedoston sivustoon Commerce-sivustossa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-132">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="2bf1a-133">Kirjaudu Commerce-järjestelmään järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-133">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="2bf1a-134">Laajenna vasemmanpuoleisessa siirtymisruudussa **vuokraajan asetukset** (hammasratassymbolin vieressä).</span><span class="sxs-lookup"><span data-stu-id="2bf1a-134">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="2bf1a-135">Valitse **Vuokraajan asetukset** -kohdasta **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-135">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="2bf1a-136">Luettelo kaikista ympäristöön liittyvistä toimialueista näkyy ikkunan pääosassa.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-136">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="2bf1a-137">Valitse **Hallitse**, jos haluat ladata robots. txt-tiedoston ympäristösi toimialueelle.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-137">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="2bf1a-138">Valitse oikealla olevasta valikosta robots.txt-tiedostoon liitetyn toimialueen viereinen **Lataus**-painike (alaspäin osoittava nuoli).</span><span class="sxs-lookup"><span data-stu-id="2bf1a-138">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="2bf1a-139">Näyttöön tulee tiedostoselainvalintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-139">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="2bf1a-140">Siirry valintaikkunassa haluamaasi sijaintiin paikallisessa asemassa, vahvista tai kirjoita tiedoston nimi ja viimeistele lataaminen valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-140">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="2bf1a-141">Tämän toiminnon avulla voidaan ladata vain robots.txt-tiedostoja, jotka on aiemmin ladattu Commerce authoring toolsin kautta.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-141">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="2bf1a-142">Robots.txt-tiedoston poistaminen</span><span class="sxs-lookup"><span data-stu-id="2bf1a-142">Delete a robots.txt file</span></span>

<span data-ttu-id="2bf1a-143">Jos haluat poistaa robots.txt-tiedoston sivustoon Commerce-sivustossa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-143">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="2bf1a-144">Kirjaudu Commerce-järjestelmään järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-144">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="2bf1a-145">Laajenna vasemmanpuoleisessa siirtymisruudussa **vuokraajan asetukset** (hammasratassymbolin vieressä).</span><span class="sxs-lookup"><span data-stu-id="2bf1a-145">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="2bf1a-146">Valitse **Vuokraajan asetukset** -kohdasta **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-146">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="2bf1a-147">Luettelo kaikista ympäristöön liittyvistä toimialueista näkyy ikkunan pääosassa.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-147">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="2bf1a-148">Valitse **Hallitse**, jos haluat poistaa robots.txt-tiedoston ympäristösi toimialueelle.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-148">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="2bf1a-149">Valitse oikealla olevasta valikosta robots.txt-tiedostoon liitetyn toimialueen viereinen **Poista**-painike (roskakorikuvake).</span><span class="sxs-lookup"><span data-stu-id="2bf1a-149">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="2bf1a-150">Näyttöön tulee tiedostoselainikkuna.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-150">A file browser window appears.</span></span>
6. <span data-ttu-id="2bf1a-151">Etsi ja valitse tiedostoselainikkunassa robots.txt-tiedosto, jonka haluat poistaa liitettyä toimialuetta varten, ja valitse sitten **Avaa**, niin lataus on valmis.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-151">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="2bf1a-152">Näyttöön tulee varoitussanomaruutu.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-152">A warning message box appears.</span></span>
7. <span data-ttu-id="2bf1a-153">Vahvista robots.txt-tiedoston **Poistaminen** valitsemalla viestiruudusta Poista.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-153">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="2bf1a-154">Tämän toiminnon avulla voidaan poistaa vain robots.txt-tiedostoja, jotka on aiemmin ladattu Commerce authoring toolsin kautta.</span><span class="sxs-lookup"><span data-stu-id="2bf1a-154">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2bf1a-155">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2bf1a-155">Additional resources</span></span>

[<span data-ttu-id="2bf1a-156">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2bf1a-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="2bf1a-157">Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="2bf1a-157">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="2bf1a-158">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="2bf1a-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="2bf1a-159">Dynamics 365 Commerce -sivuston liittäminen online-kanavaan</span><span class="sxs-lookup"><span data-stu-id="2bf1a-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="2bf1a-160">URL-uudelleenohjausten joukkolataus palveluun</span><span class="sxs-lookup"><span data-stu-id="2bf1a-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="2bf1a-161">Kuluttajakaupan vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="2bf1a-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="2bf1a-162">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="2bf1a-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="2bf1a-163">Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="2bf1a-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="2bf1a-164">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="2bf1a-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="2bf1a-165">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="2bf1a-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
