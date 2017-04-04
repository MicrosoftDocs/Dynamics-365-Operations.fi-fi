---
title: "Muotoilun lisäasetukset taloushallinnon raporteissa"
description: "Luodessasi raportin taloushallinnon raportoinnissa, sen muotoiluun on käytettävissä lisätoimintoja, kuten dimensiosuodattimia, rajoituksia sarakkeille ja raportoinnin yksiköille, ei-tulostettavia rivejä IF/THEN/ELSE -lausekkeita laskutoimituksissa."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter
ms.custom: 106571
ms.assetid: 895b5127-01d6-4495-b127-343387b743aa
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 631fec1dc135565e6d38e7faf193a7a898b508cb
ms.lasthandoff: 03/29/2017


---

# <a name="advanced-formatting-options-in-financial-reporting"></a>Muotoilun lisäasetukset taloushallinnon raporteissa

Luodessasi raportin taloushallinnon raportoinnissa, sen muotoiluun on käytettävissä lisätoimintoja, kuten dimensiosuodattimia, rajoituksia sarakkeille ja raportoinnin yksiköille, ei-tulostettavia rivejä IF/THEN/ELSE -lausekkeita laskutoimituksissa. 

Seuraavassa taulukossa kuvataan muotoilun lisäasetustoiminnot, jotka ovat käytettävissä, kun luot raportteja.

| Toiminto                   | Kuvaus                                                                                                                                                                                                                                                                                                                     |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dimensiosuodatin           | Voit käyttää haluamiasi tietojoukkoja rivi- ja sarakemäärityksien dimensioiden avulla. Moni raportti käyttää ainoastaan luonnollista segmenttiä rivimuodossa. Rivejä voidaan kuitenkin muokata niin, että ne sisältävät dimensioarvot. Haluttuja dimensioarvoja voi käyttää sarakkeen määrityksessä olevien dimensiosuodattimien avulla. |
| Raportointiyksikköön rajaaminen | Voit määrittää raporttirivin niin, että siinä näkyvät vain tiedot, jotka on yhdistetty tiettyyn raportointiyksikköön.                                                                                                                                                                                                                      |
| Piilotetut rivit (NP)     | Piilotetut rivit ovat hyödyllisiä useissa raporteissa. Jos arvon saamiseen tarvitaan useita laskutoimituksia, ne voidaan piilottaa tulostetulta raportilta. Piilotettuja rivejä voi myös käyttää raporttimallien ja edistyneempien solusijoitteluiden vianmääritykseen.                                                    |
| Sarakkeen rajoitus         | Sarakkeen rajoitus rivimäärityksessä on hyödyllinen, jos haluat piilottaa arvoja, jotka vaikuttavat vain joihinkin raporttiriveihin. Kun rivillä suoritetaan prosenttilaskutoimituksia, sarakkeen rajoitus estää sekä loppusummasarakkeiden että muiden sarakkeiden tulostamisen silloin, kun ko. numerot eivät ole käytössä.                              |
| Sarakkeen vaihto               | Voit lisätä sarakkeen vaihtoja rivin määrittelyyn näyttääksesi raportin tietoja rinnakkain. Voit lisätä useita sarakkeen vaihtoja yhden rivin määritykseen; sarakeotsikot toistuvat jokaisen sarakkeen yläosassa vaihdon jälkeen. Raportin kommentit näytetään sarakevaihtojen välissä.                              |
| IF/THEN/ELSE -lauseke     | Voit muokata rivi- tai sarakemäärityksen laskutoimituksia.                                                                                                                                                                                                                                                         |

## <a name="advanced-cell-placement"></a>Edistynyt solujen sijoittelu
Edistynyt solujen sijoittelu, tai *pakottaminen*, on tiettyjen arvojen sijoittamista tiettyihin soluihin. Pakottamista käytetään esimerkiksi oikean saldon siirtämiseen kassavirtaraportilla. Pakottamista voi käyttää seuraaviin tarkoituksiin:

-   Arvojen siirtäminen Microsoft Excelistä tiettyihin soluihin.
-   Tiettyjen arvojen kovakoodaaminen raporttiin.
-   Merkkien muokkaaminen kopioimalla arvo edellisestä solusta ja kertomalla ko. arvo -1:llä.

