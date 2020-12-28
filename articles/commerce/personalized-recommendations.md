---
title: Ota käyttöön kohdennetut tuotesuositukset
description: Tässä ohjeaiheessa kuvataan, miten mukautettuja tuotesuosituksia voidaan käyttää Microsoft Dynamics 365 Commerce -asiakkaille.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8a61ef0720839d371701f2f0a1fdec7e85a5feb7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411942"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="0ba8a-103">Ota käyttöön kohdennetut tuotesuositukset</span><span class="sxs-lookup"><span data-stu-id="0ba8a-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0ba8a-104">Tässä ohjeaiheessa kuvataan, miten mukautettuja tuotesuosituksia voidaan käyttää Microsoft Dynamics 365 Commerce -asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0ba8a-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0ba8a-105">Overview</span></span>

<span data-ttu-id="0ba8a-106">Dynamics 365 Commerce -ohjelmassa jälleenmyyjät voivat tehdä mukautettuja tuotesuosituksia (eli personointeja).</span><span class="sxs-lookup"><span data-stu-id="0ba8a-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="0ba8a-107">Näin henkilökohtaiset suositukset voidaan sisällyttää asiakaskokemukseen verkossa ja myyntipisteessä (POS).</span><span class="sxs-lookup"><span data-stu-id="0ba8a-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="0ba8a-108">Kun mukautustoiminto on käytössä, järjestelmä voi liittää käyttäjän osto- ja tuotetiedot ja luoda yksilöllisiä tuotesuosituksia.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="0ba8a-109">Mukauttamisen edellytykset</span><span class="sxs-lookup"><span data-stu-id="0ba8a-109">Personalization prerequisites</span></span>

