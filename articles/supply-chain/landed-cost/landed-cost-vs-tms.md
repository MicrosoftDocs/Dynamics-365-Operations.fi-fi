---
title: Aiheutunut kustannus vs. kuljetustenhallinta
description: 'Microsoft Dynamics 365 Supply Chain Management tarjoaa kaksi eri moduulia kuljetusten kanssa työskentelyä varten: kuljetustenhallinnan (TMS) ja aiheutuneen kustannuksen. Tässä artikkelissa on yhteenveto toiminnoista, jotka moduuleilla ovat yhteisiä, ja korostaa niiden väliset erot.'
author: Weijiesa
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 40489ff8d8683d19a5f726546cc4c43cc3e7a05d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905918"
---
# <a name="landed-cost-vs-transportation-management"></a>Aiheutunut kustannus vs. kuljetustenhallinta

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management tarjoaa kaksi eri moduulia kuljetusten kanssa työskentelyä varten: **kuljetustenhallinnan** (TMS) ja **aiheutuneen kustannuksent**. Tässä artikkelissa on yhteenveto toiminnoista, jotka moduuleilla ovat yhteisiä, ja korostaa niiden väliset erot. Voit käyttää näitä tietoja päättääksesi, mikä moduuli sopii parhaiten liiketoimintakäytäntöihin. Saattaa olla, että jotkin liiketoimintakäytännöt toimivat paremmin kuljetustenhallinnan kanssa, kun taas toiset toimivat parhaiten aiheutuneessa kustannuksessa. Sen jälkeen voit liiketoimintavaatimusten mukaan valita yksinomaan yhden moduulin tai voit yhdistää nämä kaksi moduulia.

Tämä artikkeli ei käsittele kattavasti kaikkia kummankaan moduulin ominaisuuksia. Sen sijaan se korostaa käytettävissä olevat toiminnot liittyen tuotteiden kuljetukseen toimittajalta yrityksesi varastoon, jossa se voidaan kuluttaa.

## <a name="terminology-reference-data-and-reporting-differences"></a>Termit, viitetiedot ja raportointierot

### <a name="terminology-comparison"></a>Termien vertailu

Kuljetustenhallinta ja aiheutunut kustannus käyttävät samankaltaisissa käsitteissä eri termejä. Seuraavassa taulukossa on yhteenveto näistä termeistä ja niiden käytöstä kahdessa moduulissa.

| Kuljetustenhallinnan termi | Aiheutuneen kustannuksen termi | Muistiinpanot |
|----------|------------------|-------|
| **Kuormitus**<p>*Kuormitus* on kokoelma toimituksia, jotka kuljetetaan samanaikaisesti samassa kuljetusyksikössä (kuten kuorma-autossa tai laivassa). Kuormitukset voivat olla saapuvia tai lähteviä.</p> | **Merikuljetus**<p>Yleensä *merikuljetus* on yksi alus, joka kulkee yhden *matkan*. Merikuljetus voi sisältää useita *kuljetuskontteja*, ja se voi sisältää myös organisaatiosi eri yritysten saapuvia tilauksia. Merikuljetukset voivat olla vain saapuvia.</p> | Kuljetustenhallinta käyttää myös termiä *merkikuljetuksen numero*, joka viittaa tietokenttään, johon voit kirjoittaa tunnisteen. Kuljetustenhallinnan kenttään ei kuitenkaan liity toimintoja, eikä se liity aiheutuneen kustannuksen *merikuljetus*-käsitteeseen. |
| **Reitti**<p>*Reitti* on kuljetuksen fyysinen polku lähtöpisteestä kohteeseen.</p> | **Matka**<p>*Matka* on kuljetuksen fyysinen polku lähtöpisteestä kohteeseen. Jokainen merikuljetus on liitettävä matkaan.</p> | |
| **Reittisegmentit**<p>Reitillä voi olla useita *reittisegmenttejä*, joista jokainen edustaa matkan vaihetta. Reitti voi sisältää useita rahdinkuljettajia tai palveluja, joista jokainen on reittisegmentti.</p> | **Etapit**<p>Jokaisella matkalla voi olla useita *etappeja*, joista jokainen edustaa matkan vaihetta. Etappi voi olla osa kuljetusta, verojen käsittelyä tai muuta toimintaa.</p> | |
| **Kontit**<p>*Kontti* voi olla mikä tahansa pakkaus, jota kuljetustenhallinta käyttää.</p> | **Kuljetuskontit**<p>*Kuljetuskontti* on kirjaimellisesti fyysinen kuljetuskontti, joka tunnetaan konttilaivoista.</p> | |
| **Kauppatavarakoodit**<p>Kuljetustenhallinnassa (ja muissa paikoissa Supply Chain Managementissa) *kauppatavarakoodit* yksilöivät kauppatavaratyypit. Ne voivat vaikuttaa tariffiin, vaarallisten materiaalien käsittelyyn jne.</p> | **Kauppatavarakoodit**<p>Aiheutuneessa kustannuksessa *kauppatavarakoodit* on määritetty yrityksen tasolla. Niitä käytetään pääasiassa raportoinnissa.</p> | Aiheutunut kustannus voi käyttää myös kauppatavarakoodeja, joita käytetään kuljetustenhallinnassa ja Supply Chain Managementin paikoissa. Aiheutuneen kustannuksen kauppatavarakoodeja käyttää kuitenkin vain aiheutunut kustannus. |

