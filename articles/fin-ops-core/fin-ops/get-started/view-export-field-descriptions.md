---
title: Kenttien kuvausten tarkasteleminen ja vieminen
description: Tässä artikkelissa käsitellään kenttien kuvauksien näyttämistä ja kuvauksien tuomista Kenttien kuvaus -sivun avulla.
author: rschloma
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0e4bba6524f225d614ffdab370f2a1993cb3a29
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754677"
---
# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="801b8-103">Kenttien kuvausten tarkasteleminen ja vieminen</span><span class="sxs-lookup"><span data-stu-id="801b8-103">View and export field descriptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="801b8-104">Tässä artikkelissa käsitellään kenttien kuvauksien näyttämistä ja kuvauksien tuomista Kenttien kuvaus -sivun avulla.</span><span class="sxs-lookup"><span data-stu-id="801b8-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="801b8-105">Joillakin monimutkaisimmilla kentillä on kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="801b8-105">Some of the more complex fields have field descriptions.</span></span> <span data-ttu-id="801b8-106">Nämä kuvaukset tulevat näkyviin, kun pidät hiiren osoitinta kentän päällä.</span><span class="sxs-lookup"><span data-stu-id="801b8-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="801b8-107">Voit myös tarkastella ja viedä kuvauksia **Kentän kuvaukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="801b8-107">You can also view and export descriptions on the **Field descriptions** page.</span></span>

<span data-ttu-id="801b8-108">Kaikilla sivuilla ei ole kentän kuvauksia.</span><span class="sxs-lookup"><span data-stu-id="801b8-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="801b8-109">Vain monimutkaisilla kentillä on kuvaukset; kuvauksia ei ole kentillä, joiden käyttö on selkeää.</span><span class="sxs-lookup"><span data-stu-id="801b8-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="801b8-110">Tämän vuoksi joillakin sivuilla ei ole lainkaan kenttäkuvauksia, joillakin sivuilla on muutamia kuvauksia ja joillakin monimutkaisilla sivuilla, kuten monilla parametrisivulla, on useita kuvauksia.</span><span class="sxs-lookup"><span data-stu-id="801b8-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span>

<span data-ttu-id="801b8-111">Voit lisätä halutessasi uusia kenttien kuvauksia ja mukauttaa valmiita kuvauksia, jos sinulla on kehitysympäristön käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="801b8-111">If you have access to the development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="801b8-112">Voit esimerkiksi lisätä yrityskohtaiset tiedot kentän kuvaukseen.</span><span class="sxs-lookup"><span data-stu-id="801b8-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="801b8-113">Lisätietoja on kohdassa [Kenttien kuvausten mukauttaminen](../../dev-itpro/user-interface/customize-field-help.md).</span><span class="sxs-lookup"><span data-stu-id="801b8-113">For more information, see [Customize field descriptions](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="801b8-114">Lisätietoja on käyttöliittymän kenttien kuvauksissa.</span><span class="sxs-lookup"><span data-stu-id="801b8-114">See field descriptions in the user interface</span></span>

<span data-ttu-id="801b8-115">Voit tarkastella kentän kuvauksia asettamalla hiiren osoittimen kentän päälle.</span><span class="sxs-lookup"><span data-stu-id="801b8-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="801b8-116">Jos kuvausta ei ole, kentän nimi tulee näkyviin, kun pidät hiiren osoitinta kentän päällä.</span><span class="sxs-lookup"><span data-stu-id="801b8-116">If no description is available, you see the field name when you hover over the field.</span></span>

> [!NOTE]
> <span data-ttu-id="801b8-117">Kenttien kuvauksia voidaan tarkastella Dynamics AX 7.0:ssa (helmikuu 2016) vain **Kenttien kuvaukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="801b8-117">In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.</span></span>

<span data-ttu-id="801b8-118">Seuraavassa kuvassa on kentän kuvaus, joka tulee näkyviin, kun pidät hiiren osoitinta **Lukitse nimikkeet inventoinnin ajaksi** -kentän päällä.</span><span class="sxs-lookup"><span data-stu-id="801b8-118">The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span>

