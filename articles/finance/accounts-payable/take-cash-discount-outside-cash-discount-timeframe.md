---
title: Käteisalennuksen käyttäminen käteisalennuskauden ulkopuolella
description: Tässä artikkelissa on kaksi skenaariota, jotka osoittavat, miten käteisalennus voidaan käyttää, vaikka maksu suoritettaisiin käteisalennuskauden ulkopuolella.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47acacf9b1e9667e86fcdd5ce1ed62e79d8afec3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810219"
---
# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>Käteisalennuksen käyttäminen käteisalennuskauden ulkopuolella

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on kaksi skenaariota, jotka osoittavat, miten käteisalennus voidaan käyttää, vaikka maksu suoritettaisiin käteisalennuskauden ulkopuolella.

April luo 28. kesäkuuta 2 000,00 arvoisen laskun toimittajalle 3052. Laskulla on 1 prosentin käteisalennus, jos se maksetaan 14 päivän kuluessa.

## <a name="use-cash-discount-option--always"></a>Käytä käteisalennusta -asetus = Aina
April luo maksun 1. heinäkuuta, joka on alennuspäivämäärän jälkeen. April avaa **Selvitä tapahtumat** -sivun tarkastellakseen tapahtumia, jotka voidaan selvittää. 

April merkitsee laskun maksulle. Käteisalennusta ei käytetä, koska maksu suoritetaan alennusjakson jälkeen. Toimittaja on kuitenkin sallinut, että April käyttää käteisalennusta siitä huolimatta. April muuttaa siksi **Käytä käteisalennusta** -kentän arvoksi **Aina**.

| Merkitse     | Käytä käteisalennusta | Tosite   | Tili | Käteisalennuksen päivämäärä | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Valittu | Aina            | Var-10030 | 3052    | 28.6.2015          | 12.7.2015 | 10030   | -2 000,00                      | USD      | -1 980,00        |

Alennustiedot näkyvät **Selvitä tapahtumat** -sivun alaosassa.

| Kenttä                        | Arvo     |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 12.7.2015 |
| Käteisalennussumma         | -20,00    |
| Käytä käteisalennusta            | Aina    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | -20,00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>Alennusten laskennalle käytettävä päivämäärä = Valittu päivämäärä
Jos sekä maksu ja lasku on kirjattu, käteisalennusta voi edelleen käyttää, kun tapahtumat selvitetään **Selvitä tapahtumat** -sivulla. April muuttaa **Alennusten laskennalle käytettävä päivämäärä** -kentän arvoksi **Valittu päivämäärä**. Hän syöttää päivämääräksi 28. kesäkuuta, joka on laskun käteisalennuskaudella. Tätä päivää käytetään tapahtuman käteisalennuksen laskentaan. **Tilitä avoimet tapahtumat** -sivulla April näkee, että siinä näytetään oletusarvoisesti täysi alennus, jonka arvo on 20,00. Laskurivillä näkyy, että tilitettävä summa on 1 980,00.

| Merkitse                     | Käytä käteisalennusta | Tosite   | Tili | Käteisalennuksen päivämäärä | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|--------------------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Valitut ja korostetut | Normaali            | Var-10030 | 3052    | 28.6.2015          | 12.7.2015 | 10030   | -2 000,00                      | USD      | -1 980,00        |
| Valittu                 | Normaali            | HYV-10030 | 3052    | 15.7.2015          | 15.7.2015 |         | 500,00                         | USD      | 500,00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat** -sivun alaosassa. Käytettävä alennussumma on 20,00, koska laskulle tilitettävä summa on oletussumma, eli 1 980,00.

| Kenttä                        | Arvo     |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 12.7.2015 |
| Käteisalennussumma         | -20,00    |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | -20,00    |

April päivittää laskun **Tilitettävä summa** -kentän arvoksi **-500,00**. **Käytettävä käteisalennussumma** -kentän arvoksi lasketaan **5,05**.

| Merkitse                     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitut ja korostetut | Normaali            | Var-10030 | 3052    | 28.6.2015 | 12.7.2015 | 10030   | 2 000,00                       | USD      | -500,00          |
| Valittu                 | Normaali            | HYV-10030 | 3052    | 15.7.2015 | 15.7.2015 |         | 500,00                         | USD      | 500,00           |

Alennustiedot näkyvät **Tilitä avoimet tapahtumat** -sivun alaosassa. **Käytettävä käteisalennussumma** -kentän arvo on **5,05**, koska laskun tilitettäväksi summaksi muutettiin maksun summa, 500,00.

| Kenttä                        | Arvo     |
|------------------------------|-----------|
| Käteisalennuksen päivämäärä           | 12.7.2015 |
| Käteisalennussumma         | -20,00    |
| Käytä käteisalennusta            | Normaali    |
| Käytetty käteisalennus          | 0,00      |
| Käytettävä käteisalennussumma | -5,05     |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]