### <a name="some-reference-data-isnt-shared"></a>Joitakin viitetietoja ei jaeta

Kuljetustenhallinta ja aiheutunut kustannus eivät jaa viitetietoja esimerkiksi kustannusasetuksille, matkoille ja etapeille. Jos käytät molempia moduuleita, sinun on luotava jakamattomat viitetiedot uudelleen.

### <a name="intercompany-reports-dont-work-with-goods-in-transit"></a><a name="intercompany-reports"></a>Konsernin sisäiset raportit eivät toimi kuljetettavien tuotteiden kanssa

Seuraavat raportit eivät toimi aiheutuneen kustannuksen tarjoaman kuljetettavien tuotteiden ominaisuuden yhteydessä:

- [Konsernin sisäisten kuljetettavien tuotteiden summat -raportti](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)
- [Konsernin sisäisten kuljetettavien tuotteiden summat -raportti](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)

Näissä raporteissa oletetaan, että tuotteet siirtyvät kuljetukseen heti myynnin pakkausluettelon annon jälkeen ja että ne otetaan varastoon kuljetuksesta vastaanoton yhteydessä. Kuljetettavia tuotteita ei kuitenkaan käsitellä tällä tavalla. Jos siis käytät kuljetettavien tuotteiden ja konsernin sisäisiä ominaisuuksia yhdessä, näiden molempien raporttien tulokset ovat virheelliset.

## <a name="using-the-two-modules-together"></a>Kahden moduulin käyttäminen yhdessä

Kuljetustenhallintaa voi käyttää sekä saapuvissa että lähtevissä toiminnoissa. Vaikka aiheutunut kustannus sisältää useimmat samat perustoiminnot kuin kuljetustenhallinta saapuvien toimintojen kohdalla, siinä on myös muutamia toimintoja enemmän. Siksi haluat ehkä käyttää kuljetustenhallintaa lähtevien toimintojen kohdalla ja aiheutunutta kustannusta saapuvien toimintojen yhteydessä.

Molempia moduuleita ei yleensä suositella käytettäväksi saapuville toiminnoille. Käytä moduulia, joka vastaa parhaiten tarpeitasi. Jos käytät näitä kahta moduulia yhdessä, lähdeasiakirjoja ei saa jakaa niiden välillä. Älä esimerkiksi käytä samaa ostotilausta sekä kuljetustenhallinnan että aiheutuneen kustannuksen kuormitukselle. Varmista erityisesti, ettet määritä järjestelmää luomaan saapuvia kuormituksia automaattisesti. Jos ostotilausten nimikkeet sisältyvät merikuljetukseen, niitä ei voi käsitellä osana kuormitusta.

