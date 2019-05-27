---
title: Talentin järjestelmävaatimukset ja päivityskäytäntö
description: Tässä ohjeaiheessa kerrotaan Dynamics 365 for Talentin järjestelmävaatimuksista. Lisäksi siinä käsitellään päivityskäytäntö.
author: andreabichsel
manager: AnnBe
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ea8b7485b142245a359648a2a85d2a3e2a6d6629
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517909"
---
# <a name="talent-system-requirements-and-update-policy"></a><span data-ttu-id="5260d-104">Talentin järjestelmävaatimukset ja päivityskäytäntö</span><span class="sxs-lookup"><span data-stu-id="5260d-104">Talent system requirements and update policy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5260d-105">Tässä ohjeaiheessa kuvataan Microsoft Dynamics 365 for Talent -vaatimukset, kuten Attract, Onboard ja Core HR.</span><span class="sxs-lookup"><span data-stu-id="5260d-105">This topic describes requirements for Microsoft Dynamics 365 for Talent, including Attract, Onboard, and Core HR.</span></span> <span data-ttu-id="5260d-106">Siinä esitellään myös Talentin käytettävissä olevat maat ja alueet sekä tiedot kielistä ja lokalisoinnissa Talentia koskevia tietoja varten.</span><span class="sxs-lookup"><span data-stu-id="5260d-106">It also outlines the countries and regions where Talent is available, plus information about languages and localization for Talent data.</span></span> <span data-ttu-id="5260d-107">Lisäyksissä tämä ohjeaihe sisältää Talentin päivityskäytännön.</span><span class="sxs-lookup"><span data-stu-id="5260d-107">In additions, this topic provides the update policy for Talent.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="5260d-108">Tuetut selaimet</span><span class="sxs-lookup"><span data-stu-id="5260d-108">Supported web browsers</span></span>

