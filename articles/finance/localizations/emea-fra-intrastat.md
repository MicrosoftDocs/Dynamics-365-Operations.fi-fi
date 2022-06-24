---
title: Ranskan Intrastat
description: Tässä artikkelissa on tietoja Intrastat-ilmoituksesta Ranskassa.
author: anasyash
ms.date: 07/9/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: e86d7c8f28b1b3df0066a588d380965c21dc98a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887850"
---
# <a name="french-intrastat"></a>Ranskan Intrastat

[!include[banner](../includes/banner.md)]

Ranskassa sijaitsevien yritysten, jotka on rekisteröity arvonlisäveroon ja jotka käyvät kauppaa muiden Euroopan unionin (EU) maiden kanssa, on ilmoitettava tavaroiden ja palvelujen vaihdot Ranskaan ja Ranskasta. Declaration d'exchanges de biens (Declaration of Trade in Goods, DEB) on EU-kauppaluettelon ja Intrastat-raportin yhdistelmä. Tämä raportti on toimitettava kuukausittain kaikesta yhteisön sisäisestä tavaroiden myynnistä.

Voit luoda DEB-raportin kummassa tahansa kahdesta sähköisestä tiedostomuodosta: SAISUNIC 330 tai INTRACOM.

Seuraavassa taulukossa näkyvät kentät, jotka sisältyvät ranskalaiseen Intrastat-ilmoitukseen SAISUNIC 330 -muodossa. Taulukko ilmaisee myös kentän raporttitason. Kenttä voi olla **4** (yksinkertaistettu), **1** (täysi) tai molempia.

| **Kenttä**                   | **Raporttitaso** |
|-----------------------------|------------------|
| Viitekausi         | 4, 1              | 
| Ilmoituksen numero       | 4, 1              |
| Rivin numero                 | 4, 1              |
| Maan ISO-koodi (FR)       | 4, 1              | 
| Täydennyskoodi          | 4, 1              | 
| Siren-numero                | 4, 1              | 
| Asiakkaan ALV-koodi        | 4, 1              | 
| Suuntakoodi              | 4, 1              |
| Tapahtumatyyppi            | 4, 1              | 
| Vaatimustaso            | 4, 1              |
| Kauppatavarakoodi              | 1                | 
| Kansallinen NGP                | 1                | 
| Maakunta (Osasto)         | 1                |
| Tapahtuman luonne       | 1                | 
| Alkuperämaa tai -alue      | 1                | 
| Alkuperämaa tai -alue - Tuonnit | 1                | 
| Lopullinen kohde + Viennit | 1                | 
| Laskun arvo               | 4, 1              | 
| Tilastollinen arvo           | 1                |
| Nettopaino                  | 1                | 
| Lisäyksiköt            | 1                |
| Välityskoodi              | 1                | 

Seuraavassa taulukossa näkyvät kentät, jotka sisältyvät ranskalaiseen Intrastat-ilmoitukseen INTRACOM-muodossa.
Taulukko ilmaisee myös kentän raporttitason. Kenttä voi olla **4** (yksinkertaistettu), **1** (täysi) tai molempia.

| **Kenttä**                   | **Raporttitaso**   | 
|-----------------------------|--------------------|
| Koodi                        | 4, 1               | 
| Ilmoituksen numero       | 4, 1               |
| RIvin numero              | 4, 1               | 
| Siren                       | 4, 1               |
| Maakunta (Osasto)         | 1                  |          
| Välityskoodi              | 1                  |          
| Alkuperämaa tai -alue           | 1                  |            
| Tapahtuman luonne       | 1                  |             
| Laskun arvo               | 4, 1               |             
| Toimitustavat           | 1                  |           
| Tapahtumatyyppi            | 4, 1               |            
| Vaatimustaso            | 4, 1               |           
| Kauppatavarakoodi              | 1                  |            
| Kansallinen NGP                | 1                  |            
| Nettopaino                  | 1                  |            
| Tilastollinen arvo           | 1                  |            
| Lisäyksiköt            | 1                  |            
| Alkuperämaa tai -alue - Tuonnit | 1                  |            
| Lopullinen kohde + Viennit | 1                  |            
| Asiakkaan ALV-koodi        | 4, 1               |            
| Täydennyskoodi          | 4, 1               |           
| Viitekausi         | 4, 1               |         

### <a name="set-up-intrastat"></a>Määritä Intrastat

