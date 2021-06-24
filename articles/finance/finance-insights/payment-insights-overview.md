---
title: Asiakkaan maksuennusteet (esiversio)
description: Tässä ohjeaiheessa kerrotaan maksuennusteiden ominaisuudesta. Sen avulla saat lisätietoja asiakkaan tyypillisistä maksutavoista. Tämän toiminnon avulla voit myös määrittää olosuhteet, joiden vuoksi perintäprosessit ehkä aloitetaan normaalia aikaisemmin.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 84a2342d76dc309fa1fd3de7b2c3de60e62e4d72
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186393"
---
# <a name="customer-payment-predictions-preview"></a><span data-ttu-id="49754-104">Asiakkaan maksuennusteet (esiversio)</span><span class="sxs-lookup"><span data-stu-id="49754-104">Customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="49754-105">Tässä ohjeaiheessa kerrotaan maksuennusteiden ominaisuudesta. Sen avulla saat lisätietoja asiakkaan tyypillisistä maksutavoista.</span><span class="sxs-lookup"><span data-stu-id="49754-105">This topic describes the payment predictions capability that can help you better understand a customer's typical payment practices.</span></span> <span data-ttu-id="49754-106">Tämän toiminnon avulla voit myös määrittää olosuhteet, joiden vuoksi perintäprosessit ehkä aloitetaan normaalia aikaisemmin.</span><span class="sxs-lookup"><span data-stu-id="49754-106">This feature can also help identify circumstances that should cause you to start collections processes earlier than you might otherwise start them.</span></span>

## <a name="overview"></a><span data-ttu-id="49754-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="49754-107">Overview</span></span>

<span data-ttu-id="49754-108">Organisaatiot pitävät usein haastavana ennustaa milloin asiakkaat maksavat laskut.</span><span class="sxs-lookup"><span data-stu-id="49754-108">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="49754-109">Tiedonpuute voi aiheuttaa seuraavia ongelmia:</span><span class="sxs-lookup"><span data-stu-id="49754-109">This lack of insight can cause the following issues:</span></span>

- <span data-ttu-id="49754-110">Vähemmän tarkkoja kassavirtaennusteita</span><span class="sxs-lookup"><span data-stu-id="49754-110">Less accurate cash flow forecasts</span></span>
- <span data-ttu-id="49754-111">Liian myöhään alkavat perintäprosessit</span><span class="sxs-lookup"><span data-stu-id="49754-111">Collections processes that start too late</span></span>
- <span data-ttu-id="49754-112">Tilausten vapauttaminen asiakkaille, jotka voivat jättää laskut maksamatta</span><span class="sxs-lookup"><span data-stu-id="49754-112">Orders that are released to customers who might default on their payment</span></span>

