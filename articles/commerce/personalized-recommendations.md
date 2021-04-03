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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: be460ec5ce8a9a625dc1a80f761bea9e2ab2f632
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477657"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="255f9-103">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="255f9-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="255f9-104">Tässä ohjeaiheessa kuvataan, miten mukautettuja tuotesuosituksia voidaan käyttää Microsoft Dynamics 365 Commerce -asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="255f9-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="255f9-105">Dynamics 365 Commerce -ohjelmassa jälleenmyyjät voivat tehdä mukautettuja tuotesuosituksia (eli personointeja).</span><span class="sxs-lookup"><span data-stu-id="255f9-105">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="255f9-106">Näin henkilökohtaiset suositukset voidaan sisällyttää asiakaskokemukseen verkossa ja myyntipisteessä (POS).</span><span class="sxs-lookup"><span data-stu-id="255f9-106">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="255f9-107">Kun mukautustoiminto on käytössä, järjestelmä voi liittää käyttäjän osto- ja tuotetiedot ja luoda yksilöllisiä tuotesuosituksia.</span><span class="sxs-lookup"><span data-stu-id="255f9-107">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="255f9-108">Mukauttamisen edellytykset</span><span class="sxs-lookup"><span data-stu-id="255f9-108">Personalization prerequisites</span></span>

