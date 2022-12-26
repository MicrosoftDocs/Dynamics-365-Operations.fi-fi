---
title: Tilinpäätöstehtävien usein kysytyt kysymykset
description: Tässä artikkelissa on lueteltu kysymyksiä, joita tilinpäätöksen yhteydessä voi ilmetä, sekä niiden vastaukset, joista voi olla apua tilinpäätöstehtävissä.
author: moaamer
ms.date: 12/01/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2e33c1dcbfa4da74f2e8acc6e29f04fda3abd185
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853037"
---
# <a name="year-end-activities-faq"></a>Tilinpäätöstehtävien usein kysytyt kysymykset 

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on lueteltu kysymyksiä, joita tilinpäätöksen yhteydessä voi ilmetä, sekä niiden vastaukset, joista voi olla apua tilinpäätöstehtävissä. Tämän artikkelin tiedot koskevat ensisijaisesti kirjanpidon ja ostoreskontran tilinpäätöstehtäviä.

## <a name="general-ledger-year-end-enhancements"></a>Kirjanpidon tilinpäätöksen parannukset

Microsoft Dynamics 365 Financen versio 10.0.20 sisältää tilinpäätöksen parannuksen. Tämä parannus on oletusarvoisesti käytössä versiosta 10.0.25 alkaen ja pakollinen versiosta 10.0.29 alkaen. Jos organisaatiossa on käytössä aikaisempi versio kuin 10.0.25, suosittelemme ottamaan tämän ominaisuuden käyttöön ennen tilinpäätösprosessin aloittamista. Ennen kuin voit käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat **Ominaisuuksien hallinta** ‑työtilassa tarkistaa ominaisuuden tilan sekä ottaa sen käyttöön tarvittaessa. Työtilassa ominaisuus näkyy seuraavalla tavalla:

- **Moduuli:** Kirjanpito
- **Ominaisuuden nimi:** Kirjanpidon tilinpäätöksen parannukset

Tilinpäätösmallien asetukset on siirretty uudelle asetussivulle: **Tilinpäätösmallin asetukset**. Aiempi tilinpäätössivu muuttuu samantapaiseksi kuin **kirjanpidon ulkomaanvaluutan uudelleenarvostuksen** sivu, eli siinä näytetään luettelo aina, kun tilinpäätös suoritetaan tai peruutetaan. Sivulla ei näy historiallisia tietoja tilinpäätöksistä, jotka on tehty ennen ominaisuuden ottamista käyttöön. Kirjanpitäjä voi aloittaa tilinpäätöksen uudelta sivulta.

Voit peruuttaa tilinpäätöksen valitsemalla kyseisen yrityksen viimeisimmän tilikauden ja valitsemalla sitten **Peruuta tilinpäätös**. Peruutus poistaa edellisen tilinpäätöksen kirjanpitomerkinnät, eikä tilinpäätöstä suoriteta uudelleen automaattisesti. Jos otat **Kirjanpidon tilinpäätöksen parannukset** ‑ominaisuuden käyttöön tilinpäätöksen valmistumisen jälkeen ja haluat peruuttaa historialliset tilinpäätöksen tulokset, suorita historiallinen tilinpäätös uudelleen sen jälkeen, kun olet ottanut käyttöön **Poista olemassa olevat tilinpäätösmerkinnät, kun tilinpäätös tehdään uudelleen** ‑kirjanpitoparametrin.

Voit suorittaa tilinpäätöksen uudelleen aloittamalla prosessin tilikaudelle ja yritykselle uudelleen. Prosessi käyttää edelleen kirjanpidon parametriasetusta sen määrittämiseen, otetaanko tilinpäätöksen uudelleen suorittamisessa huomioon vain uudet ja muuttuneet tapahtumat vai peruutetaanko edellinen tilipäätös kokonaan, jolloin prosessi suoritetaan uudelleen kaikille tapahtumille.

## <a name="general-ledger-the-general-ledger-year-end-enhancements-feature-is-enabled-why-cant-i-view-my-previous-year-closings-in-the-history-section-of-the-year-end-close-page"></a>Kirjanpito: Kirjanpidon tilinpäätöksen parannukset ‑ominaisuus on käytössä. Miksi en voi tarkastella aiempia tilinpäätöksiä Tilinpäätös-sivun Historia-osassa?

