---
title: Loma- ja poissaolosuunnitelman luominen
description: Luo lomasuunnitelmat erilaisille lomatyypeille Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: AnnBe
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cb42860292c5e3e654917cf2f62b525993aa795a
ms.sourcegitcommit: 1edd3d4642f8fdc801b43b981b7c1a1c36ae0645
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/11/2020
ms.locfileid: "3796494"
---
# <a name="create-a-leave-and-absence-plan"></a>Loma- ja poissaolosuunnitelman luominen

Määritä loma- ja poissaolosuunnitelmat Dynamics 365 Human Resourcesissa jokaiselle tarjoamallesi lomatyypille. Loma- ja poissaolosuunnitelmat voidaan kerätä eri taajuuksilla, esimerkiksi vuosittain, kuukausittain tai kaksi kertaa kuussa. Voit myös määrittää suunnitelmat myönnettynä, jolloin yksi jaksotus tapahtuu tiettynä päivämääränä. Voit esimerkiksi luoda suunnitelman, joka myöntää kelluvia lomia vuosittain.

Porrastetun loman suunnitelmien avulla työntekijät voivat saada etuuksia, jotka perustuvat organisaatioon käytetyn ajan mukaan. Porrastetut suunnitelmat mahdollistavat automaattisen rekisteröinnin etutunteina.

Voit määrittää maksimisiirtosummat tai minimisaldot, jotta työntekijät voivat käyttää vain keräämiensä etujen tunteja.

Esimerkiksi porrastetun suunnitelman avulla voit myöntää uusille työntekijöille 80 tuntia maksettua lomaa (PTO). Tämän jälkeen voit myöntää 120 tuntia 60 kuukauden palvelun jälkeen.

Voit myös luoda sijaintiin perustuvia lomaetuja, kuten vain johdon etuuden tunnit.

## <a name="create-a-leave-plan"></a>Luo lomasuunnitelma

1. Valitse **Loma- ja poissaolo**-sivulla **Luo uusi suunnitelma**.

2. Kirjoita **Tiedot**-kohtaan suunnitelman **Nimi**, **Alkamispäivämäärä**, **Kuvaus** ja **Loman tyyppi**.

Jos toiminto **Määrittää useita lomatyyppejä yksittäiselle loma- ja poissaolosuunnitelmalle**, lomatyypit määritetään **Kertymäaikataulussa** **Yksityiskohtien**sijaan. Voit määrittää kullekin jaksotusaikataulutaulukon tietueelle lomatyypin. Kun tämä toiminto on käytössä, sinun on käytettävä uusia tietoentiteettejä integroinnissa ja muissa tilanteissa, joissa tarvitaan entiteettejä. 

Uudet entiteetit ovat seuraavat:

- Loma- ja poissaolopankin tapahtuma V2
- Loman ja poissaolon rekisteröinti V2
- Loma- ja poissaolosuunnitelman taso V2
- Loma- ja poissaolosuunnitelma V2
- Lomapoissaolopyyntö V2

 > [!IMPORTANT]
   > Kun olet ottanut tämän ominaisuuden käyttöön, sitä ei voi poistaa käytöstä.

