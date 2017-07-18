---
title: "Tilastodimension jäsenet ja tilastomittauksen lähdemallit"
description: "Tämä ohjeaihe sisältää tietoja tilastodimension jäsenistä ja tilastomittauksen lähdemalleista. Tilastodimension jäseniä voidaan käyttää kohdistusperusteena esimerkiksi kustannusten jaon ja kohdistuksen tyyppisissä käytännöissä. Niitä voidaan käyttää myös raportoitaessa ei-rahallista kulutusta."
author: YuyuScheller
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostAccountingLedgerSourceEntryProvider, CAMStatisticalDimension, CAMAXStatisticalMeasureProviderTemplate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 180863b5c3b8fe7870ab58f3849e52583f5880c1
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017

---

# <a name="statistical-dimension-members-and-statistical-measure-provider-templates"></a>Tilastodimension jäsenet ja tilastomittauksen lähdemallit

[!include[banner](../includes/banner.md)]

Tilastodimensiota ja sen jäseniä käytetään rekisteröitäessä ja hallittaessa ei-rahallisia merkintöjä kustannuslaskennassa. Tilastodimension jäseniä voidaan käyttää kahteen tarkoitukseen:

- Kohdistusperusteena kustannusten jaon tai kustannusten kohdistuksen tyyppisissä käytännöissä.
- Ei-rahallista kulutusta raportoitaessa

## <a name="statistical-dimension"></a>Tilastodimensio

Tilastodimensiolla on yksilöivä nimi ja joukko yksilöiviä dimension jäseniä. Tilastodimensio määritetään kustannuslaskennan kirjanpidon tunnukselle. Tämä suhde sitoo kaikki vastaavat tilastodimension jäsenet kustannuslaskennan kirjanpitoon. Tämän vuoksi kaikki tilastomerkinnät luodaan kustannuslaskennan kirjanpidon kontekstissa.

> [!NOTE]
> Tilastodimensio voidaan määrittää useampaan kuin yhteen kustannuslaskennan kirjanpitoon.

Esimerkki tilastodimensiosta.

| Nimi                        | Dimension jäsenten tietoyhdistin |
|-----------------------------|--------------------------------------|
| Jaetut tilastoelementit | Tuodut dimension elementit           |

Esimerkki tilastodimensiosta, joka on määritetty kustannuslaskennan kirjanpitoon.

| Nimi                  | Kirjanpitovaluutta | Vaihtokurssin tyyppi | Kirjanpidon vuosikalenteri | Kustannustason dimensio | Tilastodimensio       |
|-----------------------|---------------------|--------------------|-----------------|------------------------|-----------------------------|
| Johdon laskentatoimi | USD                 | Vakiovaluutta  | Tilikausi     | Jaetut kustannustasot   | Jaetut tilastoelementit |

## <a name="statistical-dimension-members"></a>Tilastodimension jäsenet

Tilastodimension jäsen edustaa yksikköä, jolle haluat rekisteröidä ei-rahalliset toimenpiteet. Näitä toimenpiteitä voidaan käyttää kohdistusperusteena tai ei-rahallisten arvojen raportointiin.

Tilastodimension jäsenet voidaan luoda manuaalisesti. Voit myös tuoda ne tiedostosta tietojen hallinnan tuonti- ja vientityökalun avulla.

Tilastodimension jäsen muuttuu automaattisesti ennalta määritetyksi kohdistusperusteeksi. Sitä voidaan käyttää käytäntöjen kohdistusperusteena tai muuntyyppisten kohdistusperusteiden syötteenä.

Seuraavassa on esimerkkejä tyypillisistä tilastodimension jäsenistä.

| Tilastodimension nimi  | Tilastoelementit | kuvaus             | Yksikkö |
|-----------------------------|----------------------|-------------------------|------|
| Jaetut tilastoelementit | FTE                  | Kokoaikaiset työntekijät     | Kpl  |
| Jaetut tilastoelementit | Sähkö          | Sähkönkulutus | kWh  |
| Jaetut tilastoelementit | Pak. KP              | Pakkauksen kustannuspaikka   | h |

## <a name="statistical-measure-provider-template"></a>Tilastomittauksen lähdemalli

