---
title: Hallitse AI-ML-pohjaisia tuotesuositustuloksia
description: Tässä ohjeaiheessa kerrotaan, miten yrityksen tuotesuositusten tuloksia räätälöidään tekoälyn koneoppimisen perusteella.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770067"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="8f50d-103">Hallitse AI-ML-pohjaisia tuotesuositustuloksia</span><span class="sxs-lookup"><span data-stu-id="8f50d-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8f50d-104">Tässä ohjeaiheessa kerrotaan, miten yrityksen tuotesuositusten tuloksia räätälöidään tekoälyn koneoppimisen perusteella.</span><span class="sxs-lookup"><span data-stu-id="8f50d-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="8f50d-105">Kun tuotesuositukset on otettu käyttöön, oletusasetukset tulevat voimaan. Nämä parametrit voivat toimia erilaisissa tilanteissa.</span><span class="sxs-lookup"><span data-stu-id="8f50d-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="8f50d-106">Kannattaa käyttää jonkin verran aikaa ja pohtia, miten tulokset sopivat tuotteiden myyntiin.</span><span class="sxs-lookup"><span data-stu-id="8f50d-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="8f50d-107">Suosittelemme tulosten arviointia muutaman päivän ajan, ennen kuin parametreja muutetaan ennen testaamista uudelleen.</span><span class="sxs-lookup"><span data-stu-id="8f50d-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="8f50d-108">Tietoja suositusluettelon parametreista</span><span class="sxs-lookup"><span data-stu-id="8f50d-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="8f50d-109">Tutustu siihen, miten parametrit vaikuttavat alla oleviin tuloksiin, ennen kuin muutat parametreja.</span><span class="sxs-lookup"><span data-stu-id="8f50d-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="8f50d-110">Suosittujen tuotteiden luettelo</span><span class="sxs-lookup"><span data-stu-id="8f50d-110">Trending product list</span></span>