3. Määritä jaksotukset **Jaksotukset** -välilehdessä. Jaksotukset määrittävät, milloin ja kuinka usein työntekijä palkitaan. Tässä vaiheessa määritetään, milloin jaksotuksia on tarkoitus myöntää ja miten lomaetuja jaetaan.

   1. Valitse avattavasta **Jaksotusväli**-ruudusta arvo:

      - Päivittäin
      - Viikoittain
      - Kaksi kertaa viikossa
      - Puolikuukausittain
      - Kuukausittain
      - Neljännesvuosittain
      - Puolivuosittain
      - Vuosittain
      - Ei ole

   2. Voit määrittää jaksotuskausien laskemiseen käytettävän aloituspäivän valitsemalla vaihtoehdon **Jaksotuskauden perusta** -pudotusvalikosta:

      | Kertymäkauden perusta | Kuvaus |
      | --- | --- |
      | **Suunnitelman aloituspäivämäärä** | Jaksotuskauden aloituspäivämäärä on suunnitelman käytettävissä oleva päivämäärä. |
      | **Työntekijäkohtainen päivämäärä** | Jaksotuskauden alkamispäivämäärä määräytyy työntekijätapahtuman mukaan:</br><ul><li>Mukautettu (kunkin yksittäisen rekisteröinnin jaksotuspäivämäärän peruste on määritettävä)</li><li>Vuosipäivän päivämäärä</li><li>Alkuperäinen työsuhteen alkamispäivämäärä</li><li>Ikälisäpäivä</li><li>Työntekijän muutettu aloituspäivämäärä</li><li>Työntekijän aloituspäivämäärä</li></ul> |

   3. Valitse vaihtoehto **Jaksotuspalkkion päivämäärä** -pudotusvalikosta:

      - **Jaksotuskauden loppupäivämäärä** – työntekijälle myönnetään palkkiona vapaa-aikaa palkkiokauden viimeisenä päivänä. Oikean määrän kertyminen edellyttää, että kertymisprosessi sisältää koko kauden. Jos jaksotuskausi on esimerkiksi 1. tammikuuta 2020 – 31. tammikuuta 2020, sinun on suoritettava kertymä 1. helmikuuta 2020 ja sisällyttääksesi tammikuun.

      - **Jaksotuskauden aloituspäivämäärä** – työntekijälle myönnetään palkkiona vapaa-aikaa palkkiokauden ensimmäisenä päivänä.

   4. Valitse vaihtoehto **Jaksotuskäytäntö rekisteröitäessä** -pudotusvalikosta. Tämä arvo määrittää, miten jaksotus lasketaan, kun työntekijä rekisteröityy jaksotuskauden keskelle.

      - **Suhteellisesti jaettu** – Päivien välinen ero määritetään rekisteröitymis- ja aloituspäivämäärän välisen eron perusteella. Kyseistä eroa käytetään, kun kertymiä käsitellään.

      - **Täysi kertymä** – tasoon perustuva täysi kertymä myönnetään palkkiona ensimmäisen kertymäkäsittelyn aikana.

      - **Ei kertymää** – jaksotusta ei myönnetä palkkiona ennen seuraavaa kertymäkautta.

   5. Valitse vaihtoehto **Jaksotuskäytäntö rekisteröintiä peruessa** -pudotusvalikosta. Tämä arvo määrittää, miten jaksotus lasketaan, kun työntekijä peruu rekisteröinnin jaksotuskauden keskelle.

      - **Suhteellisesti jaettu** – Päivien välinen ero määritetään rekisteröitymis- ja aloituspäivämäärän välisen eron perusteella. Kyseistä eroa käytetään, kun kertymiä käsitellään.

      - **Täysi kertymä** – tasoon perustuva täysi kertymä myönnetään palkkiona ensimmäisen kertymäkäsittelyn aikana.

      - **Ei kertymää** – jaksotusta ei myönnetä palkkiona ennen seuraavaa kertymäkautta.

4. Määritä jaksotusaikataulu **Jaksotusaikataulu** -välilehdessä. Jaksotusaikataulu määrittää seuraavat asiat:

   - Työntekijän kertyneen ajan poistaminen käytöstä
   - Mitä määriä työntekijä kerryttää
   - Mitkä määrät siirtyvät eteenpäin

   Voit luoda tasoja myöntääksesi vapaa-aikaa palkkiona eri perustein.

   Jos sinulla on tuntihinnalla työskenteleviä työntekijöitä, voit myöntää poissaoloja työtuntien mukaan virkaiän sijasta organisaatiossasi. Työtuntitiedot tallennetaan yleensä aika- ja läsnäolojärjestelmään. Voit tuoda aika- ja läsnäolojärjestelmästä tehdyt säännölliset ja ylityötunnit sekä käyttää niitä työntekijän palkkion perustana.
   
    1. Valitse vaihtoehto **Jaksotustyyppi**-pudotusvalikosta:

      - **Kuukauden palvelu** -perustaa jaksotussuunnitelman kuukausien palvelun.

      - **Työtunnit** -suoriteperusteisen aikataulun perustana työtunteina. Lisätietoja jaksotusten käyttämisestä työtuntien osalta on kohdassa [Työajan jaksottaminen työtuntien perusteella](hr-leave-and-absence-plans.md?accrue-time-off-based-on-hours-worked).

      Lisätietoja jaksotussaldoista on kohdassa [Työajan jaksottaminen työtuntien perusteella](hr-leave-and-absence-plans.md?enrollments-and-balances).

    2. Syötä arvot jaksotusaikataulutaulukkoon:

      - **Työkuukaudet** - Kuinka monta kuukautta työntekijän on vähintään oltava töissä, jotta heille voi syntyä kertymiä. Jos et tarvitse vähimmäisarvoa, määritä arvoksi 0.

      - **Työtunnit** - Kuinka monta tuntia työntekijän on tehtävä töitä kertymäkaudella, jotta hänelle voi syntyä kertymiä. Jos et tarvitse vähimmäisarvoa, määritä arvoksi 0.

      - **Kertymäsumma** - Tuntien tai päivien määrä, joka työntekijöille kertyy kunkin kauden aikana. Kausi perustuu kertymäväliin.

      - **Vähimmäissaldo** - Voit käyttää negatiivista arvoa, jos työntekijät pyytämä loma-aika ylittää heidän käytössään olevan loma-ajan.

      - **Suurin siirrettävä** - Kertymäprosessi oikaisee enimmäissiirtokirjauksen saldon ylittävät lomasaldot aloituspäivämäärän vuosipäivänä.

      - **Myönnetty summa** - Työntekijöille aluksi myönnetty tuntien tai päivien määrä, kun rekisteröityvät lomasuunnitelmaan ensimmäisen kerran. Summaa ei jaksoteta kullekin kertymäkaudelle.
      
