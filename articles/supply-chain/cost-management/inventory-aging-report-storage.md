---
title: Varaston erääntymisraportti
description: Tässä ohjeaiheessa käsitellään toimintoa, jolla voi suorittaa varaston erääntymisraportin ja jolla tuloksen saa käyttöön lomakkeena ja kaaviona.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810248"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="a84cd-103">Varaston erääntymisraportti</span><span class="sxs-lookup"><span data-stu-id="a84cd-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="a84cd-104">Microsoft Dynamics 365 Supply Chain Managementissa voi suorittaa **Varaston erääntyminen** -raportin, jonka saa sitten käyttöön lomakkeena ja kaaviona.</span><span class="sxs-lookup"><span data-stu-id="a84cd-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="a84cd-105">Lomakkeessa sarakkeita ja koostesaldoja säädetään dynaamisesti määritetyn asettelun mukaan.</span><span class="sxs-lookup"><span data-stu-id="a84cd-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="a84cd-106">Kaavio muodostaa visuaalisen suodatusta tukevan yleiskuvan, jossa voi porautua tietoihin.</span><span class="sxs-lookup"><span data-stu-id="a84cd-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="a84cd-107">Lisäksi **Varaston erääntymisraportti** -nimisessä tietoyksikössä voi tuoda **Varaston erääntyminen** -raportin tulokset esimerkiksi Microsoft Excel- tai PDF-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="a84cd-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="a84cd-108">Tällainen **Varaston erääntyminen** -raportin suorittamistapa on kätevä, jos tuloksessa on runsaasti rivejä.</span><span class="sxs-lookup"><span data-stu-id="a84cd-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="a84cd-109">Tuloksessa voi olla esimerkiksi runsaasti rivejä, jos 50 000 nimikkeestä ja 300 myymälästä luodaan varastoja ja pyydät varaston erääntymistä nimikkeen, sijainnin ja varaston perusteella.</span><span class="sxs-lookup"><span data-stu-id="a84cd-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="a84cd-110">Varaston erääntymisraportin suorittaminen</span><span class="sxs-lookup"><span data-stu-id="a84cd-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="a84cd-111">Valitse **Kustannushintojen hallinta \> Kyselyt ja raportit \> Varaston erääntymisraportin tallennus**.</span><span class="sxs-lookup"><span data-stu-id="a84cd-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="a84cd-112">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a84cd-112">Select **New**.</span></span>
1. <span data-ttu-id="a84cd-113">Kirjoita raportin yksilöivä nimi **Prosessin tunniste – nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a84cd-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="a84cd-114">Valitse **Tunniste – tunnus** -raportti ja tee tarvittava suodatus.</span><span class="sxs-lookup"><span data-stu-id="a84cd-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="a84cd-115">Raportti suoritetaan aina erätyönä.</span><span class="sxs-lookup"><span data-stu-id="a84cd-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="a84cd-116">Kun erätyö on valmis, tulos näkyy **Varaston erääntymisraportin tallennus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="a84cd-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="a84cd-117">Voit tarkastella tulosta perinteisenä ruudukkoasetteluna valitsemalla **Näytä tiedot**.</span><span class="sxs-lookup"><span data-stu-id="a84cd-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="a84cd-118">Voit tarkastella tulosta koostekaaviona valitsemalla **Näytä kaavio**.</span><span class="sxs-lookup"><span data-stu-id="a84cd-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a84cd-119">Lomake ei sisällä raporttiasettelussa määritettyjä välisummia.</span><span class="sxs-lookup"><span data-stu-id="a84cd-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="a84cd-120">Voit viedä **Varaston erääntymisraportti** -tietoyksikössä **Varaston erääntyminen** -raportin tuloksen käyttämällä **Prosessin tunniste – nimi** -kentän suodatinta niissä muodoissa, joita tietojen hallinta tukee.</span><span class="sxs-lookup"><span data-stu-id="a84cd-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
