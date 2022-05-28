---
title: Tiedostojen ja tositteiden numeroiminen aikajärjestyksessä
description: Tässä aiheessa kerrotaan, miten sovellettavissa asiakirjoissa ja niihin liittyvissä tositteissa määritetään ja käytetään aikajärjestyksessä olevia numeroita.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0ce1afdbd31a78611e6b51dd93f7159d684c97cb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692670"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a>Tiedostojen ja tositteiden numeroiminen aikajärjestyksessä

[!include [banner](../includes/banner.md)]


Joissakin maissa asiakirjojen ja niihin liittyvien tositteiden numeroinnissa on lakisääteinen vaatimus aikajärjestyksestä. Kausien on tuettava aikajärjestystä. Kaikkien aiempien kausien numeroiden on oltava pienempiä kuin myöhempiin kausiin kuuluvat numerot. Tämän vaatimuksen täyttämiseksi on toteutettu aikajärjestyksessä numeroinnin toiminto. Tässä aiheessa kerrotaan, miten sovellettavissa asiakirjoissa ja niihin liittyvissä tositteissa määritetään ja käytetään aikajärjestyksessä olevia numeroita.

## <a name="prerequisites"></a>Edellytykset

Ota Ominaisuuksien hallinta -työtilassa käyttöön **Kronologinen numerointi** -ominaisuus. Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-chronological-numbering"></a>Aikajärjestyksessä numeroimisen konfiguroiminen

Aikajärjestyksessä numeroiminen vaikuttaa seuraaviin asiakirjoihin.

**Myyntireskontra**
- Myyntilasku
- Asiakkaan laskutosite
- Myynnin hyvityslasku
- Myynnin hyvityslaskutosite
- Vapaatekstilasku
- Vapaamuotoinen laskutosite
- Vapaamuotoinen hyvityslasku
- Vapaamuotoinen hyvityslaskutosite
- Pakkausluettelo
- Pakkausluettelon tosite
- Pakkausluettelon korjaustosite
- Korkolaskutosite
- Maksukehotustosite

**Ostoreskontra**
- Laskutustosite
- Hyvityslaskutosite
- Tuotteen vastaanoton tosite

**Projektinhallinta**
- Lasku
- Laskutustosite
- Hyvityslasku
- Hyvityslaskutosite 

### <a name="define-number-sequences"></a>Numerosarjojen määrittäminen

Voit määrittää numerosarjat kohdassa **Organisaation hallinta** > **Numerosarjat** > **Numerosarjat**. Voit määrittää tarvittavan määrän numerosarjoja, jotka kattavat tarvittavien asiakirjojen kaudet. 

Määritä kullekin numerosarjalle yritys. Numerosarjojen segmentit on määritettävä niin, että ne antavat kausien aikajärjestyksen. Segmenttien nimet voivat esimerkiksi sisältää erityisen etuliitteen, joka yksilöi tietyn kauden.

![Numerosarjojen määritys.](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a>Numerosarjaryhmien määrittäminen

Voit määrittää numerosarjaryhmiä kohdassa **Myyntireskontra** > **Määritys** > **Myyntireskontran parametrit**. Määritä **Numerosarjat**-välilehdessä niin monta numerosarjaryhmää kuin on tarpeen tarvittavien kausien kattamiseksi. 

Valitse kullekin ryhmälle **Viite**-osasta jokin tuetuista tiedostoviitteistä ja viittaa **Numerosarjan koodi** -kentässä numerosarjaan, joka oli aiemmin luotu kyseiselle jaksolle.

![Numerosarjaryhmän määritys.](media/chrono-num-sequence-group.jpg)

Konfiguroi numerosarjaryhmät samalla tavalla **Ostoreskontra**- ja **Projektinhallinta ja kirjanpito** -moduuleissa.

### <a name="configure-number-sequence-groups-chronology"></a>Numerosarjaryhmien kronologian määrittäminen

Voit määrittää numerosarjaryhmien kronologian kohdassa **Organisaation hallinto** > **Numerosarjat** > **Kronologiset numerosarjaryhmät**. Määritä numerosarjaryhmien käytettävyysehdot.

![Kronologisten numeroiden asetukset.](media/chrono-num-sequence-group-period.jpg)

| Kenttä            | kuvaus                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Voimassa  | Numerosarjaryhmän käytettävyyden alkamispäivä. |
| Vanhentumisaika      | Numerosarjaryhmän käytettävyyden päättymispäivä. Jos päättymispäivää ei käytetä, valitse **Ei koskaan**. |
| Numerosarjaryhmä | Numerosarjaryhmä, jota käytetään asiakirjan numeroiden tuottamiseen kauden aikana. |
| Alkuperäinen numerosarjaryhmä | Tätä numerosarjaryhmän koodia käytetään lisäsuodattimena, kun tiedostoille on jo määritetty tietty *pysyvä* numerosarjaryhmä. Tyhjä arvo katsotaan tietyksi arvoksi. Jos haluat ohittaa esimääritetyn ryhmän, käytä tämän asetuksen **Oletus**-asetusta. |
| Oletus | Jos tämä on otettu käyttöön, järjestelmä ohittaa esimääritetyn asiakirjanumerosarjaryhmän ja käyttää vain kauden alkamis- ja päättymispäivämääriä käytettävyyden analyysissa. Jos tämä kohta on poistettu käytöstä, järjestelmä käyttää valinnassa yhdistelmää **Voimassa** + **Vanhentumisaika** + **Alkuperäinen numerosarjaryhmä**. |

## <a name="document-posting"></a>Asiakirjan kirjaaminen
Kun kirjaat tiedoston, tiedostolle määritetään asianmukainen numerosarjaryhmä, joka perustuu asiakirjan kirjauspäivämäärään. Sen jälkeen tiedostonumero luodaan tunnistetun numerosarjan perusteella. Järjestelmä antaa viestin numerosarjaryhmän määritykseen liittyen.

![Asiakirjan numero.](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> Joissakin maissa asiakirjanumeroinnissa on käytössä erityinen logiikka. Tällöin maakohtainen logiikka korvaa **Kronologinen numerointi** -toiminnon.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
