---
title: Taloushallinnon tiedot
description: Taloushallinnon tiedot kerää Microsoft Power BI:n avulla yhteen taloushallinnon tunnusluvut, kaaviot ja tilinpäätöksiä.
author: kweekley
manager: AnnBe
ms.date: 05/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 9aaf24147900c890a14c60ab969da7124c538911
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115725"
---
# <a name="financial-insights"></a>Taloushallinnon tiedot

[!include [banner](../includes/banner.md)]

**Taloushallinnon tiedot** kerää Microsoft Power BI:n avulla yhteen taloushallinnon tunnusluvut, kaaviot ja tilinpäätöksiä. Power BI on upotettu sovellukseen. **Taloushallinnon tiedoissa** keskitytään on analyyttiseen raportointiin. Organisaation työntekijät voivat tarkastella tietoja, tutkia niitä, tiedostaa ne ja toimia. 

**Taloushallinnon tiedot** yhdistää kirjanpidon ja alareskontran tiedot ja tuottaa niiden avulla kattavan kuvan organisaation taloudellisesta tilasta.

> [!NOTE]
> Tässä asiakirjassa käytetään seuraavia Power BI -termejä:
> 
> - **Raportti** – yksi .pbix-tiedosto, johon kaikkien välilehtien visualisoinnit tallennetaan.
> - **Sivu** – Yhden välilehden sisältävä .pbix-tiedosto. Kullakin sivulla voi olla useita visualisointeja.
> - **Visualisointi** – Yksi tietolähde, kuten kortti, tunnusluku, kaavio, taulukko tai raportti. Jos sivulla oleva visualisointi on raportti, siinä ei voi olla muita visualisointeja raportoitavien tietojen koon vuoksi.

Tällä hetkellä **taloushallinnon tiedoissa** voi katsella aktiivisen yrityksen ja kaikkien yritysten tietoja. Tulevissa versioissa työtila kehittyy paikaksi, jossa voit muokata ja luoda visualisointeja Power BI:n avulla.

Vaikka **Talousjohtajan yhteenveto** -työtilassa on samat visualisoinnit **taloushallinnon tiedoissa**, se keskittyy ennen kaikkea aiemmin luotujen tietojen tarkasteluun ja suodattamiseen. Tulevissa versioissa voit lisätä uusia visualisointeja **Taloushallinnon tiedot** -työtilaan. Uudet visualisointeja on ehkä mahdollista käyttää myös muissa työtiloissa, jotka keskittyvät toisiin rooleihin, kuten projekti- tai ostoreskontrapäälliköihin. **Talousjohtajan yhteenveto** -työtilassa on jatkossakin näkyvissä kaikkien yritysten tiedot riippumatta siitä, minkä yrityksen käyttöoikeudet roolilla on.

## <a name="dynamics-365-finance-setup"></a>Dynamics 365 Finance -asetukset
**Kirjanpito**

Päätilityypin ja päätililuokkien avulla täytetään **taloushallinnon tietojen** **Tase**-raportin ja erilaisten **Tuloslaskelma**-raporttien oletuspäätilit.

Sinun on määritettävä **Päätilit**-sivulla päätili, jotta siihen voidaan määrittää jokin seuraavista tyypeistä:

- Myyntituotto
- Expense
- Käyttöomaisuus
- Velat
- Oma pääoma

Älä määritä päätileille mitään muuta päätilin tyyppiä, kuten **Tase** tai **Voitto ja tappio**. Raportit eivät voi määrittää päätilin tyyppiä, kun muita päätilityyppejä on määritetty, sillä ne eivät ole riittävän yksityiskohtaisia. Päätilin tyyppi on määritettävä näyttämään velat ja tuotto raporteissa positiivisina summina.

Jokaiselle päätilille on määritettävä päätililuokka, sillä muuten ne eivät näy tilinpäätöksissä eivätkä sisälly muihin visualisointeihin, kuten tunnuslukuihin. Päätililuokkia on parannettu siten, että sisältävät näyttöjärjestyksen. Näyttöjärjestystä käytetään nimenomaisesti **taloushallinnon tietojen** raporteissa. Kun olet muokannut päätilin luokkaa tai lisännyt uuden luokat, voit muuttaa **Näyttöjärjestys**-arvon määrittämään järjestyksessä, jossa päätilin luokat näytetään raportissa. Jos useiden päätilin luokkien näyttöjärjestystä on muutettava, Avaa Excelissä -toiminto nopeuttaa muokkausta ja muutosten julkaisemista takaisin sovellukseen.

