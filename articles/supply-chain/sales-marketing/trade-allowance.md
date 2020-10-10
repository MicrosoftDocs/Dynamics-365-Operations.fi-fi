---
title: Myynninedistämispalkkioiden hallinta
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Supply Chain Managementin myynninedistämispalkkioiden hallintaa.
author: t-benebo
manager: tfehr
ms.date: 08/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: MCRBrokerClaims, MCRBrokerWriteOffReasonPrompt, MCRRoyaltyVendTable, MCRRoyaltyVendTrans, PdsCustRebateGroup, PdsRebateAgreement, TAMCopyTradePromotions, TAMDeduction, TAMDeductionCreate, TAMDeductionDenyReason, TAMDeductionParmDeny, TAMDeductionParmMassUpdate, TAMDeductionParmMatch, TAMDeductionParmSplit, TAMDeductionParmWriteOff, TAMDeductionType, TAMDeductionWriteOffReason, TAMFundManagement, TAMFundUsage, TAMListPage, TAMMarketingObjective, TAMMerchEventType, TAMOneTimePromotion, TAMPromoCompareGraph, TAMPromoStatistic, TAMPromotionAnalysisSummary, TAMPromotionParameters, TAMPromotionPeriod, TAMTemplateListPage, TAMTradePromotionAnalysis, TAMTradePromotions, TAMWhatIfPromotionAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: t-benebo
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 411d815f7f8ed7844c328e83cb3877081a517b06
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830072"
---
# <a name="trade-allowance-management"></a>Myynninedistämispalkkioiden hallinta

[!include [banner](../includes/banner.md)]

Myynninedistämispalkkioiden hallinta auttaa yrityksiä hallitsemaan sellaisia myynninedistämisohjelmia, joissa asiakkaille voidaan tarjota suoritusperäisiä palkkioita määrä- ja toimintatavoitteiden perusteella. Omaisuuden toiminnot on suunniteltu yrityksille, jotka keskittyvät kattaviin voittoon myynninedistämisprosessien kautta hakeviin yrityksiin. Näitä toimintoja ovat myynninedistämisrahoituksen budjetointi ja kohdistus, korvaussopimustenmäärittäminen, vaatimusten luonti ja käsittely, maksujen käsittely ja myynninedistämisen tehokkuuden analysointi.


Tässä ohjeaiheessa käsitellään yleisesti myynninedistämispalkkion hallintaominaisuutta ja tutustutaan tehtäviin, jotka liittyvät yleensä myynninedistämisohjelman hallintaan. Monenlaisten käyttäjätyyppien, joilla on operatiivisia ja päätökseen tekoon liittyviä vastuualueita, odotetaan käyttävän tätä toimintoa tavoitteiden saavuttamiseksi:

- Harkinnanvaraisen rahoituksen kohdistaminen valituille tileille ja kampanjoiden myynninedistämispalkkiosopimusten määrittäminen laskutusalennusten ja kertasummamaksujen (sovitusta palvelusta) perusteella
- Neuvoteltujen kampanjasopimusten käyttäminen meneillään olevassa myynnissä ja laskutusalennusvaatimusten muodostaminen
- Muodostettujen vaatimusten laskeminen, hyväksyminen ja käsitteleminen sekä niiden välittäminen myyntireskontraan vähennyksenä maksun tilitykseen
- Asiakkaan osittaisen maksun täsmäyttäminen erääntyvän vähennyksen kanssa
- Myynninedistämisrahoituksen käytön seuranta sekä ohjelman kannattavuuden ja tehokkuuden arviointi

## <a name="audience-and-purpose"></a>Käyttäjäryhmät ja tarkoitus

Tämän asiakirjan tiedot on tarkoitettu konserniyritysten päätöksentekijöille, kuten ostopäälliköille, talousjohtajille (CFO) ja kirjanpidon päälliköille, joilla on seuraavat vastuut:

- Ylätason budjettien ja rahoituksen kohdistus
- Myyntikampanjoiden suunnittelu ja analysointi
- Laskutusalennusvaatimuksia käsittelevän, myynninedistämistapahtumien perusteella maksuja suorittavan sekä osittaiset maksut ja vähennykset täsmäyttävän henkilöstön hallinta

Näissä rooleissa toimivat henkilöt etsivät tapoja, joilla he saavuttavat seuraavat tavoitteet:

