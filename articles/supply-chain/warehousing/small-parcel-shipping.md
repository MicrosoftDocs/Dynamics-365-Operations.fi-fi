---
title: Pienten pakettien lähettäminen
description: Tässä aiheessa on tietoja pienten pakettien lähetystoiminnosta. Tämän toiminnon avulla Microsoft Dynamics 365 Supply Chain Management voi lähettää tietoja pakatusta kontista rahdinkuljettajalle sekä saada kyseiseltä rahdinkuljettajalta osoitetarran, lähetyshinnan ja seurantanumeron.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3969ee6b46f38fe2650881fb0183c60aadce6c8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831167"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="e7e55-104">Pienten pakettien lähettäminen</span><span class="sxs-lookup"><span data-stu-id="e7e55-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7e55-105">Pienten pakettien lähetystoiminnon avulla Microsoft Dynamics 365 Supply Chain Management voi olla suoraan yhteydessä rahdinkuljettajaan muodostamalla viestintäkehyksen rahdinkuljettajan ohjelmointirajapintojen kautta.</span><span class="sxs-lookup"><span data-stu-id="e7e55-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="e7e55-106">Tämä toiminto on kätevä, kun yksittäisiä myyntitilauksia lähetetään kaupallisten rahdinkuljettajien kanssa sen sijaan, että käytettäisiin konttitoimitusta tai kuorma-auton osakuormatoimitusta (LTL).</span><span class="sxs-lookup"><span data-stu-id="e7e55-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="e7e55-107">Pienten pakettien lähetystoiminto on yhteydessä rahdinkuljettajaan käyttämällä *hinnan laskentamoduulia*.</span><span class="sxs-lookup"><span data-stu-id="e7e55-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="e7e55-108">Organisaation on kehitettävä tämä hinnanlaskentamoduuli yhdessä rahdinkuljettajan tai rahdinkuljettajakeskuspalvelun kanssa.</span><span class="sxs-lookup"><span data-stu-id="e7e55-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="e7e55-109">Hinnan laskentamoduulin avulla Supply Chain Management voi lähettää tietoja pakatusta kontista rahdinkuljettajalle sekä saada kyseiseltä rahdinkuljettajalta osoitetarran, lähetyshinnan ja seurantanumeron.</span><span class="sxs-lookup"><span data-stu-id="e7e55-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="e7e55-110">Palautettu lähetyshinta lisätään lähetykseen liittyvään myyntitilaukseen muuna kuluna.</span><span class="sxs-lookup"><span data-stu-id="e7e55-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="e7e55-111">Palautettu osoitetarra voidaan sitten tulostaa automaattisesti käyttämällä ZPL (Zebra-ohjelmointikieli) -tulostimella ja kiinnittää toimitukseen.</span><span class="sxs-lookup"><span data-stu-id="e7e55-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="e7e55-112">Rahdinkuljettaja skannaa sitten tämän osoitetarran, kun se noutaa paketit varastosta.</span><span class="sxs-lookup"><span data-stu-id="e7e55-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="e7e55-113">Järjestelmän valmisteleminen tukemaan pienten pakettien lähetystoimintoa</span><span class="sxs-lookup"><span data-stu-id="e7e55-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="e7e55-114">Ennen pienten pakettien lähetystoiminnon käytön aloittamista se on otettava käyttöön ominaisuuksien hallinnassa, hinnan laskentamoduuli on lisättävä sekä **Kuljetuksenhallinta**- ja **Varastonhallinta**-moduulit on määritettävä tukemaan toimintoja.</span><span class="sxs-lookup"><span data-stu-id="e7e55-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="e7e55-115">Pienten pakettien lähetystoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e7e55-115">Turn on the SPS feature</span></span>

