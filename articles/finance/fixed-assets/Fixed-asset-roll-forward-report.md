---
title: Käyttöomaisuuden eteenpäin siirron raportti
description: Tässä ohjeaiheessa käsitellään käyttöomaisuuden eteenpäin siirron raporttia.
author: saraschi2
manager: ''
ms.date: 01/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 6793233367756b9e9d1cbfd4690b47efe49a8008
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187403"
---
# <a name="fixed-assets-roll-forward-report"></a><span data-ttu-id="057b9-103">Käyttöomaisuuden eteenpäin siirron raportti</span><span class="sxs-lookup"><span data-stu-id="057b9-103">Fixed assets roll forward report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="057b9-104">**Käyttöomaisuuden siirto eteenpäin** -raportti on helposti luettava Microsoft Excel -muotoinen raportti, jossa eritellään kauden sulkemista, tilipäätöksiä ja veroilmoituksia varten tarvittavat käyttöomaisuustiedot.</span><span class="sxs-lookup"><span data-stu-id="057b9-104">The **Fixed assets roll forward** report provides, in an easy-to-read Microsoft Excel format, the detailed fixed asset data that you require for period closing, financial statements, and tax reporting.</span></span> <span data-ttu-id="057b9-105">Raportti sisältää käyttöomaisuuden alku- ja loppusaldot sekä kauden arvostuksen muutokset. Lisäksi siinä on kauden aikana tapahtuneet uudet käyttöomaisuuden hankinnat ja luovutukset.</span><span class="sxs-lookup"><span data-stu-id="057b9-105">The report includes start and end balances for fixed assets, together with valuation movements for the period, and any new asset acquisitions and disposals that occurred during the period.</span></span> <span data-ttu-id="057b9-106">Tiedot raportoidaan käyttöomaisuuseräkohtaisesti, ja arvojen yhteenveto on saatavana käyttöomaisuusryhmille ja yritykselle.</span><span class="sxs-lookup"><span data-stu-id="057b9-106">Data is reported for individual fixed assets, and values are also summarized for fixed asset groups and the legal entity.</span></span>

