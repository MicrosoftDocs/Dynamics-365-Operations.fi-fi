---
title: Laitteiston kokovaatimukset paikallisissa ympäristöissä
description: Tässä ohjeaiheessa käsitellään laitteiston kokovaatimukset paikallisissa ympäristöissä
author: sericks007
manager: AnnBe
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 9d4f2e59d4dd78d15d561ff0da47e4b9b1a2fce3
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798301"
---
# <a name="hardware-sizing-requirements-for-on-premises-environments"></a><span data-ttu-id="72697-103">Laitteiston kokovaatimukset paikallisissa ympäristöissä</span><span class="sxs-lookup"><span data-stu-id="72697-103">Hardware sizing requirements for on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72697-104">Tutustu ennen laitteiston ja infrastruktuurin koon määrittämistä paikallisiin ympäristöihin ja [pilvikäyttöönottojen järjestelmävaatimuksiin](system-requirements.md) sekä [asennus- ja käyttöönotto-ohjeisiin](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md), sillä saat niiden avulla selkeän käsityksen perustana olevasta infrastruktuurista.</span><span class="sxs-lookup"><span data-stu-id="72697-104">Before you begin the hardware and infrastructure sizing process for an on-premises environment, familiarize yourself with the [System requirements for cloud deployments](system-requirements.md) and [Setup and deployment instructions](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) to gain a solid understanding off the underlying infrastructure.</span></span>

> [!NOTE]
> <span data-ttu-id="72697-105">Perehdy huolellisesti järjestelmän asetuksen parhaisiin käytäntöihin, jotta järjestelmä toimisi mahdollisimman hyvin.</span><span class="sxs-lookup"><span data-stu-id="72697-105">Pay close attention to the system setup best practices for optimum performance.</span></span>

<span data-ttu-id="72697-106">Kun olet perehtynyt dokumentaatioon, voit aloittaa tapahtumien ja samanaikaisten käyttäjien määrää sekä määrittämään ympäristön koon ytimen keskimääräisen siirtomäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="72697-106">After you have reviewed the documentation, you can start the process of estimating your transactional and concurrent user volume and sizing your environment based on the average core throughput.</span></span>

## <a name="factors-that-affect-sizing"></a><span data-ttu-id="72697-107">Kokoon vaikuttavia tekijöitä</span><span class="sxs-lookup"><span data-stu-id="72697-107">Factors that affect sizing</span></span>

<span data-ttu-id="72697-108">Kaikki seuraavan kuvan tekijät vaikuttavat koon.</span><span class="sxs-lookup"><span data-stu-id="72697-108">All the factors shown in the following illustration contribute to sizing.</span></span> <span data-ttu-id="72697-109">Mitä tarkempia kerätyt tiedot ovat, sitä tarkemmin voit määrittää koon.</span><span class="sxs-lookup"><span data-stu-id="72697-109">The more detailed information that is collected, the more precisely you can determine sizing.</span></span> <span data-ttu-id="72697-110">Jos laitteiston koko määritetään ilman taustatietoja, lopputulos ei ole todennäköisesti tarkka.</span><span class="sxs-lookup"><span data-stu-id="72697-110">Hardware sizing, without supporting data, is likely to be inaccurate.</span></span> <span data-ttu-id="72697-111">Suurin tapahtumarivien määrä tunnissa on tieto, joka vähintäänkin tarvitaan.</span><span class="sxs-lookup"><span data-stu-id="72697-111">The absolute minimum requirement for necessary data is the peak transaction line load per hour.</span></span>

