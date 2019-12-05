---
title: Tarjoustenhallinnan määrittäminen Attractissa
description: Tässä ohjeaiheessa käsitellään tarjousten määrittämistä Microsoft Dynamics 365 Talentissa.
author: andreabichsel
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63f45f1493935f543cfd25a7d8ed7b54170800a0
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832719"
---
# <a name="set-up-offer-management-in-attract"></a><span data-ttu-id="b8189-103">Tarjoustenhallinnan määrittäminen Attractissa</span><span class="sxs-lookup"><span data-stu-id="b8189-103">Set up offer management in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b8189-104">Kun hakija siirretään Dynamics 365 Talent: Attractissa tarjousvaiheeseen, sinun on varmistettava, että tarjoukset luodaan nopeasti hakijalle, hyväksytään tarvittaessa ja lähetetään hakijalle.</span><span class="sxs-lookup"><span data-stu-id="b8189-104">When a candidate is moved to the offer stage in Dynamics 365 Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="b8189-105">Koska useimmat tarjoukset ovat vakiomuotoisia, ne voidaan luoda uudelleenkäytettävistä malleista.</span><span class="sxs-lookup"><span data-stu-id="b8189-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="b8189-106">Attractissa kaikki tarjoukset kerätään tarjouspaketiksi. Se on kokoelma, jossa on vähintään yksi tarjousasiakirja.</span><span class="sxs-lookup"><span data-stu-id="b8189-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="b8189-107">Tässä ohjeaiheessa käsitellään kaikki vaiheet, joita noudattamalla Attractin järjestelmä määrittää erilaisia tarjouspakettimalleja Attractin tarjousten hallintatoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="b8189-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="b8189-108">Jos käyttäjällä ei ole järjestelmänvalvojan rooli, hänellä ei ole näiden toimintojen käyttöoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="b8189-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="b8189-109">Tarjouksen hallintatoiminnot ovat saatavana kattavan työhönottolaajennuksen osana.</span><span class="sxs-lookup"><span data-stu-id="b8189-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="b8189-110">Tarjouksen tiedot</span><span class="sxs-lookup"><span data-stu-id="b8189-110">Offer data</span></span> 

<span data-ttu-id="b8189-111">Tarjouksen tiedot on tarjouspakettimallin pienin yksikkö.</span><span class="sxs-lookup"><span data-stu-id="b8189-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="b8189-112">Tyypillinen tarjous koostuu vakiotekstistä ja arvojoukosta.</span><span class="sxs-lookup"><span data-stu-id="b8189-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="b8189-113">Arvojoukko on ainoa osa, joka voi vaihdella tarjouksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="b8189-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="b8189-114">Tarjouksen luonnissa on tärkeintä, että tarjouksen luoja keskittyy tarjouspakettimallissa olevaan tarjouksen tietojen paikkamerkkiluetteloon.</span><span class="sxs-lookup"><span data-stu-id="b8189-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="b8189-115">Määritä tarjouksen tiedot seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b8189-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="b8189-116">Valitse **Tarjousten hallinta**.</span><span class="sxs-lookup"><span data-stu-id="b8189-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="b8189-117">Laajenna **Kirjasto**-osa vasemmassa siirtymisruudussa ja valitse sitten **Tarjouksen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="b8189-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="b8189-118">**Tarjouksen tiedot** -sivulla on **Ehdokkaan tiedot**- ja **Työn tiedot** -osat.</span><span class="sxs-lookup"><span data-stu-id="b8189-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="b8189-119">Attractissa on muutamia valmiita tarjouksen tietojen paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="b8189-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    
    > <span data-ttu-id="b8189-120">Sivulla on osia, joissa tarjouksen tietojen erilaiset paikkamerkit voidaan järjestää loogisiksi ryhmiksi.</span><span class="sxs-lookup"><span data-stu-id="b8189-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="b8189-121">Nämä osat helpottavat tarjouksen tietojen ylläpitoa ja tietojen täyttämistä tarjouksen luontiprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="b8189-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>

