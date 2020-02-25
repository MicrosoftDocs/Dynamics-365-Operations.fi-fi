---
title: Tulostimen ER-kohteen tyyppi
description: Tässä ohjeaiheessa selitetään, miten kullekin lähteviä asiakirjoja joko PDF-muodossa tai Microsoft Office -muodossa (Excel/Word) luomaan määritetty sähköisen raportoinnin (ER) muodon KANSIO- tai TIEDOSTO-komponentin tulostinkohde määritetään.
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019747"
---
# <a name="PrinterDestinationType"></a><span data-ttu-id="829a9-103">Tulostinkohde</span><span class="sxs-lookup"><span data-stu-id="829a9-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="829a9-104">Voit lähettää luodun asiakirjan suoraan verkkotulostimeen suoraa tulostusta varten.</span><span class="sxs-lookup"><span data-stu-id="829a9-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="829a9-105">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="829a9-105">Prerequisites</span></span>

<span data-ttu-id="829a9-106">Ennen aloittamista sinun on asennettava ja määritettävä asiakirjan reititysagentti ja rekisteröitävä sitten verkkotulostimet.</span><span class="sxs-lookup"><span data-stu-id="829a9-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="829a9-107">Lisätietoja on kohdassa [Verkkotulostuksen käyttöönotto asentamalla asiakirjan reititysagentti](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent)</span><span class="sxs-lookup"><span data-stu-id="829a9-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="829a9-108">Tulostinkohteen käytettäväksi asettaminen</span><span class="sxs-lookup"><span data-stu-id="829a9-108">Make the Printer destination available</span></span>

<span data-ttu-id="829a9-109">Jos haluat, että **Tulostin**-kohde on käytettävissä Microsoftin Dynamics 365 Financen kulloisessakin esiintymässä, siirry **Ominaisuuksien hallinta** -työtilaan ja ota seuraavat ominaisuudet käyttöön tässä järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="829a9-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="829a9-110">Muunna sähköisen raportoinnin lähtevät asiakirjat Microsoft Office -muodoista PDF-muotoon</span><span class="sxs-lookup"><span data-stu-id="829a9-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="829a9-111">Asiakirjareitityksen agentti lähtevien asiakirjojen sähköisen raportoinnin kohteena</span><span class="sxs-lookup"><span data-stu-id="829a9-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="829a9-112">[![ER-tulostinkohteen toiminnon käyttöönotto ominaisuuksien hallinnassa](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="829a9-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="829a9-113">Soveltuvuus</span><span class="sxs-lookup"><span data-stu-id="829a9-113">Applicability</span></span>

<span data-ttu-id="829a9-114">**Tulostin**-kohde voidaan määrittää vain tiedostokomponenteille, joita käytetään tulosteen luomiseen joko tulostettavassa PDF-muodossa (PDF Mergerin tai PDF-tiedoston muotoelementit) tai Microsoft Office Excel/Word -muodossa (Excel-tiedosto).</span><span class="sxs-lookup"><span data-stu-id="829a9-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="829a9-115">Kun tuloste luodaan PDF-muodossa, se lähetetään tulostimeen.</span><span class="sxs-lookup"><span data-stu-id="829a9-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="829a9-116">Kun tuloste luodaan Microsoft Office -muodossa, se muunnetaan automaattisesti PDF-muotoon ja lähetetään sitten tulostimeen.</span><span class="sxs-lookup"><span data-stu-id="829a9-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="829a9-117">Rajoitukset</span><span class="sxs-lookup"><span data-stu-id="829a9-117">Limitations</span></span>

<span data-ttu-id="829a9-118">Tämä ominaisuus on esikatseluominaisuus, ja siihen sovelletaan ehdoissa [Microsoft Dynamics 365 -esikatselujen lisäkäyttöehdot](https://go.microsoft.com/fwlink/?linkid=2105274) esitettyjä käyttöehtoja.</span><span class="sxs-lookup"><span data-stu-id="829a9-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="829a9-119">**Tulostin**-kohdetta käytetään vain pilvikäyttöönotoissa.</span><span class="sxs-lookup"><span data-stu-id="829a9-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="829a9-120">Käytä tulostinkohdetta</span><span class="sxs-lookup"><span data-stu-id="829a9-120">Use the Printer destination</span></span>

1. <span data-ttu-id="829a9-121">Määritä **Käytössä** -asetuksen arvoksi **Kyllä**, jos haluat lähettää luodun tiedoston tulostimeen.</span><span class="sxs-lookup"><span data-stu-id="829a9-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="829a9-122">Valitse **Tulostimen nimi** -kentässä asianmukainen verkkotulostin.</span><span class="sxs-lookup"><span data-stu-id="829a9-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="829a9-123">Aseta **Tallenna tulostusarkistoon?** -asetuksen arvoksi **Kyllä**, jos haluat tallentaa luodun tulosteen tulostusarkistoon, jotta se voidaan tulostaa myös myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="829a9-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="829a9-124">Arkistoitu tuloste on myöhemmin käytettävissä kohdassa **Organisaation hallinta** \> **Kyselyt ja raportit** \> **Raporttiarkisto**.</span><span class="sxs-lookup"><span data-stu-id="829a9-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="829a9-125">[![Tulostinkohteen käyttö](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="829a9-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="829a9-126">**Muunna PDF-muotoon** -asetuksen ei tarvitse olla käytössä, kun määrität **Tulostin**-kohteen.</span><span class="sxs-lookup"><span data-stu-id="829a9-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="829a9-127">PDF-muunnos tulostusta varten tapahtuu, vaikka asetus ei olisi käytössä.</span><span class="sxs-lookup"><span data-stu-id="829a9-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="829a9-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="829a9-128">Additional resources</span></span>

- [<span data-ttu-id="829a9-129">Sähköisen raportoinnin (ER) yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="829a9-129">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="829a9-130">Sähköisen raportoinnin (ER) kohteet</span><span class="sxs-lookup"><span data-stu-id="829a9-130">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
