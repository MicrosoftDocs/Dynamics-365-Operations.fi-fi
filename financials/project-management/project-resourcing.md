---
title: Projektin resursointi
description: "Tämä ohjeaihe sisältää tietoja projektin rahoituksen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: c29c95fc6abd13e668c44d3ccf437bb0e879e46b
ms.lasthandoff: 03/31/2017


---

# <a name="project-resourcing"></a>Projektin resursointi

Tämä ohjeaihe sisältää tietoja projektin rahoituksen.

Projekti- ja henkilöstöpäälliköt projektin suunnitteluvaihe aikana yksi haaste on missä ne täytyy selvittää ja varata projektille oikean resurssin varauksiin. -Microsoft Dynamics 365 operaatioille ominaisuuksia projektien resourcing antavat sinun määrittää rooleja, joita käsitellään väliaikainen resursseja, jotka voidaan varata tietyn välitys tai sitoumuksen osaksi. Tämäntyyppisen resursoinnin avulla projekti- ja resurssipäälliköt voivat suorittaa seuraavia tehtäviä:

-   Määrittää roolin, jolla on resurssien kohdistamista helpottavat tarvittavat osaamisalueet.
-   Roolien avulla voit määrittää valmistelu-aikataulun, joka perustuu varattuja resursseja.
-   Arvioida kustannuksia ja määrittää alustavan budjetin projektiin liitettyjen roolien ja resurssien perusteella.
-   Roolien avulla voit arvioida resurssien varaukset, joita tarvitaan kunkin kihlautumisesta määrä.
-   Arvioida projektin koko elinkaaren ajaksi tarvittavien resurssien määrän.
-   Laatia työrakenteen käyttämällä alustavia resurssimäärityksiä.