1.  <span data-ttu-id="b8189-122">Voit luoda uuden tarjoustieto-osan valitsemalla **Lisää osa** ja antamalla sille yksilöivä nimen.</span><span class="sxs-lookup"><span data-stu-id="b8189-122">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="b8189-123">Voit lisätä tarjoustietojen paikkamerkin johonkin osaan valitsemalla **Lisää tarjouksen tiedot** ja antamalla paikkamerkille yksilöivän nimen.</span><span class="sxs-lookup"><span data-stu-id="b8189-123">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="b8189-124">Voit muokata minkä tahansa osan nimeä pitämällä osoitinta osan päällä ja päivittämällä nimen.</span><span class="sxs-lookup"><span data-stu-id="b8189-124">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="b8189-125">Voit kyllä muokata aiemmin luodun tarjoustietojen paikkamerkin nimeä, mutta varmista ensin, että paikkamerkkiä ei käytetä missään mallissa.</span><span class="sxs-lookup"><span data-stu-id="b8189-125">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="b8189-126">Siirrä sitten osoitin tarjoustietojen paikkamerkin nimen päälle ja päivitä nimi tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="b8189-126">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="b8189-127">Voit kyllä poistaa aiemmin luodun tarjoustietojen paikkamerkin, mutta varmista ensin, että paikkamerkkiä ei käytetä missään muussa mallissa.</span><span class="sxs-lookup"><span data-stu-id="b8189-127">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="b8189-128">Siirrä sen jälkeen osoitin paikkamerkin päälle. Kun roskakorikuvake tulee näkyviin, poista tarjoustietojen paikkamerkki kuvaketta napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="b8189-128">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="b8189-129">Jokaisen tarjouksen tiedon vieressä on numero, joka ilmaisee, kuinka monessa mallissa tarjoustietojen paikkamerkki on käytössä.</span><span class="sxs-lookup"><span data-stu-id="b8189-129">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="b8189-130">Voit poistaa minkä tahansa osan, siirtämällä osoittimin nimen päälle.</span><span class="sxs-lookup"><span data-stu-id="b8189-130">To delete any section, hover over the name.</span></span> <span data-ttu-id="b8189-131">Jos mitään osan tarjoustietojen paikkamerkkiä ei käytetä missään mallissa, voit poistaa sen roskakorikuvaketta napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="b8189-131">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="b8189-132">Osan poistaminen poistaa myös kaikki tarjoustietojen paikkamerkit kyseisestä osasta.</span><span class="sxs-lookup"><span data-stu-id="b8189-132">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="b8189-133">Kun tarjoustietojen paikkamerkit on määritetty, voit käyttää niitä missä tahansa asiakirjamallissa.</span><span class="sxs-lookup"><span data-stu-id="b8189-133">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="b8189-134">Tarjoustietojen paikkamerkkien käyttöä ei ole rajoitettu tiettyyn malliin, vaan samaa joukkoa voidaan käytätä kaikissa malleissa.</span><span class="sxs-lookup"><span data-stu-id="b8189-134">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="b8189-135">Tarjouksen tietojen säännöt</span><span class="sxs-lookup"><span data-stu-id="b8189-135">Offer data rules</span></span>

<span data-ttu-id="b8189-136">Useimmissa organisaatioissa on tarjousten luontisäännöt.</span><span class="sxs-lookup"><span data-stu-id="b8189-136">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="b8189-137">Organisaatio voi esimerkiksi edellyttää, että tietyn toimipaikan ja tietyn ikälisän yhdistelmänä muodostuva vuosipalkka saa olla enintään tietyn suuruinen tai että uudelle työntekijälle on käytettävissä vain muutamia tarjoustason arvoja.</span><span class="sxs-lookup"><span data-stu-id="b8189-137">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="b8189-138">Attract tukee tällä hetkellä kaikkia tällaisia CSV-tiedostoa käyttäviä tietosääntöjä.</span><span class="sxs-lookup"><span data-stu-id="b8189-138">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="b8189-139">Valmistele tietosääntöjen CSV-tiedosto seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b8189-139">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="b8189-140">Määritä sääntöjoukon tarjoustietojen paikkamerkki.</span><span class="sxs-lookup"><span data-stu-id="b8189-140">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="b8189-141">Esimerkki: **Vuosipalkka**.</span><span class="sxs-lookup"><span data-stu-id="b8189-141">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="b8189-142">Määritä riippuvaiset tarjouksen tietojen paikkamerkkiarvot.</span><span class="sxs-lookup"><span data-stu-id="b8189-142">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="b8189-143">Esimerkki: **Työn sijainti** ja **Taso**.</span><span class="sxs-lookup"><span data-stu-id="b8189-143">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="b8189-144">Määritä sarakkeiksi 1 ja 2 **Työn sijainti** ja **Taso**.</span><span class="sxs-lookup"><span data-stu-id="b8189-144">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="b8189-145">Lataa alueen arvo määrittämällä sarakkeiksi 3 ja 4 **Vuosipalkka**.</span><span class="sxs-lookup"><span data-stu-id="b8189-145">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="b8189-146">Jos haluat ladata tietyn arvon arvoalueen sijaan, määritä vain sarakkeeksi 3 **Vuosipalkka**.</span><span class="sxs-lookup"><span data-stu-id="b8189-146">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="b8189-147">Täytä Microsoft Excel -tiedoston tiedot tarvittavien roolien perusteella.</span><span class="sxs-lookup"><span data-stu-id="b8189-147">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="b8189-148">Varmista, että jokainen rivi on yksilöllinen yhdistelmä kaikista arvoista.</span><span class="sxs-lookup"><span data-stu-id="b8189-148">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="b8189-149">Tallenna tiedosto CSV-muodossa.</span><span class="sxs-lookup"><span data-stu-id="b8189-149">Save the file as a CSV format.</span></span>