## <a name="entity-store"></a>Yksikkösäilö
**Taloushallinnon tiedoissa** olevat tiedot noudetaan yksikkösäilöstä (**Järjestelmänvalvoja** \> **Asetukset** \> **Yksikkösäilö**). Jos avaat **Talousjohtajan yhteenveto**- tai **Taloushallinnon tiedot** -työtilan ja seuraava varoitussanoma avautuu visualisoinneissa, yksiköt on päivitettävä.

![Varoitus](./media/Cantdisplay.png)

Seuraavat yksiköt on päivitettävä, jos haluat nähdä **Taloushallinnon tiedot**- ja **Talousjohtajan yhteenveto** -työtilojen tiedot:

- BudgetActivityMeasure
- Taloushallinnon raportoinnin tapahtumatietojen versio 3 
- CustCollectionsBIMeasurements
- LedgerActivityMeasure
- LedgerCovLiquidityMeasurement
- Ostokuutio
- Myyntikuutio

Edellisessä versiossa LedgerActivityMeasure- ja VendPaymentBIMeasure-yksiköitä käytettiin **Talousjohtajan yhteenveto** -työtilan tiedoille. Niitä ei kuitenkaan enää käytetä nykyisessä versiossa.

Voit määrittää toistuvan erätyön päivittämään yksiköiden tiedot säännöllisesti. Koska jokainen yksikkö muodostetaan kokonaan uudelleen päivityksen aikana, valitse yksikköpäivitysten ajankohta tai tiheys huolellisesti. Ensisijainen tilinpäätöksissä käytettävä yksikkö on FinancialReportingTransactionData. Voitkin harkita sen päivittämistä muita useammin.

## <a name="security"></a>Suojaus
Upotettujen Power BI -raporttien tietoja ei voi tällä hetkellä rajoittaa niihin yritykseen, joiden käyttöoikeus käyttäjällä on. Tämän vuoksi upotettuja Power BI -raportteja hallitaan suojausasetusten tehtävillä. Määritetyt tehtävät antavat joko kaikkien yritysten tai aktiivisen yrityksen tietojen käyttöoikeuden. Seuraavassa taulussa on olemassa olevat velvollisuudet ja roolit, joihin ne on määritetty. Velvollisuuksia voi poistaa tai ne voidaan määrittää eri rooleille organisaation tarpeiden mukaan.

| Tulli                                    | Roolit | kuvaus |
|-----------------------------------------|-------|------------|
| Näytä talousjohtajan yhteenvedon työtila             | Talousjohtaja | Tämä velvollisuus antaa Talousjohtajan yhteenveto -työtilan käyttöoikeuden. Aktiivista yritystä käytetään oletusarvoisesti suodattimena. Voit kuitenkin lisätä kaikki yritykset riippumatta siitä, onko käyttäjällä muiden yritysten käyttöoikeutta. |
| Näytä nykyisen yrityksen taloushallinnon tiedot | <ul><li>Kirjanpitäjä</li><li>Laskentapäällikkö</li><li>Taloushallintopäällikkö</li><li>Tilintarkastaja</li><li>Budjettipäällikkö</li><li>Pääjohtaja</li><li>Talousjohtaja</li><li>Laskentatoimen controller</li></ul> | Tämä velvollisuus antaa Taloushallinnon tiedot -työtilan käyttöoikeuden. Aktiivista yritystä käytetään oletusarvoisesti suodattimena. Et voi lisätä muita yrityksiä. |
| Näytä yritystenväliset taloushallinnon tiedot   | Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin versiossa 7.3 tätä velvollisuutta ei ole määritetty rooliin. Seuraavassa versiossa tämä velvollisuus määritetään talousjohtajan rooliin. | Tämä velvollisuus antaa Talousjohtajan yhteenveto -työtilan valikkovaihtoehdon käyttöoikeuden. Aktiivista yritystä käytetään oletusarvoisesti suodattimena. Voit kuitenkin lisätä kaikki yritykset riippumatta siitä, onko käyttäjällä muiden yritysten käyttöoikeutta. |


## <a name="financial-reporting-vs-financial-insights"></a>Financial reporting vs. Financial insights
Vaikka **Taloushallinnon tiedot** sisältää tilinpäätöksiä, se ei korvaa sovelluksen taloushallinnon raportointia. **Taloushallinnon tietojen** oletustilinpäätökset ovat laajuudeltaan rajoitettuja eivätkä ne sisällä kaiken tyyppisiä tilinpäätöksiä. Taloushallinnon raportointi on edelleen ensisijainen työkalu lakisääteisten tilinpäätösten suunnitteluun, luontiin ja muodostamiseen.

