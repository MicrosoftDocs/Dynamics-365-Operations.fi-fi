---
title: Kustannusten koontikäytäntö ja yleiskustannuslaskenta
description: Tässä ohjeaiheessa kerrotaan, miten määritetään oikea taso toissijaisille kustannustasoille ja luodaan organisaation raportoinnin ja kustannusten jäljitettävyyden mukaiset kustannusten koontisäännöt.
author: AndersGirke
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostRollupRule, CAMDimensionHierarchy, CAMOverheadRatePolicy
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f86529359f548bf48fdef8817bd2e2260235561cce57cac28158739687ade2c1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779953"
---
# <a name="cost-rollup-policy-and-overhead-calculation"></a>Kustannusten koontikäytäntö ja yleiskustannuslaskenta 

[!include [banner](../includes/banner.md)]

Kustannuslaskennan avulla saat tietoja siitä, miten voit kustannusvirta liittyy organisaatiossa toimitettaviin tuotteisiin ja palveluihin. Kustannusten läpinäkyvyyden saavuttamiseksi kustannukset on kohdistettava kustannusobjektien välillä soveltuvan kohdistusperusteen mukaisesti. Oletusarvoisesti ensisijaisen kustannustason kustannukset kohdistetaan, mikä on toivottavaa joissakin tilanteissa. Tästä on kuitenkin joitakin seurauksia, jotka on otettava huomioon.

-   Oheiskustannusobjektien ensisijaisen kustannustason saldoksi tulee nolla yleiskustannuslaskennan jälkeen.

-   Yleiskustannuslaskenta voi luoda erittäin suuren määrän kustannusmerkintöjä.

-   Kustannusobjektien välistä kustannusvirtaa ei voi jäljittää.

Nämä vaikutukset voi välttää määrittämällä kustannusten kohdistuksen kustannuslaskennassa organisaation johdon raportointivaatimusten mukaisiksi. Tässä ohjeaiheessa kerrotaan, miten määritetään oikea taso toissijaisille kustannustasoille ja luodaan organisaation raportoinnin ja kustannusten jäljitettävyyden mukaiset kustannusten koontisäännöt.

> [!NOTE]
> Voit määrityksiä, jos raportointivaatimukset muuttuvat.

## <a name="example-of-cost-rollup-policy-setup"></a>Esimerkki kustannusten koontikäytännön asetuksista

Kuvittele, että organisaation rakenteessa on neljä kustannuspaikkaa.

![Organisaatiorakenteen esimerkki.](./media/dimension-hierarchy-org.png)

**Kustannusobjektin dimensio**

| Kustannuspaikat | kuvaus          |
|--------------|-----------|
| CC001        | Henkilöstöhallinto        |
| CC002        | Myyntitiedot   |
| CC003        | Kokoonpano  |
| CC004        | Pakkaus |

**Kustannustason dimensio**

| Kustannustasot | kuvaus | Laji    |
|---------------|-------------|---------|
| 1001          | Sähkö | Ensisijainen |
| 1002          | Palkat    | Ensisijainen |
| 1003          | Mainonta | Ensisijainen |

Organisaation raportointivaatimukset täyttävä dimension hierarkia voidaan määrittää seuraavasti.

**Dimension hierarkiatiedot**

| Dimensiohierarkian nimi | Dimensio    | Dimensiohierarkiatyypin nimi      | Käyttöoikeusluettelohierarkia |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisaatio             | Kustannuspaikat | Dimension luokitteluhierarkia | Nro                    |

**Dimensiohierarkia**

|    &nbsp;    | Dimension jäsenalueet | &nbsp;              |
|--------------|-------------------------|---------------------|
| **Solmukohdat**        | **Lähtödimension jäsen**   | **Kohdedimension jäsen** |
| Organisaatio |                         |                     |
| &nbsp;&nbsp;Hallinto             |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Myyntitiedot              | CC001                   | CC001               |
| &nbsp;&nbsp;&nbsp;&nbsp;Henkilöstöhallinto               | CC002                   | CC002               |
| &nbsp;&nbsp;Tuotanto               |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakkaus              | CC003                   | CC003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Kokoonpano             | CC004                   | CC004               |

Käytännön vaatimukset täyttävä dimension hierarkia voidaan määrittää seuraavasti.

**Dimension hierarkiatiedot**

| Dimensiohierarkian nimi | Dimensio     | Dimensiohierarkiatyypin nimi      |
|--------------------------|---------------|------------------------------------|
| Tuloslaskelma  | Kustannustasot | Dimension luokitteluhierarkia |

**Dimensiohierarkia**

