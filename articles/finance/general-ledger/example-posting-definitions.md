---
title: Kirjausmääritysesimerkkejä
description: Tässä artikkelissa on esimerkkejä, jotka osoittavat, miten kirjausmäärityksiä käytetään ostotilausten varauksiin ja budjettivarauksiin.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 301f15f1d7d8f0e10bbaf2546fcf727aff284624
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442655"
---
# <a name="posting-definition-examples"></a>Kirjausmääritysten esimerkkejä

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on esimerkkejä, jotka osoittavat, miten kirjausmäärityksiä käytetään ostotilausten varauksiin ja budjettivarauksiin.

Tutustu kirjausmäärityksiin ja tapahtuman kirjausmäärityksiin ennen tämän aiheen lukemista. Tietoja on aiheessa [Kirjausmääritykset](posting-definitions.md). Seuraavat esimerkit voidaan määrittää **Kirjausmääritykset**-sivulla. Kussakin esimerkissä on nämä skenaariot:

-   Kirjausmääritys – Vastaavuusehdot
-   Kirjausmääritys – Luodut merkinnät
-   Tapahtumat ja tilit, dimensioarvot ja määrät
-   Kirjausmäärityksestä luodut kirjanpitomerkinnät

Kun kirjausmäärityksen **Vastaavuusehdot**-ruudun tilien ja dimensioarvojen sekä tapahtuman tilien ja dimensioarvojen välillä on vastaavuus, kirjanpitomerkinnät luodaan kirjausmäärityksen **Luodut kirjaukset** -ruudun perusteella. 
> [!NOTE]
> Liitä kirjausmääritykset tapahtumatyyppeihin **Tapahtuman kirjausmääritykset** -sivulla. Kun kirjausmääritys on liitetty tapahtumatyyppiin ja **Kirjanpitoparametrit**-sivulla on valittu **Käytä kirjausmäärityksiä** -vaihtoehto, kaikki valitun tapahtumatyypin tapahtumien on käytettävä kirjausmäärityksiä.

## <a name="example-purchase-order-encumbrances"></a>Esimerkki: Ostotilauksen varaukset
Kun otat varauksen käsittelyyn käyttöön valitsemalla **Ota varausprosessi käyttöön** -vaihtoehdon **Kirjanpitoparametrit**-sivulta, varaukset on kirjattava kirjanpitoon kirjausmääritysten avulla kaikilla tileillä, joilla varaus on tehtävä. Useimmissa tapauksissa taseessa varataan kaikki kulutilit. 

Varausten kirjausmääritykset määritetään **Osto**-moduulissa **Kirjausmääritykset**-sivulla. Sen jälkeen voit valita **Tapahtuman kirjausmääritykset**-sivun **Osto**-alueesta **Ostotilaus**-tapahtumatyypin, jotta voit liittää kirjausmäärityksen ostotilauksiin. 

Kaikkien ostotilauksen varausten tositetapahtumien (eli debet- ja kredit-puolen) on täsmättävä tositteen kussakin yksilöllisessä dimensiossa.

### <a name="posting-definition--match-criteria"></a>Kirjausmääritys – Vastaavuusehdot

| Tilirakenne       | Vastaava tilinumero | Prioriteetti  |
|-------------------------|----------------------|----------|
| Tilirakenne – Tuloslaskelma | \*                   | 1        |

<em>**Vastaava tilinumero</em> -kentän tyhjä arvo* tarkoittaa, että kaikki määritetyn tilirakenteen vastaavat tilit kuuluvat täsmäytyssääntöön.

### <a name="posting-definition--generated-entries"></a>Kirjausmääritys – Luodut merkinnät

| Tilirakenne | Luotu tilinumero                    | Luotu debet/kredit |
|-------------------|---------------------------------------------|------------------------|
| Saldo           | 300143 - -(Varaustili)             | Sama                   |
| Saldo           | 300144 - -(Varaus varaustilille) | Tasapainottelu              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Tapahtumat ja tilit, dimensioarvot ja määrät

Tilit ja dimensioarvot tulevat joko ostotilausriville syötetyistä kirjanpidollisista jaoista tai tileistä ja dimensioista, jotka luodaan automaattisesti toimittajien, nimikkeiden, kategorioiden ja dimensiomallien perusteella.

| Tili + dimensiot           | Veloitus  | Hyvitys | Kommentti |
|--------------------------------|--------|--------|---------|
| 606400-OU\_1-OU\_3566-Koulutus | 250,00 |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Kirjausmäärityksestä luodut kirjanpitomerkinnät