<span data-ttu-id="b8189-150">Lataa tarjouksen tietosääntötiedosto seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b8189-150">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="b8189-151">Valitse **Tarjousten hallinta**.</span><span class="sxs-lookup"><span data-stu-id="b8189-151">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="b8189-152">Laajenna **Kirjasto**-osa vasemmassa siirtymisruudussa ja valitse sitten **Tarjouksen tietojen säännöt**.</span><span class="sxs-lookup"><span data-stu-id="b8189-152">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="b8189-153">Valitse **Uusi tietojoukko**, jolloin **Lataa palvelimeen** -valintaikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="b8189-153">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="b8189-154">Määritä sääntöjoukolle yksilöivä nimi ja lataa tallennettu CSV-tiedosto sitten palvelimeen.</span><span class="sxs-lookup"><span data-stu-id="b8189-154">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="b8189-155">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="b8189-155">Click **Add**.</span></span>
    <span data-ttu-id="b8189-156">Sääntöjoukko käsitellään taustalla, ja kun se valmistuu, saat siitä ilmoituksen sovelluksessa ja sähköpostitse.</span><span class="sxs-lookup"><span data-stu-id="b8189-156">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="b8189-157">Saat ilmoituksen, jos latauksen käsittelyssä esiintyi virheitä.</span><span class="sxs-lookup"><span data-stu-id="b8189-157">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="b8189-158">Voit sitten ladata virhelokin, korjata tiedoston ja ladata sen uudelleen palvelimeen.</span><span class="sxs-lookup"><span data-stu-id="b8189-158">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="b8189-159">Käytä ellipsipainiketta (**…**), jos haluat ladata sääntöjoukon ja päivittää arvojoukon.</span><span class="sxs-lookup"><span data-stu-id="b8189-159">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="b8189-160">Lataa tiedosto päivittämisen jälkeen uudelleen palvelimeen.</span><span class="sxs-lookup"><span data-stu-id="b8189-160">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="b8189-161">Voit poistaa palvelimeen ladatun aiemmin luodun sääntöjoukon, jos määritettävää paikkamerkkiä ei käytetä toisessa asiakirjamallissa.</span><span class="sxs-lookup"><span data-stu-id="b8189-161">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="b8189-162">Kullakin paikkamerkillä voi olla vain yksi yksilöllinen sarakejoukko, josta se on riippuvainen.</span><span class="sxs-lookup"><span data-stu-id="b8189-162">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="b8189-163">Jos esimerkki **vuosipalkka** on riippuvainen **työn sijainnista** ja **tasosta**, et voi ladata palvelimeen toista sääntöjoukkoa, jossa **vuosipalkka** on riippuvainen toisenlaisesta sarakejoukosta.</span><span class="sxs-lookup"><span data-stu-id="b8189-163">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="b8189-164">Voit ladata tarjouksen tietojen näytesääntöjoukot **Tarjouksen tietojen säännöt** -sivun **Mallit**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="b8189-164">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="b8189-165">Kun tarjouksen luoja korvaa tarjouksen tietojen sääntöjen suosittelemat arvot, tarjous merkitään muuksi kuin vakiotarjoukseksi ja tarjouksen hyväksyntätyönkulun käyttö on pakollista.</span><span class="sxs-lookup"><span data-stu-id="b8189-165">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="b8189-166">Tiedostomallit</span><span class="sxs-lookup"><span data-stu-id="b8189-166">Document templates</span></span>

