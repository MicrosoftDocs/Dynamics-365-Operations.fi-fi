---
title: Alkuperämaa
description: Monet organisaatiot myöntänyt toimittajille todistuksia varmistamaan, että tuotteet vastaavat tiettyjä sertifiointistandardeja. Nämä todistukset määräytyvät usein alkuperämaasta. Tässä ohjeaiheessa käsitellään alkuperämaatoimintoa, jonka avulla tuotteen voi linkittää alkuperämaahan ja seurata tuotteen sertifiointeja.
author: dasani-madipalli
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: b07747752dd09f39c3a7a9a647cc3d10cc4b5cc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829543"
---
# <a name="country-of-origin"></a><span data-ttu-id="50837-105">Alkuperämaa</span><span class="sxs-lookup"><span data-stu-id="50837-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50837-106">Monet organisaatiot myöntänyt toimittajille todistuksia varmistamaan, että tuotteet vastaavat tiettyjä sertifiointistandardeja.</span><span class="sxs-lookup"><span data-stu-id="50837-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="50837-107">Nämä todistukset määräytyvät usein alkuperämaasta.</span><span class="sxs-lookup"><span data-stu-id="50837-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="50837-108">Alkuperämaatoiminnon avulla tuotteen voi linkittää alkuperämaahan ja seurata tuotteen sertifiointeja.</span><span class="sxs-lookup"><span data-stu-id="50837-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="50837-109">Alkuperämaa-ominaisuuden ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="50837-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="50837-110">Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="50837-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="50837-111">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="50837-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="50837-112">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="50837-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="50837-113">**Moduuli:** *Tuotetietojen hallinta*</span><span class="sxs-lookup"><span data-stu-id="50837-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="50837-114">**Ominaisuuden nimi:** *Alkuperämaan hallinta -ominaisuus*</span><span class="sxs-lookup"><span data-stu-id="50837-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="50837-115">Lähde- ja kohdemaiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="50837-115">Configure source and destination countries</span></span>