Tilastomittaukset voivat olla peräisin monenlaisista lähteistä. Microsoft Dynamics 365 for Finance and Operations Enterprise edition on erinomainen tilastomittausten lähde. Voit käyttää tilastomittauksen lähdemallia määrittämään helposti tuotavia tilastomittauksia.

Tilastomittauksen lähdemallin määritys on yleinen ja sitä voidaan käyttää useisiin tilastodimension jäseniin.

> [!NOTE]
> Kaikkia taloushallinnon dimensioita sisältäviä taulukoita voidaan käyttää tilastomittauksen lähteinä.

**Esimerkki: Työntekijöiden kustannuspaikkakohtaisen määrä**

Kustannuspaikkakohtainen työntekijöiden määrä on tilastomittaus, jota voidaan käyttää eri tarkoituksiin, joiden avulla johto saa tietoja:

- Kustannuspaikkakohtainen tilastollisen raportoinnin mittaus
- Kohdistusperuste erilaisille kuluille
- Kustannuspaikkakohtaiset sisäiset kustannushinnat:

    - Kustannukset työntekijää kohti
    - Tuotto työntekijää kohti

HcmEmployment-taulukossa on luettelo kaikista työntekijöistä esiintymässä. Tämä on yleinen taulukko. Siksi tietueet eivät liity tiettyyn tietoalueen tunnukseen.

Esimerkki työntekijöistä HcmEmployment-taulukossa.

| Nimi       | Kustannuspaikka | kuvaus   | Työntekijätyyppi |
|------------|-------------|----|-------------|
| Työntekijä 1 | CC001       | Henkilöstöhallinto | Työntekijä     |
| Työntekijä 2 | CC002       | FI | Työntekijä     |
| Työntekijä 3 | CC002       | FI | Työntekijä     |
| Työntekijä 4 | CC003       | VS | Työntekijä     |
| Työntekijä 5 | CC003       | VS | Työntekijä     |
| Työntekijä 6 | CC002       | FI | Alihankkija  |

Kun luot **Tilastomittauksen lähdemalli**-tietueen, sinun on päätettävä, mitä toimintoa käytetään:

- **Määrä** – Tietueiden kustannusobjektikohtainen määrä siirretään.
- **Summa** – Tietueiden kustannusobjektikohtainen summa siirretään. ( **Summa**-kenttä ja **Päivämäärä**-kenttä ovat pakollisia.)

## <a name="using-the-count-function"></a>Määrä-toiminnon käyttö

Tilastomittauksen lähdemalli voidaan määrittää seuraavasti.

| Nimi  | Toiminto | Lähdetaulu  | Summakenttä      | Päivämääräkenttä     |
|-------|----------|---------------|----------------|----------------|
| FTE  | Määrä    | HcmEmployment | Ei käytettävissä | Ei käytettävissä |

Voit myös lisätä vähintään yhden alueen, joka rajaa mittauksia lähdetaulukosta.

Tässä esimerkissä voit lisätä alueeseen **Työntekijätyyppi**-kentän, jos haluat kaikkien kokopäivätoimisten työntekijöiden (FTE) määrän. Valitsemalla **Ehdot**-kentässä **Työntekijä** voit rajoittaa tulosaluetta seuraavasti.

**Alueet**

| Lähdetaulu  | Kenttä       | Kriteeri |
|---------------|-------------|----------|
| HcmEmployment | Työntekijätyyppi | Työntekijä  |

Ennen kuin saat tilastomittaukset kustannuslaskentaan, sinun on muodostettava suhde tilastomittauksen lähdemallin ja tilastodimension jäsenen välille. Tämä suhde luodaan jokaista kustannuslaskennan kirjanpitoa ja versiota kohti. Suhde sisältää tietoyhdistimen ja tietojen toimittajan. Yhdellä tilastodimension jäsenellä voi olla useita tietoyhdistimiä ja tietojen toimittajia.

> [!NOTE]
> Tässä esimerkissä luodaan suhde vain **Toteutunut versio** -tietolähteelle.

Siirry kohtaan **Kustannuslaskennan kirjanpito** \> **Todellinen versio** \> **Hallinta** \> **Tilastomittaukset** ja määritä suhde. Valitse tässä esimerkissä **Dynamics 365 for Finance and Operations, Enterprise edition – Tilastomittaukset** -tietoyhdistin, koska haluamme tuoda tietoja Finance and Operations -palvelusta.

