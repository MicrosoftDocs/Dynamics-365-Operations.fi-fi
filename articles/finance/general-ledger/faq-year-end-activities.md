---
title: Tilinpäätöstehtävien usein kysytyt kysymykset
description: Tämä ohjeaihe on koottu avuksi tilinpäätöstehtävissä.
author: kweekley
ms.date: 01/25/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1b7606314b9cf7050a565822b5b9e23beb0cb4978b20e88596c5002d918cfcd9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725071"
---
# <a name="year-end-activities-faq"></a>Tilinpäätöstehtävien usein kysytyt kysymykset 

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe on koottu avuksi tilinpäätöstehtävissä. Tämän ohjeaiheen tiedot koskevat ensisijaisesti kirjanpidon ja ostoreskontran tilinpäätöstehtäviä.

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Kirjanpito: mistä tietää, että on suorittamassa tilinpäätöstä eikä kumoamassa sitä?
Organisaatiot ovat saattaneet yrittää suorittaa tilinpäätöstä, mutta ovatkin olleet kumoamassa tilinpäätöstä. Jos tilinpäätöksen suorittaminen vaikuttaa tapahtuvan todella nopeasti tai se ei tuota alkusaldoja, tarkista **Kumoa edellinen sulkeminen** ‑asetus kohdassa **Tilikauden lopetus** (**Kirjanpito > Kauden sulkeminen > Tilikauden lopetus > Suorita tilikauden lopetus**). 

