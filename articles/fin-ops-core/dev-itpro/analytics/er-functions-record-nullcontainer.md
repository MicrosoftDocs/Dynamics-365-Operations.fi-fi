---
title: NULLCONTAINER ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NULLCONTAINER-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 1dde102acf18e451cb895b51b28d22102f38936c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915783"
---
# <span data-ttu-id="b6ca8-103"><a name="NULLCONTAINER">NULLCONTAINER ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="b6ca8-103"><a name="NULLCONTAINER">NULLCONTAINER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6ca8-104">`NULLCONTAINER`-funktio palauttaa tyhjäarvo-*säilön (tietueen)* arvon, jolla on sama rakenne kuin määritetyllä tietueluettelolla tai tietueella.</span><span class="sxs-lookup"><span data-stu-id="b6ca8-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6ca8-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="b6ca8-105">Syntax</span></span>

```
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="b6ca8-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="b6ca8-106">Arguments</span></span>

<span data-ttu-id="b6ca8-107">`list`: *Tietueluettelo* tai *Säilö (tietue)*</span><span class="sxs-lookup"><span data-stu-id="b6ca8-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="b6ca8-108">Tietolähteen kelvollinen polku on joko *Tietueluettelo* tai *Säilö (tietue)*-tyyppi.</span><span class="sxs-lookup"><span data-stu-id="b6ca8-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="b6ca8-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="b6ca8-109">Return values</span></span>

<span data-ttu-id="b6ca8-110">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="b6ca8-110">*Container (record)*</span></span>

<span data-ttu-id="b6ca8-111">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="b6ca8-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b6ca8-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="b6ca8-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="b6ca8-113">Tämä toiminto on vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="b6ca8-113">This function is obsolete.</span></span> <span data-ttu-id="b6ca8-114">Käytä sen sijaan `EMPTYRECORD`-funktiota.</span><span class="sxs-lookup"><span data-stu-id="b6ca8-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="b6ca8-115">Lisätietoja on kohdassa [EMPTYRECORD](er-functions-record-emptyrecord.md)</span><span class="sxs-lookup"><span data-stu-id="b6ca8-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="b6ca8-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="b6ca8-116">Example</span></span>

<span data-ttu-id="b6ca8-117">`NULLCONTAINER (SPLIT ("abc", 1))` palauttaa uuden tyhjän tietueen, jonka rakenne on sama kuin `SPLIT`-toiminnon palauttamalla luettelolla.</span><span class="sxs-lookup"><span data-stu-id="b6ca8-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="b6ca8-118">Lisätietoja on kohdassa [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="b6ca8-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6ca8-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b6ca8-119">Additional resources</span></span>

[<span data-ttu-id="b6ca8-120">Tallennustoiminnot</span><span class="sxs-lookup"><span data-stu-id="b6ca8-120">Record functions</span></span>](er-functions-category-record.md)