**Tietolähde**

| Nimi        | Tietoyhdistin                                                                     | Tilastodimension jäsen |
|-------------|------------------------------------------------------------------------------------|------------------------------|
| FTE D365FO | Dynamics 365 for Finance and Operations, Enterprise Edition – Tilastomittaukset | FTE                         |

**Tietojen tarjoajan konfiguraatio**

| Tilastomallin nimi |
|---------------------------|
| FTE                      |

Seuraavat tilastomerkinnät luodaan kustannuslaskennassa tilastomittausten lähdetietojen käsittelyn jälkeen.

**Kirjauskansio**

| Kirjauskansio | Kirjauskansion tyyppi                       | Kirjanpidon vuosikalenterin kausi | Vuosi(a)   |  Kausi  |  Versio | Tietoyhdistimen lähdemerkinnät|
|---------|------------------------------------|------------------------|--------|----------|----------|------------------------------|
| 00001   | Tilastokirjausten siirron kirjauskansio | Tilivuosi                 | 2017   | Kausi 1 | Kustannuslaskennan kirjanpito USMF | FTE                   |

**Tilastokirjausten siirron kirjauskansioviennit**

| Kirjauspäivä | Suuruus | Tilastoelementti |   kuvaus       | Kustannuspaikka |
|-----------------|-----------|---------------------|---------------------|-------------|
| 31.1.2017      | 1,00      | FTE                | Kokopäiväiset työntekijät | CC001       |
| 31.1.2017      | 2,00      | FTE                | Kokopäiväiset työntekijät | CC002       |
| 31.1.2017      | 2,00      | Kokopäiväiset työntekijät                | Kokoaikaiset työntekijät | CC003       |

**Tilastomerkinnät**

| Kustannusobjekti |    | Kirjauspäivä | Tilastodimension jäsen |  kuvaus        | Suuruus |
|-------------|----|-----------------|------------------------------|---------------------|-----------|
| CC001       | Henkilöstöhallinto | 31.1.2017      | Kokopäiväiset työntekijät                         | Kokoaikaiset työntekijät | 1,00      |
| CC002       | FI | 31.1.2017      | Kokopäiväiset työntekijät                         | Kokoaikaiset työntekijät | 2,00      |
| CC003       | VS | 31.1.2017      | Kokopäiväiset työntekijät                         | Kokoaikaiset työntekijät | 2,00      |

Jos ennalta määritetyn dimension jäsenen FTE-kohdistusperuste on määritetty kustannusten jakosäännöksi, kustannukset jaetaan seuraavan kohdistuskertoimen avulla.

| Kustannusobjekti | kuvaus    | Suuruus | Kohdistuskerroin |
|-------------|----|-----------|-------------------|
| CC001       | Henkilöstöhallinto | 1,00      | (1/5) × summa    |
| CC002       | FI | 2,00      | (2/5) × summa    |
| CC003       | VS | 2,00      | (2/5) × summa    |

## <a name="using-the-sum-function"></a>Summa-toiminnon käyttö

Tuotannon kustannuspaikka, CC010 (pakkaus), vastaa tuotteiden pakkausta ennen niiden toimitusta asiakkaille. Suorat työn kustannukset lisätään tuotteisiin tuoterakenteen ja reitityksen kautta. Kustannuspaikan ylläpidosta aiheutuvat epäsuorat kustannukset pitää myös määrittää valmistetuille tuotteille. Yleensä tällaisen määrityksen paras tilastomittaus on rekisteröity tuotekohtainen tuotantotuntimäärä tietyn ajan kuluessa.

ProdRouteTrans-taulukko sisältää kaikki tuotannon työtransaktiot yrityksen DataAreaID-kohtaisesti.

Esimerkki ProdRouteTrans-taulukosta.

