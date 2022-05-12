---
title: Ruudukon ominaisuudet
description: Tässä aiheessa kuvataan useita ruudukon ohjausobjektin tehokkaita ominaisuuksia. Uusi ruudukkotoiminto on otettava käyttöön näiden ominaisuuksien käyttämistä varten.
author: jasongre
ms.date: 04/25/2022
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
ms.openlocfilehash: 57133a853d1700b2d8ebb938f93af475410b82cb
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644354"
---
# <a name="grid-capabilities"></a>Ruudukon ominaisuudet

[!include [banner](../includes/banner.md)]

Uusi ruudukon ohjausobjekti sisältää useita hyödyllisiä ja tehokkaita ominaisuuksia, joilla voidaan parantaa käyttäjien tuottavuutta, kehittää mielenkiintoisempia näkymiä tiedoillesi ja hankkia merkityksellisiä tietoja datastasi. Tämä artikkeli käsittelee seuraavia ominaisuuksia: 

- Lasketaan kokonaissummia
- Järjestelmän ennakoiva kirjoitus
- Matemaattisten lausekkeiden arviointi 
- Taulukkomuotoisten tietojen ryhmittely (käytössä erikseen **Ryhmittely ruudukoissa** -toiminnossa)
- Sarakkeiden jäädyttäminen (otetaan käyttöön erikseen käyttämällä **Sarakkeiden jäädyttäminen ruudukoissa** -toimintoa)
- Sarakeleveyden automaattinen sovittaminen
- Venytettävät sarakkeet

## <a name="calculating-totals"></a>Lasketaan kokonaissummia
Taloushallinnon ja toimintojen sovelluksissa käyttäjät voivat tarkastella summia ruudukkojen numeeristen sarakkeiden alla. Nämä kokonaissummat näkyvät alatunnisteosassa ruudukon alareunassa. 

### <a name="showing-the-grid-footer"></a>Ruudukon alatunnisteen näyttäminen
Taloushallinnon ja toimintojen sovellusten jokaisen taulukkomuotoisen ruudukon alaosassa on alatunnistealue. Alatunniste voi näyttää arvokkaita tietoja, jotka liittyvät ruudukossa näkyviin tietoihin. Seuraavassa on joitakin esimerkkejä näistä tiedoista:

- Taulukossa vallittuna olevien rivien määrä (kun vähintään kaksi tietuetta on valittuna)
- Kokonaismäärät määritettyjen numeeristen sarakkeiden alla
- Tietojoukon rivimäärä 

Tämä alatunniste on oletusarvoisesti piilotettuna, mutta sen voi ottaa käyttöön. Jos haluat ruudukon alatunnisteen näkyviin, valitse **Ruudukon asetukset** ruudukon otsikosta ja valitse sitten **Näytä alatunniste** -asteus. Kun alatunniste otetaan käyttöön tietyssä ruudukossa, kyseinen asetus muistetaan, kunnes käyttäjä valitsee alatunnisteen piilottamisen. Voit piilottaa alatunnisteen valitsemalla **Ruudukon asetukset** -valikosta **Piilota alatunniste**.

### <a name="specifying-columns-with-totals"></a>Summia sisältävien sarakkeiden määritys
Yksikään sarake ei näytä kokonaissummia tällä hetkellä oletusarvoisesti. Sen sijaan tämä katsotaan yksivaiheiseksi määritystoiminnoksi, joka muistuttaa sarakkeiden leveyden muuttamista ruudukoissa. Kun määrität, että haluat nähdä sarakkeen summat, tämä asetus muistetaan, kun seuraavan kerran käyt sivulla.

Sarake voidaan määrittää näyttämään summaa kahdella tavalla: 

- Napsauta sitä saraketta, jonka summan haluat nähdä, hiiren kakkospainikkeella ja valitse **Laske sarake yhteen**. Tämä toiminto aiheuttaa seuraavat kolme tapahtumaa:

    1. Alatunniste tulee näkyviin. 
    2. Tämän sarakkeen katseluasetus tallennetaan. 
    3. Aloitetaan summan laskeminen tässä sarakkeessa ja kaikissa muissa sarakkeissa, joiden summa on määritetty laskettavaksi. Aika, joka vaaditaan näyttämään kokonaissummat, riippuu käytettävän tietokannan koosta.

