---
title: Luettelo säilöluokan ER-funktioista
description: Tässä aiheessa on tietoja sähköisen raportoinnin (ER) tukemista säilöfunktioista.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 46d1af85773f6c3d07865658c554dee74fae625f
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739073"
---
# <a name="list-of-er-functions-in-the-container-category"></a><span data-ttu-id="ccb9e-103">Luettelo säilöluokan ER-funktioista</span><span class="sxs-lookup"><span data-stu-id="ccb9e-103">List of ER functions in the container category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ccb9e-104">[Sähköisen raportoinnin (ER)](general-electronic-reporting.md) [säilöfunktioiden](er-formula-language.md#functions) avulla voidaan suorittaa *Säilö*-tietotyypin tietolähteitä sisältäviä toimintoja.</span><span class="sxs-lookup"><span data-stu-id="ccb9e-104">[Electronic reporting (ER)](general-electronic-reporting.md) container [functions](er-formula-language.md#functions) can be used to perform operations that involve data sources of the *Container* data type.</span></span> <span data-ttu-id="ccb9e-105">Näitä toimintoja esiintyy, kun käsiteltävät tiedot ilmaisevat BLOB-muotoisten binaaritietojen kokoelman.</span><span class="sxs-lookup"><span data-stu-id="ccb9e-105">These operations occur when the processing data represents a collection of binary data in binary large object (BLOB) format.</span></span> <span data-ttu-id="ccb9e-106">Tässä aiheessa on yhteenveto näistä funktioista.</span><span class="sxs-lookup"><span data-stu-id="ccb9e-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="ccb9e-107">Luettelo tuetuista toiminnoista</span><span class="sxs-lookup"><span data-stu-id="ccb9e-107">List of supported functions</span></span>

| <span data-ttu-id="ccb9e-108">Toiminto</span><span class="sxs-lookup"><span data-stu-id="ccb9e-108">Function</span></span> | <span data-ttu-id="ccb9e-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="ccb9e-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ccb9e-110">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="ccb9e-110">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="ccb9e-111">Tämä funktio palauttaa *Säilö*-arvon. Tämä arvo koostuu binaarisisällöstä, jonka koodaus on purettu määritetystä ASCII-merkkijonosta. Tämä merkkijono puolestaan ilmaiseen binaarista tekstiin koodattavien rakenteiden Base64-ryhmän.</span><span class="sxs-lookup"><span data-stu-id="ccb9e-111">This function returns a *Container* value that consists of binary content that is decoded from the specified ASCII string that represents a Base64 group of binary-to-text encoding schemes.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="ccb9e-112">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ccb9e-112">Additional resources</span></span>

[<span data-ttu-id="ccb9e-113">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ccb9e-113">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="ccb9e-114">Sähköisen raportoinnin kaavojen suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="ccb9e-114">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="ccb9e-115">Sähköisen raportoinnin kaavakieli</span><span class="sxs-lookup"><span data-stu-id="ccb9e-115">Electronic reporting formula language</span></span>](er-formula-language.md)