<span data-ttu-id="5260d-109">Microsoft Dynamics 365 for Talent in verkkosovellus voidaan suorittaa seuraavissa selaimissa, joita käytetään määritetyissä käyttöjärjestelmissä:</span><span class="sxs-lookup"><span data-stu-id="5260d-109">The Microsoft Dynamics 365 for Talent web application can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="5260d-110">Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä</span><span class="sxs-lookup"><span data-stu-id="5260d-110">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="5260d-111">Internet Explorer 11 Windows 10-, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä</span><span class="sxs-lookup"><span data-stu-id="5260d-111">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="5260d-112">Google Chrome (uusin saatavana oleva versio)</span><span class="sxs-lookup"><span data-stu-id="5260d-112">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="5260d-113">Apple Safari (uusin saatavana oleva versio)</span><span class="sxs-lookup"><span data-stu-id="5260d-113">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="5260d-114">Ohjelmistovalmistajien sivustot sisältävät tietoja kunkin selaimen uusimmasta versiosta.</span><span class="sxs-lookup"><span data-stu-id="5260d-114">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="5260d-115">Voit tallentaa tehtävän tallennustoiminnon luomat kuvat ja sisällyttää ne Microsoft Word -asiakirjoihin, jos asennettuna on Chrome-laajennus.</span><span class="sxs-lookup"><span data-stu-id="5260d-115">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="5260d-116">Työnkulkueditori käynnistetään ClickOnce-sovelluksena.</span><span class="sxs-lookup"><span data-stu-id="5260d-116">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="5260d-117">Vain Microsoft Edge ja Internet Explorer (tuetuissa Microsoft Windows -versioissa) tukevat ClickOnce-sovelluksia.</span><span class="sxs-lookup"><span data-stu-id="5260d-117">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="5260d-118">Työnkulkueditorin ClickOnce-sovellus vaatii 64-bittisen käyttöjärjestelmän.</span><span class="sxs-lookup"><span data-stu-id="5260d-118">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="5260d-119">PDF-tiedostojen esikatseluun suosittelemme modernia verkkoselainta, kuten Microsoft Edgeä (uusin julkinen versio) Windows 10 -käyttöjärjestelmässä tai Google Chromea (uusin julkinen versio) Windows 10-, Windows 8.1-, Windows 8- tai Windows 7 -käyttöjärjestelmässä tai Google Nexus 10 -tabletissa.</span><span class="sxs-lookup"><span data-stu-id="5260d-119">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="5260d-120">Verkon vaatimukset</span><span class="sxs-lookup"><span data-stu-id="5260d-120">Network requirements</span></span>
> * <span data-ttu-id="5260d-121">Dynamics 365 for Talent on suunniteltu verkkoihin, joiden viive on enintään 250–300 millisekuntia (ms).</span><span class="sxs-lookup"><span data-stu-id="5260d-121">Dynamics 365 for Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="5260d-122">Tämä viive on selaimen asiakasohjelman ja Dynamics 365 for Talentia isännöivän Microsoft Azure -palvelinkeskuksen välillä.</span><span class="sxs-lookup"><span data-stu-id="5260d-122">This is the latency from a browser client to the Microsoft Azure data center that hosts Dynamics 365 for Talent.</span></span> <span data-ttu-id="5260d-123">On suositeltavaa testata verkon viive osoitteessa [www.azurespeed.com](https://www.azurespeed.com "Azuren viivetesti").</span><span class="sxs-lookup"><span data-stu-id="5260d-123">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="5260d-124">Dynamics 365 for Talentin kaistanleveyden vaatimukset riippuvat skenaariostasi.</span><span class="sxs-lookup"><span data-stu-id="5260d-124">Bandwidth requirements for Dynamics 365 for Talent depend on your scenario.</span></span> <span data-ttu-id="5260d-125">Yleisimmät tilanteet vaativat yli 50 kilotavua sekunnissa (KBps) kaistanleveyttä.</span><span class="sxs-lookup"><span data-stu-id="5260d-125">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="5260d-126">Älä laske kaistanleveysvaatimuksia asiakkaan sijainnista kertomalla käyttäjien määrä kaistanleveyden vähimmäisvaatimuksella.</span><span class="sxs-lookup"><span data-stu-id="5260d-126">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="5260d-127">Tietyn sijainnin samanaikainen käyttö on hyvin vaikea laskea.</span><span class="sxs-lookup"><span data-stu-id="5260d-127">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="5260d-128">Asiakkaat, jotka ovat huolissaan kaistanleveyden vaatimuksista voivat käyttää Dynamics 365 for Talentin kokeiluversiota.</span><span class="sxs-lookup"><span data-stu-id="5260d-128">For customers who are concerned about bandwidth requirements, use a trial version of Dynamics 365 for Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="5260d-129">Tuetut Microsoft Office -sovellukset</span><span class="sxs-lookup"><span data-stu-id="5260d-129">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="5260d-130">Microsoft Office 2016:n Windows- tai Mac-version on oltava asennettuna, jotta Microsoft Excel- ja Word-lisäosia voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="5260d-130">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="5260d-131">Lisätietoja versiovaatimuksista on kohdassa [Office-integroinnin vianmääritys](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office-integroinnin vianmääritys").</span><span class="sxs-lookup"><span data-stu-id="5260d-131">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="5260d-132">Microsoft Office 2007 tai sitä uudempi on oltava asennettuna, jotta voit tarkastella Vie Exceliin- tai Vie Wordiin -toimintojen luomia asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="5260d-132">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="5260d-133">Alueellinen käytettävyys, kielet ja lokalisointi</span><span class="sxs-lookup"><span data-stu-id="5260d-133">Regional availability, languages, and localization</span></span>

<span data-ttu-id="5260d-134">Voit ladata PDF-tiedoston maista, alueista ja kielistä, joita Talent tukee kohdasta [Microsoft Dynamics 365:n kansainvälinen saatavuus](https://docs.microsoft.com/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="5260d-134">You can download a PDF file of the countries, regions, and languages Talent supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="5260d-135">Kun käyttöliittymä on lokalisoitu muille kielille, kaikki käyttäjätiedot tallennetaan kielellä, jolla ne on kirjoitettu.</span><span class="sxs-lookup"><span data-stu-id="5260d-135">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="5260d-136">Voit luoda sähköposteja ja malleja muilla kielillä, mutta tiedot, kuten aikataulun tiedot, ovat tällä hetkellä käytettävissä vain englanniksi.</span><span class="sxs-lookup"><span data-stu-id="5260d-136">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="5260d-137">Jos olet kehittäjä, joka on kiinnostunut maa- tai aluekohtaisten mukautusten luonnista, tai kun luot ratkaisun maalle tai alueelle, jota Microsoft ei tällä hetkellä tue, Katso lisätietoja kohdasta [Globalisaatio](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="5260d-137">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

## <a name="update-policy"></a><span data-ttu-id="5260d-138">Päivityskäytäntö</span><span class="sxs-lookup"><span data-stu-id="5260d-138">Update policy</span></span>

<span data-ttu-id="5260d-139">Microsoft Dynamics 365 for Talent on pilvipalvelu.</span><span class="sxs-lookup"><span data-stu-id="5260d-139">Microsoft Dynamics 365 for Talent is serviced as a cloud offering.</span></span> <span data-ttu-id="5260d-140">Dynamics 365 for Talentin päivitykset ovat jatkuvia ja Microsoft ottaa ne käyttöön automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="5260d-140">Updates to Dynamics 365 for Talent are continuous and applied automatically by Microsoft.</span></span>

<span data-ttu-id="5260d-141">Päivitykset julkaistaan säännöllisesti, ja ne tehdään kaikkiin ympäristöihin.</span><span class="sxs-lookup"><span data-stu-id="5260d-141">Updates are released on a regular cadence and will be made to all environments.</span></span> <span data-ttu-id="5260d-142">Dynamics 365 for Talentia tuetaan [Microsoft-tuen elinkaarikäytännön](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft-tuen elinkaari") mukaisesti, joka ilmaisee yhdenmukaisen ja ennakoitavan ohjeistuksen tuotetuen saatavuudesta.</span><span class="sxs-lookup"><span data-stu-id="5260d-142">Dynamics 365 for Talent is supported according to the [Microsoft Support Lifecycle policy](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), which provides consistent and predictable guidelines for product support availability.</span></span>