[![Tilinpäätöksen suorittaminen verrattuna sen peruuttamiseen.](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Jos **Kumoa edellinen sulkeminen** ‑asetukseksi on valittu **Kyllä**, edellinen tilinpäätös peruutetaan. Kun kumoaminen suoritetaan, kaikki loppusaldo- ja alkusaldomerkinnät poistetaan, ikään kuin tilinpäätöstä ei olisi missään vaiheessa suoritettukaan. Tositteet poistetaan. Tilinpäätöstä ei suoriteta uudelleen automaattisesti. Prosessi on aloitettava uudelleen siten, että **Kumoa edellinen sulkeminen** ‑asetuksen arvoksi muutetaan **Ei**. 

> [!NOTE]
> Loppusaldomerkinnän luominen suljettavalle vuodelle on valinnaista. Se luodaan vain, jos kirjanpitoparametrin **Luo päätöstapahtumat siirron yhteydessä** arvoksi on määritetty **Kyllä**. Alkusaldomerkintä luodaan aina, koska se on seuraavan vuoden alkusaldo.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Kirjanpito: mitä eroa on tilinpäätöksen kumoamis- ja sulkemisparametreilla?
Joillekin voi aiheuttaa hämmennystä, mitä eroa on parametreilla **Kumoa edellinen sulkeminen**, joka sijaitsee **Tilikauden lopetus** ‑valintaikkunassa, ja **Poista päätöstapahtumat siirron yhteydessä**, joka on kirjanpidossa (**Kirjanpito > Kauden sulkeminen > Tilikauden lopetus > Suorita tilikauden lopetus**).  

[![Tilinpäätöksen kumoamis- ja sulkemisparametrien välinen ero.](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Valitsemalla tilinpäätöksen suorittamisen yhteydessä avattavasta valikosta **Kumoa edellinen sulkeminen** voit poistaa kaikki loppusaldo- ja alkusaldomerkinnät, ikään kuin tilinpäätöstä ei olisi missään vaiheessa suoritettu. Tositteet poistetaan. Tilinpäätöstä ei suoriteta uudelleen automaattisesti. Tilinpäätöksen suorittamiseksi tämä prosessi on aloitettava uudelleen siten, että **Kumoa edellinen sulkeminen** ‑asetuksen arvoksi muutetaan **Ei** (**Kirjanpito > Kirjanpidon asetukset > Kirjanpitoparametrit**). 

[![Kirjanpidon parametrin määrittäminen.](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Kirjanpidon **Poista päätöstapahtumat siirron yhteydessä** ‑parametria käytetään vain suoritettaessa (ei kumottaessa) tilinpäätöstä (**Kumoa edellinen sulkeminen** ‑asetukseksi on määritetty **Ei**). Jos parametrin arvoksi määritetään **Kyllä**, kaikki loppusaldo- ja alkusaldomerkinnät poistetaan ja tilinpäätös suoritetaan uudelleen. Tätä prosessia käytetään, kun organisaatio haluaa kirjata kaikki tapahtumat, mukaan lukien edellisen tilinpäätöksen jälkeiset oikaisut, yhteen kirjanpitomerkintään loppusaldo- ja alkusaldomerkinnöissä. 

Jos tämän asetuksen arvoksi määritetään **Ei**, kaikki loppusaldo- ja alkusaldomerkinnät säilyvät. Niitä ei poisteta. Sen sijaan luodaan uusi loppusaldo- ja alkusaldomerkintä pelkästään erotukselle eli kyseisen tilikauden uusille, edellisen tilinpäätöksen jälkeen kirjatuille tapahtumille.  

> [!NOTE]
> Loppusaldomerkintä luodaan suljettavalle vuodelle. Näin tapahtuu vain, jos kirjanpidon parametrin **Luo päätöstapahtumat siirron yhteydessä** arvoksi on määritetty **Kyllä**. Alkusaldomerkintä luodaan aina, koska se on seuraavan vuoden alkusaldo. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Kirjanpito: mitä muutoksia voi tehdä tilinpäätöksen käsittelyn suorituskyvyn parantamiseksi? 
Voit tehdä useita muutoksia, jotka parantavat tilinpäätöksen käsittelyn suorituskykyä. Suosittelemme, että arvioit näiden ehdotettujen muutosten sopivuuden organisaatiollesi.  

### <a name="dimension-sets"></a>Dimensioyhdistelmät
Tilinpäätöksen suorittamisen yhteydessä kunkin dimensioyhdistelmän saldo muodostetaan uudelleen, mikä vaikuttaa suoraan suorituskykyyn. Jotkin organisaatiot luovat tarpeettomasti dimensioyhdistelmiä vain, koska niitä on jossain vaiheessa käytetty tai niitä saatettaisiin jossain vaiheessa käyttää.  Nämä tarpeettomat dimensioyhdistelmät muodostetaan edelleen uudelleen tilinpäätöksen yhteydessä, mikä pidentää käsittelyaikaa. Käy dimensioyhdistelmäsi läpi, arvioi ne ja poista mahdolliset turhat dimensioyhdistelmät.

Tarpeettomat dimensioyhdistelmät vaikuttavat myös **BudgetDimensionFocusInitializeBalance**-erätyöhön (**Kirjanpito > Tilikartta > Dimensiot > Taloushallinnon dimensioyhdistelmät**).

[![Taloushallinnon dimensioyhdistelmät.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Tilinpäätösmallin määritykset
Tilinpäätösmallin avulla organisaatio voi valita ylläpidettävän taloushallinnon dimension tason siirtäessään tulossaldoja jakamattomiin voittoihin. Asetusten avulla organisaatio voi ylläpitää yksityiskohtaisia taloushallinnon dimensioita (**Sulje kaikki**) siirtäessään saldoja jakamattomiin voittoihin tai tehdä summista yhteenvedon yksittäiseen dimensioarvoon (**Sulje yksittäinen**). Tämän voi määrittää kullekin taloushallinnon dimensiolle. Lisätietoja näistä asetuksista on ohjeaiheessa [Tilinpäätös](year-end-close.md).

Suosittelemme arvioimaan organisaation tarpeet ja sulkemaan mahdollisimman monta dimensiota käyttämällä tilinpäätöksen **Sulje yksittäinen** ‑vaihtoehtoa suorituskyvyn parantamiseksi. Kun sulkeminen tapahtuu yksittäiseen dimensioarvoon (joka voi olla myös tyhjä arvo), järjestelmä laskee vähemmän yksityiskohtaisia tietoja määrittäessään jakamattomien voittojen tilivientien saldoja.

### <a name="10013-update-or-later"></a>10.0.13-päivitys tai uudempi
Jos olet tehnyt päivityksen versioon 10.0.13 tai sitä uudempaan versioon sen jälkeen, kun organisaatiosi on viimeksi suorittanut tilinpäätöksen, tilinpäätösprosessi voi kestää pidempään [HashV2-ominaisuuden käyttöönoton](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2) vuoksi. (Termi *hash* eli hajautusarvo viittaa kenttään, joka lasketaan muista merkkijonokentistä. GUID-hajautusarvon laskemiseen käytettävä ohjelmointirajapinta päivitettiin suojauksen parantamiseksi.) Tilinpäätöksen käsittelyn nopeuttamiseksi suosittelemme muodostamaan dimensioyhdistelmien saldot uudelleen ennen tilinpäätöksen suorittamista. Jos olet jo muodostanut dimensioyhdistelmien saldot uudelleen 10.0.13-päivityksen jälkeen, uudelleenmuodostusta ei tarvitse enää tehdä uudelleen.
 
## <a name="general-ledger--what-does-the-period-close--year-end-close-do"></a>Kirjanpito – mitä Kauden sulkeminen – Tilikauden lopetus ‑ominaisuus tekee?
 
[![Kauden sulkeminen, tilikauden lopetus.](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets-new-feature"></a>Taloushallinnon dimensioyhdistelmien uudelleenmuodostuksen suorituskykyparannukset (uusi ominaisuus)
Versioon 10.0.16 lisätty uusi ominaisuus parantaa tilinpäätös- ja konsolidointiprosessien suorituskykyä. Ominaisuuden nimi on ”Taloushallinnon dimensioyhdistelmien uudelleenmuodostuksen suorituskykyparannukset”. Tämä ominaisuus muuttaa dimensioyhdistelmien uudelleenmuodostustapaa niin, että ne muodostetaan uudelleen vain olennaisen aikavälin ajaksi. Edellisissä versioissa dimensioyhdistelmät muodostettiin uudelleen kaikille päivämäärille. Jos olet esimerkiksi sulkemassa vuotta 2020, järjestelmä muodostaa uudelleen vain tilikauden 2020 tapahtumien saldot. Jos olet suorittamassa konsolidointia päivämäärävälille 1.11.2020–30.11.2020, järjestelmä muodostaa uudelleen vain kyseisen päivämäärävälin saldot.

Koska tämä ominaisuus katsotaan tärkeäksi muutokseksi, sinun on otettava se käyttöön käyttämällä **Ominaisuuksien hallinta** ‑työtilaa.
 
[![Tilikauden lopetus.](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2020"></a>Ostoreskontra: mitä muutoksia vuodelle 2020 on tehty vuoden lopun 1099-raportoinnin tueksi?

Vuonna 2020 on lisätty kaksi uutta säädöksiin liittyvää ominaisuutta vuoden lopun 1099-raportointia varten. Ensimmäinen ominaisuus, **Ota 1099-NEC- ja 1099-MISC-lomakkeiden muutokset käyttöön vuodelle 2020**, julkistettiin vuoden puolivälissä pakollisena ominaisuutena. Sen tarkoitus on varmistaa, että vuoden 2020 1099-tapahtumatietoja voidaan seurata uutta 1099-NEC-lomaketta varten. Tämä ominaisuus lisäsi uuden 1099-NEC:n tueksi tarvittavat 1099-kentät sekä päivitti 1099-MISC-kentät. Tämä päivitys päivitti myös toimittajatietueen tiedot 1099-ruutuun. 

Toinen säädöksiin liittyvä ominaisuus, **1099-raporttien päivitys vuoden 2020 verolakia varten**, sisältää seuraavat muutokset.

- 1099-OID – IRS on muuntanut lomakkeen jatkuvaan käyttöön soveltuvaksi.
   - Raportointivuoden 3. ja 4. numero on täytettävä tulostettaessa. Käytä **Raportointivuosi**-kentän 3. ja 4. numeroa **Valmisteveron (1099) tulostusvalinnat** ‑lomakkeesta. 

- 1099-NEC – uusi lomake vuodelle 2020. Tähän kirjataan muun kuin työntekijän kompensaatio. 

-   1099-MISC – lomakkeen 1099-NEC luomisen johdosta Yhdysvaltain verovirasto IRS on muuttanut lomaketta 1099-MISC ja järjestänyt tiettyjen tulojen raportoinnin ruutunumerot uudelleen.
Tulojen raportointiin ja lomakkeen ruutunumeroihin tehdyt muutokset on lueteltu alla.
   - Maksajalla on suoraa myyntiä vähintään 5 000 $ (valintaruutu) ruudussa 7.
   - Satovakuutuksen tuotto ilmoitetaan ruudussa 9.
   - Bruttotuotot asianajajalle ilmoitetaan ruudussa 10.
   - Osion 409A lykkäykset ilmoitetaan ruudussa 12.
   - Hyväksymättömät lykätyt kompensaatiotulot ilmoitetaan ruudussa 14.
   - Ruuduissa 15, 16 ja 17 ilmoitetaan pidätetyt osavaltion verot, osavaltion tunnusnumero ja osavaltiosta saadut tulot.

- Lomakkeisiin 1099-DIV ja 1099-INT ei tullut muutoksia vuodelle 2020.

- Sähköiset ilmoitukset – muotoa on muutettu uutta NEC-lomaketta varten ja MISC-lomakkeeseen on tehty edellä kuvatut muutokset. Lisätietoja sähköisten ilmoitusten vaatimuksista on [IRS:n julkaisussa 1220](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Ostoreskontra: 1099 – kuinka muutan sellaisen toimittajan 1099-ruutua ja -arvoja, joka ei ole seurannut 1099-tietoja koko vuoden ajan?
Käytä Päivitä valmistevero ‑toimintoa (**Ostoreskontra > Toimittajat > Kaikki toimittajat > Valitse toimittaja > Toimittaja-välilehti valintanauhassa > Päivitä valmistevero**), jos haluat käydä aiemmin maksetut laskutapahtumat läpi ja määrittää 1099-tiedot uudelleen **Toimittaja**-sivun **Valmistevero (1099)** ‑välilehden asetusten mukaisesti.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Voinko suorittaa Päivitä valmistevero (1099) ‑toiminnon kaikille toimittajille yhdellä kertaa?
Et voi. Päivitä valmistevero (1099) ‑toiminto suoritetaan yhdelle toimittajalle kerrallaan. Jos organisaatiollasi on tällainen tarve, äänestä ideaa [Toimittajan 1099-tietojen päivittämisen eräprosessi](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-vs-update-all-in-the-update-1099-utility"></a>Ostoreskontra: 1099 – Päivitä valmistevero ‑työkalun vaihtoehdot ”Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen” ja ”Päivitä kaikki”.
**Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen** -valintaruutu palauttaa 1099-summan maksettujen arvojen kokonaissummaksi, kun sitä käytetään yhdessä **Päivitä kaikki** ‑valintaruudun kanssa. 

[![Valmisteverotapahtumat (1099): ennen päivitysrutiinin suorittamista.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

**Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen** ‑valintaruutu tulee käyttöön vain, kun laskussa on osa osittaisia 1099-arvoja tai jos sitä on muutettu Valmistevero (1099) ‑lomakkeessa. Oletetaan esimerkiksi, että sinulla on lasku, jonka arvo on 1 000,00 $, mutta käyttäjä kirjoittaa laskulle manuaalisesti 1099-summan 500,00 $.

[![Valmisteverotapahtumat: sekä Päivitä kaikki- että Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen ‑valintaruutujen valitseminen.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Kun tämä maksetaan, maksettava 1099-summa on 500,00 $. Jos suoritat uudelleenlaskentarutiinin, järjestelmä muuttaa 1099-summaksi 1 000,00 $, joka on maksettu kokonaissumma.

[![Valmisteverotapahtumat: 1099-rutiinin suorittamisen jälkeen.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Ostoreskontra: 1099 – 1099-tapahtumien luominen manuaalisesti
Organisaation voi olla tarpeen luoda manuaalisesti 1099-tapahtumia, joita ei ole liitetty laskuun. Voit lisätä 1099-tapahtumia manuaalisesti valitsemalla **Ostoreskontra > Kausittaiset tehtävät > Valmistevero (1099) > Toimittajien tilitykset valmisteveroja (1099) varten**. Valitse **Manuaaliset 1099-tapahtumat** -painike. 

Manuaalisesti luotuja 1099-tapahtumia ei päivitetä **Päivitä kaikki** -prosessilla tai **Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen** ‑prosessilla **Päivitä valmistevero** ‑työkalussa.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Ostoreskontra: 1099 – tukeeko Dynamics 365 Finance 1096-lomaketta? 

Dynamics 365 Finance ei tulosta 1096 Annual Summary and Transmittal of US Information Returns -lomaketta.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Ostoreskontra: 1099 – onko uusia ominaisuuksia, jotka tukevat julkisen sektorin 1099-raportointia? 
Ratkaisuun on lisätty uusi julkisen sektorin ominaisuus **Päivitä 1099-tiedot päätilin mukaan**, jonka voit ottaa käyttöön **Ominaisuuksien hallinta** ‑työtilassa. Tämän ominaisuuden avulla voit liittää toimittajan 1099-arvot kirjanpidollisen jaon päätilin mukaan toimittajatietueen oletustilin sijaan.

Lisätietoja on ohjeaiheessa [1099-raportoinnin toimittajien asetukset](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
