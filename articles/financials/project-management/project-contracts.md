---
title: Projektisopimukset
description: Tässä ohjeaiheessa käsitellään esimerkkien avulla erityyppisille projekteille ja rahoituslähteille luotavia projektisopimuksia, sopimusten hallintaa ja projektin asiakkaiden laskuttamista Microsoft Dynamics 365 for Finance and Operationsissa.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0f0fcec64ce03c6e1d877fb1c8d004bb416bd95
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "310366"
---
# <a name="project-contracts"></a>Projektisopimukset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään esimerkkien avulla erityyppisille projekteille ja rahoituslähteille luotavia projektisopimuksia, sopimusten hallintaa ja projektin asiakkaiden laskuttamista Microsoft Dynamics 365 for Finance and Operationsissa.

Projektisopimukselle luotavan projektin tyyppi määrittää, miten projektin asiakkaita laskutetaan. Vaikka voit muuttaa projektisopimusta ja siihen liittyvää projektia, et voi vaihtaa projektityyppiä. 

Projektisopimuksen avulla voit laskuttaa yhden projektin tai useita projekteja samanaikaisesti. Projektisopimus auttaa lisäksi varmistamaan, että projektirakenteen kaikissa aliprojekteissa käytetään yhdenmukaista laskutusmenettelyä. 

Jokainen laskutettava projekti on liitettävä johonkin projektisopimukseen. Projektisopimuksen asetukset koskevat kaikkia projektisopimukseen liittyviä projekteja ja aliprojekteja. 

Projektisopimus voi määrittää vähintään yhden rahoituslähteen. Niinpä voitkin jakaa laskutuksen usean rahoittajan kesken, määrittää rahoitusrajat niin, että rahoituslähteiltä laskutetaan enintään määritetty summa, ja määrittää rahoitussäännöt menojen laskuttamista varten.

## <a name="funding-for-project-contracts"></a>Projektisopimusten rahoitus
Joissakin projektisopimuksissa määritetään, että useat osapuolet jakavat projektikustannusten rahoitusvastuun. Seuraavassa on muutamia esimerkkejä:

-   Suuri asiakas, jolla on useita divisioonia, pyytää rahoituksen jakamista divisioonan mukaan.
-   Yritys jakaa suuren projektin kustannukset ulkoisen organisaation kanssa.
-   Kaksi kuntaa rahoittaa yhdessä tieprojektia.
-   Siltaprojekti rahoitetaan julkishallinnolla ja yksityiseltä yritykseltä saatavalla rahoituksella.

Voit jakaa Finance and Operationsissa yhden tapahtuman tai koko projektin laskutuksen useiden asiakkaiden, avustusten tai organisaatioiden kesken. 

Monen rahoittajan projekteissa kaikkia projektin lisärahoitukseen osallistuvia kutsutaan rahoituslähteiksi. Kun asiakas, organisaatio tai avustus on määritetty rahoituslähteeksi, se määrittää vähintään yhteen rahoitussääntöön. Säännöt sisältävät kriteerit, jotka määrittävät, miten kulut kohdistetaan projektin useita rahoituslähteitä. 

Koska varastoituja nimikkeitä, kuten ostoehdotusten ja ostotilausten nimikkeitä, ei voi jakaa, kustannussummaa ei voi jakaa useiden rahoituslähteiden kesken jakeluajankohtana. Rahoituslähteen arvo onkin 0 (nolla), kunnes varasto-otto on kirjattu. Kun varasto-otto on kirjattu, kustannussumma jaetaan projektin tilin jakosääntöjen mukaan.

Voit helpottaa laskutuksen jakamista useiden rahoituslähteiden kesken seuraavien ohjeiden avulla:

