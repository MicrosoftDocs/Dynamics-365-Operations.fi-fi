---
title: Sijainnin varastointirajoitukset
description: Tässä aiheessa käsitellään sijainnin varastointirajoituksia.
author: perlynne
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e0adb9d05f0db9bbfe6bfbe72564a4e5e839f163
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004572"
---
# <a name="location-stocking-limits"></a>Sijainnin varastointirajoitukset

[!include [banner](../includes/banner.md)]

**Sijainnin varastointirajoitukset** -sivulla (**Varastonhallinta \> Määritys \> Varasto \> Sijainnin varastointirajoitukset**) voi hallita varastosijaintien kuormituskapasiteettia ilman, että olisi käytettävä fyysisten tuotteiden edistyneitä tilavuuslaskelmaprosesseja.

Sijainnin varastointirajoitusten tarkoituksena on arvioida, mikä on sijaintiin sijoitettava enimmäismäärä. Toiminto voidaan määrittää kolmella eri tasolla, joista kullakin on oma välilehti **Sijainnin varastointirajoitukset** -sivulla:

- Tuotteet
- Tuotevariantit
- Konttityypit

Kullakin tasolla voidaan määrittää erilaiset kenttien arvot. Järjestelmä arvioi sitten tietyn sijainnin kapasiteetin kunkin rivin **Määrä**- ja **Yksikkö**-arvojen perusteella. Se valitsee ensimmäiseksi tietueen, jolla on tarkin vastaavuus. Esimerkiksi rivi, jolla on arvo **Sijaintiprofiilin tunnus** -kentässä arvioidaan ennen riviä, jolla on arvo vain **Varasto**-kentässä. Myös jäljellä oleva kapasiteetti voidaan arvioida käytetyn sijainnin varastointirajatietueen **Määrä**-arvon perusteella.

Sivun **Tuotteet**-osassa voidaan määrittää seuraavat kentän arvot sijainnin varastointirajoitusten hakua varten:

- Varasto
- Sijainnin profiilitunnus
- Toimipaikka
- Pakkauskokoluokan tunnus
- Nimiketunnus
- Yksikkö

> [!NOTE]
> Jokaisen sijainnin varastointirajoitustietueen **Yksikkö**-arvoa ei tarvitse määrittää. Sijainnin kapasiteettilaskelmat perustuvat varastoyksikön määriin. Jos käytettävälle arvolle ei ole määritetty yksikkömuuntoa, sijainnin varastointirajatietue ohitetaan aivan kuin sille olisi määritetty toinen **Nimiketunnus**-arvo.

## <a name="example--purchase-order-receiving"></a>Esimerkki – ostotilauksen vastaanotto

Tämä esimerkki perustuu puhtaaseen *USMF*-esittelytietojoukkoon, jossa seuraavat arvot on määritetty **Sijainnin varastointirajoitukset** -sivun **Tuotevariantit**-välilehdessä.

| Varasto | Sijainnin profiilitunnus | Nimiketunnus | Koko | Määrä | Yksikkö |
|-----------|---------------------|-------------|------|----------|------|
| 24        | KERROS               | D0013       | M    | 300      | Kpl   |
| 24        | KERROS               | D0013       | L    | 240      | Kpl   |
| 24        | KERROS               | D0013       | L    | 360      | Kpl   |

Tuotteille määritetään eri mittayksikön tuotevariantit. Nämä variantit kohdistetaan kolmen kuormalavan (KL) sijainnin varastointirajoituksiin:

- **Koko M:** 1 KL = 100 kappaletta (kpl)
- **Koko L:** 1 KL = 80 kpl
- **Koko S:** 1 KL = 120 kpl

Niinpä jokaisessa sijainnissa, jossa **Sijaintiprofiilin tunnus** -arvoksi on määritetty *KERROS*, voi olla *3* *KL* nimiketunnusta *D0013*.

### <a name="prepare-for-the-example"></a>Esimerkin valmistelu

Tässä esimerkissä suoritetaan ostotilauksen vastaanoton työnkulku kahdelle riville. Esittelytiedot on kuitenkin päivitettävä ensin seuraavalla tavalla, sillä näin varmistetaan, että sijainneissa voi olla yhdistettyjä nimikeitä, että käytössä on vain tyhjät sijainnit *FL-002*–*FL-004* ja että avoimia saapuvia töitä ei ole.

1. Muuta sijainnin *FL-001* **Sijaintiprofiili**-kentän arvo *KERROS* arvoksi *KERROS-05*.
1. Määritä *KERROS*-sijaintiprofiilin **Salli yhdistetyt nimikkeet** -asetukseksi *Kyllä*.
1. Lisää ostotilausrivi, jossa on kaksi seuraavaa riviä.

    | Varasto | Nimiketunnus | Koko | Määrä | Yksikkö |
    |-----------|-------------|------|----------|------|
    | 24        | D0013       | L    | 4        | PL   |
    | 24        | D0013       | L    | 4        | PL   |

### <a name="process-the-example"></a>Esimerkin käsitteleminen

Ensimmäinen vastaanotettu määrä on *4*, yksikkö *KL* ja koko *S*. Tarkista luodun työn sijainnin asetusrivi. Seuraava vastaanotettu määrä on *4*, yksikkö *KL* ja koko *L*. Tarkista luodun työn sijainnin asetusrivi.

1. Kirjaudu varastosovelluksessa sisään käyttämällä lukua *24* käyttäjätunnuksena ja lukua *1* salasanana.
1. Valitse **Saapuva** \> **Oston vastaanotto**.
1. Vastaanotto: *4* *KL*, nimiketunnus *D0013*, koko *S*.
1. Tarkista luotu hyllytystyö. Tuloksen pitäisi olla seuraava:

    - 3 KL -\> FL-002
    - 1 KL -\> FL-003

1. Vastaanotto: *4* *KL*, nimiketunnus *D0013*, koko *L*.
1. Tarkista luotu hyllytystyö. Tuloksen pitäisi olla seuraava:

    - 1 KL -\> FL-003
    - 3 KL -\> FL-004

Tulosten perusteella voi päätellä, että järjestelmä ei onnistunut kohdistamaan oikeita hyllytyssijainteja. Miksi järjestelmä olisi muuten lisännyt vain *1* *KL*, koko *L* sijaintiin *FL-003* viimeisessä vaiheessa eikä *2* *KL*? Toisin sanoen miksi kyseiseen sijaintiin hyllytettävä kokonaismäärä on *3* *KL*?

Tämän selittäminen edellyttää, että tiedät sijainnin varastointirajoitusten valintaehdot. Järjestelmä valitsee tietueen, jolla on tarkin vastaavuus. Tässä esimerkiksi tarkimmin vastaava tietue on rivi, jossa **Koko**-arvo on *L*, **Määrä**-arvo on *240* ja **Yksikkö**-arvo on *Kpl*. Koska edellisestä vastaanotosta (määrä *120* *kpl*, koko *S*) on jo avoin työ, jäljellä oleva kapasiteetti lasketaan seuraavasti: *240* – *120* = *120* *kpl*. Niillä jäljellä oleva kapasiteetti on vain *1* *KL*, *80* *kpl*.

> [!NOTE]
> Sijoituksen varastointirajoitusten ei voi hallita esimerkiksi sellaisten nimikkeiden täydennystä, joilla on eri määriä samassa sijainnissa. Siinä tapauksessa on käytettävä *täydennysmallia*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]