## <a name="goods-in-transit"></a>Matkalla olevat tavarat

Yksi aiheutuneen kustannuksen pääominaisuuksista on sen kyky käsitellä kuljetettavia tuotteita. Kuljetettavien tuotteiden käsittely mahdollistaa taloudellisen omistuksen toimitetuista nimikkeistä, ennen kuin ne vastaanotetaan fyysistesti kohdevarastossa. Kuljetettavien tuotteiden käsittely on usein pakollista kansainvälisessä kaupassa.

### <a name="tms-goods-in-transit-features"></a>Kuljetustenhallinnan kuljetettavien tuotteiden ominaisuudet

Kuljetustenhallinta ei tällä hetkellä tue kuljetettavien tuotteiden käsittelyä.

### <a name="landed-cost-goods-in-transit-features"></a>Aiheutuneen kustannuksen kuljetettavien tuotteiden ominaisuudet

Kuljetettavien tuotteiden käsittely on aiheutuneen kustannuksen ensisijainen ominaisuus, ja se tarjoaa seuraavat toiminnot:

- **Kuljetettavien tuotteiden varastot** – Kuljetettavien tuotteiden varasto voidaan liittää jokaiseen varastoon Supply Chain Managementissa. Tuotteet siirretään kuljetettavien tuotteiden varastoon alkuperäisen ostotilauksen laskutuksen jälkeen. Fyysisesti varatut nimikkeet eivät ole käytettävissä kulutukseen, ennen kuin ne vastaanotetaan fyysiseen varastoonsa. Näin ollen voit ottaa tavaroiden taloudellisen omistajuuden laskuttamalla ostotilauksen.
- **Kuljetettavien tuotteiden kirjanpitotili** – Aiheutunut kustannus lisää ostotilauksen kirjausprofiiliin tietyn kirjanpidon kirjaustilin kuljetettavien tuotteiden käsittelyä varten. Kuljetettavien tuotteiden kirjanpitotili toimii tilinä, jonka tyyppi on "vastaanotetut mutta ei laskutetut tavarat". Kun alkuperäinen ostotilaus laskutetaan ja kuljetettavien tuotteiden tilaus luodaan, ostotilauksen suorakustannukset kirjataan kuljetettavien tuotteiden kirjanpitotilille, kunnes tuotteet vastaanotetaan lopullisessa fyysisessä sijainnissa.
- **Seurannan ohjauspäivitykset** – Kuljetettavien tuotteiden tilaukset tukevat aiheutuneen kustannuksen seurannan ohjaustoimintoa. Seurannan ohjauksen avulla voit päivittää tavaroiden odotetun saapumispäivän niiden kuljetuksen aikana. Seurannan ohjaus päivittää tämän jälkeen merikuljetukset ja niihin liittyvät ostotilausrivit. Odotettu toimituspäivä on tällöin käytettävissä pääsuunnittelua ja logistiikkaa varten.
- **Ylitys-/alitustapahtumien käynnistäminen** – Jos merikuljetuksen rivillä odotettujen tuotteiden ja varastoon vastaanotettujen todellisten tuotteiden välillä on varianssia, aiheutunut kustannut ratkaisee sen luomalla ylitys- tai alitustapahtumia. Tämän jälkeen voit hallita näitä tapahtumia haluamallasi tavalla joko ostotilauksen tai siirtokirjauskansion kautta. Ylitys- ja alitustapahtumat antavat linkin takaisin varianssin merikuljetukseen, alkuperäiseen ostotilaukseen ja uuteen siirtokirjauskansioon tai ostotilaukseen.
- **Kuljetettavien tuotteiden tilaukset** – Aiheutunut kustannus tuo käyttöön uuden lähdeasiakirjan, jota kutsutaan *kuljetettavien tuotteiden tilaukseksi*. Kuljetettavien tuotteiden tilauksen avulla voit laskuttaa alkuperäisen ostotilauksen ja ottaa nimikkeiden taloudellisen omistajuuden. Kun ostotilaus laskutetaan, uusi lähdeasiakirja luodaan kaikille ostotilausriveille, joissa on varastodimensioiden yhdistelmä. Tämän jälkeen tavarat siirretään fyysisesti kuljetettavien tuotteiden varastoon, jossa ne on fyysisesti varattu kuljetettavien tuotteiden tilausta vastaan eikä niitä voi kuluttaa, ellei kuljetettavia tuotteita ole vastaanotettu.

