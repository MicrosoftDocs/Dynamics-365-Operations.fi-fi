---
title: Perinnän hallinnan keskeiset käsitteet
description: Ohjeaiheessa käsitellään perinnän hallinnan keskeisiä käsitteitä.
author: mikefalkner
manager: AnnBe
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7d6f49939807102cc6c29bd50674a5e58e2b1b66
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015202"
---
# <a name="collections-management-key-concepts"></a><span data-ttu-id="32b19-103">Perinnän hallinnan keskeiset käsitteet</span><span class="sxs-lookup"><span data-stu-id="32b19-103">Collections management key concepts</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="32b19-104">Ennen kuin aloitat perinnän määrittämisen tai perinnän käyttämisen, on hyvä ymmärtää seuraavat käsitteet:</span><span class="sxs-lookup"><span data-stu-id="32b19-104">Before you start to set up or work with collections, you should understand the following concepts:</span></span>

- <span data-ttu-id="32b19-105">Asiakkaan erääntymistilannevedokset sisältävät erääntyneet saldotiedot tietyltä aikajaksolta.</span><span class="sxs-lookup"><span data-stu-id="32b19-105">Customer aging snapshots contain aged balance information at a specific point in time.</span></span>
- <span data-ttu-id="32b19-106">Perinnän asiakaspoolit helpottavat työn organisointia.</span><span class="sxs-lookup"><span data-stu-id="32b19-106">Collections customer pools help you organize your work.</span></span>
- <span data-ttu-id="32b19-107">Perimisasiamiehet voivat ylläpitää omia asiakaspoolejaan.</span><span class="sxs-lookup"><span data-stu-id="32b19-107">Collections agents can have their own customer pools.</span></span>
- <span data-ttu-id="32b19-108">Luettelosivuilla voi järjestää perinnän asiakkaita, tehtäviä ja tapauksia.</span><span class="sxs-lookup"><span data-stu-id="32b19-108">List pages organize collections customers, activities, and cases.</span></span>
- <span data-ttu-id="32b19-109">Kaikki asiakkaan perintätiedot yhdellä sivulla, jolta voit ryhtyä toimenpiteisiin.</span><span class="sxs-lookup"><span data-stu-id="32b19-109">All collections information for a customer is on one page, and you can take action from that page.</span></span>
- <span data-ttu-id="32b19-110">Korkojen ja maksujen peruuttaminen, palauttaminen tai kääntäminen yhdellä toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="32b19-110">Interest and fees can be waived, reinstated, or reversed in one step.</span></span>
- <span data-ttu-id="32b19-111">Poistotapahtumia voidaan luoda yhdessä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="32b19-111">Write-off transactions can be created in one step.</span></span>
- <span data-ttu-id="32b19-112">Ei katetta (NSF) -maksut voidaan käsitellä yhdessä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="32b19-112">Not sufficient funds (NSF) payments can be processed in one step.</span></span>

<span data-ttu-id="32b19-113">Tässä ohjeaiheessa käsitellään kukin käsite.</span><span class="sxs-lookup"><span data-stu-id="32b19-113">This topic describes each concept.</span></span>

## <a name="customer-aging-snapshots"></a><span data-ttu-id="32b19-114">Asiakkaan erääntymistilannevedokset</span><span class="sxs-lookup"><span data-stu-id="32b19-114">Customer aging snapshots</span></span>

<span data-ttu-id="32b19-115">Erääntymistilannevedos sisältää asiakkaan lasketut erääntyneet saldot tiettynä ajankohtana.</span><span class="sxs-lookup"><span data-stu-id="32b19-115">An aging snapshot contains the calculated aged balances for a customer at a specific point in time.</span></span> <span data-ttu-id="32b19-116">Nämä tiedot näytetään **Erääntyneet saldot**-luettelosivulla ja **Perintä**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="32b19-116">This information is shown on the **Aged balances** list page and the **Collections** page.</span></span> <span data-ttu-id="32b19-117">Erääntymistilannevedos on luotava, ennen kuin perinnän luettelosivun tietoja voi tarkastella (**Erääntyneet saldot**, **Perintätehtävät** ja **Perintätapaukset**).</span><span class="sxs-lookup"><span data-stu-id="32b19-117">An aging snapshot must be created before you can view information on the collections list pages (**Aged balances**, **Collections activities**, and **Collections cases**).</span></span>