-   Määritä kaikki projektille kirjatut tapahtumat käyttämään samaa myyntivaluuttaa kuin projektisopimus.
-   Määritä rahoitusrajat, jotta rahoituslähdettä laskutetaan vain projektin osalta vain määritetty summa.
-   Määritä jokaiselle työntekijälle, luokalle, luokkaryhmälle ja tapahtumatyypille (tai kaikille tapahtumatyypeille) rahoitussäännöt ja rahoitusrajat.
-   Valitse valinnainen alkamis- ja päättymispäivä määrittämään jakso, jolloin kukin rahoitussääntö on voimassa.
-   Määritä prosenttiosuus, josta kukin rahoituslähde vastaa.
-   Määrittää, mikä rahoituslähde vastaa rahoituksen kohdistuslaskelmien aiheuttamista pyöristyseroista.
-   Määritä säännöt määrittämään, miten projektikustannukset laskutetaan ulkoisille asiakkaille ja veloitetaan sisäisille organisaatioille.
-   Kirjaa tapahtumat pidossa olevalle rahoitustilille, kunnes lisärahoitusta saadaan tai kunnes päätät vastata kustannuksista sisäisesti.

Tapahtumaan liitettävä veroryhmä määritetään etsimällä veroryhmän määritys projektista. Jos veroryhmän määritys ei ole tehty projektitasolla, sitä etsitään projektisopimuksesta.

### <a name="example-multiple-funding-sources-simple"></a>Esimerkki: Useita rahoituslähteitä (yksinkertainen)

Seuraavassa taulussa on skenaarioita rahoituksen kohdistuksen hallinnasta, kun rahoituslähteitä on useita. Nämä skenaariot perustuvat seuraaviin oletuksiin:

-   Prioriteettiasetukset huomioidaan varojen kohdistuksessa ennen rahoitussääntöehtojen käyttöä.
-   Rahoitussäännön kelpoisuusaikaa aika ei ole määritetty päivämääräalueella.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Skenaario</strong></td>
<td><strong>Rahoituslähde </strong></td>
<td><strong>Kohdistusprosentti </strong></td>
<td><strong>Kohdistusprioriteetti </strong></td>
</tr>
<tr class="even">
<td>Haluat kohdistaa kustannukset yhteen rahoituslähteeseen, kunnes sen varat on käytetty, sitten toiseen rahoituslähteeseen, kunnes sen varat on käytetty, ja lopuksi jäljellä olevat kustannukset kolmanteen rahoituslähteeseen.</td>
<td><ul>
<li>Rahoituslähde 1</li>
<li>Rahoituslähde 2</li>
<li>Rahoituslähde 3</li>
</ul></td>
<td><ul>
<li>100 %</li>
<li>100 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Haluat kohdistaa 75 prosenttia kustannuksista yhteen rahoituslähteeseen ja 25 prosenttia toiseen rahoituslähteeseen. Kun jommankumman rahoituslähteet varat on käytetty, haluat maksaa jäljellä olevat kustannukset kolmannesta rahoituslähteestä.</td>
<td><ul>
<li>Rahoituslähde 1</li>
<li>Rahoituslähde 2</li>
<li>Rahoituslähde 3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Haluat kohdistaa 75 prosenttia kustannuksista yhteen rahoituslähteeseen ja 25 prosenttia toiseen rahoituslähteeseen. Kun jommankumman rahoituslähteet varat on käytetty, haluat jakaa jäljellä olevat kustannukset kolmannen ja neljännen rahoituslähteen kesken.</td>
<td><ul>
<li>Rahoituslähde 1</li>
<li>Rahoituslähde 2</li>
<li>Rahoituslähde 3</li>
<li>Rahoituslähde 4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Haluat kohdistaa ensimmäiset 25 prosenttia kustannuksista yhteen rahoituslähteeseen ja loput toiseen rahoituslähteeseen.</td>
<td><ul>
<li>Rahoituslähde 1</li>
<li>Rahoituslähde 2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Esimerkki: Useita rahoituslähteitä (monitahoinen)

Sinulla on kolme rahoituslähdettä, joita haluat käyttää seuraavassa järjestyksessä:

