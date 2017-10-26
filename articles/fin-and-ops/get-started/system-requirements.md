---
title: "Pilvikäyttöönottojen järjestelmävaatimukset"
description: "Tässä ohjeaiheessa on luettelo Microsoft Dynamics 365 for Finance and Operations Enterprise editionin nykyisen version järjestelmävaatimuksista pilvikäyttöönotoissa."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: 7fe11966b27eb0793a47835e05e465d809bf3407
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="82c46-103">Pilvikäyttöönottojen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="82c46-103">System requirements for cloud deployments</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="82c46-104">Tässä ohjeaiheessa on luettelo Microsoft Dynamics 365 for Finance and Operations Enterprise editionin nykyisen version järjestelmävaatimuksista pilvikäyttöönotoissa.</span><span class="sxs-lookup"><span data-stu-id="82c46-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for cloud deployments.</span></span> <span data-ttu-id="82c46-105">Tarkista tarvittaessa tämä vaihe ennen Finance and Operationsin asennusta, että käyttämäsi järjestelmän verkkoa, laitteistoa ja ohjelmistoa koskevat vähimmäisvaatimukset täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="82c46-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="82c46-106">Tuetut selaimet</span><span class="sxs-lookup"><span data-stu-id="82c46-106">Supported web browsers</span></span>
<span data-ttu-id="82c46-107">Verkkosovellus voidaan suorittaa seuraavissa selaimissa, joita käytetään määritetyissä käyttöjärjestelmissä:</span><span class="sxs-lookup"><span data-stu-id="82c46-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="82c46-108">Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä</span><span class="sxs-lookup"><span data-stu-id="82c46-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="82c46-109">Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä</span><span class="sxs-lookup"><span data-stu-id="82c46-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="82c46-110">Google Chrome (uusin saatavana oleva versio) Windows 10-, Windows 8.1-, Windows 8-, Windows 7- tai Google Nexus 10 -taulutietokoneen käyttöjärjestelmässä</span><span class="sxs-lookup"><span data-stu-id="82c46-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
-   <span data-ttu-id="82c46-111">Apple Safari (uusin saatavana oleva versio) Mac OS X 10.10 (Yosemite)-, 10.11 (El Capitan)-, 10.12 (Sierra)- tai Apple iPadin käyttöjärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="82c46-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="82c46-112">Ohjelmistovalmistajien sivustot sisältävät tietoja kunkin selaimen uusimmasta versiosta.</span><span class="sxs-lookup"><span data-stu-id="82c46-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> -   <span data-ttu-id="82c46-113">Chrome-laajennuksen ennakkojulkaisuversio on asennettava, jotta voit tallentaa tehtävien tallennustoiminnon luomat kuvat ja sisällyttää ne Word-asiakirjoihin.</span><span class="sxs-lookup"><span data-stu-id="82c46-113">You must install a pre-release Chrome extension to enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   <span data-ttu-id="82c46-114">Työnkulkueditori käynnistetään ClickOnce-sovelluksena.</span><span class="sxs-lookup"><span data-stu-id="82c46-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="82c46-115">Ainoastaan Microsoft Edge ja Internet Explorer (tuetussa Microsoft Windows -versiossa) tukevat ClickOnce-sovelluksia.</span><span class="sxs-lookup"><span data-stu-id="82c46-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="82c46-116">Työnkulkueditorin ClickOnce-sovellus edellyttää 64-bittisen käyttöjärjestelmää.</span><span class="sxs-lookup"><span data-stu-id="82c46-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> -   <span data-ttu-id="82c46-117">Taloushallinnon raportoinnin raportin suunnittelusovellus käynnistetään ClickOnce-sovelluksena.</span><span class="sxs-lookup"><span data-stu-id="82c46-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="82c46-118">Se edellyttää 64-bittisen käyttöjärjestelmän kanssa yhteensopivaa järjestelmää.</span><span class="sxs-lookup"><span data-stu-id="82c46-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="82c46-119">Jos käytössäsi on Chrome, sinun on asennettava ClickOnce-laajennus ladataksesi Report Designer -asiakasohjelman.</span><span class="sxs-lookup"><span data-stu-id="82c46-119">If you’re using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="82c46-120">Jos käytät Chromea Incognito-tilassa, varmista, että ClickOnce-laajennus on käytössä Incognito-tilassa.</span><span class="sxs-lookup"><span data-stu-id="82c46-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> -   <span data-ttu-id="82c46-121">PDF-tiedostojen esikatseluun suosittelemme modernia verkkoselainta, kuten Microsoft Edgeä (uusin julkinen versio) Windows 10 -käyttöjärjestelmässä tai Google Chromea (uusin julkinen versio) Windows 10-, Windows 8.1-, Windows 8- tai Windows 7 -käyttöjärjestelmässä tai Google Nexus 10 -tabletissa.</span><span class="sxs-lookup"><span data-stu-id="82c46-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="82c46-122">Retail Cloud POS -sovelluksen tuetut selaimet</span><span class="sxs-lookup"><span data-stu-id="82c46-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="82c46-123">Vähittäismyynnin pilvimyyntipiste voidaan suorittaa seuraavissa selaimissa, joita käytetään määritetyissä käyttöjärjestelmissä:</span><span class="sxs-lookup"><span data-stu-id="82c46-123">Retail Cloud POS can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="82c46-124">Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä</span><span class="sxs-lookup"><span data-stu-id="82c46-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="82c46-125">Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä</span><span class="sxs-lookup"><span data-stu-id="82c46-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="82c46-126">Chrome (uusin julkaistu versio) Windows 10, Windows 8.1 tai Windows 7 -käyttöjärjestelmässä</span><span class="sxs-lookup"><span data-stu-id="82c46-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="82c46-127">Verkon vaatimukset</span><span class="sxs-lookup"><span data-stu-id="82c46-127">Network requirements</span></span>
-   <span data-ttu-id="82c46-128">Finance and Operations on suunniteltu verkkoihin, joiden viive on enintään 250–300 millisekuntia (ms).</span><span class="sxs-lookup"><span data-stu-id="82c46-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="82c46-129">Tämä viive on selainasiakasohjelman ja sen Microsoft Azure -palvelinkeskuksen välinen viive, joka isännöi Finance and Operationsia.</span><span class="sxs-lookup"><span data-stu-id="82c46-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="82c46-130">On suositeltavaa testata verkon viive osoitteessa <http://www.azurespeed.com>.</span><span class="sxs-lookup"><span data-stu-id="82c46-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
-   <span data-ttu-id="82c46-131">Finance and Operationsin kaistanleveysvaatimus määräytyy tilanteen mukaan.</span><span class="sxs-lookup"><span data-stu-id="82c46-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="82c46-132">Yleisimmät tilanteet vaativat yli 50 kilotavua sekunnissa (KBps) kaistanleveyttä.</span><span class="sxs-lookup"><span data-stu-id="82c46-132">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="82c46-133">Suosittelemme kuitenkin suurempaa kaistanleveyttä tilanteissa, joissa hyötykuorman vaatimus on korkea, kuten työtiloissa, tai tilanteissa, joissa vaaditaan laajaa mukauttamista.</span><span class="sxs-lookup"><span data-stu-id="82c46-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="82c46-134">Finance and Operations on yleisesti optimoitu internet-käyttöön.</span><span class="sxs-lookup"><span data-stu-id="82c46-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="82c46-135">Kyselyiden määrä selainasiakasohjelmasta Azure-palvelinkeskukseen on hyvin pieni, ja koko paketti on pakattu.</span><span class="sxs-lookup"><span data-stu-id="82c46-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span> 

