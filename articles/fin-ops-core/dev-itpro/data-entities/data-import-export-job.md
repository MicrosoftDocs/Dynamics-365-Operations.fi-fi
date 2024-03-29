---
title: Tietojen tuonti- ja vientityöt – yleiskatsaus
description: Tietojenhallinnan työtilan avulla voit luoda ja hallita tietojen tuonti- ja vientitehtäviä.
author: peakerbl
ms.date: 08/26/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfd06c30ae09a175862810a0c85399358a65fdb0
ms.sourcegitcommit: 43a0fb019bc67c00c39c2778343ba89924c3322c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/12/2022
ms.locfileid: "9671455"
---
# <a name="data-import-and-export-jobs-overview"></a>Tietojen tuonti- ja vientityöt – yleiskatsaus

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Voit luoda ja hallita tietojen tuonti- ja vientitehtäviä **Tietojen hallinta** -työtilassa. Oletusarvon mukaan tietojen tuonti- ja vientiprosessi luo väliaikaisen taulun kullekin yksikölle kohdetietokantaan. Väliaikaisten taulujen avulla voit tarkistaa, puhdistaa tai muuntaa tiedot ennen niiden siirtämistä.

> [!NOTE]
> Tässä artikkelissa oletetaan, että tunnet [tietoyksiköt](data-entities.md).

## <a name="data-importexport-process"></a>Tietojen tuonti- ja vientiprosessi
Nämä ovat ohjeet tietojen tuontiin tai viemiseen.

1. Luo tuonti- tai vientityö, jossa suoritetaan seuraavat tehtävät:

    - Määritä projektin luokka.
    - Tunnista tuotavat tai vietävät yksiköt.
    - Määritä työn tietojen muoto.
    - Aseta yksiköt mielekkääseen järjestykseen niin, että ne käsitellään loogisissa ryhmissä.
    - Määritä, käytetäänkö väliaikaisia tauluja.

2. Vahvista, että lähde- ja kohdetiedot liitetään oikein.
3. Tarkista tuonti- tai vientityön turvallisuus.
4. Suorita tuonti- tai vientityö.
5. Vahvista, että työ suoritettiin odotetulla tavalla tarkastamalla työhistoria.
6. Tyhjennä väliaikaiset taulut.

Loput tämän artikkelin osat sisältävät tarkempia tietoja kustakin prosessin vaiheesta.

> [!NOTE]
> Saat uusimmat edistymistiedot näkyviin päivittämällä tietojen tuonti- ja vientilomakkeen päivityskuvakkeella. Selaintason päivitystä ei suositella, koska se keskeyttää mahdolliset erien ulkopuoliset tuonti- ja vientityöt.

## <a name="create-an-import-or-export-job"></a>Luo tuonti- tai vientityö
Tietojen tuonti- tai vientityön voi suorittaa useita kertoja.

### <a name="define-the-project-category"></a>Määritä projektin luokka
Suosittelemme, että valitset tuonti- tai vientityölle haluamasi projektiluokan huolella. Voit hallita liittyviä töitä projektiluokkien avulla.

### <a name="identify-the-entities-to-import-or-export"></a>Tunnista tuotavat tai vietävät yksiköt
Voit lisätä tiettyjä yksiköitä tuonti- tai vientityöhön tai käyttää mallia. Mallit täyttävät työn yksikköluettelolla. **Käytä mallia** -vaihtoehtoa voi käyttää, kun työlle on annettu nimi ja se on tallennettu.

### <a name="set-the-data-format-for-the-job"></a>Määritä työn tietojen muoto
Valitse yksikölle tuonnin tai viennin tietomuoto sitä valitessasi. Muodot määritetään **Lähdeasetukset**-ruudussa. Lähdetietojen muodossa yhdistyy **Tyyppi**, **Tiedostomuoto**, **Rivin erotin** ja **Sarakkeen erotin**. Vaikka määritteitä on muitenkin, näiden ymmärtäminen on olennaista. Seuraava taulukko sisältää kelvolliset yhdistelmät.

