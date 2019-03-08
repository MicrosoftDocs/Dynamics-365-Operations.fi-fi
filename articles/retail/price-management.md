---
title: Vähittäismyynnin hintojen hallinta
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Retailin myyntihintojen luontiin ja hallintaan liittyviä käsitteitä.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 04/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28a095588bd3c312a2d1c4b83e668487a209077f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "362139"
---
# <a name="retail-sales-price-management"></a>Vähittäismyyntihintojen hallinta

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja myyntihintojen luonti- ja hallintaprosessista Microsoft Dynamics 365 for Retailissa. Aiheessa keskitytään tähän prosessiin liittyviin käsitteisiin ja siihen, mitä vaikutuksia erilaisilla määritysvaihtoehdoilla on myyntihintoihin.

## <a name="terminology"></a>Termit

Ohjeaiheessa käytetään seuraavia termejä.

| Kausi | Määritelmä, käyttö ja huomautukset |
|---|---|
| Hinta | Myyntipisteasiakasohjelmassa tai myyntitilauksessa myytävien tuotteiden yksi yksikkösumma. Tässä ohjeaiheessa termi *hinta* tarkoittaa aina myyntihintaa ei varasto- tai kustannushintaa. |
| Perushinta | Vapautetun tuotteen **Hinta**-kentässä määritetty hinta. |
| Kauppasopimuksen hinta | Tuotteelle tai variantille **Hinta (myynti)** -tyypin kauppasopimuksella määritetty hinta. |
| Paras hinta | Kun tuotteessa on käytettävissä useita hintoja ja alennusta, pienin hinnan summa ja/tai alennussumma, jolla saadaan pienin mahdollinen asiakkaan maksettavaksi tuleva nettosumma. Parhaan hinnan käsitettä kutsutaan tässä ohjeaiheessa aina parhaaksi hinnaksi. Paras hinta ei ole sama asia kuin alennuksen samanaikaisuustilan **Paras hinta** -luettelointiarvo, eikä näitä kahta käsitettä saa sekoittaa keskenään. |

## <a name="price-groups"></a>Hintaryhmät

Hintaryhmät ovat olennaisia Retailin hinnan ja alennuksen hallinnassa. Hintaryhmien avulla hinnat ja alennukset määritetään vähittäismyynnin yksiköihin (eli kanaviin, luetteloihin, liitoksiin ja kanta-asiakkuusohjelmiin). Koska hintaryhmiä käytetään kaikessa hinnoittelussa ja alennuksissa, niiden käyttö on suunniteltava huolellisesti ennen aloittamista.

Sellaisenaan hintaryhmä on vain nimi, kuvaus ja mahdollisesti hinnoittelun prioriteetti. Hintaryhmistä on muistettava ennen kaikkea, että niiden avulla hallitaan monesta moneen -suhteita, joita alennuksilla ja hinnoilla on vähittäismyynnin yksiköiden kanssa.

Seuraavassa kuvassa esitellään hintaryhmien käyttöä. Huomaa, että tässä kuvassa hintaryhmä on kirjaimellisesti hinnoittelun ja alennuksen hallinnan keskellä. Vasemmalla puolella on ne vähittäismyynnin yksiköt, joilla hintoja ja alennuksia hallitaan, kun taas todelliset hinta- ja alennustietueet ovat oikealla.

![Hintaryhmät](./media/PriceGroups.png "Hintaryhmät")

Kun luotat hintaryhmiä, älä käytä samaa hintaryhmää useille vähittäismyynnin yksikkötyypeille. Jos teet niin, voi olla vaikea päätellä, miksi tiettyä hintaa tai alennusta käytetään tapahtumassa.

Kuvassa oleva punainen katkoviiva osoittaa, että Retail ei tue asiakkaaseen suoraan perustuvaa hintaryhmää, joka Microsoft Dynamics 365:n perustoiminto. Tässä tapauksessa saat vain myyntihinnan kauppasopimukset. Jos haluat käyttää asiakaskohtaisia hintoja, hintaryhmien määrittämistä suoraan asiakkaan perusteella ei suositella. Käytä sen sijaan liitoksia.

