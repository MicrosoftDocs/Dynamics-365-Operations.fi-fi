---
title: Mukautettujen tuotesuositusten yleiskatsaus
description: "Dynamics 365 for Retailissa voidaan näyttää suosituksia myyntipisteen laitteessa. Suositukset ovat nimikkeitä, joista asiakas on mahdollisesti kiinnostunut ostohistorian, toiveluettelon ja muiden asiakkaiden verkosta tai kivijalkakaupasta ostamien tuotteiden perusteella. Myyjillä, joilla on laajat tuoteluettelot, suositukset auttavat asiakasta löytämään uusia tuotteita. Esittämällä tuotesuosituksia, jotka on kohdistettu asiakkaan kiinnostuksen kohteisiin, kauppiaat parantavat lisä- ja ristiinmyyntiään ja tehostavat asiakkaiden sitoutumista. Dynamics 365 for Retailin tuotesuositukset toimivat kognitiivisten palveluiden ja Microsoft Azuren koneoppimisen avulla."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 42ffb375d9786b2ac506d6ef06e9da9ee22652a6
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="2ce18-107">Mukautettujen tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2ce18-107">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="2ce18-108">Tämä ominaisuus on toistaiseksi käytettävissä vain eristys- ja tuotantoympäristöjen (korkea saatavuus) käyttöönottotopologioissa.</span><span class="sxs-lookup"><span data-stu-id="2ce18-108">This feature is currently available on sandbox and production (high-availability) deployment topologies only.</span></span> 

<span data-ttu-id="2ce18-109">Dynamics 365 for Retailissa voidaan näyttää suosituksia myyntipisteen laitteessa.</span><span class="sxs-lookup"><span data-stu-id="2ce18-109">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="2ce18-110">Suositukset ovat nimikkeitä, joista asiakas on mahdollisesti kiinnostunut ostohistorian, toiveluettelon ja muiden asiakkaiden verkosta tai kivijalkakaupasta ostamien tuotteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="2ce18-110">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="2ce18-111">Myyjillä, joilla on laajat tuoteluettelot, suositukset auttavat asiakasta löytämään uusia tuotteita.</span><span class="sxs-lookup"><span data-stu-id="2ce18-111">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="2ce18-112">Esittämällä tuotesuosituksia, jotka on kohdistettu asiakkaan kiinnostuksen kohteisiin, kauppiaat parantavat lisä- ja ristiinmyyntiään ja tehostavat asiakkaiden sitoutumista.</span><span class="sxs-lookup"><span data-stu-id="2ce18-112">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="2ce18-113">Dynamics 365 for Retailin tuotesuositukset toimivat kognitiivisten palveluiden ja Microsoft Azuren koneoppimisen avulla.</span><span class="sxs-lookup"><span data-stu-id="2ce18-113">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="2ce18-114">Skenaariot</span><span class="sxs-lookup"><span data-stu-id="2ce18-114">Scenarios</span></span>
---------

<span data-ttu-id="2ce18-115">Tuotteen suosituksia on käytössä seuraavissa myyntipisteskenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="2ce18-115">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="2ce18-116">Ne ovat saatavissa Cloud POS - ja Modern POS (MPOS) -myyntipisteissä.</span><span class="sxs-lookup"><span data-stu-id="2ce18-116">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="2ce18-117">**Tuotteen tiedot** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="2ce18-117">On the **Product details** page:</span></span>

-   <span data-ttu-id="2ce18-118">Jos myymälän päällikkö käy **Tuotteen tiedot** -sivulla tarkastelleessaan aiempia tapahtumia eri kanavissa, moduuli ehdottaa muita nimikkeitä, jotka todennäköisesti voi ostaa yhdessä.</span><span class="sxs-lookup"><span data-stu-id="2ce18-118">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="2ce18-119">Jos myymäläpäällikkö lisää asiakkaan tapahtumaan ja käy sitten **Tuotteen tiedot** -sivulla, suositusmoduuli antaa mukautettuja suosituksia käyttäen asiakkaan tapahtumahistoriaa.</span><span class="sxs-lookup"><span data-stu-id="2ce18-119">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="2ce18-120">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="2ce18-120">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="2ce18-121">**Tapahtuma**-sivulla:</span><span class="sxs-lookup"><span data-stu-id="2ce18-121">On the **Transaction** page:</span></span>

