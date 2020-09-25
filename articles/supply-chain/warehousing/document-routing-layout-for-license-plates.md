---
title: Rekisterikilven otsikoiden asiakirjareitityksen asettelu
description: Tässä aiheessa kuvataan, miten tarrojen arvot tulostetaan muotoilumenetelmien avulla.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 9af077022ab0759534d2c1da5f39997712e6a354
ms.sourcegitcommit: 965fa733be068dc37f482d02ebbcd77f2c3d0a45
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/03/2020
ms.locfileid: "3763452"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="558fe-103">Rekisterikilven otsikoiden asiakirjareitityksen asettelu</span><span class="sxs-lookup"><span data-stu-id="558fe-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="558fe-104">Tiedoston reititysasettelu määrittää rekisterikilpietikettien asettelun ja niihin tulostettavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="558fe-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="558fe-105">Voit määrittää tulostuksen käynnistyspisteet, kun määrität matkaviestimen valikkokohteita ja työmalleja.</span><span class="sxs-lookup"><span data-stu-id="558fe-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="558fe-106">Tyypillisessä skenaariossa varaston vastaanottajat tulostavat rekisterikilpitarrat heti, kun ne tallentavat vastaanottoalueelle saapuvien kuormalavojen sisällön.</span><span class="sxs-lookup"><span data-stu-id="558fe-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="558fe-107">Fyysisiä etikettejä käytetään kuormalavoihin.</span><span class="sxs-lookup"><span data-stu-id="558fe-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="558fe-108">Tämän jälkeen niitä voidaan käyttää oikeellisuustarkistuksessa osana seuraavaa lähtevien nimikkeiden hyllytysprosessia ja tulevia lähtevien nimikkeiden poimintatoimintoja.</span><span class="sxs-lookup"><span data-stu-id="558fe-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="558fe-109">Voit tulostaa erittäin monimutkaisia etikettejä, jos tulostuslaite pystyy tulkitsemaan sille lähetettävän tekstin.</span><span class="sxs-lookup"><span data-stu-id="558fe-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="558fe-110">Esimerkiksi viivakoodin sisältävä Zebra-ohjelmointikielen (ZPL) asettelu voi muistuttaa seuraavaa esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="558fe-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

<span data-ttu-id="558fe-111">Tämän esimerkin teksti `$LicensePlateId$` korvautuu data-arvolla osana etiketin tulostusprosessia.</span><span class="sxs-lookup"><span data-stu-id="558fe-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="558fe-112">Jos haluat nähdä tulostettavat arvot, siirry kohtaan **Varaston hallinta \> Kyselyt ja raportit \> Rekisterikilven tarrat**.</span><span class="sxs-lookup"><span data-stu-id="558fe-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="558fe-113">Useiden laajalti käytettävissä olevien etikettityökalujen avulla voit muotoilla etiketin asettelun tekstin.</span><span class="sxs-lookup"><span data-stu-id="558fe-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="558fe-114">Monet näistä työkaluista tukevat `$FieldName$`-muotoa.</span><span class="sxs-lookup"><span data-stu-id="558fe-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="558fe-115">Lisäksi Microsoft Dynamics 365 Supply Chain Management käyttää erityismuotoilulogiikkaa osana tiedoston reitityksen asettelun kenttien yhdistämismääritystä.</span><span class="sxs-lookup"><span data-stu-id="558fe-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="558fe-116">Mukautetut lukumuodot</span><span class="sxs-lookup"><span data-stu-id="558fe-116">Custom number formats</span></span>

<span data-ttu-id="558fe-117">Voit mukauttaa numeeristen kenttien arvojen muotoilua käyttämällä koodeja, joiden muoto on seuraava.</span><span class="sxs-lookup"><span data-stu-id="558fe-117">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="558fe-118">Selitys tästä muodosta:</span><span class="sxs-lookup"><span data-stu-id="558fe-118">Here is an explanation of this format:</span></span>

