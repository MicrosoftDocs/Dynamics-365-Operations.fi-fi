---
title: Projektin resursointi
description: "Tässä aiheessa on tietoja projektien resursoinnista."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 2d31a5dfd16a4404e19c6c9693dacecff6f2f064
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="project-resourcing"></a>Projektin resursointi

[!include [banner](../includes/banner.md)]

Tässä aiheessa on tietoja projektien resursoinnista.

Yksi projekti- ja resurssipäälliköiden haasteista projektin suunnitteluvaiheessa on resurssien kohdistaminen. Tällöin on määritettävä ja varattava oikea resurssi projektityöhön. Microsoft Dynamics 365 for Finance and Operations -sovelluksessa voi projektien resursointitoiminnoilla määrittää roolit, joita käsitellään väliaikaisina resursseina, joita voidaan varata tiettyyn sitoumukseen tai sitoumuksen osaksi. Tämäntyyppisen resursoinnin avulla projekti- ja resurssipäälliköt voivat suorittaa seuraavia tehtäviä:

- Määrittää roolin, jolla on resurssien kohdistamista helpottavat tarvittavat osaamisalueet.
- Määrittää roolien avulla varattuihin resursseihin perustuvan alustavan sitoumusaikataulun.
- Arvioida kustannuksia ja määrittää alustavan budjetin projektiin liitettyjen roolien ja resurssien perusteella.
- Arvioida roolien avulla kuhunkin sitoumukseen tarvittavien resurssivarausten määrän.
- Arvioida projektin koko elinkaaren ajaksi tarvittavien resurssien määrän.
- Laatia työrakenteen käyttämällä alustavia resurssimäärityksiä.

