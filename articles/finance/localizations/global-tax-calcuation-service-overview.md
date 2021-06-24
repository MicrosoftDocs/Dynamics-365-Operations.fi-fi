---
title: Verolaskenta (esiversio)
description: Tässä ohjeaiheessa selitetään verolaskentamahdollisuuden yleinen laajuus ja ominaisuudet.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184098"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="16664-103">Verolaskenta (esiversio)</span><span class="sxs-lookup"><span data-stu-id="16664-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="16664-104">Verolaskenta on hyperskaalautuva monivuokaajapalvelu, jonka avulla Global Tax Engine voi automatisoida ja yksinkertaistaa verotuksen määritys- ja laskentaprosessia.</span><span class="sxs-lookup"><span data-stu-id="16664-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="16664-105">Veromoduuli on täysin konfiguroitavissa.</span><span class="sxs-lookup"><span data-stu-id="16664-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="16664-106">Määritettäviä elementtejä ovat muun muassa verotettava tietomalli, verokoodi, verojen kohdistuksen matriisi ja verolaskelmakaava.</span><span class="sxs-lookup"><span data-stu-id="16664-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="16664-107">Veromoduuli toimii Microsoft Azure -ydinpalvelualustalla ja tarjoaa modernia teknologiaa ja eksponentiaalisen skaalautuvuuden.</span><span class="sxs-lookup"><span data-stu-id="16664-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="16664-108">Verolaskenta integroituu Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin kanssa.</span><span class="sxs-lookup"><span data-stu-id="16664-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="16664-109">Lopulta se tulee integroitumaan myös Dynamics 365 Project Operationsiin, Dynamics 365 Commerceen ja muihin ensimmäisen ja kolmannen osapuolen sovelluksiin.</span><span class="sxs-lookup"><span data-stu-id="16664-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="16664-110">Kun otat veron laskentapalvelun käyttöön, joitakin liittyvien tietojen toimintoja voidaan suorittaa muissa tietokeskuksissa kuin palvelun tietoja ylläpitävässä tietokeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="16664-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="16664-111">Tarkista [ehdot](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md), ennen kuin otat veron laskentapalvelun käyttöön.</span><span class="sxs-lookup"><span data-stu-id="16664-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="16664-112">Tietosuojasi on meille tärkeä.</span><span class="sxs-lookup"><span data-stu-id="16664-112">Your privacy is important to us.</span></span> <span data-ttu-id="16664-113">Lisätietoja on [tietosuojalausekkeessa](https://go.microsoft.com/fwlink/?LinkId=521839).</span><span class="sxs-lookup"><span data-stu-id="16664-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="16664-114">Verolaskenta on mikropalvelupohjainen veromoduuli, joka tarjoaa eksponentiaalisen skaalautuvuuden.</span><span class="sxs-lookup"><span data-stu-id="16664-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="16664-115">Sen avulla voit suorittaa seuraavia tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="16664-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="16664-116">Määritä verolaskenta RCS:n (Regulatory Configuration Service) kautta.</span><span class="sxs-lookup"><span data-stu-id="16664-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="16664-117">RCS on parannettu versio sähköisen raportoinnin (ER) suunnittelijasta, ja se on saatavana erillisenä palveluna.</span><span class="sxs-lookup"><span data-stu-id="16664-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="16664-118">Määritä veromatriisi määrittämään automaattisesti verokoodit ja -prosentit.</span><span class="sxs-lookup"><span data-stu-id="16664-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="16664-119">Määritä veromatriisi määrittämään automaattisesti verorekisteröintinumerot.</span><span class="sxs-lookup"><span data-stu-id="16664-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="16664-120">Määritä verolaskelman suunnittelija määrittämään kaavoja ja ehtoja.</span><span class="sxs-lookup"><span data-stu-id="16664-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="16664-121">Jaa verotuksen määritys- ja laskentaratkaisu yritysten välillä.</span><span class="sxs-lookup"><span data-stu-id="16664-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="16664-122">Jos haluat käyttää verolaskentapalvelua, asenna verolaskentapalvelun apuohjelma Microsoft Dynamics Lifecycle Services (LCS) -palvelun projektista.</span><span class="sxs-lookup"><span data-stu-id="16664-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="16664-123">Viimeistele sitten RCS:n asetukset ja ota käyttöön verolaskentapalvelu Financessa ja Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="16664-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="16664-124">Lisätietoja on kohdassa [Veroaplvelun käytön aloittaminen](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="16664-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="16664-125">Käytettävyys</span><span class="sxs-lookup"><span data-stu-id="16664-125">Availability</span></span>

<span data-ttu-id="16664-126">Verolaskenta on käytettävissä vain eristysympäristöissä ja valituille asiakkaille julkisen esiversio-ohjelman kautta.</span><span class="sxs-lookup"><span data-stu-id="16664-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="16664-127">Lopulta se tulee yleisesti kaikkien asiakkaiden saataville ja tuotantoympäristöihin.</span><span class="sxs-lookup"><span data-stu-id="16664-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="16664-128">Uusia ominaisuuksia julkaistaan jatkuvasti, joten tarkista ajan tasalla oleva dokumentaatio usein, jotta opit tuettujen ominaisuuksien kattavuudesta ja laajuudesta.</span><span class="sxs-lookup"><span data-stu-id="16664-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="16664-129">Verolaskenta otetaan käyttöön seuraavilla Azuren maantieteellisillä alueilla.</span><span class="sxs-lookup"><span data-stu-id="16664-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="16664-130">Se otetaan käyttöön myös useammilla Azuren maantieteellisillä alueilla asiakkaiden tarpeiden mukaan:</span><span class="sxs-lookup"><span data-stu-id="16664-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="16664-131">Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="16664-131">United States</span></span>
- <span data-ttu-id="16664-132">Eurooppa</span><span class="sxs-lookup"><span data-stu-id="16664-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="16664-133">Veronlaskenta ei tue Dynamics 365:n paikallista käyttöönottoa.</span><span class="sxs-lookup"><span data-stu-id="16664-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="16664-134">Se ei myöskään tue aiempia versioita, kuten Dynamics AX 2012 -versiota.</span><span class="sxs-lookup"><span data-stu-id="16664-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="16664-135">Toiminnon tärkeimmät ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="16664-135">Feature highlights</span></span>

- <span data-ttu-id="16664-136">Määritettävä veromatriisi, jonka avulla määritetään ja lasketaan vero automaattisesti</span><span class="sxs-lookup"><span data-stu-id="16664-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="16664-137">Useiden veron rekisteröintinumeroiden tukeminen</span><span class="sxs-lookup"><span data-stu-id="16664-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="16664-138">Siirtotilausten tuki verojen määritystä ja laskentaa varten</span><span class="sxs-lookup"><span data-stu-id="16664-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="16664-139">Siirtotilausten tuki useiden verorekisterinumeroiden määrittämiseksi</span><span class="sxs-lookup"><span data-stu-id="16664-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="16664-140">Tuetut tapahtumat</span><span class="sxs-lookup"><span data-stu-id="16664-140">Supported transactions</span></span>

<span data-ttu-id="16664-141">Verolaskenta voidaan ottaa käyttöön yritys- ja tapahtumakohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="16664-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="16664-142">Seuraavia tapahtumia tuetaan:</span><span class="sxs-lookup"><span data-stu-id="16664-142">The following transactions are supported:</span></span>

- <span data-ttu-id="16664-143">Myyntiprosessi</span><span class="sxs-lookup"><span data-stu-id="16664-143">Sales process</span></span>

    - <span data-ttu-id="16664-144">Myyntitarjous</span><span class="sxs-lookup"><span data-stu-id="16664-144">Sales quotation</span></span>
    - <span data-ttu-id="16664-145">Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="16664-145">Sales order</span></span>
    - <span data-ttu-id="16664-146">Vahvistus</span><span class="sxs-lookup"><span data-stu-id="16664-146">Confirmation</span></span>
    - <span data-ttu-id="16664-147">Materiaaliluettelo</span><span class="sxs-lookup"><span data-stu-id="16664-147">Picking list</span></span>
    - <span data-ttu-id="16664-148">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="16664-148">Packing slip</span></span>
    - <span data-ttu-id="16664-149">Myyntilasku</span><span class="sxs-lookup"><span data-stu-id="16664-149">Sales invoice</span></span>
    - <span data-ttu-id="16664-150">Hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="16664-150">Credit note</span></span>
    - <span data-ttu-id="16664-151">Palautustilaus</span><span class="sxs-lookup"><span data-stu-id="16664-151">Return order</span></span>
    - <span data-ttu-id="16664-152">Otsikon muu kulu</span><span class="sxs-lookup"><span data-stu-id="16664-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="16664-153">Rivin muu kulu</span><span class="sxs-lookup"><span data-stu-id="16664-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="16664-154">Ostoprosessi</span><span class="sxs-lookup"><span data-stu-id="16664-154">Purchase process</span></span>

    - <span data-ttu-id="16664-155">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="16664-155">Purchase order</span></span>
    - <span data-ttu-id="16664-156">Vahvistus</span><span class="sxs-lookup"><span data-stu-id="16664-156">Confirmation</span></span>
    - <span data-ttu-id="16664-157">Saapumisluettelo</span><span class="sxs-lookup"><span data-stu-id="16664-157">Receipts list</span></span>
    - <span data-ttu-id="16664-158">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="16664-158">Product receipt</span></span>
    - <span data-ttu-id="16664-159">Ostolasku</span><span class="sxs-lookup"><span data-stu-id="16664-159">Purchase invoice</span></span>
    - <span data-ttu-id="16664-160">Otsikon muu kulu</span><span class="sxs-lookup"><span data-stu-id="16664-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="16664-161">Rivin muu kulu</span><span class="sxs-lookup"><span data-stu-id="16664-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="16664-162">Hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="16664-162">Credit note</span></span>
    - <span data-ttu-id="16664-163">Palautustilaus</span><span class="sxs-lookup"><span data-stu-id="16664-163">Return order</span></span>
    - <span data-ttu-id="16664-164">Ostoehdotus</span><span class="sxs-lookup"><span data-stu-id="16664-164">Purchase requisition</span></span>
    - <span data-ttu-id="16664-165">Ostoehdotuksen rivin muu kulu</span><span class="sxs-lookup"><span data-stu-id="16664-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="16664-166">Tarjouspyyntö</span><span class="sxs-lookup"><span data-stu-id="16664-166">Request for quotation</span></span>
    - <span data-ttu-id="16664-167">Tarjouspyynnön otsikon muu kulu</span><span class="sxs-lookup"><span data-stu-id="16664-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="16664-168">Tarjouspyynnön rivin muu kulu</span><span class="sxs-lookup"><span data-stu-id="16664-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="16664-169">Varastoprosessi</span><span class="sxs-lookup"><span data-stu-id="16664-169">Inventory process</span></span>

    - <span data-ttu-id="16664-170">Siirtotilaus – lähetä</span><span class="sxs-lookup"><span data-stu-id="16664-170">Transfer order – ship</span></span>
    - <span data-ttu-id="16664-171">Siirtotilaus – vastaanota</span><span class="sxs-lookup"><span data-stu-id="16664-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="16664-172">Liittyvät resurssit</span><span class="sxs-lookup"><span data-stu-id="16664-172">Related resources</span></span>

[<span data-ttu-id="16664-173">Veroapalvelun käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="16664-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="16664-174">Useita ALV-rekisterinumeroita</span><span class="sxs-lookup"><span data-stu-id="16664-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="16664-175">Siirtotilauksen verotoiminnon tuki</span><span class="sxs-lookup"><span data-stu-id="16664-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="16664-176">Näin rakennat laajennuksen veropalveluun</span><span class="sxs-lookup"><span data-stu-id="16664-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