<span data-ttu-id="8f50d-111">**Suosittujen** tuotteiden luettelossa on kaksi parametria, jotka voi muuttaa: ![Esimerkki Suositut-luettelon oletusparametreista](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="8f50d-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="8f50d-112">**Sisällytä uudet tuotteet X päivän ajalta** - Tuotteita, jotka on lisätty tiettyjä päiviä ennen kuluvaa päivää, voidaan käyttää tuote-ehdokkaiden valinnassa.</span><span class="sxs-lookup"><span data-stu-id="8f50d-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="8f50d-113">Kuvan oletusarvo ehdottaa, että 180 päivää vanhempia tuotteita voi käyttää suosittujen tuotteiden luettelossa.</span><span class="sxs-lookup"><span data-stu-id="8f50d-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="8f50d-114">**Sisällytä myynti X päivän ajalta** - Myyntitapahtumia, jotka ovat tapahtuneet tiettyjä päiviä ennen kuluvaa päivää, voidaan käyttää tuotteiden tilaamisessa.</span><span class="sxs-lookup"><span data-stu-id="8f50d-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="8f50d-115">Yllä oleva oletusarvo viittaa siihen, että kaikkia edellisten 30 päivän aikaisia tuoteostoja voidaan käyttää tuotteen sijoituksen määrittämisessä suosittujen tuotteiden luetteloa varten.</span><span class="sxs-lookup"><span data-stu-id="8f50d-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="8f50d-116">Myydyimpien tuotteiden luettelo</span><span class="sxs-lookup"><span data-stu-id="8f50d-116">Best selling product list</span></span>

<span data-ttu-id="8f50d-117">Liiketoiminnasta riippuen Myydyimmät-luettelossa voi olla eri tulokset kuin Suositut-luettelossa, vaikka molemmissa käytetään tapahtumatietoja tuotteiden järjestämiseksi.</span><span class="sxs-lookup"><span data-stu-id="8f50d-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="8f50d-118">Koska myydyimmillä tuotteilla ei ole katkaisua lajittelupäivämäärän perusteella, Myydyimmät-luettelon tuotteissa voi olla hyvin suosittuja mutta vanhoja tuotteita, jotka ovat jo pudonneet suosittujen tuotteiden luettelosta.</span><span class="sxs-lookup"><span data-stu-id="8f50d-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="8f50d-119">**Myydyimmät**-tuoteluettelossa on yksi parametri, jonka voi muuttaa:</span><span class="sxs-lookup"><span data-stu-id="8f50d-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![Esimerkki Myydyimmät-luettelon oletusparametrista](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="8f50d-121">**Sisällytä myynti X päivän ajalta** - Myyntitapahtumia, jotka ovat tapahtuneet tiettyjä päiviä ennen kuluvaa päivää, voidaan käyttää tuotteiden tilaamisessa.</span><span class="sxs-lookup"><span data-stu-id="8f50d-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="8f50d-122">Yllä oleva oletusarvo viittaa siihen, että kaikkia edellisten 30 päivän aikaisia tuoteostoja voidaan käyttää tuotteen sijoituksen määrittämisessä myydyimpien tuotteiden luetteloa varten.</span><span class="sxs-lookup"><span data-stu-id="8f50d-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="8f50d-123">Tuotteiden lisääminen suositusluetteloihin tai niiden poistaminen luetteloista manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="8f50d-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="8f50d-124">Uudet, suositut tai myydyimmät</span><span class="sxs-lookup"><span data-stu-id="8f50d-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="8f50d-125">Siirry kohtaan **Retail** > **Tuotesuositukset** > **Suositusparametrit**.</span><span class="sxs-lookup"><span data-stu-id="8f50d-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="8f50d-126">Valitse vähittäismyynnin jaettujen parametrien luettelossa **Suositusluettelot**.</span><span class="sxs-lookup"><span data-stu-id="8f50d-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="8f50d-127">Valitse luettelon lisätyt tai poistetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="8f50d-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="8f50d-128">Voit lisätä tuotteita taulukkoon valitsemalla **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="8f50d-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="8f50d-129">Etsi tuote Tuote-sarakkeessa **Nimi**-tai **Tuotenumero**-arvolla.
![Esimerkki tuotteen hakemisesta Uusi tuote -luettelosta](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="8f50d-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="8f50d-130">Valitse Rivityyppi-sarakkeesta jompikumpi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="8f50d-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="8f50d-131">**Sisällytä** – Pakottaa tuotteen luettelon alkuun</span><span class="sxs-lookup"><span data-stu-id="8f50d-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="8f50d-132">**Sulje pois** – Estää tuotetta näkymästä luettelossa ![Tuotteen Uusi tuote -luetteloon sisällyttämisen tai siitä poissulkemisen esimerkki](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="8f50d-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="8f50d-133">Jos **näyttöjärjestystä** muutetaan, **Sisällytä**-merkinnän saaneiden tuotteiden järjestys luettelossa muuttuu.</span><span class="sxs-lookup"><span data-stu-id="8f50d-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="8f50d-134">Jos kahdella tuotteilla on sama **näyttöjärjestyksen** arvo, näiden kahden tuloksen lopullinen järjestys voi poiketa taustasovelluksen järjestyksestä.</span><span class="sxs-lookup"><span data-stu-id="8f50d-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="8f50d-135">Voit poistaa tuotteita taulukosta valitsemalla poistettavan rivin ja valitsemalla sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="8f50d-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="8f50d-136">Ihmiset pitävät myös- tai Ostetaan usein yhdessä -luettelot</span><span class="sxs-lookup"><span data-stu-id="8f50d-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="8f50d-137">**Ostetaan usein yhdessä**- tai **Ihmiset pitävät myös** -luetteloiden kontekstissa koneoppimista käytetään kuluttajan ostomallien analysoimisessa. Näin voidaan suositella liittyviä tuotteita, jotka ostetaan usein yhdessä yksilöllisen alkutuotteen kohdalla.</span><span class="sxs-lookup"><span data-stu-id="8f50d-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="8f50d-138">**Alkutuote** on tuote, jolle haluat luoda tuloksia.</span><span class="sxs-lookup"><span data-stu-id="8f50d-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="8f50d-139">Lisää tälle tuotteelle tuloksia tai poista niitä, kun haluat muokata suositusluetteloita manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="8f50d-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="8f50d-140">Seuraavia ohjeita noudattamalla voit lisätä alkutuotteen tuloksia tai poistaa niitä:</span><span class="sxs-lookup"><span data-stu-id="8f50d-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="8f50d-141">Valitse **Alkutuote**.</span><span class="sxs-lookup"><span data-stu-id="8f50d-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="8f50d-142">Valitse **Tuote**-sarakkeessa ominaisuutta **nimellä** tai **tuotenumerolla.**
![Esimerkki tuotteen hakemisesta Ostetaan usein yhdessä -luettelosta](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="8f50d-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="8f50d-143">Valitse **Rivityyppi**-sarakkeesta jompikumpi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="8f50d-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="8f50d-144">**Sisällytä** – Pakottaa tuotteen luettelon alkuun</span><span class="sxs-lookup"><span data-stu-id="8f50d-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="8f50d-145">**Jätä pois** – Estää tuotetta näkymästä luettelossa</span><span class="sxs-lookup"><span data-stu-id="8f50d-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="8f50d-146">![Esimerkki tuotteen sisällyttämisestä Ostetaan usein yhdessä -luetteloon tai sen sulkemisesta pois luettelosta](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="8f50d-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="8f50d-147">Voit poistaa tuotteita taulukosta valitsemalla poistettavan rivin ja valitsemalla sitten Poista.</span><span class="sxs-lookup"><span data-stu-id="8f50d-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="8f50d-148">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8f50d-148">Additional resources</span></span>

[<span data-ttu-id="8f50d-149">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8f50d-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="8f50d-150">Ota tuotesuositukset käyttöön</span><span class="sxs-lookup"><span data-stu-id="8f50d-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="8f50d-151">Tuotesuositusluetteloiden lisääminen sivuille</span><span class="sxs-lookup"><span data-stu-id="8f50d-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