> [!NOTE]
> Excel-tiedostomuoto ei ole tällä hetkellä käytettävissä Government Community Cloudin (GCC) tietojenhallinnan työtilassa.

| Tiedostomuoto            | Rivin tai sarakkeen erotin                       | XML-tyyli                 |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-–                     |
| XML                    | \-–                                      | XML-elementin XML-määrite |
| Erotin, kiinteä leveys | Pilkku, puolipiste, sarkain, pystyviiva, kaksoispiste | \-–                     |

> [!NOTE]
> On tärkeää valita oikea arvo asetuksille **Rivin erotin**, **Sarakkeen erotin** ja **Tekstimäärite**, jos **Tiedostomuoto**-asetuksen arvona on **Erotettu**. Varmista, että tiedot eivät sisällä erottimena tai määritteenä käytettyä merkkiä, koska tämä voi johtaa virheisiin tuonnissa ja viennissä.

> [!NOTE]
> Jos tiedostomuoto on XML-perustainen, varmista, että käytät vain sallittuja merkkejä. Lisätietoja kelvollista merkeistä on kohdassa [Sallitut merkit XML 1.0:ssä](https://www.w3.org/TR/2006/REC-xml-20060816/Overview.html#charsets/). XML 1.0 ei salli ohjausmerkkejä lukuun ottamatta sarkaimia, rivinvaihtoja ja rivisyöttöjä. Virheellisiä merkkejä ovat esimerkiksi hakasulkeet, aaltosulkeet ja kenoviivat. 

Käytä tietojen tuomiseen tai viemiseen Unicodea erityisen koodisivun asemesta. Tämä auttaa antamaan kaikkein yhdenmukaisimmat tulokset ja eliminoimaan tietojenhallintatöiden epäonnistumisen, koska niissä on Unicode-merkkejä. Järjestelmän määrittämillä lähdetietomuodoilla, jotka käyttävät Unicodea, on lähteen nimessä **Unicode**. Unicode-muotoa käytetään valitsemalla Unicode-koodauksen ANSI-koodisivu **Koodisivuksi** **Alueasetukset**-välilehdessä. Valitse jokin seuraavista Unicode-koodisivuista:

| Koodisivu | Näyttönimi                |
|-----------|-----------------------------|
| 1 200      | Unicode                     |
| 12000     | Unicode (UTF-32)            |
| 12001     | Unicode (UTF-32 Big-Endian) |
| 1201      | Unicode (Big-Endian)        |
| 65000     | Unicode (UTF-7)             |
| 65001     | Unicode (UTF-8)             |

Lisätietoja koodisivuista on kohdassa [Koodisivun tunnukset](/windows/win32/intl/code-page-identifiers/).

### <a name="sequence-the-entities"></a>Aseta yksiköt sarjaan
Yksiköt voi järjestää tietomallissa tai tuonti- ja vientitöissä. Kun suoritat työn, joka sisältää useamman tietoyksikön, varmista, että yksiköt on järjestetty oikein. Yksiköt järjestetään ensisijaisesti siten, että voit käsitellä kaikki yksiköiden väliset toiminnalliset riippuvuudet. Jos yksiköillä ei ole toiminnallisia riippuvuuksia, ne voidaan ajoittaa tuotavaksi tai vietäväksi rinnakkain. 

#### <a name="execution-units-levels-and-sequences"></a>Suoritusyksiköt, -tasot ja -sarjat
Yksiköiden tuonti- tai vientijärjestystä valvovat ensin suoritusyksikön arvot, sitten suoritusyksikön taso ja lopulta sarja.

- Eri suoritusyksiköissä olevat yksiköt käsitellään rinnakkain.
- Saman suoritusyksikön yksiköt käsitellään rinnakkain, jos ne ovat samalla tasolla.
- Kunkin tason yksiköt käsitellään tason mukaisen järjestysnumeron perusteella.
- Kun yksi taso on käsitelty, käsitellään seuraava taso.

#### <a name="resequencing"></a>Uudelleenjärjestys
Voit halutessasi järjestellä yksiköt uudelleen seuraavissa tilanteissa:

- Jos kaikkiin muutoksiin käytetään yksittäistä tietotyötä, voit käyttää uudelleenjärjestysvaihtoehtoja ja optimoida siten koko työn suoritusajan. Tällöin voit käyttää suoritusyksikköä moduulin edustajana, tasoa moduulin toimintoalueen edustajana ja sarjaa yksikön edustajana. Käyttämällä tätä menetelmää voit käyttää kaikkia moduuleja samanaikaisesti, mutta voit silti käyttää moduulin järjestystä. Jos haluat varmistaa, että rinnakkaiset vaiheet onnistuvat, kaikki riippuvuudet on otettava huomioon.
- Jos käytössä on useita tietotöitä (esimerkiksi yksi työ kullekin moduulille), voit optimoida työtä muuttamalla järjestelytoiminnolla yksiköiden tasoa ja järjestystä.
- Jos riippuvuussuhteita ei ole, voidaan yksiköt järjestellä optimaalisesti eri suoritusyksiköihin.

**Uudelleenjärjestely**-valikko on käytettävissä, kun useita yksiköitä on valittuna. Voit järjestellä yksiköitä uudelleen suoritusyksikön, -tason tai -sarjan perusteella. Voit määrittää lisäyksen valittujen yksiköiden uudelleenjärjestelylle. Kunkin yksikön valittu yksikkö-, taso- ja/tai järjestysnumero päivitetään lisäyksen mukaisesti.

#### <a name="sorting"></a>Lajittelu
Voit käyttää **Lajitteluperuste**-vaihtoehtoa, jos haluat tarkastella yksikköluetteloa järjestyksessä.

### <a name="truncating"></a>Katkaiseminen
Tuontiprojekteissa voit katkaista entiteettien tietueet ennen tuontia. Tästä on hyötyä, jos tietueet on tuotava tyhjiin tauluihin. Oletusarvon mukaan tämä asetus ei ole käytössä.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Vahvista, että lähde- ja kohdetiedot liitetään oikein
Määritys on toiminto, jota käytetään sekä tuonti-, että vientitöissä.

- Tuontityössä määrityksellä kuvataan, mistä lähdetiedoston sarakkeista tehdään sarakkeita väliaikaisessa taulukossa. Järjestelmä voi siten määrittää, mitkä lähdetiedoston sarakkeet tulee kopioida mihinkin väliaikaisen taulukon sarakkeisiin.
- Vientityössä määrityksellä kuvataan, mistä väliaikaisen taulukon (eli lähteen) sarakkeista tehdään sarakkeita kohdetiedostossa.

Jos väliaikaisen taulukon ja kohdetiedoston sarakenimet vastaavat, järjestelmä luo määrityksen automaattisesti nimien perusteella. Jos nimet eivät vastaa, sarakkeita ei määritetä automaattisesti. Tällöin sinun on tehtävä määritys valitsemalla **Näytä yhdistämismääritykset** -vaihtoehto tietotyön yksikössä.

Järjestelmässä on kaksi määritysnäkymää: **Yhdistämismääritysten visualisointi**, joka on oletusnäkymä, ja **Yhdistämistiedot**. Punainen tähti (\*) osoittaa kohteen kaikki pakolliset kentät. Nämä kentät on yhdistettävä, ennen kuin voit käsitellä yksikköä. Muiden kenttien yhdistämisen voi poistaa tarvittaessa, kun käsittelet yksikköä. Voit poistaa kentän yhdistämisen valitsemalla sen joko **Yksikkö**- tai **Lähde**-sarakkeessa ja valitsemalla sitten **Poista valinta**. Tallenna muutokset **Tallenna**-painikkeella ja sulje sivun palataksesi projektiin. Voit käyttää samaa prosessia muokataksesi kenttien yhdistämismäärityksiä lähteen ja väliaikaisen taulukon välillä tuonnin jälkeen.

Voit luoda yhdistämismäärityksen sivulla valitsemalla **Luo lähteen yhdistämismääritys**. Luotu määritys toimii kuin automaattinen määritys. Tämän vuoksi yhdistämättömät kentät on yhdistettävä manuaalisesti.

![Tietotyypin yhdistämismääritys.](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>Tarkista tuonti- tai vientityön turvallisuus
Voit rajoittaa **Tietojenhallinta**-työtilan käyttöoikeutta, jotta muut kuin järjestelmänvalvojat voivat käyttää vain tiettyjä töitä. Käyttöoikeus tietotyöhön tarkoittaa täyttä käyttöoikeutta kyseisen työn suoritushistoriaan sekä väliaikaisiin tauluihin. Sinun on siis varmistettava, että käyttöoikeudet on asetettu asianmukaisesti, kun luot tietotyön.

### <a name="secure-a-job-by-roles-and-users"></a>Työn suojaaminen roolien ja käyttäjien perusteella
**Soveltuvat roolit** -valikkoa voidaan käyttää työn rajoittamiseen tietyille käyttöoikeusrooleille. Vain kyseisiin rooleihin kuuluvat käyttäjät voivat käyttää työtä.

Voit myös rajoittaa työn tietyille käyttäjille. Kun suojaat työn käyttäjien perusteella roolien sijaan, voit hallita käyttöoikeuksia tarkemmin, jos roolilla on useita käyttäjiä.

### <a name="secure-a-job-by-legal-entity"></a>Työn suojaaminen yrityksen perusteella
Tietotyöt ovat yleisiä. Näin ollen, jos tietotyö on luotu ja käytössä yrityksessä, työ on näkyvissä kaikissa muissakin järjestelmän yrityksissä. Tämän oletustoiminta voi olla haluttua tietyissä sovelluksen skenaarioissa. Organisaatio voi esimerkiksi tuoda laskujen tietoja tietoyksiköiden ja tarjota keskitetyn laskujen käsittelyryhmä, joka vastaa organisaation kaikkien osastojen laskuvirheiden käsittelystä. Tällöin on hyvä antaa kaikkien keskitetyn laskujen käsittelyryhmän jäsenten käyttää kaikkien yritysten laskujen tuontitöitä. Oletusasetus täyttää täten tarpeen yrityksen näkökulmasta.

Organisaatio voi kuitenkin haluta yrityskohtaiset laskujen käsittelyryhmät. Tässä tapauksessa yrityksen ryhmällä tulee olla käyttöoikeus ainoastaan oman yrityksensä laskujen tuontityöhön. Nämä vaatimukset täytetään määrittämällä tietotöille yrityspohjaiset käyttöoikeudet työn sisäisestä **Soveltuvat yritykset** -valikosta. Kun määritykset on tehty, käyttäjät näkevät vain työt, jotka ovat käytettävissä yrityksessä, johon he ovat kirjautuneena. Nähdäkseen toisen yrityksen työt, käyttäjien on vaihdettava kyseiseen yritykseen.

Työ voidaan suojata samaan aikaan rooli-, käyttäjä- ja yritysperusteisesti.

## <a name="run-the-import-or-export-job"></a>Suorita tuonti- tai vientityö
Voit suorittaa työn kerran valitsemalla **Tuo**- tai **Vie**-painikkeen, kun olet määrittänyt työn. Voit määrittää toistuvan työn valitsemalla **Luo toistuva tietotyö**.

> [!NOTE]
> Tuonti- tai vientityö voidaan suorittaa valitsemalla **Tuo**- tai **Vie**-painike. Tällöin erätyö ajoitetaan suoritettavaksi vain kerran. Työtä ei ehkä suoriteta heti, jos eräpalvelua on rajoitettu kuormituksesta johtuen. Työt voidaan suorittaa myös synkronisesti valitsemalla **Tuo nyt** tai **Vie nyt**. Työ käynnistetään nyt automaattisesti, mikä on kätevää, jos erä ei käynnisty rajoittamisen vuoksi. Työt voidaan myös ajoittaa suoritettaviksi myöhemmin. Tämä voidaan tehdä valitsemalla **Suorita erätyönä-** -vaihtoehto. Rajoitus koskee eräresursseja, joten eräajo ei välttämättä käynnisty heti. Erän käyttäminen on suositeltava vaihtoehto, sillä se auttaa myös suurien tietomäärien tuomisessa tai viennissä. Eräajot voidaan aikatauluttaa suoritettavaksi tiettyinä eräryhminä, mikä parantaa kuormituksen hallintaa.

## <a name="validate-that-the-job-ran-as-expected"></a>Vahvista, että työ suoritettiin odotetulla tavalla
Työhistoria on käytettävissä tuonti- ja vientitöiden ongelmanratkaisuun ja tutkintaan. Historian työt on järjestetty aikajaksoille.

![Työhistorian jaksot.](./media/dixf-job-history.md.png)

Kukin ajettu työ sisältää seuraavat tiedot:

- Suorituksen tiedot
- Suoritusloki

Suorituksen tiedoissa näkyy kunkin työn käsittelemän tietoyksikön tila. Näin löydät nopeasti seuraavat tiedot:

- Käsitellyt yksiköt.
- Yksikölle: käsitellyt tietueet ja epäonnistuneiden tietueiden määrä.
- Kunkin yksikön väliaikaiset tietueet.

Voit ladata vientitöiden väliaikaiset tiedot tiedostona, tai voit ladata ne pakettina tuonti- ja vientitöitä varten.

Voit avata suoritustiedoista suorituslokin.

## <a name="parallel-imports"></a>Rinnakkaistuonnit
Voit nopeuttaa tietojen tuontia, jolloin tiedoston tuonnin rinnakkaiskäsittely voidaan ottaa käyttöön, jos yksikkö tukee rinnakkaistuontia. Jos haluat määrittää entiteetin rinnakkaistuonnin, seuraavia vaiheita on noudatettava.

1. Valitse **Järjestelmänhallinta \> Työtilat \> Tietojen hallinta**.
2. Avaa **Tietojen tuonti- ja vientikehyksen parametrit** -sivu valitsemalla **Tuonti-/vienti**-osasta **Framework-parametri** -ruutu.
3. Avaa **Entiteetin tuonnin suoritus parametrit** -sivu valitsemalla **Entiteetin asetukset** -välilehdestä **Määritä yksikön suoritus parametrit**.
4. Määritä kohteen rinnakkaistuonti määrittämällä seuraavat kentät:

    - Valitse yksikkö **Yksikkö**-kentässä.
    - Kirjoita **Tuonnin kynnystietueiden määrä** -kenttään tuonnin kynnystietueiden määrä. Tämä määrittää, mitä tietuemäärää säie käsittelee. Jos tiedostossa on 10 000 tietuetta, tietueiden määrä on 2 500 ja tehtävän määrä 4 merkitsee, että kukin säie käsittelee 2 500 tietuetta.
    - Syötä **Tuontitehtävien määrä** -kenttään tuontitehtävien määrä. Tämä ei saa ylittää eräkäsittelyn enimmäiseräsäikeitä **Järjestelmänhallinnan \>Palvelinmäärityksissä**.

## <a name="job-history-clean-up"></a>Työhistorian siivous 
Tietojen hallinnan työhistorian puhdistustoimintoa on käytettävä suoritushistorian ajoittaista uudelleenpuhdistusta varten. Tämä toiminto korvaa aiemman väliaikaisen taulukon puhdistustoiminnon, joka on nyt vanhentunut. Puhdistusprosessi puhdistaa seuraavat taulukot.

-   Kaikki väliaikaiset taulukot

-   DMFSTAGINGVALIDATIONLOG

-   DMFSTAGINGEXECUTIONERRORS

-   DMFSTAGINGLOGDETAIL

-   DMFSTAGINGLOG

-   DMFDEFINITIONGROUPEXECUTIONHISTORY

-   DMFEXECUTION

-   DMFDEFINITIONGROUPEXECUTION

**Suoritushistorian tyhjennys** -toiminnon on oltava käytössä ominaisuuksien hallinnassa, ja sen jälkeen sitä voi käyttää kohdassa **Tietojen hallinta\> Työhistorian tyhjennys**.

### <a name="scheduling-parameters"></a>Ajoitusparametrit

Kun ajoitat puhdistusprosessia, seuraavat parametrit on määritettävä, jotta voidaan määrittää puhdistuskriteerit.

-   **Historian säilyttämisen päivien määrä** – tätä asetusta käytetään ohjaamaan säilytettävän suoritushistorian määrää. Tämä määritetään päivien määränä. Kun puhdistamistyö on ajoitettu toistuvaksi erätyönä, tämä asetus toimii samalla tavalla kuin jatkuvasti liikkuva ikkuna, jolloin jäljelle jää aina määritetyn päivien määrä historiaa ja loput poistetaan. Oletusarvo on 7 päivää.

-   **Työn suorittamisen tuntien määrä** – puhdistettavaksi tarkoitetun historian määrästä riippuen puhdistustyön kokonaissuorituksen aika voi vaihdella muutamasta minuutista muutamiin tunteihin. Tämän parametrin arvoksi on määritettävä niiden tuntien määrä, jonka ajan työtä suoritetaan. Kun puhdistustyö on suoritettu tietylle tuntimäärälle, työ lopetetaan ja puhdistusta jatketaan, kun työ suoritetaan toistuvuusaikataulun mukaan seuraavan kerran.

    Maksimisuoritusaika voidaan määrittää asettamalla enimmäisraja tuntien määrälle, jonka sisällä työ on suoritettava tämän asetuksen avulla. Puhdistuslogiikka käy läpi yhden työn suorittamisen tunnuksen kerrallaan aikajärjestyksessä, ja vanhin on ensin liittyvän suoritushistorian puhdistuksessa. Se lopettaa uusien suoritustunnuksien keräilyn tyhjennystä varten, kun jäljellä oleva suorituksen kesto on viimeisen 10 % sisällä määritetystä kestosta. Joissakin tapauksissa on odotettavissa, että puhdistustyö jatkuu määritetyn enimmäisajan jälkeen. Tämä riippuu pitkälti siitä, kuinka useita tietueita on poistettava nykyiselle suoritustunnukselle, joka käynnistettiin ennen 10 prosentin raja-arvon ylittymistä. Käynnistetty tyhjennys on suoritettava tietojen eheyden varmistamiseksi, mikä tarkoittaa, että uudelleenjärjestäminen jatkuu määritetyn rajan ylittämisestä huolimatta. Kun tämä on suoritettu, uusia suoritustunnuksia ei kerätä ja tyhjennystyö on valmis. Jäljellä oleva suoritushistoria, jota ei ole puhdistettu riittävän suoritusajan puutteen vuoksi, noudetaan seuraavan kerran, kun puhdistustyö ajoitetaan. Tämän asetuksen oletus- ja minimiarvoksi määritetään 2 tuntia.

-   **Toistuva erä** – puhdistustyö voidaan suorittaa kertaluontoisesti, manuaalisena suorittamisena, tai se voidaan myös ajoittaa toistuvaksi erätyöksi. Erä voidaan ajoittaa käyttämällä **Suorita taustalla** -asetuksia, joka on erätöiden vakiomääritys.

> [!NOTE]
> Jos väliaikaisen tallennuksen tauluja ei ole puhdistettu kokonaan, varmista, että puhdistustyö ajoitetaan suoritettavaksi toistuvana. Kuten edellä on kerrottu, kunkin puhdistuksen suorituksen yhteydessä työ puhdistaa niin monta suorituksen tunnusta kuin mahdollista annetun ajan puitteissa. Jotta puhdistusta voidaan jatkaa jäljellä olevissa väliaikaisen tallennuksen tietueissa, työ on ajoitettava suoritettavaksi säännöllisesti.

## <a name="job-history-clean-up-and-archival"></a>Työhistorian puhdistus ja arkistointi 
Työhistorian tyhjennys ja arkistointi -toiminnallisuus korvaa aiemmat siivoustoiminnon versiot. Tämä osio kertoo näistä uusista ominaisuuksista.

Yksi puhdistustoiminnon tärkeimmistä muutoksista on järjestelmän erätyön käyttö historiatietojen poistamiseen. Järjestelmän erätyön käyttö sallii talous- ja toimintosovellusten ajoittaa siivouserätyön automaattisesti ja suorittaa sen, kun järjestelmä on valmis. Erätyötä ei enää tarvitse ajoittaa manuaalisesti. Tässä oletussuoritustilassa erätyö suoritetaan tunnin välein alkaen puolilta öin, ja se säilyttää viimeisimmän 7 päivän suoritushistorian. Tyhjennetty historia arkistoidaan tulevaa noutamista varten. Alkaen versiosta 10.0.20 tämä ominaisuus on aina käytössä.

Toinen puhdistusprosessin muutos on tyhjennetyn suoritushistorian arkistointi. Puhdistustyö arkistoi poistetut tietueet blob-tallennustilaan, jota DIXF käyttää säännölliseen kanssakäymiseen. Arkistoitu tiedosto on DIXF-pakettimuodossa, ja se on käytettävissä 7 päivän ajan blob-objektissa, jolloin se voidaan ladata. Oletusarvon mukainen arkistoidun tiedoston 7 päivän säilytysaika voidaan muuttaa enintään 90 päiväksi parametreissä.

### <a name="changing-the-default-settings"></a>Oletusasetusten muuttaminen
Tämä toiminto on tällä hetkellä esikatselussa, ja se on otettava eksplisiittisesti käyttöön ottamalla käyttöön DMFEnableExecutionHistoryCleanupSystemJob. Väliaikaisen siivouksen toiminnon on oltava käytössä myös ominaisuuksien hallinnassa.

Jos haluat muuttaa arkistoidun tiedoston säilytyksen oletusasetusta, siirry tietojen hallinnan työtilaan ja valitse **Työhistorian puhdistus**. Määritä **Paketin säilyttämispäivät blob-objektissa** arvoksi 7-90 (mukaan lukien). Tämä tulee voimaan tämän muutoksen tekemisen jälkeen luoduissa arkistoissa.

### <a name="downloading-the-archived-package"></a>Arkistoidun paketin lataaminen
Tämä toiminto on tällä hetkellä esikatselussa, ja se on otettava eksplisiittisesti käyttöön ottamalla käyttöön DMFEnableExecutionHistoryCleanupSystemJob. Väliaikaisen siivouksen toiminnon on oltava käytössä myös ominaisuuksien hallinnassa.

Voit ladata arkistoidun suoritushistorian siirtymällä tietojen hallinnan työtilaan ja valitsemalla **Työhistorian puhdistus**. Valitse **Paketin varmuuskopiohistoria** avataksesi historialomakkeen. Tässä lomakkeessa näkyy luettelo kaikista arkistoiduista paketeista. Arkiston voi valita ja ladata valitsemalla **Lataa paketti**. Ladattu paketti on DIXF-pakettimuodossa ja sisältää seuraavat tiedostot:

-   Entiteetin väliaikainen taulutiedosto
-   DMFDEFINITIONGROUPEXECUTION
-   DMFDEFINITIONGROUPEXECUTIONHISTORY
-   DMFEXECUTION
-   DMFSTAGINGEXECUTIONERRORS
-   DMFSTAGINGLOG
-   DMFSTAGINGLOGDETAILS
-   DMFSTAGINGVALIDATIONLOG



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