> [!WARNING]
> <span data-ttu-id="82c46-136">Älä laske kaistanleveysvaatimuksia asiakkaan sijainnista kertomalla käyttäjien määrä kaistanleveyden vähimmäisvaatimuksella.</span><span class="sxs-lookup"><span data-stu-id="82c46-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="82c46-137">Tietyn sijainnin samanaikainen käyttö on hyvin vaikea laskea.</span><span class="sxs-lookup"><span data-stu-id="82c46-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="82c46-138">Asiakkaat, jotka ovat huolissaan kaistanleveyden vaatimuksista, voivat käyttää Finance and Operationsin ennakkoversiota.</span><span class="sxs-lookup"><span data-stu-id="82c46-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="82c46-139">.NET Framework -vaatimukset</span><span class="sxs-lookup"><span data-stu-id="82c46-139">.NET Framework requirements</span></span>
<span data-ttu-id="82c46-140">Finance and Operations edellyttää Microsoft .NET Framework 4.6.2 -versiota kaikissa ClickOnce-sovelluksissa, kuten asiakirjan reititysagentissa.</span><span class="sxs-lookup"><span data-stu-id="82c46-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="82c46-141">Asennusohjeet löydät kohdasta [.NET Frameworkin asentaminen](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="82c46-141">For installation instructions, see [Installing the .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="82c46-142">Tuetut Microsoft Office -sovellukset</span><span class="sxs-lookup"><span data-stu-id="82c46-142">Supported Microsoft Office applications</span></span>
<span data-ttu-id="82c46-143">Seuraavia Microsoft Office -sovelluksia tuetaan Finance and Operationsin pilvikäyttöönotoissa ja paikallisissa käyttöönotoissa:</span><span class="sxs-lookup"><span data-stu-id="82c46-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>

