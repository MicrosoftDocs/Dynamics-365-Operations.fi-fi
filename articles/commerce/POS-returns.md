---
title: Palautusten luominen myyntipisteessä
description: Tässä artikkelissa käsitellään palautusten käynnistämistä käteis- ja siirtotapahtumista tai asiakastilauksista Microsoft Dynamics 365 Commerce -myyntipistesovelluksessa.
author: hhainesms
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.20
ms.openlocfilehash: a49e9abd0143d480cc1cafb05be5e995fb3cebdd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856995"
---
# <a name="create-returns-in-pos"></a>Palautusten luominen myyntipisteessä

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään palautusten käynnistämistä käteis- ja siirtotapahtumista tai asiakastilauksista Microsoft Dynamics 365 Commerce -myyntipistesovelluksessa.

> [!NOTE]
> Commerce-versiossa 10.0.20 ja sitä myöhemmissä versioissa on uusi toiminto nimeltä **Myyntipisteen yhdistetty palautuksen käsittelykokemus**. Tämä ominaisuus tarjoaa myyntipisteessä yhdenmukaisen ja yhdistetyn palautusprosessin riippumatta tapahtuman tyypistä (käteis- ja siirtotapahtuma tai asiakastilaus) tai alkuperäisestä kanavasta, jossa tilaus luotiin. On suositeltavaa, että kaikki organisaatiot käyttävät tätä uutta ominaisuutta, jotta palautusten käsittelyn yleistä luotettavuutta voidaan parantaa myyntipisteessä.
>
> Kun toiminto on otettu käyttöön, sitä ei voi poistaa käytöstä.

## <a name="process-returns-by-using-the-return-transaction-operation"></a>Palautusten käsitteleminen palautustapahtumatoiminnon avulla

Suosittelemme palautustapahtumatoiminnon lisäämistä myyntipisteen [näytön asetteluun](pos-screen-layouts.md). Ennen Commerce 10.0.20 -versiota palautustapahtuma tukee oikein vain käteis- ja siirtotapahtumien palautusten käsittelyä. Kun olet käynnistänyt Commerce 10.0.20 -versiossa tai sitä myöhemmässä versiossa **Myyntipisteen yhdistetty palautuksen käsittelykokemus** -ominaisuuden, palautustapahtuma tukee myös asiakastilauksista peräisin olevaa palautusten käsittelyä. Tällaisia palautuksia ovat esimerkiksi jo laskutetut nouto- tai kotiinkuljetustilaukset.

Palautustapahtumatoiminnosta käyttäjät voivat etsiä käteis- ja siirtotapahtuman tai asiakastilauksen, jonka perusteella hän voi palauttaa, kirjoittamalla jonkin seuraavista neljästä hakuehdosta. Käyttäjät voivat määrittää nämä ehdot käyttämällä laitteen näppäimistöä, näyttönäppäimistöä tai viivakoodiskanneria.

- Vastaanottotunnus
- Tilauksen numero
- Kanavan viitetunnus (tunnetaan myös nimellä tilausvahvistustunnus)
- Laskun tunnus

Jos hakuehtoja vastaava tapahtuma tai tilaus löytyy, näkyviin tulee **Palautuskelpoiset tuotteet** -sivu. Siellä käyttäjät voivat määrittää palautettavat nimikkeet. He voivat myös määrittää palautusmääriä ja syykoodeja.

Myyntipiste näyttää jokaisen palautuskelpoisen tuotteen tilausrivin tiedot alkuperäisestä ostomäärästä sekä aiemmin käsiteltyjen palautusten määrät. Palautusmäärän, jonka käyttäjä määrittää tilausriville, on oltava pienempi tai yhtä suuri kuin **Palautettavissa** -kentän arvo.

![Palautuskelpoiset tuotteet -sivu.](media/returnslist.png)

Jos käyttäjällä on fyysinen tuote palautuskäsittelyn aikana ja tuotteella on viivakoodi, käyttäjä voi rekisteröidä palautuksen skannaamalla viivakoodin. Jokainen viivakoodin skannaus lisää palautusmäärää yhdellä nimikkeellä. Jos viivakoodin etiketissä on kuitenkin upotettu määrä, tämä määrä lisätään **Palautetaan nyt** -kenttään.

Käyttäjät voivat myös valita manuaalisesti palautettavat nimikkeet **Palautuskelpoiset tuotteet** -sivulla ja päivittää sitten **Palautetaan nyt** -kentän oikeanpuoleisessa ruudussa.