Seuraava vertailukaavio auttaa erottamaan vaihtoehdot toisistaan:


|                                                          | Taloushallinnon raportointi                                               | Taloushallinnon tiedot |
|----------------------------------------------------------|-------------------------------------------------------------------|--------------------|
| **Muokkaa oletusraportteja**                                 | Kyllä                                                               | En |
| **Luo uusia raportteja**                                   | Kyllä                                                               | En |
| **Raporttien tulostaminen**                                        | Kyllä                                                               | En |
| **Vie Exceliin**                                      | Kyllä                                                               | Rajoitettu raakatietojen vienti Exceliin, muotoilematon raportti |
| **Raportointihierarkian/organisaatiohierarkian tuki**   | Kyllä                                                               | En |
| **Alareskontran tietojen raportti**                             | Kyllä Rajoitettu yhteen toimittajaan, asiakkaaseen                              | Kyllä Toimittaja-, asiakas-, toimittaja/asiakasryhmät, toimittajan/asiakkaan osoitteet jne. |
| **Raportointivaluutta**                                   | Kyllä Kirjanpitovaluutta ja muuntaminen raportointivaluutaksi       | Ei Vain kirjanpitovaluutta |
| **Suojaus**                                             | Kyllä Financen ja raporttipuun suojauksen noudattaminen | Rajoitettu kaikkien yritysten raporttien näyttäminen (Finance and Operationsin suojauksesta riippumatta) tai vain aktiivinen yritys |
| **Erilaisten tilikarttojen ja tilivuosien tuki** | Kyllä                                                               | En |
| **Ulkoisten tietojen raportti**                              | En                                                                | En |
| **Konsolidointien tuki**                               | Kyllä                                                               | Rajoitettu raportointi useissa yrityksissä mutta vain kirjanpitovaluutan käyttö |

Alkuperäisen **Talousjohtajan yhteenveto** -työtilan käyttöliittymän lisäksi uudet tunnusluvut, kaaviot ja tilinpäätökset ovat käytettävissä Seuraavat tilinpäätökset ovat käytettävissä:

- Pääkirja
- Tase
- Aluekohtainen tuloslaskelma
- Tuloilmoitus – todellinen vs. budjetti
- Tuloslaskelma ja varianssit
- 12 kuukauden trendin tuloslaskelma
- Kulujen kolmen vuoden trendi
- Toimittajakohtaiset kulut
- Asiakaskohtainen myynti

## <a name="edit-visuals"></a>Visualisointien muokkaus
**Taloushallinnon tietojen** ensimmäisessä versiossa visualisointeja ei voitu muokata. Tulevissa versioissa käyttäjät, joilla on soveltuvat käyttöoikeudet, voivat luoda uusia visualisointeja, kopioida aiemmin luotuja visualisointeja ja muokata visualisointeja. Vaikka raportit sisältävät .pbix-tiedostot ovat käytettävissä resursseina, oletusraporttien muokkaamista ei suositella. Lisämuutoksia tehdään tilinpäätösten luonnissa käytettävään tietomalliin, oletusraportteihin ja mukautettuun raportin visualisointiin. Jotta voisit käyttää hyväksesi seuraavan version uusia ominaisuuksia ja tietomallissa tehtyjä muutoksia, sinun olisikin tehtävä uudelleen kaikki oletusmalleihin Microsoft Power BI Desktopissa tekemäsi muutokset.

## <a name="filtering"></a>Suodatus
Käyttäjät voivat suodattaa raportin vasemmalla olevan **Suodatus**-ruudun avulla. Tätä samaa ruutua voi käyttää myös Power BI Desktopista. Suodatustasoja on useita, eivätkä kaikki ole välttämättä käytettävissä sen mukaan, mitä valintoja olet tehnyt sivulla (välilehdessä), tai oletko käyttämässä porautumistoimintoja:

- **Raporttitason suodattimet** – näitä suodattimia käytetään kaikkien sivujen (välilehtien) kaikissa visualisoinneissa.
- **Sivutason suodattimet** – Näitä suodattamia käytetään kaikissa aktiivisen välilehden visualisoinneissa. Niitä käytetään raporttitason suodattimien jälkeen.
- **Visualisointitason suodattimet** – Näitä suodattimia käytetään vain valitussa visualisoinnissa. Näitä suodattimia käytetään sivutason suodattimien ohella.
- **Porautumissuodatin** – Tämä suodatin suodattaa nykyiseen visualisointiin käytettävästä lähdevisualisoinnista, kun poraudut lähdevisualisoinnista nykyiseen visualisointiin.

