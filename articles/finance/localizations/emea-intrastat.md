---
title: Intrastat – yleiskatsaus
description: Tämä aihe sisältää tietoja Intrastat-raportoinnista, jota käytetään Euroopan unionin (EU) jäsenvaltioiden ja alueiden välillä käytävän tavaroiden (ja joissakin tapauksessa myös palveluiden) kaupan raportoinnissa. Artikkeli sisältää raportointiprosessin yleiskatsauksen ja kertoo pakolliset asetukset ja edellytykset.
author: EvgenyPopovMBS
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bafbb908531e003d2184409bf5d09ed5848fc474
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216785"
---
# <a name="intrastat-overview"></a><span data-ttu-id="8f566-104">Intrastat – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8f566-104">Intrastat overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f566-105">Tämä aihe sisältää tietoja Intrastat-raportoinnista, jota käytetään Euroopan unionin (EU) jäsenvaltioiden ja alueiden välillä käytävän tavaroiden (ja joissakin tapauksessa myös palveluiden) kaupan raportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="8f566-105">This topic provides information about Intrastat reporting for the trade of goods and, in some cases, services among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="8f566-106">Artikkeli sisältää raportointiprosessin yleiskatsauksen ja kertoo pakolliset asetukset ja edellytykset.</span><span class="sxs-lookup"><span data-stu-id="8f566-106">It provides an overview of the reporting process, and describes the required settings and prerequisites.</span></span>

<span data-ttu-id="8f566-107">Intrastat on järjestelmä, jolla kerätään tietoja ja muodostetaan tilastoja Euroopan unionin (EU) jäsenvaltioiden ja alueiden välisestä kaupasta.</span><span class="sxs-lookup"><span data-stu-id="8f566-107">Intrastat is the system for collecting information and generating statistics about the trade of goods among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="8f566-108">Intrastat-raportointi on pakollista aina, kun tuote ylittää EU-maan tai -alueen rajan.</span><span class="sxs-lookup"><span data-stu-id="8f566-108">Intrastat reporting is required whenever a product crosses the border of another EU country/region.</span></span> <span data-ttu-id="8f566-109">Monissa maissa ja monilla alueilla Intrastat-raportointi koskee myös palveluja.</span><span class="sxs-lookup"><span data-stu-id="8f566-109">In several countries/regions, Intrastat reporting also applies to services.</span></span> <span data-ttu-id="8f566-110">Intrastat-raporteissa voidaan kerätä pakollisia ja valinnaisia elementtejä.</span><span class="sxs-lookup"><span data-stu-id="8f566-110">Mandatory and optional elements can be collected in Intrastat reporting.</span></span> <span data-ttu-id="8f566-111">Seuraavat elementit ovat pakollisia: tietojen ilmoittamisesta vastuussa olevan osapuolen arvonlisäveronumero (ALV-numero), viitekausi, suunta (saapuva vai lähtevä), 8-numeroinen tavarankoodi, kumppanin jäsenvaltio (lähettäjäjäsenvaltio saapuvissa ja määräjäsenvaltio lähetyksissä), tavaroiden arvo, tavaroiden määrä (nettopaino ja lisäyksikkö) ja tapahtuman luonne.</span><span class="sxs-lookup"><span data-stu-id="8f566-111">The following elements are mandatory: the value-added tax (VAT) number of the party that is responsible for providing information, the reference period, the flow (arrival or dispatch), the eight-digit commodity code, the partner member state (member state of consignment on arrivals and member state of destination on dispatches), the value of the goods, the quantity of the goods (net mass and supplementary unit), and the nature of the transaction.</span></span> <span data-ttu-id="8f566-112">Maat ja alueet voivat myös kerätä erilaisten ehtojen mukaisesti valinnaisia elementtejä.</span><span class="sxs-lookup"><span data-stu-id="8f566-112">Countries/regions can also collect optional elements under various conditions.</span></span> <span data-ttu-id="8f566-113">Valinnaisia elementtejä ovat esimerkiksi alkuperämaa tai -alue, toimitusehdot, kuljetustapa, yksityiskohtaisempi tavaran koodi kuin CN8, alkuperäalue lähetyksissä ja määräalue saapuvissa, tilastomenettely, tilastoarvo, tavaroiden kuvaus sekä kuormauksen tai kuorman purkamisen satama tai lentoasema.</span><span class="sxs-lookup"><span data-stu-id="8f566-113">Some optional elements are the country/region of origin, the delivery terms, the mode of transport, a more detailed commodity code than CN8, the region of origin on dispatches and the region of destination on arrivals, the statistical procedure, the statistical value, a description of the goods, and the port/airport of loading/unloading.</span></span>

## <a name="overview-of-the-intrastat-reporting-process"></a><span data-ttu-id="8f566-114">Intrastat-raportointiprosessin yhteenveto</span><span class="sxs-lookup"><span data-stu-id="8f566-114">Overview of the Intrastat reporting process</span></span>
<span data-ttu-id="8f566-115">Seuraavissa osissa kuvataan Intrastat-raportoinnissa käytettävää yleistä tiedonkulkua.</span><span class="sxs-lookup"><span data-stu-id="8f566-115">The following sections describe the overall flow of information that is used for Intrastat reporting.</span></span>

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a><span data-ttu-id="8f566-116">1. Anna toisen EU-maan tai -alueen rajan ylittävä tapahtuma</span><span class="sxs-lookup"><span data-stu-id="8f566-116">1. Enter a transaction that crosses the border of another EU country/region</span></span>