Jos tapahtumalle määritetään suurin käytettävissä oleva **Palautetaan nyt** -määrä, käyttäjä voi määrittää palautuskelpoisen enimmäismäärän kaikilla riveillä valitsemalla myyntipistesovelluksen palkissa **Valitse kaikki** -toiminnon.

Käyttäjän on valittava palautusten syykoodi tietoruudun avulla jokaiselle riville, jolla on **Palautetaan nyt** -määrä. Käteis- ja siirtotapahtumien palautuksissa palautuksen syykoodit määritetään myymälän toimintoprofiilin tietokoodeina. Asiakastilausten palautuksissa palautuksen syykoodit määritetään Dynamics 365 Commerce -pääkonttorin **Palautuksen syykoodit** -sivulla.

Kun jokaiselle palautettavalle nimikkeelle on määritetty palautusmäärä ja syykoodi, käyttäjä voi jatkaa käsittelyä valitsemalla myyntipistesovelluksen palkissa **Palauta**-toiminnon. Näyttöön tulee myyntipisteen tapahtumasivu, jossa edellisellä sivulla valitut palautettavat nimikkeet on lisätty ostoskoriin. Nimikkeiden **Palautetaan nyt** -määrät näkyvät tapahtuman negatiivisena määränä ja kokonaishyvitys lasketaan.

Käyttäjät voivat lisätä palautustapahtumaan rivejä, jos he luovat vaihtotilausta. Käyttäjät voivat myös lisätä enemmän ad-hoc-palautusnimikkeitä palautustapahtumaan käyttämällä lisätylle positiivisen määrän myyntiriville **Palauta tuote** -toimintoa.

> [!NOTE]
> Myyntipisteen **Palauta tuote** -toiminto ei tarkista alkuperäistä tapahtumaa ja sallii minkä tahansa tuotteen palauttamisen. Siksi suosittelemme, että vain valtuutettu käyttäjä voi suorittaa tämän toiminnon tai että tätä toimintoa varten on suoritettava esimiehen hyväksyntä.

Jos hyvitys erääntyy uloskuittauksessa, organisaatiot voivat määrittää [palautusten maksukäytännöt](refund_policy_returns.md), jotka rajoittavat asiakashyvityksen yhteydessä käytettävät maksutavat. Jos alkuperäinen tapahtuma on maksettu luottokortilla maksun käsittelypalvelun ja järjestelmän konfiguraation mukaan, käyttäjillä voi olla mahdollisuus [myöntää palautus alkuperäiselle kortille](dev-itpro/linked-refunds.md). Tällöin hyvitys voidaan käsitellä ilman, että asiakkaan on luettava luottokorttinsa uudelleen. Alkuperäistä maksun tunnusta käytetään hyvityksen maksamisen yhteydessä.

## <a name="other-return-options-in-pos"></a>Myyntipisteen muut palautusvaihtoehdot

Kun **Myyntipisteen yhdistetty palautuksen käsittelykokemus** -ominaisuus on käytössä, käyttäjät voivat myös käynnistää käteis- ja siirtotapahtuman tai asiakastilauksen palautuksen myyntipisteen **Näytä kirjauskansio** -toiminnolla. Sen jälkeen he voivat valita tapahtuman kirjauskansiosta ja valita sitten **Palauta**-toiminnon myyntipistesovelluksen palkissa. Tämä toiminto on käytettävissä vain, jos tilauksessa on palautusrivejä. Tämä käynnistää saman käyttäjäkokemuksen kuin **Palautustapahtuma**-toiminto.

Käyttäjät voivat myös hakea ja peruuttaa asiakastilauksia myyntipisteen **Peruuta tilaus** -toiminnon avulla. (Tätä toimintoa ei voi käyttää käteis- ja siirtotapahtumille.) Tällöin asiakastilauksen palautuksen voi käynnistää asiakastilauksen palautuksen valinnan jälkeen myyntipistesovelluksen palkin **Palauta**-toiminnon avulla. Tämä toiminto on käytettävissä vain, jos tilauksessa on palautusrivejä. Tämä käynnistää saman käyttäjäkokemuksen kuin **Palautustapahtuma**- tai **Näytä kirjauskansio** -toiminto.

## <a name="return-orders-are-posted-to-commerce-headquarters-as-sales-orders"></a>Palautustilaukset kirjataan Commerce headquartersiin myyntitilauksina. 