<span data-ttu-id="50837-116">Ennen kuin tuotteelle myönnetään todistus, tuote on linkitettävä kohdemaahan ja sen alkuperämaahan.</span><span class="sxs-lookup"><span data-stu-id="50837-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="50837-117">Valitse **Tuotetietojen hallinta \> Asetukset \> Tuotteen yhteensopivuus \> Alkuperämaa \> Alkuperämaasäännöt**.</span><span class="sxs-lookup"><span data-stu-id="50837-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="50837-118">Valitse aiemmin luodun maan asetukset muokattavaksi tai luo uudet maa-asetukset valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="50837-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="50837-119">Määritä seuraavat valitun tai uuden maan arvot:</span><span class="sxs-lookup"><span data-stu-id="50837-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="50837-120">Kenttä</span><span class="sxs-lookup"><span data-stu-id="50837-120">Field</span></span> | <span data-ttu-id="50837-121">kuvaus</span><span class="sxs-lookup"><span data-stu-id="50837-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="50837-122">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="50837-122">Item number</span></span> | <span data-ttu-id="50837-123">Valitse tuotteen nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="50837-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="50837-124">Kohdemaa</span><span class="sxs-lookup"><span data-stu-id="50837-124">Destination country</span></span> | <span data-ttu-id="50837-125">Valitse maa, johon tuote lähetetään.</span><span class="sxs-lookup"><span data-stu-id="50837-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="50837-126">Alkuperämaa</span><span class="sxs-lookup"><span data-stu-id="50837-126">Origin country</span></span> | <span data-ttu-id="50837-127">Valitse maa, josta tuote lähetetään.</span><span class="sxs-lookup"><span data-stu-id="50837-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="50837-128">Tämän asetuksen tarkoitus on auttaa luomaan tuoterakenneraportti, jossa alkuperämaa voidaan sisällyttää kuhunkin osaan, johon lähde- ja kohdemaa on määritetty.</span><span class="sxs-lookup"><span data-stu-id="50837-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="50837-129">Tämän raportin avulla saadaan kokonaisvaltainen käsityksen siitä, mistä osat tulevat ja mihin ne ovat menossa.</span><span class="sxs-lookup"><span data-stu-id="50837-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="50837-130">Toimittajien varmenteiden seuraaminen</span><span class="sxs-lookup"><span data-stu-id="50837-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="50837-131">Voit seurata toimittajille myönnettyjä varmenteita **Toimittajien alkuperämaavarmenteet** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="50837-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="50837-132">Sinun on päätettävä, mitä varmenneasiakirjoja myönnetään ja miten ne raportoidaan asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="50837-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="50837-133">Tämä toimintoa auttaa seuraamaan varmenteita.</span><span class="sxs-lookup"><span data-stu-id="50837-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="50837-134">Sen avulla voi myös valita, näkyvätkö varmennenumerot laskuissa, pakkausluetteloissa ja/tai tilausvahvistuksissa.</span><span class="sxs-lookup"><span data-stu-id="50837-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="50837-135">Voit määrittää varmenteen tiedot seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="50837-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="50837-136">Valitse **Tuotetietojen hallinta \> Asetukset \> Tuotteen yhteensopivuus \> Alkuperämaa \> Toimittajan alkuperämaavarmenteet**.</span><span class="sxs-lookup"><span data-stu-id="50837-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="50837-137">Valitse aiemmin luodun varmenteen asetukset muokattavaksi tai luo uudet varmenneasetukset valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="50837-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="50837-138">Määritä seuraavat valitun tai uuden varmenteen asetukset:</span><span class="sxs-lookup"><span data-stu-id="50837-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="50837-139">Kenttä</span><span class="sxs-lookup"><span data-stu-id="50837-139">Field</span></span> | <span data-ttu-id="50837-140">kuvaus</span><span class="sxs-lookup"><span data-stu-id="50837-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="50837-141">Toimittajatili</span><span class="sxs-lookup"><span data-stu-id="50837-141">Vendor account</span></span> | <span data-ttu-id="50837-142">Valitse toimittaja, jolle varmenne myönnetään.</span><span class="sxs-lookup"><span data-stu-id="50837-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="50837-143">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="50837-143">Item number</span></span> | <span data-ttu-id="50837-144">Valitse nimike, jolle varmenne myönnetään.</span><span class="sxs-lookup"><span data-stu-id="50837-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="50837-145">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="50837-145">Country/region</span></span> | <span data-ttu-id="50837-146">Kohdemaa tai -alue, jossa tätä varmennetta on käytettävä.</span><span class="sxs-lookup"><span data-stu-id="50837-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="50837-147">Varmenteen numero</span><span class="sxs-lookup"><span data-stu-id="50837-147">Certificate number</span></span> | <span data-ttu-id="50837-148">Anna myönnetyn varmenteen tunnusnumero.</span><span class="sxs-lookup"><span data-stu-id="50837-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="50837-149">Voimassa</span><span class="sxs-lookup"><span data-stu-id="50837-149">Effective</span></span> | <span data-ttu-id="50837-150">Valitse ensimmäinen päivämäärä, jolloin nykyinen varmenne on voimassa.</span><span class="sxs-lookup"><span data-stu-id="50837-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="50837-151">Vanhentumisaika</span><span class="sxs-lookup"><span data-stu-id="50837-151">Expiration</span></span> | <span data-ttu-id="50837-152">Valitse viimeinen päivämäärä, jolloin nykyinen varmenne on voimassa.</span><span class="sxs-lookup"><span data-stu-id="50837-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="50837-153">Tulosta laskulle</span><span class="sxs-lookup"><span data-stu-id="50837-153">Print on invoice</span></span> | <span data-ttu-id="50837-154">Valitse tämä valintaruutu, kun varmennenumero tulostetaan laskuihin, joiden osoitteena on määritetty maa määritetyllä päivämääräalueella.</span><span class="sxs-lookup"><span data-stu-id="50837-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="50837-155">Tulosta pakkausluettelossa</span><span class="sxs-lookup"><span data-stu-id="50837-155">Print on packing slip</span></span> | <span data-ttu-id="50837-156">Valitse tämä valintaruutu, kun varmennenumero tulostetaan pakkausluetteloihin, joiden osoitteena on määritetty maa määritetyllä päivämääräalueella.</span><span class="sxs-lookup"><span data-stu-id="50837-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="50837-157">Tulosta myyntitilauksessa</span><span class="sxs-lookup"><span data-stu-id="50837-157">Print on sales order</span></span> | <span data-ttu-id="50837-158">Valitse tämä valintaruutu, kun varmennenumero tulostetaan myyntitilauksiin, joiden osoitteena on määritetty maa määritetyllä päivämääräalueella.</span><span class="sxs-lookup"><span data-stu-id="50837-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="50837-159">Sisällytä alkuperämaa tuoterakenneraportteihin</span><span class="sxs-lookup"><span data-stu-id="50837-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="50837-160">Kun luot tuoterakenneraportin, voit sisällyttää kunkin sellaisen osan alkuperämaan, jonka lähde- ja kohdemaa on määritetty **Alkuperämaasäännöt**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="50837-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="50837-161">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="50837-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="50837-162">Avaa tuotteen **Vapautetun tuotteen tiedot** -sivu valitsemalla tai luomalla tuote.</span><span class="sxs-lookup"><span data-stu-id="50837-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="50837-163">Valitse toimintoruudun **Suunnittele**-välilehden **Tuoterakenne**-ryhmässä **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="50837-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="50837-164">Valitse avautuvan sivun toimintoruudussa **Tuoterakenne \> Tulosta**.</span><span class="sxs-lookup"><span data-stu-id="50837-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="50837-165">Määritä **Tuoterakennerivit**-valintaikkunassa **Kohdemaa**-kentässä kohdemaa, jota haluat tarkastella raportissa.</span><span class="sxs-lookup"><span data-stu-id="50837-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="50837-166">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="50837-166">Select **OK**.</span></span>

<span data-ttu-id="50837-167">Kunkin osan alkuperämaasta tietoja sisältävä raportti luodaan ja näytetään.</span><span class="sxs-lookup"><span data-stu-id="50837-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="50837-168">Esimerkki raportista.</span><span class="sxs-lookup"><span data-stu-id="50837-168">Here is an example of the report.</span></span>

<span data-ttu-id="50837-169">![Alkuperämaaraportti](media/country-of-origin-report.png "Alkuperämaaraportti")</span><span class="sxs-lookup"><span data-stu-id="50837-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]