Seuraavissa osissa on lisätietoja niistä vähittäismyynnin yksiköistä, joilla voit määrittää erilliset hinnat, kun hintaryhmiä käytetään. Hintojen ja alennusten näiden kohteiden määritysten kahdessa vaiheessa. Näiden vaiheiden suorittamisjärjestyksellä ei ole merkitystä. Loogista on kuitenkin määrittää ensin yksiköiden hintaryhmät, koska tämä vaihe tehdään todennäköisesti vain kerran käyttöönoton yhteydessä. Voit sitten määrittää hintaryhmät luotaville hinnoille ja alennuksille yksi kerrallaan.

### <a name="channels"></a>Kanavat

Vähittäismyyntialalla on yleistä, että eri kanavilla on eri hinta. Kanavakohtaisiin hintoihin vaikuttaa kaksi ensisijaista tekijää: kustannukset ja paikalliset markkinaolosuhteet.

- **Kustannukset** – Mitä kauempana kanava on tuotteen lähteestä, sitä enemmän tuotteen varastointi maksaa. Esimerkiksi tuoretuotteiden säilyvyysaika on rajallinen ja niillä on tietyt tuotantovaatimukset (kuten kasvukausi). Talven aikana tuore salaatti maksaa enemmän pohjoisen ilmanalan kuin eteläisen ilmanalan alueilla. Jos määrität kanavien hintoja maantieteellisesti laajalla alueella, haluat todennäköisesti määrittää eri hinnat eri kanavissa.
- **Paikallisten markkinaolosuhteet** – jos myymälällä on suora kilpailija kadun toisella puolella, se ottaa hinnat todennäköisesti herkemmin huomioon kuin myymällä, jolla ei ole lähellä suoraa kilpailijaa.

### <a name="affiliations"></a>Liitokset

Liitoksen yleismääritelmä on ryhmään tehty linkitys tai liitos. Retailissa liitokset ovat asiakasryhmiä. Liitokset ovat huomattavasti joustavampi tapa tehdä asiakashinnoittelua ja alennuksia kuin Microsoft Dynamics 365:n asiakas- ja alennusryhmiä koskeva perustoiminto. Liitosta voi ensinnäkin käyttää sekä hinnoissa että alennuksissa, kun taas muussa kuin vähittäismyynnin hinnoittelussa kullakin alennus- ja hintatyypillä on oma ryhmä. Lisäksi asiakas voi kuulua useisiin liitoksiin mutta vain yhteen kunkin tyypin muun kuin vähittäismyynnin hinnoitteluryhmään. Ja vaikka liitokset voidaan määrittää siten, ne linkitetään asiakkaaseen, se ei ole pakollista. Anonyymeille asiakkaille voidaan käyttää myyntipisteessä tilapäisiä liitoksia. Tyypillinen esimerkki anonyymistä liitosalennuksesta on eläkeläis- tai opiskelija-alennus, jossa asiakas saa alennuksen näyttämällä ryhmän jäsenkortin.

Vaikka liitokset liittyvät useimmiten alennuksiin, voit määrittää niiden avulla myös erotushinnoittelun. Kun esimerkiksi jälleenmyyjä myy työntekijälle, jälleenmyyjä ehkä haluaa muuttaa myyntihintaa sen sijaan, että normaalihintaan käytettäisiin alennusta. Toinen esimerkki on jälleenmyyjä, joka myy kuluttaja- että yritysasiakkaille ja joka antaa yritysasiakkaille paremman hinnan ostojen määrän perusteella. Liitosten avulla voidaan käyttää kumpaakin skenaariota.

### <a name="loyalty-programs"></a>Kanta-asiakasohjelmat

Hintojen ja alennusten kannalta kanta-asiakasohjelma on käytännössä liitos, jolle on annettu tietty nimi. Kanta-asiakasohjelmalle voidaan määrittää sekä hinnat että alennukset samalla tavoin kuin ne määritetään liitokselle. Asiakkaat saavat kuitenkin kanta-asiakashinnoittelun tapahtuman tai tilauksen aikana eri tavalla kuin liitoshinnoittelussa. Asiakkaat saavat kanta-asiakashinnoittelun vain, jos kanta-asiakaskortti lisätään tapahtumaan. Kun kanta-asiakaskortti lisätään tapahtumaa, myös kanta-asiakasohjelma lisätään. Erikoishinnat ja alennukset otetaan sitten käyttöön kanta-asiakasohjelman avulla.

