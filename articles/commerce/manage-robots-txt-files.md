---
title: Robots.txt-tiedostojen hallinta
description: Tässä ohjeaiheessa kerrotaan, miten robots.txt-tiedostoja hallitaan Microsoft Dynamics 365 Commercella.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: ad87594b9c20d0c2b53e8d4e7c1170a78babe74b
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517449"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="b95ab-103">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="b95ab-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b95ab-104">Tässä ohjeaiheessa kerrotaan, miten robots.txt-tiedostoja hallitaan Microsoft Dynamics 365 Commercella.</span><span class="sxs-lookup"><span data-stu-id="b95ab-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b95ab-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b95ab-105">Overview</span></span>

<span data-ttu-id="b95ab-106">Robottien poissulkemisstandardi tai robots.txt on standardi, jonka avulla sivustot kommunikoivat Web-robottien kanssa.</span><span class="sxs-lookup"><span data-stu-id="b95ab-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="b95ab-107">Se ohjeistaa Web-robotteja kaikista verkkosivuston alueista, joilla ei pitäisi käydä.</span><span class="sxs-lookup"><span data-stu-id="b95ab-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="b95ab-108">Hakukoneet käyttävät usein robotteja indeksoidakseen verkkosivustoja.</span><span class="sxs-lookup"><span data-stu-id="b95ab-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="b95ab-109">Jos haluat sulkea robotit pois palvelimelta, luo tiedosto palvelimelle.</span><span class="sxs-lookup"><span data-stu-id="b95ab-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="b95ab-110">Tässä tiedostossa määritetään robots-sovelluksen käyttöoikeuskäytäntö.</span><span class="sxs-lookup"><span data-stu-id="b95ab-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="b95ab-111">Tiedoston on oltava käytettävissä HTTP-protokollan kautta paikallisessa URL-osoitteessa **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="b95ab-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="b95ab-112">Robots.txt-tiedosto auttaa hakukoneita indeksoimaan sivustosi sisällön.</span><span class="sxs-lookup"><span data-stu-id="b95ab-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="b95ab-113">Dynamics 365 Commerce auttaa sinua lataamaan robots.txt-tiedoston toimialueellesi.</span><span class="sxs-lookup"><span data-stu-id="b95ab-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="b95ab-114">Voit ladata kullekin Commerce Environment -verkkotunnukselle yhden robots.txt-tiedoston ja liittää sen toimialueeseen.</span><span class="sxs-lookup"><span data-stu-id="b95ab-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="b95ab-115">Lisä tietoja robots.txt-tiedostosta on [Web Robots-sivuilla](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="b95ab-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="b95ab-116">Robots.txt-tiedoston lataaminen</span><span class="sxs-lookup"><span data-stu-id="b95ab-116">Upload a robots.txt file</span></span>

