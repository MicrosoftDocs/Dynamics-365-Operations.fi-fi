---
title: Käteisalennukset
description: Käteisalennukset määritetään ja jaetaan osto- ja myyntireskontrassa.  Käytettävissä oleva käteisalennus voidaan määrittää myyntilaskulla tai toimittajan laskulla. Se käytetään, jos lasku maksetaan käteisalennuksen päivänä.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: kfend
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b75637bfb38c13591223ff11be36d958b3972d4f
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804126"
---
# <a name="cash-discounts"></a>Käteisalennukset

[!include [banner](../includes/banner.md)]

Käteisalennukset määritetään ja jaetaan osto- ja myyntireskontrassa. Käytettävissä oleva käteisalennus voidaan määrittää myyntilaskulla tai toimittajan laskulla. Se käytetään, jos lasku maksetaan käteisalennuksen päivänä. 

## <a name="cash-discounts"></a>Käteisalennukset

Asiakkaiden ja toimittajien käteisalennuksia luodaan **Käteisalennukset**-sivulla. Voit lisäksi määrittää **Seuraava alennuskoodi** -kentässä sarjan peräkkäisiä käteisalennuksia, jotka tulevat voimaan, kun edellisen vanhenee. Lisätietoja on myöhemmin tässä artikkelissa kohdassa Esimerkki: käteisalennussarja. Jos lasku, hyvitystapahtuma (maksu tai hyvityslasku) tai molemmat annetaan jonain muuna valuuttana kuin yrityksen kirjanpitovaluuttana, käteisalennus lasketaan käyttämällä vaihtokurssia, joka perustuu maksun tai hyvityslaskun päivämäärään. Jos lasku tai luottoasiakirja annetaan eri yrityksille ja jos yrityksillä on eri kirjanpitovaluutat, vaihtokurssi haetaan laskun yrityksestä luottoasiakirjan päivämäärällä. Lisätietoja on myöhemmin tässä artikkelissa kohdassa Esimerkki: käteisalennusten vaihtokurssit.

## <a name="defaulting-order-of-cash-discount-main-account"></a>Käteisalennuksen päätilin oletusjärjestys

Jos lasku maksetaan käteisalennukseen oikeuttavassa määräajassa, käteisalennus kirjataan automaattisesti käteisalennuksen päätilille seuraavassa oletusjärjestyksessä:
1.  Päätili, joka on määritetty **Vaihtoehtoinen käteisalennustili** -kentässä asiakkaan **Tilitä avoimet tapahtumat** -sivulla tai toimittajan **Tilitä avoimet tapahtumat** -sivulla.
2.  Päätili, joka on määritetty sen kirjanpidon kirjausryhmän  **Asiakkaan käteisalennus**- tai **Toimittajan käteisalennus** -kentässä, joka on liitetty laskun arvonlisäverokoodiin. Määritä kirjanpidon kirjausryhmät **Kirjanpidon kirjausryhmät** -sivulla ja määritä ne **Arvolisäverokoodit**-sivun arvonlisäverokoodeihin.
3.  Pääkirjaustili, joka on tilitetyssä laskussa olevan käteisalennuskoodin **Käteisalennukset**-sivulla joko **Asiakkaan alennusten päätili** -kentässä tai **Toimittajan alennusten päätili** -kentässä.
4.  **Automaattisten tapahtumien tilit** -sivulla määritetty käteisalennusten päätili.

## <a name="example-series-of-cash-discounts"></a> Esimerkki: käteisalennussarja
Määritä kolme käteisalennuskoodia seuraavasti:
-   Koodi 5D10% – 10 %:n käteisalennus, jos lasku maksetaan 5 päivän kuluessa.
-   Koodi 10D5% – 5 %:n käteisalennus, jos lasku maksetaan 10 päivän kuluessa.
-   Koodi 14D2% – 2 %:n käteisalennus, jos lasku maksetaan 14 päivän kuluessa.

**Seuraava alennuskoodi** -kentässä:
-   Valitse koodille 5D10% vaihtoehto 10D5%.
-   Valitse koodille 10D5% vaihtoehto 14D2%.
-   Jätä 14P2%-koodin osalta Seuraava alennuskoodi -kenttä tyhjäksi.

Kolme käteisalennusta seuraavat toisiaan, kun maksupäivä ylittää laskun edellisen käteisalennuspäivämäärän. Laskua maksettaessa voi käyttää vain yhtä alennuskoodia sen perusteella, mikä käteisalennussarjan käteisalennuspäivämäärä toteutuu.

## <a name="example-exchange-rates-for-cash-discounts"></a> Esimerkki: käteisalennusten vaihtokurssit
Yrityksen kirjanpitovaluutta on euro ja Yhdysvaltain dollarille on määritetty seuraavat vaihtokurssit:
-   1. helmikuuta = 110.
-   1. maaliskuuta = 80

1 000 dollarin lasku kirjataan 15.2. käteisalennusehdolla 20D2%. Laskun summa kirjanpitovaluutassa on 1 100 EUR 980 dollarin maksu täsmäytetään laskun kanssa 1.3. Käteisalennussumma on 20 dollaria. Maksun summa kirjanpitovaluuttana on 784 euroa. Käteisalennuksen summa kirjanpitovaluuttana lasketaan käyttämällä maaliskuun 1. päivän vaihtokurssia : 20 \* 80 / 100 = 16 euroa.

> [!NOTE]
> Jos **Myyntireskontran parametrit**- tai **Ostoreskontran parametrit** -sivulla valitaan **Laske käteisalennukset osamaksuille** -vaihtoehto, käytetään osamaksun maksupäivänä voimassaolevaa vaihtokurssia. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
