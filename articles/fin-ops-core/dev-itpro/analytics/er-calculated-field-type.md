---
title: Laskettu kenttä -tyyppisten ER-tietolähteiden parametrisoitujen kutsujen tuki
description: Tässä ohjeaiheessa käsitellään ER-tietolähteiden Laskettu kenttä -tyypin käyttöä.
author: NickSelin
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 897133a27f9d3da2f576ce675c0949f824cde881
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749486"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="f0747-103">Laskettu kenttä -tyyppisten ER-tietolähteiden parametrisoitujen kutsujen tuki</span><span class="sxs-lookup"><span data-stu-id="f0747-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0747-104">Tässä ohjeaiheessa käsitellään sähköisen raportoinnin (ER) tietolähteiden suunnittelua **Laskettu kenttä** -tyypin avulla.</span><span class="sxs-lookup"><span data-stu-id="f0747-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="f0747-105">Tietolähteessä voi olla ER-lauseke, jota voidaan suoritettaessa hallita niiden parametriargumenttien arvoilla, jotka on määritetty tätä tietolähdettä kutsuvassa sidonnassa.</span><span class="sxs-lookup"><span data-stu-id="f0747-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="f0747-106">Jos kyseisen tietolähteelle määritetään parametrisoidut kutsut, voit käyttää yhtä tietolähdettä useissa sidonnoissa, mikä vähentää ER-mallimäärityksissä tai ER-muodoissa määritettävien tietolähteiden kokonaismäärää.</span><span class="sxs-lookup"><span data-stu-id="f0747-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="f0747-107">Se myös yksinkertaistaa määritettyä ER-komponenttia, mikä puolestaan vähentää ylläpitokustannuksia ja muiden kuluttajien käyttökustannuksia.</span><span class="sxs-lookup"><span data-stu-id="f0747-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f0747-108">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="f0747-108">Prerequisites</span></span>
<span data-ttu-id="f0747-109">Tämän aiheen esimerkkien suorittaminen edellyttää seuraavia käyttöoikeuksia:</span><span class="sxs-lookup"><span data-stu-id="f0747-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="f0747-110">Jonkin seuraavan roolin käyttöoikeus:</span><span class="sxs-lookup"><span data-stu-id="f0747-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="f0747-111">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="f0747-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="f0747-112">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="f0747-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f0747-113">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="f0747-113">System administrator</span></span>

- <span data-ttu-id="f0747-114">Sellaisen Regulatory Configuration Servicesin (RCS) käyttöoikeus, joka on valmisteltu samalle vuokralaiselle kuin Finance and Operations yhdessä seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="f0747-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="f0747-115">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="f0747-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="f0747-116">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="f0747-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f0747-117">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="f0747-117">System administrator</span></span>