Jos toiminto **Määritä useita lomatyyppejä yksittäiselle loma- ja poissaolosuunnitelmalle** on käytössä, valitse vaihtoehto **Lomatyyppi**-kohdasta. 

   > [!IMPORTANT]
   > Kun olet ottanut tämän ominaisuuden käyttöön, sitä ei voi poistaa käytöstä.

Jos **Käytä kokopäiväistä vastaavuutta** -toiminto on käytössä, henkilöstöhallinnossa käytetään kokopäiväistä vastaavuutta (FTE), joka on määritetty toimipaikan työntekijän kertymän jaksottamisen yhteydessä. Jos esimerkiksi FTE on 0,5 ja jaksotussumma on 10, työntekijän jaksotus on 5. Voit käyttää tätä toimintoa vain, jos otat käyttöön useita lomatyyppejä.  

5. Valitse **Tallenna**.

## <a name="accrue-time-off-based-on-hours-worked"></a>Jaksottaminen tehtyjen työtuntien perustella

Jos sinulla on tuntihinnalla työskenteleviä työntekijöitä, voit myöntää poissaoloja työtuntien mukaan virkaiän sijasta organisaatiossasi. Työtuntitiedot tallennetaan yleensä aika- ja läsnäolojärjestelmään. Voit tuoda aika- ja läsnäolojärjestelmästäsi tehdyt säännölliset ja ylityötunnit sekä käyttää sitä työntekijän palkkion perustana.

Kun valitset työtunnit jaksotustyypiksi, voit käyttää kahdenlaisia tunteja jaksotukseen: tavallisia työtunteja tai ylityötunteja. Työtuntiperusteisten suunnitelmien jaksotuksen käsittelyssä käytetään jaksotusväliä ja jaksotuskausiperustaa määrittämään jaksotettavat tunnit.

### <a name="annual-accrual-frequency"></a>Vuotuinen jaksotusväli

| Jaksotuksen myöntöpäivämäärä    | Työtuntitaso    | Jaksotussumma        | Työtuntien päivämäärät   | Todelliset työtunnit| Palkkio               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31.12.2018            | 2080                 | 144                   | 1.1.2018–31.12.2018  | 2085                | 144                 |        
| 31.12.2018            | 2080                 | 144                   | 1.1.2018–31.12.2018  | 2 000                | 0                 |


### <a name="monthly-accrual-frequency"></a>Kuukausittainen jaksotusväli

| Jaksotuksen myöntöpäivämäärä    | Työtuntitaso    | Jaksotussumma        | Työtuntien päivämäärät   | Todelliset työtunnit| Palkkio               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31.8.2018             | 160                  | 12                    | 1.8.2018–31.8.2018   | 184                 | 12                  |        
| 31.8.2018             | 160                  | 3                     | 1.8.2018–31.8.2018   | 184                 | 3                   |

### <a name="semi-monthly-accrual-frequency"></a>Puolikuukausittainen jaksotusväli

| Jaksotuksen myöntöpäivämäärä    | Työtuntitaso    | Jaksotussumma        | Työtuntien päivämäärät   | Todelliset työtunnit| Palkkio               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31.8.2018             | 80                   | 6                     | 16.8.2018–31.8.2018  | 81                  | 6                  |        
| 31.8.2018             | 80                   | 6                     | 16.8.2018–31.8.2018  | 75                  | 0                   |

### <a name="weekly-accrual-frequency"></a>Viikoittainen jaksotusväli

| Jaksotuksen myöntöpäivämäärä    | Työtuntitaso    | Jaksotussumma        | Työtuntien päivämäärät   | Todelliset työtunnit| Palkkio               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31.8.2018             | 40                   | 3                     | 27.8.2018–31.8.2018  | 42                  | 3                  |        
| 31.8.2018             | 40                   | 3                     | 27.8.2018–31.8.2018  | 35                  | 0                   |