**Huomautus:** raportin määritys on usein tehtävä niin, että sarakkeiden laskutoimitukset suoritetaan ennen rivien laskutoimituksia. Voit tehdä tämän määrityksen noudattamalla seuraavia ohjeita.

1.  Avaa raportin suunnitteluohjelmassa raportin määritys.
2.  Valitse **Asetukset** -välilehden **Laskennan prioriteetti** -kohdasta **Suorita sarakkeen laskutoimitukset ennen rivejä**.

## <a name="designing-the-report"></a>Raportin suunnitteleminen
Kun olet suunnitellut raportin, sinun on ensin luotava kaikki erittelyrivit ja varmistettava, että arvot näkyvät odotetulla tavalla. Lisää sitten **NP** (Piilotettu) -muotoiluja piilottamaan yksityiskohdat, joihin lopulliset arvot sisältyvät. **Tärkeää:** Kun käytät **CAL**-muotoilukoodia rivin määrityksessä, et voi porautua tapahtumatietoihin. Pakottaminen, kaavoja käyttämällä seuraavaa muotoa: &lt;kohde-sarake&gt;=&lt;peräisin sarake&gt;. &lt;rivin koodi&gt; erottaa mitään muita harjoittelu riville pilkku ja välilyönti. Esimerkki: D=C.190,E=C.100

## <a name="examples-of-advanced-formatting-options"></a>Esimerkkejä muotoilun lisäasetuksista
Seuraavissa esimerkeissä esitellään, miten rivi- ja sarakemääritys muotoillaan pakottamaan yksinkertainen kassavirtaraportti (esimerkki 1) ja tilastollinen raportti (esimerkki 2).

### <a name="example-1-basic-forcing"></a>Esimerkki 1: Yksinkertainen pakottaminen

Seuraavassa taulukossa on esimerkki rivin määrityksestä, jossa käytetään yksinkertaista pakottamista.

| Rivin koodi | Kuvaus                      | Muotoilukoodi | Liittyvät kaavat/rivit/yksiköt | Muotoilun ohitus | Normaali saldo | Tulostuksen hallinta | Sarakkeen rajoitus | Rivin muuttuja               | Linkki taloushallinnon dimensioihin |
|----------|----------------------------------|-------------|-----------------------------|-----------------|----------------|---------------|--------------------|----------------------------|------------------------------|
| 100      | Kassa kauden alussa (NP) |             |                             |                 |                |               |                    | Määrite tilin = \[/BB\] | + Segment2 = \[1100\]         |
| 130      | Kassa kauden alussa      | CAL         | C=C.100,F=D.100             |                 |                |               |                    |                            |                              |
| 160      |                                  |             |                             |                 |                |               |                    |                            |                              |
| 190      |                                  |             |                             |                 |                |               |                    |                            |                              |

Seuraavassa taulukossa on esimerkki sarakkeen määrityksestä, jossa käytetään yksinkertaista pakottamista rivillä.

|                              | A   | B    | K        | D      | E      | P    |
|------------------------------|-----|------|----------|--------|--------|------|
| Ylätunniste 1                     |     |      |          |        |        |      |
| Ylätunniste 2                     | A   | B    | K        | D      | E      | P    |
| Ylätunniste 3                     |     |      |          |        |        |      |
| Sarakelaji                  | RIVI | KUVAUS | FD       | FD     | FD     | LASKENTA |
| Kirjakoodi/määriteluokka |     |      | TODELLINEN   | TODELLINEN | TODELLINEN |      |
| Tilikausi                  |     |      | PERUS     | PERUS   | PERUS   |      |
| Kausi                       |     |      | PERUS     | PERUS   | PERUS   |      |
| Katetut kaudet              |     |      | KAUSITTAINEN | VUODEN ALUSTA/BB | VUODEN ALUSTA    |      |
| Resepti                      |     |      |          |        |        | E-D  |
| Sarakkeen leveys                 | 5   | 30   | 14       | 14     | 14     | 14   |

### <a name="example-2-statistical-reports"></a>Esimerkki 2: Tilastolliset raportit

Seuraavassa taulukossa on esimerkki rivin määrityksestä, jossa käytetään pakottamista tilastollisessa raportissa.