|      &nbsp;             | Dimension jäsenalueet |      &nbsp;         |
|-------------------------|-------------------------|---------------------|
| Solmukohdat                   | Lähtödimension jäsen   | Kohdedimension jäsen |
| Tuloslaskelma |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Ensisijainen kustannus                    | 10 001                   | 10003               |

Kustannusobjektin mukainen kustannusmerkinnän saldo näyttää seuraavalta kirjanpidon merkintöjen käsittelyn jälkeen.

|      &nbsp;          | **Kustannusobjekti** | &nbsp;    |  &nbsp;   |  &nbsp;   | **Yhteensä**     |
|----------------------|-----------------|-----------|-----------|-----------|---------------|
| **Kustannustaso**     | **CC001**       | **CC002** | **CC003** | **CC004** |               |
| **1001 Sähkö** | 100,00          | 200 000    | 6.000,00  | 2.000,00  | **8.300,00**  |
| **1002 Palkat**    | 10.000,00       | 10.000,00 | 8.000,00  | 6.500,00  | **34.500,00** |
| **1003 Mainonta** | 0,00            | 4.000,00  | 0,00      | 0,00      | **4.000,00**  |
|                      | 10.100,00       | 14.200,00 | 14.000,00 | 8.500,00  | **46.800,00** |

**Tilastodimensio**

| Tilastoelementit |    kuvaus   |
|----------------------|------------------|
| SE-1                 | HR-palvelut      |
| SE-2                 | Taloushallinnon palvelut |

Kustannusobjekti CC001 HR liittyy useaan kustannusobjektin henkilöstöpalveluihin.

Henkilöstöpalveluja kulutetaan seuraavan suuruusjakelun mukaan.

| Kustannusobjekti | kuvaus |   HR-palvelut |
|-------------|-------------|----|
| CC002       | Myyntitiedot     | 35 |
| CC003       | Kokoonpano    | 55 |
| CC004       | Pakkaus   | 10 |

Kustannusobjekti CC002 Taloushallinto liittyy useaan kustannusobjektiin.

Taloushallinnon palveluja kulutetaan seuraavan suuruusjakelun mukaan.

| Kustannusobjekti |   kuvaus    |  Taloushallinnon palvelut   |
|-------------|------------------|----|
| CC003       | Kokoonpano         | 65 |
| CC004       | Pakkaus        | 35 |

Kustannusten kohdistuskäytännöt voidaan määrittää seuraavasti.

| Käytännön nimi | kuvaus     | Kustannusobjektin dimensiohierarkia | Tilastodimensio | Kustannustason dimensio |
|-------------|-----------------|---------------------------------|-----------------------|------------------------|
| 2017        | Kustannusten kohdistus | Organisaatio                    | Tilastoelementit  | Kustannustasot          |

Kustannusten kohdistussäännöt voidaan määrittää seuraavasti.

| Kustannusobjektin dimensiohierarkiasolmu | Kustannustoiminta | Kohdistusperuste        |
|--------------------------------------|---------------|------------------------|
| CC001                                | Yhteensä         | **Henkilöstöpalvelut**        |
| CC002                                | Yhteensä         | **Taloushallinnon palvelut** |

## <a name="brhow-cost-flows-between-cost-centers"></a><br>Kustannuspaikkojen välinen kustannusvirta 

Jos haluat tietää minkälainen on organisaation kustannuspaikkojen välinen kustannusvirta, voit luoda kullekin kustannuspaikalle **Toissijainen**-tyypin kustannustasoja. Näitä kustannustasoja voi sitten käyttää siirtämään saldoja kustannuspaikkojen välillä yleiskustannuslaskennan aikana.

Kustannustason dimension jäsenet voidaan määrittää seuraavasti.

| Kustannustasot | Laji          |     &nbsp;    |
|---------------|---------------|---------------|
| 1001          | Sähkö   | Ensisijainen       |
| 1002          | Palkat      | Ensisijainen       |
| 1003          | Mainonta   | Ensisijainen       |
| **SC-CC001**  | **Henkilöstöhallinto**        | **Toissijainen** |
| **SC-CC002**  | **Myyntitiedot**   | **Toissijainen** |
| **SC-CC003**  | **Kokoonpano**  | **Toissijainen** |
| **SC-CC004**  | **Pakkaus** | **Toissijainen** |

**Tuloslaskelma**-dimensiohierarkia on päivitettävä uuden dimension jäsenillä, jotta dimension hierarkia sisältää oikeat raportoinnin ja käytäntöjen määrittämisessä käytettävät tiedot.

**Dimension hierarkiatiedot**

| Dimensiohierarkian nimi | Dimensio     | Dimensiohierarkiatyypin nimi      |
|--------------------------|---------------|------------------------------------|
| Tuloslaskelma  | Kustannustasot | Dimension luokitteluhierarkia |

