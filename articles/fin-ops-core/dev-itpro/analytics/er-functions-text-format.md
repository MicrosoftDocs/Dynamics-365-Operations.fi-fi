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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b347a7209ee543f6bd687c2864203eb632d6a4a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688410"
---
# <a name="format-er-function"></a>FORMAT ER-funktio

[!include [banner](../includes/banner.md)]

`FORMAT`-funktio palauttaa määritetyn *Merkkijono*-arvon sen jälkeen, kun se on muotoiltu korvaamalla kaikki **%N**-esiintymät *N*:llä argumentilla.

## <a name="syntax"></a>Syntaksi

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>Argumentit

`string`: *Merkkijono*

Viittaus *Merkkijono*-tyypin tietolähteeseen, joka on muotoiltava. Tämä argumentti on pakollinen.

`argument 1`: *Merkkijono*

Ensimmäinen argumentti, jota käytetään korvaamaan **%1** -esiintymät. Tämä argumentti on pakollinen.

`argument N`: *Merkkijono*

Argumentti numero *N*, jota käytetään korvaamaan **%2**, **%3**, jne. -esiintymät. Nämä lisäargumentit ovat valinnaisia.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Jos parametrille ei ole annettu argumenttia, parametri palautetaan merkkijonoon arvona **"%N"**. *Todellinen*-tyyppisten arvojen oletusmerkkijonon muunnos on rajoitettu kahteen desimaaliin.

## <a name="example"></a>Esimerkki

Seuraavassa kuvassa **PaymentModel**-tietolähde palauttaa asiakastietueiden luettelon **Asiakas**-komponentin avulla. Se palauttaa käsittelypäivämäärän arvon **ProcessingDate**-kentän avulla.

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

Sähköinen raportointi (ER) -muodossa, joka on suunniteltu sähköisen tiedoston luomiseen valituille asiakkaille, tietolähteeksi valitaan **PaymentModel** ja se ohjaa prosessin kulkua. Jos valittu asiakas pysäytetään raportin käsittelypäivämääränä, poikkeus heitetään ilmoituksesi käyttäjälle. Tälle käsittelyn ohjausobjektin tyypille muotoiltua kaavaa käytetään seuraavissa resursseissa:

- Otsikko SYS70894, jolla on seuraava teksti:

    - **Kielelle EN-US:** "Nothing to print"
    - **Kielelle FI:** "Ei mitään tulostettavaa"

- Otsikko SYS18389, jolla on seuraava teksti:

    - **Kielelle FI-FI**: Asiakas %1 on pysäytetty kohdassa %2.
    - **Kielelle DE:** "Debitor '%1' wird für %2 gesperrt."

Tässä on lauseke, jota voi muotoilla.

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

Jos raporttia käsitellään asiakkaalle **Litware Retail** 17.12.2015 ja maa-asetuksina on **EN-US** ja kielenä on **EN-US**, tämä kaava palauttaa seuraavan tekstin, joka voidaan esittää poikkeussanomana käyttäjälle:

*Ei tulostettavaa. Asiakas Litware Retail on pysäytetty 17/12/2015.*

Jos sama raportti käsitellään asiakkaalle **Litware Retail** 17.12.2015 ja maa-asetuksina on **FI** ja kielenä on **FI**, tämä kaava palauttaa seuraavan tekstin, jossa on eri päivämäärämuoto:

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> Otsikoiden ER-kaavoissa käytetään seuraavaa syntaksia:
>
> - **Etikettejä varten Microsoft  Dynamics 365 Finance -sovelluksen resursseista**: **\@X**, jossa **X** on sovellusobjektipuun (AOT) etikettitunnus
> - **ER-määrityksissä sijaitsevat otsikot:** **@"GER_LABEL:X"**, jossa **X** on ER-määrityksen otsikon tunnus

## <a name="additional-resources"></a>Lisäresurssit

[Tekstitoiminnot](er-functions-category-text.md)