Varausten kirjaamiseksi luodaan kirjanpitomerkinnät.

| Tili + dimensiot           | Veloitus  | Hyvitys | Kommentti |
|--------------------------------|--------|--------|---------|
| 300143-OU\_1-OU\_3566-Koulutus | 250,00 |        |         |
| 300144-OU\_1-OU\_3566-Koulutus |        | 250,00 |         |

Tässä esimerkissä kaikki Tilirakenne – Tuloslaskelma -skenaarioon kuuluvat tilit vastaavat kirjausmäärityksen ehtoja. Siten kun 606500-OU\_1-OU\_3566-Koulutus arvioidaan, kirjaukset luodaan kirjausmäärityksen **Luodut kirjaukset** -ruudussa määritellyille tileille.

## <a name="example-budget-appropriations"></a>Esimerkki: Budjettivaraukset
Kun otat budjettivarauksen käyttöön valitsemalla **Kirjanpitoparametrit**-sivulta **Ota käyttöön budjettivaraus** -vaihtoehdon, budjettitapahtumat on kirjattava kirjanpitoon käyttämällä kirjausmäärityksiä. Jos budjetin hallinnan konfiguraatio on aktiivinen ja otettu käyttöön, kirjausmäärityksillä ja tapahtumakirjauksen määrityksillä voidaan tukea varausten, tarkistusten, siirtojen, projektien, käyttöomaisuuden ja tarjonta- sekä kysyntäennusteiden tapahtumien kirjaamista kirjanpitoon. 

Jos haluat määrittää kirjausmäärityksen budjettitapahtumille, joiden budjettityyppi on **Alkuperäinen budjetti** ja joissa on varaukset käytössä, valitse **Kirjausmääritykset**-sivulta **Budjetti**-moduuli. Tämän jälkeen voit **Tapahtuman kirjausmääritykset** -sivun **Budjetti**-alueessa budjettikoodien avulla liittää kirjausmäärityksen budjettitapahtumiin, joiden budjettityyppi on **Alkuperäinen budjetti**. 

Kun budjettivarauksia ja kirjausmäärityksiä otetaan käyttöön, budjettitapahtumat kirjataan budjetin hallintaan ja kirjanpitoon.

### <a name="posting-definition--match-criteria"></a>Kirjausmääritys – Vastaavuusehdot

| Tilirakenne       | Vastaava tilinumero | Prioriteetti  |
|-------------------------|----------------------|----------|
| Tilirakenne – Tuloslaskelma | \*                   | 1        |

<em>**Vastaava tilinumero</em> -kentän tyhjä arvo* tarkoittaa, että kaikki määritetyn tilirakenteen vastaavat tilit kuuluvat täsmäytyssääntöön.

### <a name="posting-definition--generated-entries"></a>Kirjausmääritys – Luodut merkinnät

| Tilirakenne | Luotu tilinumero              | Luotu debet/kredit |
|-------------------|---------------------------------------|------------------------|
| Tilirakenne | 300145 - -(Arvioidun tuoton tili) | Sama                   |
| Tilirakenne | 300146 - -(Tilinpäätössiirtojen tili)     | Tasapainottelu              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Tapahtumat ja tilit, dimensioarvot ja määrät

Voit lisätä budjettitiliviennin tilit, dimensioarvot ja summat **Budjettitapahtuma**-sivulle.

| Tili + dimensiot           | Veloitus | Hyvitys | Kommentti |
|--------------------------------|-------|--------|---------|
| 606400-OU\_1-OU\_3566-Koulutus |       | 250,00 |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Kirjausmäärityksestä luodut kirjanpitomerkinnät

Kirjanpitotapahtumat luodaan, jotta alkuperäinen budjetti voidaan kirjata kuhunkin dimensioon.

| Tili + dimensiot           | Veloitus  | Hyvitys | Kommentti |
|--------------------------------|--------|--------|---------|
| 300145-OU\_1-OU\_3566-Koulutus |        | 250,00 |         |
| 300146-OU\_1-OU\_3566-Koulutus | 250,00 |        |         |

Tässä esimerkissä kaikki Tilirakenne – Tuloslaskelma -skenaarioon kuuluvat tilit vastaavat kirjausmäärityksen ehtoja. Niinpä kun 606400-OU\_1-OU\_3566-Koulutus arvioidaan, kirjanpitotapahtumat luodaan.