1.  Käytä rahoituslähdettä 2 ja 3 yhtä paljon, kunnes rahoituslähde 2 on kulutettu.
2.  Jatka rahoituslähteen 3 käyttöä, kunnes se on kulutettu.
3.  Käytä rahoituslähdettä 1 sen jälkeen, kun rahoituslähde 3 on kulutettu.

Voit saavuttaa tämän tavoitteen toimimalla seuraavasti:

-   Määritä rahoituslähteille 2 ja 3 kummallekin rahoitusrajasumma.
-   Luo seuraavat rahoitussäännöt:
    -   Sääntö 1 (prioriteetti 1): kohdistaa 50 prosenttia tapahtumista rahoituslähteeseen 2 ja 50 prosenttia rahoituslähteeseen 3.
    -   Sääntö 2 (prioriteetti 2): kohdista 100 prosenttia tapahtumista rahoituslähteeseen 3.
    -   Sääntö 3 (prioriteetti 3): kohdista 100 prosenttia tapahtumista rahoituslähteeseen 1.

Nämä asetukset toimivat, koska tapahtumia verrataan sääntöihin ja rajoihin, joiden perustella määritetään, käytetäänkö niitä mitään tapahtumassa. Jos mitään tiettyä sääntöä tai rajaa ei käytetä tapahtumassa, käytetään kaikkien tapahtumien sääntöä. Kaikkien tapahtumien sääntö vastaa kaikkia tapahtumia. 

Jos tapahtumaa vastaava sääntö löytyy, kyseisessä säännössä kohdistettua prosenttia käytetään ensin. Tätä ennen kuitenkin tarkistetaan, koskeeko jokin määritetty raja löydettyä vastinetta. Jos soveltuva raja löytyy ja rahoituslähteen varat on kulutettu, rahoitusrajaan liitetty rahoitussääntö hylätään ja ohjelma tarkistaa seuraavan käytettävän säännön. 

Joissakin tapauksissa vain osa tapahtumasta voidaan kohdistaa säännön mukaisesti. Syynä voi olla esimerkiksi se, että raja saavutetaan tapahtumaa kohdistettaessa. Siinä tapauksessa säännön mukaan kohdistetaan vain tietty summa, kuten 50 prosenttia kuhunkin rahoituslähteeseen. Näin menetellään säännössä 1, joka käsiteltiin aiemmin tässä osassa. Loput kohdistetaan järjestyksessä seuraavan säännön mukaisesti. 

