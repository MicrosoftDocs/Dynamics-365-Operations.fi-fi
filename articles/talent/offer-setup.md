---
title: "Tarjoustenhallinnan määrittäminen"
description: "Tässä ohjeaiheessa käsitellään tarjousten määrittämistä Talentissa."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: fa2f2f9f67562524961352a87a7db49992776e46
ms.contentlocale: fi-fi
ms.lasthandoff: 10/22/2018

---
# <a name="set-up-offer-management"></a><span data-ttu-id="891f3-103">Tarjoustenhallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="891f3-103">Set up offer management</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="891f3-104">Kun hakija siirretään Dynamics 365 for Talent: Attractissa tarjousvaiheeseen, sinun on varmistettava, että tarjoukset luodaan nopeasti hakijalle, hyväksytään tarvittaessa ja lähetetään hakijalle.</span><span class="sxs-lookup"><span data-stu-id="891f3-104">When a candidate is moved to the offer stage in Dynamics 365 for Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="891f3-105">Koska useimmat tarjoukset ovat vakiomuotoisia, ne voidaan luoda uudelleenkäytettävistä malleista.</span><span class="sxs-lookup"><span data-stu-id="891f3-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="891f3-106">Attractissa kaikki tarjoukset kerätään tarjouspaketiksi. Se on kokoelma, jossa on vähintään yksi tarjousasiakirja.</span><span class="sxs-lookup"><span data-stu-id="891f3-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="891f3-107">Tässä ohjeaiheessa käsitellään kaikki vaiheet, joita noudattamalla Attractin järjestelmä määrittää erilaisia tarjouspakettimalleja Attractin tarjousten hallintatoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="891f3-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="891f3-108">Jos käyttäjällä ei ole järjestelmänvalvojan rooli, hänellä ei ole näiden toimintojen käyttöoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="891f3-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="891f3-109">Tarjouksen hallintatoiminnot ovat saatavana kattavan työhönottolaajennuksen osana.</span><span class="sxs-lookup"><span data-stu-id="891f3-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="891f3-110">Tarjouksen tiedot</span><span class="sxs-lookup"><span data-stu-id="891f3-110">Offer data</span></span> 

<span data-ttu-id="891f3-111">Tarjouksen tiedot on tarjouspakettimallin pienin yksikkö.</span><span class="sxs-lookup"><span data-stu-id="891f3-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="891f3-112">Tyypillinen tarjous koostuu vakiotekstistä ja arvojoukosta.</span><span class="sxs-lookup"><span data-stu-id="891f3-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="891f3-113">Arvojoukko on ainoa osa, joka voi vaihdella tarjouksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="891f3-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="891f3-114">Tarjouksen luonnissa on tärkeintä, että tarjouksen luoja keskittyy tarjouspakettimallissa olevaan tarjouksen tietojen paikkamerkkiluetteloon.</span><span class="sxs-lookup"><span data-stu-id="891f3-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="891f3-115">Määritä tarjouksen tiedot seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="891f3-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="891f3-116">Valitse **Tarjousten hallinta**.</span><span class="sxs-lookup"><span data-stu-id="891f3-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="891f3-117">Laajenna **Kirjasto**-osa vasemmassa siirtymisruudussa ja valitse sitten **Tarjouksen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="891f3-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="891f3-118">**Tarjouksen tiedot** -sivulla on **Ehdokkaan tiedot**- ja **Työn tiedot** -osat.</span><span class="sxs-lookup"><span data-stu-id="891f3-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="891f3-119">Attractissa on muutamia valmiita tarjouksen tietojen paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="891f3-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    
    > <span data-ttu-id="891f3-120">Sivulla on osia, joissa tarjouksen tietojen erilaiset paikkamerkit voidaan järjestää loogisiksi ryhmiksi.</span><span class="sxs-lookup"><span data-stu-id="891f3-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="891f3-121">Nämä osat helpottavat tarjouksen tietojen ylläpitoa ja tietojen täyttämistä tarjouksen luontiprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="891f3-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>