<span data-ttu-id="32b19-118">Kunkin asiakkaan erääntymistilannevedos sisältää erääntymistilanteen otsikko- ja erittelytietueet, jotka vastaavat kutakin erääntymiskautta erääntymiskauden määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="32b19-118">For each customer, an aging snapshot has an aging snapshot header and detail records that correspond to each aging period in the aging period definition.</span></span>

<span data-ttu-id="32b19-119">Erääntymistilannevedoksen otsikko sisältää asiakkaan tilillä erääntyneen kokonaissumman, luottorajan, pakkausluettelon summan, myyntitilauksen summan, riitautettujen tapahtumien määrän ja riitautettujen tapahtumien kokonaissumman.</span><span class="sxs-lookup"><span data-stu-id="32b19-119">The aging snapshot header contains the total amount that is due, credit limit, packing slip amount, sales order amount, number of disputed transactions, and total amount of the disputed transactions for the customer account.</span></span> <span data-ttu-id="32b19-120">Kaikki tämän asiakkaan tapahtumat sisällytetään näiden summien laskentaan.</span><span class="sxs-lookup"><span data-stu-id="32b19-120">All transactions for the customer are included in the calculation of these amounts.</span></span> <span data-ttu-id="32b19-121">Erääntynyt kokonaissumma, luottoraja, pakkausluettelon summa ja myyntitilauksen summa näytetään **Perintä**-sivun **Luottotiedot**-tietoruudussa.</span><span class="sxs-lookup"><span data-stu-id="32b19-121">The total amount that is due, credit limit, packing slip amount, and sales order amount are shown in the **Credit information** FactBox on the **Collections** page.</span></span>

<span data-ttu-id="32b19-122">Erääntymistilannevedoksen erittelytietue luodaan jokaiselle erääntymiskauden määrittelyyn sisältyvälle erääntymiskaudelle.</span><span class="sxs-lookup"><span data-stu-id="32b19-122">For each aging period in the aging period definition, a detail record is created in the aging snapshot.</span></span> <span data-ttu-id="32b19-123">Kukin erittelytietue sisältää erääntymiskauden tunnuksen sekä tapahtumien kokonaissumman erääntymiskauden päivämääriltä.</span><span class="sxs-lookup"><span data-stu-id="32b19-123">Each detail record contains the ID of the aging period and the total amount of the transactions that have dates in the aging period.</span></span> <span data-ttu-id="32b19-124">Tapahtumat määritetään erääntymiskaudelle, kuten 30 päivää myöhässä.</span><span class="sxs-lookup"><span data-stu-id="32b19-124">Transactions are assigned to an aging period, such as 30 days past due.</span></span> <span data-ttu-id="32b19-125">Päivämäärä on suhteessa **Erääntyy**-päivämäärään, joka määritetään erääntymistilannevedosta luotaessa.</span><span class="sxs-lookup"><span data-stu-id="32b19-125">The date is relative to the **Aging as of** date value that you specify when you create the aging snapshot.</span></span> <span data-ttu-id="32b19-126">Nämä tiedot näytetään **Erääntyneet saldot** -luettelosivulla sekä **Perintä**-sivun **Erääntyneet saldot** -tietoruudussa.</span><span class="sxs-lookup"><span data-stu-id="32b19-126">This information is shown on the **Aged balances** list page and in the **Aged balances** FactBox on the **Collections** page.</span></span>

## <a name="collections-customer-pools"></a><span data-ttu-id="32b19-127"> Perinnän asiakaspoolit </span><span class="sxs-lookup"><span data-stu-id="32b19-127">Collections customer pools</span></span>

