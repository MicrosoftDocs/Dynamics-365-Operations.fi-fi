---
title: Kohdistusperusteet
description: "Tässä ohjeaiheessa on tietoja kohdistusperusteista. Kohdistusperusteet ovat kustannuslaskennan keskeisiä osia, ja niitä käytetään lähinnä yleiskustannusten kohdistamiseen."
author: AndersGirke
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 63f39a6c06a0c6b5df901f7aa4235aab3c4ac06e
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="allocation-bases"></a>Kohdistusperusteet 

[!include[banner](../includes/banner.md)]

Kustannuslaskentaa kohdistaa yleiskustannukset kohdistusperusteen perusteella. Kohdistusperuste voi olla määrä, kuten koneen käyttötunnit, kulutetut kilowattitunnit (kWh) tai käytössä olevat neliömetrit. Kohdistusperusteita käytetään lähinnä yleiskustannusten määrittämiseen tuotettavalle varastolle. Esimerkiksi IT-osasto kohdistaa kustannukset kunkin osaston käyttämien tietokoneiden määrän mukaan.

Kustannuslaskennassa on kolmenlaisia kustannusperusteita:

- Ennalta määritetyn dimension jäsenen kohdistusperusteet
- Hierarkian kohdistusperusteet
- Kaavan kohdistusperusteet

## <a name="predefined-dimension-member-allocation-bases"></a>Ennalta määritetyn dimension jäsenen kohdistusperusteet

Ennalta määritetyn dimension jäsenen kohdistusperusteet luodaan automaattisesti, kun jokin seuraavan tyyppisistä dimension jäsenistä luodaan:

- Tilastodimension jäsenet
- Kustannustason dimension jäsenet

> [!NOTE]
> Kustannustason dimension jäseneen perustuvat ennalta määritetyn dimension jäsenen kohdistusperusteet ottavat huomioon vain tietolähteen arvot. Tietolähde voi olla esimerkiksi kirjanpito tai budjetti.

### <a name="example-1-use-a-cost-element-dimension-member-as-the-allocation-base"></a>Esimerkki 1: Kustannustason dimension jäsenen käyttö kohdistusperusteena
Tässä esimerkissä näytetään sellaisen kustannuksen kohdistussäännön luonti, jolla kustannustaso 10002 (työntekijän vakuutus) kohdistetaan kustannustasoon 10001 (palkat) kirjattuun saldoon. Kohdistussääntö määritetään kunkin osaston palkkojen suhteessa kokonaispalkkakustannuksiin. (Tarkistettava)

Tilikartta määritetään kirjanpidossa seuraavasti:

| Tilikartta | Päätili | kuvaus        | Päätilin tyyppi |
|------------------|--------------|--------------------|-------------------|
| Yhteiset ominaisuudet           | 10 001        | Palkat           | Kulu           |
| Yhteiset ominaisuudet           | 10 002        | Työntekijän vakuutus | Kulu           |

Määritä ensin kustannustason dimensio ja sitten tietoyhdistin. Seuraavat tapahtumat luodaan kustannuslaskennassa tietojen tuonnin jälkeen.

**Kustannustason dimension jäsenet**

| Kustannustason dimension nimi | Kustannustaso |  kuvaus       | Laji    |
|-----------------------------|--------------|--------------------|---------|
| Kustannustasot               | 10 001        | Palkat           | Ensisijainen |
| Kustannustasot               | 10 002        | Työntekijän vakuutus | Ensisijainen |

**Ennalta määritetyn dimension jäsenen kohdistusperusteet** 

| Nimi  | kuvaus        | Kustannustason dimensio |
|-------|--------------------|------------------------|
| 10 001 | Palkat           | Kustannustasot          |
| 10 002 | Työntekijän vakuutus | Kustannustasot          |

Seuraavat viennit on kirjattu kirjanpitoon:

- Palkat-päätilin näyttävät viennit tulevat palkanlaskentajärjestelmästä, ja ne on kirjattu kustannuspaikkoihin.
- Työntekijän vakuutuskulu kirjataan manuaalisesti oletuskustannuspaikkaan.