| Rivin koodi | Kuvaus               | Muotoilukoodi | Liittyvät kaavat/rivit/yksiköt     | Muotoilun ohitus      | Normaali saldo | Tulostuksen hallinta | Sarakkeen rajoitus | Rivin muuttuja | Linkki taloushallinnon dimensioihin               |
|----------|---------------------------|-------------|---------------------------------|----------------------|----------------|---------------|--------------------|--------------|--------------------------------------------|
| 50       | Tilastotiedot   | MAKS         |                                 |                      |                |               |                    |              |                                            |
| 100      | Henkilöstön määrä - US            | CAL         | 4                               | \#\#\#0.;($\#\#\#0.) |                |               |                    |              |                                            |
| 115      | Henkilöstön määrä - Kansainv. | CAL         | 11                              | \#\#\#0.;($\#\#\#0.) |                |               |                    |              |                                            |
| 130      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 190      | Myynti, USA                  |             |                                 |                      | K              |               |                    |              | + Segment2 = \[41\*\], Segment3 = \[00\]    |
| 220      | Myynti, kv.       |             |                                 |                      | K              |               |                    |              | + Segment2 = \[41\*\], Segment3 = \[01:99\] |
| 250      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 280      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 310      | Myynti, USA                  | CAL         | D=C.190,E=C.100,F=(C.100/C.190) |                      |                |               |                    |              |                                            |
| 340      | Myynti, kv.       | CAL         | D=C.220,E=C115,F=(C.220/C.115)  |                      |                |               |                    |              |                                            |

Seuraavassa taulukossa on esimerkki sarakkeen määrityksestä, jossa käytetään pakottamista tilastollisessa raportissa.

|                              | A   | B    | K      | D            | E     | P            |
|------------------------------|-----|------|--------|--------------|-------|--------------|
| Ylätunniste 1                     | A   | B    | K      | D            | E     | P            |
| Ylätunniste 2                     | -   | -    | Vuoden alusta    | Vuosittainen myynti | Henkilökunta | $ henkilöä kohti |
| Ylätunniste 3                     |     |      |        |              |       |              |
| Sarakelaji                  | RIVI | KUVAUS | FD     | LASKENTA         | LASKENTA  | LASKENTA         |
| Kirjakoodi/määriteluokka |     |      | TODELLINEN |              |       |              |
| Tilikausi                  |     |      | PERUS   |              |       |              |
| Kausi                       |     |      | PERUS   |              |       |              |
| Katetut kaudet              |     |      | VUODEN ALUSTA    |              |       |              |
| Resepti                      |     |      |        |              |       | E-D          |
| Sarakkeen leveys                 | 5   | 30   | 14     | 14           | 14    | 14           |

## <a name="restricting-a-row-to-a-specific-reporting-unit"></a>Rivin rajoittaminen tiettyyn raportointiyksikköön
Raportin rivin ollessa rajoitettu tiettyyn raportoinnin yksikköön, rivillä näytetään ainoastaan nimettyyn yksikköön linkitetyt tiedot, ohittaen muiden raportointipuussa olevien yksiköiden tiedot. Voit esimerkiksi luoda rivin, joka sisältää yksityiskohtaisia tietoja tietyn osaston kokonaistoimintakuluista. Raportti voi sisältää kaksoisarvoja, jos raportti sisältää sekä raportointipuun että rivin määrityksen, johon sisältyy useampi kuin ainoastaan luonnollinen tili. Esimerkkinä raportoinnin puurakenne, jossa luetellaan organisaation kuusi osastoa, sekä rivin määritys, jossa luetellaan rivillä oleva tietyn tilin ja osaston yhdistelmä. Raporttia luodessa tietyn tilin ja osaston yhdistelmä tulostetaan jokaiselle raportointipuun tasolle, vaikka osasto ei välttämättä vastaisikaan puurakenteen sisältöä. Näin tapahtuu, koska rivi ohittaa raportin määrityksessä yleensä suodatetun tiedon. Eräs tapa estää kahdennettujen tietojen ilmenemistä on rajoittaa rivi tiettyyn raportoinnin yksikköön. **Huomautus:** Jos rivi sisältää dimensioita ja rajoitat sen raportoinnin aliyksikköön, rivin summa sisältyy aliyksikköön sekä sen ylempiin yksiköihin, mutta tiedot eivät kahdennu.

### <a name="restrict-a-row-to-a-reporting-unit"></a>Rivin rajoittaminen raportointiyksikköön

