---
title: GETENUMVALUEBYNAME ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) GETENUMVALUEBYNAME-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
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
ms.openlocfilehash: 29d7ec6498090ea47259303237c5a64a26e4926b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685928"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="25e83-103">GETENUMVALUEBYNAME ER-funktio</span><span class="sxs-lookup"><span data-stu-id="25e83-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25e83-104">`GETENUMVALUEBYNAME`-funktio etsii määritetystä luettelointitietolähteestä tiettyä *Enum*-arvoa käyttämällä *merkkijono*-arvona määritettyä luetteloinnin nimeä.</span><span class="sxs-lookup"><span data-stu-id="25e83-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="25e83-105">Jos *Enum*-arvo löytyy, funktio palauttaa sen.</span><span class="sxs-lookup"><span data-stu-id="25e83-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="25e83-106">Muussa tapauksessa funktio palauttaa **Null**-luettelointiarvon.</span><span class="sxs-lookup"><span data-stu-id="25e83-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="25e83-107">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="25e83-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="25e83-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="25e83-108">Arguments</span></span>

<span data-ttu-id="25e83-109">`enumeration data source path`: *Luettelointi*</span><span class="sxs-lookup"><span data-stu-id="25e83-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="25e83-110">Tieto lähteen kelvollinen polku, joka on jokin seuraavista luettelointityypeistä:</span><span class="sxs-lookup"><span data-stu-id="25e83-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="25e83-111">Sähköisen raportointimallin (ER) numerointi</span><span class="sxs-lookup"><span data-stu-id="25e83-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="25e83-112">ER-muodon numerointi</span><span class="sxs-lookup"><span data-stu-id="25e83-112">ER format enumeration</span></span>
- <span data-ttu-id="25e83-113">Microsoft Dynamics 365 Financen numerointi</span><span class="sxs-lookup"><span data-stu-id="25e83-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="25e83-114">`enumeration value text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="25e83-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="25e83-115">Merkkijonoarvo, joka edustaa yksittäisen luettelointiarvon nimeä.</span><span class="sxs-lookup"><span data-stu-id="25e83-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="25e83-116">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="25e83-116">Return values</span></span>

<span data-ttu-id="25e83-117">Tyhjäarvot salliva *Enum*</span><span class="sxs-lookup"><span data-stu-id="25e83-117">Nullable *Enum*</span></span>

<span data-ttu-id="25e83-118">Tulokseksi saatava luettelointiarvo.</span><span class="sxs-lookup"><span data-stu-id="25e83-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="25e83-119">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="25e83-119">Usage notes</span></span>

<span data-ttu-id="25e83-120">Poikkeusta ei heitetä, jos *Enum*-arvoa ei löydy *merkkijono*-arvona määritetyn luettelointiarvon nimen avulla.</span><span class="sxs-lookup"><span data-stu-id="25e83-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="25e83-121">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="25e83-121">Example 1</span></span>

<span data-ttu-id="25e83-122">Seuraavassa kuvassa on tietomallin **ReportDirection**-luettelointi.</span><span class="sxs-lookup"><span data-stu-id="25e83-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="25e83-123">Huomaa, että luettelointiarvoille on määritetty otsikot.</span><span class="sxs-lookup"><span data-stu-id="25e83-123">Notice that labels are defined for the enumeration values.</span></span>

