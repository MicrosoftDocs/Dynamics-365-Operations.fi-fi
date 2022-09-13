---
title: Ruudukon ominaisuudet
description: Tässä artikkelissa kuvataan useita ruudukon ohjausobjektin tehokkaita ominaisuuksia. Uusi ruudukkotoiminto on otettava käyttöön näiden ominaisuuksien käyttämistä varten.
author: jasongre
ms.date: 08/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 096f441d39dde0f322ed117ab35a6a4641a38a93
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405462"
---
# <a name="grid-capabilities"></a>Ruudukon ominaisuudet

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Uusi ruudukon ohjausobjekti sisältää useita hyödyllisiä ja tehokkaita ominaisuuksia, joilla voidaan parantaa käyttäjien tuottavuutta, kehittää mielenkiintoisempia näkymiä tiedoillesi ja hankkia merkityksellisiä tietoja datastasi. Tämä artikkeli käsittelee seuraavia ominaisuuksia: 

- Laskettujen arvojen näyttäminen 
- Järjestelmän ennakoiva kirjoitus
- Matemaattisten lausekkeiden arviointi 
- Taulukkomuotoisten tietojen ryhmittely (käytössä erikseen **Ryhmittely ruudukoissa** -toiminnossa)
- Sarakkeiden jäädyttäminen (otetaan käyttöön erikseen käyttämällä **Sarakkeiden jäädyttäminen ruudukoissa** -toimintoa)
- Sarakeleveyden automaattinen sovittaminen
- Venytettävät sarakkeet

## <a name="showing-calculated-values"></a>Laskettujen arvojen näyttäminen
Talous- ja toimintosovellusten avulla käyttäjät voivat tarkastella ruudukon kunkin numeerisen sarakkeen laskettua arvoa. Nämä lasketut arvot näkyvät alatunnisteosassa ruudukon alareunassa.

[![Laskettujen arvojen näyttäminen ruudukkoina.](./media/grids-aggregation.png)](./media/grids-aggregation.png)

Versioissa ennen versiota 10.0.29 kokonaissumma on ainoa tuettu laskettu arvo. Version 10.0.29 jälkeen käyttäjät voivat kuitenkin valita seuraavista neljästä lasketusta arvosta otettuaan käyttöön **Laajennetut ruudukon koosteominaisuudet** -ominaisuuden:

- Pienin arvo
- Suurin arvo
- Kokonaissumma
- Keskiarvo

Yhdessä sarakkeessa voi olla vain yksi laskettu arvotyyppi. Kunkin ruudukon sarakkeen voi kuitenkin konfiguroida niin, että siinä näkyy erityyppinen laskettu arvo.

### <a name="showing-the-grid-footer"></a>Ruudukon alatunnisteen näyttäminen
Talous- ja toimintosovellusten jokaisen taulukkomuotoisen ruudukon alaosassa on alatunnistealue. Alatunniste voi näyttää arvokkaita tietoja, jotka liittyvät ruudukossa näkyviin tietoihin. Seuraavassa on joitakin esimerkkejä näistä tiedoista:

- Taulukossa vallittuna olevien rivien määrä (kun vähintään kaksi tietuetta on valittuna)
- Konfiguroitujen numeeristen sarakkeiden alaosassa olevat lasketut arvot (esimerkiksi loppusummat)
- Tietojoukon rivimäärä 

Tämä alatunniste on oletusarvoisesti piilotettuna, mutta sen voi ottaa käyttöön. Jos haluat ruudukon alatunnisteen näkyviin, valitse **Ruudukon asetukset** ruudukon otsikosta ja valitse sitten **Näytä alatunniste** -asteus. Kun alatunniste otetaan käyttöön tietyssä ruudukossa, kyseinen asetus muistetaan, kunnes käyttäjä valitsee alatunnisteen piilottamisen. Voit piilottaa alatunnisteen valitsemalla **Ruudukon asetukset** -valikosta **Piilota alatunniste**.

### <a name="specifying-columns-with-calculated-values"></a>Laskettuja arvoja sisältävien sarakkeiden määrittäminen
Yksikään sarake ei näytä laskettuja arvoja tällä hetkellä oletusarvoisesti. Sen sijaan määritys katsotaan yksivaiheiseksi toiminnoksi, joka muistuttaa sarakkeiden leveyden muuttamista ruudukoissa. Kun määrität, että haluat nähdä sarakkeen lasketun arvon, tämä asetus muistetaan, kun seuraavan kerran käyt sivulla.

Sarake voidaan määrittää näyttämään lasketun arvon kahdella tavalla:

- Pidä valittuna (tai napsauta hiiren kakkospainikkeella) saraketta, jonka laskettua arvoa haluat tarkastella. Jos **Laajennetut ruudukon koosteominaisuudet** -toiminto on käytössä, valitse **Näytä sarakkeiden kokonaissummat** ja valitse sitten haluttu laskettu arvo. Jos tätä toimintoa ei ole otettu käyttöön, valitse **Tämä sarake yhteensä**. Tämä toiminto aiheuttaa seuraavat kolme tapahtumaa:

    1. Ruudukon alatunniste tulee näkyviin. 
    2. Järjestelmä tallentaa sarakkeen lasketun arvon tarkasteluasetukset. 
    3. Aloitetaan haluttu laskeminen tässä sarakkeessa ja kaikissa muissa sarakkeissa, joiden laskettu arvo on määritetty tarkasteltavaksi. Laskettujen arvojen näyttämiseen tarvittava aika määräytyy tietojoukon koon mukaan.

- Valitse alatunnisteen näkymisen jälkeen **Näytä summa** (tai **Valitse laskettu arvo**, jos **Laajennetut ruudukon koosteominaisuudet** -ominaisuus on otettu käyttöön) sen sarakkeen alaosan alatunnistealueella, jolle haluat tarkastella laskettua arvoa. Jos määritettyjä sarakkeita ei ole, painike on käytettävissä kaikkien numeeristen sarakkeiden alatunnisteessa.

    Kun vähintään yksi sarake on määritetty näyttämään laskettu arvo, **Näytä summa** (tai **Valitse laskettu arvo**) -painike on käytettävissä vain osoitettaessa tai kohdistettaessa. Painikkeen valintatoiminto vain tallentaa sarakkeen lasketun arvon tarkastelua varten niin, että asetuksia käytetään sivulla myös myöhemmin. Alatunnisteessa tämä tila ilmaistaan ajatusviivalla, joka näkyy sarakkeessa. (Huomaa, että laskettu arvo näkyy heti, jos tietojoukko on tarpeeksi pieni.)

Jos teet virheen etkä enää halua tarkastella laskettua arvoa tietyssä sarakkeessa, valitse ja pidä saraketta painettuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse sitten **Piilota yhteensä** (tai **Näytä sarakkeiden kokonaissummat \> Ei mikään**, jos **Laajennetut ruudukon koosteominaisuudet** -ominaisuus on käytössä). Vaihtoehtoisesti voit valita **Piilota yhteensä** (tai **Piilota laskettu arvo**) sarakkeen alatunnisteessa. Tämä valinta tallennetaan myös tulevia sivuvierailuja varten. 

### <a name="calculating-aggregate-values"></a>Koostearvojen laskeminen
Kun siirryt sivulle, jolla alatunniste on näkyvissä ja sarakkeet on jo määritetty näyttämään lasketut arvot, ne eivät ehkä näy alatunnisteessa. Näkyminen riippuu sivun tietojoukon koosta. Jos tietojoukko on riittävän pieni, lasketut arvot ja tietojoukon rivien määrä näytetään automaattisesti. Jos määrittämiesi sarakkeiden alatunnisteissa on ajatusviivoja, tietojoukko on liian suuri, jotta järjestelmä näyttäisi lasketut arvot heti. Tällöin arvojen laskenta edellyttää täsmällistä toimintoa. Voit laskea arvot valitsemalla alatunnisteen **Laske**-painikkeen. Vaihtoehtoisesti valitse ja pidä saraketta, jonka summan haluat näyttää, painettuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse sitten **Tämä sarake yhteensä** (tai **Näytä sarakkeiden kokonaissummat** ja sitten haluttu laskettu arvo, jos **Laajennetut ruudukon koosteominaisuudet** -ominaisuus on käytössä).

Jos laskeminen kestää liian kauan, voit peruuttaa toiminnon milloin tahansa valitsemalla **Peruuta**. Joskus tietojoukko on liian suuri, jotta voidaan laskea kokonaisarvot (organisaation asettama raja). Tällöin saat sen sijaan ilmoituksen, että suodatat tietojasi enemmän.

> [!NOTE]
> Järjestelmänvalvojat voivat muokata koosteiden laskennassa käytettävissä olevien tietueiden rajaa muuttamalla **Kunkin ruudukon paikallisen tietueen enimmäismäärä** -parametria **Asiakkaan suorituskykyasetukset** -sivulla. Oletusarvo on 25 000 tietuetta. Järjestelmänvalvojien tulee olla varovaisia muuttaessaan tätä arvoa, koska liian suuri arvo voi kuluttaa käyttäjän laitteen käytettävissä olevan muistin. On suositeltavaa, että arvo on enintään 50 000 tietuetta.

Lasketut arvot päivittyvät automaattisesti, kun päivität, poistat tai luot rivejä tietojoukossa.