1.  <span data-ttu-id="891f3-122">Voit luoda uuden tarjoustieto-osan valitsemalla **Lisää osa** ja antamalla sille yksilöivä nimen.</span><span class="sxs-lookup"><span data-stu-id="891f3-122">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="891f3-123">Voit lisätä tarjoustietojen paikkamerkin johonkin osaan valitsemalla **Lisää tarjouksen tiedot** ja antamalla paikkamerkille yksilöivän nimen.</span><span class="sxs-lookup"><span data-stu-id="891f3-123">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="891f3-124">Voit muokata minkä tahansa osan nimeä pitämällä osoitinta osan päällä ja päivittämällä nimen.</span><span class="sxs-lookup"><span data-stu-id="891f3-124">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="891f3-125">Voit kyllä muokata aiemmin luodun tarjoustietojen paikkamerkin nimeä, mutta varmista ensin, että paikkamerkkiä ei käytetä missään mallissa.</span><span class="sxs-lookup"><span data-stu-id="891f3-125">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="891f3-126">Siirrä sitten osoitin tarjoustietojen paikkamerkin nimen päälle ja päivitä nimi tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="891f3-126">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="891f3-127">Voit kyllä poistaa aiemmin luodun tarjoustietojen paikkamerkin, mutta varmista ensin, että paikkamerkkiä ei käytetä missään muussa mallissa.</span><span class="sxs-lookup"><span data-stu-id="891f3-127">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="891f3-128">Siirrä sen jälkeen osoitin paikkamerkin päälle. Kun roskakorikuvake tulee näkyviin, poista tarjoustietojen paikkamerkki kuvaketta napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="891f3-128">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="891f3-129">Jokaisen tarjouksen tiedon vieressä on numero, joka ilmaisee, kuinka monessa mallissa tarjoustietojen paikkamerkki on käytössä.</span><span class="sxs-lookup"><span data-stu-id="891f3-129">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="891f3-130">Voit poistaa minkä tahansa osan, siirtämällä osoittimin nimen päälle.</span><span class="sxs-lookup"><span data-stu-id="891f3-130">To delete any section, hover over the name.</span></span> <span data-ttu-id="891f3-131">Jos mitään osan tarjoustietojen paikkamerkkiä ei käytetä missään mallissa, voit poistaa sen roskakorikuvaketta napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="891f3-131">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="891f3-132">Osan poistaminen poistaa myös kaikki tarjoustietojen paikkamerkit kyseisestä osasta.</span><span class="sxs-lookup"><span data-stu-id="891f3-132">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="891f3-133">Kun tarjoustietojen paikkamerkit on määritetty, voit käyttää niitä missä tahansa asiakirjamallissa.</span><span class="sxs-lookup"><span data-stu-id="891f3-133">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="891f3-134">Tarjoustietojen paikkamerkkien käyttöä ei ole rajoitettu tiettyyn malliin, vaan samaa joukkoa voidaan käytätä kaikissa malleissa.</span><span class="sxs-lookup"><span data-stu-id="891f3-134">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="891f3-135">Tarjouksen tietojen säännöt</span><span class="sxs-lookup"><span data-stu-id="891f3-135">Offer data rules</span></span>

