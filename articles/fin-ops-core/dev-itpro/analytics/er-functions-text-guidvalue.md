---
title: GUIDVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) GUIDVALUE-funktiota käytetään.
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
ms.openlocfilehash: a7b8c782aff488a433c40a49ab7f4fe2d0e944e4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041162"
---
# <span data-ttu-id="1b6e7-103"><a name="GUIDVALUE">GUIDVALUE ER -funktio</a></span><span class="sxs-lookup"><span data-stu-id="1b6e7-103"><a name="GUIDVALUE">GUIDVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b6e7-104">`GUIDVALUE`-funktio muuntaa *Merkkijono*-tyypin määritetyn syötteen *GUID*-tyypin tietokohteeksi.</span><span class="sxs-lookup"><span data-stu-id="1b6e7-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b6e7-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="1b6e7-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="1b6e7-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="1b6e7-106">Arguments</span></span>

<span data-ttu-id="1b6e7-107">`input`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="1b6e7-107">`input`: *String*</span></span>

<span data-ttu-id="1b6e7-108">*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="1b6e7-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="1b6e7-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="1b6e7-109">Return values</span></span>

<span data-ttu-id="1b6e7-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="1b6e7-110">*GUID*</span></span>

<span data-ttu-id="1b6e7-111">Tulokseksi saatu maailmanlaajuisesti yksilöivä tunniste (GUID) -arvo.</span><span class="sxs-lookup"><span data-stu-id="1b6e7-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1b6e7-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="1b6e7-112">Usage notes</span></span>

<span data-ttu-id="1b6e7-113">Voit tehdä muunnon vastakkaiseen suuntaan käyttämällä [TEXT](er-functions-text-text.md)-funktiota. (*GUID*-tietotyypin määritetty syöte siis muunnetaan *String*-tietotyypin tietokohteeksi.)</span><span class="sxs-lookup"><span data-stu-id="1b6e7-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="1b6e7-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="1b6e7-114">Example</span></span>

<span data-ttu-id="1b6e7-115">Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:</span><span class="sxs-lookup"><span data-stu-id="1b6e7-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="1b6e7-116">*Lasketun kenttätyypin* **myID**-tietolähde, joka sisältää lausekkeen `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="1b6e7-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="1b6e7-117">**Users**-tietolähde, joka on *Taulukkotietueet*-tyypiä, joka viittaa UserInfo-tauluun</span><span class="sxs-lookup"><span data-stu-id="1b6e7-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="1b6e7-118">Tämän jälkeen voit käyttää lauseketta, kuten `FILTER (Users, Users.objectId = myID)`, joka suodattaa UserInfo-taulukon *GUID*-tietotyypin **objectID**-kentän mukaan.</span><span class="sxs-lookup"><span data-stu-id="1b6e7-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b6e7-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1b6e7-119">Additional resources</span></span>

[<span data-ttu-id="1b6e7-120">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="1b6e7-120">Text functions</span></span>](er-functions-category-text.md)
