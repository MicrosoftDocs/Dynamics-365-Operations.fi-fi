---
title: ER-muodon parametrien määrittäminen yrityskohtaisesti
description: Tässä ohjeaiheessa käsitellään sähköisen raportoinnin (ER) muodon parametrien yrityskohtaista määrittämistä.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: b51a7ae8587a3cbb65efc4af574929efcbc8fbf8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681469"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="6c7db-103">ER-muodon parametrien määrittäminen yrityskohtaisesti</span><span class="sxs-lookup"><span data-stu-id="6c7db-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="6c7db-104">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="6c7db-104">Prerequisites</span></span>

<span data-ttu-id="6c7db-105">Näiden vaiheiden suorittaminen edellyttää, että ensin on suoritettu vaiheet kohdassa [ER-muotojen määrittäminen käyttämään yrityskohtaisesti määritettyjä parametreja](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="6c7db-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="6c7db-106">Tässä ohjeaiheessa olevien esimerkkien suorittaminen edellyttää jonkin seuraavan roolin Microsoft Dynamics 365 Finance (Finance) -käyttöoikeutta:</span><span class="sxs-lookup"><span data-stu-id="6c7db-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="6c7db-107">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="6c7db-107">Electronic reporting developer</span></span>
- <span data-ttu-id="6c7db-108">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="6c7db-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="6c7db-109">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="6c7db-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="6c7db-110">ER-konfiguraatioiden tuominen</span><span class="sxs-lookup"><span data-stu-id="6c7db-110">Import ER configurations</span></span>

1.  <span data-ttu-id="6c7db-111">Kirjaudu ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="6c7db-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="6c7db-112">Valitse oletuskoontinäytössä **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="6c7db-113">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="6c7db-114">Tuo Financen nykyiseen esiintymään määritykset, jotka vietiin RCS:stä (Regulatory Configuration Services) ohjeaiheen [ER-muotojen määrittäminen käyttämään yrityskohtaisesti määritettyjä parametreja](er-app-specific-parameters-configure-format.md) vaiheiden suorittamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="6c7db-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="6c7db-115">Toimi seuraavien ohjeiden mukaisesti kussakin sähköisen raportoinnin (ER) määrityksessä ja suorita ohjeet seuraavassa järjestyksessä: tietomalli, mallimääritys ja muodot.</span><span class="sxs-lookup"><span data-stu-id="6c7db-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="6c7db-116">Valitse **Exchange \> Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="6c7db-117">Valitse tarvittava XML-muotoinen ER-määritystiedosto valitsemalla **Selaa**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="6c7db-118">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-118">Select **OK**.</span></span>
    
    <span data-ttu-id="6c7db-119">Seuraavassa kuvassa näkyy määritykset, jotka on oltava tehtyinä, kun olet valmis.</span><span class="sxs-lookup"><span data-stu-id="6c7db-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![Sähköisen raportoinnin konfiguroinnit -sivu](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="6c7db-121">DEMF-yrityksen parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6c7db-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="6c7db-122">Voit määrittää ER-muodon sovelluskohtaiset parametrit ER-kehyksen avulla.</span><span class="sxs-lookup"><span data-stu-id="6c7db-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="6c7db-123">Valitse **DEMF**-yritys.</span><span class="sxs-lookup"><span data-stu-id="6c7db-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="6c7db-124">Valitse määrityspuussa muoto **LE-tietojen haun oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="6c7db-125">Valitse toimintoruudussa **Konfiguroinnit**-välilehden **Sovelluskohtaiset parametrit**-ryhmässä **Määritys**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![ER-sovelluskohtaiset parametrit -sivu](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="6c7db-127">Voit määrittää **Sovelluskohtaiset parametrit** -sivulla **LE-tietojen haun oppimismuoto** -muodon **Valitsin**-tietolähteen.</span><span class="sxs-lookup"><span data-stu-id="6c7db-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="6c7db-128">Jos ER-perusmuodossa on useita **Haku**-tyyppisiä tietolähteitä, tietolähde on valittava **Haut**-pikavälilehdessä, ennen kuin tietolähteen sääntöjoukon määrittämisen voi aloittaa.</span><span class="sxs-lookup"><span data-stu-id="6c7db-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="6c7db-129">Kullekin tietolähteelle voi määrittää erilliset säännöt jokaiselle valitun ER-muodon versiolle.</span><span class="sxs-lookup"><span data-stu-id="6c7db-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="6c7db-130">Valitun ER-perusmuodon versiossa käytettävissä oleva haun kaikkien tietolähteiden koko sääntöjoukko muodostaa ER-muodon sovelluskohtaiset parametrit.</span><span class="sxs-lookup"><span data-stu-id="6c7db-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="6c7db-131">Valitse ER-muodon versio **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="6c7db-132">Valitse **Ehdot**-pikavälilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="6c7db-133">Avaa haku valitsemalla uuden tietueen **Koodi**-kentässä avattavan valikon nuoli.</span><span class="sxs-lookup"><span data-stu-id="6c7db-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="6c7db-134">Haku tuloksena on verotuskoodien luettelo valintaa varten.</span><span class="sxs-lookup"><span data-stu-id="6c7db-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="6c7db-135">ER-perusmuodossa määritetty **Model.Data.Tax**-tietolähde palauttaa tämän luettelon.</span><span class="sxs-lookup"><span data-stu-id="6c7db-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="6c7db-136">Koska tässä tietolähteessä on **Nimi**-kenttä, kunkin verokoodin nimi näkyy haussa.</span><span class="sxs-lookup"><span data-stu-id="6c7db-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![ER-sovelluskohtaiset parametrit -sivu](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="6c7db-138">Valitse **VAT19**-verokoodi.</span><span class="sxs-lookup"><span data-stu-id="6c7db-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="6c7db-139">Avaa haku valitsemalla uuden tietueen **Haun tulos** -kentässä avattavan valikon nuoli.</span><span class="sxs-lookup"><span data-stu-id="6c7db-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="6c7db-140">Haun tuloksena on TaxationLevel-muodon luetteloinnin arvoluettelo valintaa varten.</span><span class="sxs-lookup"><span data-stu-id="6c7db-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="6c7db-141">Huomaa, että jos sen käyttäjän ensisijaiseksi kieleksi on valittu suomi, jona olet kirjautunut sisään, haun arvojen otsikot ovat suomeksi, mikäli ne on käännetty ER-perusmuodossa.</span><span class="sxs-lookup"><span data-stu-id="6c7db-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="6c7db-142">Jos lisäksi haun tietolähteen otsikko on käännetty, kyseinen otsikko näkyy käyttäjän ensisijaisella kielellä **Haku**-valintalehdessä.</span><span class="sxs-lookup"><span data-stu-id="6c7db-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![ER-sovelluskohtaiset parametrit -sivu](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="6c7db-144">Valitse **Normaali verotus** -arvo.</span><span class="sxs-lookup"><span data-stu-id="6c7db-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="6c7db-145">Tämän tietueen lisääminen määrittää seuraavan säännön: aina kun **Valitsin**-haun tietolähdettä pyydetään ja **VAT19**-verokoodi välitetään argumenttina, **Normaali verotus** palautetaan pyydettynä verotustasona.</span><span class="sxs-lookup"><span data-stu-id="6c7db-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="6c7db-146">Valitse **Lisää** ja toimi sitten seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6c7db-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="6c7db-147">Valitse **Koodi**-kentässä **InVAT19**-verokoodi.</span><span class="sxs-lookup"><span data-stu-id="6c7db-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="6c7db-148">Valitse **Haun tulos** -kentässä **Normaali verotus** -arvo.</span><span class="sxs-lookup"><span data-stu-id="6c7db-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="6c7db-149">Valitse uudelleen **Lisää** ja toimi sitten seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6c7db-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="6c7db-150">Valitse **Koodi**-kentässä **VAT7**-verokoodi.</span><span class="sxs-lookup"><span data-stu-id="6c7db-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="6c7db-151">Valitse **Haun tulos** -kentässä **Alennettu verotus** -arvo.</span><span class="sxs-lookup"><span data-stu-id="6c7db-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="6c7db-152">Valitse uudelleen **Lisää** ja toimi sitten seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6c7db-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="6c7db-153">Valitse **Koodi**-kentässä **InVAT7**-verokoodi.</span><span class="sxs-lookup"><span data-stu-id="6c7db-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="6c7db-154">Valitse **Haun tulos** -kentässä **Alennettu verotus** -arvo.</span><span class="sxs-lookup"><span data-stu-id="6c7db-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="6c7db-155">Valitse uudelleen **Lisää** ja toimi sitten seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6c7db-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="6c7db-156">Valitse **Koodi**-kentässä **THIRD**-verokoodi.</span><span class="sxs-lookup"><span data-stu-id="6c7db-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="6c7db-157">Valitse **Haun tulos** -kentässä **Ei verotusta** -arvo.</span><span class="sxs-lookup"><span data-stu-id="6c7db-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="6c7db-158">Valitse uudelleen **Lisää** ja toimi sitten seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6c7db-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="6c7db-159">Valitse **Koodi**-kentässä **InVAT0**-verokoodi.</span><span class="sxs-lookup"><span data-stu-id="6c7db-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="6c7db-160">Valitse **Haun tulos** -kentässä **Ei verotusta** -arvo.</span><span class="sxs-lookup"><span data-stu-id="6c7db-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="6c7db-161">Valitse uudelleen **Lisää** ja toimi sitten seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6c7db-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="6c7db-162">Valitse **Koodi**-kentässä **\*Ei tyhjä\*** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="6c7db-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="6c7db-163">Valitse **Haun tulos** -kentässä **Muu**-arvo.</span><span class="sxs-lookup"><span data-stu-id="6c7db-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="6c7db-164">Tämän viimeisen tietueen lisääminen määrittää seuraavan säännön: aina kun argumenttina välitetty verokoodi ei vastaa mitään edellisistä säännöistä, haun tietolähde palauttaa **Muu**-arvon pyydettynä verotustasona.</span><span class="sxs-lookup"><span data-stu-id="6c7db-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![ER-sovelluskohtaiset parametrit -sivu](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="6c7db-166">Valitse **Tila**-kentässä **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="6c7db-167">Kun suoritat ER-muodon version, jonka tilana on joko **Valmis** tai **Jaettu**, tämän sääntöjoukon tilan on oltava **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="6c7db-168">Muussa tapauksessa ER-perusmuodon suoritus keskeytyy, kun muoto yrittää ladata tietoja tästä sääntöjoukosta, kun **Valitsin**-haun tietolähdettä suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="6c7db-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="6c7db-169">Kun suoritan ER-muodon version, jonka tila on **Luonnos**, ER-perusmuoto voi käyttää tätä sääntöjoukkoa riippumatta siitä, mikä sen tila on.</span><span class="sxs-lookup"><span data-stu-id="6c7db-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="6c7db-170">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-170">Select **Save**.</span></span>
18. <span data-ttu-id="6c7db-171">Sulje **Sovelluskohtaiset parametrit** -sivu.</span><span class="sxs-lookup"><span data-stu-id="6c7db-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="6c7db-172">ER-muodon suorittaminen DEMF-yrityksessä</span><span class="sxs-lookup"><span data-stu-id="6c7db-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="6c7db-173">Valitse määrityspuussa muoto **LE-tietojen haun oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="6c7db-174">Valitse toimintoruudussa **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="6c7db-175">Valitse avautuvassa valintaikkunassa **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="6c7db-176">Lataa muodostuva raportti ja tallenna se paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="6c7db-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="6c7db-177">Huomaa, että muodostetussa raportissa **InVAT7**-verokoodin yhteenveto on **Alennettu**-tasolla sekä **VAT19**- ja **InVA19**-verokoodien yhteenvedot **Normaali**-tasolla.</span><span class="sxs-lookup"><span data-stu-id="6c7db-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="6c7db-178">Yrityskohtaisen sääntöjoukon määritys määrittää tämän toiminnan.</span><span class="sxs-lookup"><span data-stu-id="6c7db-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="6c7db-179">Valitse **Vero \> Välilliset verot \> Arvonlisävero \> Arvonlisäverokoodit**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="6c7db-180">Valitse **InVAT7**-verokoodi.</span><span class="sxs-lookup"><span data-stu-id="6c7db-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="6c7db-181">Valitse toimintoruudun **Arvonlisäverokoodi**-välilehden **Kyselyt**-ryhmässä **Kirjattu arvonlisävero**. Voit sitten tarkastella tietoja veroarvosta ja käytetystä verokoodikohtaisesta veroprosentista.</span><span class="sxs-lookup"><span data-stu-id="6c7db-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![Kirjattu arvonlisävero -sivu](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="6c7db-183">Sulje Kirjattu arvonlisävero -sivu.</span><span class="sxs-lookup"><span data-stu-id="6c7db-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="6c7db-184">USMF-yrityksen parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6c7db-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="6c7db-185">Valitse **USMF**-yritys.</span><span class="sxs-lookup"><span data-stu-id="6c7db-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="6c7db-186">Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="6c7db-187">Laajenna määrityspuussa **Model to learn parameterized calls**, laajenna **Parametrisoitujen kutsujen oppimismuoto** ja valitse **LE-tietojen haun oppimismuoto** -muoto.</span><span class="sxs-lookup"><span data-stu-id="6c7db-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="6c7db-188">Valitse toimintoruudussa **Konfiguroinnit**-välilehden **Sovelluskohtaiset parametrit**-ryhmässä **Määritys**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="6c7db-189">Valitse valitun ER-muodon versio **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="6c7db-190">Valitse **Ehdot**-pikavälilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="6c7db-191">Avaa haku valitsemalla uuden tietueen **Koodi**-kentässä avattavan valikon nuoli.</span><span class="sxs-lookup"><span data-stu-id="6c7db-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="6c7db-192">Haun tuloksena on nyt **USMF**-yritysveron verokoodiluettelo, josta valinta tehdään.</span><span class="sxs-lookup"><span data-stu-id="6c7db-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![ER-sovelluskohtaiset parametrit -sivu](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="6c7db-194">Valitse **EXEMPT**-verokoodi.</span><span class="sxs-lookup"><span data-stu-id="6c7db-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="6c7db-195">Valitse uuden tietuen **Haun tulos** -kentässä **Ei verotusta** -arvo.</span><span class="sxs-lookup"><span data-stu-id="6c7db-195">In the **Lookup resul** t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="6c7db-196">Valitse **Lisää** uudelleen.</span><span class="sxs-lookup"><span data-stu-id="6c7db-196">Select **Add** again.</span></span>
11. <span data-ttu-id="6c7db-197">Valitse uuden tietueen **Koodi**-kentässä **\*Ei tyhjä\*** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="6c7db-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="6c7db-198">Valitse uuden tietuen **Haun tulos** -kentässä **Normaali verotus** -arvo.</span><span class="sxs-lookup"><span data-stu-id="6c7db-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="6c7db-199">Valitse **Tila**-kentässä **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="6c7db-200">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-200">Select **Save**.</span></span>

    ![ER-sovelluskohtaiset parametrit -sivu](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="6c7db-202">Sulje **Sovelluskohtaiset parametrit** -sivu.</span><span class="sxs-lookup"><span data-stu-id="6c7db-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="6c7db-203">ER-muodon suorittaminen USMF-yrityksessä</span><span class="sxs-lookup"><span data-stu-id="6c7db-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="6c7db-204">Valitse määrityspuussa muoto **LE-tietojen haun oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="6c7db-205">Valitse toimintoruudussa **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="6c7db-206">Valitse avautuvassa valintaikkunassa **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="6c7db-207">Lataa muodostuva raportti ja tallenna se paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="6c7db-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="6c7db-208">Huomaa, että muodostetussa raportissa on nyt käytetty uudelleen samaa ER-muotoa eri yrityksessä ilman, että ER-muotoa olisi säädetty.</span><span class="sxs-lookup"><span data-stu-id="6c7db-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="6c7db-209">Yrityskohtaisten parametrien käyttäminen uudelleen</span><span class="sxs-lookup"><span data-stu-id="6c7db-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="6c7db-210">Vientiparametrit</span><span class="sxs-lookup"><span data-stu-id="6c7db-210">Export parameters</span></span>

1.  <span data-ttu-id="6c7db-211">Siirry kohtaan **Organisaation hallinto \> Työtilat \> Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="6c7db-212">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="6c7db-213">Valitse määrityspuussa muoto **LE-tietojen haun oppimismuoto**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="6c7db-214">Valitse toimintoruudussa **Konfiguroinnit**-välilehden **Sovelluskohtaiset parametrit**-ryhmässä **Määritys**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="6c7db-215">Valitse ER-muodon versio **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="6c7db-216">Valitse toimintoruudussa **Vie**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="6c7db-217">Lataa muodostuva tiedosto ja tallenna se paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="6c7db-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="6c7db-218">Määritetty sovelluskohtaisten parametrien joukko on nyt viety XML-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="6c7db-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="6c7db-219">Tuontiparametrit</span><span class="sxs-lookup"><span data-stu-id="6c7db-219">Import parameters</span></span>

1.  <span data-ttu-id="6c7db-220">Valitse ER-muodon versio **1.1.2**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="6c7db-221">Valitse toimintoruudussa **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="6c7db-222">Vahvista valitsemalla **Kyllä**, että muodon tämän version aiemmin luodut sovelluskohtaiset parametrit korvataan.</span><span class="sxs-lookup"><span data-stu-id="6c7db-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="6c7db-223">Etsi versioon **1.1.1** viedyt sovelluskohtaiset parametrit sisältävä tiedosto valitsemalla **Selaa**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="6c7db-224">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-224">Select **OK**.</span></span>

    <span data-ttu-id="6c7db-225">ER-muodon versiossa **1.1.2** on nyt ne sovelluskohtaiset parametrit, jotka määritettiin alun perin versioon **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="6c7db-226">Huomaa, että ER-muodon sovelluskohtaiset parametrit ovat yrityskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="6c7db-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="6c7db-227">Yhdelle yritykselle määritettyjen sovelluskohtaisten parametrien käyttäminen uudelleen toisessa yrityksessä edellyttää, että ne viedään, kun olet kirjautuneena ensimmäiseen yritykseen ja tuodaan sitten, kun olet kirjautunut toiseen yritykseen.</span><span class="sxs-lookup"><span data-stu-id="6c7db-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="6c7db-228">Voit siirtää tällä tavoin myös yhteen Financen esiintymään määritettyjä ER-muotoon liittyviä sovelluskohtaisia parametreja toiseen Financen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="6c7db-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="6c7db-229">Ota huomioon, että jos määrität yhden ER-muodon version sovelluskohtaiset parametrit ja tuot saman muodon korkeamman version nykyiseen Financen esiintymään, aiemmin luotuja sovelluskohtaisia parametreja ei käytetä tuodussa versiossa.</span><span class="sxs-lookup"><span data-stu-id="6c7db-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="6c7db-230">Ota myös huomioon, että kun valitset tuotavan tiedoston, kyseisen tiedoston sovelluskohtaisten parametrien rakennetta verrataan vastaavan tuotavaksi valitun ER-muodon **Haku**-tyypin tietolähteen rakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="6c7db-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="6c7db-231">Tuonti tehdään, kun kunkin sovelluskohtaisen parametrin rakenne vastaa vastaavan tietolähteen rakennetta tuotavaksi valitussa ER-muodossa.</span><span class="sxs-lookup"><span data-stu-id="6c7db-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="6c7db-232">Jos rakenteet eivät vastaa toisiaan, saat varoitussanoman, joka ilmaisee, että tuontia ei voi tehdä.</span><span class="sxs-lookup"><span data-stu-id="6c7db-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="6c7db-233">Jos pakotat tuonnin, valitun ER-muodon aiemmin luodut sovelluskohtaiset parametrit tyhjennetään ja ne on määritettävä alusta alkaen.</span><span class="sxs-lookup"><span data-stu-id="6c7db-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="6c7db-234">Sovelluskohtaisten parametrien ja ER-muodon välinen suhde</span><span class="sxs-lookup"><span data-stu-id="6c7db-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="6c7db-235">ER-muodon ja sen sovelluskohtaisten parametrien välinen suhde muodostetaan ER-muodon yksilöivällä esiintymästä riippumattomalla tunnuskoodilla.</span><span class="sxs-lookup"><span data-stu-id="6c7db-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="6c7db-236">Niinpä kun poistat ER-muodon Financesta, ER-muotoon määritetyt sovelluskohtaiset parametrit jäävät Financen nykyiseen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="6c7db-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="6c7db-237">Niitä voidaan käyttää, kun ER-perusmuoto tuodaan uudelleen Financen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="6c7db-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="6c7db-238">Sovelluskohtaisten parametrien käyttäminen ER-kehystä käyttämällä</span><span class="sxs-lookup"><span data-stu-id="6c7db-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="6c7db-239">Edellisessä esimerkissä olet käyttänyt ER-muodon sovelluskohtaisia parametreja ER-kehyksen avulla.</span><span class="sxs-lookup"><span data-stu-id="6c7db-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="6c7db-240">Tällä tavoin et kuitenkaan voi rajoittaa tietyn ER-muodon sovelluskohtaisten parametrien käyttöä.</span><span class="sxs-lookup"><span data-stu-id="6c7db-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="6c7db-241">Jos kyseisiä rajoituksia on käytettävä, toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6c7db-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="6c7db-242">Käytä joko aiemmin luotua **ERSolutionAppSpecificParametersDesigner**-valikkovaihtoehtoa uudelleen tai käytä omaa **ERSolutionAppSpecificParametersDesigner**-valikkovaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="6c7db-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![Visual Studio -sivu](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="6c7db-244">Noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="6c7db-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="6c7db-245">Luo uusi valikkovaihtoehdon painike ja linkitä se vastaavaan **ERSolutionTable**-taulukon tietueeseen määrittämällä sen **Tietolähde**-ominaisuudeksi **ERSolutionTable**.</span><span class="sxs-lookup"><span data-stu-id="6c7db-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![Visual Studio -sivu](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="6c7db-247">Luo yksinkertainen painike ja korvaa **Napsautus**-menetelmä seuraavassa esimerkissä kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="6c7db-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="6c7db-248">Tällä tavoin voit määrittää yksilöivän ratkaisutunnuksen (määritetty **GUID**-arvon avulla) sallimaan vain tietyn ER-muodon ja siitä johdettavien kopioiden sovelluskohtaisten parametrien käyttämisen.</span><span class="sxs-lookup"><span data-stu-id="6c7db-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="6c7db-249">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6c7db-249">Additional resources</span></span>

[<span data-ttu-id="6c7db-250">Sähköisen raportoinnin kaavojen suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="6c7db-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="6c7db-251">ER-muotojen määrittäminen käyttämään yrityskohtaisesti määritettyjä parametreja</span><span class="sxs-lookup"><span data-stu-id="6c7db-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)