1.  Valitse Report Designerissa **Rivien määritykset** ja valitse sitten muokattava rivin määritys.
2.  Kaksoisnapsauta haluamaasi **Liittyvät kaavat/rivit/yksiköt** -solua.
3.  Valitse **Raportoinnin yksikön valinta** -valintaikkunan **Raportointipuu**-kentästä puu, joka liitetään raportin määritykseen.
4.  Valitse raportoinnin yksikkö ja napsauta **OK**. Rajoitus näkyy rivin määrityksen solussa.
5.  Kaksoisnapsauta **Linkitä Taloushallinnon dimensio** -sarakkeen rajoitetun rivin solua ja kirjoita linkki taloushallinnon järjestelmään.

## <a name="selecting-print-control-in-a-row-definition"></a>Tulostuksen hallinnan valinta rivin määrityksessä
Voit määrittää tulostuksen hallintakoodin jokaiselle sarakkeelle **Tulostuksen hallinta** -solun avulla.

### <a name="add-print-control-codes-to-a-report-row"></a>Tulostuksen hallintakoodin lisääminen raportin riville

1.  Avaa Report Designer -ohjelmassa muokattava rivin määritys.
2.  Kaksoisnapsauta **Tulostuksen hallinta** -solua.
3.  Valitse **Tulostuksen hallinta** -valintaikkunasta tulostuksen hallintakoodi; voit valita useamman koodin pitämällä Ctrl-näppäimen pohjassa. Voit myös kirjoittaa tulostuksen hallintakoodeja suoraan **Tulostuksen hallinta** -soluun. Erota tulostuksen hallintakoodit pilkuilla.
4.  Valitse tulostusasetusten ehdot.
5.  Napsauta **OK**.

### <a name="regular-print-control-codes"></a>Tavalliset tulostuksen hallintakoodit

Seuraavassa taulukossa kuvataan rivimääritykselle käytettävissä olevat tavanomaiset tulostuksen hallintakoodit.

| Tulostuksen hallintakoodi | Tulostuksen hallintakoodin tulkitseminen         | Kuvaus                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NP                 | Piilotettu rivi                                 | Estää rivin summien tulostumisen raportille sekä summien käytön laskennassa. Voit ottaa piilotetun sarakkeen mukaan laskutoimitukseen viittaamalla sarakkeeseen suoraan laskentakaavassa. Esimerkkinä piilotettu rivi 240 sisällytetään seuraavaan laskutoimitukseen: **230+240+250**. Piilotettua riviä 240 ei kuitenkaan sisällytetä seuraavaan laskutoimitukseen: **230:250**. |
| CS                 | Valuuttasymboli; käytä tällä rivillä olevaa valuuttamuotoa | Käyttää valuuttasymbolia kaikissa summissa, poislukien prosenttiosuudet. Prosenttiosuuksissa ei ole koskaan valuuttasymbolia.                                                                                                                                                                                                                                                                                                |
| XD                 | Piilota rivi tilin lisätietojen raportilla            | Estää tilien näyttämisen tilin lisätietojen raporteilla sekä tapahtuman lisätietoraporteilla. Tämä tulostuksen hallintakoodi on hyödyllinen, jos rivi sisältää useita tilejä, joiden ei tule näkyä tilin lisätietoraportilla tai tapahtuman lisätietoraportilla.                                                                                                                                                           |
| X0                 | Piilota rivi, jos kaikki nollia                        | Poista rivi raportista, jos kaikki rivin solut ovat tyhjiä tai sisältävät vain nollia. Tämä hallintakoodi on tärkeä ainoastaan silloin, kun nollasaldojen estäminen ei ole valittuna raportin määrityksessä.                                                                                                                                                                                            |
| B0                 | Jätä nolla-sarakkeet tyhjäksi                         | Jättää ne sarakkeet, jotka eivät sisällä lainkaan summia tyhjäksi.                                                                                                                                                                                                                                                                                                                                                      |
| XR                 | Piilota koonti                                  | Piilota koonti. Jos raportissa käytetään raportointipuuta, tämän rivin summia ei koota vastaaviksi ylätason solmuiksi.                                                                                                                                                                                                                                                                               |
| SR                 | Estä pyöristys                                | Estää tämän rivin summien pyöristyksen.                                                                                                                                                                                                                                                                                                                                                          |
| XT                 | Piilota rivin tapahtuman lisätietoraportilla        | Estää tapahtumien näyttämisen tapahtuman lisätietoraportilla. Tämä tulostuksen hallintakoodi on hyödyllinen, jos rivi sisältää useita tilejä, joiden ei tule näkyä tapahtuman lisätietoraportilla.                                                                                                                                                                                                             |

