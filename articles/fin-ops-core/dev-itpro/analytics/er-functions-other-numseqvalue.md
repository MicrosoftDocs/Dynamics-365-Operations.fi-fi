---
title: NUMSEQVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NUMSEQVALUE-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 70e07fe429472b703f739baa09f700fb8970d34e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744020"
---
# <a name="numseqvalue-er-function"></a><span data-ttu-id="b1851-103">NUMSEQVALUE ER -funktio</span><span class="sxs-lookup"><span data-stu-id="b1851-103">NUMSEQVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1851-104">`NUMSEQVALUE`-funktio palauttaa *merkkijono*-arvon, joka edustaa numerosarjan uutta luotua arvoa määritetyn numerosarjan, laajuuden ja vaikutusalueen tunnuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="b1851-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="b1851-105">Aluetunnus on sama kuin yrityksen koodi, joka toimitetaan kontekstissa, jossa sähköisen raportoinnin (ER) muoto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="b1851-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b1851-106">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="b1851-106">Syntax 1</span></span>

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="b1851-107">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="b1851-107">Syntax 2</span></span>

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="b1851-108">Syntaksi 3</span><span class="sxs-lookup"><span data-stu-id="b1851-108">Syntax 3</span></span>

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="b1851-109">Argumentit</span><span class="sxs-lookup"><span data-stu-id="b1851-109">Arguments</span></span>

<span data-ttu-id="b1851-110">`number sequence code`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="b1851-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="b1851-111">Tekstiarvo, joka edustaa sen numerosarjan koodia, jossa uusi arvo vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="b1851-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="b1851-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="b1851-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="b1851-113">*Int64*-arvo, joka vastaa NumberSequenceTable-taulun tietueen tunnusta, joka sisältää sen numerosarjan määritelmän, jossa uusi arvo vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="b1851-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="b1851-114">`scope type`: *Enum-arvo*</span><span class="sxs-lookup"><span data-stu-id="b1851-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="b1851-115">**ERExpressionNumberSequenceScopeType**-luetteloinnin luettelointiarvo, joka määrittää sen numerosarjan laajuuden, jossa uusi arvo vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="b1851-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="b1851-116">Käytettävissä olevat aluetyypit ovat **Jaettu**, **Yritys**ja **Yhtiö**.</span><span class="sxs-lookup"><span data-stu-id="b1851-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="b1851-117">`scope ID`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="b1851-117">`scope ID`: *String*</span></span>

<span data-ttu-id="b1851-118">*Merkkijono*-arvo, joka määrittää vaikutusalueen määritetyn aluetyypin perusteella.</span><span class="sxs-lookup"><span data-stu-id="b1851-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="b1851-119">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="b1851-119">Return values</span></span>

<span data-ttu-id="b1851-120">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="b1851-120">*String*</span></span>

<span data-ttu-id="b1851-121">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="b1851-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b1851-122">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="b1851-122">Usage notes</span></span>

<span data-ttu-id="b1851-123">Määritä **Jaettu**-vaikutusalueen tyypille tyhjä merkkijono vaikutusalueen tunnuksena.</span><span class="sxs-lookup"><span data-stu-id="b1851-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="b1851-124">Määritä **Yhtiö**- ja **Yritys**-vaikutusalueen tyypin yhtiön koodi vaikutusalueen tunnuksena.</span><span class="sxs-lookup"><span data-stu-id="b1851-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="b1851-125">Jos määrität tyhjän merkkijonon vaikutusalueen tunnukseksi näille vaikutusaluetyypeille, käytetään nykyistä yritystunnusta.</span><span class="sxs-lookup"><span data-stu-id="b1851-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="b1851-126">Kun käytetään syntaksia 1, numerosarjaa pyydetään **yrityksen** aluetyypille, ja yrityksen koodin toimittaa konteksti, jossa ER-muoto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="b1851-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="b1851-127">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="b1851-127">Example 1</span></span>