<span data-ttu-id="e7e55-116">Ennen kuin pienten pakettien lähetystoimintotoa voidaan käyttää, se on otettava käyttöön järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="e7e55-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="e7e55-117">Järjestelmänvalvojat voivat tarkistaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa toiminnon tilan ja ottaa sen tarvittaessa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e7e55-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="e7e55-118">Tässä tapauksessa toiminto näkyy seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="e7e55-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e7e55-119">**Moduuli:** *Kuljetustenhallinta*</span><span class="sxs-lookup"><span data-stu-id="e7e55-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="e7e55-120">**Toiminnon nimi:** *Pienten pakettien lähetys*</span><span class="sxs-lookup"><span data-stu-id="e7e55-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="e7e55-121">Hinnan laskentamoduulinen ottaminen käyttöön ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e7e55-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="e7e55-122">Supply Chain Management ei sisällä yhtään hinnan laskentamoduulia.</span><span class="sxs-lookup"><span data-stu-id="e7e55-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="e7e55-123">Tarvittavat hinnan laskentamoduulin on hankittava tai luotava, minkä jälkeen ne on lisättävä järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="e7e55-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="e7e55-124">Microsoftilla on kuitenkin hinnan laskennan esittelymoduuli, jota voi käyttää testaukseen.</span><span class="sxs-lookup"><span data-stu-id="e7e55-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="e7e55-125">Hinnan laskennan esittelymoduulin lataaminen ja ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e7e55-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="e7e55-126">Hinnan laskennan esittelymoduuli haetaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e7e55-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="e7e55-127">Lataa GitHubissa [hinnan laskennan DLL (dynamic-link library) -kirjasto](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span><span class="sxs-lookup"><span data-stu-id="e7e55-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="e7e55-128">Tallenna DLL-kirjasto Supply Chain Management -palvelimessa kansioon **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="e7e55-129">Toiminnallisten hinnan laskentamoduulien luominen ja ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e7e55-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="e7e55-130">Lisätietoja toiminnallisten tuotanto- tai testiympäristössä käytettävien hinnan laskentamoduulien luomisesta ja ottamisesta käyttöön on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="e7e55-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="e7e55-131">Uuden kuljetuksenhallintamoduulin luominen</span><span class="sxs-lookup"><span data-stu-id="e7e55-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="e7e55-132">Kuljetustenhallintamoduulien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e7e55-132">Set up transportation management engines</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="e7e55-133">Lisätietoja pienten pakettien lähetyksen hinnan laskentamoduulin luomisesta on seuraavassa blogikirjoituksessa: [Pienten pakettien lähettäminen: pienten pakettien lähetystoiminnon hyödyntäminen Microsoft Dynamics 365:ssä](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span><span class="sxs-lookup"><span data-stu-id="e7e55-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="e7e55-134">Hinnan laskentamoduulin määrittäminen Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="e7e55-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="e7e55-135">Kun pienten pakettien hinnan laskentamoduuli on luotu ja otettu käyttöön, se määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e7e55-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="e7e55-136">Valitse **Kuljetustenhallinta \> Asetukset \> Moduulit \> Hinnan laskenta**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="e7e55-137">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="e7e55-138">Määritä uudella rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="e7e55-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="e7e55-139">**Hinnoittelumoduuli** – Anna hinnan laskentamoduulille yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="e7e55-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="e7e55-140">Jos käytössä on hinnan laskennan esittelymoduuli, anna nimeksi *Hinnan laskennan esittelymoduuli*.</span><span class="sxs-lookup"><span data-stu-id="e7e55-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="e7e55-141">**Nimi** – Anna lyhyt hinnan laskentamoduulin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="e7e55-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="e7e55-142">Jos käytössä on hinnan laskennan esittelymoduuli, anna nimeksi *Hinnan laskennan esittelymoduuli*.</span><span class="sxs-lookup"><span data-stu-id="e7e55-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="e7e55-143">**Luokituksen metatietojen tunnus** – Valitse hinnan laskentaperuste.</span><span class="sxs-lookup"><span data-stu-id="e7e55-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="e7e55-144">Hinta voidaan laskea esimerkiksi etäisyyden perusteella.</span><span class="sxs-lookup"><span data-stu-id="e7e55-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="e7e55-145">Jos käytössä on hinnan laskennan esittelymoduuli, tämän kentän voi jättää tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="e7e55-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="e7e55-146">**Laskennan kokoonpano** – Anna käyttöönotetun DLL-paketin tiedostonimi.</span><span class="sxs-lookup"><span data-stu-id="e7e55-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="e7e55-147">Jos käytössä on hinnan laskennan esittelymoduuli, anna nimeksi *TMSSmallParcelShippingEngine.dll*.</span><span class="sxs-lookup"><span data-stu-id="e7e55-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="e7e55-148">**Moduulin luokka** – Anna hinnan laskentamoduulille muodostetun luokan nimi.</span><span class="sxs-lookup"><span data-stu-id="e7e55-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="e7e55-149">Jos käytössä on hinnan laskennan esittelymoduuli, anna nimeksi *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span><span class="sxs-lookup"><span data-stu-id="e7e55-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="e7e55-150">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="e7e55-150">Example scenario</span></span>

<span data-ttu-id="e7e55-151">Tässä esimerkkiskenaariossa näytetään, miten pienten pakettien lähetystoiminto määritetään ja miten sitä käytetään sen jälkeen, kun järjestelmä on valmisteltu aiemmin tässä aiheessa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="e7e55-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="e7e55-152">Tässä skenaariossa käytetään edellä mainittua hinnan laskennan esittelymoduulia.</span><span class="sxs-lookup"><span data-stu-id="e7e55-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="e7e55-153">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e7e55-153">Make demo data available</span></span>

<span data-ttu-id="e7e55-154">Tämän skenaarion käyttäminen tässä määritettyjen esittelytietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakiomuotoiset [esittelytiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu.</span><span class="sxs-lookup"><span data-stu-id="e7e55-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="e7e55-155">Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.</span><span class="sxs-lookup"><span data-stu-id="e7e55-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="e7e55-156">Määritä skenaario</span><span class="sxs-lookup"><span data-stu-id="e7e55-156">Set up the scenario</span></span>

<span data-ttu-id="e7e55-157">Tässä esimerkkiskenaariossa tarvitaan esittelyrahdinkuljettaja, rahdinkuljettajaryhmä, pakkauskäytäntö ja pakkausprofiili.</span><span class="sxs-lookup"><span data-stu-id="e7e55-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="e7e55-158">Seuraavissa alakohdissa käsitellään skenaariossa tarvittavien tietueiden valmistelua.</span><span class="sxs-lookup"><span data-stu-id="e7e55-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="e7e55-159">Tuotantoskenaarion määritysprosessi muistuttaa yleensä tässä kuvattua prosessia.</span><span class="sxs-lookup"><span data-stu-id="e7e55-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="e7e55-160">Määritettävät arvot ovat kuitenkin erilaisia.</span><span class="sxs-lookup"><span data-stu-id="e7e55-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="e7e55-161">Rahdinkuljettajien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e7e55-161">Set up carriers</span></span>

<span data-ttu-id="e7e55-162">Rahdinkuljettaja määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e7e55-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="e7e55-163">Valitse **Kuljetustenhallinta \> Asetukset \> Rahdinkuljettajat \> Lähetyksen rahdinkuljettajat**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="e7e55-164">Lisää rahdinkuljettaja valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="e7e55-165">Määritä otsikossa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e7e55-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="e7e55-166">**Rahdinkuljettaja:** *Esittelyn rahdinkuljettaja*</span><span class="sxs-lookup"><span data-stu-id="e7e55-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e7e55-167">**Nimi:** *Esittelyn rahdinkuljettaja*</span><span class="sxs-lookup"><span data-stu-id="e7e55-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e7e55-168">**Tila:** *Maa*</span><span class="sxs-lookup"><span data-stu-id="e7e55-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="e7e55-169">Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e7e55-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e7e55-170">**Aktivoi lähetyksen rahdinkuljettaja:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="e7e55-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="e7e55-171">**Aktivoi rahdinkuljettajan luokitus:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="e7e55-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="e7e55-172">Lisää palvelu ruudukkoon valitsemalla **Palvelut**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="e7e55-173">Määritä uuden palvelun seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e7e55-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="e7e55-174">**Rahdinkuljetuspalvelu:** *Esittelyn rahdinkuljetuspalvelu*</span><span class="sxs-lookup"><span data-stu-id="e7e55-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e7e55-175">**Nimi:** *Esittelyn rahdinkuljetuspalvelu*</span><span class="sxs-lookup"><span data-stu-id="e7e55-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e7e55-176">**Kuljetusmenetelmä:** *Maa*</span><span class="sxs-lookup"><span data-stu-id="e7e55-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="e7e55-177">Anna tarvittaessa kaikkiin muihin kenttiin jokin arvo.</span><span class="sxs-lookup"><span data-stu-id="e7e55-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="e7e55-178">(Kun uusi rahdinkuljettajatietue tallennetaan, uusi toimitustapa luodaan ja **Toimitustapa**-kenttä määritetään automaattisesti.)</span><span class="sxs-lookup"><span data-stu-id="e7e55-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="e7e55-179">Lisää hinnoitteluprofiili ruudukkoon **Hinnoitteluprofiilit**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="e7e55-180">Määritä uuden profiilin seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e7e55-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="e7e55-181">**Hinnoitteluprofiili:** *Esittelyn rahdinkuljetuspalvelu*</span><span class="sxs-lookup"><span data-stu-id="e7e55-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e7e55-182">**Nimi:** *Esittelyn rahdinkuljetuspalvelu*</span><span class="sxs-lookup"><span data-stu-id="e7e55-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e7e55-183">**Hinnan laskenta:** *Hinnan laskennan esittelymoduuli*</span><span class="sxs-lookup"><span data-stu-id="e7e55-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="e7e55-184">Anna tarvittaessa kaikkiin muihin kenttiin jokin arvo.</span><span class="sxs-lookup"><span data-stu-id="e7e55-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="e7e55-185">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="e7e55-186">Lisätietoja rahdinkuljettajien määrittämisestä on kohdassa [Rahdinkuljettajien määrittäminen](../transportation/tasks/set-up-shipping-carriers.md).</span><span class="sxs-lookup"><span data-stu-id="e7e55-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="e7e55-187">Rahdinkuljetuspalvelutilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e7e55-187">Set up carrier service accounts</span></span>

<span data-ttu-id="e7e55-188">Rahdinkuljetuspalvelutili määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e7e55-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="e7e55-189">Valitse **Kuljetustenhallinta \> Asetukset \> Hinnoittelu \> Rahdinkuljetuspalvelutili**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="e7e55-190">Lisää rahdinkuljetuspalvelutili valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="e7e55-191">Määritä uuden tilin seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e7e55-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="e7e55-192">**Rahdinkuljettaja:** *Esittelyn rahdinkuljettaja*</span><span class="sxs-lookup"><span data-stu-id="e7e55-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e7e55-193">**Rahdinkuljetuspalvelu:** *Esittelyn rahdinkuljetuspalvelu*</span><span class="sxs-lookup"><span data-stu-id="e7e55-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e7e55-194">**Rahdinkuljettajan asiakastilin numero:** Rahdinkuljettajan asiakastilin numero, jolla yhteys rahdinkuljettajaan vahvistetaan ja todennetaan.</span><span class="sxs-lookup"><span data-stu-id="e7e55-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="e7e55-195">Rahdinkuljettaja ilmoittaa tämän arvon.</span><span class="sxs-lookup"><span data-stu-id="e7e55-195">Your carrier will provide this value.</span></span> <span data-ttu-id="e7e55-196">Jos käytössä on esittelypalvelu, arvo voi olla mikä tahansa.</span><span class="sxs-lookup"><span data-stu-id="e7e55-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="e7e55-197">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="e7e55-197">**Site:** *6*</span></span>
    - <span data-ttu-id="e7e55-198">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="e7e55-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7e55-199">**Rahdinkuljettajan asiakastilin numero** -arvo on usein ainoa arvo, joka tarvitaan yhteyden todentamiseen.</span><span class="sxs-lookup"><span data-stu-id="e7e55-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="e7e55-200">Jos rahdinkuljettaja kuitenkin edellyttää lisätodennusparametreja, organisaation on mukautettava tätä sivua lisäämällä tarvittavat lisäkenttiä.</span><span class="sxs-lookup"><span data-stu-id="e7e55-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="e7e55-201">Kontin pakkauskäytännön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e7e55-201">Set up a container packing policy</span></span>

<span data-ttu-id="e7e55-202">Kontin pakkauskäytäntö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e7e55-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="e7e55-203">Jos ZPL-tulostinmääritystä ei ole vielä tehty, määritä se asiakirjan reititysagenttisovelluksella.</span><span class="sxs-lookup"><span data-stu-id="e7e55-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="e7e55-204">Lisätietoja on kohdassa [Asiakirjojen tulostamisen yleiskatsaus](../../fin-ops-core/dev-itpro/analytics/print-documents.md) ja siihen liittyvissä aiheissa.</span><span class="sxs-lookup"><span data-stu-id="e7e55-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="e7e55-205">Valitse **Varastonhallinta \> Asetukset \> Kontit \> Kontin pakkauskäytännöt**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="e7e55-206">Lisää kontin pakkauskäytäntö valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="e7e55-207">Määritä uuden käytännön otsikossa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e7e55-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="e7e55-208">**Kontin pakkauskäytäntö:** *Esittelyn pakkauskäytäntö*</span><span class="sxs-lookup"><span data-stu-id="e7e55-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="e7e55-209">**Kuvaus:** käytännön kuvaus</span><span class="sxs-lookup"><span data-stu-id="e7e55-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="e7e55-210">Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e7e55-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e7e55-211">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="e7e55-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="e7e55-212">**Lopullisen lähetyksen oletussijainti:** *Lastauspaikan ovi*</span><span class="sxs-lookup"><span data-stu-id="e7e55-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="e7e55-213">**Painoyksikkö:** *KG*</span><span class="sxs-lookup"><span data-stu-id="e7e55-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="e7e55-214">**Kontin sulkemiskäytäntö:** *Automaattinen vapautus*</span><span class="sxs-lookup"><span data-stu-id="e7e55-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="e7e55-215">**Kontin vapautuskäytäntö:** *Tee saatavaksi lopullisessa lähetyssijainnissa*</span><span class="sxs-lookup"><span data-stu-id="e7e55-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="e7e55-216">Määritä seuraavat arvot **Kontin lastiluettelo** -pikavälilehdessä:</span><span class="sxs-lookup"><span data-stu-id="e7e55-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e7e55-217">**Automaattinen lastiluettelo konttia suljettaessa:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="e7e55-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="e7e55-218">**Kontin lastiluettelon vaatimukset:** *Kuljetustenhallinta*</span><span class="sxs-lookup"><span data-stu-id="e7e55-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="e7e55-219">**Tulosta kontin sisältö:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="e7e55-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="e7e55-220">Määritä seuraavat arvot **Rahdinkuljettajan etiketin tulostus** -pikavälilehdessä:</span><span class="sxs-lookup"><span data-stu-id="e7e55-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e7e55-221">**Tulosta kontin osoitetarra:** *Aina*</span><span class="sxs-lookup"><span data-stu-id="e7e55-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="e7e55-222">**Tulostimen nimi:** osoitetarrat tulostavan ZPL-tulostimen nimi.</span><span class="sxs-lookup"><span data-stu-id="e7e55-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="e7e55-223">Pakkausprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e7e55-223">Set up a packing profile</span></span>

<span data-ttu-id="e7e55-224">Määritä pakkausprofiili seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e7e55-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="e7e55-225">Valitse **Varastonhallinta \> Asetukset \> Pakkaus \> Pakkausprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="e7e55-226">Lisää pakkausprofiili ruudukkoon valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="e7e55-227">Määritä uuden profiilin seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e7e55-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="e7e55-228">**Pakkausprofiilin tunnus:** *Esittely pakkausprofiili*</span><span class="sxs-lookup"><span data-stu-id="e7e55-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="e7e55-229">**Kuvaus:** profiilin kuvaus</span><span class="sxs-lookup"><span data-stu-id="e7e55-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="e7e55-230">**Kontin pakkauskäytäntö:** *Esittelyn pakkauskäytäntö*</span><span class="sxs-lookup"><span data-stu-id="e7e55-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="e7e55-231">**Konttitunnuksen tila:** *Automaattinen*</span><span class="sxs-lookup"><span data-stu-id="e7e55-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="e7e55-232">**Kontin tyyppi:** *Pieni pakkaus*</span><span class="sxs-lookup"><span data-stu-id="e7e55-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="e7e55-233">Asiakkaan määrittäminen käyttämään pienten pakettien lähetyksen rahdinkuljettajaa</span><span class="sxs-lookup"><span data-stu-id="e7e55-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="e7e55-234">Määritä asiakas käyttämään luotua rahdinkuljettajaa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e7e55-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="e7e55-235">Valitse **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="e7e55-236">Etsi ja valitse ruudukossa asiakas *US-027*.</span><span class="sxs-lookup"><span data-stu-id="e7e55-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="e7e55-237">Valitse toimintoruudun **Yleiset**-välilehden **Asetukset**-ryhmässä **Rahdinkuljettajan asiakastilit**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="e7e55-238">Lisää tili ruudukkoon valitsemalla **Rahdinkuljettajan asiakastilit** -sivun toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="e7e55-239">Määritä uuden tilin seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e7e55-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="e7e55-240">**Rahdinkuljettaja:** *Esittelyn rahdinkuljettaja*</span><span class="sxs-lookup"><span data-stu-id="e7e55-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e7e55-241">**Rahdinkuljettajan asiakastilin numero:** *12345* (Arvolla ei ole sinänsä merkitystä tässä skenaariossa, mutta siihen viitataan seuraavassa osassa.)</span><span class="sxs-lookup"><span data-stu-id="e7e55-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="e7e55-242">Esimerkkiskenaarion suorittaminen</span><span class="sxs-lookup"><span data-stu-id="e7e55-242">Go through the example scenario</span></span>

<span data-ttu-id="e7e55-243">Kun kaikki näytetiedot on määritetty edellisessä osassa kuvatulla tavalla, esimerkkiskenaario voidaan suorittaa.</span><span class="sxs-lookup"><span data-stu-id="e7e55-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="e7e55-244">Myyntitilauksen luominen ja työn käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="e7e55-244">Create a sales order and process the work</span></span>

<span data-ttu-id="e7e55-245">Luo myyntitilaus seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e7e55-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="e7e55-246">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e7e55-247">Luo uusi myyntitilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="e7e55-248">Määritä **Luo myyntitilaus** -valintaikkunan **Asiakastili**-kentän arvoksi *US-027*.</span><span class="sxs-lookup"><span data-stu-id="e7e55-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="e7e55-249">Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="e7e55-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="e7e55-250">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="e7e55-250">The new sales order is opened.</span></span> <span data-ttu-id="e7e55-251">Määritä **Myyntitilauksen otsikko** -pikavälilehden **Rahdinkuljettajan asiakastilin numero** -kentän arvoksi asiakkaalle aiemmin valittu arvo (*12345*).</span><span class="sxs-lookup"><span data-stu-id="e7e55-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="e7e55-252">Lisää **Myyntitilausrivit**-osassa myyntirivi ja määritä sille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e7e55-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="e7e55-253">**Nimiketunnus:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e7e55-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="e7e55-254">**Määrä** *1*</span><span class="sxs-lookup"><span data-stu-id="e7e55-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="e7e55-255">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="e7e55-255">**Site:** *6*</span></span>
    - <span data-ttu-id="e7e55-256">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="e7e55-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e7e55-257">Vaihda **Otsikko**-näkymään.</span><span class="sxs-lookup"><span data-stu-id="e7e55-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="e7e55-258">Määritä **Toimitus**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e7e55-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e7e55-259">**Rahdinkuljettaja:** *Esittelyn rahdinkuljettaja*</span><span class="sxs-lookup"><span data-stu-id="e7e55-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e7e55-260">**Rahdinkuljetuspalvelu:** *Esittelyn rahdinkuljetuspalvelu*</span><span class="sxs-lookup"><span data-stu-id="e7e55-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="e7e55-261">Siirry takaisin **Rivit**-näkymään.</span><span class="sxs-lookup"><span data-stu-id="e7e55-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="e7e55-262">Jos myyntirivin toimitustapa pyydetään päivittämään, valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="e7e55-263">Valitse **Myyntitilausrivit**-osassa aiemmin määritetty myyntirivi ja valitse sitten **Varasto \> Varaus**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="e7e55-264">Valitse **Varaus**-sivulla **Varaa erä**, jos haluat varata koko valitun rivin määrän varastosta.</span><span class="sxs-lookup"><span data-stu-id="e7e55-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="e7e55-265">Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.</span><span class="sxs-lookup"><span data-stu-id="e7e55-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="e7e55-266">Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="e7e55-267">Työ luodaan siirtämään nimikkeet keräilysijainnista pakkausasemalle.</span><span class="sxs-lookup"><span data-stu-id="e7e55-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="e7e55-268">Valitse **Myyntitilausrivi**-osassa **Varasto \> Lähetyksen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="e7e55-269">Kirjoita **Lähetyksen tiedot** -sivulla oleva lähetyksen tunnus muistiin.</span><span class="sxs-lookup"><span data-stu-id="e7e55-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="e7e55-270">Tunnusta tarvitaan, kun lähetys pakataan pakkausasemalla.</span><span class="sxs-lookup"><span data-stu-id="e7e55-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="e7e55-271">Palaa myyntitilaukseen sulkemalla **Lähetyksen tiedot**-sivu.</span><span class="sxs-lookup"><span data-stu-id="e7e55-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="e7e55-272">Kirjoita myyntitilauksen numero muistiin ja valitse **Varastonhallinta \> Työ \> Kaikki työt**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="e7e55-273">Etsi ja valitse myyntitilauksen numerolla tilaukselle luotu työ.</span><span class="sxs-lookup"><span data-stu-id="e7e55-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="e7e55-274">Valitse toimintoruudun **Työ**-välilehdessä **Valmistunut työ**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="e7e55-275">Valitse käyttäjätunnus **Valmistunut työ** -sivun **Käyttäjätunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e7e55-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="e7e55-276">Valitse sitten toimintoruudussa **Tarkista työ**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="e7e55-277">Jos työ läpäisee tarkistuksen, valitse toimintoruudussa **Valmistunut työ**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="e7e55-278">Työ merkitään valmiiksi, mikä simuloi nimikkeiden siirtymistä pakkausasemalle.</span><span class="sxs-lookup"><span data-stu-id="e7e55-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="e7e55-279">Lähetyksen pakkaaminen</span><span class="sxs-lookup"><span data-stu-id="e7e55-279">Pack the shipment</span></span>

<span data-ttu-id="e7e55-280">Pakkaa lähetys seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e7e55-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="e7e55-281">Valitse **Varastonhallinta \> Asetukset \> Työntekijä** ja varmista, että käyttäjätili on liitetty varastonhallinnan työntekijätiliin.</span><span class="sxs-lookup"><span data-stu-id="e7e55-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="e7e55-282">Valitse **Varastoinhallinta \> Keräily ja konttiinpakkaus \> Pakkaus**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="e7e55-283">Määritä seuraavat arvot **Valitse pakkausasema** -valintaikkunassa:</span><span class="sxs-lookup"><span data-stu-id="e7e55-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e7e55-284">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="e7e55-284">**Site:** *6*</span></span>
    - <span data-ttu-id="e7e55-285">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="e7e55-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="e7e55-286">**Sijainti:** *Pakkaus*</span><span class="sxs-lookup"><span data-stu-id="e7e55-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="e7e55-287">**Pakkausprofiilin tunnus:** *Esittely pakkausprofiili*</span><span class="sxs-lookup"><span data-stu-id="e7e55-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="e7e55-288">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-288">Select **OK**.</span></span>
1. <span data-ttu-id="e7e55-289">**Pakkaus**-sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="e7e55-289">The **Pack** page appears.</span></span> <span data-ttu-id="e7e55-290">Tuotantoskenaariossa työntekijä voi skannata rekisterikilven tai lähetyksen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="e7e55-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="e7e55-291">Avaa kuitenkin tässä skenaariossa **Kaikki lähetykset** -sivu ja etsi juuri luodun lähetyksen lähetyksen numero.</span><span class="sxs-lookup"><span data-stu-id="e7e55-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="e7e55-292">Anna sitten tämä arvo **Pakkaus**-sivun **Rekisterikilpi tai lähetys** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="e7e55-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="e7e55-293">Vaihtoehtoisesti voit antaa aiemmin muistiin kirjoitetun lähetyksen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="e7e55-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="e7e55-294">Valitse toimintoruudussa **Uusi kontti**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="e7e55-295">Avautuvassa valintaikkunassa on tietoja uudesta kontista.</span><span class="sxs-lookup"><span data-stu-id="e7e55-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="e7e55-296">Älä muuta oletusarvoja ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="e7e55-297">Valitse **Pakkaus**-sivun **Nimikkeen pakkaus** -pikavälilehden **Tunniste**-kentässä *A0002*. Voit nyt pakata kyseisen nimikkeen.</span><span class="sxs-lookup"><span data-stu-id="e7e55-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="e7e55-298">Nimike lisätään konttiin.</span><span class="sxs-lookup"><span data-stu-id="e7e55-298">The item is added to the container.</span></span>
1. <span data-ttu-id="e7e55-299">Valitse toimintoruudussa **Lähetettävät kontit**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="e7e55-300">Avautuvalla **Lähetettävät kontit** -sivulla on juuri luodun kontin rivi.</span><span class="sxs-lookup"><span data-stu-id="e7e55-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="e7e55-301">Kyseisen rivin **Kontin lastiluettelon tunnus** -kenttä on kuitenkin toistaiseksi tyhjä, koska osoitetarraa ja seurantanumeroa ei ole vielä saata rahdinkuljettajalta.</span><span class="sxs-lookup"><span data-stu-id="e7e55-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="e7e55-302">Valitse toimintoruudussa **Sulje kontti**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="e7e55-303">Määritä **Sulje kontti** -valintaikkunan **Bruttopaino**-kentän arvoksi *1 kg* ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7e55-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="e7e55-304">Osoitetarra on tulostettava seuraavaksi aiemmin valitulla ZPL-tulostimella.</span><span class="sxs-lookup"><span data-stu-id="e7e55-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="e7e55-305">Tarran pitäisi on seuraavan esimerkin kaltainen:</span><span class="sxs-lookup"><span data-stu-id="e7e55-305">It should resemble the following example.</span></span>

    <span data-ttu-id="e7e55-306">![Osoitetarraesimerkki](media/sps-label-example.png "Osoitetarraesimerkki")</span><span class="sxs-lookup"><span data-stu-id="e7e55-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="e7e55-307">Huomaa, että rahdinkuljettajalta saadut **Kontin lastiluettelon tunnus**- ja **Kokonaisrahti**-arvot on lisätty sellaisenaan.</span><span class="sxs-lookup"><span data-stu-id="e7e55-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]