Kun **Myyntipisteen yhdistetty palautuksen käsittelykokemus** -ominaisuus on käytössä, kaikki POS-sovelluksessa luodut palautukset kirjoitetaan Commerce headquartersiin myyntitilauksiksi, joissa on negatiivisia rivejä. Versioissa ennen Commerce 10.0.20 -versiota käyttäjät voivat valita, kirjataanko palautustilaukset myyntitilauksina, joilla on negatiivisia rivejä, vai käytetäänkö palautustilauksia, jotka on luotava palautusnumeron vahvistuksen (RMA) prosessin yhteydessä. 

**Myyntipisteen yhdistetty palautuksen käsittelykokemus** -ominaisuudessa RMA-palautusprosessin käyttäminen palautusten luomiseen POS-sovelluksessa on poistettu. Kun tämä ominaisuus on otettu käyttöön, kaikki palautukset luodaan myyntitilauksina, joissa on negatiivisia rivejä.

## <a name="offline-return-processing-improvements"></a>Offline-palautusten käsittelyn parannukset

Kun palautus käsitellään POS-sovelluksessa, järjestelmä yrittää useimmiten suorittaa reaaliaikaisen palvelun (RTS) kutsun Commerce Headquarters -keskukseen ja vahvistaa nykyiset määrät, jotka voidaan palauttaa. Tämän oikeellisuustarkistuksen avulla voidaan estää petoksia, joissa asiakas yrittää palauttaa saman nimikkeen useaan sijaintiin.

Jos haluat käsitellä tilanteet, joissa RTS-kutsua ei voi suorittaa verkko- tai yhteysongelmien vuoksi, on käytössä prosessi, joka synkronoi palautusmäärätiedot Commerce Headquarters -pääkonttorista myymälän kanavatietokantaan säännöllisesti. Tämä kanavan puolella olevan palautuksen seuranta auttaa varmistamaan, että POS-pisteessä näkyvät **Palautettavissa**-määrät ovat kohtuudella tarkkoja silloinkin, kun POS on offline-tilassa. Näin myös varmistetaan, että POS voi jatkaa kanavan puolen tietojen tarkistamista estääkseen petolliset palautukset.

Jos haluat käyttää offline-palautusprosessia sopivalla tavalla, organisaatioiden on ajoitettava Commerce Headquartersissa **Päivitä palautusmäärät** -erätyö siten, että se suoritetaan säännöllisesti. On suositeltavaa suorittaa tämä työ samalla tiheydellä kuin P-työ, joka tuo uusia tapahtumia Commerce-kanavista Commerce headquartersiin.

**Päivitä palautusmäärät** -työ laskee määrän, joka on käytettävissä kaikkien Commerce headquartersissa olevien myyntitilausten palautukseen. Työn laskemia tietoja on sitten lähetettävä kanavatietokantoihin, jotta myymälän kanavat voidaan päivittää. Tähän tarkoitukseen käytetään **Palautusmäärät** (1200) -jakelutyötä. Koska palautettavaa määrää koskevat tiedot synkronoidaan Commerce headquartersista, jos palautus käsitellään POS-pisteessä, mutta RTS-kutsua ei voi tehdä, POS voi tarkistaa tietyn myyntirivin käytettävissä olevat **Palautettavissa**-määrät kanavan puolella olevien palautustietojen avulla.

Kun RTS-kutsuja ei voi tehdä ja POS käyttää kanavan puolella olevia tietoja palautusten oikeellisuustarkistuksessa, näyttöön tulee varoitussanoma, jossa käyttäjälle tiedotetaan offline-palautuksen luomisesta. Siksi he ovat tietoisia, että myyntipisteessä näkyvä käytettävissä oleva **Palautettavissa**-määrä saattaa olla vanhentunut, eikä enää tarkka sen mukaan, milloin **Päivitä palautusmäärät** -työ on edellisen kerran käsitelty ja synkronoitu kanavaan.

Asiakas on esimerkiksi käsitellyt äskettäin palautusta tilausriville toisessa kanavassa, mutta tietoja ei ole vielä synkronoitu kanavatietokantoihin **Päivitä palautusmäärät** -työn avulla. Tämän jälkeen asiakas siirtyy toiseen myymälään ja yrittää palauttaa saman nimikkeen uudelleen. Jos myymälä ei voi tehdä Commerce headquartersiin RTS-kutsua ja näin saada reaaliaikaisia palautustietoja, POS sallii nimikkeen palauttamisen uudelleen. Käyttäjää varoitetaan kuitenkin, että palautuksen vahvistamiseen käytettävät tiedot saattavat olla vanhentuneet. Sanoma, jonka käyttäjä saa, on vain varoitussanoma. Se ei estä käyttäjää jatkamasta palautusten käsittelyprosessia.