| Kirjauspäivä | Kustannuspaikka |  kuvaus        | Päätili |  kuvaus       | Summa kirjanpitovaluuttana |
|-----------------|-------------|---------------------|--------------|--------------------|-------------------------------|
| 3.1.2017      | CC001       | Henkilöstöhallinto                  | 10 001        | Palkat           | 2 000,00                      |
| 3.1.2017      | CC002       | FI                  | 10 001        | Palkat           | 5 000,00                      |
| 3.1.2017      | CC003       | VS                  | 10 001        | Palkat           | 3 000,00                      |
| 3.1.2017      | CC099       | Oletuskustannuspaikka | 10 002        | Työntekijän vakuutus | 1 000,00                      |

Seuraavat viennit luodaan kustannuslaskennassa kirjanpidon lähdetietojen käsittelyn jälkeen.

**Kustannusmerkinnät**

| Kustannusobjekti |  kuvaus        | Kustannustaso  |  kuvaus       | Kustannustoiminta   |Summa|Kirjauspäivä|
|-------------|---------------------|---------------|--------------------|-----------------|------|---------------|
| CC001       | Henkilöstöhallinto                  | 10 001         | Palkat           | Luokittelematon    |2 000,00|  3.1.2017    |
| CC002       | FI                  | 10 001         | Palkat           | Luokittelematon    |5 000,00|     3.1.2017         |
| CC003       | VS                  | 10 001         | Palkat           | Luokittelematon    |3 000,00|      3.1.2017        |
| CC099       | Oletuskustannuspaikka | 10 002         | Työntekijän vakuutus | Luokittelematon    |1 000,00|      3.1.2017       |

Tässä yksinkertaistetussa esimerkissä luodaan kohdistussääntö, jolla kustannustaso 10002 (työntekijän vakuutus) kohdistetaan suhteessa kustannustasoon 10001 (palkat) kirjattuun saldoon.

**Kustannusten jakosääntö**

| Kustannusobjektin dimensiohierarkiasolmu | Kustannustason dimensiohierarkiasolmu | Kustannustoiminta | Kohdistusperuste |
|--------------------------------------|---------------------------------------|---------------|-----------------|
| CC099                                | 10 002                                 | Luokittelematon  | 10 001           |

**Yleiskustannuslaskennan suorittaminen**

Kun kustannustasoa 10001 (palkat) on käytetty kohdistusperusteena, yleiskustannuslaskennan tulos on seuraava:

| Kustannusobjekti | kuvaus | Suuruus |   Kohdistuskerroin         | Summa |
|-------------|-------------|-----------|-----------------------------|--------|
| CC001       | Henkilöstöhallinto          | 2 000     | (2 000 ÷ 10 000) × 1 000,00 | 200,00 |
| CC002       | FI          | 5 000     | (5 000 ÷ 10 000) × 1 000,00 | 500,00 |
| CC003       | VS          | 3 000     | (3 000 ÷ 10 000) × 1 000,00 | 300,00 |

**Kirjauskansio**

| Kirjauskansio | Kirjauskansion tyyppi                          | Kirjanpidon vuosikalenterin kausi | Vuosi(a) | Kausi   | Versio                                                                 |
|---------|---------------------------------------|------------------------|------|----------|-------------------------------------------------------------------------|
| 00001   | Kustannusten jaon laskentakirjauskansio | Tilivuosi                 | 2017 | Kausi 1 | Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1 |

**Kustannusobjektin saldon kirjauskansioviennit**

| Kirjauspäivä | Kustannusobjekti | kuvaus         | Kustannustaso | kuvaus        | Kustannustoiminta |  Summa  |
|-----------------|-------------|---------------------|--------------|--------------------|---------------|----------|
| 31.1.2017      | CC099       | Oletuskustannuspaikka | 10 002        | Työntekijän vakuutus | Luokittelematon  | 1 000,00 |

**Kustannusmerkinnät**