- Kun alatunniste on näkyvissä, valitse **Näytä summa** sen sarakkeen alatunnistealueella, jonka summan haluat nähdä. Jos määritettyjä sarakkeita ei ole, **Näytä summa** -painike on käytettävissä kaikkien numeeristen sarakkeiden osalta. 

    Kun vähintään yksi sarake on määritetty summia varten, **Näytä summa** -painikkeet ovat käytettävästi vain osoittamalla tai kohdistamalla. **Näytä summa** -painikkeen valintatoiminto vain tallentaa tämän sarakkeen summan katselun asetukset niin, että asetuksia käytetään sivulla myös myöhemmin. Alatunnisteessa tämä tila ilmaistaan ajatusviivalla, joka näkyy sarakkeessa. (Vaihtoehtoisesti, jos tietojoukko on tarpeeksi pieni, summa näytetään heti.)

Jos teet virheen, etkä enää halua nähdä tietyn sarakkeen summaa, napsauta sitä hiiren kakkospainikkeella ja valitse **Piilota summa** tai valitse **Piilota summa** -painike kyseisen sarakkeen alatunnisteesta. Tämä valinta tallennetaan myös tulevia sivuvierailuja varten. 

### <a name="calculating-totals"></a>Lasketaan kokonaissummia
Kun tulet sivulle, jolla alatunniste on näkyvissä ja sarakkeita on jo määritetty summia varten, summat saattavat näkyä alatunnisteessa. Näkyminen riippuu sivun tietojoukon koosta. Jos tietojoukko on riittävän pieni, summat ja tietojoukon rivien määrä näytetään automaattisesti. Jos alatunnisteessa on ajatusviivoja niiden sarakkeiden alla, jotka on määritetty summia varten, tietojoukko on liian suuri sille, että järjestelmä pystyisi näyttämään summat välittömästi. Tällöin summien laskeminen vaatii erillisiä toimia. Nämä summat saadaan laskettua napsauttamalla alatunnisteen **Laske**-painiketta tai napsauttamalla hiiren kakkospainikkeella haluttua saraketta ja valitsemalla **Laske sarake yhteen**.

Jos laskeminen kestää liian kauan, voit peruuttaa toiminnon valitsemalla **Peruuta**-painikkeen. Joskus tietojoukko on liian suuri summien laskemiseen (organisaation määrittämä raja) ja sinua pyydetään suodattamaan tietosi tarkemmin. 

> [!NOTE]
> Järjestelmänvalvojat voivat muokata summan laskennassa käytettävissä olevien tietueiden rajaa muuttamalla **Kunkin ruudukon paikallisen tietueen enimmäismäärä** -parametria **Asiakkaan suorituskykyasetukset** -sivulla. Oletusarvo on 25 000 tietuetta. Järjestelmänvalvojien tulee olla varovaisia muuttaessaan tätä arvoa, koska liian suuri arvo voi kuluttaa käyttäjän laitteen käytettävissä olevan muistin. Suosituksena on, että tietueita on enintään 50 000.   

Kokonaissummat päivittyvät automaattisesti, kun päivität, poistat tai luot rivejä tietojoukossa.

## <a name="typing-ahead-of-the-system"></a>Järjestelmän ennakoiva kirjoitus
Monissa liiketoimintaskenaarioissa tietojen nopea syöttäminen järjestelmään on erittäin tärkeää. Aiemmin käyttäjät voivat muuttaa tietoja vain nykyisellä rivillä, ennen kuin uusi ruudukko-ohjausobjekti otettiin käyttöön. Ennen kuin he voivat luoda uuden rivin tai vaihtaa toiselle riville, heidän oli pakko odottaa, että järjestelmä tarkisti mahdolliset muutokset onnistuneesti. Kun yritetään lyhentää aikaa, jonka käyttäjät odottavat näiden vahvistusten valmistumista, ja parantaa käyttäjien tuottavuutta, uusi ruudukko säätää nämä vahvistukset niin, että ne ovat asynkronisia. Tämän vuoksi käyttäjä voi siirtyä muihin riveihin ja tehdä muutoksia, kun edellisen rivin oikeellisuustarkistus odottaa. 