<span data-ttu-id="057b9-107">**Käyttöomaisuuden siirto eteenpäin** -raportti käyttää sähköistä raportointi- eli ER-kehystä.</span><span class="sxs-lookup"><span data-stu-id="057b9-107">The **Fixed assets roll forward** report uses the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="057b9-108">Käyttömaisuusmallin ja käyttöomaisuuden eteenpäinsiirron määrityksen on tuotava ennen raportin suorittamista Microsoft Dynamics Lifecycle Servicesistä (LCS).</span><span class="sxs-lookup"><span data-stu-id="057b9-108">Before you can run the report, the Fixed assets model and Fixed asset roll-forward configurations must be imported from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="057b9-109">Ohjeet löydät artikkelista [Lataa sähköisen raportoinnin konfiguraatiot Lifecycle Servicesistä](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span><span class="sxs-lookup"><span data-stu-id="057b9-109">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span></span>

<span data-ttu-id="057b9-110">Raportti on saatavana Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin versiossa 7.3 tai hotfix-korjauksena Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin heinäkuun 2017 versiossa.</span><span class="sxs-lookup"><span data-stu-id="057b9-110">This report is available in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, or as a hotfix for Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span> <span data-ttu-id="057b9-111">Heinäkuun 2017 versiota käyttävissä ympäristöissä on otettava käyttöön kolme hotfix-korjausta:</span><span class="sxs-lookup"><span data-stu-id="057b9-111">Three hotfixes must be applied to environments that have the July 2017 release:</span></span>

- <span data-ttu-id="057b9-112">**KB 4041754:** sähköisen raportoinnin (ER) määritystä ei voi ladata LCS:stä, sillä sitä ei voi käyttää nykyisessä versiossa sen jälkeen, kun ympäristön päivityspaketti on otettu käyttöön</span><span class="sxs-lookup"><span data-stu-id="057b9-112">**KB 4041754:** Electronic reporting (ER) configuration can't be downloaded from LCS as not applicable for the current version after applying the platform update package</span></span>
- <span data-ttu-id="057b9-113">**KB 4056107:** sähköisen raportoinnin (GER) kumulatiivinen päivitys 5</span><span class="sxs-lookup"><span data-stu-id="057b9-113">**KB 4056107:** Electronic reporting (GER) cumulative update 5</span></span>
- <span data-ttu-id="057b9-114">**KB 4056353:** Käyttöomaisuuden ilmoitusten ja huomautusten raportit eivät vastaa GAAP- ja IFRS-vaatimuksia</span><span class="sxs-lookup"><span data-stu-id="057b9-114">**KB 4056353:** Fixed assets Statement and Notes reports don't meet the requirements in GAAP and IFRS</span></span>

<span data-ttu-id="057b9-115">Seuraavassa taulussa käsitellään raportissa valittavina olevat kentät.</span><span class="sxs-lookup"><span data-stu-id="057b9-115">The following table describes the fields that are available on the report.</span></span>


|                    <span data-ttu-id="057b9-116">Kenttä</span><span class="sxs-lookup"><span data-stu-id="057b9-116">Field</span></span>                    |                                                                                                                                <span data-ttu-id="057b9-117">kuvaus</span><span class="sxs-lookup"><span data-stu-id="057b9-117">Description</span></span>                                                                                                                                |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              <span data-ttu-id="057b9-118">Saldot: alku</span><span class="sxs-lookup"><span data-stu-id="057b9-118">Balances: Opening</span></span>              |                                                                                           <span data-ttu-id="057b9-119">Käyttöomaisuuden nettokirjanpitoarvo raportissa määritettynä alkupäivämääränä.</span><span class="sxs-lookup"><span data-stu-id="057b9-119">The fixed asset net book value as of the "from" date that is specified on the report.</span></span>                                                                                           |
|              <span data-ttu-id="057b9-120">Saldot: loppu</span><span class="sxs-lookup"><span data-stu-id="057b9-120">Balances: Closing</span></span>              |                                                                                            <span data-ttu-id="057b9-121">Käyttöomaisuuden nettokirjanpitoarvo raportissa määritettynä päättymismääränä.</span><span class="sxs-lookup"><span data-stu-id="057b9-121">The fixed asset net book value as of the "to" date that is specified on the report.</span></span>                                                                                            |
|         <span data-ttu-id="057b9-122">Hankinnat: alkuarvo</span><span class="sxs-lookup"><span data-stu-id="057b9-122">Acquisitions: Opening value</span></span>         |                                                 <span data-ttu-id="057b9-123">Kaikkien <strong>Hankinta</strong>- ja <strong>Hankintaoikaisu</strong>-tyyppisten tapahtumien summa raportissa määritettyyn alkupäivämäärään saakka.</span><span class="sxs-lookup"><span data-stu-id="057b9-123">The sum of all transactions of the <strong>Acquisition</strong> and <strong>Acquisition adjustment</strong> types up to the "from" date that is specified on the report.</span></span>                                                  |
|      <span data-ttu-id="057b9-124">Hankinnat: kauden hankinnat</span><span class="sxs-lookup"><span data-stu-id="057b9-124">Acquisitions: Period acquisitions</span></span>      |                                                 <span data-ttu-id="057b9-125">Kaikkien <strong>Hankinta</strong>- ja <strong>Hankintaoikaisu</strong>-tyyppisten tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana.</span><span class="sxs-lookup"><span data-stu-id="057b9-125">The sum of all transactions of the <strong>Acquisition</strong> and <strong>Acquisition adjustment</strong> types that were posted during the date range for the report.</span></span>                                                  |
|       <span data-ttu-id="057b9-126">Hankinnat: kauden luovutukset</span><span class="sxs-lookup"><span data-stu-id="057b9-126">Acquisitions: Period disposals</span></span>        |                                                                        <span data-ttu-id="057b9-127">Kaikkien sellaisten kirjattujen hankinnan peruutusten summa, joiden luovutustapahtuma oli raportin päivämäärävälin aikana.</span><span class="sxs-lookup"><span data-stu-id="057b9-127">The sum of all acquisition reversals that were posted that had a disposal transaction during the date range for the report.</span></span>                                                                        |
|         <span data-ttu-id="057b9-128">Hankinnat: loppuarvo</span><span class="sxs-lookup"><span data-stu-id="057b9-128">Acquisitions: Closing value</span></span>         |                                                  <span data-ttu-id="057b9-129">Kaikkien <strong>Hankinta</strong>- ja <strong>Hankintaoikaisu</strong>-tyyppisten tapahtumien summa raportissa määritettyyn päättymismäärään saakka.</span><span class="sxs-lookup"><span data-stu-id="057b9-129">The sum of all transactions of the <strong>Acquisition</strong> and <strong>Acquisition adjustment</strong> types up to the "to" date that is specified on the report.</span></span>                                                   |
|        <span data-ttu-id="057b9-130">Poistot: alkuarvo</span><span class="sxs-lookup"><span data-stu-id="057b9-130">Depreciations: Opening value</span></span>         | <span data-ttu-id="057b9-131">Kaikkien <strong>Poisto</strong>-, <strong>Poistojen oikaisu</strong>-, <strong>Erityinen poistovähennys</strong>- ja <strong>Erikoispoisto</strong>-tyyppisten tapahtumien summa raportissa määritettyyn alkupäivämäärään saakka.</span><span class="sxs-lookup"><span data-stu-id="057b9-131">The sum of all transactions of the <strong>Depreciation</strong>, <strong>Depreciation adjustment</strong>, <strong>Special depreciation allowance</strong>, and <strong>Extraordinary depreciation</strong> types up to the "from" date that is specified on the report.</span></span> |
|     <span data-ttu-id="057b9-132">Poistot: kauden poistot</span><span class="sxs-lookup"><span data-stu-id="057b9-132">Depreciations: Period depreciations</span></span>     |                         <span data-ttu-id="057b9-133">Kaikkien <strong>Poisto</strong>, <strong>Poistojen oikaisu</strong>- ja <strong>Erikoispoisto</strong>--tyyppisten tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana.</span><span class="sxs-lookup"><span data-stu-id="057b9-133">The sum of all transactions of the <strong>Depreciation</strong>, <strong>Depreciation adjustment</strong>, and <strong>Extraordinary depreciation</strong> types that were posted during the date range for the report.</span></span>                          |
| <span data-ttu-id="057b9-134">Poistot: kauden erikoispoistot</span><span class="sxs-lookup"><span data-stu-id="057b9-134">Depreciations: Period special depreciations</span></span> |                                                              <span data-ttu-id="057b9-135">Kaikkien <strong>Erityinen poistovähennys</strong>-tyypin tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana.</span><span class="sxs-lookup"><span data-stu-id="057b9-135">The sum of all transactions of the <strong>Special depreciation allowance</strong> type that were posted during the date range for the report.</span></span>                                                               |
|       <span data-ttu-id="057b9-136">Poistot: kauden luovutukset</span><span class="sxs-lookup"><span data-stu-id="057b9-136">Depreciations: Period disposals</span></span>       |                                                                       <span data-ttu-id="057b9-137">Kaikkien sellaisten kirjattujen poiston peruutusten summa, joiden luovutustapahtuma oli raportin päivämäärävälin aikana.</span><span class="sxs-lookup"><span data-stu-id="057b9-137">The sum of all depreciation reversals that were posted that had a disposal transaction during the date range for the report.</span></span>                                                                        |
|        <span data-ttu-id="057b9-138">Poistot: loppuarvo</span><span class="sxs-lookup"><span data-stu-id="057b9-138">Depreciations: Closing value</span></span>         |  <span data-ttu-id="057b9-139">Kaikkien <strong>Poisto</strong>-, <strong>Poistojen oikaisu</strong>-, <strong>Erityinen poistovähennys</strong>- ja <strong>Erikoispoisto</strong>-tyyppisten tapahtumien summa raportissa määritettyyn päättymismäärään saakka.</span><span class="sxs-lookup"><span data-stu-id="057b9-139">The sum of all transactions of the <strong>Depreciation</strong>, <strong>Depreciation adjustment</strong>, <strong>Special depreciation allowance</strong>, and <strong>Extraordinary depreciation</strong> types up to the "to" date that is specified on the report.</span></span>  |
|    <span data-ttu-id="057b9-140">Kirjanpitoarvon korotus/alennus: alkuarvo</span><span class="sxs-lookup"><span data-stu-id="057b9-140">Write-ups/Write downs: Opening value</span></span>     |                              <span data-ttu-id="057b9-141">Kaikkien <strong>Kirjanpitoarvon korotus</strong>-, <strong>Kirjanpitoarvon alennus</strong>- ja <strong>Uudelleenarvostus</strong>-tyyppisten tapahtumien summa raportissa määritettyyn alkupäivämäärään saakka.</span><span class="sxs-lookup"><span data-stu-id="057b9-141">The sum of all transactions of the <strong>Write up adjustment</strong>, <strong>Write down adjustment</strong>, and <strong>Revaluation</strong> types up to the "from" date that is specified on the report.</span></span>                               |
|   <span data-ttu-id="057b9-142">Kirjanpitoarvon korotus/alennus: kauden kirjanpitoarvon korotus</span><span class="sxs-lookup"><span data-stu-id="057b9-142">Write-ups/Write downs: Period write ups</span></span>   |                                                                    <span data-ttu-id="057b9-143">Kaikkien <strong>Kirjanpitoarvon korotus</strong> -tyypin tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana.</span><span class="sxs-lookup"><span data-stu-id="057b9-143">The sum of all transactions of the <strong>Write up adjustment</strong> type that were posted during the date range for the report.</span></span>                                                                    |
|  <span data-ttu-id="057b9-144">Kirjanpitoarvon korotus/alennus: kauden kirjanpitoarvon alennus</span><span class="sxs-lookup"><span data-stu-id="057b9-144">Write-ups/Write downs: Period write downs</span></span>  |                                                                   <span data-ttu-id="057b9-145">Kaikkien <strong>Kirjanpitoarvon alennus</strong> -tyypin tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana.</span><span class="sxs-lookup"><span data-stu-id="057b9-145">The sum of all transactions of the <strong>Write down adjustment</strong> type that were posted during the date range for the report.</span></span>                                                                   |
| <span data-ttu-id="057b9-146">Kirjanpitoarvon korotus/alennus: kauden uudelleenarvostukset</span><span class="sxs-lookup"><span data-stu-id="057b9-146">Write-ups/Write downs: Period revaluations</span></span>  |                                                                        <span data-ttu-id="057b9-147">Kaikkien <strong>Uudelleenarvostus</strong>-tyypin tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana.</span><span class="sxs-lookup"><span data-stu-id="057b9-147">The sum of all transactions of the <strong>Revaluation</strong> type that were posted during the date range for the report.</span></span>                                                                        |
|   <span data-ttu-id="057b9-148">Kirjanpitoarvon korotus/alennus: kauden luovutukset</span><span class="sxs-lookup"><span data-stu-id="057b9-148">Write-ups/Write downs: Period disposals</span></span>   |                                                           <span data-ttu-id="057b9-149">Kaikkien sellaisten kirjattujen kirjanpitoarvon korotuksen, kirjanpitoarvon alennuksen ja uudelleenarvostuksen peruutusten summa, joiden luovutustapahtuma oli raportin päivämäärävälin aikana.</span><span class="sxs-lookup"><span data-stu-id="057b9-149">The sum of all write-up, write-down, and revaluation reversals that were posted that had a disposal transaction during the date range for the report.</span></span>                                                           |
|    <span data-ttu-id="057b9-150">Kirjanpitoarvon korotus/alennus: loppuarvo</span><span class="sxs-lookup"><span data-stu-id="057b9-150">Write-ups/Write downs: Closing value</span></span>     |                               <span data-ttu-id="057b9-151">Kaikkien <strong>Kirjanpitoarvon korotus</strong>-, <strong>Kirjanpitoarvon alennus</strong>- ja <strong>Uudelleenarvostus</strong>-tyyppisten tapahtumien summa raportissa määritettyyn päättymismäärään saakka.</span><span class="sxs-lookup"><span data-stu-id="057b9-151">The sum of all transactions of the <strong>Write up adjustment</strong>, <strong>Write down adjustment</strong>, and <strong>Revaluation</strong> types up to the "to" date that is specified on the report.</span></span>                                |
|          <span data-ttu-id="057b9-152">Luovutukset: luovutuksen päivämäärä</span><span class="sxs-lookup"><span data-stu-id="057b9-152">Disposals: Disposal date</span></span>           |                                                                                                                <span data-ttu-id="057b9-153">Käyttöomaisuuskirjan luovutuksen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="057b9-153">The disposal date for the fixed asset book.</span></span>                                                                                                                |
|    <span data-ttu-id="057b9-154">Luovutukset: nettokirjanpitoarvon luovutus</span><span class="sxs-lookup"><span data-stu-id="057b9-154">Disposals: Net book value at disposal</span></span>    |                                                                                                    <span data-ttu-id="057b9-155">Käyttöomaisuuskirjan nettokirjanpitoarvo luovutushetkellä.</span><span class="sxs-lookup"><span data-stu-id="057b9-155">The net book value of the fixed asset book at the time of disposal.</span></span>                                                                                                    |
|            <span data-ttu-id="057b9-156">Luovutukset: myyntiarvo</span><span class="sxs-lookup"><span data-stu-id="057b9-156">Disposals: Sale value</span></span>            |                                                                                               <span data-ttu-id="057b9-157">Käyttöomaisuuskirjan luovutuksen myyntiarvo – myyntitapahtuma.</span><span class="sxs-lookup"><span data-stu-id="057b9-157">The sales value for the fixed asset book with a disposal – sale transaction.</span></span>                                                                                                |
|           <span data-ttu-id="057b9-158">Luovutukset: hävikkiarvo</span><span class="sxs-lookup"><span data-stu-id="057b9-158">Disposals: Scrap value</span></span>            |                                                                                               <span data-ttu-id="057b9-159">Käyttöomaisuuskirjan luovutuksen hävikkiarvo – hävikkitapahtuma.</span><span class="sxs-lookup"><span data-stu-id="057b9-159">The scrap value for the fixed asset book with a disposal – scrap transaction.</span></span>                                                                                               |
|           <span data-ttu-id="057b9-160">Luovutukset: tulos</span><span class="sxs-lookup"><span data-stu-id="057b9-160">Disposals: Profit/Loss</span></span>            |                                                                                 <span data-ttu-id="057b9-161">Käyttöomaisuuskirjan luovutustapahtuman osana lasketun voiton tai tappion arvo.</span><span class="sxs-lookup"><span data-stu-id="057b9-161">The profit or loss value that is calculated as part of the disposal transaction for the fixed asset book.</span></span>                                                                                 |