| Kustannusobjekti |  kuvaus        | Kustannustaso |    kuvaus     | Kustannustoiminta | Summa    | Kirjauspäivä |
|-------------|---------------------|--------------|--------------------|---------------|-----------|-----------------|
| CC099       | Oletuskustannuspaikka | 10 002        | Työntekijän vakuutus | Luokittelematon  | -1 000,00 | 31.1.2017      |
| CC001       | Henkilöstöhallinto                  | 10 002        | Työntekijän vakuutus | Luokittelematon  | 200,00    | 31.1.2017      |
| CC002       | FI                  | 10 002        | Työntekijän vakuutus | Luokittelematon  | 500,00    | 31.1.2017      |
| CC099       | VS                  | 10 002        | Työntekijän vakuutus | Luokittelematon  | 300,00    | 31.1.2017      |

### <a name="example-2-use-a-statistical-dimension-member-as-the-allocation-base"></a>Esimerkki 2: Tilastodimension jäsenen käyttö kohdistusperusteena

Tilastodimension jäseniä voidaan käyttää kohdistusperusteena määrittämään käytäntöjä tai raportoimaan kustannusobjektikohtaista ei-rahallista kulutusta. Voit luoda tilastodimension jäseniä manuaalisesti tai tuoda ne tiedostosta tietojen hallinnan tuonti- ja vientityökalulla.

**Tilastodimension jäsenet**

| Tilastodimension nimi | Tilastoelementti | kuvaus               | Yksikkö |
|----------------------------|---------------------|---------------------------|------|
| Tilastoelementit       | FTE                 | Kokoaikaiset työntekijät       | Kpl   |
| Tilastoelementit       | Sähkö         | Sähkönkulutus   | kWh  |

Kun tilastodimension jäsen on tallennettu, vastaava tietue luodaan ennalta määritetyissä dimension jäsenen kohdistusperusteissa.

**Ennalta määritetyn dimension jäsenen kohdistusperusteet**

| Nimi        | kuvaus             | Tilastoelementin dimensio |
|-------------|-------------------------|-------------------------------|
| FTE         | Kokoaikaiset työntekijät     | Tilastoelementit          |
| Sähkö | Sähkönkulutus | Tilastoelementit          |

Tilastomitat voivat olla peräisin erilaisista lähteistä:

- Sähkökulutus voidaan mitata mittareilla, jotka on asennettu eri alueilla yrityksessä.
- Tilastomittaukset ovat tauluissa. Esimerkiksi HcmEmployment-taulu sisältää kaikkien työntekijöiden ja heidän kustannuspaikkojensa luettelon.

| Nimi       | Kustannuspaikka |  kuvaus  | Työntekijätyyppi |
|------------|-------------|----|-------------|
| Työntekijä A | CC001       | Henkilöstöhallinto | Työntekijä     |
| Työntekijä B | CC002       | FI | Työntekijä     |
| Työntekijä C | CC002       | FI | Työntekijä     |
| Työntekijä D | CC003       | VS | Työntekijä     |
| Työntekijä F | CC003       | VS | Työntekijä     |

> [!NOTE]
> Kaikkia taloushallinnon dimensiota sisältäviä tauluja voidaan käyttää tilastomittausten lähteinä.

Kustannuslaskenta tukee tilastomittauskokoelmaa seuraavan tietoyhteyden avulla:

- Tietojen hallinnan tuonti- ja vientityökalu
- Tilastomittaukset

Tilastomittausten saanti järjestelmästä edellyttää tilastomittauksen lähdemallin käyttöä. Lisätietoja on kohdassa Tilastomittauksen lähdemalli. (Linkki lisätään, kun ohjeaihe on kirjoitettu.)

**Tilastomittauksen lähdemallit**

| Nimi  | Toiminto | Lähdetaulu  | Summakenttä      | Päivämääräkenttä     |
|-------|----------|---------------|----------------|----------------|
| FTE-työntekijät | Laskenta    | HcmEmployment | Ei käytettävissä | Ei käytettävissä |

Seuraavat viennit luodaan kustannuslaskennassa tilastomittausten lähdetietojen käsittelyn jälkeen.

**Tilastomerkinnät**