![Suodatusasetukset](./media/filter.png)

Voit poistaa tietyn suodatusarvon valitsemalla sen vieressä pyyhinsymbolin. Älä poista suodatinta valitsemalla X. Jos valitse X, suodatettava kenttä poistetaan suodatusvaihtoehdoista. Jos poistat kentän vahingossa suodattimesta, sulje työtila ja avaa se sitten uudelleen. Oletussuodatusasetukset otetaan uudelleen käyttöön.

Kun avaat työtilan ensimmäisen kerran, aktiivista yritystä käytetään oletusarvoisesti raporttitason suodattimena. Käyttäjät voivat käyttöoikeuksiensa mukaan ehkä lisätä muita yrityksiä tai vaihtaa suodattamisessa valittuna olevaa oletusyritystä.

**Kirjanpidon vuosikalenteri** -suodatin on pakollinen sen vuoksi, että visualisoinnissa käytettäisiin oikeaa kalenteria. Raporttitason suodattimeksi on oletusarvoisesti määritetty aktiivisen yrityksen kirjanpidon vuosikalenteri. Jos vaihdat suodattimeksi kirjanpidon vuosikalenterin, joka alku- tai loppupäivämäärä on erilainen, alkusaldoja ei sisällytetä. Tämän vuoksi **Tase**-tilinpäätöksissä näkyvä saldo ei ole oikea. Jos valitse suodattimessa ylimääräisen kirjanpidon vuosikalenterin, saat käyttöösi lisää sarakkeita. Kussakin lisäsarakejoukossa on kirjanpidon eri vuosikalenterin summat.

Myös **Kirjanpitotaso**-taso on pakollinen. Suodattimeksi on oletusarvoisesti määritetty Valittu. Voit valita suodattimessa muita kirjanpitotasoja, jos haluat nähdä kootut summat.

Myös **Päivämäärä**- ja **Tilivuosi**-kentissä on suodattimia. Näitä suodattimia käytetään yleensä sivutasolla. **Päivämäärä**-kenttää oletusarvoisesti suhteellista päivämäärä, jota voi muuttaa. Voit myös poistaa suhteellisen päivämäärän suodattimen ja käyttää sen sijaan **Tilivuosi**-suodatinta.

## <a name="currency"></a>Valuutta

Kaikki kirjanpidon tietoja raportoivat visualisoinnit näyttävät summat kirjanpitovaluuttana. Niinpä yrityksen mukaan suodatettaessa on oltava huolellinen, että vain samaa kirjanpitovaluuttaa käyttävät yritykset sisällytetään. Muussa tapauksessa koottavilla tiedoilla on eri valuutta.

Kaikki alareskontran tietoja raportoivat visualisoinnit näyttävät summat järjestelmän valuuttana. Tällaisia tietoja ovat esimerkiksi **Kassavirtaennuste**- ja **10 parasta** -visualisoinnit. Järjestelmän valuutta ja järjestelmän vaihtokurssin tyyppi määritetään **Järjestelmän parametrit**-sivulla.

**Saldo pankkitilin mukaan** -visualisointi käyttää summia pankkitilin valuuttana.

## <a name="dimensions"></a>Dimensiot

Oletustilinpäätökset eivät sisällä taloushallinnon dimensioita vaan keskittyvät päätiliin. Taloushallinnon dimensioiden tuki on käytettävissä tulevissa versioissa, kun raportit ovat muokattavissa. Organisaatiot sitten voivat silloin suodattaa taloushallinnon dimensioiden arvojen perusteella.

Joissakin tilinpäätöksissä on dimensioita, jotka perustavat alareskontran tapahtumiin. Uusien raporttien tavoitteena on mahdollistaa sellaisten dimensioiden suodattaminen, joita ei ole määritetty taloushallinnon dimensioiksi. Esimerkiksi toimittajakohtaisten kulujen oletusraporttia voi tarkentaa päätilin ulkopuolelle, joten toimittajakohtaisesti eritellyt saldot ovat näkyvissä. Toimittajaa ei ole määritetty taloushallinnon dimensiona. Sen sijaan järjestelmä etsii toimittajan palauttamalla alkuperäisen alareskontran tapahtuman.

