---
title: NULLCONTAINER ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NULLCONTAINER-funktiota käytetään.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: d08a4a12d2b142744d3f35c6f1088ec25158c97c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563219"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="505e1-103">NULLCONTAINER ER-funktio</span><span class="sxs-lookup"><span data-stu-id="505e1-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="505e1-104">`NULLCONTAINER`-funktio palauttaa tyhjäarvo-*säilön (tietueen)* arvon, jolla on sama rakenne kuin määritetyllä tietueluettelolla tai tietueella.</span><span class="sxs-lookup"><span data-stu-id="505e1-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="505e1-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="505e1-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="505e1-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="505e1-106">Arguments</span></span>

<span data-ttu-id="505e1-107">`list`: *Tietueluettelo* tai *Säilö (tietue)*</span><span class="sxs-lookup"><span data-stu-id="505e1-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="505e1-108">Tietolähteen kelvollinen polku on joko *Tietueluettelo* tai *Säilö (tietue)*-tyyppi.</span><span class="sxs-lookup"><span data-stu-id="505e1-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="505e1-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="505e1-109">Return values</span></span>

<span data-ttu-id="505e1-110">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="505e1-110">*Container (record)*</span></span>

<span data-ttu-id="505e1-111">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="505e1-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="505e1-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="505e1-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="505e1-113">Tämä toiminto on vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="505e1-113">This function is obsolete.</span></span> <span data-ttu-id="505e1-114">Käytä sen sijaan `EMPTYRECORD`-funktiota.</span><span class="sxs-lookup"><span data-stu-id="505e1-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="505e1-115">Lisätietoja on kohdassa [EMPTYRECORD](er-functions-record-emptyrecord.md)</span><span class="sxs-lookup"><span data-stu-id="505e1-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="505e1-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="505e1-116">Example</span></span>

<span data-ttu-id="505e1-117">`NULLCONTAINER (SPLIT ("abc", 1))` palauttaa uuden tyhjän tietueen, jonka rakenne on sama kuin `SPLIT`-toiminnon palauttamalla luettelolla.</span><span class="sxs-lookup"><span data-stu-id="505e1-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="505e1-118">Lisätietoja on kohdassa [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="505e1-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="505e1-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="505e1-119">Additional resources</span></span>

[<span data-ttu-id="505e1-120">Tallennustoiminnot</span><span class="sxs-lookup"><span data-stu-id="505e1-120">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]