**Dimensiohierarkia**

|      &nbsp;             | Dimension jäsenalueet |  &nbsp;             |
|-------------------------|-------------------------|---------------------|
| Solmukohdat                   | Lähtödimension jäsen   | Kohdedimension jäsen |
| Tuloslaskelma |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Ensisijainen kustannus                        | 10 001                   | 10003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Toissijainen kustannus                         | **SC-CC001**            | **SC-CC004**        |

Luo **kustannusten koontikäytäntö**, jossa kukin kustannuspaikka on yhdistetty vastaavaan tyypin **Toissijainen** kustannustasoon.

**Kustannusten koontikäytännöt**

| Käytännön nimi | kuvaus | Kustannusobjektin dimensiohierarkia | Kustannustason dimensiohierarkia |
|-------------|-------------|---------------------------------|----------------------------------|
| 2017        | Kustannusvirta   | Organisaatio                    | Tuloslaskelma          |

**Kustannusten koontisäännöt**

| Kustannusobjektin dimensiohierarkiasolmu | Kustannustason dimensiohierarkiasolmu | Toissijainen kustannustaso |
|--------------------------------------|---------------------------------------|------------------------|
| CC001                                | Tuloslaskelma               | **SC-CC001**           |
| CC002                                | Tuloslaskelma               | **SC-CC002**           |
| CC003                                | Tuloslaskelma               | **SC-CC003**           |
| CC004                                | Tuloslaskelma               | **SC-CC004**           |

## <a name="perform-overhead-calculation"></a>Yleiskustannuslaskennan suorittaminen

**Kirjauskansio**

| Kirjauskansio | Kirjauskansion tyyppi            | Kirjanpidon vuosikalenterin kausi | Vuosi(a) | Kausi | Versio       |
|---------|-------------------------|------------------------|------|--------|---------------|
| 00002   | Kustannusten kohdistuskirjauskansio | Tilivuosi                 | 2017    | Kausi 1 | Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1 |

Järjestelmä käyttää nyt **kustannusten koontikäytäntöä**, kun se luo **kustannusobjektin saldon kirjauskansioviennit**.

**Kustannusobjektin saldon kirjauskansioviennit**

| Kirjauspäivä | Kustannusobjekti | kuvaus  | Kustannustaso | kuvaus |  Summa |
|-----------------|-------------|--------------|----------|-----------|-----------|
| 31.1.2017      | CC001       | Henkilöstöhallinto           | SC-CC001 | Henkilöstöhallinto        | 10.100,00 |
| 31.1.2017      | CC002       | Myyntitiedot      | SC-CC002 | Myyntitiedot   | 17.735,00 |
| 31.1.2017      | CC003       | Kokoonpano     | SC-CC003 | Kokoonpano  | 31.082,75 |
| 31.1.2017      | CC004       | Pakkaus    | SC-CC004 | Pakkaus | 15.717,25 |

> [!NOTE]
> Kirjauskansioviennit luodaan mahdollisen **kustannusten koontikäytännön** sääntöjen perusteella. Näytettävä saldo on yleiskustannuslaskennan saldo.

Kirjauskansiovienneistä avattavalla **Kustannusobjektin kustannussaldon kirjauskansioviennin tiedot** -sivulla näkee, miten saldo on saatu.

**Esimerkki: kustannusobjektin CC002 Myyntitiedot kirjauskansiovienti**

**Kustannusobjektin kustannussaldon kirjauskansioviennin tiedot**

| Kustannustason dimension jäsen | kuvaus |  Summa   |
|-------------------------------|-------------|-----------|
| 1001                          | Sähkö | 200 000    |
| 1002                          | Palkat    | 10.000,00 |
| 1003                          | Mainonta | 4.000,00  |
| SC-CC001                      | Henkilöstöhallinto          | 3.535,00  |

**Yleiskustannuslaskennan luomat kustannusmerkinnät**

| Kustannusobjekti | kuvaus  | Kustannustaso   | kuvaus  |        Summa     |       Kirjauspäivä     |
|-------------|--------------|----------|-----------------|-------------|------------|
| CC001       | Henkilöstöhallinto           | SC-CC001 | Henkilöstöhallinto              | \- 10.100,00 | 31.1.2017 |
| CC002       | Myyntitiedot      | SC-CC001 | Henkilöstöhallinto              | 3.535,00    | 31.1.2017 |
| CC003       | Kokoonpano     | SC-CC001 | Henkilöstöhallinto              | 5.555,00    | 31.1.2017 |
| CC004       | Pakkaus    | SC-CC001 | Henkilöstöhallinto              | 1.010,00    | 31.1.2017 |
| CC002       | Myyntitiedot      | SC-CC002 | Myyntitiedot         | \- 17.735,00 | 31.1.2017 |
| CC003       | Kokoonpano     | SC-CC002 | Myyntitiedot         | 11.527,75   | 31.1.2017 |
| CC004       | Pakkaus    | SC-CC002 | Myyntitiedot         | 6.207,25    | 31.1.2017 |

