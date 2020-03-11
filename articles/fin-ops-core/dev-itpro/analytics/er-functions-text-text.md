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
ms.openlocfilehash: c08aca949ffc7e62009bf3f6c664d96b368f43e7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040891"
---
# <span data-ttu-id="169e4-103"><a name="TEXT">TEXT ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="169e4-103"><a name="TEXT">TEXT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="169e4-104">`TEXT`-funktio palauttaa määritetyn numeron *merkkijono*-arvona, sen jälkeen, kun se on muunnettu tekstimerkkijonoksi. Se puolestaan muotoillaan nykyisen sovellusesiintymän palvelimen aluekohtaisten asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="169e4-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="169e4-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="169e4-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="169e4-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="169e4-106">Arguments</span></span>

<span data-ttu-id="169e4-107">`number`: *Kokonaisluku* tai *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="169e4-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="169e4-108">Numero, jota ei pidä muuntaa tekstimerkkijonoksi.</span><span class="sxs-lookup"><span data-stu-id="169e4-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="169e4-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="169e4-109">Return values</span></span>

<span data-ttu-id="169e4-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="169e4-110">*String*</span></span>

<span data-ttu-id="169e4-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="169e4-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="169e4-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="169e4-112">Usage notes</span></span>

<span data-ttu-id="169e4-113">*Todellinen*-tyyppisten arvojen merkkijonon muunnos on rajoitettu kahteen desimaaliin.</span><span class="sxs-lookup"><span data-stu-id="169e4-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="169e4-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="169e4-114">Example</span></span>

<span data-ttu-id="169e4-115">Jos Microsoft Dynamics 365 Finance -esiintymän palvelimen aluekohtaisiksi asetuksiksi on määritetty **FI-FI**, `TEXT (NOW ())` palauttaa nykyisen sovellusistunnon päivämäärän 17.12.2015 tekstimerkkijonona **17.12.2015 07.59.23**.</span><span class="sxs-lookup"><span data-stu-id="169e4-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="169e4-116">`TEXT (1/3)` palauttaa **"0.33"**.</span><span class="sxs-lookup"><span data-stu-id="169e4-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="169e4-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="169e4-117">Additional resources</span></span>

[<span data-ttu-id="169e4-118">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="169e4-118">Text functions</span></span>](er-functions-category-text.md)
