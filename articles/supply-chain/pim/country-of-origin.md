---
title: Alkuperämaa
description: Monet organisaatiot myöntänyt toimittajille todistuksia varmistamaan, että tuotteet vastaavat tiettyjä sertifiointistandardeja. Nämä todistukset määräytyvät usein alkuperämaasta. Tässä ohjeaiheessa käsitellään alkuperämaatoimintoa, jonka avulla tuotteen voi linkittää alkuperämaahan ja seurata tuotteen sertifiointeja.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596226"
---
# <a name="country-of-origin"></a><span data-ttu-id="ecd05-105">Alkuperämaa</span><span class="sxs-lookup"><span data-stu-id="ecd05-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecd05-106">Monet organisaatiot myöntänyt toimittajille todistuksia varmistamaan, että tuotteet vastaavat tiettyjä sertifiointistandardeja.</span><span class="sxs-lookup"><span data-stu-id="ecd05-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="ecd05-107">Nämä todistukset määräytyvät usein alkuperämaasta.</span><span class="sxs-lookup"><span data-stu-id="ecd05-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="ecd05-108">Alkuperämaatoiminnon avulla tuotteen voi linkittää alkuperämaahan ja seurata tuotteen sertifiointeja.</span><span class="sxs-lookup"><span data-stu-id="ecd05-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="ecd05-109">Lähde- ja kohdemaiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ecd05-109">Configure source and destination countries</span></span>