### <a name="conditional-print-control-codes"></a>Ehdolliset tulostuksen hallintakoodit

Seuraavassa taulukossa kuvataan rivimääritykselle käytettävissä olevat tulostuksen ehdolliset hallintakoodit.

| Tulostuksen hallintakoodi | Kuvaus                                  |
|--------------------|----------------------------------------------|
| (ei mitään)             | Poista ehdollisen tulostuksen valinta.       |
| PR                 | Tulostaa ainoastaan tämän rivin veloitussaldot.  |
| CR                 | Tulostaa ainoastaan tämän rivin maksettavat saldot. |

## <a name="column-restriction-cell-in-a-row-definition"></a>Sarakkeen rajoitus -solu rivin määrityksessä
**Sarakkeen rajoitus** -solulla on useita toimintoja rivin määrityksessä. Voit käyttää **Sarakkeen rajoitus** -solua, rivin tyypistä riippuen, määrittääksesi seuraavat toiminnot:

-   Solu rajoittaa rivin summien tulostamisen yhteen sarakkeeseen. Tästä toiminnosta on hyötyä, jos olet luomassa taulukkomuotoista tasetta.
-   Soluun on mahdollista määrittää lajiteltava summien sarake.

## <a name="using-a-calculation-formula-in-a-row-definition"></a>Laskentakaavan käyttäminen rivin määrityksessä
Rivimääritys-laskukaava voi sisältää **+**, **-**, **\***, ja **/**toimijoita, ja myös **sitten/Jos/ELSE** lauseita. Lisäksi, laskutoimituksessa voi käyttää yksittäisiä soluja ja absoluuttisia summia (todellisia lukuja, jotka sisältyvät kaavaan). Kaava voi sisältää enintään 1 024 merkkiä. Laskentakaavoja ei voi käyttää riveille, jotka sisältävät **Linkki taloushallinnon dimensioon** (FD) -tyypin soluja. Voit kuitenkin käyttää laskentakaavoja peräkkäisille riveille, piilottaa kyseiset rivit tulostukselta ja laskea yhteen laskentarivien summat.

### <a name="operators-in-a-calculation-formula"></a>Laskentakaavan operaattorit

Laskentakaavassa on mahdollista käyttää monimutkaisempia operaattoreita kuin rivin summakaavassa. Kuitenkin voit käyttää **\***ja **/**muita operaattoreita, jos haluat kertoa yhdessä toimijoiden (\*) ja jakaa summat (/). Jos haluat käyttää aluetta tai summaa laskentakaavassa, sinun on käytettävä ät-merkkiä (@) jokaisen rivikoodin edessä, ellet käytä saraketta rivin määrityksessä. Esimerkiksi, voit lisätä Summa-rivin 100 Summa-rivin 330, voit käyttää rivin yhteensä kaavan **100 + 330** tai laskentakaava **@100+@330**. **Huomautus:** ät-merkkiä (@) on käytettävä ennen jokaista rivin koodia, jota käytetään laskukaavassa. Muutoin luku luetaan absoluuttisena summana. Esimerkiksi kaava **@100+330** USD 330 Lisää summa-rivin 100. Ät-merkki (@) ei ole pakollinen viitattaessa laskentakaavan sarakkeeseen.

### <a name="create-a-calculation-formula"></a>Laskentakaavan luominen

1.  Valitse Report Designerissa **Rivien määritykset** ja avaa muokattava rivin määritys.
2.  Kaksoisnapsauta **Muotoilukoodi** -solua ja valitse sitten **CAL**.
3.  Kirjoita laskentakaava **Liittyvät kaavat/rivit/yksiköt** -soluun.

### <a name="example-of-a-calculation-formula-for-specific-rows"></a>Esimerkki tiettyjä rivejä koskevasta laskukaavasta

Tässä esimerkissä laskentakaava **@100+@330** 100-rivin summa lisätään 330 rivin summa tarkoittaa. Rivin Summa kaava **340 + 370** Lisää 340 riville summa Summa-rivillä 370. (Summa-rivillä 370 on summan laskenta-kaava).