- Markkinointikampanjan varojen käytön tehostaminen
- Erilaisten myynninedistämisohjelmien ja -palkkioiden joustava käyttö
- Vähentää johdon painetta sekä virheitä, jotka liittyvät kampanjoiden suorituskyvyn valvontaan ja vaatimusten käsittelyyn.
- Kassavirtaennusteiden parantaminen jaksottamalla tulevia velkoja
- Arvotetun perusteen käyttö nykyisiä ja tulevia kampanjoita koskevissa neuvotteluissa asiakkaiden kanssa

## <a name="promotional-fund-and-trade-allowance-agreement"></a>Kampanjan rahoitus ja myynninedistämispalkkio

Myynninedistämispalkkiosopimus on kannustinohjelma, jossa suoritusperusteista rahallista palkkiota tarjotaan asiakkaille, jotka saavuttavat tietyt määrään ja/tai toimintaan liittyvät tavoitteet. Kampanjarahoitus on budjetoitu meno. Tällä tavoin myynninedistämiskampanjoita voidaan tarkistaa.

### <a name="promotional-fund"></a>Kampanjan rahoitus

Myynninedistämissopimuksiin kohdistetut varat kirjataan **Varat**-sivulla. Avaa **Varat**-sivu valitsemalla **Myynti ja markkinointi** \> **Myynninedistämispalkkiot** \> **Varat** \> **Varat**.

![Varat-sivu](./media/trade-allowance-management-funds-page.png "Varat-sivu")

Voit tarkastella **Varat**-sivulla kampanjan varojen tietoja.

**Yleiset**-pikavälilehdessä on kausi, jonka rahoitus on voimassa, ja budjetoitu summa. Jotta rajoitus voitaisiin kohdistaa kampanjasopimukseen, **Tila**-kentän arvon on oltava **Hyväksytty**.

**Asiakkaat**-pikavälilehdessä näyttää asiakashierarkian. Voit valita rahoituksen kohteena olevat asiakkaat vetämällä ne kohtaan **Rahoitus - asiakkaat**. Pikavälilehdessä näkee myös, miten rahoituksen kokonaissumma on jaettu.

**Nimikkeet**-pikavälilehdessä on kampanjaan sisältyvät nimikkeet.

### <a name="trade-allowance-agreement"></a>Myynninedistämisen palkkiosopimus

Kun rahoituksen määritys on tehty, kampanjasuunnittelun seuraava vaihe on kampanjasopimusten (joita kutsutaan myynninedistämisen palkkiosopimuksiksi), kohdistaa varat ja määrittää suoritustavoitteet kullekin myynninedistämistapahtumalle.

Myynninedistämisen palkkiosopimuksen kirjataan **Myynninedistämisen palkkiosopimukset** -sivulla. Avaa **Myynninedistämisen palkkiosopimukset** -sivu ja valitse **Myynti ja markkinointi** \> **Myynninedistämispalkkiot** \> **Myynninedistämisen palkkiosopimukset**.

![Myynninedistämispalkkiosopimukset-sivu](./media/trade-allowance-management-agreements-page.png "Myynninedistämispalkkiosopimukset-sivu")

#### <a name="header"></a>Otsikko

Siirry ylätunnistenäkymään valitsemalla **Ylätunniste**.

Määritä **Yleiset**-pikavälilehden **Tilaus - mihin**- ja **Tilaus - mistä** -kenttiin kausi, jonka sopimus on voimassa. Jos sopimuksen hyväksyntätila on **Sisäinen hyväksyntä**, sopimus ei ole vielä voimassa eikä sitä voi käyttää myyntitilauksen käsittelyn aikana.

**Yleiset**-pikavälilehden **Analyysi**-osassa on tärkeitä kenttiä, jotka määrittävät kampanjan arvioinnissa käytettävät määrät ja kustannukset:

- **Perusyksiköt**-kenttä määrittää, kuinka paljon tuotteita on myytävä valituille asiakkaille, ennen kuin kampanjaa käytetään.
- **Laskettu lähetysmäärä** -arvo lasketaan **Nousuprosentti**-arvon perusteella. Tämä luku on kampanjan suunniteltu nousutavoite.
- **Myynninedistämispalkkion kustannus** -kenttä lasketaan myynninedistämisen palkkiosopimuksessa olevien eri tapahtumien määrien perusteella.

**Asiakkaat**-pikavälilehdessä on vasemmalla luettelo, jossa voit valita ja tarkastella asiakasryhmiä. Nämä ryhmät on määritetty valmiiksi hierarkioiksi. Voit valita palkkiosopimuksen kohteeksi koko hierarkian tai tiettyjä tilejä.