<span data-ttu-id="32b19-128">Asiakaspoolit ovat kyselyjä, jotka määrittävät asiakastietueryhmän.</span><span class="sxs-lookup"><span data-stu-id="32b19-128">Customer pools are queries that define a group of customer records.</span></span> <span data-ttu-id="32b19-129">Näiden ryhmitettyjen tietueiden avulla voi tarkastella sisältyvien asiakastilien tietoja sekä hallita niiden perintä- tai erääntymisprosesseja.</span><span class="sxs-lookup"><span data-stu-id="32b19-129">You can use these grouped records to view information for the customer accounts that are included, and to manage collections or aging processes for them.</span></span> <span data-ttu-id="32b19-130">Voit suodattaa perinnän luettelosivujen tietoja asiakaspoolien avulla.</span><span class="sxs-lookup"><span data-stu-id="32b19-130">You can use customer pools to filter information on the collections list pages.</span></span> <span data-ttu-id="32b19-131">Voit käyttää niitä suodattamaan myös erääntymistilannevedoksen luontiin sisältyneitä asiakastilejä.</span><span class="sxs-lookup"><span data-stu-id="32b19-131">You also can use them to filter the customer accounts that are included when aging snapshots are created.</span></span>

## <a name="collections-agents"></a><span data-ttu-id="32b19-132">Perimisasiamiehet</span><span class="sxs-lookup"><span data-stu-id="32b19-132">Collections agents</span></span>

<span data-ttu-id="32b19-133">Käyttäjät voivat tarkastella oletusarvoisesti kaikkia asiakastietoja perinnän luettelosivuilla.</span><span class="sxs-lookup"><span data-stu-id="32b19-133">By default, users can view all customer information on the collections list pages.</span></span> <span data-ttu-id="32b19-134">Perimisasiamiestietueiden avulla voidaan määrittää asiakaspoolit, joiden avulla voi suodattaa tietoja perinnän luettelosivuilla ja **Perintä**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="32b19-134">Collections agent records let you determine the customer pools that can be used to filter information on the collections list pages and the **Collections** page.</span></span>

<span data-ttu-id="32b19-135">Perimisasiamies työskentelee asiakkaiden kanssa varmistaakseen, että maksut peritään ajoissa.</span><span class="sxs-lookup"><span data-stu-id="32b19-135">Collections agents work with customers to make sure that payments are collected in a timely manner.</span></span> <span data-ttu-id="32b19-136">He ovat työtekijöitä, jotka on määritetty käyttäjille **Käyttäjän määritys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="32b19-136">They are workers who are assigned to users on the **User setup** page.</span></span>

## <a name="collections-list-pages"></a><span data-ttu-id="32b19-137"> Perinnän luettelosivut </span><span class="sxs-lookup"><span data-stu-id="32b19-137">Collections list pages</span></span>

<span data-ttu-id="32b19-138">Seuraavat luettelosivut ovat hyödyllisiä perintätietojen järjestämisessä:</span><span class="sxs-lookup"><span data-stu-id="32b19-138">The following list pages help you organize collections information:</span></span>