| Rivin koodi | Kuvaus                 | Muotoilukoodi | Liittyvät kaavat/rivit/yksiköt | Tulostuksen hallinta | Rivin muuttuja | Linkki taloushallinnon dimensioihin |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Kassa kauden alussa |             |                            | NP            | BB           | + Tili =\[1100:1110\]       |
| 370      | Kassa vuoden alussa   | CAL         | @100+@330                  | NP            |              |                              |
| 400      | Kassa kauden alussa | TOT         | 340+370                    |               |              |                              |

Kun rivimäärityksen rivillä on muotoilukoodi **CAL** ja kirjoitat matemaattisen laskentakaavan **Liittyvät kaavat/rivit/yksiköt** -soluun, sinun on syötettävä myös liittyvän sarakkeen kirjain ja raportin rivi. Esimerkiksi **A.120** edustamaan sarakkeen A rivi 120. Voit myös käyttää ät-merkki (@) osoittamaan kaikki sarakkeet. Esimerkiksi **@120**edustamaan 120-rivin kaikkia sarakkeita. Matemaattisen laskutoimituksen, joka ei ole sarakkeen kirjaimen tai at-merkillä (@) oletetaan olevan reaaliluku. **Huomautus:** Jos käytät viittaamaan rivin otsikko rivillä koodi, piste (.) on käytettävä sarakkeen kirjaimen ja otsikko väliin erotinpalkin (esimerkiksi **A.GROSS\_MARGIN/A.SALES**). Jos käytät ät-merkki (@), erotin ei tarvita (esimerkiksi **@GROSS\_MARGIN/@SALES**).

### <a name="example-of-a-calculation-formula-for-a-specific-column"></a>Esimerkki tiettyä saraketta koskevasta laskukaavasta

Tässä esimerkissä laskentakaavan **E=C.340** tarkoittaa, että sarakkeen C ja rivin 340 kohdassa olevaa solua koskeva laskenta suoritetaan vain sarakkeessa E. **Huomautus:** kun laskentakaavassa viitataan sarakkeeseen, ät-merkki (@) ei ole pakollinen.

| Rivin koodi | Kuvaus                 | Muotoilukoodi | Liittyvät kaavat/rivit/yksiköt | Tulostuksen hallinta | Rivin muuttuja | Linkki taloushallinnon dimensioihin |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Kassa kauden alussa |             |                            | NP            | BB           | + Tili =\[1100:1110\]       |
| 370      | Kassa vuoden alussa   | CAL         | E=C.340                    | NP            |              |                              |
| 400      | Kassa kauden alussa | TOT         | 340+370                    |               |              |                              |

### <a name="modifying-a-number-in-selected-columns"></a>Valituissa sarakkeissa olevan numeron muuttaminen

Kun muokkaat tietyn sarakkeen tietyllä rivillä olevaa numeroa tai laskentakaavaa, etkä halua muutosten vaikuttavan muihin raportin sarakkeisiin, voit määrittää rivimäärityksen **Muotoilukoodi**-sarakkeeseen koodiksi **CAL** (Laskenta).

-   Laskutoimituksen kaikille raportin (**FD**) sarakkeille voit suorittaa siten, että et lisää sarakkeen määritystä.
-   Rajoitetaan kaavassa sarakkeita kirjoittamalla sarakkeen kirjaimen, yhtäläisyysmerkki (**=**), ja sitten kaava.
-   Voit määrittää useita sarakkeita. Kun käytät ät-merkkiä (@) tietyllä sarakkeen sijoittelulla, ät-merkki (@) liittyy riviin.
-   Voit määrittää useamman sarakekaavan yhdelle riville. Erota kaavat toisistaan pilkuilla.

### <a name="calculation-examples"></a>Esimerkkejä laskutoimituksista

| Laskelma            | Luotava toiminto                                                                                                   |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| @130\*.75              | Jokaisen riville 130 kuuluvan sarakkeen arvo kerrotan 0,75:llä. Tulos sijoitetaan jokaisen sarakkeen nykyiselle riville. |
| B=@130\*.75            | Sama laskenta suoritetaan vain sarakkeessa B.                                                                      |
| A, B,C=(@100/@130)\*.75 | A=(A.100/A.130)\*.75 B=(B.100/B.130)\*.75 C=(C.100/C.130)\*.75                                                           |

### <a name="ifthenelse-statements-in-a-row-definition"></a>IF/THEN/ELSE (jos/sitten/muuten)-lausekkeet rivimäärityksessä

