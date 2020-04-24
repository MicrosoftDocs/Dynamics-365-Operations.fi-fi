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
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 62d4301f9dbe301c2a2573102d911a8d0ec58eb0
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261323"
---
# <a name="document-routing-layout-for-license-plate-labels"></a>Rekisterikilven otsikoiden asiakirjareitityksen asettelu

[!include [banner](../includes/banner.md)]

Tiedoston reititysasettelu määrittää rekisterikilpietikettien asettelun ja niihin tulostettavat tiedot. Voit määrittää tulostuksen käynnistyspisteet, kun määrität matkaviestimen valikkokohteita ja työmalleja.

Tyypillisessä skenaariossa varaston vastaanottajat tulostavat rekisterikilpitarrat heti, kun ne tallentavat vastaanottoalueelle saapuvien kuormalavojen sisällön. Fyysisiä etikettejä käytetään kuormalavoihin. Tämän jälkeen niitä voidaan käyttää oikeellisuustarkistuksessa osana seuraavaa lähtevien nimikkeiden hyllytysprosessia ja tulevia lähtevien nimikkeiden poimintatoimintoja.

Voit tulostaa erittäin monimutkaisia etikettejä, jos tulostuslaite pystyy tulkitsemaan sille lähetettävän tekstin. Esimerkiksi viivakoodin sisältävä Zebra-ohjelmointikielen (ZPL) asettelu voi muistuttaa seuraavaa esimerkkiä.

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

Tämän esimerkin teksti `$LicensePlateId$` korvautuu data-arvolla osana etiketin tulostusprosessia.

Jos haluat nähdä tulostettavat arvot, siirry kohtaan **Varaston hallinta \> Kyselyt ja raportit \> Rekisterikilven tarrat**.

Useiden laajalti käytettävissä olevien etikettityökalujen avulla voit muotoilla etiketin asettelun tekstin. Monet näistä työkaluista tukevat `$FieldName$`-muotoa. Lisäksi Microsoft Dynamics 365 Supply Chain Management käyttää erityismuotoilulogiikkaa osana tiedoston reitityksen asettelun kenttien yhdistämismääritystä.

## <a name="custom-number-formats"></a>Mukautetut lukumuodot

Voit mukauttaa numeeristen kenttien arvojen muotoilua käyttämällä koodeja, joiden muoto on seuraava.

```dos
$FieldName:FormatString$
```

Selitys tästä muodosta:

- `FieldName` on tietokentän nimi (esimerkiksi **Määrä**).
- `FormatString` määrittää, miten tiedot on tarkoitus tulostaa.

Seuraavissa esimerkeissä näytetään, miten työmäärä- (**Määrä**)-kenttää voi mukauttaa:

- Jos haluat näyttää aina neljä numeroa (käyttämällä paikkamerkkeinä nollia), käytä `$Qty:0000$`-toimintoa. Jos määrä on esimerkiksi 10, otsikossa näkyy teksti "0010".
- Jos haluat näyttää aina kaksi desimaalia, käytä `$Qty:0.00$`-kenttää. Jos määrä on esimerkiksi 10, otsikossa näkyy teksti "10.00".

Täydellinen luettelo käytettävissä olevista numeromuotomerkkijonoista on kohdassa [Mukautetut numeeriset muotomerkkijonot](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="custom-string-formats"></a>Mukautetut merkkijonomuodot

Voit poistaa merkkijonon ensimmäiset merkit seuraavan kentän ja muotoilukoodin avulla.

```dos
$FieldName:#..$
```

Tässä `#` määrittää ohitettavien merkkien määrän. Jos esimerkiksi haluat tulostaa sarjatoimitusyksikkökoodin (SSCC) rekisterinumeron, joka ei sisällä kahta ensimmäistä merkkiä, käytä `$LicensePlateId:2..$`-tunnusta. Tässä tapauksessa rekisterinumero 0011111111111222221 tulostetaan muodossa "11111111111222221".

## <a name="custom-datetime-formats"></a>Mukautetut päivämäärän ja ajan muodot

Seuraavassa esimerkissä näkyy, miten päivämäärien tulostukseen käytettävää muotoa voidaan ohjata.

```dos
$PrintedDate:dd-MM-yyyy$
```

Tässä esimerkissä päivämäärä, joka on 30. huhtikuuta 2020, näkyy muodossa "30-04-2020".

Täydellinen luettelo käytettävissä olevista päivä-/aikamuodoista on kohdassa [Mukautetut päivä-/aikamuotomerkkijonot](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="print-individual-lines-from-multiline-data"></a>Rivien tulostaminen monirivistä tiedoista

Jos tietokenttä sisältää useita rivejä (rivejä, jotka on eroteltu rivinvaihtojen mukaan), voit tulostaa yksittäisen rivin käyttämällä seuraavaa muotoa.

```dos
$FieldName[#]$
```

Tässä `#` on rivinumero, jonka haluat tulostaa. (Käytä numeroa 1 ensimmäiselle riville.)

Järjestelmässä on esimerkiksi `AdditionalAddress`-kenttä, johon on tallennettu seuraava moniriviosoite:

Contoso Inc.  
123 Kadunnimi  
Joku kaupunki, joku osavaltio

Voit tulostaa tämän osoitteen yksi rivin kerrallaan, käyttämällä seuraavia koodeja.

| Koodi | Teksti, joka on tulostettu |
|---|---|
| `$AdditionalAddress[1]$` | Contoso Inc. |
| `$AdditionalAddress[2]$` | 123 Kadunnimi |
| `$AdditionalAddress[3]$` | Joku kaupunki, joku osavaltio |

## <a name="print-and-format-from-a-display-method"></a>Tulostaminen ja muotoileminen näyttötavasta

Voit tulostaa näyttötavasta käyttämällä seuraavaa muotoa.

```dos
$DisplayMethod()$
```

Voit yhdistää tämän muodon muihin tässä ohjeaiheessa aiemmin kuvattuihin tyyppeihin. Sinulla on esimerkiksi näyttötapa, jonka nimi on `DisplayListOfItemsNumbers()` ja haluat tulostaa tämän menetelmän ensimmäisen nimiketunnuksen. Voit käyttää tässä tapauksessa seuraavaa koodia.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Lisätietoja tarrojen tulostamisesta

Lisätietoja etikettien määrittämisestä ja tulostamisesta on kohdassa [Rekisterikilven tarratulostuksen ottaminen käyttöön](tasks/license-plate-label-printing.md).
