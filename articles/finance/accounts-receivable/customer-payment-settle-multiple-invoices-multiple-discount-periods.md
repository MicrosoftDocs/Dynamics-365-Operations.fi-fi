---
title: Useita alennuskausia kattavien laskujen tilittäminen yhdellä maksulla
description: Tässä ohjeaiheessa näytetään, miten maksetaan useita laskuja, kun kukin lasku on oikeutettu käteisalennukseen. Tämän artikkelin skenaariot osoittavat sen, miten käteisalennukset voivat vaihdella maksuajankohdan mukaan.
author: ShivamPandey-msft
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5187835da33d729e50aad9c813d8753d240fb81
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727619"
---
# <a name="use-one-payment-to-settle-invoices-that-span-multiple-discount-periods"></a>Useita alennuskausia kattavien laskujen tilittäminen yhdellä maksulla

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa näytetään, miten maksetaan useita laskuja, kun kukin lasku on oikeutettu käteisalennukseen. Tämän artikkelin skenaariot osoittavat sen, miten käteisalennukset voivat vaihdella maksuajankohdan mukaan.

Fabrikam myy tavaroita asiakkaalle 4032. Fabrikam tarjoaa 1 prosentin käteisalennuksen, jos lasku maksetaan 14 päivän kuluessa. Fabrikam myöntää käteisalennukset myös osamaksuista. Tilityksen parametrit sijaitsevat **Myyntireskontran parametrit** -sivulla.

## <a name="invoices"></a>Laskut
Asiakkaalla 4032 on kolme laskua, joiden yhteissumma on 3 000,00:

-   Lasku FTI-10040, summa 1 000,00, kirjattiin 15.5. Tämä lasku oikeuttaa 1 prosentin käteisalennuksen, jos se maksetaan 14 päivän kuluessa.
-   Lasku FTI-10041, summa 1 000,00, kirjattiin 25.6. Tämä lasku oikeuttaa 1 prosentin käteisalennuksen, jos se maksetaan 14 päivän kuluessa.
-   Lasku FTI-10042, summa 1 000,00, kirjattiin 25.6. Tämä lasku on oikeutettu 2 prosentin käteisalennukseen, jos se maksetaan viiden päivän sisällä ja 1 prosentin alennuksen, jos se maksetaan 14 päivän kuluessa.

## <a name="settle-all-invoices-on-june-29"></a>Kaikkien laskujen tilittäminen 29. kesäkuuta
Jos Erik luo maksukirjauskansion, jotta laskut voidaan tilittää kokonaan 29. kesäkuuta, maksettava summa on 2 970,00. Alennussummat ovat yhteensä 30,00. Erik luo maksun asiakkaalle 4032 ja avaa sitten **Selvitä tapahtumat** -sivun. Erik merkitsee **Selvitä tapahtumat** -sivulla tilitettäviksi kaikki kolme laskuriviä:

-   Laskun FTI-10040 maksettava summa on 1 000,00. Käteisalennusta ei käytetä.
-   Laskun FTI-10041 maksettava summa on 990,00. 1 prosentin käteisalennus (10,00) käytetään.
-   Laskun FTI-10042 maksettava summa on 980,00. 2 prosentin käteisalennus (20,00) käytetään.

| Merkitse                     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Valuutta | Täsmäytettävä summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valittu                 | Normaali            | FTI-10040 | 4032    | 15.5.2015 | 15.6.2015 | 10040   | 1 000,00                             |                                       | USD      | 1 000,00         |
| Valittu                 | Normaali            | FTI-10041 | 4032    | 25.6.2015 | 25.7.2015 | 10041   | 1 000,00                             |                                       | USD      | 990,00           |
| Valitut ja korostetut | Normaali            | FTI-10042 | 4032    | 25.6.2015 | 25.7.2015 | 10042   | 1 000,00                             |                                       | USD      | 980,00           |

Kun maksu on kirjattu, asiakkaan saldo on 0,00.

## <a name="settle-all-invoices-on-july-1"></a>Kaikkien laskujen tilittäminen 1. heinäkuuta
Jos Erik luo maksukirjauskansion, jotta laskut voidaan tilittää kokonaan 1. heinäkuuta, maksettava summa on 2 980,00. Erik luo maksun asiakkaalle 4032 ja avaa sitten **Selvitä tapahtumat** -sivun. Erik merkitsee **Selvitä tapahtumat** -sivulla tilitettäviksi kaikki kolme laskuriviä:

-   Laskun FTI-10040 maksettava summa on 1 000,00. Käteisalennusta ei käytetä.
-   Laskun FTI-10041 maksettava summa on 990,00. 1 prosentin käteisalennus (10,00) käytetään.
-   Laskun FTI-10042 maksettava summa on 990,00. 1 prosentin käteisalennus (10,00) käytetään. Vaikka 1. heinäkuuta on 2 prosentin alennukseen oikeuttavan kauden jälkeen, se on yhä 1 prosentin alennukseen oikeuttavalla kaudella.

