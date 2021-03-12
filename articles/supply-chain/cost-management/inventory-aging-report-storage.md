---
title: Varaston erääntymisraportin tallennus
description: Tässä ohjeaiheessa käsitellään toimintoa, jolla voi suorittaa varaston erääntymisraportin ja jolla tuloksen saa käyttöön lomakkeena ja kaaviona.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8a292bd7a7ccbb09af1955e1e253b45e230c1009
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005424"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="c066f-103">Varaston erääntymisraportin tallennus</span><span class="sxs-lookup"><span data-stu-id="c066f-103">Inventory aging report storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c066f-104">Microsoft Dynamics 365 Supply Chain Managementissa voi suorittaa **Varaston erääntymisraportin tallennus** -raportin, jonka saa sitten käyttöön lomakkeena ja kaaviona.</span><span class="sxs-lookup"><span data-stu-id="c066f-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="c066f-105">Lomakkeessa sarakkeita ja koostesaldoja säädetään dynaamisesti määritetyn asettelun mukaan.</span><span class="sxs-lookup"><span data-stu-id="c066f-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="c066f-106">Kaavio muodostaa visuaalisen suodatusta tukevan yleiskuvan, jossa voi porautua tietoihin.</span><span class="sxs-lookup"><span data-stu-id="c066f-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="c066f-107">Lisäksi **Varaston erääntymisraportti** -nimisessä tietoyksikössä voi tuoda **Varaston erääntymisraportin tallennus** -raportin tulokset esimerkiksi Microsoft Excel- tai PDF-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="c066f-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="c066f-108">Tällainen **Varaston erääntymisraportin tallennus** -raportin suorittamistapa on kätevä, jos tuloksessa on runsaasti rivejä.</span><span class="sxs-lookup"><span data-stu-id="c066f-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="c066f-109">Tuloksessa voi olla esimerkiksi runsaasti rivejä, jos 50 000 nimikkeestä ja 300 myymälästä luodaan varastoja ja pyydät varaston erääntymistä nimikkeen, sijainnin ja varaston perusteella.</span><span class="sxs-lookup"><span data-stu-id="c066f-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="c066f-110">Varastoarvon tallennuksen raporttitoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="c066f-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="c066f-111">Ennen kuin käytät tätä toimintoa, sinun on otettava se käyttöön järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="c066f-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="c066f-112">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="c066f-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="c066f-113">Toiminto näkyy seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="c066f-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="c066f-114">**Moduuli** - kustannustenhallinta</span><span class="sxs-lookup"><span data-stu-id="c066f-114">**Module** - Cost management</span></span>
- <span data-ttu-id="c066f-115">**Toiminnon nimi** - Varaston erääntymisraportin tallennus</span><span class="sxs-lookup"><span data-stu-id="c066f-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="c066f-116">Suorita varaston erääntymisraportin tallennus</span><span class="sxs-lookup"><span data-stu-id="c066f-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="c066f-117">Valitse **Kustannushintojen hallinta \> Kyselyt ja raportit \> Varaston erääntymisraportin tallennus**.</span><span class="sxs-lookup"><span data-stu-id="c066f-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="c066f-118">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="c066f-118">Select **New**.</span></span>
1. <span data-ttu-id="c066f-119">Kirjoita raportin yksilöivä nimi **Prosessin tunniste – nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c066f-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="c066f-120">Valitse **Tunniste – tunnus** -raportti ja tee tarvittava suodatus.</span><span class="sxs-lookup"><span data-stu-id="c066f-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="c066f-121">Raportti suoritetaan aina erätyönä.</span><span class="sxs-lookup"><span data-stu-id="c066f-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="c066f-122">Kun erätyö on valmis, tulos näkyy **Varaston erääntymisraportin tallennus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c066f-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="c066f-123">Voit tarkastella tulosta perinteisenä ruudukkoasetteluna valitsemalla **Näytä tiedot**.</span><span class="sxs-lookup"><span data-stu-id="c066f-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="c066f-124">Voit tarkastella tulosta koostekaaviona valitsemalla **Näytä kaavio**.</span><span class="sxs-lookup"><span data-stu-id="c066f-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c066f-125">Lomake ei sisällä raporttiasettelussa määritettyjä välisummia.</span><span class="sxs-lookup"><span data-stu-id="c066f-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="c066f-126">Voit viedä **Varaston erääntymisraportti** -tietoyksikössä **Varaston erääntymisraportin tallennus** -raportin tuloksen käyttämällä **Prosessin tunniste – nimi** -kentän suodatinta niissä muodoissa, joita tietojen hallinta tukee.</span><span class="sxs-lookup"><span data-stu-id="c066f-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