**Nimikkeet**-pikavälilehdellä samalla tavoin kuin **Varat**-sivun **Nimikkeet**-pikavälilehdellä tuotteita lisätään sopimukseen, ja tällä tavoin sen myynti liitetään sovittuun palkkioon.

Voit tarkastella **Varat**-pikavälilehdessä tähän sopimukseen liitettyjä kampanjarahoitusta. Voit tarkastella myös sopimuksen tapahtuman kustannusten kohdistusta. Jos tapahtuman kustannusten kohdistus on 100 prosenttia, kyseinen kampanja rahoitetaan kokonaisuudessaan samasta lähteestä. Kampanjasopimus voi vaihtoehtoisesti saada rahoitusta useista lähteistä, ja käytettävä kohdistusprosessi voi olla yhtä suuri tai erottava.

#### <a name="lines"></a>Rivejä

Siirry rivinäkymän valitsemalla seuraavaksi **Rivit**.

**Myynninedistämistapahtumat**-välilehdessä on näkyvissä sopimukseen kuuluvat tapahtumatyypit. Tapahtumatyyppejä on kolme: laskualennus, kokonaissumma ja laskun ulkopuolinen alennus.

Kun valitse myynninedistämistapahtuman ja **Summat**-välilehden, tapahtuman tiedot ovat näkyvissä.

![Myynninedistämispalkkiosopimuksen rivit](./media/trade-allowance-management-agreements-lines.png "Myynninedistämispalkkiosopimuksen rivit")

**Myynninedistämispalkkiorivit**-osassa määritetään määrä- tai summa-alueet, jotka asiakkaan on määritysten mukaan saavutettava palkkion saadakseen.

Jos myynninedistämistapahtuman tyyppi on **Laskualennus**, **Summat**-välilehden yläosassa on määritetty säännöt, joiden mukaan laskualennusta käytetään ja se muodostetaan ja maksetaan. Säännöt voivat esimerkiksi määrittää seuraavat ehdot laskualennusvaatimukselle:

- Se perustuu myyntitilauksen luontipäivään (**Laskentapäivätyyppi**-arvo on **Luotu**).
- Se lasketaan myyntilausrivin alennuksia edeltävän summan eikä nettosumman perusteella, sillä nettosumma sisältää asennukset (**Oton lähde** -arvo on **Brutto**).
- Se perustuu myytyjen tuotteiden määrään eikä summaan (**Ostohyvitysrivin vaihtotyyppi** -arvo on **Määrä**).
- Se lasketaan kuukauden jaksona (**Myynnin kumulointiperuste** -arvo on **Kuukausi**). 
- Se selvitetään vähennyksen eikä ostoreskontraa käyttämällä (**Maksutyyppi**-arvo on **Asiakkaan vähennykset**).

Jos myynninedistämistapahtuman tyyppi on **Kokonaissumma**, **Summat**-välilehdessä on näkyvissä määrä, joka maksetaan asiakkaalle vähennyksinä, kun asiakas saavuttaa tietyn suoritustavoitteen. Jos hyväksynnän tila on **Avoin**, kokonaissummaa ei ole vielä maksettu.

Jotta sopimusta voisi soveltaa myyntitilauksessa, jotka käyttävät sopimuksen ehdot, sopimuksen tilan on oltava **Vahvistettu**. 

## <a name="perform-sales-under-the-planned-merchandising-event-and-generate-bill-back-claims"></a>Myynnin toteuttaminen suunnittelussa myynninedistämistapahtumassa ja laskualennusvaatimusten muodostaminen

Kun luot myyntitilauksen, jossa on sopimuksen vaatimukset täyttäviä rivejä, voit tarkastella liittyviä tietoja **Myyntitilaus**-sivulla valitsemalla **Myyntitilausrivi** \> **Näytä** \> **Hintatiedot**.

Myyjä näkee **Hintatiedot**-sivun **Ostohyvitykset**-pikavälilehdessä voimassaolevan myynninedistämisen palkkiosopimuksen laskualennuksen (ostohyvitysohjelman tunnus on näkyvissä) ja rivillä käytetyn kokonaissumman. Tämä summa näkyy myös **Ostohyvityksen summa** -kentässä **Hintatiedot**-sivun **Marginaaliarvio**-osassa.

Kun myyntilasku on kirjattu, vastaava laskutusalennusvaatimus muodostetaan kullekin laskuriville.

