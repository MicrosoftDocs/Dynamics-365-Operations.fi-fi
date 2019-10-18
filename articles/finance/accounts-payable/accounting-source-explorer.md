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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 904f1f9fb139248205b426aec5a0372f2edb1e59
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177614"
---
# <a name="accounting-source-explorer"></a><span data-ttu-id="5ecad-103">Kirjanpitolähteen hallinta</span><span class="sxs-lookup"><span data-stu-id="5ecad-103">Accounting source explorer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ecad-104">Tässä artikkelissa on tietoja kirjanpitolähteen hallinnasta, jota voidaan käyttää kirjanpidon kirjauksien lähdetietojen yksityiskohtaisessa analyysissä.</span><span class="sxs-lookup"><span data-stu-id="5ecad-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="5ecad-105">"Accounting source explorer" on uusi sivu, joka näyttää lähdetiedot.</span><span class="sxs-lookup"><span data-stu-id="5ecad-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="5ecad-106">Voit käyttää kirjanpidon lähdehallintaa joko erillisenä työkaluna tai analysoida kirjanpidon kirjauksien tietoja.</span><span class="sxs-lookup"><span data-stu-id="5ecad-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="5ecad-107">Kirjanpidon lähdehallinnan avulla voit esimerkiksi saada kaikkein yksityiskohtaisimmat lähdetiedot kirjausketjun saldolle tai tositetapahtumalle.</span><span class="sxs-lookup"><span data-stu-id="5ecad-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="5ecad-108">Voit sitten käyttää Export to MS Excel -toimintoa, jotta voit tutkia tietoja lisää Microsoft Excelissä (esimerkiksi pivot-taulukossa tai pivot-taulukkoraportissa).</span><span class="sxs-lookup"><span data-stu-id="5ecad-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="5ecad-109">Accounting source explorer näyttää aina saman kokonaissumman jokaiselle kirjanpitotilille kuin yleisessä kirjanpidossa näkyy (esimerkiksi pääkirjassa).</span><span class="sxs-lookup"><span data-stu-id="5ecad-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="5ecad-110">Kuten pääkirjassa, voit näyttää segmenttejä eri sarakkeissa.</span><span class="sxs-lookup"><span data-stu-id="5ecad-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="5ecad-111">Valitse vain haluamasi taloushallinnon dimensiojoukko.</span><span class="sxs-lookup"><span data-stu-id="5ecad-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="5ecad-112">Parametrien avulla voit määrittää päivämäärävälin analyysia varten.</span><span class="sxs-lookup"><span data-stu-id="5ecad-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="5ecad-113">Tämä toiminto muistuttaa myös pääkirjan toimintoja.</span><span class="sxs-lookup"><span data-stu-id="5ecad-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="5ecad-114">Kaikille asiakirjoille, jotka käyttävät lähdetiedoston kehystä, kirjanpidon lähdehallinta näyttää lisätiedot, jotka perustuvat kirjanpidollisiin jakoihin ja, jos mahdollista, projektin kirjanpidollisiin jakoihin.</span><span class="sxs-lookup"><span data-stu-id="5ecad-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="5ecad-115">Nämä tiedot sisältävät rahasumman tyypin, projektin, tehtävän, luokan ja rivin ominaisuuden.</span><span class="sxs-lookup"><span data-stu-id="5ecad-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="5ecad-116">Seuraavassa on esimerkkejä analyysistä, jonka voit tehdä:</span><span class="sxs-lookup"><span data-stu-id="5ecad-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="5ecad-117">Ostotilauksien ja toimittajalaskujen väliset varianssit, koska rahasumma tyyppi, esimerkiksi kulujen varianssia, edustaa kutakin varianssia</span><span class="sxs-lookup"><span data-stu-id="5ecad-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="5ecad-118">Laskutettavat ja ei-laskutettavat tunnit ja kulut projektissa, liiketoimintayksikössä ja päätilissä</span><span class="sxs-lookup"><span data-stu-id="5ecad-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="5ecad-119">Niille lähdeasiakirjoille, jotka käyttävät lähdeasiakirjojen viitteen käyttäjätietojen käsitettä, "Accounting source explorer" näyttää vielä enemmän tietoja, kuten asiakas, toimittaja, työntekijä, tuote, määrä, yksikkö teksti sekä kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="5ecad-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="5ecad-120">Seuraavassa on esimerkkejä analyysistä, jonka voit tehdä:</span><span class="sxs-lookup"><span data-stu-id="5ecad-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="5ecad-121">Hotellikulut kunkin yrityksen yksikölle ja tilikauden hotellimerkki, kuluraporttien mukaan</span><span class="sxs-lookup"><span data-stu-id="5ecad-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="5ecad-122">Toimittajan, tuotemallin ja osaston mukaiset alennukset</span><span class="sxs-lookup"><span data-stu-id="5ecad-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="5ecad-123">Nämä tiedostot voit löytää myös todellisesta asiakirjan lähteestä "Accounting source explorerista".</span><span class="sxs-lookup"><span data-stu-id="5ecad-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>



