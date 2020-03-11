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
ms.openlocfilehash: ea71bfc4b30164fd32e804bf83a46c49cd18d155
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041466"
---
# <span data-ttu-id="87a58-103"><a name="NULLCONTAINER">NULLCONTAINER ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="87a58-103"><a name="NULLCONTAINER">NULLCONTAINER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87a58-104">`NULLCONTAINER`-funktio palauttaa tyhjäarvo-*säilön (tietueen)* arvon, jolla on sama rakenne kuin määritetyllä tietueluettelolla tai tietueella.</span><span class="sxs-lookup"><span data-stu-id="87a58-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="87a58-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="87a58-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="87a58-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="87a58-106">Arguments</span></span>

<span data-ttu-id="87a58-107">`list`: *Tietueluettelo* tai *Säilö (tietue)*</span><span class="sxs-lookup"><span data-stu-id="87a58-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="87a58-108">Tietolähteen kelvollinen polku on joko *Tietueluettelo* tai *Säilö (tietue)*-tyyppi.</span><span class="sxs-lookup"><span data-stu-id="87a58-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="87a58-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="87a58-109">Return values</span></span>

<span data-ttu-id="87a58-110">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="87a58-110">*Container (record)*</span></span>

<span data-ttu-id="87a58-111">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="87a58-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="87a58-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="87a58-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="87a58-113">Tämä toiminto on vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="87a58-113">This function is obsolete.</span></span> <span data-ttu-id="87a58-114">Käytä sen sijaan `EMPTYRECORD`-funktiota.</span><span class="sxs-lookup"><span data-stu-id="87a58-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="87a58-115">Lisätietoja on kohdassa [EMPTYRECORD](er-functions-record-emptyrecord.md)</span><span class="sxs-lookup"><span data-stu-id="87a58-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="87a58-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="87a58-116">Example</span></span>

<span data-ttu-id="87a58-117">`NULLCONTAINER (SPLIT ("abc", 1))` palauttaa uuden tyhjän tietueen, jonka rakenne on sama kuin `SPLIT`-toiminnon palauttamalla luettelolla.</span><span class="sxs-lookup"><span data-stu-id="87a58-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="87a58-118">Lisätietoja on kohdassa [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="87a58-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87a58-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="87a58-119">Additional resources</span></span>

[<span data-ttu-id="87a58-120">Tallennustoiminnot</span><span class="sxs-lookup"><span data-stu-id="87a58-120">Record functions</span></span>](er-functions-category-record.md)