-   <span data-ttu-id="82c46-144">Microsoft Office 2016:n Windows- tai Mac-version on oltava asennettuna, jotta Microsoft Excel ja Word-lisäosia voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="82c46-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="82c46-145">Lisätietoja versiovaatimuksista on ohjeaiheessa [Office-integroinnin vianmääritys](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="82c46-145">For more information about version requirements, see [Office integration troubleshooting](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
-   <span data-ttu-id="82c46-146">Microsoft Office 2007 tai sitä uudempi on oltava asennettuna, jotta voit tarkastella Vie Exceliin tai Vie Wordiin -toimintojen luomia asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="82c46-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-requirements"></a><span data-ttu-id="82c46-147">Retail Modern POS -vaatimukset</span><span class="sxs-lookup"><span data-stu-id="82c46-147">Retail Modern POS requirements</span></span>

> [!NOTE]
> <span data-ttu-id="82c46-148">Jos Retail Modern POS käyttää offline-tietokantaa, tietokoneen on vastattava kaikkia Microsoft SQL Serverin järjestelmävaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="82c46-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="82c46-149">Retail Modern POS -offline-tietokantaa voi käyttää Microsoft SQL Server 2012 Service Pack 3:ssa tai uudemmassa, Microsoft SQL Server 2014 Service Pack 2:ssa tai uudemmassa ja Microsoft SQL Server 2016:ssa.</span><span class="sxs-lookup"><span data-stu-id="82c46-149">A Retail Modern POS offline database will work on Microsoft SQL Server 2012 with Service Pack 3 or later, Microsoft SQL Server 2014 with Service Pack 2 or later, and Microsoft SQL Server 2016.</span></span> <span data-ttu-id="82c46-150">Aina kannattaa käyttää uusinta käytettävissä olevaa versiota ja asentaa uusimmat Service Packit.</span><span class="sxs-lookup"><span data-stu-id="82c46-150">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="82c46-151">Tuetut käyttöjärjestelmät</span><span class="sxs-lookup"><span data-stu-id="82c46-151">Supported operating systems</span></span>

-   <span data-ttu-id="82c46-152">Retail Modern POS on 32-bittinen sovellus, mutta sen voi suorittaa sekä x86- että x64-arkkitehtuureilla.</span><span class="sxs-lookup"><span data-stu-id="82c46-152">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="82c46-153">Retail Modern POS on tuettu vain Windows 10 Pro, Enterprise ja Enterprise LTSB -versioissa.</span><span class="sxs-lookup"><span data-stu-id="82c46-153">Retail Modern POS is supported only on Windows 10 Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB) editions.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="82c46-154">Järjestelmän vähimmäisvaatimukset</span><span class="sxs-lookup"><span data-stu-id="82c46-154">Minimum system requirements</span></span>

-   <span data-ttu-id="82c46-155">Pienin tuettu näyttötarkkuus on 1280 × 1024.</span><span class="sxs-lookup"><span data-stu-id="82c46-155">The minimum supported resolution is 1,280 × 1,024.</span></span>
-   <span data-ttu-id="82c46-156">Tietokoneen, jolla Retail Modern POS -sovellusta käytetään on vastattava seuraavia vaatimuksia:</span><span class="sxs-lookup"><span data-stu-id="82c46-156">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    -   <span data-ttu-id="82c46-157">Siinä on oltava vähintään kaksiytiminen suoritin, jonka nopeus on vähintään 2 gigahertsiä (GHz).</span><span class="sxs-lookup"><span data-stu-id="82c46-157">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    -   <span data-ttu-id="82c46-158">Siinä on oltava vähintään 3 gigatavua (Gt) keskusmuistia.</span><span class="sxs-lookup"><span data-stu-id="82c46-158">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>
    -   <span data-ttu-id="82c46-159">Siinä on oltava internet-yhteys.</span><span class="sxs-lookup"><span data-stu-id="82c46-159">It must have internet access.</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="82c46-160">Retail hardware station -vaatimukset</span><span class="sxs-lookup"><span data-stu-id="82c46-160">Retail hardware station requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="82c46-161">Tuetut käyttöjärjestelmät</span><span class="sxs-lookup"><span data-stu-id="82c46-161">Supported operating systems</span></span>