Jos kanavan puolen tiedot eivät ole ajan tasalla jostain syystä ja offline-palautus käsitellään määrälle, joka ylittää todellisen käytettävissä olevan **Palautettavissa**-määrän, laskelman kirjaamisen yhteydessä saattaa tulla virheilmoitus, kun tapahtuma luodaan Commerce headquarters -sovelluksessa.

> [!NOTE]
> Kun **Myyntipisteen yhdistetty palautuksen käsittelykokemus** -ominaisuus on käytössä, käyttöön tulevat uudet valinnaiset ominaisuudet, jotka tukevat sarjallistettujen tuotepalautusten oikeellisuustarkistusta. Lisätietoja: [Sarjanumeron avulla ohjattujen tuotteiden palautus myyntipisteessä](POS-serial-returns.md).

## <a name="version-details"></a>Versiotiedot

Seuraavassa luettelossa on eri komponenttien vähimmäisversiovaatimukset.
- Commerce headquarters: versio 10.0.20
- Commerce Scale Unit (CSU): versio 9.30
- Myyntipiste (POS): versio 9.30

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Ota käyttöön oikea verojen laskeminen osittaisen määrän palautuksille

Tämä ominaisuus varmistaa, että kun tilaus palautetaan käyttäen useaa laskua, verot täsmäävät alun perin veloitetun verosumman kanssa.

1. Tee **Ominaisuuksien hallinta** -työtilassa haku hakusanoilla **Ota käyttöön oikea verojen laskeminen osittaisen määrän palautuksille**.
1. Valitse **Ota käyttöön oikea verojen laskeminen osittaisen määrän palautuksille** -toiminto ja valitse sitten **Ota käyttöön**.

## <a name="set-up-return-locations-for-retail-stores"></a>Aseta palautussijainnit vähittäismyymälöille.

Commercen avulla voit määrittää vähittäismyynnin tietokoodeihin ja myynnin sekä markkinoinnin syykoodeihin perustuvat palautussijainnit. Kun asiakas palauttaa oston, kassanhoitajat usein ilmaisevat palautuksen syyn. Voit määrittää, että palautetut tuotteet on määritettävä varaston eri palautussijainteihin riippuen siitä, kuinka kassanhoitaja valitsee myyntipisteessä tieto- ja syykoodit.

Asiakas palauttaa esimerkiksi viallisen tuotteen, ja kassanhoitaja käsittelee palautustapahtuman. Kun Retail POS näyttää palautusten tietokoodin, kassa valitsee viallisten palautusten alikoodin. Palautettu tuote määritetään tällöin automaattisesti tiettyyn palautussijaintiin.

Palautuksen sijainti voi olla varasto, sijainti varastossa, tai tietty jopa kuormalava riippuen varastosijainneista, jotka organisaatiosi on määrittänyt. Voit yhdistää jokaisen palautussijainnin yhteen tai useampaan vähittäiskaupan tietokoodiin sekä myynnin ja markkinoinnin syykoodiin.

### <a name="prerequisites"></a>Edellytykset

Ennen kuin voit määrittää palautuskohteita, sinun on määritettävä seuraavat elementit:

- **Vähittäismyyntitietokoodit** – Myyntipisteen kassalla antaa ohjeita, jotka on määritetty **Retail**-moduulissa. Lisätietoja on kohdassa [Tietokoodien määrittäminen](/dynamicsax-2012/appuser-itpro/setting-up-info-codes).
- **Myynti- ja markkinointisyykoodit** – Myyntipisteen kassalla antaa ohjeita, jotka on määritetty **Myynti ja markkinointi** -moduulissa. Lisätietoja on kohdassa [Syykoodien määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-return-reason-codes).
- **Varastosijainnit** – paikat, joissa varastoa pidetään. Lisätietoja on kohdassa [Varastosijaintien määrittäminen](/dynamicsax-2012/appuser-itpro/about-locations).
    
### <a name="set-up-return-locations"></a>Määritä palautussijainnit