## <a name="typing-ahead-of-the-system"></a>Järjestelmän ennakoiva kirjoitus
Monissa liiketoimintaskenaarioissa tietojen nopea syöttäminen järjestelmään on erittäin tärkeää. Aiemmin käyttäjät voivat muuttaa tietoja vain nykyisellä rivillä, ennen kuin uusi ruudukko-ohjausobjekti otettiin käyttöön. Sen vuoksi tehtyään muutoksia riviin käyttäjät eivät voineet siirtyä eri riville tai luoda uutta riviä, ennen kuin järjestelmä tarkisti muutokset nykyisellä rivillä ja (riviä luotaessa) suoritti kaikki uuden rivin luontiin liittyvät logiikkavaihtoehdot. Kun yritetään lyhentää aikaa, jonka käyttäjät odottavat näiden toimintojen valmistumista, ja parantaa käyttäjien tuottavuutta, uusi ruudukko säätää nämä toiminnot niin, että ne ovat asynkronisia. Käyttäjät voivat luoda uusia rivejä tai siirtyä muille riveille muutosten luomiseksi, kun aiemmat rivien vahvistukset ja rivien luontilogiikka odottavat. 

[![Järjestelmän ennakoiva kirjoitus.](./media/gridFastEntry-07-25-2022.gif)](./media/gridFastEntry-07-25-2022.gif)

Tämän uuden toiminnon tukemiseksi rivitilan sarakkeen oikealle puolelle on lisätty uusi sarake rivin tilalle, kun ruudukko on muokkaustilassa. Tämä sarake ilmaisee jonkin seuraavista tiloista:

- **Tyhjä** – Ei tilaa kuvaa ilmaisee, että järjestelmä on tallentanut rivin onnistuneesti.
- **Käsittely odottaa** – Tämä tila ilmaisee, että palvelin ei ole vielä tallentanut rivin muutoksia, vaan ne ovat käsiteltävien muutosten jonossa. Ennen kuin suoritat toimenpiteitä ruudukon ulkopuolella, sinun on odotettava kaikkien odottavien muutosten käsittelemistä. Lisäksi näiden rivien teksti on kursivoitu rivien tallentamattoman tilan ilmaisemiseksi. 
- **Virheellinen tila** – Tämä tila ilmaisee, että rivin käsittelyn aikana käynnistettiin jokin varoitus tai sanoma, ja se on voinut estää järjestelmää tallentamasta muutoksia kyseiseen riviin. Vanhassa ruudukossa joutui palaamaan riville korjaamaan ongelman heti, mikäli tallennus ei onnistunut. Uusi ruudukko kuitenkin ilmoittaa, että vahvistusongelma ilmeni, mutta voit päättää, milloin haluat korjata kaikki rivin ongelmat. Kun olet valmis korjaamaan ongelman, voit siirtää kohdistuksen manuaalisesti takaisin riville. Vaihtoehtoisesti voit valita **Korjaa tämä ongelma** -toiminnon. Tämä toimenpide siirtää kohdistuksen välittömästi riville, jolla on ongelma, ja voit tehdä muokkauksia ruudukon sisä- tai ulkopuolelle. Huomaa, että seuraavien odottavien rivien käsittely pysäytetään, kunnes tämä vahvistusvaroitus on ratkaistu. 
- **Keskeytetty** – Tämä tila ilmaisee, että palvelimen käsittely keskeytetään, koska rivin oikeellisuustarkistus käynnistää ponnahdusikkunan, joka edellyttää käyttäjän toimia. Koska käyttäjä saattaa kirjoittaa tietoja toiselle riville, ponnahdusikkuna ei tule heti näkyviin kyseiselle käyttäjälle. Sen sijaan se esitetään, kun käyttäjä päättää jatkaa käsittelyä. Tähän tilaan liittyy ilmoitus, joka kertoo käyttäjälle tilanteesta. Ilmoitus sisältää **Jatka käsittelyä** -toiminnon, joka käynnistää ponnahdusikkunan.

### <a name="differences-when-entering-data-ahead-of-the-system"></a>Erot, kun tietoja syötetään ennen järjestelmää
Kun syötät tietoja ennen järjestelmän käsittelypaikan tietoja, voit odottaa joitakin muutoksia tietojen syöttökokemukseen:

- Huomaa, että avattavia hakuluetteloita ei ole, kenttien arvoja ei vahvista sen jälkeen, kun siirryt saman rivin eri sarakkeeseen eikä oletusarvoja aluksi näytetä sarakkeissa. Näin tapahtuu, kun luodaan tai päivitetään ennen järjestelmää. Kuitenkin vakiokokemusta jatketaan sen jälkeen, kun järjestelmä on saavuttanut sen paikan, jossa olet muokkaamassa. Jos olet tehnyt muutoksia kenttään, jolle yleensä annetaan oletusarvo, muutokset korvaavat oletusarvon, kun palvelin aloittaa rivin käsittelemisen.
- Jos luot uuden rivin käyttämällä **alanuoli** näppäintä, kaikki ruudukon sarakkeet näkyvät muokattavissa. Oletusarvon mukaan kohdistus tulee uuden rivin ensimmäiseen sarakkeeseen. Tämä sarake ei ehkä ole sama sarake, joka on saanut alkuperäisen kohdistuksen vanhassa ruudukossa, tai sarake, jossa kohdistus vastaanotetaan, kun valitset **Uusi**-painikkeen. Organisaatiosi voi mukauttaa järjestelmää ja muuttaa saraketta, joka saa ensimmäisen kohdistuksen, kun **alanuoli** näppäin valitaan. Lisätietoja on kohdassa [Sarakkeen määrittäminen, jossa alkuperäinen kohdistus vastaanotetaan, kun uusia rivejä luodaan alanuolinäppäimellä](#developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key). Mukauttamisen avulla voit optimoida kunkin ruudukon tietojen syöttöä varten. Voit järjestää kentät uudelleen siten, että ensimmäinen sarake on sarake, josta haluat aloittaa tietojen syöttämisen. Voit myös järjestää yleisesti uudelleen kentät tietojen syöttöä varten vähentääksesi sarkainkohtien keskeytyksiä ja piilottaa kaikki kentät, joita ei tarvita tietojen lisäämiseen tässä näkymässä.

### <a name="pasting-from-excel"></a>Liittäminen Excelistä
Käyttäjät ovat aina voineet viedä tietoja talous- ja toimintosovelluksista Microsoft Exceliin käyttämällä **Vie Exceliin** -mekanismia. Mahdollisuus syöttää tietoja ennen järjestelmää mahdollistaa kuitenkin sen, että uusi ruudukko tukee taulujen kopioimista Excelistä ja liittämistä suoraan talous- ja toimintosovellusten ruudukkoihin. Ruudukon solu, josta liittämistoiminto käynnistetään, määrittää, mihin kopioitu taulukko alkaa liittää. Kopioidun taulun sisältö korvaa ruudukon sisällön lukuun ottamatta kahta tapausta:

- Jos kopioidun taulukon sarakkeiden määrä ylittää ruudukon jäljellä olevien sarakkeiden määrän, alkaen liittämissijainnista, käyttäjälle ilmoitetaan, että ylimääräiset sarakkeet on ohitettu. 
- Jos kopioidun taulukon rivien määrä ylittää ruudukon rivien määrän alkaen liittämissijainnista, aiemmin luodut solut korvataan liitetystä sisällöstä ja kopioidun taulukon ylimääräiset rivit lisätään uusina riveinä ruudukon alaosaan. 

## <a name="evaluating-math-expressions"></a>Matemaattisten lausekkeiden arviointi
Tuottavuutta tehostaakseen käyttäjät voivat antaa matemaattisia kaavoja ruudukon numeerisiin soluihin. Heidän ei tarvitse tehdä laskelmia järjestelmän ulkopuolisissa sovelluksissa. Jos esimerkiksi syötät **=15\*4** ja painat sitten **sarkainnäppäintä** ja siirryt pois kentästä, järjestelmä arvioi lausekkeen ja tallentaa kentän arvoksi **60**.

[![Matemaattisten lausekkeiden arviointi.](./media/gridMathExpression-07-25-2022.gif)](./media/gridMathExpression-07-25-2022.gif)

Jos haluat, että järjestelmä tunnistaa arvon lausekkeena, aloita arvo yhtäsuuruusmerkillä (**=**). Lisätietoja tuetuista operaattoreista ja syntaksista on kohdassa [Tuetut matemaattiset symbolit](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

Versiosta 10.0.29 lähtien mahdollisuus arvioida numeerisissa ohjausobjekteissa olevia matemaattisia lausekkeita on laajennettu, ja se on nyt käytettävissä myös ruudukon ulkopuolella.

## <a name="grouping-tabular-data"></a>Taulukkomuotoisten tietojen ryhmittely
Yrityskäyttäjien on usein suoritettava tiedoille ad-hoc-analyyseja. Vaikka tämä analyysi voidaan tehdä viemällä tiedot Microsoft Exceliin ja käyttämällä pivot-taulukoita, **Ryhmittely ruudukoissa** -toimintoa (joka on erillinen uuden ruudukon ohjausominaisuus), käyttäjät voivat järjestää taulukkomuotoiset tiedot mielenkiintoisilla tavoilla talous- ja toimintosovelluksia käyttäen. Koska tämä ominaisuus laajentaa **Lasketut arvot** -ominaisuutta, **Ryhmittely** mahdollistaa yksityiskohtaisia tietoja koskevat tiedot antamalla ryhmätasolla lasketut arvot (esimerkiksi välisummat).

[![Tietojen ryhmittely ruudukossa.](./media/grids-groupingWithTotals.png)](./media/grids-groupingWithTotals.png)

Jos haluat käyttää tätä toimintoa, napsauta hiiren kakkospainikkeella saraketta, jota haluat käyttää ryhmittelyperusteena ja valitse **Ryhmittele tämän sarakkeen perusteella**. Tämä toiminto lajittelee tiedot valitun sarakkeen mukaan, lisää uuden **Ryhmittelyperuste**-sarakkeen ruudukon alkuun ja lisää otsikkorivit kunkin ryhmän alkuun. Nämä otsikkorivit sisältävät seuraavat tiedot kustakin ryhmästä:

- Ryhmän tietojen arvo 
- Sarakkeen nimi (nämä tiedot ovat erityisen hyödyllisiä silloin, kun käytössä on useita ryhmittelytasoja)
- Tämän ryhmän tietorivien määrä
- Minkä tahansa konfiguroidun sarakkeen lasketut arvot (esimerkiksi välisummat, jos sarake on määritetty näyttämään kokonaissumma)

Kun [Tallennetut näkymät](saved-views.md) on käytössä, voit tallentaa ryhmittelyn niiden sivujen näkymän osana, joiden avulla voit tallentaa kyselyitä näkymiin. Esimerkiksi ne, joilla on suuren näkymän valitsimet. Lisätietoa on [Näkymien välillä vaihtaminen](saved-views.md#switching-between-views) -osiossa. 

### <a name="multiple-levels-of-grouping"></a>Useita ryhmittelytasoja
Kun olet ryhmitellyt tiedot yhden sarakkeen mukaan, voit ryhmitellä tiedot eri sarakkeen mukaan valitsemalla **Ryhmittele tämän sarakkeen mukaan** halutussa sarakkeessa. Tämä prosessi voidaan toistaa, kunnes ryhmittelyssä on viisi sisäkkäistä tasoa, mikä on suurin tuettu syvyys. Tässä vaiheessa et voi enää ryhmitellä lisäsarakkeiden mukaan.

Voit milloin tahansa poistaa ryhmittelyn mistä tahansa sarakkeesta napsauttamalla saraketta hiiren kakkospainikkeella ja valitsemalla **Pura ryhmittely**. Voit myös poistaa ryhmittelyn kaikista sarakkeista valitsemalla **Ruudukon asetukset** ja sitten **Pura kaikki ryhmittelyt**.

### <a name="sorting-grouped-data"></a>Ryhmiteltyjen tietojen lajitteleminen
Kun olet ryhmitellyt tiedot yhden tai useamman sarakkeen mukaan, voit vaihtaa minkä tahansa ryhmittelysarakkeen lajittelusuunnan vastaavan sarakkeen otsikon kautta. 

Jos lajittelet ei-ryhmitellyn sarakkeen, ryhmittely jää ennalleen. Tiedot lajitellaan kunkin ryhmän sisällä valitun sarakkeen mukaan.

### <a name="expanding-and-collapsing-groups"></a>Ryhmien laajentaminen ja kutistaminen
Tietojen alkuperäisessä ryhmittelyssä ryhmät ovat laajennettuina. Voit luoda tiedoista yhteenvetonäkymiä kutistamalla yksittäisiä ryhmiä. Vaihtoehtoisesti voit käyttää ryhmän laajentamista ja kutistamista, jos haluat auttaa tiedoissa siirtymisessä. Jos haluat laajentaa tai kutistaa ryhmän, valitse vastaavan ryhmän otsikkorivin kaksoisnuolikuvakkeen (>) painike. Huomaa, että eri ryhmien laajennus- tai kutistustilaa **ei** tallenneta mukautuksessa.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Rivien valitseminen ja valinnan poistaminen ryhmätasolla
Voit valita nopeasti ryhmän kaikki rivit tai poistaa niiden valinnan valitsemalla vastaavan ryhmän otsikkorivin valintaruudun. Tämä on samanlainen toiminto kuin rivien valitseminen (tai valinnan poistaminen) ruudukossa. Ryhmän otsikkorivin valintaruutu vaikuttaa aina nykyisen valinnan tilaan kyseisen ryhmän riveillä. Näin siitä huolimatta, onko valittuna kaikki rivit, osa riveistä tai ei yhtään riviä.

### <a name="hiding-column-names"></a>Sarakkeiden nimien piilottaminen
Kun ryhmittelet tietoja, oletusarvo on sarakkeen nimen näkyminen ryhmän otsikkorivillä. Voit valita, haluatko supistaa sarakkeen nimen ryhmän otsikkorivillä valitsemalla **Ruudukkovalinnat** > **Piilota ryhmän sarakkeen nimi**.

### <a name="grouping-on-date-and-time-columns"></a>Päivämäärä- ja aikasarakkeiden ryhmittely
Kun ryhmittelet Päivämäärä- tai Päivämäärä/aika-kenttiä, voit ryhmitellä tiedot vuoden, kuukauden tai päivän mukaan. Vastaavan otsikkorivin ryhmä "arvo" vastaa kyseisen kentän muotoa. Lisäksi DateTime- ja Time-kentät voi ryhmitellä tunnin, minuutin tai sekunnin mukaan.

> [!IMPORTANT]
> Käyttäjät eivät voi tällä hetkellä lisätä ryhmittelysaraketta sen jälkeen, kun he ovat ryhmitelleet päivämäärä- tai aikasarakkeen segmentissä.

## <a name="freezing-columns"></a>Sarakkeiden kiinnittäminen
Osa ruudukon sarakkeista voi olla kontekstin kannalta niin tärkeitä, ettei niitä haluta vierittää pois näkyvistä. Näiden sarakkeiden arvojen kannattaa sen sijaan olla aina näkyvissä. **Jäädytä ruudukon sarakkeet** -toiminto antaa tämän joustavuuden käyttäjille. 

[![Sarakkeiden lukitseminen ruudukossa.](./media/gridFreezingColumns-07-25-2022.gif)](./media/gridFreezingColumns-07-25-2022.gif)

Sarake kiinnitetään napsauttamalla sarakkeen otsikkoa kakkospainikkeella ja valitsemalla sitten **Kiinnitä sarake**. Kun tämä vaihe viimeistellään ensimmäisen kerran, valitusta sarakkeesta tulee ensimmäisen sarake eikä sitä vieritetä pois näkyvistä. Tämän jälkeen kiinnitettävät sarakkeet lisätään viimeksi kiinnitetyn sarakkeen oikealle puolelle. Vakiosiirtotoiminnolla voi järjestää kiinnitettyjen sarakkeiden järjestyksen uudelleen tarpeen mukaan. Kiinnitettyjä sarakkeita ei kuitenkaan voi siirtää niin, että ne näkyvät kiinnittämättömien sarakkeiden joukossa. Kiinnittämättömiä sarakkeita ei vastaavasti voi siirtää niin, että ne näkyvät kiinnitettyjen sarakkeiden joukossa.

Sarakkeen kiinnitys poistetaan napsauttamalla lukitun sarakkeen otsikkoa kakkospainikkeella ja valitsemalla sitten **Poista sarakkeen kiinnitys**. 

Huomaa, että uuden ruudukon rivivalinta ja rivin tilasarakkeet on aina kiinnitetty kahtena ensimmäisenä sarakkeena. Tämä tarkoittaa, että nämä sarakkeet ovat aina näkyvissä käyttäjille, kun ne lisätään ruudukkoon, riippumatta vaakasuuntaisesta vierityssijainnista ruudukossa. Näiden kahden sarakkeen järjestystä ei voi muuttaa.

## <a name="autofit-column-width"></a>Sarakeleveyden automaattinen sovittaminen
Kuten Excelissä käyttäjät voivat automaattisesti pakottaa sarakkeen koon muuttamisen sen sisällön perusteella, joka sarakkeessa näkyy. Kaksoisnapauta (tai kaksoisnapsauta) sarakkeen koonmuuttokahvoja. Vaihtoehtoisesti voit laittaa kohdistuksen sarakkeen otsikkoon ja valita sitten **A**-näppäimen (automaattista sovitusta varten).

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Miten otan uuden ruudukonhallinnan käyttöön omassa ympäristössäni? 

**Uusi ruudukon ohjausobjekti** -toiminto on käytettävissä suoraan ominaisuuksien hallinnassa missä tahansa ympäristössä. Kun ominaisuus on käytössä ominaisuuksien hallinnassa, kaikki myöhemmät käyttäjäistunnot käyttävät uutta ruudukon ohjausobjektia. 

Tämä ominaisuus oli oletusarvoisesti käytössä versiossa 10.0.21. Se on tulossa pakolliseksi lokakuussa 2022.

## <a name="developer-topics"></a>Kehittäjän aiheet

### <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Kehittäjä] Uuden ruudukon käyttämisen kieltäminen yksittäissivuilta 
Jos organisaatiossa havaitaan sivu, jolla on ongelmia käyttää uutta ruudukkoa, ohjelmistorajapinnan avulla voi sallia yksittäisen lomakkeen käyttää vanhaa ruudukon ohjausobjektia samalla, kun sallitaan muun järjestelmän käyttää uutta ruudukon ohjausobjektia. Jos haluat kieltää yksittäiseltä sivulta uuden ruudukon käyttämisen, lisää seuraava kutsuviesti `super()` lomakkeen menetelmään `run()`.

```this.forceLegacyGrid();```

Tämä ohjelmointirajapinta vanhentuu lopulta, jotta tämä vanha ruudukon ohjausobjekti voidaan poistaa käytöstä. Se on kuitenkin käytettävissä vähintään 12 kuukauden ajan sen poiston jälkeen. Jos jokin ongelma edellyttää tämän ohjelmointirajapinnan käyttöä, ilmoita siitä Microsoftille.

#### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Sivun pakottaminen käyttämään uutta ruudukkoa sen jälkeen, kun ruudukon käyttöä ei hyväksytty aiemmin
Jos yksittäinen sivu on jätetty pois uudesta ruudukosta, uusi ruudukko halutaan ehkä myöhemmin ottaa uudelleen käyttöön, kun taustalla olevat ongelmat on ratkaistu. Se tehdään yksinkertaisesti poistamalla `forceLegacyGrid()`-kutsu. Muutos tulee voimaan vasta, kun jokin seuraavista tapahtuu:

- **Ympäristön ottaminen uudelleen käyttöön**: kun ympäristö päivitetään ja otetaan uudelleen käyttöön, ne sivut sisältävä taulukko, jotka eivät ole ottaneet uutta taulukkoa (FormControlReactGridState) käyttöön, tyhjennetään automaattisesti.
- **Taulukon manuaalinen tyhjentäminen**: Kehitysskenaarioissa FormControlReactGridState-taulukon tyhjentämiseen ja AOS:n uudelleenkäynnistämiseen on käytettävä SQL:ää. Tämä toimintojen yhdistelmä nollaa niiden sivujen välimuistiin tallennuksen, jotka eivät ole ottaneet uutta ruudukkoa käyttöön:

### <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Kehittäjä] Yksittäisten ruudukoiden poisvalitseminen Järjestelmän ennakoiva kirjoitus -toiminnosta
Jotkin skenaariot eivät toimi hyvin ruudukon *Järjestelmän ennakoiva kirjoitus* -ominaisuuden kanssa. (Esimerkiksi jokin koodi, joka laukeaa, kun rivi tarkistetaan, aiheuttaa tietolähdetutkimusta, ja tutkimus voi tämän jälkeen aiheuttaa vahvistamattomien muokkausten vahingoittumisen aiemmin luoduilla riveillä.) Jos organisaatiosi havaitsee tällaisia skenaarioita, käytettävissä on sovellusliittymä, jonka avulla kehittäjä voi poisvalita yksittäisen ruudukon asynkronisesta rivitarkistuksesta ja palauttaa sen vanhaan toimintoon.

Kun asynkroninen rivitarkistus poistetaan käytöstä ruudukossa, käyttäjät eivät voi luoda uutta riviä tai siirtyä ruudukon eri riville, kun nykyisellä rivillä on oikeellisuustarkistusongelmia. Tämän toimenpiteen sivuvaikutuksena tauluja ei voi liittää Excelistä talous- ja toimintosovellusten ruudukkoihin.

Jos haluat kieltää ruudukolta asynkronisen rivitarkistuksen käyttämisen, lisää seuraava kutsu `super()`-kohdan jälkeen lomakkeen `run()`-menetelmään.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Tämä kutsu tulee kutsua vain poikkeustapauksissa, eikä se saa olla kaikkien ruudukoiden normi.
> - Tätä sovellusliittymää ei suositella käyttöön otettavaksi suorituksen aikana lomakkeen lataamisen jälkeen.

### <a name="developer-size-to-available-width-columns"></a>[Kehittäjä] Size-to-available-width -sarakkeet
Jos sovellu kehittäjä määrittää **widthmode**-ominaisuuden arvoksi **SizeToAvailable** uudessa ruudukossa oleville sarakkeille, näillä sarakkeilla on aluksi sama leveys kuin niillä olisi, jos ominaisuuden arvona olisi **SizeToContent**. Ne kuitenkin venyvät käyttämään kaiken ruudukon sisällä olevan leveyden. Jos useiden sarakkeiden ominaisuuden arvoksi on määritetty **SizeToAvailable**, kyseiset sarakkeet jakavat ruudukossa käytettävissä olevan tilan. Jos käyttäjä kuitenkin muuttaa jonkin tällaisen sarakkeen kokoa manuaalisesti, sarake muuttuu staattiseksi. Se pysyy samanlevyisenä eikä enää laajene käyttämään ruudukossa olevaa ylimäärästä leveyttä.

### <a name="developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key"></a>[Kehittäjä] Sarakkeen määrittäminen, jossa alkuperäinen kohdistus vastaanotetaan, kun uusia rivejä luodaan alanuolinäppäimellä
Kuten kohdassa [Erot, kun tietoja syötetään ennen järjestelmää](#differences-when-entering-data-ahead-of-the-system) mainittiin, Järjestelmän ennakoiva kirjoitus -ominaisuus on käytössä ja käyttäjä luo uuden rivin **alanuoli** näppäintä käyttäen, oletustoiminta on uuden rivin ensimmäisen sarakkeen kohdistus. Tämä kokemus voi olla eri kuin kokemus vanhassa ruudukossa tai kun **Uusi**-painike on valittu.

Käyttäjät ja organisaatiot voivat luoda tallennettuja näkymiä, jotka on optimoitu tietojen syöttöä varten. (Voit esimerkiksi järjestää sarakkeet uudelleen siten, että ensimmäinen sarake on sarake, josta haluat aloittaa tietojen syötön.) Lisäksi version 10.0.29 jälkeen organisaatiot voivat muuttaa tätä toimintatapaa käyttäen **selectedControlOnCreate()**-menetelmää. Tämän menetelmän avulla kehittäjä voi määrittää sarakkeen, joka saa ensimmäisen kohdistuksen, kun uusi rivi luodaan **alanuoli** näppäimellä. Syötteenä tämä ohjelmointirajapinta ottaa sitä saraketta vastaavan ohjaustunnuksen, jonka olisi saatava alkuperäinen kohdistus.

### <a name="developer-handling-grids-with-non-react-extensible-controls"></a>[Kehittäjä] Ruudukoiden käsitteleminen ei-reaktiivisten laajennettavien ohjausobjektien avulla
Jos järjestelmä löytää ei-reaktiivisen laajennettavan ohjausobjektin ruudukon lataamisen aikana, järjestelmä hahmontaa vanhan ruudukon. Kun käyttäjä havaitsee tällaisen tilanteen ensimmäisen kerran, näyttöön tulee sivun päivitystarpeesta kertova sanoma. Tämän jälkeen tämä sivu lataa vanhan ruudukon automaattisesti ilman lisäilmoituksia käyttäjille seuraavaan järjestelmän päivitykseen asti. 

Tämä tilanne ratkeaa pysyvästi, jos laajennettavien ohjausobjektien tekijät luovat ruudukossa käytettävistä ohjausobjekteista reaktiivisia versioita.  Kehittämisen jälkeen ohjausobjektin X++-luokka voidaan varustaa **FormReactControlAttribute**-määritteellä. Näin määritetään reaktiivisen nipun sijainti kyseiseen ohjausobjektiin lataamista varten. Luokka `SegmentedEntryControl` on esimerkkinä.  

## <a name="known-issues"></a>Tunnetut ongelmat
Tässä osassa luettelo uuden ruudukko-ohjausobjektin tunnetuista ongelmista.

### <a name="open-issues"></a>Avoimet asiat
- Kun **Uusi ruudukon ohjausobjekti** -toiminto on otettu käyttöön, jotkin sivut jatkavat olemassa olevan ruudukon ohjausobjektin käyttämistä. Näin tapahtuu seuraavissa tilanteissa:
 
    - [Ratkaistu] Sivulla on korttiluettelo, joka hahmonnetaan käyttämällä useaa saraketta.
        - **Uusi ruudukon ohjausobjekti** tukee tätä korttiluettelotyyppiä versiosta 10.0.30 alkaen. Kaikki käyttö, joissa forceLegacyGrid() on mukana tätä tarkoitusta varten, voidaan poistaa. 
    - [Ratkaistu] Sivulla on ryhmitelty korttiluettelo.
        - **Uusi ruudukon ohjausobjekti** tukee ryhmiteltyjä korttiluetteloita versiosta 10.0.30 alkaen. Kaikki käyttö, joissa forceLegacyGrid() on mukana tätä tarkoitusta varten, voidaan poistaa. 
    - [Ratkaistu] Ruudukkosarake, jolla on ei-reaktiivinen laajennettava ohjausobjekti.
        - Laajennettavat ohjausobjektit voivat määrittää ohjausobjektin reaktiivisen version, joka ladataan, kun se sijoitetaan ruudukkoon. Se muokkaa ohjausobjektin määritystä tämän ohjausobjektin lataamiseksi ruudukossa käyttöä varten. Lisätietoja on vastaavassa kehittäjän osassa. 

    Kun käyttäjä havaitsee jonkin näistä tilanteista, näyttöön tulee sivun päivityksestä kertova sanoma. Kun tämä sanoma tulee näyttöön, sivu jatkaa aiemmin luodun ruudukon käyttämistä kaikille käyttäjille seuraavaan tuoteversiopäivitykseen asti. Näiden skenaarioiden parempi käsittely ja uuden ruudukon käyttäminen otetaan huomioon seuraavassa päivityksessä.

- [KB 4582758] Tietueet ovat epätarkkoja, kun zoomausta muutetaan arvosta 100 mihin tahansa muuhun prosenttiarvoon

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