<span data-ttu-id="72697-112">[![Laitteiston koon määrittäminen paikallisissa ympäristöissä](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span><span class="sxs-lookup"><span data-stu-id="72697-112">[![Hardware sizing for on-premises environments](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span></span>

<span data-ttu-id="72697-113">Vasemmalta oikealle tarkasteltaessa tärkein tekijä, jonka avulla koko voidaan määrittää tarkasti, on tapahtumaprofiili tai tapahtuman kuvaus.</span><span class="sxs-lookup"><span data-stu-id="72697-113">Viewed from left to right, the first and most important factor needed to accurately estimate sizing is a transaction profile or a transaction characterization.</span></span> <span data-ttu-id="72697-114">On tärkeää, että suurin tapahtumien määrä tunnissa on tiedossa.</span><span class="sxs-lookup"><span data-stu-id="72697-114">It's important to always find the peak transactional volume per hour.</span></span> <span data-ttu-id="72697-115">Jos kuormitushuippuja on useita, nämä jaksot on määritettävä tarkasti.</span><span class="sxs-lookup"><span data-stu-id="72697-115">If there are multiple peak periods, then these periods need to be accurately defined.</span></span>

<span data-ttu-id="72697-116">Kun tiedät, miten kuormitus vaikuttaa infrastruktuuriin, sinun on saatava tarkemmat tiedot myös seuraavista tekijöistä:</span><span class="sxs-lookup"><span data-stu-id="72697-116">As you understand the load that impacts your infrastructure, you also need to understand more detail about these factors:</span></span>

- <span data-ttu-id="72697-117">**Tapahtumat** – Tapahtumilla on tavallisesti tietty huippu päivän tai viikon aikana.</span><span class="sxs-lookup"><span data-stu-id="72697-117">**Transactions** – Typically transactions have certain peaks throughout the day/week.</span></span> <span data-ttu-id="72697-118">Se puolestaan määräytyy lähinnä tapahtumatyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="72697-118">This mostly depends on the transaction type.</span></span> <span data-ttu-id="72697-119">Aika- ja tapahtumakirjauksissa huippu on yleensä kerran viikossa, kun taas myyntitilauskirjaukset tapahtuvat usein kerralla integroinnin kautta tai vähitellen päivän mittaan.</span><span class="sxs-lookup"><span data-stu-id="72697-119">Time and expense entries usually show peaks once per week, whereas Sales order entries often come in bulk via integration or trickle in during the day.</span></span>
- <span data-ttu-id="72697-120">**Yhtäaikaisten käyttäjien määrä** – Yhtäaikaisten käyttäjien määrä on toiseksi tärkein kokoon vaikuttava tekijä.</span><span class="sxs-lookup"><span data-stu-id="72697-120">**Number of concurrent users** – The number of concurrent users is the second most important sizing factor.</span></span> <span data-ttu-id="72697-121">Kokoarvioita ei saa luotettavasti yhtäaikaisten käyttäjien määrän perusteella, joten jos sinulla on vain nämä tiedot, arvioi määrä suunnilleen ja palaa tähän kohtaan, kun sinulla on enemmän tietoja.</span><span class="sxs-lookup"><span data-stu-id="72697-121">You cannot reliably get sizing estimates based on the number of concurrent users, so if this is the only data you have available, estimate an approximate number, and then revisit this when you have more data.</span></span> <span data-ttu-id="72697-122">Yhtäaikaisen käyttämän tarkan määritelmän mukaan</span><span class="sxs-lookup"><span data-stu-id="72697-122">An accurate concurrent user definition means that:</span></span>

    - <span data-ttu-id="72697-123">nimetyt käyttäjät eivät ole yhtäaikaisia käyttäjiä</span><span class="sxs-lookup"><span data-stu-id="72697-123">Named users are not concurrent users.</span></span>
    - <span data-ttu-id="72697-124">yhtäaikaiset käyttäjät ovat aina nimettyjen käyttäjien alijoukko</span><span class="sxs-lookup"><span data-stu-id="72697-124">Concurrent users are always a subset of named users.</span></span> 
    - <span data-ttu-id="72697-125">suurin kuormitus määrittää suurimman yhtäaikaisten käyttäjien määrän kokoa määritettäessä.</span><span class="sxs-lookup"><span data-stu-id="72697-125">Peak workload defines the maximum concurrency for sizing.</span></span>

    <span data-ttu-id="72697-126">Yhtäaikainen käyttäjä on käyttäjä, joka täyttää kaikki seuraavat ehdot:</span><span class="sxs-lookup"><span data-stu-id="72697-126">Criteria for concurrent users is that the user meets all the following criteria:</span></span>

    - <span data-ttu-id="72697-127">kirjautunut sisään</span><span class="sxs-lookup"><span data-stu-id="72697-127">Logged on.</span></span>
    - <span data-ttu-id="72697-128">käyttää tapahtumia tai kyselyjä laskennan aikana</span><span class="sxs-lookup"><span data-stu-id="72697-128">Working transactions/inquiries at the time of counting.</span></span>
    - <span data-ttu-id="72697-129">istunto ei ole käyttämätön.</span><span class="sxs-lookup"><span data-stu-id="72697-129">Not an idle session.</span></span>

- <span data-ttu-id="72697-130">**Tietoja kokoonpano** – Tämä tarkoittaa lähinnä sitä, miten järjestelmä asennetaan ja määritetään.</span><span class="sxs-lookup"><span data-stu-id="72697-130">**Data composition** – This is mostly about how your system will be set up and configured.</span></span> <span data-ttu-id="72697-131">Kyse voi olla esimerkiksi yritysten, nimikkeiden ja tuoterakennetasojen määrästä sekä suojausasetusten monimutkaisuudesta.</span><span class="sxs-lookup"><span data-stu-id="72697-131">For example, how many legal entities you will have, how many items, how many BOM levels, and how complex your security setup will be.</span></span> <span data-ttu-id="72697-132">Kukin näistä tekijöistä voi vaikuttaa jonkin verran suorituskykyyn, joten älykkäät infrastruktuuriratkaisut voivat kumota näiden tekijöiden vaikutuksen.</span><span class="sxs-lookup"><span data-stu-id="72697-132">Each of those factors may have a small impact on performance, so these factors can be offset by using smart choices when it comes to infrastructure.</span></span>
- <span data-ttu-id="72697-133">**Laajennukset** – Mukautukset voivat olla yksinkertaisia tai monimutkaisia.</span><span class="sxs-lookup"><span data-stu-id="72697-133">**Extensions** – Customizations can be simple or complex.</span></span> <span data-ttu-id="72697-134">Mukautusten määrä ja niiden monimutkaisuus ja käyttö vaikuttavat eri tavoin tarvittavan infrastruktuurin kokoon.</span><span class="sxs-lookup"><span data-stu-id="72697-134">The number of customizations and the nature of complexity and usage has a varied impact on the size of the infrastructure needed.</span></span> <span data-ttu-id="72697-135">Monimutkaisissa mukautuksissa kannattaa suorittaa suorituskykyarviointeja ja varmistaa näin teho testataan. Samalla saadaan parempi käsitys infrastruktuurin tarpeista.</span><span class="sxs-lookup"><span data-stu-id="72697-135">For complex customizations, it's advised to conduct performance evaluations to ensure that they are not only tested for efficiency but also help understand the infrastructure needs.</span></span> <span data-ttu-id="72697-136">Tämä on entistäkin tärkeämpää, kun laajennuksia ei ole koodattu suorituskyvyn ja skaalautuvuuden parhaiden käytäntöjen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="72697-136">This is even more critical when the extensions are not coded according to best practices for performance and scalability.</span></span>
- <span data-ttu-id="72697-137">**Raportointi ja analytiikka** – Nämä tekijät sisältävät yleensä raskaiden kyselyjen tekemistä useissa järjestelmän tietokannoissa.</span><span class="sxs-lookup"><span data-stu-id="72697-137">**Reporting and analytics** – These factors typically include running heavy queries against the various databases in the system.</span></span> <span data-ttu-id="72697-138">Tieto siitä, milloin laajoja raportteja ajetaan, ja niiden vähentäminen auttaa ymmärtämään, mikä vaikutus niillä on.</span><span class="sxs-lookup"><span data-stu-id="72697-138">Understanding and reducing the frequency when expensive reports run will help you understand the impact of them.</span></span>
- <span data-ttu-id="72697-139">**Kolmannen osapuolen ratkaisut** – näillä ratkaisuilla, kuten riippumattomilla ohjelmistotoimittajilla, on samat vaikutukset ja suositukset kuin laajennuksilla.</span><span class="sxs-lookup"><span data-stu-id="72697-139">**Third-party solutions** – These solutions, like ISVs, have the same implications and recommendations as extensions.</span></span>

## <a name="sizing-your-environment"></a><span data-ttu-id="72697-140">Ympäristön mitoitus</span><span class="sxs-lookup"><span data-stu-id="72697-140">Sizing your environment</span></span>

<span data-ttu-id="72697-141">Sinun on tiedettävä suurin käsiteltävä tapahtumien määrä kokovaatimusten selvittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="72697-141">To understand your sizing requirements, you need to know the peak volume of transactions that you need to process.</span></span> <span data-ttu-id="72697-142">Useimmat lisäjärjestelmät, kuten Management Reporter tai SSRS, eivät ole toiminnan kannalta yhtä tärkeitä.</span><span class="sxs-lookup"><span data-stu-id="72697-142">Most auxiliary systems, like Management Reporter or SSRS, are less mission critical.</span></span> <span data-ttu-id="72697-143">Tämän vuoksi tässä asiakirjassa käsitellään lähinnä AOS-palvelinta ja SQL Serveriä.</span><span class="sxs-lookup"><span data-stu-id="72697-143">As a result, this document focuses mostly on AOS and SQL Server.</span></span>

> [!NOTE]
> <span data-ttu-id="72697-144">Yleensä ottaen laskentatasot skaalautuvat ylöspäin ja ne on syytä määrittää muodossa N+1 – toisin sanoen jos arvioit tarpeeksi kolme AOS-palvelinta, lisää neljäs AOS.</span><span class="sxs-lookup"><span data-stu-id="72697-144">In general, the compute tiers scale out and should be set up in an N+1 fashion, meaning if you estimate three AOS, add a fourth AOS.</span></span> <span data-ttu-id="72697-145">Tietokantataso on määritettävä aina päällä olevana suuren käytettävyyden asennuksena.</span><span class="sxs-lookup"><span data-stu-id="72697-145">The database tier should be set up in an Always On highly-available setup.</span></span>

## <a name="sql-server-oltp"></a><span data-ttu-id="72697-146">SQL Server (OLTP)</span><span class="sxs-lookup"><span data-stu-id="72697-146">SQL Server (OLTP)</span></span>

### <a name="sizing"></a><span data-ttu-id="72697-147">Koko</span><span class="sxs-lookup"><span data-stu-id="72697-147">Sizing</span></span>

- <span data-ttu-id="72697-148">3 000–15 000 tapahtumariviä/tunti/ydin tietokantapalvelimessa.</span><span class="sxs-lookup"><span data-stu-id="72697-148">3K to 15K transaction lines per hour per core on DB server.</span></span>
- <span data-ttu-id="72697-149">Ensisijaisen SQL Serverin tavallinen AOS–SQL-ydinsuhde on 3:1.</span><span class="sxs-lookup"><span data-stu-id="72697-149">Typical AOS-to-SQL core ratio 3:1 for the primary SQL Server.</span></span> <span data-ttu-id="72697-150">Lisäytimiä tarvitaan valitun suuren käyttävyyden määrityksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="72697-150">Additional cores are required based on the chosen high availability configuration.</span></span>

    - <span data-ttu-id="72697-151">Paljon tietokantoja käyttävien toimenpiteiden käsittely jo pienentää suhteeksi 2:1.</span><span class="sxs-lookup"><span data-stu-id="72697-151">Processing database-heavy operations may regress this to 2:1.</span></span>

- <span data-ttu-id="72697-152">Seuraavat tekijät vaikuttavat vaihteluun:</span><span class="sxs-lookup"><span data-stu-id="72697-152">The following factors influence variations:</span></span>

    - <span data-ttu-id="72697-153">Käytettävät parametriasetukset.</span><span class="sxs-lookup"><span data-stu-id="72697-153">Parameter settings in use.</span></span>
    - <span data-ttu-id="72697-154">Laajennusten tasot.</span><span class="sxs-lookup"><span data-stu-id="72697-154">Levels of extensions.</span></span>
    - <span data-ttu-id="72697-155">Lisätietojen, kuten tietokantalokin ja hälytysten, käyttö.</span><span class="sxs-lookup"><span data-stu-id="72697-155">Usage of additional functionality, such as database log and alerts.</span></span> <span data-ttu-id="72697-156">Suuri tietokantalokiin kirjaus pienentää entisestään tunti- ja ydinkohtaisen siirtomäärän alle 3 000 riviin.</span><span class="sxs-lookup"><span data-stu-id="72697-156">Extreme database logging will further reduce throughput per hour per core below 3K lines.</span></span>
    - <span data-ttu-id="72697-157">Tietojen kokopanon monimutkaisuus – esimerkiksi yksinkertaisen tilikartan tai tarkan ja yksityiskohtaisen tilikartan valitsimen vaikuttaa siirtomäärään.</span><span class="sxs-lookup"><span data-stu-id="72697-157">Complexity of data composition – A simple chart of accounts versus a detailed fine-grained chart of accounts has implications on throughput (as an example).</span></span>
    - <span data-ttu-id="72697-158">Tapahtuman kuvaus.</span><span class="sxs-lookup"><span data-stu-id="72697-158">Transaction characterization.</span></span>
    - <span data-ttu-id="72697-159">2–16 Gt muistia/ydin.</span><span class="sxs-lookup"><span data-stu-id="72697-159">2 GB to 16 GB memory for each core.</span></span>
    - <span data-ttu-id="72697-160">Tietokantapalvelimen lisätietokannat, kuten Management Reporter- ja SSRS-tietokannat.</span><span class="sxs-lookup"><span data-stu-id="72697-160">Auxiliary databases on DB server such as Management reporter and SSRS databases.</span></span>
    - <span data-ttu-id="72697-161">Tilapäistietokanta = 15 prosenttia tietokannan koosta, ja tiedostoja on yhtä paljon kuin fyysisiä suorittimia.</span><span class="sxs-lookup"><span data-stu-id="72697-161">Temp DB = 15% of DB size, with as many files as physical processors.</span></span>
    - <span data-ttu-id="72697-162">SAN-koko ja -siirtomäärä yhtäaikaisten tapahtumien yhteismäärän ja -käytön perusteella.</span><span class="sxs-lookup"><span data-stu-id="72697-162">SAN size and throughput based on total concurrent transaction volume/usage.</span></span>

### <a name="high-availability"></a><span data-ttu-id="72697-163">Suuri käytettävyys</span><span class="sxs-lookup"><span data-stu-id="72697-163">High availability</span></span>

<span data-ttu-id="72697-164">SQL Serveriä kannattaa aina käyttää joko klusterina tai peilaavana asennuksena.</span><span class="sxs-lookup"><span data-stu-id="72697-164">We recommend always utilizing SQL Server in either a cluster or mirroring setup.</span></span> <span data-ttu-id="72697-165">Toisessa SQL-solmussa on oltava yhtä monta ydintä kuin ensisijaisessa solmussa.</span><span class="sxs-lookup"><span data-stu-id="72697-165">The second SQL node should have the same number of cores as the primary node.</span></span>

### <a name="active-directory-federation-services-ad-fs"></a><span data-ttu-id="72697-166">Active Directory -liittoutumispalvelut (AD FS)</span><span class="sxs-lookup"><span data-stu-id="72697-166">Active Directory Federation Services (AD FS)</span></span>

<span data-ttu-id="72697-167">Lisätietoja AD FS -kokomäärityksistä on [AD FS:n palvelinkapasiteetin dokumentaatiossa](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span><span class="sxs-lookup"><span data-stu-id="72697-167">For AD FS sizing, see the [AD FS Server Capacity documentation](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span></span>

<span data-ttu-id="72697-168">Käyttöönoton esiintymien määrän suunnittelua varten on [kokotaulukko](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx).</span><span class="sxs-lookup"><span data-stu-id="72697-168">A [sizing spreadsheet](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) is available for planning the number of instances in your deployment.</span></span>

## <a name="aos-online-and-batch"></a><span data-ttu-id="72697-169">AOS (verkko ja erä)</span><span class="sxs-lookup"><span data-stu-id="72697-169">AOS (Online and batch)</span></span>

### <a name="sizing"></a><span data-ttu-id="72697-170">Koko</span><span class="sxs-lookup"><span data-stu-id="72697-170">Sizing</span></span>

- <span data-ttu-id="72697-171">Tapahtumien määrän ja käytön mukaan tapahtuva koon määritys</span><span class="sxs-lookup"><span data-stu-id="72697-171">Sizing by transaction volume/usage</span></span>

    - <span data-ttu-id="72697-172">2 000–6 000 riviä/ydin</span><span class="sxs-lookup"><span data-stu-id="72697-172">2K to 6K lines per core</span></span>
    - <span data-ttu-id="72697-173">16 Gt/esiintymä</span><span class="sxs-lookup"><span data-stu-id="72697-173">16 GB per instance</span></span>
    - <span data-ttu-id="72697-174">Vakiorunko – 4–24 ydintä</span><span class="sxs-lookup"><span data-stu-id="72697-174">Standard box – 4 to 24 cores</span></span>
    - <span data-ttu-id="72697-175">10–15 Enterprise-käyttäjää/ydin</span><span class="sxs-lookup"><span data-stu-id="72697-175">10 to 15 Enterprise users per core</span></span>
    - <span data-ttu-id="72697-176">15–25 tehtäväkäyttäjää/ydin</span><span class="sxs-lookup"><span data-stu-id="72697-176">15 to 25 Activity users per core</span></span>
    - <span data-ttu-id="72697-177">25–50 ryhmän jäsentä/ydin</span><span class="sxs-lookup"><span data-stu-id="72697-177">25 to 50 Team members per core</span></span>

- <span data-ttu-id="72697-178">Erä</span><span class="sxs-lookup"><span data-stu-id="72697-178">Batch</span></span>

    - <span data-ttu-id="72697-179">1–4 eräsäiettä/ydin</span><span class="sxs-lookup"><span data-stu-id="72697-179">1 to 4 batch threads per core</span></span>
    - <span data-ttu-id="72697-180">Koko perustuu eräikkunan kuvaukseen</span><span class="sxs-lookup"><span data-stu-id="72697-180">Size based on batch window characterization</span></span>

- <span data-ttu-id="72697-181">Huomaa, että AOS, tietojen hallinta ja erä ovat samassa roolissa Service Fabricissa.</span><span class="sxs-lookup"><span data-stu-id="72697-181">Note that the AOS, Data Management, and Batch are on the same role in the Service Fabric.</span></span> <span data-ttu-id="72697-182">Koko on määritettävä näiden kolmen toiminnon yhdistetylle kuormitukselle eikä erikseen niin kuin Microsoft Dynamics AX 2012:ssa.</span><span class="sxs-lookup"><span data-stu-id="72697-182">You need to size for these three workloads combined, and not separate these like in Microsoft Dynamics AX 2012.</span></span>
- <span data-ttu-id="72697-183">SQL Serverin vaihtelutekijät koskevat myös näitä kokomäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="72697-183">The same variability factors for SQL Server apply here.</span></span>

### <a name="high-availability"></a><span data-ttu-id="72697-184">Suuri käytettävyys</span><span class="sxs-lookup"><span data-stu-id="72697-184">High availability</span></span>

- <span data-ttu-id="72697-185">Varmista, että käytettävissä on vähintään 1–2 AOS-palvelinta enemmän kuin mitä arvioit.</span><span class="sxs-lookup"><span data-stu-id="72697-185">Ensure that you have at least 1 to 2 more AOS available than you estimate.</span></span>
- <span data-ttu-id="72697-186">Varmista, että käytettävissä on ainakin 3–4 virtuaali-isäntää.</span><span class="sxs-lookup"><span data-stu-id="72697-186">Ensure that you have at least 3 to 4 virtual hosts available.</span></span>

## <a name="management-reporter"></a><span data-ttu-id="72697-187">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="72697-187">Management reporter</span></span>

<span data-ttu-id="72697-188">Ellei käyttö ole erittäin suurta suositeltu vähimmäisvaatimus on useimmissa tapauksissa kaksi solmua.</span><span class="sxs-lookup"><span data-stu-id="72697-188">In most cases, unless used extensively, the recommended minimum requirements using two nodes should work well.</span></span> <span data-ttu-id="72697-189">Vain siinä tapauksessa, että käyttö on erittäin runsasta, tarvitaan enemmän kuin kaksi solmua.</span><span class="sxs-lookup"><span data-stu-id="72697-189">Only in cases where there is heavy use will you need more than two nodes.</span></span> <span data-ttu-id="72697-190">Skaalaa tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="72697-190">Please scale as needed.</span></span>

## <a name="sql-server-reporting-services"></a><span data-ttu-id="72697-191">SQL Server -raportointipalvelut.</span><span class="sxs-lookup"><span data-stu-id="72697-191">SQL Server Reporting Services</span></span>

<span data-ttu-id="72697-192">Yleisesti saatavilla olevassa julkaisuversiossa voidaan ottaa käyttöön vain yksi SSRS-solmu.</span><span class="sxs-lookup"><span data-stu-id="72697-192">For the general availability release, only one SSRS node can be deployed.</span></span> <span data-ttu-id="72697-193">Seuraa SSRS-solmua testauksen aikana ja lisää SSRS:n käytössä olevien ytimien määrää tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="72697-193">Monitor your SSRS node while testing and increase the number of cores available for SSRS on a need basis.</span></span> <span data-ttu-id="72697-194">Varmista, että virtuaali-isäntään valmiiksi määritetty toissijainen solmu ei ole sama kuin SSRS VM.</span><span class="sxs-lookup"><span data-stu-id="72697-194">Make sure that you have a preconfigured secondary node available on a virtual host that is different than the SSRS VM.</span></span> <span data-ttu-id="72697-195">Tämä on tärkeää, jos SSRS:ää isännöivässä virtuaalikoneessa tai virtuaali-isännässä on ongelma.</span><span class="sxs-lookup"><span data-stu-id="72697-195">This is important if there is an issue with the virtual machine that hosts SSRS or the virtual host.</span></span> <span data-ttu-id="72697-196">Siinä tapauksessa ne on vaihdettava.</span><span class="sxs-lookup"><span data-stu-id="72697-196">If this the case, they would need to be replaced.</span></span>

## <a name="environment-orchestrator"></a><span data-ttu-id="72697-197">Ympäristön Orchestrator-palvelu</span><span class="sxs-lookup"><span data-stu-id="72697-197">Environment Orchestrator</span></span>

<span data-ttu-id="72697-198">Orchestrator-palvelu hallitsee käyttöönottoa ja siihen liittyviä LCS-yhteyksiä.</span><span class="sxs-lookup"><span data-stu-id="72697-198">The Orchestrator service is the service that manages your deployment and the related communication with LCS.</span></span> <span data-ttu-id="72697-199">Palvelu otetaan käyttöön ensisijaisena Service Fabric -palveluna, ja sitä varten tarvitaan vähintään kolme VM-konetta.</span><span class="sxs-lookup"><span data-stu-id="72697-199">This service is deployed as the primary Service Fabric service and requires at least three VMs.</span></span> <span data-ttu-id="72697-200">Palvelu on samassa sijainnissa kuin Service Fabricin Orchestration-palvelut.</span><span class="sxs-lookup"><span data-stu-id="72697-200">This service is co-located with the Service Fabric orchestration services.</span></span> <span data-ttu-id="72697-201">Sen koon pitäisi perustua klusterin suurimpaan kuormitukseen.</span><span class="sxs-lookup"><span data-stu-id="72697-201">This and should be sized to the peak load of the cluster.</span></span> <span data-ttu-id="72697-202">Lisätietoja on ohjeaiheessa [Service Fabric -klusterin erillisen käyttöönoton suunnittelu ja valmistelu](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span><span class="sxs-lookup"><span data-stu-id="72697-202">For more information, see [Plan and prepare your Service Fabric Standalone cluster deployment](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

## <a name="virtualization-and-oversubscription"></a><span data-ttu-id="72697-203">Virtualisointi ja ylitilaus</span><span class="sxs-lookup"><span data-stu-id="72697-203">Virtualization and oversubscription</span></span>

<span data-ttu-id="72697-204">Toiminnan kannalta keskeiset palvelut, kuten AOS, on isännöitävä virtuaali-isännissä, joille on varattu omat resurssit (ytimet, muisti ja levy).</span><span class="sxs-lookup"><span data-stu-id="72697-204">Mission critical services like the AOS should be hosted on Virtual hosts that have dedicated resources – cores, memory, and disk.</span></span>
