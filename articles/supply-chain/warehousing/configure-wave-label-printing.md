---
title: Aallon etikettitulostuksen määrittäminen ja käyttäminen
description: Tässä ohjeaiheessa käsitellään aallon etikettitulostusta ja sen määrittämistä.
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: a08f10c1f5c3ff5b9023f37614c4e113b3a6b30d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211763"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="b6a94-103">Aallon etikettitulostuksen määrittäminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="b6a94-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6a94-104">Aallon etikettitulostus on vaihtoehtoinen tapa tulostaa etikettejä. Siinä otetaan käyttöön uusin aallon vaihe, jossa luodaan ja tulostetaan etikettejä suoraan aaltomallista aallon suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="b6a94-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="b6a94-105">Tämän vuoksi etiketit ovat saatavana jo ennen kuin työtekijät suorittavat työtilauksen mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="b6a94-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="b6a94-106">Työntekijät voivat sitten kiinnittää tarvittavat etiketit keräilyn aikana eikä sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="b6a94-107">Aallon etikettitulostus luo etikettiasettelut ZLP (Zebra Programming Language) -kielen avulla.</span><span class="sxs-lookup"><span data-stu-id="b6a94-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="b6a94-108">Etikettiasettelu on jaettu kolmeen osaan (ylätunniste, teksti ja alatunniste), jolloin etikettien rakenne pysyy samana.</span><span class="sxs-lookup"><span data-stu-id="b6a94-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="b6a94-109">Aallon etikettimalli ilmaisee järjestelmälle käytettävän etikettiasettelun.</span><span class="sxs-lookup"><span data-stu-id="b6a94-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="b6a94-110">Käyttäjät voivat määrittää käytettävän tulostimen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-110">Users can specify which printer is used.</span></span> <span data-ttu-id="b6a94-111">He voivat myös tarvittaessa tulostaa etikettejä monessa tulostimessa samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="b6a94-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="b6a94-112">**Aallon etiketin historia** -sivulle on kirjattu kaikki etiketit, jotka on luotu kyseisellä määrityksellä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="b6a94-113">Etikettejä voi tulostaa ja lajitella työn ylätunnisteiden perusteella, minkä lisäksi voidaan tulostaa työn ylätunnistekohtaisia keskeytysetikettejä sekä etikettejä kontin sisällöstä, laatikkoetikettejä ja muita vastaavia etikettejä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="b6a94-114">Tämä toiminto ei korvaa nykyistä asiakirjan reititykseen perustuvaa etikettitulostustoimintoa.</span><span class="sxs-lookup"><span data-stu-id="b6a94-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="b6a94-115">Aallon etikettitulostukseen liittyvät parannukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="b6a94-116">Etiketit tulostetaan yhden työrivin pakkausten määrän perusteella ilman konttiinpakkausta.</span><span class="sxs-lookup"><span data-stu-id="b6a94-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="b6a94-117">(Pakkaus on yksikkö, joka on määritetty yksikön sarjaryhmäriveillä.)</span><span class="sxs-lookup"><span data-stu-id="b6a94-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="b6a94-118">Useiden etikettisarjojen tulostaminen (kuten pakkaus- ja kuormalavaetiketit).</span><span class="sxs-lookup"><span data-stu-id="b6a94-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="b6a94-119">Etiketin luetteloinnin (kuten 1/124, 2/124, ... 124/124) sisällyttäminen ja luettelointialueen määrittäminen (kuten työrivi, kuormarivi tai lähetys).</span><span class="sxs-lookup"><span data-stu-id="b6a94-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="b6a94-120">Rahtikirjan tunnuksen luominen ja tulostaminen etiketteihin ennen rahtikirjan muodostamista.</span><span class="sxs-lookup"><span data-stu-id="b6a94-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="b6a94-121">Yksilöivän SSCC (Serial Shipping Container Code) -koodiin luominen kullekin pakkaukselle ja sen sisällyttäminen jokaiseen tarraan.</span><span class="sxs-lookup"><span data-stu-id="b6a94-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="b6a94-122">GS1-yhteensopivien numerosarjojen luominen rahtikirjan tunnuksille ja SSCC-koodeille.</span><span class="sxs-lookup"><span data-stu-id="b6a94-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="b6a94-123">Etikettien uudelleentulostaminen sekä mobiililaitteita että raskaasta asiakkaasta.</span><span class="sxs-lookup"><span data-stu-id="b6a94-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="b6a94-124">Etikettien mitätöinti (esimerkiksi lyhyissä keräilyskenaarioissa) ja niiden uudelleentulostaminen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="b6a94-125">Aallon etikettihistorian tyhjentäminen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="b6a94-126">Asiakirjareitityksen asettelujen parannukset jaetaan asiakirjareitityksen asettelujen ja aallon etiketin asettelujen kesken.</span><span class="sxs-lookup"><span data-stu-id="b6a94-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="b6a94-127">(Lisätietoja on kohdassa [Rekisterikilven asiakirjareitityksen asettelu](../warehousing/document-routing-layout-for-license-plates.md).)</span><span class="sxs-lookup"><span data-stu-id="b6a94-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="b6a94-128">Nämä parannukset tehostavat etikettien käyttöä pakkauksissa ennen pakkausta kuormalavalle.</span><span class="sxs-lookup"><span data-stu-id="b6a94-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="b6a94-129">Niistä on hyötyä etenkin suurille jälleenmyyjille lähettäville yrityksille, sillä ne vahvistavat tilausten vastaanotan lukemalla kunkin pakkauksen erikseen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="b6a94-130">Tässä ohjeaiheessa käsiteltävät määritysskenaariot voidaan toteuttaa joko erikseen tai yhdistelminä sen mukaan, mikä vastaa parhaiten liiketoimintarpeita.</span><span class="sxs-lookup"><span data-stu-id="b6a94-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="b6a94-131">Voit suunnitella useita aallon sarjana käytettäviä etikettimalleja (josta on esimerkki skenaariossa 3).</span><span class="sxs-lookup"><span data-stu-id="b6a94-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="b6a94-132">Voit esimerkiksi käyttää skenaariota 1 pakkausten etikettien tulostamiseen ja skenaariota 2 kuormalavan etikettien tulostamiseen (jos varaston kuormalavojen koossa ja kokoonpanossa on eroja):</span><span class="sxs-lookup"><span data-stu-id="b6a94-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="b6a94-133">Aallon etiketin tulostustoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="b6a94-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="b6a94-134">Ennen kuin voit käyttää *Aallon etikettitulostus* -toimintoa, sen on oltava otettuna käyttöön järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="b6a94-135">Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="b6a94-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b6a94-136">Tässä tapauksessa toiminto näkyy seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="b6a94-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b6a94-137">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="b6a94-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b6a94-138">**Toiminnon nimi:** *Aallon etikettitulostus*</span><span class="sxs-lookup"><span data-stu-id="b6a94-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="b6a94-139">Skenaario 1: Aallon etikettitulostus, kun luotavana on yksi aallon etiketti</span><span class="sxs-lookup"><span data-stu-id="b6a94-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="b6a94-140">Tässä skenaariossa näytetään, miten yritys voi tulostaa lähetyksen etikettejä suurelle jälleenmyyjälle, joka vahvistaa tilausten vastaanotot automaattisesti lukemalla kunkin pakkauksen erikseen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="b6a94-141">Tämä skenaario sisältää työnkulun alusta loppuun.</span><span class="sxs-lookup"><span data-stu-id="b6a94-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="b6a94-142">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="b6a94-142">Make demo data available</span></span>

<span data-ttu-id="b6a94-143">Tämän skenaarion käyttäminen edellyttää, että demotiedot on asennettu ja että **USMF**-yritys on valittu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="b6a94-144">Aallon etikettimenetelmän saatavuuden varmistaminen</span><span class="sxs-lookup"><span data-stu-id="b6a94-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="b6a94-145">On mahdollista, että aallon käsittelymenetelmät on luotava uudelleen, jotta aallon etiketin tulostusmenetelmä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="b6a94-146">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon käsittelymenetelmät**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="b6a94-147">Varmista, että **waveLabelPrinting** on luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b6a94-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="b6a94-148">Jos se ei ole luettelossa, lisää se valitsemalla toimintoruudussa **Luo menetelmät uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="b6a94-149">Aaltomallin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b6a94-149">Configure a wave template</span></span>

