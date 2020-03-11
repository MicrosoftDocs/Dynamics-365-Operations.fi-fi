---
title: Järjestelmävaatimukset
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72379e91ace61f5e33ac6cab259b5c32902c7b3b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008832"
---
# <a name="system-requirements"></a><span data-ttu-id="88d8d-102">Järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="88d8d-102">System requirements</span></span>

<span data-ttu-id="88d8d-103">Tässä artikkelissa kuvataan Microsoft Dynamics 365 Human Resourcesin vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="88d8d-103">This article describes requirements for Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="88d8d-104">Siinä esitellään myös maat ja alueet, joissa Human Resources on käytettävissä sekä Human Resources -tietojen kielistä ja lokalisoinnista.</span><span class="sxs-lookup"><span data-stu-id="88d8d-104">It also outlines the countries and regions where Human Resources is available, and information about languages and localization for Human Resources data.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="88d8d-105">Tuetut selaimet</span><span class="sxs-lookup"><span data-stu-id="88d8d-105">Supported web browsers</span></span>

<span data-ttu-id="88d8d-106">Human Resources toimii kaikilla seuraavilla verkkoselaimilla, joita käytetään määritetyissä käyttöjärjestelmissä:</span><span class="sxs-lookup"><span data-stu-id="88d8d-106">Human Resources can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="88d8d-107">Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä</span><span class="sxs-lookup"><span data-stu-id="88d8d-107">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="88d8d-108">Internet Explorer 11 Windows 10-, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä</span><span class="sxs-lookup"><span data-stu-id="88d8d-108">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="88d8d-109">Google Chrome (uusin saatavana oleva versio)</span><span class="sxs-lookup"><span data-stu-id="88d8d-109">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="88d8d-110">Apple Safari (uusin saatavana oleva versio)</span><span class="sxs-lookup"><span data-stu-id="88d8d-110">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="88d8d-111">Ohjelmistovalmistajien sivustot sisältävät tietoja kunkin selaimen uusimmasta versiosta.</span><span class="sxs-lookup"><span data-stu-id="88d8d-111">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="88d8d-112">Voit tallentaa tehtävän tallennustoiminnon luomat kuvat ja sisällyttää ne Microsoft Word -asiakirjoihin, jos asennettuna on Chrome-laajennus.</span><span class="sxs-lookup"><span data-stu-id="88d8d-112">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="88d8d-113">Työnkulkueditori käynnistetään ClickOnce-sovelluksena.</span><span class="sxs-lookup"><span data-stu-id="88d8d-113">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="88d8d-114">Vain Microsoft Edge ja Internet Explorer (tuetuissa Microsoft Windows -versioissa) tukevat ClickOnce-sovelluksia.</span><span class="sxs-lookup"><span data-stu-id="88d8d-114">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="88d8d-115">Työnkulkueditorin ClickOnce-sovellus vaatii 64-bittisen käyttöjärjestelmän.</span><span class="sxs-lookup"><span data-stu-id="88d8d-115">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="88d8d-116">PDF-tiedostojen esikatseluun suosittelemme modernia verkkoselainta, kuten Microsoft Edgeä (uusin julkinen versio) Windows 10 -käyttöjärjestelmässä tai Google Chromea (uusin julkinen versio) Windows 10-, Windows 8.1-, Windows 8- tai Windows 7 -käyttöjärjestelmässä tai Google Nexus 10 -tabletissa.</span><span class="sxs-lookup"><span data-stu-id="88d8d-116">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="88d8d-117">Verkon vaatimukset</span><span class="sxs-lookup"><span data-stu-id="88d8d-117">Network requirements</span></span>
> * <span data-ttu-id="88d8d-118">Human Resources on suunniteltu verkkoihin, joiden viive on enintään 250–300 millisekuntia (ms).</span><span class="sxs-lookup"><span data-stu-id="88d8d-118">Human Resources is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="88d8d-119">Tämä viive on selaimen asiakasohjelman ja Human Resourcesia isännöivän Microsoft Azure -palvelinkeskuksen välillä.</span><span class="sxs-lookup"><span data-stu-id="88d8d-119">This is the latency from a browser client to the Microsoft Azure data center that hosts Human Resources.</span></span> <span data-ttu-id="88d8d-120">On suositeltavaa testata verkon viive osoitteessa [www.azurespeed.com](https://www.azurespeed.com "Azuren viivetesti").</span><span class="sxs-lookup"><span data-stu-id="88d8d-120">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="88d8d-121">Human Resourcesin kaistanleveyden vaatimukset riippuvat skenaariostasi.</span><span class="sxs-lookup"><span data-stu-id="88d8d-121">Bandwidth requirements for Human Resources depend on your scenario.</span></span> <span data-ttu-id="88d8d-122">Yleisimmät tilanteet vaativat yli 50 kilotavua sekunnissa (KBps) kaistanleveyttä.</span><span class="sxs-lookup"><span data-stu-id="88d8d-122">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="88d8d-123">Älä laske kaistanleveysvaatimuksia asiakkaan sijainnista kertomalla käyttäjien määrä kaistanleveyden vähimmäisvaatimuksella.</span><span class="sxs-lookup"><span data-stu-id="88d8d-123">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="88d8d-124">Tietyn sijainnin samanaikainen käyttö on hyvin vaikea laskea.</span><span class="sxs-lookup"><span data-stu-id="88d8d-124">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="88d8d-125">Asiakkaat, jotka ovat huolissaan kaistanleveyden vaatimuksista voivat käyttää Human Resourcesin kokeiluversiota.</span><span class="sxs-lookup"><span data-stu-id="88d8d-125">For customers who are concerned about bandwidth requirements, use a trial version of Human Resources.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="88d8d-126">Tuetut Microsoft Office -sovellukset</span><span class="sxs-lookup"><span data-stu-id="88d8d-126">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="88d8d-127">Microsoft Office 2016:n Windows- tai Mac-version on oltava asennettuna, jotta Microsoft Excel- ja Word-lisäosia voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="88d8d-127">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="88d8d-128">Lisätietoja versiovaatimuksista on kohdassa [Office-integroinnin vianmääritys](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office-integroinnin vianmääritys").</span><span class="sxs-lookup"><span data-stu-id="88d8d-128">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="88d8d-129">Microsoft Office 2007 tai sitä uudempi on oltava asennettuna, jotta voit tarkastella Vie Exceliin- tai Vie Wordiin -toimintojen luomia asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="88d8d-129">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="88d8d-130">Alueellinen käytettävyys, kielet ja lokalisointi</span><span class="sxs-lookup"><span data-stu-id="88d8d-130">Regional availability, languages, and localization</span></span>

<span data-ttu-id="88d8d-131">Voit ladata PDF-tiedoston maista, alueista ja kielistä, joita Human Resources tukee kohdasta [Microsoft Dynamics 365:n kansainvälinen saatavuus](https://docs.microsoft.com/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="88d8d-131">You can download a PDF file of the countries, regions, and languages Human Resources supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="88d8d-132">Kun käyttöliittymä on lokalisoitu muille kielille, kaikki käyttäjätiedot tallennetaan kielellä, jolla ne on kirjoitettu.</span><span class="sxs-lookup"><span data-stu-id="88d8d-132">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="88d8d-133">Voit luoda sähköposteja ja malleja muilla kielillä, mutta tiedot, kuten aikataulun tiedot, ovat tällä hetkellä käytettävissä vain englanniksi.</span><span class="sxs-lookup"><span data-stu-id="88d8d-133">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="88d8d-134">Jos olet kehittäjä, joka on kiinnostunut maa- tai aluekohtaisten mukautusten luonnista, tai kun luot ratkaisun maalle tai alueelle, jota Microsoft ei tällä hetkellä tue, Katso lisätietoja kohdasta [Globalisaatio](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="88d8d-134">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>