Kanta-asiakasohjelmissa voi olla useita tasoja, ja alennukset voivat vaihdella tason mukaan. Tällä tavoin vähittäismyyjät voivat antaa paljon ostaville asiakkaille paremmat palkkiot ilman, että kyseisille asiakkaille on luotava manuaalisesti oma ryhmä.

Kanta-asiakasohjelmilla on hintojen ja alennusten lisäksi muita toimintoja. Hinnoittelun ja alennusten kannalta katsottuna ne kuitenkin vastaavat liitoksia.

### <a name="catalogs"></a>Luettelot

Osa vähittäismyyjistä käyttää fyysisiä tai virtuaalisia luetteloita markkinoidessaan ja hinnoitellessaan tuotteita kohdeasiakasryhmille. Koska luetteloiden avulla tapahtuva kohdemarkkinointi on osa heidän liiketoimintamalliaan, kyseiset vähittäismyyjät voivat määrittää erotushinnat eri luetteloihin. Microsoft Dynamics 365 tukee tätä toimintoa, sillä se sallii luettelokohtaisten alennusten ja hintojen määrittämisen samalla tavalla kuin kanava- tai liitoskohtaisten alennusten määrittämisen. Voit liittää luetteloa muokatessa hintaryhmät luetteloon samalla tavalla kuin ne liitetään kanavaan, liitokseen tai kanta-asiakasohjelmaan.

### <a name="best-practices-for-price-groups"></a>Hintaryhmien parhaat käytännöt

Älä käytä hintaryhmää useille vähittäismyynnin yksikkötyypeille. Käytä sen sijaan kanavien hintaryhmiä, eri hintaryhmiä liitoksille tai kanta-asiakasohjelmille jne. Voit käyttää hintaryhmän nimessä etu- tai jälkiliitettä erottamaan ryhmä visuaalisesti käyttämistäsi erilaisista hintaryhmätyypeistä.

Vältä hintaryhmien määrittämistä suoraan asiakkaan perusteella. Käytä sen sijaan liitosta. Voit määrittää tällä tavoin asiakkaille kaikenlaisia hinta- ja alennustyyppejä pelkän myyntisopimuksen kauppasopimusten sijaan.

## <a name="pricing-priority"></a>Hinnoitteluprioriteetti

Hinnoitteluprioriteetti on sellaisenaan vain numero ja kuvaus. Hinnoitteluprioriteetteja voi käyttää hintaryhmissä. Niitä voidaan käyttää myös suoraan alennuksissa. Kun hinnoitteluprioriteetteja käytetään, jälleenmyyjä voi korvata niiden avulla parhaan hinnan hallitsemalla järjestystä, jossa hintoja ja alennuksia käytetään tuotteissa. Suurempi hinnoitteluprioriteetin numero arvioidaan ennen pienempää hinnoitteluprioriteetin numeroa. Jos jostakin prioriteettinumerosta löytyy lisäksi hinta tai alennus, kaikki hinnat tai alennukset, joiden prioriteettinumerot ovat pienemmät, ohitetaan.

Hinta ja alennus saadaan kahdesta eri hinnoitteluprioriteetista, koska hinnoitteluprioriteetteja käytetään itsenäisesti hintoihin ja alennuksiin.

Jos haluat käyttää hintojen hinnoitteluprioriteettia, hinnoitteluprioriteetti on määritettävä hintaryhmään, jonka jälkeen kyseiselle ryhmälle on luota myyntihinnan kauppasopimus.

Hinnoitteluprioriteettitoiminto otettiin käyttöön tukemaan skenaariota, jossa vähittäismyyjä haluaa käyttää korkeampia hintoja tietyssä myymäläjoukossa. Esimerkki: Vähittäismyyjä on määrittänyt aluehinnat Yhdysvaltojen itärannikolle mutta haluaa korkeammat hinnat joillekin tuotteille New York Cityn myymälöissä, koska tuotteiden myynti siellä on kalliimpaa ja/tai koska paikalliset markkinat hyväksyvät korkeammat hinnat.