- <span data-ttu-id="558fe-119">`FieldName` on tietokentän nimi (esimerkiksi **Määrä**).</span><span class="sxs-lookup"><span data-stu-id="558fe-119">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="558fe-120">`FormatString` määrittää, miten tiedot on tarkoitus tulostaa.</span><span class="sxs-lookup"><span data-stu-id="558fe-120">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="558fe-121">Seuraavissa esimerkeissä näytetään, miten työmäärä- (**Määrä**)-kenttää voi mukauttaa:</span><span class="sxs-lookup"><span data-stu-id="558fe-121">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="558fe-122">Jos haluat näyttää aina neljä numeroa (käyttämällä paikkamerkkeinä nollia), käytä `$Qty:0000$`-toimintoa.</span><span class="sxs-lookup"><span data-stu-id="558fe-122">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="558fe-123">Jos määrä on esimerkiksi 10, otsikossa näkyy teksti "0010".</span><span class="sxs-lookup"><span data-stu-id="558fe-123">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="558fe-124">Jos haluat näyttää aina kaksi desimaalia, käytä `$Qty:0.00$`-kenttää.</span><span class="sxs-lookup"><span data-stu-id="558fe-124">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="558fe-125">Jos määrä on esimerkiksi 10, otsikossa näkyy teksti "10.00".</span><span class="sxs-lookup"><span data-stu-id="558fe-125">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="558fe-126">Täydellinen luettelo käytettävissä olevista numeromuotomerkkijonoista on kohdassa [Mukautetut numeeriset muotomerkkijonot](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="558fe-126">For a complete list of the available number format strings, see [Custom numeric format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="558fe-127">Mukautetut merkkijonomuodot</span><span class="sxs-lookup"><span data-stu-id="558fe-127">Custom string formats</span></span>

<span data-ttu-id="558fe-128">Voit poistaa merkkijonon ensimmäiset merkit seuraavan kentän ja muotoilukoodin avulla.</span><span class="sxs-lookup"><span data-stu-id="558fe-128">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="558fe-129">Tässä `#` määrittää ohitettavien merkkien määrän.</span><span class="sxs-lookup"><span data-stu-id="558fe-129">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="558fe-130">Jos esimerkiksi haluat tulostaa sarjatoimitusyksikkökoodin (SSCC) rekisterinumeron, joka ei sisällä kahta ensimmäistä merkkiä, käytä `$LicensePlateId:2..$`-tunnusta.</span><span class="sxs-lookup"><span data-stu-id="558fe-130">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="558fe-131">Tässä tapauksessa rekisterinumero 0011111111111222221 tulostetaan muodossa "11111111111222221".</span><span class="sxs-lookup"><span data-stu-id="558fe-131">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="558fe-132">Mukautetut päivämäärän ja ajan muodot</span><span class="sxs-lookup"><span data-stu-id="558fe-132">Custom date/time formats</span></span>

<span data-ttu-id="558fe-133">Seuraavassa esimerkissä näkyy, miten päivämäärien tulostukseen käytettävää muotoa voidaan ohjata.</span><span class="sxs-lookup"><span data-stu-id="558fe-133">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="558fe-134">Tässä esimerkissä päivämäärä, joka on 30. huhtikuuta 2020, näkyy muodossa "30-04-2020".</span><span class="sxs-lookup"><span data-stu-id="558fe-134">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="558fe-135">Täydellinen luettelo käytettävissä olevista päivä-/aikamuodoista on kohdassa [Mukautetut päivä-/aikamuotomerkkijonot](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="558fe-135">For a complete list of the available date/time formats, see [Custom date and time format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="558fe-136">Rivien tulostaminen monirivistä tiedoista</span><span class="sxs-lookup"><span data-stu-id="558fe-136">Print individual lines from multiline data</span></span>

<span data-ttu-id="558fe-137">Jos tietokenttä sisältää useita rivejä (rivejä, jotka on eroteltu rivinvaihtojen mukaan), voit tulostaa yksittäisen rivin käyttämällä seuraavaa muotoa.</span><span class="sxs-lookup"><span data-stu-id="558fe-137">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="558fe-138">Tässä `#` on rivinumero, jonka haluat tulostaa.</span><span class="sxs-lookup"><span data-stu-id="558fe-138">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="558fe-139">(Käytä numeroa 1 ensimmäiselle riville.)</span><span class="sxs-lookup"><span data-stu-id="558fe-139">(Use 1 for the first line.)</span></span>

<span data-ttu-id="558fe-140">Järjestelmässä on esimerkiksi `AdditionalAddress`-kenttä, johon on tallennettu seuraava moniriviosoite:</span><span class="sxs-lookup"><span data-stu-id="558fe-140">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="558fe-141">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="558fe-141">Contoso Inc.</span></span>  
<span data-ttu-id="558fe-142">123 Kadunnimi</span><span class="sxs-lookup"><span data-stu-id="558fe-142">123 Street Name</span></span>  
<span data-ttu-id="558fe-143">Joku kaupunki, joku osavaltio</span><span class="sxs-lookup"><span data-stu-id="558fe-143">Some City, Some State</span></span>

<span data-ttu-id="558fe-144">Voit tulostaa tämän osoitteen yksi rivin kerrallaan, käyttämällä seuraavia koodeja.</span><span class="sxs-lookup"><span data-stu-id="558fe-144">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="558fe-145">Koodi</span><span class="sxs-lookup"><span data-stu-id="558fe-145">Code</span></span> | <span data-ttu-id="558fe-146">Teksti, joka on tulostettu</span><span class="sxs-lookup"><span data-stu-id="558fe-146">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="558fe-147">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="558fe-147">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="558fe-148">123 Kadunnimi</span><span class="sxs-lookup"><span data-stu-id="558fe-148">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="558fe-149">Joku kaupunki, joku osavaltio</span><span class="sxs-lookup"><span data-stu-id="558fe-149">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="558fe-150">Tulostaminen ja muotoileminen näyttötavasta</span><span class="sxs-lookup"><span data-stu-id="558fe-150">Print and format from a display method</span></span>

<span data-ttu-id="558fe-151">Voit tulostaa näyttötavasta käyttämällä seuraavaa muotoa.</span><span class="sxs-lookup"><span data-stu-id="558fe-151">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="558fe-152">Voit yhdistää tämän muodon muihin tässä ohjeaiheessa aiemmin kuvattuihin tyyppeihin.</span><span class="sxs-lookup"><span data-stu-id="558fe-152">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="558fe-153">Sinulla on esimerkiksi näyttötapa, jonka nimi on `DisplayListOfItemsNumbers()` ja haluat tulostaa tämän menetelmän ensimmäisen nimiketunnuksen.</span><span class="sxs-lookup"><span data-stu-id="558fe-153">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="558fe-154">Voit käyttää tässä tapauksessa seuraavaa koodia.</span><span class="sxs-lookup"><span data-stu-id="558fe-154">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="558fe-155">Lisätietoja tarrojen tulostamisesta</span><span class="sxs-lookup"><span data-stu-id="558fe-155">More information about how to print labels</span></span>

<span data-ttu-id="558fe-156">Lisätietoja etikettien määrittämisestä ja tulostamisesta on kohdassa [Rekisterikilven tarratulostuksen ottaminen käyttöön](tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="558fe-156">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>