| Kustannusobjekti | kuvaus      | Kirjauspäivä | Tilastodimension jäsen | kuvaus         | Suuruus |
|-------------|------------------|-----------------|------------------------------|---------------------|-----------|
| CC001       | Henkilöstöhallinto               | 31.1.2017      | FTE-työntekijät                        | Kokoaikaiset työntekijät | 1,00      |
| CC002       | FI               | 31.1.2017      | FTE-työntekijät                        | Kokoaikaiset työntekijät | 2,00      |
| CC003       | VS               | 31.1.2017      | FTE-työntekijät                        | Kokoaikaiset työntekijät | 2,00      |

Tämä on esimerkki kustannusten jakosäännöstä, jos kokoaikaisen työntekijän ennalta määritetyn dimension jäsenen kohdistusperuste on määritetty sen kohdistusperusteena.

| Kustannusobjekti | kuvaus  | Suuruus | Kohdistuskerroin |
|-------------|------|-----------|-------------------|
| CC001       | Henkilöstöhallinto   | 1,00      | (1/5) × summa    |
| CC002       | FI   | 2,00      | (2/5) × summa    |
| CC003       | VS   | 2,00      | (2/5) × summa    |

Voit tuoda tilastomittaukset kustannuslaskentaan tuotujen tilastomittausten tietoyksikön avulla. Voit käyttää myös tietojen hallinnan tuonti- ja vientityökalua. Sähkönkulutus kirjataan Exceliin seuraavasti.

| Kirjauspäivä | Dimension jäsen | Suuruus | Lähdetunniste |
|-----------------|------------------|-----------|-------------------|
| 31.1.2017      | CC001            | 2,450.00  | Sähkö       |
| 31.1.2017      | CC002            | 4,100.00  | Sähkö       |
| 31.1.2017      | CC003            | 15,000.00 | Sähkö       |

Seuraavat viennit luodaan kustannuslaskennassa tilastomittausten lähdetietojen käsittelyn jälkeen.

**Tilastomerkinnät**

| Kustannusobjekti |    | Kirjauspäivä | Tilastodimension jäsen |    kuvaus          | Suuruus |
|-------------|----|-----------------|------------------------------|-------------------------|-----------|
| CC001       | Henkilöstöhallinto | 31.1.2017      | Sähkö                  | Sähkönkulutus | 2,450.00  |
| CC002       | FI | 31.1.2017      | Sähkö                  | Sähkönkulutus | 4,100.00  |
| CC003       | VS | 31.1.2017      | Sähkö                  | Sähkönkulutus | 15,000.00 |

Tämä on esimerkki kustannusten jakosäännöstä, jos sähkön ennalta määritetyn dimension jäsenen kohdistusperuste on määritetty sen kohdistusperusteena.

| Kustannusobjekti | kuvaus  | Suuruus | Kohdistuskerroin          |
|-------------|------|-----------|----------------------------|
| CC001       | Henkilöstöhallinto   | 2,450.00  | (2 450 ÷ 21 550) × summa  |
| CC002       | FI   | 4,100.00  | (4 100 ÷ 21 550) × summa  |
| CC003       | VS   | 15,000.00 | (15 000 ÷ 21 550) × summa |

## <a name="hierarchy-allocation-bases"></a>Hierarkian kohdistusperusteet

Kustannuslaskijat voivat luoda hierarkian kohdistusperusteet manuaalisesti käyttämällä kustannusobjektidimension hierarkiasolmua aiemmin luodussa kohdistusperusteessa. Voit rajoittaa tällä tavoin alkuperäisen ennalta määritetyn dimension jäsenen kohdistusperusteen aluetta. Vain ennalta määritetyn dimension jäsenen kohdistusperustetta voidaan käyttää useiden hierarkian kohdistusperusten luontiin. Alueita voidaan ylläpitää siinä kustannusobjektidimension hierarkiassa, joka on liitetty hierarkian kohdistusperusteisiin.

### <a name="example-hierarchy-allocation-bases-that-are-based-on-full-time-employees-in-the-organization"></a>Esimerkki: Organisaation kokoaikaisiin työntekijöihin perustuvat hierarkian kohdistusperusteet
Tämä on esimerkki kustannusobjektidimension hierarkiasta, joka voidaan luoda kuvaamaan yksinkertaistettua organisaatiota.

