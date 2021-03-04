---
title: Jaksotettu poissaolo työtuntien mukaan
description: Tässä ohjeaiheessa kuvataan, miten lomasuunnitelmat voidaan määrittää jaksotettuun poissaoloon työtuntien mukaan.
author: andreabichsel
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-09-17
ms.dyn365.ops.version: ''
ms.openlocfilehash: 229ae14b9e2dedcd0ade094a772f16c0524d32a7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461069"
---
# <a name="accrue-time-off-based-on-hours-worked"></a>Jaksotettu poissaolo työtuntien mukaan

## <a name="overview"></a>Yleiskuvaus

Organisaatiot, joissa on tuntihinnalla työskenteleviä työntekijöitä, voivat myöntää poissaoloja työtuntien mukaan virkaiän sijasta organisaatiossa. Työtuntitiedot tallennetaan yleensä aika- ja läsnäolojärjestelmään. 

## <a name="leave-plans"></a>Lomasuunnitelmat

Lomasuunnitelmassa jaksotustyyppi voidaan ilmaista joko palvelukuukausien tai työtuntien mukaan. Kun valittuna ovat työtunnit, jaksotuksessa voi käyttää kahdenlaisia tunteja, tavallisia työtunteja tai ylityötunteja.

Voit määrittää lomasuunnitelman työtuntien mukaan seuraavien ohjeiden mukaisesti:

1. Napsauta **Loma- ja poissaolosuunnitelmat**-sivulla **Luo uusi suunnitelma**.
2. Kirjoita lomasuunnitelmasi nimi.
3. Valitse suunnitelman jaksotusväli.
5. Valitse suunnitelman aloituspäivä.
6. Valitse jaksotuskausiperusta ja työntekijäkohtainen päivämäärä tarvittaessa.
7. Valitse jakosotusaikataululle jaksotustyypiksi **Työtunnit**.
8. Valitse jaksotuksessa käytettävien tuntien tyyppi.
9. Kirjoita työtuntien määrä ja liittyvä jaksotussumma, vähimmäissaldo sekä siirtokirjauksen tai palkkiosumman enimmäismäärä.

Työtuntiperusteisten suunnitelmien jaksotuksen käsittelyssä käytetään jaksotusväliä ja jaksotuskausiperustaa määrittämään jaksotettavat tunnit.

## <a name="annual-accrual-frequency"></a>Vuotuinen jaksotusväli

| Jaksotuksen myöntöpäivämäärä    | Työtuntitaso    | Jaksotussumma        | Työtuntien päivämäärät   | Todelliset työtunnit| Palkkio               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31.12.2018            | 2080                 | 144                   | 1.1.2018–31.12.2018  | 2085                | 144                 |        
| 31.12.2018            | 2080                 | 144                   | 1.1.2018–31.12.2018  | 2 000                | 0                 |


## <a name="monthly-accrual-frequency"></a>Kuukausittainen jaksotusväli

| Jaksotuksen myöntöpäivämäärä    | Työtuntitaso    | Jaksotussumma        | Työtuntien päivämäärät   | Todelliset työtunnit| Palkkio               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31.8.2018             | 160                  | 12                    | 1.8.2018–31.8.2018   | 184                 | 12                  |        
| 31.8.2018             | 160                  | 3                     | 1.8.2018–31.8.2018   | 184                 | 3                   |

## <a name="semi-monthly-accrual-frequency"></a>Puolikuukausittainen jaksotusväli

| Jaksotuksen myöntöpäivämäärä    | Työtuntitaso    | Jaksotussumma        | Työtuntien päivämäärät   | Todelliset työtunnit| Palkkio               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31.8.2018             | 80                   | 6                     | 16.8.2018–31.8.2018  | 81                  | 6                  |        
| 31.8.2018             | 80                   | 6                     | 16.8.2018–31.8.2018  | 75                  | 0                   |

## <a name="weekly-accrual-frequency"></a>Viikoittainen jaksotusväli

| Jaksotuksen myöntöpäivämäärä    | Työtuntitaso    | Jaksotussumma        | Työtuntien päivämäärät   | Todelliset työtunnit| Palkkio               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31.8.2018             | 40                   | 3                     | 27.8.2018–31.8.2018  | 42                  | 3                  |        
| 31.8.2018             | 40                   | 3                     | 27.8.2018–31.8.2018  | 35                  | 0                   |

## <a name="employee-assigned-leave-plans"></a>Työntekijälle määritetyt lomasuunnitelmat

Työntekijälle määritetyissä lomasuunnitelmissa tuntien tasoperusta ja tyyppi näytetään suunnitelmille, joissa työtunnit määritetään jaksotustyyppisenä. Aktiivisille suunnitelmille näytetään viitteenä sen hetkisen päivämäärän jaksotuskausien todelliset työtunnit. 

## <a name="loading-data"></a>Ladataan tietoja

Todelliset tunnit voidaan tuoda käyttämällä tiedonhallinnan lomien ja poissaolojen vapaatuntien yksikköä. Jos käytät työaikakalentereita, tuonti vahvistaa, että nämä tavalliset työtunnit eivät ylitä kalenterin määrittämien ajoitettujen tuntien määrää päivässä. Tuonti vahvistaa myös, että tietyn päivän työtunnit eivät ylitä 24 tuntia. 

Jotta voit tuoda lomien jaksotusprosessissa käytettävät todelliset tunnit, tarvitset seuraavia tietoja:

+ Henkilöstönumero 
+ Työn päivämäärä
+ Laji
+ Tunnit

Yhteen päivään voi liittyä vain yksi tyyppi kutakin.

| HENKILÖSTÖNUMERO       | TYÖN PÄIVÄMÄÄRÄ           | TYYPPI                  | TUNNIT                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 6.8.2018             | Säännöllinen               | 8                    |       
| 000337                | 7.8.2018             | Säännöllinen               | 8                    |
| 000337                | 7.8.2018             | Ylityö              | 3                    |
| 000337                | 8.8.2018             | Säännöllinen               | 8                    |
| 000337                | 7.8.2018             | Säännöllinen               | 8                    |
| 000337                | 9.8.2018             | Säännöllinen               | 8                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]