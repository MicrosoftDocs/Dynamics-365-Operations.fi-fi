---
title: Alihankinta
description: "Tämä ohjeaihe auttaa sinua luomaan valmistuksen alihankintaa koskevan esittelyn Microsoft Dynamics 365 for Finance and Operationsissa."
author: christophernread
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ade3f4ad9878c9e885afc5034334e41897512871
ms.openlocfilehash: 55b516f928eadea9b7ddbb1192db79f3ab7fa204
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2018

---

# <a name="subcontracting"></a><span data-ttu-id="cbbfd-103">Alihankinta</span><span class="sxs-lookup"><span data-stu-id="cbbfd-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cbbfd-104">Tämä ohjeaihe auttaa sinua luomaan valmistuksen alihankintaa koskevan esittelyn Microsoft Dynamics 365 for Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="cbbfd-105">Tämän ohjeaiheen ensimmäisessä osassa kuvataan tietojen määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="cbbfd-106">Toisessa osassa selvitetään esittelyn vaiheita.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="cbbfd-107">Kohdeyleisö</span><span class="sxs-lookup"><span data-stu-id="cbbfd-107">Target audience</span></span>

<span data-ttu-id="cbbfd-108">Tässä ohjeaiheessa kerrotaan, miten voit määrittää valmistuksen alihankinnan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="cbbfd-109">Voit tehdä alihankintatoiminnon työnkulun perusmäärityksen HQUS-yrityksen olemassa olevien tietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="cbbfd-110">HQUS-yrityksen esittelytiedot sisältävät asetusparametreja, jotka on määritetty etukäteen esittelyn vaiheiden tukemiseksi.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="cbbfd-111">Vaikka esittelyssä käsitellään erilaisten roolien tärkeimpiä heikkouksia ja haasteita, järjestelmänvalvoja voi täydentää esittelyä.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="cbbfd-112">Esittelyskenaario</span><span class="sxs-lookup"><span data-stu-id="cbbfd-112">Demo scenario</span></span>

<span data-ttu-id="cbbfd-113">HQUS-yrityksessä valmistetaan korkealaatuisia kaiuttimia.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="cbbfd-114">Valmistusprosessin aikana kaiuttimet kulkevat seuraavan kolmen työvaiheen läpi.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="cbbfd-115">**Alustava kokoonpano** – Kaiuttimen kotelon kokoaminen.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="cbbfd-116">Kotelon materiaali valitaan materaalivarastosta ennen työvaiheen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="cbbfd-117">**Pinnoitus** – Kun kaiuttimen kotelo on koottu, se on pinnoitettava.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="cbbfd-118">Tämän työvaiheen suorittaa toimittaja (alihankkija).</span><span class="sxs-lookup"><span data-stu-id="cbbfd-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="cbbfd-119">Alustavasti koottu kaiuttimen kotelo lähetetään pinnoituksesta vastaavalle alihankkijalle kahden materiaalin kanssa.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="cbbfd-120">**Viimeistely** – Kun alihankkija on pinnoittanut alustavasti kootun kaiuttimen kotelon, se palautetaan HQUS-yritykselle kaiuttimen lopullista kokoamista varten.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="cbbfd-121">Seuraavassa kuvassa näytetään kolme työvaihetta ja materiaalit, joita niissä käytetään.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![Alustavan kokoamisen, pinnoituksen ja viimeistelyn työvaiheet sekä niissä käytetyt materiaalit](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="cbbfd-123">Määritys</span><span class="sxs-lookup"><span data-stu-id="cbbfd-123">Setup</span></span>

<span data-ttu-id="cbbfd-124">Ennen esittelyn aloittamista on määritettävä tiedot.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="cbbfd-125">Valmiin tuotteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="cbbfd-125">Set up the finished product</span></span>