**IF/THEN/ELSE** -lausekkeita on mahdollista lisätä mihin tahansa kelvolliseen laskutoimitukseen, ja niitä voi käyttää **CAL**-muodossa. Voit määrittää **IF/THEN/ELSE** -laskentakaavoja **Liittyvät kaavat/rivit/yksiköt** sarakkeen soluun. **SITTEN/Jos/ELSE** laskennan kaavat käyttävät seuraavaa muotoa: Jos &lt;tosi/epätosi-lauseke&gt; sitten &lt;kaavan&gt; muuten &lt;kaavan&gt;**muuten &lt;kaavan&gt;** lauseeseen on valinnainen.

#### <a name="if-statements"></a>IF-lausekkeet

Lauseke, joka seuraa **IF**-lauseketta voi olla mikä tahansa lauseke, joka voi olla joko tosi tai epätosi. Lauseke, joka seuraa **IF**-lauseketta voi olla yksinkertainen arvio tai monimutkainen lauseke, joka voi sisältää useita lausekkeita. Seuraavassa on muutamia esimerkkejä:

-   **Jos A.200&gt;0** (yksinkertainen arviointi)
-   **Jos A.200&gt;0-A.200&lt;10 000** (Monimutkainen lauseke)
-   **Jos A.200&gt;10000 tai ((A.340/B.1200)\*2 &lt;1200)** (Monimutkainen lauseke, joka sisältää useita lausekkeita)

Termillä **Kaudet** tarkoitetaan **IF**-lausekkeessa raportilla olevien kausien määrää. Termiä käytetään yleensä laskemaan keskiarvo vuoden alusta. Esimerkiksi, kun ajat kauden 7 YTD-raportin, **B.150/Periods** tarkoittaa, että sarakkeen B rivin 150 arvo jaetaan 7:llä.

#### <a name="then-and-else-formulas"></a>THEN ja ELSE -kaavat

**THEN** ja **ELSE** -kaavat voivat olla mikä tahansa kelpaava laskutoimitus, yksinkertaisista arvon määrityksistä monimutkaisiin kaavoihin. Esimerkiksi lause **Jos A.200&gt;0, sitten A=B.200** tarkoittaa "Jos solun sarakkeessa A rivillä 200 on enemmän kuin 0 (nolla)-arvon laittaa nykyisen rivin sarakkeen A solu sarakkeessa B 200 rivin solu." Edeltävä **IF/THEN** -lauseke sijoittaa arvon yhteen nykyisen rivin sarakkeeseen. Voit käyttää myös ät-merkkiä (@) sekä tosi/epätosi-arvioinneissa että kaavassa edustaen kaikkia sarakkeita. Seuraavat ovat muita esimerkkejä, jotka kuvaillaan seuraavissa osissa:

-   **Jos A.200 &gt;0, sitten B.200**: A.200-solun arvo on positiivinen, jos nykyisen rivin jokaisen sarakkeen arvon solun B.200 otetaan käyttöön.
-   **Jos A.200 &gt;0, sitten @200**: A.200-solun arvo on positiivinen, jos jokaisesta sarakkeesta 200-rivin arvo on otettu käyttöön vastaavan sarakkeen nykyisen rivin.
-   **Jos @200&gt;0, sitten @200**: 200-rivin nykyiseen sarakkeeseen arvo on positiivinen, jos nykyisen rivin saman sarakkeen arvon rivin 200 otetaan käyttöön.

### <a name="restricting-a-calculation-to-a-reporting-unit-in-a-row-definition"></a>Laskutoimituksen rajoittaminen raportoinnin yksikköön rivin määrityksessä

