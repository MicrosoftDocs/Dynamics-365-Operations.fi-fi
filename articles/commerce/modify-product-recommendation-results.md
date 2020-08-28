---
title: AI-ML-pohjaisten tuotesuositustulosten muokkaaminen
description: Tässä ohjeaiheessa kerrotaan, miten yrityksen tuotesuositusten tuloksia räätälöidään tekoälyn koneoppimisen perusteella.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: bc6a793061a3e644599f0882ff163f5f57b2162d
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664951"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="fbd87-103">AI-ML-pohjaisten tuotesuositustulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="fbd87-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fbd87-104">Tässä ohjeaiheessa kerrotaan, miten yrityksen tuotesuositusten tuloksia muokataan tekoälyn koneoppimisen perusteella.</span><span class="sxs-lookup"><span data-stu-id="fbd87-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="fbd87-105">Kun tuotesuositukset on otettu käyttöön, oletusasetukset tulevat voimaan. Nämä parametrit voivat toimia erilaisissa tilanteissa.</span><span class="sxs-lookup"><span data-stu-id="fbd87-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="fbd87-106">Kannattaa käyttää jonkin verran aikaa ja pohtia, miten tulokset sopivat tuotteiden myyntiin.</span><span class="sxs-lookup"><span data-stu-id="fbd87-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="fbd87-107">Suosittelemme tulosten arviointia muutaman päivän ajan, ennen kuin parametreja muutetaan ennen testaamista uudelleen.</span><span class="sxs-lookup"><span data-stu-id="fbd87-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="fbd87-108">Tietoja suositusluettelon parametreista</span><span class="sxs-lookup"><span data-stu-id="fbd87-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="fbd87-109">Tutustu siihen, miten parametrit vaikuttavat alla oleviin tuloksiin, ennen kuin muutat parametreja.</span><span class="sxs-lookup"><span data-stu-id="fbd87-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="fbd87-110">Suosittujen tuotteiden luettelo</span><span class="sxs-lookup"><span data-stu-id="fbd87-110">"Trending" product list</span></span>

<span data-ttu-id="fbd87-111">Suositut-tuoteluettelossa on kaksi parametria, jotka voi muuttaa:</span><span class="sxs-lookup"><span data-stu-id="fbd87-111">The "Trending" product list has two parameters that can be changed:</span></span>

![Esimerkki Suosituimmat-luettelon oletusparametreista](./media/exampletrendingparameters.png)

1. <span data-ttu-id="fbd87-113">**Sisällytä uudet tuotteet X päivän ajalta** - Tuotteita, jotka on lisätty tiettyjä päiviä ennen kuluvaa päivää, voidaan käyttää tuote-ehdokkaiden valinnassa.</span><span class="sxs-lookup"><span data-stu-id="fbd87-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="fbd87-114">Kuvan oletusarvo ehdottaa, että 180 päivää vanhempia tuotteita voi käyttää suosittujen tuotteiden luettelossa.</span><span class="sxs-lookup"><span data-stu-id="fbd87-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="fbd87-115">**Sisällytä myynti X päivän ajalta** - Myyntitapahtumia, jotka ovat tapahtuneet tiettyjä päiviä ennen kuluvaa päivää, voidaan käyttää tuotteiden tilaamisessa.</span><span class="sxs-lookup"><span data-stu-id="fbd87-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="fbd87-116">Yllä oleva oletusarvo viittaa siihen, että kaikkia edellisten 30 päivän aikaisia tuoteostoja voidaan käyttää tuotteen sijoituksen määrittämisessä suosittujen tuotteiden luetteloa varten.</span><span class="sxs-lookup"><span data-stu-id="fbd87-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="fbd87-117">Myydyimpien tuotteiden luettelo</span><span class="sxs-lookup"><span data-stu-id="fbd87-117">"Best selling" product list</span></span>