Kuten tämän ohjeaiheen Paras hinta -osassa kerrottiin, vähittäismyynnin hinnoittelumoduuli valitsee normaalista kahdesta hinnasta alhaisemman. Jälleenmyyjä ei tämän vuoksi yleensä voi käyttää kahdesta hinnasta korkeampaa myymälässä, jossa on sekä itärannikon että New Yorkin hintaryhmät. Ennen hinnoitteluprioriteettitoiminnon ottamisesta käyttöön jälleenmyyjä ratkaisi tämän ongelman määrittämällä hinnat jokaiselle tuotteelle kahdesti ja jättämällä molemmat hintaryhmät määrittämättä. Vaihtoehtoisesti jälleenmyyjältä oli luotava ylimääräiset hintaryhmät eristämään korkeampia hintoja käyttävät tuotteet tuotteista, joilla oli tavalliset alhaisemmat hinnat.

Hinnoitteluprioriteettitoiminnon avulla jälleenmyyjä voi kuitenkin luoda myymälän hinnoille hinnoitteluprioriteetin, joka on korkeampi kuin alueellisten hintojen hinnoitteluprioriteetti. Vaihtoehtoisesti jälleenmyyjä voi luoda hinnoitteluprioriteetin vain myymälän hinnoille ja jättää alueellisille hinnoille oletushinnoitteluprioriteetti, joka on 0 (nolla). Kummatkin asetukset auttavat varmistamaan, että myymälän hintoja käytetään aina ennen alueellisia hintoja.

### <a name="pricing-priority-example"></a>Esimerkki hinnoitteluprioriteetista

Tarkastellaan esimerkkiä, jossa myymälän hinnat ohittavat muut hinnat.

Valtakunnallinen jälleenmyyjä määrittää useimmat hinnat alueittain, joita on neljä: koillinen, kaakko, keskilänsi ja länsi. Se on määrittänyt useita kustannuksiltaan korkeita markkina-alueita, jotka tukevat korkeita hintoja. Kyseiset markkina-alueet New York City, Chicago ja San Francisco ympäristöalueineen.

Tässä esimerkissä poraudutaan koillisen alueeseen. Myymälä 1 on Bostonissa ja myymälä 2 Manhattanilla. Bostonin myymälän kaksi hintaryhmää on linkitetty kanavaan: koillinen ja myymälä 1. Manhattanien myymälän kolme hintaryhmää on linkitetty kanavaan: koillinen, NYC ja myymälä 2.

Jälleenmyyjältä määrittää kaksi hinnoitteluprioriteettia: korkeiden kustannusten on prioriteettinumero on 5 ja myymälän hintojen prioriteettinumero on 10. (Muista, että hinnoitteluprioriteetti on oletusarvoisesti 0 \[nolla\] ja että prioriteettinumeroltaan suurempaa hintaa tai alennusta käytetään ennen prioriteettinumeroltaan pienempää hintaa tai alennusta.) Koillisen hintaryhmän hinnoitteluprioriteetiksi on jätetty oletusarvo **0** (nolla). New York Cityn hintaryhmän hinnoitteluprioriteetiksi on määritetty **5**, koska New York City on kustannuksiltaan korkea markkina-alue. Myymälän 1 ja myymälän 2 hintaryhmien hinnoitteluprioriteetiksi määritetään **10**.

Jälleenmyyjä myy kahta tuotetta: tuote 1 on tavallinen t-paita ja tuote 2 tietyn tuotemerkin farkut.

| Tuote | Koillisen hinta | NYC-hinta | Myymälän hinta |
|---|---|---|---|
| T-paita | 15 $ | Ei joukkoa | Ei joukkoa |
| Muotifarkut | 50 $ | 70 $ | Ei joukkoa |

T-paita myydään samalla hinnalla (15 $) sekä Bostonin että Manhattanin myymälässä, koska kumpaankin kanavaan linkitetylle koillisen hintaryhmälle on määritetty vain yksi hinta. Muotifarkkujen myyntihinta Bostonin myymälässä on 50 $, koska kyseinen hinta on ainoa kyseisessä myymälässä käytettävissä oleva hinta. Manhattanin myymälässä on kuitenkin käytettävissä kaksi hintaa : 50 $ ja 70 $. Koska NYC-hintaryhmän hinnoitteluprioriteetti 5 on korkeampi kuin koillisen hintaryhmän hinnoitteluprioriteetteja 0 (nolla), myyntipisteen järjestelmää käyttää hintaa 70 $.