<span data-ttu-id="b95ab-117">Kun olet luonut ja muokannut robots.txt-tiedostoasi [robottien poissulkemisstandardin](https://www.robotstxt.org/orig.html) mukaisesti, varmista, että tiedosto on käytettävissä tietokoneessa, jossa käytät Commercen luontityökaluja.</span><span class="sxs-lookup"><span data-stu-id="b95ab-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="b95ab-118">Tiedoston on oltava nimeltään **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="b95ab-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="b95ab-119">Parhaan tuloksen saamiseksi sen on oltava standardissa mainitussa muodossa.</span><span class="sxs-lookup"><span data-stu-id="b95ab-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="b95ab-120">Jokainen Commerce-asiakas on vastuussa robots.txt-tiedoston sisällön validoinnista ja ylläpitämisestä.</span><span class="sxs-lookup"><span data-stu-id="b95ab-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="b95ab-121">Ladataksesi robots.txt -tiedoston, sinun on oltava kirjautuneena sisään Commercen järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="b95ab-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="b95ab-122">Jos haluat ladata robots.txt-tiedoston sivustoon Commerce-sivustossa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b95ab-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b95ab-123">Kirjaudu Commerce-järjestelmään järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="b95ab-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="b95ab-124">Laajenna vasemmanpuoleisessa siirtymisruudussa **vuokraajan asetukset** (hammasratassymbolin vieressä).</span><span class="sxs-lookup"><span data-stu-id="b95ab-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="b95ab-125">Valitse **Vuokraajan asetukset** -kohdasta **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="b95ab-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="b95ab-126">Luettelo kaikista ympäristöön liittyvistä toimialueista näkyy ikkunan pääosassa.</span><span class="sxs-lookup"><span data-stu-id="b95ab-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="b95ab-127">Valitse **Hallitse**, jos haluat ladata robots. txt-tiedoston ympäristösi toimialueelle.</span><span class="sxs-lookup"><span data-stu-id="b95ab-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="b95ab-128">Valitse oikealla olevasta valikosta robots.txt-tiedostoon liitetyn toimialueen viereinen **lähetys**-painike (ylöspäin osoittava nuoli).</span><span class="sxs-lookup"><span data-stu-id="b95ab-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="b95ab-129">Näyttöön tulee tiedostoselainvalintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="b95ab-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="b95ab-130">Etsi ja valitse valintaikkunassa robots.txt-tiedosto, jonka haluat ladata liitettyä toimialuetta varten, ja valitse sitten **Avaa**, niin lataus on valmis.</span><span class="sxs-lookup"><span data-stu-id="b95ab-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="b95ab-131">Latauksen aikana Commerce tarkistaa, että tiedosto on tekstitiedosto, mutta se ei vahvista tiedoston sisältöä.</span><span class="sxs-lookup"><span data-stu-id="b95ab-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="b95ab-132">Robots.txt-tiedoston lataaminen</span><span class="sxs-lookup"><span data-stu-id="b95ab-132">Download a robots.txt file</span></span>

<span data-ttu-id="b95ab-133">Jos haluat ladata robots.txt-tiedoston sivustoon Commerce-sivustossa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b95ab-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b95ab-134">Kirjaudu Commerce-järjestelmään järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="b95ab-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="b95ab-135">Laajenna vasemmanpuoleisessa siirtymisruudussa **vuokraajan asetukset** (hammasratassymbolin vieressä).</span><span class="sxs-lookup"><span data-stu-id="b95ab-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="b95ab-136">Valitse **Vuokraajan asetukset** -kohdasta **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="b95ab-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="b95ab-137">Luettelo kaikista ympäristöön liittyvistä toimialueista näkyy ikkunan pääosassa.</span><span class="sxs-lookup"><span data-stu-id="b95ab-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="b95ab-138">Valitse **Hallitse**, jos haluat ladata robots. txt-tiedoston ympäristösi toimialueelle.</span><span class="sxs-lookup"><span data-stu-id="b95ab-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="b95ab-139">Valitse oikealla olevasta valikosta robots.txt-tiedostoon liitetyn toimialueen viereinen **Lataus**-painike (alaspäin osoittava nuoli).</span><span class="sxs-lookup"><span data-stu-id="b95ab-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="b95ab-140">Näyttöön tulee tiedostoselainvalintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="b95ab-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="b95ab-141">Siirry valintaikkunassa haluamaasi sijaintiin paikallisessa asemassa, vahvista tai kirjoita tiedoston nimi ja viimeistele lataaminen valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b95ab-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="b95ab-142">Tämän toiminnon avulla voidaan ladata vain robots.txt-tiedostoja, jotka on aiemmin ladattu Commerce authoring toolsin kautta.</span><span class="sxs-lookup"><span data-stu-id="b95ab-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="b95ab-143">Robots.txt-tiedoston poistaminen</span><span class="sxs-lookup"><span data-stu-id="b95ab-143">Delete a robots.txt file</span></span>

<span data-ttu-id="b95ab-144">Jos haluat poistaa robots.txt-tiedoston sivustoon Commerce-sivustossa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b95ab-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b95ab-145">Kirjaudu Commerce-järjestelmään järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="b95ab-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="b95ab-146">Laajenna vasemmanpuoleisessa siirtymisruudussa **vuokraajan asetukset** (hammasratassymbolin vieressä).</span><span class="sxs-lookup"><span data-stu-id="b95ab-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="b95ab-147">Valitse **Vuokraajan asetukset** -kohdasta **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="b95ab-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="b95ab-148">Luettelo kaikista ympäristöön liittyvistä toimialueista näkyy ikkunan pääosassa.</span><span class="sxs-lookup"><span data-stu-id="b95ab-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="b95ab-149">Valitse **Hallitse**, jos haluat poistaa robots.txt-tiedoston ympäristösi toimialueelle.</span><span class="sxs-lookup"><span data-stu-id="b95ab-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="b95ab-150">Valitse oikealla olevasta valikosta robots.txt-tiedostoon liitetyn toimialueen viereinen **Poista**-painike (roskakorikuvake).</span><span class="sxs-lookup"><span data-stu-id="b95ab-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="b95ab-151">Näyttöön tulee tiedostoselainikkuna.</span><span class="sxs-lookup"><span data-stu-id="b95ab-151">A file browser window appears.</span></span>
6. <span data-ttu-id="b95ab-152">Etsi ja valitse tiedostoselainikkunassa robots.txt-tiedosto, jonka haluat poistaa liitettyä toimialuetta varten, ja valitse sitten **Avaa**, niin lataus on valmis.</span><span class="sxs-lookup"><span data-stu-id="b95ab-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="b95ab-153">Näyttöön tulee varoitussanomaruutu.</span><span class="sxs-lookup"><span data-stu-id="b95ab-153">A warning message box appears.</span></span>
7. <span data-ttu-id="b95ab-154">Vahvista robots.txt-tiedoston **Poistaminen** valitsemalla viestiruudusta Poista.</span><span class="sxs-lookup"><span data-stu-id="b95ab-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="b95ab-155">Tämän toiminnon avulla voidaan poistaa vain robots.txt-tiedostoja, jotka on aiemmin ladattu Commerce authoring toolsin kautta.</span><span class="sxs-lookup"><span data-stu-id="b95ab-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b95ab-156">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b95ab-156">Additional resources</span></span>

[<span data-ttu-id="b95ab-157">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b95ab-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="b95ab-158">Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="b95ab-158">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="b95ab-159">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="b95ab-159">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="b95ab-160">Dynamics 365 Commerce -sivuston liittäminen online-kanavaan</span><span class="sxs-lookup"><span data-stu-id="b95ab-160">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="b95ab-161">URL-uudelleenohjausten joukkolataus palveluun</span><span class="sxs-lookup"><span data-stu-id="b95ab-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="b95ab-162">Kuluttajakaupan vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="b95ab-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="b95ab-163">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="b95ab-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="b95ab-164">Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="b95ab-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="b95ab-165">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="b95ab-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="b95ab-166">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="b95ab-166">Enable location-based store detection</span></span>](enable-store-detection.md)