## <a name="miscellaneous-charges-and-shipment-costs"></a>Muut kulut ja lähetyskustannukset

Yksi tärkeimpiä tuotteiden lähetysten ja lähetysten hallinnan osa-alueita on lähetyksiin liittyvien yleiskustannusten tunnistaminen. Nämä yleiskustannukset eivät ole ostotilaukseen ja lähetykseen tai merikuljetukseen liittyviä suoria varastokustannuksia. Sen sijaan ne ovat lisäkustannuksia, jotka ovat lähtöisin tuotteiden siirrosta toimittajalta organisaatioon. Näihin kustannuksiin voivat sisältyä rahtikulut, jotka liittyvät tuotteiden lähetykseen fyysisestä sijainnista toiseen, tai verot, jotka liittyvät tuotteiden tuontiin ulkomaisilta toimittajilta.

Aiheutunut kustannus käsittelee näitä kustannuksia luomalla uudentyyppisen kustannusrakenteen, jota kutsutaan *automaattisiksi kustannuksiksi*. Kuljetustenhallinta käsittelee nämä kustannukset muiden kulujen toimintojen avulla.

### <a name="tms-charge-and-cost-features"></a>Kuljetustenhallinnan veloitus- ja kustannusominaisuudet

Kuljetustenhallinta käyttää muita kuluja asiaankuuluville lähdeasiakirjariveille kohdistettujen kuormituksen lisäkustannusten hallintaan. Nämä muut kulut voidaan määrittää joko ostotilausrivin tai ostotilauksen otsikon tasolla.

Kuljetustenhallinnassa muut kulut voidaan jakaa varaston painolla, tilavuudella tai määrällä. Kulut voidaan jakaa rahtimaksuilla tai lisämaksuilla. Lisäkehitystä tarvitaan, jotta kuljetustenhallinnassa voidaan käyttää ylimääräisiä jakomenetelmiä.

### <a name="landed-cost-charge-and-cost-features"></a>Aiheutuneen kustannuksen veloitus- ja kustannusominaisuudet

Aiheutunut kustannus tarjoa joukon kustannustoimintoja, jotka käsittelevät tuotteiden lähetykseen liittyviä lisäkustannuksia. Nämä kustannukset tunnetaan automaattisina kustannuksina, ja niitä käytetään lähetyksen ensimmäisen laskutuksen aikana käyttämällä arvioitua kustannussummaa. Jokaista kustannustyyppiä hallitaan omassa kirjauksessa. Kun todelliset yleiskustannusten laskut on kirjattu, arvioidut kustannukset päivitetään automaattisesti toteutuneiden kustannusten mukaan.

Lisäksi tuotteiden lähetykseen liittyvät yleiskustannukset voidaan laskuttaa merikuljetuksen aikana alkuperäsatamasta tai milloin tahansa tuotteiden vastaanoton jälkeen. Tämä ominaisuus mahdollistaa joustavammin tavaroiden kulutuksen.

Seuraavassa luettelossa on kuvattu joitakin aiheutuneen kustannuksen veloitus- ja kustannusominaisuuksiin liittyviä käsitteitä:

