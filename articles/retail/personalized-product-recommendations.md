---
title: Mukautettujen tuotesuositusten yleiskatsaus
description: "Tässä ohjeaiheessa on tietoja Dynamics 365 for Retailin tuotesuosituksista, jotka voidaan näyttää myyntipisteen laitteessa."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 006ea02d4fb10092fed82516f1d17d0da750c6a1
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="68621-103">Mukautettujen tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="68621-103">Personalized product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="68621-104">Tuotesuosituspalvelun nykyinen versio ollaan poistamassa, sillä toiminto suunnitellaan uudelleen käyttämällä parempaa algoritmia ja uudempia vähittäismyyntiin soveltuvia ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="68621-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="68621-105">Lisätietoja on kohdassa [Poistetut tai vanhentuneet ominaisuudet](../dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="68621-105">For more information see [Removed or deprecated features](../dev-itpro/migration-upgrade/deprecated-features.md).</span></span> <span data-ttu-id="68621-106">Siirry sivun alareunaan, jos sinulla on ongelmia, jotka liittyvät ympäristössä jo käyttöönotettuihin tuotesuosituksiin.</span><span class="sxs-lookup"><span data-stu-id="68621-106">Navigate to the bottom of the page if you are facing issues with already-enabled product recommendations for your environment.</span></span> 

<span data-ttu-id="68621-107">Dynamics 365 for Retailissa voidaan näyttää suosituksia myyntipisteen laitteessa.</span><span class="sxs-lookup"><span data-stu-id="68621-107">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="68621-108">Suositukset ovat nimikkeitä, joista asiakas on mahdollisesti kiinnostunut ostohistorian, toiveluettelon ja muiden asiakkaiden verkosta tai kivijalkakaupasta ostamien tuotteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="68621-108">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="68621-109">Myyjillä, joilla on laajat tuoteluettelot, suositukset auttavat asiakasta löytämään uusia tuotteita.</span><span class="sxs-lookup"><span data-stu-id="68621-109">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="68621-110">Esittämällä tuotesuosituksia, jotka on kohdistettu asiakkaan kiinnostuksen kohteisiin, kauppiaat parantavat lisä- ja ristiinmyyntiään ja tehostavat asiakkaiden sitoutumista.</span><span class="sxs-lookup"><span data-stu-id="68621-110">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="68621-111">Dynamics 365 for Retailin tuotesuositukset toimivat kognitiivisten palveluiden ja Microsoft Azuren koneoppimisen avulla.</span><span class="sxs-lookup"><span data-stu-id="68621-111">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="68621-112">Skenaariot</span><span class="sxs-lookup"><span data-stu-id="68621-112">Scenarios</span></span>
---------

<span data-ttu-id="68621-113">Tuotteen suosituksia on käytössä seuraavissa myyntipisteskenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="68621-113">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="68621-114">Ne ovat saatavissa Cloud POS - ja Modern POS (MPOS) -myyntipisteissä.</span><span class="sxs-lookup"><span data-stu-id="68621-114">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="68621-115">**Tuotteen tiedot** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="68621-115">On the **Product details** page:</span></span>

-   <span data-ttu-id="68621-116">Jos myymälän päällikkö käy **Tuotteen tiedot** -sivulla tarkastelleessaan aiempia tapahtumia eri kanavissa, moduuli ehdottaa muita nimikkeitä, jotka todennäköisesti voi ostaa yhdessä.</span><span class="sxs-lookup"><span data-stu-id="68621-116">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="68621-117">Jos myymäläpäällikkö lisää asiakkaan tapahtumaan ja käy sitten **Tuotteen tiedot** -sivulla, suositusmoduuli antaa mukautettuja suosituksia käyttäen asiakkaan tapahtumahistoriaa.</span><span class="sxs-lookup"><span data-stu-id="68621-117">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="68621-118">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="68621-118">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="68621-119">**Tapahtuma**-sivulla:</span><span class="sxs-lookup"><span data-stu-id="68621-119">On the **Transaction** page:</span></span>

