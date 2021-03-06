---
title: Ylisuurten maksujen käteisalennukset
description: Tämän artikkelin skenaariossa kerrotaan, miten maksua käsitellään, kun asiakkaalle annetaan käteisalennus, mutta tämä maksaa liikaa.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be501c049ae7b884e317cbf3bd1918fec3fb421d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830486"
---
# <a name="cash-discounts-for-overpayments"></a>Ylisuurten maksujen käteisalennukset

[!include [banner](../includes/banner.md)]

Tämän artikkelin skenaariossa kerrotaan, miten maksua käsitellään, kun asiakkaalle annetaan käteisalennus, mutta tämä maksaa liikaa. 

Laskua on maksettu liikaa, kun maksusumma on suurempi kuin laskun summa, josta on vähennetty käteisalennus. Määrittääksesi miten käteisalennuksen erotus käsitellään, kun laskua on maksettu liikaa, käytä **Käteisalennuksen hallinta** ja **Liikaa tai liian vähän maksetun summan enimmäismäärä** -kenttiä **Myyntireskontran parametrit** -sivulla. Seuraavassa esimerkissä asiakas on maksanut laskussa liikaa 0,50.

| Laskun kokonaissumma | Käteisalennus saatavilla | Maksettava summa, joka sisältää käteisalennuksen | Summa, jonka asiakas todellisuudessa maksaa |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| 105,00        | 10,50                   | 94,50                                               | 95,00                             |

## <a name="cash-discount-administration--specific"></a>Käteisalennuksen hallinta = Yksilöity
Kun **Yksilöity** -asetus on valittu **Käteisalennuksen hallinta** -kenttään **Automaattisten tapahtumien tilit** -sivulla, koko käteisalennuksen otetaan huomioon. Liikamaksu kirjataan joko käteisalennuksen eron kirjanpitotilille tai säilytetään saldona asiakkaan tilillä. Järjestelmän toiminta riippuu siitä, onko liikamaksun summa 0,00:n ja **Liikaa / liian vähän maksetun summan enimmäismäärä** -kentän summan välillä, vai onko liikamaksun summa suurempi kuin **Liikaa / liian vähän maksetun summan enimmäismäärä** -summa.

### <a name="scenario-1"></a>Skenaario 1

Tässä tilanteessa liikamaksun summa on 0,00:n ja suurimman liika- tai alimaksun välillä. Lasku on kirjattu summalle 105,00, ja käteisalennus on käytettävissä, jos lasku maksetaan seitsemän päivän kuluessa.

| Laskun kokonaissumma | Käteisalennus saatavilla | Maksettava summa, joka sisältää käteisalennuksen |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Asiakas suorittaa maksun summalla 95,00 käteisalennuskauden ollessa voimassa. Maksu selvitetään laskun kanssa, jonka arvo on 105,00. Kun lasku ja maksu on selvitetty, seuraavat tapahtumat luodaan asiakkaalle Myyntireskontraan.

| Tapahtuma   | Summa | Saldo |
|---------------|--------|---------|
| Lasku       | 105,00 | 0,00    |
| Maksu       | –95,00 | 0,00    |
| Käteisalennus | –10,50 | 0,00    |

Seuraavat kirjanpitomerkinnät luodaan maksulle ja täsmäytykselle. **Maksu**

| Tili             | Veloitussumma | Kredit-summa |
|---------------------|--------------|---------------|
| Käteinen                | 95,00        |               |
| Myyntireskontra |              | 95,00         |

**Tilitys**

| Tili                                                                                                          | Veloitussumma | Kredit-summa |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| Käteisalennus (**Asiakkaan alennusten päätili** -kenttä **Käteisalennukset**-sivulla)                 | 10,50        |               |
| Myyntireskontra                                                                                              |              | 10,50         |
| Asiakkaan käteisalennus (**Asiakkaan käteisalennus** -kenttä **Tili automaattisille tapahtumille** -sivulla) |              | 0,50          |
| Myyntireskontra                                                                                              | 0,50         |               |

