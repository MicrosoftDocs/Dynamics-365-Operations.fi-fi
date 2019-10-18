---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (31. lokakuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d2ad9be740d917a760815718a1473d7bcba97968
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025929"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-31-2018"></a><span data-ttu-id="1ddc4-103">Dynamics 365 Talent: Core HR:n uudet tai muuttuneet ominaisuudet (31. lokakuuta 2018)</span><span class="sxs-lookup"><span data-stu-id="1ddc4-103">What's new or changed in Dynamics 365 Talent: Core HR (October 31, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1ddc4-104">**Koontiversio 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="1ddc4-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="1ddc4-105">Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance"></a><span data-ttu-id="1ddc4-106">Linkkien luonti Talentista Financeen</span><span class="sxs-lookup"><span data-stu-id="1ddc4-106">Create links from Talent to Finance</span></span>
<span data-ttu-id="1ddc4-107">Tällä uudella siirtymistoiminnolla voi muodostaa linkin Talentista Financeen, joten voit siirtyä suoraan Finance-sivuille.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-107">This new navigation functionality allows you to link from Talent to Finance, giving you direct navigation into Finance pages.</span></span> <span data-ttu-id="1ddc4-108">Voit määrittää linkkien määrityksen yhteydessä linkin nimen ja ryhmän, kohdan, jossa linkkiä käytetään Talentissa, ja Financessa avattavan kohdesivun.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="1ddc4-109">Tulossa pian</span><span class="sxs-lookup"><span data-stu-id="1ddc4-109">Coming soon</span></span>
<span data-ttu-id="1ddc4-110">Myöhemmin lisättävä kenttäkonteksti mahdollistaa suoran siirtymisen vastaaviin Financen tietueisiin.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance.</span></span> <span data-ttu-id="1ddc4-111">Voit esimerkiksi antaa **Linkki kenttään** -asetuksella kontekstin, jolla siirrytään suoraan tiettyyn työntekijään tai työpaikkaan Financessa.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="1ddc4-112">Kohdejärjestelmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1ddc4-112">Configure target systems</span></span>

<span data-ttu-id="1ddc4-113">Järjestelmänvalvojat voivat määrittää Talentissa linkit, joita käytetään järjestelmänhallinnan työtilan kautta.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="1ddc4-114">Määrityksen osan muodostavat Finance-ympäristöt, joihin haluat siirtyä linkin kohteena.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-114">Part of the configuration is the Finance environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="1ddc4-115">Se tehdään nimeämällä kohdejärjestelmä ja antamalla Finance-ympäristön URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-115">You do this by giving the target system a name and providing the URL of the Finance environment.</span></span> <span data-ttu-id="1ddc4-116">Esimerkki annettavasta Financen URL-osoitteesta: https://devax00124aos.cloud.test.dynamics.com/.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-116">Here is an example of a Finance URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="1ddc4-117">Kun olet määrittänyt kohdejärjestelmät, voit määrittää linkit.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="1ddc4-118">Määritä linkit</span><span class="sxs-lookup"><span data-stu-id="1ddc4-118">Configure links</span></span>

<span data-ttu-id="1ddc4-119">Jokaiseen luotavaan linkkiin on määritettävä seuraavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="1ddc4-120">Linkki – linkin nimi, jota käytetään vain tunnistamiseen.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="1ddc4-121">Ota tämä linkki käyttöön – valitse **Kyllä**, jos haluat näyttää linkin Talentin käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="1ddc4-122">Näyttönimi – Määritä nimi, joka näkyy Financeen vievänä linkkinä.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-122">Display name - Define the name that will appear as a link to Finance.</span></span> <span data-ttu-id="1ddc4-123">Näitä tietoja ei ole tällä hetkellä käännetty.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="1ddc4-124">Surface-linkki lomakkeessa – valitse sivu, jolla haluat linkin näkyvän.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="1ddc4-125">Ryhmä – ryhmät eivät ole pakollisia, mutta jos haluat järjestää linkit ryhmien avulla, valitse **Ryhmä**-kentässä aiemmin luotu ryhmä tai luo uusi ryhmä.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="1ddc4-126">Kohdejärjestelmä – Valitse kohderyhmä, joka luotiin **Määritä kohdejärjestelmä** -asetuksella.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="1ddc4-127">Se on Finance-ympäristö, jota käytetään siirryttäessä linkin avulla.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-127">This will be the Finance environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="1ddc4-128">Käytä käyttäjän nykyistä yritystä – Valitse **Kyllä**, jos haluat käyttää käyttäjän nykyistä yrityskontekstia Financeen siirryttäessä.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance.</span></span> <span data-ttu-id="1ddc4-129">Jos valitset **Ei**, voit valita käytettävän yrityksen.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="1ddc4-130">Kohdevalikkovaihtoehto – Anna Financen valikkovaihtoehto, jota linkin on käytettävä siirryttäessä.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-130">Target menu item - Enter the menu item from Finance that the link should use when navigating.</span></span> <span data-ttu-id="1ddc4-131">Käytettävissä on ne valikkotoiminnot, joihin voi siirtyä suoraan.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="1ddc4-132">Voit etsiä tarvittavan valikkotoiminnon avaamalla ensin Financen ja sitten sivun, johon siirrytään.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-132">To find the menu item required, open Finance and open the page that is the target of the navigation.</span></span> <span data-ttu-id="1ddc4-133">Kopioi valikkotoiminto URL-osoitteesta.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="1ddc4-134">Jos esimerkiksi haluat, että linkki vie Finance and Operationsin työntekijäluetteloon, anna arvo, joka URL-osoitteessa &mi-kohdan jälkeen.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="1ddc4-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="1ddc4-136">Tässä esimerkissä valikkotoiminto, johon työntekijäluettelosivulla siirrytään on HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="1ddc4-137">Linkki tietolähteeseen – Valitse tietolähde, johon linkki viittaa.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="1ddc4-138">Käytettävissä on tavallisimmat lähteet, kuten **Työntekijä** ja **Toimi**.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="1ddc4-139">Linkki kenttään – (tulossa pian) Tämän kentän valinta mahdollistaa suoran siirtymisen yhdestä Talentin tietueesta yhteen Financen tietueeseen.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="1ddc4-140">Linkkien käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="1ddc4-140">Access to links</span></span>

<span data-ttu-id="1ddc4-141">Järjestelmänvalvojat näkevät juuri luodut linkit määritetyillä sivuilla, vaikka **Ota tämä linkki käyttöön** -asetuksena olisi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="1ddc4-142">Tämä mahdollistaakin linkkien testaamisen, ennen kuin ne ovat muiden työntekijöiden käytössä.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="1ddc4-143">Kaikki muut roolit näkevät määritetyt linkit vasta, kun **Ota tämä linkki käyttöön** -asetuksena on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="1ddc4-144">Työntekijät, joilla on linkit sisältävien sivujen käyttöoikeus, on myös linkkien käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="1ddc4-145">Käyttäjillä voi olla myös Financessa määritettyjä käyttöoikeuksia, jotka koskevat Finance and Operationsin sivujen käyttöoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-145">Users can also have security rights within Finance defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="1ddc4-146">Jos heillä ei niitä ole, linkkiä käytettäessä avautuu suojauksen valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="1ddc4-147">Muut muutokset ja korjaukset</span><span class="sxs-lookup"><span data-stu-id="1ddc4-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="1ddc4-148">Uudelleen työntekijälle ei voi määrittää toimea, jonka aloituspäivä on tulevaisuudessa</span><span class="sxs-lookup"><span data-stu-id="1ddc4-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="1ddc4-149">Tehtyjen muutosten myöstä työntekijälle voidaan määrittää tulevaisuudessa alkava toimi.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="1ddc4-150">Toimet, joiden alkamispäivä on tulevaisuudessa, voidaan valita ja työntekijän määritys tehdään tallennettaessa tai työnkulun päättyessä (jos työnkulku on otettu käyttöön).</span><span class="sxs-lookup"><span data-stu-id="1ddc4-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="1ddc4-151">Uutta työntekijää ei voi määrittää aiemmin luotuun toimeen</span><span class="sxs-lookup"><span data-stu-id="1ddc4-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="1ddc4-152">Tehtyjen muutosten myötä uuden työntekijän määritys voidaan nyt määrittää aiemmin luotuihin toimiin.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="1ddc4-153">Ikälisäpäivä tai toimiston sijainti katoaa, kun työsuhteen alkamispäivä on menneisyydessä ja tietue tallennetaan</span><span class="sxs-lookup"><span data-stu-id="1ddc4-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="1ddc4-154">Tehtyjen muutosten myötä **Ikälisäpäivä** ja **Toimiston sijainti** näkyvät nyt oikein, kun entisten työntekijöiden muutokset tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="1ddc4-155">Työntekijän sivulla ei voi antaa tulevaisuuteen päivättyjä työsuhteita</span><span class="sxs-lookup"><span data-stu-id="1ddc4-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="1ddc4-156">Tulevaisuuteen päivättyjen työsuhteiden työsuhdetiedot on poistettu käytöstä työntekijän pääsivulla.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="1ddc4-157">Työnsuhdetiedot voidaan antaa **Päivämäärän hallinta** -sivuilla.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="1ddc4-158">Tulevissa versioissa tehdään lisää muutoksia, jotta työsuhdetiedot voidaan tehdä suoraan työnkulkuprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="1ddc4-159">ValidFrom ja ValidTo HcmPersonalContactPersonEntity lisätty</span><span class="sxs-lookup"><span data-stu-id="1ddc4-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="1ddc4-160">Data Management Framework (DMF) -yksikkö HcmPersonalContactPersonEntity on päivitetty sisältämään voimassaolon alkamis- ja päättymispäivät, jotta tietyt etujen integrointiskenaariot voidaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="1ddc4-161">Tunnettu ongelma</span><span class="sxs-lookup"><span data-stu-id="1ddc4-161">Known issue</span></span>
- <span data-ttu-id="1ddc4-162">**Ongelma**: kun työntekijään lisätään uusi liite, **Uusi**- ja **Muokkaa**-painikkeet näkyvät harmaina.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="1ddc4-163">**Ongelman kiertäminen:** Varmista ennen liitesivun avaamista, että **Työntekijä**-sivun tietoruudut on suljettu.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="1ddc4-164">Jos tietoruudut ovat suljettuja **Työntekijä**-sivua ladattaessa, liitepainikkeet otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="1ddc4-165">(Tämä ongelma korjataan seuraavassa ympäristöpäivityksessä.)</span><span class="sxs-lookup"><span data-stu-id="1ddc4-165">(This issue will be fixed in the next platform update.)</span></span>