<span data-ttu-id="b1851-128">ER-muodossa voit määrittää *käyttäjän syötteen parametri*-tyypin **AskNumSeq**-tietolähteen.</span><span class="sxs-lookup"><span data-stu-id="b1851-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="b1851-129">Tämä tietolähde viittaa **kuvauksen** laajennettuun tietotyyppiin (EDT).</span><span class="sxs-lookup"><span data-stu-id="b1851-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="b1851-130">Seuraavaksi määritetään **lasketun kenttätyypin** *numseq*-tietolähde.</span><span class="sxs-lookup"><span data-stu-id="b1851-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="b1851-131">Tässä tietolähteessä on lauseke `NUMSEQVALUE (AskNumSeq)`.</span><span class="sxs-lookup"><span data-stu-id="b1851-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="b1851-132">Kun **NumSeq**-tietolähdettä kutsutaan, se palauttaa suorituksen aikana määritetyn numerosarjan uuden luodun arvon syöttämällä sen koodin valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="b1851-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="b1851-133">Numerosarjaa pyydetään **yrityksen** vaikutusaluetyypille.</span><span class="sxs-lookup"><span data-stu-id="b1851-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="b1851-134">Yrityksen koodin toimittaa konteksti, jossa ER-muoto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="b1851-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="b1851-135">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="b1851-135">Example 2</span></span>

<span data-ttu-id="b1851-136">Seuraavat tietolähteet määritetään omassa mallimäärityksessäsi:</span><span class="sxs-lookup"><span data-stu-id="b1851-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="b1851-137">*Taulu*-tyypin **LedgerParms**-tietolähde.</span><span class="sxs-lookup"><span data-stu-id="b1851-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="b1851-138">Tämä tietolähde viittaa LedgerParameters-tauluun.</span><span class="sxs-lookup"><span data-stu-id="b1851-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="b1851-139">*Laskettu kenttä* -tyypin **NumSeq**-tietolähde.</span><span class="sxs-lookup"><span data-stu-id="b1851-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="b1851-140">Tässä tietolähteessä on lauseke `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span><span class="sxs-lookup"><span data-stu-id="b1851-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="b1851-141">Kun **NumSeq**-tietolähde kutsutaan, se palauttaa juuri luodun numerosarjan arvon. Tämä arvo määritettiin sen yrityksen kirjanpitoparametreissa, ja se antaa kontekstin, jossa ER-muoto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="b1851-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="b1851-142">Tämä numerosarja yksilöi kirjauskansiot ja toimii tapahtumat yhteen liittävänä eränumerona.</span><span class="sxs-lookup"><span data-stu-id="b1851-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="b1851-143">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="b1851-143">Example 3</span></span>

<span data-ttu-id="b1851-144">Seuraavat tietolähteet määritetään omassa mallimäärityksessäsi:</span><span class="sxs-lookup"><span data-stu-id="b1851-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="b1851-145">Microsoft Dynamics 365 Financen *luettelointi*-tyypin **enumScope**-tietolähde.</span><span class="sxs-lookup"><span data-stu-id="b1851-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="b1851-146">Tämä tietolähde viittaa **ERExpressionNumberSequenceScopeType**-luettelointiin.</span><span class="sxs-lookup"><span data-stu-id="b1851-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="b1851-147">*Laskettu kenttä* -tyypin **NumSeq**-tietolähde.</span><span class="sxs-lookup"><span data-stu-id="b1851-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="b1851-148">Tässä tietolähteessä on lauseke `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span><span class="sxs-lookup"><span data-stu-id="b1851-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="b1851-149">Kun **NumSeq**-tietolähde kutsutaan, se palauttaa juuri luodun **Gene\_1**-numerosarjan arvon. Tämä arvo määritettiin yritykselle, ja se antaa kontekstin, jossa ER-muoto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="b1851-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1851-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b1851-150">Additional resources</span></span>

[<span data-ttu-id="b1851-151">Muut (liiketoiminnan toimialuekohtaiset) toiminnot</span><span class="sxs-lookup"><span data-stu-id="b1851-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
