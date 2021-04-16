---
title: Verolaskentapalvelu (esiversio)
description: Tässä ohjeaiheessa selitetään verolaskentapalvelun yleinen laajuus ja ominaisuudet.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818221"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="94682-103">Verolaskentapalvelu (esiversio)</span><span class="sxs-lookup"><span data-stu-id="94682-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="94682-104">Verolaskentapalvelu on hyperskaalautuva monivuokaajapalvelu, jonka avulla Global Tax Engine voi automatisoida ja yksinkertaistaa verotuksen määritys- ja laskentaprosessia.</span><span class="sxs-lookup"><span data-stu-id="94682-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="94682-105">Veromoduuli on täysin konfiguroitavissa.</span><span class="sxs-lookup"><span data-stu-id="94682-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="94682-106">Määritettäviä elementtejä ovat muun muassa verotettava tietomalli, verokoodi, verojen kohdistuksen matriisi ja verolaskelmakaava.</span><span class="sxs-lookup"><span data-stu-id="94682-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="94682-107">Veromoduuli toimii Microsoft Azure -ydinpalvelualustalla ja tarjoaa modernia teknologiaa ja eksponentiaalisen skaalautuvuuden.</span><span class="sxs-lookup"><span data-stu-id="94682-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="94682-108">Verolaskentapalvelu integroituu Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin kanssa.</span><span class="sxs-lookup"><span data-stu-id="94682-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="94682-109">Lopulta se tulee integroitumaan myös Dynamics 365 Project Operationsiin, Dynamics 365 Commerceen ja muihin ensimmäisen ja kolmannen osapuolen sovelluksiin.</span><span class="sxs-lookup"><span data-stu-id="94682-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="94682-110">Verolaskentapalvelu on Microsoft-pohjainen veromoduuli, joka tarjoaa eksponentiaalisen skaalautuvuuden.</span><span class="sxs-lookup"><span data-stu-id="94682-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="94682-111">Sen avulla voit suorittaa seuraavia tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="94682-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="94682-112">Määritä verolaskentapalvelu RCS:n (Regulatory Configuration Service) kautta.</span><span class="sxs-lookup"><span data-stu-id="94682-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="94682-113">RCS on parannettu versio sähköisen raportoinnin (ER) suunnittelijasta, ja se on saatavana erillisenä palveluna.</span><span class="sxs-lookup"><span data-stu-id="94682-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="94682-114">Määritä veromatriisi määrittämään automaattisesti verokoodit ja -prosentit.</span><span class="sxs-lookup"><span data-stu-id="94682-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="94682-115">Määritä veromatriisi määrittämään automaattisesti verorekisteröintinumerot.</span><span class="sxs-lookup"><span data-stu-id="94682-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="94682-116">Määritä verolaskelman suunnittelija määrittämään kaavoja ja ehtoja.</span><span class="sxs-lookup"><span data-stu-id="94682-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="94682-117">Jaa verotuksen määritys- ja laskentaratkaisu yritysten välillä.</span><span class="sxs-lookup"><span data-stu-id="94682-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="94682-118">Jos haluat käyttää verolaskentapalvelua, asenna verolaskentapalvelun apuohjelma Microsoft Dynamics Lifecycle Services (LCS) -palvelun projektista.</span><span class="sxs-lookup"><span data-stu-id="94682-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="94682-119">Viimeistele sitten RCS:n asetukset ja ota käyttöön verolaskentapalvelu Financessa ja Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="94682-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="94682-120">Lisätietoja on kohdassa [Veroaplvelun käytön aloittaminen](https://go.microsoft.com/fwlink/?linkid=2138482).</span><span class="sxs-lookup"><span data-stu-id="94682-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="94682-121">Käytettävyys</span><span class="sxs-lookup"><span data-stu-id="94682-121">Availability</span></span>

<span data-ttu-id="94682-122">Veronlaskentapalvelu on käytettävissä vain eristysympäristöissä ja valituille asiakkaille julkisen esiversio-ohjelman kautta.</span><span class="sxs-lookup"><span data-stu-id="94682-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="94682-123">Lopulta se tulee yleisesti kaikkien asiakkaiden saataville ja tuotantoympäristöihin.</span><span class="sxs-lookup"><span data-stu-id="94682-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="94682-124">Verolaskentapalveluun toimitetaan uusia ominaisuuksia jatkossakin.</span><span class="sxs-lookup"><span data-stu-id="94682-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="94682-125">Muista siksi tarkistaa ajan tasalla oleva dokumentaatio usein, jotta opit tuettujen ominaisuuksien kattavuudesta ja laajuudesta.</span><span class="sxs-lookup"><span data-stu-id="94682-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="94682-126">Verolaskentapalvelu otetaan käyttöön seuraavilla Azuren maantieteellisillä alueilla.</span><span class="sxs-lookup"><span data-stu-id="94682-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="94682-127">Se otetaan käyttöön myös useammilla Azuren maantieteellisillä alueilla asiakkaiden tarpeiden mukaan:</span><span class="sxs-lookup"><span data-stu-id="94682-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="94682-128">Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="94682-128">United States</span></span>
- <span data-ttu-id="94682-129">Eurooppa</span><span class="sxs-lookup"><span data-stu-id="94682-129">Europe</span></span>
- <span data-ttu-id="94682-130">Ranska</span><span class="sxs-lookup"><span data-stu-id="94682-130">France</span></span>
- <span data-ttu-id="94682-131">Iso-Britannia</span><span class="sxs-lookup"><span data-stu-id="94682-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="94682-132">Veronlaskentapalvelu ei tue Dynamics 365:n paikallista käyttöönottoa.</span><span class="sxs-lookup"><span data-stu-id="94682-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="94682-133">Se ei myöskään tue aiempia versioita, kuten Dynamics AX 2012 -versiota.</span><span class="sxs-lookup"><span data-stu-id="94682-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="94682-134">Toiminnon tärkeimmät ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="94682-134">Feature highlights</span></span>

- <span data-ttu-id="94682-135">Määritettävä veromatriisi, jonka avulla määritetään ja lasketaan vero automaattisesti</span><span class="sxs-lookup"><span data-stu-id="94682-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="94682-136">Useiden arvonlisäveron rekisteröintinumeroiden tukeminen</span><span class="sxs-lookup"><span data-stu-id="94682-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="94682-137">Siirtotilausten tuki verojen määritystä ja laskentaa varten</span><span class="sxs-lookup"><span data-stu-id="94682-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="94682-138">Siirtotilausten tuki useiden ALV-rekisterinumeroiden määrittämiseksi</span><span class="sxs-lookup"><span data-stu-id="94682-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="94682-139">Tuetut tapahtumat</span><span class="sxs-lookup"><span data-stu-id="94682-139">Supported transactions</span></span>

<span data-ttu-id="94682-140">Verolaskentapalvelu voidaan ottaa käyttöön yritys- ja tapahtumakohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="94682-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="94682-141">Seuraavia tapahtumia tuetaan:</span><span class="sxs-lookup"><span data-stu-id="94682-141">The following transactions are supported:</span></span>

- <span data-ttu-id="94682-142">Myyntiprosessi</span><span class="sxs-lookup"><span data-stu-id="94682-142">Sales process</span></span>

    - <span data-ttu-id="94682-143">Myyntitarjous</span><span class="sxs-lookup"><span data-stu-id="94682-143">Sales quotation</span></span>
    - <span data-ttu-id="94682-144">Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="94682-144">Sales order</span></span>
    - <span data-ttu-id="94682-145">Vahvistus</span><span class="sxs-lookup"><span data-stu-id="94682-145">Confirmation</span></span>
    - <span data-ttu-id="94682-146">Materiaaliluettelo</span><span class="sxs-lookup"><span data-stu-id="94682-146">Picking list</span></span>
    - <span data-ttu-id="94682-147">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="94682-147">Packing slip</span></span>
    - <span data-ttu-id="94682-148">Myyntilasku</span><span class="sxs-lookup"><span data-stu-id="94682-148">Sales invoice</span></span>
    - <span data-ttu-id="94682-149">Hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="94682-149">Credit note</span></span>
    - <span data-ttu-id="94682-150">Palautustilaus</span><span class="sxs-lookup"><span data-stu-id="94682-150">Return order</span></span>
    - <span data-ttu-id="94682-151">Otsikon muu kulu</span><span class="sxs-lookup"><span data-stu-id="94682-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="94682-152">Rivin muu kulu</span><span class="sxs-lookup"><span data-stu-id="94682-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="94682-153">Ostoprosessi</span><span class="sxs-lookup"><span data-stu-id="94682-153">Purchase process</span></span>

    - <span data-ttu-id="94682-154">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="94682-154">Purchase order</span></span>
    - <span data-ttu-id="94682-155">Vahvistus</span><span class="sxs-lookup"><span data-stu-id="94682-155">Confirmation</span></span>
    - <span data-ttu-id="94682-156">Saapumisluettelo</span><span class="sxs-lookup"><span data-stu-id="94682-156">Receipts list</span></span>
    - <span data-ttu-id="94682-157">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="94682-157">Product receipt</span></span>
    - <span data-ttu-id="94682-158">Ostolasku</span><span class="sxs-lookup"><span data-stu-id="94682-158">Purchase invoice</span></span>
    - <span data-ttu-id="94682-159">Otsikon muu kulu</span><span class="sxs-lookup"><span data-stu-id="94682-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="94682-160">Rivin muu kulu</span><span class="sxs-lookup"><span data-stu-id="94682-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="94682-161">Hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="94682-161">Credit note</span></span>
    - <span data-ttu-id="94682-162">Palautustilaus</span><span class="sxs-lookup"><span data-stu-id="94682-162">Return order</span></span>
    - <span data-ttu-id="94682-163">Ostoehdotus</span><span class="sxs-lookup"><span data-stu-id="94682-163">Purchase requisition</span></span>
    - <span data-ttu-id="94682-164">Ostoehdotuksen rivin muu kulu</span><span class="sxs-lookup"><span data-stu-id="94682-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="94682-165">Tarjouspyyntö</span><span class="sxs-lookup"><span data-stu-id="94682-165">Request for quotation</span></span>
    - <span data-ttu-id="94682-166">Tarjouspyynnön otsikon muu kulu</span><span class="sxs-lookup"><span data-stu-id="94682-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="94682-167">Tarjouspyynnön rivin muu kulu</span><span class="sxs-lookup"><span data-stu-id="94682-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="94682-168">Varastoprosessi</span><span class="sxs-lookup"><span data-stu-id="94682-168">Inventory process</span></span>

    - <span data-ttu-id="94682-169">Siirtotilaus – lähetä</span><span class="sxs-lookup"><span data-stu-id="94682-169">Transfer order – ship</span></span>
    - <span data-ttu-id="94682-170">Siirtotilaus – vastaanota</span><span class="sxs-lookup"><span data-stu-id="94682-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="94682-171">Liittyvät resurssit</span><span class="sxs-lookup"><span data-stu-id="94682-171">Related resources</span></span>

[<span data-ttu-id="94682-172">Veroapalvelun käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="94682-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="94682-173">Useita ALV-rekisterinumeroita</span><span class="sxs-lookup"><span data-stu-id="94682-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="94682-174">Siirtotilauksen verotoiminnon tuki</span><span class="sxs-lookup"><span data-stu-id="94682-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="94682-175">Näin rakennat laajennuksen veropalveluun</span><span class="sxs-lookup"><span data-stu-id="94682-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