| Hierarkian nimi | Solmutaso 0 | Solmutaso 1 | Solmutaso 2 | Dimension jäsenet |
|----------------|--------------|--------------|--------------|-------------------|
| Organisaatio   | Toimitusjohtaja          | Talousjohtaja          | FICO         | CC001             |
| Organisaatio   | Toimitusjohtaja          | Talousjohtaja          | Henkilöstöhallinto           | CC002             |
| Organisaatio   | Toimitusjohtaja          | Tietohallintojohtaja          | VS           | CC003             |

Edellisessä osiossa luotu kokoaikaisen työntekijän ennalta määritetyn dimension jäsenen kohdistusperuste sisältää seuraavat viennit.

**Tilastomerkinnät**

| Kustannusobjekti | kuvaus  | Kirjauspäivä | Tilastodimension jäsen | kuvaus | Suuruus |
|-------------|------|-----------------|------------------------------|---------------------|-----------|
| CC001       | Henkilöstöhallinto   | 31.1.2017      | FTE-työntekijät                        | Kokoaikaiset työntekijät | 1,00      |
| CC002       | FI   | 31.1.2017      | FTE-työntekijät                        | Kokoaikaiset työntekijät | 2,00      |
| CC003       | VS   | 31.1.2017      | FTE-työntekijät                        | Kokoaikaiset työntekijät | 2,00      |

Kustannus on jaettava organisaation talouspäällikölle raportoivien kustannuspaikkojen kesken. Oikeaksi kohdistussuhteeksi tiedetään kustannuspaikkakohtainen kokoaikaisten työntekijöiden määrä.

**Hierarkian kohdistusperusteet**

| Nimi                  | Kohdistusperuste | Kustannusobjektin dimensiohierarkia | Kustannusobjektin dimensiohierarkiasolmu |
|-----------------------|-----------------|---------------------------------|--------------------------------------|
| Talousjohtajan kokoaikaisten työntekijöiden määrä | FTE-työntekijät           | Organisaatio                    | Talousjohtaja                                  |

Voit tarkistaa esikatselutoiminnolla hierarkian luodun kohdistusperusteen järjestelmän tilastotulosten perusteella.

**Kohdistusperusteen tiedot**

| Kustannusobjekti | kuvaus  |  Suuruus |
|-------------|------|------------|
| CC001       | Henkilöstöhallinto   | 1,00       |
| CC002       | FI   | 2,00       |

Tämä on esimerkki kustannusten jakosäännöstä, jos kokoaikaisten työntekijöiden määrä talousjohtajan hierarkian kohdistusperusteessa on määritetty sen kohdistusperusteena.

| Kustannusobjekti | kuvaus  | Suuruus | Kohdistuskerroin |
|-------------|------|-----------|-------------------|
| CC001       | Henkilöstöhallinto   | 1,00      | (1/3) × summa    |
| CC002       | FI   | 2,00      | (2/3) × summa    |

## <a name="formula-allocation-bases"></a>Kaavan kohdistusperusteet

Voit määrittää kaavan kohdistusperusteen avulla kaavojen lisäasetuksia oikean kohdistusperusteen saamiseksi. Voit luoda manuaalisesti kaavan kohdistusperusteita.

Kun luot kaavan kohdistusperusteen, valitset, mikä tilastodimensio ja kustannustasodimensio on kaavan peruste. Kaikkia aiemmin valituista dimensioista tulevia kohdistusperusteita voi käyttää kaavan kohdistusperusteena.

> [!NOTE]
> Aiemmin määritettyjä kaavan kohdistusperusteita voi käyttää kaavan uuden kohdistusperusteen määrittämiseen.

Kaavan kohdistusperusteen kertoimissa luodaan alias, joka liitetään joko kohdistusperusteeseen tai vakioon. Aliaksia käytetään sitten kaavan määrittämiseen.

Voit määrittää kaavan seuraavien operaattorien avulla.

| Symboli:t | Teksti           |
|---------|----------------|
| ( )     | Sulkeet    |
| \<      | Pienempi kuin   |
| \>      | Suurempi kuin    |
| +       | Lisäys       |
| –       | Vähennyslasku    |
| \*      | Kertolasku |

