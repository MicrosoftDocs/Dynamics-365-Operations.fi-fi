---
title: Ranskan Intrastat
description: Tässä artikkelissa on tietoja Intrastat-ilmoituksesta Ranskassa.
author: anasyash
ms.date: 11/30/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 2076649c7fff9f47b9c1fda62a103168b19bb973
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831802"
---
# <a name="french-intrastat"></a>Ranskan Intrastat

[!include[banner](../includes/banner.md)]

Ranskassa sijaitsevien yritysten, jotka on rekisteröity arvonlisäveroon ja jotka käyvät kauppaa muiden Euroopan unionin (EU) maiden kanssa, on ilmoitettava tavaroiden ja palvelujen vaihdot Ranskaan ja Ranskasta. Declaration d'exchanges de biens (Declaration of Trade in Goods, DEB) on EU-kauppaluettelon ja Intrastat-raportin yhdistelmä. Tämä raportti on toimitettava kuukausittain kaikesta yhteisön sisäisestä tavaroiden myynnistä.

Voit luoda DEB-raportin kummassa tahansa kahdesta sähköisestä tiedostomuodosta: SAISUNIC 330 tai INTRACOM.

Seuraavassa taulukossa näkyvät kentät, jotka sisältyvät ranskalaiseen Intrastat-ilmoitukseen SAISUNIC 330 -muodossa. Taulukko ilmaisee myös kunkin kentän raporttitasot. Kentässä voi olla seuraavat raporttitasot:

- **4** – Veroilmoitus.
- **1** – Tilastollinen vastaus.
- **5** – Tilastollinen vastaus lähetys- ja veroilmoitukseen sekä yhteistäyttö.

| Kenttä                       | Raporttitasot |
|-----------------------------|---------------|
| Viitekausi         | 4, 1, 5       |
| Ilmoituksen numero       | 4, 1, 5       |
| Rivin numero                 | 4, 1, 5       |
| Maan ISO-koodi (FR)       | 4, 1, 5       |
| Täydennyskoodi          | 4, 1, 5       |
| Siren-numero                | 4, 1, 5       |
| Asiakkaan ALV-koodi        | 4, 1, 5       |
| Suuntakoodi              | 4, 1, 5       |
| Tapahtumatyyppi            | 4, 1, 5       |
| Vaatimustaso            | 4, 1, 5       |
| Kauppatavarakoodi              | 1, 5          |
| Kansallinen NGP                | 1, 5          |
| Maakunta (Osasto)         | 1, 5          |
| Tapahtuman luonne       | 1, 5          |
| Alkuperämaa tai -alue      | 1, 5          |
| Alkuperämaa tai -alue - Tuonnit | 1, 5          |
| Lopullinen kohde + Viennit | 1, 5          |
| Laskun arvo               | 4, 1, 5       |
| Tilastollinen arvo           | 1, 5          |
| Nettopaino                  | 1, 5          |
| Lisäyksiköt            | 1, 5          |
| Välityskoodi              | 1, 5          |

Seuraavassa taulukossa näkyvät kentät, jotka sisältyvät ranskalaiseen Intrastat-ilmoitukseen INTRACOM-muodossa. Taulukko ilmaisee myös kunkin kentän raporttitasot. Kentässä voi olla seuraavat raporttitasot:

- **4** – Veroilmoitus.
- **1** – Tilastollinen vastaus.
- **5** – Tilastollinen vastaus lähetys- ja veroilmoitukseen sekä yhteistäyttö.

