---
title: Eri dimensioiden määrittäminen pakkausta ja varastointia varten
description: Tässä aiheessa käsitellään, miten määritetään, missä prosessissa (pakkaus, varastointi ja sisäkkäinen pakkaus) kutakin määritettyä dimensiota käytetään.
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: aa5cbf807e809238489c539d3ad8c0bc34421774
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501291"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="11ea5-103">Eri dimensioiden määrittäminen pakkausta ja varastointia varten</span><span class="sxs-lookup"><span data-stu-id="11ea5-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="11ea5-104">Jotkin nimikkeet pakataan tai tallennetaan siten, että fyysisiä dimensioita on ehkä seurattava eri tavalla kussakin prosessissa.</span><span class="sxs-lookup"><span data-stu-id="11ea5-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="11ea5-105">*Pakkauksen tuotedimensiot* -toiminnolla voi määrittää kullekin tuotteelle vähintään yhden dimensiotyypin.</span><span class="sxs-lookup"><span data-stu-id="11ea5-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="11ea5-106">Kussakin dimensiotyypissä on fyysisten mittojen joukko (paino, leveys, syvyys ja korkeus), ja se muodostaa prosessin, jossa kyseisiä fyysisiä mitta-arvoja käytetään.</span><span class="sxs-lookup"><span data-stu-id="11ea5-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="11ea5-107">Kun tämä toiminto on otettu käyttöön, järjestelmä tukee seuraavia dimensiotyyppejä:</span><span class="sxs-lookup"><span data-stu-id="11ea5-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="11ea5-108">*Varasto* – varastodimensioita käytetään sijainnin tilavuustietojen ohella määrittämään, kuinka monta kappaletta nimikettä voidaan varastoida eri varastosijainteihin.</span><span class="sxs-lookup"><span data-stu-id="11ea5-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="11ea5-109">*Pakkaus* – pakkausdimensioita käytetään konttiinpakkaamisen ja manuaalisen pakkausprosessin aikana määrittämään, kuinka monta kappaletta nimikettä sopii erilaisiin konttityyppeihin.</span><span class="sxs-lookup"><span data-stu-id="11ea5-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="11ea5-110">*Sisäkkäinen pakkaus* – sisäkkäisiä pakkausdimensioita käytetään, kun pakkausprosessi sisältää useita tasoja.</span><span class="sxs-lookup"><span data-stu-id="11ea5-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="11ea5-111">*Varastodimensioita* tuetaan myös silloin, kun *Pakkauksen tuotedimensiot* -toimintoa ei ole otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="11ea5-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="11ea5-112">Ne määritetään **Fyysiset dimensiot** -sivulla Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="11ea5-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="11ea5-113">Kaikki prosessit, joissa pakkauksen ja sisäkkäisen pakkauksen dimensioita ei ole määritetty, käyttävät näitä dimensioita.</span><span class="sxs-lookup"><span data-stu-id="11ea5-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="11ea5-114">*Pakkauksen* ja *sisäkkäisen pakkauksen* dimensiot määritetään **Fyysiset tuotedimensiot** -sivulla, joka lisätään, kun *Pakkauksen tuotedimensiot* -toiminto otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="11ea5-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="11ea5-115">Tässä aiheessa on skenaario, joka näyttää, miten tätä toimintoa käytetään.</span><span class="sxs-lookup"><span data-stu-id="11ea5-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="11ea5-116">Pakkauksen tuotedimensiot -toiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="11ea5-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="11ea5-117">Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="11ea5-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="11ea5-118">Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="11ea5-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="11ea5-119">Tässä tapauksessa toiminto näkyy seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="11ea5-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="11ea5-120">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="11ea5-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="11ea5-121">**Toiminnon nimi:** *Pakkauksen tuotedimensiot*</span><span class="sxs-lookup"><span data-stu-id="11ea5-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="11ea5-122">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="11ea5-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="11ea5-123">Määritä skenaario</span><span class="sxs-lookup"><span data-stu-id="11ea5-123">Set up the scenario</span></span>

<span data-ttu-id="11ea5-124">Ennen esimerkkiskenaarion suorittamista järjestelmä on valmisteltava tässä osassa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="11ea5-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="11ea5-125">Esittelytietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="11ea5-125">Enable demo data</span></span>