<span data-ttu-id="b8189-167">Tarjouksen asiakirjamalli voi auttaa järjestelmänvalvojia luomaan tarjouskirjeitä.</span><span class="sxs-lookup"><span data-stu-id="b8189-167">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="b8189-168">Tarjouksen asiakirjamalli koostuu tekstistä, joka on osa tarjousta, ja määritetyistä tarjoustietojen paikkamerkeistä.</span><span class="sxs-lookup"><span data-stu-id="b8189-168">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="b8189-169">Luo tarjouksen asiakirjamalli seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b8189-169">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="b8189-170">Valitse **Tarjousten hallinta**.</span><span class="sxs-lookup"><span data-stu-id="b8189-170">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="b8189-171">Laajenna **Kirjasto**-osa vasemmassa siirtymisruudussa ja valitse sitten **Mallit**.</span><span class="sxs-lookup"><span data-stu-id="b8189-171">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="b8189-172">Avautuvalla **Mallit**-sivulla on luettelo asiakirjamalleista, jotka on jo määritetty.</span><span class="sxs-lookup"><span data-stu-id="b8189-172">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="b8189-173">Luo uusi asiakirjamalli valitsemalla **Uusi malli**.</span><span class="sxs-lookup"><span data-stu-id="b8189-173">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="b8189-174">Anna mallille yksilöivä nimi ja valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="b8189-174">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="b8189-175">Voit lisätä tai muokata tarjousasiakirjan sisältöä RTF-editorissa.</span><span class="sxs-lookup"><span data-stu-id="b8189-175">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="b8189-176">Voit lisätä tauluja, kuvia ja hyperlinkkejä käyttämällä tekstieditorin yläosassa olevia vaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="b8189-176">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="b8189-177">Voit lisätä tarjoustietojen paikkamerkkien tarjouksen malliasiakirjaan</span><span class="sxs-lookup"><span data-stu-id="b8189-177">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="b8189-178">vetämällä ja pudottamalla oikeasta ruudusta</span><span class="sxs-lookup"><span data-stu-id="b8189-178">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="b8189-179">sijoittamalla tarjoustietojen paikkamerkin suoraan työpaikkaan tunnisteen avulla.</span><span class="sxs-lookup"><span data-stu-id="b8189-179">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="b8189-180">Kirjoita ensin **\#** ja aloita sitten tarjoustietojen paikkamerkin nimen kirjoittaminen.</span><span class="sxs-lookup"><span data-stu-id="b8189-180">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="b8189-181">Vaihtoehdot tulevaa näkyviin avattavana luettelon.</span><span class="sxs-lookup"><span data-stu-id="b8189-181">Options will appear in the drop-down list.</span></span> <span data-ttu-id="b8189-182">Lisää tarjoustietojen paikkamerkki napsauttamalla sitä tai painamalla **Enter**-näppäintä.</span><span class="sxs-lookup"><span data-stu-id="b8189-182">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="b8189-183">Voit liittää paikkamerkin tarjouksen asiakirjamalliin ilman, että hakija näkee sen arvon, siirtämällä osoittimen tarjoustietojen paikkamerkin päälle ja napsauttamalla **Kiinnitä**-kuvaketta.</span><span class="sxs-lookup"><span data-stu-id="b8189-183">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="b8189-184">Paikkamerkki siirretään nyt tarjouksen asiakirjamallin **Kiinnitetyn tarjouksen tiedot** -osaan.</span><span class="sxs-lookup"><span data-stu-id="b8189-184">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="b8189-185">Voit poistaa kiinnityksen toimimalla samalla tavoin mutta valitsemalla **Poista kiinnity** tarjoustietojen paikkamerkkiluettelossa.</span><span class="sxs-lookup"><span data-stu-id="b8189-185">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="b8189-186">Voit tarkastella aktiivisia tarjoustietojen paikkamerkkejä siirtymällä oikeassa ruudussa **Aktiiviset**-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="b8189-186">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="b8189-187">Jos lisää tarjoustietojen sääntöjoukkoa noudattavan paikkamerkin, näet kyseisen tarjoustietojen paikkamerkin riippuvuuden muista arvoista.</span><span class="sxs-lookup"><span data-stu-id="b8189-187">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="b8189-188">Vaihtoehtoisesti voit **tuoda** sisällön paikallisen tiedoston .docx-tiedostosta ja muokata sitä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="b8189-188">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="b8189-189">Tässä tapauksessa sinun ei tarvitsee kirjoittaa kaikkea sisältöä editorissa.</span><span class="sxs-lookup"><span data-stu-id="b8189-189">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="b8189-190">Voit esikatsella tarjousasiakirjaa valitsemalla sivun yläosassa**Esikatselu**-vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="b8189-190">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="b8189-191">Voit hallita, saako tarjouksen luoja muokata tarjousasiakirjan sisältöä valitsemalla sivun yläosassa **Hallitse käyttöoikeutta**.</span><span class="sxs-lookup"><span data-stu-id="b8189-191">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="b8189-192">Jos haluat, että tarjouksen luoja voi vain lisätä paikkamerkin arvot tekstin muokkaamisen sijaan, määritä käyttöoikeuden arvoksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="b8189-192">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="b8189-193">Tallenna eteneminen valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8189-193">Click **Save** to save your progress.</span></span> <span data-ttu-id="b8189-194">Malli tallennetaan luonnoksena.</span><span class="sxs-lookup"><span data-stu-id="b8189-194">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="b8189-195">Viimeistele asiakirja ja merkitse se julkaistuksi valitsemalla **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="b8189-195">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="b8189-196">Näet asiakirjamallikirjaston saapumissivulla, mitkä asiakirjamallit ovat aktiivisia, mitkä luonnostilassa ja mitkä on arkistoitu eikä enää käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b8189-196">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="b8189-197">Voit poistaa tarjousasiakirjamallit, jotka eivät sisälly nykyiseen tarjouspakettimalliin.</span><span class="sxs-lookup"><span data-stu-id="b8189-197">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="b8189-198">Tarjouspakettimallit</span><span class="sxs-lookup"><span data-stu-id="b8189-198">Offer package templates</span></span>