[![Projektin elinkaari](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Projektin suunnittelu tuotot suunnitellut resurssit voidaan korvata henkilöstö-resursseja. Projektipäällikkö voit myös palata ja päivittää resourcing varauksia projektin vaiheiden aikana.

## <a name="set-up-project-resources"></a>Projektiresurssien määrittäminen
Sinun täytyy määrittää kalenteri ja liittää se työntekijään. Kalenterin avulla ajoittaa projektin ja projektin resurssit, jotka on varattu työaika. Kalenteria määrittäessään projektipäälliköt voivat suorittaa resurssien tasaamisen resurssien optimoinnin yhteydessä. Kalenterin aikataulun perusteella resursseille voidaan asettaa rajoituksia. Voit määrittää kalenteri **kalenterit** sivulla. 

Kun määrität työntekijän projektin resurssiksi, voit valita työntekijät, jotka toimivat yrityksessä, jolle olet määrittämässä resursseja tai voit valita työntekijöiden organisaation muiden yritysten. Nämä ovat konsernin resurssit. Seuraavassa ohjeessa selitetään määrittäminen työntekijän projektiresurssiksi yrityksen ja konsernin Projektiresurssi määrittämisestä.

### <a name="set-up-a-worker-as-a-project-resource"></a>Työntekijän määrittäminen projektiresurssiksi

1.  - **Työntekijöiden**, sivu **työntekijöiden** luettelosta, työntekijä, jota olet lisäämässä projekti resurssina ja avaa työntekijätietueeseen.
2.  Valitse toimintoruudussa **projektin**&gt;**asennus**&gt;**Projektiasetukset**.
3.  Valitse kalenteri ja sulje sivu.

Voit myös määrittää resurssille oletusprojektit eräänlaisena esimäärityksenä. Esimäärityksiä voidaan käyttää, kun resurssi- tai projektipäällikkö tietää jo etukäteen, missä projekteissa resurssi työskentelee. Esimääritykset voivat perustua myös projektin sponsorin tai asiakkaan pyyntöön. Jos haluat esimäärittää projektin, valitse **Määritä projektit** -sivulta **Projektit**-välilehdestä **Jäljellä olevat projektit** -luettelosta haluamasi projekti.

### <a name="set-up-an-intercompany-resource"></a>Määritä konsernin sisäinen resurssi

Määrittäessäsi työntekijälle kuin konsernin sisäinen resurssi lainaavan yrityksen ja vieraan pääoman yrityksen asetukset tulee täyttää. 

**Motivoitunut yrityksessä:**

1.  Tarkista Dynamics 365 operaatioille, lainaavan yrityksen on valittuna, ja noudata edellä, "Määritä työntekijän projektin resurssiksi."
2.  Siirry ** kirjanpidon **&gt; ** kirjausasetusten **&gt;**konserniyritysten välisen laskennan**. Click **New**.
3.  -** Oikeushenkilön tunnus ** motivoitunut yritys-kenttään. Täytä muut kentät tarpeen mukaan ja valitse sitten **Tallenna**.
4.  Go ** projekti, projektinhallinta- ja **&gt; ** asennus **&gt;**hinnat ** &gt;**siirtohinta**.** **
5.  Käyttöön ** siirtohinta **-lomakkeen- **uusi**, ja ** lainaava yritys **-kentässä, valitse sopiva yritys.
6.  Jos haluat lainata vain vieraan pääoman yrityksen resurssi, jonka olet luonut tämän osan alussa **resurssin**, jonka olet luonut resurssin nimi-kenttään. Jos haluat määrittää kaikki resursseja yrityksen vieraan pääoman yritys, jätä ** resurssin ** tyhjä kenttä.
7.  Siirry ** projekti, projektinhallinta- ja **&gt; ** asennus **&gt;**projektin hallinnan ja kirjanpidon parametrit**, ja ** konsernin **-välilehdessä määrittää ** konsernin resurssien ajoitus ja tuntilomakkeiden ** kentän arvoksi **Kyllä**.

**Vieraan pääoman yrityksessä:**

1.  Siirry **projekti, projektinhallinta- ja**&gt;**projektin resurssit**&gt;**resurssien luettelon**.
2.  Kirjoita nimi, jonka loit edellisessä lainaavan yrityksen Varmista, että nimi on mukana yrityksen vieraan pääoman resurssiluettelossa resurssien search-suodatin.

## <a name="manage-resource-competencies"></a>Resurssin osaamisalueiden hallinta
Resurssin osaamista ovat olennainen osa resurssien hallinta. Osaamisalueita voi käyttää perustasona määriteltäessä resursseja, joilla on oikeanlaiset taidot, koulutus, todistukset ja projektikokemus. Nämä tiedot on määritettävä joka resurssille ja päivitettävä säännöllisesti. Näin voit maksimoida osaamisen, kun tiettyjä resurssien osaamisalueita yhdistellään projektin resurssimäärityksen yhteydessä. [![Taidot, tutkinnot, koulutuksen ja projektikokemuksen esimerkkejä](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Seuraavissa ohjeissa selitetään, miten voi määrittää joitakin resurssin osaamisalueista. 

Voit määrittää työntekijän osaamisalueet joko Henkilöstöhallinto-osassa **Työntekijät**-luettelossa tai Projektinhallinta ja kirjanpito -osassa **Resurssit**-sivulla. Seuraavista toimista **työntekijöiden** käytetään Human resources-sivu.

### <a name="set-up-competencies-certificates"></a>Osaamisalueiden määrittäminen: todistukset

1.  Valitse **Työntekijät**-luettelosivulta sen työntekijän rivi, johon haluat lisätä todistustiedot.
2.  Napsauta toimintoruudun **Työntekijä**-välilehdessä **Osaamistiedot**-ryhmässä **Todistukset**.
3.  Valitse **Uusi**.
4.  Valitse **Todistuksen tyyppi** -kentästä **PMP**.
5.  Valitse **Alkamispäivä** -kentästä **10/1/2015**.
6.  Valitse **Tallenna** ja sulje sitten sivu.

### <a name="set-up-competencies-skills"></a>Osaamisalueiden määrittäminen: osaamisalueet

1.  Varmista **Työntekijät**-luettelosivulla, että aiemmassa vaiheessa valitsemasi työntekijä on yhä valittuna. Valitse sitten toimintoruudun **Työntekijä**-välilehdessä **Osaamistiedot**-ryhmässä **Osaamisalueet**.
2.  Valitse **Uusi**.
3.  Valitse **Osaamisalue**-kentästä **Projektinhallinta**.
4.  Valitse **Taso**-kentästä **Asiantuntija**.
5.  Valitse **Tasopäivämäärä**-kentästä **1-/14/2014**.
6.  Kirjoita **Kokemus vuosina** -kenttään arvoksi **10**.
7.  Valitse **Tallenna** ja sulje sitten sivu.

## <a name="create-a-new-project"></a>Luo uusi projekti
1.  Valitse **projekti, projektinhallinta- ja**&gt;**työtilojen**&gt;**projektin hallinta**.
2.  Valitse **Uusi projekti** ja syötä sitten seuraavat arvot:
    -   **Projektin tyyppi** - aika- ja materiaaliprojektit
    -   **Projektinimi** -XYZ Upgrade-vaihe 2
    -   **Projektiryhmän** -TM\_KET
    -   **Projektin Sopimustunnusta** -00000002
3.  Valitse **Luo projekti**.

### <a name="assign-a-resource-to-a-project"></a>Resurssin määrittäminen projektiin

1.  Valitse **henkilöstöhallinnon**&gt;**työntekijöiden**&gt;**työntekijöiden**.
2.  Valitse **Työntekijät**-luettelosta sen työntekijän tietue, jonka osaamisalueet määritit aiemmassa vaiheessa, ja avaa tietue.
3.  Valitse toimintoruudussa **Projekti**-välilehden **Asetukset**-ryhmästä **Määritä projektit**.
4.  Napsauta **Resurssin oikeellisuustarkistuksen projektimääritykset** -sivulla **Projektit**-välilehteä.
5.  - **Lisää projekti valitut projektit**, projektin XYZ päivittää Phase 2 suodatus
6.  Valitse **Jäljellä olevat projektit** -ruudusta haluamasi projekti ja lisää se **Valitut projektit** -ruutuun napsauttamalla nuolta.
7.  Sulje sivu.

Tarvittaessa voit myös määrittää resurssille luokkia. Luokkatyyppi on joko Kustannus tai Tuotto. Tämä määräytyy organisaation mukaan. Jos resurssille ei ole määritettyjä luokkia, Dynamics 365 työvaiheiden etsiä oletusluokka tunti hintojen, kustannusten ja tuoton.

### <a name="set-up-project-resource-and-role-characteristics"></a>Projektin resurssin ja rooliominaisuuksien määrittäminen

Projektipäällikkö voi projektin resursointitoiminnolla luoda projektissa tarvittavia rooleja. Rooleja voidaan käyttää vahvistettuja resursseja on edelleen Tuntematon resurssien varaamista. Roolit tilapäisesti varattavissa resursseiksi suunniteltu niin, että voit jatkaa projektin suunnittelun vaiheet. 

[![Esimerkki rooli](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Skenaario: **Contoso palkattiin suorittamaan aika- ja materiaaliprojekti, jolla on hyväksytty projektin perustamisasiakirja. Nuorempi projektipäällikkö on yhä laatimassa projektin laajuutta. Resurssinhallinta on tällä hetkellä tunnistaa tietyt resurssit, jotka varataan toimimaan uuden projektin. Vanhempi projektipäällikkö on yksi rooleja, jotka tärkeän hankkeen luonteen vuoksi projektin sponsori pyysi. Resurssinhallinta on hankittava uusi resurssi ja määrittää roolin järjestelmässä siltä varalta, että nuorempi projektipäällikkö edellyttää projektin suunnitteluvaiheessa resurssitiedot. 

Seuraavissa vaiheissa esitetään, miten Resurssienhallinta nimittäminen projektin hallinnan roolien määrittäminen ja resurssien ominaisuuksia liittää. Myöhemmin roolin avulla voidaan hakea käytettävissä olevia resursseja, jotka vastaavat tarvittavia resurssin osaamisalueita.

1.  Valitse **projekti, projektinhallinta- ja**&gt;**asennus**&gt;**resurssien**&gt;**roolien asennuksen**.
2.  Valitse **Uusi** ja syötä seuraavat arvot:
    -   **Roolin tunnus** -vanhempi projektipäällikkö
    -   **Kuvaus** -vanhempi projektipäällikkö
3.  Valitse **Luo**.
4.  Valitse **Vastaava projektipäällikkö** -rooli ja valitse sitten **Määritä ominaisuudet**.
5.  Valitse **Ominaisuuden tyyppi** -kentästä **Osaamisalue**.
6.  Syötä **Käytettävissä olevat ominaisuudet** -kenttään hakemasi osaamisalue.
7.  Valitse **Ominaisuustyyppi**-kentästä **Todistus**.
8.  Syötä **Käytettävissä olevat ominaisuudet** -kenttään haettava todistustyyppi.
9.  Valitse **OK** ja sulje sivu.

### <a name="assign-a-project-resource-to-a-project"></a>Projektiresurssin määrittäminen projektiin

1.  Valitse **projekti, projektinhallinta- ja**&gt;**yhteisen**&gt;**projektien**&gt;**kaikkien projektien**, ja Avaa **XYZ päivittää Phase 2** projektin.
2.  Valitse **Projektiryhmän ja ajoitus** -välilehdestä **Lisää**.
3.  Valitse **Rooli**-kentästä **Ryhmän jäsen**.
4.  Valitse **Varaa kalenterista**.
5.  Valitse **Resurssin saatavuus** -sivulta **Näyttöasetukset**.
6.  Syötä **Muuta näyttöasetuksia** -sivulle seuraavat arvot:
    -   **Päivämäärä alueen näkymän muoto** - päivä
    -   **Näytä saatavuus kuvaukset** - Kyllä
    -   **Näytä jäljellä oleva kapasiteetti** - Kyllä
7.  Valitse resurssiluettelosta haluamasi resurssi.
8.  Valitse **Kova kirja**&gt;**täysi kapasiteetti**.
9.  Sulje sivu.

### <a name="assign-a-resource-to-a-default-role"></a>Resurssin määrittäminen oletusrooliin

Projektin tai resurssin päälliköt avulla voit porautua syvemmälle resursseja, jotka voidaan varata projektille. Voit liittää oletusroolin aiemmin luotuun tai vasta hankittuun resurssiin. Esimerkiksi kun Daniel oli palkataan, hän oli kokemus ja taidot liiketoiminta-analyytikko roolin täyttää. Resurssinhallinta määritetty tämä rooli Daniel's oletus roolissa. Tämän vuoksi Resurssienhallinta lisätään Daniel joukon business analyytikot, jotka ovat käytettävissä projektityöhön. 

Resurssin varauksen aikana projektipäälliköt voi suodattaa roolin resurssit, jotka ovat käytettävissä projektityöhön. Päälliköt voivat käyttää näitä tietoja yhtenä ehtona analysoidessaan päätöksiä useiden ehtojen perusteella resurssien täyttämisen yhteydessä. He voivat lisätä suodattimeen muitakin resurssin ominaisuuksia ja hakea niiden avulla resursseja, joilla on projektissa tarvittavat osaamisalueet, koulutus ja kokemus. 

**Skenaario:** hyväksyttyä hanketta on aloitettu ja nimittäminen projektin hallinnan rooli oli varattu resurssiksi suunnitellun projektin suunnitteluvaihe aikana. Resurssipäällikön on nyt hankittava rooliin sopiva resurssi.

1.  Valitse **projekti, projektinhallinta- ja**&gt;**projektin resurssit**&gt;**resurssien luettelon**.
2.  Valitse **Resurssi**-luettelosta **Daniel Goldschmidt**.
3.  Valitse **projektin resurssien**&gt;**ylläpitäminen**&gt;**resurssin roolin**.
4.  Valitse **Uusi** ja syötä seuraavat arvot:
    -   **Tehokas** - (kuluva päivämäärä)
    -   **Vanhentumisen** - ei koskaan
    -   **Roolin** -vanhempi projektipäällikkö
5.  Valitse **Tallenna** ja sulje sitten sivu.
6.  Lisää **Osaamistiedot**-välilehdessä **ProjectMgmt**-osaamisalue ja **PMP**-todistus.

## <a name="set-up-role-based-pricing"></a>Roolipohjaisen hinnoittelun määrittäminen
Rooleille voidaan määrittää kaikki kustannukset sekä myynti- ja siirtohinnat.

1.  Valitse **projekti, projektinhallinta- ja**&gt;**asennus**&gt;**hinnat**&gt;**myyntihinta (tunti)**.
2.  Click **New**.
3.  Anna voimaantulopäivämäärä.
4.  Valitse **Rooli**-sarakkeesta haluamasi rooli.
5.  Syötä **Hinnoittelu**-sarakkeeseen hinta valitulle resurssiroolille.

## <a name="form-a-project-team"></a>Työryhmän muodostavat
Käyttämään rooleja, jotka on aiemmin määritetty projektin projektipäällikkö täytyy yhdistää projektin roolit. Projektille voidaan määrittää useita rooleja ja toimintoja varten 365 Dynamics otsikot automaattisesti nämä roolit aikana varaus Sekaannusten välttämiseksi. Esimerkiksi jos projektipäällikkö vaatii kolme software Engineer kolme ohjelmisto insinööri roolit, joilla ohjelmisto insinööri 1, ohjelmisto insinööri 2 ja ohjelmisto insinööri 3 kuin niiden otsikot luodaan automaattisesti. Jos roolille on määritetty ominaisuudet jo aiemmin, niitä käytetään suodattimina resurssia haettaessa. Hakua voi tarkentaa lisäämällä muitakin ominaisuuksia tarpeen mukaan. 

Myös näyttöasetukset voidaan mukauttaa, jotta resurssien käytettävyys saadaan paremmin näkyviin. Näyttöperusteeksi voi valita käytettävyyden tunnin, päivän, viikon, kuukauden, vuosineljänneksen tai vuoden perusteella. Myös resurssien käytettävissä ja jäljellä olevan kapasiteetin voi suodattaa näkyviin. Tämä vaihtoehto on hyödyllinen ajanhallinnassa, kun arvioit tehtäviin käytettävissä olevaa aikaa tai resurssien käytettävyyttä. 

Projektipäällikkö voi Valitse rooli-sivulla ja jos on vapaa resurssi, joka sopii vaatimus, valitse voit varata resurssin, voit täyttää rooli. Huomaa, että resursseja ei tarvitse olla tässä vaiheessa varattu suunnittelun vaiheessa. Luodessasi WBS, voit korvata henkilöstö resurssit projektin roolit. Jos roolit on korvattu WBS henkilöstö resurssit, resurssien asetukset päivittää automaattisesti projektiryhmän luetteloidaan ja ajoitus. 

[![Projektiryhmä luettelo, joka sisältää rooleja sekä todellisia resursseja](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektipäällikkö voi varata resurssin projektiin eri tavoilla, esimerkiksi valitsemalla **Jäljellä oleva kapasiteetti**, **Koko kapasiteetti**, **Kapasiteettiprosentti** ja **Määritä tunnit**. Nämä varausasetukset voi peruuttaa milloin tahansa, jos resurssimääritykset muuttuvat. Kahta varaustyyppiä tuetaan:

-   **Kova kirja** – resurssien varaamiseen oli hyväksytty ja vahvistettu toimimaan kihlautumisesta määritetyn keston ajaksi.
-   **Alustavasti** – resurssien varauksia määritettiin alustavasti määritetyn keston kihlautumisesta toimimaan.

Seuraavissa vaiheissa on selostettu, miten projektiryhmä luodaan.

### <a name="create-a-project-team"></a>Projektiryhmän luominen

1.  Valitse **Kaikki projektit** -luettelosivulta haluamasi projekti ja valitse sitten **Muokkaa**.
2.  - **Projektin ryhmän ja ajoitus** -lehden **aikataulun viimeinen päivämäärä** -kenttään alkamispäivämäärä lisättynä yhdellä kuukaudella. Esimerkiksi jos aikataulun aloituspäivä on 24. kesäkuuta 2017 (24/06/2017), Määritä **/24/07-2017**.
3.  Click **Add**.
4.  Valitse **Lisää roolit projektiin** -ruudun **Rooli**-kentästä **Vastaava projektipäällikkö**.
5.  Valitse **Vaaditut osaamisalueet**.
6.  Aiemmin vastaavan projektipäällikön roolille määrittämäsi ominaisuudet tulevat oletusarvoisesti valituiksi **Valitse ominaisuudet** -sivulla. Napsauta **OK**.
7.  Syötä **Lisää roolit projektiin** -sivulla **Resurssien määrä** -kenttään arvoksi **1**.
8.  Hakutoiminto näyttää **Resurssi**-kentässä kaikki resurssit, joilla on tarvittavat osaamistiedot. Valitse **Daniel Goldschmidt** ja sitten **Luo**.
9.  Valitse **Projekti**-sivulla **Lisää**.
10. Valitse **Lisää roolit projektiin** -ruudun **Rooli**-kentästä **Ryhmän jäsen**. Syötä **Resurssien määrä** -kenttään arvoksi **5**.
11. Valitse **Luo**.
12. Valitse **Projektit**-sivulla **Toteuta resurssi**.

## <a name="resource-capacity-synchronization"></a>Resurssin kapasiteetin synkronointi
Resurssin synkronointiprosessi auttaa varmistamaan, että kalenterin ja peruskalenterin tiedot siirtyvät projektiresurssien ajoitukseen. Jos kalenteria muutetaan, prosessit tekevät projektiresurssien ajoitukseen tarvittavat päivitykset. Prosessit auttavat myös parantamaan suorituskykyä, koska kalenterin resurssitiedot synkronoidaan etukäteen, jotta resurssin ajoitustietoihin tehtävät päivitykset voidaan tehdä nopeammin. Prosessit kannattaa ajoittaa eräajona, ei yksitellen. Muussa tapauksessa riskinä on, että edelliseen synkronointiin sisällytettävät päivämäärät unohtuvat. Jos sisällytettäviä päivämääriä ei käytetä, päivämäärien synkronointiin voi jäädä aukkoja.

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Kalenterin synkronointi](./media/projectresourcing04-1024x471.jpg)

**Synchronize resource capacity roll-ups**

Synkronointiprosessin tarkoituksena on synkronoida kaikki resurssin kalenteritiedot. Näihin tietoihin sisältyvät peruskalenterin tiedot kaikista muutoksista, jotka tehdään projektin resurssikalenterin kapasiteettitaulukkoon. Jos resurssit on lisätty projektiin, synkronointi varmistaa, että päivitettyjä tietoja on käytettävissä. Synkronoinnin voi tehdä milloin tahansa. 

Ne kannattaa tehdä eräajona. Vaihtoehdot ovat käytettävissä kapasiteettivarauksia synkronoitaessa.

-   Valitse **projekti, projektinhallinta- ja**&gt;**Kausittainen**&gt;**synkronoinnin kapasiteetti**&gt;**resurssien kapasiteetti-koonnissa synkronoi**.

| Vaihtoehto | kuvaus                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kyllä    | Synkronoi kaikki resurssitiedot kalenteriin ja peruskalenterin tietojen kanssa ja korvaa kaikki projektin resurssin kapasiteettikalenterissa olevat tiedot.                                                  |
| Ei     | Synkronoi resurssitiedot päivämäärävälin koodin sekä määritettyjen alkamis- ja päättymispäivämäärien perusteella. Tämä vaihtoehto ei poista nykyisiä tietoja, ja se päivittää vain uusien lisättyjen resurssien tiedot. |

[![Synkronoinnin aikana](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Roolien määrittäminen työrakennemalleille
Projektipäälliköt voivat määrittää työrakennemalleja ja käyttää niitä luodessaan uusille projekteille työrakennetta. Projektipäälliköt voivat luoda rooleja, kun he luovat mallin. Seuraavien ohjeiden avulla voit määrittää roolin WBS template.* * **

1.  Valitse **projekti, projektinhallinta- ja**&gt;**asennus**&gt;**projektien**&gt;**Työrakennemallit**.
2.  Valitse valitun työrakennemallin **Tiedot**-kohta.
3.  Valitse luettelosta haluamasi tehtävä ja valitse sitten **Rooli**-kentästä tehtävään määritettävä rooli.

### <a name="work-with-a-wbs"></a>Työrakenteen käsitteleminen

Voit luoda uuden työrakenteen tai kopioida sen aiemmin luodusta työrakennemallista. Projektipäällikkö voi hallita resursseja helposti määrittämällä työrakenteessa roolit uusille tehtäville. Roolit voidaan korvata, kun resurssi on hankittu tai kun vahvistettu resurssi tehtävään on määritetty. Näin projektipäälliköt voivat suorittaa joustavasti seuraavat tehtävät:

-   Määrittää työrakenteen työpaketteihin tarvittavan resurssien määrän.
-   Arvioida projektikustannukset.
-   Määritellä alustavan budjetin.
-   Arvioida tehtävän kestoa roolien ja resurssien perusteella.
-   Kehittää joitakin projektinhallintasuunnitelmia käytettävissä olevien projektitietojen pohjalta.

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
<td>Lisää suunnitellut resurssit automaattisesti käyttämällä tehtävään liitettyjä rooleja. Työvaiheiden 365 Dynamics ehdottaa automaattisesti suunnitellut resursseja käyttämällä useita ehtoja päätös analyysi, joka perustuu rooleihin. Kun tehtäville on määritetty roolit ja työaika (tunnit) työrakenteessa ja rakenne on julkaistu, valitse <strong>Luo ryhmä automaattisesti</strong>. Tarvittava suunniteltujen resurssien määrä lisätään työrakenteeseen ja <strong>Projektiryhmä ja ajoitus</strong> -välilehteen.</td>
</tr>
<tr class="odd">
<td>Resurssi (avattava luettelo)</td>
<td><strong>Käynnistä resurssimääritys</strong> -sivulla voit valita resurssit kiinteää tai alustavaa varausta varten määritetyn keston perusteella. Voit muokata näyttöasetuksia niin, että saat näkyviin ja voit määrittää resurssitehtävien keston. Voit valita ja määrittää resursseja työpakettitasolla käyttämällä seuraavia vaihtoehtoja:
<ul>
<li><strong>Hyväksy</strong> – vahvistaa tehtävään liitettyyn resurssiin tehdyt muutokset.</li>
<li><strong>Peruuta</strong> – peruuttaa tehtävään liitettyyn resurssiin tehdyt muutokset.</li>
<li><strong>Määrittää automaattisesti</strong> – tämä vaihtoehto valitsee käytettävissä staffed resurssia vastaava rooli valitun tehtävän kanssa.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Valitse **projekti, projektinhallinta- ja**&gt;**projektien**&gt;**kaikkien projektien**.
2.  Valitse luettelosta **XYZ-päivitysvaihe 2** -projekti.
3.  Valitse **suunnitelma**&gt;**toimintojen**&gt;**työrakenne**.
4.  Valitse **Uusi** ja lisää seuraavat ykköstason tehtävät työrakenteeseen:
    -   Aloittaminen
    -   Suunnittelu
    -   Suoritetaan
    -   Valvonta ja ohjaus
    -   Sulje

5.  Määritä päivämäärät ja vaivaa kuva (tuntia), seuraavassa esitetyllä tavalla. [![Päivämäärät ja vaivaa](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
6.  Valitse **Aloittaminen**-tehtävärivi ja valitse sitten **Rooli**-kentästä **Vastaava projektipäällikkö**.
7.  Valitse **Julkaise**.
8.  Valitse samalta riviltä **Resurssi**-kentästä **Daniel Goldschmidt**.
9.  Valitse **Hyväksy**.
10. Valitsemalla **Suunnittelu**-tehtävärivi ja valitse sitten **Rooli**-kentästä **Yritysanalyytikko**.
11. Valitse **Julkaise** ja sitten **Luo ryhmä automaattisesti**.
12. Valitse näyttöön tulevassa valintaikkunassa **Kyllä**.
13. Tarkista, että **Resurssi**-kentässä arvona on **Yritysanalyytikko 1**.
14. Avaa hakutoiminto **Yritysanalyytikko 1** -resurssin kohdalla ja valitse **Käynnistä resurssimäärityksen lomake**.
15. Valitse tehtävään työntekijä.
16. Valitse **Pehmeä liittäminen**&gt;**täysi kapasiteetti**.
17. Valitse **Tallenna** ja sulje sivu. 

> [!NOTE] 
> Saat varoituksen, että määritettyä resurssia on nyt 2, koska varojen määrä jää 1.
18. Tarkista **Työrakenne**-sivulta työrakenteen resurssimääritys ja valitse sitten **Tallenna**.

## <a name="resource-fulfillment-for-planned-resources"></a>Resurssin toteuttaminen suunnitelluille resursseille
Projektipäällikkö voi suunnitella projektille tarvittavat resurssiroolit. Resurssipäällikkö näkee suunnitellut resurssit pyyntöinä **Resurssin toteuttaminen** -sivulla ja voi määrittää varsinaiset resurssit.

1.  Valitse **projekti, projektinhallinta- ja**&gt;**projektien**&gt;**kaikkien projektien**.
2.  Valitse luettelosta **XYZ-päivitysvaihe 2** -projekti.
3.  Valitse **Projekti**.
4.  Valitse **Muokkaa**.
5.  - **Projektin ryhmän ja ajoitus** -välilehden ** ** valitsemalla **Lisää**.
6.  Valitse **Lisää roolit** -valintaikkunassa **Ohjelmistokehittäjä**-rooli.
7.  Valitse **Luo**.
8.  Sulje projektisivu.
9.  Valitse **projekti, projektinhallinta- ja**&gt;**projektin resurssit**&gt;**resurssin valmistuminen**.
10. Valitse **Ohjelmistokehittäjä 1** **XYZ-päivitysvaihe 2** -projektille.
11. Valitse työntekijä ja napsauta sitten **Määritä**.
12. Tarkista, että **Ohjelmistokehittäjä 1** -rivi on poistettu **XYZ-päivitysvaihe 2** -projektista.
13. Tarkista **Projektiryhmä ja ajoitus** -välilehdessä, että vaiheessa 11 valitsemasi työntekijä on lisätty **XYZ-päivitysvaihe 2** -projektiin **ohjelmistokehittäjäksi**.

## <a name="requests-for-project-resources"></a>Projektiresurssien pyyntöihin
Projektin resurssien ajoituksen toimintoja tukee vain henkilöstöpäälliköt voivat jakaa resursseja henkilöstö tapahtumista tai projekteja. Voit ottaa tämän toiminnon käyttöön tekemällä seuraavat toimet tai varmista, että ne on täytetty.

-   Määritä numerosarjat.
-   Määritä projektinhallinnan ja kirjanpidon työnkulut.
-   Ota käyttöön resurssien pyyntö-työnkulun.

Sen jälkeen, kun olet tarkistanut tai suorittaa edellä mainittuja tehtäviä, voit tehdä seuraavat tehtävät tarvittaessa.

-   Luo staffed alustavasti varattu resurssi resurssin request.
-   Valvonnan resurssien pyyntöihin.
-   Täytettävä resurssi-pyynnöt.
-   WBS pyytää resurssin staffed.
-   Kirja ilman erityistä pyyntöä staffed resurssin projektiin resursseja.

## <a name="monitor-project-teams"></a>Näytön Projektiryhmät
1.  Valitse **projekti, projektinhallinta- ja**&gt;**projektien**&gt;**kaikkien projektien**.
2.  Napsauta projektiluettelossa **XYZ-päivitysvaihe 2** -projektin **Projektitunnus**-linkkiä.
3.  Tarkista **Projektiryhmä ja ajoitus** -pikavälilehdessä, että luettelossa näkyvät projektiresurssit ovat oikein.