- **Kustannusalue** – Kustannukset ja veloitukset voidaan määrittää eri tasoille eli *kustannusalueille* merikuljetuksessa. Kustannukset voidaan ottaa käyttöön merikuljetuksen tasolla ja jakaa eri nimikkeeseen merikuljetuksessa. Lisäksi kustannuksia voidaan käyttää kontin, ostotilauksen, nimikkeen tai siirtotilauksen tasolla. Kutakin kustannusveloitusta voidaan hallita erikseen eri alueilla, ja ne voidaan jakaa nimikekustannusten mukaan.
- **Jakomenetelmät** – Aiheutuneessa kustannuksessa on käytettävissä useita jakomenetelmiä. Kustannusveloitukset voidaan jakaa määrän, dollarisumman, arvon, painon, tilavuuden, mitan tai käyttäjän määrittämän tilavuusmitan mukaan.
- **Selvitys/varianssinhallinta** – Kustannusveloitukset määritetään omaksi kustannuskoodityypiksi aiheutuneessa kustannuksessa. Kunkin kustannuskoodityypin avulla voit määrittää arvioitujen kustannusveloitusten selvitystilin sekä arvioitujen kustannusten ja toteutuneiden kustannusten varianssien jaksotus- ja ostohinnan varianssitilit. Kun arvioidut kustannukset kirjataan alustavasti, selvitystilille tulee saldo. Kun todelliset laskut on kirjattu, todelliset kustannusveloitukset kirjataan ja arvioidut kustannukset veloitetaan selvitystililtä.

## <a name="matching-freight-bills-and-invoices"></a>Täsmäytä rahtilaskut ja laskut

### <a name="tms-bill-and-invoice-matching-features"></a>Kuljetustenhallinnan kulujen ja laskun täsmäytyksen ominaisuudet

Kuljetustenhallinta voi täsmäyttää rahtilaskuja, jotka sisältävät arvioituja kustannuksia, ja laskuja todellisilla rahtikustannuksilla. Kyse voi olla sähköisestä laskusta tai paperilaskusta. Arvioitujen kustannusten ja toteutuneiden kustannusten täsmäytysvarianssi ei vaikuta varastonarvostukseen.

Lisätietoja on kohdassa [Rahdin täsmäytys kuljetustenhallinnassa](../transportation/reconcile-freight-transportation-management.md).

### <a name="landed-cost-bill-and-invoice-matching-features"></a>Aiheutuneen kustannuksen kulujen ja laskun täsmäytyksen ominaisuudet

Aiheutunut kustannus voi täsmäyttää rahtilaskut arvioituihin kustannusveloituksiin ja laskuttaa toteutuneet kustannukset arvioituihin kustannuksiin. Rahtikulut ovat laskutuksen yhteydessä laskukirjauskansiossa, ja arvioidut kustannukset poistetaan selvitystililtä. Lisäksi todelliset kustannusveloitukset kirjataan nimikkeen myytyjen tuotteiden kustannuksiin yhdessä arvioitujen kulujen ja todellisten kulujen varianssien kanssa. Tämän ansiosta laskutusprosessi on joustava.

## <a name="tracking"></a>Seuranta

Sekä kuljetustenhallinnan että aiheutuneen kustannuksen tärkeä ominaisuus on kyky seurata tavaroita ja tunnistaa, missä kohtaa matkaa ne ovat lähtöpisteestä lopulliseen kohdevarastoon. Seurannan avulla voit seurata ja päivittää tavaroiden sijaintia ja sitä, milloin niiden odotetaan saapuvan varastoon kulutusta varten. Tuotteiden tilan lisäksi matkan aikana aiheutunut kustannus tarjoaa odotetut ja toteutuneet päivämäärät matkan jokaiselle vaiheelle.

### <a name="tms-tracking-features"></a>Kuljetustenhallinnan seurantaominaisuudet