Voit määrittää palautussijainnit noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Varastot** ja valitse varasto.
1. Valitse **Retail**-pikavälilehden **Oletuspalautussijainti**-kentässä varastosijainti, jota käytetään palautuksille, kun tietokoodit tai syykoodit eivät ole yhdistetty palautussijainteihin.
1. Valitse **Palautuksen oletuskuormalava**-kentässä kuormalava, jota käytetään palautuksille, kun tietokoodit tai syykoodit eivät ole yhdistetty palautussijainteihin.
1. Siirry kohtaan **Retail ja Commerce \> Varaston hallinta \> Palautussijainnit**.
1. Valitse **Uusi** luodaksesi uuden palautussijaintikäytännön.
1. Kirjoita palautussijainnin yksilöivä nimi ja kuvaus.

    > [!NOTE]
    > Nimi lisätään automaattisesti, jos palautussijainneille on määritetty numerosarja.

1. Määritä **Yleiset**-pikavälilehdessä **Tulosta tarrat** -asetuksen arvoksi **Kyllä**, jos haluat tulostaa tarrat kaikkiin palautussijainteihin määritettyihin tuotteisiin.
1. Määritä **Estä varasto** -asetukseksi **Kyllä**, jotta palautetut tuotteet siirretään oletuspalautussijaintiin pois varastosta, ja jotta niiden myynti estetään.
1. Liitä tietyt vähittäismyyntitietokoodit ja alikoodit palautussijainteihin seuraavasti:

    1. Valitse **Vähittäismyynnin tietokoodit**-pikavälilehdessä **Lisää**.
    1. Valitse palautusten tietokoodi **Tietokoodi**-kentässä.
    1. Valitse **Alikoodi**-kentässä alikoodi palautussyylle. **Kuvaus**-kentässä näkyy valitun alikoodin kuvaus.
    1. **Myymälä**-kentässä valitse myymälä, jossa tietokoodia käytetään.
    1. Määritä palautussijainti **Varasto**-, **Sijainti**- ja **Kuormalavan tunnus** -kenttien avulla. Voit esimerkiksi määrittää tietyn sijainnin myymälässä valitsemalla myymälän **Myymälä**-kentässä ja sijainnin **Sijainti**-kentässä.
    1. Valitse **Estä varasto**-valintaruutu ottaaksesi varastosta palautettuja tuotteita ja estääksesi niiden myynnin.

1. Liitä tietyt myynnin ja markkinoinnin syykoodit palautussijainteihin seuraavasti:

    1. Valitse **Myynnin ja markkinoinnin syykoodit** -pikavälilehdessä **Lisää**.
    1. Valitse syykoodi palautuksille **Syykoodi** -kentässä. **Kuvaus**-kentässä näkyy valitun syykoodin kuvaus.
    1. **Myymälä**-kentässä valitse myymälä, jossa syykoodia käytetään.
    1. Määritä palautussijainti **Varasto**-, **Sijainti**- ja **Kuormalavan tunnus** -kenttien avulla. Voit määrittää esimerkiksi tietyn kuormalavan varastosijainnissa valitsemalla varaston **Varasto**-kentässä, sijainnin **Sijainti**-kentässä ja kuormalavan **kuormalavan tunnus** -kentässä.
    1. Valitse **Estä varasto**-valintaruutu ottaaksesi varastosta palautettuja tuotteita ja estääksesi niiden myynnin.

    > [!NOTE]
    > Jos nimikkeelle käytetään palautussijaintikäytäntöä, mutta kassanhoitajan valitsemien palautusten syy ei vastaa mitään koodia, joka on määritetty **vähittäismyynnin tietokoodien** tai **myynnin ja markkinoinnin syykoodien** pikavälilehdissä, nimike lähetetään **Varasto**-sivulla määritettyyn oletuspalautussijaintiin. **Palautussijainnit**-sivun **Yleiset**-pikavälilehden **Estä varasto** -valintaruudun asetus määrittää myös, onko palauttavan nimikkeen varasto estettävä.

1. Valitse **Retail ja Commerce \> Commercen tuotehierarkia**.
1. Valitse palautussijainti **Varaston hallinta - luokan ominaisuudet** -pikavälilehden **Palautussijainti**-kentässä. Koska samalle myymälälle voidaan määrittää useita palautussijaintikäytäntöjä, tässä kohdassa valittava arvo määrittää käytetyn palautussijaintikäytännön.

## <a name="additional-resources"></a>Lisäresurssit

[Sarjanumeron avulla ohjattujen tuotteiden palautus myyntipisteessä](POS-serial-returns.md)

[Aiemmin hyväksyttyjen ja vahvistettujen tapahtumien linkitetyt hyvitykset](dev-itpro/linked-refunds.md)

[Kanavan palautus- ja maksuhyvityskäytännön luominen ja päivittäminen](refund_policy_returns.md)

[Myyntipistekäyttöliittymän visuaaliset kokoonpanot](pos-screen-layouts.md)