| Viite        | Numero | Työvaihe | Laji | Aika  | Fyysinen pvm. | Tuoteryhmä (taloushallinnon dimensio) | Oikeushenkilö |
|------------------|--------|-----------|------|-------|---------------|-------------------------------------|--------------|
| Tuotantotilaus | P0001  | Pakkaus | Aika | 8,00  | 1.1.2017    | Appelsiinimehu, yritysmyynti                    | USMF         |
| Tuotantotilaus | P0001  | Pakkaus | Aika | 8,00  | 2.1.2017    | Appelsiinimehu, yritysmyynti                    | USMF         |
| Tuotantotilaus | P0002  | Pakkaus | Aika | 4,00  | 3.1.2017    | Appelsiinimehu, kuluttajamyynti               | USMF         |
| Tuotantotilaus | P0003  | Pakkaus | Aika | 4,00  | 3.1.2017    | Appelsiinimehu, kuluttajamyynti               | USMF         |
| Tuotantotilaus | P0004  | Ennalistaminen  | Aika | 10,00 | 3.1.2017    | Appelsiinimehu, kuluttajamyynti               | USMF         |

Kun luot **Tilastomittauksen lähdemalli**-tietueen, sinun on päätettävä, mitä toimintoa käytetään:

- **Määrä** – Tietueiden kustannusobjektikohtainen määrä siirretään.
- **Summa** – Tietueiden kustannusobjektikohtainen summa siirretään. ( **Summa**-kenttä ja **Päivämäärä**-kenttä ovat pakollisia.)

Tilastomittauksen lähdemalli voidaan määrittää seuraavasti.

| Nimi    | Toiminto | Lähdetaulu   | Summakenttä | Päivämääräkenttä    |
|---------|----------|----------------|-----------|---------------|
| Pak. KP | Summa      | ProdRouteTrans | Tunnit     | Fyysinen pvm. |

Voit myös lisätä alueita, jotka rajaavat mittauksia lähdetaulukosta.

Jos haluat laskea yhteen tuntimäärän, joka liittyy kohtaan CC010 Pakkauksen kustannuspaikka, voit lisätä **Työvaihe**-kenttään alueen. Valitsemalla **Ehdot**-kentässä **Pakkaus** voit rajoittaa tulosaluetta.

**Alueet**

| Lähdetaulu   | Kenttä     | Kriteeri  |
|----------------|-----------|-----------|
| ProdRouteTrans | Työvaihe | Pakkaus |

Ennen kuin saat tilastomittaukset kustannuslaskentaan, sinun on muodostettava suhde tilastomittauksen lähdemallin ja tilastodimension jäsenen välille. Tämä suhde luodaan jokaista kustannuslaskennan kirjanpitoa ja versiota kohti. Suhde sisältää tietoyhdistimen ja tietojen toimittajan. Yhdellä tilastodimension jäsenellä voi olla useita tietoyhdistimiä ja tietojen toimittajia.

> [!NOTE]
> Tässä esimerkissä luodaan suhde vain **Toteutunut versio** -tietolähteelle.

Siirry kohtaan **Kustannuslaskennan kirjanpito** \> **Todellinen versio** \> **Hallinta** \> **Tilastomittaukset** ja määritä suhde. Valitse tässä esimerkissä **Dynamics 365 for Finance and Operations, Enterprise edition – Tilastomittaukset** -tietoyhdistin, koska haluamme tuoda tietoja Finance and Operations -palvelusta.

**Tietolähde**

| Nimi           | Tietoyhdistin                                                                     | Tilastodimension jäsen |
|----------------|------------------------------------------------------------------------------------|------------------------------|
| Pak. KP D365FO | Dynamics 365 for Finance and Operations, Enterprise Edition – Tilastomittaukset | Pak. KP                      |

Järjestelmä tunnistaa, että ProdRouteTrans on taulukko, jossa jokainen tietue kuuluu erilliseen yritykseen. Tämän vuoksi järjestelmä pyytää sinua valitsemaan yrityksen, josta tapahtumat tuodaan.

**Tietojen tarjoajan konfiguraatio**

| Tilastomallin nimi | Oikeushenkilö |
|---------------------------|--------------|
| Pak. KP                   | USMF         |

Seuraavat tilastomerkinnät luodaan kustannuslaskennassa tilastomittausten lähdetietojen käsittelyn jälkeen.

**Kirjauskansio**