Seuraavia dimensioita käytetään oletusraporteissa. Mikään niistä ei ole taloushallinnan dimensio.

- Toimittaja
- Toimittajaryhmä
- Asiakas
- Asiakasryhmä
- Maa/alue
- Osavaltio tai provinssi
- Paikkakunta

> [!IMPORTANT] 
> Jos teet useiden toimittajien tai asiakkaiden yhteenvedon yhteen tositteeseen talouskirjauskansioiden avulla, tiedot eivät ole oikein. Raportointi ei voi määrittää, mikä toimittaja vai asiakas liittyy tiettyyn kirjauskansioviennin kirjanpitotiliin, koska kyseistä tietoa ei ole missään. Tämän vuoksi useiden toimittajien, asiakkaiden, käyttöomaisuuden tai projektien tietojen kirjaamista yhteen tositteeseen ei suositella.

## <a name="drill-on-data"></a>Tietoihin porautuminen

Power BI:n kautta on käytettävissä erilaisia poraustasoja. Jokaisella tasolla on oma nimi ja omat toiminnot. Voit porautua myös riveihin ja sarakkeisiin. Tässä osassa käsitellään erilaisia vaihtoehtoja käyttämällä esimerkkinä **Pääkirja**-raporttia ja näyttämällä, miten riveihin poraudutaan. Sarakkeissa on samat toiminnot. Vain **Poraudu**-asetus on vaihdettava.

Seuraavassa kuvassa **Pääkirja**-raportti on tiivistetty rivihierarkian ylimmälle tasolle päätilin tyyppiin.

![Alustava saldo -ilmoitus](./media/trial-balance.png)

Voit tarkastella hierarkian seuraavaa tasoa eli pääkirjan luokkia, valitsemalla **Poraudu**-kentässä ensin **Rivit** ja sitten **Laajenna**-painikkeen (Poraudu-kentän kolmas painike). Näet nyt kaikki päätilin luokat laajennettuina. Power BI:ssä ei voi tällä hetkellä laajentaa yhtä riviä tai saraketta siten, että kaikki muut rivit tai sarakkeet olisivat näkyvissä.

![Alustava saldo porautuminen riveihin](./media/trial-balance2.png)

Jos haluat laajentaa kaikkien rivien päätileihin, valitse uudelleen **Laajenna**-painike. Jos kuitenkin haluat porautua vain yhden rivin päätileihin, valitse ensin **Poraudu**-painike (alanuoli oikealla ikkunassa) ja sitten rivi, johon haluat porautua. Seuraavassa kuvassa näkee, mitä tapahtuu, kun **Myynti**-rivi on valittu **Poraudu**-painikkeen valinnan jälkeen.

![Alustava saldo -laajennuspainike](./media/trial-balance3.png)

Kun olet porautunut yhteen riviin, koko pääkirjaan palaaminen edellyttää useita napsautuksia. **Poraudu ylöspäin** -painikkeella (ensimmäinen painike **Poraudu**-kentän jälkeen) poraudutaan **Myynti**-luokassa ylöspäin seuraavan kuvan osoittamalla tavalla.

![Alustava saldo poraudu ylöspäin -painike](./media/trial-balance4.png)

Voit palata rivien yhteenvedon korkeimmalle tasolla jatkamalla **Poraudu**-painikkeen käyttöä.

Power BI:ssä on myös painike, jolla voit siirtyä hierarkian seuraavalle tasolle (toinen painike **Poraudu**-kentän jälkeen). Tämä painikkeen vaikutus on toinen kuin **Laajenna**-painikkeessa (kolmas painike **Poraudu**-kentän jälkeen), koska sitä käytetään hierarkian laajentamiseen. Kun laajennat hierarkian, hierarkiaa ylläpidetään raportissa. Jos esimerkiksi laajennat edellä näytetyllä tavalla päätilin tyypin, näet edelleen päätilin tyypin pääraportissa. Kun hierarkiassa sen sijaan siirrytään seuraavalle tasolle, raportti ei enää näytä ylätasoa hierarkiassa. (Katso seuraava kuva.)

![Alustava saldo poraudu takaisin -painike](./media/trial-balance5.png)

Jos haluat nähdä tapahtumatiedot, joihin yhteenvetosaldot perustuvat, voit valita joitakin summia, joissa haluat porautua takaisin Financial and Operationsiin.