> [!NOTE]
> Jokaisen hinnoitteluprioriteetin on käsiteltävä vähittäismyynnin hinnoittelumoduulin logiikka. Tämän vuoksi hinnoitteluprioriteetteja kannattaa käyttää harkiten, jotta hinnan ja alennuksen laskenta ei hidastu.

## <a name="types-of-prices"></a>Hintatyypit

Tuotteen hinta voidaan määrittää Microsoft Dynamics 365:ssä kolmessa paikassa:

- Suoraan tuotteessa (perushinta)
- Myyntihinnan kauppasopimuksessa
- Hinnanoikaisussa

Perushinta ja kauppasopimuksen ovat osa Microsoft Dynamics 365:n perustoimintoja, ja ne ovat käytettävissä vaikka Retail ei olisi käytössä. Hinnanoikaisutoiminto on käytettävissä vain Retailissa. Seuraavassa osassa on lisätietoja kustakin hinnan määritysasetuksesta. Lisäksi selitetään, miten asetuksia voi käyttää yhdessä.

## <a name="setting-prices"></a>Hintojen määrittäminen

### <a name="base-price"></a>Perushinta

Tuotteen hinta on kätevintä määrittää suoraan tuotteessa. Tuotteessa suoraan määritettävää arvoa kutsutaan usein tuotteen perushinnaksi. Perushinta määritetään **Vapautetun tuotteen tiedot** -sivun **Myynti**-välilehden **Hinta**-kentässä. Antamasi arvon valuutta on yrityksen valuuttana. Oletusarvoisesti hinta koskee määrää 1 siinä mittayksikössä, joka määritettiin **Myynti**-välilehden **Yksikkö**-kentässä. Tuotteen todellinen yksikkökohtainen hinta perustuu mittayksikköön, hinnan määrään ja valuuttaan.

Jos tuotteella on yksi hinta kaikille, perushinta on tehokkain tapa hallita kyseisen tuotteen hintaa. Vaikka käyttäisit kauppasopimuksia hintojen määrittämiseen, määrität ehkä myös tuotteen perushinnan. Jos et sitten käytä **Kaikki**-kauppasopimusta, sinulla varahinta, jota käytetään silloin, kun mitään kauppasopimusta ei käytetä.

Jos vähittäismyyntikanavan valuutta ei ole sama kuin yrityksen valuutta, kyseisen vähittäismyyntikanavan perushinta määritetään käyttämällä valuutan muuntoa tuotteessa määritetyssä hinnassa.

Vaikka hintayksikkö ei ole yleinen vähittäismyynnin skenaario, vähittäismyynnin hinnoittelumoduuli tukee sitä. Jos hintayksikön arvoksi on määritetty jokin muu kuin **0** (nolla), yksikkökohtainen hinta on sama kuin hinta + hintayksikkö. Jos tuotteen hinta on esimerkiksi 10,00 $ ja yksikköhinta on 50, määrältään 1:n hinta on 0,20 $0 (= 10,00 $ / 50).

### <a name="sales-price-trade-agreement"></a>Myyntihinnan kauppasopimus

Voit luoda kauppasopimuksen kirjauskansion avulla kullekin tuotteelle myyntihinnan kauppasopimuksia. Microsoft Dynamics 365:ssä on kolme myyntihinnan kauppasopimusten asiakasaluetta: **Taulu**, **Ryhmä** ja **Kaikki**. Asiakkaan alue määrittää asiakkaat, joita annettu myyntihinnan kauppasopimus koskee.

Myyntihinnan **Taulu**-asiakassopimus on tarkoitettu yhdelle, suoraan kauppasopimuksessa määritetylle asiakkaalle. Tämä skenaario ei ole tavallinen B2C-skenaariossa. Jos se kuitenkin tapahtuu, vähittäismyynnin hinnoittelumoduuli käyttää hinnan määrityksessä **Taulu**-kauppasopimuksia.