![Tieto mallin luetteloinnissa käytettävissä olevat arvot](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="25e83-125">Seuraavassa kuvassa on nämä tiedot:</span><span class="sxs-lookup"><span data-stu-id="25e83-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="25e83-126">**$Direction**-tietolähde määritetään ER-raportissa.</span><span class="sxs-lookup"><span data-stu-id="25e83-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="25e83-127">Tämä tietolähde määritetään **ReportDirection**-mallin luetteloinnin perusteella.</span><span class="sxs-lookup"><span data-stu-id="25e83-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="25e83-128">`$IsArrivals`-lauseke on suunniteltu käyttämään mallin luettelointiin perustuvaa **$Direction**-tietolähdettä tämän toiminnon parametrina.</span><span class="sxs-lookup"><span data-stu-id="25e83-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="25e83-129">Tämän vertailulausekkeen arvo on **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="25e83-129">The value of this comparison expression is **TRUE**.</span></span>

![Esimerkki tietomallin luetteloinnista](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="25e83-131">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="25e83-131">Example 2</span></span>

<span data-ttu-id="25e83-132">Funktioiden `GETENUMVALUEBYNAME` ja [`LISTOFFIELDS`](er-functions-list-listoffields.md) avulla voit tuettujen luettelointien arvoja ja otsikoita tekstiarvoina.</span><span class="sxs-lookup"><span data-stu-id="25e83-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="25e83-133">(Tuettuja luettelointeja ovat sovellusluetteloinnit, tietomalliluetteloinnit ja muotoluetteloinnit.)</span><span class="sxs-lookup"><span data-stu-id="25e83-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="25e83-134">Seuraavassa kuvassa **TransType**-tietolähde lisätään mallin yhdistämismääritykseen.</span><span class="sxs-lookup"><span data-stu-id="25e83-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="25e83-135">Tämä tietolähde viittaa **LedgerTransType**-sovellusluettelointiin.</span><span class="sxs-lookup"><span data-stu-id="25e83-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![Mallin yhdistämismäärityksen tietolähde, joka viittaa sovellusluettelointiin](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="25e83-137">Seuraavassa kuvassa on **TransTypeList**-tietolähde, joka määritetään mallin yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="25e83-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="25e83-138">Tämä tietolähde määritetään **TransType**-sovellusluetteloinnin perusteella.</span><span class="sxs-lookup"><span data-stu-id="25e83-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="25e83-139">`LISTOFFIELDS`-funktion avulla palautetaan kaikki luettelointiarvot kenttiä sisältävien tietueiden luettelona.</span><span class="sxs-lookup"><span data-stu-id="25e83-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="25e83-140">Näin jokaisen luettelointiarvon tiedot tulevat näkyviin.</span><span class="sxs-lookup"><span data-stu-id="25e83-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="25e83-141">**EnumValue**-kenttä määritetään **TransTypeList**-tietolähdettä varten käyttämällä lauseketta `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`.</span><span class="sxs-lookup"><span data-stu-id="25e83-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="25e83-142">Tämä kenttä palauttaa luettelointiarvon jokaiselle tämän luettelon tietueelle.</span><span class="sxs-lookup"><span data-stu-id="25e83-142">This field returns an enumeration value for every record in this list.</span></span>

![Valitun luetteloinnin kaikki luettelointiarvot tietueluettelona palauttavan mallin yhdistämismäärityksen tietolähde](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="25e83-144">Seuraavassa kuvassa on **VendTrans**-tietolähde, joka määritetään mallin yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="25e83-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="25e83-145">Tämä tietolähde palauttaa toimittajan tapahtumatietueita **VendTrans**-sovellustaulukosta.</span><span class="sxs-lookup"><span data-stu-id="25e83-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="25e83-146">Kunkin tapahtuman kirjanpitotyyppi määräytyy **TransType**-kentän arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="25e83-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="25e83-147">**TransTypeTitle**-kenttä määritetään **VendTrans**-tietolähdettä varten käyttämällä lauseketta `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`.</span><span class="sxs-lookup"><span data-stu-id="25e83-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="25e83-148">Tämä kenttä palauttaa nykyisen tapahtuman luettelointiarvon otsikon tekstinä, jos tämä luettelointiarvo on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="25e83-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="25e83-149">Muussa tapauksessa se palauttaa tyhjän merkkijonoarvon.</span><span class="sxs-lookup"><span data-stu-id="25e83-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="25e83-150">**TransTypeTitle**-kenttä on sidottu sellaisen tietomallin **LedgerType**-kenttään, joka mahdollistaa näiden tietojen käytön kaikissa ER-muodoissa, joissa tätä tietomallia käytetään tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="25e83-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![Toimittajatapahtumia palauttavan mallin yhdistämismäärityksen tietolähde](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="25e83-152">Seuraavassa kuvassa näkyy, miten voit käyttää [tietolähteen virheenkorjausta](er-debug-data-sources.md) määritetyn mallin yhdistämismäärityksen testaamiseen.</span><span class="sxs-lookup"><span data-stu-id="25e83-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![Määritetyn mallin yhdistämismärityksen testaaminen tietolähteen virheenkorjauksen avulla](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="25e83-154">Tietomallin **LedgerType** näyttää tapahtumatyyppien otsikkoja odotetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="25e83-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="25e83-155">Jos aiot käyttää tätä menetelmää suureen määrään tapahtumatietoja, sinun on otettava huomioon suorituksen suorituskyky.</span><span class="sxs-lookup"><span data-stu-id="25e83-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="25e83-156">Lisätietoja: [Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="25e83-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25e83-157">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="25e83-157">Additional resources</span></span>

[<span data-ttu-id="25e83-158">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="25e83-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="25e83-159">Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi</span><span class="sxs-lookup"><span data-stu-id="25e83-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="25e83-160">LISTOFFIELDS ER-funktio</span><span class="sxs-lookup"><span data-stu-id="25e83-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="25e83-161">FIRSTORNULL ER-funktio</span><span class="sxs-lookup"><span data-stu-id="25e83-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="25e83-162">WHERE ER-funktio</span><span class="sxs-lookup"><span data-stu-id="25e83-162">WHERE ER function</span></span>](er-functions-list-where.md)