<span data-ttu-id="8f566-117">Myyntilasku, vapaatekstilasku, ostolasku, projektilaskun, asiakkaan pakkausluettelo, toimittajan tuotteen vastaanotto tai siirtotilaus siirretään Intrastat-kirjauskansioon vain, jos määrämaan tai -alueen tyyppi (lähtevissä) tai lähettäjätyyppi (saapuvissa) on **EU**.</span><span class="sxs-lookup"><span data-stu-id="8f566-117">A customer invoice, free text invoice, purchase invoice, project invoice, customer packing slip, vendor product receipt, or transfer order is transferred to the Intrastat journal only if the country/region type of the destination (on dispatches) or consignment (on arrivals) is **EU**.</span></span> <span data-ttu-id="8f566-118">Tämän toiminto laajennettiin Microsoft Dynamics 365 for Operationsiin (1611), ja sen avulla voit määrittää rahtiosoitteita EU:n sisäisille tapahtumille.</span><span class="sxs-lookup"><span data-stu-id="8f566-118">This feature was extended for Microsoft Dynamics 365 for Operations (1611) and allows you to specify lading addresses for an intra-community transaction.</span></span> <span data-ttu-id="8f566-119">Jos rahtiosoite on eri kuin toimittajan osoite (tai asiakkaan osoite palautustilauksen osalta), Intrastat-raportointi toimii näillä tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="8f566-119">If a lading address differs with a vendor business address (or customer business address for return order) the Intrastat reporting will operate with this information.</span></span> <span data-ttu-id="8f566-120">Kun luot myyntitilauksen, vapaatekstilaskun, ostotilauksen, toimittajan laskun, projektilaskun tai siirtotilauksen, joissakin ulkomaankauppaan liittyvissä kentissä on oletusarvot asiakirjan otsikossa tai rivillä.</span><span class="sxs-lookup"><span data-stu-id="8f566-120">When you create a sales order, free text invoice, purchase order, vendor invoice, project invoice, or transfer order, some fields that are related to foreign trade have default values in the document header or on the line.</span></span> <span data-ttu-id="8f566-121">Tapahtuman oletuskoodi otetaan vastaavasta kentästä **Ulkomaankaupan parametrit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="8f566-121">The default transaction code is taken from the corresponding field on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="8f566-122">Tavaran oletuskoodi, alkuperämaa tai -alue sekä alkuperäosavaltio tai -provinssi otetaan nimikkeestä.</span><span class="sxs-lookup"><span data-stu-id="8f566-122">The default commodity code, country/region of origin, and state/province of origin are taken from the item.</span></span> <span data-ttu-id="8f566-123">Voit muuttaa oletusarvoja ja lisätä muut ulkomaankauppaan liittyvät tiedot: tilastomenettelyn, kuljetustavan ja sataman.</span><span class="sxs-lookup"><span data-stu-id="8f566-123">You can change the default values and can also fill in other foreign trade–related information: the statistics procedure, transport method, and port.</span></span>

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="8f566-124">2. Voit luoda tietoja EU-maiden -ja alueiden välisestä kaupasta Intrastat-kirjauskansion avulla.</span><span class="sxs-lookup"><span data-stu-id="8f566-124">2. Use the Intrastat journal to generate information about trade among EU countries/regions</span></span>

