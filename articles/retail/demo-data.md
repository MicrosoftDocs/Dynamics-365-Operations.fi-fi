---
title: "Demotietojen näytön asettelut Retail Modern POS:issa (MPOS) ja Cloud POS:issa"
description: "Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 for Retail -sovelluksen myyntipisteiden käyttökokemusten demotietojoukon näyttöasetteluista."
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 41930e89a7cae5cdb84e728da47de3bc5de312ca
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="demo-data-screen-layouts-in-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="38028-103">Demotietojen näytön asettelut Retail Modern POS:issa (MPOS) ja Cloud POS:issa</span><span class="sxs-lookup"><span data-stu-id="38028-103">Demo data screen layouts in Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="38028-104">Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 for Retail -sovelluksen myyntipisteiden käyttökokemusten demotietojoukon näyttöasetteluista.</span><span class="sxs-lookup"><span data-stu-id="38028-104">This topic provides information about the screen layouts that are included with the demo data set for the point of sale (POS) experiences in Microsoft Dynamics 365 for Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="38028-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="38028-105">Overview</span></span>

<span data-ttu-id="38028-106">Retail-demotietoihin sisältyvissä mallinäyttöasetteluissa on sisältöä, joka on optimoitu useita vähittäismyyntisegmenttejä, myymälän työntekijöiden rooleja ja laitteita varten.</span><span class="sxs-lookup"><span data-stu-id="38028-106">The sample screen layouts that are included with Retail demo data provide content that is optimized for various retail segments, store worker roles, and devices.</span></span> <span data-ttu-id="38028-107">Yksi asettelu voi sisältää useita painikeruudukoiden asettelukokoja ja -yhdistelmiä. Näin myymälän työntekijät voiva siirtyä laitteiden ja asemien välillä.</span><span class="sxs-lookup"><span data-stu-id="38028-107">A single layout can contain several layout sizes and combinations of button grids, to help ensure coverage as store workers move between devices and stations.</span></span> <span data-ttu-id="38028-108">Tässä ohjeaiheessa käsitellään näiden asetteluiden välisiä eroja, asetteluiden työvaiheita ja niiden mahdollistamia yleisiä käyttökokemuksia.</span><span class="sxs-lookup"><span data-stu-id="38028-108">This topic highlights the differences between these layouts, the operations that they provide, and the overall experiences that they deliver.</span></span>