<span data-ttu-id="f0747-118">Seuraavat tiedostot täytyy myös ladata ja tallentaa paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="f0747-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="f0747-119">**Sisältö**</span><span class="sxs-lookup"><span data-stu-id="f0747-119">**Content**</span></span>                           | <span data-ttu-id="f0747-120">**Tiedostonimi**</span><span class="sxs-lookup"><span data-stu-id="f0747-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f0747-121">Esimerkin ER-tietomallin konfigurointi</span><span class="sxs-lookup"><span data-stu-id="f0747-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="f0747-122">Model to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="f0747-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="f0747-123">Esimerkin ER-metadatan konfigurointi</span><span class="sxs-lookup"><span data-stu-id="f0747-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="f0747-124">Metadata to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="f0747-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="f0747-125">Esimerkin ER-mallikartoituksen konfigurointi</span><span class="sxs-lookup"><span data-stu-id="f0747-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="f0747-126">Mapping to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="f0747-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="f0747-127">Esimerkin ER-format-konfigurointi</span><span class="sxs-lookup"><span data-stu-id="f0747-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="f0747-128">Format to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="f0747-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="f0747-129">Kirjautuminen RCS-esiintymään</span><span class="sxs-lookup"><span data-stu-id="f0747-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="f0747-130">Tällä esimerkissä luodaan määritys malliyritykselle Litware, Inc. Ensiksi on kuitenkin suoritettava RCS:ssä [Konfiguraation lähteiden luominen ja niiden merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="f0747-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="f0747-131">Valitse oletuskoontinäytössä **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="f0747-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="f0747-132">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="f0747-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="f0747-133">Tuo ladatut kokoonpanot RCS:ään seuraavassa järjestyksessä: tietomalli, metatiedot, mallin määritys, muoto.</span><span class="sxs-lookup"><span data-stu-id="f0747-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="f0747-134">Tee seuraavat vaiheet kussakin ER-kokoonpanossa:</span><span class="sxs-lookup"><span data-stu-id="f0747-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="f0747-135">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="f0747-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="f0747-136">Valitse **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="f0747-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="f0747-137">Valitse ensin **Selaa** ja sitten tarvittava XML-muotoinen ER-kokoonpano.</span><span class="sxs-lookup"><span data-stu-id="f0747-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="f0747-138">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0747-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="f0747-139">Annetun ER-ratkaisun tarkastelu</span><span class="sxs-lookup"><span data-stu-id="f0747-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="f0747-140">Mallin määrityksen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="f0747-140">Review model mapping</span></span>

1. <span data-ttu-id="f0747-141">Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.</span><span class="sxs-lookup"><span data-stu-id="f0747-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="f0747-142">Valitse **Mapping to learn parameterized calls**.</span><span class="sxs-lookup"><span data-stu-id="f0747-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="f0747-143">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="f0747-143">Select **Designer**.</span></span>
4. <span data-ttu-id="f0747-144">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="f0747-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="f0747-145">Tämä ER-mallimääritys on suunniteltu seuraavia toimia varten:</span><span class="sxs-lookup"><span data-stu-id="f0747-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="f0747-146">**TaxTable**-taulussa olevan verokoodiluettelon (**Tax**-tietolähde) noutaminen.</span><span class="sxs-lookup"><span data-stu-id="f0747-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="f0747-147">**TaxTable**-taulussa olevan verotapahtumaluettelon (**Trans**-tietolähde) noutaminen:</span><span class="sxs-lookup"><span data-stu-id="f0747-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="f0747-148">Noudetun tapahtumaluettelon ryhmittely (**Gr**-tietolähde) verokoodin mukaan.</span><span class="sxs-lookup"><span data-stu-id="f0747-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="f0747-149">Ryhmitettyjen tapahtumien laskeminen verokoodikohtaisten koostettujen arvojen mukaan:</span><span class="sxs-lookup"><span data-stu-id="f0747-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="f0747-150">Veron perusarvojen summa.</span><span class="sxs-lookup"><span data-stu-id="f0747-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="f0747-151">Veroarvojen summa.</span><span class="sxs-lookup"><span data-stu-id="f0747-151">Sum of tax values.</span></span>
            - <span data-ttu-id="f0747-152">Käytetyn veroprosentin vähimmäisarvo.</span><span class="sxs-lookup"><span data-stu-id="f0747-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="f0747-153">Tässä kokoonpanossa mallin yhdistäminen käyttää tälle mallille luotujen ja Finance and Operationsissa suoritettujen ER-muotojen perustietomallia.</span><span class="sxs-lookup"><span data-stu-id="f0747-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="f0747-154">Tämän vuoksi **Tax**- ja **Gr**-tietolähteiden sisältö näkyy ER-muodoissa abstrakteina tietolähteinä.</span><span class="sxs-lookup"><span data-stu-id="f0747-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![Tax- ja Gr-tietolähteet näkyvät mallimäärityksen suunnittelusivulla](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="f0747-156">Sulje **Mallimäärityksen sunnittelun** sivu.</span><span class="sxs-lookup"><span data-stu-id="f0747-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="f0747-157">Sulje **Mallimääritys**-sivu.</span><span class="sxs-lookup"><span data-stu-id="f0747-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="f0747-158">Muodon tarkastelu</span><span class="sxs-lookup"><span data-stu-id="f0747-158">Review format</span></span>

1. <span data-ttu-id="f0747-159">Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.</span><span class="sxs-lookup"><span data-stu-id="f0747-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="f0747-160">Valitse **Parametrisoitujen kutsujen oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="f0747-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="f0747-161">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="f0747-161">Select **Designer**.</span></span> <span data-ttu-id="f0747-162">Tämä ER-muoto on suunniteltu seuraavia toimia varten:</span><span class="sxs-lookup"><span data-stu-id="f0747-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="f0747-163">XML-muotoisen veroilmoituksen luominen.</span><span class="sxs-lookup"><span data-stu-id="f0747-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="f0747-164">Seuraavien verotustasojen näyttäminen veroilmoituksessa: normaali, alennettu ja ei mitään.</span><span class="sxs-lookup"><span data-stu-id="f0747-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="f0747-165">Useiden tietojen näyttäminen kustakin verotustasosta siten, että kunkin tason tiedoilla on eri numero.</span><span class="sxs-lookup"><span data-stu-id="f0747-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Muodon suunnittelutoiminto -sivu](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="f0747-167">Valitse **Määritys**.</span><span class="sxs-lookup"><span data-stu-id="f0747-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="f0747-168">Laajenna **Malli**, **Tiedot** ja **Yhteenveto**.</span><span class="sxs-lookup"><span data-stu-id="f0747-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="f0747-169">Laskettu **Model.Data.Summary.Level** -kenttä sisältää lausekkeen, joka palauttaa verotustason koodin (**Normaali**, **Alennettu**, **Ei mitään** tai **Muu**) sellaisen verokoodin tekstiarvona, joka voidaan suorituksenaikaisesti noutaa **Model.Data.Summary**-tietolähteestä.</span><span class="sxs-lookup"><span data-stu-id="f0747-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![Model to learn parameterized calls -tietomallin tiedot muodon suunnittelusivulla](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="f0747-171">Laajenna **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="f0747-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="f0747-172">Laajenna **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="f0747-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="f0747-173">**Model**.**Data2.Summary2**-tietolähde on määritetty ryhmälle, jonka **Model.Data.Summary**-tietolähdetapahtuma erittelee verotustason mukaan (joka saadaan lasketusta **Model.Data.Summary.Level**-kentästä) ja laskee koosteet.</span><span class="sxs-lookup"><span data-stu-id="f0747-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Model.Data2.Summary2-tietolähteen tiedot muodon suunnittelusivulla](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="f0747-175">Tarkista lasketut **Model**.**Data2.Level1**, **Model**.**Data2.Level2**- ja **Model**.**Data2.Level3**-kentät.</span><span class="sxs-lookup"><span data-stu-id="f0747-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="f0747-176">**Model**.**Data2.Summary2**-tietueluettelo suodatetaan näiden laskettujen kenttien avulla palauttamaan vain tiettyä verotustasoa vastaavat tietueet.</span><span class="sxs-lookup"><span data-stu-id="f0747-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="f0747-177">Sulje **Muodon suunnittelija** -sivu.</span><span class="sxs-lookup"><span data-stu-id="f0747-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="f0747-178">Johdetun luominen</span><span class="sxs-lookup"><span data-stu-id="f0747-178">Create a derived format</span></span>
<span data-ttu-id="f0747-179">Voit parantaa annettua muotoa lisäämällä yhden lasketun kentän suodattamaan tarvittavan verotustason sen sijaan, että käyttäisit kolmea aiemmin luotua kenttää: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** ja **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="f0747-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="f0747-180">Tarvittava verotustaso voidaan määrittää sijainnissa, josta tämä uusi laskettu kenttä kutsutaan.</span><span class="sxs-lookup"><span data-stu-id="f0747-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="f0747-181">Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.</span><span class="sxs-lookup"><span data-stu-id="f0747-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="f0747-182">Valitse **Parametrisoitujen kutsujen oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="f0747-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="f0747-183">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="f0747-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="f0747-184">Valitse **Johdettu nimestä: Parametrisoitujen kutsujen oppimismuoto, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="f0747-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="f0747-185">Anna **Nimi**-kentässä **Parametrisoitujen kutsujen oppimismuoto (mukautettu)**.</span><span class="sxs-lookup"><span data-stu-id="f0747-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="f0747-186">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="f0747-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="f0747-187">Tietueluettelon palauttavan parametrisoidun lasketun kentän luominen</span><span class="sxs-lookup"><span data-stu-id="f0747-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="f0747-188">Aloittaminen lisäämällä uusi laskettu kenttä</span><span class="sxs-lookup"><span data-stu-id="f0747-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="f0747-189">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="f0747-189">Select **Designer**.</span></span>
2. <span data-ttu-id="f0747-190">Laajenna kaikki muotokohteet valitsemalla **Laajenna/tiivistä**.</span><span class="sxs-lookup"><span data-stu-id="f0747-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="f0747-191">Valitse **Määritys**.</span><span class="sxs-lookup"><span data-stu-id="f0747-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="f0747-192">Laajenna **Malli**.</span><span class="sxs-lookup"><span data-stu-id="f0747-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="f0747-193">Valitse **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="f0747-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="f0747-194">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f0747-194">Select **Add**.</span></span>
7. <span data-ttu-id="f0747-195">Valitse **Toiminnot\\Lasketut kentät**.</span><span class="sxs-lookup"><span data-stu-id="f0747-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="f0747-196">Kirjoita **Nimi**-kenttään **Tasot**.</span><span class="sxs-lookup"><span data-stu-id="f0747-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="f0747-197">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="f0747-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="f0747-198">Parametrin määrittäminen lasketun kentän lisäämistä varten</span><span class="sxs-lookup"><span data-stu-id="f0747-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="f0747-199">Valitse **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="f0747-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="f0747-200">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f0747-200">Select **New**.</span></span>
3. <span data-ttu-id="f0747-201">Kirjoita **Nimi**-kenttään **Verotustaso**.</span><span class="sxs-lookup"><span data-stu-id="f0747-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="f0747-202">Kirjoita **Tyyppi**-kenttään **Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="f0747-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="f0747-203">Parametrin argumenttityypin määrittämisessä voidaan käyttää vain primitiivisiä tietotyyppejä.</span><span class="sxs-lookup"><span data-stu-id="f0747-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="f0747-204">Niissä tähän tarkoitukseen ei voi käyttää **Tietueluettelo**-, **Tietue**- ja **Valintalista**-tyyppejä.</span><span class="sxs-lookup"><span data-stu-id="f0747-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="f0747-205">Yhdelle lasketulle kentälle voi määrittää enintään 8 parametria.</span><span class="sxs-lookup"><span data-stu-id="f0747-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Parametrin tietolähdeluettelo](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="f0747-207">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0747-207">Select **OK**.</span></span>

<span data-ttu-id="f0747-208">Tämän parametrin lisääminen määrittää ehdon, joka on oltava käytössä, jotta tämän lasketun kentän voi kutsua.</span><span class="sxs-lookup"><span data-stu-id="f0747-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="f0747-209">Tämän lasketun kentän kutsuminen edellyttää, että **Verotustaso**-parametrin argumentti määritetään arvoksi **Merkkijono**-muodossa.</span><span class="sxs-lookup"><span data-stu-id="f0747-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="f0747-210">Varmista, että määrität parametrit vain säilössä oleville lasketuille kentille (joko **Tietueluettelo**, **Tietue** tai **Säilö**).</span><span class="sxs-lookup"><span data-stu-id="f0747-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="f0747-211">Määritetty parametri on käytettävissä tämän lasketun kentän tietolähdeluettelossa.</span><span class="sxs-lookup"><span data-stu-id="f0747-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="f0747-212">Voit lisätä parametrin määritettyyn lausekkeeseen valitsemalla **Lisää tietolähde**.</span><span class="sxs-lookup"><span data-stu-id="f0747-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Tietolähdekentät](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="f0747-214">Lasketun kentän lisäämän lausekkeen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f0747-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="f0747-215">Kirjoita **Resepti**-kenttään:</span><span class="sxs-lookup"><span data-stu-id="f0747-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="f0747-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="f0747-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="f0747-217">Valitse tietolähdeluettelossa **Verotustaso**-parametri.</span><span class="sxs-lookup"><span data-stu-id="f0747-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="f0747-218">Valitse **Lisää tietolähde**.</span><span class="sxs-lookup"><span data-stu-id="f0747-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="f0747-219">Viimeistele lauseke **Resepti**-kentässä muotoon:</span><span class="sxs-lookup"><span data-stu-id="f0747-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="f0747-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Verotustaso')**</span><span class="sxs-lookup"><span data-stu-id="f0747-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="f0747-221">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f0747-221">Select **Save**.</span></span>

    ![Tietolähdekentän tiedot](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="f0747-223">Sulje **Reseptien suunnittelu** -sivu.</span><span class="sxs-lookup"><span data-stu-id="f0747-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="f0747-224">Uuden lasketun kentän lisäämisen viimeistely</span><span class="sxs-lookup"><span data-stu-id="f0747-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="f0747-225">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0747-225">Select **OK**.</span></span>

<span data-ttu-id="f0747-226">**Reseptien suunnittelu** -sivulla oleva määritetty parametrisoitu laskettu **Tasot**-kenttä edellyttää **Merkkijono**-argumenttia.</span><span class="sxs-lookup"><span data-stu-id="f0747-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Laajennettu lasketun kentän tasoluettelo](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements&quot;></a><span data-ttu-id=&quot;f0747-228&quot;>Muodon elementtien sitominen määritetyn lasketun kentän avulla</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-228&quot;>Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id=&quot;f0747-229&quot;>Valitse laskettu kenttä valitsemalla **Model.Data2.Levels**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-229&quot;>Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id=&quot;f0747-230&quot;>Valitse **Statement.Taxation.Regular**-muotoelementti.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-230&quot;>Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id=&quot;f0747-231&quot;>Valitse **Sido**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-231&quot;>Select **Bind**.</span></span>
4. <span data-ttu-id=&quot;f0747-232&quot;>Valitsemalla **Kyllä** voit vahvistaa käytössä olevan tietolähteen **Taso1** korvaamisen uudella tietolähteellä **Tasot** kaikissa valitun muotoelementin sisäkkäisissä muotoelementeissä.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-232&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id=&quot;f0747-233&quot;>Kohdistettu sidonta on muodostettu parametrisoidun lasketun kentän kutsuna.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-233&quot;>Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id=&quot;f0747-234&quot;>Sidotun muotoelementin nimeä käytetään oletusarvoisesti parametrisoidun lasketun kentän argumenttina seuraavien ehtojen mukaisesti:</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-234&quot;>By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id=&quot;f0747-235&quot;>Laskettu kenttä on määritetty käyttämään yhtä parametria.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-235&quot;>The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id=&quot;f0747-236&quot;>Kyseisen parametrin tietotyypiksi on määritetty **merkkijono**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-236&quot;>The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id=&quot;f0747-237&quot;>Jos sidotun muotoelementin nimi on tyhjä, kyseisen elementin tietolähteen nimeä käytetään kohdistetussa sidonnassa.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-237&quot;>When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id=&quot;f0747-238&quot;>Valitse **Statement.Taxation.Reduced**-muotoelementti.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-238&quot;>Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id=&quot;f0747-239&quot;>Valitse **Sido**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-239&quot;>Select **Bind**.</span></span>
7. <span data-ttu-id=&quot;f0747-240&quot;>Valitsemalla **Kyllä** voit vahvistaa käytössä olevan tietolähteen **Taso2** korvaamisen uudella tietolähteellä **Tasot** kaikissa valitun muotoelementin sisäkkäisissä muotoelementeissä.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-240&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id=&quot;f0747-241&quot;>Valitse **Statement.Taxation.None**-muotoelementti.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-241&quot;>Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id=&quot;f0747-242&quot;>Valitse **Sido**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-242&quot;>Select **Bind**.</span></span>
10. <span data-ttu-id=&quot;f0747-243&quot;>Valitsemalla **Kyllä** voit vahvistaa käytössä olevan tietolähteen **Taso3** korvaamisen uudella tietolähteellä **Tasot** kaikissa valitun muotoelementin sisäkkäisissä muotoelementeissä.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f0747-243&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id=&quot;f0747-244&quot;>Jos määrität verotustasoon viittaavan XML-elementin (kuten **Model.Data2.Levels(&quot;Alennettu")** tekstiarvona) parametrisoidun lasketun kentän argumentin, samaa ei tarvitse tehdä sisäkkäisille XML-määritteille, sillä niiden sidonnat perivät automaattisesti päätasolla määritetyn argumentin arvon (**Model.Data2.Levels.aggregated.Base**, ei siis **Model.Data2.Levels("Alennettu").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="f0747-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="f0747-245">Parametrisoidun lasketun kentän toistuvia kutsuja ei tueta.</span><span class="sxs-lookup"><span data-stu-id="f0747-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="f0747-246">Voit valita **Muokkaa reseptiä** ja muuta valitussa sidonnassa olevan parametrisoidun lasketun kentän oletusarvoista kohdistusta.</span><span class="sxs-lookup"><span data-stu-id="f0747-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="f0747-247">Jos tämä argumentti puuttuu, seurauksena voi olla suorituksenaikaisia virheitä; käyttäjille ilmoitetaan tällaisesta tilanteesta, kun nykyinen muoto vahvistetaan.</span><span class="sxs-lookup"><span data-stu-id="f0747-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Vahvistuksen varoitusilmoitus](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="f0747-249">Tietueen palauttavan parametrisoidun lasketun kentän luominen</span><span class="sxs-lookup"><span data-stu-id="f0747-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="f0747-250">Kun parametrisoitu laskettu kenttä palauttaa tietueen, tämän tietueen yksittäisten kenttien tukemista muotoelementteihin on tuettava.</span><span class="sxs-lookup"><span data-stu-id="f0747-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="f0747-251">Tällaisissa tapauksissa ei ole pääsidontaa, joka sisältää parametrisoidun lasketun kentän kutsuvan argumentin arvon. Tämä arvo on määritettävä yksittäisen tietuen kentässä.</span><span class="sxs-lookup"><span data-stu-id="f0747-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="f0747-252">Aloittaminen lisäämällä uusi laskettu kenttä</span><span class="sxs-lookup"><span data-stu-id="f0747-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="f0747-253">Valitse **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="f0747-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="f0747-254">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f0747-254">Select **Add**.</span></span>
3. <span data-ttu-id="f0747-255">Valitse **Toiminnot\\Lasketut kentät**.</span><span class="sxs-lookup"><span data-stu-id="f0747-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="f0747-256">Kirjoita **Nimi**-kenttään **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="f0747-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="f0747-257">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="f0747-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="f0747-258">Parametrin määrittäminen lasketun kentän lisäämistä varten</span><span class="sxs-lookup"><span data-stu-id="f0747-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="f0747-259">Valitse **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="f0747-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="f0747-260">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f0747-260">Select **New**.</span></span>
3. <span data-ttu-id="f0747-261">Kirjoita **Nimi**-kenttään **Verotustaso**.</span><span class="sxs-lookup"><span data-stu-id="f0747-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="f0747-262">Kirjoita **Tyyppi**-kenttään **Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="f0747-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="f0747-263">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0747-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="f0747-264">Lasketun kentän lisäämän lausekkeen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f0747-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="f0747-265">Kirjoita **Resepti**-kenttään</span><span class="sxs-lookup"><span data-stu-id="f0747-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="f0747-266">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="f0747-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="f0747-267">Valitse **Verotustaso**-parametri.</span><span class="sxs-lookup"><span data-stu-id="f0747-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="f0747-268">Valitse **Lisää tietolähde**.</span><span class="sxs-lookup"><span data-stu-id="f0747-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="f0747-269">Liitä **Resepti**-kentässä **'Verotustaso'))** tekstiin, jonka kirjoitit vaiheessa 1. Lauseke viimeistellään muotoon:</span><span class="sxs-lookup"><span data-stu-id="f0747-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="f0747-270">**FIRSTORNULL(\@.Levels('Verotustaso'))**</span><span class="sxs-lookup"><span data-stu-id="f0747-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="f0747-271">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f0747-271">Select **Save**.</span></span>
6. <span data-ttu-id="f0747-272">Sulje **Reseptien suunnittelu** -sivu.</span><span class="sxs-lookup"><span data-stu-id="f0747-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="f0747-273">Uuden lasketun kentän lisäämisen viimeistely</span><span class="sxs-lookup"><span data-stu-id="f0747-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="f0747-274">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0747-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="f0747-275">Muodon elementtien sitominen määritetyn lasketun kentän avulla</span><span class="sxs-lookup"><span data-stu-id="f0747-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="f0747-276">Valitse määritetty laskettu kenttä laajentamalla **Model.Data2.LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="f0747-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="f0747-277">Laajenna määritetyn lasketun kentän **Model.Data2.LevelRecord.aggregated**-säilö.</span><span class="sxs-lookup"><span data-stu-id="f0747-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="f0747-278">Valitse **Model.Data2.LevelRecord.aggregated.Base**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="f0747-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="f0747-279">Valitse **Statement.Taxation.None**-muotoelementti.</span><span class="sxs-lookup"><span data-stu-id="f0747-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="f0747-280">Valitse **Poista sidonta**.</span><span class="sxs-lookup"><span data-stu-id="f0747-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="f0747-281">Valitse **Statement.Taxation.None.Base**-muotoelementti.</span><span class="sxs-lookup"><span data-stu-id="f0747-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="f0747-282">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="f0747-282">Select **Bind**.</span></span>
8. <span data-ttu-id="f0747-283">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="f0747-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="f0747-284">Muuta lauseke muotoon **Model.Data2.LevelRecord("Ei mitään").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="f0747-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Päivitetty lauseke](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="f0747-286">Käyttämättömien laskettujen kenttien poistaminen</span><span class="sxs-lookup"><span data-stu-id="f0747-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="f0747-287">Valitse **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="f0747-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="f0747-288">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="f0747-288">Select **Delete**.</span></span>
3. <span data-ttu-id="f0747-289">Valitse **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="f0747-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="f0747-290">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="f0747-290">Select **Delete**.</span></span>
5. <span data-ttu-id="f0747-291">Valitse **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="f0747-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="f0747-292">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="f0747-292">Select **Delete**.</span></span>
7. <span data-ttu-id="f0747-293">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f0747-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="f0747-294">Käytit samaa laskettua **Model.Data2.Levels**-kenttää useita kertoja muodon sidonnoissa.</span><span class="sxs-lookup"><span data-stu-id="f0747-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="f0747-295">Yhden lasketun kentän käyttäminen ja ylläpitäminen on paljon helpompaa kuin useiden samankaltaisten kenttien käyttö ja ylläpito.</span><span class="sxs-lookup"><span data-stu-id="f0747-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="f0747-296">Sulje **Muodon suunnittelija** -sivu.</span><span class="sxs-lookup"><span data-stu-id="f0747-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="f0747-297">Johdetun muodon korjatun version viimeisteleminen</span><span class="sxs-lookup"><span data-stu-id="f0747-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="f0747-298">Valitse **Versiot**-pikavälilehdessä **Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="f0747-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="f0747-299">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="f0747-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="f0747-300">Johdetun muodon valmiin version vieminen</span><span class="sxs-lookup"><span data-stu-id="f0747-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="f0747-301">Valitse kokoonpanopuussa **Parametrisoitujen kutsujen oppimismuoto (mukautettu)**.</span><span class="sxs-lookup"><span data-stu-id="f0747-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="f0747-302">Valitse **Version**-pikavälilehdessä valmis versio 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="f0747-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="f0747-303">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="f0747-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="f0747-304">Valitse **Vie XML-tiedostona**.</span><span class="sxs-lookup"><span data-stu-id="f0747-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="f0747-305">Tallenna ladattu kokoonpano paikallisesti XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="f0747-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="f0747-306">ER-muotojen testaaminen</span><span class="sxs-lookup"><span data-stu-id="f0747-306">Test ER formats</span></span> 
<span data-ttu-id="f0747-307">Voit suorittaa alkuperäiset ja parannetut ER-muodot ja varmistaa tällä tavoin, että määritetyt parametrisoidut lasketut kentät toimivat oikein.</span><span class="sxs-lookup"><span data-stu-id="f0747-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="f0747-308">ER-konfiguraatioiden tuominen</span><span class="sxs-lookup"><span data-stu-id="f0747-308">Import ER configurations</span></span>
<span data-ttu-id="f0747-309">Voit tuoda tarkistetut kokoonpanot RCS:stä käyttämällä **RCS**-tyyppistä ER-säilöä.</span><span class="sxs-lookup"><span data-stu-id="f0747-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="f0747-310">Jos olet jo suorittanut ohjeaiheen [Sähköisen raportoinnin (ER) konfiguraatioiden tuonti Regulatory Configuration Services (RCS) -palvelusta](rcs-download-configurations.md) vaiheet, tuo aiemmin tässä aiheessa käsitellyt määritykset ympäristöön määritetyn ER-säilön avulla.</span><span class="sxs-lookup"><span data-stu-id="f0747-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="f0747-311">Toimi muussa tapauksessa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f0747-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="f0747-312">Valitse **DEMF**-yritys ja valitse oletuskoontinäytössä **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="f0747-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="f0747-313">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="f0747-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="f0747-314">Tuo kokoonpanot Microsoft Download Centeristä seuraavassa järjestyksessä: tietomalli, mallin määritys, muoto.</span><span class="sxs-lookup"><span data-stu-id="f0747-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="f0747-315">Tee seuraavat vaiheet kussakin ER-kokoonpanossa:</span><span class="sxs-lookup"><span data-stu-id="f0747-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="f0747-316">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="f0747-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="f0747-317">Valitse **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="f0747-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="f0747-318">Valitse ensin **Selaa** ja sitten tarvittava XML-muotoinen ER-kokoonpano.</span><span class="sxs-lookup"><span data-stu-id="f0747-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="f0747-319">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0747-319">Select **OK**.</span></span>

4. <span data-ttu-id="f0747-320">Tuo RCS:stä viety **Parametrisoitujen kutsujen oppimismuoto (mukautettu)** -muodon valmis versio 1.1.1:</span><span class="sxs-lookup"><span data-stu-id="f0747-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="f0747-321">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="f0747-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="f0747-322">Valitse **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="f0747-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="f0747-323">Valitse ensin **Selaa** ja sitten paikallisesti tallennettu XML-muotoinen **Format to learn parameterized calls (mukautettu)** -tiedosto.</span><span class="sxs-lookup"><span data-stu-id="f0747-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="f0747-324">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0747-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="f0747-325">ER-muotojen suorittaminen</span><span class="sxs-lookup"><span data-stu-id="f0747-325">Run ER formats</span></span>

1. <span data-ttu-id="f0747-326">Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.</span><span class="sxs-lookup"><span data-stu-id="f0747-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="f0747-327">Valitse **Parametrisoitujen kutsujen oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="f0747-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="f0747-328">Valitse ylimmässä valintanauhassa **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="f0747-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="f0747-329">Tallenna paikallisesti luotu tuotos.</span><span class="sxs-lookup"><span data-stu-id="f0747-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="f0747-330">Valitse **Parametrisoitujen kutsujen oppimismuoto (mukautettu)**.</span><span class="sxs-lookup"><span data-stu-id="f0747-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="f0747-331">Valitse ylimmässä valintanauhassa **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="f0747-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="f0747-332">Tallenna luotu tuotos paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="f0747-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="f0747-333">Vertaa luotujen tuotosten sisältöä.</span><span class="sxs-lookup"><span data-stu-id="f0747-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0747-334">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f0747-334">Additional resources</span></span>

- [<span data-ttu-id="f0747-335">Sähköisen raportoinnin (ER) kaavojen suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="f0747-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="f0747-336">Paranna sähköisen raportoinnin ratkaisujen suorituskykyä lisäämällä parametrisoidut LASKETTU KENTTÄ -tietolähteet.</span><span class="sxs-lookup"><span data-stu-id="f0747-336">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]