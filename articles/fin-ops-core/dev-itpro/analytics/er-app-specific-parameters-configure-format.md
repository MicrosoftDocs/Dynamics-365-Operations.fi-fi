---
title: ER-muotojen määrittäminen käyttämään yrityskohtaisesti määritettyjä parametreja
description: Tässä ohjeaiheessa käsitellään sähköisen raportoinnin (ER) muotojen määrittämistä siten, että ne käyttävät yrityskohtaisesti määritettyjä parametreja.
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: d32da76ee46ff5293ae8fefb16d251564b6be21a
ms.sourcegitcommit: d6196d83c7b9166ddb4fe43a91e6bd0ad9da2099
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/31/2019
ms.locfileid: "2694243"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="58ad5-103">ER-muotojen määrittäminen käyttämään yrityskohtaisesti määritettyjä parametreja</span><span class="sxs-lookup"><span data-stu-id="58ad5-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="58ad5-104">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="58ad5-104">Overview</span></span>

<span data-ttu-id="58ad5-105">Monissa suunniteltavissa sähköisen raportoinnin (ER) muodoissa tiedot on suodatettava käyttämällä esiintymän yrityskohtaista arvojoukkoa (kuten verokoodijoukkoa verotapahtumien suodattamiseen).</span><span class="sxs-lookup"><span data-stu-id="58ad5-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="58ad5-106">Jos tällainen suodatustyyppi on määritetty ER-muodossa, yrityksestä riippuvaisia arvoja (kuten verokoodeja) käytetään tällä hetkellä ER-muodon lausekkeissa määrittämään tiedon suodatussäännöt.</span><span class="sxs-lookup"><span data-stu-id="58ad5-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="58ad5-107">Niinpä ER-muoto on yrityskohtainen ja tarvittavien raporttien muodostaminen edellyttää, että alkuperäisestä ER-muodosta luodaan johdettu kopio kullekin yritykselle, jossa ER-muoto on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="58ad5-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="58ad5-108">Niinpä kutakin johdettua ER-muotoa on muokattava yrityskohtaisten arvojen tuontia varten, sen perusta on uusittava aina, kun alkuperäisinen (perus)versio on päivitetty, se on vietävä testiympäristöstä ja tuotava tuotantoympäristöön, jossa on otettava tuotantokäyttöön, ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="58ad5-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="58ad5-109">Tämän vuoksi on useita syitä, miksi tällaisen määritetyn ER-ratkaisun ylläpito on monimutkaista ja vie paljon aikaa:</span><span class="sxs-lookup"><span data-stu-id="58ad5-109">Therefore, maintenance of this type of configured ER solution is quite complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="58ad5-110">Mitä useampia yrityksiä on, sittä useampia ER-muotomäärityksiä on ylläpidettäviä.</span><span class="sxs-lookup"><span data-stu-id="58ad5-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="58ad5-111">ER-määritysten ylläpito edellyttää yrityskäyttäjät osaavat käyttää sähköistä raportointia.</span><span class="sxs-lookup"><span data-stu-id="58ad5-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="58ad5-112">Sovelluskohtaisten ER-parametrien avulla tehokäyttäjät voivat määrittää ER-muodon tietojen suodattamisen abstraktin sääntöjoukon perusteella.</span><span class="sxs-lookup"><span data-stu-id="58ad5-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="58ad5-113">Tämä sääntöjoukko voidaan määrittää käyttämään ER-muodossa käytettävissä olevia tietolähteitä.</span><span class="sxs-lookup"><span data-stu-id="58ad5-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="58ad5-114">Yrityskäyttäjät voivat sitten määrittää ER-kehyksen ulkopuolelle ulottuvia todellisia sääntöjä käyttöliittymässä, joka muodostetaan automaattisesti. Se perustuu vastaavan ER-muodon asetuksiin ja niihin valitun yrityksen tietoihin, joita ER-muodon tietolähteet käyttävät.</span><span class="sxs-lookup"><span data-stu-id="58ad5-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="58ad5-115">ER-muodolle määritetty sääntöjoukko voidaan viedä Dynamics 365 Finance (Finance) -esiintymän nykyisestä yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="58ad5-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="58ad5-116">Se voidaan sitten tuoda joko saman Finance-esiintymän toiseen yritykseen tai toiseen esiintymään saman ER-muodon sääntöjoukkona.</span><span class="sxs-lookup"><span data-stu-id="58ad5-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="58ad5-117">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="58ad5-117">Prerequisites</span></span>