-   <span data-ttu-id="68621-120">Suositusmoduuli ehdottaa nimikkeitä kaikkien ostoskorissa olevien tuotteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="68621-120">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="68621-121">Jos myymäläpäällikkö lisää asiakkaan tapahtumaan, suositusmoduuli antaa henkilökohtaisia suosituksia käyttäen asiakkaan tapahtumahistoriaa ja ostoskorissa olevien nimikkeiden tietoja.</span><span class="sxs-lookup"><span data-stu-id="68621-121">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="68621-122">Jotta suositukset voitaisiin näyttää **Tapahtuma**-sivulla, vähittäismyyjän pitää päivittää näytön asettelu Dynamics 365 for Retailissa.</span><span class="sxs-lookup"><span data-stu-id="68621-122">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="68621-123">**Suositukset**-ohjausobjekti on pudotettava **Tapahtuma**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="68621-123">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="68621-124">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="68621-124">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="68621-125">**Asiakastiedot**-sivulla:</span><span class="sxs-lookup"><span data-stu-id="68621-125">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="68621-126">Suositusmoduuli ehdottaa nimikkeitä käyttäjätunnuksen ja asiakkaan toivelistassa olevien tuotteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="68621-126">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="68621-127">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="68621-127">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="68621-128">Dynamics 365 for Retailin määrittäminen ottamaan käyttöön myyntipisteen suositukset</span><span class="sxs-lookup"><span data-stu-id="68621-128">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="68621-129">Voit määrittää tuotesuositukset seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="68621-129">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="68621-130">Varmista, että olet valinnut oikean **yrityksen**.</span><span class="sxs-lookup"><span data-stu-id="68621-130">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="68621-131">Siirry kohtaan **Yksikkösäilö**. Valitse **Vähittäismyynti** ja valitse sitten **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="68621-131">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="68621-132">Nyt käytössä ovat esittelytiedot (tai omat tiedot) toiminnallisesta tietokannasta. Ne siirretään yksikkösäilöön.</span><span class="sxs-lookup"><span data-stu-id="68621-132">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="68621-133">Valinnainen: Jos haluat näyttää suositukset Tapahtuma-näytössä, siirry kohtaan **Näytön asettelu**, valitse näyttöasettelu, käynnistä **Näytön asettelun suunnittelutoiminto** ja pudota **Suositukset**-ohjausobjekti haluamaasi paikkaan.</span><span class="sxs-lookup"><span data-stu-id="68621-133">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="68621-134">Siirry kohtaan **Vähittäismyynnin parametrit**, valitse **Automaattianalyysipalvelut** ja valitse **Kyllä** kohdassa **Ota käyttöön myyntipisteen suositukset**.</span><span class="sxs-lookup"><span data-stu-id="68621-134">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="68621-135">Saat suositukset näkyviin myyntipisteessä suorittamalla yleisen konfiguraatiotyön **1110**.</span><span class="sxs-lookup"><span data-stu-id="68621-135">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="68621-136">Saat myyntipisteen näytön asetteluun tehdyt muutokset näkyviin suorittamalla kanavan konfigurointityön **1070**.</span><span class="sxs-lookup"><span data-stu-id="68621-136">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="68621-137">Miten se toimii?</span><span class="sxs-lookup"><span data-stu-id="68621-137">How does it work?</span></span>
<span data-ttu-id="68621-138">Kun päivität **Yksikkösäilö**-yksikön, seuraavat toiminnot tapahtuvat.</span><span class="sxs-lookup"><span data-stu-id="68621-138">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="68621-139">Dynamics 365 for Retailin toiminnallisesta tietokannasta poimitaan tiedot kognitiivisten palveluiden edellyttämässä muodossa ja ne lähetetään yksikkösäilöön.</span><span class="sxs-lookup"><span data-stu-id="68621-139">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="68621-140">Azure Data Factory (ADF) käyttää tietoja puhdistaakseen tiedot käyttäen Hive-skriptejä osana ADF-toimintoja.</span><span class="sxs-lookup"><span data-stu-id="68621-140">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="68621-141">Puhdistetut tiedot tallennetaan blob-säilöpalveluun.</span><span class="sxs-lookup"><span data-stu-id="68621-141">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="68621-142">Kognitiivisten palvelujen API käyttää blob-etäsäilöpalvelun tietoja harjoittaakseen suositusmallia.</span><span class="sxs-lookup"><span data-stu-id="68621-142">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="68621-143">Kun otat käyttöön **Ota suositukset käyttöön** -asetuksen ja suoritat konfiguraatiotyöt, tapahtuu seuraavat toiminnot.</span><span class="sxs-lookup"><span data-stu-id="68621-143">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="68621-144">Mallin tunnistetiedot ja tunnus noudetaan ohjelmointirajapinnasta ja tallennetaan Dynamics 365 for Retailin operatiiviseen tietokantaan, AOS:n web.config-tiedostoon sekä Retail-palvelimelle.</span><span class="sxs-lookup"><span data-stu-id="68621-144">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="68621-145">Mallin tunnistetiedot ja tunnus annetaan saataville CRT:lle niin, että tuotteen suosituspyynnöt online-tilassa olevista Cloud POS- ja MPOS -myyntipisteistä voidaan suorittaa.</span><span class="sxs-lookup"><span data-stu-id="68621-145">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>

> ## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="68621-146">Jo käyttöönotettuihin tuotesuosituksiin liittyvien ongelmien vianmääritys</span><span class="sxs-lookup"><span data-stu-id="68621-146">Troubleshoot issues where you have Product recommendations already enabled</span></span> 
> - <span data-ttu-id="68621-147">Valitse **Vähittäismyynnin parametrit** > **Automaattianalyysipalvelut** > **Poista tuotesuosituksen käytöstä** ja suorita **Yleinen konfiguraatiotyö [1110]**.</span><span class="sxs-lookup"><span data-stu-id="68621-147">Navigate to **Retail Parameters** > **Machine learning** > **Disable product recommendations** and run **Global configuration job [1110]**.</span></span> <span data-ttu-id="68621-148">Jos et löydä **Automaattianalyysipalvelut** -välilehtiä, ota yhteys Dynamics-tukeen.</span><span class="sxs-lookup"><span data-stu-id="68621-148">If you are not able to locate **Machine learning** tab, please contact Dynamics Support.</span></span> 
> 
> - <span data-ttu-id="68621-149">Jos lisäsit **suositusten ohjausobjektin** tapahtumanäyttöön **näytön asettelun suunnittelutoiminnolla**, poista myös se.</span><span class="sxs-lookup"><span data-stu-id="68621-149">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span> 



<a name="additional-resources"></a><span data-ttu-id="68621-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="68621-150">Additional resources</span></span>
--------

[<span data-ttu-id="68621-151">Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumasivulle</span><span class="sxs-lookup"><span data-stu-id="68621-151">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




