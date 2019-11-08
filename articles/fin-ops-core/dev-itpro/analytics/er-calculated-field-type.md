---
title: Laskettu kenttä -tyyppisten ER-tietolähteiden parametrisoitujen kutsujen tuki
description: Tässä ohjeaiheessa käsitellään ER-tietolähteiden Laskettu kenttä -tyypin käyttöä.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 20d48795b23628bbba2896bf48940936a25e0435
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550081"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="59363-103">Laskettu kenttä -tyyppisten ER-tietolähteiden parametrisoitujen kutsujen tuki</span><span class="sxs-lookup"><span data-stu-id="59363-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59363-104">Tässä ohjeaiheessa käsitellään sähköisen raportoinnin (ER) tietolähteiden suunnittelua **Laskettu kenttä** -tyypin avulla.</span><span class="sxs-lookup"><span data-stu-id="59363-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="59363-105">Tietolähteessä voi olla ER-lauseke, jota voidaan suoritettaessa hallita niiden parametriargumenttien arvoilla, jotka on määritetty tätä tietolähdettä kutsuvassa sidonnassa.</span><span class="sxs-lookup"><span data-stu-id="59363-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="59363-106">Jos kyseisen tietolähteelle määritetään parametrisoidut kutsut, voit käyttää yhtä tietolähdettä useissa sidonnoissa, mikä vähentää ER-mallimäärityksissä tai ER-muodoissa määritettävien tietolähteiden kokonaismäärää.</span><span class="sxs-lookup"><span data-stu-id="59363-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="59363-107">Se myös yksinkertaistaa määritettyä ER-komponenttia, mikä puolestaan vähentää ylläpitokustannuksia ja muiden kuluttajien käyttökustannuksia.</span><span class="sxs-lookup"><span data-stu-id="59363-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="59363-108">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="59363-108">Prerequisites</span></span>
<span data-ttu-id="59363-109">Tämän aiheen esimerkkien suorittaminen edellyttää seuraavia käyttöoikeuksia:</span><span class="sxs-lookup"><span data-stu-id="59363-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="59363-110">Jonkin seuraavan roolin käyttöoikeus:</span><span class="sxs-lookup"><span data-stu-id="59363-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="59363-111">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="59363-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="59363-112">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="59363-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="59363-113">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="59363-113">System administrator</span></span>

- <span data-ttu-id="59363-114">Sellaisen Regulatory Configuration Servicesin (RCS) käyttöoikeus, joka on valmisteltu samalle vuokralaiselle kuin Finance and Operations yhdessä seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="59363-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="59363-115">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="59363-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="59363-116">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="59363-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="59363-117">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="59363-117">System administrator</span></span>