<span data-ttu-id="891f3-136">Useimmissa organisaatioissa on tarjousten luontisäännöt.</span><span class="sxs-lookup"><span data-stu-id="891f3-136">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="891f3-137">Organisaatio voi esimerkiksi edellyttää, että tietyn toimipaikan ja tietyn ikälisän yhdistelmänä muodostuva vuosipalkka saa olla enintään tietyn suuruinen tai että uudelle työntekijälle on käytettävissä vain muutamia tarjoustason arvoja.</span><span class="sxs-lookup"><span data-stu-id="891f3-137">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="891f3-138">Attract tukee tällä hetkellä kaikkia tällaisia CSV-tiedostoa käyttäviä tietosääntöjä.</span><span class="sxs-lookup"><span data-stu-id="891f3-138">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="891f3-139">Valmistele tietosääntöjen CSV-tiedosto seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="891f3-139">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="891f3-140">Määritä sääntöjoukon tarjoustietojen paikkamerkki.</span><span class="sxs-lookup"><span data-stu-id="891f3-140">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="891f3-141">Esimerkki: **Vuosipalkka**.</span><span class="sxs-lookup"><span data-stu-id="891f3-141">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="891f3-142">Määritä riippuvaiset tarjouksen tietojen paikkamerkkiarvot.</span><span class="sxs-lookup"><span data-stu-id="891f3-142">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="891f3-143">Esimerkki: **Työn sijainti** ja **Taso**.</span><span class="sxs-lookup"><span data-stu-id="891f3-143">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="891f3-144">Määritä sarakkeiksi 1 ja 2 **Työn sijainti** ja **Taso**.</span><span class="sxs-lookup"><span data-stu-id="891f3-144">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="891f3-145">Lataa alueen arvo määrittämällä sarakkeiksi 3 ja 4 **Vuosipalkka**.</span><span class="sxs-lookup"><span data-stu-id="891f3-145">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="891f3-146">Jos haluat ladata tietyn arvon arvoalueen sijaan, määritä vain sarakkeeksi 3 **Vuosipalkka**.</span><span class="sxs-lookup"><span data-stu-id="891f3-146">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="891f3-147">Täytä Microsoft Excel -tiedoston tiedot tarvittavien roolien perusteella.</span><span class="sxs-lookup"><span data-stu-id="891f3-147">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="891f3-148">Varmista, että jokainen rivi on yksilöllinen yhdistelmä kaikista arvoista.</span><span class="sxs-lookup"><span data-stu-id="891f3-148">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="891f3-149">Tallenna tiedosto CSV-muodossa.</span><span class="sxs-lookup"><span data-stu-id="891f3-149">Save the file as a CSV format.</span></span>

<span data-ttu-id="891f3-150">Lataa tarjouksen tietosääntötiedosto seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="891f3-150">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="891f3-151">Valitse **Tarjousten hallinta**.</span><span class="sxs-lookup"><span data-stu-id="891f3-151">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="891f3-152">Laajenna **Kirjasto**-osa vasemmassa siirtymisruudussa ja valitse sitten **Tarjouksen tietojen säännöt**.</span><span class="sxs-lookup"><span data-stu-id="891f3-152">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="891f3-153">Valitse **Uusi tietojoukko**, jolloin **Lataa palvelimeen** -valintaikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="891f3-153">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="891f3-154">Määritä sääntöjoukolle yksilöivä nimi ja lataa tallennettu CSV-tiedosto sitten palvelimeen.</span><span class="sxs-lookup"><span data-stu-id="891f3-154">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="891f3-155">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="891f3-155">Click **Add**.</span></span>
    <span data-ttu-id="891f3-156">Sääntöjoukko käsitellään taustalla, ja kun se valmistuu, saat siitä ilmoituksen sovelluksessa ja sähköpostitse.</span><span class="sxs-lookup"><span data-stu-id="891f3-156">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="891f3-157">Saat ilmoituksen, jos latauksen käsittelyssä esiintyi virheitä.</span><span class="sxs-lookup"><span data-stu-id="891f3-157">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="891f3-158">Voit sitten ladata virhelokin, korjata tiedoston ja ladata sen uudelleen palvelimeen.</span><span class="sxs-lookup"><span data-stu-id="891f3-158">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="891f3-159">Käytä ellipsipainiketta (**…**), jos haluat ladata sääntöjoukon ja päivittää arvojoukon.</span><span class="sxs-lookup"><span data-stu-id="891f3-159">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="891f3-160">Lataa tiedosto päivittämisen jälkeen uudelleen palvelimeen.</span><span class="sxs-lookup"><span data-stu-id="891f3-160">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="891f3-161">Voit poistaa palvelimeen ladatun aiemmin luodun sääntöjoukon, jos määritettävää paikkamerkkiä ei käytetä toisessa asiakirjamallissa.</span><span class="sxs-lookup"><span data-stu-id="891f3-161">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!HUOMAUTUKSET]