<span data-ttu-id="58ad5-118">Tämän ohjeaiheen esimerkkien käyttämistä varten tarvitset Regulatory Configuration Services (RCS) -esiintymän, joka on valmisteltu samalle vuokraajalle kuin Finance ja jossa roolina on jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="58ad5-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="58ad5-119">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="58ad5-119">Electronic reporting developer</span></span>
- <span data-ttu-id="58ad5-120">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="58ad5-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="58ad5-121">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="58ad5-121">System administrator</span></span>

<span data-ttu-id="58ad5-122">Ohjeaiheen [LASKETTU KENTTÄ -tyyppisten ER-tietolähteiden parametrisoitujen kutsujen tuki](er-calculated-field-type.md) vaiheiden suorittaminen on suositeltavaa.</span><span class="sxs-lookup"><span data-stu-id="58ad5-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="58ad5-123">Jos olet jo tehnyt kyseiset vaiheet, voit ohittaa seuraavan osan, **ER-määritysten tuonti RCS:ään**, vaiheet.</span><span class="sxs-lookup"><span data-stu-id="58ad5-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="58ad5-124">ER-määritysten tuonti RCS:ään</span><span class="sxs-lookup"><span data-stu-id="58ad5-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="58ad5-125">Lataa [Microsoft Download Centerissä](https://go.microsoft.com/fwlink/?linkid=851448) zip-tiedosto **LASKETTU KENTTÄ -tyyppisten ER-tietolähteiden parametrisoitujen kutsujen tuki**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-125">From [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=851448), download the **Support parameterized calls of ER data sources of CALCULATED FIELD type** zip file.</span></span> <span data-ttu-id="58ad5-126">Tämä zip-tiedosto sisältää seuraavat ER-määritykset, jotka on purettava ja tallennettava paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="58ad5-126">This zip file contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="58ad5-127">**Sisällön kuvaus**</span><span class="sxs-lookup"><span data-stu-id="58ad5-127">**Content description**</span></span>                        | <span data-ttu-id="58ad5-128">**Tiedostonimi**</span><span class="sxs-lookup"><span data-stu-id="58ad5-128">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="58ad5-129">**ER-tietomallin** määritystiedostoesimerkki</span><span class="sxs-lookup"><span data-stu-id="58ad5-129">Sample **ER data model** configuration file</span></span>    | <span data-ttu-id="58ad5-130">Model to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="58ad5-130">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="58ad5-131">**ER-metatietojen** määritystiedostoesimerkki</span><span class="sxs-lookup"><span data-stu-id="58ad5-131">Sample **ER metadata** configuration file</span></span>      | <span data-ttu-id="58ad5-132">Metadata to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="58ad5-132">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="58ad5-133">**ER-mallin yhdistämismäärityksen** määritystiedostoesimerkki</span><span class="sxs-lookup"><span data-stu-id="58ad5-133">Sample **ER model mapping** configuration file</span></span> | <span data-ttu-id="58ad5-134">Mapping to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="58ad5-134">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="58ad5-135">**ER-muodon** määritysesimerkki</span><span class="sxs-lookup"><span data-stu-id="58ad5-135">Sample **ER format** configuration</span></span>             | <span data-ttu-id="58ad5-136">Format to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="58ad5-136">Format to learn parameterized calls.version.1.1.xml</span></span>  |