<span data-ttu-id="59363-118">Lataa [Microsoft Download Centerissä](https://go.microsoft.com/fwlink/?linkid=874684) pakattu zip-tiedosto **Laskettu kenttä -tyyppisten ER-tietolähteiden parametrisoitujen kutsujen tuki**.</span><span class="sxs-lookup"><span data-stu-id="59363-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="59363-119">Se sisältää seuraavat ER-kokoonpanot, jotka on purettava ja tallennettava paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="59363-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="59363-120">**Sisältö**</span><span class="sxs-lookup"><span data-stu-id="59363-120">**Content**</span></span>                           | <span data-ttu-id="59363-121">**Tiedostonimi**</span><span class="sxs-lookup"><span data-stu-id="59363-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59363-122">Esimerkin ER-tietomallin konfigurointi</span><span class="sxs-lookup"><span data-stu-id="59363-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="59363-123">Model to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="59363-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="59363-124">Esimerkin ER-metadatan konfigurointi</span><span class="sxs-lookup"><span data-stu-id="59363-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="59363-125">Metadata to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="59363-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="59363-126">Esimerkin ER-mallikartoituksen konfigurointi</span><span class="sxs-lookup"><span data-stu-id="59363-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="59363-127">Mapping to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="59363-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="59363-128">Esimerkin ER-format-konfigurointi</span><span class="sxs-lookup"><span data-stu-id="59363-128">Sample ER format configuration</span></span>        | <span data-ttu-id="59363-129">Format to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="59363-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="59363-130">Kirjautuminen RCS-esiintymään</span><span class="sxs-lookup"><span data-stu-id="59363-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="59363-131">Tällä esimerkissä luodaan määritys malliyritykselle Litware, Inc. Ensiksi on kuitenkin suoritettava RCS:ssä [Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="59363-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="59363-132">Valitse oletuskoontinäytössä **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="59363-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="59363-133">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="59363-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="59363-134">Tuo ladatut kokoonpanot RCS:ään seuraavassa järjestyksessä: tietomalli, metatiedot, mallin määritys, muoto.</span><span class="sxs-lookup"><span data-stu-id="59363-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="59363-135">Tee seuraavat vaiheet kussakin ER-kokoonpanossa:</span><span class="sxs-lookup"><span data-stu-id="59363-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="59363-136">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="59363-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="59363-137">Valitse **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="59363-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="59363-138">Valitse ensin **Selaa** ja sitten tarvittava XML-muotoinen ER-kokoonpano.</span><span class="sxs-lookup"><span data-stu-id="59363-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="59363-139">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="59363-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="59363-140">Annetun ER-ratkaisun tarkastelu</span><span class="sxs-lookup"><span data-stu-id="59363-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="59363-141">Mallin määrityksen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="59363-141">Review model mapping</span></span>

1. <span data-ttu-id="59363-142">Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.</span><span class="sxs-lookup"><span data-stu-id="59363-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="59363-143">Valitse **Mapping to learn parameterized calls**.</span><span class="sxs-lookup"><span data-stu-id="59363-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="59363-144">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="59363-144">Select **Designer**.</span></span>
4. <span data-ttu-id="59363-145">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="59363-145">Select **Designer**.</span></span>  
   
<span data-ttu-id="59363-146">Tämä ER-mallimääritys on suunniteltu seuraavia toimia varten:</span><span class="sxs-lookup"><span data-stu-id="59363-146">This ER model mapping is designed to do the following:</span></span>

- <span data-ttu-id="59363-147">**TaxTable**-taulussa olevan verokoodiluettelon (**Tax**-tietolähde) noutaminen.</span><span class="sxs-lookup"><span data-stu-id="59363-147">Fetch the list of tax codes (**Tax** data source) residing in the   **TaxTable** table.</span></span>
- <span data-ttu-id="59363-148">**TaxTable**-taulussa olevan verotapahtumaluettelon (**Trans**-tietolähde) noutaminen:</span><span class="sxs-lookup"><span data-stu-id="59363-148">Fetch the list of tax transactions (**Trans** data source) residing in the   **TaxTrans** table:</span></span>
    
    - <span data-ttu-id="59363-149">Noudetun tapahtumaluettelon ryhmittely (**Gr**-tietolähde) verokoodin mukaan.</span><span class="sxs-lookup"><span data-stu-id="59363-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
    - <span data-ttu-id="59363-150">Ryhmitettyjen tapahtumien laskeminen verokoodikohtaisten koostettujen arvojen mukaan:</span><span class="sxs-lookup"><span data-stu-id="59363-150">Calculate for grouped transactions following aggregated values per   tax code:</span></span>

        - <span data-ttu-id="59363-151">Veron perusarvojen summa.</span><span class="sxs-lookup"><span data-stu-id="59363-151">Sum of tax base values.</span></span>
        - <span data-ttu-id="59363-152">Veroarvojen summa.</span><span class="sxs-lookup"><span data-stu-id="59363-152">Sum of tax values.</span></span>
        - <span data-ttu-id="59363-153">Käytetyn veroprosentin vähimmäisarvo.</span><span class="sxs-lookup"><span data-stu-id="59363-153">Minimum value of applied tax rate.</span></span>

<span data-ttu-id="59363-154">Tässä kokoonpanossa mallin yhdistäminen käyttää tälle mallille luotujen ja Finance and Operationsissa suoritettujen ER-muotojen perustietomallia.</span><span class="sxs-lookup"><span data-stu-id="59363-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="59363-155">Tämän vuoksi **Tax**- ja **Gr**-tietolähteiden sisältö näkyy ER-muodoissa abstrakteina tietolähteinä.</span><span class="sxs-lookup"><span data-stu-id="59363-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

  ![Tax- ja Gr-tietolähteet näkyvät mallimäärityksen suunnittelusivulla](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="59363-157">Sulje **Mallimäärityksen sunnittelun** sivu.</span><span class="sxs-lookup"><span data-stu-id="59363-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="59363-158">Sulje **Mallimääritys**-sivu.</span><span class="sxs-lookup"><span data-stu-id="59363-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="59363-159">Muodon tarkastelu</span><span class="sxs-lookup"><span data-stu-id="59363-159">Review format</span></span>

1. <span data-ttu-id="59363-160">Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.</span><span class="sxs-lookup"><span data-stu-id="59363-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="59363-161">Valitse **Format to learn parameterized calls**.</span><span class="sxs-lookup"><span data-stu-id="59363-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="59363-162">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="59363-162">Select **Designer**.</span></span> <span data-ttu-id="59363-163">Tämä ER-muoto on suunniteltu seuraavia toimia varten:</span><span class="sxs-lookup"><span data-stu-id="59363-163">This ER format is designed to do the following:</span></span>

  - <span data-ttu-id="59363-164">XML-muotoisen veroilmoituksen luominen.</span><span class="sxs-lookup"><span data-stu-id="59363-164">Generate a tax statement in XML format.</span></span>
  - <span data-ttu-id="59363-165">Seuraavien verotustasojen näyttäminen veroilmoituksessa: normaali, alennettu ja ei mitään.</span><span class="sxs-lookup"><span data-stu-id="59363-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
  - <span data-ttu-id="59363-166">Useiden tietojen näyttäminen kustakin verotustasosta siten, että kunkin tason tiedoilla on eri numero.</span><span class="sxs-lookup"><span data-stu-id="59363-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

  ![Muodon suunnittelutoiminto -sivu](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="59363-168">Valitse **Määritys**.</span><span class="sxs-lookup"><span data-stu-id="59363-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="59363-169">Laajenna **Malli**, **Tiedot** ja **Yhteenveto**.</span><span class="sxs-lookup"><span data-stu-id="59363-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

   <span data-ttu-id="59363-170">Laskettu **Model.Data.Summary.Level** -kenttä sisältää lausekkeen, joka palauttaa verotustason koodin (**Normaali**, **Alennettu**, **Ei mitään** tai **Muu**) sellaisen verokoodin tekstiarvona, joka voidaan suorituksenaikaisesti noutaa **Model.Data.Summary**-tietolähteestä.</span><span class="sxs-lookup"><span data-stu-id="59363-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

  ![Model to learn parameterized calls -tietomallin tiedot muodon suunnittelusivulla](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="59363-172">Laajenna **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="59363-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="59363-173">Laajenna **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="59363-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
   <span data-ttu-id="59363-174">**Model**.**Data2.Summary2**-tietolähde on määritetty ryhmälle, jonka **Model.Data.Summary**-tietolähdetapahtuma erittelee verotustason mukaan (joka saadaan lasketusta **Model.Data.Summary.Level**-kentästä) ja laskee koosteet.</span><span class="sxs-lookup"><span data-stu-id="59363-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

  ![Model.Data2.Summary2-tietolähteen tiedot muodon suunnittelusivulla](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="59363-176">Tarkista lasketut **Model**.**Data2.Level1**, **Model**.**Data2.Level2**- ja **Model**.**Data2.Level3**-kentät.</span><span class="sxs-lookup"><span data-stu-id="59363-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="59363-177">**Model**.**Data2.Summary2**-tietueluettelo suodatetaan näiden laskettujen kenttien avulla palauttamaan vain tiettyä verotustasoa vastaavat tietueet.</span><span class="sxs-lookup"><span data-stu-id="59363-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="59363-178">Sulje **Muodon suunnittelija** -sivu.</span><span class="sxs-lookup"><span data-stu-id="59363-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="59363-179">Johdetun luominen</span><span class="sxs-lookup"><span data-stu-id="59363-179">Create a derived format</span></span>
<span data-ttu-id="59363-180">Voit parantaa annettua muotoa lisäämällä yhden lasketun kentän suodattamaan tarvittavan verotustason sen sijaan, että käyttäisit kolmea aiemmin luotua kenttää: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** ja **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="59363-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="59363-181">Tarvittava verotustaso voidaan määrittää sijainnissa, josta tämä uusi laskettu kenttä kutsutaan.</span><span class="sxs-lookup"><span data-stu-id="59363-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="59363-182">Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.</span><span class="sxs-lookup"><span data-stu-id="59363-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="59363-183">Valitse **Format to learn parameterized calls**.</span><span class="sxs-lookup"><span data-stu-id="59363-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="59363-184">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="59363-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="59363-185">Valitse **Derive from Name: Format to learn parameterized calls, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="59363-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="59363-186">Anna **Nimi**-kentässä **Format to learn parameterized calls (mukautettu)**.</span><span class="sxs-lookup"><span data-stu-id="59363-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="59363-187">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="59363-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="59363-188">Tietueluettelon palauttavan parametrisoidun lasketun kentän luominen</span><span class="sxs-lookup"><span data-stu-id="59363-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="59363-189">Aloittaminen lisäämällä uusi laskettu kenttä</span><span class="sxs-lookup"><span data-stu-id="59363-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="59363-190">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="59363-190">Select **Designer**.</span></span>
2. <span data-ttu-id="59363-191">Laajenna kaikki muotokohteet valitsemalla **Laajenna/tiivistä**.</span><span class="sxs-lookup"><span data-stu-id="59363-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="59363-192">Valitse **Määritys**.</span><span class="sxs-lookup"><span data-stu-id="59363-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="59363-193">Laajenna **Malli**.</span><span class="sxs-lookup"><span data-stu-id="59363-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="59363-194">Valitse **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="59363-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="59363-195">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="59363-195">Select **Add**.</span></span>
7. <span data-ttu-id="59363-196">Valitse **Toiminnot\\Lasketut kentät**.</span><span class="sxs-lookup"><span data-stu-id="59363-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="59363-197">Kirjoita **Nimi**-kenttään **Tasot**.</span><span class="sxs-lookup"><span data-stu-id="59363-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="59363-198">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="59363-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="59363-199">Parametrin määrittäminen lasketun kentän lisäämistä varten</span><span class="sxs-lookup"><span data-stu-id="59363-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="59363-200">Valitse **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="59363-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="59363-201">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="59363-201">Select **New**.</span></span>
3. <span data-ttu-id="59363-202">Kirjoita **Nimi**-kenttään **Verotustaso**.</span><span class="sxs-lookup"><span data-stu-id="59363-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="59363-203">Kirjoita **Tyyppi**-kenttään **Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="59363-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="59363-204">Parametrin argumenttityypin määrittämisessä voidaan käyttää vain primitiivisiä tietotyyppejä.</span><span class="sxs-lookup"><span data-stu-id="59363-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="59363-205">Niissä tähän tarkoitukseen ei voi käyttää **Tietueluettelo**-, **Tietue**- ja **Valintalista**-tyyppejä.</span><span class="sxs-lookup"><span data-stu-id="59363-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="59363-206">Yhdelle lasketulle kentälle voi määrittää enintään 8 parametria.</span><span class="sxs-lookup"><span data-stu-id="59363-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Parametrin tietolähdeluettelo](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="59363-208">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="59363-208">Select **OK**.</span></span>

<span data-ttu-id="59363-209">Tämän parametrin lisääminen määrittää ehdon, joka on oltava käytössä, jotta tämän lasketun kentän voi kutsua.</span><span class="sxs-lookup"><span data-stu-id="59363-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="59363-210">Tämän lasketun kentän kutsuminen edellyttää, että **Verotustaso**-parametrin argumentti määritetään arvoksi **Merkkijono**-muodossa.</span><span class="sxs-lookup"><span data-stu-id="59363-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="59363-211">Varmista, että määrität parametrit vain säilössä oleville lasketuille kentille (joko **Tietueluettelo**, **Tietue** tai **Säilö**).</span><span class="sxs-lookup"><span data-stu-id="59363-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="59363-212">Määritetty parametri on käytettävissä tämän lasketun kentän tietolähdeluettelossa.</span><span class="sxs-lookup"><span data-stu-id="59363-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="59363-213">Voit lisätä parametrin määritettyyn lausekkeeseen valitsemalla **Lisää tietolähde**.</span><span class="sxs-lookup"><span data-stu-id="59363-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Tietolähdekentät](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="59363-215">Lasketun kentän lisäämän lausekkeen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="59363-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="59363-216">Kirjoita **Resepti**-kenttään:</span><span class="sxs-lookup"><span data-stu-id="59363-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="59363-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="59363-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="59363-218">Valitse tietolähdeluettelossa **Verotustaso**-parametri.</span><span class="sxs-lookup"><span data-stu-id="59363-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="59363-219">Valitse **Lisää tietolähde**.</span><span class="sxs-lookup"><span data-stu-id="59363-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="59363-220">Viimeistele lauseke **Resepti**-kentässä muotoon:</span><span class="sxs-lookup"><span data-stu-id="59363-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="59363-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Verotustaso')**</span><span class="sxs-lookup"><span data-stu-id="59363-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="59363-222">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="59363-222">Select **Save**.</span></span>

    ![Tietolähdekentän tiedot](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="59363-224">Sulje **Reseptien suunnittelu** -sivu.</span><span class="sxs-lookup"><span data-stu-id="59363-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="59363-225">Uuden lasketun kentän lisäämisen viimeistely</span><span class="sxs-lookup"><span data-stu-id="59363-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="59363-226">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="59363-226">Select **OK**.</span></span>

<span data-ttu-id="59363-227">**Reseptien suunnittelu** -sivulla oleva määritetty parametrisoitu laskettu **Tasot**-kenttä edellyttää **Merkkijono**-argumenttia.</span><span class="sxs-lookup"><span data-stu-id="59363-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Laajennettu lasketun kentän tasoluettelo](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="59363-229">Muodon elementtien sitominen määritetyn lasketun kentän avulla</span><span class="sxs-lookup"><span data-stu-id="59363-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="59363-230">Valitse laskettu kenttä valitsemalla **Model.Data2.Levels**.</span><span class="sxs-lookup"><span data-stu-id="59363-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="59363-231">Valitse **Statement.Taxation.Regular**-muotoelementti.</span><span class="sxs-lookup"><span data-stu-id="59363-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="59363-232">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="59363-232">Select **Bind**.</span></span>
4. <span data-ttu-id="59363-233">Valitsemalla **Kyllä** voit vahvistaa käytössä olevan tietolähteen **Taso1** korvaamisen uudella tietolähteellä **Tasot** kaikissa valitun muotoelementin sisäkkäisissä muotoelementeissä.</span><span class="sxs-lookup"><span data-stu-id="59363-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="59363-234">Kohdistettu sidonta on muodostettu parametrisoidun lasketun kentän kutsuna.</span><span class="sxs-lookup"><span data-stu-id="59363-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="59363-235">Sidotun muotoelementin nimeä käytetään oletusarvoisesti parametrisoidun lasketun kentän argumenttina seuraavien ehtojen mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="59363-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="59363-236">Laskettu kenttä on määritetty käyttämään yhtä parametria.</span><span class="sxs-lookup"><span data-stu-id="59363-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="59363-237">Kyseisen parametrin tietotyypiksi on määritetty **merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="59363-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="59363-238">Jos sidotun muotoelementin nimi on tyhjä, kyseisen elementin tietolähteen nimeä käytetään kohdistetussa sidonnassa.</span><span class="sxs-lookup"><span data-stu-id="59363-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="59363-239">Valitse **Statement.Taxation.Reduced**-muotoelementti.</span><span class="sxs-lookup"><span data-stu-id="59363-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="59363-240">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="59363-240">Select **Bind**.</span></span>
7. <span data-ttu-id="59363-241">Valitsemalla **Kyllä** voit vahvistaa käytössä olevan tietolähteen **Taso2** korvaamisen uudella tietolähteellä **Tasot** kaikissa valitun muotoelementin sisäkkäisissä muotoelementeissä.</span><span class="sxs-lookup"><span data-stu-id="59363-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="59363-242">Valitse **Statement.Taxation.None**-muotoelementti.</span><span class="sxs-lookup"><span data-stu-id="59363-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="59363-243">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="59363-243">Select **Bind**.</span></span>
10. <span data-ttu-id="59363-244">Valitsemalla **Kyllä** voit vahvistaa käytössä olevan tietolähteen **Taso3** korvaamisen uudella tietolähteellä **Tasot** kaikissa valitun muotoelementin sisäkkäisissä muotoelementeissä.</span><span class="sxs-lookup"><span data-stu-id="59363-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="59363-245">Jos määrität verotustasoon viittaavan XML-elementin (kuten **Model.Data2.Levels("Alennettu")** tekstiarvona) parametrisoidun lasketun kentän argumentin, samaa ei tarvitse tehdä sisäkkäisille XML-määritteille, sillä niiden sidonnat perivät automaattisesti päätasolla määritetyn argumentin arvon (**Model.Data2.Levels.aggregated.Base**, ei siis **Model.Data2.Levels("Alennettu").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="59363-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="59363-246">Parametrisoidun lasketun kentän toistuvia kutsuja ei tueta.</span><span class="sxs-lookup"><span data-stu-id="59363-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="59363-247">Voit valita **Muokkaa reseptiä** ja muuta valitussa sidonnassa olevan parametrisoidun lasketun kentän oletusarvoista kohdistusta.</span><span class="sxs-lookup"><span data-stu-id="59363-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="59363-248">Jos tämä argumentti puuttuu, seurauksena voi olla suorituksenaikaisia virheitä; käyttäjille ilmoitetaan tällaisesta tilanteesta, kun nykyinen muoto vahvistetaan.</span><span class="sxs-lookup"><span data-stu-id="59363-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Vahvistuksen varoitusilmoitus](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="59363-250">Tietueen palauttavan parametrisoidun lasketun kentän luominen</span><span class="sxs-lookup"><span data-stu-id="59363-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="59363-251">Kun parametrisoitu laskettu kenttä palauttaa tietueen, tämän tietueen yksittäisten kenttien tukemista muotoelementteihin on tuettava.</span><span class="sxs-lookup"><span data-stu-id="59363-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="59363-252">Tällaisissa tapauksissa ei ole pääsidontaa, joka sisältää parametrisoidun lasketun kentän kutsuvan argumentin arvon. Tämä arvo on määritettävä yksittäisen tietuen kentässä.</span><span class="sxs-lookup"><span data-stu-id="59363-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="59363-253">Aloittaminen lisäämällä uusi laskettu kenttä</span><span class="sxs-lookup"><span data-stu-id="59363-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="59363-254">Valitse **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="59363-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="59363-255">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="59363-255">Select **Add**.</span></span>
3. <span data-ttu-id="59363-256">Valitse **Toiminnot\\Lasketut kentät**.</span><span class="sxs-lookup"><span data-stu-id="59363-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="59363-257">Kirjoita **Nimi**-kenttään **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="59363-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="59363-258">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="59363-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="59363-259">Parametrin määrittäminen lasketun kentän lisäämistä varten</span><span class="sxs-lookup"><span data-stu-id="59363-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="59363-260">Valitse **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="59363-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="59363-261">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="59363-261">Select **New**.</span></span>
3. <span data-ttu-id="59363-262">Kirjoita **Nimi**-kenttään **Verotustaso**.</span><span class="sxs-lookup"><span data-stu-id="59363-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="59363-263">Kirjoita **Tyyppi**-kenttään **Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="59363-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="59363-264">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="59363-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="59363-265">Lasketun kentän lisäämän lausekkeen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="59363-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="59363-266">Kirjoita **Resepti**-kenttään</span><span class="sxs-lookup"><span data-stu-id="59363-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="59363-267">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="59363-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="59363-268">Valitse **Verotustaso**-parametri.</span><span class="sxs-lookup"><span data-stu-id="59363-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="59363-269">Valitse **Lisää tietolähde**.</span><span class="sxs-lookup"><span data-stu-id="59363-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="59363-270">Liitä **Resepti**-kentässä **'Verotustaso'))** tekstiin, jonka kirjoitit vaiheessa 1. Lauseke viimeistellään muotoon:</span><span class="sxs-lookup"><span data-stu-id="59363-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="59363-271">**FIRSTORNULL(\@.Levels('Verotustaso'))**</span><span class="sxs-lookup"><span data-stu-id="59363-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="59363-272">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="59363-272">Select **Save**.</span></span>
6. <span data-ttu-id="59363-273">Sulje **Reseptien suunnittelu** -sivu.</span><span class="sxs-lookup"><span data-stu-id="59363-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="59363-274">Uuden lasketun kentän lisäämisen viimeistely</span><span class="sxs-lookup"><span data-stu-id="59363-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="59363-275">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="59363-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="59363-276">Muodon elementtien sitominen määritetyn lasketun kentän avulla</span><span class="sxs-lookup"><span data-stu-id="59363-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="59363-277">Valitse määritetty laskettu kenttä laajentamalla **Model.Data2.LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="59363-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="59363-278">Laajenna määritetyn lasketun kentän **Model.Data2.LevelRecord.aggregated**-säilö.</span><span class="sxs-lookup"><span data-stu-id="59363-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="59363-279">Valitse **Model.Data2.LevelRecord.aggregated.Base**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="59363-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="59363-280">Valitse **Statement.Taxation.None**-muotoelementti.</span><span class="sxs-lookup"><span data-stu-id="59363-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="59363-281">Valitse **Poista sidonta**.</span><span class="sxs-lookup"><span data-stu-id="59363-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="59363-282">Valitse **Statement.Taxation.None.Base**-muotoelementti.</span><span class="sxs-lookup"><span data-stu-id="59363-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="59363-283">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="59363-283">Select **Bind**.</span></span>
8. <span data-ttu-id="59363-284">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="59363-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="59363-285">Muuta lauseke muotoon **Model.Data2.LevelRecord("Ei mitään").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="59363-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Päivitetty lauseke](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="59363-287">Käyttämättömien laskettujen kenttien poistaminen</span><span class="sxs-lookup"><span data-stu-id="59363-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="59363-288">Valitse **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="59363-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="59363-289">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="59363-289">Select **Delete**.</span></span>
3. <span data-ttu-id="59363-290">Valitse **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="59363-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="59363-291">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="59363-291">Select **Delete**.</span></span>
5. <span data-ttu-id="59363-292">Valitse **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="59363-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="59363-293">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="59363-293">Select **Delete**.</span></span>
7. <span data-ttu-id="59363-294">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="59363-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="59363-295">Käytit samaa laskettua **Model.Data2.Levels**-kenttää useita kertoja muodon sidonnoissa.</span><span class="sxs-lookup"><span data-stu-id="59363-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="59363-296">Yhden lasketun kentän käyttäminen ja ylläpitäminen on paljon helpompaa kuin useiden samankaltaisten kenttien käyttö ja ylläpito.</span><span class="sxs-lookup"><span data-stu-id="59363-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="59363-297">Sulje **Muodon suunnittelija** -sivu.</span><span class="sxs-lookup"><span data-stu-id="59363-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="59363-298">Johdetun muodon korjatun version viimeisteleminen</span><span class="sxs-lookup"><span data-stu-id="59363-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="59363-299">Valitse **Versiot**-pikavälilehdessä **Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="59363-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="59363-300">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="59363-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="59363-301">Johdetun muodon valmiin version vieminen</span><span class="sxs-lookup"><span data-stu-id="59363-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="59363-302">Valitse kokoonpanopuussa **Format to learn parameterized calls (mukautettu)**.</span><span class="sxs-lookup"><span data-stu-id="59363-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="59363-303">Valitse **Version**-pikavälilehdessä valmis versio 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="59363-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="59363-304">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="59363-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="59363-305">Valitse **Vie XML-tiedostona**.</span><span class="sxs-lookup"><span data-stu-id="59363-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="59363-306">Tallenna ladattu kokoonpano paikallisesti XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="59363-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="59363-307">ER-muotojen testaaminen</span><span class="sxs-lookup"><span data-stu-id="59363-307">Test ER formats</span></span> 
<span data-ttu-id="59363-308">Voit suorittaa alkuperäiset ja parannetut ER-muodot ja varmistaa tällä tavoin, että määritetyt parametrisoidut lasketut kentät toimivat oikein.</span><span class="sxs-lookup"><span data-stu-id="59363-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="59363-309">ER-konfiguraatioiden tuominen</span><span class="sxs-lookup"><span data-stu-id="59363-309">Import ER configurations</span></span>
<span data-ttu-id="59363-310">Voit tuoda tarkistetut kokoonpanot RCS:stä käyttämällä **RCS**-tyyppistä ER-säilöä.</span><span class="sxs-lookup"><span data-stu-id="59363-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="59363-311">Jos olet jo suorittanut ohjeaiheen [Sähköisen raportoinnin konfiguraatioiden tuonti Regulatory Configuration Services (RCS) -palvelusta](rcs-download-configurations.md) vaiheet, tuo aiemmin tässä aiheessa käsitellyt määritykset ympäristöön määritetyn ER-säilön avulla.</span><span class="sxs-lookup"><span data-stu-id="59363-311">If you already went through the steps in the topic, [Import Electronic reporting configurations from Regulatory Configuration Services](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="59363-312">Toimi muussa tapauksessa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="59363-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="59363-313">Valitse **DEMF**-yritys ja valitse oletuskoontinäytössä **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="59363-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="59363-314">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="59363-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="59363-315">Tuo kokoonpanot Microsoft Download Centeristä seuraavassa järjestyksessä: tietomalli, mallin määritys, muoto.</span><span class="sxs-lookup"><span data-stu-id="59363-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="59363-316">Tee seuraavat vaiheet kussakin ER-kokoonpanossa:</span><span class="sxs-lookup"><span data-stu-id="59363-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="59363-317">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="59363-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="59363-318">Valitse **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="59363-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="59363-319">Valitse ensin **Selaa** ja sitten tarvittava XML-muotoinen ER-kokoonpano.</span><span class="sxs-lookup"><span data-stu-id="59363-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="59363-320">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="59363-320">Select **OK**.</span></span>

4. <span data-ttu-id="59363-321">Tuo RCS:stä viety **Format to learn parameterized calls (mukautettu)** -muodon valmis versio 1.1.1:</span><span class="sxs-lookup"><span data-stu-id="59363-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="59363-322">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="59363-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="59363-323">Valitse **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="59363-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="59363-324">Valitse ensin **Selaa** ja sitten paikallisesti tallennettu XML-muotoinen **Format to learn parameterized calls (mukautettu)** -tiedosto.</span><span class="sxs-lookup"><span data-stu-id="59363-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="59363-325">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="59363-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="59363-326">ER-muotojen suorittaminen</span><span class="sxs-lookup"><span data-stu-id="59363-326">Run ER formats</span></span>

1. <span data-ttu-id="59363-327">Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.</span><span class="sxs-lookup"><span data-stu-id="59363-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="59363-328">Valitse **Format to learn parameterized calls**.</span><span class="sxs-lookup"><span data-stu-id="59363-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="59363-329">Valitse ylimmässä valintanauhassa **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="59363-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="59363-330">Tallenna paikallisesti luotu tuotos.</span><span class="sxs-lookup"><span data-stu-id="59363-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="59363-331">Valitse **Format to learn parameterized calls (mukautettu)**.</span><span class="sxs-lookup"><span data-stu-id="59363-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="59363-332">Valitse ylimmässä valintanauhassa **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="59363-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="59363-333">Tallenna luotu tuotos paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="59363-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="59363-334">Vertaa luotujen tuotosten sisältöä.</span><span class="sxs-lookup"><span data-stu-id="59363-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59363-335">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="59363-335">Additional resources</span></span>
[<span data-ttu-id="59363-336">Sähköisen raportoinnin kaavojen suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="59363-336">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