### <a name="employee-assigned-leave-plans"></a>Työntekijälle määritetyt lomasuunnitelmat

Työntekijälle määritetyissä loma-suunnitelmissa työtuntisuunnitelman tasoperuste ja tyyppi näkyvät. Aktiivisille suunnitelmille näytetään viitteenä sen hetkisen päivämäärän jaksotuskausien todelliset työtunnit.

### <a name="loading-data"></a>Ladataan tietoja

Voit tuoda todelliset tunnit käyttämällä tiedonhallinnan **Lomien ja poissaolojen vapaatuntien** yksikköä. Jos käytät työaikakalentereita, tuonti vahvistaa, että nämä tavalliset työtunnit eivät ylitä kalenterin määrittämien ajoitettujen tuntien määrää päivässä. Tuonti vahvistaa myös, että tietyn päivän työtunnit eivät ylitä 24:ää. 

Tarvitset seuraavia tietoja, jotta voit tuoda lomien jaksotusprosessissa käytettävät todelliset tunnit:

- Henkilöstönumero 
- Työn päivämäärä
- Laji
- Tunnit

Yhteen päivään voi liittyä vain yksi tyyppi kutakin.

| Henkilöstönumero       | Työn päivämäärä           | Laji                  | Tunnit                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 6.8.2018             | Säännöllinen               | 8                    |       
| 000337                | 7.8.2018             | Säännöllinen               | 8                    |
| 000337                | 7.8.2018             | Ylityö              | 3                    |
| 000337                | 8.8.2018             | Säännöllinen               | 8                    |
| 000337                | 7.8.2018             | Säännöllinen               | 8                    |
| 000337                | 9.8.2018             | Säännöllinen               | 8                    |

## <a name="enrollments-and-balances"></a>Rekisteröitymiset ja saldot

### <a name="enrollment-date"></a>Rekisteröintipäivä

Rekisteröintipäivä määrittää, milloin työntekijä voi aloittaa vapaa-ajan keräämisen. Esimerkiksi työntekijä, joka on rekisteröitynyt lomasuunnitelmaan 15.6.2018, voi aloittaa vapaa-ajan keräämisen vasta 15.6.2018.

### <a name="current-balance"></a>Nykyinen saldo

Nykyisen saldo on se loman määrä, joka on vapaa-aikapyyntöjen käytettävissä. Tämä määrä sisältää kertymät, hyväksytyt pyynnöt ja oikaisut kuluvaan päivämäärään mennessä.

### <a name="current-balance-examples"></a>Nykyiseen saldoon liittyviä esimerkkejä

#### <a name="annual-plan"></a>Vuosisuunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Rekisteröintipäivä | Kertymäväli | Kertymäkauden perusta | Palkkion jaksotuspäivämäärä    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Vuosittainen            | Suunnitelman aloituspäivämäärä      | Kertymäkauden loppupäivämäärä |

Kertymät käsitellään 1. tammikuuta 2019 (1.1.2019), jotta siihen sisältyy koko kausi.

**Tulokset**