> - <span data-ttu-id="891f3-163">Kullakin paikkamerkillä voi olla vain yksi yksilöllinen sarakejoukko, josta se on riippuvainen.</span><span class="sxs-lookup"><span data-stu-id="891f3-163">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="891f3-164">Jos esimerkki **vuosipalkka** on riippuvainen **työn sijainnista** ja **tasosta**, et voi ladata palvelimeen toista sääntöjoukkoa, jossa **vuosipalkka** on riippuvainen toisenlaisesta sarakejoukosta.</span><span class="sxs-lookup"><span data-stu-id="891f3-164">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="891f3-165">Voit ladata tarjouksen tietojen näytesääntöjoukot **Tarjouksen tietojen säännöt** -sivun **Mallit**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="891f3-165">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="891f3-166">Kun tarjouksen luoja korvaa tarjouksen tietojen sääntöjen suosittelemat arvot, tarjous merkitään muuksi kuin vakiotarjoukseksi ja tarjouksen hyväksyntätyönkulun käyttö on pakollista.</span><span class="sxs-lookup"><span data-stu-id="891f3-166">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="891f3-167">Tiedostomallit</span><span class="sxs-lookup"><span data-stu-id="891f3-167">Document templates</span></span>

<span data-ttu-id="891f3-168">Tarjouksen asiakirjamalli voi auttaa järjestelmänvalvojia luomaan tarjouskirjeitä.</span><span class="sxs-lookup"><span data-stu-id="891f3-168">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="891f3-169">Tarjouksen asiakirjamalli koostuu tekstistä, joka on osa tarjousta, ja määritetyistä tarjoustietojen paikkamerkeistä.</span><span class="sxs-lookup"><span data-stu-id="891f3-169">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="891f3-170">Luo tarjouksen asiakirjamalli seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="891f3-170">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="891f3-171">Valitse **Tarjousten hallinta**.</span><span class="sxs-lookup"><span data-stu-id="891f3-171">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="891f3-172">Laajenna **Kirjasto**-osa vasemmassa siirtymisruudussa ja valitse sitten **Mallit**.</span><span class="sxs-lookup"><span data-stu-id="891f3-172">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="891f3-173">Avautuvalla **Mallit**-sivulla on luettelo asiakirjamalleista, jotka on jo määritetty.</span><span class="sxs-lookup"><span data-stu-id="891f3-173">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="891f3-174">Luo uusi asiakirjamalli valitsemalla **Uusi malli**.</span><span class="sxs-lookup"><span data-stu-id="891f3-174">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="891f3-175">Anna mallille yksilöivä nimi ja valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="891f3-175">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="891f3-176">Voit lisätä tai muokata tarjousasiakirjan sisältöä RTF-editorissa.</span><span class="sxs-lookup"><span data-stu-id="891f3-176">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="891f3-177">Voit lisätä tauluja, kuvia ja hyperlinkkejä käyttämällä tekstieditorin yläosassa olevia vaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="891f3-177">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="891f3-178">Voit lisätä tarjoustietojen paikkamerkkien tarjouksen malliasiakirjaan</span><span class="sxs-lookup"><span data-stu-id="891f3-178">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="891f3-179">vetämällä ja pudottamalla oikeasta ruudusta</span><span class="sxs-lookup"><span data-stu-id="891f3-179">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="891f3-180">sijoittamalla tarjoustietojen paikkamerkin suoraan työpaikkaan tunnisteen avulla.</span><span class="sxs-lookup"><span data-stu-id="891f3-180">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="891f3-181">Kirjoita ensin **\#** ja aloita sitten tarjoustietojen paikkamerkin nimen kirjoittaminen.</span><span class="sxs-lookup"><span data-stu-id="891f3-181">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="891f3-182">Vaihtoehdot tulevaa näkyviin avattavana luettelon.</span><span class="sxs-lookup"><span data-stu-id="891f3-182">Options will appear in the drop-down list.</span></span> <span data-ttu-id="891f3-183">Lisää tarjoustietojen paikkamerkki napsauttamalla sitä tai painamalla **Enter**-näppäintä.</span><span class="sxs-lookup"><span data-stu-id="891f3-183">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!HUOMAUTUKSET]
    > - <span data-ttu-id="891f3-185">Voit liittää paikkamerkin tarjouksen asiakirjamalliin ilman, että hakija näkee sen arvon, siirtämällä osoittimen tarjoustietojen paikkamerkin päälle ja napsauttamalla **Kiinnitä**-kuvaketta.</span><span class="sxs-lookup"><span data-stu-id="891f3-185">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="891f3-186">Paikkamerkki siirretään nyt tarjouksen asiakirjamallin **Kiinnitetyn tarjouksen tiedot** -osaan.</span><span class="sxs-lookup"><span data-stu-id="891f3-186">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="891f3-187">Voit poistaa kiinnityksen toimimalla samalla tavoin mutta valitsemalla **Poista kiinnity** tarjoustietojen paikkamerkkiluettelossa.</span><span class="sxs-lookup"><span data-stu-id="891f3-187">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="891f3-188">Voit tarkastella aktiivisia tarjoustietojen paikkamerkkejä siirtymällä oikeassa ruudussa **Aktiiviset**-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="891f3-188">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="891f3-189">Jos lisää tarjoustietojen sääntöjoukkoa noudattavan paikkamerkin, näet kyseisen tarjoustietojen paikkamerkin riippuvuuden muista arvoista.</span><span class="sxs-lookup"><span data-stu-id="891f3-189">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="891f3-190">Vaihtoehtoisesti voit **tuoda** sisällön paikallisen tiedoston .docx-tiedostosta ja muokata sitä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="891f3-190">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="891f3-191">Tässä tapauksessa sinun ei tarvitsee kirjoittaa kaikkea sisältöä editorissa.</span><span class="sxs-lookup"><span data-stu-id="891f3-191">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="891f3-192">Voit esikatsella tarjousasiakirjaa valitsemalla sivun yläosassa**Esikatselu**-vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="891f3-192">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="891f3-193">Voit hallita, saako tarjouksen luoja muokata tarjousasiakirjan sisältöä valitsemalla sivun yläosassa **Hallitse käyttöoikeutta**.</span><span class="sxs-lookup"><span data-stu-id="891f3-193">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="891f3-194">Jos haluat, että tarjouksen luoja voi vain lisätä paikkamerkin arvot tekstin muokkaamisen sijaan, määritä käyttöoikeuden arvoksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="891f3-194">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="891f3-195">Tallenna eteneminen valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="891f3-195">Click **Save** to save your progress.</span></span> <span data-ttu-id="891f3-196">Malli tallennetaan luonnoksena.</span><span class="sxs-lookup"><span data-stu-id="891f3-196">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="891f3-197">Viimeistele asiakirja ja merkitse se julkaistuksi valitsemalla **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="891f3-197">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="891f3-198">Näet asiakirjamallikirjaston saapumissivulla, mitkä asiakirjamallit ovat aktiivisia, mitkä luonnostilassa ja mitkä on arkistoitu eikä enää käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="891f3-198">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="891f3-199">Voit poistaa tarjousasiakirjamallit, jotka eivät sisälly nykyiseen tarjouspakettimalliin.</span><span class="sxs-lookup"><span data-stu-id="891f3-199">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="891f3-200">Tarjouspakettimallit</span><span class="sxs-lookup"><span data-stu-id="891f3-200">Offer package templates</span></span>

