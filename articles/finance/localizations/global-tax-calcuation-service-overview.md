---
title: Verolaskenta (esiversio)
description: Tässä ohjeaiheessa selitetään verolaskentamahdollisuuden yleinen laajuus ja ominaisuudet.
author: wangchen
ms.date: 04/12/2021
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
ms.openlocfilehash: 3df952e0632807e55f176e63dc2047be5e622ec2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892346"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="8867b-103">Verolaskenta (esiversio)</span><span class="sxs-lookup"><span data-stu-id="8867b-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="8867b-104">Verolaskenta on hyperskaalautuva monivuokaajapalvelu, jonka avulla Global Tax Engine voi automatisoida ja yksinkertaistaa verotuksen määritys- ja laskentaprosessia.</span><span class="sxs-lookup"><span data-stu-id="8867b-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="8867b-105">Veromoduuli on täysin konfiguroitavissa.</span><span class="sxs-lookup"><span data-stu-id="8867b-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="8867b-106">Määritettäviä elementtejä ovat muun muassa verotettava tietomalli, verokoodi, verojen kohdistuksen matriisi ja verolaskelmakaava.</span><span class="sxs-lookup"><span data-stu-id="8867b-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="8867b-107">Veromoduuli toimii Microsoft Azure -ydinpalvelualustalla ja tarjoaa modernia teknologiaa ja eksponentiaalisen skaalautuvuuden.</span><span class="sxs-lookup"><span data-stu-id="8867b-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="8867b-108">Verolaskenta integroituu Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin kanssa.</span><span class="sxs-lookup"><span data-stu-id="8867b-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8867b-109">Lopulta se tulee integroitumaan myös Dynamics 365 Project Operationsiin, Dynamics 365 Commerceen ja muihin ensimmäisen ja kolmannen osapuolen sovelluksiin.</span><span class="sxs-lookup"><span data-stu-id="8867b-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="8867b-110">Verolaskenta on mikropalvelupohjainen veromoduuli, joka tarjoaa eksponentiaalisen skaalautuvuuden.</span><span class="sxs-lookup"><span data-stu-id="8867b-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="8867b-111">Sen avulla voit suorittaa seuraavia tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="8867b-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="8867b-112">Määritä verolaskenta RCS:n (Regulatory Configuration Service) kautta.</span><span class="sxs-lookup"><span data-stu-id="8867b-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="8867b-113">RCS on parannettu versio sähköisen raportoinnin (ER) suunnittelijasta, ja se on saatavana erillisenä palveluna.</span><span class="sxs-lookup"><span data-stu-id="8867b-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="8867b-114">Määritä veromatriisi määrittämään automaattisesti verokoodit ja -prosentit.</span><span class="sxs-lookup"><span data-stu-id="8867b-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="8867b-115">Määritä veromatriisi määrittämään automaattisesti verorekisteröintinumerot.</span><span class="sxs-lookup"><span data-stu-id="8867b-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="8867b-116">Määritä verolaskelman suunnittelija määrittämään kaavoja ja ehtoja.</span><span class="sxs-lookup"><span data-stu-id="8867b-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="8867b-117">Jaa verotuksen määritys- ja laskentaratkaisu yritysten välillä.</span><span class="sxs-lookup"><span data-stu-id="8867b-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="8867b-118">Jos haluat käyttää verolaskentapalvelua, asenna verolaskentapalvelun apuohjelma Microsoft Dynamics Lifecycle Services (LCS) -palvelun projektista.</span><span class="sxs-lookup"><span data-stu-id="8867b-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="8867b-119">Viimeistele sitten RCS:n asetukset ja ota käyttöön verolaskentapalvelu Financessa ja Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="8867b-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="8867b-120">Lisätietoja on kohdassa [Veroaplvelun käytön aloittaminen](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="8867b-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="8867b-121">Käytettävyys</span><span class="sxs-lookup"><span data-stu-id="8867b-121">Availability</span></span>

<span data-ttu-id="8867b-122">Verolaskenta on käytettävissä vain eristysympäristöissä ja valituille asiakkaille julkisen esiversio-ohjelman kautta.</span><span class="sxs-lookup"><span data-stu-id="8867b-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="8867b-123">Lopulta se tulee yleisesti kaikkien asiakkaiden saataville ja tuotantoympäristöihin.</span><span class="sxs-lookup"><span data-stu-id="8867b-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="8867b-124">Uusia ominaisuuksia julkaistaan jatkuvasti, joten tarkista ajan tasalla oleva dokumentaatio usein, jotta opit tuettujen ominaisuuksien kattavuudesta ja laajuudesta.</span><span class="sxs-lookup"><span data-stu-id="8867b-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="8867b-125">Verolaskenta otetaan käyttöön seuraavilla Azuren maantieteellisillä alueilla.</span><span class="sxs-lookup"><span data-stu-id="8867b-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="8867b-126">Se otetaan käyttöön myös useammilla Azuren maantieteellisillä alueilla asiakkaiden tarpeiden mukaan:</span><span class="sxs-lookup"><span data-stu-id="8867b-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="8867b-127">Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="8867b-127">United States</span></span>
- <span data-ttu-id="8867b-128">Eurooppa</span><span class="sxs-lookup"><span data-stu-id="8867b-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="8867b-129">Veronlaskenta ei tue Dynamics 365:n paikallista käyttöönottoa.</span><span class="sxs-lookup"><span data-stu-id="8867b-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="8867b-130">Se ei myöskään tue aiempia versioita, kuten Dynamics AX 2012 -versiota.</span><span class="sxs-lookup"><span data-stu-id="8867b-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="8867b-131">Toiminnon tärkeimmät ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="8867b-131">Feature highlights</span></span>

