---
title: FORMAT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) FORMAT-funktiota käytetään.
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
ms.openlocfilehash: 3f3e8e5f6676c26b8d604ed950470463f04c0473
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743876"
---
# <a name="format-er-function"></a><span data-ttu-id="a7c03-103">FORMAT ER-funktio</span><span class="sxs-lookup"><span data-stu-id="a7c03-103">FORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7c03-104">`FORMAT`-funktio palauttaa määritetyn *Merkkijono*-arvon sen jälkeen, kun se on muotoiltu korvaamalla kaikki **%N**-esiintymät *N*:llä argumentilla.</span><span class="sxs-lookup"><span data-stu-id="a7c03-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7c03-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="a7c03-105">Syntax</span></span>

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="a7c03-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="a7c03-106">Arguments</span></span>

<span data-ttu-id="a7c03-107">`string`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="a7c03-107">`string`: *String*</span></span>

<span data-ttu-id="a7c03-108">Viittaus *Merkkijono*-tyypin tietolähteeseen, joka on muotoiltava.</span><span class="sxs-lookup"><span data-stu-id="a7c03-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="a7c03-109">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="a7c03-109">This argument is required.</span></span>

<span data-ttu-id="a7c03-110">`argument 1`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="a7c03-110">`argument 1`: *String*</span></span>

<span data-ttu-id="a7c03-111">Ensimmäinen argumentti, jota käytetään korvaamaan **%1** -esiintymät.</span><span class="sxs-lookup"><span data-stu-id="a7c03-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="a7c03-112">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="a7c03-112">This argument is required.</span></span>

<span data-ttu-id="a7c03-113">`argument N`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="a7c03-113">`argument N`: *String*</span></span>

<span data-ttu-id="a7c03-114">Argumentti numero *N*, jota käytetään korvaamaan **%2**, **%3**, jne. -esiintymät.</span><span class="sxs-lookup"><span data-stu-id="a7c03-114">The *N*th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="a7c03-115">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="a7c03-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="a7c03-116">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="a7c03-116">Return values</span></span>

<span data-ttu-id="a7c03-117">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="a7c03-117">*String*</span></span>

<span data-ttu-id="a7c03-118">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="a7c03-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a7c03-119">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="a7c03-119">Usage notes</span></span>

<span data-ttu-id="a7c03-120">Jos parametrille ei ole annettu argumenttia, parametri palautetaan merkkijonoon arvona **"%N"**.</span><span class="sxs-lookup"><span data-stu-id="a7c03-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="a7c03-121">*Todellinen*-tyyppisten arvojen oletusmerkkijonon muunnos on rajoitettu kahteen desimaaliin.</span><span class="sxs-lookup"><span data-stu-id="a7c03-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="a7c03-122">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="a7c03-122">Example</span></span>

<span data-ttu-id="a7c03-123">Seuraavassa kuvassa **PaymentModel**-tietolähde palauttaa asiakastietueiden luettelon **Asiakas**-komponentin avulla.</span><span class="sxs-lookup"><span data-stu-id="a7c03-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="a7c03-124">Se palauttaa käsittelypäivämäärän arvon **ProcessingDate**-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="a7c03-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="a7c03-125">Sähköinen raportointi (ER) -muodossa, joka on suunniteltu sähköisen tiedoston luomiseen valituille asiakkaille, tietolähteeksi valitaan **PaymentModel** ja se ohjaa prosessin kulkua.</span><span class="sxs-lookup"><span data-stu-id="a7c03-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="a7c03-126">Jos valittu asiakas pysäytetään raportin käsittelypäivämääränä, poikkeus heitetään ilmoituksesi käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="a7c03-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="a7c03-127">Tälle käsittelyn ohjausobjektin tyypille muotoiltua kaavaa käytetään seuraavissa resursseissa:</span><span class="sxs-lookup"><span data-stu-id="a7c03-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="a7c03-128">Otsikko SYS70894, jolla on seuraava teksti:</span><span class="sxs-lookup"><span data-stu-id="a7c03-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="a7c03-129">**Kielelle EN-US:** "Nothing to print"</span><span class="sxs-lookup"><span data-stu-id="a7c03-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="a7c03-130">**Kielelle FI:** "Ei mitään tulostettavaa"</span><span class="sxs-lookup"><span data-stu-id="a7c03-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="a7c03-131">Otsikko SYS18389, jolla on seuraava teksti:</span><span class="sxs-lookup"><span data-stu-id="a7c03-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="a7c03-132">**Kielelle FI-FI**: Asiakas %1 on pysäytetty kohdassa %2.</span><span class="sxs-lookup"><span data-stu-id="a7c03-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="a7c03-133">**Kielelle DE:** "Debitor '%1' wird für %2 gesperrt."</span><span class="sxs-lookup"><span data-stu-id="a7c03-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="a7c03-134">Tässä on lauseke, jota voi muotoilla.</span><span class="sxs-lookup"><span data-stu-id="a7c03-134">Here is the expression that can be designed.</span></span>

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="a7c03-135">Jos raporttia käsitellään asiakkaalle **Litware Retail** 17.12.2015 ja maa-asetuksina on **EN-US** ja kielenä on **EN-US**, tämä kaava palauttaa seuraavan tekstin, joka voidaan esittää poikkeussanomana käyttäjälle:</span><span class="sxs-lookup"><span data-stu-id="a7c03-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="a7c03-136">*Ei tulostettavaa. Asiakas Litware Retail on pysäytetty 17/12/2015.*</span><span class="sxs-lookup"><span data-stu-id="a7c03-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="a7c03-137">Jos sama raportti käsitellään asiakkaalle **Litware Retail** 17.12.2015 ja maa-asetuksina on **FI** ja kielenä on **FI**, tämä kaava palauttaa seuraavan tekstin, jossa on eri päivämäärämuoto:</span><span class="sxs-lookup"><span data-stu-id="a7c03-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="a7c03-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span><span class="sxs-lookup"><span data-stu-id="a7c03-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="a7c03-139">Otsikoiden ER-kaavoissa käytetään seuraavaa syntaksia:</span><span class="sxs-lookup"><span data-stu-id="a7c03-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="a7c03-140">**Etikettejä varten Microsoft  Dynamics 365 Finance -sovelluksen resursseista**: **\@X**, jossa **X** on sovellusobjektipuun (AOT) etikettitunnus</span><span class="sxs-lookup"><span data-stu-id="a7c03-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **\@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="a7c03-141">**ER-määrityksissä sijaitsevat otsikot:** **@"GER_LABEL:X"**, jossa **X** on ER-määrityksen otsikon tunnus</span><span class="sxs-lookup"><span data-stu-id="a7c03-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a7c03-142">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a7c03-142">Additional resources</span></span>

[<span data-ttu-id="a7c03-143">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="a7c03-143">Text functions</span></span>](er-functions-category-text.md)