![Laitteiden välisten demotietojen asettelut](../retail/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a><span data-ttu-id="38028-110">Näyttöasettelun tunnuksen rakenne</span><span class="sxs-lookup"><span data-stu-id="38028-110">Anatomy of a screen layout ID</span></span>

<span data-ttu-id="38028-111">Retail-sovelluksen äyttöasettelut ovat kohdassa **Retail** > **Kanavan asetukset** > **Myyntipisteen asetukset** > **Myyntipiste** > **Näyttöasetukset**.</span><span class="sxs-lookup"><span data-stu-id="38028-111">To find screen layouts in Retail, go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>

![Retail-sovelluksen näyttöasettelut](../retail/media/demo-screen-layouts-fig-2-1.png)

<span data-ttu-id="38028-113">Näyttöasetteluiden tunnuksissa voi olla enintään 10 merkkiä.</span><span class="sxs-lookup"><span data-stu-id="38028-113">Screen layout IDs can have a maximum of 10 characters.</span></span> <span data-ttu-id="38028-114">Tunnus on merkkijono, joka sisältää seuraavat kolme tietoa tässä järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="38028-114">The ID is a string that consists of three pieces of information, in this order:</span></span>

1. <span data-ttu-id="38028-115">Yritys </span><span class="sxs-lookup"><span data-stu-id="38028-115">Company</span></span>
2. <span data-ttu-id="38028-116">Asetteluversio</span><span class="sxs-lookup"><span data-stu-id="38028-116">Layout version</span></span>
3. <span data-ttu-id="38028-117">Henkilötyyppi</span><span class="sxs-lookup"><span data-stu-id="38028-117">Persona</span></span>

### <a name="company"></a><span data-ttu-id="38028-118">Yritys </span><span class="sxs-lookup"><span data-stu-id="38028-118">Company</span></span>

| <span data-ttu-id="38028-119">Kirje</span><span class="sxs-lookup"><span data-stu-id="38028-119">Letter</span></span> | <span data-ttu-id="38028-120">Yritys </span><span class="sxs-lookup"><span data-stu-id="38028-120">Company</span></span>         |
|--------|-----------------|
| <span data-ttu-id="38028-121">A</span><span class="sxs-lookup"><span data-stu-id="38028-121">A</span></span>      | <span data-ttu-id="38028-122">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="38028-122">Adventure Works</span></span> |
| <span data-ttu-id="38028-123">P</span><span class="sxs-lookup"><span data-stu-id="38028-123">F</span></span>      | <span data-ttu-id="38028-124">Fabrikam:</span><span class="sxs-lookup"><span data-stu-id="38028-124">Fabrikam</span></span>        |
| <span data-ttu-id="38028-125">Y</span><span class="sxs-lookup"><span data-stu-id="38028-125">C</span></span>      | <span data-ttu-id="38028-126">Contoso</span><span class="sxs-lookup"><span data-stu-id="38028-126">Contoso</span></span>         |

### <a name="layout-version"></a><span data-ttu-id="38028-127">Asetteluversio</span><span class="sxs-lookup"><span data-stu-id="38028-127">Layout version</span></span>

| <span data-ttu-id="38028-128">Version numero</span><span class="sxs-lookup"><span data-stu-id="38028-128">Version number</span></span> | <span data-ttu-id="38028-129">kuvaus</span><span class="sxs-lookup"><span data-stu-id="38028-129">Description</span></span>                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="38028-130">3</span><span class="sxs-lookup"><span data-stu-id="38028-130">3</span></span>              | <span data-ttu-id="38028-131">Perusversio, joka tukee eri laitteiden ja kuvasuhteiden useita näyttökokoja</span><span class="sxs-lookup"><span data-stu-id="38028-131">The base version that supports multiple screen sizes for various devices and aspect ratios</span></span> |
| <span data-ttu-id="38028-132">3.1</span><span class="sxs-lookup"><span data-stu-id="38028-132">3.1</span></span>            | <span data-ttu-id="38028-133">Perusversio, jolla on **Suositellut tuotteet** -ruudun lisätuki</span><span class="sxs-lookup"><span data-stu-id="38028-133">The base version that has additional support for the **Recommended products** panel</span></span>        |

### <a name="persona"></a><span data-ttu-id="38028-134">Henkilötyyppi</span><span class="sxs-lookup"><span data-stu-id="38028-134">Persona</span></span>

| <span data-ttu-id="38028-135">Lyhenne</span><span class="sxs-lookup"><span data-stu-id="38028-135">Abbreviation</span></span> | <span data-ttu-id="38028-136">Henkilötyyppi</span><span class="sxs-lookup"><span data-stu-id="38028-136">Persona</span></span>       | <span data-ttu-id="38028-137">Sisältö</span><span class="sxs-lookup"><span data-stu-id="38028-137">Contents</span></span> |
|--------------|---------------|----------|
| <span data-ttu-id="38028-138">CSH</span><span class="sxs-lookup"><span data-stu-id="38028-138">CSH</span></span>          | <span data-ttu-id="38028-139">Kassa</span><span class="sxs-lookup"><span data-stu-id="38028-139">Cashier</span></span>       | <span data-ttu-id="38028-140">Kassa-asettelut sisältävät kaikki tapahtumiin liittyvät työvaiheet, kuten asiakastilaukset, palautukset, alennukset, mitätöinnit ja lahjakortit.</span><span class="sxs-lookup"><span data-stu-id="38028-140">Cashier layouts include all transaction-related operations, such as customer orders, returns, discounts, voids, and gift cards.</span></span> <span data-ttu-id="38028-141">Nämä asettelut sisältävät myös varastonhallinnan päivittäiset tehtävät, kuten hintatarkistukset, varastohaut ja varaston inventoinnit.</span><span class="sxs-lookup"><span data-stu-id="38028-141">These layouts also include daily tasks for inventory management, such price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="38028-142">Aloitussummat, vuorojen keskeytykset ja kello sisältävät myös perusvuorojen hallinnan.</span><span class="sxs-lookup"><span data-stu-id="38028-142">Basic shift management is also provided for start amounts, suspending shifts, and time clock.</span></span> |
| <span data-ttu-id="38028-143">MGR</span><span class="sxs-lookup"><span data-stu-id="38028-143">MGR</span></span>          | <span data-ttu-id="38028-144">Myymäläpäällikkö</span><span class="sxs-lookup"><span data-stu-id="38028-144">Store Manager</span></span> | <span data-ttu-id="38028-145">Myymäläpäällikön asettelu sisältää kaikki tapahtumiin liittyvät työvaiheet, jotka löytyvät kassanhoitajan asetteluista. Niiden lisäksi se sisältää verojen ohitukset.</span><span class="sxs-lookup"><span data-stu-id="38028-145">Store Manager layouts include all transaction-related operations that are found in the Cashier layouts but also include tax overrides.</span></span> <span data-ttu-id="38028-146">Nämä asettelut sisältävät myös varastonhallinnan päivittäiset tehtävät, kuten hintatarkistukset, varastohaut ja varaston inventoinnit.</span><span class="sxs-lookup"><span data-stu-id="38028-146">These layouts also include daily tasks for inventory management, such as price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="38028-147">Vuoronhallinta sisältää vuorojen aloittamisen, keskeyttämisen ja päättämisen.</span><span class="sxs-lookup"><span data-stu-id="38028-147">Shift management is provided for starting, suspending, and closing shifts.</span></span> <span data-ttu-id="38028-148">Lisäksi asettelut sisältävät kassatoiminnot tapahtumille, poistoille, kassan laskemiselle maksuvälineittäin ja toimituksille kassakaappiin ja pankkiin.</span><span class="sxs-lookup"><span data-stu-id="38028-148">Additionally, the layouts include drawer operations for entries, removals, tender declarations, and safe and bank drops.</span></span> <span data-ttu-id="38028-149">Näiden asetteluiden avulla voi myös käyttää suoritusraportteja ja tulostaa X- ja Z-raportteja.</span><span class="sxs-lookup"><span data-stu-id="38028-149">Finally, these layouts include access to performance reports, and enable X and Z reports to be printed.</span></span> |
| <span data-ttu-id="38028-150">STK</span><span class="sxs-lookup"><span data-stu-id="38028-150">STK</span></span>          | <span data-ttu-id="38028-151">Varastonhoitaja</span><span class="sxs-lookup"><span data-stu-id="38028-151">Stock Clerk</span></span>   | <span data-ttu-id="38028-152">Varastonhoitajan asettelut on optimoitu varastonhallintaa varten.</span><span class="sxs-lookup"><span data-stu-id="38028-152">Stock Clerk layouts are optimized for inventory management.</span></span> <span data-ttu-id="38028-153">Niiden avulla voi käyttää hinnantarkistusten, varastohakujen, keräilyjen ja vastaanottojen, varaston inventointien ja myyntirakenteen purkamisen päivittäisiä tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="38028-153">They include access to daily tasks for price checks, inventory lookups, picking and receiving, stock counts, and kit disassembly.</span></span> <span data-ttu-id="38028-154">Nämä asettelut sisältävät myös aikaan ja vuorojen keskeytykseen liittyvät vuorojen perustyövaiheet.</span><span class="sxs-lookup"><span data-stu-id="38028-154">These layouts also provide basic shift operations for time clock and suspending shifts.</span></span> <span data-ttu-id="38028-155">Vaikka nämä asettelut on tarkoitettu pääasiassa tilausjärjestelmätehtäviä varten, myymälänhoitajilla on samoja tapahtumanäyttöjen työvaiheet kuin kassanhoitajilla.</span><span class="sxs-lookup"><span data-stu-id="38028-155">Although these layouts are intended mainly for back-office tasks, stock clerks have the same operations as cashiers for transaction screens.</span></span> |

### <a name="example-layout"></a><span data-ttu-id="38028-156">Esimerkkiasettelu</span><span class="sxs-lookup"><span data-stu-id="38028-156">Example layout</span></span>

<span data-ttu-id="38028-157">Tässä on esimerkki Fabrikam-yrityksen asettelun versio 3 näyttöasettelun tunnuksesta sekä myymäläpäällikön henkilötyyppi:</span><span class="sxs-lookup"><span data-stu-id="38028-157">Here is an example of a screen layout ID for the Fabrikam company, layout version 3, and the Store Manager persona:</span></span>

<span data-ttu-id="38028-158">F3MGR</span><span class="sxs-lookup"><span data-stu-id="38028-158">F3MGR</span></span>

<span data-ttu-id="38028-159">Seuraavassa kuvassa on esimerkki Fabrikamin myymäläpäällikön aloitusnäytöstä.</span><span class="sxs-lookup"><span data-stu-id="38028-159">The following illustration shows an example of the Welcome screen for a Fabrikam store manager.</span></span>

![Fabrikam myymäläpäällikön aloitusnäyttö](../retail/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a><span data-ttu-id="38028-161">Asettelukoot</span><span class="sxs-lookup"><span data-stu-id="38028-161">Layout sizes</span></span>

### <a name="full-vs-compact-layouts"></a><span data-ttu-id="38028-162">Täydeliset ja kompaktit asettelut</span><span class="sxs-lookup"><span data-stu-id="38028-162">Full vs. compact layouts</span></span>

<span data-ttu-id="38028-163">Näyttöasettelu voi sisältää täysikokoisten ja pienikokoisten laitteiden kokoonpanoja.</span><span class="sxs-lookup"><span data-stu-id="38028-163">A screen layout can have configurations for both full devices and compact devices.</span></span> <span data-ttu-id="38028-164">Tämän vuoksi käyttäjä voidaan määrittää yhteen näyttöasetteluun, joka toimii myymälän erikokoissa ja erityyppisissä laitteissa.</span><span class="sxs-lookup"><span data-stu-id="38028-164">Therefore, a user can be assigned to a single screen layout that will work across various sizes and form factors in the store.</span></span>

- <span data-ttu-id="38028-165">**Modern POS - täydellinen** - täydelliset asettelut ovat yleensä parhaimmillaan suurissa näytöissä kuten pöytätietokoneiden näytöissä tai tableteissa.</span><span class="sxs-lookup"><span data-stu-id="38028-165">**Modern POS - Full** – Typically, full layouts are best used for larger displays, such as desktop computer monitors or tablets.</span></span> <span data-ttu-id="38028-166">Käyttäjät voivat valita asettelun sisältämät käyttöliittymäelementit, määrittää elementtien koon ja sijoittelun sekä elementtien yksityiskohtaiset ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="38028-166">Users can select the UI elements that the layout includes, specify the size and placement of those elements, and configure their detailed properties.</span></span> <span data-ttu-id="38028-167">Täydelliset asettelut tukevat sekä vaaka- että pystykokoonpanoja.</span><span class="sxs-lookup"><span data-stu-id="38028-167">Full layouts support both portrait and landscape configurations.</span></span>
- <span data-ttu-id="38028-168">**Modern POS - kompakti** - kompaktit asettelut sopivat yleensä parhaiten puhelimiin tai pieniin tabletteihin.</span><span class="sxs-lookup"><span data-stu-id="38028-168">**Modern POS - Compact** – Typically, compact layouts are best used for phones or small tablets.</span></span> <span data-ttu-id="38028-169">Kompaktien laitteiden suunnittelumahdollisuudet ovat rajalliset.</span><span class="sxs-lookup"><span data-stu-id="38028-169">Design possibilities are limited for compact devices.</span></span> <span data-ttu-id="38028-170">Käyttäjät voivat määrittää kuitti- ja summaruutujen sarakkeet ja kentät.</span><span class="sxs-lookup"><span data-stu-id="38028-170">Users can configure the columns and fields for the receipt pane and the totals pane.</span></span>

### <a name="screen-resolutions-that-are-provided"></a><span data-ttu-id="38028-171">Käytettävissä olevat näytön tarkkuudet</span><span class="sxs-lookup"><span data-stu-id="38028-171">Screen resolutions that are provided</span></span>

<span data-ttu-id="38028-172">Seuraavassa taulukossa ovat tavallisissa näyttöjen resoluutioissa käytettävissä olevat asetteluiden koot.</span><span class="sxs-lookup"><span data-stu-id="38028-172">The following table shows the layout sizes that are provided for typical screen resolutions.</span></span>

| <span data-ttu-id="38028-173">Asettelutyyppi</span><span class="sxs-lookup"><span data-stu-id="38028-173">Layout type</span></span> | <span data-ttu-id="38028-174">Tarkkuus</span><span class="sxs-lookup"><span data-stu-id="38028-174">Resolution</span></span> | <span data-ttu-id="38028-175">Kuvasuhde</span><span class="sxs-lookup"><span data-stu-id="38028-175">Aspect ratio</span></span> | <span data-ttu-id="38028-176">Kohdenäyttö</span><span class="sxs-lookup"><span data-stu-id="38028-176">Target display</span></span>          |
|-------------|------------|--------------|-------------------------|
| <span data-ttu-id="38028-177">Järjestä uudelleen\*</span><span class="sxs-lookup"><span data-stu-id="38028-177">Compact\*</span></span>   | <span data-ttu-id="38028-178">480 × 853</span><span class="sxs-lookup"><span data-stu-id="38028-178">480 × 853</span></span>  | <span data-ttu-id="38028-179">16:9</span><span class="sxs-lookup"><span data-stu-id="38028-179">16:9</span></span>         | <span data-ttu-id="38028-180">Puhelimet</span><span class="sxs-lookup"><span data-stu-id="38028-180">Phones</span></span>                  |
| <span data-ttu-id="38028-181">Täysi</span><span class="sxs-lookup"><span data-stu-id="38028-181">Full</span></span>        | <span data-ttu-id="38028-182">1 024 × 768</span><span class="sxs-lookup"><span data-stu-id="38028-182">1024 × 768</span></span> | <span data-ttu-id="38028-183">4:3</span><span class="sxs-lookup"><span data-stu-id="38028-183">4:3</span></span>          | <span data-ttu-id="38028-184">Tabletit</span><span class="sxs-lookup"><span data-stu-id="38028-184">Tablets</span></span>                 |
| <span data-ttu-id="38028-185">Täysi\*</span><span class="sxs-lookup"><span data-stu-id="38028-185">Full\*</span></span>      | <span data-ttu-id="38028-186">1 280 × 720</span><span class="sxs-lookup"><span data-stu-id="38028-186">1280 × 720</span></span> | <span data-ttu-id="38028-187">16:9</span><span class="sxs-lookup"><span data-stu-id="38028-187">16:9</span></span>         | <span data-ttu-id="38028-188">Tabletit</span><span class="sxs-lookup"><span data-stu-id="38028-188">Tablets</span></span>                 |
| <span data-ttu-id="38028-189">Täysi</span><span class="sxs-lookup"><span data-stu-id="38028-189">Full</span></span>        | <span data-ttu-id="38028-190">1 366 × 768</span><span class="sxs-lookup"><span data-stu-id="38028-190">1366 × 768</span></span> | <span data-ttu-id="38028-191">16:9</span><span class="sxs-lookup"><span data-stu-id="38028-191">16:9</span></span>         | <span data-ttu-id="38028-192">Tabletit, suuret näytöt</span><span class="sxs-lookup"><span data-stu-id="38028-192">Tablets, larger screens</span></span> |
| <span data-ttu-id="38028-193">Täysi</span><span class="sxs-lookup"><span data-stu-id="38028-193">Full</span></span>        | <span data-ttu-id="38028-194">1 440 × 960</span><span class="sxs-lookup"><span data-stu-id="38028-194">1440 × 960</span></span> | <span data-ttu-id="38028-195">3:2</span><span class="sxs-lookup"><span data-stu-id="38028-195">3:2</span></span>          | <span data-ttu-id="38028-196">Tabletit, suuret näytöt</span><span class="sxs-lookup"><span data-stu-id="38028-196">Tablets, larger screens</span></span> |

<span data-ttu-id="38028-197">\* Nämä asettelujen lisäkoot ovat käytettävissä vain Adventure Works- ja Fabrikam-asetteluissa.</span><span class="sxs-lookup"><span data-stu-id="38028-197">\* These additional layout sizes are available only in Adventure Works and Fabrikam layouts.</span></span>


>[!TIP]
> <span data-ttu-id="38028-198">Myyntipiste valitsee automaattisesti asettelujen koot sen mukaan, mikä käytettävissä oleva koko on lähimpänä nykyisen sovellusikkunan näytön resoluutiota.</span><span class="sxs-lookup"><span data-stu-id="38028-198">POS automatically selects layout sizes, based on the closest size that is available for the screen resolution of the current app window.</span></span> <span data-ttu-id="38028-199">Voit etsiä Retail Modern POS (MPOS)- tai Retail Cloud POS (CPOS) -sovelluksessa tällä hetkellä käytössä olevan näyttöasettelun tunnuksen ja näytön resoluution avaamalla **Asetukset**-sivun ja siirtymällä **Istunnon tiedot** -osaan.</span><span class="sxs-lookup"><span data-stu-id="38028-199">To find the screen layout ID and layout resolution that are currently used, in Retail Modern POS (MPOS) or Retail Cloud POS (CPOS), open the **Settings** page, and look in the **Session information** section.</span></span> <span data-ttu-id="38028-200">Voit tarkastella myös nykyisen sovelluksen tai selainkehyksen todellista ikkunan resoluutiota.</span><span class="sxs-lookup"><span data-stu-id="38028-200">You can also see the actual window resolution for your current application or browser frame.</span></span> <span data-ttu-id="38028-201">Kun nämä tiedot ovat käytettävissä, löydät Retail-sovelluksen asettelun sisällön lähteen siirtymällä kohtaan **Kanavan asetukset** > **Myyntipisteen asetukset** > **Myyntipiste** > **Näyttöasettelut**.</span><span class="sxs-lookup"><span data-stu-id="38028-201">After you have this information, you can find the source of the layout content in Retail by going to **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>


![Näyttöasettelut ja asettelun resoluutiot/koot Retail-ohjelmassa ja myyntipisteessä](../retail/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a><span data-ttu-id="38028-203">Yritykset ja tuotemerkit</span><span class="sxs-lookup"><span data-stu-id="38028-203">Companies and brands</span></span>

<span data-ttu-id="38028-204">Jokainen kuvitteellinen yritys on luotu eri vähittäismyyntisegmenttiä varten. Yritykset sisältävät tuoteluettelot, jotka on suunniteltu yrityksen markkinoita varten.</span><span class="sxs-lookup"><span data-stu-id="38028-204">Each fictitious company is targeted to a different retail segment and includes product catalogs that are tuned for the company's market.</span></span> <span data-ttu-id="38028-205">Jokaisella yrityksellä on yksilöivä visuaalinen tuotemerkki ja tuotteet.</span><span class="sxs-lookup"><span data-stu-id="38028-205">Each company has a unique visual brand that accompanies its products.</span></span> <span data-ttu-id="38028-206">Brändäyksen elementtejä ovat korostusväri, tumma tai vaalea teema ja valokuvat, jotka tarjoavat realistiset käyttökokemukset.</span><span class="sxs-lookup"><span data-stu-id="38028-206">Branding elements include the accent color, dark or light theme, and accompanying photographs that provide realistic experiences.</span></span>

### <a name="company-segment-and-visual-characteristics"></a><span data-ttu-id="38028-207">Yrityksen segmentti ja visuaaliset ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="38028-207">Company segment and visual characteristics</span></span>

| <span data-ttu-id="38028-208">Yritys </span><span class="sxs-lookup"><span data-stu-id="38028-208">Company</span></span>         | <span data-ttu-id="38028-209">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="38028-209">Location</span></span> | <span data-ttu-id="38028-210">Segmentti</span><span class="sxs-lookup"><span data-stu-id="38028-210">Segment</span></span>        | <span data-ttu-id="38028-211">Korostus</span><span class="sxs-lookup"><span data-stu-id="38028-211">Accent</span></span> | <span data-ttu-id="38028-212">Teema</span><span class="sxs-lookup"><span data-stu-id="38028-212">Theme</span></span> |
|-----------------|----------|----------------|--------|-------|
| <span data-ttu-id="38028-213">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="38028-213">Adventure Works</span></span> | <span data-ttu-id="38028-214">Seattle</span><span class="sxs-lookup"><span data-stu-id="38028-214">Seattle</span></span>  | <span data-ttu-id="38028-215">Urheilutarvikkeet</span><span class="sxs-lookup"><span data-stu-id="38028-215">Sporting Goods</span></span> | <span data-ttu-id="38028-216">Sininen</span><span class="sxs-lookup"><span data-stu-id="38028-216">Blue</span></span>   | <span data-ttu-id="38028-217">Tumma</span><span class="sxs-lookup"><span data-stu-id="38028-217">Dark</span></span>  |
| <span data-ttu-id="38028-218">Fabrikam:</span><span class="sxs-lookup"><span data-stu-id="38028-218">Fabrikam</span></span>        | <span data-ttu-id="38028-219">Houston</span><span class="sxs-lookup"><span data-stu-id="38028-219">Houston</span></span>  | <span data-ttu-id="38028-220">Muoti</span><span class="sxs-lookup"><span data-stu-id="38028-220">Fashion</span></span>        | <span data-ttu-id="38028-221">Vihreä</span><span class="sxs-lookup"><span data-stu-id="38028-221">Green</span></span>  | <span data-ttu-id="38028-222">Vaalea</span><span class="sxs-lookup"><span data-stu-id="38028-222">Light</span></span> |
| <span data-ttu-id="38028-223">Contoso</span><span class="sxs-lookup"><span data-stu-id="38028-223">Contoso</span></span>         | <span data-ttu-id="38028-224">Boston</span><span class="sxs-lookup"><span data-stu-id="38028-224">Boston</span></span>   | <span data-ttu-id="38028-225">Elektroniikka</span><span class="sxs-lookup"><span data-stu-id="38028-225">Electronics</span></span>    | <span data-ttu-id="38028-226">Punainen</span><span class="sxs-lookup"><span data-stu-id="38028-226">Red</span></span>    | <span data-ttu-id="38028-227">Tumma</span><span class="sxs-lookup"><span data-stu-id="38028-227">Dark</span></span>  |


>[!NOTE]
> <span data-ttu-id="38028-228">Adventure Works ja Fabrikam on tuotemerkkien kaksi lippulaivaa.</span><span class="sxs-lookup"><span data-stu-id="38028-228">Adventure Works and Fabrikam are the two flagship brands.</span></span> <span data-ttu-id="38028-229">Contoso on käytettävissä, mutta se ei sisällä kaikkia asetteluita.</span><span class="sxs-lookup"><span data-stu-id="38028-229">Contoso is available, but not all layouts have been provided.</span></span>


<span data-ttu-id="38028-230">Seuraavissa kuvissa ovat kolmen kuvitteellisen yrityksen aloitussivut ja tapahtumasivut.</span><span class="sxs-lookup"><span data-stu-id="38028-230">The following illustrations show examples of the welcome page and transaction page for the three fictitious companies.</span></span>

### <a name="adventure-works"></a><span data-ttu-id="38028-231">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="38028-231">Adventure Works</span></span>

![Adventure Worksin demotietojen aloitussivu.](../retail/media/demo-screen-layouts-fig-4-1a.png)

![Adventure Worksin demotietojen tapahtumasivu.](../retail/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a><span data-ttu-id="38028-234">Fabrikam:</span><span class="sxs-lookup"><span data-stu-id="38028-234">Fabrikam</span></span>

![Fabrikamin demotietojen aloitussivu.](../retail/media/demo-screen-layouts-fig-4-2a.png)

![Fabrikamin demotietojen tapahtumasivu.](../retail/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a><span data-ttu-id="38028-237">Contoso</span><span class="sxs-lookup"><span data-stu-id="38028-237">Contoso</span></span>

![Contoso demotietojen asettelut](../retail/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a><span data-ttu-id="38028-239">Käyttäjän sisäänkirjausmatriisi</span><span class="sxs-lookup"><span data-stu-id="38028-239">User sign in matrix</span></span>

<span data-ttu-id="38028-240">Käyttäjien käytettävissä on erilaisia näyttöasetteluita.</span><span class="sxs-lookup"><span data-stu-id="38028-240">Users have been provided for the various screen layouts.</span></span> <span data-ttu-id="38028-241">Näytöt voi ottaa käyttöön seuraavan taulukon avulla.</span><span class="sxs-lookup"><span data-stu-id="38028-241">By using the following table, you should be able to access any of the screens.</span></span> <span data-ttu-id="38028-242">Kirjaudu sisään soveltuvan operaattorin tunnuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="38028-242">Just sign in by using an appropriate operator ID.</span></span>

| <span data-ttu-id="38028-243">Yritys </span><span class="sxs-lookup"><span data-stu-id="38028-243">Company</span></span>         | <span data-ttu-id="38028-244">Näyttöasettelun tunnus</span><span class="sxs-lookup"><span data-stu-id="38028-244">Screen layout ID</span></span> | <span data-ttu-id="38028-245">Henkilötyyppi</span><span class="sxs-lookup"><span data-stu-id="38028-245">Persona</span></span>          | <span data-ttu-id="38028-246">Operaattorin tunnukset</span><span class="sxs-lookup"><span data-stu-id="38028-246">Operator IDs</span></span>           |
|-----------------|------------------|---------------   |------------------------|
| <span data-ttu-id="38028-247">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="38028-247">Adventure Works</span></span> | <span data-ttu-id="38028-248">A3MGR</span><span class="sxs-lookup"><span data-stu-id="38028-248">A3MGR</span></span>            | <span data-ttu-id="38028-249">Myymäläpäällikkö</span><span class="sxs-lookup"><span data-stu-id="38028-249">Store Manager</span></span>    | <span data-ttu-id="38028-250">000154, 000137, 000073</span><span class="sxs-lookup"><span data-stu-id="38028-250">000154, 000137, 000073</span></span> |
| <span data-ttu-id="38028-251">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="38028-251">Adventure Works</span></span> | <span data-ttu-id="38028-252">A3CSH</span><span class="sxs-lookup"><span data-stu-id="38028-252">A3CSH</span></span>            | <span data-ttu-id="38028-253">Kassa</span><span class="sxs-lookup"><span data-stu-id="38028-253">Cashier</span></span>          | <span data-ttu-id="38028-254">000150, 000175, 000165</span><span class="sxs-lookup"><span data-stu-id="38028-254">000150, 000175, 000165</span></span> |
| <span data-ttu-id="38028-255">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="38028-255">Adventure Works</span></span> | <span data-ttu-id="38028-256">A3STK</span><span class="sxs-lookup"><span data-stu-id="38028-256">A3STK</span></span>            | <span data-ttu-id="38028-257">Varastonhoitaja</span><span class="sxs-lookup"><span data-stu-id="38028-257">Stock Clerk</span></span>      | <span data-ttu-id="38028-258">000155, 000181, 000152</span><span class="sxs-lookup"><span data-stu-id="38028-258">000155, 000181, 000152</span></span> |
| <span data-ttu-id="38028-259">Fabrikam:</span><span class="sxs-lookup"><span data-stu-id="38028-259">Fabrikam</span></span>        | <span data-ttu-id="38028-260">F3MGR</span><span class="sxs-lookup"><span data-stu-id="38028-260">F3MGR</span></span>            | <span data-ttu-id="38028-261">Myymäläpäällikkö</span><span class="sxs-lookup"><span data-stu-id="38028-261">Store Manager</span></span>    | <span data-ttu-id="38028-262">000160, 000168, 000163</span><span class="sxs-lookup"><span data-stu-id="38028-262">000160, 000168, 000163</span></span> |
| <span data-ttu-id="38028-263">Fabrikam:</span><span class="sxs-lookup"><span data-stu-id="38028-263">Fabrikam</span></span>        | <span data-ttu-id="38028-264">F3CSH</span><span class="sxs-lookup"><span data-stu-id="38028-264">F3CSH</span></span>            | <span data-ttu-id="38028-265">Kassa</span><span class="sxs-lookup"><span data-stu-id="38028-265">Cashier</span></span>          | <span data-ttu-id="38028-266">000161, 000113, 000114</span><span class="sxs-lookup"><span data-stu-id="38028-266">000161, 000113, 000114</span></span> |
| <span data-ttu-id="38028-267">Fabrikam:</span><span class="sxs-lookup"><span data-stu-id="38028-267">Fabrikam</span></span>        | <span data-ttu-id="38028-268">F3STK</span><span class="sxs-lookup"><span data-stu-id="38028-268">F3STK</span></span>            | <span data-ttu-id="38028-269">Varastonhoitaja</span><span class="sxs-lookup"><span data-stu-id="38028-269">Stock Clerk</span></span>      | <span data-ttu-id="38028-270">000164, 000112, 000123</span><span class="sxs-lookup"><span data-stu-id="38028-270">000164, 000112, 000123</span></span> |
| <span data-ttu-id="38028-271">Contoso</span><span class="sxs-lookup"><span data-stu-id="38028-271">Contoso</span></span>         | <span data-ttu-id="38028-272">C3MGR</span><span class="sxs-lookup"><span data-stu-id="38028-272">C3MGR</span></span>            | <span data-ttu-id="38028-273">Myymäläpäällikkö</span><span class="sxs-lookup"><span data-stu-id="38028-273">Store Manager</span></span>    | <span data-ttu-id="38028-274">000100, 000111</span><span class="sxs-lookup"><span data-stu-id="38028-274">000100, 000111</span></span>         |
| <span data-ttu-id="38028-275">Contoso</span><span class="sxs-lookup"><span data-stu-id="38028-275">Contoso</span></span>         | <span data-ttu-id="38028-276">C3CSH</span><span class="sxs-lookup"><span data-stu-id="38028-276">C3CSH</span></span>            | <span data-ttu-id="38028-277">Kassa</span><span class="sxs-lookup"><span data-stu-id="38028-277">Cashier</span></span>          | <span data-ttu-id="38028-278">000110, 000120</span><span class="sxs-lookup"><span data-stu-id="38028-278">000110, 000120</span></span>         |
| <span data-ttu-id="38028-279">Contoso</span><span class="sxs-lookup"><span data-stu-id="38028-279">Contoso</span></span>         | <span data-ttu-id="38028-280">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="38028-280">Not applicable</span></span>   | <span data-ttu-id="38028-281">Varastonhoitaja</span><span class="sxs-lookup"><span data-stu-id="38028-281">Stock Clerk</span></span>      | <span data-ttu-id="38028-282">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="38028-282">Not applicable</span></span>         |


>[!TIP]
> <span data-ttu-id="38028-283">Saat parhaat tulokset, kun aktivoit vastaavan myymäläsijainnin kassakoneen ja määrität yritykseksi sen henkilötyypin yrityksen, jonka haluat kirjautuvan sisään.</span><span class="sxs-lookup"><span data-stu-id="38028-283">For best results, activate a register in the corresponding store location, and set the company to the company of the persona that you plan to use when you sign in.</span></span> <span data-ttu-id="38028-284">Näin voit varmistaa, että visuaalinen profiili ja brändäyskuvat ovat kaikkialla samanlaiset.</span><span class="sxs-lookup"><span data-stu-id="38028-284">In this way, you help guarantee that the visual profile and branding images are aligned across the experience.</span></span> <span data-ttu-id="38028-285">Jos esimerkiksi haluat nähdä Fabrikamin kassanhoitajan asettelun, aktivoi Houstonin alueen kassakone.</span><span class="sxs-lookup"><span data-stu-id="38028-285">For example, if you're interested in seeing a Fabrikam layout for a cashier, you should activate a register in the Houston store.</span></span>


<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail > Channel setup > POS setup > POS > Images**. -->

<!-- ![Images in Dynamics 365 for Retail](../retail/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../retail/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->