- <span data-ttu-id="8867b-132">Määritettävä veromatriisi, jonka avulla määritetään ja lasketaan vero automaattisesti</span><span class="sxs-lookup"><span data-stu-id="8867b-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="8867b-133">Useiden veron rekisteröintinumeroiden tukeminen</span><span class="sxs-lookup"><span data-stu-id="8867b-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="8867b-134">Siirtotilausten tuki verojen määritystä ja laskentaa varten</span><span class="sxs-lookup"><span data-stu-id="8867b-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="8867b-135">Siirtotilausten tuki useiden verorekisterinumeroiden määrittämiseksi</span><span class="sxs-lookup"><span data-stu-id="8867b-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="8867b-136">Tuetut tapahtumat</span><span class="sxs-lookup"><span data-stu-id="8867b-136">Supported transactions</span></span>

<span data-ttu-id="8867b-137">Verolaskenta voidaan ottaa käyttöön yritys- ja tapahtumakohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="8867b-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="8867b-138">Seuraavia tapahtumia tuetaan:</span><span class="sxs-lookup"><span data-stu-id="8867b-138">The following transactions are supported:</span></span>

- <span data-ttu-id="8867b-139">Myyntiprosessi</span><span class="sxs-lookup"><span data-stu-id="8867b-139">Sales process</span></span>

    - <span data-ttu-id="8867b-140">Myyntitarjous</span><span class="sxs-lookup"><span data-stu-id="8867b-140">Sales quotation</span></span>
    - <span data-ttu-id="8867b-141">Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="8867b-141">Sales order</span></span>
    - <span data-ttu-id="8867b-142">Vahvistus</span><span class="sxs-lookup"><span data-stu-id="8867b-142">Confirmation</span></span>
    - <span data-ttu-id="8867b-143">Materiaaliluettelo</span><span class="sxs-lookup"><span data-stu-id="8867b-143">Picking list</span></span>
    - <span data-ttu-id="8867b-144">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="8867b-144">Packing slip</span></span>
    - <span data-ttu-id="8867b-145">Myyntilasku</span><span class="sxs-lookup"><span data-stu-id="8867b-145">Sales invoice</span></span>
    - <span data-ttu-id="8867b-146">Hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="8867b-146">Credit note</span></span>
    - <span data-ttu-id="8867b-147">Palautustilaus</span><span class="sxs-lookup"><span data-stu-id="8867b-147">Return order</span></span>
    - <span data-ttu-id="8867b-148">Otsikon muu kulu</span><span class="sxs-lookup"><span data-stu-id="8867b-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="8867b-149">Rivin muu kulu</span><span class="sxs-lookup"><span data-stu-id="8867b-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="8867b-150">Ostoprosessi</span><span class="sxs-lookup"><span data-stu-id="8867b-150">Purchase process</span></span>

    - <span data-ttu-id="8867b-151">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="8867b-151">Purchase order</span></span>
    - <span data-ttu-id="8867b-152">Vahvistus</span><span class="sxs-lookup"><span data-stu-id="8867b-152">Confirmation</span></span>
    - <span data-ttu-id="8867b-153">Saapumisluettelo</span><span class="sxs-lookup"><span data-stu-id="8867b-153">Receipts list</span></span>
    - <span data-ttu-id="8867b-154">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="8867b-154">Product receipt</span></span>
    - <span data-ttu-id="8867b-155">Ostolasku</span><span class="sxs-lookup"><span data-stu-id="8867b-155">Purchase invoice</span></span>
    - <span data-ttu-id="8867b-156">Otsikon muu kulu</span><span class="sxs-lookup"><span data-stu-id="8867b-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="8867b-157">Rivin muu kulu</span><span class="sxs-lookup"><span data-stu-id="8867b-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="8867b-158">Hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="8867b-158">Credit note</span></span>
    - <span data-ttu-id="8867b-159">Palautustilaus</span><span class="sxs-lookup"><span data-stu-id="8867b-159">Return order</span></span>
    - <span data-ttu-id="8867b-160">Ostoehdotus</span><span class="sxs-lookup"><span data-stu-id="8867b-160">Purchase requisition</span></span>
    - <span data-ttu-id="8867b-161">Ostoehdotuksen rivin muu kulu</span><span class="sxs-lookup"><span data-stu-id="8867b-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="8867b-162">Tarjouspyyntö</span><span class="sxs-lookup"><span data-stu-id="8867b-162">Request for quotation</span></span>
    - <span data-ttu-id="8867b-163">Tarjouspyynnön otsikon muu kulu</span><span class="sxs-lookup"><span data-stu-id="8867b-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="8867b-164">Tarjouspyynnön rivin muu kulu</span><span class="sxs-lookup"><span data-stu-id="8867b-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="8867b-165">Varastoprosessi</span><span class="sxs-lookup"><span data-stu-id="8867b-165">Inventory process</span></span>

    - <span data-ttu-id="8867b-166">Siirtotilaus – lähetä</span><span class="sxs-lookup"><span data-stu-id="8867b-166">Transfer order – ship</span></span>
    - <span data-ttu-id="8867b-167">Siirtotilaus – vastaanota</span><span class="sxs-lookup"><span data-stu-id="8867b-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="8867b-168">Liittyvät resurssit</span><span class="sxs-lookup"><span data-stu-id="8867b-168">Related resources</span></span>

[<span data-ttu-id="8867b-169">Veroapalvelun käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="8867b-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="8867b-170">Useita ALV-rekisterinumeroita</span><span class="sxs-lookup"><span data-stu-id="8867b-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="8867b-171">Siirtotilauksen verotoiminnon tuki</span><span class="sxs-lookup"><span data-stu-id="8867b-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="8867b-172">Näin rakennat laajennuksen veropalveluun</span><span class="sxs-lookup"><span data-stu-id="8867b-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)