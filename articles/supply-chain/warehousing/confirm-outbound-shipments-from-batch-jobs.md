---
title: Vahvista lähtevät lähetykset erätöistä
description: Tässä ohjeaiheessa on ohjeita erätyön määrittämiseksi. Erätyö vahvistaa automaattisesti lähtevät siirtotilauslähetykset lähetysvalmiille kuormille.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 69e61e1c04dd72efbe1d2f028c078100e07176f6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838439"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="d15d1-103">Vahvista lähtevät lähetykset erätöistä</span><span class="sxs-lookup"><span data-stu-id="d15d1-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d15d1-104">Tässä ohjeaiheessa on ohjeita erätyön määrittämiseksi. Erätyö vahvistaa automaattisesti lähtevät siirtotilauslähetykset lähetysvalmiille kuormille.</span><span class="sxs-lookup"><span data-stu-id="d15d1-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="d15d1-105">Tässä kuvattu erätyö koskee vain siirtotilauslähetyksiä, ei myyntitilauksia.</span><span class="sxs-lookup"><span data-stu-id="d15d1-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="d15d1-106">Lähtevien lähetysten vahvistaminen erätöistä -ominaisuuden käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="d15d1-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="d15d1-107">Ennen kuin käytät tätä toimintoa, se on otettava käyttöön järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="d15d1-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="d15d1-108">Järjestelmänvalvojat voivat käyttää [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sivua ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="d15d1-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="d15d1-109">Ominaisuus näkyy seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d15d1-109">The feature is listed as:</span></span>

- <span data-ttu-id="d15d1-110">**Moduuli** - *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="d15d1-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="d15d1-111">**Ominaisuuden nimi** - *Lähtevien lähetysten vahvistaminen erätöistä*</span><span class="sxs-lookup"><span data-stu-id="d15d1-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="d15d1-112">Käsittele lähtevät lähetykset</span><span class="sxs-lookup"><span data-stu-id="d15d1-112">Process outbound shipments</span></span>

<span data-ttu-id="d15d1-113">Voit määrittää ajoitetun erätyön, joka suorittaa lähtevän lähetyksen vahvistuksen kuormille, jotka ovat valmiita lähetettäviksi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d15d1-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="d15d1-114">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Käsittele lähtevät lähetykset**.</span><span class="sxs-lookup"><span data-stu-id="d15d1-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="d15d1-115">**Vahvista lähetys** -valintaikkuna aukeaa.</span><span class="sxs-lookup"><span data-stu-id="d15d1-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="d15d1-116">Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatus**.</span><span class="sxs-lookup"><span data-stu-id="d15d1-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="d15d1-117">Kyselyeditorin valintaikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="d15d1-117">The query editor dialog box opens.</span></span> <span data-ttu-id="d15d1-118">Valitse **Alue**-välilehdessä rivi, jolla on seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="d15d1-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="d15d1-119">**Taulu** - *Kuormat*</span><span class="sxs-lookup"><span data-stu-id="d15d1-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="d15d1-120">**Johdettu taulu** - *Kuormat*</span><span class="sxs-lookup"><span data-stu-id="d15d1-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="d15d1-121">**Kenttä** - *Kuorman tila*</span><span class="sxs-lookup"><span data-stu-id="d15d1-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="d15d1-122">**Ehdot** - *Lastattu*</span><span class="sxs-lookup"><span data-stu-id="d15d1-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="d15d1-123">Valitse **OK**, jos haluat palata **Vahvista lähetys** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="d15d1-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="d15d1-124">Määritä **Suorita taustalla** -pikavälilehdessä **Erän käsittely** -kohdan arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d15d1-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="d15d1-125">Valitse **Suorita taustalla** -pikavälilehdessä **Toistuminen**.</span><span class="sxs-lookup"><span data-stu-id="d15d1-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="d15d1-126">**Määritä toistuminen** -valintaikkuna aukeaa.</span><span class="sxs-lookup"><span data-stu-id="d15d1-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="d15d1-127">Määritä yritykselle ajon aikataulu tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="d15d1-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="d15d1-128">Valitse **OK**, jos haluat palata **Vahvista lähetys** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="d15d1-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="d15d1-129">Valitse **OK** **Vahvista lähetys** -valintaikkunassa, jos haluat lisätä erätyön eräjonoon.</span><span class="sxs-lookup"><span data-stu-id="d15d1-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="d15d1-130">Lisätietoja on kohdassa [Eräkäsittelyn yleiskatsaus](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d15d1-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]