### <a name="scenario-2"></a>Skenaario 2

Tässä skenaariossa liikamaksun summa on enemmän kuin suurin liika- tai alimaksun summa. Lasku on kirjattu summalle 105,00, ja käteisalennus on käytettävissä, jos lasku maksetaan seitsemän päivän kuluessa.

| Laskun kokonaissumma | Käteisalennus saatavilla | Maksettava summa, joka sisältää käteisalennuksen |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Asiakas suorittaa maksun summalla 95,00 käteisalennuskauden ollessa voimassa. Maksu selvitetään laskun kanssa, jonka arvo on 105,00. Kun lasku ja maksu on selvitetty, seuraavat tapahtumat luodaan asiakkaalle Myyntireskontraan.

| Tapahtuma   | Summa | Saldo |
|---------------|--------|---------|
| Lasku       | 105,00 | 0,00    |
| Maksu       | –95,00 | –0,50   |
| Käteisalennus | –10,50 | 0,00    |

Liikamaksun summa 0,50 säilyy avoimena saldona maksuissa ja se voidaan täsmätä toisen laskun kanssa. Seuraavat kirjanpitomerkinnät luodaan maksulle ja täsmäytykselle. **Maksu**

| Tili             | Veloitussumma | Kredit-summa |
|---------------------|--------------|---------------|
| Käteinen                | 95,00        |               |
| Myyntireskontra |              | 95,00         |

**Tilitys**

| Tili                                                                                          | Veloitussumma | Kredit-summa |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Käteisalennus (**Asiakkaan alennusten päätili** -kenttä **Käteisalennukset**-sivulla) | 10,50        |               |
| Myyntireskontra                                                                              |              | 10,50         |

## <a name="cash-discount-administration--unspecific"></a>Käteisalennuksen hallinta = Yksilöimätön
Kun **Yksilöimätön** -asetus on valittu **Käteisalennuksen hallinta** -kenttään **Automaattisten tapahtumien tilit** -sivulla, käteisalennuksen summasta vähennetään liikamaksun summa. Järjestelmä toimii näin aina, riippumatta siitä, onko liikamaksun summa suurempi tai pienempi kuin **Liikaa / liian vähän maksetun summan enimmäismäärä** -kentän summa.

### <a name="scenario-3"></a>Skenaario 3

Tässä skenaariossa lasku on kirjattu summalle 105,00, ja käteisalennus on käytettävissä, jos lasku maksetaan seitsemän päivän kuluessa.

| Laskun kokonaissumma | Käteisalennus saatavilla | Maksettava summa, joka sisältää käteisalennuksen |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Asiakas suorittaa maksun summalla 95,00 käteisalennuskauden ollessa voimassa. Maksu selvitetään laskun kanssa, jonka arvo on 105,00. Kun lasku ja maksu on selvitetty, seuraavat tapahtumat luodaan asiakkaalle Myyntireskontraan.

| Tapahtuma   | Summa | Saldo |
|---------------|--------|---------|
| Lasku       | 105,00 | 0,00    |
| Maksu       | –95,00 | –0,00   |
| Käteisalennus | –10,00 | 0,00    |

Käteisalennuksen määrä vähennetään arvosta 10,50 arvoon 10,00. Maksua ja laskua pidetään selvitettyinä. **Maksu**

| Tili             | Veloitussumma | Kredit-summa |
|---------------------|--------------|---------------|
| Käteinen                | 95,00        |               |
| Myyntireskontra |              | 95,00         |

**Tilitys**

| Tili                                                                                          | Veloitussumma | Kredit-summa |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Käteisalennus (**Asiakkaan alennusten päätili** -kenttä **Käteisalennukset**-sivulla) | 10,50        |               |
| Myyntireskontra                                                                              |              | 10,50         |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]