Seuraavassa taulussa tätä skenaariota käsitellään tarkemmin.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Kohdistus </strong></td>
<td><strong>Erittely</strong></td>
</tr>
<tr class="even">
<td>Rahoitussäännöt</td>
<td><ul>
<li>Sääntö 1 (prioriteetti 1): Kaikki tapahtumat. Rahoituslähteen 2 kohdistus 50 % ja rahoituslähteen 3 50 %.</li>
<li>Sääntö 2 (prioriteetti 2): Kaikki tapahtumat. Rahoituslähteen 3 kohdistus 100 %.</li>
<li>Sääntö 3 (prioriteetti 2): Kaikki tapahtumat. Rahoituslähteen 1 kohdistus 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rahoitusrajat</td>
<td><ul>
<li>Rahoituslähteen 1 raja = 10 000,00</li>
<li>Rahoituslähteen 2 raja = 500,00</li>
<li>Rahoituslähteen 3 raja = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Tapahtuma 1</td>
<td><strong>Tapahtuman summa:</strong> 100,00<strong> Rahoitus:</strong> Tapahtuma maksetaan vain säännön 1 mukaisesti, koska tapahtuma on maksettu kokonaan, kun sääntöä 1 on käytetty. Tapahtuma rahoitetaan tason rahoituslähteen 2 ja 3 kesken.
<ul>
<li>Rahoituslähde 2: 50,00</li>
<li>Rahoituslähde 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tapahtuma 2</td>
<td><strong>Tapahtuman summa:</strong> 5 000,00<strong>Rahoitus:</strong> Tapahtuma maksetaan kolmen säännön mukaisesti. <strong>Sääntö 1</strong>
<ul>
<li>Rahoituslähde 2: 450,00</li>
<li>Rahoituslähde 3: 450,00</li>
</ul>
<strong>Sääntö 2</strong>
<ul>
<li>Rahoituslähde 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Sääntö 3</strong>
<ul>
<li>Rahoituslähde 1: 3 850,00 (= 5 000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Rahoitus yhteensä, joka jaetaan kullekin rahoituslähteelle</td>
<td><ul>
<li>Rahoituslähde 1: 3 850,00</li>
<li>Rahoituslähde 2: 500,00</li>
<li>Rahoituslähde 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Laskutussäännöt
Kun neuvottelet projektisopimuksen asiakkaan kanssa, voit määrittää, miten ja milloin voit laskuttaa asiakkaalta projektin työn. Voit määrittää projektisopimukseen ja projektin määrittämisen jälkeen projektin laskutussäännöt. Tarjoussäännöt on määritetty projektisopimukseen perustuvissa projektiehdoissa. Luotavat laskutussäännöt määräytyvät projektisopimuksen ehtojen ja projektityypin, kuten Aika ja materiaali tai Kiinteä hinta, mukaan. Voit luoda yhteen projektisopimukseen useita laskutussääntöjä. Voit määrittää laskutussäännön useita projekteja varten, jotka liittyvät samaan projektisopimukseen ja joilla on samanlaiset laskutusehdot. 

Voit määrittää seuraavat laskutussääntöjen tyypit:

-   **Toimitusyksikkö** – Laskuta asiakasta, kun toimitusyksikkö on valmis. Määrität sopimuksen toimitusyksiköt.
-   **Edistyminen** – Laskuta asiakasta, kun projektista on valmiina tietty prosenttiosuus. Voit määrittää laskutuksen säännön automaattisesti laskemaan prosenttiosuus työn valmistumisesta, tai voit manuaalisesti laskea prosenttiosuuden työn valmistumisesta ja asiakkaalta laskutettavan summan.
-   **Välitavoite** – laskuta asiakasta projektin välitavoitteen koko summa, kun välitavoite saavutetaan.
-   **Maksu** – laskuta asiakasta palveluistasi sekä veloita häneltä hallinnointipalkkio, joka on tavallisesti prosenttiosuus palveluiden kustannuksesta.
-   **Aika ja materiaali** – laskuta asiakasta projektissa käytetyistä materiaaleista ja ajasta.

Voit määrittää kaikentyyppisten laskutussääntöjen kohdalla myyntilaskuista vähennettävän pidätysprosentin, kunnes projekti saavuttaa sovitun vaiheen. Maksun pidätysprosentti määritetään projektisopimuksessa. Summa lasketaan ja vähennetään myyntilaskun rivien kokonaissummasta. 

Voit määrittää **Aika ja materiaali**- ja **Edistyminen** -laskutussäännöille laskutettavia luokkia. Laskutettavat luokat osoittavat tapahtumat, jotka pitää sisällyttää myyntilaskuihin. 

Kun olet valmis laskuttamaan asiakasta, projektin laskutettava summa lasketaan laskutuksen säännöillä ja projektin laskuehdotus luodaan. 

Seuraavissa osassa on esimerkkejä laskutussääntöjen määrittämisestä projektille ja niiden hallinnasta.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Esimerkki: Luo toimitettujen yksiköiden määrään perustuva laskutussääntö

Organisaatio solmii sopimuksen yhteensä viiden koulutusistunnon toimittamisesta asiakkaan työntekijöille. Kunkin koulutusistunnon hinta on 10 000. Laskutat asiakasta jokaisen koulutusistunnon jälkeen. 

Käytät sopimuksen laskutussääntöjen määrittämiseen seuraavia arvoja:

-   Toimitusyksikkö on yksi koulutustilaisuus.
-   Yksikköhinta on 10 000 koulutustilaisuutta kohti.
-   Yksiköiden kokonaismäärä on viisi koulutustapahtumaa.

Kun yksi koulutusistunto on suoritettu, voit luoda laskun ensimmäisen yksikön toimituksesta summalle 10 000 ja lähettää laskun asiakkaalle.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Esimerkki: Luo projektin valmistumisasteeseen perustuva laskutussääntö (lasketaan manuaalisesti)

Organisaatiosi, joka on erikoistunut ohjelmistokonsultointiin, sitoutuu kehittämään asiakkaalle osan tuotteesta, jota asiakas kehittää. Organisaatiosi sitoutuu toimittamaan tuotteelle ohjelmistokoodia kuuden kuukauden ajan. Asiakas suostuu maksamaan organisaatiollesi työstä yhteensä 100 000. Luot laskutussäännön, jolla asiakasta laskutetaan projektissa suoritetun prosenttimääräisen työn perusteella. Prosenttiosuus on määritetty sopimuksessa.

-   Ensimmäisen kuukauden lopussa tapaat asiakkaan ja määrität valmiin työn osuuden. Kun olette tarkastaneet projektin yhdessä asiakkaan kanssa, päätätte, että projekti on 15-prosenttisesti valmis.
-   Luot laskun summalle 15 000 (15 prosenttia summasta 100 000) ja lähetät sen asiakkaalle.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Esimerkki: Luo projektin valmistumisasteeseen perustuva laskutussääntö (lasketaan automaattisesti)

Organisaatiosi on ohjelmistokehitysyritys, joka sopii kehittävänsä asiakkaalle palkanlaskennan kirjanpitopaketin hintaan 30 000. Asiakas sitoutuu maksamaan organisaatiollesi työn valmistumisprosentin mukaisesti. Arvioit, että projektikustannukset ovat 20 000. Projektisopimus määrittää työluokat laskutusprosessia varten. Määrität laskutussäännöt, jotka laskevat automaattisesti laskujen summat kunkin luokan töiden valmistumisprosentin mukaan. Asetat budjetin jokaiselle luokalle:

-   **Kehitys** – kustannus 15 000 ja tuotto 20 000
-   **Asennus** – kustannus 5 000 ja tuotto 10 000

Kun myyntilasku luodaan ensimmäisen kerran, laskutussumma lasketaan automaattisesti perusteella seuraavat tiedot:

-   Työntekijä lähettää projektiin aikaraportin kuukauden kuluttua. Työntekijän tuntikustannukset ovat 5 000 kehitykselle ja 1 000 asennukselle. Kehitystyöstä on suoritettu 33 prosenttia (toteutunut kustannus 5 000 / budjetoitu kustannus 15 000) ja asennustyöstä on suoritettu 20 prosenttia (toteutunut kustannus 1 000 / budjetoitu kustannus 5 000).
-   Laskun summa 8 667 lasketaan automaattisesti (33 prosenttia 20 000:sta + 20 prosenttia 10 000:sta).
-   Luot laskun summalle 8 667 ja lähetät sen asiakkaalle.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Esimerkki: Luo laskutussääntö sovittujen välitavoitteiden perusteella

Organisaatio on johdon konsultointiyritys, joka on sopinut suorittavansa markkinointitutkimuksen kuluttajatuotteelle, jota asiakas suunnittelee myyvänsä. Asiakas sitoutuu käyttämään palveluitasi kolmen kuukauden ajan maaliskuusta alkaen ja sitoutuu maksamaan organisaatiollesi 50 000. Projektissa on kolme välitavoitetta:

-   Välitavoite 1: Kerää kuluttajatiedot – 31. maaliskuuta
-   Välitavoite 2: Analysoi kuluttajatiedot – 30. huhtikuuta
-   Välitavoite 3: esitä ehdotus tuotteen kannattavuudesta – 31. toukokuuta

Asiakas sopii maksavansa organisaatiolle 10 000 ensimmäisestä välitavoitteesta, 20 000 toisesta välitavoitteesta ja 20 000 kolmannesta välitavoitteesta. 

Projektisopimusta määritettäessä sovit laskuttavasi asiakasta valmistuneen välitavoitteen perusteella. Laskutussääntöasetukset sisältävät seuraavat vaiheet:

-   Määritä projektin välitavoitteet.
-   Määritä summa, joka asiakkaalta laskutetaan, kun kukin välitavoite valmistuu.

Kun ensimmäinen välitavoite valmistuu 31. maaliskuuta, merkitset välitavoitteen valmiiksi ja luot sitten laskun summalle 10 000. Lasku lähetetään asiakkaalle. Et voi luoda laskua välitavoitteelle, ennen kuin välitavoite on merkitty valmiiksi.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Esimerkki: Luo palveluihin ja hallintokuluun perustuva laskutussääntö

Organisaatio on johdon konsultointiyritys, joka on sopinut suorittavansa markkinointitutkimuksen arvioidakseen asiakkaan, vähittäismyyntiyrityksen, kehittämän tuotteen kannattavuuden. Sopimuksen ehdoissa määritetään, että käytettävissä on yrityksen kolmen parhaan johdon konsultin palvelut ja että käytössä on veloitus käytetyn ajan ja materiaalin perusteella. Asiakas sopii maksuksi 100/tunti ja 10 prosentin hallintakulun projektiin käytettyjen konsultointituntien osalta. 

Luo projektisopimusta määritettäessä laskutussääntö, joka lisää 10 prosentin hallintokulun projektissa käytettyihin konsultointitunteihin. 

Kun luot laskun asiakkaalle, asiakkaalta laskutetaan 10 prosentin hallintokulu ja konsultointituntien hinta. Jos esimerkiksi kolme konsulttia työskenteli projektissa yhteensä 200 tuntia, lasku luodaan summalle 22 000 seuraavan laskelman perusteella:

-   200 tuntia 100 tunnissa = 20,000
-   10 prosentin hallintamaksu = 2 000
-   Laskun kokonaissumma = 22.000

Jos maksut ovat verotettavia asiakkaalle ja arvonlisäveroryhmä valitaan projektisopimukseen, arvonlisäveroryhmä syötetään automaattisesti laskutuksen säännön maksuille.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Esimerkki: Luo laskutussääntö ajan ja materiaalien arvolle

Organisaatiosi on ohjelmointialan konsulttiyritys, joka sopii toimittavansa viisi teknistä konsulttia työskentelemään asiakkaan ohjelmistokehitysprojektissa seuraavan kuuden kuukauden ajan. Asiakas sopii maksavansa 150/konsultointitunnista ja toimistotarvikekulut. Organisaatiosi lähettää laskun asiakkaalle jokaisen kuukauden lopussa. 

Projektisopimusta määritettäessä sovit laskuttavasi asiakasta joka kuukausi projektiin käytetyn ajan ja materiaalin perusteella. Luot laskutussäännön, joka sisältää seuraavat tiedot:

-   Sopimuskausi on kuusi kuukautta.
-   Konsultointiaika lasketaan hinnalla 150/tunti.
-   Toimistotarvikkeet laskutetaan kustannuksen perusteella, eikä projektin kokonaiskustannus voi olla suurempi kuin 10 000.
-   Luot myyntilaskun projektin aikana kunkin kalenterikuukauden lopussa.

Konsultit kirjaavat projektiin ensimmäisen kuukauden aikana yhteensä 800 tuntia. Projektin veloitettujen toimistotarvikkeiden kustannus on 2 000. Niinpä kuukauden lopussa luodaan arvo, jonka arvo on 122 000 (800 tuntia x 150/tunti + 2 000 toimistotarvikkeisiin).