<span data-ttu-id="8f566-125">Tilastoja varten tiedot EU-maiden ja -alueiden välisestä kaupasta luodaan kuukausittain.</span><span class="sxs-lookup"><span data-stu-id="8f566-125">For statistical purposes, you generate information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="8f566-126">Voit siirtää tapahtumat vapaatekstilaskusta, myyntilaskusta, asiakkaan pakkausluettelosta, toimittajan laskusta, toimittajan pakkausluettelosta, projektilaskusta tai siirtotilauksesta **Ulkomaankaupan parametrit** -sivulla määritettyjen ehtojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8f566-126">You can transfer transactions from a free text invoice, customer invoice, customer packing slip, vendor invoice, vendor packing slip, project invoice, or transfer order, according to the transfer criteria that are set up on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="8f566-127">Voit antaa tapahtumat myös manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="8f566-127">Alternatively, you can enter transactions manually.</span></span> <span data-ttu-id="8f566-128">Voit päivittää manuaalisesti siirretyt tapahtumat Intrastat-kirjauskansiossa, jos päivitys on tarpeellinen.</span><span class="sxs-lookup"><span data-stu-id="8f566-128">You can manually update transferred transactions in the Intrastat journal, if any updates are required.</span></span> <span data-ttu-id="8f566-129">Voit tiivistää Intrastat-kirjauskansion tapahtumat **Intrastatin tiivistys** -sivulla määritettyjen erityisehtojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8f566-129">Under specific conditions that are set up on the **Compression of Intrastat** page, you can compress the transactions in the Intrastat journal.</span></span> <span data-ttu-id="8f566-130">Joissakin maissa ja joillakin alueilla voi käyttää pienen tapahtuman rajaa.</span><span class="sxs-lookup"><span data-stu-id="8f566-130">Some countries/regions let you apply a small transaction threshold.</span></span> <span data-ttu-id="8f566-131">Voit sitten raportoida kyseisen rajan alle jäävät tapahtumat erityisellä tavaran koodilla.</span><span class="sxs-lookup"><span data-stu-id="8f566-131">You can then report transactions that are below that threshold under the specified commodity code.</span></span> <span data-ttu-id="8f566-132">Voit päivittää tavaran koodin vastaavilla Intrastat-kirjauskansion riveillä **Ulkomaankaupan parametrit** -sivun **Vähimmäisraja**-asetuksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8f566-132">You can update the commodity code on the corresponding Intrastat journal lines, based on the **Minimum limit** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="8f566-133">Voit myös tiivistää kyseiset tapahtumat **Intrastatin tiivistys** -asetuksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8f566-133">You can also compress those transactions, based on the **Compression of Intrastat** setting.</span></span> <span data-ttu-id="8f566-134">Voit tarkistaa Intrastat-kirjauskansion tapahtumien valmiusasteen **Ulkomaankaupan parametrit** -sivun **Tarkista asetukset** -asetuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="8f566-134">You can validate the completeness of the transactions in the Intrastat journal, based on the **Check setup** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="8f566-135">Vastaavien kenttien tietojen valmiusaste voidaan tarkistaa: maa tai alue, osavaltio tai provinssi, paino, tavaran koodi, tapahtumakoodi, lisäyksikkö, satama, alkuperä, toimitusehdot, kuljetustapa ja ALV-tunnus.</span><span class="sxs-lookup"><span data-stu-id="8f566-135">The data in corresponding fields might be validated for completeness: country/region, state or province, weight, commodity code, transaction code, additional unit, port, origin, terms of delivery, transport method, and tax exempt number.</span></span> <span data-ttu-id="8f566-136">Tapahtumat, jotka eivät ole valmiita, saavat merkinnän ei kelpaa.</span><span class="sxs-lookup"><span data-stu-id="8f566-136">Transactions that aren't completed will be marked as not valid.</span></span>

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="8f566-137">3. Voit raportoida tietoja EU-maiden -ja alueiden välisestä kaupasta Intrastat-kirjauskansion avulla.</span><span class="sxs-lookup"><span data-stu-id="8f566-137">3. Use the Intrastat journal to report information about trade among EU countries/regions</span></span>

<span data-ttu-id="8f566-138">Tilastoja varten tiedot EU-maiden ja -alueiden välisestä kaupasta raportoidaan kuukausittain.</span><span class="sxs-lookup"><span data-stu-id="8f566-138">For statistical purposes, you report information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="8f566-139">Voit tulostaa Intrastat-raportin **Ulkomaankaupan parametrit** -sivun **Raporttimuodon yhdistäminen** -asetusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8f566-139">You can print the Intrastat report, based on the **Report format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="8f566-140">Voit myös luoda sähköisen tiedoston **Ulkomaankaupan parametrit** -sivun **Tiedostomuodon yhdistäminen** -asetusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8f566-140">You can also generate an electronic file, based on the **File format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="8f566-141">Lisätietoja Intrastat-raportoinnista, kuten edellytyksistä, on Intrastat-raportoinnin tehtävätallenteissa:</span><span class="sxs-lookup"><span data-stu-id="8f566-141">For more information about Intrastat reporting, including required prerequisites, see the Intrastat reporting task recordings:</span></span>