| Merkitse                     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Valuutta | Täsmäytettävä summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valittu                 | Normaali            | FTI-10040 | 4032    | 15.5.2015 | 15.6.2015 | 10040   | 1 000,00                             |                                       | USD      | 1 000,00         |
| Valittu                 | Normaali            | FTI-10041 | 4032    | 25.6.2015 | 25.7.2015 | 10041   | 1 000,00                             |                                       | USD      | 990,00           |
| Valitut ja korostetut | Normaali            | FTI-10042 | 4032    | 25.6.2015 | 25.7.2015 | 10042   | 1 000,00                             |                                       | USD      | 990,00           |

## <a name="partial-settlement-on-june-29"></a>Osittainen tilitys 29. kesäkuuta
Asiakas 4032 voi maksaa laskun osissa, esimerkiksi puolet kustakin laskusta. Erik luo maksun asiakkaalle 4032 ja avaa sitten **Selvitä tapahtumat** -sivun. Erik merkitsee **Selvitä tapahtumat** -sivulla tilitettäviksi kaikki kolme laskuriviä. Erik syöttää kullekin riville tilitettävän summan asiakkaan antamien ohjeiden mukaan. Kun Erik valitse jonkin rivin, hän näkee rivin alennussumman ja käytettävän käteisalennuksen summan. Koska asiakas maksaa puolet laskusta, Erik näkee, että **Käteisalennussumma**-kentässä laskun FTI 10042 arvo on **20,00**, mutta **Käytetty käteisalennus** -kentän arvo on **10,00**. Maksettava summa on 1 485,00.

| Merkitse                     | Käytä käteisalennusta | Tosite   | Tili | Päivämäärä      | Eräpäivä  | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Valuutta | Täsmäytettävä summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valittu                 | Normaali            | FTI-10040 | 4032    | 15.5.2015 | 15.6.2015 | 10040   | 1 000,00                             |                                       | USD      | 500,00           |
| Valittu                 | Normaali            | FTI-10041 | 4032    | 25.6.2015 | 25.7.2015 | 10041   | 1 000,00                             |                                       | USD      | 495,00           |
| Valitut ja korostetut | Normaali            | FTI-10042 | 4032    | 25.6.2015 | 25.7.2015 | 10042   | 1 000,00                             |                                       | USD      | 490,00           |

Arnie voi myös syöttää manuaalisesti maksusumman 1 485,00 ennen kuin hän avaa **Selvitä tapahtumat** -sivun. Jos Arnie manuaalisesti syöttää maksusumman ja merkitsee siten kaikki kolme tapahtumaa, mutta hän ei muuta **Täsmäytettävä summa** -kentän arvoa kunkin tapahtuman osalta, hän saa seuraavan sanoman, kun sivu sulkeutuu:

> Merkittyjen tapahtumien kokonaissumma poikkeaa kirjauskansion summasta. Muutetaanko kirjauskansion summa?

Jos Erik haluaa määrittää maksettavaksi summaksi vain 1 485,00, hän valitsee vaihtoehdon **Ei** ja kirjaa kirjauskansion. Tapahtumat tilitetään seuraavasti:

1.  Lasku FTI-10040 on kokonaan tilitetty summasta 1 000,00, koska se on syötetty 15. toukokuuta ja on vanhin lasku. Käteisalennusta ei käytetä. Maksutapahtuman jäljelle jäävä summa on 485,00.
2.  Laskua FTI-10041 ei tilitetä lainkaan. Laskut FTI-10041 ja FTI-10042 on syötetty järjestelmään samana päivänä. Laskulle FTI-10041 voidaan kuitenkin käyttää 1 prosentin alennus ja laskulle FTI-10042 voidaan käyttää 2 prosentin alennus. Koska laskulle FTI-10042 on käytettävissä parempi alennus, jäljellä oleva summa 485,00 tilitetään laskulla FTI-10042.
3.  Lasku FTI-10042 tilitetään jäljellä olevasta summasta 485,00. Fabrikam myöntää osittaisia alennuksia. Tässä tapauksessa alennus on 9,90 (= 485,00 ÷ 0,98 × 0,02). Summa (485,00) jaetaan 0,98:lla, koska käytettävissä on 2 prosentin alennus (eli asiakas maksaa 98 prosenttia laskusta). Tulos kerrotaan alennusprosentilla eli 2 prosentilla. Maksettava summa 485,00 ja alennus 9,90 tekevät yhteensä 494,90. Alkuperäisen laskun summa oli 1 000,00. Tapahtuman saldo on siten 505,10 (= 1 000,00 – 494,90).

Arnie tarkastelee tietoja **Asiakastapahtumat**-sivulla.

| Tosite    | Tapahtumatyyppi | Päivämäärä      | Lasku | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo  | Valuutta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10040  | Lasku          | 15.5.2015 | 10040   | 1 000,00                             |                                       | 0,00     | USD      |
| FTI-10041  | Lasku          | 25.6.2015 | 10041   | 1 000,00                             |                                       | 1 000,00 | USD      |
| FTI-10042  | Lasku          | 25.6.2015 | 10042   | 1 000,00                             |                                       | 505,10   | USD      |
| ARP-10040  | Maksu          | 29.6.2015 |         |                                      | 1 485,00                              | 0,00     | USD      |
| ALE-10040 | Käteisalennus    | 29.6.2015 |         |                                      | 9,90                                  | 0,00     | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