Ennen **Kirjanpidon tilinpäätöksen parannukset** ‑ominaisuuden käyttöönottoa järjestelmä seuraa edellisen tilinpäätösprosessin suorituksen päivämäärää ja aikaa. Jokaisen tilinpäätöksen suorituskerran historiaa ei seurata. Näin ollen kunkin tilinpäätöksen suorituksen tiedot eivät ole näytettävissä. Kun ominaisuus on otettu käyttöön, seuraavien tilinpäätösprosessien tietoja ylläpidetään. Tositteita kaikista aiemmista tilinpäätösprosesseista – myös ennen ominaisuuden käyttöönottoa suoritetuista – voi tarkastella **Tositetapahtumat**-sivulla. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-cant-be-run-because-one-or-more-ledger-transactions-posted-into-the-fiscal-year-that-you-are-closing-were-settled-to-a-ledger-transaction-in-a-different-fiscal-year-what-does-this-error-mean"></a>Kirjanpito: tilinpäätösprosessi epäonnistuu seuraavan virheen vuoksi: ”Tilikauden sulkemista ei voi suorittaa, koska vähintään yksi suljettavan tilikauden aikana kirjattu kirjanpitotapahtuma täsmäytettiin kirjanpitotapahtumaan eri tilikaudella.” Mitä tämä virhe tarkoittaa?

Koska **Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä** ‑ominaisuus on käytössä, vain suljettavana olevan tilikauden selvitetyt kirjanpitotapahtumat jätetään pois alkusaldosta. Tämä toiminta aiheuttaa sen, että debet- ja kreditsaldot eivät täsmää. Lisätietoja on kohdassa [Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä](awareness-between-ledger-settlement-year-end-close.md).

## <a name="general-ledger-reversal-of-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-for-112022-cant-be-reversed-because-beginning-balance-transaction-have-been-ledger-settled-in-fiscal-year-112023-what-does-this-error-mean"></a>Kirjanpito: tilinpäätösprosessin peruuttaminen epäonnistuu seuraavan virheen vuoksi: ”Tilikauden 1.1.2022 tilinpäätöstä ei voi palauttaa, koska alkusaldon tapahtumat on selvitetty kirjanpitoon tilikautena 1.1.2023.” Mitä tämä virhe tarkoittaa?

Koska **Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä** ‑ominaisuus on käytössä, tilinpäätösprosessien peruutukset eivät ole sallittuja, jos avaustapahtumat on selvitetty uudella tilikaudella. Peruuta uuden tilikauden 2023 kirjanpidon selvitys, ennen kuin peruutat 1.1.2022 tilinpäätöksen. Vaihtoehtoisesti voi sulkea tilikauden 1.1.2022, mutta vain uusien oikaisevien merkintöjen osalta. Jos haluat sulkea tilikauden vain oikaisujen osalta, poista **Poista olemassa olevat tilinpäätösmerkinnät, kun tilinpäätös tehdään uudelleen** ‑kirjanpitoparametrin valinta.

## <a name="general-ledger-why-isnt-the-ledger-settlement-automation-processing-decembers-ledger-settlement-transactions"></a>Kirjanpito: miksei kirjanpidon selvityksen automaatio käsittele joulukuun kirjanpidon selvitystapahtumia?

**Kirjanpidon selvitysten automatisointi** ‑ominaisuus suorittaa automaation tapahtumille, joiden päivämäärä on tilikauden ensimmäisen päivän ja kuluvan päivän eli esiintymän suorituspäivämäärän välillä. Jos tilikausi päättyy 31. joulukuuta, sinun on ehkä muutettava esiintymän suorituspäivämäärää varmistaaksesi, että se suoritetaan joulukuun aikana. Oletetaan esimerkiksi, että automaatio on määritetty suoritettavaksi joka kuukauden ensimmäisenä päivänä. Tämä automaatio suoritetaan 1.12.2022, ja se on ajoitettu suoritettavaksi 1.1.2023. Päivämäärän 1.1.2023 esiintymää on suositeltavaa muuttaa siten, että se suoritetaankin 31.12.2022. Tällä muutoksella varmistetaan, että automaattisessa selvityksessä otetaan huomioon joulukuun 2. ja 31. päivän välille päivätyt tapahtumat.

## <a name="general-ledger-whats-the-difference-between-the-reverse-year-end-close-action-and-the-delete-existing-year-end-entries-when-reclosing-parameter-for-year-end-close"></a>Kirjanpito: mitä eroa on Peruuta tilinpäätös ‑toiminnolla ja Poista olemassa olevat tilinpäätösmerkinnät, kun tilinpäätös tehdään uudelleen ‑parametrilla?

