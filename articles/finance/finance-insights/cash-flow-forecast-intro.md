---
title: Kassavirtaennuste (esiversio)
description: Tässä ohjeaiheessa kuvataan kassavirtaennusteominaisuutta.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 0df58d3571b124acbd1edbc6d6acdd49479c309e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990586"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="236d5-103">Kassavirtaennuste (esiversio)</span><span class="sxs-lookup"><span data-stu-id="236d5-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="236d5-104">Kassavirta on kriittinen toiminto kaikille yrityksille.</span><span class="sxs-lookup"><span data-stu-id="236d5-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="236d5-105">Jopa kannattavia yrityksiä voi kohdata maksukyvyttömyys, jos ne eivät ylläpidä kassavirtaa vastaamaan välittömiin tarpeisiin.</span><span class="sxs-lookup"><span data-stu-id="236d5-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="236d5-106">Finance Insightsin kassavirran ennustusominaisuuden avulla yritykset voivat tarkkailla ja hallinnoida kassan saldoja tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="236d5-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="236d5-107">Tämä toiminto auttaa yrityksiä ennustamaan kassavirtoja aiempaa paremmin koneoppimisen avulla.</span><span class="sxs-lookup"><span data-stu-id="236d5-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="236d5-108">Se voi myös auttaa esimiehiä tekemään päätöksiä, jotka optimoivat mahdollisuudet nykyisen kassatilanteen mukaan.</span><span class="sxs-lookup"><span data-stu-id="236d5-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="236d5-109">Useimmissa yrityksissä kassavirran hallinta ja kassavirtaennusteiden suorittaminen on työläs, toistuva ja manuaalinen prosessi.</span><span class="sxs-lookup"><span data-stu-id="236d5-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="236d5-110">Useimmat yritykset luottavat Microsoft Excel -ratkaisuihin, jotka saattavat olla monimutkaisia.</span><span class="sxs-lookup"><span data-stu-id="236d5-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="236d5-111">Kassavirran tarkan ennustamisen haasteet ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="236d5-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="236d5-112">Päätöksentekijät eivät aina voi käyttää tietoja, koska ne ovat hajallaan useissa paikoissa, kuten:</span><span class="sxs-lookup"><span data-stu-id="236d5-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="236d5-113">Kirjanpito-tai yritysresurssien suunnittelujärjestelmä</span><span class="sxs-lookup"><span data-stu-id="236d5-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="236d5-114">Taloushallinnon suunnitteluohjelmisto</span><span class="sxs-lookup"><span data-stu-id="236d5-114">Financial planning software</span></span>
  - <span data-ttu-id="236d5-115">Excel</span><span class="sxs-lookup"><span data-stu-id="236d5-115">Excel</span></span>
  - <span data-ttu-id="236d5-116">Muut ohjelmistosovellukset</span><span class="sxs-lookup"><span data-stu-id="236d5-116">Additional software applications</span></span> 