Myyntihinnan **Ryhmä**-kauppasopimus on tyyppi, jota käytetään eniten vähittäismyyntitoiminnoissa. Retailin ulkopuolella myyntihinnan **Ryhmä**-kauppasopimukset on tarkoitettu yksinkertaiselle asiakasryhmälle. Asiakasryhmän käsitettä on kuitenkin laajennettu Retailissa siten, että on yleinen vähittäismyynnin hintaryhmä. Hintaryhmä voidaan linkittää vähittäismyynnin kanavaan, liitokseen, kanta-asiakasohjelmaan tai luetteloon. Lisätietoja hintaryhmistä on aiemmin tässä ohjeaiheessa Hintaryhmät-osassa.

> [!NOTE]
> Kauppasopimuksen hintaa käytetään aina ennen perushintaa.

### <a name="price-adjustment"></a>Hinnanoikaisu

Nimensä mukaisesti hinnanoikaisun avulla muokataan joko suoraan tuotteessa tai kauppasopimuksen avulla määritettyä hintaan. Hinnanoikaisun avulla voi vain pienentää hintaa; sitä ei siis voi nostaa. Hinnanoikaisua suositellaan jälleenmyyjille tuotteiden ajan mittaan tapahtuvien hinnanalennusten luontiin, seurantaan ja hallintaan.

Hinnanoikaisutyyppejä on kolme: prosenttialennus, alennussumma ja hinta. Myyntitapahtumassa käytetään prosenttialennus- tai alennussummatyypistä hinnanoikaisua. Hintatyypistä hinnanoikaisua käytetään vain, jos oikaistu hinta on pienempi kuin perushintaa tai kauppasopimuksen hintaa käyttämällä määritetty hinta. Jos siis hinnanoikaisussa määritetty hinta on suurempi kuin oikaisematon hinta, hinnanoikaisua ei käytetä.

## <a name="determining-price-for-a-product-in-a-transaction"></a>Tapahtuman tuotteen hinnan määrittäminen

Hinta ja alennus lasketaan tapahtumassa etsimällä asiakkaalle paras hinta. Tämän periaatteen mukaisesti käytetään alhaisinta hintaa, jos useita hintoja löytyy. Lisäksi käytetään sellaista alennusten yhdistelmää, jolla koko tapahtumalle saadaan suurin alennussumma. Joissakin tapauksissa yksittäisessä tuotteessa on käytettävä pienempää alennusta, jotta lisäalennuksia voidaan käyttää tapahtuman muihin tuotteisiin.

Ainoa poikkeus asiakkaalle parhaan hinnan etsimisperiaatteeseen on edullisten yhdistelmäalennusten asetus. Tällä asetuksella otetaan käyttöön jälleenmyyjän kannalta edullisimmat alennukset tuotteita valittaessa ja ryhmitettäessä. Kun tapahtuma näin ollen sisältää enemmän tuotteita kuin tarvitaan edullisinta alennusta varten, vähittäismyynnin hinnoittelumoduuli valitsee tuotteet, joilla asiakkaan alennussumma on mahdollisimman pieni.

Vähittäismyynnin hinnoittelumoduuli palauttaa kolme hintaa jokaiselle tuotteelle: perushinta, kauppasopimuksen hinta ja aktiivinen hinta.

Perushinta on pelkkä tuotteen ominaisuus, joka on sama kaikille kaikkialla.

Jos myyntihinnan kauppasopimuksessa **Etsi seuraava** -asetukseksi on määritetty **Kyllä**, alhaisinta soveltuville myyntihinnan kauppasopimuksille löydettyä hintaa käytetään kauppasopimuksen hintana. Kauppasopimukset voidaan etsiä käyttämällä hintaryhmiä tai **Kaikki**-tilikoodia. Kauppasopimukset voidaan vaihtoehtoisesti määrittää myös suoraan asiakkaalle. Jos **Etsi seuraava** -asetukseksi on määritetty **Ei**, käytetään ensimmäistä löydettyä kauppasopimusta. Jos yhtään myyntihinnan kauppasopimusta ei löydetä, kauppasopimuksen hinta määritetään vastaamaan perushintaa.

Aktiivinen hinta lasketaan ottamalla kauppasopimuksen hinta ja käyttämällä suurinta tuotetta koskevaa hinnanoikaisua. Jos yhtään hinnanoikaisua ei löydetä tai jos laskettu aktiivinen hinta on suurempi kuin kauppasopimuksen hinta, aktiivinen hinta määritetään vastaamaan kauppasopimuksen hintaa. Muista, ettet voi nostaa tuotteen hintaa käyttämällä hinnanoikaisua. Käytettäviä hinnanoikaisuja on etsittävä käyttämällä hintaryhmä, jotka on määritetty kanavaan, luetteloon, liitokseen tai kanta-asiakasohjelmaan.

