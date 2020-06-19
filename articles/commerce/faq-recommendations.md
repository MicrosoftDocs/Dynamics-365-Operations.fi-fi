---
title: Tuotesuositukset – usein kysytyt kysymykset
description: Tässä ohjeaiheessa on tietoja prosesseista ja työkaluista, joiden avulla voit tehdä tuotesuosituksiin tai niiden tuloksiin liittyvien ongelmien vianmäärityksen.
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
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e27e4c4d8bdf614d6f55f44daeac3bc152219004
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404299"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="72a88-103">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="72a88-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="72a88-104">Tässä ohjeaiheessa on tietoja prosesseista ja työkaluista, joiden avulla voit tehdä [tuotesuosituksiin](product-recommendations.md) tai niiden tuloksiin liittyvien ongelmien vianmäärityksen.</span><span class="sxs-lookup"><span data-stu-id="72a88-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="72a88-105">Parhaat käytännöt</span><span class="sxs-lookup"><span data-stu-id="72a88-105">Best practices</span></span>
<span data-ttu-id="72a88-106">On erittäin tärkeää käyttää päätuote- ja tuotevariantti-käsitteitä.</span><span class="sxs-lookup"><span data-stu-id="72a88-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="72a88-107">Päätuotteen päätason varianttien järkevä ryhmittely auttaa algoritmien ja palvelun luetteloinnissa ja parempien mallien luomisessa.</span><span class="sxs-lookup"><span data-stu-id="72a88-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="72a88-108">Lisäksi palvelua voi käyttää vain yhdessä tuotteessa sen sijaan, että kaikki toisiinsa läheisesti liittyvät variantit kuuluisivat luetteloon.</span><span class="sxs-lookup"><span data-stu-id="72a88-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="72a88-109">Kun kaikki toisiinsa läheisesti liittyvät variantit asetetaan luetteloon, saattaa tapahtua virheitä tai tuloksissa voi olla kaksoiskappaleita.</span><span class="sxs-lookup"><span data-stu-id="72a88-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="72a88-110">Miksi suositusluetteloista puuttuu tuotteita?</span><span class="sxs-lookup"><span data-stu-id="72a88-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="72a88-111">Jos tuotesuositusluettelosta puuttuu nimike, kyseessä voi olla tuotteen määritysongelma.</span><span class="sxs-lookup"><span data-stu-id="72a88-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="72a88-112">Esimerkiksi tuotteen alkamis- tai päättymispäivämäärä voi olla virheellinen, dimensio saattaa olla väärin määritetty tai tuote ei ehkä ole oikeassa kanavavalikoimassa.</span><span class="sxs-lookup"><span data-stu-id="72a88-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="72a88-113">Jos nimike puuttuu tekoälyn koneoppimiseen perustuvasta suositusluettelosta, nimike ei ehkä vastaa suositusluettelon ehtoja tai sillä ei ole tarpeeksi ostotapahtumia, jotta suositusluettelo voisi näyttää sen.</span><span class="sxs-lookup"><span data-stu-id="72a88-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="72a88-114">Suosittelemme, että tarkistat seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="72a88-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="72a88-115">**Varmista, että tuotesuositukset on otettu käyttöön HQ:ssa.**</span><span class="sxs-lookup"><span data-stu-id="72a88-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="72a88-116">Lisätietoja tämän palvelun käyttöönottamisesta on kohdassa [Tuotesuositusten ottaminen käyttöön](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="72a88-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="72a88-117">**Varmista, että tärkeimmät tuoteominaisuudet on määritetty.**</span><span class="sxs-lookup"><span data-stu-id="72a88-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="72a88-118">Esimerkiksi tuotevalikoimien arvoksi on määritettävä **Sisältyy**.</span><span class="sxs-lookup"><span data-stu-id="72a88-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="72a88-119">**Juuri lajiteltujen tuotteiden näkyminen luettelossa voi kestää jopa 3 tuntia.**</span><span class="sxs-lookup"><span data-stu-id="72a88-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="72a88-120">**Jos tuote ei vieläkään näy Suositut-, Myydyimmät-, Ihmiset pitävät myös- tai Ostetaan usein yhdessä -luetteloissa, tuotteella ei ehkä ole riittävästi tapahtumia.**</span><span class="sxs-lookup"><span data-stu-id="72a88-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="72a88-121">Tässä tapauksessa voit odottaa, että tuotteella on enemmän tapahtumia, päivittää oletussuositusluettelon parametrit tai muokata suositustuoteluettelon tuloksia manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="72a88-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="72a88-122">Lisätietoja suositusparametreista on kohdassa [Tekoälyn koneoppimiseen perustuvien tuotesuositusten tulosten hallinta](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="72a88-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="72a88-123">**Varmista, että tuote täyttää luettelon suositusehdot.**</span><span class="sxs-lookup"><span data-stu-id="72a88-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="72a88-124">Lisätietoja tuotesuositusten parametreista on kohdassa [Tekoälyn koneoppimiseen perustuvien tuotesuositusten tulosten hallinta](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="72a88-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="72a88-125">Miten voin estää huonojen suositustulosten palauttamisen?</span><span class="sxs-lookup"><span data-stu-id="72a88-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="72a88-126">Suositusluettelot vaativat suuren määrän tapahtumia, jotta tuloksia saadaan.</span><span class="sxs-lookup"><span data-stu-id="72a88-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="72a88-127">Siksi on tärkeää, että käyttäjät antavat kaikki aiemmat tapahtumatiedot.</span><span class="sxs-lookup"><span data-stu-id="72a88-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="72a88-128">Lisäksi tuotteilla, joilla ei ole tapahtumia tai jolla on vain vähän tapahtumia, ei yleensä ole **Ihmiset pitävät myös**- tai **Ostetaan usein yhdessä** -tuloksia eivätkä ne näy **Suositut**- tai **Myydyimmät**-suositusluetteloissa.</span><span class="sxs-lookup"><span data-stu-id="72a88-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="72a88-129">Tämä voi tapahtua usein aivan uusille tuotteille tai vanhoille tuotteille, joita ei osteta paljon.</span><span class="sxs-lookup"><span data-stu-id="72a88-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="72a88-130">Tämä ongelma ratkeaa helposti suosittujen uusien nimikkeiden kohdalla.</span><span class="sxs-lookup"><span data-stu-id="72a88-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="72a88-131">Suosittelemme, että teet seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="72a88-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="72a88-132">**Varmista, että tuote täyttää kyseisen luettelon suositusehdot.**</span><span class="sxs-lookup"><span data-stu-id="72a88-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="72a88-133">Lisätietoja tuotesuositusten parametreista on kohdassa Tekoälyn koneoppimiseen perustuvien tuotesuositusten tulosten muokkaaminen.</span><span class="sxs-lookup"><span data-stu-id="72a88-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="72a88-134">**Jos tuote on uusi, muokkaa suositusluetteloa, kunnes tuotteella on lisää tapahtumia.**</span><span class="sxs-lookup"><span data-stu-id="72a88-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="72a88-135">Lisätietoja suositusluettelon muokkaamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvien tuotesuositusten tulosten hallinta](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="72a88-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="72a88-136">**Varmista, että tuote täyttää kyseisen luettelon suositusehdot.**</span><span class="sxs-lookup"><span data-stu-id="72a88-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="72a88-137">Lisätietoja tuotesuositusten parametreista on kohdassa [Tekoälyn koneoppimiseen perustuvien tuotesuositusten tulosten hallinta](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="72a88-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="72a88-138">**Jos tuote on uusi, muokkaa suositusluetteloa, kunnes tuotteella on lisää tapahtumia**.</span><span class="sxs-lookup"><span data-stu-id="72a88-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="72a88-139">Lisätietoja suositusluettelon muokkaamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvien tuotesuositusten tulosten hallinta](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="72a88-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="72a88-140">Voinko poistaa tuotteen, mutta silti nähdä sen myymälässä?</span><span class="sxs-lookup"><span data-stu-id="72a88-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="72a88-141">Voit tarvittaessa muokata luetteloita, jotka on luotu algoritmien avulla.</span><span class="sxs-lookup"><span data-stu-id="72a88-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="72a88-142">Jos tuote poistetaan suositusluettelosta, se löytyy yhä myymälästä.</span><span class="sxs-lookup"><span data-stu-id="72a88-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="72a88-143">Lisätietoja tuotesuositusten tulosten muokkaamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvien tuotesuositusten tulosten hallinta](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="72a88-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="72a88-144">Jos haluat estää nimikkeen löytymisen myymälästä, muuta **Nimikelajitelma**-kohdan arvoksi **Sulje pois**.</span><span class="sxs-lookup"><span data-stu-id="72a88-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="72a88-145">Miten voin lisätä luettelon sähköisen kaupankäynnin sivulle?</span><span class="sxs-lookup"><span data-stu-id="72a88-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="72a88-146">Lisätietoja tuotesuositussivujen lisäämisestä sähköisen kaupankäynnin sivustoon on kohdassa [Tuotesuositusluetteloiden lisääminen sivuille](add-reco-list-to-page.md).</span><span class="sxs-lookup"><span data-stu-id="72a88-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="72a88-147">Miten otan käyttöön suositukset myyntipisteellä?</span><span class="sxs-lookup"><span data-stu-id="72a88-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="72a88-148">Kun olet ottanut käyttöön tuotesuositukset, sinun on lisättävä suositusten paneeli ohjausobjektin myyntipistenäyttöön.</span><span class="sxs-lookup"><span data-stu-id="72a88-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="72a88-149">Lisätietoja on kohdassa [Suositusten ohjausobjektin lisääminen tapahtumanäyttöön myyntipistelaitteissa](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="72a88-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72a88-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="72a88-150">Additional resources</span></span>

[<span data-ttu-id="72a88-151">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="72a88-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="72a88-152">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="72a88-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="72a88-153">Tuotesuositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="72a88-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="72a88-154">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="72a88-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="72a88-155">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="72a88-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="72a88-156">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="72a88-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="72a88-157">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="72a88-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="72a88-158">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="72a88-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="72a88-159">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="72a88-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="72a88-160">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="72a88-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)