- <span data-ttu-id="236d5-117">Ennustaminen perustuu sisäiseen tietoon, joka sijaitsee kunkin domainin tai osaston siilossa.</span><span class="sxs-lookup"><span data-stu-id="236d5-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="236d5-118">Kassavirtaennusteiden tarkkuuden mittaaminen sen jälkeen, kun myyntitiedot on saatu, on epävarmaa ja vaikeaa.</span><span class="sxs-lookup"><span data-stu-id="236d5-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="236d5-119">Kassavirtaennusteominaisuuden tiedot</span><span class="sxs-lookup"><span data-stu-id="236d5-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="236d5-120">Kassavirtaennusteominaisuus sisältää seuraavat toiminnot.</span><span class="sxs-lookup"><span data-stu-id="236d5-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="236d5-121">Kassavirtatietojen helppo integroiminen ulkoisista järjestelmistä Dynamics 365 Financeen.</span><span class="sxs-lookup"><span data-stu-id="236d5-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="236d5-122">Kassavirtaennusteissa voi käyttää myös tietojen tuonti- ja vientikehystä.</span><span class="sxs-lookup"><span data-stu-id="236d5-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="236d5-123">Tämän kehyksen avulla on helppo integroida tiedot Excel ODatan kanssa.</span><span class="sxs-lookup"><span data-stu-id="236d5-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="236d5-124">Voit yhdistää tietoja useista lähteistä ja luoda kattavan kassavirtaratkaisun.</span><span class="sxs-lookup"><span data-stu-id="236d5-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="236d5-125">Esittelee älykkään kassatilanteen.</span><span class="sxs-lookup"><span data-stu-id="236d5-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="236d5-126">Kassatilanne luodaan asiakkaan maksutoiminnan perusteella. Sen avulla ennustetaan, milloin yritys voi odottaa rahojen tulevan tilille.</span><span class="sxs-lookup"><span data-stu-id="236d5-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="236d5-127">Se myös analysoi maksavien toimittajien aiempia malleja ja ennustaa, milloin tulevat laskut ja tilaukset todennäköisesti maksetaan.</span><span class="sxs-lookup"><span data-stu-id="236d5-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="236d5-128">Esittelee älykkäitä kassavirtaennusteita pitkän aikavälin ennustamista varten käyttämällä aikasarjojen ennustamista automaattisen integroinnin ja AI Builderin kautta.</span><span class="sxs-lookup"><span data-stu-id="236d5-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="236d5-129">Mahdollisuus tallentaa tietty kassavirran tilanne tai ennusteet, muokata niitä ja tämän jälkeen vertailla helposti ja mitata ennusteen suorituskyky todellisten taloustietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="236d5-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="236d5-130">Ottaa käyttöön mitä jos -analyysin tilannevedoksen vertailun avulla.</span><span class="sxs-lookup"><span data-stu-id="236d5-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="236d5-131">Voit esimerkiksi luoda useita tilannevedoksia, jotka edustavat optimistisia, pessimistisiä ja realistisia kassavirtanäkymiä. Tämän jälkeen voit verrata eroja ja tarkastella niitä.</span><span class="sxs-lookup"><span data-stu-id="236d5-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="236d5-132">Mahdollisuus tarkastella kassavirtaennustetta useissa valuutoissa ja eri yrityksissä sekä suodattaa ja tarkastella pankkitiliin liittyvää kassavirtaa.</span><span class="sxs-lookup"><span data-stu-id="236d5-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="236d5-133">Voit suodattaa ja tarkastella taloushallinnon dimensioihin liittyviä pankkitilejä.</span><span class="sxs-lookup"><span data-stu-id="236d5-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="236d5-134">Dynamics 365 Financen kassavirtaennustetoiminnon avulla organisaatio voi muuntaa työlään, monimutkaisen ja silti toistuvan kassavirtaennusteen yksinkertaiseksi, automatisoiduksi prosessiksi.</span><span class="sxs-lookup"><span data-stu-id="236d5-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="236d5-135">Kassavirtaennusteen työläimpien kohtien automatisointi mahdollistaa kriittiseen päätöksentekoon keskittymisen ja haluttujen tulosten saamisen.</span><span class="sxs-lookup"><span data-stu-id="236d5-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="236d5-136">Kassavirran ennustamisen dimensioiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="236d5-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="236d5-137">**Kassavirran ennustamisen määritykset** -sivun uuden välilehden avulla voit määrittää, mitkä taloushallinnon dimensiot otetaan käyttöön suodatettaessa **Kassavirran ennustaminen** -työtilaa.</span><span class="sxs-lookup"><span data-stu-id="236d5-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="236d5-138">Tämä välilehti näkyy vain, kun Kassavirtaennusteet-toiminto on käytössä.</span><span class="sxs-lookup"><span data-stu-id="236d5-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="236d5-139">Valitse **Dimensiot**-välilehdessä suodatuksessa käytettävät dimensiot luettelosta ja siirrä ne oikeanpuoleiseen sarakkeeseen nuolinäppäinten avulla.</span><span class="sxs-lookup"><span data-stu-id="236d5-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="236d5-140">Kassavirtaennustetietojen suodattamiseen voidaan valita vain kaksi dimensiota.</span><span class="sxs-lookup"><span data-stu-id="236d5-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

#### <a name="privacy-notice"></a><span data-ttu-id="236d5-141">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="236d5-141">Privacy notice</span></span>
<span data-ttu-id="236d5-142">Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.</span><span class="sxs-lookup"><span data-stu-id="236d5-142">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