Kuljetustenhallinta sisältää rajallisia toimintoja saapuvien kuormitusten seurantaa varten. Se näyttää päivämäärät ja mahdollistaa integroinnin, joka mahdollistaa tarkan sijainnin löytämisen (esimerkiksi **Kuljetuksen tila** -sivulla).

Voit määrittää kullekin reittisegmentille arvioidut aikataulut ja saapumisajat.

### <a name="landed-cost-tracking-features"></a>Aiheutuneen kustannuksen seurantaominaisuudet

Aiheutunut kustannus voi antaa seurannan ohjauksen jokaiselle merikuljetukselle lähtösatamasta lopulliseen kohteeseen. Seurannan ohjaus määrittää merikuljetuksen tilan. Tila ilmaisee, onko merikuljetus merellä, tullitarkastuksessa vai paikallisessa toimituksessa matkalla lopulliseen varastoonsa. Tilan voi määrittää ostotilausrivin, kontin ja merikuljetuksen otsikon tasolla. Sen vuoksi ohjaus on eritellympää.

Lisäksi määritettyihin läpimenoaikoihin perustuva vahvistettu odotettu päivämäärä liitetään matkan jokaiseen vaiheeseen. Vahvistetut ja odotetut toimituspäivämäärät lisätään ostotilausriviin ja kuljetettavien tuotteiden tilauksiin, ja niitä voidaan käyttää pääsuunnittelussa ja logistiikassa. Odotettujen päivämäärien lisäksi toteutuneet päivämäärät voidaan päivittää. Sen jälkeen matkan seuraavat vaiheet päivitetään vastaavasti.

## <a name="multi-leg-journeys"></a>Usean etapin matkat

Matkan käsitteen avulla määritetään, missä vaiheessa tuotteet ovat prosessissa, ja se ohjaa tuotteiden tilaa kuljetettaessa. Tuotteet voivat käydä läpi useita matkan etappeja, ja voit liittää erilaisia kustannuksia tiettyyn etappiin. Esimerkkejä ovat aluksen merimatkan rahtikustannukset ja paikalliset kuljetuskustannukset tuotteiden kuljetuksessa satamasta kohteeseen.

### <a name="tms-multi-leg-journey-features"></a>Kuljetustenhallinnan monietappisen matkan ominaisuudet

Kuljetustenhallinnassa reitit voidaan jakaa reittisegmentteihin niin, että ne edustavat monietappista reittiä. Kuljetustenhallinta voi kohdistaa spot-hintoja ja lisämaksut yksittäisiin reittisegmentteihin.

Lisätietoja on kohdassa [Useita pysähdyksiä sisältävän rahdinkuljetusreitin suunnittelu](../transportation/plan-freight-transportation-routes-multiple-stops.md).

### <a name="landed-cost-multi-leg-journey-features"></a>Aiheutuneen kustannuksen monietappisen matkan ominaisuudet

Aiheutunut kustannus tarjoaa kehyksen tuotteiden siirtämiselle lähtöpisteestä kohteeseen eri etappien kautta, jotka ovat matkan pysähdyksiä tai vaiheita. Etapit yhdistetään luomaan matkamalleja, jotka määrittelevät, miten tuotteet siirtyvät toimittajalta organisaatioosi.

Voit määrittää jokaisessa matkan etapissa edelleen kunkin ostotilausrivin tilan sekä siihen liittyvät läpimenoajat. Kaikkien etappien yhdistetyn läpimenoajan avulla määritetään arvioitu toimituspäivä. Kuljetettavien tuotteiden käsittely on kuitenkin pakollisia monietappisilla matkoilla. Merikuljetuksen tuotteiden matkaa hallitaan aiheutuneeseen kustannukseen liittyvässä taulukossa.

## <a name="receiving-by-container"></a>Vastaanotto kontin mukaan

On tärkeää hallita, kuinka tuotteet jaetaan ja varastoidaan aluksessa. Aluksessa tuotteita voidaan säilyttää yhdessä kontissa tai useassa kontissa. Kun tuotteet vastaanotetaan, ne vastaanotetaan kontteihin, ja merikuljetuksen eri kontit voidaan ottaa vastaan eri aikoina tai eri päivinä.