-   <span data-ttu-id="82c46-162">Retail hardware station on 32-bittinen sovellus, mutta sen voi suorittaa sekä x86- että x64-arkkitehtuureilla.</span><span class="sxs-lookup"><span data-stu-id="82c46-162">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="82c46-163">Retail hardware station on tuettu seuraavissa käyttöjärjestelmissä:</span><span class="sxs-lookup"><span data-stu-id="82c46-163">Retail hardware station is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="82c46-164">Windows 7 Professional, Enterprise ja Ultimate</span><span class="sxs-lookup"><span data-stu-id="82c46-164">Windows 7 Professional, Enterprise, and Ultimate editions</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="82c46-165">Windows 7:ää tuetaan vain, jos Internet Explorer 11 asennetaan manuaalisesti järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="82c46-165">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    -   <span data-ttu-id="82c46-166">Windows 8.1 Update 1 Professional, Enterprise ja Embedded</span><span class="sxs-lookup"><span data-stu-id="82c46-166">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="82c46-167">Windows 10 Pro, Enterprise ja Enterprise LTSB</span><span class="sxs-lookup"><span data-stu-id="82c46-167">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="82c46-168">Järjestelmän vähimmäisvaatimukset</span><span class="sxs-lookup"><span data-stu-id="82c46-168">Minimum system requirements</span></span>

<span data-ttu-id="82c46-169">Tietokoneen on täytettävä kaikki järjestelmän vähimmäisvaatimukset, jotta seuraavien kohteiden asennus ja käyttö on mahdollista:</span><span class="sxs-lookup"><span data-stu-id="82c46-169">The computer must meet all system requirements for installing and using the following items:</span></span>

-   <span data-ttu-id="82c46-170">IIS (Internet Information Services)</span><span class="sxs-lookup"><span data-stu-id="82c46-170">Internet Information Services (IIS)</span></span>
-   <span data-ttu-id="82c46-171">Kolmannen osapuolen laitteisto</span><span class="sxs-lookup"><span data-stu-id="82c46-171">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="82c46-172">Vähittäismyymälän vähittäismyyntilaitteen vaatimukset</span><span class="sxs-lookup"><span data-stu-id="82c46-172">Retail Store Scale Unit requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="82c46-173">Tuetut käyttöjärjestelmät</span><span class="sxs-lookup"><span data-stu-id="82c46-173">Supported operating systems</span></span>

-   <span data-ttu-id="82c46-174">Vähittäismyymälän vähittäismyyntilaite on 32-bittinen sovellus, mutta sen voi suorittaa sekä x86- että x64-arkkitehtuureilla.</span><span class="sxs-lookup"><span data-stu-id="82c46-174">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="82c46-175">Vähittäismyymälän vähittäismyyntilaite on tuettu seuraavissa käyttöjärjestelmissä:</span><span class="sxs-lookup"><span data-stu-id="82c46-175">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="82c46-176">Windows 7 Professional, Enterprise ja Ultimate</span><span class="sxs-lookup"><span data-stu-id="82c46-176">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="82c46-177">Windows 8.1 Update 1 Professional, Enterprise ja Embedded</span><span class="sxs-lookup"><span data-stu-id="82c46-177">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="82c46-178">Windows 10 Pro, Enterprise ja Enterprise LTSB</span><span class="sxs-lookup"><span data-stu-id="82c46-178">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="82c46-179">Järjestelmän vähimmäisvaatimukset</span><span class="sxs-lookup"><span data-stu-id="82c46-179">Minimum system requirements</span></span>

-   <span data-ttu-id="82c46-180">4 Gt RAM-muistia</span><span class="sxs-lookup"><span data-stu-id="82c46-180">4 GB of RAM</span></span>
-   <span data-ttu-id="82c46-181">1,6 GHz korkein ytimen suoritinnopeus (vähintään kaksi ydintä)</span><span class="sxs-lookup"><span data-stu-id="82c46-181">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="82c46-182">Vähintään 10 gigatavua vapaata tallennustilaa (kanavatietokanta voi vaatia paljon tallennustilaa)</span><span class="sxs-lookup"><span data-stu-id="82c46-182">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="82c46-183">Suositeltavat järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="82c46-183">Recommended system requirements</span></span>