- <span data-ttu-id="32b19-139">**Erääntyneet saldot** – tämän luettelosivun sarakkeet näyttävät asiakkaan saldot ja erääntyneet summat erääntymiskauden mukaan.</span><span class="sxs-lookup"><span data-stu-id="32b19-139">**Aged balances** – The columns on this list page show customer balances and aged amounts by aging period.</span></span> <span data-ttu-id="32b19-140">Nämä tiedot on tallennettu erääntymistilannevedokseen.</span><span class="sxs-lookup"><span data-stu-id="32b19-140">This information is stored in an aging snapshot.</span></span> <span data-ttu-id="32b19-141">Erääntymiskaudet on määritelty käytetyn erääntymiskauden määritelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="32b19-141">The aging periods are determined by the aging period definition that is used.</span></span> <span data-ttu-id="32b19-142">Erääntymiskauden määritelmä on otettu asiakaspoolista, jos poolikyselyyn on määritetty asiakaspooli.</span><span class="sxs-lookup"><span data-stu-id="32b19-142">The aging period definition is taken from the customer pool, if a customer pool was specified for the pool query.</span></span> <span data-ttu-id="32b19-143">Jos asiakaspoolilla ei ole erääntymiskausimääritelmää, käytetään **Myyntireskontran parametrit** -sivulla määritettyä oletuserääntymiskauden määritelmää.</span><span class="sxs-lookup"><span data-stu-id="32b19-143">If the pool doesn't have an aging period definition, the default aging period definition that is specified on the **Accounts receivable parameters** page is used.</span></span> <span data-ttu-id="32b19-144">Jos oletuserääntymiskauden määritystä ei ole määritetty, käytetään **Erääntymiskausien määritykset** -sivun ensimmäistä erääntymiskausimääritystä.</span><span class="sxs-lookup"><span data-stu-id="32b19-144">If no default aging period definition is specified, the first aging period definition on the **Aging period definitions** page is used.</span></span>
- <span data-ttu-id="32b19-145">**Perintätehtävät** – Tämä luettelosivun sarakkeissa näytetään tehtävät, jotka on tunnistettu perintätehtäviksi.</span><span class="sxs-lookup"><span data-stu-id="32b19-145">**Collections activities** – The columns on this list page show activities that are identified as collections activities.</span></span> <span data-ttu-id="32b19-146">Nämä tehtävät luodaan **Perintä**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="32b19-146">These activities are created on the **Collections** page.</span></span> <span data-ttu-id="32b19-147">Aktiviteettien avulla seurataan perintään liittyvää työtä.</span><span class="sxs-lookup"><span data-stu-id="32b19-147">You use activities to track the collections-related work that you do.</span></span>
- <span data-ttu-id="32b19-148">**Perintätapaukset** – tämän luettelosivun sarakkeissa näytetään tietoja tapauksista, jotka kuuluvat **Perintä**-tapaustyypin sisältävään tapausluokkaan.</span><span class="sxs-lookup"><span data-stu-id="32b19-148">**Collections cases** – The columns on this list page show information for cases that belong to a case category that has a case type of **Collections**.</span></span>

### <a name="aging-snapshots"></a><span data-ttu-id="32b19-149">Erääntymistilannevedokset</span><span class="sxs-lookup"><span data-stu-id="32b19-149">Aging snapshots</span></span>

<span data-ttu-id="32b19-150">Erääntymistilannevedos on luotava ennen kuin voit tarkastella perinnän luettelosivujen tietoja.</span><span class="sxs-lookup"><span data-stu-id="32b19-150">An aging snapshot must be created before you can view information on the collections list pages.</span></span> <span data-ttu-id="32b19-151">Näkyvissä ovat vain niiden asiakkaiden tiedot, joille on luotu erääntymistilannevedos.</span><span class="sxs-lookup"><span data-stu-id="32b19-151">Information is shown only for customers that an aging snapshot has been created for.</span></span> <span data-ttu-id="32b19-152">Luettelosivulla näkyviä tietueita voi lisäksi suodattaa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="32b19-152">The records that are shown on the list page can be filtered further, as described here:</span></span>

- <span data-ttu-id="32b19-153">Oletusarvoisesti käyttäjällä on käyttöoikeus kaikkiin asiakkaisiin, joilla on erääntymistilannevedos.</span><span class="sxs-lookup"><span data-stu-id="32b19-153">By default, users have access to all customers who have an aging snapshot.</span></span>
- <span data-ttu-id="32b19-154">Jos järjestelmässä on asiakaspooleja, käyttäjä on määritettävä perimisasiamieheksi voidakseen käyttää pooleja perinnän luettelosivun tietojen suodattamiseen.</span><span class="sxs-lookup"><span data-stu-id="32b19-154">If customer pools exist, a user must be set up as a collections agent to use the pools to filter information on the collections list pages.</span></span> <span data-ttu-id="32b19-155">Tiedot rajoitetaan asiakkaisiin, jotka kuuluvat valittuun asiakaspooliin.</span><span class="sxs-lookup"><span data-stu-id="32b19-155">Information is limited to the customers who are included in the selected customer pool.</span></span>
- <span data-ttu-id="32b19-156">Jos käyttäjä on määritetty perimisasiamieheksi, ainoastaan kyseiselle perimisasiamiehelle valitut poolit ovat saatavilla perinnän luettelosivuilla.</span><span class="sxs-lookup"><span data-stu-id="32b19-156">If a user is set up as a collections agent, only the pools that are selected for that collections agent are available on the collections list pages.</span></span> <span data-ttu-id="32b19-157">Jos **Anna edustajan tarkastella kaikkia asiakaspooleja** -asetus on valittuna perimisasiamiehen **Perimisasiamies**-sivulla, kyseinen edustaja voi käyttää kaikkia pooleja.</span><span class="sxs-lookup"><span data-stu-id="32b19-157">If the **Allow agent to view all customer pools** option is selected on the **Collections agent** page for the collections agent, all pools are available for that agent.</span></span>