Perinteisiä **JOS**-lausekkeita ei tueta. Voit kuitenkin lausekkeita ja tarkistaa niiden totuusarvon.

| Tiliote | Valintasäännöt | Tulos |
|-----------|------------|--------|
| a \> b    | Tosi       | 1      |
| a \> b    | Epätosi      | 0      |

### <a name="example-1-a-simple-formula"></a>Esimerkki 1: Yksinkertainen kaava

Sähkölaskussa on usein kaksi osaa:

- kiinteä sähkönsiirtomaksu
- Kilowattituntikohtainen kulutukseen perustuva kustannus.

Sähkön ennalta määritetty dimension jäsenen kohdistusperuste on jo määritetty, ja se sisältää seuraavat arvot.

**Tilastomerkinnät**

| Kustannusobjekti | Nimi | Kirjauspäivä | Tilastodimension jäsen | kuvaus             | Suuruus |
|-------------|------|-----------------|------------------------------|-------------------------|-----------|
| CC001       | Henkilöstöhallinto   | 31.1.2017      | Sähkö                  | Sähkönkulutus | 2,450.00  |
| CC002       | FI   | 31.1.2017      | Sähkö                  | Sähkönkulutus | 4,100.00  |
| CC003       | VS   | 31.1.2017      | Sähkö                  | Sähkönkulutus | 15,000.00 |

Jos kiinteä maksu on nyt jaettava tasaisesti sähkökuluttavien kustannusobjektien kesken, voit kohdistaa kustannukset kahdella tavalla:

- Voit luoda uuden ennalta määritetyn kohdistusperusteen, Kiinteä sähkö, ja käyttää sitten tilastomittausta, jonka arvo on 1,0, jokaisella sähköä kuluttavalla kustannusobjektilla.
- Voit luoda kaavan kohdistusperusteen, Kiinteä sähkö, joka käyttää järjestelmään jo määritettyä sähkön ennalta määritettyä kohdistusperustetta. Tämän vaihtoehdon etuna on, että tiedot on ladattava kustannuslaskentaan vain yhdelle sähkön tilastodimension jäsenelle.

**Kaavan kohdistusperuste** 

| Nimi              | Kustannustason dimensio | Tilastodimensio | Resepti |
|-------------------|------------------------|-----------------------|---------|
| Kiinteä sähkö |                        | Tilastoelementit  |         |

Ennen **Kaava**-kentän täyttämistä on määritettävä kaavassa käytettävä kaava.

**Kaavan kohdistusperusteen kertoimet**

| Alias | Vakio | Kohdistusperuste |
|-------|----------|-----------------|
| a     |          | Sähkö     |
| b     | 0,01     |                 |

Huomaa, että 0 (nolla) ei ole tuettu vakio.

**Kaavan kohdistusperuste**

| Nimi              | Kustannustason dimensio | Tilastodimensio | Resepti |
|-------------------|------------------------|-----------------------|---------|
| Kiinteä sähkö |                        | Tilastoelementit  | a \> b  |

Voit tarkistaa esikatselutoiminnolla kaavan luodun kohdistusperusteen järjestelmän tilastotulosten perusteella.

**Kohdistusperusteen tiedot**

| Kustannusobjekti | kuvaus  | Resepti           | Suuruus |
|-------------|------|-------------------|-----------|
| CC001       | Henkilöstöhallinto   | 2.450,00 \> 0,01  | 1,00      |
| CC002       | FI   | 4.100,00 \> 0,01  | 1,00      |
| CC003       | VS   | 15.000,00 \> 0,01 | 1,00      |

Tämä on esimerkki kustannusten jakosäännöstä, jos sähkön kaavan kohdistusperuste on määritetty sen kohdistusperusteena.

**Kustannusobjektin suuruuden kohdistuskerroin**

| Kustannusobjekti | Nimi | Suuruus |  Kohdistuskerroin |
|-------------|------|-----------|--------------------|
| CC001       | Henkilöstöhallinto   | 1,00      | (1/3) × summa     |
| CC002       | FI   | 1,00      | (1/3) × summa     |
| CC003       | VS   | 1,00      | (1/3) × summa     |