<span data-ttu-id="891f3-201">Tarjouspaketit ovat hakijan kanssa jaettavia tarjouksen tietoja, ja ne koostuvat vähintään yhdestä tarjousasiakirjamallista.</span><span class="sxs-lookup"><span data-stu-id="891f3-201">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="891f3-202">Luo tarjouspaketti seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="891f3-202">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="891f3-203">Valitse **Tarjousten hallinta**.</span><span class="sxs-lookup"><span data-stu-id="891f3-203">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="891f3-204">Valitse vasemmassa siirtymisruudussa **Paketit**.</span><span class="sxs-lookup"><span data-stu-id="891f3-204">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="891f3-205">Näkyviin tulee luettelo aktiivisista pakettimalleista, jotka ovat tarjouksen luojien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="891f3-205">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="891f3-206">Luo uusi tarjouspaketti valitsemalla **Uusi paketti**.</span><span class="sxs-lookup"><span data-stu-id="891f3-206">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="891f3-207">Anna yksilöivä nimi ja valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="891f3-207">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="891f3-208">Valitse **Lisää malli**.</span><span class="sxs-lookup"><span data-stu-id="891f3-208">Click **Add template**.</span></span>

    >[!HUOMAUTUKSET]
    > - <span data-ttu-id="891f3-210">Voit joko luoda uuden mallin tai valita aiemmin luodun mallin.</span><span class="sxs-lookup"><span data-stu-id="891f3-210">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="891f3-211">Jos päätät lisätä aiemmin luodun mallin, sinun on varmistettava, että tarjousasiakirjamalli on tallennettu, viimeistelty ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="891f3-211">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="891f3-212">Voit valita niin monta asiakirjamallia kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="891f3-212">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="891f3-213">Valitse **Valmis**, jonka jälkeen palaat **paketin hallintaan**.</span><span class="sxs-lookup"><span data-stu-id="891f3-213">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="891f3-214">Voit määrittää asiakirjojen järjestyksen sekä merkitä, mitä tiettyä tarjousasiakirjaa on käytettävä tarjousta luotaessa.</span><span class="sxs-lookup"><span data-stu-id="891f3-214">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="891f3-215">Tarjouksen luojalla on mahdollisuus poistaa asiakirjat, joissa on merkintä **Ei pakollinen**.</span><span class="sxs-lookup"><span data-stu-id="891f3-215">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="891f3-216">Tallenna tarjouspakettimalli, jotta se on myös kaikkien muiden tarjouksen luojien käytettävissä, valitsemalla **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="891f3-216">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="891f3-217">Voit tarkastella tarjouspakettimallien luonnoksi valitsemalla **Luonnokset**-välilehden. Jos tarjouspakettimalliin tehdään muutoksia, se on tallennettava ja julkaistava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="891f3-217">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="891f3-218">Tarjousprosessin asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="891f3-218">Configure an offer process</span></span>