## <a name="collections-page"></a><span data-ttu-id="32b19-158"> Perintä-sivu</span><span class="sxs-lookup"><span data-stu-id="32b19-158">Collections page</span></span>

<span data-ttu-id="32b19-159">**Perintä**-sivulla voit tarkastella ja hallita asiakkaan perintätietoja, tehtäviä ja tapauksia sekä suorittaa niille toimenpiteitä.</span><span class="sxs-lookup"><span data-stu-id="32b19-159">You can use the **Collections** page to view, manage, and take action on collections information, activities, and cases for a customer.</span></span>

<span data-ttu-id="32b19-160">Sivun yläosassa on valitun asiakkaan tapaukset, keskiosassa asiakkaan tapahtumat ja alaosassa asiakkaan tehtävät.</span><span class="sxs-lookup"><span data-stu-id="32b19-160">The upper section of the page shows cases for the selected customer, the middle section shows transactions for the customer, and the lower section shows activities for the customer.</span></span> <span data-ttu-id="32b19-161">Voit luoda perintätapauksia seurataksesi yhden tai useamman tapahtuman ja tehtävän perintätietoja.</span><span class="sxs-lookup"><span data-stu-id="32b19-161">You can create collections cases to track collections information for one or more transactions and activities.</span></span> <span data-ttu-id="32b19-162">Ylä- ja alaosien tietoja voidaan suodattaa tapauskohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="32b19-162">The information in the upper and lower sections can be filtered by case.</span></span>

<span data-ttu-id="32b19-163">Valitun asiakkaan erääntyneet saldot ja luottorajatiedot näkyvät tietoruuduissa.</span><span class="sxs-lookup"><span data-stu-id="32b19-163">FactBoxes show aged balances and credit limit information for the selected customer.</span></span> <span data-ttu-id="32b19-164">Nämä tiedot on tallennettu erääntymistilannevedokseen.</span><span class="sxs-lookup"><span data-stu-id="32b19-164">This information is stored in the aging snapshot.</span></span> <span data-ttu-id="32b19-165">Voit päivittää erääntymistilannevedoksen tiedot nykyisillä tiedoilla tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="32b19-165">As you require, you can update the aging snapshot with current information.</span></span>

<span data-ttu-id="32b19-166">Toimintoruutu sisältää painikkeita, joilla voit tarkastella valittuun asiakkaaseen, tapaukseen, tapahtumaan tai tehtävään liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="32b19-166">The Action Pane contains buttons that let you view related information for the selected customer, case, transaction, or activity.</span></span> <span data-ttu-id="32b19-167">Voit myös suorittaa yleisiä toimintoja, kuten tapahtuman perintätilan muuttaminen, sähköpostiviestien lähettäminen integroidun sähköpostipalvelun välityksellä, asiakkaiden hyvittäminen, NSF-maksujen käsittely ja perintäkelvottomien saldojen poiskirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="32b19-167">You can also perform common actions, such as changing the collections status of a transaction, sending email through the integration with your email provider, reimbursing customers, processing NSF payments, and writing off uncollectible balances.</span></span>

## <a name="waiving-reinstating-or-reversing-interest-and-fees"></a><span data-ttu-id="32b19-168">Korkojen ja kulujen peruuttaminen, palauttaminen tai kääntäminen</span><span class="sxs-lookup"><span data-stu-id="32b19-168">Waiving, reinstating, or reversing interest and fees</span></span>

<span data-ttu-id="32b19-169">Voit peruuttaa, palauttaa tai kääntää kokonaisia korkolaskuja tai niiden osana olevia kuluja ja tapahtumakorkoja.</span><span class="sxs-lookup"><span data-stu-id="32b19-169">You can waive, reinstate, or reverse whole interest notes, or the fees and transaction interest that are part of interest notes.</span></span> <span data-ttu-id="32b19-170">Valitse **Kaikki asiakkaat** -luettelosivun toimintoruudun **Perintä**-välilehdessä **Korkolasku**, **Tapahtumakorko** tai **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="32b19-170">On the **Collect** tab on the Action Pane of the **All customers** list page, select **Interest note**, **Transaction interest**, or **Fee**.</span></span>