<span data-ttu-id="cbbfd-126">Tässä menettelyssä käydään läpi julkaistun tuotteen D8100, "Pinnoitettu kotelo", määritystä.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="cbbfd-127">Valitse **Tuotetietojen hallinta \>Tuotteet \>Julkaistut tuotteet**, jotta voit avata **Julkaistun tuotteen tiedot** -sivun.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="cbbfd-128">Hae olemassa olevaa julkaistua tuotetta kirjoittamalla pikasuodatinkenttään **D8100**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![Julkaistun tuotteen D8100 suodattaminen Julkaistun tuotteen tiedot -sivulle](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="cbbfd-130">Valitse toimintoruudun **Suunnittele**-välilehdessä **Reititys**, jotta voit avata **Reititys**-sivun.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="cbbfd-131">**Reititys**-sivu näyttää julkaistun tuotteen D8100 kahdeksan reititysversiota.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="cbbfd-132">Kahdeksan reititysversiota jaetaan neljän reitityksen välille toimipaikassa 1 ja toimipaikassa 5.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="cbbfd-133">Reititystä 000400 käytetään kustannuslaskentaan, reititystä 00041 käytetään, kun pinnoitus on sisäinen työvaihe, ja reititystä 00042 käytetään, kun pinnoitus on ulkoinen työvaihe.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![Kahdeksan reititysversioita Reititys-sivulla](./media/subcontract03_route-page.png)

4. <span data-ttu-id="cbbfd-135">Valitse **Versiot**-ruudukon yläruudussa reititysversio **00042** toimipaikalle **5**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="cbbfd-136">Valitse **Yleiskatsaus**-välilehden alemmassa ruudussa työvaihe **20** (**Cbnt CtSc**) ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![Työvaihe 20 reititysversiolle 00042 toimipaikalle 5 valittu](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="cbbfd-138">Valitse **Yleinen**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-138">Select the **General** tab.</span></span>

    <span data-ttu-id="cbbfd-139">Huomaa, että **Reititystyyppi**-kentän arvoksi on määritetty **Toimittaja**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="cbbfd-140">Tämä arvo ilmaisee, että työvaihe 20 (Cbnt CtSc) suoritetaan alihankintana.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![Reititystyypin kentän arvoksi on määritetty Toimittaja Yleiset-välilehdessä](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="cbbfd-142">Valitse **Resurssivaatimukset**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="cbbfd-143">Ominaisuuksia käytetään löytämään sovellettava resurssi tuotantosuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="cbbfd-144">Huomaa työvaiheen 20 (Cbnt CtSc) osalta, että resurssi, jolla on kaksi ominaisuutta, **pinnoitus** ja **pinnoitetut kotelot**, on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![Pinnoitus- ja pinnoitetut kotelot -ominaisuudet Resurssivaatimukset-välilehdessä](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="cbbfd-146">Valitse **Sovellettavat resurssit**, jotta voit avata **Sovellettavat resurssit** -valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="cbbfd-147">Löytyy kolme resurssia, jotka vastaavat työvaiheen resurssivaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="cbbfd-148">Huomaa, että resurssit 8851 ja 8852 ovat **Toimittaja**-tyyppiä.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![Kolme asianmukaista resurssia Sovellettavat resurssit -valintaikkunassa](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="cbbfd-150">Valitse **OK**, jotta voit sulkea **Sovellettavat resurssit** -valintaikkunan, ja palaa **Reititys**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="cbbfd-151">Sulje **Reititys**-sivu, jotta voit palata **Julkaistun tuotteen tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![Julkaistun tuotteen tiedot -sivu](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="cbbfd-153">Valitse toimintoruudun **Suunnittele**-välilehdessä **Tuoterakenneversiot**, jotta voit avata **Tuoterakenneversiot**-sivun.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="cbbfd-154">**Tuoterakenneversiot**-sivulla on julkaistun tuotteen D8100 neljä tuoterakenneversiota.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="cbbfd-155">Tuoterakennetta 000040 käytetään kustannuslaskentaan ja suunnitteluun, tuoterakennetta 000041 käytetään, jos pinnoituksen työvaihe suoriteaan yrityksen sisällä, ja tuoterakenteita 000042 ja 000043 käytetään, jos pinnoituksen työvaihe suoritetaan alihankintana.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="cbbfd-156">Huomaa, että nimike S8050 on **Palvelu**-nimiketyyppinen tuote.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="cbbfd-157">Tämä nimike edustaa alihankintana suoritettavaa työtä.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-157">This item represents the subcontracted work.</span></span>

    ![Neljä tuoterakenneversiota Tuoterakenneversiot-sivulla](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="cbbfd-159">Valitse **Tuoterakennerivit**-pikavälilehdestä **Muokkaa**, jotta voit avata **Muokkaa tuoterakenneriviä** -valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="cbbfd-160">Kun tuotantotilaus on luotu ja arvioitu julkaistulle tuotteelle D8100, nimikkeelle S8050 luodaan automaattisesti ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="cbbfd-161">Tämä ostotilaus linkitetään tuotantotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="cbbfd-162">Jotta ostotilaukset voidaan luoda automaattisesti, **Rivityyppi**-kentän arvoksi on määritettävä **Toimittaja**, ja alihankkijalle on valittava toimittajatili.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="cbbfd-163">Tässä tapauksessa toimittajatili on US-801.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="cbbfd-164">Huomaa, että tuoterakennerivi on liitetty pinnoituksen työvaiheeseen työvaihenumeron kautta (tässä tapauksessa 20).</span><span class="sxs-lookup"><span data-stu-id="cbbfd-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![Tuoterakennerivin valintaikkunan muokkaaminen](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="cbbfd-166">Salasanan luominen varastotyöntekijöille</span><span class="sxs-lookup"><span data-stu-id="cbbfd-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="cbbfd-167">Sinun on määritettävä salasana varastotyöntekijöille, jotka käyttävät käsikäyttöisiä laitteita.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="cbbfd-168">Valitse **Varaston hallinta \> Määritys \> Työntekijä**, jotta voit avata **Työn käyttäjät** -sivun.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="cbbfd-169">Valitse **Käyttäjät**-pikavälilehdestä rivi käyttäjälle **51**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![Työn käyttäjät -sivu](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="cbbfd-171">Valitse **Nollaa salasana**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="cbbfd-172">Syötä **Salasana**- ja **Vahvista salasana** -kenttiin **1**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="cbbfd-173">Valitse **Määritä salasana**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="cbbfd-174">Vaiheittainen esittely</span><span class="sxs-lookup"><span data-stu-id="cbbfd-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="cbbfd-175">**Skenaario ja tausta**</span><span class="sxs-lookup"><span data-stu-id="cbbfd-175">**Scenario and background**</span></span>

<span data-ttu-id="cbbfd-176">Tuotteelle D8100 luodaan 10 osan tuotantotilaus, "Pinnoitettu kotelo".</span><span class="sxs-lookup"><span data-stu-id="cbbfd-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="cbbfd-177">Kotelot pinnoitetaan alihankintana, jonka suorittaa toimittaja US-801, Perfect Coating Solutions.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="cbbfd-178">Tuotantotilaus sisältää kolme työvaihetta.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-178">The production order consists of three operations.</span></span> <span data-ttu-id="cbbfd-179">Ensimmäisessä työvaiheessa kotelo kootaan alustavasti yrityksen sisällä.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="cbbfd-180">Alustavan kokoonpanon materiaali vapautetaan keräystä varten raakamateriaalin varastossa.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="cbbfd-181">Kun alustava kokoonpano on valmis, alustavasti koottu kotelo lähetetään Perfect Coating Solutionsille niiden kahden materiaalin kanssa, joita tarvitaan pinnoituksen työvaiheessa.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="cbbfd-182">Kun pinnoitettu kotelo on saatu takaisin toimittajalta, se viedään lopullisen sisäisen kokoonpanon työvaiheen läpi, ennen kuin se ilmoitetaan valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="cbbfd-183">Valitse **Tuotannonhallinta \> Tuotantotilaukset \> Kaikki tuotantotilaukset**, jotta voit avata **Kaikki tuotantotilaukset** -sivun.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="cbbfd-184">Valitse toimintoruudussa **Uusi tuotantotilaus**, jotta voit avata **Luo tuotantotilaus** -valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![Tuotantotilaus-valintaikkunan luominen](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="cbbfd-186">Valitse **Nimikkeen numero** -kentässä **D8100**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="cbbfd-187">Kun olet valinnut nimikkeen numeron, näkyviin tulevat varastodimension kentät.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="cbbfd-188">Valitse **Väri**-kentässä **Kromi**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="cbbfd-189">Näyttöön tulee viestiruutu, jossa tiedustellaan, onko tuoterakenteen aktiiviset versiot ja reititys sisällytettävä.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![Viestiruutu](./media/subcontract13_message-box.png)

5. <span data-ttu-id="cbbfd-191">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-191">Select **Yes**.</span></span> 

    <span data-ttu-id="cbbfd-192">**Luo tuotantojärjestys** -valintaikkunassa tuoterakenteen aktiiviset versiot ja reititys tuotteelle D8100 valitaan automaattisesti **Tuoterakenteen numero**- ja **Reititysnumero**-kentissä.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="cbbfd-193">Tässä tapauksessa valitaan tuoterakenne **000040** ja reititys **000040**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cbbfd-194">Versiota 000040 käytetään sekä tuoterakenteelle että reititykselle kustannuslaskentaan ja suunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="cbbfd-195">Valitse **Toimipaikka**-kentässä **5**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="cbbfd-196">Valitse **Varasto**-kentässä **51**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="cbbfd-197">Muuta **Tuoterakenteen numero**- ja **Reititysnumero**-kentissä arvoa, joksi valittiin automaattisesti **000042**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cbbfd-198">Versiota 000042 käytetään sekä tuoterakenteelle että reititykselle kotelon siirtämiseksi alihankintaan toimittajalle US-801.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![Luo tuotantotilaus -valintaikkunassa määritetyt arvot](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="cbbfd-200">Valitse **Luo** tuotantotilauksen luomiseksi ja palaa **Kaikki tuotantotilaukset** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![Uusi tuotantotilaus Kaikki tuotantotilaukset -sivulla](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="cbbfd-202">Valitse toimintoruudun **Tuotantotilaus**-välilehdessä **Arvio**, jotta voit avata **Arvio**-valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![Arvio-valintaikkuna](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="cbbfd-204">Valitse **OK** arvion vahvistamiseksi ja palaa **Kaikki tuotantotilaukset** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cbbfd-205">Kun tuotantotilaus on arvioitu, toimittajalle US-801 luodaan palvelunimikkeen S8050 ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="cbbfd-206">Valitse toimintoruudun **Tuotantotilaus**-välilehdessä **Tuoterakenne**, jotta voit avata **Tuoterakenne**-sivun. Voit täällä tarkastella tuotantotilauksen tuoterakennerivejä.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="cbbfd-207">Huomaa palvelunimikkeen S8050 osalta, että täällä on viittaus ostotilaukseen, joka luotiin tuotantotilauksen arvioinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![Tuotantotilauksen tuoterakennerivit Tuoterakenne-sivulla](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="cbbfd-209">Sulje **Tuoterakenne**-sivu, jotta voit palata **Kaikki tuotantotilaukset** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="cbbfd-210">Valitse toimintoruudun **Aikataulu**-välilehdessä **Ajoita työt**, jotta voit avata **Työn ajoitus** -valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="cbbfd-211">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="cbbfd-211">Specify the following values:</span></span>

    - <span data-ttu-id="cbbfd-212">Valitse **Ajoituksen suunta** -kentässä **Huomisesta päivästä eteenpäin**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="cbbfd-213">Määritä **Rajallinen kapasiteetti** -vaihtoehdoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![Työn ajoitus -valintaikkuna](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="cbbfd-215">Valitse **OK**, jotta voit sulkea **Työn ajoitus** -valintaikkunan ja palata **Kaikki tuotantotilaukset** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="cbbfd-216">Valitse toimintoruudun **Aikataulu**-välilehdessä **Gantt**, jotta voit avata **Gantt-kaavio – Resurssinäkymä** -sivun.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="cbbfd-217">Gantt-kaavio tarjoaa visuaalisen yleiskatsauksen siitä, miten tuotannon töitä ajoitetaan resursseissa.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="cbbfd-218">Huomaa, että ulkoinen pinnoituksen työvaihe koostuu kolmesta työstä: prosessityöstä, kuljetustyöstä ja jonoaikatyöstä.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![Gantt-kaavio – Resurssinäkymä-sivu](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="cbbfd-220">Sulje **Gantt-kaavio – Resurssinäkymä**-sivu, jotta voit palata **Kaikki tuotantotilaukset** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="cbbfd-221">Valitse toimintoruudun **Tuotantotilaus**-välilehdestä **Vapauta**, jotta voit avata **Vapauta**-valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![Vapauta-valintaikkuna](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="cbbfd-223">Valitse **OK**, jotta voit sulkea **Vapauta**-valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="cbbfd-224">Valitse **Tuotannonhallinta \> Kausittaiset tehtävät \> Vapauta varastoon \> Tuoterakenteen ja lomakerivien automaattinen vapauttaminen**, jotta voit avata **Tuoterakenteen ja lomakkeen rivien automaattinen vapautus** -valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![Tuoterakenteen ja lomakkeen rivien automaattinen vapautus -valintaikkuna](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="cbbfd-226">Valitse **OK**, jotta voit suorittaa tuoterakenteen ja lomakkeen rivien automaattisen vapautustyön.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="cbbfd-227">Tämä työ vapauttaa raakamateriaalien keräystyön varastoon.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="cbbfd-228">Valitse **Tuotannonhallinta \> Tuotantotilaukset \> Kaikki tuotantotilaukset**, jotta voit avata **Kaikki tuotantotilaukset** -sivun.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="cbbfd-229">Valitse pikasuodatinkentän avulla tuotantotilaus, jonka parissa olet työskennellyt.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="cbbfd-230">Valitse toimintoruudun **Varasto**-välilehdessä **Työn tiedot**, jotta voit avata **Työ**-sivun.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="cbbfd-231">Huomaa, että sivulla näkyy kaksi työjoukkoa raakamateriaalin keräykseen.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="cbbfd-232">Ensimmäinen työ on materiaaleille M8100 ja M8101.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="cbbfd-233">Näitä materiaaleja käytetään työvaiheessa 10.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="cbbfd-234">Toinen työ on materiaaleille M8202 ja M8250.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="cbbfd-235">Näitä materiaaleja käytetään työvaiheessa 20, joka on alihankintana suoritettava työvaihe.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![Kaksi työjoukkoa raakamateriaalin keräykseen Työ-sivulla](./media/subcontract22_work-page.png)

26. <span data-ttu-id="cbbfd-237">Käynnistä varastosovellus varastotyön käsittelemiseksi työvaiheelle 10.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="cbbfd-238">Valitse **Tuotannonhallinta \> Tuotantotilaukset \> Kaikki tuotantotilaukset**, jotta voit avata **Kaikki tuotantotilaukset** -sivun.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="cbbfd-239">Valitse pikasuodatinkentän avulla tuotantotilaus, jonka parissa olet työskennellyt.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="cbbfd-240">Valitse toimintoruudun **Tuotantotilaus**-välilehdestä **Käynnistä**, jotta voit avata **Käynnistä**-valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="cbbfd-241">Määritä **Yleiset**-välilehdelle seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="cbbfd-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="cbbfd-242">Valitse **Työvaiheesta nro**</span><span class="sxs-lookup"><span data-stu-id="cbbfd-242">In the **From Oper. No.**</span></span> <span data-ttu-id="cbbfd-243">-kentässä **10**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-243">field, select **10**.</span></span>
    - <span data-ttu-id="cbbfd-244">Valitse **Työvaiheeseen nro**</span><span class="sxs-lookup"><span data-stu-id="cbbfd-244">In the **To Oper. No.**</span></span> <span data-ttu-id="cbbfd-245">-kentässä **10**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-245">field, select **10**.</span></span>

    ![Yleiset-välilehdessä määritetyt arvot](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="cbbfd-247">Valitse **OK**, jotta voit sulkea **Käynnistä** -valintaikkunan ja palata **Kaikki tuotantotilaukset** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="cbbfd-248">Huomaa, että tuotantotilauksen tilana on nyt **Käynnistetty**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="cbbfd-249">Työvaiheen 10 materiaalit käytetään keräysluettelokirjauskansion automaattisessa kirjauksessa.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="cbbfd-250">Työvaiheen 10 ajankäyttö lasketaan reitityskorttikirjauskansion automaattisen kirjauksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="cbbfd-251">Käynnistä varastosovellus varastotyön käsittelemiseksi työvaiheelle 20.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="cbbfd-252">Valitse toimintoruudun **Tuotantotilaus**-välilehdestä **Käynnistä**, jotta voit avata **Käynnistä**-valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="cbbfd-253">Määritä **Yleiset**-välilehdelle seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="cbbfd-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="cbbfd-254">Valitse **Työvaiheesta nro**</span><span class="sxs-lookup"><span data-stu-id="cbbfd-254">In the **From Oper. No.**</span></span> <span data-ttu-id="cbbfd-255">-kentässä **20**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-255">field, select **20**.</span></span>
    - <span data-ttu-id="cbbfd-256">Valitse **Työvaiheeseen nro**</span><span class="sxs-lookup"><span data-stu-id="cbbfd-256">In the **To Oper. No.**</span></span> <span data-ttu-id="cbbfd-257">-kentässä **20**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-257">field, select **20**.</span></span>
    - <span data-ttu-id="cbbfd-258">Kirjoita **Määrä**-kenttään **10**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="cbbfd-259">Määritä **Kirjaa keräysluettelo nyt** -vaihtoehdon arvoksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-259">Set the **Post picking list now** option to **No**.</span></span>

    ![Yleiset-välilehdessä määritetyt arvot](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="cbbfd-261">Valitse **OK**, jotta voit sulkea **Käynnistä** -valintaikkunan ja palata **Kaikki tuotantotilaukset** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="cbbfd-262">Keräysluettelo luodaan materiaaleille, joita käytetään pinnoituksen työvaiheessa, ja palvelunimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="cbbfd-263">Palvelunimike edustaa alihankintana suoritettavan työvaiheen kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="cbbfd-264">Valitse toimintoruudun **Näytä**-välilehdessä **Keräysluettelo**, jotta voit avata **Keräysluettelo**-sivun.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="cbbfd-265">Valitse keräilylettelo, jota ei kirjata, ja valitse sitten kirjauskansion numero, jotta voit tarkastella kirjauskansion rivejä.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![Kirjauskansion rivit Keräysluettelo-sivulla](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="cbbfd-267">Valitse toimintoruudussa **Tulosta**\>**Keräysluettelon raportti**, jotta voit avata **Keräysluettelon raportti** -valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="cbbfd-268">Määritä **Käytä toimitusilmoituksen asettelua** -vaihtoehdon arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![Keräysluettelon raportti -valintaikkuna](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="cbbfd-270">Valitse **OK**, jotta voit luoda **Keräysluettelo**-raportin.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="cbbfd-271">Tässä tapauksessa toimittajan toimitusilmoitus tulostetaan tuotannon keräysluettelon kirjauskansiosta.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="cbbfd-272">Toimitusilmoituksessa määritetään materiaalit, jotka lähetetään toimittajalle, joka suorittaa pinnoituksen työvaiheen.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![Keräysluetteloraportti](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="cbbfd-274">Sulje **Keräysluettelo**-raportti, jotta voit palata **Keräysluettelo**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="cbbfd-275">Valitse toimintoruudussa **Kirjaus**, jotta voit avata **Kirjauskansio**-valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![Kirjauskansio-valintaikkuna](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="cbbfd-277">Valitse **OK**, jotta voit sulkea **Kirjauskansio**-valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="cbbfd-278">Avaa ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-278">Open the purchase order.</span></span>

    ![Ostotilaus-sivu](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="cbbfd-280">Valitse toimintoruudun **Osto**-välilehdessä **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="cbbfd-281">Valitse **Kirjaus**, jotta voit avata **Kirjauskansio**-valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="cbbfd-282">Valitse **OK**, jotta voit sulkea **Kirjauskansio**-valintaikkunan ja palata **Ostotilaus**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="cbbfd-283">Muuta yksikköhinta arvosta **33** arvoon **40**.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-283">Change the unit price from **33** to **40**.</span></span>

    ![Yksikköhinta muuttunut Ostotilaus-sivulla](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="cbbfd-285">Vahvista ostotilaus uudelleen.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="cbbfd-286">Tuotekuitti.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-286">Product receipt.</span></span>

    ![Tuotekuitin kirjaus -valintaikkuna](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="cbbfd-288">Ostolasku.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-288">Purchase invoice.</span></span>
52. <span data-ttu-id="cbbfd-289">Päivitä täsmäytyksen tilaa.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-289">Update the match status.</span></span>

    ![Toimittajalasku-sivu](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="cbbfd-291">Ilmoita valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-291">Report as finished.</span></span>

    ![Ilmoita valmiiksi -valintaikkuna](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="cbbfd-293">Loppu.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-293">End.</span></span>

    ![Loppu-valintaikkuna](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="cbbfd-295">Kustannusvertailu.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-295">Cost comparison.</span></span>

    ![Kustannusvertailukaaviot](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="cbbfd-297">Puuttuva määritys tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="cbbfd-297">Missing setup in data.</span></span>