| Jaksotussumma | Vähimmäissaldo | Enimmäissiirtokirjaus | Pyydetty määrä | Nykyinen saldo (1.1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Nykyinen saldo (160) = kertynyt määrä (200) – pyydetty määrä (40)

#### <a name="semimonthly-plan"></a>Kaksi kertaa kuussa -suunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Rekisteröintipäivä | Kertymäväli | Kertymäkauden perusta | Palkkion jaksotuspäivämäärä    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaksi kertaa kuussa       | Suunnitelman aloituspäivämäärä      | Kertymäkauden loppupäivämäärä |

Kertymät käsitellään 1. toukokuuta 2018 (1.5.2018), jotta siihen sisältyy koko kausi.

**Tulokset**

| Jaksotussumma | Vähimmäissaldo | Enimmäissiirtokirjaus | Pyydetty määrä | Nykyinen saldo (1.1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Nykyinen saldo (22) = kertynyt määrä (5 × 6) – pyydetty määrä (8)

#### <a name="monthly-plan"></a>Kuukausisuunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Rekisteröintipäivä | Kertymäväli | Kertymäkauden perusta | Palkkion jaksotuspäivämäärä    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaksi kertaa kuussa       | Suunnitelman aloituspäivämäärä      | Kertymäkauden loppupäivämäärä |

Kertymät käsitellään 1. toukokuuta 2018 (1.5.2018), jotta siihen sisältyy koko kausi.

**Tulokset**

| Jaksotussumma | Vähimmäissaldo | Enimmäissiirtokirjaus | Pyydetty määrä | Nykyinen saldo (1.1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Nykyinen saldo (7) = kertynyt määrä (5 × 3) – pyydetty määrä (8)

### <a name="forecasted-balance"></a>Ennustettu saldo

*Ennustettu saldo* on se loman määrä, joka on käytettävissä tulevana ajankohtana. Kertymät ja siirtokirjausten oikaisut ennustetaan kyseiseen päivämäärään saakka.

Henkilöstöhallinnossa käytetään seuraavaa kaavaa:

Maanantain ennustettu saldo = nykyinen saldo – pyynnöt + kertymät – siirtokirjausoikaisu

### <a name="forecasted-balance-examples"></a>Esimerkkejä ennustetusta saldosta

#### <a name="annual-plan"></a>Vuosisuunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Rekisteröintipäivä | Kertymäväli | Kertymäkauden perusta | Palkkion jaksotuspäivämäärä    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Vuosittainen            | Suunnitelman aloituspäivämäärä      | Kertymäkauden loppupäivämäärä |

Kertymät käsitellään 15. helmikuuta 2019 (15.2.2019), jotta siihen sisältyy koko kausi.

**Tulokset**

| Jaksotussumma | Vähimmäissaldo | Enimmäissiirtokirjaus | Nykyinen saldo | Ennustettu saldo (15.2.2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Ennustettu saldo (40) = kertynyt määrä (20) + nykyinen saldo (40) – siirtokirjausoikaisu (20)

#### <a name="semimonthly-plan"></a>Kaksi kertaa kuussa -suunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Rekisteröintipäivä | Kertymäväli | Kertymäkauden perusta | Palkkion jaksotuspäivämäärä    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaksi kertaa kuussa       | Suunnitelman aloituspäivämäärä      | Kertymäkauden loppupäivämäärä |

Kertymät käsitellään 15. helmikuuta 2019 (15.2.2019), jotta siihen sisältyy koko kausi.

**Tulokset**

| Jaksotussumma | Vähimmäissaldo | Enimmäissiirtokirjaus | Nykyinen saldo | Ennustettu saldo (15.2.2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Ennustettu saldo (35) = kertynyt määrä (5 × 3) + nykyinen saldo (40) – siirtokirjausoikaisu (20)

#### <a name="monthly-plan"></a>Kuukausisuunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Rekisteröintipäivä | Kertymäväli | Kertymäkauden perusta | Palkkion jaksotuspäivämäärä    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaksi kertaa kuussa       | Suunnitelman aloituspäivämäärä      | Kertymäkauden loppupäivämäärä |

Kertymät käsitellään 15. helmikuuta 2019 (15.2.2019), jotta siihen sisältyy koko kausi.

**Tulokset**

| Jaksotussumma | Vähimmäissaldo | Enimmäissiirtokirjaus | Nykyinen saldo | Ennustettu saldo (15.2.2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Ennustettu saldo (30) = kertynyt määrä (10 × 1) + nykyinen saldo (40) – siirtokirjausoikaisu (20)

### <a name="proration-balance-examples"></a>Esimerkkejä jaetusta saldosta

#### <a name="prorated-monthly-plan"></a>Jaettu kuukausisuunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Kertymäväli | Kertymäkauden perusta |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Kuukausittain           | Suunnitelman aloituspäivämäärä      |

**Tulokset**

| Työntekijä            | Työkuukaudet | Rekisteröintipäivä | Aloituspäivämäärä | Jaksotussumma | Kertymän käsittely | Tase |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2,53    |

#### <a name="full-accrual-monthly-plan"></a>Täyden kertymän kuukausisuunnitelma

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Kertymäväli | Kertymäkauden perusta |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Kuukausittain           | Suunnitelman aloituspäivämäärä      |

**Tulokset**

| Työntekijä            | Työkuukaudet | Rekisteröintipäivä | Aloituspäivämäärä | Jaksotussumma | Kertymän käsittely | Tase |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>Ei kertymää kuukausisuunnitelmassa

**Suunnitelman asetukset**

| Suunnitelman aloituspäivämäärä | Kertymäväli | Kertymäkauden perusta |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Kuukausittain           | Suunnitelman aloituspäivämäärä      |

**Tulokset**

| Työntekijä            | Työkuukaudet | Rekisteröintipäivä | Aloituspäivämäärä | Jaksotussumma | Kertymän käsittely | Tase |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3.00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1.00           | 9/1/2018        | 2.00    |

## <a name="see-also"></a>Lisätietoja

- [Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)
- [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md)
- [Jaksota loma- ja poissaolosuunnitelmia](hr-leave-and-absence-accrue.md)