| Kenttä                       | Raporttitasot |
|-----------------------------|---------------|
| Suuntakoodi              | 4, 1, 5       |
| Ilmoituksen numero       | 4, 1, 5       |
| RIvin numero              | 4, 1, 5       |
| Siren                       | 4, 1, 5       |
| Maakunta (Osasto)         | 1, 5          |
| Välityskoodi              | 1, 5          |
| Alkuperämaa tai -alue           | 1, 5          |
| Tapahtuman luonne       | 1, 5          |
| Laskun arvo               | 4, 1, 5       |
| Toimitustavat           | 1, 5          |
| Tapahtumatyyppi            | 4, 1, 5       |
| Vaatimustaso            | 4, 1, 5       |
| Kauppatavarakoodi              | 1, 5          |
| Kansallinen NGP                | 1, 5          |
| Nettopaino                  | 1, 5          |
| Tilastollinen arvo           | 1, 5          |
| Lisäyksiköt            | 1, 5          |
| Alkuperämaa tai -alue - Tuonnit | 1, 5          |
| Lopullinen kohde + Viennit | 1, 5          |
| Asiakkaan ALV-koodi        | 4, 1, 5       |
| Täydennyskoodi          | 4, 1, 5       |
| Viitekausi         | 4, 1, 5       |

## <a name="set-up-intrastat"></a>Määritä Intrastat