<span data-ttu-id="891f3-219">Tarjouksen luontiprosessissa on useita osia, joita Attractin järjestelmänvalvoja voi määrittää.</span><span class="sxs-lookup"><span data-stu-id="891f3-219">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="891f3-220">**Tarjouksen hyväksynnät** – Valitse, onko tarjoukset hyväksyttävä, ennen kuin tarjous voidaan lähettää hakijalle.</span><span class="sxs-lookup"><span data-stu-id="891f3-220">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="891f3-221">Voit järjestelmänvalvojana päättää, tehdäänkö kaikki tarjouksen hyväksynnät peräkkäisessä tai rinnakkaisessa hyväksyntätyönkulussa.</span><span class="sxs-lookup"><span data-stu-id="891f3-221">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="891f3-222">Voit myös määrittää, onko tarjouksen hyväksyjien liitettävä hyväksyntään kommentti.</span><span class="sxs-lookup"><span data-stu-id="891f3-222">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="891f3-223">Tarjouksen hyväksyntä on pakollista kaikissa ei vakiomuotoisissa tarjouksissa.</span><span class="sxs-lookup"><span data-stu-id="891f3-223">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="891f3-224">**Hakijan tarjouskokemus** – Järjestelmänvalvojana voi määrittää, onko kaikille tarjouksilla vanhentumispäivä ja jos on, mikä on vanhentumispäivämäärän oletussiirtymä.</span><span class="sxs-lookup"><span data-stu-id="891f3-224">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="891f3-225">Voit myös määrittää, voiko hakija hylätä tarjouksen.</span><span class="sxs-lookup"><span data-stu-id="891f3-225">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="891f3-226">**Sähköiset allekirjoitukset** – Tällä hetkellä hakijoiden ainoa sähköinen allekirjoitusvaihtoehto on nimen kirjoittaminen tarjouspaketissa tarjouksen hyväksymisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="891f3-226">**e-Signatures** - Currently, the only electronic signature option available is for candidates to type their name in the offer package while accepting the offer.</span></span> <span data-ttu-id="891f3-227">Jatkossa tulemme ottamaan integroimaan kumppanien muita sähköisiä allekirjoituspalveluja.</span><span class="sxs-lookup"><span data-stu-id="891f3-227">We will introduce partner integrations with other electronic signature providers in the future.</span></span>


<span data-ttu-id="891f3-228">Lisätietoja tarjouksen luontiprosessista on kohdassa [Tarjousten luominen, hyväksyminen ja allekirjoittaminen](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="891f3-228">To learn more about the offer creation process, see [Creating, approving, and signing offers](./creating-offers.md).</span></span>

