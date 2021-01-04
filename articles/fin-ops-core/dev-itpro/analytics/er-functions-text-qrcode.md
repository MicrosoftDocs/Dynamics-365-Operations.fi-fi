---
title: QRCODE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) QRCODE-funktiota käytetään.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b62ed829202028ca0cbf95a0dbc3460d047ca5a5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682964"
---
# <a name="qrcode-er-function"></a><span data-ttu-id="bc082-103">QRCODE ER -funktio</span><span class="sxs-lookup"><span data-stu-id="bc082-103">QRCODE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc082-104">`QRCODE`-funktio palauttaa *Säilön* arvon, joka esittää määritetyn merkkijonon nopean vastauskoodin (QR Code) binaarimuodossa.</span><span class="sxs-lookup"><span data-stu-id="bc082-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc082-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="bc082-105">Syntax</span></span>

```vb
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="bc082-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="bc082-106">Arguments</span></span>

<span data-ttu-id="bc082-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="bc082-107">`text`: *String*</span></span>

<span data-ttu-id="bc082-108">*Merkkijono*-arvo, joka esittelee alkuperäisen tekstin.</span><span class="sxs-lookup"><span data-stu-id="bc082-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="bc082-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="bc082-109">Return values</span></span>

<span data-ttu-id="bc082-110">*Säiliö*</span><span class="sxs-lookup"><span data-stu-id="bc082-110">*Container*</span></span>

<span data-ttu-id="bc082-111">Tuloksena oleva binaarinen virta.</span><span class="sxs-lookup"><span data-stu-id="bc082-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="bc082-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="bc082-112">Example</span></span>

<span data-ttu-id="bc082-113">Voit määrittää sähköisen raportoinnin (ER) muodon, joka luo lähtevän asiakirjan Microsoft Office -muodossa (Excel-työkirjat tai Word-asiakirjat) käyttämällä esimääritettyä mallia.</span><span class="sxs-lookup"><span data-stu-id="bc082-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="bc082-114">Tämä malli saattaa sisältää **kuva**-objektin (Excel-työkirjan) tai **kuvasisällön ohjausobjektin** (Word-asiakirjan) QR-koodikuvan paikkamerkkinä.</span><span class="sxs-lookup"><span data-stu-id="bc082-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="bc082-115">Sinun on lisättävä konfiguroituun ER-muotoon **Solu**-elementti, jota käytetään tämän paikkamerkin täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="bc082-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="bc082-116">Jos haluat määrittää, mitä tietoja QR-koodiin tallennetaan, sinun on määritettävä sidonta tälle **solu**-elementille.</span><span class="sxs-lookup"><span data-stu-id="bc082-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="bc082-117">Voit esimerkiksi määrittää tällaisen sidonnan siten, että se sisältää seuraavan lausekkeen:</span><span class="sxs-lookup"><span data-stu-id="bc082-117">For example, you can configure such binding as containing the following expression:</span></span>

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="bc082-118">Kun suoritat määritetyn ER-muodon, **LabelText** -kentän **model.ListOfShelfLabels** -tietolähdettä käytetään QR-koodikuvan luomiseen.</span><span class="sxs-lookup"><span data-stu-id="bc082-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="bc082-119">Tämä kuva korvaa asiakirjamallissa olevan QR-koodikuvan paikkamerkin käyttämällä lähtevän asiakirjan luomiseen.</span><span class="sxs-lookup"><span data-stu-id="bc082-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="bc082-120">Kun tämä luodun asiakirjan kuva skannataan, se palauttaa tekstin, joka otettiin mallin **LabelText**-kentästä **ListOfShelfLabels** -tietolähteestä.</span><span class="sxs-lookup"><span data-stu-id="bc082-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="bc082-121">Katso lisätietoja kohdasta [Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](electronic-reporting-embed-images-shapes.md)</span><span class="sxs-lookup"><span data-stu-id="bc082-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc082-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="bc082-122">Additional resources</span></span>

[<span data-ttu-id="bc082-123">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="bc082-123">Text functions</span></span>](er-functions-category-text.md)