Joillekin voi aiheuttaa hämmennystä, mitä eroa on **Peruuta tilinpäätös** ‑toiminnolla ja kirjanpidon **Poista olemassa olevat tilinpäätösmerkinnät, kun tilinpäätös tehdään uudelleen** ‑parametrilla (**Kirjanpito \> Kirjanpidon asetukset \> Kirjanpitoparametrit**).

Valitsemalla tilinpäätöksen suorittamisen yhteydessä **Peruuta tilinpäätös** ‑toiminnon voit poistaa kaikki loppusaldo- ja alkusaldomerkinnät, ikään kuin tilinpäätöstä ei olisi missään vaiheessa suoritettu. Tässä tapauksessa tositteet poistetaan. Tilinpäätöstä ei suoriteta uudelleen automaattisesti. Voit suorittaa tilinpäätöksen valitsemalla **Tee tilinpäätös** ‑toiminnon.

Kirjanpidon **Poista olemassa olevat tilinpäätösmerkinnät, kun tilinpäätös tehdään uudelleen** ‑parametria käytetään vain tilinpäätöstä tehdessä (ei peruutettaessa sitä). Jos parametrin arvoksi määritetään **Kyllä**, kaikki loppusaldo- ja alkusaldomerkinnät poistetaan ja tilinpäätös suoritetaan uudelleen. Tätä vaihtoehtoa käytetään, kun organisaatio haluaa kirjata kaikki tapahtumat, mukaan lukien edellisen tilinpäätöksen jälkeiset oikaisut, yhteen kirjanpitomerkintään loppusaldo- ja alkusaldomerkinnöissä. Jos parametrin arvoksi määritetään **Ei**, kaikki loppusaldo- ja alkusaldomerkinnät säilyvät. Niitä ei poisteta. Sen sijaan luodaan uusi loppusaldo- ja alkusaldomerkintä pelkästään erotukselle eli kyseisen tilikauden uusille, edellisen tilinpäätöksen jälkeen kirjatuille tapahtumille.

> [!NOTE]
> Loppusaldomerkintä luodaan suljettavalle vuodelle. Näin tapahtuu vain, jos kirjanpidon parametrin **Luo päätöstapahtumat siirron yhteydessä** arvoksi on määritetty **Kyllä**. Alkusaldomerkintä luodaan aina, koska se on seuraavan vuoden alkusaldo.

## <a name="general-ledger-what-is-the-difference-between-close-all-and-close-single-options-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process"></a>Kirjanpito: mitä eroa on tilinpäätösprosessin Siirrä tulosdimensiot ‑osan Sulje kaikki- ja Sulje yksittäinen ‑vaihtoehdoilla?

**Sulje kaikki** säilyttää alkuperäisen taloushallinnon dimension arvot kirjatuista tapahtumista, ja käyttää niitä alkusaldojen luomiseen säilytettyjen tuottojen tilille. Erilliset kertyneiden tuottojen alkusaldot luodaan jokaiselle yksilölliselle taloushallinnon dimensioarvoyhdistelmälle. Jos valittuna on **Sulje yksittäinen**, kaikki kyseiselle taloushallinnon dimensiolle kirjatut tapahtumat tiivistetään kertyneiden tuottojen alkusaldoksi **Sulje yksittäinen** ‑kentän jälkeen näkyvään kenttään syötetylle dimensioarvolle. 

Oletetaan esimerkiksi, että kaikki tilivuoden tapahtumat on kirjattu Päätili – Osasto ‑tilirakenteella. Mallin taloushallinnon dimensiolle Osasto on valittu **Sulje yksittäinen** ja dimension arvoksi on syötetty 100. Jos kaikkien osastoille 200, 300 ja 400 kirjattujen tapahtumien kokonaisarvo on 100 000 $, Kertynyt tuotto – 100 ‑tilille luodaan yksi alkusaldo. Jos valitset **Sulje yksittäinen**, mutta jätät taloushallinnon dimensioarvon tyhjäksi, kaikki tapahtumat kirjataan kertyneihin tuottoihin ja dimension arvo on tyhjä.

## <a name="general-ledger-when-i-select-close-single-option-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process-will-my-detailed-transactional-information-be-lost"></a>Kirjanpito: kun valitsen Sulje yksittäinen ‑vaihtoehdon tilinpäätösprosessin Siirrä tulosdimensiot ‑osassa, häviävätkö yksityiskohtaiset tapahtumatiedot?

