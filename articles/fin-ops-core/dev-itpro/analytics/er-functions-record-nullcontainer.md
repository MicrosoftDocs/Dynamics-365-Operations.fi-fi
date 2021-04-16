---
title: NULLCONTAINER ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NULLCONTAINER-funktiota käytetään.
author: NickSelin
ms.date: 12/12/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: af6651ef3c62bd8d1285fa8179ac923d3c333ce7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746504"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="7c7c5-103">NULLCONTAINER ER-funktio</span><span class="sxs-lookup"><span data-stu-id="7c7c5-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c7c5-104">`NULLCONTAINER`-funktio palauttaa tyhjäarvo-*säilön (tietueen)* arvon, jolla on sama rakenne kuin määritetyllä tietueluettelolla tai tietueella.</span><span class="sxs-lookup"><span data-stu-id="7c7c5-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c7c5-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="7c7c5-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="7c7c5-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="7c7c5-106">Arguments</span></span>

<span data-ttu-id="7c7c5-107">`list`: *Tietueluettelo* tai *Säilö (tietue)*</span><span class="sxs-lookup"><span data-stu-id="7c7c5-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="7c7c5-108">Tietolähteen kelvollinen polku on joko *Tietueluettelo* tai *Säilö (tietue)*-tyyppi.</span><span class="sxs-lookup"><span data-stu-id="7c7c5-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="7c7c5-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="7c7c5-109">Return values</span></span>

<span data-ttu-id="7c7c5-110">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="7c7c5-110">*Container (record)*</span></span>

<span data-ttu-id="7c7c5-111">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="7c7c5-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7c7c5-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="7c7c5-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="7c7c5-113">Tämä toiminto on vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="7c7c5-113">This function is obsolete.</span></span> <span data-ttu-id="7c7c5-114">Käytä sen sijaan `EMPTYRECORD`-funktiota.</span><span class="sxs-lookup"><span data-stu-id="7c7c5-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="7c7c5-115">Lisätietoja on kohdassa [EMPTYRECORD](er-functions-record-emptyrecord.md)</span><span class="sxs-lookup"><span data-stu-id="7c7c5-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="7c7c5-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="7c7c5-116">Example</span></span>

<span data-ttu-id="7c7c5-117">`NULLCONTAINER (SPLIT ("abc", 1))` palauttaa uuden tyhjän tietueen, jonka rakenne on sama kuin `SPLIT`-toiminnon palauttamalla luettelolla.</span><span class="sxs-lookup"><span data-stu-id="7c7c5-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="7c7c5-118">Lisätietoja on kohdassa [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="7c7c5-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c7c5-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7c7c5-119">Additional resources</span></span>

[<span data-ttu-id="7c7c5-120">Tallennustoiminnot</span><span class="sxs-lookup"><span data-stu-id="7c7c5-120">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]