## <a name="category-price-rules"></a>Luokan hintasäännöt

Retailin luokan hintasääntöominaisuudella on helppo luoda uusia kauppasopimuksia kaikille luokan tuotteille. Tällä ominaisuudella voi myös automaattisesti etsiä luokan tuotteille aiemmin luodut kauppasopimukset ja päättää niiden voimassaolon.

Kun valitset aiemmin luotujen kauppasopimusten vanhentumisasetuksen, järjestelmä luo uuden kauppasopimuksen kirjauskansion sellaisen luokan tuotteille, joissa on aktiivinen kauppasopimus. Kirjauskansion on kuitenkin kirjattava manuaalisesti. Luokan hintasäännöillä voi etsiä aiemmin luotuja kauppasopimuksia vain, jos käytät samaa hintasääntöjä. (Toisin sanoen luot uuden hintasäännön, joka käyttää samaa luokkaa kuin aiemmin.) Jos et käytä samaa hintasääntöä, aiemmin luodut kauppasopimukset eivät vanhene.

Hintoja voi nostaa tai laskea käyttämällä luokan hintasääntöjen **Hintasääntö**- ja **Hintaperuste**-kenttiä.

- Valitse **Hintasääntö**-kentässä käytettävä hinnanmuutostyyppi:

    - **Hinnankorotus** – Hintaperusteen prosenttiosuutta käytetään myyntihinnan laskentaan. Esimerkiksi 10,00 maksavan tuotteen, jonka myyntihinta on 15,00, hinnankorotus on 50 prosenttia.
    - **Kate** – Tuoton määrän laskemiseen käytetyn myyntihinnan prosenttiosuus. Esimerkiksi 10,00 maksavan tuotteen, jonka myyntihinta on 15,00, kate on 33,3 prosenttia.
    - **Kiinteä summa** – Hintaperusteeseen lisätty määrä, jota käytetään myyntihinnan laskemiseen. Esimerkiksi 15,00 maksavan tuotteen, jonka myyntihinta on 10,00, kiinteä summa on 5,00.

- Valitse **Hintaperuste**-kenttään muokattava hintatyyppi:

    - **Peruskustannus**– Summa, jonka jälleenmyyjä maksoi toimittajalle.
    - **Perushinta** – Myyntihinta kauppasopimusten ja hinnanoikaisujen soveltamista ennen.
    - **Nykyinen hinta** – Myyntihinta kauppasopimusten ja hinnanoikaisujen soveltamisen jälkeen.

Eri tuoteluokkien eri tuotteiden hinnat on helppo päivittää käyttämällä lisätuoteluokkia luokan hintasääntöjen kanssa.

## <a name="best-practices"></a>Parhaat käytännöt

Microsoft SQL Server Expressiä käytetään usein kanavatietokantoissa kustannussyistä (maksuton). Muista, että SQL Server Expressissä on laitteistorajoituksia ja että tietojen kokoa rajoitetaan. Jos suunnittelu epäonnistuu, SQL Server Expressin tietojen kokorajoitus täyttyy pian. Tämä ei koske vain innoittelua vaan myös muita tuotteen alueita. Seuraavat parhaat käytännöt auttavat vähentämään tietojen kokoa:

- Jos käytät kauppasopimuksia ja hinnat muuttuvat, vanhojen kauppasopimusten voimassaolo kannattaa päättää määrittämällä päättymispäivä. Ajan mittaan tämä käytäntö auttaa vähentämään kanavatietokannoissa säilytettävien kauppasopimusten määrää. Se auttaa myös vähentämään niiden tietojen määrää, joita hinnan laskenta-algoritmin on käytettävä.
- Jos hinnat vaihtelevat tuotevarianttien mukaan, harkitse tuotteen perushinnan käyttämistä yleisimmän variantin hintana. Käytä sitten kauppasopimuksia vain niiden varianttihinnoille, jotka ovat poikkeuksia. Tämä käytäntö auttaa vähentämään kauppasopimustietueiden määrää. Koska tietoja on helppo tuoda Microsoft Dynamics 365:een, jokaisen tuotteen jokaisen variantin kauppasopimuksen tuonti voi houkutella. Tällä tavoin voidaan saada useita kauppasopimuksia, joilla on sama arvo. Niinpä se voikin kasvattaa turhaa tietojen kokoa.
- Retail käsittelee varianttikohtaiset hinnat tarkimmasta vähiten tarkkaan. Jos tuotedimensio ei vaikuta hintaan, sille ei tarvitse määrittää kauppasopimuksia. Jos tuote on esimerkiksi saatavana kolmessa eri värissä ja neljässä eri koossa, mutta hinta vaihtelee vain koon mukaan. Jos määrität kauppasopimuksen jokaiselle variantille, voit luoda 12 tietuetta. Voit sen sijaan määrittää kauppasopimuksen vain jokaiselle koolle ja jättää väridimension tyhjäksi. Tässä tapauksessa syntyy vain neljä tietuetta.

    Jos vaihtoehtoisesti jokainen dimensioarvo tuottaa eri hinnan, voit määrittää päätuotteelle yhden kauppasopimuksen ja jättää kaikki tuotedimensiot tyhjäksi. Määritä sitten erillinen kauppasopimus kullekin dimensioarvolle, jolla saadaan eri hinta. Jos esimerkiksi koon XXL hinta on korkeampi kaikkien muiden kokojen hinnan ollessa sama, tarvitset vain kaksi kauppasopimusta: yhden päätuotteelle ja yhden koolle XXL.

## <a name="prices-that-include-tax-vs-prices-that-exclude-tax"></a>Verollisten ja verottomien hintojen vertailu

Microsoft Dynamics 365:ssä määritettävissä myyntihinnoissa ei määritetä, sisältääkö määritettävä hinta-arvo arvolisäveron vai ei. Tämä arvo on vain hinta. Vähittäismyyntikanavien **arvolisäveron sisältävän hinnan** asetus sallii vähittäismyyntikanavien määrittämisen siten, että hinnat joko sisältävät arvolisäverot tai eivät sisällä niitä. Tämä asetus määritetään kanavassa ja se voidaan muuttaa vaikkapa vain yhdessä yrityksessä.

Jos käsittelet sekä arvonlisäveron sisältäviä että sen pois jättäviä tyyppejä, hintojen määrittäminen oikein on tärkeää, koska asiakkaan maksama kokonaissumma muuttuu, jos kanavan **arvolisäveron sisältävän hinnan** asetusta muutetaan.

## <a name="differences-between-retail-pricing-and-non-retail-pricing"></a>Vähittäismyynnin hinnoittelun ja muun kuin vähittäismyynnin hinnoittelun väliset erot

Samalla hinnoittelumoduulilla lasketaan kaikkien kanavien vähittäismyynnin hinnat: puhelinkeskus, myymälä ja verkkokauppa. Tämä auttaa ottamaan käyttöön yhtenäiset kaupankäyntiskenaariot.

Vähittäismyynnin hinnoittelu on suunniteltu toimimaan vähittäismyynnin yksiköiden eikä muiden kuin vähittäismyynnin yksiköiden kanssa. Se on suunniteltu nimenomaan määrittämään hinnat myymälöittäin eikä varastoittain.

Vähittäismyynnin hinnoittelumoduuli ei tue seuraavia hinnoitteluominaisuuksia:

- Hinnan määrittäminen toimipaikan ja varaston varastodimensioiden avulla
- Määritepohjainen hinnoittelu
- Toimittajan alennuksen välitys

Lisäksi **vain** vähittäismyynnin hinnoittelumoduuli tukee seuraavia hinnoitteluominaisuuksia:

- Hinta perustuu tuotedimensioihin seuraavassa järjestyksessä: tarkin varianttihinta, vähiten tarkin varianttihinta ja päätuotteen hinta. Kahta tuotedimensiota (kuten väriä ja kokoa) käyttämällä määritettyä hintaa käytetään ennen hintaa, joka on määritetty käyttämällä vain yhtä tuotedimensiota (kuten kokoa).
- Hinnoittelua ja alennuksia voidaan ohjata samalla hintaryhmällä.