| Kirjauskansio | Kirjauskansion tyyppi                     | Kirjanpidon vuosikalenterin kausi | Vuosi(a)   | Kausi | Versio   |   Tietoyhdistimen lähdemerkinnät  |
|---------|----------------------------------|------------------------|--------|---------|----------------|---------|
| 00002   | Tilastokirjausten siirron kirjauskansio | Tilivuosi               | 2017    | Kausi 1  | Kustannuslaskennan kirjanpito USMF | Pak. KP |

**Tilastokirjausten siirron kirjauskansioviennit**

| Kirjauspäivä | Suuruus | Tilastoelementti |  kuvaus          | Tuoteryhmä         |
|-----------------|-----------|---------------------|-----------------------|-----------------------|
| 31.1.2017      | 16,00     | Pak. KP             | Pakkauksen kustannuspaikka | Appelsiinimehu, yritysmyynti      |
| 31.1.2017      | 8,00      | Pak. KP             | Pakkauksen kustannuspaikka | Appelsiinimehu, kuluttajamyynti |

**Tilastomerkinnät**

| Kustannusobjekti           | Kirjauspäivä | Tilastodimension jäsen |    kuvaus        | Suuruus |
|-----------------------|-----------------|------------------------------|-----------------------|-----------|
| Appelsiinimehu, yritysmyynti      | 31.1.2017      | Pak. KP                      | Pakkauksen kustannuspaikka | 16,00     |
| Appelsiinimehu, kuluttajamyynti | 31.1.2017      | Pak. KP                      | Pakkauksen kustannuspaikka | 8,00      |

Jos ennalta määritetyn dimension jäsenen Pak. KP -kohdistusperuste on määritetty kustannusten jakosäännöksi, kustannukset jaetaan seuraavan kohdistuskertoimen avulla.

| Kustannusobjekti           | Suuruus | Kohdistuskerroin  |
|-----------------------|-----------|--------------------|
| Appelsiinimehu, yritysmyynti      | 16,00     | (16 ÷ 24) × määrä |
| Appelsiinimehu, kuluttajamyynti | 8,00      | (8 ÷ 24) × määrä  |

## <a name="imported-statistical-measures"></a>Tuodut tilastomittaukset

Voit tuoda tilastomittauksia kustannuslaskentaan käyttämällä tietojen hallinnan tuonti/vienti-työkalua.

Tietoyksikön, jota käytetään tuontiin, nimi on Tuodut tilastomittaukset.

> [!NOTE]
> Tämä tietoyksikkö on suunniteltu mahdollistamaan enintään viisi dimensioarvoa tietuetta kohti.

Sähkön kulutus kirjataan Microsoft Excel -tiedostoon tietoyksikön esimääritetyn muodon avulla. Esimerkki:

| Kirjauspäivä | Dimension jäsenen nimi 1 | Dimension jäsenen nimi 2 | Dimension jäsenen nimi 5 | Suuruus  | Lähdetunniste |
|-----------------|------------------------|------------------------|------------------------|------------|-------------------|
| 31.1.2017      | CC001                  |                        |                        | 2,450.00   | Sähkö       |
| 31.1.2017      | CC002                  |                        |                        | 4,100.00   | Sähkö       |
| 31.1.2017      | CC003                  |                        |                        | 15,000.00  | Sähkö       |

Kun olet tuonut tiedot tietojen hallinnan kautta, tiedot tallennetaan kustannuslaskennan väliaikaiseen taulukkoon. Siksi tuotuja tietoja voidaan käyttää useissa kustannuslaskennan kirjanpidoissa. Tietoja ei tarvitse ladata uudelleen.

Tuo tiedot siirtymällä kohtaan **Tuodut tiedot** \> **Tietoyksikkö** \> **Tuodut tilastomittaukset**.

| Lähdetunniste | Kirjauspäivä | Suuruus  | Dimension jäsenen nimi 1 | Dimension jäsenen nimi 2 | Dimension jäsenen nimi 5 |
|-------------------|-----------------|------------|------------------------|------------------------|------------------------|
| Sähkö       | 31.1.2017      | 2,450.00   | CC001                  |                        |                        |
| Sähkö       | 31.1.2017      | 4,100.00   | CC002                  |                        |                        |
| Sähkö       | 31.1.2017      | 15,000.00  | CC003                  |                        |                        |

