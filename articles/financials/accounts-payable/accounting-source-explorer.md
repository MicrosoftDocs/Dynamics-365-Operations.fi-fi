---
title: Kirjanpitolähteen hallinta
description: Tässä artikkelissa on tietoja kirjanpitolähteen hallinnasta, jota voidaan käyttää kirjanpidon kirjauksien lähdetietojen yksityiskohtaisessa analyysissä.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de5de039c0e3332943bae4846768fc628810906e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559364"
---
# <a name="accounting-source-explorer"></a><span data-ttu-id="5f6de-103">Kirjanpitolähteen hallinta</span><span class="sxs-lookup"><span data-stu-id="5f6de-103">Accounting source explorer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f6de-104">Tässä artikkelissa on tietoja kirjanpitolähteen hallinnasta, jota voidaan käyttää kirjanpidon kirjauksien lähdetietojen yksityiskohtaisessa analyysissä.</span><span class="sxs-lookup"><span data-stu-id="5f6de-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="5f6de-105">"Accounting source explorer" on uusi sivu, joka näyttää lähdetiedot.</span><span class="sxs-lookup"><span data-stu-id="5f6de-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="5f6de-106">Voit käyttää kirjanpidon lähdehallintaa joko erillisenä työkaluna tai analysoida kirjanpidon kirjauksien tietoja.</span><span class="sxs-lookup"><span data-stu-id="5f6de-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="5f6de-107">Kirjanpidon lähdehallinnan avulla voit esimerkiksi saada kaikkein yksityiskohtaisimmat lähdetiedot kirjausketjun saldolle tai tositetapahtumalle.</span><span class="sxs-lookup"><span data-stu-id="5f6de-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="5f6de-108">Voit sitten käyttää Export to MS Excel -toimintoa, jotta voit tutkia tietoja lisää Microsoft Excelissä (esimerkiksi pivot-taulukossa tai pivot-taulukkoraportissa).</span><span class="sxs-lookup"><span data-stu-id="5f6de-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="5f6de-109">Accounting source explorer näyttää aina saman kokonaissumman jokaiselle kirjanpitotilille kuin yleisessä kirjanpidossa näkyy (esimerkiksi pääkirjassa).</span><span class="sxs-lookup"><span data-stu-id="5f6de-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="5f6de-110">Kuten pääkirjassa, voit näyttää segmenttejä eri sarakkeissa.</span><span class="sxs-lookup"><span data-stu-id="5f6de-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="5f6de-111">Valitse vain haluamasi taloushallinnon dimensiojoukko.</span><span class="sxs-lookup"><span data-stu-id="5f6de-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="5f6de-112">Parametrien avulla voit määrittää päivämäärävälin analyysia varten.</span><span class="sxs-lookup"><span data-stu-id="5f6de-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="5f6de-113">Tämä toiminto muistuttaa myös pääkirjan toimintoja.</span><span class="sxs-lookup"><span data-stu-id="5f6de-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="5f6de-114">Kaikille asiakirjoille, jotka käyttävät lähdetiedoston kehystä, kirjanpidon lähdehallinta näyttää lisätiedot, jotka perustuvat kirjanpidollisiin jakoihin ja, jos mahdollista, projektin kirjanpidollisiin jakoihin.</span><span class="sxs-lookup"><span data-stu-id="5f6de-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="5f6de-115">Nämä tiedot sisältävät rahasumman tyypin, projektin, tehtävän, luokan ja rivin ominaisuuden.</span><span class="sxs-lookup"><span data-stu-id="5f6de-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="5f6de-116">Seuraavassa on esimerkkejä analyysistä, jonka voit tehdä:</span><span class="sxs-lookup"><span data-stu-id="5f6de-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="5f6de-117">Ostotilauksien ja toimittajalaskujen väliset varianssit, koska rahasumma tyyppi, esimerkiksi kulujen varianssia, edustaa kutakin varianssia</span><span class="sxs-lookup"><span data-stu-id="5f6de-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="5f6de-118">Laskutettavat ja ei-laskutettavat tunnit ja kulut projektissa, liiketoimintayksikössä ja päätilissä</span><span class="sxs-lookup"><span data-stu-id="5f6de-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="5f6de-119">Niille lähdeasiakirjoille, jotka käyttävät lähdeasiakirjojen viitteen käyttäjätietojen käsitettä, "Accounting source explorer" näyttää vielä enemmän tietoja, kuten asiakas, toimittaja, työntekijä, tuote, määrä, yksikkö teksti sekä kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="5f6de-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="5f6de-120">Seuraavassa on esimerkkejä analyysistä, jonka voit tehdä:</span><span class="sxs-lookup"><span data-stu-id="5f6de-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="5f6de-121">Hotellikulut kunkin yrityksen yksikölle ja tilikauden hotellimerkki, kuluraporttien mukaan</span><span class="sxs-lookup"><span data-stu-id="5f6de-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="5f6de-122">Toimittajan, tuotemallin ja osaston mukaiset alennukset</span><span class="sxs-lookup"><span data-stu-id="5f6de-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="5f6de-123">Nämä tiedostot voit löytää myös todellisesta asiakirjan lähteestä "Accounting source explorerista".</span><span class="sxs-lookup"><span data-stu-id="5f6de-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>



