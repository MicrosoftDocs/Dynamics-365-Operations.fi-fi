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
ms.openlocfilehash: dac6283ec35d3d03f586ca157048bd3ecc4bfa8a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743924"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="3a3c7-103">NULLCONTAINER ER-funktio</span><span class="sxs-lookup"><span data-stu-id="3a3c7-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a3c7-104">`NULLCONTAINER`-funktio palauttaa tyhjäarvo-*säilön (tietueen)* arvon, jolla on sama rakenne kuin määritetyllä tietueluettelolla tai tietueella.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a3c7-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="3a3c7-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="3a3c7-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="3a3c7-106">Arguments</span></span>

<span data-ttu-id="3a3c7-107">`list`: *Tietueluettelo* tai *Säilö (tietue)*</span><span class="sxs-lookup"><span data-stu-id="3a3c7-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="3a3c7-108">Tietolähteen kelvollinen polku on joko *Tietueluettelo* tai *Säilö (tietue)*-tyyppi.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3a3c7-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="3a3c7-109">Return values</span></span>

<span data-ttu-id="3a3c7-110">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="3a3c7-110">*Container (record)*</span></span>

<span data-ttu-id="3a3c7-111">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3a3c7-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="3a3c7-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="3a3c7-113">Tämä toiminto on vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-113">This function is obsolete.</span></span> <span data-ttu-id="3a3c7-114">Käytä sen sijaan `EMPTYRECORD`-funktiota.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="3a3c7-115">Lisätietoja on kohdassa [EMPTYRECORD](er-functions-record-emptyrecord.md)</span><span class="sxs-lookup"><span data-stu-id="3a3c7-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="3a3c7-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="3a3c7-116">Example</span></span>

<span data-ttu-id="3a3c7-117">`NULLCONTAINER (SPLIT ("abc", 1))` palauttaa uuden tyhjän tietueen, jonka rakenne on sama kuin `SPLIT`-toiminnon palauttamalla luettelolla.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="3a3c7-118">Lisätietoja on kohdassa [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="3a3c7-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a3c7-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="3a3c7-119">Additional resources</span></span>

[<span data-ttu-id="3a3c7-120">Tallennustoiminnot</span><span class="sxs-lookup"><span data-stu-id="3a3c7-120">Record functions</span></span>](er-functions-category-record.md)