Voit rajoittaa laskennan ja raportoinnin puussa laativan yhdessä niin, että tuloksena oleva summa ei ole koottu ylemmän tason yksikköön, **@Unit**koodi **liittyvät kaavat/riviä/yksiköt** rivimääritys-solussa. **@Unit**Koodi näkyy sarakkeessa B reporting puun **nimi**. Kun käytät **@Unit**koodia arvot eivät ole alitehtävien kokoaminen, mutta laskennassa arvioidaan raportointi puun kaikilla tasoilla. **Huomautus:** Jotta voisit käyttää tätä toimintoa, rivimääritykseen on liitettävä raportointipuu. Laskentarivi voi viitata laskennan tai kirjanpitotietojen riviin. Laskutoimitus kirjataan rivimäärityksen **Liittyvät kaavat/rivit/yksiköt** -soluun sekä taloushallinnon tietotyypin rajoitukseen. Laskennassa täytyy käyttää ehdollista laskelman, joka alkaa **Jos @Unit**rakentamiseen. Tässä on esimerkki: Jos @Unit(myynti) sitten @100muuten 0 Tämä laskenta sisältää 100 rivin välein raportin sarakkeen summa mutta vain myynti-yksikköä. Jos järjestelmässä on useita SALES-yksiköitä, määrä näytetään kaikissa yksiköissä. Lisäksi rivi 100 voi olla taloushallinnon tietorivi, ja se voidaan määrittää piilotetuksi. Tässä tapauksessa summan näyttäminen estetään kaikissa puun yksiköissä. Voit myös rajoittaa summan yhteen raportin sarakkeeseen, kuten sarake H, käyttämällä sarakerajoitusta tulostamaan arvon ainoastaan kyseiseen raportin sarakkeeseen. Voit sisällyttää **OR**-yhdistelmiä **IF**-lausekkeisiin. Tässä on esimerkki: Jos @Unit(myynti) tai @Unit(SALESWEST) 5 sitten muuten @100voit määrittää yksikön laskentatyyppi rajoituksen jollakin seuraavista tavoista:

-   Kirjoita yksikön nimen kohdalle kelpaava yksikkö. Esimerkiksi **Jos @Unit(myynti)** avulla laskentaan kaikki yksikön, jonka nimi on myynti, vaikka raportoinnin puussa on useita myynnin yksiköt.
-   Kirjoita yrityksen ja yksikön nimi rajoittaaksesi laskutoimitus tietyn yrityksen tiettyihin yksikköihin. Esimerkiksi **Jos @Unit(ACME: myynti**) rajoittaa ACME yrityksen myynnin yksiköt laskenta.
-   Kirjoita koko hierarkiakoodi raportointipuusta rajoittaaksesi laskutoimituksen tiettyyn yksikköön. Esimerkiksi **Jos @Unit(yhteenveto ^ ACME ^ LÄNSIRANNIKOLLA ^ myynti)**. **Huomautus:** Täydellisen hierarkiakoodin löydät napsauttamalla hiiren oikealla painikkeella raportointipuun määritystä ja valitsemalla sitten **Kopioi raportointiyksikön tunniste (H-koodi)**.

#### <a name="restrict-a-calculation-to-a-reporting-unit"></a>Laskutoimituksen rajoittaminen raportointiyksikköön

1.  Valitse Report Designerissa **Rivien määritykset** ja avaa muokattava rivin määritys.
2.  Kaksoisnapsauta **Muotoilukoodi** -solua ja valitse sitten **CAL**.
3.  Valitse **liittyvät kaavat/riviä/yksiköt** solu ja kirjoita sitten Ehdollinen laskelman, joka alkaa **Jos @Unit**rakentamiseen.

### <a name="ifthenelse-statements-in-a-column-definition"></a>IF/THEN/ELSE (jos/sitten/muuten)-lausekkeet sarakemäärityksessä

**IF/THEN/ELSE**-lausekkeiden avulla voit tehdä minkä tahansa laskutoimituksen riippuvaiseksi mistä tahansa toisesta sarakkeesta. Voit viitata **IF**-lausekkeessa muihin sarakkeisiin, mutta et raportin soluun. Kaikkien laskutoimitusten on koskettava kokonaista saraketta. Esimerkiksi lause **Jos B&gt;100 ja muut B-C\*1,25** tarkoittaa "sarakkeessa B on suurempi kuin 100, jos sijoittaa arvon sarakkeesta B **laskenta** sarakkeen. Jos B-sarakkeen summa on pienempi kuin 100, C-sarakkeen arvo kerrotaan 1,25:llä ja tulos sijoitetaan **CALC**-sarakkeeseen. " **IF**-lauseketta on aina seurattava looginen lauseke, jonka tulos on joko tosi tai epätosi. Sekä **THEN**- ja **ELSE**-lausekkeet voivat viittauksia rajoittamattomaan määrään sarakkeita, ja kyseiset kaavat voivat olla juuri niin monimutkaisia kuin haluat. **Huomautus:** Et voi sijoittaa laskutoimituksen tuloksia mihinkään muuhun sarakkeeseen. Tulosten on oltava sarakkeessa, joka sisältää kaavan.


