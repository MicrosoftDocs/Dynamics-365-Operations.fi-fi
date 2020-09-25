---
title: Paranna sähköisen raportoinnin ratkaisujen suorituskykyä lisäämällä parametrisoidut LASKETTU KENTTÄ -tietolähteet.
description: Tässä ohjeaiheessa kerrotaan, miten sähköisen raportoinnin ratkaisujen suorituskykyä voi parantaa lisäämällä parametrisoidut LASKETTU KENTTÄ -tietolähteet.
author: NickSelin
manager: AnnBe
ms.date: 09/02/2020
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
ms.openlocfilehash: a87098e82284a4951f3a4de050f6ba3f587fd20a
ms.sourcegitcommit: 5472005274f2f94fba82dda90de128f39d8b8390
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760079"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="e8329-103">Paranna sähköisen raportoinnin ratkaisujen suorituskykyä lisäämällä parametrisoidut LASKETTU KENTTÄ -tietolähteet.</span><span class="sxs-lookup"><span data-stu-id="e8329-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8329-104">Tässä ohjeaiheessa kerrotaan, miten voit [jäljittää suorituskykyä](trace-execution-er-troubleshoot-perf.md) suoritetuissa [sähköisen raportoinnin](general-electronic-reporting.md) muodoissa ja käyttää sitten näitä jäljitystietoja suorituskyvyn parantamisessa määrittämällä parametrisoitu **Laskettu kenttä** -tietolähde.</span><span class="sxs-lookup"><span data-stu-id="e8329-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="e8329-105">Osana sähköisen raportoinnin konfiguraation suunnittelua yritysasiakirjojen luomista varten määritetään menetelmä, jonka avulla tiedot haetaan sovelluksesta ja syötetään luotavaan tuotokseen.</span><span class="sxs-lookup"><span data-stu-id="e8329-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="e8329-106">Kun parametrisoidun sähköisen raportoinnin **Laskettu kenttä** -tyyppinen tietolähde on suunniteltu, voit vähentää tietokantakutsujen määrää sekä vähentää merkittävästi aikaa, joka kuluu sähköisen raportoinnin muodon suorituksen tietojen keräämiseen kuluvaa aikaa ja käytettyjä kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="e8329-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e8329-107">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="e8329-107">Prerequisites</span></span>

