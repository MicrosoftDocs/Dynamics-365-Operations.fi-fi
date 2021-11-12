---
title: ER-funktio CHANGETIMEZONE
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CHANGETIMEZONE-funktiota käytetään.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 48e96cfbc19503daf6a20363c4520c765f11a249
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647931"
---
# <a name="changetimezone-er-function"></a>ER-funktio CHANGETIMEZONE

[!include [banner](../includes/banner.md)]

`CHANGETIMEZONE`-funktio palauttaa *[DateTime](er-formula-supported-data-types-primitive.md#datetime)*-arvon koordinoidussa yleisajassa (Greenwichin ajassa \[GMT\]), joka muunnetaan tietystä päivämäärä/aika-arvosta yhdellä aikavyöhykkeellä päivämäärä/aika-arvoksi toisella aikavyöhykkeellä.

## <a name="syntax"></a>Syntaksi

```vb
CHANGETIMEZONE (datetime, base time zone, target time zone)
```

## <a name="arguments"></a>Argumentit

`datetime`: *DateTime*

Päivämäärä/aika-arvo koordinoidun yleisajan aikavyöhykkeellä, joka edustaa muunnettavaa päivämäärä/aika-arvoa.

`base time zone`: *[Merkkijono](er-formula-supported-data-types-primitive.md#string)*

Sen aikavyöhykkeen nimi, johon kulloinenkin päivämäärä/aika-arvo siirretään ennen muuntamista.

`target time zone`: *Merkkijono*

Sen aikavyöhykkeen nimi, johon muunnettu päivämäärä/aika-arvo siirretään muuntamisen aikana.

## <a name="return-values"></a>Palautusarvot

*Päivämäärä ja aika*

Tuloksena oleva päivämäärä/aika-arvo koordinoidun yleisajan aikavyöhykkeellä.

## <a name="usage-notes"></a>Käyttöhuomautukset

Lähde- ja kohdeaikavyöhykkeiden määritykseen voi käyttää [Internet Assigned Numbers Authorityn (IANA)](https://www.iana.org/) [tarjoamia](https://data.iana.org/time-zones/releases/) tai Microsoft Windowsin [tukemia](/windows-hardware/manufacture/desktop/default-time-zones) aikavyöhykkeiden nimiä.

Suorituksen aikana ilmenee poikkeus Aikavyöhykettä \<time zone name\> ei ole olemassa, jos annettu nimi ei ole IANA:n luettelossa tai Windowsin rekisterissä.

Niiden aikavyöhykkeiden osalta, joissa käytetään kesäaikaa, muuntamisessa otetaan huomioon koordinoidun yleisajan kesäaikapoikkeama. Muuntamisessa käytetään viimeisimpiä tätä poikkeamaa koskevia tietoja.

## <a name="example-1"></a>Esimerkki 1

Tässä esimerkissä käytetään Windowsin aikavyöhykenimiä.

Määrität **Laskettu kenttä** -tyypin **DSX**-tietolähteen. Se sisältää seuraavan lausekkeen:

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "E. Europe Standard Time", "Hawaiian Standard Time"), "O")
)
```

Jos määrität **Laskettu kenttä** -tyypin **DSY**-tietolähteen arvoksi `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX**-tietolähde palauttaa tekstin **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Tämä teksti ilmaisee, että kahden annetun aikavyöhykkeen välinen aikaero 1. kesäkuuta on yli 24 tuntia. Näin ollen muunnettu päivämäärä/aika-arvo on yhden päivän aikaisempi kuin annettu päivämäärä/aika-arvo, koska perusaikavyöhyke on kohdeaikavyöhykettä edellä.

Jos määrität **Laskettu kenttä** -tyypin **DSY**-tietolähteen arvoksi `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX**-tietolähde palauttaa tekstin **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Tämä teksti ilmaisee, että kahden annetun aikavyöhykkeen välinen aikaero 1. joulukuuta on alle 24 tuntia. Näin ollen muunnettu päivämäärä/aika-arvo vastaa annettua päivämäärä/aika-arvoa.

> [!NOTE]
> Sama lauseke palauttaa eri varianssin annetun ja muunnetun päivämäärä/aika-arvon välillä saman aikavyöhykeparin osalta, koska kyseisillä aikavyöhykkeillä noudetaan eri koordinoidun yleisajan kesäaikapoikkeamaa tiettynä päivänä/aikana.

## <a name="example-2"></a>Esimerkki 2

Tässä esimerkissä käytetään IANA:n aikavyöhykenimiä.

Määrität **Laskettu kenttä** -tyypin **DSX**-tietolähteen. Se sisältää seuraavan lausekkeen:

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "Europe/Athens", "US/Hawaii"), "O")
)
```

