---
title: TEXT ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) TEXT-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: c26d0c4c8c6290bd2dbb10a288bbd59941a8d98e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915553"
---
# <span data-ttu-id="f8ae9-103"><a name="TEXT">TEXT ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="f8ae9-103"><a name="TEXT">TEXT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8ae9-104">`TEXT`-funktio palauttaa määritetyn numeron *merkkijono*-arvona, sen jälkeen, kun se on muunnettu tekstimerkkijonoksi. Se puolestaan muotoillaan nykyisen sovellusesiintymän palvelimen aluekohtaisten asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="f8ae9-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ae9-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="f8ae9-105">Syntax</span></span>

```
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="f8ae9-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="f8ae9-106">Arguments</span></span>

<span data-ttu-id="f8ae9-107">`number`: *Kokonaisluku* tai *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="f8ae9-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="f8ae9-108">Numero, jota ei pidä muuntaa tekstimerkkijonoksi.</span><span class="sxs-lookup"><span data-stu-id="f8ae9-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="f8ae9-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="f8ae9-109">Return values</span></span>

<span data-ttu-id="f8ae9-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f8ae9-110">*String*</span></span>

<span data-ttu-id="f8ae9-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="f8ae9-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f8ae9-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="f8ae9-112">Usage notes</span></span>

<span data-ttu-id="f8ae9-113">*Todellinen*-tyyppisten arvojen merkkijonon muunnos on rajoitettu kahteen desimaaliin.</span><span class="sxs-lookup"><span data-stu-id="f8ae9-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="f8ae9-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="f8ae9-114">Example</span></span>

<span data-ttu-id="f8ae9-115">Jos Microsoft Dynamics 365 Finance -esiintymän palvelimen aluekohtaisiksi asetuksiksi on määritetty **FI-FI**, `TEXT (NOW ())` palauttaa nykyisen sovellusistunnon päivämäärän 17.12.2015 tekstimerkkijonona **17.12.2015 07.59.23**.</span><span class="sxs-lookup"><span data-stu-id="f8ae9-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="f8ae9-116">`TEXT (1/3)` palauttaa **"0.33"**.</span><span class="sxs-lookup"><span data-stu-id="f8ae9-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8ae9-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f8ae9-117">Additional resources</span></span>

[<span data-ttu-id="f8ae9-118">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="f8ae9-118">Text functions</span></span>](er-functions-category-text.md)