-   <span data-ttu-id="82c46-184">6 Gt RAM-muistia</span><span class="sxs-lookup"><span data-stu-id="82c46-184">6 GB of RAM</span></span>
-   <span data-ttu-id="82c46-185">2,4 GHz i7 (tai vastaava) ydinkohtainen suoritinnopeus (suositus on neljä ydintä)</span><span class="sxs-lookup"><span data-stu-id="82c46-185">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
-   <span data-ttu-id="82c46-186">Vähintään 10 gigatavua vapaata tallennustilaa (kanavatietokanta voi vaatia paljon tallennustilaa)</span><span class="sxs-lookup"><span data-stu-id="82c46-186">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="82c46-187">Connectorin vaatimukset</span><span class="sxs-lookup"><span data-stu-id="82c46-187">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="82c46-188">Tuetut käyttöjärjestelmät</span><span class="sxs-lookup"><span data-stu-id="82c46-188">Supported operating systems</span></span>

-   <span data-ttu-id="82c46-189">Connector for Microsoft Dynamics AX:ssä on kaksi erillistä asennusohjelmaa – toinen Async Server Connector -palvelua ja toinen Real-time Service for Dynamics AX 2012 R3 -palvelua varten.</span><span class="sxs-lookup"><span data-stu-id="82c46-189">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Dynamics AX 2012 R3.</span></span>
-   <span data-ttu-id="82c46-190">Molemmat komponentit ovat 32-bittinen sovelluksia, mutta ne voi suorittaa sekä x86- että x64-arkkitehtuureilla.</span><span class="sxs-lookup"><span data-stu-id="82c46-190">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="82c46-191">Seuraavat käyttöjärjestelmät tukevat molempia komponentteja:</span><span class="sxs-lookup"><span data-stu-id="82c46-191">Both components are supported on the following operating systems:</span></span>

    -   <span data-ttu-id="82c46-192">Windows 7 Professional, Enterprise ja Ultimate</span><span class="sxs-lookup"><span data-stu-id="82c46-192">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="82c46-193">Windows 8.1 Update 1 Professional, Enterprise ja Embedded</span><span class="sxs-lookup"><span data-stu-id="82c46-193">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="82c46-194">Windows 10 Pro, Enterprise ja Enterprise LTSB</span><span class="sxs-lookup"><span data-stu-id="82c46-194">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>
    -   <span data-ttu-id="82c46-195">Microsoft Windows Server 2012 R2 ja Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="82c46-195">Microsoft Windows Server 2012 R2 and Microsoft Windows Server 2016</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="82c46-196">Järjestelmän vähimmäisvaatimukset</span><span class="sxs-lookup"><span data-stu-id="82c46-196">Minimum system requirements</span></span>
-   <span data-ttu-id="82c46-197">2 Gt RAM-muistia (suositus:, 4 Gt RAM-muistia)</span><span class="sxs-lookup"><span data-stu-id="82c46-197">2 GB of RAM (4 GB of RAM are recommended.)</span></span>
-   <span data-ttu-id="82c46-198">1,6 GHz korkein ytimen suoritinnopeus (vähintään kaksi ydintä)</span><span class="sxs-lookup"><span data-stu-id="82c46-198">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="82c46-199">Vähintään 10 gigatavua vapaata tallennustilaa (kanavatietokanta voi vaatia paljon tallennustilaa)</span><span class="sxs-lookup"><span data-stu-id="82c46-199">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="82c46-200">Vaatimukset paikalliseen kehitykseen virtuaalikoneessa</span><span class="sxs-lookup"><span data-stu-id="82c46-200">Requirements for development on local VMs</span></span>
<span data-ttu-id="82c46-201">Lisätietoja paikallisesta virtuaalikoneessa (VMs) kehittämistä koskevista vaatimuksista on kohdassa [Paikalliset virtuaalikoneet](../../dev-itpro/dev-tools/access-instances.md).</span><span class="sxs-lookup"><span data-stu-id="82c46-201">For information about the requirements for development on local virtual machines (VMs), see [VM running on-premises](../../dev-itpro/dev-tools/access-instances.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="82c46-202">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="82c46-202">See also</span></span>

[<span data-ttu-id="82c46-203">Dynamics 365 for Finance and Operations, Enterprise Editionin kokeiluversion hankkiminen</span><span class="sxs-lookup"><span data-stu-id="82c46-203">Get an evaluation copy of Dynamics 365 for Finance and Operations, Enterprise edition</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)

