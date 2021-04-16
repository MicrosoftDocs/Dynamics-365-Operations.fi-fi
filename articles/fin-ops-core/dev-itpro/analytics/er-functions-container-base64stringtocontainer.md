---
title: Base64StringToContainer-ER-funktio
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) Base64StringToContainer-funktion käyttöä.
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
ms.openlocfilehash: 6fd08d9a2522bdf497b1926c884a4583065d9f19
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754371"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="c6099-103">Base64StringToContainer-ER-funktio</span><span class="sxs-lookup"><span data-stu-id="c6099-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6099-104">`BASE64STRINGTOCONTAINER`-[funktio](er-formula-language.md#functions) muuntaa *Merkkijono*-tyypin määritetyn syötteen *[Säilö](er-functions-category-container.md)*-tyypin tietokohteeksi.</span><span class="sxs-lookup"><span data-stu-id="c6099-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6099-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="c6099-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="c6099-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="c6099-106">Arguments</span></span>

<span data-ttu-id="c6099-107">`input`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="c6099-107">`input`: *String*</span></span>

<span data-ttu-id="c6099-108">*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="c6099-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="c6099-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="c6099-109">Return values</span></span>

<span data-ttu-id="c6099-110">*Säilö*</span><span class="sxs-lookup"><span data-stu-id="c6099-110">*Container*</span></span>

<span data-ttu-id="c6099-111">Näin tulokseksi saadaan BLOB-muotoinen binaariarvo.</span><span class="sxs-lookup"><span data-stu-id="c6099-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c6099-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="c6099-112">Usage notes</span></span>

<span data-ttu-id="c6099-113">Parametri ei kelpaa -poikkeus annetaan, jos syöttömerkkijono ei sisällä oikeaa binaarin tekstiin koodaamisrakenteiden Base64-ryhmää.</span><span class="sxs-lookup"><span data-stu-id="c6099-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="c6099-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="c6099-114">Example</span></span>

<span data-ttu-id="c6099-115">Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:</span><span class="sxs-lookup"><span data-stu-id="c6099-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="c6099-116">**DocuTypeGroup**-sovellusluettelointiin viittaava *Dynamics 365 for Operations / Luettelointi* -tyypin **DocuTypeGroupEnum**-juuritietolähde.</span><span class="sxs-lookup"><span data-stu-id="c6099-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="c6099-117">**CustTable**-sovellustauluun viittaava *Dynamics 365 for Operations / Taulutietueet* -tyypin **Asiakas**-juuritietolähde</span><span class="sxs-lookup"><span data-stu-id="c6099-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="c6099-118">Seuraavalla tavalla määritetyn *Laskettu kenttä* -tyypin **\#Media**-tietolähde:</span><span class="sxs-lookup"><span data-stu-id="c6099-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="c6099-119">Se lisätään **Asiakas**-tietolähteen alitietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="c6099-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="c6099-120">Se sisältää lausekkeen `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span><span class="sxs-lookup"><span data-stu-id="c6099-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="c6099-121">Seuraavalla tavalla määritetyn *Laskettu kenttä* -tyypin **\#MediaAsBase64String**-tietolähde:</span><span class="sxs-lookup"><span data-stu-id="c6099-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="c6099-122">Se lisätään **Asiakas.\#Media**-tietolähteen alitietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="c6099-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="c6099-123">Se sisältää lausekkeen `Customer.'#Media'.'getFileContentAsBase64String()'`.</span><span class="sxs-lookup"><span data-stu-id="c6099-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="c6099-124">Seuraavalla tavalla määritetyn *Laskettu kenttä* -tyypin **\#BlobFomBase64**-tietolähde:</span><span class="sxs-lookup"><span data-stu-id="c6099-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="c6099-125">Se lisätään **Asiakas.\#Media**-tietolähteen alitietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="c6099-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="c6099-126">Se sisältää lausekkeen `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span><span class="sxs-lookup"><span data-stu-id="c6099-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="c6099-127">Tässä esimerkissä **\#MediaAsBase64String**-tietolähde koodaa nykyisen medialiitteen binaarisisällön tekstinä, joka ilmaisee binaarin tekstiin koodaamisrakenteiden Base64-ryhmän.</span><span class="sxs-lookup"><span data-stu-id="c6099-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="c6099-128">**\#BlobFomBase64**-tietolähde purkaa Base64-merkkijonon koodauksen ja palauttaa BLOB-muotoisen binaariarvon.</span><span class="sxs-lookup"><span data-stu-id="c6099-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![ER-mallin yhdistämismäärityksen suunnitteluohjelman sivun näytetietolähde](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="c6099-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c6099-130">Additional resources</span></span>

[<span data-ttu-id="c6099-131">Säilöfunktiot</span><span class="sxs-lookup"><span data-stu-id="c6099-131">Container functions</span></span>](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]