Ennen kuin saat tilastomittaukset kustannuslaskentaan, sinun on muodostettava suhde lähdetunnisteen ja tilastodimension jäsenen välille. Tämä suhde luodaan jokaista kustannuslaskennan kirjanpitoa ja versiota kohti. Suhde sisältää tietoyhdistimen ja tietojen toimittajan. Yhdellä tilastodimension jäsenellä voi olla useita tietoyhdistimiä ja tietojen toimittajia.

> [!NOTE]
> Tässä esimerkissä luodaan suhde vain **Toteutunut versio** -tietolähteelle.

Siirry kohtaan **Kustannuslaskennan kirjanpito** \> **Todellinen versio** \> **Hallinta** \> **Tilastomittaukset** ja määritä suhde. Valitse tässä skenaariossa **Tuodut tilastomittaukset** -tietoyhdistin, koska tiedot on tuotu kolmannen osapuolen järjestelmästä Excelin kautta kustannuslaskentaan.

**Tietolähde**

| Nimi        | Tietoyhdistin                | Tilastodimension jäsen |
|-------------|-------------------------------|------------------------------|
| Sähkö | Tuodut tilastomittaukset | Sähkö                  |

**Tietojen tarjoajan konfiguraatio**

| Tuo lähdetunniste | Toiminto | Dimensio 1   | Dimensio 2 | Dimensio 5 |
|--------------------------|----------|--------------|------------|------------|
| Sähkö              | Summa      | Kustannuspaikat |            |            |

> [!NOTE]
> Kun määrität tietopalvelun konfiguroinnin, sinun on määritettävä mitkä kustannusobjektin dimensiot vastaavat tuotuja tapahtumia. Seuraavat tilastomerkinnät luodaan kustannuslaskennassa tilastomittausten lähdetietojen käsittelyn jälkeen.

**Kirjauskansio**

| Kirjauskansio | Kirjauskansion tyyppi                       | Kirjanpidon vuosikalenterin kausi | Vuosi(a)  | Jakso  |Versio      |Tietoyhdistimen lähdemerkinnät |
|---------|------------------------------------|------------------------|-------|--------|---------------|-------------|
| 00002   | Tilastokirjausten siirron kirjauskansio | Tilivuosi                 | 2017  | Kausi 1 | Kustannuslaskennan kirjanpito USMF | Sähkö |

**Tilastokirjausten siirron kirjauskansioviennit**

| Kirjauspäivä | Suuruus  | Kustannustaso |   kuvaus           | Kustannuspaikka |
|-----------------|------------|--------------|-------------------------|-------------|
| 31.1.2017      | 2,450.00   | Sähkö  | Sähkönkulutus | CC001       |
| 31.1.2017      | 4,100.00   | Sähkö  | Sähkönkulutus | CC002       |
| 31.1.2017      | 15,000.00  | Sähkö  | Sähkönkulutus | CC003       |

**Tilastomerkinnät**

| Kustannusobjekti |    | Kirjauspäivä | Tilastodimension jäsen |      kuvaus                   | Suuruus  |
|-------------|----|-----------------|------------------------------|-------------------------|------------|
| CC001       | Henkilöstöhallinto | 31.1.2017      | Sähkö                  | Sähkönkulutus | 2,450.00   |
| CC002       | FI | 31.1.2017      | Sähkö                  | Sähkönkulutus | 4,100.00   |
| CC003       | VS | 31.1.2017      | Sähkö                  | Sähkönkulutus | 15,000.00  |

Jos ennalta määritetyn dimension jäsenen Sähkö-kohdistusperuste on määritetty kustannusten jakosäännöksi, kustannukset jaetaan seuraavan kohdistuskertoimen avulla.

| Kustannusobjekti |    | Suuruus | Kohdistuskerroin          |
|-------------|----|-----------|----------------------------|
| CC001       | Henkilöstöhallinto | 2,450.00  | (2 450 ÷ 21 550) × summa  |
| CC002       | FI | 4,100.00  | (4 100 ÷ 21 550) × summa  |
| CC003       | VS | 15,000.00 | (15 000 ÷ 21 550) × summa |

## <a name="see-also"></a>Lisätietoja

[Kohdistusperusteet](allocation-bases.md)