[![Projektin elinkaari](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Projektisuunnittelun edetessä suunnitellut resurssit voidaan korvata henkilöstöllisillä resursseilla. Projektipäällikkö voi myös palata päivittämään resursointivaraukset missä tahansa projektin vaiheessa.

## <a name="set-up-project-resources"></a>Projektiresurssien määrittäminen
Sinun täytyy määrittää kalenteri ja liittää se työntekijään. Kalenterin avulla aikataulutetaan projekti ja siihen varattujen resurssien työaika. Kalenteria määrittäessään projektipäälliköt voivat suorittaa resurssien tasaamisen resurssien optimoinnin yhteydessä. Kalenterin aikataulun perusteella resursseille voidaan asettaa rajoituksia. Voit määrittää kalenterin **Kalenterit**-sivulla.

Työntekijän projektin resurssiksi määrittäessäsi voit valita sen yrityksen työntekijät, jolle resursseja määritetään. Voit vaihtoehtoisesti valita työntekijät muista organisaation yrityksistä. Nämä työntekijät ovat konsernin sisäisiä resursseja.

Seuraavissa ohjeissa selitetään, miten työntekijä määritetään yrityksen projektiin resurssiksi ja miten konsernin sisäinen projektin resurssi määritetään.

### <a name="set-up-a-worker-as-a-project-resource"></a>Työntekijän määrittäminen projektiresurssiksi

1. Valitse **Työntekijät**-sivun **Työntekijät**-luettelosta työntekijä, jonka haluat lisätä projektiin resurssiksi, ja avaa haluamasi työntekijätietue.
2. Valitse toimintoruudussa **Projekti** &gt; **Asetukset** &gt; **Projektiasetukset**.
3. Valitse kalenteri ja sulje sivu.

Voit myös määrittää resurssille oletusprojektit eräänlaisena esimäärityksenä. Esimäärityksiä voidaan käyttää, kun resurssi- tai projektipäällikkö tietää jo etukäteen, missä projekteissa resurssi työskentelee. Esimääritykset voivat perustua myös projektin sponsorin tai asiakkaan pyyntöön. Jos haluat esimäärittää projektin, valitse **Määritä projektit** -sivulta **Projektit**-välilehdestä **Jäljellä olevat projektit** -luettelosta haluamasi projekti.

### <a name="set-up-an-intercompany-resource"></a>Konsernin sisäisen resurssin määrittäminen

Kun määrität työntekijää konsernin sisäiseksi resurssiksi, määritä tiedot yrityksestä, joka antaa resurssin lainaksi ja yrityksestä, joka ottaa resurssin lainaksi.

**Yritys, joka antaa resurssin lainaksi**

1. Varmista Finance and Operationsissa, että resurssin lainaava yritys on valittu. Tee sitten toimenpiteet, jotka on mainittu edellä olevassa kohdassa Työntekijän määrittäminen projektiresurssiksi.
2. Valitse **Konsernin sisäinen kirjanpito** -sivulla **Uusi**.
3. **Yrityksen tunnus** -kenttään yritys, jolta resurssi lainataan. Anna tarvittavat tiedot muihin kenttiin ja valitse sitten **Tallenna**.
4. Valitse **Siirtohinta** -sivulla **Uusi**.
5. **Lainaava yritys** -kenttään asianmukainen yritys.
6. Jos haluat lainata lainaavalle yritykselle vain resurssin, jonka loit tämän osan alussa, valitse **Resurssi**-kentässä luomasi resurssin nimi. Jos haluat, että kaikki lainan antavan yrityksen resurssit ovat lainaavan yrityksen käytettävissä, jätä **Resurssi**-kenttä tyhjäksi.
7. Määritä **Projektinhallinnan ja kirjanpidon parametrit** -sivun **Konsernin sisäinen** -välilehden **Ota käyttöön konsernin sisäinen resurssien ajoitus ja aikaraportit** -asetuksen arvoksi **Kyllä**.

**Yritys, joka lainaa resurssin**

- Syötä **Resurssiluettelo**-sivun hakusuodattimeen sille yritykselle luomasi resurssin nimi, jolta resurssi lainataan. Varmista, että nimi löytyy sen yrityksen resurssiluettelosta, jolle resurssi lainataan.

## <a name="manage-resource-competencies"></a>Resurssin osaamisalueiden hallinta
Resurssin osaamistietojen määritys on olennainen osa resurssien hallintaa. Osaamisalueita voi käyttää perustasona määriteltäessä resursseja, joilla on oikeanlaiset taidot, koulutus, todistukset ja projektikokemus. Nämä tiedot on määritettävä joka resurssille ja päivitettävä säännöllisesti. Näin voit maksimoida osaamisen, kun tiettyjä resurssien osaamisalueita yhdistellään projektin resurssimäärityksen yhteydessä.

[![Esimerkkejä osaamisalueista, todistuksista, koulutuksesta ja projektikokemuksesta](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Seuraavissa ohjeissa selitetään, miten voi määrittää joitakin resurssin osaamisalueista.

Voit määrittää työntekijän osaamisalueet joko Henkilöstöhallinto-osassa **Työntekijät**-luettelossa tai Projektinhallinta ja kirjanpito -osassa **Resurssit**-sivulla. Seuraavissa vaiheissa käytetään Henkilöstöhallinto-osan **Työntekijät**-luetteloa.

### <a name="set-up-competencies-certificates"></a>Osaamisalueiden määrittäminen: todistukset

1. Valitse **Työntekijät**-luettelosivulta sen työntekijän rivi, jonka todistustiedot haluat lisätä.
2. Valitse toimintoruudun **Työntekijä**-välilehdessä **Osaamistiedot**-ryhmässä **Todistukset**.
3. Valitse **Uusi** ja sitten **Todistuksen tyyppi** -kenttään **PMP**.
4. Anna **Aloituspäivä** -kenttään **10/1/2015** ja valitse **Tallenna**.

### <a name="set-up-competencies-skills"></a>Osaamisalueiden määrittäminen: osaamisalueet

1. Varmista **Työntekijät**-luettelosivulla, että aiemmassa vaiheessa valitsemasi työntekijä on yhä valittuna. Valitse sitten toimintoruudun **Työntekijä**-välilehdessä **Osaamistiedot**-ryhmässä **Osaamisalueet**.
2. Valitse **Uusi**.
3. Valitse **Osaamisalue**-kentästä **Projektinhallinta**.
4. Valitse **Taso**-kentästä **Asiantuntija**.
5. Valitse **Tasopäivämäärä**-kentästä **1-/14/2014**.
6. Kirjoita **Kokemus vuosina** -kenttään arvoksi **10**.
7. Valitse **Tallenna** ja sulje sitten sivu.

## <a name="create-a-new-project"></a>Luo uusi projekti
1. Valitse **Projektin hallinta** -sivulla **Uusi projekti** ja anna seuraavat arvot:

    - **Projektityyppi:** Aika ja materiaali
    - **Projektin nimi:** XYZ-päivitysvaihe 2
    - **Projektiryhmä**: TM\_WIP
    - **Projektisopimuksen tunnus:** 00000002

2. Valitse **Luo projekti**.

### <a name="assign-a-resource-to-a-project"></a>Resurssin määrittäminen projektiin

1. Valitse **Työntekijät**-sivun **Työntekijät**-luettelosta sen työntekijän tietue, jonka osaamisalueet määritit aiemmassa vaiheessa, ja avaa tietue.
2. Valitse toimintoruudussa **Projekti**-välilehden **Asetukset**-ryhmästä **Määritä projektit**.
3. Suodata **Resurssin oikeellisuustarkistuksen projektimääritykset** -sivun **Projektit**-välilehden **Lisää projekti valittuihin projekteihin** -kentässä **XYZ-päivitysvaihe 2** -projektiin.
4. Valitse **Jäljellä olevat projektit** -ruudusta haluamasi projekti ja lisää se **Valitut projektit** -ruutuun napsauttamalla nuolta.

Tarvittaessa voit myös määrittää resurssille luokkia. Luokkatyyppi on joko **Kustannus** tai **Tuotto**. Luokkatyyppi määräytyy organisaation mukaan. Jos resurssille ei ole määritetty luokkia, Finance and Operations etsii oletusluokan kustannusten ja tuoton tuntihinnoista.

### <a name="set-up-project-resource-and-role-characteristics"></a>Projektin resurssin ja rooliominaisuuksien määrittäminen

Projektipäällikkö voi projektin resursointitoiminnolla luoda projektissa tarvittavia rooleja. Rooleja voidaan käyttää, kun vahvistetut resurssit eivät ole vielä tiedossa resurssien varaamisen aikana. Rooleja voidaan väliaikaisesti varata suunnitelluiksi resursseiksi, jotta voit jatkaa projektin suunnitteluvaiheita.

[![Esimerkki roolista](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Skenaario:** Contoso palkattiin suorittamaan aika- ja materiaaliprojekti, jolla on hyväksytty projektin perustamisasiakirja. Nuorempi projektipäällikkö on yhä laatimassa projektin laajuutta. Resurssipäällikkö on parhaillaan määrittämässä resursseja, jotka varataan uuteen projektiin. Koska projekti on erityisen tärkeä, projektin sponsori on toivonut yhden rooleista olevan vastaava projektipäällikkö. Resurssipäällikön on hankittava uusi resurssi, ja hän määrittää roolin järjestelmään siltä varalta, että nuorempi projektipäällikkö tarvitsee resurssitiedot projektin suunnittelua varten.

Seuraavissa vaiheissa on esitetty, miten resurssipäällikkö voi määrittää vastaavan projektipäällikön roolin ja liittää siihen resurssin ominaisuudet. Myöhemmin roolin avulla voidaan hakea käytettävissä olevia resursseja, jotka vastaavat tarvittavia resurssin osaamisalueita.

1. Valitse **Määritä roolit** -sivulla **Uusi** ja anna seuraavat arvot:

    - **Roolin tunnus:** Vastaava projektipäällikkö
    - **Kuvaus:** Vastaava projektipäällikkö

2. Valitse **Luo**.
3. Valitse **Vastaava projektipäällikkö** -rooli ja sitten **Määritä ominaisuudet**.
4. Valitse **Ominaisuuden tyyppi** -kentästä **Osaamisalue**.
5. Syötä **Käytettävissä olevat ominaisuudet** -kenttään haettava osaamisalue.
6. Valitse **Ominaisuustyyppi**-kentästä **Todistus**.
7. Syötä **Käytettävissä olevat ominaisuudet** -kenttään haettava todistustyyppi.

### <a name="assign-a-project-resource-to-a-project"></a>Projektiresurssin määrittäminen projektiin

1. Valitse **Kaikki projektit** -sivulla **XYZ-päivitysvaihe 2** -projekti.
2. Valitse **Projektiryhmä ja ajoitus** -välilehdestä **Lisää**.
3. Valitse **Rooli**-kentästä **Ryhmän jäsen**.
4. Valitse **Varaa kalenterista**.
5. Valitse **Resurssin saatavuus** -sivulta **Näyttöasetukset**.
6. Syötä **Muuta näyttöasetuksia** -sivulle seuraavat arvot:

    - **Päivämääräalueen muoto:** Päivä
    - **Näytä saatavuuskuvaukset:** Kyllä
    - **Näytä jäljellä oleva kapasiteetti:** Kyllä

7. Valitse resurssiluettelosta haluamasi resurssi.
8. Valitse **Kiinteä varaus** ja **Koko kapasiteetti**.


### <a name="assign-a-resource-to-a-default-role"></a>Resurssin määrittäminen oletusrooliin

Voit auttaa projekti- tai resurssipäälliköitä porautumalla alemmas resursseihin, jotka voidaan varata projektiin. Voit liittää oletusroolin aiemmin luotuun tai vasta hankittuun resurssiin. Esimerkiksi kun Daniel palkattiin, hänellä oli yritysanalyytikon rooliin tarvittava kokemus ja osaamisalueet. Resurssipäällikkö määritti tämän roolin Danielin oletusrooliksi. Resurssipäällikkö lisäsi Danielin toisin sanoen niiden yritysanalyytikkojen pooliin, jotka ovat käytettävissä projekteissa.

Resurssin varaamisen yhteydessä projektipäälliköt voivat suodattaa roolin resurssit, jotka ovat käytettävissä projektitöihin. Päälliköt voivat käyttää näitä tietoja yhtenä ehtona analysoidessaan päätöksiä useiden ehtojen perusteella resurssien täyttämisen yhteydessä. He voivat lisätä suodattimeen muitakin resurssin ominaisuuksia ja hakea niiden avulla resursseja, joilla on projektissa tarvittavat osaamisalueet, koulutus ja kokemus.

**Skenaario:** Hyväksytty projekti on alkanut, ja vastaavan projektipäällikön rooli on varattu suunniteltuna resurssina projektin suunnitteluvaiheessa. Resurssipäällikön on nyt hankittava rooliin sopiva resurssi.

1. Valitse **Resurssiluettelo**-sivulta **Daniel Goldschmidt**.
2. Valitse **Resurssin rooli** -sivulla **Uusi** ja anna seuraavat arvot:

    - **Voimassa:** Anna nykyinen päivämäärä.
    - **Päättyminen:** anna arvoksi **Ei koskaan**.
    - **Rooli:** anna arvoksi **Vastaava projektipäällikkö**.

3. Valitse **Tallenna** ja sulje sitten sivu.
4. Lisää **Osaamistiedot**-välilehdessä **ProjectMgmt**-osaamisalue ja **PMP**-todistus.

## <a name="set-up-role-based-pricing"></a>Roolipohjaisen hinnoittelun määrittäminen
Rooleille voidaan määrittää kaikki kustannukset sekä myynti- ja siirtohinnat.

1. Valitse **Myyntihinta (tunti)** -sivulta **Uusi** ja anna voimaantulopäivä.
2. Valitse **Rooli**-sarakkeesta haluamasi rooli.
3. Syötä **Hinnoittelu**-sarakkeeseen hinta valitulle resurssiroolille.

## <a name="form-a-project-team"></a>Projektiryhmän muodostaminen
Projektipäällikön täytyy liittää projektin yhteydessä aiemmin määritetyt roolit projektiin, jotta hän voi käyttää niitä. Projektille voidaan määrittää useita rooleja. Sekaannuksen estämiseksi Finance and Operations nimeää roolit automaattisesti varauksen aikana. Jos projektipäällikkö tarvitsee esimerkiksi kolme ohjelmistosuunnittelijaa, luodaan automaattisesti kolme ohjelmistosuunnittelijan roolia, joiden nimikkeinä on **ohjelmistosuunnittelija 1**, **ohjelmistosuunnittelija 2** ja **ohjelmistosuunnittelija 3**. Jos roolille on määritetty ominaisuudet jo aiemmin, niitä käytetään suodattimina resurssia haettaessa. Hakua voi tarkentaa lisäämällä muitakin ominaisuuksia tarpeen mukaan.

Myös näyttöasetukset voidaan mukauttaa, jotta resurssien käytettävyys saadaan paremmin näkyviin. Näyttöperusteeksi voi valita käytettävyyden tunnin, päivän, viikon, kuukauden, vuosineljänneksen tai vuoden perusteella. Myös resurssien käytettävissä ja jäljellä olevan kapasiteetin voi suodattaa näkyviin. Tämä vaihtoehto on hyödyllinen ajanhallinnassa, kun arvioit tehtäviin käytettävissä olevaa aikaa tai resurssien käytettävyyttä.

Projektipäällikkö voi valita sivulta haluamansa roolin. Jos vaatimuksia vastaava resurssi on käytettävissä, projektipäällikkö voi valintansa mukaan varata resurssin rooliin. Huomaa, että resursseja ei tarvitse varata tässä suunnitteluvaiheessa. Työrakennetta luodessasi voit korvata roolit projektin henkilöstöllisillä resursseilla. Jos roolit korvataan työrakenteessa henkilöstöllisillä resursseilla, resurssiasetukset päivittävät projektiryhmän luettelon ja aikataulun automaattisesti.

[![Projektiryhmän luettelo, joka sisältää sekä roolit todellinen resurssit](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektipäällikkö voi varata resurssin projektiin eri tavoilla, esimerkiksi valitsemalla **Jäljellä oleva kapasiteetti**, **Koko kapasiteetti**, **Kapasiteettiprosentti** ja **Määritä tunnit**. Nämä varausasetukset voi peruuttaa milloin tahansa, jos resurssimääritykset muuttuvat. Kahta varaustyyppiä tuetaan:

- **Kiinteä varaus** – Resurssivaraus on hyväksytty ja resurssin työskentely sitoumuksessa on vahvistettu tietyksi ajaksi.
- **Alustava varaus** – Resurssivaraus on alustavasti määritetty työskentelemään sitoumuksessa tietyllä ajalla.

Seuraavissa vaiheissa on selostettu, miten projektiryhmä luodaan.

### <a name="create-a-project-team"></a>Projektiryhmän luominen

1. Valitse **Kaikki projektit** -luettelosivulta haluamasi projekti ja valitse sitten **Muokkaa**.
2. Syötä **Projektiryhmän ja ajoitus** -välilehdessä **Ajoita päättymispäivä** -kenttään aikataulun alkamispäivä plus yksi kuukausi. Jos aikataulun alkamispäivä on esimerkiksi 24. kesäkuuta 2017 (24/06/2017), syötä **24/07/2017**.
3. Valitse **Lisää**.
4. Valitse **Lisää roolit projektiin** -ruudun **Rooli**-kentästä **Vastaava projektipäällikkö**.
5. Valitse **Vaaditut osaamisalueet**.
6. Aiemmin vastaavan projektipäällikön roolille määrittämäsi ominaisuudet tulevat oletusarvoisesti valituiksi **Valitse ominaisuudet** -sivulla. Valitse **OK**.
7. Syötä **Lisää roolit projektiin** -sivulla **Resurssien määrä** -kenttään arvoksi **1**.
8. Hakutoiminto näyttää **Resurssi**-kentässä kaikki resurssit, joilla on tarvittavat osaamistiedot. Valitse **Daniel Goldschmidt** ja sitten **Luo**.
9. Valitse **Projekti**-sivulla **Lisää**.
10. Valitse **Lisää roolit projektiin** -ruudun **Rooli**-kentästä **Ryhmän jäsen**. Syötä **Resurssien määrä** -kenttään arvoksi **5**.
11. Valitse **Luo**.
12. Valitse **Projektit**-sivulla **Toteuta resurssi**.

## <a name="resource-capacity-synchronization"></a>Resurssin kapasiteetin synkronointi
Resurssin synkronointiprosessi auttaa varmistamaan, että kalenterin ja peruskalenterin tiedot siirtyvät projektiresurssien ajoitukseen. Jos kalenteria muutetaan, prosessit tekevät projektiresurssien ajoitukseen tarvittavat päivitykset. Prosessit parantavat myös suorituskykyä, koska resurssin kalenteritiedot synkronoidaan etukäteen. Näin päivitykset resurssien ajoitustietoihin tapahtuvat entistä nopeammin. Prosessit kannattaa ajoittaa eräajona, ei yksitellen. Muussa tapauksessa riskinä on, että edelliseen synkronointiin sisällytettävät päivämäärät unohtuvat. Jos sisällytettäviä päivämääriä ei käytetä, päivämäärien synkronointiin voi jäädä aukkoja.

![Kalenterin synkronointi](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Synkronoi resurssin kapasiteetin koonnit

Synkronointiprosessin tarkoituksena on synkronoida kaikki resurssin kalenteritiedot. Näihin tietoihin sisältyvät peruskalenterin tiedot kaikista muutoksista, jotka tehdään projektin resurssikalenterin kapasiteettitaulukkoon. Jos projektiin lisätään uusia resursseja, synkronoinnin avulla voidaan varmistaa, että päivitetyt kalenteritiedot ovat käytettävissä. Synkronoinnin voi tehdä milloin tahansa.

Ne kannattaa tehdä eräajona. Vaihtoehdot ovat käytettävissä kapasiteettivarauksia synkronoitaessa.

1. Valitse **Projektinhallinta ja kirjanpito** &gt; **Kausittainen** &gt; **Kapasiteetin synkronointi** &gt; **Synkronoi resurssin kapasiteetin koonnit**.
2. Määritä asetukset seuraavassa taulukossa.

    | Vaihtoehto      | kuvaus |
    |-------------|-------------|
    | Kausikoodi | Voit myös valita pääkirjanpidon päivämäärävälin koodin, jolla asetetaan resurssin kapasiteetin koontien synkronointiprosessin aloitus- ja lopetuspäivämäärät. |
    | Aloituspäivämäärä  | Anna resurssin kapasiteetin koontien synkronointiprosessin aloituspäivä. |
    | Päättymispäivämäärä    | Anna resurssin kapasiteetin koontien synkronointiprosessin päättymispäivä. |

[![Synkronointiprosessi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Roolien määrittäminen työrakennemalleille
Projektipäälliköt voivat määrittää työrakennemalleja ja käyttää niitä luodessaan uusille projekteille työrakennetta. Projektipäälliköt voivat lisätä rooleja malleja luodessaan. Voit määrittää roolin työrakennemalliin seuraavasti. 

1. Valitse **Projektinhallinta ja kirjanpito** &gt; **Asetukset** &gt; **Projektit** &gt; **Työrakennemallit**.
2. Valitse valitun työrakennemallin **Tiedot**-kohta.
3. Valitse luettelosta haluamasi tehtävä ja valitse sitten **Rooli**-kentästä tehtävään määritettävä rooli.

### <a name="work-with-a-wbs"></a>Työrakenteen käsitteleminen

Voit luoda uuden työrakenteen tai kopioida sen aiemmin luodusta työrakennemallista. Projektipäällikkö voi hallita resursseja helposti määrittämällä työrakenteessa roolit uusille tehtäville. Roolit voidaan korvata, kun resurssi on hankittu tai kun vahvistettu resurssi tehtävään on määritetty. Näin projektipäälliköt voivat suorittaa joustavasti seuraavat tehtävät:

- Määrittää työrakenteen työpaketteihin tarvittavan resurssien määrän.
- Arvioida projektikustannukset.
- Määritellä alustavan budjetin.
- Arvioida tehtävän kestoa roolien ja resurssien perusteella.
- Kehittää joitakin projektinhallintasuunnitelmia käytettävissä olevien projektitietojen pohjalta.

Työrakenteeseen on liitetty lisäasetuksia, jotka helpottavat resursointitoimintojen käyttöä.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vaihtoehto</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Resurssimääritykset</td>
<td>Tarkastele määritettyjä resursseja, päivämääriä, tuntimääriä ja tehtävien varaustyyppiä työrakenteessa.</td>
</tr>
<tr class="even">
<td>Luo ryhmä automaattisesti</td>
<td>Lisää suunnitellut resurssit automaattisesti käyttämällä tehtävään liitettyjä rooleja. Finance and Operations ehdottaa suunniteltuja resursseja automaattisesti käyttämällä rooleihin perustuvaa useiden ehtojen analyysia. Kun tehtäville on määritetty roolit ja työaika (tunnit) työrakenteessa ja rakenne on julkaistu, valitse <strong>Luo ryhmä automaattisesti</strong>. Tarvittava suunniteltujen resurssien määrä lisätään työrakenteeseen ja <strong>Projektiryhmä ja ajoitus</strong> -välilehteen.</td>
</tr>
<tr class="odd">
<td>Resurssi (avattava luettelo)</td>
<td><strong>Käynnistä resurssimääritys</strong> -sivulla voit valita resurssit kiinteää tai alustavaa varausta varten määritetyn keston perusteella. Voit muokata näyttöasetuksia niin, että saat näkyviin ja voit määrittää resurssitehtävien keston. Voit valita ja määrittää resursseja työpakettitasolla käyttämällä seuraavia vaihtoehtoja:
<ul>
<li><strong>Hyväksy</strong> – vahvistaa tehtävään liitettyyn resurssiin tehdyt muutokset.</li>
<li><strong>Peruuta</strong> – peruuttaa tehtävään liitettyyn resurssiin tehdyt muutokset.</li>
<li><strong>Määritä automaattisesti</strong> – Valitulle tehtävälle valitaan automaattisesti käytettävissä oleva henkilöstöllisen resurssi ja sitä vastaava rooli.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Valitse **Kaikki projektit** -sivulla **XYZ-päivitysvaihe 2** -projekti.
2. Valitse **Suunnitelma** &gt; **Tehtävät** &gt; **Työrakenne**.
3. Valitse **Uusi** ja lisää seuraavat ykköstason tehtävät työrakenteeseen:

    - Aloittaminen
    - Suunnittelu
    - Suoritetaan
    - Valvonta ja ohjaus
    - Sulje

4. Määritä päivämäärät ja työmäärä (tunteina) kuvassa esitetyllä tavalla.

    [![Päivämäärien ja työmäärän määrittäminen](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Valitse **Aloittaminen**-tehtävärivi ja valitse sitten **Rooli**-kentästä **Vastaava projektipäällikkö**.
6. Valitse **Julkaise**.
7. Valitse samalta riviltä **Resurssi**-kentästä **Daniel Goldschmidt** ja valitse sitten **Hyväksy**.
8. Valitsemalla **Suunnittelu**-tehtävärivi ja valitse sitten **Rooli**-kentästä **Yritysanalyytikko**.
9. Valitse **Julkaise** ja sitten **Luo ryhmä automaattisesti**.
10. Valitse näyttöön tulevassa viesti-ikkunassa **Kyllä**.
11. Tarkista, että **Resurssi**-kentässä arvona on **Yritysanalyytikko 1**.
12. Avaa hakutoiminto **Yritysanalyytikko 1** -resurssin kohdalla ja valitse **Käynnistä resurssimäärityksen lomake**. Valitse tehtävään työntekijä.
13. Valitse **Määritä alustavasti** &gt; **Koko kapasiteetti**.

    > [!NOTE] 
    > Näyttöön ei tule varoitusta siitä, että määritetyn resurssin arvo on nyt 2, koska resurssien määrä on edelleen 1.

14. Tarkista **Työrakenne**-sivulta työrakenteen resurssimääritys ja valitse sitten **Tallenna**.

## <a name="resource-fulfillment-for-planned-resources"></a>Resurssin toteuttaminen suunnitelluille resursseille
Projektipäällikkö voi suunnitella projektille tarvittavat resurssiroolit. Resurssipäällikkö näkee suunnitellut resurssit pyyntöinä **Resurssin toteuttaminen** -sivulla ja voi määrittää varsinaiset resurssit.

1. Valitse **Kaikki projektit** -sivulla **XYZ-päivitysvaihe 2** -projekti.
2. Valitse **Projekti** ja sitten **Muokkaa**.
3. Valitse **Projektiryhmä ja ajoitus** -välilehdestä **Lisää**.
4. Valitse **Lisää roolit** -valintaikkunassa **Ohjelmistokehittäjä**-rooli.
5. Valitse **Tallenna** ja sulje sitten projektisivu.
6. Valitse **Resurssin toteuttaminen** -sivulta **Ohjelmistokehittäjä 1** **XYZ-päivitysvaihe 2** -projektiin.
7. Valitse työntekijä ja sitten **Määritä**.
8. Tarkista, että **Ohjelmistokehittäjä 1** -rivi on poistettu **XYZ-päivitysvaihe 2** -projektista.
9. Tarkista **Projektiryhmä ja ajoitus** -välilehdessä, että edellisessä vaiheessa valitsemasi työntekijä on lisätty **XYZ-päivitysvaihe 2** -projektiin **ohjelmistokehittäjäksi**.

## <a name="requests-for-project-resources"></a>Projektiresurssien pyynnöt
Projektiresurssin ajoitustoiminto tukee vain resurssipäälliköitä, jotka jakavat henkilöllisiä resursseja sitoumuksiin tai projekteihin. Tämä toiminto otetaan käyttöön suorittamalla seuraavat tehtävät valmiiksi tai varmistamalla, että ne on suoritettu:

- Määritä numerosarjat.
- Määritä projektinhallinnan ja kirjanpidon työnkulut.
- Ota resurssipyynnön työnkulut käyttöön.

Kun edeltävät tehtävät on suoritettu, voit suorittaa seuraavat tehtävät tarvittaessa:

- Luo resurssipyyntö alustavasti varatusta henkilöllisestä resurssista.
- Seuraa resurssipyyntöjä.
- Täytä resurssipyynnöt.
- Pyydä henkilöllistä resurssia työrakenteesta.
- Varaa projektin resurssit ilman henkilöllisen resurssin pyyntöä.

## <a name="monitor-project-teams"></a>Projektiryhmien seuranta
1. Valitse **Kaikki projektit** -sivulla **XYZ-päivitysvaihe 2** -projektin **Projektitunnus**-linkki.
2. Tarkista **Projektiryhmä ja ajoitus** -pikavälilehdessä, että luettelossa näkyvät projektiresurssit ovat oikein.