- [Microsoft Dynamics Lifecycle Servicesin](https://lcs.dynamics.com/Logon/Index) jaetussa omaisuuskirjastossa voidaan ladata seuraavan Intrastat-ilmoituksen uusimmat sähköisen raportoinnin (ER) määritykset:

    - Intrastat-malli
    - Intrastat-raportti
    - Intrastat INTRACOM (FR)
    - Intrastat-SAISUNIC (FR)

    Lisätietoja on aiheessa [Lataa sähköisen raportoinnin määritykset Lifecycle Servicesistä](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

### <a name="set-up-vat-ids"></a>ALV-tunnusten määrittäminen

#### <a name="set-up-vat-codes-for-your-company"></a>Yrityksen ALV-koodien määrittäminen

1. Valitse **Vero** \> **Asetukset** \> **Arvonlisävero** \> **ALV-tunnukset**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Maa tai alue**-kentässä **FRA**.
4. Syötä **ALV-tunnus** -kenttään yrityksen ALV-numero.
5. Valitse **Organisaation hallinto** \> **Organisaatiot** \> **Yritykset** ja valitse yritys.
6. Määritä **Ulkomaankauppa ja logistiikka** -pikavälilehden **Intrastat**-osan **ALV-tunnuksen vienti** - ja **ALV-tunnuksen tuonti** -kentissä vaiheessa 4 luotu koodi.
7. Syötä yrityksesi verorekisteröintinumero **Verorekisteröinti**-pikavälilehden **Verorekisteröintinumero**-kenttään.

#### <a name="set-up-the-vat-ids-for-trading-partners"></a>Kauppakumppanien ALV-tunnusten määrittäminen

##### <a name="create-a-registration-type-for-the-company-code"></a>Yrityskoodin rekisteröintityypin luominen

Kaikille maille ja alueille, joissa yritys käy kauppaa, on määritettävä ALV-tunnuksen rekisteröintityyppi.

1. Valitse **Organisaation hallinto** \> **Yleinen osoitekirja** \> **Rekisteröintityypit** \> **Rekisteröintityypit**.
2. Luo ALV-tunnuksen rekisteröintityyppi valitsemalla toimintoruudussa **Uusi**.
3. Anna uuden rekisteröintityypin nimi **Määritä rekisteröintityypin tiedot** -valintaikkunan **Nimi**-kenttään. Anna nimeksi esimerkiksi **ALV-tunnus**.
4. Valitse **Maa tai alue**-kentässä kauppakumppanin alkuperämaa tai -alue.
5. Valitse **Luo**.

##### <a name="match-the-registration-type-with-a-registration-category"></a>Rekisteröintityypin ja rekisteröintiluokan kohdistaminen

1. Valitse **Organisaation hallinto** \> **Yleinen osoitekirja** \> **Rekisteröintityypit** \> **Rekisteröintiluokat**.
2. Luo rekisterityypin ja rekisteriluokan välille linkki valitsemalla toimintoruudussa **Uusi**.
3. Valitse ALV-tunnuksen rekisteröintityypiksi **ALV-tunnus**-rekisteröintiluokka.
4. Toista vaiheet 2 ja 3 myös muiden niitä maita ja alueita varten luotujen rekisteröintityyppien osalta, joissa yritys käy kauppaa.

##### <a name="set-up-the-vat-number-of-a-trading-partner"></a>Kauppakumppanin ALV-numeron määrittäminen

1. Valitse **Myyntireskontra** \> **Asiakkaat** \> **Kaikki asiakkaat**.
2. Valitse ruudukossa asiakas.
3. Valitse toimintoruudun **Asiakas**-välilehden **Rekisteröinti**-ryhmässä **Rekisteröintitunnukset**.
4. Luo rekisteröintitunnus valitsemalla **Rekisteröintitunnus**-pikavälilehdessä **Lisää**.
5. Valitse **Rekisteröintityyppi**-kentässä rekisteröintityyppi, joka luotiin yrityskoodia varten.
6. Anna **Rekisteröintinumero**-kentässä yrityksen ALV-numero.
7. Valitse toimintoruudussa **Tallenna** ja sulje sitten sivu.

Lisätietoja on kohdassa [Rekisteröintitunnukset](emea-registration-ids.md).

### <a name="set-up-foreign-trade-parameters"></a>Määritä ulkomaankaupan parametrit

1. Siirry kohtaan **Vero** \> **Asetukset** \> **Ulkomaankauppa** \> **Ulkomaankaupan parametrit**.
2. Valitse **Intrastat**-välilehden **Sähköisen raportoinnin** pikavälilehden **Tiedostomuodon määritys** -kentästä **Intrastat INTRACOM (FR)** tai **Intrastat SAISUNIC (FR)**.
3. Valitse **Raporttimuodon määritys** -kentässä **Intrastat-raportti**.
4. Valitse **Kauppatavarakoodihierarkia**-pikavälilehden **Luokkahierarkia**-kentästä **Intrastat**.
5. Valitse **Yleiset**-pikavälilehden **Tapahtumakoodi**-kentästä tavaroiden siirroissa käytettävä koodi.
6. Valitse **Hyvityslasku**-kentässä tavaroiden palautuksissa käytettävä koodi.
7. Valitse **Työntekijä**-kentässä yhteyshenkilön nimi.
8. Lisää **Yhteyshenkilö**-välilehdessä yhteyshenkilöä koskevat tiedot:

    - Syötä **Puhelin**-kenttään yhteyshenkilön puhelinnumero.
    - Syötä **Faksi**-kenttään yhteyshenkilön faksinumero.

9. Ilmoita **Maan tai alueen ominaisuudet** -välilehden **Maa tai alue** -kentässä kaikki maat tai alueet, joiden kanssa yritys käy kauppaa. Valitse kunkin EU-jäsenmaan kohdalla **Maa-/aluetyyppi**-kentässä **EU**, minkä jälkeen maa näkyy Intrastat-raportissa. Valitse Ranskan osalta **Maa-/aluetyyppi**-kentässä **Kotimaa**.

### <a name="set-up-compression-of-intrastat"></a>Intrastatin tiivistysasetukset

- Siirry kohtaan **Vero** \> **Asetukset** \> **Ulkomaankauppa** \> **Intrastatin pakkaus** ja valitse kentät, joita tulisi vertailla, kun Intrastat-tiedoista tehdään yhteenveto. Valitse Ranskan Intrastat-raporttiin seuraavat kentät:
 
    - Tilastomenettely
    - Alkuperämaa/-alue
    - Välitys
    - Korjaus
    - Maa tai alue
    - Alkuperä-/kohdemaa
    - Siirtosuunta
    - Lähettäjän maa tai alue
    - Tapahtumakoodi
    - Kauppatavara

### <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Intrastat-ilmoituksen tuoteparametrien määrittäminen

1. Siirry kohtaan **Tuotetietojen hallinta** \> **Tuotteet** \> **Vapautetut tuotteet**.
2. Valitse tuote ruudukossa.
3. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **Kauppatavara**-kentässä kauppatavarakoodi. Kauppatavaran nimi tulostetaan **Kauppatavaroiden kuvaus** -kenttään Intrastat-raportissa.
4. Valitse tuotteen alkuperämaa tai -alue **Alkuperä**-osan **Maa tai alue** -kenttä.
5. Anna **Varastonhallinta**-pikavälilehden **Nettopaino**-kentässä tuotteen paino kilogrammoina.

### <a name="ngp-codes"></a>NGP-koodit

DEB-raportissa tuotteiden koodaus koostuu seuraavista elementeistä:

- EU:n tariffi- ja tilastonimikköä edustava kahdeksannumeroinen CN8-tunnus.
- Yksinumeroinen kansallinen tai alueellinen Nomenclature Générale des Produits (NGP) -nimikekoodi, jos tarpeen.

Vuonna 2022 NGP koskee vain kolmenlaisia tuotteita:

- Jotkin nauta- lammas- ja vuohiperäiset tuotteet
- Sotilasvälineet
- Ranskalaiset viinit

NGP-koodit on määritettävä ja yhdistettävä niihin liittyviin tuotteisiin. **NGP-kenttä** määritetään sitten automaattisesti **Intrastat-kirjauskansio** -sivulla.

#### <a name="set-up-an-ngp-code"></a>NGP-koodin määrittäminen

1. Siirry kohtaan **Vero** \> **Asetukset** \> **Ulkomaankauppa** \> **NGP-koodit**.
2. Valitse toimintoruudussa **Uusi**.
3. Syötä **NGP**-kenttään yksinumeroinen koodi.
4. Anna koodi kuvaus **Kuvaus**-kentässä.

#### <a name="assign-an-ngp-code-to-a-product"></a>Liitä NGP-koodi tuotteeseen

1. Siirry kohtaan **Tuotetietojen hallinta** \> **Tuotteet** \> **Vapautetut tuotteet**.
2. Valitse tuote ruudukossa.
3. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **NGP**-kentästä haluamasi NGP-koodi.

### <a name="set-up-warehouse-parameters-for-the-intrastat-declaration"></a>Intrastat-ilmoituksen varastoparametrien määrittäminen

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Varasto** \> **Varastot**.
2. Valitse ensin varasto ja sitten **Osoitteet**-pikavälilehdessä **Lisää** tai **Muokkaa**.
3. Valitse varaston kaupunki valintaruudun **Kaupunki**-kentässä. Kaupungin osavaltiota tai provinssia käytetään DEB-raportin maakuntana.

### <a name="set-up-the-transport-method"></a>Kuljetustavan määrittäminen

1. Valitse **Vero** \> **Määritys** \> **Ulkomaankauppa** \> **Kuljetustapa**.
2. Valitse toimintoruudussa **Uusi**.
3. Anna yksilöivä koodi **Kuljetus**-kentässä. Ranskan yrityksissä käytetään yksinumeroisia kuljetuskoodeja.

### <a name="intrastat-journal"></a>Intrastat-kirjauskansio

Voit hallita EU-maiden kanssa käytävään ulkomaankauppaan liittyviä tapahtumia valitsemalla **Vero** \> **Ilmoitukset** \> **Ulkomaan kauppa** \> **Intrastat**. Lisätietoja on kohdassa [Intrastat-yleiskatsaus](emea-intrastat.md).

**NGP**-sarake koskee Ranskaa ja näyttää tuotteen NGP-koodin. Jos NGP ei ole sovellettavissa tuotteeseen, näytössä näkyy **0** (nolla). NGP-koodia voi muuttaa valitsemalla tapahtuman ja valitsemalla sitten **Yleiset**-välilehden **Koodit**-osan **NGP**-kentässä vaaditun NGP-koodin.

#### <a name="intrastat-transfer"></a>Intrastat-siirto

**Intrastat**-sivulla voit valita **Siirto**-kentässä automaattisesti siirrettäviksi yhteisön sisäistä kauppaa koskevat tiedot myyntitilauksesta, vapaatekstilaskuista, ostotilauksista, toimittajalaskuista, toimittajan tuotteen vastaanotoista, projektilaskuista ja siirtotilauksista. Vain ne asiakirjat siirretään, joissa on EU-maa tai -alue vastaanottajana (lähetyksille) tai vastaanottajana (saapuville).

Koska DEB-raportti on EU:n myyntiluettelon ja Intrastat-raportin yhdistelmä, se sisältää myös *kolmionmuotoiset* tapahtumat, joissa suoritetaan suora toimitus yhdestä EU-maasta (osapuoli A) toiseen EU-maahan (osapuoli C) ja ranskalainen yritys (osapuoli B) on kolmionmuotoisen kaupan keskellä.

#### <a name="generate-a-deb-intrastat-report"></a>Luo DEB (Intrastat) -raportti

1. Siirry kohtaan **Vero** \> **Ilmoitukset** \> **Ulkomaankauppa** \> **Intrastat**.
2. Valitse toimintoruudussa **Tuloste** \> **Raportti**.
3. Määritä seuraavat kentät **Intrastat-raportti**-valintaruudussa.

    | Kenttä            | kuvaus                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Päivämäärästä        | Valitse raportin aloituspäivä.                                                                                               |
    | Päivämäärään          | Valitse raportin päättymispäivä.                                                                                                 |
    | Luo tiedosto    | Määritä tämän vaihtoehdon arvoksi **Kyllä**, jos haluat luoda .txt-tiedoston.                                                                                 |
    | Tiedostonimi        | Kirjoita Intrastat-raporttisi .txt-tiedoston nimi.                                                                          |
    | Luo raportti  | Määritä tämän vaihtoehdon arvoksi **Kyllä**, jos haluat luoda .xml-tiedoston.                                                                                |
    | Raporttitiedoston nimi | Kirjoita tarvittava nimi.                                                                                                            |
    | Vain korjauksia | Määritä täksi asetukseksi **Kyllä**, jos haluat raportoida vain korjaukset. Määritä arvoksi **Ei**, kun haluat raportoida sekä normaalit tapahtumat että korjaukset.         |
    | Siirtosuunta        | Valitse **Saapumiset**, kun haluat raportin yhteisön sisäisistä saapumisista. Valitse **Lähetykset**, kun haluat raportin yhteisön sisäisistä lähetyksistä. |

4. Sulje **Intrastat-raportti**-valintaikkuna valitsemalla **OK**.
5. Valitse raporttitaso **Sähköisen raportin parametrit** -valintaikkunan **Parametrit**-pikavälilehden **Raporttitaso**-kentässä. Raporttitaso voi olla **1 – tilastollinen vastaus**, **4 – veroilmoitus** tai **5 – tilastollinen vastaus lähetys- ja veroilmoitukseen**.

## <a name="example"></a>Esimerkki

Seuraavassa esimerkissä kerrotaan, miten ranskalainen Intrastat määritetään ja DEB-raportti luodaan. Se käyttää **DEMF**-yritystä.

### <a name="preliminary-setup"></a>Alustavat asetukset

1. [Microsoft Dynamics Lifecycle Servicesin](https://lcs.dynamics.com/Logon/Index) jaetussa resurssikirjastossa voi ladata viimeisimmät versiot seuraavista elektronisen raportoinnin (ER) määrityksistä Intrastat-ilmoitusmuodoista:

    - Intrastat-malli
    - Intrastat-raportti
    - Intrastat INTRACOM (FR)

2. Määritä tuotehierarkia:

    1. Siirry kohtaan **Tuotetietojen hallinta** \> **Asetukset** \> **Luokat ja ominaisuudet** \> **Luokkahierarkiat**.
    2. Valitse ruudukossa **Intrastat**.
    3. Valitse toimintoruudun **Luokkahierarkia**-välilehden **Ylläpidä**-ryhmässä **Muokkaa**.
    4. Valitse toimintoruudussa **Uusi luokkasolmu**.
    5. Syötä **Nimi**-kenttään **Autres Libournais**.
    6. Syötä **Koodi**-kenttään **2204 21 42**.
    7. Valitse toimintoruudussa **Tallenna**.

### <a name="set-up-vat-ids"></a>ALV-tunnusten määrittäminen

#### <a name="set-up-vat-codes-for-your-company"></a>Yrityksen ALV-koodien määrittäminen

1. Valitse **Vero** \> **Asetukset** \> **Arvonlisävero** \> **ALV-tunnukset**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Maa tai alue**-kentässä **FRA**.
4. Syötä **ALV-tunnus**-kenttään **MS123456**.
5. Valitse **Organisaation hallinta** \> **Organisaatiot** \>**Yritykset** ja valitse **DEMF**.
6. Määritä **Ulkomaankauppa ja logistiikka** -pikavälilehden **Intrastat**-osan **ALV-tunnuksen vienti** - ja **ALV-tunnuksen tuonti** -kentissä vaiheessa 4 luotu koodi.
7. Syötä **Verorekisteröinti**-pikavälilehden **Verorekisterinumero**-kenttään **123456789**.

#### <a name="set-up-the-vat-ids-for-trading-partners"></a>Kauppakumppanien ALV-tunnusten määrittäminen

##### <a name="create-a-registration-type-for-the-company-code"></a>Yrityskoodin rekisteröintityypin luominen

1. Valitse **Organisaation hallinto** \> **Yleinen osoitekirja** \> **Rekisteröintityypit** \> **Rekisteröintityypit**.
2. Luo ALV-tunnuksen rekisteröintityyppi valitsemalla toimintoruudussa **Uusi**.
3. Anna **Määritä rekisteröintityypin tiedot** -valintaikkunan **Nimi**-kenttään **ALV-tunnus**.
4. Valitse **Maa tai alue**-kentässä **DEU**.
5. Valitse **Luo**.

##### <a name="match-the-registration-type-with-a-registration-category"></a>Rekisteröintityypin ja rekisteröintiluokan kohdistaminen

1. Valitse **Organisaation hallinto** \> **Yleinen osoitekirja** \> **Rekisteröintityypit** \> **Rekisteröintiluokat**.
2. Luo rekisterityypin ja rekisteriluokan välille linkki valitsemalla toimintoruudussa **Uusi**.
3. Valitse **DEU**-maan **ALV-tunnus**-rekisteröintityypiksi **ALV-tunnus**-rekisteröintiluokka.

##### <a name="set-up-the-customers-vat-registration-number"></a>Asiakkaan ALV-rekisteröintinumeron määrittäminen

1. Valitse **Myyntireskontra** \> **Asiakkaat** \> **Kaikki asiakkaat**.
2. Valitse ruudukossa **DE-016**.
3. Valitse toimintoruudun **Asiakas**-välilehden **Rekisteröinti**-ryhmässä **Rekisteröintitunnukset**.
4. Luo rekisteröintitunnus valitsemalla **Rekisteröintitunnus**-pikavälilehdessä **Lisää**.
5. Valitse **Rekisteröintityyppi**-kentässä **ALV-tunnus**.
6. Syötä **Rekisteröintinumero**-kenttään **DE9012**.
7. Valitse toimintoruudussa **Tallenna** ja sulje sitten sivu.
8. Valitse **Lasku ja toimitus** -pikavälilehden **Arvonlisävero**-osan **Verovapausnumero**-kentässä **DE9012**.

### <a name="set-up-foreign-trade-parameters"></a>Määritä ulkomaankaupan parametrit

1. Siirry kohtaan **Vero** \> **Asetukset** \> **Ulkomaankauppa** \> **Ulkomaankaupan parametrit**.
2. Valitse **Intrastat**-välilehden **Yleiset**-pikavälilehden **Tapahtumakoodi**-kentästä **11**.
3. Valitse **Sähköisen raportoinnin** pikavälilehden **Tiedostomuodon määritys** -kentästä **Intrastat INTRACOM (FR)**.
4. Valitse **Raporttimuodon määritys** -kentässä **Intrastat-raportti**.
5. Valitse **Kauppatavarakoodihierarkia**-pikavälilehden **Luokkahierarkia**-kentästä **Intrastat**.
6. Valitse **Työntekijä**-kentässä tietue.
7. Syötä **Yhteyshenkilö**-välilehden **Puhelin**-kenttään yhteyshenkilön puhelinnumero.
8. Syötä **Faksi**-kenttään yhteyshenkilön faksinumero.

### <a name="create-ngp-code"></a>NGP-koodin luominen

1. Siirry kohtaan **Vero** \> **Asetukset** \> **Ulkomaankauppa** \> **NGP-koodit**.
2. Valitse toimintoruudussa **Uusi**.
3. Syötä **NGP**-kenttään **8**.
4. Syötä **Kuvauksen nimi** -kenttään **NGP 8**.
5. Valitse toimintoruudussa **Tallenna**.

### <a name="set-up-product-information"></a>Tuotetietojen määrittäminen

1. Siirry kohtaan **Tuotetietojen hallinta** \> **Tuotteet** \> **Vapautetut tuotteet**.
2. Valitse ruudukossa **D0001**.
3. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **NGP**-kentässä **8**.
4. Valitse **Kauppatavara**-kentässä **2204 21 42**.
5. Valitse **Alkuperä**-osan **Maa tai alue** -kentässä **FRA**.
6. Anna **Nettopaino**-kentässä **2** **Varastonhallinta**-pikavälilehden **Painomitat**-osassa.
7. Valitse toimintoruudussa **Tallenna** ja sulje sitten sivu.
8. Valitse ruudukossa **D0003**.
9. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **Kauppatavara**-kentässä **100 200 30**.
10. Valitse **Alkuperä**-osan **Maa tai alue** -kentässä **DEU**.
11. Anna **Nettopaino**-kentässä **5** **Varastonhallinta**-pikavälilehden **Painomitat**-osassa.
12. Valitse toimintoruudussa **Tallenna**.

### <a name="set-up-regime-codes"></a>Hallinnon koodien määrittäminen

1. Valitse **Vero** \> **Asetukset** \> **Ulkomaankauppa** \> **Tilastomenettely**.
2. Valitse toimintoruudussa **Uusi**.
3. Syötä **Tilastomenettely**-kentässä **21**.
4. Syötä **Teksti 1** -kenttään **Hallinnon koodi 21**

### <a name="change-the-site-address"></a>Toimipaikan osoitteen muuttaminen

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Varasto** \> **Toimipaikat**.
2. Valitse ruudukossa **1**.
3. Valitse **Osoitteet**-pikavälilehdessä **Muokkaa**.
4. Valitse **Muokkaa osoitetta** -valintaikkunan **Maa tai alue** -kentässä **FRA**.
5. Valitse **OK**.
6. Valitse ensin **Varastonhallinta** \> **Asetukset** \> **Varasto** \> **Varastot** ja valitse sitten varasto.
7. Valitse **Osoitteet**-pikavälilehdessä **Lisää**.
8. Valitse **Uusi osoite** -valintaikkunan **Maa tai alue** -kentässä **FRA**.
9. Valitse **Paikkakunta**-kentässä **Bordeaux**.
10. Sulje valintaikkuna valitsemalla **OK**.

### <a name="set-up-a-transport-method"></a>Kuljetustavan määrittäminen

1. Valitse **Vero** \> **Määritys** \> **Ulkomaankauppa** \> **Kuljetustapa**.
2. Valitse toimintoruudussa **Uusi**.
3. Anna **Kuljetus**-kenttään arvo **3**.
4. Anna **Kuvaus**-kenttään arvo **Maantiekuljetus**.

### <a name="assign-a-transport-mode-to-a-mode-of-delivery"></a>Kuljetustavan määrittäminen toimitustavalle

1. Valitse **Hankinta** \> **Määritys** \> **Jakelu** \> **Toimitustavat**.
2. Valitse ruudukossa **50**.
3. Valitse **Ulkomaankauppa**-pikavälilehden **Kuljetus** -kentässä **3**.

### <a name="create-a-sales-order-with-an-eu-customer-that-includes-the-new-product"></a>Uuden tuotteen sisältävän myyntitilauksen luominen EU-asiakkaalle

1. Valitse **Myyntireskontra** \> **Tilaukset** \> **Kaikki myyntitilaukset**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Luo myyntitilaus** -valintaikkunan **Asiakas**-osan **Asiakastili**-kentässä **DE-016**.
4. Valitse **Osoite**-osan **Toimitusosoite**-kentästä plusmerkki (**+**), kun haluat luoda osoitteen.
5. Syötä **Uusi osoite**-valintaruudun **Kuvauksen nimi**-kenttään **Saksa**.
6. Valitse **Maa tai alue**-kentässä **DEU**.
7. Valitse **OK**.
8. Valitse **Luo uusi myyntitilaus**-valintaruudussa **OK**.
9. Valitse **Myyntitilauksen rivit** -pikavälilehden **Nimikkeen numero** -kentässä **0001**.
10. Valitse **Ulkomaankauppa**-välilehden **Rivien erittely** -pikavälilehden **Tilastomenettely**-kentässä **21**.
11. Valitse **Alkuperä**-kentässä **AL**.
12. Valitse toimintoruudussa **Tallenna**.
13. Varmista **Otsikko**-välilehden **Toimitus**-pikavälilehdessä, että **Toimitustapa**-kentässä on valittu **50**.
14. Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.
15. Valitse **Laskun kirjaus**-valintaikkunan **Parametrit**-pikavälilehden **Parametri**-osan **Määrä**-kentästä **Kaikki**. Valitse sitten **OK**, kun haluat kirjata laskun.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Tapahtuman siirtäminen Intrastat-kirjauskansioon ja tuloksen tarkistaminen

1. Siirry kohtaan **Vero** \> **Ilmoitukset** \> **Ulkomaankauppa** \> **Intrastat**.
2. Valitse toimintoruudussa **Siirto**.
3. Määritä **Intrastat (Siirto)** -valintaikkunan **Parametrit**-osassa **Myyntilasku**-asetuksen arvoksi **Kyllä**. Valitse sitten **OK**.
4. Lajittele tapahtumat **Päivämäärä**-kentän mukaan. Ylin tapahtuma on tulostapahtuma.

    ![Intrastat-sivulla olevan myyntitilauksen ilmaiseva rivi](media/intrastat_fr_1.png)

5. Saat lisätietoja valitsemalla ensin tapahtumarivin ja sitten **Yleiset**-välilehden.

    ![Myyntitilauksen tiedot Intrastat-sivun Yleiset-välilehdessä](media/intrastat_fr_2.png)

6. Valitse toimintoruudussa **Tuloste** \> **Raportti**.
7. Valitse **Intrastat-raportin** valintaikkunan **Parametrit**-pikavälilehden **Päivämäärä**-osasta luomasi myyntitilauksen kuukausi.
8. Määritä **Vientiasetukset**-osassa **Muodosta tiedosto** -asetuksen arvoksi **Kyllä**.
9. Kirjoita **Tiedostonimi**-kenttään vaadittu nimi.
10. Sulje **Intrastat-raportti**-valintaikkuna valitsemalla **OK**.
11. Valitse **Sähköisen raportin parametrit** -valintaikkunan **Parametrit**-pikavälilehden **Raporttitaso**-kentässä **5 – tilastollinen vastaus lähetys- ja veroilmoitukseen** ja tarkista raportti.

    ![Viennin Intrastatin Intracom-raportti](media/intrastat_fr_3.png)

12. Luodun Excel-raportin tarkistaminen

    ![Viennin Intrastat-raportti](media/intrastat_fr_4.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