1.  Lataa [Microsoft Dynamics Lifecycle Servicesin (LCS)](https://lcs.dynamics.com/Logon/Index) jaetussa resurssikirjastossa viimeisimmät versiot seuraavista elektronisen raportoinnin (ER) määrityksistä Intrastat-ilmoitukselle:

    - Intrastat-malli
    - Intrastat-raportti
    - Intrastat INTRACOM (FR)
    - Intrastat-SAISUNIC (FR)

    Lisätietoja on aiheessa [Lataa sähköisen raportoinnin määritykset Lifecycle Servicesistä](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

2.  Siirry Dynamics 365 Financessa kohtaan **Vero** > **Asetukset** >  **Ulkomaankauppa** > **Ulkomaankaupan parametrit** ja seuraa näitä vaiheita:

    1. Valitse **Intrastat**-välilehden **Sähköisen raportoinnin** pikavälilehden **Tiedostomuodon määritys** -kentästä **Intrastat INTRACOM (FR)** tai **Intrastat SAISUNIC (FR)**.
    2. Valitse **Raporttimuodon määritys** -kentässä **Intrastat-raportti**.
    3. Valitse **Kauppatavarakoodihierarkia**-pikavälilehden **Luokkahierarkia**-kentästä **Intrastat**.
    4. Valitse **Yleiset**-pikavälilehden **Tapahtumakoodi**-kentästä tavaroiden siirroissa käytettävä koodi.
    5. Valitse **Hyvityslasku**-kentässä tavaroiden palautuksissa käytettävä koodi.
    6. Lisää vientiraportin erittelytaso **Viennin vaatimustaso** -kenttään. Valittu taso vaikuttaa riveihin, jotka näytetään raportissa. Lisätietoja on tämän artikkelin alussa olevissa taulukoissa.

3. Siirry kohtaan **Organisaation hallinto** > **Organisaatiot** > **Yritykset**, valitse yrityksesi ja seuraa sitten näitä vaiheita:

    1. Syötä NAF-koodisi **Rekisteröintinumerot**-pikavälilehden **NAF-koodi**-kenttään. Lisätietoja on kohdassa [FR-00003 NAF-koodit ja Siret-numerot](tasks/fr-00003-naf-codes-siret-numbers.md).
    2. Määritä **Ulkomaankaupan ja logistiikan** pikavälilehden **Intrastat**-osassa **ALV-vapautusnumeron vienti** - ja **ALV-vapautusnumeron tuonti** -kentät.
    3. Syötä yrityksesi verorekisteröintinumero **Verorekisteröinti**-pikavälilehden **Verorekisteröintinumero**-kenttään.

4. Kun haluat määrittää asiakkaille NAF-koodit ja verovapausnumerot, siirry kohtaan **Myyntireskontra** > **Asiakkaat** > **Kaikki asiakkaat** ja seuraa näitä vaiheita:

    1. Valitse asiakas.
    2. Syötä **Lasku ja toimitus** -pikavälilehden **Arvonlisävero**-osan **Verovapausnumero**-kenttään asiakkaan verovapausnumero.
    3. Syötä **Myynnin demografiset tiedot** -pikavälilehden **Ranskan Siret** -kenttään yrityksen Siret-numero.
    4. Syötä yrityksen NAF-koodi **NAF-koodi**-kenttään.
    5. Toista nämä vaiheet muille asiakkaille.

5. Kun haluat määrittää asiakkaille NAF-koodit ja verovapausnumerot, siirry kohtaan **Ostoreskontra** > **Toimittajat** > **Kaikki toimittajat** ja seuraa näitä vaiheita:

    1. Valitse toimittaja.
    2. Syötä **Lasku ja toimitus** -pikavälilehden **Arvonlisävero**-osan **Verovapausnumero**-kenttään toimittajan verovapausnumero.
    3. Syötä **Ostojen demografiset tiedot** -pikavälilehden **Ranskan Siret** -kenttään yrityksen Siret-numero.
    4. Syötä yrityksen NAF-koodi **NAF-koodi**-kenttään.
    5. Toista nämä vaiheet muille toimittajille.

6. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Intrastatin pakkaus** ja valitse sitten kentät, joita on vertailtava, kun Intrastat-tiedoista tehdään yhteenveto. Valitse Ranskan Intrastatille **Tilastomenettely**, **Alkuperäosavaltio**, **Alkuperämaa tai -alue**, **Toimitusehdot**, **Välitys**, **Korjaus**, **Maa tai alue**, **Alkuperä- tai kohdemaakunta**, **Suunta**, **Lähettäjän maa tai alue**, **Lähettäjän osavaltio**, **Osavaltio**, **Tapahtumakoodi** ja **Kauppatavara**.

7. Siirry kohtaan **Varastonhallinta** > **Asetukset** > **Varasto** > **Varastot**, valitse varasto ja seuraa sitten näitä vaiheita:

    1. Valitse **Osoitteet**-pikavälilehdeltä **Lisää** tai **Muokkaa**.
    2. Valitse varaston kaupunki valintaruudun **Kaupunki**-kentässä. Kaupungin osavaltiota käytetään DEB-raportin maakuntana.

### <a name="ngp-codes"></a>NGP-koodit

DEB-raportissa tuotteiden koodaus koostuu seuraavista elementeistä:

  - EU:n tariffi- ja tilastonimikköä edustava kahdeksannumeroinen CN8-tunnus.
  - Yksinumeroinen kansallinen tai alueellinen Nomenclature Générale des Produits (NGP) -nimikekoodi, jos tarpeen.

Vuonna 2021 NGP koskee vain kolmenlaisia tuotteita:

  - Jotkin nauta- lammas- ja vuohiperäiset tuotteet
  - Sotilasvälineet
  - Ranskalaiset viinit

 NGP-koodit on määritettävä ja yhdistettävä niihin liittyviin tuotteisiin. **NGP-kenttä** määritetään sitten automaattisesti **Intrastat-kirjauskansio** -sivulla.

#### <a name="set-up-an-ngp-code"></a>NGP-koodin määrittäminen

1. Siirry kohtaan **Vero** > **Asetukset** > **Ulkomaankauppa** > **NGP-koodit**.
2. Valitse toimintoruudussa **Uusi** ja luo NGP-koodi.
3. Syötä **NGP**-kenttään yksinumeroinen koodi.
4. Anna koodi kuvaus **Kuvaus**-kentässä.

#### <a name="assign-an-ngp-code-to-a-product"></a>Liitä NGP-koodi tuotteeseen

1. Valitse **Tuotetietojen hallinta** > **Tuotteet** > **Vapautetut tuotteet**.
2. Valitse tuote ruudukossa.
3. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **NGP**-kentästä haluamasi NGP-koodi.

## <a name="intrastat-journal"></a>Intrastat-kirjauskansio

Siirry kohtaan **Vero** > **Ilmoitukset** > **Ulkomaan** **kauppa** > **Intrastat**, kun haluat hallita tapahtumia, jotka liittyvät ulkomaankauppaan EU-maiden kanssa. Lisätietoja on kohdassa [Intrastat-yleiskatsaus](emea-intrastat.md).

**NGP**-saraketta käytetään vain Ranskalle. Se näyttää tuotteen NGP-koodin. Jos NGP ei ole sovellettavissa tuotteeseen, näytössä näkyy **0** (nolla). Voit muokata NGP-koodia. Valitse tapahtuma ja valitse sitten **Yleiset**-välilehden **Koodit**-osasta **NGP**-kentästä vaadittu NGP-koodi.

### <a name="intrastat-transfer"></a>Intrastat-siirto

**Intrastat**-sivulla voit valita **Siirto**-kentässä automaattisesti siirrettäviksi yhteisön sisäistä kauppaa koskevat tiedot myyntitilauksesta, vapaatekstilaskuista, ostotilauksista, toimittajalaskuista, toimittajan tuotteen vastaanotoista, projektilaskuista ja siirtotilauksista. Vain ne asiakirjat siirretään, joissa on EU-maa tai -alue vastaanottajana (lähetyksille) tai vastaanottajana (saapuville).

Koska DEB-raportti on EU:n myyntiluettelon ja Intrastat-raportin yhdistelmä, se sisältää myös *kolmionmuotoiset* tapahtumat, joissa suoritetaan suora toimitus yhdestä EU-maasta (osapuoli A) toiseen EU-maahan (osapuoli C) ja ranskalainen yritys (osapuoli B) on kolmionmuotoisen kaupan keskellä.

### <a name="generate-a-deb-intrastat-report"></a>Luo DEB (Intrastat) -raportti

1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
2. Valitse toimintoruudussa **Tuloste** > **Raportti**.
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

## <a name="example"></a>Esimerkki

Seuraavassa esimerkissä kerrotaan, miten ranskalainen Intrastat määritetään ja DEB-raportti luodaan. Se käyttää **DEMF**-yritystä.

1. Lataa [Microsoft Dynamics Lifecycle Servicesin (LCS)](https://lcs.dynamics.com/Logon/Index) jaetussa resurssikirjastossa viimeisimmät versiot seuraavista elektronisen raportoinnin (ER) määrityksistä Intrastat-ilmoituksen muodolle:

    - Intrastat-malli
    - Intrastat-raportti
    - Intrastat INTRACOM (FR)

2. Määritä tapahtumakoodi Financessa:

    1. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Tapahtumakoodit**.
    2. Valitse toimintoruudussa **Uusi**.
    3. Syötä **Tapahtumakoodi**-kenttään **11**.
    4. Syötä **Nimi**-kenttään **Osto tai Myynti**.
    5. Valitse toimintoruudussa **Tallenna**.

3.  Määritä tuotehierarkia:

    1. Valitse **Tuotetietojen hallinta** > **Määritys** > **Luokat ja määritteet** > **Luokkahierarkiat**.
    2. Valitse ruudukossa **Intrastat**. Valitse sitten toimintoruudun **Luokkahieratkia**-välilehden **Ylläpidä**-ryhmässä **Muokkaa**.
    3. Valitse toimintoruudussa **Uusi luokkasolmu**.
    4. Syötä **Nimi**-kenttään **Autres Libournais**.
    5. Syötä **Koodi**-kenttään **2204 21 42**
    6. Valitse toimintoruudussa **Tallenna**.

4. Siirry kohtaan **Vero** > **Asetukset** > **Ulkomaankauppa** > **Ulkomaankaupan parametrit** ja seuraa näitä vaiheita:

    1. Valitse **Intrastat**-välilehden **Yleiset**-pikavälilehden **Tapahtumakoodi**-kentästä **11**.
    2. Valitse **Sähköisen raportoinnin** pikavälilehden **Tiedostomuodon määritys** -kentästä **Intrastat INTRACOM (FR)**.
    3. Valitse **Raporttimuodon määritys** -kentässä **Intrastat-raportti**.
    4. Valitse **Kauppatavarakoodihierarkia**-pikavälilehden **Luokkahierarkia**-kentästä **Intrastat**.

5. NGP-koodin määrittäminen:

    1. Siirry kohtaan **Vero** > **Asetukset** > **Ulkomaankauppa** > **NGP-koodit**.
    2. Valitse toimintoruudussa **Uusi**.
    3. Syötä **NGP**-kenttään **8**.
    4. Syötä **Kuvauksen nimi** -kenttään **NGP 8**.
    5. Valitse toimintoruudussa **Tallenna**.

6. Liitä NGP-koodi tuotteeseen:

    1. Valitse **Tuotetietojen hallinta** > **Tuotteet** > **Vapautetut tuotteet**.
    2. Valitse ruudukossa **0001**.
    3. Valitse **Ulkomaankauppa**-pikavälilehden **NGP** -kentässä **8**.
    4. Valitse **Kauppatavara**-kentässä **2204 21 42**.
    5. Valitse toimintoruudussa **Tallenna**.

7. Luo myyntitilaus, joka sisältää uuden tuotteen:

    1. Valitse **Myyntireskontra** > **Tilaukset** > **Kaikki myyntitilaukset**.
    2. Valitse toimintoruudussa **Uusi**.
    3. Valitse **Luo** **myynti** **tilaus** -valintaikkunan **Asiakas**-osan **Asiakkaan** **tili**-kentässä **100001**.
    4. Valitse **Osoite**-osan **Toimitusosoite**-kentästä plusmerkki (**+**), kun haluat luoda osoitteen.
    5. Syötä **Uusi osoite**-valintaruudun **Kuvauksen nimi**-kenttään **Saksa**.
    6. Valitse **Maa tai alue**-kentässä **DEU**.
    7. Valitse **OK**.
    8. Valitse **Luo uusi myyntitilaus**-valintaruudussa **OK**.
    9. Valitse **Myynti** **tilauksen rivit** -pikavälilehden **Nimikkeen numero** kentässä **0001**.
    10. Valitse toimintoruudussa **Tallenna**.
    11. Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.
    12. Valitse **Laskun kirjaus**-valintaikkunan **Parametrit**-pikavälilehden **Parametri**-osan **Määrä**-kentästä **Kaikki**. Valitse sitten **OK**, kun haluat kirjata laskun.

8.  Luo DEB-raportti:

    1. Siirry kohtaan **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**:
    2. Toimintoruudussa. valitse **Siirrä**.
    3. Määritä **Intrastat (Siirto)** -valintaikkunan **Parametrit**-osassa **Myyntilasku**-asetuksen arvoksi **Kyllä**. Valitse sitten **OK**.
    4. Lajittele tapahtumat **Päivämäärä**-kentän mukaan. Ylin tapahtuma on tulostapahtuma. **NGP**-kenttä määritetään automaattisesti.
    5. Valitse toimintoruudussa **Tuloste** &gt; **Raportti**.
    6. Valitse **Intrastat-raportin** valintaikkunan **Parametrit**-pikavälilehden **Päivämäärä**-osasta luomasi myyntitilauksen kuukausi.
    7. Määritä **Vientiasetukset**-osassa **Muodosta tiedosto** -asetuksen arvoksi **Kyllä**.
    8. Kirjoita **Tiedostonimi**-kenttään vaadittu nimi.
    9. Valitse **OK** ja tarkista raportti.