- <span data-ttu-id="e8329-108">Tässä ohjeaiheessa olevien esimerkkien suorittaminen edellyttää käyttöoikeutta johonkin seuraavaan [rooliin](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="e8329-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="e8329-109">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="e8329-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="e8329-110">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="e8329-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="e8329-111">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="e8329-111">System administrator</span></span>

- <span data-ttu-id="e8329-112">Yritykselle on asetettava **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="e8329-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="e8329-113">Tämän ohjeaiheen [lisäyksen 1](#appendix1) vaiheiden mukaisesti voit ladata tämän ohjeaiheen esimerkkien suorittamisessa tarvittavien Microsoftin sähköisen raportoinnin näyteratkaisun komponentit.</span><span class="sxs-lookup"><span data-stu-id="e8329-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="e8329-114">Määritä tämän ohjeaiheen [lisäyksen 2](#appendix2) ohjeiden avulla sähköisen raportoinnin parametrien vähimmäismäärä, joka vaaditaan sähköisen raportoinnin kehystä varten Microsoftin sähköisen raportoinnin näyteratkaisin suorituskyvyn parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="e8329-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="e8329-115">Sähköisen raportoinnin näyteratkaisun tuominen</span><span class="sxs-lookup"><span data-stu-id="e8329-115">Import the sample ER solution</span></span>

<span data-ttu-id="e8329-116">Oletetaan, että sinun on suunniteltava uusi sähköisen raportoinnin ratkaisu, jonka avulla luodaan toimittajatapahtumat näyttävä uusi raportti.</span><span class="sxs-lookup"><span data-stu-id="e8329-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="e8329-117">Tällä hetkellä voit etsiä valitun toimittajan tapahtumat **Toimittajatapahtumat**-sivulta (Siirry **Ostoreskontra** \> **Toimittajat** \> **Kaikki toimittajat**, valitse toimittaja ja sitten toimintoruudun **Toimittaja**-välilehti kohdassa valitse **Tapahtumat**-ryhmästä **Tapahtumat**).</span><span class="sxs-lookup"><span data-stu-id="e8329-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="e8329-118">Haluat kuitenkin saada kaikki toimittajatapahtumat yhdessä sähköisessä asiakirjassa XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="e8329-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="e8329-119">Tämä ratkaisu koostuu useista sähköisen raportoinnin konfiguraatioista, jotka sisältävät vaaditun tietomallin, mallien yhdistämismääritykset ja muotokomponentit.</span><span class="sxs-lookup"><span data-stu-id="e8329-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="e8329-120">Ensimmäinen vaihe on sähköisen raportoinnin näyteratkaisun tuominen toimittajatapahtumien luomista varten.</span><span class="sxs-lookup"><span data-stu-id="e8329-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="e8329-121">Kirjaudu Microsoft Dynamics 365 Financen esiintymään, joka on valmisteltu yrityksellesi.</span><span class="sxs-lookup"><span data-stu-id="e8329-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="e8329-122">Tässä aiheessa luodaan ja muokataan konfiguraatioita malliyritykselle **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="e8329-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="e8329-123">Varmista, että tämä konfiguraation tarjoaja on lisätty Finance-esiintymään ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="e8329-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="e8329-124">Lisätietoja on kohdassa [Määrityspalvelujen luonti ja merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e8329-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="e8329-125">Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="e8329-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="e8329-126">Tuo **Konfiguraatiot** -sivulla lataamasi ER-kokoonpanot Financen edellytyksenä seuraavassa järjestyksessä: tietomalli, metatiedot, mallikartoitus, muoto.</span><span class="sxs-lookup"><span data-stu-id="e8329-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="e8329-127">Luo kukin mukautus seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e8329-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="e8329-128">Valitse toimintoruudussa **Vaihda** \> **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="e8329-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="e8329-129">Valitse soveltuva sähköisen raportoinnin konfiguraation tiedosto XML-muodossa valitsemalla **Selaa**.</span><span class="sxs-lookup"><span data-stu-id="e8329-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="e8329-130">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8329-130">Select **OK**.</span></span>

![Konfiguraatiot-sivun tuodut konfiguraatiot](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="e8329-132">Sähköisen raportoinnin näyteratkaisun tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="e8329-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="e8329-133">Mallin määrityksen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="e8329-133">Review the model mapping</span></span>

1. <span data-ttu-id="e8329-134">Valitse **Konfiguraatiot**-sivun konfiguraatiopuu, laajenna **Suorituskyvyn parantamisen malli** ja valitse sitten **Suorituskyvyn parantamisen yhdistämismääritys**.</span><span class="sxs-lookup"><span data-stu-id="e8329-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="e8329-135">Valitse toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="e8329-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="e8329-136">Valitse **Malli tietolähteen yhdistämismääritystä varten** -sivun toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="e8329-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="e8329-137">Tämä sähköisen raportoinnin mallin yhdistämismääritys on suunniteltu seuraavia toimintoja varten:</span><span class="sxs-lookup"><span data-stu-id="e8329-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="e8329-138">Hae VendTrans-tauluun (**Trans**-tietolähde) tallennettujen toimittajatapahtumien luettelo.</span><span class="sxs-lookup"><span data-stu-id="e8329-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="e8329-139">Hae jokaiselle tapahtumalle VendTable-taulusta toimittajatietue, johon tapahtuma on kirjattu (**\#Vend**-tietolähde).</span><span class="sxs-lookup"><span data-stu-id="e8329-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="e8329-140">**\#Vend**-tietolähde on määritetty hakemaan vastaava toimittajatietue käyttämällä olemassa olevaa monta yhteen -suhdetta **\@.'\>Relations'.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="e8329-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="e8329-141">Tässä kokoonpanossa mallin yhdistäminen käyttää tälle mallille luotujen ja Financessa suoritettujen sähköisen raportoinnin muotojen perustietomallia.</span><span class="sxs-lookup"><span data-stu-id="e8329-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="e8329-142">Tämän vuoksi **Trans**-tietolähteen sisältö näkyy sähköisen raportoinnin muodoissa, esimerkiksi abstrakteina **mallitietolähteinä**.</span><span class="sxs-lookup"><span data-stu-id="e8329-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![Mallin yhdistämismäärityksen suunnitteluohjelman sivun Trans-tietolähde](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="e8329-144">Sulje **Mallimäärityksen sunnittelun** sivu.</span><span class="sxs-lookup"><span data-stu-id="e8329-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="e8329-145">Sulje **Malli tietolähteen yhdistämismääritystä varten** -sivu.</span><span class="sxs-lookup"><span data-stu-id="e8329-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="e8329-146">Muodon tarkastelu</span><span class="sxs-lookup"><span data-stu-id="e8329-146">Review format</span></span>

1. <span data-ttu-id="e8329-147">Valitse **Konfiguraatiot**-sivun konfiguraatiopuu, laajenna **Suorituskyvyn parantamisen malli** ja valitse sitten **Suorituskyvyn parantamisen muoto**.</span><span class="sxs-lookup"><span data-stu-id="e8329-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="e8329-148">Valitse toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="e8329-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="e8329-149">Valitse **Muodon suunnittelu** -sivun **Yhdistämismääritys**-välilehdessä **Laajenna/kutista**.</span><span class="sxs-lookup"><span data-stu-id="e8329-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="e8329-150">Laajenna **Malli**-, **Tiedot**- ja **Tapahtuma**-kohteet.</span><span class="sxs-lookup"><span data-stu-id="e8329-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="e8329-151">Tämä sähköisen raportoinnin muoto on suunniteltu toimittajatapahtumien raportin luomiseksi XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="e8329-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![Muootile tietolähteet ja määritetyt muotoiluelementtien sidokset Muodon suunnittelutoiminto -sivulla](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="e8329-153">Sulje **Muodon suunnittelija** -sivu.</span><span class="sxs-lookup"><span data-stu-id="e8329-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="e8329-154">Sähköisen raportoinnin näyteratkaisun suorittaminen jäljityksen suorittamista varten</span><span class="sxs-lookup"><span data-stu-id="e8329-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="e8329-155">Ajatellaan, että olet suunnitellut sähköisen raportoinnin ratkaisun ensimmäisen version.</span><span class="sxs-lookup"><span data-stu-id="e8329-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="e8329-156">Haluat nyt testata ratkaisun Finance-esiintymässä ja analysoida suorituskyvyn.</span><span class="sxs-lookup"><span data-stu-id="e8329-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="e8329-157">ER-suorituskykyjäljityksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e8329-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="e8329-158">Valitse **DEMF**-yritys.</span><span class="sxs-lookup"><span data-stu-id="e8329-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="e8329-159">Seuraa [ER-suorituskykyjäljityksen ottaminen käyttöön](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) -kohdan ohjeita ja luo suorituskykyjäljitys sähköisen raportoinnin muotoilun suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="e8329-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![Käyttäjän parametrit -valintaikkuna](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="e8329-161">Suorita ER-muoto</span><span class="sxs-lookup"><span data-stu-id="e8329-161">Run the ER format</span></span>

1. <span data-ttu-id="e8329-162">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="e8329-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e8329-163">Valitse **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn parantamisen muoto**.</span><span class="sxs-lookup"><span data-stu-id="e8329-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="e8329-164">Valitse toimintoruudussa **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="e8329-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="e8329-165">Suorituskykyjäljityksen käyttäminen mallin yhdistämismäärityksen suorituskyvyn analysoimisessa</span><span class="sxs-lookup"><span data-stu-id="e8329-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="e8329-166">Valitse **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn parantamisen yhdistämismääritys**.</span><span class="sxs-lookup"><span data-stu-id="e8329-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="e8329-167">Valitse toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="e8329-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="e8329-168">Valitse **Mallin yhdistämismääritykset** -sivun toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="e8329-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="e8329-169">Valitse **Mallin määrityssuunnittelija** -sivulla hallintapaneelista **Suorituskyvyn jäljitysmuoto**.</span><span class="sxs-lookup"><span data-stu-id="e8329-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="e8329-170">Valitse uusin jäljitys ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8329-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="e8329-171">Joidenkin nykyisen mallin yhdistämismääritysten tietolähdenimikkeiden käytettävissä on nyt uusia tietoja:</span><span class="sxs-lookup"><span data-stu-id="e8329-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="e8329-172">Tietolähteen avulla tietoja haettaessa käytetty todellinen aika</span><span class="sxs-lookup"><span data-stu-id="e8329-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="e8329-173">Sama aika ilmaistaan prosentteina kokonaisajasta, joka käytettiin koko mallin määrityksen suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="e8329-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![Mallin yhdistämismäärityksen suunnittelu -sivun suoritusajan tiedot](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="e8329-175">**Suorituskyvyn tilastotiedot** -ruudukossa on tieto, että **Trans**-tietolähde kutsuu VendTrans-taulua kerran.</span><span class="sxs-lookup"><span data-stu-id="e8329-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="e8329-176">Arvo **\[265\]\[Q:265\]** **Trans**-tietolähteessä osoittaa, että 265 toimittajatapahtumaa on noudettu sovelluksen taulusta ja palautettu tietomallille.</span><span class="sxs-lookup"><span data-stu-id="e8329-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="e8329-177">**Suorituskyvyn tilastotiedot** -ruudukossa on myös nykyisen mallin yhdistämismäärityksen kaksoiskappaleiden tietokantapyynnöt, kun **\#Vend**-tietolähdettä suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="e8329-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="e8329-178">Kaksoiskappaleita tulee seuraavista syistä:</span><span class="sxs-lookup"><span data-stu-id="e8329-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="e8329-179">Toimittajan taulua kutsutaan kaksi kertaa jokaista 265 iteroitua toimittajatapahtumaa kohden. Yhteensä kutsuja on 530:</span><span class="sxs-lookup"><span data-stu-id="e8329-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="e8329-180">Yksi kutsu tehdään toimittajan tilinumeron syöttämistä varten.</span><span class="sxs-lookup"><span data-stu-id="e8329-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="e8329-181">Yksi kutsu tehdään toimittajan nimen syöttämistä varten.</span><span class="sxs-lookup"><span data-stu-id="e8329-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="e8329-182">Toimittajan taulua kutsutaan jokaista iteroitua toimittajatapahtumaa kohden, vaikka noudetut tapahtumat on kirjattu vain viidelle toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="e8329-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="e8329-183">530 kutsusta 525 on kaksoiskappaleita.</span><span class="sxs-lookup"><span data-stu-id="e8329-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="e8329-184">Seuraavassa kuvassa näkyy sanoma, joka ilmaisee, että kutsut ovat päällekkäisiä kutsuja (tietokantapyyntöjä).</span><span class="sxs-lookup"><span data-stu-id="e8329-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![Virheilmoitus tietokantapyyntöjen kaksoiskappaleista mallin yhdistämismäärityksen suunnittelusivulla](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="e8329-186">Ota huomioon, että yli 80 prosenttia (noin kuusi sekuntia) mallin yhdistämismäärityksen kokonaissuoritusajasta on kulunut VendTable-sovellustaulun arvojen hakemiseen.</span><span class="sxs-lookup"><span data-stu-id="e8329-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="e8329-187">Tämä prosenttiosuus on liian suuri viiden toimittajan kahdelle määritteelle verrattuna VendTrans-sovellustaulun tietojen määrään.</span><span class="sxs-lookup"><span data-stu-id="e8329-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="e8329-188">Voit vähentää kunkin tapahtuman toimittajan tietojen haussa käytettävien kutsujen määrää ja parantaa mallin yhdistämismäärityksne suorituskykyä käyttämällä **\#Vend**-tietolähteen välimuistiin tallentamista.</span><span class="sxs-lookup"><span data-stu-id="e8329-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="e8329-189">**Trans\\\#Vend**-tietolähde tallennetaan välimuistiin nykyiselle **Trans**-tietolähteelle suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="e8329-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="e8329-190">Kun **\#Vend**-tietolähde tallennetaan välimuistiin, kutsujen kaksoiskappaleiden määrä vähenee 525 kutsusta 260 kutsuun. Kaksoiskappaleita kuitenkin on yhä.</span><span class="sxs-lookup"><span data-stu-id="e8329-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="e8329-191">Voit poistaa kaksoiskappaleet kokonaan määrittämällä uuden parametrisoidun tietolähteen, jonka tyyppi on **Laskettu kenttä**.</span><span class="sxs-lookup"><span data-stu-id="e8329-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="e8329-192">Paranna mallin määritystä suorituksen jälkeisten tietojen perusteella</span><span class="sxs-lookup"><span data-stu-id="e8329-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="e8329-193">Mallin yhdistämismäärityksen logiikan muuttaminen</span><span class="sxs-lookup"><span data-stu-id="e8329-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="e8329-194">Näiden ohjeiden avulla voit käyttää **Laskettu kenttä** -tyyppistä tietolähdettä. Se auttaa estämään tietokannan kutsujen kaksoiskappaleita.</span><span class="sxs-lookup"><span data-stu-id="e8329-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="e8329-195">Valitse **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn parantamisen yhdistämismääritys**.</span><span class="sxs-lookup"><span data-stu-id="e8329-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="e8329-196">Valitse toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="e8329-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="e8329-197">Valitse **Mallin yhdistämismääritykset** -sivun toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="e8329-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="e8329-198">Lisää **Mallin yhdistämismäärityksen suunnittelija** -sivulla **Taulun tietueet** -tyyppinen tietolähde VendTable-sovellustauluun seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e8329-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="e8329-199">Laajenna **Tietolähdetyypit** -ruudussa **Dynamics 365 for Operations** ja valitse **Taulun tietueet**.</span><span class="sxs-lookup"><span data-stu-id="e8329-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="e8329-200">Valitse **Lisää pääkansio**.</span><span class="sxs-lookup"><span data-stu-id="e8329-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="e8329-201">Anna valintaikkunan **Nimi**-kenttään **Vend**-arvo.</span><span class="sxs-lookup"><span data-stu-id="e8329-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="e8329-202">Anna **Taulu**-kenttään **VendTable**-arvo.</span><span class="sxs-lookup"><span data-stu-id="e8329-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="e8329-203">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8329-203">Select **OK**.</span></span>

5. <span data-ttu-id="e8329-204">Voit parametrisoida **Laskettu kenttä** -tyyppisten tietolähteiden kutsut vain, jos nämä tietolähteet ovat säilössä.</span><span class="sxs-lookup"><span data-stu-id="e8329-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="e8329-205">Noudata tämän vuoksi näitä ohjeita, jos haluat lisätä **Tyhjä säilö** -tyyppisen tietolähteen uuden **Laskettu kenttä** -tyyppisen parametrisoidun tietolähteen tallennuspaikaksi.</span><span class="sxs-lookup"><span data-stu-id="e8329-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="e8329-206">Laajenna **Tietolähdetyypit** -ruudussa **Yleistä** ja valitse **Tyhjä säilö**.</span><span class="sxs-lookup"><span data-stu-id="e8329-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="e8329-207">Valitse **Lisää pääkansio**.</span><span class="sxs-lookup"><span data-stu-id="e8329-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="e8329-208">Anna valintaikkunan **Nimi**-kenttään **Box**-arvo.</span><span class="sxs-lookup"><span data-stu-id="e8329-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="e8329-209">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8329-209">Select **OK**.</span></span>

    ![Mallin yhdistämismäärityksen suunnitteluohjelman sivun Box-tietolähde](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="e8329-211">Lisää **Laskettu kenttä** -tyyppinen parametrisoitu tietolähde seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e8329-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="e8329-212">Valitse **Tietolähteet**-ruudussa **Box**.</span><span class="sxs-lookup"><span data-stu-id="e8329-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="e8329-213">Laajenna **Tietolähdetyypit**-ruudussa **Funktiot** ja valitse **Laskettu kenttä**.</span><span class="sxs-lookup"><span data-stu-id="e8329-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="e8329-214">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e8329-214">Select **Add**.</span></span>
    4. <span data-ttu-id="e8329-215">Anna valintaikkunan **Nimi**-kenttään **Vend**-arvo.</span><span class="sxs-lookup"><span data-stu-id="e8329-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="e8329-216">Valitse **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="e8329-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="e8329-217">Valitse **Kaavan suunnittelutoiminto** -sivulla **Parametrit** ja määritä, mitkä parametrit on annettava tietolähteen kutsumisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e8329-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="e8329-218">Valitse **Parametrit**-valintaruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e8329-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="e8329-219">Anna **Nimi**-kenttään **parmVendAccNumber**-arvo.</span><span class="sxs-lookup"><span data-stu-id="e8329-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="e8329-220">Kirjoita **Tyyppi**-kenttään **Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="e8329-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="e8329-221">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8329-221">Select **OK**.</span></span>
    11. <span data-ttu-id="e8329-222">Syötä **Kaava**-kenttään **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span><span class="sxs-lookup"><span data-stu-id="e8329-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="e8329-223">Valitse **Tallenna** ja sulje **Kaavan suunnittelutoiminto** -sivu.</span><span class="sxs-lookup"><span data-stu-id="e8329-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="e8329-224">Lisää uusi tietolähde valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8329-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="e8329-225">Merkitse lisätty tietolähde välimuistiin tallennetuksi suorituksen aikana seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e8329-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="e8329-226">Valitse **Tietolähteet**-ruudussa **Box\\Vend**.</span><span class="sxs-lookup"><span data-stu-id="e8329-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="e8329-227">Valitse **Välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="e8329-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e8329-228">**Box\\Vend**-tietolähde tallennetaan välimuistiin **Trans**-tietolähteen kaikille toimittajatapahtumille suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="e8329-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="e8329-229">Päivitä upotettu **Trans\\\#Vend**-tietolähde niin, että se käyttää **Box\\Vend**-tietolähdettä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e8329-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="e8329-230">Laajenna **Tietolähteet**-ruudussa **Trans**.</span><span class="sxs-lookup"><span data-stu-id="e8329-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="e8329-231">Valitse **Trans\\\#Vend**-tietolähde ja valitse sitten **Muokkaa** \> **Muokkaa kaavaa**.</span><span class="sxs-lookup"><span data-stu-id="e8329-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="e8329-232">Syötä **Kaavan suunnittelutoiminto** -sivun **Kaava**-kenttään **Box.Vend(\@.AccountNum)**.</span><span class="sxs-lookup"><span data-stu-id="e8329-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="e8329-233">Valitse **Tallenna** ja sulje **Kaavan suunnittelutoiminto** -sivu.</span><span class="sxs-lookup"><span data-stu-id="e8329-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="e8329-234">Valitse **OK** ja viimeistele valitun tietolähteen muutokset.</span><span class="sxs-lookup"><span data-stu-id="e8329-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="e8329-235">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e8329-235">Select **Save**.</span></span>

    ![Mallin yhdistämismäärityksen suunnitteluohjelman sivun Vend-tietolähde](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="e8329-237">Sulje **Mallimäärityksen sunnittelun** sivu.</span><span class="sxs-lookup"><span data-stu-id="e8329-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="e8329-238">Sulje **Mallimääritykset**-sivu.</span><span class="sxs-lookup"><span data-stu-id="e8329-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="e8329-239">ER-mallin yhdistämismäärityksen muokatun version täydentäminen</span><span class="sxs-lookup"><span data-stu-id="e8329-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="e8329-240">Valitse **Konfiguraatiot**-sivun **Versiot**-pikavälilehdessä version **1.2** **Suorituskyvyn parannuksen yhdistämismääritys** -konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="e8329-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="e8329-241">Valitse **Muuta tilaa** \> **Valmis** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8329-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="e8329-242">Muokatun ER-ratkaisun suorittaminen jäljityksen suorittamista varten</span><span class="sxs-lookup"><span data-stu-id="e8329-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="e8329-243">Luo uusi suoritusjälki [Suorita ER-muoto](#run-format) toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="e8329-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="e8329-244">Suorituskykyjäljityksen käyttäminen mallin yhdistämismäärityksen oikaisujen analysoimisessa</span><span class="sxs-lookup"><span data-stu-id="e8329-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="e8329-245">Valitse **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn parantamisen yhdistämismääritys**.</span><span class="sxs-lookup"><span data-stu-id="e8329-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="e8329-246">Valitse toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="e8329-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="e8329-247">Valitse **Mallin yhdistämismääritykset** -sivun toimintoruudussa **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="e8329-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="e8329-248">Valitse **Mallin määrityssuunnittelija** -sivulla hallintapaneelista **Suorituskyvyn jäljitysmuoto**.</span><span class="sxs-lookup"><span data-stu-id="e8329-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="e8329-249">Valitse uusin jäljitys ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8329-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="e8329-250">Huomaa, että mallimääritykseen tehdyt oikaisut ovat poistaneet tietokannasta päällekkäisiä kyselyitä.</span><span class="sxs-lookup"><span data-stu-id="e8329-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="e8329-251">Tämän mallimäärityksen tietokantataulukoihin ja tietolähteisiin tehtyjen kutsujen määrä on myös vähennetty.</span><span class="sxs-lookup"><span data-stu-id="e8329-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![Mallin yhdistämismäärityksen suunnitteluohjelman sivun 1 jäljitystiedot](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="e8329-253">Suorituksen kokonaisaikaa on vähennetty noin 20 kertaa (noin 8 sekunnista noin 400 millisekuntiin).</span><span class="sxs-lookup"><span data-stu-id="e8329-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="e8329-254">Näin ollen koko sähköisen raportoinnin ratkaisun suorituskykyä on parannettu.</span><span class="sxs-lookup"><span data-stu-id="e8329-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![Mallin yhdistämismäärityksen suunnitteluohjelman sivun 2 jäljitystiedot](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="e8329-256">Liite 1: Microsoftin sähköisen raportoinnin näyteratkaisun komponenttien lataaminen</span><span class="sxs-lookup"><span data-stu-id="e8329-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="e8329-257">Seuraavat tiedostot täytyy ladata ja tallentaa paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="e8329-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="e8329-258">Tiedosto</span><span class="sxs-lookup"><span data-stu-id="e8329-258">File</span></span>                                        | <span data-ttu-id="e8329-259">Sisältö</span><span class="sxs-lookup"><span data-stu-id="e8329-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="e8329-260">Suorituskyvyn parannuksen malli.versio.1</span><span class="sxs-lookup"><span data-stu-id="e8329-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="e8329-261">Esimerkin ER-tietomallin konfigurointi</span><span class="sxs-lookup"><span data-stu-id="e8329-261">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="e8329-262">Suorituskyvyn parannuksen yhdistämismääritys.versio.1.1</span><span class="sxs-lookup"><span data-stu-id="e8329-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="e8329-263">Esimerkin ER-mallikartoituksen konfigurointi</span><span class="sxs-lookup"><span data-stu-id="e8329-263">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="e8329-264">Suorituskyvyn parannuksen muoto.versio.1.1</span><span class="sxs-lookup"><span data-stu-id="e8329-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="e8329-265">Esimerkin ER-format-konfigurointi</span><span class="sxs-lookup"><span data-stu-id="e8329-265">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="e8329-266">Liite 2: Sähköisen raportoinnin kehyksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e8329-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="e8329-267">Ennen kuin alat käyttää sähköisen raportoinnin kehystä Microsoftin sähköisen raportoinnin näyteratkaisun suorituskyvyn parantamiseksi, sinun on määritettävä sähköisen raportoinnin parametrien vähimmäisjoukko.</span><span class="sxs-lookup"><span data-stu-id="e8329-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="e8329-268">Konfiguroi ER-parametrit</span><span class="sxs-lookup"><span data-stu-id="e8329-268">Configure ER parameters</span></span>

1. <span data-ttu-id="e8329-269">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="e8329-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e8329-270">Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit** -osassa **Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="e8329-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="e8329-271">Määritä **Sähköisen raportoinnin parametrit** -sivun **Yleinen**-välilehdessä **Ota käyttöön suunnittelutila** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e8329-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="e8329-272">Määritä **Liitteet**-välilehdessä seuraavat parametrit:</span><span class="sxs-lookup"><span data-stu-id="e8329-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="e8329-273">Valitse **Konfiguraatiot**-kentässä **Tiedosto**-tyyppi **DEMF**-yritykselle.</span><span class="sxs-lookup"><span data-stu-id="e8329-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="e8329-274">Valitse **Työarkisto**-, **Väliaikainen**-, **Perusrivi**- ja **Muut**-kentissä **Tiedosto**-tyyppi.</span><span class="sxs-lookup"><span data-stu-id="e8329-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="e8329-275">Lisätietoja ER-parametreista on kohdassa [Määritä ER-kehys](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e8329-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="e8329-276">Aktivoi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="e8329-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="e8329-277">Jokainen lisätty ER-konfiguraatio merkitään ER-konfiguraation lähteen omistamaksi.</span><span class="sxs-lookup"><span data-stu-id="e8329-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="e8329-278">ER-konfiguraation lähdettä, joka on aktivoitu **Sähköinen raportointi** -työtilassa, käytetään tähän tarkoitukseen.</span><span class="sxs-lookup"><span data-stu-id="e8329-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="e8329-279">Siksi sinun on aktivoitava ER-konfiguraation lähde **Sähköinen raportointi** -työtilassa, ennen kuin voit alkaa lisätä tai muokata ER-konfiguraatioita.</span><span class="sxs-lookup"><span data-stu-id="e8329-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="e8329-280">Vain sähköisen raportoinnin konfiguraation omistaja voi muokata konfiguraatiota.</span><span class="sxs-lookup"><span data-stu-id="e8329-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="e8329-281">Siksi ennen kuin ER-konfiguraatiota voi muokata, asianmukainen ER-konfiguraation lähde on aktivoitava **Sähköinen raportointi** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="e8329-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="e8329-282">Tarkista ER-konfiguraation lähteiden luettelo</span><span class="sxs-lookup"><span data-stu-id="e8329-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="e8329-283">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="e8329-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e8329-284">Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit**-osassa **Konfiguraation lähteet**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="e8329-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="e8329-285">**Konfiguraation lähdetaulu** -sivulla jokaisen lähteen tietueella on yksilöllinen nimi ja URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="e8329-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="e8329-286">Tarkista tämän sivun sisältö.</span><span class="sxs-lookup"><span data-stu-id="e8329-286">Review the contents of this page.</span></span> <span data-ttu-id="e8329-287">Jos **Litware, Inc.** -tietue on jo olemassa, ohita seuraava menettely: [Uuden sähköisen raportoinnin konfiguraation toimittajan lisääminen](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="e8329-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="e8329-288">Lisää uusi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="e8329-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="e8329-289">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="e8329-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e8329-290">Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit**-osassa **Konfiguraation lähteet**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="e8329-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="e8329-291">Valitse **Konfiguraation lähteet**-sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e8329-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="e8329-292">Kirjoita **Nimi**-kenttään **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="e8329-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="e8329-293">Kirjoita **Internetosoite**-kenttään `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="e8329-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="e8329-294">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e8329-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="e8329-295">Aktivoi ER-konfiguraation lähde</span><span class="sxs-lookup"><span data-stu-id="e8329-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="e8329-296">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="e8329-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e8329-297">Valitse **Lokalisoinnin konfiguraatiot**-sivun **Konfiguraation lähteet**-osassa **Litware, Inc.** -ruutu ja valitse sitten **Aseta aktiiviseksi**.</span><span class="sxs-lookup"><span data-stu-id="e8329-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="e8329-298">Lisätietoja ER-konfiguraation lähteistä on kohdassa [Konfiguraation lähteiden luonti ja merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e8329-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8329-299">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e8329-299">Additional resources</span></span>

- [<span data-ttu-id="e8329-300">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e8329-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="e8329-301">Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi</span><span class="sxs-lookup"><span data-stu-id="e8329-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="e8329-302">Laskettu kenttä -tyyppisten ER-tietolähteiden parametrisoitujen kutsujen tuki</span><span class="sxs-lookup"><span data-stu-id="e8329-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)