**Sulje kaikki**- ja **Sulje yksittäinen** ‑vaihtoehtojen avulla voit määrittää, mitkä tulostileille kirjattujen tapahtumien taloushallinnon dimensiot siirretään jakamattomien voittojen päätilille. Tämä ei vaikuta tulostilien historiallisiin kirjauksiin, vaan ne säilyvät entisellään. Vaihtoehto vaikuttaa erittelytasoon, joka siirretään jakamattomien voittojen tileille uuden tilikauden alkusaldoksi. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-the-reporting-currency-for-the-year-does-not-balance-what-does-this-mean"></a>Kirjanpito: tilinpäätösprosessi epäonnistuu, koska tilikauden raportointivaluutta ei täsmää. Mitä tämä tarkoittaa?

Tämä virhe voi esiintyä, kun **Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä** ‑ominaisuus (selvittämisominaisuus) on otettu käyttöön. Kun ominaisuus on käytössä, tilitettyjä kirjanpitotapahtumia ei enää sisällytetä seuraavan tilikauden alkusaldoon, kun kirjanpidon tilinpäätös tehdään. Selvitettyjen kirjanpitotapahtumien jättäminen pois voi aiheuttaa haasteita asiakkaille tilinpäätöksessä, jos kirjanpito on määritetty raportointivaluutalla.   
Kirjanpidon selvitys suoritetaan vain kirjanpitovaluutalle.  Kun kirjanpitotapahtumat selvitetään, vahvistuksella varmistetaan vain, että kirjanpitovaluutan debetsaldot täsmäävät kreditsaldojen kanssa. Näiden kirjanpitotapahtumien raportointivaluuttasummia ei vahvisteta, joten niiden debetsaldot eivät ehkä täsmää kreditsaldojen kanssa.  Lisäksi kirjanpidon selvitys ei laske ja kirjaa automaattisesti tuottoja ja tappioita raportointivaluuttana.  Näiden rajoitusten vuoksi tuotto-/tappiotapahtuman on oltava olemassa raportointivaluuttana, kun kirjanpidon selvitys suoritetaan.  Jos tuottoa/tappiota ei sisällytetä kirjanpidon selvitykseen, tilinpäätöksen tuloksena on saldojen täsmäämättömyydestä ilmoittava sanoma.  Lisätietoja on kohdassa [Tietojen selvittäminen kirjanpidon selvityksen ja raportointivaluutan välillä ‑ominaisuus ei täsmää](reporting-currency-yec.md).

## <a name="general-ledger-what-can-be-changed-to-help-enhance-the-performance-of-year-end-processing"></a>Kirjanpito: mitä muutoksia voi tehdä tilinpäätöksen käsittelyn suorituskyvyn parantamiseksi?

Voit tehdä useita muutoksia, jotka parantavat tilinpäätöksen käsittelyn suorituskykyä. Suosittelemme, että arvioit näiden ehdotettujen muutosten sopivuuden organisaatiollesi.

### <a name="optimize-year-end-close-service"></a>Tilinpäätöksen optimointipalvelu

**Optimoi tilikauden lopetus** ‑palvelu auttaa Microsoft Dynamics 365 Finance ‑asiakkaita nopeuttamaan tilinpäätöksen tekemistä siirtämällä raskaat tilinpäätöksen käsittelytoimet mikropalvelulle. Tehokkaan tilinpäätöksen säästämän ajan ansiosta kukin Finance-tiimi voi reagoida ajoissa oikaisutarpeisiin, minkä seurauksena on taloushallinnon raporttien luominen. Käsittelemällä tilinpäätöksen mikropalvelussa voi vapauttaa arvokkaita resursseja. Käsittelyn siirtäminen minimoi SQL Server ‑palvelimen kuormituksen ja antaa asiakkaille mahdollisuuden nopeuttaa tilinpäätöksen käsittelyä.

**Optimoi tilinpäätös** ‑palvelu on käytettävissä versiossa 10.0.31, jotta useammat asiakkaat voivat käyttää uutta palvelua vuoden 2022 tilinpäätöstä varten. Lisäksi palvelu on otettu takautuvasti käyttöön versioissa 10.0.30 ja 10.0.29. Lisätietoja on kohdassa [Tilinpäätöksen optimointi](optimize-year-end-close.md).

### <a name="dimension-sets"></a>Dimensioyhdistelmät