> [!NOTE]
> Voit avata **Hintatiedot**-sivun valitsemalla **Myyntireskontran parametrit** -sivun **Hinnat**-välilehdessä **Ota käyttöön hintatiedot** -valintaruutu. I

## <a name="process-claims-and-pass-them-as-deductions-to-ar"></a>Vaatimusten käsittely ja välittäminen vähennyksinä myyntireskontraan

Laskualennusten käsittelyn seuraava vaihe on vaatimusten tarkastelu, laskeminen ja hyväksyminen sekä niiden muuntaminen vähennyksiksi.

Laskualennuksen työtila on paikka, jossa kampanjasopimuksen omistaja voi säännöllisesti arvioida ja käsitellä muodostetut vaatimukset. Lisäksi myyntireskontran järjestelmänvalvoja muuntaa siellä hyväksytyt vaatimukset vähennyksiksi tai tavallisiksi laskuiksi vaatimuksen maksutavan perusteella.

Voit tarkastella vaatimuksen rivejä **Laskutusalennuksen työtila** -sivulla. Jos vaatimusten tila on **Laskettava uudelleen**, vaatimuksen on laskettava uudelleen mahdollisen kumulatiivisen vaikutuksen vuoksi.

### <a name="recalculate-claims"></a>Vaatimusten laskeminen uudelleen

Voit laskea vaatimukset uudelleen valitsemalla toimintoruudussa **Kumuloi**. Valitse sitten **Kumuloi ostohyvitykset** -valintaikkunassa asiakas.

Uudelleenlaskennan vuoksi ohjelma muodostaa summille uudet vaatimukset ja oikaisee tällä tavoin alkuperäiset vaatimukset yksikkökohtaisista hyväksyttävistä summista. Jokaiselle yksilöivälle asiakas-, nimike-, valuutta-, mittayksikkö-, varastodimensio-, taloushallinnon dimensio- ja arvonlisäveroryhmäyhdistelmälle muodostetaan yksi oikaisuvaatimus. Näissä oikaisuvaatimuksissa on sama viittaus myyntitilauksen ja laskun numeroon kuin oikaistavissa vaatimuksissa (eli vaatimuksissa, jota luotiin alun perin myyntiasiakirjasta). Alkuperäisestä vaatimuksesta poiketen oikaisuvaatimuksessa ei ole alkuperäisen myyntitilausrivin summia ja määrää kuvaavien kenttien arvoja.

Kun uudelleenlaskenta on valmis, vaatimuksen tilaksi muutetaan **Laskettu**. Voit hyväksyä vaatimuksen valitsemalla toimintoruudussa **Hyväksy**.

### <a name="process-claims-and-pass-them-to-ar"></a>Vaatimusten käsittely ja välittäminen myyntireskontraan

Vaatimukset voi nyt käsitellä myyntireskontrassa. Voit käsitellä ne valitsemalla toimintoruudussa **Käsittele**. 

Kun vaateet on käsitelty, niiden tilaksi on muuttunut **Merkitse**, mikä ilmaisee, että kirjauskansion kirjaus (kirjaus tehdään ostohyvityksen jaksotuskirjauskansioon myyntireskontran parametrimääritysten mukaisesti) on aiheuttavat seuraavat tapahtumat: 

- Vaatimukset on siirretty asiakkaan väliaikaiseen saldoon vähennyksinä.
- Ostohyvityksen jaksotuskirjauskansiota on hyvitetty ilmaisemaan tulevaa velkaa asiakkaalle
- Ostohyvityksen kulutiliä on veloitettu osoituksena myyntiin liittyvistä kustannuksista.

Myyntireskontran työntekijän on nyt viimeisteltävä prosessi käsittelemällä jaksotusvähennykset siirtämällä ne asiakkaan saldoon hyvityslaskuna (velka). 

Aloita tehtävä valitsemalla toimintoruudun **Asiakas**-sivulla **Perintä** \> **Selvitä tapahtumat**. Valitse sitten **Selvitä tapahtumat** -sivulla **Toiminnot** \> **Laskutusalennusohjelma**. Ostohyvityssivulla on näkyvissä kaikki aiemmin käsitellyt laskutusalennusvaatimukset.

Jos haluat luoda hyvityslaskun, valitse kaikilla riveillä **Merkitse**-valintaruutu ja valitse sitten **Toiminnot** \> **Luo hyvityslasku**.

