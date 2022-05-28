---
title: Hyvityslaskujen alennuksia sisältävän asiakkaan osamaksun tilittäminen
description: Tässä artikkelissa käydään läpi skenaario, jossa käteisalennus tehdään hyvityslaskussa, kun myös alkuperäisellä laskulla on käteisalennus.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a5ecf69c83805834c01c03d0af9b7b8c5310920
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725090"
---
# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Hyvityslaskujen alennuksia sisältävän asiakkaan osamaksun tilittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käydään läpi skenaario, jossa käteisalennus tehdään hyvityslaskussa, kun myös alkuperäisellä laskulla on käteisalennus. 

Fabrikam myöntää asiakkaille käteisalennuksia osamaksuista ja hyvityslaskuista. Käteisalennus voidaan tehdä hyvityslaskulla, kun hyvityslasku tehdään laskusta, josta asiakas on saanut käteisalennuksen. Sen sijaan, että antaisit hyvityksen koko summasta, voit hyvittää asiakkaan saldoa summalla, joka ei sisällä asiakkaan saamaa käteisalennuksen osuutta. Tilityksen parametrit sijaitsevat **Myyntireskontran parametrit** -sivulla.

## <a name="invoice-and-credit-note"></a>Lasku ja hyvityslasku
Asiakkaalla 4035 on lasku, jonka arvo on 1 000,00, ja hyvityslasku, jonka arvo on 100,00. Kumpaankin saa 1 prosentin alennuksen, jos se maksetaan 14 päivän kuluessa. Arnie voi tarkastella tietoja **Asiakastapahtumat**-sivulla.

| Tosite    | Tapahtumatyyppi | Päivämäärä      | Lasku  | Summa tapahtuman valuuttana debet | Summa tapahtuman valuuttana kredit | Saldo  | Valuutta |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | Lasku          | 28.6.2015 | 10050    | 1 000,00                             |                                       | 1 000,00 | USD      |
| CCRN-10050 | Hyvityslasku      | 28.6.2015 | KR-10050 |                                      | 100,00                                | -100,00  | USD      |

## <a name="settle-a-credit-note-with-an-invoice"></a>Hyvityslaskun tilittäminen laskun kanssa
Arnie avaa **Asiakastapahtumat**-sivulla **Selvitä tapahtumat** -sivun. Arnie voi tilittää laskun ja hyvityslaskun **Selvitä tapahtumat** -sivulla. Arnie tarkistaa tilityksen yhteydessä käteisalennuksen päivämäärät ja summat. Arnie merkitsee asiakirjat ja tilittää sitten tapahtumat napsauttamalla **Kirjaa**. Hyvityslaskuun sisältyy alennus -1,00, koska Fabrikam myöntää alennuksia hyvityslaskuista.

| Merkitse     | Käytä käteisalennusta | Tosite    | Tili | Päivämäärä      | Eräpäivä  | Lasku  | Summa tapahtuman valuuttana | Valuutta | Täsmäytettävä summa |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Valittu | Normaali            | FTI-10050  | 4035    | 28.6.2015 | 28.7.2015 | 10050    | 1 000,00                       | USD      | 990,00           |
| Valittu | Normaali            | CCRN-10050 | 4035    | 28.6.2015 | 28.7.2015 | KR-10050 | -100,00                        | USD      | -99,00           |

Alennustiedot näkyvät **Selvitä tapahtumat** -sivun alaosassa.

- **Käteisalennuksen päivämäärä**: 12.7.2015 
- **Käteisalennussumma**: -1,00     
- **Käytä käteisalennusta**: normaali    
- **Käytetty käteisalennus**: 0,00      
- **Käytettävä käteisalennussumma**: -1,00     

Tilitys on 100,00, ja siihen sisältyy maksusuoritus 99,00 ja alennus 1,00.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