<span data-ttu-id="0ba8a-110">Ennen kuin teet mukautettuja tuotesuosituksia asiakkaiden käyttöön, huomaa, että tuotesuosituksia tuetaan vain niiden Commerce-käyttäjien osalta, jotka ovat siirtyneet käyttämään tallennustilaa Azure Data Lake -säilössä.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="0ba8a-111">Ennen kuin asiakkaat voivat vastaanottaa mukautettuja tuotesuosituksia, jälleenmyyjien on [otettava tuotesuositukset käyttöön](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="0ba8a-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="0ba8a-112">Ottamalla käyttöön tuotesuositukset otat myös mukauttamisen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="0ba8a-113">Jos kuitenkin poistat mukauttamisen käytöstä, et poista käytöstä muita tuotesuosituksia.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="0ba8a-114">Lisätietoja tuotesuosituksista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="0ba8a-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="0ba8a-115">Ota käyttöön mukautukset</span><span class="sxs-lookup"><span data-stu-id="0ba8a-115">Turn on personalization</span></span>

<span data-ttu-id="0ba8a-116">Mukautukset otetaan käyttöön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="0ba8a-117">Hae **Ominaisuuksien hallinta** Commercen pääkonttoriversiossa.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-117">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="0ba8a-118">Avaa käytettävissä olevien ominaisuuksien luettelo valitsemalla **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-118">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="0ba8a-119">Kirjoita hakuruutuun **Suositukset**.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-119">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="0ba8a-120">Valitse **Kohdennetut tuotesuositukset** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-120">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="0ba8a-121">Valitse **Kohdennetut tuotesuositukset** -ominaisuusruudussa **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-121">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Mukautusten ottaminen käyttöön](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="0ba8a-123">Kun mukautus otetaan käyttöön, mukautettujen tuotesuositusluetteloiden luontiprosessi aloitetaan.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-123">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="0ba8a-124">Enintään yksi päivä saattaa olla tarpeen, ennen kuin nämä luettelot ovat käytettävissä ja näkyvissä verkossa ja POS-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-124">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="0ba8a-125">Mukautetut luettelot</span><span class="sxs-lookup"><span data-stu-id="0ba8a-125">Personalized lists</span></span>

<span data-ttu-id="0ba8a-126">Tietokoneella luotujen luetteloiden mukautuksen lisäksi suosituspalvelu mahdollistaa tuotekehityskokemuksen mukauttamisen sekä verkossa että myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-126">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="0ba8a-127">Kun mukauttaminen on otettu käyttöön, jälleenmyyjät voivat näyttää asiakkaan henkilökohtaiset poiminnat -luettelot online-tilassa tai Suositeltava asiakkaalle -luetteloissa kassapäätteissä.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-127">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="0ba8a-128">Lisäksi jälleenmyyjät voivat soveltaa mukauttamista olemassa oleviin tuotesuositusluetteloihin ja tarjota todennettujen käyttäjien yleisiä tietosuojasäännöksiä (GDPR).</span><span class="sxs-lookup"><span data-stu-id="0ba8a-128">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="0ba8a-129">Jos poistat mukauttamisen käytöstä, poistat myös nämä ominaisuudet käytöstä.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-129">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="0ba8a-130">Poiminnat sinulle -luettelot verkosta</span><span class="sxs-lookup"><span data-stu-id="0ba8a-130">Online "Picks for you" lists</span></span>

<span data-ttu-id="0ba8a-131">Poimittu sinulle -luettelo on tekoälykoneoppimisluettelo (AI-ML), joka näyttää todennetun käyttäjän mukautetun luettelon ehdotetuista tuotteista.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-131">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="0ba8a-132">Tämä luettelo perustuu käyttäjän monikanavaiseen ostohistoriaan.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-132">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="0ba8a-133">Mukautetut suositukset päivitetään dynaamisesti, kun käyttäjä tekee enemmän ostoksia.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-133">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="0ba8a-134">Tämäntyyppinen luettelo tukee myös luokkasuodatusta, jolloin vähittäiskauppiaat voivat näyttää siirtymishierarkioiden perusteella parhaimmistoa.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-134">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="0ba8a-135">Ennen kuin Poiminnat sinulle -luettelo voi näkyä verkkokaupan sivulla, seuraavien käyttäjävaatimusten on täytyttävä:</span><span class="sxs-lookup"><span data-stu-id="0ba8a-135">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="0ba8a-136">Käyttäjien on oltava kirjautuneena sisään.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-136">Users must be signed in.</span></span> <span data-ttu-id="0ba8a-137">Anonyymit käyttäjät eivät näe mukautettuja suosituksia.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-137">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="0ba8a-138">Käyttäjillä on oltava vähintään yksi osto tilillään.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-138">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="0ba8a-139">Käyttäjien on valittava, jotta he saavat henkilökohtaisia suosituksia.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-139">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="0ba8a-140">Seuraavassa kuvassa on esimerkki verkkokaupan sivulla olevasta Poiminnat sinulle -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-140">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Poiminnat sinulle -luettelot verkosta](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="0ba8a-142">Suositeltava asiakkaalle-luettelot POS-sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="0ba8a-142">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="0ba8a-143">Vähittäiskauppiaat voivat mukauttaa aiemmin luotuja asiakastietosivuja ja lisätä niiden clienteling-kokemusta lisäämällä asia yhteyteen Suositeltava asiakkaalle -luettelon.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-143">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="0ba8a-144">Seuraavassa kuvassa on esimerkki kassapäätteessä olevasta Suositeltu asiakkaalle -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-144">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Suositeltava asiakkaalle -luettelot POS-sovelluksessa](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="0ba8a-146">Käytä mukauttamista aiemmin luotuihin suositusluetteloihin</span><span class="sxs-lookup"><span data-stu-id="0ba8a-146">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="0ba8a-147">Jälleenmyyjät voivat soveltaa mukauttamista aiemmin luotuihin suositusluetteloihin, kuten Uusi, Trendit, Myydyin, Ihmiset pitivät myös ja Usein ostetut yhdessä.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-147">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="0ba8a-148">Kun mukauttamista käytetään aiemmin luoduissa luetteloissa, nimikkeet, jotka on aiemmin ostettu kirjautuneen käyttäjän toimesta, poistetaan näistä luetteloista.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-148">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="0ba8a-149">Sekä anonyymeille käyttäjille että käyttäjille, jotka ovat jättäytymässä yksilöllisten suositusten vastaanottamisesta, näytetään aiemmin luotujen luetteloiden oletusversiot.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-149">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="0ba8a-150">Siksi vähittäiskauppiaiden ei tarvitse ylläpitää erillisiä sivukokemuksia manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-150">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="0ba8a-151">Esimerkiksi kirjautuneena oleva käyttäjä on jo ostanut mustan kellon ja ruskeat työsaappaat, jotka näkyvät seuraavassa kuvassa Trendit - oletus -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-151">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="0ba8a-152">Siksi käyttäjä näkee uusia tuotteita näiden tuotteiden sijasta, kuten Trendit - mukautettu -luettelossa näkyy.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-152">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Mukauttamisen ottaminen käyttöön](./media/applypersonalization.png)

<span data-ttu-id="0ba8a-154">Jos haluat käyttää mukauttamista aiemmin luotuun suositusluetteloon Commercen sivustonluontityökalussa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-154">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0ba8a-155">Avaa aiemmin luotu sivustonluontisivu, joka sisältää tuotekokoelmamoduulin.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-155">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="0ba8a-156">Valitse vasemmasta siirtymisruudusta tuotekokoelmamoduuli.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-156">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="0ba8a-157">Valitse luettelo oikeanpuoleisessa siirtymisruudussa **Tuotteet**-kohdan alta.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-157">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="0ba8a-158">Valitse luettelotyyppi **Valitse tuoteluettelon konfigurointi** -valintaikkunan **Tyyppi**-kohdasta.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-158">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="0ba8a-159">Valitse **Käytä mukauttamista** -valintaruutu ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-159">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Mukauttamisen kohdistaminen trendiluetteloon](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="0ba8a-161">Tallenna sivu, lopeta sen muokkaus ja sitten julkaise se.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-161">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="0ba8a-162">Kun sivu on julkaistu, kirjautuneet käyttäjät näkevät mukautetut trendiluettelot.</span><span class="sxs-lookup"><span data-stu-id="0ba8a-162">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ba8a-163">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0ba8a-163">Additional resources</span></span>

[<span data-ttu-id="0ba8a-164">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0ba8a-164">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="0ba8a-165">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="0ba8a-165">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="0ba8a-166">Ota tuotesuositukset käyttöön</span><span class="sxs-lookup"><span data-stu-id="0ba8a-166">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="0ba8a-167">"Osta samankaltaisia tyylejä" -suositusten käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="0ba8a-167">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="0ba8a-168">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="0ba8a-168">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="0ba8a-169">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="0ba8a-169">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="0ba8a-170">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="0ba8a-170">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="0ba8a-171">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="0ba8a-171">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="0ba8a-172">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="0ba8a-172">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="0ba8a-173">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="0ba8a-173">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="0ba8a-174">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="0ba8a-174">Product recommendations FAQ</span></span>](faq-recommendations.md)