Sekä kuljetustenhallinta että aiheutunut kustannus tarjoaa toimintoja tuotteiden vastaanottamisen hallintaan kontissa. Kuljetustenhallinta käyttää kuormitusten käsitettä kuljetuskonttiin liittyvien tuotteiden, ostotilausten ja siirtotilausten hallinnassa. Kuljetustenhallinta tukee vastaanottoa lähetysilmoituksen (ASN) kautta vastaanotetun pakkausrakenteen perusteella. Aiheutunut kustannus käyttää kuljetuskonttien käsitettä ostotilausten käsittelemiseen ja konttiin liittyvien yleiskustannusten hallintaan.

### <a name="tms-receiving-by-container-features"></a>Kuljetustenhallinnan vastaanotto kontin mukaan – ominaisuudet

Kuljetustenhallinta tukee saapuvia lähetysilmoituksia, kaikkia vastaanottovariantteja varastonhallinnan mobiilisovelluksen kautta sekä kaikkia vastaanottotapoja Supply Chain Management -asiakasohjelman kautta.

### <a name="landed-cost-receiving-by-container-features"></a>Aiheutuneen kustannuksen vastaanotto kontin mukaan – ominaisuudet

Tukeakseen vastaanottoa kontin mukaan aiheutunut kustannus luo kuljetuskonttitietueita ja liittää ostotilaukset tiettyyn kuljetuskonttiin käyttämällä konttitunnusta. Yleiskustannukset voidaan sitten liittää tähän kuljetuskonttiin ja jakaa niin, että ne liittyvät asianomaisiin ostotilauksiin.

Aiheutuneen kustannuksen kontit voidaan vastaanottaa uudentyyppisen vastaanoton avulla, jota kutsutaan *kuljetettavien tuotteiden vastaanotoksi* saapumisen kirjauskansioiden kautta tai mobiililaitteen vastaanoton kautta. Kun saapumisen kirjauskansioita käytetään, määrät voidaan alustaa kuljetettavien tuotteiden tilauksesta tai kontin alkuperäisistä ostotilausriveistä. Aiheutunut kustannus tarjoaa kaksi työtyyppiä vastaanottoon varastonhallinnan mobiilisovelluksen kautta.

Aiheutunut kustannus ei anna lähetysilmoitusta (ASN) tuotteiden sähköistä vastaanottoa varten. Lisäksi se ei tue varastonhallinnan mobiilisovelluksen työnkulkuja, jotka käsittelevät prosessikuormituksen vastaanottoa, rekisterikilven vastaanottoa tai yhdistetyn rekisterikilven vastaanottoa.

## <a name="rate-shopping-by-vendor"></a>Hintojen haku toimittajan mukaan

Hintojen haun ansiosta yritys voi valita kuljetustoimittajan alimman hinnan, nopeimman reitin tai molemmat huomioon otettavien yhdistelmien perusteella.

### <a name="tms-rate-shopping-features"></a>Kuljetustenhallinnan hintojen hakuominaisuudet

Kuljetustenhallinnassa voit tunnistaa saapuvien ja lähtevien tilausten toimittaja- ja reititysratkaisut. Voit esimerkiksi tunnistaa nopeimman reitin tai edullisimman hinnan lähetykselle.

Kuljetustenhallinta tarjoaa täyden hintojen haun ja rahtioptimoinnin hinnan ja reitin työtilan kautta, joustavat hinnoitteluvaihtoehdot hinnoittelumoduulin kautta, hinnoittelumoduulin ohjelmointirajapinnan integrointiin ulkoisten osapuolten kanssa sekä tilavuuspainon tuen.

Lisätietoja on kohdassa [Kuljetustenhallintamoduulit](../transportation/transportation-management-engines.md).

