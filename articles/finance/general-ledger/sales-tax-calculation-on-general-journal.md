---
title: Yleisten kirjauskansioiden rivien arvonlisäveron laskeminen
description: Tässä aiheessa selitetään, miten arvonlisäverot lasketaan erityyppisille tileille (toimittaja, asiakas, kirjanpito ja projekti) yleisen kirjauskansioiden riveille.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 25eb8dd6965f659f0febe53a6340cb1381c5664f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204903"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a>Yleisten kirjauskansioiden rivien arvonlisäveron laskeminen
[!include [banner](../includes/banner.md)]

Tässä aiheessa selitetään, miten arvonlisäverot lasketaan erityyppisille tileille (toimittaja, asiakas, kirjanpito ja projekti) yleisen kirjauskansioiden riveille.

Prosessi voidaan jakaa kolmeen vaiheeseen:

- Määritä arvonlisäveron suunta.

- Määritä arvonlisäveron summa, joka tallennetaan väliaikaiseen arvonlisäveron tauluun.

- Määritä arvonlisäveron summa ja tositteessa oleva tili.

## <a name="determine-the-sales-tax-direction"></a>Määritä arvonlisäveron suunta

Arvonlisäveron suunnan määritystapa riippuu tositteessa olevan tilin tyypistä. Arvonlisäveron suunta määräytyy tilin tyypin ja arvonlisäverokoodin yhdistelmän mukaan. Seuraavat osiot selittävät vaihtoehdot yksityiskohtaisemmin. 

### <a name="account-type-is-project"></a>Tilin tyyppi on Projekti

Jos tositteessa on kirjauskansiorivi, jossa tilin tyyppinä on **Projekti**, kaikki tositteen kirjauskansiorivit käyttävät samaa veron suuntaa. Sääntö esitellään seuraavassa kuvassa. Seuraavissa kohdissa näytetään mahdolliset verojen suunnat projektitileille.

•   Jos arvonlisäverokoodi on käyttövero, arvonlisäveron suunta on Käyttövero.

•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.

•   Jos arvonlisäverokoodi on EU:n sisäinen ALV, arvonlisäveron suunta on Maksettava arvonlisävero.

•   Jos arvonlisäverokoodi on käänteinen veloitus, arvonlisäveron suunta on Maksettava arvonlisävero.

Muussa tapauksessa arvonlisäveron suunta on Saatava arvonlisävero.

Seuraava kaavio kuvaa säännön graafisesti.

