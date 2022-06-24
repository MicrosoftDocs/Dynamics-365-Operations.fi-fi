---
title: Veron kaksoisvaluutan tuki
description: Tässä artikkelissa kerrotaan, miten kaksoisvaluutan kirjanpitotoiminto laajennetaan veroluokkaan, sekä veron laskennan ja kirjaamisen vaikutukset
author: EricWang
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 13d70d964a83c2efba090244d549bdb38ad25af2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909037"
---
# <a name="dual-currency-support-for-sales-tax"></a>Arvonlisäveron kaksoisvaluutan tuki
[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten kaksoisvaluutan kirjanpitotoiminto laajennetaan arvonlisäverolle, sekä arvonlisäveron laskentojen, kirjaamisen ja tilitysten vaikutukset.

Dynamics 365 Finance -sovelluksen kaksoisvaluuttatoiminto otettiin käyttöön versiossa 8.1 (lokakuu 2018). Se muuttaa raportointivaluutan kirjanpitomerkintöjen laskentatapaa.

Aiemmissa versioissa tapahtumat muunnettiin raportointivaluutaksi seuraavassa järjestyksessä: 

- Kokonaistapahtuma laskettiin tapahtumavaluuttana > Tapahtumasumma muunnettiin kirjanpitovaluutaksi > Kirjanpitovaluuttasumma muunnettiin raportointivaluutaksi

Kun kaksoisvaluuttatoiminto on otettu käyttöön, tapahtumat muunnetaan raportointivaluutaksi seuraavassa järjestyksessä:

- Tapahtuman valuuttasumma > Raportointivaluuttasumma

Lisätietoja kaksoisvaluutasta on kohdassa [Kaksoisvaluutta](dual-currency.md).

Kaksoisvaluutan tuen johdosta toimintojen hallinnassa on käytettävissä seuraavat kaksi uutta toimintoa: 

- Arvonlisäveron muuntaminen (uusi versiossa 10.0.13)
- Määritä taloushallinnon dimensiot toteutuneille valuuttaoikaisun voitto-/tappiotileille arvonlisäveron tilitystä varten (uusi versiossa 10.0.17)

Arvonlisäverojen kaksoisvaluutan tuki varmistaa sen, että verot lasketaan tarkasti verovaluuttana ja että arvonlisäveron tilityksen täsmäytys lasketaan tarkasti sekä kirjanpitovaluuttana että raportointivaluuttana.

## <a name="sales-tax-conversion"></a>Arvonlisäveron muunto

**Arvonlisäveron muuttamisen** parametri määrittää kaksi vaihtoehtoa, joiden avulla verosumman voi muuntaa tapahtumavaluutasta verovaluutaksi. 

- Kirjanpitovaluutta: Polku on Summa tapahtumavaluuttana > Summa kirjanpitovaluuttana > Summa verovaluuttana. Valuutan muuntamisessa käytetään kirjanpitovaluutan vaihtokurssin tyyppiä (määritetty kirjanpidon asetuksissa).
- Raportointivaluutta: Polku on Summa tapahtumavaluuttana > Summa raportointivaluuttana > Summa verovaluuttana. Valuutan muuntamisessa käytetään raportointivaluutan vaihtokurssin tyyppiä (määritetty kirjanpidon asetuksissa).

### <a name="example"></a>Esimerkki

Seuraavassa on yksinkertainen esimerkki tästä toiminnosta:

Kirjanpidon ja veron valuutan asetukset

| Tapahtumavaluutta | Kirjanpitovaluutta | Raportointivaluutta | Veron valuutta |
| -------------------- | ------------------- | ------------------ | ------------ |
| Euro                  | USD                 | GBP                | GBP          |

Vaihtokurssi

| Lähdevaluutta | Kohdevaluutta | Kerroin | Vaihtokurssi |
| ------------- | ----------- | ------ | ------------- |
| Euro           | USD         | 1      | 1.11          |
| Euro           | GBP         | 1      | 0.83          |
| USD           | GBP         | 1      | 0.75          |

Verosumman laskeminen eri parametrivaihtoehdoissa

Verosumma = 100 euroa

| Arvonlisäveron muunnoksen parametrit | Tapahtumavaluutta (euroina) | Kirjanpitovaluutta (Yhdysvaltain dollareina) | Raportointivaluutta (Ison-Britannian puntina) | Veron valuutta (Ison-Britannian puntina) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Kirjanpitovaluutta             | 100                        | 111                       | 83                       | **83.25**          |
| Raportointivaluutta              | 100                        | 111                       | 83                       | **83**             |

Tämä parametri voidaan määrittää veroviranomaisen vaatimustenmukaisuuteen liittyvän tarpeen perusteella.


### <a name="upgrade-consideration"></a>Päivitä huomioon otettavat seikat

Tämä toiminto koskee vain uusia tapahtumia. Jos verotapahtuma on jo tallennettu TAXTRANS-taulukkoon, mutta sitä ei ole vielä tilitetty, järjestelmä ei laske verosummaa uudelleen veron valuuttana, koska veron kirjausajankohdan vaihtokurssi puuttuu.

Jos haluat estää edellä kerrotun skenaarion, suosittelemme tämän parametrin arvon muuttamista uudelle (puhtaalla) verotilityskaudella, joka ei sisällä tilittämättömiä verotapahtumia. Jos haluat muuttaa tätä arvoa veron tilityskauden aikana, suorita Tilitä ja kirjaa arvonlisävero -ohjelma nykyisellä verontilityskaudella ennen kuin muutat tämän parametrin arvoa.

Tämä ominaisuus lisää kirjanpitomerkintöjä, jotka selventävät valuutanvaihdon voittoja ja tappioita. Tiedot tehdään realisoituneilla valuuttaoikaisun tulostileillä, kun uudelleenarvostus tehdään arvonlisäveron tilityksen yhteydessä. Lisätietoja on jäljempänä tässä artikkelissa osassa [Verotilitysten automaattinen saldo raportointivaluuttana](#tax-settlement-auto-balance-in-reporting-currency).

> [!NOTE]
> Tilityksen aikana taloushallinnon dimensioiden tiedot ovat liikevaihtotilejä eli tasetilejä, jotka syötetään valuuttaoikaisun tuloslaskelmaan eli tulostilille. Koska taloushallinnon dimensioiden arvon rajoitukset eroavat tasetilien ja tulostilien rajoitusten osalta, arvonlisäveron selvitys- ja kirjaamisprosessin aikana voi esiintyä virhe. Jotta tilirakenteita ei tarvitse muokata, voit ottaa käyttöön Täytä taloushallinnon dimensiot toteutuneihin valuuttaoikaisuvoittoihin/-tappiotileihin arvonlisäveron tilittämiseksi -ominaisuuden. Tämä ominaisuus pakottaa taloushallinnon dimensioiden aktivoimisen valuuttaoikaisuvoittojen/-tappioiden tileihin. 

## <a name="track-reporting-currency-tax-amount"></a>Raportointivaluutan verosumman seuraaminen

Veroon liittyviin taulukoihin lisättiin kolme uutta kenttää, jotta summia voidaan seurata raportointivaluutassa. Nämä kentät kuuluvat TAXUNCOMMITTED- ja TAXTRANS-taulukoihin:

- TaxAmountRep: verosumma raportointivaluuttana
- TaxBaseAmountRep: perussumma raportointivaluuttana
- TaxInCostPriceRep: vähennyskelvoton summa raportointivaluuttana

Jos vero on tallennettu vain TAXUNCOMMITTED-taulukkoon, mutta ei vielä kirjattu, järjestelmä laskee verosumman uudelleen raportointivaluuttana kirjauksen yhteydessä ja tallentaa sen TAXTRANS-taulukkoon.

Tämä julkaisu ei sisällä muutoksia raportteihin ja lomakkeisiin, joissa verosumma näytetään raportointivaluuttana. Raportteihin ja lomakkeisiin tehdyt muutokset toimitetaan tulevassa versiossa.



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a>Veron tilityksen automaattinen täsmäytys raportointivaluuttana

Jos veron tilitystä ei ole täsmäytetty raportointivaluuttana, esimerkiksi siksi että arvonlisäveron muuntamisen polku on Kirjanpitovaluutta tai vaihtokurssia muutetaan yhden veron tilityskauden aikana, järjestelmä luo automaattisesti kirjanpitomerkinnät ja oikaisee verosumman eron ja tekee siitä vastakirjauksen kirjanpidon asetuksissa määritetyn toteutuneen vaihtokurssin voitto-/tappiotilin mukaan.

Käytetään edellistä esimerkkiä tämän toiminnon esittelemiseksi ja oletetaan, että TAXTRANS-taulukon tiedot kirjausajankohtana ovat seuraavat.

| Arvonlisäveron muunnoksen parametrit | Tapahtumavaluutta (euroina) | Kirjanpitovaluutta (Yhdysvaltain dollareina) | Raportointivaluutta (Ison-Britannian puntina) | Veron valuutta (Ison-Britannian puntina) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Kirjanpitovaluutta             | 100                        | 111                       | 83                       | **83.25**          |
| Raportointivaluutta              | 100                        | 111                       | 83                       | **83**             |

Kun arvonlisäveron tilitysohjelma suoritetaan kuukauden lopussa, kirjanpitomerkintä on seuraava.
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a>Skenaario: arvonlisäveron muunnos = Kirjanpitovaluutta

| Päätili           | Tapahtumavaluutta (Ison-Britannian puntina) | Kirjanpitovaluutta (Yhdysvaltain dollareina) | Raportointivaluutta (Ison-Britannian puntina) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Maksettava/vastaanotettava vero | -83,25                     | -111                      | -83,25                   |
| Veron tilitys         | 83.25                      | 111                       | 83.25                    |
| Toteutunut voitto/tappio     | 0                          | 0                         | -0,25                    |
| Maksettava/vastaanotettava vero | 0                          | 0                         | 0.25                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a>Skenaario: arvonlisäveron muunnos = Raportointivaluutta


| Päätili           | Tapahtumavaluutta (Ison-Britannian puntina) | Kirjanpitovaluutta (Yhdysvaltain dollareina) | Raportointivaluutta (Ison-Britannian puntina) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Maksettava/vastaanotettava vero | -83                        | -110,67                   | -83                      |
| Veron tilitys         | 83                         | 110.67                    | 83                       |
| Toteutunut voitto/tappio     | 0                          | 0.33                      | 0                        |
| Maksettava/vastaanotettava vero | 0                          | -0,33                     | 0                        |



Lisätietoja on seuraavissa aiheissa:

- [Kaksoisvaluutta](dual-currency.md)
- [Arvonlisäveron yleiskatsaus](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