Kirjauskansio kirjataan hyvityslaskun luomisen yhteydessä. (Kirjattava kirjauskansio on myyntireskontran parametreissa määritetty Myyntireskontran kulutuksen kirjauskansio). Tämän vuoksi varsinainen velkasumma (hyvitys) on siirretty asiakkaan saldoon. Tämä tilanne tarkoittaa, että seuraavat tapahtumat ovat tapahtuneet:

- Asiakkaan myyntisaamisten tiliä on hyvitetty.
- Ostohyvityksen jaksotustiliä on veloitettu.

Voit hyväksyä myynninedistämistapauksen **Kokonaissumma**-tyypin valitsemalla tapahtuman **Myynninedistämisen palkkiosopimukset** -sivulla ja valitsemalla sitten **Summa**-välilehdessä **Hyväksy**.

## <a name="settle-the-deduction-that-is-due-and-the-customer-short-pay-by-using-the-deduction-workbench"></a>Erääntyvän vähennyksen ja asiakkaan osittaisen maksun selvittäminen vähennyksen työtilassa

Asiakkaat päättävät usein laskutusalennusta ennakoiden maksaa tietyt laskut vain osittain. Jotta maksujen täsmäytyksessä ei olisi ongelmia myöhemmin, myyntireskontran työntekijä rekisteröi nämä osittaiset maksut vähennyksinä, kun hän kirjaa toteutuneita asiakasmaksuja. Nämä asiakkaan vähennyksen on sitten helppo selvittää vähennyksen työtilassa yritykseltä erääntyvien vaatimussummien perusteella.

Voit rekisteröidä asiakkaan osittaisen maksun maksukirjauskansioon valitsemalla **Myyntireskontra** \> **Maksut** \> **Maksukirjauskansio** ja luomalla uuden maksukirjauskansion. Valitse sitten toimintoruudussa **Vähennykset**. Voit luoda **Vähennys**-sivulla osittain maksetun summan ja seurata sitä.

Perintäesimies vastaa nyt siitä, että avoin hyvityslaskutapahtuma ja osittainen maksutapahtuma selvitetään keskenään vähennyksen työtilassa.

Voit hallita vähennyksiä valitsemalla **Myynti ja markkinointi** \> **Myynninedistämispalkkiot** \> **vähennykset** \> **Vähennyksen työtila**. Sivun yläosassa on rivejä, jotka edustavat asiakkaan osittaisia maksuja. Sivun alaosassa on asiakkaan avoimet hyvitystapahtumat. 

Selvitä avointa tapahtumaa koskeva vähennys merkitsemällä vähennysrivi ja merkitsemällä rivi sitten Avoimet tapahtumat -välilehdessä. Valitse toimintoruudussa Ylläpito > Täsmäytä.

Alkuperäisen vaatimuksen tilana on nyt **Valmis**.

## <a name="analyze-the-effectiveness-of-the-promotion-and-fund-consumption"></a>Kampanjan ja rahoituksen käytön tehokkuuden analysointi

Saat yleiskatsauksen ohjelman avaintilastoista ja rahoituksen käytöstä käyttämällä erilaisia myynninedistämispalkkioiden hallinnassa käytössä olevia raportteja ja analyysinäkymiä.

**Myynninedistämispalkkiotehtävä**-sivulla **Yleiskuvaus**-välilehdessä on myynninedistämisen palkkiosopimuksen tärkeimmät tiedot. Muissa välilehdissä on lisätietoja liitetyistä asiakirjoista, maksuista ja muista ohjelmaan liittyvistä tapahtumista.

**Yhteenveto**-välilehdessä on näkyvissä kampanjassa myytyjen tuotteiden kokonaismäärä, laskutettu myyntimäärä sekä maksetut laskutusalennukset ja kokonaissummat.

**Laskutusalennushyvitykset**-välilehdessä on tietoja yksittäisistä asiakkaalle hyvitetyistä laskutusalennuksista.

Jos haluat analysoidaan yleiskuvan kampanjan erilaisista suorituskykymittareista, voit käyttää analyysinäkymää. Siirry analyysinäkymään valitsemalla **Myynti ja markkinointi** \> **Myynninedistämispalkkiot** \> **Myynninedistämisen palkkiosopimukset**. Valitse toimintoruudussa **Analyysi**.  

Jos haluat analysoidaan yleiskuvan kampanjan erilaisista suorituskykymittareista, voit käyttää analyysinäkymää. Siirry analyysinäkymään valitsemalla **Myynti ja markkinointi** \> **Myynninedistämispalkkiot** \> **Myynninedistämisen palkkiosopimukset**. Valitse toimintoruudussa **Analyysi**. 