<span data-ttu-id="b8189-199">Tarjouspaketit ovat hakijan kanssa jaettavia tarjouksen tietoja, ja ne koostuvat vähintään yhdestä tarjousasiakirjamallista.</span><span class="sxs-lookup"><span data-stu-id="b8189-199">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="b8189-200">Luo tarjouspaketti seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b8189-200">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="b8189-201">Valitse **Tarjousten hallinta**.</span><span class="sxs-lookup"><span data-stu-id="b8189-201">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="b8189-202">Valitse vasemmassa siirtymisruudussa **Paketit**.</span><span class="sxs-lookup"><span data-stu-id="b8189-202">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="b8189-203">Näkyviin tulee luettelo aktiivisista pakettimalleista, jotka ovat tarjouksen luojien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b8189-203">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="b8189-204">Luo uusi tarjouspaketti valitsemalla **Uusi paketti**.</span><span class="sxs-lookup"><span data-stu-id="b8189-204">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="b8189-205">Anna yksilöivä nimi ja valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="b8189-205">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="b8189-206">Valitse **Lisää malli**.</span><span class="sxs-lookup"><span data-stu-id="b8189-206">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="b8189-207">Voit joko luoda uuden mallin tai valita aiemmin luodun mallin.</span><span class="sxs-lookup"><span data-stu-id="b8189-207">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="b8189-208">Jos päätät lisätä aiemmin luodun mallin, sinun on varmistettava, että tarjousasiakirjamalli on tallennettu, viimeistelty ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="b8189-208">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="b8189-209">Voit valita niin monta asiakirjamallia kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="b8189-209">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="b8189-210">Valitse **Valmis**, jonka jälkeen palaat **paketin hallintaan**.</span><span class="sxs-lookup"><span data-stu-id="b8189-210">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="b8189-211">Voit määrittää asiakirjojen järjestyksen sekä merkitä, mitä tiettyä tarjousasiakirjaa on käytettävä tarjousta luotaessa.</span><span class="sxs-lookup"><span data-stu-id="b8189-211">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="b8189-212">Tarjouksen luojalla on mahdollisuus poistaa asiakirjat, joissa on merkintä **Ei pakollinen**.</span><span class="sxs-lookup"><span data-stu-id="b8189-212">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="b8189-213">Tallenna tarjouspakettimalli, jotta se on myös kaikkien muiden tarjouksen luojien käytettävissä, valitsemalla **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="b8189-213">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="b8189-214">Voit tarkastella tarjouspakettimallien luonnoksi valitsemalla **Luonnokset**-välilehden. Jos tarjouspakettimalliin tehdään muutoksia, se on tallennettava ja julkaistava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="b8189-214">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="b8189-215">Tarjousprosessin asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8189-215">Configure an offer process</span></span>