<span data-ttu-id="58ad5-137">Kirjaudu seuraavaksi RCS-esiintymään.</span><span class="sxs-lookup"><span data-stu-id="58ad5-137">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="58ad5-138">Tässä esimerkissä luodaan määritys esimerkkiyritykselle Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="58ad5-138">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="58ad5-139">Ennen menettelyn suorittamista sinun on suoritettava RCS:n ohjeaiheen [Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) vaiheet.</span><span class="sxs-lookup"><span data-stu-id="58ad5-139">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="58ad5-140">Valitse oletuskoontinäytössä **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-140">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="58ad5-141">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-141">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="58ad5-142">Tuo aiemmin RCS:ään ladatut ER-määritykset seuraavassa järjestyksessä: tietomalli, metatiedot, mallin yhdistämismääritys ja muoto.</span><span class="sxs-lookup"><span data-stu-id="58ad5-142">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="58ad5-143">Luo kukin ER-määritys seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="58ad5-143">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="58ad5-144">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-144">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="58ad5-145">Valitse **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-145">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="58ad5-146">Valitse tarvittava XML-muotoinen ER-määritystiedosto valitsemalla **Selaa**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-146">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="58ad5-147">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-147">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="58ad5-148">Annetun ER-ratkaisun tarkastelu</span><span class="sxs-lookup"><span data-stu-id="58ad5-148">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="58ad5-149">Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.</span><span class="sxs-lookup"><span data-stu-id="58ad5-149">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="58ad5-150">Valitse **Parametrisoitujen kutsujen oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-150">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="58ad5-151">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-151">Select **Designer**.</span></span>
4.  <span data-ttu-id="58ad5-152">Valitse **Laajenna/kutista**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-152">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="58ad5-153">**Parametrisoitujen kutsujen oppimismuoto** -ER-muoto on suunniteltu muodostamaan XML-muotoinen veroilmoitus, joka sisältää useita verotustasoja (normaali, alennettu ja ei mitään).</span><span class="sxs-lookup"><span data-stu-id="58ad5-153">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="58ad5-154">Tasoilla olevien yksityiskohtien määrä vaihtelee.</span><span class="sxs-lookup"><span data-stu-id="58ad5-154">Each level has a different number of details.</span></span>

    ![ER-toiminnon suunnittelutoiminnon sivu](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="58ad5-156">Laajenna **Yhdistämismääritys**-välilehdessä **Malli**, **Tiedot** ja **Yhteenveto**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-156">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="58ad5-157">**Model.Data.Summary**-tietolähde palauttaa verotapahtumien luettelon.</span><span class="sxs-lookup"><span data-stu-id="58ad5-157">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="58ad5-158">Tapahtumien yhteenveto tehdään verokoodin mukaan.</span><span class="sxs-lookup"><span data-stu-id="58ad5-158">These transactions are summarized by tax code.</span></span> <span data-ttu-id="58ad5-159">Tässä tietolähteessä laskettu **Model.Data.Summary.Level**-kenttä on määritetty palauttamaan kunkin summatun tietueen verotason koodin.</span><span class="sxs-lookup"><span data-stu-id="58ad5-159">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="58ad5-160">Jos verokoodi voidaan noutaa suorituksenaikaisesti **Model.Data.Summary**-tietolähteestä, laskettu kenttä sisältää verotustason koodin (**Normaali**, **Alennettu**, **Ei mitään** tai **Muu**) tekstiarvona.</span><span class="sxs-lookup"><span data-stu-id="58ad5-160">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="58ad5-161">Lasketun **Model.Data.Summary.Level**-kentän avulla suodatetaan **Model.Data.Summary**-tietolähteen tietueet ja annetaan suodatetut tiedot kussakin verotason ilmaisevassa XML-elementissä käyttämällä kenttiä **Model.Data2.Level1**, **Model.Data2.Level2** ja **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-161">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![ER-toiminnon suunnittelutoiminnon sivu](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="58ad5-163">Laskettu **Model.Data.Summary.Level**-kenttä on määritetty sisältämään ER-lauseke.</span><span class="sxs-lookup"><span data-stu-id="58ad5-163">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="58ad5-164">Huomaa, että verokoodit (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** ja **InVAT0**) on koodattu pysyvästi tähän määritykseen.</span><span class="sxs-lookup"><span data-stu-id="58ad5-164">Note that tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="58ad5-165">Tämän vuoksi tämä ER-muoto määräytyy sen yrityksen mukaan, jossa nämä verokoodit on määritetty.</span><span class="sxs-lookup"><span data-stu-id="58ad5-165">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![ER-toiminnon suunnittelutoiminnon sivu](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="58ad5-167">Toimi seuraavasti, jos haluat, että kussakin yrityksessä tuetaan eri verokoodijoukkoa:</span><span class="sxs-lookup"><span data-stu-id="58ad5-167">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="58ad5-168">Luo kullekin yritykselle ER-muodon johdettu versio.</span><span class="sxs-lookup"><span data-stu-id="58ad5-168">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="58ad5-169">Päivitä lasketun **Model.Data.Summary.Level**-kentän verokoodit yrityksen asetuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="58ad5-169">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="58ad5-170">Sulje **Muodon suunnittelija** -sivu.</span><span class="sxs-lookup"><span data-stu-id="58ad5-170">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="58ad5-171">Johdetun luominen</span><span class="sxs-lookup"><span data-stu-id="58ad5-171">Create a derived format</span></span>

<span data-ttu-id="58ad5-172">Voit sitten tukea samassa ER-muodossa yrityskohtaisia verokoodijoukkoja käyttämällä sovelluskohtaisia ER-parametreja.</span><span class="sxs-lookup"><span data-stu-id="58ad5-172">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="58ad5-173">Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.</span><span class="sxs-lookup"><span data-stu-id="58ad5-173">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="58ad5-174">Valitse **Parametrisoitujen kutsujen oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-174">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="58ad5-175">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-175">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="58ad5-176">Valitse **Johdettu nimestä: Parametrisoitujen kutsujen oppimismuoto, Microsoft** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="58ad5-176">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="58ad5-177">Kirjoita **Nimi**-kenttään **LE-tietojen haun oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-177">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="58ad5-178">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-178">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="58ad5-179">Johdetun muodon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="58ad5-179">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="58ad5-180">Muodon luetteloinnin lisääminen</span><span class="sxs-lookup"><span data-stu-id="58ad5-180">Add a format enumeration</span></span>

<span data-ttu-id="58ad5-181">Seuraavaksi lisätään uusi ER-muodon luettelointi.</span><span class="sxs-lookup"><span data-stu-id="58ad5-181">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="58ad5-182">Tämän muodon luetteloinnin arvot näytetään yrityskäyttäjille, jotka määrittävät ER-muodossa käytettäville eri verotustasoille yrityskohtaiset verokoodijoukot.</span><span class="sxs-lookup"><span data-stu-id="58ad5-182">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="58ad5-183">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-183">Select **Designer**.</span></span>
2.  <span data-ttu-id="58ad5-184">Valitse **Muodon luetteloinnit**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-184">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="58ad5-185">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-185">Select **Add**.</span></span>
4.  <span data-ttu-id="58ad5-186">Kirjoita **Nimi**-kenttään **Verotustasojen luettelo**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-186">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="58ad5-187">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-187">Select **Save**.</span></span>
6.  <span data-ttu-id="58ad5-188">Valitse **Muodon luettelointiarvot** -välilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-188">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="58ad5-189">Kirjoita **Nimi**-kenttään **Normaali verotus**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-189">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="58ad5-190">Valitse **Lisää** uudelleen.</span><span class="sxs-lookup"><span data-stu-id="58ad5-190">Select **Add** again.</span></span>
9.  <span data-ttu-id="58ad5-191">Kirjoita **Nimi**-kenttään **Alennettu verotus**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-191">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="58ad5-192">Valitse **Lisää** uudelleen.</span><span class="sxs-lookup"><span data-stu-id="58ad5-192">Select **Add** again.</span></span>
11. <span data-ttu-id="58ad5-193">Kirjoita **Nimi**-kenttään **Ei verotusta**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-193">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="58ad5-194">Valitse **Lisää** uudelleen.</span><span class="sxs-lookup"><span data-stu-id="58ad5-194">Select **Add** again.</span></span>
13. <span data-ttu-id="58ad5-195">Kirjoita **Nimi**-kenttään **Muu**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-195">In the **Name** field, enter **Other**.</span></span>

    ![ER-toiminnon suunnittelutoiminnon sivu](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="58ad5-197">Koska yrityskäyttäjät voivat käyttää eri kieliä yrityskohtaisten verokoodijoukkojen määrittämiseen, tämän luetteloinnin arvot kannattaa kääntää niille kielille, jotka on määritetty kyseisten käyttäjien ensisijaisiksi kieliksi Financessa.</span><span class="sxs-lookup"><span data-stu-id="58ad5-197">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="58ad5-198">Valitse **Ei verotusta** -tietue.</span><span class="sxs-lookup"><span data-stu-id="58ad5-198">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="58ad5-199">Napsauta **Otsikko**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="58ad5-199">Click in the **Label** field.</span></span>
16. <span data-ttu-id="58ad5-200">Valitse **Käännä**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-200">Select **Translate**.</span></span>
17. <span data-ttu-id="58ad5-201">Kirjoita **Tekstin käännös** -ruudun **Otsikon tunnus** -kenttään **LBL_LEVELENUM_NO**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-201">In the **Text translation** pane, in the **Label Id** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="58ad5-202">Kirjoita **Teksti oletuskielellä** -kenttään **No taxation**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-202">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="58ad5-203">Valitse **Kieli**-kentässä **FI**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-203">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="58ad5-204">Kirjota **Käännetty teksti** -kenttään **Ei verotusta**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-204">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="58ad5-205">Valitse **Käännä**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-205">Select **Translate**.</span></span>

    ![ER-toiminnon suunnittelutoiminnon sivu](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="58ad5-207">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-207">Select **Save**.</span></span>
23. <span data-ttu-id="58ad5-208">Sulje **Muodon luetteloinnit** -sivu.</span><span class="sxs-lookup"><span data-stu-id="58ad5-208">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="58ad5-209">Uuden haun tietolähteen lisääminen</span><span class="sxs-lookup"><span data-stu-id="58ad5-209">Add a new lookup data source</span></span>

<span data-ttu-id="58ad5-210">Seuraavaksi lisätään uusi tietolähde määrittämään, miten yrityskäyttäjät määrittävät yrityskohtaiset säännöt tunnistamaan oikean verotustason kullekin summatulle tapahtumatietueelle.</span><span class="sxs-lookup"><span data-stu-id="58ad5-210">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="58ad5-211">Valitse **Yhdistämismääritys**-välilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-211">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="58ad5-212">Valitse **Muodon luetteloinnit\Haku**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-212">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="58ad5-213">Olet juuri määrittänyt, että jokainen sääntö, jonka yrityskäyttäjät määrittävät verotustason tunnistamiseen, palauttaa ER-muodon luetteloinnin arvon.</span><span class="sxs-lookup"><span data-stu-id="58ad5-213">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="58ad5-214">Huomaa, että **Haku**-tietolähdetyypin käyttö on mahdollista **Tietomalli**- ja **Dynamics 365 for Operations** -lohkoissa **Muodon luettelointi** -lohkon lisäksi.</span><span class="sxs-lookup"><span data-stu-id="58ad5-214">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="58ad5-215">Tämän vuoksi ER-tietomallin luettelointeja ja sovelluksen luettelointeja voi käyttää määrittämään niiden arvojen tyypin, joka palautetaan kyseisen tyypin tietolähteiksi.</span><span class="sxs-lookup"><span data-stu-id="58ad5-215">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that is are returned for data sources of that type.</span></span>
    
3.  <span data-ttu-id="58ad5-216">Kirjoita **Nimi**-kenttään **Valitsin**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="58ad5-217">Valitse **Muodon luettelointi** -kentässä **Verotustasojen luettelo**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="58ad5-218">Määritit juuri, että yrityskäyttäjän on valittava kunkin tässä tietolähteessä määritettävän säännön osalta palautetuksi arvoksi jonkin muodon luetteloinnin **Verotustasojen luettelo** -arvon.</span><span class="sxs-lookup"><span data-stu-id="58ad5-218">You just specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="58ad5-219">Valitse **Muokkaa hakua**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="58ad5-220">Valitse **Sarakkeet**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="58ad5-221">Laajenna **Malli**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="58ad5-222">Laajenna **Tiedot**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="58ad5-223">Laajenna **Vero**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="58ad5-224">Valitse **Model.Data.Tax.Code**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="58ad5-225">Valitse **Lisää**-painike (oikea nuoli).</span><span class="sxs-lookup"><span data-stu-id="58ad5-225">Select the **Add** button (the right arrow).</span></span>

    ![ER-toiminnon suunnittelutoiminnon sivu](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="58ad5-227">Määritit juuri, että yrityskäyttäjän on valittava yksi verokoodi kunkin tässä tietolähteessä verotustason tunnistukseen määritettävän säännön ehdoksi.</span><span class="sxs-lookup"><span data-stu-id="58ad5-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="58ad5-228">**Model.Data.Tax**-tietolähde palauttaa sen verokoodiluettelon, jonka yrityskäyttäjä voi valita.</span><span class="sxs-lookup"><span data-stu-id="58ad5-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="58ad5-229">Koska tässä tietolähteessä on **Nimi**-kenttä, verokoodin nimi näytetään jokaiselle verokoodin arvolle, jonka haku näyttää yrityskäyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="58ad5-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="58ad5-230">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-230">Select **OK**.</span></span>

    ![ER-toiminnon suunnittelutoiminnon sivu](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="58ad5-232">Yrityskäyttäjät voivat lisätä useita sääntöjä tietueina tähän tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="58ad5-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="58ad5-233">Kukin tietueen numerona on rivikoodi.</span><span class="sxs-lookup"><span data-stu-id="58ad5-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="58ad5-234">Säännöt arvioidaan nousevan rivinumeron perusteella.</span><span class="sxs-lookup"><span data-stu-id="58ad5-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="58ad5-235">Koska valitsit **Verokoodi**-kentän sääntöjen ehdoksi tässä haun tietolähteessä ja koska **Verokoodi** on määritetty **Merkkijono**-tietotyypin kentäksi, kukin sääntö arvioidaan suorituksenaikana vertaamalla tietolähteeseen välitettyä verokoodia tietolähteen tässä tietueessa määritettyyn verokoodiin.</span><span class="sxs-lookup"><span data-stu-id="58ad5-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="58ad5-236">Kun määritysehtoa vastaava sääntö löytyy, tietolähde palauttaa **Haun tulos** -kentässä määritetyn säännön hakuarvon.</span><span class="sxs-lookup"><span data-stu-id="58ad5-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="58ad5-237">Jos mitään sääntöä ei löydy, tapahtuu poikkeus, joka ilmaisee käyttäjälle, että nykyinen tietolähde ei voi palauttaa oikeaa arvoa.</span><span class="sxs-lookup"><span data-stu-id="58ad5-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="58ad5-238">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-238">Select **Save**.</span></span>
14. <span data-ttu-id="58ad5-239">Sulje **Haun suunnittelija** -sivu.</span><span class="sxs-lookup"><span data-stu-id="58ad5-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="58ad5-240">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-240">Select **OK**.</span></span>

    <span data-ttu-id="58ad5-241">Huomaa, että lisäämäsi uusi tietolähde palauttaa verotustason muodon luetteloinnin **Verotustasojen luettelo** -arvon mille tahansa tietolähteeseen välitetylle verokoodille **Merkkijono**-tietotyypin **Koodi**-parametrin argumenttina.</span><span class="sxs-lookup"><span data-stu-id="58ad5-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![ER-toiminnon suunnittelutoiminnon sivu](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="58ad5-243">Huomaa, että määritettyjen sääntöjen arviointi määräytyy niiden kenttien tietotyypin mukaan, jotka on valittu määrittämään kyseisten sääntöjen ehtoja.</span><span class="sxs-lookup"><span data-stu-id="58ad5-243">Note that the evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="58ad5-244">Kun valitset kentän, joka on määritetty joko **Numeerinen**- tai **Päivämäärä**-tietotyypin kentäksi, ehdot poikkeavat edellä käsitellyn **Merkkijono**-tietotyypin ehdoista.</span><span class="sxs-lookup"><span data-stu-id="58ad5-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="58ad5-245">**Numeerinen**- ja **Päivämäärä**-kenttien säännöt on määritettävä arvoalueena.</span><span class="sxs-lookup"><span data-stu-id="58ad5-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="58ad5-246">Säännön ehdon katsotaan sitten toteutuvan, kun tietolähteeseen välitetty arvo on määritetyllä alueella.</span><span class="sxs-lookup"><span data-stu-id="58ad5-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="58ad5-247">Seuraavassa kuvassa on esimerkki tämän tyyppisestä määrityksestä.</span><span class="sxs-lookup"><span data-stu-id="58ad5-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="58ad5-248">**Merkkijono**-tietotyypin **Model.Data.Tax.Code**-kentän lisäksi **Reaaliluku**-tietotyypin **Model.Tax.Summary.Base**-kenttää käytetään määrittämään haun tietolähteen ehtoja.</span><span class="sxs-lookup"><span data-stu-id="58ad5-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![ER-toiminnon suunnittelutoiminnon sivu](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="58ad5-250">Koska tämän haun tietolähteeksi on valittu **Model.Data.Tax.Code**- ja **Model.Tax.Summary.Base**-kentät, jokainen tämän tietolähteen sääntö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="58ad5-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="58ad5-251">Avautuvassa luettelossa muodon luetteloinnin **Verotustasojen luettelo** -arvo on valittava palautetuksi arvoksi.</span><span class="sxs-lookup"><span data-stu-id="58ad5-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="58ad5-252">Verokoodi on annettava tämän säännön ehdoksi.</span><span class="sxs-lookup"><span data-stu-id="58ad5-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="58ad5-253">Vain **Model.Data.Tax**-tietolähteestä saatavat verokoodit hyväksytään.</span><span class="sxs-lookup"><span data-stu-id="58ad5-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="58ad5-254">Veron perusteen vähimmäis-ja enimmäisarvot on annettava tämän säännön ehdoiksi</span><span class="sxs-lookup"><span data-stu-id="58ad5-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="58ad5-255">Tämän tietolähteen kukin sääntö arvioidaan suorituksen aikana seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="58ad5-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="58ad5-256">Vastasiko tietolähteeseen välitetyn **Merkkijono**-tietotyypin koodi säännön verokoodia?</span><span class="sxs-lookup"><span data-stu-id="58ad5-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="58ad5-257">Sijoittuiko tietolähteeseen välitetyn **Reaaliluku**-tietotyypin arvon määritettyjen vähimmäis- ja enimmäisarvojen väliin?</span><span class="sxs-lookup"><span data-stu-id="58ad5-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="58ad5-258">Säännön käyttö katsotaan mahdolliseksi, kun kumpikin ehto täyttyy.</span><span class="sxs-lookup"><span data-stu-id="58ad5-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="58ad5-259">Lisätyn haun tietolähteen otsikon kääntäminen</span><span class="sxs-lookup"><span data-stu-id="58ad5-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="58ad5-260">Koska yrityskäyttäjät voivat käyttää eri kieliä yrityskohtaisten verokoodijoukkojen määrittämiseen, lisättävän haun tietolähteen otsikko kannattaa kääntää, jota käyttäjät näkevät sen ensisijaisella kielellään kyseisellä sivulla.</span><span class="sxs-lookup"><span data-stu-id="58ad5-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="58ad5-261">Valitse **Model.Data.Selector**-tietolähde.</span><span class="sxs-lookup"><span data-stu-id="58ad5-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="58ad5-262">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="58ad5-263">Napsauta **Otsikko**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="58ad5-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="58ad5-264">Valitse **Käännä**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="58ad5-265">Kirjoita **Tekstin käännös** -ruudun **Otsikon tunnus** -kenttään **LBL_SELECTOR_DS**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-265">In the **Text translation** pane, in the **Label Id** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="58ad5-266">Kirjoita **Teksti oletuskielellä** -kenttään **Select tax level by tax code**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="58ad5-267">Valitse **Kieli**-kentässä **FI**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="58ad5-268">Kirjoita **Käännetty teksti** -kenttään **Valitse verotustaso verokoodin perusteella**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="58ad5-269">Valitse **Käännä**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-269">Select **Translate**.</span></span>
10. <span data-ttu-id="58ad5-270">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-270">Select **OK**.</span></span>

    ![ER-toiminnon suunnittelutoiminnon sivu](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="58ad5-272">Uuden kentän lisääminen käyttämään määritettyä hakua</span><span class="sxs-lookup"><span data-stu-id="58ad5-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="58ad5-273">Laajenna **Model.Data**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="58ad5-274">Valitse **Model.Data.Summary**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="58ad5-275">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-275">Select **Add**.</span></span>
4.  <span data-ttu-id="58ad5-276">Valitse **Toiminnot/Lasketut kentät**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="58ad5-277">Kirjoita **Nimi**-kenttään **LevelByLookup**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="58ad5-278">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="58ad5-279">Kirjoita **Kaava**-kenttään **Model.Selector(Model.Data.Summary.Code)**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="58ad5-280">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-280">Select **Save**.</span></span>

    ![ER-toiminnon suunnittelutoiminnon sivu](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="58ad5-282">Sulje **Kaavaeditori**-sivu.</span><span class="sxs-lookup"><span data-stu-id="58ad5-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="58ad5-283">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-283">Select **OK**.</span></span>

    ![ER-toiminnon suunnittelutoiminnon sivu](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="58ad5-285">Huomaa, että lisäämäsi laskettu **LevelByLookup**-kenttä palauttaa verotustason kunkin summatun verotapahtumatietueen muodon luetteloinnin **Verotustasojen luettelo** -arvona.</span><span class="sxs-lookup"><span data-stu-id="58ad5-285">Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id="58ad5-286">Tietueen verokoodi välitetään haun **Model.Selector**-tietolähteeseen, ja oikea verotustaso valitaan kyseisen tietolähteen sääntöjoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="58ad5-286">The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name="add-a-new-format-enumeration-based-data-source"></a><span data-ttu-id="58ad5-287">Uuden muodon luettelointiin perustuvan tietolähteen lisääminen</span><span class="sxs-lookup"><span data-stu-id="58ad5-287">Add a new format enumeration-based data source</span></span>

<span data-ttu-id="58ad5-288">Seuraavaksi lisätään uusi tietolähde, joka viittaa aiemmin lisättyyn muodon luettelointiin.</span><span class="sxs-lookup"><span data-stu-id="58ad5-288">Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id="58ad5-289">Tämän tietolähteen arvoja käytetään myöhemmin ER-muodon lausekkeessa.</span><span class="sxs-lookup"><span data-stu-id="58ad5-289">Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id="58ad5-290">Valitse **Lisää pääkansio**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-290">Select **Add root**.</span></span>
2.  <span data-ttu-id="58ad5-291">Valitse **Muodon luetteloinnit\Luettelointi**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-291">Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id="58ad5-292">Kirjoita **Nimi**-kenttään **TaxationLevel**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-292">In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id="58ad5-293">Valitse **Muodon luettelointi** -kentässä **Verotustasojen luettelo**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-293">In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id="58ad5-294">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-294">Select **Save**.</span></span>

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a><span data-ttu-id="58ad5-295">Aiemmin luodun kentän muokkaaminen aloittamaan haku</span><span class="sxs-lookup"><span data-stu-id="58ad5-295">Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id="58ad5-296">Seuraavaksi muokataan aiemmin luotua laskettua kenttää siten, että se käyttää määritettyä haun tietolähdettä palauttamaan oikean verotustason arvon verokoodin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="58ad5-296">Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id="58ad5-297">Valitse **Model.Data.Summary.Level**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-297">Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id="58ad5-298">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-298">Select **Edit**.</span></span>
3.  <span data-ttu-id="58ad5-299">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-299">Select **Edit formula**.</span></span>

    <span data-ttu-id="58ad5-300">Huomaa, että **Model.Data.Summary.Level**-kentän nykyinen lauseke sisältää seuraavat pysyvästi koodatut verokoodit:</span><span class="sxs-lookup"><span data-stu-id="58ad5-300">Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id="58ad5-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span><span class="sxs-lookup"><span data-stu-id="58ad5-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="58ad5-302">Lisää **Kaava**-kenttään **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![ER-toiminnon suunnittelutoiminnon sivu](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="58ad5-304">Huomaa, että **Model.Data.Summary.Level**-kentän lauseke palauttaa nyt verotustason nykyisen tietueen verokoodin ja sen sääntöjoukon perusteella, jonka yrityskäyttäjä määrittää haun **Model.Data.Selector**-tietolähteessä.</span><span class="sxs-lookup"><span data-stu-id="58ad5-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="58ad5-305">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-305">Select **Save**.</span></span>
6.  <span data-ttu-id="58ad5-306">Sulje **Reseptien suunnittelu** -sivu.</span><span class="sxs-lookup"><span data-stu-id="58ad5-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="58ad5-307">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-307">Select **OK**.</span></span>
8.  <span data-ttu-id="58ad5-308">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-308">Select **Save**.</span></span>
9.  <span data-ttu-id="58ad5-309">Sulje **Muodon suunnittelutoiminto** -sivu.</span><span class="sxs-lookup"><span data-stu-id="58ad5-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="58ad5-310">Johdetun muodon luonnosversion viimeisteleminen</span><span class="sxs-lookup"><span data-stu-id="58ad5-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="58ad5-311">Valitse **Versiot**-pikavälilehdessä **Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-311">On the **Versions** fast tab, select **Change status**.</span></span>
2.  <span data-ttu-id="58ad5-312">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="58ad5-313">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="58ad5-314">Muokatun muodon valmiin version vieminen</span><span class="sxs-lookup"><span data-stu-id="58ad5-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="58ad5-315">Valitse määrityspuussa **LE-tietojen haun oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-315">In the configuration tree, select the **Format to learn how to lookup LE data** item.</span></span>
2.  <span data-ttu-id="58ad5-316">Valitse **Versiot**-pikavälilehdessä tietue, jonka tila on **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-316">On the **Versions** fast tab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="58ad5-317">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="58ad5-318">Valitse **Vie XML-tiedostona**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="58ad5-319">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="58ad5-319">Select **OK**.</span></span>
6.  <span data-ttu-id="58ad5-320">Selain lataa **Format to learn how to lookup LE data.xml**-tiedoston.</span><span class="sxs-lookup"><span data-stu-id="58ad5-320">The web browser downloads a **Format to learn how to lookup LE data.xml** file.</span></span> <span data-ttu-id="58ad5-321">Tallenna tiedosto paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="58ad5-321">Store this file locally.</span></span>

<span data-ttu-id="58ad5-322">Toista edellä oleva vaiheet **LE-tietojen haun oppimismuoto** -muodon päänimikkeissä ja tallenna seuraavat tiedostot paikallisesti:</span><span class="sxs-lookup"><span data-stu-id="58ad5-322">Repeat steps in this section for parent items of the **Format to learn how to lookup LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="58ad5-323">Format to learn parameterized calls.xml</span><span class="sxs-lookup"><span data-stu-id="58ad5-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="58ad5-324">Mapping to learn parameterized calls.xml</span><span class="sxs-lookup"><span data-stu-id="58ad5-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="58ad5-325">Model to learn parameterized calls.xml</span><span class="sxs-lookup"><span data-stu-id="58ad5-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="58ad5-326">Lisätietoja määritetyn **LE-tietojen haun oppimismuoto** -ER-muodon käyttämisestä siten, että sillä määritetään yrityskohtainen verokoodijoukko suodattamaan verotapahtumia eri verotustasoilla, on ohjeaiheen [ER-muodon parametrien määrittäminen yrityskohtaisesti](er-app-specific-parameters-set-up.md) ohjeissa.</span><span class="sxs-lookup"><span data-stu-id="58ad5-326">To learn how to use the configured **Format to learn how to lookup LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="58ad5-327">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="58ad5-327">Additional resources</span></span>

[<span data-ttu-id="58ad5-328">Sähköisen raportoinnin kaavojen suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="58ad5-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="58ad5-329">ER-muodon parametrien määrittäminen yrityskohtaisesti</span><span class="sxs-lookup"><span data-stu-id="58ad5-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)
