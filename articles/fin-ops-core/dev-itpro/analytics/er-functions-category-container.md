---
title: Luettelo säilöluokan ER-funktioista
description: Tässä aiheessa on tietoja sähköisen raportoinnin (ER) tukemista säilöfunktioista.
author: NickSelin
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 95f207538ea4f0f7df775bf28d0dcf6529d1a91c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753237"
---
# <a name="list-of-er-functions-in-the-container-category"></a><span data-ttu-id="82de0-103">Luettelo säilöluokan ER-funktioista</span><span class="sxs-lookup"><span data-stu-id="82de0-103">List of ER functions in the container category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82de0-104">[Sähköisen raportoinnin (ER)](general-electronic-reporting.md) [säilöfunktioiden](er-formula-language.md#functions) avulla voidaan suorittaa *Säilö*-tietotyypin tietolähteitä sisältäviä toimintoja.</span><span class="sxs-lookup"><span data-stu-id="82de0-104">[Electronic reporting (ER)](general-electronic-reporting.md) container [functions](er-formula-language.md#functions) can be used to perform operations that involve data sources of the *Container* data type.</span></span> <span data-ttu-id="82de0-105">Näitä toimintoja esiintyy, kun käsiteltävät tiedot ilmaisevat BLOB-muotoisten binaaritietojen kokoelman.</span><span class="sxs-lookup"><span data-stu-id="82de0-105">These operations occur when the processing data represents a collection of binary data in binary large object (BLOB) format.</span></span> <span data-ttu-id="82de0-106">Tässä aiheessa on yhteenveto näistä funktioista.</span><span class="sxs-lookup"><span data-stu-id="82de0-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="82de0-107">Luettelo tuetuista toiminnoista</span><span class="sxs-lookup"><span data-stu-id="82de0-107">List of supported functions</span></span>

| <span data-ttu-id="82de0-108">Toiminto</span><span class="sxs-lookup"><span data-stu-id="82de0-108">Function</span></span> | <span data-ttu-id="82de0-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="82de0-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="82de0-110">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="82de0-110">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="82de0-111">Tämä funktio palauttaa *Säilö*-arvon. Tämä arvo koostuu binaarisisällöstä, jonka koodaus on purettu määritetystä ASCII-merkkijonosta. Tämä merkkijono puolestaan ilmaiseen binaarista tekstiin koodattavien rakenteiden Base64-ryhmän.</span><span class="sxs-lookup"><span data-stu-id="82de0-111">This function returns a *Container* value that consists of binary content that is decoded from the specified ASCII string that represents a Base64 group of binary-to-text encoding schemes.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="82de0-112">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="82de0-112">Additional resources</span></span>

[<span data-ttu-id="82de0-113">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="82de0-113">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="82de0-114">Sähköisen raportoinnin kaavojen suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="82de0-114">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="82de0-115">Sähköisen raportoinnin kaavakieli</span><span class="sxs-lookup"><span data-stu-id="82de0-115">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]