### <a name="landed-cost-rate-shopping-features"></a>Aiheutuneen kustannuksen hintojen hakuominaisuudet

Aiheutunut kustannus tarjoaa vain rajoitetun tuen hintojen haulle toimittajan mukaan. Vaikka voitkin määrittää huolitsijan arvot, aiheutettu kustannus ei vertaile niitä usean toimittajan välillä.

## <a name="driver-check-incheck-out-with-appointment-scheduling"></a>Kuljettajan sisään- ja uloskuittaus tapaamisen ajoittamisella

Kuljettajan sisään- ja uloskuittausominaisuuksien avulla järjestelmä voi valvoa saapumisia ja estää ruuhkautumisen laitureilla.

### <a name="tms-driver-check-incheck-out-features"></a>Kuljetustenhallinnan kuljettajan sisään- ja uloskuittausominaisuudet

Kuljetustenhallinnassa voit luoda *tapaamisia*. Tapaaminen edustaa tapahtumia, jotka tapahtuvat laiturilla ostotilauksen vastaanottamiseksi, myyntitilauksen lähettämiseksi tai sisään tulevan tai lähtevän kuorman käsittelemiseksi tiettynä päivänä ja tiettyyn aikaan. Tapaamiset varmistavat, että laiturit ovat käytettävissä tavaroiden lastaamista ja purkua varten. Tapaamiset voivat estää tilanteet, joissa useat rahdinkuljettajat saapuvat sijaintiin samanaikaisesti.

Järjestelmä sallii kuljettajien sisäänkuittauksen tietyllä laiturin ovella.

### <a name="landed-cost-driver-check-incheck-out-features"></a>Aiheutuneen kustannuksen kuljettajan sisään- ja uloskuittausominaisuudet

Aiheutunut kustannus voi tallentaa kontin toimituspäivän ja -ajan arviot.

## <a name="transfer-orders-and-additional-costs"></a>Siirtotilaukset ja lisäkustannukset

Yritysten on usein pystyttävä siirtämään tavaroita varastosta toiseen. Kun tällainen siirto tapahtuu, kustannukset liitetään siihen ja haluat ehkä tunnistaa nämä kustannukset. Aiheutuneessa kustannuksessa siirtotilauksia voi lisätä merikuljetukseen tai alukseen tuotteiden liikkeiden seuraamiseksi varastosta tai sijainnista toiseen, toimitusajan ja odotetun toimituspäivän arvioimiseksi sekä yleiskustannusten lisäämiseksi tuotteiden siirtoon.

### <a name="tms-transfer-order-cost-features"></a>Kuljetustenhallinnan siirtotilauksen kustannusominaisuudet

Kuljetustenhallinta tukee siirtoihin liitettyjen rahtimaksujen luontia. Vaikka näitä kuluja voi tarkastella siirtotilauksen avulla, aiheutunutta kustannusta ei lisätä nimikkeen kuluihin. Rahtitäsmäytystä tuetaan luomalla näihin kuluihin perustuva rahtilasku. Tämän jälkeen rahtikirja täsmäytetään toimittajan rahtilaskuun.

### <a name="landed-cost-transfer-order-cost-features"></a>Aiheutuneen kustannuksen siirtotilauksen kustannusominaisuudet

Aiheutuneen kustannuksen avulla voit lisätä siirtotilauksia alukseen tai merikuljetukseen. Tällä tavoin voit lisätä lähetyskustannukset merikuljetukseen varastotilityksiksi siirtotilauksen vastaanoton yhteydessä. Yleiskustannukset voidaan laskuttaa todellisista kustannuksista, ja niitä seurataan merikuljetuksen suhteen myytyjen tuotteiden kustannusten päivittämiseksi. Vaikka siirtotilaukset eivät käytä kuljetettavien tuotteiden käsittelyä vakiojulkaisussa, ne voidaan lisätä merikuljetuksiin. Aiheutunut kustannus lisätään kunkin nimikkeen kokonaiskustannuksiin.