Kun **yleiskustannuslaskenta** on valmis, voit raportoida tulokset esimerkiksi seuraavilla työkaluilla: Microsoft SharePoint -työtila, Excel tai Power BI.

## <a name="view-reporting-in-excel"></a>Raporttien näyttäminen Excelissä 

Voit tarkastella tietoja dimensiohierarkioiden ansiosta eri koostetasoilla.

Tässä on esimerkki Excelin Power Pivot -raportoinnista.

| **Tuloslaskelma** | **Kustannusobjekti** |      &nbsp;    |   &nbsp;      |     &nbsp;    |  **Yhteensä**    |
|-----------------------------|-----------------|----------------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002**      | **CC003**     | **CC004**     |               |
| **Ensisijainen kustannus**            | **10.100,00**   | **14.200,00**  | **14.000,00** | **8.500,00**  | **46.800,00** |
| &nbsp;&nbsp;&nbsp;&nbsp; 1001                            | 100,00          | 200,00         | 6.000,00      | 2.000,00      | **8.300,00**  |
| &nbsp;&nbsp;&nbsp;&nbsp; 1002                            | 10.000,00       | 10.000,00      | 8.000,00      | 6.500,00      | **34.500,00** |
|&nbsp;&nbsp;&nbsp;&nbsp; 1003                             | 0,00            | 4.000,00       | 0,00          | 0,00          | **4.000,00**  |
|**Toissijainen kustannus**                            | **-10 100,00**  | **-14 200,00** | **17,082,75** | **7.217,25**  | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC001                            | \- 10.100,00     | 3.535,00       | 5.555,00      | 1.010,00      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC002                             | 0,00            | \- 17.735,00    | 11.527,75     | 6.207,25      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC003                            | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC004                             | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
| **Yhteensä**                   | **0,00**        | **0,00**       | **31.082,75** | **15.717,25** | **46.800,00** |

**Kustannuksen koontikäytännön** ja **toissijaisen tyypin kustannustasojen** ansiosta voit jättää sisäisen raportoinnin kustannusobjektikohtaisen ensisijaisen kustannuksen ensisijaiseksi kustannukseksi, joka ei muutu **yleiskustannuslaskennan** jälkeen.

Jos sama esimerkki on suoritettu **kustannuksen koontikäytäntöä** luomatta, raportoinnin tulos olisi sama kuin alla oleva. Kustannusvirta on oikein mutta kustannuspaikkojen välinen kustannusvirtojen jäljitettävyys ja yksityiskohdat menetetään.

| **Tuloslaskelma** | **Kustannusobjekti** |   &nbsp;  |    &nbsp;     |  &nbsp;       |          **Yhteensä**  |
|-----------------------------|-----------------|-----------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002** | **CC003**     | **CC004**     |               |
| **Ensisijainen kustannus**            | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |
|&nbsp;&nbsp;&nbsp;&nbsp; 1001                              | 0,00            | 0,00      | 6.207,75      | 2.092,25      | **8.300,00**  |
| &nbsp;&nbsp;&nbsp;&nbsp; 1002                             | 0,00            | 0,00      | 22.275,00     | 12.225,00     | **34.500,00** |
|&nbsp;&nbsp;&nbsp;&nbsp; 1003                              | 0,00            | 0,00      | 2600,00       | 1.400,00      | **4.000,00**  |
|**Toissijainen kustannus**                            | **0,00**        | **0,00**  | **0,00**      | **0,00**      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC001                             | 0,00            | 0,00      | 0,00          | 0,00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC002                             | 0,00            | 0,00      | 0,00          | 0,00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC003                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC004                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
| **Yhteensä**                   | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |

Voit määrittää organisaation raportointi- ja jäljitettävyysvaatimusten mukaisen tason toissijaisille kustannustasoille ja luoda tarvittavat kustannusten koontisäännöt.

Selkeä **kohdistusten kohdistuksen** ja **kustannuksen koontikäytäntöjen** välinen ero varmistaa, että jatkuvat päivitykset voidaan tehdä joustavasti ilman, että ne vaikuttavat toisiinsa.



## <a name="additional-resources"></a>Lisäresurssit
-  [Kustannusobjektin dimensiot](cost-objects.md)
-  [Kustannustason dimensiot](cost-elements.md)
-  [Dimensiohierarkia](dimension-hierarchy.md)
-  [Yleiskustannuslaskenta](overhead-calculation.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]