<span data-ttu-id="255f9-109">Ennen kuin teet mukautettuja tuotesuosituksia asiakkaiden käyttöön, huomaa, että tuotesuosituksia tuetaan vain niiden Commerce-käyttäjien osalta, jotka ovat siirtyneet käyttämään tallennustilaa Azure Data Lake -säilössä.</span><span class="sxs-lookup"><span data-stu-id="255f9-109">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="255f9-110">Ennen kuin asiakkaat voivat vastaanottaa mukautettuja tuotesuosituksia, jälleenmyyjien on [otettava tuotesuositukset käyttöön](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="255f9-110">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="255f9-111">Ottamalla käyttöön tuotesuositukset otat myös mukauttamisen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="255f9-111">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="255f9-112">Jos kuitenkin poistat mukauttamisen käytöstä, et poista käytöstä muita tuotesuosituksia.</span><span class="sxs-lookup"><span data-stu-id="255f9-112">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="255f9-113">Lisätietoja tuotesuosituksista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="255f9-113">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="255f9-114">Ota käyttöön mukautukset</span><span class="sxs-lookup"><span data-stu-id="255f9-114">Turn on personalization</span></span>

<span data-ttu-id="255f9-115">Mukautukset otetaan käyttöön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="255f9-115">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="255f9-116">Hae **Ominaisuuksien hallinta** Commercen pääkonttoriversiossa.</span><span class="sxs-lookup"><span data-stu-id="255f9-116">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="255f9-117">Avaa käytettävissä olevien ominaisuuksien luettelo valitsemalla **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="255f9-117">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="255f9-118">Kirjoita hakuruutuun **Suositukset**.</span><span class="sxs-lookup"><span data-stu-id="255f9-118">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="255f9-119">Valitse **Kohdennetut tuotesuositukset** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="255f9-119">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="255f9-120">Valitse **Kohdennetut tuotesuositukset** -ominaisuusruudussa **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="255f9-120">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Mukautusten ottaminen käyttöön](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="255f9-122">Kun mukautus otetaan käyttöön, mukautettujen tuotesuositusluetteloiden luontiprosessi aloitetaan.</span><span class="sxs-lookup"><span data-stu-id="255f9-122">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="255f9-123">Enintään yksi päivä saattaa olla tarpeen, ennen kuin nämä luettelot ovat käytettävissä ja näkyvissä verkossa ja POS-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="255f9-123">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="255f9-124">Mukautetut luettelot</span><span class="sxs-lookup"><span data-stu-id="255f9-124">Personalized lists</span></span>

<span data-ttu-id="255f9-125">Tietokoneella luotujen luetteloiden mukautuksen lisäksi suosituspalvelu mahdollistaa tuotekehityskokemuksen mukauttamisen sekä verkossa että myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="255f9-125">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="255f9-126">Kun mukauttaminen on otettu käyttöön, jälleenmyyjät voivat näyttää asiakkaan henkilökohtaiset poiminnat -luettelot online-tilassa tai Suositeltava asiakkaalle -luetteloissa kassapäätteissä.</span><span class="sxs-lookup"><span data-stu-id="255f9-126">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="255f9-127">Lisäksi jälleenmyyjät voivat soveltaa mukauttamista olemassa oleviin tuotesuositusluetteloihin ja tarjota todennettujen käyttäjien yleisiä tietosuojasäännöksiä (GDPR).</span><span class="sxs-lookup"><span data-stu-id="255f9-127">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="255f9-128">Jos poistat mukauttamisen käytöstä, poistat myös nämä ominaisuudet käytöstä.</span><span class="sxs-lookup"><span data-stu-id="255f9-128">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="255f9-129">Poiminnat sinulle -luettelot verkosta</span><span class="sxs-lookup"><span data-stu-id="255f9-129">Online "Picks for you" lists</span></span>

<span data-ttu-id="255f9-130">Poimittu sinulle -luettelo on tekoälykoneoppimisluettelo (AI-ML), joka näyttää todennetun käyttäjän mukautetun luettelon ehdotetuista tuotteista.</span><span class="sxs-lookup"><span data-stu-id="255f9-130">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="255f9-131">Tämä luettelo perustuu käyttäjän monikanavaiseen ostohistoriaan.</span><span class="sxs-lookup"><span data-stu-id="255f9-131">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="255f9-132">Mukautetut suositukset päivitetään dynaamisesti, kun käyttäjä tekee enemmän ostoksia.</span><span class="sxs-lookup"><span data-stu-id="255f9-132">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="255f9-133">Tämäntyyppinen luettelo tukee myös luokkasuodatusta, jolloin vähittäiskauppiaat voivat näyttää siirtymishierarkioiden perusteella parhaimmistoa.</span><span class="sxs-lookup"><span data-stu-id="255f9-133">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="255f9-134">Ennen kuin Poiminnat sinulle -luettelo voi näkyä verkkokaupan sivulla, seuraavien käyttäjävaatimusten on täytyttävä:</span><span class="sxs-lookup"><span data-stu-id="255f9-134">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="255f9-135">Käyttäjien on oltava kirjautuneena sisään.</span><span class="sxs-lookup"><span data-stu-id="255f9-135">Users must be signed in.</span></span> <span data-ttu-id="255f9-136">Anonyymit käyttäjät eivät näe mukautettuja suosituksia.</span><span class="sxs-lookup"><span data-stu-id="255f9-136">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="255f9-137">Käyttäjillä on oltava vähintään yksi osto tilillään.</span><span class="sxs-lookup"><span data-stu-id="255f9-137">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="255f9-138">Käyttäjien on valittava, jotta he saavat henkilökohtaisia suosituksia.</span><span class="sxs-lookup"><span data-stu-id="255f9-138">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="255f9-139">Seuraavassa kuvassa on esimerkki verkkokaupan sivulla olevasta Poiminnat sinulle -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="255f9-139">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Poiminnat sinulle -luettelot verkosta](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="255f9-141">Suositeltava asiakkaalle-luettelot POS-sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="255f9-141">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="255f9-142">Vähittäiskauppiaat voivat mukauttaa aiemmin luotuja asiakastietosivuja ja lisätä niiden clienteling-kokemusta lisäämällä asia yhteyteen Suositeltava asiakkaalle -luettelon.</span><span class="sxs-lookup"><span data-stu-id="255f9-142">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="255f9-143">Seuraavassa kuvassa on esimerkki kassapäätteessä olevasta Suositeltu asiakkaalle -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="255f9-143">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Suositeltava asiakkaalle -luettelot POS-sovelluksessa](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="255f9-145">Käytä mukauttamista aiemmin luotuihin suositusluetteloihin</span><span class="sxs-lookup"><span data-stu-id="255f9-145">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="255f9-146">Jälleenmyyjät voivat soveltaa mukauttamista aiemmin luotuihin suositusluetteloihin, kuten Uusi, Trendit, Myydyin, Ihmiset pitivät myös ja Usein ostetut yhdessä.</span><span class="sxs-lookup"><span data-stu-id="255f9-146">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="255f9-147">Kun mukauttamista käytetään aiemmin luoduissa luetteloissa, nimikkeet, jotka on aiemmin ostettu kirjautuneen käyttäjän toimesta, poistetaan näistä luetteloista.</span><span class="sxs-lookup"><span data-stu-id="255f9-147">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="255f9-148">Sekä anonyymeille käyttäjille että käyttäjille, jotka ovat jättäytymässä yksilöllisten suositusten vastaanottamisesta, näytetään aiemmin luotujen luetteloiden oletusversiot.</span><span class="sxs-lookup"><span data-stu-id="255f9-148">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="255f9-149">Siksi vähittäiskauppiaiden ei tarvitse ylläpitää erillisiä sivukokemuksia manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="255f9-149">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="255f9-150">Esimerkiksi kirjautuneena oleva käyttäjä on jo ostanut mustan kellon ja ruskeat työsaappaat, jotka näkyvät seuraavassa kuvassa Trendit - oletus -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="255f9-150">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="255f9-151">Siksi käyttäjä näkee uusia tuotteita näiden tuotteiden sijasta, kuten Trendit - mukautettu -luettelossa näkyy.</span><span class="sxs-lookup"><span data-stu-id="255f9-151">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Mukauttamisen ottaminen käyttöön](./media/applypersonalization.png)