<span data-ttu-id="32b19-171">Nämä muutokset vaikuttavat vain korkolaskuihin sekä niihin sisältyviin korkoihin ja kuluihin.</span><span class="sxs-lookup"><span data-stu-id="32b19-171">These adjustments affect only interest notes, and the interest and fees that they include.</span></span> <span data-ttu-id="32b19-172">Lisätietoja asiakkaan velkana olevien kulujen poiskirjaamisesta on tämän ohjeaiheen kohdassa [Poistotapahtumien luominen](#creating-write-off-transactions).</span><span class="sxs-lookup"><span data-stu-id="32b19-172">For information about how to write off all the charges that a customer owes, see the [Creating write-off transactions](#creating-write-off-transactions) section of this topic.</span></span>

<span data-ttu-id="32b19-173">Lisätietoja on ohjeaiheissa Korkoryhmäalueen luominen ja Koron käsittely.</span><span class="sxs-lookup"><span data-stu-id="32b19-173">For more information see, Create an interest code with a range and Process interest.</span></span>

## <a name="creating-write-off-transactions"></a><span data-ttu-id="32b19-174">Poistotapahtumien luominen</span><span class="sxs-lookup"><span data-stu-id="32b19-174">Creating write-off transactions</span></span>

<span data-ttu-id="32b19-175">Voit kirjata luottotappiot pois valitsemalla **Poisto** **Perinnät**-sivulla ja perinnän luettelosivuilla.</span><span class="sxs-lookup"><span data-stu-id="32b19-175">You can write off bad debts by selecting **Write off** on the **Collections** page and the collections list pages.</span></span>

<span data-ttu-id="32b19-176">Kun kirjaat pois asiakkaan tapahtumia, kaikki asiakkaan tapahtumat merkitään automaattisesti selvitettäväksi.</span><span class="sxs-lookup"><span data-stu-id="32b19-176">When you write off transactions for a customer, all transactions for that customer are automatically marked for settlement.</span></span> <span data-ttu-id="32b19-177">Poiskirjattava summa riippuu merkittyjen tapahtumien nettosummasta.</span><span class="sxs-lookup"><span data-stu-id="32b19-177">The amount that is written off depends on the net amount of the marked transactions.</span></span> <span data-ttu-id="32b19-178">Poiskirjaustapahtuma luodaan yleisessä kirjauskansiossa ja se voi sisältää enintään kolmen tyyppisiä kirjauskansion rivejä:</span><span class="sxs-lookup"><span data-stu-id="32b19-178">The write-off transaction is created in a general journal and can contain up to three types of journal lines:</span></span>

- <span data-ttu-id="32b19-179">Ensimmäinen kirjauskansiorivi sisältää asiakastapahtuman poiskirjauksen.</span><span class="sxs-lookup"><span data-stu-id="32b19-179">The first type of journal line contains the customer write-off entry.</span></span> <span data-ttu-id="32b19-180">Jos merkityt tapahtumat sisältävät useita valuuttakoodien, dimensioiden ja kirjausprofiilien yhdistelmiä, kullekin yhdistelmälle luodaan erillinen kirjauskansion rivi.</span><span class="sxs-lookup"><span data-stu-id="32b19-180">If the marked transactions contain multiple combinations of currency codes, dimensions, and posting profiles, a separate journal line is created for each combination.</span></span>
- <span data-ttu-id="32b19-181">Toinen kirjauskansiorivi sisältää kirjanpidon poiskirjauksen.</span><span class="sxs-lookup"><span data-stu-id="32b19-181">The second type of journal line contains the general ledger write-off entry.</span></span> <span data-ttu-id="32b19-182">Jos merkityt tapahtumat sisältävät useita valuuttakoodien, dimensioiden ja kirjausprofiilien yhdistelmiä, kullekin yhdistelmälle luodaan erillinen kirjauskansion rivi.</span><span class="sxs-lookup"><span data-stu-id="32b19-182">If the marked transactions contain multiple combinations of currency codes, dimensions, and posting profiles, a separate journal line is created for each combination.</span></span>
- <span data-ttu-id="32b19-183">Kirjauskansiorivin kolmas tyyppi on kirjanpidon poiskirjaustieto arvonlisäveroille.</span><span class="sxs-lookup"><span data-stu-id="32b19-183">The third type of journal line contains the general ledger write-off information for sales taxes.</span></span> <span data-ttu-id="32b19-184">Kirjauskansiorivi luodaan vain, jos **Erillinen arvonlisävero** -asetus on valittuna **Myyntireskontran parametri** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="32b19-184">This journal line is created only if the **Separate sales tax** option is selected on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="32b19-185">Jos merkityt tapahtumat sisältävät useita arvonlisäveron kulutilien, dimensioiden ja arvonlisäverokoodien yhdistelmiä, kullekin yhdistelmälle luodaan erillinen kirjauskansion rivi.</span><span class="sxs-lookup"><span data-stu-id="32b19-185">If the marked transactions contain multiple combinations of sales tax payable accounts, dimensions, and sales tax codes, a separate journal line is created for each combination.</span></span> <span data-ttu-id="32b19-186">Poiskirjaustapahtuma luodaan tapahtuman valuutalla.</span><span class="sxs-lookup"><span data-stu-id="32b19-186">The write-off transaction is created in the transaction currency.</span></span> <span data-ttu-id="32b19-187">Lisätietoja on ohjeaiheessa Poiskirjauksen kirjauskansion luominen asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="32b19-187">For more information see, Create a write-off journal for a customer.</span></span>

## <a name="process-nsf-payments"></a><span data-ttu-id="32b19-188">NSF-maksujen käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="32b19-188">Process NSF payments</span></span>

<span data-ttu-id="32b19-189">Voit käsitellä NSF-maksuja valitsemalla **Perintä**-sivulla **NSF-maksu**.</span><span class="sxs-lookup"><span data-stu-id="32b19-189">You can process NSF payments by selecting **NSF payment** on the **Collections** page.</span></span> <span data-ttu-id="32b19-190">Maksu peruutetaan, kun valitset tämän painikkeen.</span><span class="sxs-lookup"><span data-stu-id="32b19-190">When you select this button, the payment is canceled.</span></span> <span data-ttu-id="32b19-191">Jos NSF-maksu koskee asiakkaan kuluja, veloitustapahtuma luodaan maksujen kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="32b19-191">If an NSF fee applies for the customer, a charge transaction is created in a payment journal.</span></span> <span data-ttu-id="32b19-192">Maksun summa perustuu automaattisten veloitusten asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="32b19-192">The amount of the fee is based on the settings for the automatic charges.</span></span> <span data-ttu-id="32b19-193">NSF-maksuihin sovellettavat automaattiset veloitukset määritetään kuluryhmässä, joka on valittu **Pankkitilit**-sivulla pankkitilille, jota asia koskee.</span><span class="sxs-lookup"><span data-stu-id="32b19-193">The automatic charges that apply to NSF payments are specified by the charges group that is selected on the **Bank accounts** page for the affected bank account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32b19-194">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="32b19-194">Additional resources</span></span>

[<span data-ttu-id="32b19-195">Asiakkaan luotonhallinnan parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="32b19-195">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="32b19-196">Asiakkaan luotonhallinnan määritystiedot</span><span class="sxs-lookup"><span data-stu-id="32b19-196">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="32b19-197">Asiakkaan luotonhallintatietojen lisääminen</span><span class="sxs-lookup"><span data-stu-id="32b19-197">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="32b19-198">Asiakasluottoryhmät</span><span class="sxs-lookup"><span data-stu-id="32b19-198">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="32b19-199">Asiakkaan luottorajan oikaisut</span><span class="sxs-lookup"><span data-stu-id="32b19-199">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="32b19-200">Myyntitilausten luottorajapidot</span><span class="sxs-lookup"><span data-stu-id="32b19-200">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="32b19-201">Asiakkaan luotonhallinnan kausittaiset tehtävät</span><span class="sxs-lookup"><span data-stu-id="32b19-201">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)