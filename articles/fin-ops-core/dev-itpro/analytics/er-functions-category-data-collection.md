---
title: Luettelo ER-funktioista tietojenkeräysluokassa
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin (ER) tukemista tietojenkeräysfunktioista.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b318945c9cd10b237843d26cfdc46fc08e84e268
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917807"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="ca7ea-103">Luettelo ER-funktioista tietojenkeräysluokassa</span><span class="sxs-lookup"><span data-stu-id="ca7ea-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca7ea-104">Sähköisen raportoinnin (ER) tiedonkeruufunktioita käytetään suorittamaan laskenta ja summaus ER-muodossa, joka suoritetaan perustuen tietoihin, jotka on jo luotu **teksti**- tai **XML**-muodossa.</span><span class="sxs-lookup"><span data-stu-id="ca7ea-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="ca7ea-105">Tätä lähestymistapaa käytetään parantamaan suoritettavan ER-muodon suorituskykyä, syöttämään arvojen juoksevat summat luotaviin asiakirjoihin ja muihin tarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="ca7ea-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="ca7ea-106">Tässä aiheessa on yhteenveto näistä funktioista.</span><span class="sxs-lookup"><span data-stu-id="ca7ea-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="ca7ea-107">Luettelo tuetuista toiminnoista</span><span class="sxs-lookup"><span data-stu-id="ca7ea-107">List of supported functions</span></span>

| <span data-ttu-id="ca7ea-108">Toiminto</span><span class="sxs-lookup"><span data-stu-id="ca7ea-108">Function</span></span> | <span data-ttu-id="ca7ea-109">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="ca7ea-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ca7ea-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="ca7ea-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="ca7ea-111">Tämä funktio palauttaa *Tietueluettelon* arvon, joka sisältää luettelon arvoista, jotka on palautettu **kerättyjen tietojen avainarvo** -ominaisuuden muotoelementeistä ja kerätty, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja jotka täyttävät määritetyt ehdot.</span><span class="sxs-lookup"><span data-stu-id="ca7ea-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="ca7ea-112">Jokainen ehto muodostuu avainalueesta ja avainarvosta.</span><span class="sxs-lookup"><span data-stu-id="ca7ea-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="ca7ea-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="ca7ea-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="ca7ea-114">Tämä funktio palauttaa *Kokonaislukuarvon*, joka vastaa niiden muotoelementtien määrää, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyn ehdon.</span><span class="sxs-lookup"><span data-stu-id="ca7ea-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="ca7ea-115">Ehto muodostuu avainalueesta ja avainarvosta.</span><span class="sxs-lookup"><span data-stu-id="ca7ea-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="ca7ea-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="ca7ea-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="ca7ea-117">Tämä funktio palauttaa *Kokonaislukuarvon*, joka vastaa niiden muotoelementtien määrää, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyt ehdot.</span><span class="sxs-lookup"><span data-stu-id="ca7ea-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="ca7ea-118">Jokainen ehto muodostuu avainalueesta ja avainarvosta.</span><span class="sxs-lookup"><span data-stu-id="ca7ea-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="ca7ea-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="ca7ea-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="ca7ea-120">Tämä funktio palauttaa *Merkkijonoarvon*, joka edustaa nykyisen ER-muodon elementin nimeä.</span><span class="sxs-lookup"><span data-stu-id="ca7ea-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="ca7ea-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="ca7ea-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="ca7ea-122">Tämä funktio palauttaa *Todellisen* arvon, joka on niiden arvojen summa, jotka palautettiin muotoiluelementtien sitomisella ja, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyn ehdon.</span><span class="sxs-lookup"><span data-stu-id="ca7ea-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="ca7ea-123">Ehto muodostuu avainalueesta ja avainarvosta.</span><span class="sxs-lookup"><span data-stu-id="ca7ea-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="ca7ea-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="ca7ea-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="ca7ea-125">Tämä funktio palauttaa *Todellisen* arvon, joka on niiden arvojen summa, jotka palautettiin muotoiluelementtien sitomisella ja, jotka kerättiin, kun muotoelementtejä käytettiin lähtevän asiakirjan luomiseen muotoajon aikana ja joka täyttää määritetyt ehdot.</span><span class="sxs-lookup"><span data-stu-id="ca7ea-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="ca7ea-126">Jokainen ehto muodostuu avainalueesta ja avainarvosta.</span><span class="sxs-lookup"><span data-stu-id="ca7ea-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="ca7ea-127">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ca7ea-127">Additional resources</span></span>

[<span data-ttu-id="ca7ea-128">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ca7ea-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="ca7ea-129">Sähköisen raportoinnin kaavojen suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="ca7ea-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="ca7ea-130">Sähköisen raportoinnin kaavakieli</span><span class="sxs-lookup"><span data-stu-id="ca7ea-130">Electronic reporting formula language</span></span>](er-formula-language.md)