### <a name="example-2-an-advanced-formula"></a>Esimerkki 2: Lisäasetuksia käyttävä kaava
Tässä esimerkissä sähkön kustannus ei vain seuraa toteutunutta sähkönkulutusta kilowattitunteina. Johto haluaa sisällyttää kannustimen sähkönkulutuksen vähentämiseen. 

| Sääntö              | Osuus | 
|-------------------|------|
| a < = 10 000,00 kWh | 0.75 |
| a > 10 000,00 kWh  | 1.15 |

Kaavan uusi kohdistusperuste, Sähkö käyttö, on luotu.

**Kaavan kohdistusperuste**

| Nimi              | Kustannustason dimensio | Tilastodimensio | Resepti |
|-------------------|------------------------|-----------------------|---------|
| Sähkön käyttö |                        | Tilastoelementit  |         |

Ennen **Kaava**-kentän täyttämistä on määritettävä kaavassa käytettävä kaava.

**Kaavan kohdistusperusteen kertoimet**

| Alias | Vakio  | Kohdistusperuste |
|-------|-----------|-----------------|
| a     |           | Sähkö     |
| b     | 10 000,00 |                 |
| c     | 0.75      |                 |
| d     | 1.15      |                 |

**Kaavan kohdistusperuste**

| Nimi              | Kustannustason dimensio | Tilastodimensio | Resepti                                                    |
|-------------------|------------------------|-----------------------|------------------------------------------------------------|
| Kiinteä sähkö |                        | Tilastoelementit  | ((a \> b) × ((b × c) + (a – b) × d)) + ((a \<= b] × a × c) |

Voit tarkistaa esikatselutoiminnolla kaavan luodun kohdistusperusteen järjestelmän tilastotulosten perusteella.

**Kohdistusperusteen tiedot**

| Kustannusobjekti |    | Resepti                                                                                                                             | Suuruus |
|-------------|----|-------------------------------------------------------------------------------------------------------------------------------------|-----------|
| CC001       | Henkilöstöhallinto | ((2 450,00 \> 10 000,00) × ((10 000,00 × 0,75) + (2 450,00 – 10 000,00) × 1,15)) + ((2 450,00 \<= 10 000,00) × 2 450,00 × 0,75)     | 1,837.50  |
| CC002       | FI | ((2 450,00 \> 10 000,00) × ((10 000,00 × 0,75) + (2 450,00 – 10 000,00) × 1,15)) + ((2 450,00 \<= 10 000,00) × 2 450,00 × 0,75)     | 3,075.00  |
| CC003       | VS | ((2 450,00 \> 10 000,00) × ((10 000,00 × 0,75) + (2 450,00 – 10 000,00) × 1,15)) + ((2 450,00 \<= 10 000,00) × 2 450,00 × 0,75) | 1,3250.00 |

Seuraavaksi tarkastellaan lähemmin CC003 (IT):n kaavaa:

((15 000,00 \> 10 000,00) × ((10 000,00 × 0,75) + (15 000,00 – 10 000,00) × 1,15)) + ((15 000,00 \<= 10 000,00) × 15 000,00 × 0,75) = 13 250,00

(1 × (7 500,00 + 5 000,00 × 1,15)) + (0 × 15 000,00 × 0,75)            

1 × 7 500,00 + 5 750,00 + 0 

Tämä on esimerkki kustannusten jakosäännöstä, jos Kiinteä sähkö -kaavan kohdistusperuste on määritetty sen kohdistusperusteena.

| Kustannusobjekti |  kuvaus  | Suuruus | Kohdistuskerroin                |
|-------------|----|-----------|----------------------------------|
| CC001       | Henkilöstöhallinto | 1,837.50  | (1 837,50 ÷ 18 162,50) × summa  |
| CC002       | FI | 3,075.00  | (3 075,00 ÷ 18 162,50) × summa  |
| CC003       | VS | 13,250.00 | (13 250,00 ÷ 18 162,50) × summa |