Tämän uuden toiminnon tukemiseksi rivitilan sarakkeen oikealle puolelle on lisätty uusi sarake rivin tilalle, kun ruudukko on muokkaustilassa. Tämä sarake ilmaisee jonkin seuraavista tiloista:

- **Tyhjä** – Ei tilaa kuvaa ilmaisee, että järjestelmä on tallentanut rivin onnistuneesti.
- **Käsittely odottaa** – Tämä tila ilmaisee, että palvelin ei ole vielä tallentanut rivin muutoksia, vaan ne ovat käsiteltävien muutosten jonossa. Ennen kuin suoritat toimenpiteitä ruudukon ulkopuolella, sinun on odotettava kaikkien odottavien muutosten käsittelemistä. Lisäksi näiden rivien teksti on kursivoitu rivien tallentamattoman tilan ilmaisemiseksi. 
- **Virheellinen tila** – Tämä tila ilmaisee, että rivin käsittelyn aikana käynnistettiin jokin varoitus tai sanoma, ja se on voinut estää järjestelmää tallentamasta muutoksia kyseiseen riviin. Vanhassa ruudukossa joutui palaamaan riville korjaamaan ongelman heti, mikäli tallennus ei onnistunut. Uusi ruudukko kuitenkin ilmoittaa, että vahvistusongelma ilmeni, mutta voit päättää, milloin haluat korjata kaikki rivin ongelmat. Kun olet valmis korjaamaan ongelman, voit siirtää kohdistuksen manuaalisesti takaisin riville. Vaihtoehtoisesti voit valita **Korjaa tämä ongelma** -toiminnon. Tämä toimenpide siirtää kohdistuksen välittömästi riville, jolla on ongelma, ja voit tehdä muokkauksia ruudukon sisä- tai ulkopuolelle. Huomaa, että seuraavien odottavien rivien käsittely pysäytetään, kunnes tämä vahvistusvaroitus on ratkaistu. 
- **Keskeytetty** – Tämä tila ilmaisee, että palvelimen käsittely keskeytetään, koska rivin oikeellisuustarkistus käynnistää ponnahdusikkunan, joka edellyttää käyttäjän toimia. Koska käyttäjä saattaa kirjoittaa tietoja toiselle riville, ponnahdusikkuna ei tule heti näkyviin kyseiselle käyttäjälle. Sen sijaan se esitetään, kun käyttäjä päättää jatkaa käsittelyä. Tähän tilaan liittyy ilmoitus, joka kertoo käyttäjälle tilanteesta. Ilmoitus sisältää **Jatka käsittelyä** -toiminnon, joka käynnistää ponnahdusikkunan.

Kun käyttäjät syöttävät tietoja ennen palvelimen käsittelemisen paikkaa, he voivat odottaa, että tietojen syöttämisessä ilmenee joitakin heikentymistä, kuten hakujen puuttumista, ohjaustason tarkistamista ja oletusarvojen syöttämistä. Käyttäjiä, jotka tarvitsevat avattavan luettelon löytääkseen arvon, kehotetaan odottamaan, että palvelin on kiinni nykyiselle riville. Ohjaustason oikeellisuustarkistus ja oletusarvojen määritys tapahtuvat myös, kun palvelin käsittelee rivin.

### <a name="pasting-from-excel"></a>Liittäminen Excelistä
Käyttäjät ovat aina voineet viedä tietoja taloushallinnon ja toimintojen sovelluksista Microsoft Exceliin käyttämällä **Vie Exceliin** -mekanismia. Mahdollisuus syöttää tietoja ennen järjestelmää mahdollistaa kuitenkin sen, että uusi ruudukko tukee taulujen kopioimista Excelistä ja liittämistä suoraan taloushallinnon ja toimintojen sovellusten ruudukkoihin. Ruudukon solu, josta liittämistoiminto käynnistetään, määrittää, mihin kopioitu taulukko alkaa liittää. Kopioidun taulun sisältö korvaa ruudukon sisällön lukuun ottamatta kahta tapausta:

- Jos kopioidun taulukon sarakkeiden määrä ylittää ruudukon jäljellä olevien sarakkeiden määrän, alkaen liittämissijainnista, käyttäjälle ilmoitetaan, että ylimääräiset sarakkeet on ohitettu. 
- Jos kopioidun taulukon rivien määrä ylittää ruudukon rivien määrän alkaen liittämissijainnista, aiemmin luodut solut korvataan liitetystä sisällöstä ja kopioidun taulukon ylimääräiset rivit lisätään uusina riveinä ruudukon alaosaan. 