<span data-ttu-id="ecd05-110">Ennen kuin tuotteelle myönnetään todistus, tuote on linkitettävä kohdemaahan ja sen alkuperämaahan.</span><span class="sxs-lookup"><span data-stu-id="ecd05-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="ecd05-111">Valitse **Tuotetietojen hallinta \> Asetukset \> Tuotteen yhteensopivuus \> Alkuperämaa \> Alkuperämaasäännöt**.</span><span class="sxs-lookup"><span data-stu-id="ecd05-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="ecd05-112">Valitse aiemmin luodun maan asetukset muokattavaksi tai luo uudet maa-asetukset valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ecd05-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="ecd05-113">Määritä seuraavat valitun tai uuden maan arvot:</span><span class="sxs-lookup"><span data-stu-id="ecd05-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="ecd05-114">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ecd05-114">Field</span></span> | <span data-ttu-id="ecd05-115">kuvaus</span><span class="sxs-lookup"><span data-stu-id="ecd05-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="ecd05-116">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="ecd05-116">Item number</span></span> | <span data-ttu-id="ecd05-117">Valitse tuotteen nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="ecd05-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="ecd05-118">Kohdemaa</span><span class="sxs-lookup"><span data-stu-id="ecd05-118">Destination country</span></span> | <span data-ttu-id="ecd05-119">Valitse maa, johon tuote lähetetään.</span><span class="sxs-lookup"><span data-stu-id="ecd05-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="ecd05-120">Alkuperämaa</span><span class="sxs-lookup"><span data-stu-id="ecd05-120">Origin country</span></span> | <span data-ttu-id="ecd05-121">Valitse maa, josta tuote lähetetään.</span><span class="sxs-lookup"><span data-stu-id="ecd05-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="ecd05-122">Tämän asetuksen tarkoitus on auttaa luomaan tuoterakenneraportti, jossa alkuperämaa voidaan sisällyttää kuhunkin osaan, johon lähde- ja kohdemaa on määritetty.</span><span class="sxs-lookup"><span data-stu-id="ecd05-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="ecd05-123">Tämän raportin avulla saadaan kokonaisvaltainen käsityksen siitä, mistä osat tulevat ja mihin ne ovat menossa.</span><span class="sxs-lookup"><span data-stu-id="ecd05-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="ecd05-124">Toimittajien varmenteiden seuraaminen</span><span class="sxs-lookup"><span data-stu-id="ecd05-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="ecd05-125">Voit seurata toimittajille myönnettyjä varmenteita **Toimittajien alkuperämaavarmenteet** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ecd05-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="ecd05-126">Sinun on päätettävä, mitä varmenneasiakirjoja myönnetään ja miten ne raportoidaan asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="ecd05-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="ecd05-127">Tämä toimintoa auttaa seuraamaan varmenteita.</span><span class="sxs-lookup"><span data-stu-id="ecd05-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="ecd05-128">Sen avulla voi myös valita, näkyvätkö varmennenumerot laskuissa, pakkausluetteloissa ja/tai tilausvahvistuksissa.</span><span class="sxs-lookup"><span data-stu-id="ecd05-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="ecd05-129">Voit määrittää varmenteen tiedot seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="ecd05-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="ecd05-130">Valitse **Tuotetietojen hallinta \> Asetukset \> Tuotteen yhteensopivuus \> Alkuperämaa \> Toimittajan alkuperämaavarmenteet**.</span><span class="sxs-lookup"><span data-stu-id="ecd05-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="ecd05-131">Valitse aiemmin luodun varmenteen asetukset muokattavaksi tai luo uudet varmenneasetukset valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ecd05-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="ecd05-132">Määritä seuraavat valitun tai uuden varmenteen asetukset:</span><span class="sxs-lookup"><span data-stu-id="ecd05-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="ecd05-133">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ecd05-133">Field</span></span> | <span data-ttu-id="ecd05-134">kuvaus</span><span class="sxs-lookup"><span data-stu-id="ecd05-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="ecd05-135">Toimittajatili</span><span class="sxs-lookup"><span data-stu-id="ecd05-135">Vendor account</span></span> | <span data-ttu-id="ecd05-136">Valitse toimittaja, jolle varmenne myönnetään.</span><span class="sxs-lookup"><span data-stu-id="ecd05-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="ecd05-137">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="ecd05-137">Item number</span></span> | <span data-ttu-id="ecd05-138">Valitse nimike, jolle varmenne myönnetään.</span><span class="sxs-lookup"><span data-stu-id="ecd05-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="ecd05-139">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="ecd05-139">Country/region</span></span> | <span data-ttu-id="ecd05-140">Kohdemaa tai -alue, jossa tätä varmennetta on käytettävä.</span><span class="sxs-lookup"><span data-stu-id="ecd05-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="ecd05-141">Varmenteen numero</span><span class="sxs-lookup"><span data-stu-id="ecd05-141">Certificate number</span></span> | <span data-ttu-id="ecd05-142">Anna myönnetyn varmenteen tunnusnumero.</span><span class="sxs-lookup"><span data-stu-id="ecd05-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="ecd05-143">Voimassa</span><span class="sxs-lookup"><span data-stu-id="ecd05-143">Effective</span></span> | <span data-ttu-id="ecd05-144">Valitse ensimmäinen päivämäärä, jolloin nykyinen varmenne on voimassa.</span><span class="sxs-lookup"><span data-stu-id="ecd05-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="ecd05-145">Vanhentumisaika</span><span class="sxs-lookup"><span data-stu-id="ecd05-145">Expiration</span></span> | <span data-ttu-id="ecd05-146">Valitse viimeinen päivämäärä, jolloin nykyinen varmenne on voimassa.</span><span class="sxs-lookup"><span data-stu-id="ecd05-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="ecd05-147">Tulosta laskulle</span><span class="sxs-lookup"><span data-stu-id="ecd05-147">Print on invoice</span></span> | <span data-ttu-id="ecd05-148">Valitse tämä valintaruutu, kun varmennenumero tulostetaan laskuihin, joiden osoitteena on määritetty maa määritetyllä päivämääräalueella.</span><span class="sxs-lookup"><span data-stu-id="ecd05-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="ecd05-149">Tulosta pakkausluettelossa</span><span class="sxs-lookup"><span data-stu-id="ecd05-149">Print on packing slip</span></span> | <span data-ttu-id="ecd05-150">Valitse tämä valintaruutu, kun varmennenumero tulostetaan pakkausluetteloihin, joiden osoitteena on määritetty maa määritetyllä päivämääräalueella.</span><span class="sxs-lookup"><span data-stu-id="ecd05-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="ecd05-151">Tulosta myyntitilauksessa</span><span class="sxs-lookup"><span data-stu-id="ecd05-151">Print on sales order</span></span> | <span data-ttu-id="ecd05-152">Valitse tämä valintaruutu, kun varmennenumero tulostetaan myyntitilauksiin, joiden osoitteena on määritetty maa määritetyllä päivämääräalueella.</span><span class="sxs-lookup"><span data-stu-id="ecd05-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="ecd05-153">Sisällytä alkuperämaa tuoterakenneraportteihin</span><span class="sxs-lookup"><span data-stu-id="ecd05-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="ecd05-154">Kun luot tuoterakenneraportin, voit sisällyttää kunkin sellaisen osan alkuperämaan, jonka lähde- ja kohdemaa on määritetty **Alkuperämaasäännöt**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="ecd05-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="ecd05-155">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="ecd05-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="ecd05-156">Avaa tuotteen **Vapautetun tuotteen tiedot** -sivu valitsemalla tai luomalla tuote.</span><span class="sxs-lookup"><span data-stu-id="ecd05-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="ecd05-157">Valitse toimintoruudun **Suunnittele**-välilehden **Tuoterakenne**-ryhmässä **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="ecd05-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="ecd05-158">Valitse avautuvan sivun toimintoruudussa **Tuoterakenne \> Tulosta**.</span><span class="sxs-lookup"><span data-stu-id="ecd05-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="ecd05-159">Määritä **Tuoterakennerivit**-valintaikkunassa **Kohdemaa**-kentässä kohdemaa, jota haluat tarkastella raportissa.</span><span class="sxs-lookup"><span data-stu-id="ecd05-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="ecd05-160">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecd05-160">Select **OK**.</span></span>

<span data-ttu-id="ecd05-161">Kunkin osan alkuperämaasta tietoja sisältävä raportti luodaan ja näytetään.</span><span class="sxs-lookup"><span data-stu-id="ecd05-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="ecd05-162">Esimerkki raportista.</span><span class="sxs-lookup"><span data-stu-id="ecd05-162">Here is an example of the report.</span></span>

<span data-ttu-id="ecd05-163">![Alkuperämaaraportti](media/country-of-origin-report.png "Alkuperämaaraportti")</span><span class="sxs-lookup"><span data-stu-id="ecd05-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