-   <span data-ttu-id="8f566-142">EU Intrastat -ilmoituksen luominen</span><span class="sxs-lookup"><span data-stu-id="8f566-142">Generate an EU Intrastat declaration,</span></span>
-   <span data-ttu-id="8f566-143">Siirrä tapahtumat Intrastatiin</span><span class="sxs-lookup"><span data-stu-id="8f566-143">Transfer transactions to the Intrastat,</span></span>
-   <span data-ttu-id="8f566-144">Rahtiosoitteen määrittäminen yhteisönsisäiselle tapahtumalle.</span><span class="sxs-lookup"><span data-stu-id="8f566-144">Specifying lading address for an intra-community transaction.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8f566-145">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="8f566-145">Prerequisites</span></span>
<span data-ttu-id="8f566-146">Seuraavassa taulussa luetellaan Intrastat-raportoinnin edellytykset.</span><span class="sxs-lookup"><span data-stu-id="8f566-146">The following table lists the prerequisites for Intrastat reporting.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f566-147">Edellytys</span><span class="sxs-lookup"><span data-stu-id="8f566-147">Prerequisite</span></span></th>
<th><span data-ttu-id="8f566-148">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="8f566-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f566-149">Osoitemääritys</span><span class="sxs-lookup"><span data-stu-id="8f566-149">Address setup</span></span></td>
<td><span data-ttu-id="8f566-150">Määritä maiden ja alueiden ISO (International Organization for Standardization) -koodit.</span><span class="sxs-lookup"><span data-stu-id="8f566-150">Set up International Organization for Standardization (ISO) codes for countries/regions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f566-151">Oikeushenkilö</span><span class="sxs-lookup"><span data-stu-id="8f566-151">Legal entity</span></span></td>
<td><span data-ttu-id="8f566-152">Määritä tuonnin ja viennin ALV-tunnukset, sivuliikkeen alanumeron tuonti ja vienti sekä yritykselle määritetty Intrastat-koodi.</span><span class="sxs-lookup"><span data-stu-id="8f566-152">Set up tax exempt numbers for import/export, the branch number extension for import/export, and the Intrastat code that is assigned to the legal entity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f566-153">Tuoteluokkahierarkia (myyntihierarkia, hankintahierarkia)</span><span class="sxs-lookup"><span data-stu-id="8f566-153">Product category hierarchy (sales hierarchy, procurement hierarchy)</span></span></td>
<td><span data-ttu-id="8f566-154">Määritä luokkasolmujen Intrastat-kauppatavarakoodit <strong>Luokkahierarkia</strong>-sivun <strong>Kauppatavarakoodit</strong>-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="8f566-154">Assign the Intrastat commodity codes to the category nodes on the <strong>Commodity codes</strong> tab of the <strong>Category hierarchy</strong> page.</span></span> <span data-ttu-id="8f566-155">Kun määrität kauppatavarakoodin pääluokkasolmulle, koodia käytetään kaikissa aliluokkasolmuissa.</span><span class="sxs-lookup"><span data-stu-id="8f566-155">When you assign a commodity code to a parent category node, that code is applicable to all child category nodes.</span></span> <span data-ttu-id="8f566-156">Valittuja kauppatavarakoodeja voi käyttää <strong>Valittu</strong>-näkymässä, kun valitset kauppatavarakoodin tuotteen tiedoissa sekä myynti-, osto- ja siirtotilausriveillä.</span><span class="sxs-lookup"><span data-stu-id="8f566-156">The selected commodity codes will be available in the <strong>Selected</strong> view when you select a commodity code in the product details, and on sales order, purchase order, and transfer order lines.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f566-157">Vapautetun tuotteen tiedot</span><span class="sxs-lookup"><span data-stu-id="8f566-157">Released product details</span></span></td>
<td><span data-ttu-id="8f566-158">Määritä seuraavat vapautettujen tuotteiden ulkomaankaupan tiedot:</span><span class="sxs-lookup"><span data-stu-id="8f566-158">Set up the following foreign trade data for released products:</span></span>
<ul>
<li><span data-ttu-id="8f566-159"><strong>Kauppatavarakoodi</strong> – valitse joko määritetyistä tuoteluokista haettu valittujen kauppatavaroiden luettelo tai täydellinen Intrastat-kauppatavarakoodien luettelo.</span><span class="sxs-lookup"><span data-stu-id="8f566-159"><strong>Commodity code</strong> – Select from either the list of selected commodities that is retrieved from assigned product categories or the full list of Intrastat commodity codes.</span></span></li>
<li><span data-ttu-id="8f566-160"><strong>Tilastollinen maksuprosentti</strong></span><span class="sxs-lookup"><span data-stu-id="8f566-160"><strong>Statistical charges percentage</strong></span></span></li>
<li><span data-ttu-id="8f566-161"><strong>Alkuperämaa tai -alue</strong> – valitse oletusmaa tai -alue, josta tavarat kokonaisuudessaan hankittiin tai jossa ne valmistettiin.</span><span class="sxs-lookup"><span data-stu-id="8f566-161"><strong>Country/region of origin</strong> – Select the default country/region where the goods were completely obtained or produced.</span></span></li>
<li><span data-ttu-id="8f566-162"><strong>Alkuperäosavaltio tai -provinssi tai määräosavaltio tai -provinssi</strong> – saapuvien oletusarvoinen määräosavaltio tai -provinssi ja lähtevien alkuperäosavaltio tai -provinssi.</span><span class="sxs-lookup"><span data-stu-id="8f566-162"><strong>State/province of origin/destination</strong> – Select the default state/province of destination for arrivals and the state/province of origin for dispatches.</span></span></li>
<li><span data-ttu-id="8f566-163"><strong>Nettopaino kilogrammoina</strong></span><span class="sxs-lookup"><span data-stu-id="8f566-163"><strong>Net weight in kg</strong></span></span></li>
<li><span data-ttu-id="8f566-164"><strong>Sulje pois</strong> - Ota tämä parametri käyttöön, kun haluat, ettei tämän tuotteen tapahtumia siirretä Intrastatiin</span><span class="sxs-lookup"><span data-stu-id="8f566-164"><strong>Exclude</strong> - Enable this parameter to not transfer transactions with this product to Intrastat</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f566-165">Asiakkaat</span><span class="sxs-lookup"><span data-stu-id="8f566-165">Customers</span></span></td>
<td><span data-ttu-id="8f566-166">Määritä asiakkaan EU-maassa tai -alueella oleva toimitusosoite.</span><span class="sxs-lookup"><span data-stu-id="8f566-166">Set up the customer delivery address in the EU country/region.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f566-167">Toimittajat</span><span class="sxs-lookup"><span data-stu-id="8f566-167">Vendors</span></span></td>
<td><span data-ttu-id="8f566-168">Määritä toimittajan EU-maassa tai -alueella oleva toimitusosoite.</span><span class="sxs-lookup"><span data-stu-id="8f566-168">Set up the vendor address in the EU country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f566-169">Muut kulut</span><span class="sxs-lookup"><span data-stu-id="8f566-169">Miscellaneous charges</span></span></td>
<td><span data-ttu-id="8f566-170">Määritä laskusummaan, tilastosumman tai molempiin sisällytettävä muiden kulujen koodi.</span><span class="sxs-lookup"><span data-stu-id="8f566-170">Set up the miscellaneous charges code to include in the invoice amount, the statistical amount, or both.</span></span> <span data-ttu-id="8f566-171">Määritä <strong>Kulukoodit</strong>-sivun <strong>Ulkomaankauppa</strong>-välilehdessä <strong>Intrastat-laskun arvo</strong> sisällyttämään kulujen summa laskun arvoon. Määritä myös <strong>Tilastollinen Intrastat-arvo</strong> sisällyttämään kulujen summa tilastoarvoon.</span><span class="sxs-lookup"><span data-stu-id="8f566-171">On the <strong>Charges codes</strong> page, on the <strong>Foreign trade</strong> tab, enable <strong>Intrastat invoice value</strong> to include the charges amount in the invoice value, and enable <strong>Intrastat statistical value</strong> to include the charges amount in the statistical value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f566-172">Sähköinen raportointi</span><span class="sxs-lookup"><span data-stu-id="8f566-172">Electronic reporting</span></span></td>
<td><span data-ttu-id="8f566-173">Määritä sähköisen raportoinnin määritykset viemään Intrastat-tiedot sähköisenä tiedostona viranomaisten pyytämässä muodossa ja luomaan esikatselu käyttäjälle soveltuvassa luettavassa muodossa (kuten Microsoft Excelissä).</span><span class="sxs-lookup"><span data-stu-id="8f566-173">Set up electronic reporting configurations to export Intrastat data in an electronic file that has the format that is requested by the relevant authorities, and to preview Intrastat data in a user-friendly, readable format (for example, in Microsoft Excel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f566-174">Varastointi</span><span class="sxs-lookup"><span data-stu-id="8f566-174">Warehousing</span></span></td>
<td><span data-ttu-id="8f566-175">Liitä toimittajatilit varastokoodeihin verovapausnumeron täyttämiseksi siirtotilausta siirrettäessä.</span><span class="sxs-lookup"><span data-stu-id="8f566-175">Associate vendor accounts with warehouse codes for filling tax exempt number when transferring Transfer order.</span></span></td>
</tr>
</tbody>
</table>

## <a name="setup"></a><span data-ttu-id="8f566-176">Määritys</span><span class="sxs-lookup"><span data-stu-id="8f566-176">Setup</span></span>
<span data-ttu-id="8f566-177">Seuraavissa osissa käsitellään pakollisia Intrastat-raportoinnin asetuksia.</span><span class="sxs-lookup"><span data-stu-id="8f566-177">The following sections describe the settings that are required for Intrastat reporting.</span></span>

### <a name="set-up-all-required-intrastat-related-lists"></a><span data-ttu-id="8f566-178">Kaikkien Intrastatiin liittyvien luetteloiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8f566-178">Set up all required Intrastat-related lists</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f566-179">Luettelo</span><span class="sxs-lookup"><span data-stu-id="8f566-179">List</span></span></th>
<th><span data-ttu-id="8f566-180">Lisätiedot</span><span class="sxs-lookup"><span data-stu-id="8f566-180">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f566-181">Kauppatavarakoodit</span><span class="sxs-lookup"><span data-stu-id="8f566-181">Commodity codes</span></span></td>
<td><span data-ttu-id="8f566-182">Määritä tyypin <strong>Kauppatavarakoodi</strong> luokkahierarkia ja anna kaikki kauppatavarakoodit yhdistetyn nimikkeistöluettelon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8f566-182">Set up a category hierarchy of type <strong>Commodity code</strong>, and enter all commodity codes according to the combined nomenclature list.</span></span> <span data-ttu-id="8f566-183">Määritä jokaiselle kauppatavaralle seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="8f566-183">For each commodity, you set up the following information:</span></span>
<ul>
<li><span data-ttu-id="8f566-184">Kauppatavaran nimi ja kauppatavarakoodi</span><span class="sxs-lookup"><span data-stu-id="8f566-184">The name of the commodity and the commodity code</span></span></li>
<li><span data-ttu-id="8f566-185">Kutsumanimi ja/tai käännetty nimi</span><span class="sxs-lookup"><span data-stu-id="8f566-185">The friendly name and/or translated name</span></span></li>
<li><span data-ttu-id="8f566-186"><strong>Ulkomaankauppa</strong>-välilehden raportoinnin (lisä)yksiköiden asetukset. Voit valita lisäyksikön yksikköluettelosta.</span><span class="sxs-lookup"><span data-stu-id="8f566-186">Settings for reporting additional (supplementary) units on the <strong>Foreign trade</strong> tab. You can select the additional unit in the unit list.</span></span> <span data-ttu-id="8f566-187">Voit myös määrittää, raportoidaanko kauppatavaroiden paino valitun lisäyksikön lisäksi.</span><span class="sxs-lookup"><span data-stu-id="8f566-187">You can also specify whether the weight of commodities must be reported in addition to the selected additional unit.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f566-188">Tapahtumakoodit</span><span class="sxs-lookup"><span data-stu-id="8f566-188">Transaction codes</span></span></td>
<td><span data-ttu-id="8f566-189">Määritä tapahtuman luonne maan&#39; tai alueen&#39; vaatimusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8f566-189">Set up the nature of the transaction according to your country&#39;s/region&#39;s requirements.</span></span> <span data-ttu-id="8f566-190">Kullekin määritetylle tapahtumakoodille on määritettävä säännöt laskusummien sekä siirtotilausten ja myynti- ja ostotilausten tilastosummien laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="8f566-190">For each transaction code that you set up, you must set up the rules for calculating invoice amounts and statistical amounts for transfer orders and sales/purchase orders.</span></span>
<ul>
<li><span data-ttu-id="8f566-191">Siirtotilauksille määritetään jokin seuraavista laskusummien ja tilastosummien laskusäännöistä:</span><span class="sxs-lookup"><span data-stu-id="8f566-191">For transfer orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="8f566-192"><strong>Tyhjä</strong> – määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="8f566-192"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="8f566-193"><strong>Rahoituksellinen kustannus</strong> – summa on yhtä suuri kuin rahoituksellinen kustannus.</span><span class="sxs-lookup"><span data-stu-id="8f566-193"><strong>Financial cost amount</strong> – The amount will be equal to the financial cost.</span></span></li>
<li><span data-ttu-id="8f566-194"><strong>Kokonaiskustannukset</strong> – summa on yhtä suuri kuin tapahtuman kokonaiskustannukset.</span><span class="sxs-lookup"><span data-stu-id="8f566-194"><strong>Total cost</strong> – The amount will be equal to the total cost of the transaction.</span></span></li>
<li><span data-ttu-id="8f566-195"><strong>Manuaalinen</strong> – summa on yhtä suuri kuin siirtotilausrivillä manuaalisesti määritetty summa.</span><span class="sxs-lookup"><span data-stu-id="8f566-195"><strong>Manual</strong> – The amount will be equal to the amount that is manually specified on the transfer order line.</span></span></li>
</ul></li>
<li><span data-ttu-id="8f566-196">Myynti- ja ostotilauksille määritetään jokin seuraavista laskusummien ja tilastosummien laskusäännöistä:</span><span class="sxs-lookup"><span data-stu-id="8f566-196">For sales orders and purchase orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="8f566-197"><strong>Tyhjä</strong> – määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="8f566-197"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="8f566-198"><strong>Laskun summa</strong> – summa on yhtä suuri kuin kauppatavaran laskutettu summa.</span><span class="sxs-lookup"><span data-stu-id="8f566-198"><strong>Invoice amount</strong> – The amount will be equal to the amount that is invoiced for the commodity.</span></span></li>
<li><span data-ttu-id="8f566-199"><strong>Veron peruste</strong> – summa on yhtä suuri kuin summa, joka laskutetaan ennen alennusten käyttöä.</span><span class="sxs-lookup"><span data-stu-id="8f566-199"><strong>Base amount</strong> – The amount will be equal to the amount that would be invoiced before any discount is applied.</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f566-200">Välitystavat</span><span class="sxs-lookup"><span data-stu-id="8f566-200">Transport methods</span></span></td>
<td><span data-ttu-id="8f566-201">Määritä kuljetustapa maan&#39;s tai alueen&#39;; vaatimusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8f566-201">Set up the transport mode according to your country&#39;s/region&#39;s requirements.</span></span> <span data-ttu-id="8f566-202">Voit kullekin toimitustavalla oletuskuljetustavan <strong>Ulkomaankauppa</strong>-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="8f566-202">For each delivery mode, you can set up a default transport method on the <strong>Foreign trade</strong> tab.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f566-203">Satamat</span><span class="sxs-lookup"><span data-stu-id="8f566-203">Ports</span></span></td>
<td><span data-ttu-id="8f566-204">Määritä kuormauksen tai kuorman purkamisen satama tai lentoasema, jos kyseiset tiedot kerään maassa tai alueella.</span><span class="sxs-lookup"><span data-stu-id="8f566-204">Set up the port/airport of loading/unloading if this information is collected by your country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f566-205">Tilastomenettelyt</span><span class="sxs-lookup"><span data-stu-id="8f566-205">Statistics procedures</span></span></td>
<td><span data-ttu-id="8f566-206">Määritä tilastomenettely, jos nämä tiedot kerätään maassa tai alueella.</span><span class="sxs-lookup"><span data-stu-id="8f566-206">Set up the statistical procedure if this information is collected by your country/region.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a><span data-ttu-id="8f566-207">Intrastat-tapahtumien tiivistämissääntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8f566-207">Set up rules for compressing Intrastat transactions</span></span>

<span data-ttu-id="8f566-208">Voit valita **Intrastatin tiivistys** -sivulla tiivistyksessä käytettävät kentät.</span><span class="sxs-lookup"><span data-stu-id="8f566-208">On the **Compression of Intrastat** page, you can select the fields to use for compression.</span></span> <span data-ttu-id="8f566-209">Kaikki tapahtumat, joilla Intrastat-kirjauskansiossa valittujen kenttien kaltainen arvoyhdistelmä, tiivistetään yhdeksi tapahtumaksi, kun suoritat tiivistystoiminnon Intrastat-kirjauskansiossa.</span><span class="sxs-lookup"><span data-stu-id="8f566-209">All transactions that have the same combination of values for the selected fields in the Intrastat journal will be compressed into a single transaction when you run the Compress function in the Intrastat journal.</span></span>

### <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="8f566-210">Määritä ulkomaankaupan parametrit</span><span class="sxs-lookup"><span data-stu-id="8f566-210">Set up foreign trade parameters</span></span>

<span data-ttu-id="8f566-211">Määritä seuraavan taulun parametrit **Ulkomaankaupan parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="8f566-211">Use the **Foreign trade parameters** page to set up the parameters in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f566-212">Välilehti</span><span class="sxs-lookup"><span data-stu-id="8f566-212">Tab</span></span></th>
<th><span data-ttu-id="8f566-213">Parametrit</span><span class="sxs-lookup"><span data-stu-id="8f566-213">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f566-214">Yleinen</span><span class="sxs-lookup"><span data-stu-id="8f566-214">General</span></span></td>
<td><ul>
<li><span data-ttu-id="8f566-215"><strong>Yleinen</strong> – määritä seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="8f566-215"><strong>General</strong> – Specify the following information:</span></span>
<ul>
<li><span data-ttu-id="8f566-216">Myyntitilausten, ostotilausten, hyvityslaskujen ja siirtotilausten tapahtumakoodien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="8f566-216">The default transaction codes for sales orders, purchase orders, credit notes, and transfer orders.</span></span> <span data-ttu-id="8f566-217">Hyvityslaskulle määritettyä tapahtumakoodia käytetään myös fyysisten tavaroiden palautuskoodina, ja sitä käytetään poikkeavin fyysisten palautusten ja oikaisuhyvityslaskujen vertailussa.</span><span class="sxs-lookup"><span data-stu-id="8f566-217">The transaction code that is set up for credit notes is also used as the code for physical goods return and is used for deviating physical returns versus correction credit notes.</span></span> <span data-ttu-id="8f566-218">Fyysisten tavaroiden palautukset raportoidaan Intrastat-siirrossa eri suuntaan.</span><span class="sxs-lookup"><span data-stu-id="8f566-218">Returns of physical goods are reported in Intrastat transfer with a different direction.</span></span> <span data-ttu-id="8f566-219">Saapumisen palautus ilmoitetaan lähetykseksi ja lähetyksen palautus ilmoitetaan saapumiseksi.</span><span class="sxs-lookup"><span data-stu-id="8f566-219">The return of arrival is reported as dispatch and the return of dispatch is reported as arrival.</span></span></li>
<li><span data-ttu-id="8f566-220">Intrastat-raporttien valmistelusta vastaava työntekijä.</span><span class="sxs-lookup"><span data-stu-id="8f566-220">The employee who is responsible for preparing Intrastat reports.</span></span></li>
</ul></li>
<li><span data-ttu-id="8f566-221"><strong>Vähimmäisraja</strong> – määritä raja-arvon alittavien tapahtumien päivitysasetukset:</span><span class="sxs-lookup"><span data-stu-id="8f566-221"><strong>Minimum limit</strong> – Specify the settings for updating transactions that are below the threshold:</span></span>
<ul>
<li><span data-ttu-id="8f566-222">Raja-arvo ja paino</span><span class="sxs-lookup"><span data-stu-id="8f566-222">The threshold amount and weight</span></span></li>
<li><span data-ttu-id="8f566-223">Raja-arvon alittavissa tapahtumissa käytettävä kauppatavarakoodi</span><span class="sxs-lookup"><span data-stu-id="8f566-223">The commodity code to apply to transactions that are under the threshold</span></span></li>
</ul></li>
<li><span data-ttu-id="8f566-224"><strong>Siirrä</strong> – Määritä ehdot, joilla tapahtumat siirretään Intrastat-kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="8f566-224"><strong>Transfer</strong> – Specify the criteria for transferring transactions to the Intrastat journal.</span></span> <span data-ttu-id="8f566-225">Voit määrittää, että tapahtumat siirretään vasta, kun nimikkeissä toteutuu yksi seuraavista ehdoista tai kaikki ehdot toteutuvat:</span><span class="sxs-lookup"><span data-stu-id="8f566-225">You can specify that transactions are transferred only when the items meet one or all of the following criteria:</span></span>
<ul>
<li><span data-ttu-id="8f566-226">Nimikkeet eivät&#39; ole palvelunimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="8f566-226">The items aren&#39;t service items.</span></span></li>
<li><span data-ttu-id="8f566-227">Nimillä on kauppatavarakoodi.</span><span class="sxs-lookup"><span data-stu-id="8f566-227">The items have a commodity code.</span></span></li>
<li><span data-ttu-id="8f566-228">Nimikkeillä on paino.</span><span class="sxs-lookup"><span data-stu-id="8f566-228">The items have a weight.</span></span></li>
<li><span data-ttu-id="8f566-229">Nimikkeillä on lisäyksiköitä.</span><span class="sxs-lookup"><span data-stu-id="8f566-229">The items have additional units.</span></span></li>
</ul></li>
<li><span data-ttu-id="8f566-230"><strong>Tarkista asetukset</strong> – Määritä Intrastat-tietojen valmiusasteen tarkistussäännöt.</span><span class="sxs-lookup"><span data-stu-id="8f566-230"><strong>Check setup</strong> – Specify the rules for validating the completeness of Intrastat data.</span></span> <span data-ttu-id="8f566-231">Voit valita, mitkä tiedot tarkistetaan.</span><span class="sxs-lookup"><span data-stu-id="8f566-231">You can select which data is validated.</span></span></li>
<li><span data-ttu-id="8f566-232"><strong>Pyöristyssäännöt</strong> – määritä seuraavat Intrastat-raportoinnin pyöristyssummien ja painojen asetukset:</span><span class="sxs-lookup"><span data-stu-id="8f566-232"><strong>Rounding rules</strong> – Specify the following settings for rounding amounts and weights in Intrastat reporting:</span></span>
<ul>
<li><span data-ttu-id="8f566-233">Pyöristyssääntö (tarkkuus)</span><span class="sxs-lookup"><span data-stu-id="8f566-233">The rounding rule (precision)</span></span></li>
<li><span data-ttu-id="8f566-234">Pyöristystavoista: ylöspäin, alaspäin tai normaali</span><span class="sxs-lookup"><span data-stu-id="8f566-234">The rounding method: up, down, or normal</span></span></li>
<li><span data-ttu-id="8f566-235">Summien ja painojen desimaalien määrä</span><span class="sxs-lookup"><span data-stu-id="8f566-235">The number of decimal places for amounts and weights</span></span></li>
<li><span data-ttu-id="8f566-236">Ohjeet alle 1 kilogramman (kg) painojen pyöristämiseen: ylöspäin 1 kg:hen, normaali tai ei pyöristystä</span><span class="sxs-lookup"><span data-stu-id="8f566-236">Instructions for rounding weights that are less than 1 kilogram (kg): up to 1 kg, normal, or no rounding</span></span></li>
</ul></li>
<li><span data-ttu-id="8f566-237"><strong>Sähköinen raportointi</strong> – määritä viittaukset sähköisen raportoinnin määrityksiin, jotta voit luoda sähköisen tiedoston ja raportin.</span><span class="sxs-lookup"><span data-stu-id="8f566-237"><strong>Electronic reporting</strong> – Specify references to electronic reporting configurations, so that you can generate an electronic file and report.</span></span></li>
<li><span data-ttu-id="8f566-238"><strong>Kauppatavarakoodihierarkia</strong> – määritä Intrastat-kauppatavarakoodia CN8 ilmaiseva <strong>Kauppatavarakoodi</strong>-tyypin luokkahierarkia.</span><span class="sxs-lookup"><span data-stu-id="8f566-238"><strong>Commodity code hierarchy</strong> – Specify the category hierarchy of the <strong>Commodity code</strong> type that represents Intrastat commodity code CN8.</span></span></li>
  <li> <span data-ttu-id="8f566-239"><strong>Vaihtokurssin tyyppi</strong> – Voit myös määrittää vaihtokurssin, jota käytetään Intrastat-myynnin ja -oston raportointiin ulkomaalaisina valuuttoina.</span><span class="sxs-lookup"><span data-stu-id="8f566-239"><strong>Exchange rate type</strong> – Optionally, specify an exchange rate to be used to report Intrastat sales and purchase transactions in foreign currencies.</span></span> <span data-ttu-id="8f566-240">Tätä käytetään, jos kurssi ei ole sama kuin se, jota käytetään, kun tapahtuma kirjataan.</span><span class="sxs-lookup"><span data-stu-id="8f566-240">This is used if the rate is different than the one applied when posting the transaction.</span></span></li>  
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f566-241">Edustajan yhteystiedot</span><span class="sxs-lookup"><span data-stu-id="8f566-241">Agent contact information</span></span></td>
<td><span data-ttu-id="8f566-242">Määritä edustajan&#39; nimi, osoite, ALV-tunnus, puhelinnumero ja faksinumero.</span><span class="sxs-lookup"><span data-stu-id="8f566-242">Specify the agent&#39;s name, address, tax exempt number, telephone number, and fax number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f566-243">Maan tai alueen ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="8f566-243">Country/region properties</span></span></td>
<td><span data-ttu-id="8f566-244">Määritä nykyinen yritys maaksi tai alueeksi <strong>Kotimaa</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f566-244">Set the country/region of the current legal entity to <strong>Domestic</strong>.</span></span> <span data-ttu-id="8f566-245">Määritä nykyisen yrityksen kanssa EU-kauppaa tekevien EU-maiden tai -alueiden maaksi tai alueeksi <strong>EU</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f566-245">Set the country/region of EU countries/regions that participate in EU trade with the current legal entity to <strong>EU</strong>.</span></span> <span data-ttu-id="8f566-246">Kunkin maan tai alueen kohdalla ilmoitetaan myös maa- ta aluekoodi ulkomaankauppaa varten.</span><span class="sxs-lookup"><span data-stu-id="8f566-246">For each country/region, you also identify country/region code for foreign trade purposes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f566-247">Numerojärjestys</span><span class="sxs-lookup"><span data-stu-id="8f566-247">Number sequence</span></span></td>
<td><span data-ttu-id="8f566-248">Määritä Intrastat-kirjauskansion numerosarja.</span><span class="sxs-lookup"><span data-stu-id="8f566-248">Specify the number sequence for the Intrastat journal.</span></span></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