![Verojen mahdolliset suunnat projektitileille](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a>Tilin tyyppi on Toimittaja

Jos tositteessa on kirjauskansiorivi, jossa tilin tyyppinä on **Toimittaja**, kaikki tositteen kirjauskansiorivit käyttävät samaa veron suuntaa. Seuraavissa kohdissa näytetään mahdolliset verojen suunnat toimittajatileille. 

•   Jos arvonlisäverokoodi on käyttövero, arvonlisäveron suunta on Käyttövero.

•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.

•   Jos arvonlisäverokoodi on EU:n sisäinen ALV, arvonlisäveron suunta on Maksettava arvonlisävero.

•   Jos arvonlisäverokoodi on käänteinen veloitus, arvonlisäveron suunta on Maksettava arvonlisävero.

Muussa tapauksessa arvonlisäveron suunta on Saatava arvonlisävero.

Seuraava kaavio kuvaa säännön graafisesti.

![Verojen mahdolliset suunnat toimittajatileille](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a>Tilin tyyppi on Asiakas

Jos tositteessa on kirjauskansiorivi, jossa tilin tyyppinä on **Asiakas**, kaikki tositteen kirjauskansiorivit käyttävät samaa veron suuntaa. Seuraavissa kohdissa näytetään mahdolliset verojen suunnat asiakastileille.

•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.

•   Jos arvonlisäverokoodi on EU:n sisäinen ALV, arvonlisäveron suunta on Saatava arvonlisävero.

•   Jos arvonlisävero on käänteinen veloitus, arvonlisäveron suunta on Saatava arvonlisävero.

Muussa tapauksessa arvonlisäveron suunta on Maksettava arvonlisävero.

Seuraava kaavio kuvaa säännön graafisesti.

![Verojen mahdolliset suunnat asiakastileille](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a>Tilin tyyppi on Kirjanpito

Seuraavassa kuvassa esitetään sääntö, jota käytetään, kun tositteessa on vain kirjauskansiorivejä, joissa tilin tyyppi **Kirjanpito**. Seuraavissa kohdissa näytetään mahdolliset verojen suunnat kirjanpitotileille.

•   Jos arvonlisäverokoodi on käyttövero, arvonlisäveron suunta on Käyttövero.

•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.

Muussa tapauksessa, jos kirjauskansion summa on debet (positiivinen), arvonlisäveron suunta on Saatava arvonlisävero. Jos kirjauskansion summa on kredit (negatiivinen), arvonlisäveron suunta on Maksettava arvonlisävero.

Seuraava kaavio kuvaa säännön graafisesti.

![Verojen mahdolliset suunnat kirjanpitotileille](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a>Korvaa arvonlisäveron suunta

Voit korvata arvonlisäveron suunnan, kun tosite sisältää vain rivejä, jossa tilin tyyppi on **Kirjanpito**.

Siirry kohtaan **Kirjanpito \> Tilikartta \> Tilit \> Päätilit** ja valitse **Yrityksen ohitukset** -pikavälilehti.

## <a name="determine-the-sales-tax-amount"></a>Määritä arvonlisäveron summa

Tässä osiossa kuvataan, miten arvonlisäveron summan etumerkki lasketaan.

![Arvonlisäverotapahtumat-sivu](media/sales-tax-amount-sign.jpg)

Seuraavassa taulukossa esitetään yleinen sääntö, joka määrittää arvonlisäveron summien etumerkin väliaikaisessa arvonlisäveron taulussa.

| Kirjauskansiorivin summa | Arvonlisäveron suunta  | Arvonlisäveron summan etumerkki |
|---------------------|----------------------|-----------------------|
| Positiivinen            | Saatava arvonlisävero | Positiivinen              |
| Positiivinen            | Maksettava arvonlisävero    | Negatiivinen              |
| Negatiivinen            | Saatava arvonlisävero | Negatiivinen              |
| Negatiivinen            | Maksettava arvonlisävero    | Positiivinen              |

Tositteilla, joilla on vain **Projekti**- tai **Kirjanpito**-rivejä, on erityissääntö, kun **Kirjanpito**-riville on valittu arvonlisäveroryhmä tai nimikkeen arvonlisäveroryhmä. Tätä sääntöä ohjaa yleisten kirjauskansioiden Ota käyttöön itsenäinen arvonlisäveron laskeminen -toiminto. Kun tämä toiminto ei ole käytössä, **Kirjanpito**-rivin veron summa käyttää **Projekti**-rivin debet/kredit-suuntaa. Kun tämä toiminto on käytössä, **Kirjanpito**-rivin veron summa käyttää sen omaa debet/kredit-suuntaa. Seuraava taulukko esittää säännön molemmille skenaariolle. 

**Sääntö, kun toiminto on käytössä**

| Kirjauskansiorivin projektin summa | Arvonlisäveron suunta  | Arvonlisäveron summan etumerkki |
|--------------------------------|----------------------|-----------------------|
| Positiivinen                       | Saatava arvonlisävero | Positiivinen              |
| Negatiivinen                       | Saatava arvonlisävero | Negatiivinen              |

**Sääntö, kun toiminto ei ole käytössä**

| Kirjauskansiorivin kirjanpidon summa  | Arvonlisäveron suunta  | Arvonlisäveron summan etumerkki |
|--------------------------------|----------------------|-----------------------|
| Positiivinen                       | Saatava arvonlisävero | Positiivinen              |
| Negatiivinen                       | Saatava arvonlisävero | Negatiivinen              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a>Määritä arvonlisäveron summa ja tositteessa oleva tili

Kun kirjaat arvonlisäveroja, päätili haetaan kirjanpidon kirjausryhmän profiilista. Kun arvonlisäverot ovat saatavia, järjestelmä käyttää profiilissa määritettyä Saatava arvonlisävero -tiliä. Kun arvonlisäverot ovat maksettavia, järjestelmä käyttää profiilissa määritettyä Maksettava arvonlisävero -tiliä.

Seuraavassa taulukossa kuvataan yleinen sääntö.

| Arvonlisäveron suunta  | Arvonlisäveron summan etumerkki | Arvonlisäverotili      | Tositteen summa |
|----------------------|-----------------------|------------------------|-------------------|
| Saatava arvonlisävero | Positiivinen              | Saatava vero -tili | Positiivinen (debet)  |
| Saatava arvonlisävero | Negatiivinen              | Saatava vero -tili | Negatiivinen (kredit)  |
| Maksettava arvonlisävero    | Positiivinen              | Maksettava vero -tili    | Negatiivinen (kredit)  |
| Maksettava arvonlisävero    | Negatiivinen              | Maksettava vero -tili    | Positiivinen (debet)  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]