<span data-ttu-id="49754-113">Asiakkaan maksuennusteet (esiversio) auttaa organisaatioita ennustamaan, milloin myyntilasku maksetaan.</span><span class="sxs-lookup"><span data-stu-id="49754-113">Customer payment predictions (preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="49754-114">Näin voidaan luoda perintästrategioita, joiden avulla voidaan nostaa ajoissa maksamisen todennäköisyyttä.</span><span class="sxs-lookup"><span data-stu-id="49754-114">Therefore, they can create collections strategies that help increase the likelihood that they will be paid on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="49754-115">Ennusteet</span><span class="sxs-lookup"><span data-stu-id="49754-115">Predictions</span></span>

<span data-ttu-id="49754-116">Maksuennusteiden avulla organisaatiot voivat parantaa liiketoimintaprosesseja. Ennusteet auttavat tunnistamaan laskut, jotka todennäköisesti maksetaan myöhässä.</span><span class="sxs-lookup"><span data-stu-id="49754-116">Payment predictions let organizations improve their business processes by helping them identify the invoices that are likely to be paid late.</span></span> <span data-ttu-id="49754-117">Organisaatio voi käyttää näitä tietoja sellaisten toimintojen yhteydessä, jotka parantavat ajoissa maksamista.</span><span class="sxs-lookup"><span data-stu-id="49754-117">Organization can use that information to take actions that improve the chances that they will be paid on time.</span></span>

<span data-ttu-id="49754-118">Asiakkaan maksuennusteet -toiminto käyttää koneoppimismallia. Sen avulla voidaan tarkasti ennustaa, milloin asiakas maksaa maksamattoman laskun.</span><span class="sxs-lookup"><span data-stu-id="49754-118">The Customer payment predictions feature uses a machine learning model to more accurately predict when a customer will pay an outstanding invoice.</span></span> <span data-ttu-id="49754-119">Tämä koneoppimismalli sisältää aiempia laskuja, maksuja ja asiakastietoja.</span><span class="sxs-lookup"><span data-stu-id="49754-119">This machine learning model includes historical invoices, payments, and customer data.</span></span>

<span data-ttu-id="49754-120">Toiminto määrittää jokaiselle avoimelle laskulle kolme maksutodennäköisyyttä:</span><span class="sxs-lookup"><span data-stu-id="49754-120">For each open invoice, the feature assigns three payment probabilities:</span></span>

- <span data-ttu-id="49754-121">Todennäköisyys, että maksun suorittaminen tapahtuu ajoissa</span><span class="sxs-lookup"><span data-stu-id="49754-121">The probability that the payment will be made on time</span></span>
- <span data-ttu-id="49754-122">Todennäköisyys, että maksun suorittaminen tapahtuu myöhässä</span><span class="sxs-lookup"><span data-stu-id="49754-122">The probability that the payment will be made late</span></span>
- <span data-ttu-id="49754-123">Todennäköisyys, että maksun suorittaminen tapahtuu erittäin paljon myöhässä</span><span class="sxs-lookup"><span data-stu-id="49754-123">The probability that the payment will be made very late</span></span>

<span data-ttu-id="49754-124">Toiminto sisältää myös odotettujen maksujen koostetun näkymän.</span><span class="sxs-lookup"><span data-stu-id="49754-124">The feature also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="49754-125">[![Maksuennusteiden koostenäkymä](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="49754-125">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="49754-126">Kullekin laskulle määritetään todennäköisyys ajoissa maksamisesta.</span><span class="sxs-lookup"><span data-stu-id="49754-126">Each invoice is assigned a probability of on-time payment.</span></span> <span data-ttu-id="49754-127">Laskut, joiden ajoissa maksamisen todennäköisyys on alle 50 prosenttia, merkitään punaisella ympyrällä. Se osoittaa, että ne ehkä tarvitsevat perintäasiamiehen huomiota.</span><span class="sxs-lookup"><span data-stu-id="49754-127">Invoices that have a probability of on-time payment that is less than 50 percent are tagged with a red circle to indicate that they might require attention from a collections agent.</span></span>

<span data-ttu-id="49754-128">[![Maksun todennäköisyyksien luettelo](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="49754-128">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="49754-129">Asiakkaan maksuennusteiden toiminto sisältää myös tilannekohtaista tietoa, joka selittää ennustusta.</span><span class="sxs-lookup"><span data-stu-id="49754-129">The Customer payment predictions feature also provides contextual information to explain the prediction.</span></span> <span data-ttu-id="49754-130">Nämä tiedot sisältävät ennusteeseen vaikuttaneet tärkeimmät tekijät, asiakkaan liikesuhteen nykyisen tilan ja tietoja asiakkaan aiemmasta maksutoiminnasta.</span><span class="sxs-lookup"><span data-stu-id="49754-130">This information includes the top factors that influenced the prediction, the current state of business with the customer, and details about the customer's historical payment behavior.</span></span>

<span data-ttu-id="49754-131">Monissa yrityksissä perintäprosessi on ollut reaktiivinen toiminto.</span><span class="sxs-lookup"><span data-stu-id="49754-131">In many businesses, the collections process has been a reactive activity.</span></span> <span data-ttu-id="49754-132">Toisin sanoen perintäprosessi ei käynnisty, ennen kuin laskut erääntyvät.</span><span class="sxs-lookup"><span data-stu-id="49754-132">In other words, the collections process doesn't start until invoices become due.</span></span> <span data-ttu-id="49754-133">Asiakkaan maksuennusteiden avulla organisaatiot voivat olla proaktiivisempia perinnän suhteen.</span><span class="sxs-lookup"><span data-stu-id="49754-133">Customer payment predictions let organizations be more proactive about collections.</span></span> <span data-ttu-id="49754-134">Niiden ei enää tarvitse odottaa, että tapahtuma erääntyy, ennen kuin perintäprosessi aloitetaan.</span><span class="sxs-lookup"><span data-stu-id="49754-134">They no longer have to wait for a transaction to become due to start the collections process.</span></span> <span data-ttu-id="49754-135">Sen sijaan ne voivat selvittää maksuennusteiden ominaisuuden avulla, parantaako ennakkoiva perintä todennäköisyyttä ajoissa tapahtuvasta maksun maksamisesta.</span><span class="sxs-lookup"><span data-stu-id="49754-135">Instead, they can use the payment predictions capability to determine whether proactive collections will improve the probability that they will be paid on time.</span></span>

## <a name="methodology"></a><span data-ttu-id="49754-136">Metodologia</span><span class="sxs-lookup"><span data-stu-id="49754-136">Methodology</span></span>

<span data-ttu-id="49754-137">Aiemmin on yleensä ollut vaikeaa kehittää ja käyttää tekoälyratkaisuja.</span><span class="sxs-lookup"><span data-stu-id="49754-137">In the past, it has typically been difficult to develop and deploy an artificial intelligence (AI) solution.</span></span> <span data-ttu-id="49754-138">Tämä prosessi vaati tiimin, joka sisältää datatieteilijöitä, aihealueen asiantuntijoita ja teknikoita, jotka käyttävät paljon aikaa käyttökelpoisen tekoälyratkaisun muotoiluun, kehittämiseen, käyttöönottamiseen ja ylläpitoon.</span><span class="sxs-lookup"><span data-stu-id="49754-138">The process has required a team that includes data scientists, subject matter experts (SMEs), and engineers, who work over time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="49754-139">Asiakkaan maksuennusteiden avulla on helppo ottaa käyttöön ja käyttää tekoälysovellusta Microsoft Dynamics 365 Financessa.</span><span class="sxs-lookup"><span data-stu-id="49754-139">Customer payment predictions makes it easy to deploy and use an AI solution in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="49754-140">Microsoft toimittaa valmiiksi pakattuja tekoälyratkaisuja, jotka on muodostettu Microsoft AI Builderin pohjalta.</span><span class="sxs-lookup"><span data-stu-id="49754-140">Microsoft is prepackaging AI solutions that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="49754-141">Tämän vuoksi käyttäjät voivat ottaa tekoälysovelluksen käyttöön yhdellä hiiren napsautuksella. Näin he saavat käyttöönsä älykkäät ennusteet.</span><span class="sxs-lookup"><span data-stu-id="49754-141">Therefore, users can deploy the AI solution in a single mouse click to take advantage of the benefits of intelligent predictions.</span></span> <span data-ttu-id="49754-142">Jos et ole tyytyväinen ennusteiden tarkkuuteen, tehokäyttäjä voi lisätä (jälleen yhdellä hiiren napsautuksella) AI Builderin laajennuskokemuksen ja sitten valita ennusteiden muodostamiseen käytettäviä kenttiä tai poistaa niiden valinnan.</span><span class="sxs-lookup"><span data-stu-id="49754-142">If you aren't satisfied with the accuracy of predictions, a power user can (again, in a single mouse click) enter the AI Builder extension experience, and then select or clear the fields that are used to generate predictions.</span></span> <span data-ttu-id="49754-143">Kun olet valmis, voit kouluttaa mallia ja julkaista muutokset.</span><span class="sxs-lookup"><span data-stu-id="49754-143">When you're ready, you can "train" the model and publish the changes.</span></span> <span data-ttu-id="49754-144">Juuri koulutettu malli valitaan automaattisesti ja ennusteet luodan Dynamics 365 Financessa.</span><span class="sxs-lookup"><span data-stu-id="49754-144">The newly trained model will automatically be picked up to generate predictions in Dynamics 365 Finance.</span></span>

## <a name="release-details"></a><span data-ttu-id="49754-145">Julkaisun tiedot</span><span class="sxs-lookup"><span data-stu-id="49754-145">Release details</span></span>

<span data-ttu-id="49754-146">Finance Insightsin julkinen esiversio on saatavilla käyttöönotoissa kokeilua varten Yhdysvalloissa, Euroopassa ja Yhdistyneessä kuningaskunnassa.</span><span class="sxs-lookup"><span data-stu-id="49754-146">Finance Insights public preview is available to try for deployments in the United States of America, Europe, and United Kingdom.</span></span> <span data-ttu-id="49754-147">Microsoft lisää tukea jatkuvasti myös muilla alueilla.</span><span class="sxs-lookup"><span data-stu-id="49754-147">Microsoft is incrementally adding support for additional regions.</span></span>

<span data-ttu-id="49754-148">Julkisen esiversion ominaisuudet tulee ottaa käyttöön vain Taso 2 -eristysympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="49754-148">Public preview features should be turned on only in Tier 2 sandbox environments.</span></span> <span data-ttu-id="49754-149">Eristysympäristössä luotuja määrityksiä ja tekoälymalleja ei ehkä siirretä tuotantoympäristöön.</span><span class="sxs-lookup"><span data-stu-id="49754-149">Setup and AI models that are created in a sandbox environment might not be migrated to the production environment.</span></span> <span data-ttu-id="49754-150">Lisätietoja on kohdassa [Microsoft Dynamics 365 -esiversioiden lisäkäyttöehdot](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="49754-150">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