## <a name="evaluating-math-expressions"></a>Matemaattisten lausekkeiden arviointi
Tuottavuutta tehostaakseen käyttäjät voivat antaa matemaattisia kaavoja ruudukon numeerisiin soluihin. Heidän ei tarvitse tehdä laskelmia järjestelmän ulkopuolisissa sovelluksissa. Jos esimerkiksi syötät **=15\*4** ja painat sitten **sarkainnäppäintä** ja siirryt pois kentästä, järjestelmä arvioi lausekkeen ja tallentaa kentän arvoksi **60**.

Jos haluat, että järjestelmä tunnistaa arvon lausekkeena, aloita arvo yhtäsuuruusmerkillä (**=**). Lisätietoja tuetuista operaattoreista ja syntaksista on kohdassa [Tuetut matemaattiset symbolit](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Taulukkomuotoisten tietojen ryhmittely
Yrityskäyttäjien on usein suoritettava tiedoille ad-hoc-analyyseja. Vaikka tämä voidaan tehdä viemällä tiedot Microsoft Exceliin ja käyttämällä pivot-taulukoita, **Ryhmittely ruudukoissa** -toimintoa (joka on erillinen uuden ruudukon ohjausominaisuus), käyttäjät voivat järjestää taulukkomuotoiset tiedot mielenkiintoisilla tavoilla taloushallinnon ja toimintojen sovelluksia käyttäen. Koska tämä toiminto laajentaa **Summat**-toimintoa, **Ryhmittely** mahdollistaa myös merkityksellisten tietojen hankkimisen datasta tarjoamalla ryhmätason välisummia.

Jos haluat käyttää tätä toimintoa, napsauta hiiren kakkospainikkeella saraketta, jota haluat käyttää ryhmittelyperusteena ja valitse **Ryhmittele tämän sarakkeen perusteella**. Tämä toiminto lajittelee tiedot valitun sarakkeen mukaan, lisää uuden **Ryhmittelyperuste**-sarakkeen ruudukon alkuun ja lisää otsikkorivit kunkin ryhmän alkuun. Nämä otsikkorivit sisältävät seuraavat tiedot kustakin ryhmästä:

- Ryhmän tietojen arvo 
- Sarakkeen nimi (nämä tiedot ovat erityisen hyödyllisiä silloin, kun käytössä on useita ryhmittelytasoja)
- Tämän ryhmän tietorivien määrä
- Kaikkien summattavaksi määritettyjen sarakkeiden välisummat

Kun [Tallennetut näkymät](saved-views.md) on käytössä, voit tallentaa ryhmittelyn niiden sivujen näkymän osana, joiden avulla voit tallentaa kyselyitä näkymiin. Esimerkiksi ne, joilla on suuren näkymän valitsimet. Lisätietoa on [Näkymien välillä vaihtaminen](saved-views.md#switching-between-views) -osiossa. 

### <a name="multiple-levels-of-grouping"></a>Useita ryhmittelytasoja
Kun olet ryhmitellyt tiedot yhden sarakkeen mukaan, voit ryhmitellä tiedot eri sarakkeen mukaan valitsemalla **Ryhmittele tämän sarakkeen mukaan** halutussa sarakkeessa. Tämä prosessi voidaan toistaa, kunnes ryhmittelyssä on viisi sisäkkäistä tasoa, mikä on suurin tuettu syvyys. Tässä vaiheessa et voi enää ryhmitellä lisäsarakkeiden mukaan.

Voit milloin tahansa poistaa ryhmittelyn mistä tahansa sarakkeesta napsauttamalla saraketta hiiren kakkospainikkeella ja valitsemalla **Pura ryhmittely**. Voit myös poistaa ryhmittelyn kaikista sarakkeista valitsemalla **Ruudukon asetukset** ja sitten **Pura kaikki ryhmittelyt**.

### <a name="sorting-grouped-data"></a>Ryhmiteltyjen tietojen lajitteleminen
Kun olet ryhmitellyt tiedot yhden tai useamman sarakkeen mukaan, voit vaihtaa minkä tahansa ryhmittelysarakkeen lajittelusuunnan vastaavan sarakkeen otsikon kautta. 

Ei-ryhmiteltyjen sarakkeiden lajittelutapa määräytyy tuoteversion mukaan:

- Versiossa 10.0.24 ja sitä aiemmissa versioissa, jos lajittelet ei-ryhmiteltyjen sarakkeiden mukaan, ryhmittely poistetaan kaikista sarakkeista ja tiedot lajitellaan valitun sarakkeen mukaan. 
- Versiossa 10.0.25 ja sitä myöhemmissä versioissa, jos lajittelet ei-ryhmiteltyjen sarakkeiden mukaan, ryhmittely säilyy koskemattomana ja tiedot lajitellaan kunkin ryhmän sisällä valitun sarakkeen mukaan.

### <a name="expanding-and-collapsing-groups"></a>Ryhmien laajentaminen ja kutistaminen
Tietojen alkuperäisessä ryhmittelyssä ryhmät ovat laajennettuina. Voit luoda tiedoista yhteenvetonäkymiä kutistamalla yksittäisiä ryhmiä. Vaihtoehtoisesti voit käyttää ryhmän laajentamista ja kutistamista, jos haluat auttaa tiedoissa siirtymisessä. Jos haluat laajentaa tai kutistaa ryhmän, valitse vastaavan ryhmän otsikkorivin kaksoisnuolikuvakkeen (>) painike. Huomaa, että eri ryhmien laajennus- tai kutistustilaa **ei** tallenneta mukautuksessa.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Rivien valitseminen ja valinnan poistaminen ryhmätasolla
Voit valita nopeasti ryhmän kaikki rivit tai poistaa niiden valinnan valitsemalla vastaavan ryhmän otsikkorivin valintaruudun. Tämä on samanlainen toiminto kuin rivien valitseminen (tai valinnan poistaminen) ruudukossa. Ryhmän otsikkorivin valintaruutu vaikuttaa aina nykyisen valinnan tilaan kyseisen ryhmän riveillä. Näin siitä huolimatta, onko valittuna kaikki rivit, osa riveistä tai ei yhtään riviä.

### <a name="hiding-column-names"></a>Sarakkeiden nimien piilottaminen
Kun ryhmittelet tietoja, oletusarvo on sarakkeen nimen näkyminen ryhmän otsikkorivillä. Voit valita, haluatko supistaa sarakkeen nimen ryhmän otsikkorivillä valitsemalla **Ruudukkovalinnat** > **Piilota ryhmän sarakkeen nimi**.

### <a name="grouping-on-date-and-time-columns"></a>Päivämäärä- ja aikasarakkeiden ryhmittely
Alkaen versiosta 10.0.24 Date- tai DateTime-kentissä vaihtoehto on lisätty ryhmään vuoden, kuukauden tai päivän mukaan. Vastaavan otsikkorivin ryhmä "arvo" vastaa kyseisen kentän muotoa. Lisäksi DateTime- ja Time-kentät voi ryhmitellä tunnin, minuutin tai sekunnin mukaan. 

## <a name="freezing-columns"></a>Sarakkeiden kiinnittäminen
Osa ruudukon sarakkeista voi olla kontekstin kannalta niin tärkeitä, ettei niitä haluta vierittää pois näkyvistä. Näiden sarakkeiden arvojen kannattaa sen sijaan olla aina näkyvissä. **Jäädytä ruudukon sarakkeet** -toiminto antaa tämän joustavuuden käyttäjille. 

Sarake kiinnitetään napsauttamalla sarakkeen otsikkoa kakkospainikkeella ja valitsemalla sitten **Kiinnitä sarake**. Kun tämä vaihe viimeistellään ensimmäisen kerran, valitusta sarakkeesta tulee ensimmäisen sarake eikä sitä vieritetä pois näkyvistä. Tämän jälkeen kiinnitettävät sarakkeet lisätään viimeksi kiinnitetyn sarakkeen oikealle puolelle. Vakiosiirtotoiminnolla voi järjestää kiinnitettyjen sarakkeiden järjestyksen uudelleen tarpeen mukaan. Kiinnitettyjä sarakkeita ei kuitenkaan voi siirtää niin, että ne näkyvät kiinnittämättömien sarakkeiden joukossa. Kiinnittämättömiä sarakkeita ei vastaavasti voi siirtää niin, että ne näkyvät kiinnitettyjen sarakkeiden joukossa.

Sarakkeen kiinnitys poistetaan napsauttamalla lukitun sarakkeen otsikkoa kakkospainikkeella ja valitsemalla sitten **Poista sarakkeen kiinnitys**. 

Huomaa, että uuden ruudukon rivivalinta ja rivin tilasarakkeet on aina kiinnitetty kahtena ensimmäisenä sarakkeena. Tämä tarkoittaa, että nämä sarakkeet ovat aina näkyvissä käyttäjille, kun ne lisätään ruudukkoon, riippumatta vaakasuuntaisesta vierityssijainnista ruudukossa. Näiden kahden sarakkeen järjestystä ei voi muuttaa.

## <a name="autofit-column-width"></a>Sarakeleveyden automaattinen sovittaminen
Kuten Excelissä käyttäjät voivat automaattisesti pakottaa sarakkeen koon muuttamisen sen sisällön perusteella, joka sarakkeessa näkyy. Voit tehdä tämän kaksoisnapsauttamalla sarakkeen koonmuuttokahvoja tai kohdistamalla sarakkeen otsikkoon ja painamalla **A** (automaattinen sovittaminen). Tämä ominaisuus on käytettävissä versiosta 10.0.23 alkaen.

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Miten otan uuden ruudukonhallinnan käyttöön omassa ympäristössäni? 

**Uusi ruudukon ohjausobjekti** -toiminto on käytettävissä suoraan ominaisuuksien hallinnassa missä tahansa ympäristössä. Kun ominaisuus on käytössä ominaisuuksien hallinnassa, kaikki myöhemmät käyttäjäistunnot käyttävät uutta ruudukon ohjausobjektia. 

Tämä ominaisuus otetaan oletusarvoisesti käyttöön versiosta 10.0.21 lähtien ja sen on määrä tulla pakolliseksi lokakuussa 2022.  

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Kehittäjä] Uuden ruudukon käyttämisen kieltäminen yksittäissivuilta 
Jos organisaatiossa havaitaan sivu, jolla on ongelmia käyttää uutta ruudukkoa, ohjelmistorajapinnan avulla voi sallia yksittäisen lomakkeen käyttää vanhaa ruudukon ohjausobjektia samalla, kun sallitaan muun järjestelmän käyttää uutta ruudukon ohjausobjektia. Jos haluat kieltää yksittäiseltä sivulta uuden ruudukon käyttämisen, lisää seuraava kutsuviesti `super()` lomakkeen menetelmään `run()`.

```this.forceLegacyGrid();```

Tämä ohjelmointirajapinta on käytössä kunnes uusi ruudukon ohjausobjekti tulee pakolliseksi. Muutos on tällä hetkellä kohdistettu lokakuulle 2022. Jos jokin ongelma edellyttää tämän ohjelmointirajapinnan käyttöä, ilmoita siitä Microsoftille.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Sivun pakottaminen käyttämään uutta ruudukkoa sen jälkeen, kun ruudukon käyttöä ei hyväksytty aiemmin
Jos yksittäinen sivu on jätetty pois uudesta ruudukosta, uusi ruudukko halutaan ehkä myöhemmin ottaa uudelleen käyttöön, kun taustalla olevat ongelmat on ratkaistu. Se tehdään yksinkertaisesti poistamalla `forceLegacyGrid()`-kutsu. Muutos tulee voimaan vasta, kun jokin seuraavista tapahtuu:

- **Ympäristön ottaminen uudelleen käyttöön**: kun ympäristö päivitetään ja otetaan uudelleen käyttöön, ne sivut sisältävä taulukko, jotka eivät ole ottaneet uutta taulukkoa (FormControlReactGridState) käyttöön, tyhjennetään automaattisesti.
- **Taulukon manuaalinen tyhjentäminen**: Kehitysskenaarioissa FormControlReactGridState-taulukon tyhjentämiseen ja AOS:n uudelleenkäynnistämiseen on käytettävä SQL:ää. Tämä toimintojen yhdistelmä nollaa niiden sivujen välimuistiin tallennuksen, jotka eivät ole ottaneet uutta ruudukkoa käyttöön:

## <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Kehittäjä] Yksittäisten ruudukoiden poisvalitseminen Järjestelmän ennakoiva kirjoitus -toiminnosta
Jotkin skenaariot eivät toimi hyvin ruudukon *Järjestelmän ennakoiva kirjoitus* -ominaisuuden kanssa. (Esimerkiksi jokin koodi, joka laukeaa, kun rivi tarkistetaan, aiheuttaa tietolähdetutkimusta, ja tutkimus voi tämän jälkeen aiheuttaa vahvistamattomien muokkausten vahingoittumisen aiemmin luoduilla riveillä.) Jos organisaatiosi havaitsee tällaisia skenaarioita, käytettävissä on sovellusliittymä, jonka avulla kehittäjä voi poisvalita yksittäisen ruudukon asynkronisesta rivitarkistuksesta ja palauttaa sen vanhaan toimintoon.

Kun asynkroninen rivitarkistus poistetaan käytöstä ruudukossa, käyttäjät eivät voi luoda uutta riviä tai siirtyä ruudukon eri riville, kun nykyisellä rivillä on oikeellisuustarkistusongelmia. Tämän toimenpiteen sivuvaikutuksena tauluja ei voi liittää Excelistä taloushallinnon ja toimintojen sovellusten ruudukkoihin.

Jos haluat kieltää ruudukolta asynkronisen rivitarkistuksen käyttämisen, lisää seuraava kutsu `super()`-kohdan jälkeen lomakkeen `run()`-menetelmään.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Tämä kutsu tulee kutsua vain poikkeustapauksissa, eikä se saa olla kaikkien ruudukoiden normi.
> - Tätä sovellusliittymää ei suositella käyttöön otettavaksi suorituksen aikana lomakkeen lataamisen jälkeen.

## <a name="developer-size-to-available-width-columns"></a>[Kehittäjä] Size-to-available-width -sarakkeet
Jos sovellu kehittäjä määrittää **widthmode**-ominaisuuden arvoksi **SizeToAvailable** uudessa ruudukossa oleville sarakkeille, näillä sarakkeilla on aluksi sama leveys kuin niillä olisi, jos ominaisuuden arvona olisi **SizeToContent**. Ne kuitenkin venyvät käyttämään kaiken ruudukon sisällä olevan leveyden. Jos useiden sarakkeiden ominaisuuden arvoksi on määritetty **SizeToAvailable**, kyseiset sarakkeet jakavat ruudukossa käytettävissä olevan tilan. Jos käyttäjä kuitenkin muuttaa jonkin tällaisen sarakkeen kokoa manuaalisesti, sarake muuttuu staattiseksi. Se pysyy samanlevyisenä eikä enää laajene käyttämään ruudukossa olevaa ylimäärästä leveyttä.

## <a name="known-issues"></a>Tunnetut ongelmat
Tässä osassa luettelo uuden ruudukko-ohjausobjektin tunnetuista ongelmista.

### <a name="open-issues"></a>Avoimet asiat
- Kun **Uusi ruudukon ohjausobjekti** -toiminto on otettu käyttöön, jotkin sivut jatkavat olemassa olevan ruudukon ohjausobjektin käyttämistä. Näin tapahtuu seuraavissa tilanteissa:
 
    - Sivulla on korttiluettelo, joka hahmonnetaan käyttämällä useaa saraketta.
    - Sivulla on ryhmitelty korttiluettelo.
    - Ruudukkosarake, jolla on ei-reaktiivinen laajennettava ohjausobjekti.

    Kun käyttäjä havaitsee jonkin näistä tilanteista, näyttöön tulee sivun päivityksestä kertova sanoma. Kun tämä sanoma tulee näyttöön, sivu jatkaa aiemmin luodun ruudukon käyttämistä kaikille käyttäjille seuraavaan tuoteversiopäivitykseen asti. Näiden skenaarioiden parempi käsittely ja uuden ruudukon käyttäminen otetaan huomioon seuraavassa päivityksessä.

- [KB 4582758] Tietueet ovat epätarkkoja, kun zoomausta muutetaan arvosta 100 mihin tahansa muuhun prosenttiarvoon
- [KB 4592012] Odottamaton asiakasohjelman virhe IE11:ssä liitettäessä useita rivejä Excelissä

    Microsoft ei ole korjaamassa tätä ongelmaa


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