Jos määrität **Laskettu kenttä** -tyypin **DSY**-tietolähteen arvoksi `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX**-tietolähde palauttaa tekstin **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Tämä teksti ilmaisee, että kahden annetun aikavyöhykkeen välinen aikaero 1. kesäkuuta on yli 24 tuntia. Näin ollen muunnettu päivämäärä/aika-arvo on yhden päivän aikaisempi kuin annettu päivämäärä/aika-arvo, koska perusaikavyöhyke on kohdeaikavyöhykettä edellä.

Jos määrität **Laskettu kenttä** -tyypin **DSY**-tietolähteen arvoksi `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX**-tietolähde palauttaa tekstin **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Tämä teksti ilmaisee, että kahden annetun aikavyöhykkeen välinen aikaero 1. joulukuuta on alle 24 tuntia. Näin ollen muunnettu päivämäärä/aika-arvo vastaa annettua päivämäärä/aika-arvoa.

## <a name="example-3"></a>Esimerkki 3

Määrität **Laskettu kenttä** -tyypin **DSX**-tietolähteen. Se sisältää seuraavan lausekkeen:

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "US/Hawaii", "Europe/Athens"), "O")
)
```

Jos määrität **Laskettu kenttä** -tyypin **DSY**-tietolähteen arvoksi `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX**-tietolähde palauttaa tekstin **2021-06-01T12:55:00.0000000+00:00 -> 2021-06-02T01:55:00.0000000+00:00'**. Tämä teksti ilmaisee, että kahden annetun aikavyöhykkeen välinen aikaero 1. kesäkuuta on yli 24 tuntia. Näin ollen muunnettu päivämäärä/aika-arvo on yhden päivän myöhempi kuin annettu päivämäärä/aika-arvo, koska kohdeaikavyöhyke on perusaikavyöhykettä edellä.

## <a name="example-4"></a>Esimerkki 4

Saatat saada ulkoisesta lähteestä päivämäärä/aika-leiman tekstinä, joka ei sisällä aikavyöhyketietoja. Saatat kuitenkin tietää aikavyöhykkeen, jolla lähdettä ylläpidetään. Voit esimerkiksi saada päivä/aika-leiman **01/12/2021 12:55:00** palvelulta, jota ylläpidetään Espanjassa. Tämän päivämäärä/aika-arvon virheetön tallennus tietokantaan edellyttää seuraavaa muunnosta:

- Määritä **Laskettu kenttä** -tyypin **DSY**-tietolähde muuntamaan päivämäärä/aika-leima tekstistä koordinoidun yleisajan päivämäärä/aika-arvoksi.

    `DATETIMEVALUE ("01/12/2021 12:55:00", "dd/MM/yyyy HH:mm:ss", "ES")`

- Määritä **Laskettu kenttä** -tyypin **DSX**-tietolähde vaihtamaan muunnettu päivämäärä/aika-arvo koordinoituun yleisaikaan ulkoisen lähteen aikavyöhykkeen päivämäärä/aika-arvoksi.

    `CHANGETIMEZONE(DSY, "Romance Standard Time", "GMT Standard Time")`

> [!NOTE]
> Kun käytät `CHANGETIMEZONE`-funktiota päivämäärä/aika-muunnokseen, ota huomioon, että mikä tahansa päivämäärä/aika-arvo tallennetaan tietokantaan koordinoidun yleisajan aikavyöhykkeen mukaisena arvona. Ennen kuin tämä arvo voidaan esittää sovellussivuilla, se muunnetaan. Muunnoksessa otetaan huomioon aikavyöhyke joka on [määritetty](../../fin-ops/organization-administration/tasks/set-users-preferred-time-zone.md) kulloinkin kirjautuneena olevan sovelluksen käyttäjän ensisijaisesi aikavyöhykkeeksi.

## <a name="additional-resources"></a>Lisäresurssit

[Päivämäärä- ja aikatoiminnot](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