<span data-ttu-id="11ea5-126">Tämän skenaarion käyttäminen tässä määritettyjen esittelytietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakiomuotoiset [esittelytiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu.</span><span class="sxs-lookup"><span data-stu-id="11ea5-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="11ea5-127">Sinun on myös valittava *USMF*-yritys ennen kuin aloitat.</span><span class="sxs-lookup"><span data-stu-id="11ea5-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="11ea5-128">Uuden fyysisen dimension lisääminen tuotteeseen</span><span class="sxs-lookup"><span data-stu-id="11ea5-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="11ea5-129">Tuotteeseen lisätään uusi fyysinen dimensio seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="11ea5-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="11ea5-130">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="11ea5-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="11ea5-131">Valitse tuote, jonka **nimiketunnus** on *A0001*.</span><span class="sxs-lookup"><span data-stu-id="11ea5-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="11ea5-132">Valitse toimintoruudun **Varastonhallinta**-välilehden **Varasto**-ryhmässä **Fyysiset tuotedimensiot**.</span><span class="sxs-lookup"><span data-stu-id="11ea5-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="11ea5-133">**Fyysiset tuotedimensiot** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="11ea5-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="11ea5-134">Lisää uusi dimensio ja seuraavat asetukset ruudukkoon valitsemalla toimintoruudussa **Uusi**:</span><span class="sxs-lookup"><span data-stu-id="11ea5-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="11ea5-135">**Fyysisen dimension tyyppi** - *Pakkaus*</span><span class="sxs-lookup"><span data-stu-id="11ea5-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="11ea5-136">**Fyysinen yksikkö** - *kpl*</span><span class="sxs-lookup"><span data-stu-id="11ea5-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="11ea5-137">**Paino** - *4*</span><span class="sxs-lookup"><span data-stu-id="11ea5-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="11ea5-138">**Painon yksikkö** - *kg*</span><span class="sxs-lookup"><span data-stu-id="11ea5-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="11ea5-139">**Syvyys** - *3*</span><span class="sxs-lookup"><span data-stu-id="11ea5-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="11ea5-140">**Korkeus** - *4*</span><span class="sxs-lookup"><span data-stu-id="11ea5-140">**Height** - *4*</span></span>
    - <span data-ttu-id="11ea5-141">**Leveys** - *3*</span><span class="sxs-lookup"><span data-stu-id="11ea5-141">**Width** - *3*</span></span>
    - <span data-ttu-id="11ea5-142">**Pituus** - *cm*</span><span class="sxs-lookup"><span data-stu-id="11ea5-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="11ea5-143">**Tilavuuden yksikkö** - *cm3*</span><span class="sxs-lookup"><span data-stu-id="11ea5-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="11ea5-144">**Tilavuus**-kenttä lasketaan automaattisesti **Syvyys**-, **Korkeus**- ja **Leveys**-asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="11ea5-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="11ea5-145">Uuden konttityypin luominen</span><span class="sxs-lookup"><span data-stu-id="11ea5-145">Create a new container type</span></span>

<span data-ttu-id="11ea5-146">Valitse **Varastonhallinta \> Asetukset \> Kontit \> Konttityypit** ja luo uusi tietue, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="11ea5-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="11ea5-147">**Kontin tyyppikoodi** - *Pieni laatikko*</span><span class="sxs-lookup"><span data-stu-id="11ea5-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="11ea5-148">**Kuvaus** - *Lyhyt laatikko*</span><span class="sxs-lookup"><span data-stu-id="11ea5-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="11ea5-149">**Enimmäisnettopaino** - *50*</span><span class="sxs-lookup"><span data-stu-id="11ea5-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="11ea5-150">**Tilavuus** - *144*</span><span class="sxs-lookup"><span data-stu-id="11ea5-150">**Volume** - *144*</span></span>
- <span data-ttu-id="11ea5-151">**Pituus** - *6*</span><span class="sxs-lookup"><span data-stu-id="11ea5-151">**Length** - *6*</span></span>
- <span data-ttu-id="11ea5-152">**Leveys** - *6*</span><span class="sxs-lookup"><span data-stu-id="11ea5-152">**Width** - *6*</span></span>
- <span data-ttu-id="11ea5-153">**Korkeus** - *4*</span><span class="sxs-lookup"><span data-stu-id="11ea5-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="11ea5-154">Konttiryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="11ea5-154">Create a container group</span></span>

<span data-ttu-id="11ea5-155">Valitse **Varastonhallinta \> Asetukset \> Kontit \> Konttiryhmät** ja luo uusi tietue, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="11ea5-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="11ea5-156">**Konttiryhmän tunnus** - *Lyhyt laatikko*</span><span class="sxs-lookup"><span data-stu-id="11ea5-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="11ea5-157">**Kuvaus** - *Lyhyt laatikko*</span><span class="sxs-lookup"><span data-stu-id="11ea5-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="11ea5-158">Valitse uusi rivi **Tiedot**-osaan.</span><span class="sxs-lookup"><span data-stu-id="11ea5-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="11ea5-159">Määritä **konttityypiksi** *Lyhyt laatikko*.</span><span class="sxs-lookup"><span data-stu-id="11ea5-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="11ea5-160">Aseta kontin muodostusmalli</span><span class="sxs-lookup"><span data-stu-id="11ea5-160">Set up a container build template</span></span>

<span data-ttu-id="11ea5-161">Valitse **Varastonhallinta \> Asetukset \> Kontit \> Kontin rakennusmallit** ja valitse sitten **Laatikot**.</span><span class="sxs-lookup"><span data-stu-id="11ea5-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="11ea5-162">Muuta **konttiryhmän tunnukseksi** *Lyhyt laatikko*.</span><span class="sxs-lookup"><span data-stu-id="11ea5-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="11ea5-163">Skenaarion suorittaminen</span><span class="sxs-lookup"><span data-stu-id="11ea5-163">Run the scenario</span></span>

<span data-ttu-id="11ea5-164">Kun järjestelmä on valmisteltu edellisessä osassa kuvatulla tavalla, seuraavassa osassa kuvattu skenaario voidaan suorittaa.</span><span class="sxs-lookup"><span data-stu-id="11ea5-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="11ea5-165">Myyntitilauksen ja lähetyksen luominen</span><span class="sxs-lookup"><span data-stu-id="11ea5-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="11ea5-166">Tässä prosessissa luodaan lähetys nimikkeen *pakkauksen* dimensioiden perusteella, kun korkeus on alle 3.</span><span class="sxs-lookup"><span data-stu-id="11ea5-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="11ea5-167">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="11ea5-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="11ea5-168">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="11ea5-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="11ea5-169">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11ea5-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="11ea5-170">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="11ea5-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="11ea5-171">**Varasto**: *63*</span><span class="sxs-lookup"><span data-stu-id="11ea5-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="11ea5-172">Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="11ea5-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="11ea5-173">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="11ea5-173">The new sales order is opened.</span></span> <span data-ttu-id="11ea5-174">**Myyntitilausrivit**-pikavälilehden ruudukossa pitäisi olla uusi tyhjä rivi.</span><span class="sxs-lookup"><span data-stu-id="11ea5-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="11ea5-175">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11ea5-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="11ea5-176">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="11ea5-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="11ea5-177">**Määrä** *5*</span><span class="sxs-lookup"><span data-stu-id="11ea5-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="11ea5-178">Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Varaus**.</span><span class="sxs-lookup"><span data-stu-id="11ea5-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="11ea5-179">Varaa varasto **Varaus**-sivun toimintoruudussa valitsemalla **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="11ea5-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="11ea5-180">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="11ea5-180">Close the page.</span></span>
1. <span data-ttu-id="11ea5-181">Luo varaston työ valitsemalla toimintoruudun **Varasto**-välilehdessä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="11ea5-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="11ea5-182">Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Lähetyksen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="11ea5-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="11ea5-183">Valitse toimintoruudun **Kuljetus**-välilehdessä **Näytä kontit**.</span><span class="sxs-lookup"><span data-stu-id="11ea5-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="11ea5-184">Vahvista, että nimikkeen konttiinpakkauksessa käytettiin kahta *Lyhyt laatikko* -konttia.</span><span class="sxs-lookup"><span data-stu-id="11ea5-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="11ea5-185">Nimikkeen sijoittaminen varastoon</span><span class="sxs-lookup"><span data-stu-id="11ea5-185">Place an item into storage</span></span>

1. <span data-ttu-id="11ea5-186">Avaa mobiililaite, kirjaudu varastoon 63 ja valitse **Varasto \> Oikaisu sisään**.</span><span class="sxs-lookup"><span data-stu-id="11ea5-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="11ea5-187">Anna **Sijainti** = *SHORT-01*.</span><span class="sxs-lookup"><span data-stu-id="11ea5-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="11ea5-188">Tee uusi rekisterikilpi, jossa **Nimike** = *A0001* ja **Määrä** = *1 kpl*.</span><span class="sxs-lookup"><span data-stu-id="11ea5-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="11ea5-189">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="11ea5-189">Select **OK**.</span></span> <span data-ttu-id="11ea5-190">Näyttöön avautuu virhe sanoma Sijainti SHORT-01 epäonnistui, koska nimike A0001 ei sovi sijainnin määritettyihin dimensioihin.</span><span class="sxs-lookup"><span data-stu-id="11ea5-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="11ea5-191">Tämä johtuu siitä, että tuotteen *Varasto*-tyypin dimensiot ovat suuremmat kuin sijaintiprofiilissa määritetyt dimensiot.</span><span class="sxs-lookup"><span data-stu-id="11ea5-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]