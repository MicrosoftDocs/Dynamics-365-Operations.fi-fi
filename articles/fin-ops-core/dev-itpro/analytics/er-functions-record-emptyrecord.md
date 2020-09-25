---
title: EMPTYRECORD ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) EMPTYRECORD-funktiota käytetään.
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
ms.openlocfilehash: 2e46fcef3d53483b782ac39a0661fc0edc8d861c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743947"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="b995a-103">EMPTYRECORD ER-funktio</span><span class="sxs-lookup"><span data-stu-id="b995a-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b995a-104">`EMPTYRECORD`-funktio palauttaa tyhjäarvo-*säilön (tietueen)* arvon, jolla on sama rakenne kuin määritetyllä tietueluettelolla tai tietueella.</span><span class="sxs-lookup"><span data-stu-id="b995a-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b995a-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="b995a-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="b995a-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="b995a-106">Arguments</span></span>

<span data-ttu-id="b995a-107">`list`: *Tietueluettelo* tai *Säilö (tietue)*</span><span class="sxs-lookup"><span data-stu-id="b995a-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="b995a-108">Tietolähteen kelvollinen polku on joko *Tietueluettelo* tai *Säilö (tietue)*-tyyppi.</span><span class="sxs-lookup"><span data-stu-id="b995a-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="b995a-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="b995a-109">Return values</span></span>

<span data-ttu-id="b995a-110">*Kontti (tietue)*</span><span class="sxs-lookup"><span data-stu-id="b995a-110">*Container (record)*</span></span>

<span data-ttu-id="b995a-111">Tuloksena oleva tietueen arvo.</span><span class="sxs-lookup"><span data-stu-id="b995a-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b995a-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="b995a-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="b995a-113">Tyhjä-tietue on tietue, jossa kaikissa kentissä on tyhjä arvo.</span><span class="sxs-lookup"><span data-stu-id="b995a-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="b995a-114">Tyhjä arvo numeroilla **0** (nolla), merkkijonoilla tyhjä merkkijono jne.</span><span class="sxs-lookup"><span data-stu-id="b995a-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="b995a-115">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="b995a-115">Example</span></span>

<span data-ttu-id="b995a-116">`EMPTYRECORD (SPLIT ("abc", 1))` palauttaa uuden tyhjän tietueen, jonka rakenne on sama kuin `SPLIT`-toiminnon palauttamalla luettelolla.</span><span class="sxs-lookup"><span data-stu-id="b995a-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="b995a-117">Lisätietoja on kohdassa [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="b995a-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b995a-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b995a-118">Additional resources</span></span>

[<span data-ttu-id="b995a-119">Tallennustoiminnot</span><span class="sxs-lookup"><span data-stu-id="b995a-119">Record functions</span></span>](er-functions-category-record.md)