Kun poraudutut raporteista taaksepäin, päädyt kirjanpitolähteen hallintaan (ASE) tositetapahtumien sijaan. Kirjanpitolähteen hallinta ei näytä vain kirjanpidon kirjanpitotapahtumia, vaan näkyvissä on myös alareskontratapahtuman tiedot. Saatkin paljon enemmän tietoja alkuperäistä tapahtumasta analyysia varten. Näet esimerkiksi, kuka toimittaja tai asiakas oli, mitä asiakas osti tai toimittaja myi sekä jopa mikä oli tapahtumassa käytetty projekti.

Raportin seuraavat suodattimet lähetetään kirjanpitolähteen hallintaan, jolloin näkyviin tulee kootut tapahtumat:

Pakolliset suodatuskentät:

- Oikeushenkilö
- Kirjanpidon vuosikalenteri
- Vuosi(a)
- Päätilin tunnus

Valinnaiset suodatuskentät:

- Vuosineljännes
- Kuukausi
- Jakso

Jos et laajenna rivissä riittävän pitkälle, porautuminen ei toimi. Jos laajennat vain päätilin luokkaan, et voi porautua saldon kirjanpitolähteen hallintaan, sillä päätili on kirjanpitolähteen hallinnan pakollinen suodatuskenttä.

Jos laajennat liian pitkälle rivillä, raporttien lisäsuodattimia ei lähetetä kirjanpitolähteen hallintaan. Tämän vuoksi luvut voivat olla erilaisia. Jos esimerkiksi laajennat maahan tai alueeseen Aluekohtainen tuloslaskelma -raportin riveillä, maata tai aluetta ei sisällytetä kirjanpitolähteen hallinnan suodattimena.

> [!NOTE]
> Voit porautua raportin riveillä tai sarakkeissa niin syvälle, että kirjanpitolähteen hallinta ei tällä hetkellä tue kyseisten tietojen suodatusta. Niinpä joissakin tilanteissa eriteltyjen tapahtumien summa kirjanpitolähteen hallinnassa ei vastaa saldoa, johon poraudut takaisin. Tämän toiminnon kehittämistä jatketaan tulevaisuudessa.

## <a name="hierarchies"></a>Hierarkiat

Oletusraportit käyttävät tietoihin porautumiseen ja tietojen laajentamiseen kahta hierarkiaa. Toinen hierarkia koskee rivejä ja toinen sarakkeita. Molemmat hierarkiat on määritetty valmiiksi raportin rakenteessa. Useimmissa raporteissa rivihierarkia on **Päätilin tyyppi** \> **Päätilin luokat** \> **Päätili**. Joissakin raporteissa on kuitenkin lisäkenttiä, kuten Maa ja alue. Hierarkian lisäsolmu perustuvat kunkin tapahtuman alareskontran tietoihin.

Sarakkeiden hierarkia keskittyy yrityksiin ja tilikausiin. Useimmissa raporteissa sarakehierarkia on **Yritys** \> **Kirjanpidon vuosikalenteri** \> **Tilivuosi** \> **Vuosineljännes** \> **Kausi**.

Raportit eivät tällä hetkellä tue organisaatiohierarkioita, joista voisi koota tietoja.

## <a name="data-limitations"></a>Tietojen rajoitukset
Raportin visualisoinneissa voi näytettävien rivien määrä on rajallinen. Tällä hetkellä rajaksi on määritetty 30 000. Jos tämä raja ylittyy, visualisointi ilmoittaa siitä varoitussymbolilla.

![Tietojen rajoitukset](./media/data-limit.png)

Jos enimmäismäärä ylitetään, raportissa näkyvät kokonaissummat ovat virheellisiä, koska kaikkia rivejä ei ole ladattu visualisointiin.

### <a name="empty-rows"></a>Tyhjät rivit
Power BI:ssä ei ole tyhjien rivien piilottamis- ja näyttämisasetusta. Jos rivillä ei ole tietoja, rivi ei näy visualisoinnissa.


## <a name="additional-resources-for-power-bi"></a>Power BI:n lisäresurssit

Seuraavissa resursseissa olevat tiedot eivät ole välttämättömiä otettaessa käyttöön upotettuja raportteja tuotantoympäristön **Talousjohtajan yhteenveto**- tai **Taloushallinnon tiedot** -työtilassa. Niistä on kuitenkin hyötyä kehityskehyksissä ja tilanteissa, joissa halutaan upottaa omia Power BI -raportteja.

- [Analyyttisten työtilojen ja raporttien käyttäminen 1-Box-ympäristössä](https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/)

- [Analytiikan lisääminen työtiloihin Power BI Embeddedin avulla](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces)