Kun suoritat tilinpäätökset, jokainen dimensioyhdistelmän saldo muodostetaan uudelleen. Tämä toiminta vaikuttaa suoraan suorituskykyyn. Jotkin organisaatiot luovat tarpeettomasti dimensioyhdistelmiä vain, koska niitä on jossain vaiheessa käytetty tai niitä saatettaisiin jossain vaiheessa käyttää. Koska nämä tarpeettomat dimensioyhdistelmät muodostetaan edelleen uudelleen tilinpäätöksen yhteydessä, käsittelyaika pitenee. Käy dimensioyhdistelmäsi läpi, arvioi ne ja poista mahdolliset turhat dimensioyhdistelmät.

Tarpeettomat dimensioyhdistelmät vaikuttavat myös **BudgetDimensionFocusInitializeBalance**-erätyöhön (**Kirjanpito \> Tilikartta \> Dimensiot \> Taloushallinnon dimensioyhdistelmät**).

[![Taloushallinnon dimensioyhdistelmät.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Tilinpäätösmallin määritykset

Tilinpäätösmallin avulla organisaatio voi valita ylläpidettävän taloushallinnon dimension tason siirtäessään tulossaldoja jakamattomiin voittoihin. Asetusten avulla organisaatio voi ylläpitää yksityiskohtaisia taloushallinnon dimensioita (**Sulje kaikki**) siirtäessään saldoja jakamattomiin voittoihin tai tehdä summista yhteenvedon yksittäiseen dimensioarvoon (**Sulje yksittäinen**). Tämän voi määrittää kullekin taloushallinnon dimensiolle. Lisätietoja näistä asetuksista on artikkelissa [Tilinpäätös](year-end-close.md).

Suosittelemme arvioimaan organisaation tarpeet ja sulkemaan mahdollisimman monta dimensiota käyttämällä tilinpäätöksen **Sulje yksittäinen** ‑vaihtoehtoa suorituskyvyn parantamiseksi. Kun sulkeminen tapahtuu yksittäiseen dimensioarvoon (joka voi olla myös tyhjä arvo), järjestelmä laskee vähemmän yksityiskohtaisia tietoja määrittäessään jakamattomien voittojen tilivientien saldoja.

### <a name="degenerate-dimensions"></a>Johdetut dimensiot

Johdetulla dimensiolla ei ole juurikaan uudelleenkäyttöarvoa itsenäisesti eikä yhdessä muiden dimensioiden kanssa. Johdettuja dimensioita on kahta eri tyyppiä. Ensimmäinen tyyppi on yksittäin johdettu dimensio. Tavallisesti tämäntyyppinen degeneroitu dimensio näkyy vain yksittäisessä tapahtumassa tai pienissä tapahtumajoukoissa. Toinen tyyppi on dimensio, joka muuttuu johdetuksi yhdessä yhden tai useamman sellaisen muun dimension kanssa, joka ilmentää samoja mahdollisuuksia mahdollisten luotavien permutaatioiden perusteella. Johdetulla dimensiolla voi olla merkittävä vaikutus tilinpäätösprosessin suorituskykyyn. Voit minimoida suorituskykyongelmat määrittämällä tilinpäätöksen asetuksissa kaikille johdetuille dimensioille **Sulje yksittäinen** ‑asetuksen edellisessä osassa kuvatulla tavalla.

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2022"></a>Ostoreskontra: mitä muutoksia vuodelle 2022 on tehty vuoden lopun 1099-raportoinnin tueksi?

#### <a name="update-to-all-1099-forms"></a>Päivitys kaikkiin 1099-lomakkeisiin

Vuoden 2022 verovuoden kaikkiin 1099-lomakkeisiin on tehty seuraavat muutokset:

- Vuonna 2021 vuosi oli kiinteänä 1099-lomakkeissa. Vuodesta 2022 alkaen raportti täyttää vuositiedon.

#### <a name="1099-misc"></a>1099-MISC

Verovuoden 2022 lomakkeeseen 1099-MISC on tehty seuraavat päivitykset:

- Ruutu 13: näyttää nyt FATCA (Foreign Account Tax Compliance Act) ‑ilmoitusvaatimuksen.
- Rasia 14: käytetään nyt ylimääräisten "kultaisten laskuvarjomaksujen" raportointiin.
- Ruutu 15: käytetään nyt ylimääräistä kompensaation lykkäystä koskevien NQDC (nonqualified deferred compensation) ‑suunnitelmien alaisten maksujen raportointiin.
- Ruutu 16: käytetään nyt osavaltion ennakonpidätysten raportointiin.
- Ruutu 17: käytetään nyt maksajan osavaltionumeron raportointiin.
- Ruutu 18: käytetään nyt osavaltion tuloveron tulojen raportointiin.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Ostoreskontra: 1099 – kuinka muutan sellaisen toimittajan 1099-ruutua ja -arvoja, joka ei ole seurannut 1099-tietoja koko vuoden ajan?

Käytä **Päivitä valmistevero** ‑toimintoa, jos haluat käydä aiemmin maksetut laskutapahtumat läpi ja määrittää 1099-tiedot uudelleen **Toimittaja**-sivun **Valmistevero (1099)** ‑välilehden asetusten mukaisesti. Jos haluat käyttää **Päivitä valmistevero** ‑toimintoa, siirry kohtaan **Ostoreskontra \> Toimittajat \> Kaikki toimittajat**, valitse toimittaja ja valitse sitten **Toimittaja**-välilehden toimintoruudusta **Päivitä valmistevero**.

## <a name="can-i-run-the-update-1099-functionality-for-all-my-vendors-at-once"></a>Voinko suorittaa Päivitä valmistevero (1099) ‑toiminnon kaikille toimittajille yhdellä kertaa?

Voit käyttää **Päivitä useiden toimittajien 1099-tiedot** ‑sivua toimittajatietueen 1099-ruudun päivittämiseen sekä tapahtumien päivittämiseen 1099-ruudun tiedoilla. Voit avata tämän sivun valitsemalla **Ostoreskontra \> Kausittainen tehtävä \> Valmistevero (1099)**. Jotta voit käyttää sivua, sinulla on oltava **Päivitä 1099-ruutu ja tapahtumat useille toimittajille** ‑suojausoikeus.

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Ostoreskontra: 1099 – Päivitä valmistevero ‑työkalun vaihtoehdot ”Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen” ja ”Päivitä kaikki”

**Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen** -valintaruutu palauttaa 1099-summan maksettujen arvojen kokonaissummaksi, kun sitä käytetään yhdessä **Päivitä kaikki** ‑valintaruudun kanssa.

[![Valmisteverotapahtumat (1099): ennen päivitysrutiinin suorittamista.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

**Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen** ‑valintaruutu tulee käyttöön vain, kun laskussa on osa osittaisia 1099-arvoja tai jos laskua on muutettu Valmistevero (1099) ‑lomakkeessa. Oletetaan esimerkiksi, että sinulla on lasku, jonka arvo on 1 000,00 $, mutta käyttäjä kirjoittaa laskulle manuaalisesti 1099-summan 500,00 $.

[![Valmisteverotapahtumat: sekä Päivitä kaikki- että Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen ‑valintaruutujen valitseminen.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Kun tämä lasku maksetaan, maksettava 1099-summa on 500,00 $. Jos suoritat uudelleenlaskentarutiinin, järjestelmä muuttaa 1099-summaksi 1 000,00 $, joka on maksettu kokonaissumma.

[![Valmisteverotapahtumat: 1099-rutiinin suorittamisen jälkeen.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Ostoreskontra: 1099 – 1099-tapahtumien luominen manuaalisesti

Organisaation voi olla tarpeen luoda manuaalisesti 1099-tapahtumia, joita ei ole liitetty laskuun. Voit lisätä 1099-tapahtumia manuaalisesti valitsemalla **Ostoreskontra \> Kausittaiset tehtävät \> Valmistevero (1099) \> Toimittajien tilitykset valmisteveroja (1099) varten**. Valitse **Manuaaliset 1099-tapahtumat** -painike.

Manuaalisesti luotuja 1099-tapahtumia ei päivitetä **Päivitä kaikki** -prosessilla tai **Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen** ‑prosessilla **Päivitä valmistevero** ‑työkalussa.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Ostoreskontra: 1099 – tukeeko Dynamics 365 Finance 1096-lomaketta?

Dynamics 365 Finance ei tulosta 1096 Annual Summary and Transmittal of US Information Returns -lomaketta.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Ostoreskontra: 1099 – onko uusia ominaisuuksia, jotka tukevat julkisen sektorin 1099-raportointia?

Ratkaisuun on lisätty uusi julkisen sektorin ominaisuus **Päivitä 1099-tiedot päätilin mukaan**, jonka voit ottaa käyttöön **Ominaisuuksien hallinta** ‑työtilassa. Tämän ominaisuuden avulla voit liittää toimittajan 1099-arvot kirjanpidollisen jaon päätilin mukaan toimittajatietueen oletustilin sijaan.

Lisätietoja on ohjeaiheessa [1099-raportoinnin toimittajien asetukset](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