-   <span data-ttu-id="2ce18-122">Suositusmoduuli ehdottaa nimikkeitä kaikkien ostoskorissa olevien tuotteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="2ce18-122">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="2ce18-123">Jos myymäläpäällikkö lisää asiakkaan tapahtumaan, suositusmoduuli antaa henkilökohtaisia suosituksia käyttäen asiakkaan tapahtumahistoriaa ja ostoskorissa olevien nimikkeiden tietoja.</span><span class="sxs-lookup"><span data-stu-id="2ce18-123">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="2ce18-124">Jotta suositukset voitaisiin näyttää **Tapahtuma**-sivulla, vähittäismyyjän pitää päivittää näytön asettelu Dynamics 365 for Retailissa.</span><span class="sxs-lookup"><span data-stu-id="2ce18-124">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="2ce18-125">**Suositukset**-ohjausobjekti on pudotettava **Tapahtuma**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="2ce18-125">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="2ce18-126">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="2ce18-126">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="2ce18-127">**Asiakastiedot**-sivulla:</span><span class="sxs-lookup"><span data-stu-id="2ce18-127">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="2ce18-128">Suositusmoduuli ehdottaa nimikkeitä käyttäjätunnuksen ja asiakkaan toivelistassa olevien tuotteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="2ce18-128">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="2ce18-129">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="2ce18-129">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="2ce18-130">Dynamics 365 for Retailin määrittäminen ottamaan käyttöön myyntipisteen suositukset</span><span class="sxs-lookup"><span data-stu-id="2ce18-130">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="2ce18-131">Voit määrittää tuotesuositukset seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="2ce18-131">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="2ce18-132">Varmista, että olet valinnut oikean **yrityksen**.</span><span class="sxs-lookup"><span data-stu-id="2ce18-132">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="2ce18-133">Siirry kohtaan **Yksikkösäilö**, valitse **Vähittäismyynti** ja sitten **Päivitä**. Tämä käyttää demotietoja (tai omia tietojasi) toiminnallisesta tietokannasta ja siirtää ne yksikkösäilöön.</span><span class="sxs-lookup"><span data-stu-id="2ce18-133">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="2ce18-134">Valinnainen: Jos haluat näyttää suositukset Tapahtuma-näytössä, siirry kohtaan **Näytön asettelu**, valitse näyttöasettelu, käynnistä **Näytön asettelun suunnittelutoiminto** ja pudota **Suositukset**-ohjausobjekti haluamaasi paikkaan.</span><span class="sxs-lookup"><span data-stu-id="2ce18-134">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**,and then drop the **recommendations** control where needed.</span></span>
4.  <span data-ttu-id="2ce18-135">Siirry kohtaan **Vähittäismyynnin parametrit**, valitse **Automaattianalyysipalvelut** ja valitse **Kyllä** kohdassa **Ota käyttöön myyntipisteen suositukset**.</span><span class="sxs-lookup"><span data-stu-id="2ce18-135">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="2ce18-136">Saat suositukset näkyviin myyntipisteessä suorittamalla yleisen konfiguraatiotyön **1110**.</span><span class="sxs-lookup"><span data-stu-id="2ce18-136">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="2ce18-137">Saat myyntipisteen näytön asetteluun tehdyt muutokset näkyviin suorittamalla kanavan konfigurointityön **1070**.</span><span class="sxs-lookup"><span data-stu-id="2ce18-137">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="2ce18-138">[]()Miten se toimii?</span><span class="sxs-lookup"><span data-stu-id="2ce18-138">[]()How does it work?</span></span>
<span data-ttu-id="2ce18-139">Kun päivität **Yksikkösäilö**-yksikön, seuraavat toiminnot tapahtuvat.</span><span class="sxs-lookup"><span data-stu-id="2ce18-139">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="2ce18-140">Dynamics 365 for Retailin toiminnallisesta tietokannasta poimitaan tiedot kognitiivisten palveluiden edellyttämässä muodossa ja ne lähetetään yksikkösäilöön.</span><span class="sxs-lookup"><span data-stu-id="2ce18-140">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="2ce18-141">Azure Data Factory (ADF) käyttää tietoja puhdistaakseen tiedot käyttäen Hive-skriptejä osana ADF-toimintoja.</span><span class="sxs-lookup"><span data-stu-id="2ce18-141">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="2ce18-142">Puhdistetut tiedot tallennetaan blob-säilöpalveluun.</span><span class="sxs-lookup"><span data-stu-id="2ce18-142">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="2ce18-143">Kognitiivisten palvelujen API käyttää blob-etäsäilöpalvelun tietoja harjoittaakseen suositusmallia.</span><span class="sxs-lookup"><span data-stu-id="2ce18-143">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="2ce18-144">Kun otat käyttöön **Ota suositukset käyttöön** -asetuksen ja suoritat konfiguraatiotyöt, tapahtuu seuraavat toiminnot.</span><span class="sxs-lookup"><span data-stu-id="2ce18-144">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="2ce18-145">Mallin tunnistetiedot ja tunnus noudetaan ohjelmointirajapinnasta ja tallennetaan Dynamics 365 for Retailin operatiiviseen tietokantaan, AOS:n web.config-tiedostoon sekä Retail-palvelimelle.</span><span class="sxs-lookup"><span data-stu-id="2ce18-145">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="2ce18-146">Mallin tunnistetiedot ja tunnus annetaan saataville CRT:lle niin, että tuotteen suosituspyynnöt online-tilassa olevista Cloud POS- ja MPOS -myyntipisteistä voidaan suorittaa.</span><span class="sxs-lookup"><span data-stu-id="2ce18-146">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="2ce18-147">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="2ce18-147">See also</span></span>
--------

[<span data-ttu-id="2ce18-148">Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumasivulle</span><span class="sxs-lookup"><span data-stu-id="2ce18-148">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