<span data-ttu-id="255f9-153">Jos haluat käyttää mukauttamista aiemmin luotuun suositusluetteloon Commercen sivustonluontityökalussa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="255f9-153">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="255f9-154">Avaa aiemmin luotu sivustonluontisivu, joka sisältää tuotekokoelmamoduulin.</span><span class="sxs-lookup"><span data-stu-id="255f9-154">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="255f9-155">Valitse vasemmasta siirtymisruudusta tuotekokoelmamoduuli.</span><span class="sxs-lookup"><span data-stu-id="255f9-155">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="255f9-156">Valitse luettelo oikeanpuoleisessa siirtymisruudussa **Tuotteet**-kohdan alta.</span><span class="sxs-lookup"><span data-stu-id="255f9-156">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="255f9-157">Valitse luettelotyyppi **Valitse tuoteluettelon konfigurointi** -valintaikkunan **Tyyppi**-kohdasta.</span><span class="sxs-lookup"><span data-stu-id="255f9-157">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="255f9-158">Valitse **Käytä mukauttamista** -valintaruutu ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="255f9-158">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Mukauttamisen kohdistaminen trendiluetteloon](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="255f9-160">Tallenna sivu, lopeta sen muokkaus ja sitten julkaise se.</span><span class="sxs-lookup"><span data-stu-id="255f9-160">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="255f9-161">Kun sivu on julkaistu, kirjautuneet käyttäjät näkevät mukautetut trendiluettelot.</span><span class="sxs-lookup"><span data-stu-id="255f9-161">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="255f9-162">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="255f9-162">Additional resources</span></span>

[<span data-ttu-id="255f9-163">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="255f9-163">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="255f9-164">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="255f9-164">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="255f9-165">Ota tuotesuositukset käyttöön</span><span class="sxs-lookup"><span data-stu-id="255f9-165">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="255f9-166">"Osta samankaltaisia tyylejä" -suositusten käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="255f9-166">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="255f9-167">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="255f9-167">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="255f9-168">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="255f9-168">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="255f9-169">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="255f9-169">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="255f9-170">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="255f9-170">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="255f9-171">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="255f9-171">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="255f9-172">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="255f9-172">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="255f9-173">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="255f9-173">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