<span data-ttu-id="801b8-119">[![Esimerkki kentän kuvauksesta](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="801b8-119">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="801b8-120">Tarkastele kentän ohjetta ja vie ohje Kenttien kuvaukset -sivulla</span><span class="sxs-lookup"><span data-stu-id="801b8-120">Use the Field descriptions page to view and export field help</span></span>

<span data-ttu-id="801b8-121">Voit tarkastella ja viedä **Kenttien kuvaukset** -sivulla kenttien kuvauksia.</span><span class="sxs-lookup"><span data-stu-id="801b8-121">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="801b8-122">Voit tarkastella kuvauksia, jotka ovat käytettävissä yhdelle sivulle kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="801b8-122">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="801b8-123">Näytä sivun kuvaukset</span><span class="sxs-lookup"><span data-stu-id="801b8-123">View the descriptions for a page</span></span>

<span data-ttu-id="801b8-124">Tarkastele sivun kuvauksia seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="801b8-124">To view the descriptions for a page, follow this step.</span></span>

- <span data-ttu-id="801b8-125">Kirjoita sivun nimi **Valitse sivu** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="801b8-125">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="801b8-126">Voit vaihtoehtoisesti avata kaikkien sivujen luettelon napsauttamalla nuolta ja selaamalla tai suodattamalla sitten luetteloa.</span><span class="sxs-lookup"><span data-stu-id="801b8-126">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="801b8-127">Voit käyttää joko käyttöliittymässä näkyvää nimeä (kuten **Asiakkaat**) tai koodinimeä, (AOT-nimeä), joka on käytettävissä, kun napsautat sivua hiiren kakkospainikkeella (kuten **CustTable**).</span><span class="sxs-lookup"><span data-stu-id="801b8-127">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span>

<span data-ttu-id="801b8-128">Lisätietoja sivuluettelon suodattimesta on myöhemmin tässä artikkelissa kohdassa Sivun haku.</span><span class="sxs-lookup"><span data-stu-id="801b8-128">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span>

<span data-ttu-id="801b8-129">Jos valitset **Sisällytä kenttiä ilman kuvaus** -asetukseksi **Kyllä**, kaikki sivun kentät näytetään, vaikka niillä ei olisi kuvausta.</span><span class="sxs-lookup"><span data-stu-id="801b8-129">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="801b8-130">Tuo sivun kuvaukset</span><span class="sxs-lookup"><span data-stu-id="801b8-130">Export the descriptions for a page</span></span>

<span data-ttu-id="801b8-131">Voit viedä sivun kuvauksia toimimalla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="801b8-131">To export the descriptions for a page, follow these steps.</span></span>

1. <span data-ttu-id="801b8-132">Valitse sivu **Valitse sivu** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="801b8-132">In the **Select a page** field, select a page.</span></span>
2. <span data-ttu-id="801b8-133">Napsauta **Avaa Microsoft Officessa** -painiketta oikeassa yläkulmassa ja valitse sitten **FieldDescriptionTmp**.</span><span class="sxs-lookup"><span data-stu-id="801b8-133">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="801b8-134">Hakemassa sivua</span><span class="sxs-lookup"><span data-stu-id="801b8-134">Searching for a page</span></span>

<span data-ttu-id="801b8-135">Voit etsiä sivua usealla eri tavalla **Valitse sivu** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="801b8-135">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="801b8-136">Usein avattava luettelo on avattava napsauttamalla **Valitse sivu** -kentässä nuolta ja tehtävä sitten valinta suodatetusta sivuluettelosta.</span><span class="sxs-lookup"><span data-stu-id="801b8-136">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

- <span data-ttu-id="801b8-137">Voit kirjoittaa nimen osittain ja tehdä sitten valinnan avattavassa luettelossa suodatetusta sivuluettelosta.</span><span class="sxs-lookup"><span data-stu-id="801b8-137">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
- <span data-ttu-id="801b8-138">Avaa avattava luettelo ja valitse sitten joko **Sivun nimi** -otsikko luettelon alussa tai **Sivu AOT-nimi** -otsikko.</span><span class="sxs-lookup"><span data-stu-id="801b8-138">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="801b8-139">Voit käyttää avattavassa valintaikkunassa suodatuksen lisäasetuksia, kuten asetusta **Sivun nimi alkaa**.</span><span class="sxs-lookup"><span data-stu-id="801b8-139">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
- <span data-ttu-id="801b8-140">Kirjoita sivun kokonainen nimi.</span><span class="sxs-lookup"><span data-stu-id="801b8-140">Type the full name of the page.</span></span> <span data-ttu-id="801b8-141">Jos käytät tätä asetusta, avattava luettelo kannattaa avata ja katsoa, mitä muuta luettelossa on, vaikka kenttien kuvaukset ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="801b8-141">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>

    - <span data-ttu-id="801b8-142">Jos on yksi nimi tarkka vastine, kyseisen sivun kenttien kuvaukset näkyvät.</span><span class="sxs-lookup"><span data-stu-id="801b8-142">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    - <span data-ttu-id="801b8-143">Jos tarkkoja vastineita on useita, kuvauksia ei näytetä.</span><span class="sxs-lookup"><span data-stu-id="801b8-143">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="801b8-144">Avaa avattava luettelo ja valitse sopiva sivu.</span><span class="sxs-lookup"><span data-stu-id="801b8-144">You must open the drop-down list and select the page that you want.</span></span>
    - <span data-ttu-id="801b8-145">Jos kirjoittamasi nimi on toisen sivun nimen osa, näet sivun kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="801b8-145">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="801b8-146">Jos kuitenkin avaat avattavan luettelon, näkyvissä on lisää nimen sisältäviä sivuja.</span><span class="sxs-lookup"><span data-stu-id="801b8-146">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="801b8-147">Kuvauksia ei esimerkiksi näytetä, jos kirjoitat **Inventointi** **Valitse sivu** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="801b8-147">For example, no descriptions are shown when you type **Counting** in the **Select a page** field.</span></span> <span data-ttu-id="801b8-148">Kun avaat luettelon näet, että kahdella sivulla on nimi **Inventointi** ja inventointi-sana on useiden sivujen nimessä.</span><span class="sxs-lookup"><span data-stu-id="801b8-148">You open the drop-down list, and see that there are two pages that have the name **Counting** and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="801b8-149">Jos valitset sivun, jonka AOT-nimi on **InventJournalCount**, kyseisen sivun kenttien kuvaukset näytetään.</span><span class="sxs-lookup"><span data-stu-id="801b8-149">If you select the page that has the AOT name **InventJournalCount**, the field descriptions are shown for that page.</span></span> <span data-ttu-id="801b8-150">Jos kuitenkin avaat avattavan luettelon uudelleen, näet, että luettelo sisältää nyt kaikki sivut, joiden AOT-nimeen InventJournalCount sisältyy.</span><span class="sxs-lookup"><span data-stu-id="801b8-150">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="801b8-151">Vianmääritys</span><span class="sxs-lookup"><span data-stu-id="801b8-151">Troubleshooting</span></span>

<span data-ttu-id="801b8-152">Tässä osassa on tietoja, jotka on sellaisten ongelmien vianmäärityksessä, joita voi tulla esiin kenttien kuvauksia käytettäessä.</span><span class="sxs-lookup"><span data-stu-id="801b8-152">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="801b8-153">Kentän kuvausta ei löydy.</span><span class="sxs-lookup"><span data-stu-id="801b8-153">I can't find a field description</span></span>

<span data-ttu-id="801b8-154">Monimutkaisempia kenttiä varten lisätään parhaillaan kuvauksia.</span><span class="sxs-lookup"><span data-stu-id="801b8-154">We're in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="801b8-155">Jos tarvitset tiettyä kenttää koskevaa apua, ilmoita siitä meille lisäämällä kommentti tähän aiheeseen.</span><span class="sxs-lookup"><span data-stu-id="801b8-155">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="801b8-156">Kuvauksen kentästä ei ole apua</span><span class="sxs-lookup"><span data-stu-id="801b8-156">The field description isn't helpful</span></span>

<span data-ttu-id="801b8-157">Ilmoita meille lisäämällä kommentti tähän aiheeseen.</span><span class="sxs-lookup"><span data-stu-id="801b8-157">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="801b8-158">Jos mahdollista, kerro, mitä lisätietoja tarvitset.</span><span class="sxs-lookup"><span data-stu-id="801b8-158">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="801b8-159">En löydä kenttää Kenttien kuvaukset -sivulla</span><span class="sxs-lookup"><span data-stu-id="801b8-159">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="801b8-160">Voit näyttää kaikki kentät sivulla, kun määrität **Sisällytä kentät, joihin ei liity kuvausta** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="801b8-160">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="801b8-161">Varmista, että olet valinnut oikean sivun valitsemalla **Valitse sivu** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="801b8-161">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="801b8-162">Jos kirjoittamasi nimi on toisen kentän nimeä, olet ehkä valinnut sivun, jonka nimi on pidempi.</span><span class="sxs-lookup"><span data-stu-id="801b8-162">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="801b8-163">En löydä sivua Kenttien kuvaukset -sivulla</span><span class="sxs-lookup"><span data-stu-id="801b8-163">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="801b8-164">Lisätietoja erilaisista sivujen etsimistavoista on aiemmin tässä artikkelissa kohdassa Sivujen etsiminen.</span><span class="sxs-lookup"><span data-stu-id="801b8-164">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="801b8-165">Jos kirjoitit sivun tarkan nimen, kentän kuvauksia ei ehkä näytetä, jos usealla sivulla on sama nimi.</span><span class="sxs-lookup"><span data-stu-id="801b8-165">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="801b8-166">Avaa suodatettu luettelo käytettävissä olevista sivuista napsauttamalla **Valitse sivu** -kentän nuolta.</span><span class="sxs-lookup"><span data-stu-id="801b8-166">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="801b8-167">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="801b8-167">Additional resources</span></span>

[<span data-ttu-id="801b8-168">Kenttien kuvausten mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="801b8-168">Customize field descriptions</span></span>](../../dev-itpro/user-interface/customize-field-help.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]