<span data-ttu-id="fbd87-118">Liiketoiminnasta riippuen Myydyimmät-luettelossa voi olla eri tulokset kuin Suositut-luettelossa, vaikka molemmissa käytetään tapahtumatietoja tuotteiden järjestämiseksi.</span><span class="sxs-lookup"><span data-stu-id="fbd87-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="fbd87-119">Koska myydyimmillä tuotteilla ei ole katkaisua lajittelupäivämäärän perusteella, Myydyimmät-luettelon tuotteissa voi olla hyvin suosittuja mutta vanhoja tuotteita, jotka ovat jo pudonneet suosittujen tuotteiden luettelosta.</span><span class="sxs-lookup"><span data-stu-id="fbd87-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="fbd87-120">Myydyimmät-tuoteluettelossa on yksi parametri, jonka voi muuttaa:</span><span class="sxs-lookup"><span data-stu-id="fbd87-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![Esimerkki Myydyimmät-luettelon oletusparametrista](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="fbd87-122">**Sisällytä myynti X päivän ajalta** - Myyntitapahtumia, jotka ovat tapahtuneet tiettyjä päiviä ennen kuluvaa päivää, voidaan käyttää tuotteiden tilaamisessa.</span><span class="sxs-lookup"><span data-stu-id="fbd87-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="fbd87-123">Yllä oleva oletusarvo viittaa siihen, että kaikkia edellisten 30 päivän aikaisia tuoteostoja voidaan käyttää tuotteen sijoituksen määrittämisessä myydyimpien tuotteiden luetteloa varten.</span><span class="sxs-lookup"><span data-stu-id="fbd87-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="fbd87-124">Tuotteiden lisääminen suositusluetteloihin tai niiden poistaminen luetteloista manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="fbd87-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="fbd87-125">Uudet-, suositut- tai myydyimmät -luettelot</span><span class="sxs-lookup"><span data-stu-id="fbd87-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="fbd87-126">Siirry kohtaan **Retail ja Kauppa** > **Tuotesuositukset** > **Suositusparametrit**.</span><span class="sxs-lookup"><span data-stu-id="fbd87-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="fbd87-127">Valitse jaettujen parametrien luettelossa **Suositusluettelot**.</span><span class="sxs-lookup"><span data-stu-id="fbd87-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="fbd87-128">Valitse luettelon lisätyt tai poistetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="fbd87-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="fbd87-129">Voit lisätä tuotteita taulukkoon valitsemalla **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="fbd87-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="fbd87-130">Etsi tuotesarakkeesta tuotteen **Nimi** tai **Tuotenumero.**</span><span class="sxs-lookup"><span data-stu-id="fbd87-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![Esimerkki tuotteen etsimisestä uudesta tuoteluettelosta](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="fbd87-132">Valitse Rivityyppi-sarakkeesta jompikumpi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="fbd87-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="fbd87-133">**Sisällytä** – Pakottaa tuotteen luettelon alkuun</span><span class="sxs-lookup"><span data-stu-id="fbd87-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="fbd87-134">**Jätä pois** – Estää tuotetta näkymästä luettelossa</span><span class="sxs-lookup"><span data-stu-id="fbd87-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![Esimerkki tuotteen sisällytysluettelosta tai poisjättämisestä uuden tuoteluettelon avulla](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="fbd87-136">Jos **näyttöjärjestystä** muutetaan, **Sisällytä**-merkinnän saaneiden tuotteiden järjestys luettelossa muuttuu.</span><span class="sxs-lookup"><span data-stu-id="fbd87-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="fbd87-137">Jos kahdella tuotteilla on sama **näyttöjärjestyksen** arvo, näiden kahden tuloksen lopullinen järjestys voi poiketa taustasovelluksen järjestyksestä.</span><span class="sxs-lookup"><span data-stu-id="fbd87-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="fbd87-138">Voit poistaa tuotteita taulukosta valitsemalla poistettavan rivin ja valitsemalla sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="fbd87-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="fbd87-139">Ihmiset pitävät myös- tai Ostetaan usein yhdessä -luettelot</span><span class="sxs-lookup"><span data-stu-id="fbd87-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="fbd87-140">Ostetaan usein yhdessä- tai Ihmiset pitävät myös -luetteloiden kontekstissa koneoppimista käytetään kuluttajan ostomallien analysoimisessa. Näin voidaan suositella liittyviä tuotteita, jotka ostetaan usein yhdessä yksilöllisen alkutuotteen kohdalla.</span><span class="sxs-lookup"><span data-stu-id="fbd87-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="fbd87-141">*Alkutuote* on tuote, jolle haluat luoda tuloksia.</span><span class="sxs-lookup"><span data-stu-id="fbd87-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="fbd87-142">Lisää tälle tuotteelle tuloksia tai poista niitä, kun haluat muokata suositusluetteloita manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="fbd87-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="fbd87-143">Seuraavia ohjeita noudattamalla voit lisätä alkutuotteen tuloksia tai poistaa niitä:</span><span class="sxs-lookup"><span data-stu-id="fbd87-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="fbd87-144">Valitse **Alkutuote**.</span><span class="sxs-lookup"><span data-stu-id="fbd87-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="fbd87-145">Valitse **Tuote**-sarakkeessa ominaisuutta **nimellä** tai **tuotenumerolla.**
![Esimerkki tuotteen hakemisesta Ostetaan usein yhdessä -luettelosta](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="fbd87-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="fbd87-146">Valitse **Rivityyppi**-sarakkeesta jompikumpi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="fbd87-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="fbd87-147">**Sisällytä** – Pakottaa tuotteen luettelon alkuun</span><span class="sxs-lookup"><span data-stu-id="fbd87-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="fbd87-148">**Jätä pois** – Estää tuotetta näkymästä luettelossa</span><span class="sxs-lookup"><span data-stu-id="fbd87-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="fbd87-149">![Esimerkki tuotteen sisällyttämisestä Ostetaan usein yhdessä -luetteloon tai sen sulkemisesta pois luettelosta](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="fbd87-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="fbd87-150">Voit poistaa tuotteita taulukosta valitsemalla poistettavan rivin ja valitsemalla sitten Poista.</span><span class="sxs-lookup"><span data-stu-id="fbd87-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="fbd87-151">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fbd87-151">Additional resources</span></span>

[<span data-ttu-id="fbd87-152">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="fbd87-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="fbd87-153">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="fbd87-153">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="fbd87-154">Tuotesuositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="fbd87-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="fbd87-155">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="fbd87-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="fbd87-156">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="fbd87-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="fbd87-157">"Osta samankaltaisia tyylejä" -suositusten käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="fbd87-157">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="fbd87-158">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="fbd87-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="fbd87-159">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="fbd87-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="fbd87-160">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="fbd87-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="fbd87-161">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="fbd87-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="fbd87-162">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="fbd87-162">Product recommendations FAQ</span></span>](faq-recommendations.md)