<span data-ttu-id="b8189-216">Tarjouksen luontiprosessissa on useita osia, joita Attractin järjestelmänvalvoja voi määrittää.</span><span class="sxs-lookup"><span data-stu-id="b8189-216">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="b8189-217">**Tarjouksen hyväksynnät** – Valitse, onko tarjoukset hyväksyttävä, ennen kuin tarjous voidaan lähettää hakijalle.</span><span class="sxs-lookup"><span data-stu-id="b8189-217">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="b8189-218">Voit järjestelmänvalvojana päättää, tehdäänkö kaikki tarjouksen hyväksynnät peräkkäisessä tai rinnakkaisessa hyväksyntätyönkulussa.</span><span class="sxs-lookup"><span data-stu-id="b8189-218">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="b8189-219">Voit myös määrittää, onko tarjouksen hyväksyjien liitettävä hyväksyntään kommentti.</span><span class="sxs-lookup"><span data-stu-id="b8189-219">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="b8189-220">Tarjouksen hyväksyntä on pakollista kaikissa ei vakiomuotoisissa tarjouksissa.</span><span class="sxs-lookup"><span data-stu-id="b8189-220">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="b8189-221">**Hakijan tarjouskokemus** – Järjestelmänvalvojana voi määrittää, onko kaikille tarjouksilla vanhentumispäivä ja jos on, mikä on vanhentumispäivämäärän oletussiirtymä.</span><span class="sxs-lookup"><span data-stu-id="b8189-221">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="b8189-222">Voit myös määrittää, voiko hakija hylätä tarjouksen.</span><span class="sxs-lookup"><span data-stu-id="b8189-222">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="b8189-223">**Sähköiset allekirjoitukset** – Voit järjestelmänvalvojana valita menetelmä, jolla ehdokkaat allekirjoittavat tarjoukset.</span><span class="sxs-lookup"><span data-stu-id="b8189-223">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="b8189-224">Adobe Sign – Kaikki tarjouspaketit lähetetään ja allekirjoitetaan Adobe Signin kautta.</span><span class="sxs-lookup"><span data-stu-id="b8189-224">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="b8189-225">Jokaisella tarjouksen julkaisevalla tekijällä on oltava oma Attractiin yhdistetty Adobe Sign -tili.</span><span class="sxs-lookup"><span data-stu-id="b8189-225">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="b8189-226">Lisätietoja Adobe Sign -käyttöoikeuksista ja maksuttomasta kokeilusta on tässä [linkissä](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span><span class="sxs-lookup"><span data-stu-id="b8189-226">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="b8189-227">DocuSign – Kaikki tarjouspaketit lähetetään ja allekirjoitetaan DocuSignin kautta.</span><span class="sxs-lookup"><span data-stu-id="b8189-227">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="b8189-228">Jokaisella tarjouksen julkaisevalla tekijällä on oltava oma Attractiin yhdistetty DocuSign-tili.</span><span class="sxs-lookup"><span data-stu-id="b8189-228">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="b8189-229">ESign – Tämä oletusasetus on heti käyttövalmis, ja käyttäjä voi allekirjoittaa tarjouksen kirjoittamalla nimensä ja nimikirjaimensa.</span><span class="sxs-lookup"><span data-stu-id="b8189-229">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="b8189-230">Lisätietoja tarjouksen luontiprosessista on kohdassa [Tarjousten luominen, hyväksyminen ja allekirjoittaminen](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="b8189-230">To learn more about the offer creation process, see [Create, approve, and sign offers](./creating-offers.md).</span></span>