<span data-ttu-id="b6a94-150">Aaltomallin avulla tietyt aaltomenetelmien esiintymät voidaan linkittää vastaavaan aallon etikettimalliin.</span><span class="sxs-lookup"><span data-stu-id="b6a94-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="b6a94-151">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="b6a94-152">Valitse malli, kuten **62 Lähetyksen oletus**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="b6a94-153">Siirrä **Aallon etiketin tulostus** -menetelmä **Menetelmät**-pikavälilehdessä **Valitut menetelmät** -sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="b6a94-154">Valitse **Valitut menetelmät** -sarakkeessa **Aallon etiketin tulostus** -menetelmä ja valitsen sen **Aallon vaihekoodi** -kentässä *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="b6a94-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="b6a94-155">Lisätietoja aallon vaihekoodeista on kohdassa [Aallon vaihekoodit](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b6a94-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="b6a94-156">Aallon etikettiasettelun luominen</span><span class="sxs-lookup"><span data-stu-id="b6a94-156">Create a wave label layout</span></span>

<span data-ttu-id="b6a94-157">Etiketin asettelu määrittää, mitä tietoja etikettiin tulostetaan ja miten ne näkyvät etiketissä. Annettava ZPL-koodi lähetetään tulostimeen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="b6a94-158">Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etiketin asettelut**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="b6a94-159">Luo tietue, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-160">**Etiketin asettelutunnus:** *Pakkaus*</span><span class="sxs-lookup"><span data-stu-id="b6a94-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="b6a94-161">**Kuvaus:** *Pakkaus (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="b6a94-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="b6a94-162">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="b6a94-163">Valitse toimintoruudussa **Aallon etiketin riviasetukset**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="b6a94-164">**Aallon etiketin riviasetukset** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="b6a94-165">Etiketin dynaaminen osa määritetään tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="b6a94-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="b6a94-166">Lisää rivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-167">**Rivin tunnus:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="b6a94-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="b6a94-168">**Rivin taulukon nimi:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="b6a94-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="b6a94-169">**Rivin lähtökohta:** *0*</span><span class="sxs-lookup"><span data-stu-id="b6a94-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="b6a94-170">Tämä kenttä määrittää pystysuunnassa paikan, josta rivi alkaa etiketissä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="b6a94-171">**Rivin korkeus:** *0*</span><span class="sxs-lookup"><span data-stu-id="b6a94-171">**Row height:** *0*</span></span>

        <span data-ttu-id="b6a94-172">Tämä kenttää määrittää kunkin rivin korkeuden (pisteinä) ZPL-standardin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b6a94-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="b6a94-173">Rivin korkeus on positiivinen vaakasuuntaisissa etiketeissä ja negatiivinen pystysuuntaisissa etiketeissä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="b6a94-174">Koska tässä esimerkissä on vain yksi rivi, arvoksi voidaan määrittää *0* (nolla).</span><span class="sxs-lookup"><span data-stu-id="b6a94-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="b6a94-175">**Riviä sivua kohden:** *1*</span><span class="sxs-lookup"><span data-stu-id="b6a94-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="b6a94-176">Tämä kenttä määrittää, kuinka monta riviä kuhunkin etikettiin tulostetaan.</span><span class="sxs-lookup"><span data-stu-id="b6a94-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b6a94-177">Tämän asetuksen seurauksena kullekin aallon etikettitaulun tietueelle tulostetaan erillinen ZPL-etiketti.</span><span class="sxs-lookup"><span data-stu-id="b6a94-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="b6a94-178">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-178">Close the page.</span></span>
1. <span data-ttu-id="b6a94-179">Valitse toimintoruudussa **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="b6a94-180">Lisää kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-181">**Taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-182">**Johdettu taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-183">**Kenttä:** *Työtyyppi*</span><span class="sxs-lookup"><span data-stu-id="b6a94-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="b6a94-184">**Ehdot:** *Keräily*</span><span class="sxs-lookup"><span data-stu-id="b6a94-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="b6a94-185">Tämä kysely varmistaa, että etikettiin tulostetaan vain keräilytyyppiset työrivit, eikä siis poispanotyyppisiä työrivejä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="b6a94-186">Jos haluat tulostaa rahtikirjan tunnuksen valitse **Liitokset**-välilehdessä **Työrivit**-taulu ja liitä **Lähetykset**-taulu siihen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="b6a94-187">Sulkee kyselyeditorin valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="b6a94-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="b6a94-188">**Tulostimen tekstiasettelu** -pikavälilehdessä on kolme osaa, johon voi kirjoittaa tulostinkoodin: **ylätunnisteosio**, **tekstiosio** ja **alatunnisteosio**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="b6a94-189">Anna **ylätunnisteosion** **Etiketin ylätunniste** -kenttään vaadittavan ylätunnisteen koodi.</span><span class="sxs-lookup"><span data-stu-id="b6a94-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="b6a94-190">Jos käytössä on esimerkiksi Zebra-tulostimet voit käyttää seuraavaa koodia.</span><span class="sxs-lookup"><span data-stu-id="b6a94-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="b6a94-191">Anna **tekstiosion** **Etiketin teksti** -kenttään vaadittavan tekstin ZPL-koodi.</span><span class="sxs-lookup"><span data-stu-id="b6a94-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="b6a94-192">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="b6a94-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="b6a94-193">Anna **tekstiosion** **Etiketin alatunniste** -kenttään vaadittavan alatunnisteen ZPL-koodi.</span><span class="sxs-lookup"><span data-stu-id="b6a94-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="b6a94-194">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="b6a94-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="b6a94-195">Tämä asetus tulostaa yhden kopion kustakin etiketistä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="b6a94-196">Jos kopioita tarvitaan enemmän (esimerkiksi yksi kuormalavan kummallekin puolelle), määritä alatunnisteen **\^PQn**-osan **n**-arvoksi tarvittava määrä kopioita.</span><span class="sxs-lookup"><span data-stu-id="b6a94-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="b6a94-197">Jos kutakin etikettiä halutaan tulostaa neljä kappaletta, käytä määritystä **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="b6a94-198">Etiketti on nyt käyttövalmis.</span><span class="sxs-lookup"><span data-stu-id="b6a94-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="b6a94-199">Aallon etikettityypin luominen</span><span class="sxs-lookup"><span data-stu-id="b6a94-199">Create a wave label type</span></span>

<span data-ttu-id="b6a94-200">Aallon etikettityyppien avulla aallon etikettimallit linkitetään yksikön sarjaryhmärivien yksikköön.</span><span class="sxs-lookup"><span data-stu-id="b6a94-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="b6a94-201">Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etikettityypit**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="b6a94-202">Lisää aallon etikettityyppi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-203">**Etikettityyppi:** *Pakkaus*</span><span class="sxs-lookup"><span data-stu-id="b6a94-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="b6a94-204">**Kuvaus:** *Pakkaus*</span><span class="sxs-lookup"><span data-stu-id="b6a94-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="b6a94-205">Määritä yksikön sarjaryhmät</span><span class="sxs-lookup"><span data-stu-id="b6a94-205">Set up unit sequence groups</span></span>

<span data-ttu-id="b6a94-206">Seuraavaksi määritetään aallon etikettityypin yksikön sarjaryhmä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="b6a94-207">Valitse **Varastonhallinta \> Asetukset \> Varasto \> Yksikön sarjaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="b6a94-208">Valitse **Kpl laatikko KL** -ryhmä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="b6a94-209">Määritä **Laatikko**-rivin **Aallon tasotyyppi** -kentän arvoksi *Pakkaus*.</span><span class="sxs-lookup"><span data-stu-id="b6a94-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="b6a94-210">Aallon etikettimallin luominen</span><span class="sxs-lookup"><span data-stu-id="b6a94-210">Create a wave label template</span></span>

<span data-ttu-id="b6a94-211">Seuraavaksi luodaan aallon etikettityypin aallon etikettimalli.</span><span class="sxs-lookup"><span data-stu-id="b6a94-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="b6a94-212">Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etikettimallit**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="b6a94-213">Lisää aallon tasomalli ja määritä seuraavat arvot ylätunnisteessa:</span><span class="sxs-lookup"><span data-stu-id="b6a94-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="b6a94-214">**Etikettimallin nimi:** *Pakkausetiketit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="b6a94-215">**Kuvaus:** *Pakkausetiketit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="b6a94-216">**Aallon vaihekoodi:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="b6a94-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="b6a94-217">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="b6a94-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="b6a94-218">Määritä **Yleiset**-pikavälilehden **Aallon etikettityyppi** -kentän arvoksi *Pakkaus*.</span><span class="sxs-lookup"><span data-stu-id="b6a94-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="b6a94-219">Lisää **Aallon etikettimallin tiedot** -pikavälilehdessä uusi rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-220">**Etiketin asettelutunnus:** *Pakkaus*</span><span class="sxs-lookup"><span data-stu-id="b6a94-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="b6a94-221">**Tulostimen nimi:** valitse sopiva ZPL-tulostin.</span><span class="sxs-lookup"><span data-stu-id="b6a94-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="b6a94-222">**Suorita kysely:** *Kyllä* (Tämä asetus on valinnainen, mutta sen käyttöä suositellaan suorituskyvyn optimoinnin vuoksi.)</span><span class="sxs-lookup"><span data-stu-id="b6a94-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="b6a94-223">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="b6a94-224">Valinnainen: Jos asiakaskohtainen etikettirakenne määritetään, asiakastilin etsimistä varten on luotava kysely.</span><span class="sxs-lookup"><span data-stu-id="b6a94-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="b6a94-225">Valitse **Aallon etikettimallin tiedot** -pikavälilehdessä **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="b6a94-226">Lisää sitten kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-227">**Taulukko:** *Lähetykset*</span><span class="sxs-lookup"><span data-stu-id="b6a94-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="b6a94-228">**Johdettu taulu:** *Lähetykset*</span><span class="sxs-lookup"><span data-stu-id="b6a94-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="b6a94-229">**Kenttä:** *Tilin numero*</span><span class="sxs-lookup"><span data-stu-id="b6a94-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="b6a94-230">**Ehdot:** anna soveltuvan asiakastilin numero.</span><span class="sxs-lookup"><span data-stu-id="b6a94-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="b6a94-231">Kun olet valmis, sulje kyselyeditorin valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="b6a94-232">Avaa koko etikettimallin kyselyeditorin valintaikkuna valitsemalla toimintoruudussa **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="b6a94-233">Lisää kyselyeditorin valintaikkunan **Lajittelu**-välilehdessä rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-234">**Taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-235">**Johdettu taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-236">**Kenttä:** *Viittauksen kuormarivin tunnus (tietuetunnus)*</span><span class="sxs-lookup"><span data-stu-id="b6a94-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="b6a94-237">**Hakusuunta:** *Laskeva*</span><span class="sxs-lookup"><span data-stu-id="b6a94-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="b6a94-238">Sulje kyselyeditorin valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="b6a94-239">Avautuva sanomaruutu pyytää vahvistamaan ryhmittelyn nollaustoiminnon.</span><span class="sxs-lookup"><span data-stu-id="b6a94-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="b6a94-240">Jatka valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="b6a94-241">Valitse Toimintoruudussa **Aallon etiketin malliryhmä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="b6a94-242">Valitse **Aallon etiketin malliryhmä** -valintaikkunassa rivi, jossa **Viitekentän nimi** -kentän asetuksena *Viittauksen kuormarivin tunnus* ja valitse sitten rivin **Etiketin luontitunnus** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b6a94-243">Tämä asetus luo kullekin kuormariville yhden etikettisarjan (Pakkaus 1/X) koko aallon osalta työn ryhmittelyasetuksesta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="b6a94-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="b6a94-244">Tämä etikettisarja voidaan tulostaa etikettiasetteluun.</span><span class="sxs-lookup"><span data-stu-id="b6a94-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="b6a94-245">Numerosarjalaajennusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b6a94-245">Configure number sequence extensions</span></span>

<span data-ttu-id="b6a94-246">Numerosarjalaajennuksilla hallitaan tiettyjen numerosarjojen GS1-vaatimustenmukaisuutta.</span><span class="sxs-lookup"><span data-stu-id="b6a94-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="b6a94-247">Tämä määritys on valinnainen nykyisessä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="b6a94-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="b6a94-248">Lisätietoja ja määritysohjeet ovat kohdassa [Numerosarjalaajennusten määrittäminen](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="b6a94-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="b6a94-249">Myyntitilauksen luominen ja sen vapauttaminen varastoon</span><span class="sxs-lookup"><span data-stu-id="b6a94-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="b6a94-250">Valitse **Myynti ja markkinointi \> Myyntitilaus \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="b6a94-251">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-252">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b6a94-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b6a94-253">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="b6a94-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="b6a94-254">Lisää kaksi myyntitilausriviä, joilla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="b6a94-255">Myyntitilausrivi 1:</span><span class="sxs-lookup"><span data-stu-id="b6a94-255">Sales order line 1:</span></span>

        - <span data-ttu-id="b6a94-256">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b6a94-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="b6a94-257">**Määrä** *9024*</span><span class="sxs-lookup"><span data-stu-id="b6a94-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="b6a94-258">**Yksikkö:** *kpl* (9024 kpl = 376 laatikkoa = 47 kuormalavaa)</span><span class="sxs-lookup"><span data-stu-id="b6a94-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="b6a94-259">Myyntitilausrivi 2:</span><span class="sxs-lookup"><span data-stu-id="b6a94-259">Sales order line 2:</span></span>

        - <span data-ttu-id="b6a94-260">**Nimiketunnus:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="b6a94-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="b6a94-261">**Määrä** *9016*</span><span class="sxs-lookup"><span data-stu-id="b6a94-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="b6a94-262">**Yksikkö:** *kpl* (9016 kpl = 322 laatikkoa = 46 kuormalavaa)</span><span class="sxs-lookup"><span data-stu-id="b6a94-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="b6a94-263">Nämä nimikkeet ja määrät ovat vain esimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="b6a94-264">Niiden on käytettävä aiemmin määritettyä yksikön sarjaryhmää, niille on määritettävä soveltuva yksikkömuunnos *kappaleesta* *laatikkoon* ja edelleen *kuormalavaksi* ja niiden varaston on oltava varastossa *62*.</span><span class="sxs-lookup"><span data-stu-id="b6a94-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="b6a94-265">Lisätietoja on kohdassa [Mittayksikkö ja varastointikäytännöt](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b6a94-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="b6a94-266">Valitse tilausrivi 1.</span><span class="sxs-lookup"><span data-stu-id="b6a94-266">Select sales order line 1.</span></span> <span data-ttu-id="b6a94-267">Valitse sitten **Myyntitilausrivi**-osan **Varasto**-valikossa **Varaukset**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="b6a94-268">Valitse **Varaus**-sivun toimintoruudussa **Varaa erä** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="b6a94-269">Toista vaiheet 4 ja 5 myyntitilausriville 2.</span><span class="sxs-lookup"><span data-stu-id="b6a94-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="b6a94-270">Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b6a94-271">Seuraavat tapahtumat:</span><span class="sxs-lookup"><span data-stu-id="b6a94-271">The following events occur:</span></span>

    - <span data-ttu-id="b6a94-272">Järjestelmä käsittelee luodun lähetyksen käyttämällä etiketin tulostusvaiheen sisältävää mallia.</span><span class="sxs-lookup"><span data-stu-id="b6a94-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="b6a94-273">Etiketin asettelun avulla määritetään etiketin muoto, ja näin saatu etiketti tulostetaan etikettimallissa valitulla tulostimella.</span><span class="sxs-lookup"><span data-stu-id="b6a94-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="b6a94-274">Aallon etiketit luodaan ja tulostetaan.</span><span class="sxs-lookup"><span data-stu-id="b6a94-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="b6a94-275">Etikettien ja pakkausten määrä on sama (tässä esimerkiksi rivillä 1 on 376 laatikkoetikettiä ja rivillä 2 niitä on 322).</span><span class="sxs-lookup"><span data-stu-id="b6a94-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="b6a94-276">Lähetyksille luodaan uusi rahtikirjan tunnus.</span><span class="sxs-lookup"><span data-stu-id="b6a94-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="b6a94-277">Jos numerosarjalaajennukset määritettiin, aallon etikettitunnus noudattaa **SSCC-18**-lukumuotoilua.</span><span class="sxs-lookup"><span data-stu-id="b6a94-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="b6a94-278">Voit tarkastella aallon etikettejä ja tulostaa niitä uudelleen seuraavilta sivuilta.</span><span class="sxs-lookup"><span data-stu-id="b6a94-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="b6a94-279">Valitse kunkin sivun toimintoruudun **Lähetykset**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Aallon etiketit**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="b6a94-280">Kaikki lähetykset \> Lähetyksen tiedot</span><span class="sxs-lookup"><span data-stu-id="b6a94-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="b6a94-281">Kaikki kuormat \> Kuorman tiedot</span><span class="sxs-lookup"><span data-stu-id="b6a94-281">All loads \> Load details</span></span>
- <span data-ttu-id="b6a94-282">Kaikki aallot</span><span class="sxs-lookup"><span data-stu-id="b6a94-282">All waves</span></span>
- <span data-ttu-id="b6a94-283">Aalto-otsikot</span><span class="sxs-lookup"><span data-stu-id="b6a94-283">Wave labels</span></span>
- <span data-ttu-id="b6a94-284">Aallon etikettihistoria</span><span class="sxs-lookup"><span data-stu-id="b6a94-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="b6a94-285">Skenaario 2: Aallon konttiinpakkauksen etikettitulostus (ilman aallon etikettitietueita)</span><span class="sxs-lookup"><span data-stu-id="b6a94-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="b6a94-286">Tässä skenaariossa tulostetaan aallon etikettejä konttipakkausta käytettäessä. Tällä tavoin nimikkeet jaetaan automaattisesti pakkauksiin eikä aallon etikettitietuetta tarvita.</span><span class="sxs-lookup"><span data-stu-id="b6a94-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="b6a94-287">Tässä tapauksessa kontin tunnus toimii SSCC-koodin paikkamerkkinä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="b6a94-288">Tämä skenaarion ja skenaarion 1 tärkeimmät erot:</span><span class="sxs-lookup"><span data-stu-id="b6a94-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="b6a94-289">**Aallon etikettimallit:** Aallon etikettityyppiä ei valita aallon etikettimallissa eikä etiketin luontiryhmittelyä tarvita.</span><span class="sxs-lookup"><span data-stu-id="b6a94-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="b6a94-290">Muutoin aallon etikettimalli määritetään ja linkitys aaltomalliin tehdään skenaariossa 1 kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="b6a94-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="b6a94-291">Aallon etikettityyppi on jätettävä tyhjäksi, sillä se estää aallon etikettien luonnin.</span><span class="sxs-lookup"><span data-stu-id="b6a94-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="b6a94-292">**Aallon etiketin asettelut:** Aallon etikettiasettelun riviasettelut tehdään työriveillä eikä aallon etikettitietueille.</span><span class="sxs-lookup"><span data-stu-id="b6a94-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="b6a94-293">Etikettiasettelun riviasetus on määritettävä käyttämällä **WHSWorkLine**-taulua eikä **WHSWaveLabel**-taulua.</span><span class="sxs-lookup"><span data-stu-id="b6a94-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="b6a94-294">**Riviä sivua kohden** -asetus määrittää, kuinka monta riviä tekstiosassa on.</span><span class="sxs-lookup"><span data-stu-id="b6a94-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="b6a94-295">Tämä määritys sopii myös liiketoimintaskenaarioihin, joissa useita eri nimikkeitä pakataan yhteen etiketilliseen laatikkoon tai kuormalavalle, ja tämä pakkausprosessi voidaan määrittää työn luonnilla (kuten lähetyksen mukaan ryhmitetty työ).</span><span class="sxs-lookup"><span data-stu-id="b6a94-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="b6a94-296">Tämä skenaario sisältää työnkulun alusta loppuun.</span><span class="sxs-lookup"><span data-stu-id="b6a94-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="b6a94-297">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="b6a94-297">Make demo data available</span></span>

<span data-ttu-id="b6a94-298">Tämän skenaarion käyttäminen edellyttää, että demotiedot on asennettu ja että **USMF**-yritys on valittu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="b6a94-299">Aallon etikettimenetelmän saatavuuden varmistaminen</span><span class="sxs-lookup"><span data-stu-id="b6a94-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="b6a94-300">On mahdollista, että aallon käsittelymenetelmät on luotava uudelleen, jotta aallon etiketin tulostusmenetelmä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="b6a94-301">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon käsittelymenetelmät**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="b6a94-302">Varmista, että **waveLabelPrinting** on luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b6a94-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="b6a94-303">Jos se ei ole luettelossa, lisää se valitsemalla toimintoruudussa **Luo menetelmät uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="b6a94-304">Aaltomallin asetuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b6a94-304">Set up a wave template</span></span>

<span data-ttu-id="b6a94-305">Aaltomallin avulla tietyt aaltomenetelmien esiintymät voidaan linkittää vastaavaan aallon etikettimalliin.</span><span class="sxs-lookup"><span data-stu-id="b6a94-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="b6a94-306">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="b6a94-307">Valitse malli, kuten **63 Konttiinpakkaus**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="b6a94-308">Siirrä **Aallon etiketin tulostus** -menetelmä **Menetelmät**-pikavälilehdessä **Valitut menetelmät** -sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="b6a94-309">Valitse **Valitut menetelmät** -sarakkeessa **Aallon etiketin tulostus** -menetelmä ja valitsen sen **Aallon vaihekoodi** -kentässä *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="b6a94-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="b6a94-310">Lisätietoja aallon vaihekoodeista on kohdassa [Aallon vaihekoodit](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b6a94-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="b6a94-311">Aallon etikettiasettelun luominen</span><span class="sxs-lookup"><span data-stu-id="b6a94-311">Create a wave label layout</span></span>

1. <span data-ttu-id="b6a94-312">Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etiketin asettelut**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="b6a94-313">Luo tietue, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-314">**Etiketin asettelutunnus:** *Pakkaus*</span><span class="sxs-lookup"><span data-stu-id="b6a94-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="b6a94-315">**Kuvaus:** *Pakkaus (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="b6a94-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="b6a94-316">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="b6a94-317">Valitse toimintoruudussa **Aallon etiketin riviasetukset**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="b6a94-318">**Aallon etiketin riviasetukset** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="b6a94-319">Etiketin dynaaminen osa määritetään tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="b6a94-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="b6a94-320">Lisää rivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-321">**Rivin tunnus:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="b6a94-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="b6a94-322">**Rivin taulukon nimi:** *WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="b6a94-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="b6a94-323">**Rivin lähtökohta:** *500*</span><span class="sxs-lookup"><span data-stu-id="b6a94-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="b6a94-324">Tämä kenttä määrittää pystysuunnassa paikan, josta rivi alkaa etiketissä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="b6a94-325">**Rivin korkeus:** *-50*</span><span class="sxs-lookup"><span data-stu-id="b6a94-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="b6a94-326">Tämä kenttä määrittää kunkin rivin korkeuden.</span><span class="sxs-lookup"><span data-stu-id="b6a94-326">This field defines the height of each row.</span></span> <span data-ttu-id="b6a94-327">Rivin korkeus on positiivinen vaakasuuntaisissa etiketeissä ja negatiivinen pystysuuntaisissa etiketeissä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="b6a94-328">**Riviä sivua kohden:** *5*</span><span class="sxs-lookup"><span data-stu-id="b6a94-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="b6a94-329">Tämä kenttä määrittää, kuinka monta riviä kuhunkin etikettiin tulostetaan.</span><span class="sxs-lookup"><span data-stu-id="b6a94-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b6a94-330">Tämä asetus tulostaa kullekin työlle useita ZPL-etikettejä, ja kullakin sivulla voi olla enintään viisi työriviä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="b6a94-331">Jos esimerkiksi konttiin tulostettavassa etiketissä on 12 riviä, etikettejä tulostetaan kolme.</span><span class="sxs-lookup"><span data-stu-id="b6a94-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="b6a94-332">Jos haluat tulostaa erillisen etiketin kullekin keräilyriville, määritä arvoksi *1*.</span><span class="sxs-lookup"><span data-stu-id="b6a94-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="b6a94-333">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-333">Close the page.</span></span>
1. <span data-ttu-id="b6a94-334">Valitse toimintoruudussa **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="b6a94-335">Lisää kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-336">**Taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-337">**Johdettu taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-338">**Kenttä:** *Työtyyppi*</span><span class="sxs-lookup"><span data-stu-id="b6a94-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="b6a94-339">**Ehdot:** *Keräily*</span><span class="sxs-lookup"><span data-stu-id="b6a94-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="b6a94-340">Jos haluat tulostaa rahtikirjan tunnuksen valitse **Liitokset**-välilehdessä **Työrivit**-taulu ja liitä **Lähetykset**-taulu siihen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="b6a94-341">Sulkee kyselyeditorin valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="b6a94-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="b6a94-342">**Tulostimen tekstiasettelu** -pikavälilehdessä on kolme osaa, johon voi kirjoittaa tulostinkoodin: **ylätunnisteosio**, **tekstiosio** ja **alatunnisteosio**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="b6a94-343">Anna **ylätunnisteosion** **Etiketin ylätunniste** -kenttään vaadittavan ylätunnisteen koodi.</span><span class="sxs-lookup"><span data-stu-id="b6a94-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="b6a94-344">Jos käytössä on esimerkiksi Zebra-tulostimet voit käyttää seuraavaa koodia.</span><span class="sxs-lookup"><span data-stu-id="b6a94-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="b6a94-345">Anna **tekstiosion** **Etiketin teksti** -kenttään vaadittavan tekstin ZPL-koodi.</span><span class="sxs-lookup"><span data-stu-id="b6a94-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="b6a94-346">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="b6a94-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="b6a94-347">Anna **tekstiosion** **Etiketin alatunniste** -kenttään vaadittavan alatunnisteen ZPL-koodi.</span><span class="sxs-lookup"><span data-stu-id="b6a94-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="b6a94-348">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="b6a94-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="b6a94-349">Tämä asetus tulostaa yhden kopion kustakin etiketistä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="b6a94-350">Jos kopioita tarvitaan enemmän (esimerkiksi yksi kuormalavan kummallekin puolelle), määritä alatunnisteen **\^PQn**-osan **n**-arvoksi tarvittava määrä kopioita.</span><span class="sxs-lookup"><span data-stu-id="b6a94-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="b6a94-351">Jos kutakin etikettiä halutaan tulostaa neljä kappaletta, käytä määritystä **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="b6a94-352">Etiketti on nyt käyttövalmis.</span><span class="sxs-lookup"><span data-stu-id="b6a94-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="b6a94-353">Aallon etikettimallin luominen</span><span class="sxs-lookup"><span data-stu-id="b6a94-353">Create a wave label template</span></span>

1. <span data-ttu-id="b6a94-354">Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etikettimallit**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="b6a94-355">Lisää aallon tasomalli ja määritä seuraavat arvot ylätunnisteessa:</span><span class="sxs-lookup"><span data-stu-id="b6a94-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="b6a94-356">**Etikettimallin nimi:** *Konttietiketit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="b6a94-357">**Kuvaus:** *Konttietiketit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="b6a94-358">**Aallon vaihekoodi:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="b6a94-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="b6a94-359">**Varasto**: *63*</span><span class="sxs-lookup"><span data-stu-id="b6a94-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="b6a94-360">Lisää **Aallon etikettimallin tiedot** -pikavälilehdessä rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-361">**Etiketin asettelutunnus:** *Kontti*</span><span class="sxs-lookup"><span data-stu-id="b6a94-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="b6a94-362">**Tulostimen nimi:** valitse sopiva ZPL-tulostin.</span><span class="sxs-lookup"><span data-stu-id="b6a94-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="b6a94-363">**Suorita kysely:** *Kyllä* (Tämä asetus on valinnainen, mutta sen käyttöä suositellaan suorituskyvyn optimoinnin vuoksi.)</span><span class="sxs-lookup"><span data-stu-id="b6a94-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="b6a94-364">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="b6a94-365">Valinnainen: Jos asiakaskohtainen etikettirakenne määritetään, asiakastilin etsimistä varten on luotava kysely.</span><span class="sxs-lookup"><span data-stu-id="b6a94-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="b6a94-366">Valitse **Aallon etikettimallin tiedot** -pikavälilehdessä **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="b6a94-367">Lisää sitten kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-368">**Taulukko:** *Lähetykset*</span><span class="sxs-lookup"><span data-stu-id="b6a94-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="b6a94-369">**Johdettu taulu:** *Lähetykset*</span><span class="sxs-lookup"><span data-stu-id="b6a94-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="b6a94-370">**Kenttä:** *Tilin numero*</span><span class="sxs-lookup"><span data-stu-id="b6a94-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="b6a94-371">**Ehdot:** anna soveltuvan asiakastilin numero.</span><span class="sxs-lookup"><span data-stu-id="b6a94-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="b6a94-372">Kun olet valmis, sulje kyselyeditorin valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="b6a94-373">Numerosarjalaajennusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b6a94-373">Configure number sequence extensions</span></span>

<span data-ttu-id="b6a94-374">Numerosarjalaajennuksilla hallitaan tiettyjen numerosarjojen GS1-vaatimustenmukaisuutta.</span><span class="sxs-lookup"><span data-stu-id="b6a94-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="b6a94-375">Tämä määritys on valinnainen nykyisessä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="b6a94-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="b6a94-376">Lisätietoja ja määritysohjeet ovat kohdassa [Numerosarjalaajennusten määrittäminen](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="b6a94-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="b6a94-377">Myyntitilauksen luominen ja sen vapauttaminen varastoon</span><span class="sxs-lookup"><span data-stu-id="b6a94-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="b6a94-378">Valitse **Myynti ja markkinointi \> Myyntitilaus \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="b6a94-379">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-380">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b6a94-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b6a94-381">**Varasto**: *63*</span><span class="sxs-lookup"><span data-stu-id="b6a94-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="b6a94-382">Lisää viisi myyntitilausriviä:</span><span class="sxs-lookup"><span data-stu-id="b6a94-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="b6a94-383">Myyntitilausrivi 1:</span><span class="sxs-lookup"><span data-stu-id="b6a94-383">Sales order line 1:</span></span>

        - <span data-ttu-id="b6a94-384">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b6a94-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="b6a94-385">**Määrä** *10*</span><span class="sxs-lookup"><span data-stu-id="b6a94-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="b6a94-386">Myyntitilausrivi 2:</span><span class="sxs-lookup"><span data-stu-id="b6a94-386">Sales order line 2:</span></span>

        - <span data-ttu-id="b6a94-387">**Nimiketunnus:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="b6a94-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="b6a94-388">**Määrä** *20*</span><span class="sxs-lookup"><span data-stu-id="b6a94-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="b6a94-389">Myyntitilausrivi 3:</span><span class="sxs-lookup"><span data-stu-id="b6a94-389">Sales order line 3:</span></span>

        - <span data-ttu-id="b6a94-390">**Nimiketunnus:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="b6a94-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="b6a94-391">**Määrä** *20*</span><span class="sxs-lookup"><span data-stu-id="b6a94-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="b6a94-392">Myyntitilausrivi 4:</span><span class="sxs-lookup"><span data-stu-id="b6a94-392">Sales order line 4:</span></span>

        - <span data-ttu-id="b6a94-393">**Nimiketunnus:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="b6a94-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="b6a94-394">**Määrä** *40*</span><span class="sxs-lookup"><span data-stu-id="b6a94-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="b6a94-395">Myyntitilausrivi 5:</span><span class="sxs-lookup"><span data-stu-id="b6a94-395">Sales order line 5:</span></span>

        - <span data-ttu-id="b6a94-396">**Nimiketunnus:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="b6a94-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="b6a94-397">**Määrä** *50*</span><span class="sxs-lookup"><span data-stu-id="b6a94-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="b6a94-398">Nämä nimikkeet ja määrät ovat vain esimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="b6a94-399">Niiden on oltava varastossa määritetyssä varastossa.</span><span class="sxs-lookup"><span data-stu-id="b6a94-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="b6a94-400">Valitse tilausrivi 1.</span><span class="sxs-lookup"><span data-stu-id="b6a94-400">Select sales order line 1.</span></span> <span data-ttu-id="b6a94-401">Valitse sitten **Myyntitilausrivi**-osan **Varasto**-valikossa **Varaukset**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="b6a94-402">Valitse **Varaus**-sivun toimintoruudussa **Varaa erä** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="b6a94-403">Toista vaiheet 4 ja 5 kullekin lisätylle myyntitilausriville.</span><span class="sxs-lookup"><span data-stu-id="b6a94-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="b6a94-404">Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b6a94-405">Seuraavat tapahtumat:</span><span class="sxs-lookup"><span data-stu-id="b6a94-405">The following events occur:</span></span>

    - <span data-ttu-id="b6a94-406">Järjestelmä käsittelee luodun lähetyksen käyttämällä etiketin tulostusvaiheen sisältävää mallia.</span><span class="sxs-lookup"><span data-stu-id="b6a94-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="b6a94-407">Etiketin asettelun avulla määritetään etiketin muoto, ja näin saadussa etiketissä on viisi riviä ja se tulostetaan etikettimallissa valitulla tulostimella.</span><span class="sxs-lookup"><span data-stu-id="b6a94-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="b6a94-408">Lähetyksille luodaan uusi rahtikirjan tunnus.</span><span class="sxs-lookup"><span data-stu-id="b6a94-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="b6a94-409">Jos numerosarjalaajennukset määritettiin, aallon etikettitunnus noudattaa **SSCC-18**-lukumuotoilua.</span><span class="sxs-lookup"><span data-stu-id="b6a94-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="b6a94-410">Voit tulostaa nämä aallon etiketit uudelleen valitsemalla **Varastonhallinta \> Kyselyt ja raportit \> Aallon etiketin historia**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="b6a94-411">Skenaario 3: Moneen tasoon luokiteltujen etikettien aallon etikettitulostus</span><span class="sxs-lookup"><span data-stu-id="b6a94-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="b6a94-412">Tässä skenaariossa näytetään, miten aallon etiketin tulostustoimintoa käytetään, kun varastoprosessit edellyttävät moneen tasoon luokiteltuja lähetyksen etikettejä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="b6a94-413">Esimerkiksi pakkauksille ja kuormalavoille on voitava tulostaa eri etiketit, ja koko lähetykselle on voitava tulostaa keskeytysetiketti.</span><span class="sxs-lookup"><span data-stu-id="b6a94-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="b6a94-414">Keskeytysetiketit ovat erillinen etikettityyppi, joita voidaan käyttää rullien ja konttien välissä, kuten lähetystunnuksen etikettien ja viivakoodin välillä. Tällä tavoin etiketit on helppo lajitella tulostuksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="b6a94-415">Suurin ero tämän skenaarion ja skenaarion 1 määrityksissä on keskeytysetikettien käyttöönoton lisäksi se, että useita etikettityyppejä on liitettävä aallon etikettimalleihin ja yksikön sarjaryhmäriveihin.</span><span class="sxs-lookup"><span data-stu-id="b6a94-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="b6a94-416">Tämä määritys tehdään määrittämällä seuraavat elementit tässä skenaariossa:</span><span class="sxs-lookup"><span data-stu-id="b6a94-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="b6a94-417">**Aallon käsittelymenetelmät:** aallon etikettimenetelmän merkitään toistettavaksi, se lisätään vähintään kaksi kertaa aaltomalliin ja erilaiset aallon vaihekoodit määritetään.</span><span class="sxs-lookup"><span data-stu-id="b6a94-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="b6a94-418">**Aallon etikettimallit:** Aallon etikettimallit määritetään ja ne linkitetään aaltomalliin.</span><span class="sxs-lookup"><span data-stu-id="b6a94-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="b6a94-419">Kullakin aallon etikettimallilla on oltava oma aallon etikettityyppi.</span><span class="sxs-lookup"><span data-stu-id="b6a94-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="b6a94-420">**Aallon etiketin asettelut:** Useita aallon etiketin asetteluja luodaan.</span><span class="sxs-lookup"><span data-stu-id="b6a94-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="b6a94-421">Jokaisella etiketin tasolla on erillinen etiketin asettelu, minkä lisäksi keskeytysetiketillä on oma asettelu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="b6a94-422">Tämä skenaario sisältää työnkulun alusta loppuun.</span><span class="sxs-lookup"><span data-stu-id="b6a94-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="b6a94-423">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="b6a94-423">Make demo data available</span></span>

<span data-ttu-id="b6a94-424">Tämän skenaarion käyttäminen edellyttää, että demotiedot on asennettu ja että **USMF**-yritys on valittu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="b6a94-425">Aallon käsittelymenetelmän määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b6a94-425">Set up a wave process method</span></span>

1. <span data-ttu-id="b6a94-426">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon käsittelymenetelmät**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="b6a94-427">Varmista, että **waveLabelPrinting** on luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b6a94-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="b6a94-428">Jos se ei ole luettelossa, lisää se valitsemalla toimintoruudussa **Luo menetelmät uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="b6a94-429">Valitse **waveLabelPrinting**-menetelmässä **Tee menetelmästä toistettava** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="b6a94-430">Aaltomallin asetuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b6a94-430">Set up a wave template</span></span>

1. <span data-ttu-id="b6a94-431">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="b6a94-432">Valitse malli, kuten **62 Lähetyksen oletus**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="b6a94-433">Siirrä **Aallon etiketin tulostus** -menetelmä **Menetelmät**-pikavälilehdessä **Valitut menetelmät** -sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="b6a94-434">Määritä **Valitut menetelmät** -sarakkeessa **Aallon vaihekoodi** -arvo, kuten *Pakkaus*, **Aallon etiketin tulostus** -menetelmään.</span><span class="sxs-lookup"><span data-stu-id="b6a94-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="b6a94-435">Lisätietoja aallon vaihekoodeista on kohdassa [Aallon vaihekoodit](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b6a94-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="b6a94-436">Siirrä **Aallon etiketin tulostus** -menetelmä **Valitut menetelmät** -sarakkeeseen toisen kerran.</span><span class="sxs-lookup"><span data-stu-id="b6a94-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="b6a94-437">Määritä **Valitut menetelmät** -sarakkeessa toinen **Aallon vaihekoodi** -arvo, kuten *Kuormalava*, toiseen **Aallon etiketin tulostus** -menetelmään.</span><span class="sxs-lookup"><span data-stu-id="b6a94-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="b6a94-438">Lisätietoja aallon vaihekoodeista on kohdassa [Aallon vaihekoodit](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b6a94-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="b6a94-439">Kolmen aallon etikettiasettelun luominen</span><span class="sxs-lookup"><span data-stu-id="b6a94-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="b6a94-440">Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etiketin asettelut**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="b6a94-441">Luo tietue, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-442">**Etiketin asettelutunnus:** *Pakkaus*</span><span class="sxs-lookup"><span data-stu-id="b6a94-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="b6a94-443">**Kuvaus:** *Pakkaus (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="b6a94-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="b6a94-444">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="b6a94-445">Valitse toimintoruudussa **Aallon etiketin riviasetukset**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="b6a94-446">**Aallon etiketin riviasetukset** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="b6a94-447">Etiketin dynaaminen osa määritetään tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="b6a94-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="b6a94-448">Lisää rivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-449">**Rivin tunnus:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="b6a94-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="b6a94-450">**Rivin taulukon nimi:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="b6a94-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="b6a94-451">**Rivin lähtökohta:** *0*</span><span class="sxs-lookup"><span data-stu-id="b6a94-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="b6a94-452">Tämä kenttä määrittää pystysuunnassa paikan, josta rivi alkaa etiketissä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="b6a94-453">**Rivin korkeus:** *0*</span><span class="sxs-lookup"><span data-stu-id="b6a94-453">**Row height:** *0*</span></span>

        <span data-ttu-id="b6a94-454">Tämä kenttää määrittää kunkin rivin korkeuden (pisteinä) ZPL-standardin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b6a94-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="b6a94-455">Rivin korkeus on positiivinen vaakasuuntaisissa etiketeissä ja negatiivinen pystysuuntaisissa etiketeissä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="b6a94-456">Koska tässä esimerkissä on vain yksi rivi, arvoksi voidaan määrittää *0* (nolla).</span><span class="sxs-lookup"><span data-stu-id="b6a94-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="b6a94-457">**Riviä sivua kohden:** *1*</span><span class="sxs-lookup"><span data-stu-id="b6a94-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="b6a94-458">Tämä kenttä määrittää, kuinka monta riviä kuhunkin etikettiin tulostetaan.</span><span class="sxs-lookup"><span data-stu-id="b6a94-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b6a94-459">Tämän asetuksen seurauksena kullekin aallon etikettitaulun tietueelle tulostetaan erillinen ZPL-etiketti.</span><span class="sxs-lookup"><span data-stu-id="b6a94-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="b6a94-460">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-460">Close the page.</span></span>
1. <span data-ttu-id="b6a94-461">Valitse toimintoruudussa **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="b6a94-462">Lisää kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-463">**Taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-464">**Johdettu taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-465">**Kenttä:** *Työtyyppi*</span><span class="sxs-lookup"><span data-stu-id="b6a94-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="b6a94-466">**Ehdot:** *Keräily*</span><span class="sxs-lookup"><span data-stu-id="b6a94-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="b6a94-467">Tämä kysely varmistaa, että etikettiin tulostetaan vain keräilytyyppiset työrivit, eikä siis poispanotyyppisiä työrivejä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="b6a94-468">Jos haluat tulostaa rahtikirjan tunnuksen valitse **Liitokset**-välilehdessä **Työrivit**-taulu ja liitä **Lähetykset**-taulu siihen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="b6a94-469">Sulkee kyselyeditorin valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="b6a94-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="b6a94-470">**Tulostimen tekstiasettelu** -pikavälilehdessä on kolme osaa, johon voi kirjoittaa tulostinkoodin: **ylätunnisteosio**, **tekstiosio** ja **alatunnisteosio**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="b6a94-471">Anna **ylätunnisteosion** **Etiketin ylätunniste** -kenttään vaadittavan ylätunnisteen koodi.</span><span class="sxs-lookup"><span data-stu-id="b6a94-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="b6a94-472">Jos käytössä on esimerkiksi Zebra-tulostimet voit käyttää seuraavaa koodia.</span><span class="sxs-lookup"><span data-stu-id="b6a94-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="b6a94-473">Anna **tekstiosion** **Etiketin teksti** -kenttään vaadittavan tekstin ZPL-koodi.</span><span class="sxs-lookup"><span data-stu-id="b6a94-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="b6a94-474">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="b6a94-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="b6a94-475">Anna **tekstiosion** **Etiketin alatunniste** -kenttään vaadittavan alatunnisteen ZPL-koodi.</span><span class="sxs-lookup"><span data-stu-id="b6a94-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="b6a94-476">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="b6a94-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="b6a94-477">Tämä asetus tulostaa yhden kopion kustakin etiketistä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="b6a94-478">Jos kopioita tarvitaan enemmän (esimerkiksi yksi kuormalavan kummallekin puolelle), määritä alatunnisteen **\^PQn**-osan **n**-arvoksi tarvittava määrä kopioita.</span><span class="sxs-lookup"><span data-stu-id="b6a94-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="b6a94-479">Jos kutakin etikettiä halutaan tulostaa neljä kappaletta, käytä määritystä **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="b6a94-480">Ensimmäinen etiketti on nyt käyttövalmis.</span><span class="sxs-lookup"><span data-stu-id="b6a94-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="b6a94-481">Luo toinen asettelutietue, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-482">**Etiketin asettelutunnus:** *Kuormalava*</span><span class="sxs-lookup"><span data-stu-id="b6a94-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="b6a94-483">**Kuvaus:** *Kuormalava*</span><span class="sxs-lookup"><span data-stu-id="b6a94-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="b6a94-484">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="b6a94-485">Valitse toimintoruudussa **Aallon etiketin riviasetukset**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="b6a94-486">**Aallon etiketin riviasetukset** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="b6a94-487">Etiketin dynaaminen osa määritetään tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="b6a94-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="b6a94-488">Lisää rivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-489">**Rivin tunnus:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="b6a94-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="b6a94-490">**Rivin taulukon nimi:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="b6a94-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="b6a94-491">**Rivin lähtökohta:** *0*</span><span class="sxs-lookup"><span data-stu-id="b6a94-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="b6a94-492">Tämä kenttä määrittää pystysuunnassa paikan, josta rivi alkaa etiketissä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="b6a94-493">**Rivin korkeus:** *0*</span><span class="sxs-lookup"><span data-stu-id="b6a94-493">**Row height:** *0*</span></span>

        <span data-ttu-id="b6a94-494">Tämä kenttää määrittää kunkin rivin korkeuden (pisteinä) ZPL-standardin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b6a94-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="b6a94-495">Rivin korkeus on positiivinen vaakasuuntaisissa etiketeissä ja negatiivinen pystysuuntaisissa etiketeissä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="b6a94-496">Koska tässä esimerkissä on vain yksi rivi, arvoksi voidaan määrittää *0* (nolla).</span><span class="sxs-lookup"><span data-stu-id="b6a94-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="b6a94-497">**Riviä sivua kohden:** *1*</span><span class="sxs-lookup"><span data-stu-id="b6a94-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="b6a94-498">Tämä kenttä määrittää, kuinka monta riviä kuhunkin etikettiin tulostetaan.</span><span class="sxs-lookup"><span data-stu-id="b6a94-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b6a94-499">Tällä asetuksella kullekin aallon etikettitaulun tietueelle tulostetaan erillinen ZPL-etiketti.</span><span class="sxs-lookup"><span data-stu-id="b6a94-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="b6a94-500">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-500">Close the page.</span></span>
1. <span data-ttu-id="b6a94-501">Valitse toimintoruudussa **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="b6a94-502">Lisää kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-503">**Taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-504">**Johdettu taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-505">**Kenttä:** *Työtyyppi*</span><span class="sxs-lookup"><span data-stu-id="b6a94-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="b6a94-506">**Ehdot:** *Keräily*</span><span class="sxs-lookup"><span data-stu-id="b6a94-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="b6a94-507">Tämä kysely varmistaa, että etikettiin tulostetaan vain keräilytyyppiset työrivit, eikä siis poispanotyyppisiä työrivejä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="b6a94-508">Jos haluat tulostaa rahtikirjan tunnuksen valitse **Liitokset**-välilehdessä **Työrivit**-taulu ja liitä **Lähetykset**-taulu siihen.</span><span class="sxs-lookup"><span data-stu-id="b6a94-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="b6a94-509">Sulkee kyselyeditorin valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="b6a94-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="b6a94-510">**Tulostimen tekstiasettelu** -pikavälilehdessä on kolme osaa, johon voi kirjoittaa tulostinkoodin: **ylätunnisteosio**, **tekstiosio** ja **alatunnisteosio**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="b6a94-511">Anna **ylätunnisteosion** **Etiketin ylätunniste** -kenttään vaadittavan ylätunnisteen koodi.</span><span class="sxs-lookup"><span data-stu-id="b6a94-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="b6a94-512">Jos käytössä on esimerkiksi Zebra-tulostimet voit käyttää seuraavaa koodia.</span><span class="sxs-lookup"><span data-stu-id="b6a94-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="b6a94-513">Anna **tekstiosion** **Etiketin teksti** -kenttään vaadittavan tekstin ZPL-koodi.</span><span class="sxs-lookup"><span data-stu-id="b6a94-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="b6a94-514">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="b6a94-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="b6a94-515">Anna **tekstiosion** **Etiketin alatunniste** -kenttään vaadittavan alatunnisteen ZPL-koodi.</span><span class="sxs-lookup"><span data-stu-id="b6a94-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="b6a94-516">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="b6a94-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="b6a94-517">Tämä asetus tulostaa yhden kopion kustakin etiketistä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="b6a94-518">Jos kopioita tarvitaan enemmän (esimerkiksi yksi kuormalavan kummallekin puolelle), määritä alatunnisteen **\^PQn**-osan **n**-arvoksi tarvittava määrä kopioita.</span><span class="sxs-lookup"><span data-stu-id="b6a94-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="b6a94-519">Jos kutakin etikettiä halutaan tulostaa neljä kappaletta, käytä määritystä **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="b6a94-520">Toinen etiketti on nyt käyttövalmis.</span><span class="sxs-lookup"><span data-stu-id="b6a94-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="b6a94-521">Luo kolmas asettelutietue, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-522">**Etiketin asettelutunnus:** *Keskeytys*</span><span class="sxs-lookup"><span data-stu-id="b6a94-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="b6a94-523">**Kuvaus:** *Keskeytysetiketti*</span><span class="sxs-lookup"><span data-stu-id="b6a94-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="b6a94-524">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="b6a94-525">**Tulostimen tekstiasettelu** -pikavälilehdessä on kolme osaa, johon voi kirjoittaa tulostinkoodin: **ylätunnisteosio**, **tekstiosio** ja **alatunnisteosio**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="b6a94-526">Anna **ylätunnisteosion** **Etiketin ylätunniste** -kenttään vaadittavan ylätunnisteen ZPL-koodi.</span><span class="sxs-lookup"><span data-stu-id="b6a94-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="b6a94-527">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="b6a94-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="b6a94-528">Tällä kertaa tekstiosaa ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="b6a94-528">This time, no body is required.</span></span> <span data-ttu-id="b6a94-529">Anna tämän vuoksi tarvittava teksti **alatunnisteosiossa**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="b6a94-530">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="b6a94-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="b6a94-531">Kolmas etiketti on nyt käyttövalmis.</span><span class="sxs-lookup"><span data-stu-id="b6a94-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b6a94-532">Tämä kolmas etiketti on keskeytysetiketti, joka erottaa etikettirullat toisistaan.</span><span class="sxs-lookup"><span data-stu-id="b6a94-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="b6a94-533">Kahden aallon etikettityypin luominen</span><span class="sxs-lookup"><span data-stu-id="b6a94-533">Create two wave label types</span></span>

1. <span data-ttu-id="b6a94-534">Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etikettityypit**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="b6a94-535">Luo tietue, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-536">**Etikettityyppi:** *Pakkaus*</span><span class="sxs-lookup"><span data-stu-id="b6a94-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="b6a94-537">**Kuvaus:** *Pakkaus*</span><span class="sxs-lookup"><span data-stu-id="b6a94-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="b6a94-538">Luo toinen tietue, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-539">**Etikettityyppi:** *Kuormalava*</span><span class="sxs-lookup"><span data-stu-id="b6a94-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="b6a94-540">**Kuvaus:** *Kuormalava*</span><span class="sxs-lookup"><span data-stu-id="b6a94-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="b6a94-541">Määritä yksikön sarjaryhmät</span><span class="sxs-lookup"><span data-stu-id="b6a94-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="b6a94-542">Valitse **Varastonhallinta \> Asetukset \> Varasto \> Yksikön sarjaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="b6a94-543">Valitse tai luo **Kpl laatikko KL** -ryhmä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="b6a94-544">Määritä **Laatikko**-rivin **Aallon tasotyyppi** -kentän arvoksi *Pakkaus*.</span><span class="sxs-lookup"><span data-stu-id="b6a94-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="b6a94-545">Määritä **Kuormalava**-rivin **Aallon tasotyyppi** -kentän arvoksi *Kuormalava*.</span><span class="sxs-lookup"><span data-stu-id="b6a94-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="b6a94-546">Aallon etikettimallien luominen</span><span class="sxs-lookup"><span data-stu-id="b6a94-546">Create wave label templates</span></span>

1. <span data-ttu-id="b6a94-547">Valitse **Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etikettimallit**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="b6a94-548">Luo etikettimalli, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-549">**Etikettimallin nimi:** *Pakkausetiketit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="b6a94-550">**Kuvaus:** *Pakkausetiketit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="b6a94-551">**Aallon vaihekoodi:** *Pakkaus*</span><span class="sxs-lookup"><span data-stu-id="b6a94-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="b6a94-552">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="b6a94-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="b6a94-553">Valitse **Yleinen**-pikavälilehden **Aallon etikettityyppi**-kentässä arvo, kuten *Pakkaus*.</span><span class="sxs-lookup"><span data-stu-id="b6a94-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="b6a94-554">Lisää **Aallon etikettimallin tiedot** -pikavälilehdessä rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-555">**Etiketin asettelutunnus:** *Pakkaus*</span><span class="sxs-lookup"><span data-stu-id="b6a94-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="b6a94-556">**Tulostimen nimi:** valitse sopiva ZPL-tulostin.</span><span class="sxs-lookup"><span data-stu-id="b6a94-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="b6a94-557">**Suorita kysely:** *Kyllä* (Tämä asetus on valinnainen, mutta sen käyttöä suositellaan suorituskyvyn optimoinnin vuoksi.)</span><span class="sxs-lookup"><span data-stu-id="b6a94-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="b6a94-558">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="b6a94-559">Valinnainen: Jos asiakaskohtainen etikettirakenne määritetään, asiakastilin etsimistä varten on luotava kysely.</span><span class="sxs-lookup"><span data-stu-id="b6a94-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="b6a94-560">Valitse **Aallon etikettimallin tiedot** -pikavälilehdessä **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="b6a94-561">Lisää sitten kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-562">**Taulukko:** *Lähetykset*</span><span class="sxs-lookup"><span data-stu-id="b6a94-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="b6a94-563">**Johdettu taulu:** *Lähetykset*</span><span class="sxs-lookup"><span data-stu-id="b6a94-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="b6a94-564">**Kenttä:** *Tilin numero*</span><span class="sxs-lookup"><span data-stu-id="b6a94-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="b6a94-565">**Ehdot:** anna soveltuvan asiakastilin numero.</span><span class="sxs-lookup"><span data-stu-id="b6a94-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="b6a94-566">Kun olet valmis, sulje kyselyeditorin valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="b6a94-567">Avaa koko etikettimallin kyselyeditorin valintaikkuna valitsemalla toimintoruudussa **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="b6a94-568">Lisää kyselyeditorin valintaikkunan **Lajittelu**-välilehdessä rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-569">**Taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-570">**Johdettu taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-571">**Kenttä:** *Viittauksen kuormarivin tunnus (tietuetunnus)*</span><span class="sxs-lookup"><span data-stu-id="b6a94-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="b6a94-572">**Hakusuunta:** *Laskeva*</span><span class="sxs-lookup"><span data-stu-id="b6a94-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="b6a94-573">Lisää toinen rivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-574">**Taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-575">**Johdettu taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-576">**Kenttä:** *Lähetyksen tunnus*</span><span class="sxs-lookup"><span data-stu-id="b6a94-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="b6a94-577">**Hakusuunta:** *Laskeva*</span><span class="sxs-lookup"><span data-stu-id="b6a94-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="b6a94-578">Sulje kyselyeditorin valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="b6a94-579">Avautuva sanomaruutu pyytää vahvistamaan ryhmittelyn nollaustoiminnon.</span><span class="sxs-lookup"><span data-stu-id="b6a94-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="b6a94-580">Jatka valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="b6a94-581">Valitse Toimintoruudussa **Aallon etiketin malliryhmä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="b6a94-582">Määritä **Aalloin etiketin malliryhmä** -valintaikkunassa seuraavat arvot sille riville, jonka **Viitekentän nimi** -kentän asetuksena on *Lähetyksen tunnus*:</span><span class="sxs-lookup"><span data-stu-id="b6a94-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="b6a94-583">**Tulosta keskeytysetiketti:** valitse tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="b6a94-584">**Etiketin asettelutunnus:** Valitse keskeytysetiketti.</span><span class="sxs-lookup"><span data-stu-id="b6a94-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="b6a94-585">(Valitse esimerkiksi aiemmin tässä skenaariossa luotu *Keskeytys*-etiketti.)</span><span class="sxs-lookup"><span data-stu-id="b6a94-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="b6a94-586">**Tulostiminen nimi:** Valitse keskeytysetiketin tulostin.</span><span class="sxs-lookup"><span data-stu-id="b6a94-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="b6a94-587">(Yleensä etikettirullien jakamista varten on syytä valita sama tulostin, joka valittiin **Aallon etikettimallin tiedot** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="b6a94-588">Muutkin skenaariot ovat kuitenkin mahdollisia.)</span><span class="sxs-lookup"><span data-stu-id="b6a94-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="b6a94-589">Valitse rivillä, jonka **Viitekentän nimi** -kentän asetuksena on *Viittauksen kuormarivin tunnus*, **Etiketin luontitunnus** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b6a94-590">Tämä asetus luo kullekin kuormariville yhden etikettisarjan (Pakkaus 1/X) koko aallon osalta työn ryhmittelyasetuksesta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="b6a94-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="b6a94-591">Tämä etikettisarja voidaan tulostaa etikettiasetteluun.</span><span class="sxs-lookup"><span data-stu-id="b6a94-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="b6a94-592">Lisäksi eri lähetysten etiketit erotetaan valitulla keskeytysetiketillä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="b6a94-593">Sulje **Aallon etiketin malliryhmä** -valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="b6a94-594">Luo toinen etikettimalli, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-595">**Etikettimallin nimi:** *Kuormalavaetiketit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="b6a94-596">**Kuvaus:** *Kuormalavaetiketit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="b6a94-597">**Aallon vaihekoodi:** *Kuormalava*</span><span class="sxs-lookup"><span data-stu-id="b6a94-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="b6a94-598">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="b6a94-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="b6a94-599">Valitse **Yleinen**-pikavälilehden **Aallon etikettityyppi**-kentässä arvo, kuten *Kuormalava*.</span><span class="sxs-lookup"><span data-stu-id="b6a94-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="b6a94-600">Lisää **Aallon etikettimallin tiedot** -pikavälilehdessä rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-601">**Etiketin asettelutunnus:** *Kuormalava*</span><span class="sxs-lookup"><span data-stu-id="b6a94-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="b6a94-602">**Tulostimen nimi:** valitse sopiva ZPL-tulostin.</span><span class="sxs-lookup"><span data-stu-id="b6a94-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="b6a94-603">**Suorita kysely:** *Kyllä* (Tämä asetus on valinnainen, mutta sen käyttöä suositellaan suorituskyvyn optimoinnin vuoksi.)</span><span class="sxs-lookup"><span data-stu-id="b6a94-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="b6a94-604">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="b6a94-605">Valinnainen: Jos asiakaskohtainen etikettirakenne määritetään, asiakastilin etsimistä varten on luotava kysely.</span><span class="sxs-lookup"><span data-stu-id="b6a94-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="b6a94-606">Valitse **Aallon etikettimallin tiedot** -pikavälilehdessä **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="b6a94-607">Lisää sitten kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-608">**Taulukko:** *Lähetykset*</span><span class="sxs-lookup"><span data-stu-id="b6a94-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="b6a94-609">**Johdettu taulu:** *Lähetykset*</span><span class="sxs-lookup"><span data-stu-id="b6a94-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="b6a94-610">**Kenttä:** *Tilin numero*</span><span class="sxs-lookup"><span data-stu-id="b6a94-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="b6a94-611">**Ehdot:** anna soveltuvan asiakastilin numero.</span><span class="sxs-lookup"><span data-stu-id="b6a94-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="b6a94-612">Kun olet valmis, sulje kyselyeditorin valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="b6a94-613">Avaa koko etikettimallin kyselyeditorin valintaikkuna valitsemalla toimintoruudussa **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="b6a94-614">Lisää kyselyeditorin valintaikkunan **Lajittelu**-välilehdessä rivi, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-615">**Taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-616">**Johdettu taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-617">**Kenttä:** *Viittauksen kuormarivin tunnus (tietuetunnus)*</span><span class="sxs-lookup"><span data-stu-id="b6a94-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="b6a94-618">**Hakusuunta:** *Laskeva*</span><span class="sxs-lookup"><span data-stu-id="b6a94-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="b6a94-619">Lisää toinen rivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-620">**Taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-621">**Johdettu taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="b6a94-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="b6a94-622">**Kenttä:** *Lähetyksen tunnus*</span><span class="sxs-lookup"><span data-stu-id="b6a94-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="b6a94-623">**Hakusuunta:** *Laskeva*</span><span class="sxs-lookup"><span data-stu-id="b6a94-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="b6a94-624">Sulje kyselyeditorin valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="b6a94-625">Avautuva sanomaruutu pyytää vahvistamaan ryhmittelyn nollaustoiminnon.</span><span class="sxs-lookup"><span data-stu-id="b6a94-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="b6a94-626">Jatka valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="b6a94-627">Valitse Toimintoruudussa **Aallon etiketin malliryhmä**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="b6a94-628">Määritä **Aalloin etiketin malliryhmä** -valintaikkunassa seuraavat arvot sille riville, jonka **Viitekentän nimi** -kentän asetuksena on *Lähetyksen tunnus*:</span><span class="sxs-lookup"><span data-stu-id="b6a94-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="b6a94-629">**Tulosta keskeytysetiketti:** valitse tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="b6a94-630">**Etiketin asettelutunnus:** Valitse keskeytysetiketti.</span><span class="sxs-lookup"><span data-stu-id="b6a94-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="b6a94-631">(Valitse esimerkiksi aiemmin tässä skenaariossa luotu *Keskeytys*-etiketti.)</span><span class="sxs-lookup"><span data-stu-id="b6a94-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="b6a94-632">**Tulostiminen nimi:** Valitse keskeytysetiketin tulostin.</span><span class="sxs-lookup"><span data-stu-id="b6a94-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="b6a94-633">(Yleensä etikettirullien jakamista varten on syytä valita sama tulostin, joka valittiin **Aallon etikettimallin tiedot** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="b6a94-634">Muutkin skenaariot ovat kuitenkin mahdollisia.)</span><span class="sxs-lookup"><span data-stu-id="b6a94-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="b6a94-635">Valitse rivillä, jonka **Viitekentän nimi** -kentän asetuksena on *Viittauksen kuormarivin tunnus*, **Etiketin luontitunnus** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b6a94-636">Tämä asetus luo kullekin kuormariville yhden etikettisarjan (Pakkaus 1/X) koko aallon osalta työn ryhmittelyasetuksesta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="b6a94-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="b6a94-637">Tämä etikettisarja voidaan tulostaa etikettiasetteluun.</span><span class="sxs-lookup"><span data-stu-id="b6a94-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="b6a94-638">Lisäksi eri lähetysten etiketit erotetaan valitulla keskeytysetiketillä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="b6a94-639">Numerosarjalaajennusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b6a94-639">Configure number sequence extensions</span></span>

<span data-ttu-id="b6a94-640">Numerosarjalaajennuksilla hallitaan tiettyjen numerosarjojen GS1-vaatimustenmukaisuutta.</span><span class="sxs-lookup"><span data-stu-id="b6a94-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="b6a94-641">Tämä määritys on valinnainen nykyisessä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="b6a94-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="b6a94-642">Lisätietoja ja määritysohjeet ovat kohdassa [Numerosarjalaajennusten määrittäminen](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="b6a94-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="b6a94-643">Myyntitilauksen luominen ja sen vapauttaminen varastoon</span><span class="sxs-lookup"><span data-stu-id="b6a94-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="b6a94-644">Valitse **Myynti ja markkinointi \> Myyntitilaus \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="b6a94-645">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="b6a94-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b6a94-646">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b6a94-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b6a94-647">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="b6a94-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="b6a94-648">Lisää kaksi myyntitilausriviä:</span><span class="sxs-lookup"><span data-stu-id="b6a94-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="b6a94-649">Myyntitilausrivi 1:</span><span class="sxs-lookup"><span data-stu-id="b6a94-649">Sales order line 1:</span></span>

        - <span data-ttu-id="b6a94-650">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b6a94-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="b6a94-651">**Määrä** *9024*</span><span class="sxs-lookup"><span data-stu-id="b6a94-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="b6a94-652">**Yksikkö:** *kpl* (9024 kpl = 376 laatikkoa = 47 kuormalavaa)</span><span class="sxs-lookup"><span data-stu-id="b6a94-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="b6a94-653">Myyntitilausrivi 2:</span><span class="sxs-lookup"><span data-stu-id="b6a94-653">Sales order line 2:</span></span>

        - <span data-ttu-id="b6a94-654">**Nimiketunnus:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="b6a94-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="b6a94-655">**Määrä** *9016*</span><span class="sxs-lookup"><span data-stu-id="b6a94-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="b6a94-656">**Yksikkö:** *kpl* (9016 kpl = 322 laatikkoa = 46 kuormalavaa)</span><span class="sxs-lookup"><span data-stu-id="b6a94-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="b6a94-657">Nämä nimikkeet ja määrät ovat vain esimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="b6a94-658">Niiden on käytettävä aiemmin määritettyä yksikön sarjaryhmää, niille on määritettävä soveltuva yksikkömuunnos *kappaleesta* *laatikkoon* ja edelleen *kuormalavaksi* ja niiden varaston on oltava varastossa *62*.</span><span class="sxs-lookup"><span data-stu-id="b6a94-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="b6a94-659">Lisätietoja on kohdassa [Mittayksikkö ja varastointikäytännöt](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b6a94-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="b6a94-660">Valitse tilausrivi 1.</span><span class="sxs-lookup"><span data-stu-id="b6a94-660">Select sales order line 1.</span></span> <span data-ttu-id="b6a94-661">Valitse sitten **Myyntitilausrivi**-osan **Varasto**-valikossa **Varaukset**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="b6a94-662">Valitse **Varaus**-sivun toimintoruudussa **Varaa erä** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="b6a94-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="b6a94-663">Toista vaiheet 4 ja 5 myyntitilausriville 2.</span><span class="sxs-lookup"><span data-stu-id="b6a94-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="b6a94-664">Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="b6a94-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b6a94-665">Seuraavat tapahtumat:</span><span class="sxs-lookup"><span data-stu-id="b6a94-665">The following events occur:</span></span> 

    - <span data-ttu-id="b6a94-666">Järjestelmä käsittelee luodun lähetyksen käyttämällä etiketin tulostusvaiheen sisältävää mallia.</span><span class="sxs-lookup"><span data-stu-id="b6a94-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="b6a94-667">Etiketin asettelun avulla määritetään etiketin muoto, ja näin saatu etiketti tulostetaan etikettimallissa valitulla tulostimella.</span><span class="sxs-lookup"><span data-stu-id="b6a94-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="b6a94-668">Aallon etiketit luodaan ja tulostetaan.</span><span class="sxs-lookup"><span data-stu-id="b6a94-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="b6a94-669">Etikettien määrä on sama kuin pakkausten määrä. (Tässä esimerkissä rivillä 1 on 376 laatikkoetikettiä ja rivillä 2 on 322 laatikkoetikettiä; rivillä 1 on 47 kuormalavaetikettiä ja rivillä 2 on 47 kuormalavaetikettiä, minkä lisäksi kahdessa keskeytysetiketissä on lähetyksen tunnus.)</span><span class="sxs-lookup"><span data-stu-id="b6a94-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="b6a94-670">Lähetyksille luodaan uusi rahtikirjan tunnus.</span><span class="sxs-lookup"><span data-stu-id="b6a94-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="b6a94-671">Jos numerosarjalaajennukset määritettiin, aallon etikettitunnus noudattaa **SSCC-18**-lukumuotoilua.</span><span class="sxs-lookup"><span data-stu-id="b6a94-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="b6a94-672">Voit tarkastella aallon etikettejä ja tulostaa niitä uudelleen seuraavilta sivuilta:</span><span class="sxs-lookup"><span data-stu-id="b6a94-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="b6a94-673">Kaikki lähetykset \> Lähetyksen tiedot</span><span class="sxs-lookup"><span data-stu-id="b6a94-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="b6a94-674">Kaikki kuormat \> Kuorman tiedot</span><span class="sxs-lookup"><span data-stu-id="b6a94-674">All loads \> Load details</span></span>
- <span data-ttu-id="b6a94-675">Kaikki aallot</span><span class="sxs-lookup"><span data-stu-id="b6a94-675">All waves</span></span>
- <span data-ttu-id="b6a94-676">Aalto-otsikot</span><span class="sxs-lookup"><span data-stu-id="b6a94-676">Wave labels</span></span>
- <span data-ttu-id="b6a94-677">Aallon etikettihistoria</span><span class="sxs-lookup"><span data-stu-id="b6a94-677">Wave label history</span></span>

<span data-ttu-id="b6a94-678">Useimmilla näistä sivuista sopiva toiminto löytyy valitsemalla **Aallon etiketit** toimintoruudun **Lähetykset**-välilehden **Liittyvät tiedot** -ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="b6a94-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]