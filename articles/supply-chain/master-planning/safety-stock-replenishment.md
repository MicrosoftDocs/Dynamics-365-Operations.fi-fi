---
title: Nimikkeiden varmuusvaraston täyttäminen
description: Tässä aiheessa käsitellään varmuusvaraston täyttämistä ja nimikkeiden varmuusvarastomäärien määrittämistä.
author: thethehelga
ms.date: 8/23/2021
ms.topic: article
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended, ReqSafetyKeyDefaultDataWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-oldolg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 28f902c589cd80f1c34dc2758232548309db9aca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474625"
---
# <a name="safety-stock-fulfillment-for-items"></a>Nimikkeiden varmuusvaraston täyttäminen

[!include [banner](../includes/banner.md)]

Varmuusvarasto ilmaisee, kuinka paljon ylimääräistä nimikettä on varastossa, jotta voidaan estää nimikkeen loppuminen varastosta. Varmuusvarastoa käytetään puskurivarastona siltä varalta, että toimittaja ei voi toimittaa myyntitilauksia vastaavaa määrää nimikkeitä asiakkaan pyydettyyn lähetyspäivämäärään mennessä. Kun myyntilaus täytetään varmuusvarastosta, varmuusvarastoa vähennetään. Voit tuoda varaston automaattisesti takaisin varmuusvarastotasolle pääsuunnittelun avulla.

## <a name="set-up-safety-stock-levels-for-items"></a>Nimikkeiden varmuusvarastotasojen määrittäminen

Varmuusvarasto määritetään nimikkeen kattavuuden osana valitsemalla **Nimikkeen kattavuus** -sivulla **Vapautetut tuotteet \> Suunnitelma \> Kattavuus**.

Anna **Minimi**-kenttään nimikkeen varmuusvarastotaso. Arvo ilmoitetaan varastoyksikköinä. Jos jätät kentän tyhjäksi, käytetään oletusarvoa eli nollaa. Tätä kenttää voit käyttää, kun valitset **Kattavuuskoodi**-luettelossa **Kausi**, **Tarve** tai **Min./Maks.**. Varastotasoraja koskee varastosaatavuutta, joten varaukset ja merkinnät voivat laukaista varmuusvaraston täydennyksen, ennen kuin fyysinen määrä alittaa määritetyn minimitason.

> [!NOTE]
> Kaikki muut suunnitellut kattavuusdimensiot on määritettävä ennen **Minimi**-kentän määrittämistä. Tällä tavoin estetään virheellisen tietueen käyttö pääsuunnittelun aikana. Näin voi käydä, jos dimensioryhmää esimerkiksi laajennetaan ylimääräisellä suunnitellulla kattavuusdimensiolla, jolle ei ole vielä määritetty minimi- ja maksimivarastomääriä.

Voit käsitellä kysynnän kausivaihteluita minimitunnisteiden avulla. Voit esimerkiksi vähentää varaston vähimmäistasoa kysynnän ollessa vähäistä ja nostaa tasoa vähitellen muina kuukausina. Minimitunnus luodaan valitsemalla **Pääsuunnittelu \> Asetukset \> Kattavuus \> Minimi- ja maksimitunnukset**. Voit määrittää minimitunnuksen säätämään varmuusvarastotasoa kausivaihtelun mukaan **Nimikkeen kattavuus** -sivun **Vähimmäiskoodi**-kentässä.

## <a name="example-minimum-key"></a>Esimerkki: Vähimmäiskoodi

Seuraava menettely on esimerkki, jossa esitetään, miten luodaan minimitunnus, joka vastaa lisääntyneestä kausikysynnästä kevät- ja kesäkuukausina.

1. Siirry kohtaan **Pääsuunnittelu \> Määritys \> Kattavuus \> Minimi-/maksimitunnukset**.
1. Luo minimi-/maksimitunnus valitsemalla **Uusi**.
1. Kirjoita **Minimi- tai maksimitunnus** -kenttään tunnukselle tunniste. Kirjoita **Nimi**-kenttään tunnuksen nimi.
1. Määritä **Käytä voimaantulopäivämäärää** -asetuksen arvoksi *Kyllä* ja jätä **Voimaantulopäivä**-kenttä tyhjäksi, jotta tunnus tulee voimaan kuluvan vuoden ensimmäisestä päivästä alkaen.

    > [!NOTE]
    > Asetusten **Käytä voimaantulopäivämäärää** ja **Voimaantulopäivämäärä** yhdistelmä määrittää päivämäärän, josta alkaen tunnus on voimassa.
    >
    > - Kun **Käytä voimaantulopäivämäärää** -asetuksen arvona on *Ei*, tunnus on voimassa kulloisestakin päivämäärästä tai järjestelmän päivämäärästä alkaen.
    > - Kun **Käytä voimaantulopäivämäärää** -asetuksen arvona on *Kyllä*, tunnus on voimassa **Voimaantulopäivämäärä**-kentässä määritetystä päivämäärästä alkaen.

1. Luo **Kaudet**-osassa 12 riviä ja määritä niille seuraavat arvot:

    - **Muutos** – Määritä kullekin riville yksilöllinen numero väliltä 1–12. Tässä kentässä näkyy **Yksikkö**-kentän määrittämän aikayksikön asteittainen muutos.
    - **Yksikkö** – Valitse jokaiselle riville *Kuukaudet*.
    - **Alkamispäivämäärä**, **Päättymispäivämäärä** ja **Kuukausi** – Nämä kentät määritetään automaattisesti asetusten **Muutos** ja **Yksikkö** perusteella. Kuukausikaudet alkavat kuluvan vuoden ensimmäisestä päivästä.
    - **Kerroin** — Anna arvot, joita käsitellään seuraavassa taulukossa. Tällä kentällä määritetään kerroin, jolla vähimmäisvarasto kerrotaan.

        | Rivi (muutos) | Kerroin | Tulos |
        |---|---|---|
        | 1–3 | 1 | Minimivarasto perustaa **Nimikkeen kattavuus** -sivun tammi–maaliskuun asetukseen. |
        | 4–5 | 2 | Vähimmäisvarasto kerrotaan kertoimella 2 huhtikuusta toukokuuhun. |
        | 6–8 | 2.5 | Vähimmäisvarasto kerrotaan kertoimella 2,5 ajalla kesäkuu - elokuu. |
        | 9–12 | 1 | Vähimmäisvarasto palaa **Nimikkeen kattavuus** -sivun syys–joulukuun asetukseen. |

    Asetusten pitäisi nyt muistuttaa seuraavan kuvan asetuksia.

    ![Tunnusten vähimmäis- tai enimmäiskaudet.](media/min-max-key-periods.png "Tunnusten vähimmäis- tai enimmäiskaudet")

> [!NOTE]
> Voit myös käyttää ohjattua toimintoa minimi-/maksimitunnuksen luomiseen. Avaa ohjattu **Minimi-/maksimitunnukset** -toiminto valitsemalla **Ohjattu toiminto** **Minimi-/maksimitunnukset**-sivun toimintoruudussa. Ohjattu toiminto opastaa minimi-/maksimiavaimen luomiseen ja määrittämisen vaiheittain.

Jos kattavuuskoodi on *Min./Maks.*, voit määrittää myös nimikkeellä varastossa säilytettävän maksimimäärän. Arvo ilmoitetaan myös varastoyksikköinä. Jos oletettu varastosaatavuus laskee valitun minimivarastotason alapuolelle, pääsuunnittelu luo suunnitellun tilauksen täyttämään kaikki avoimet tarpeet, joka tuo varastosaatavuuden määritettyyn enimmäismäärään. Kuten varaston vähimmäismäärän määrittämisessä, kaikki muut suunnitellut kattavuusdimensiot on määritettävä, ennen kuin **Maksimi**-kenttä voidaan määrittää.

## <a name="example-minmax-coverage-code"></a>Esimerkki: Min./Maks.-kattavuuskoodi

Minimimäärä on 10, ja maksimimäärä on 15. Nykyinen käytettävissä oleva varasto on 4. Tällöin vähimmäismäärätarve on 6. Koska enimmäismääräksi on kuitenkin määritetty 15, pääsuunnittelu luo 11 yksikön suunnitellun tilauksen.

Kausivaihtelua noudattavilla nimikkeillä on ehkä käytettävä erilaisia enimmäistasoja. Sitä varten **Maksimitunnukset** on määritettävä valitsemalla **Pääsuunnittelu \> Asetukset \> Kattavuus \> Minimi- ja maksimitunnukset**. Täytä **Nimikkeen kattavuus** -sivun **Maksimitunnus**-kenttä. Voit tarkastella **Min./Maks.**-välilehden minimitunnuksilla määritettyjen varmuusvarastotasojen tietoja **Nimikkeen kattavuus** -sivulla. Sinun on varmistettava, että tietyn ajanjakson minimi- ja maksimiarvot ovat synkronoituja.

## <a name="safety-stock-fulfillment"></a>Varmuusvaraston täyttäminen

Voit valita **Täytä vähimmäisarvo** -parametrilla päivämäärän tai ajanjakson, jolloin varastotason on vastattava **Minimi**-kenttään määritettyä määrää. Tätä kenttää voit käyttää, kun valitset **Kattavuuskoodi**-luettelossa **Kausi**, **Tarve** tai **Min./Maks.**.

Jos **Minimitunnukset** on käytössä, valitse **Minimikaudet**-valintaruutu, jos haluat täyttää kaikkien minimitunnukselle määritettyjen kausien vähimmäisvarastotason. Jos poistat valintaruudun valinnan, vain valitun kauden vähimmäisvarasto täytetään.

Seuraava skenaario näyttää, miten tätä parametria käytetään ja mitä eroja sen arvoilla on.

> [!NOTE]
> Kaikissa tämän aiheen kuvissa x-akseli vastaa varastoa, y-akseli päiviä, palkit varastotasoa ja nuolet tapahtumia, kuten myyntitilausrivejä, ostotilausrivejä tai suunniteltuja tilauksia.

[![Varmuusvaraston täyttämisen yleinen skenaario.](media/Scenario1.png)](media/Scenario1.png)

**Täytä vähimmäisarvo** -parametrillä voi olla seuraavat arvot:

### <a name="todays-date"></a>Tämän päivän päivämäärä

Määritetty minimimäärä saavutetaan päivänä, jolloin pääsuunnittelu suoritetaan. Järjestelmä yrittää täyttää varmuusvarastorajan mahdollisimman nopeasti, vaikka se ei olisi realistista läpimenoajan vuoksi.

[![Tarve tämän päivän päivämääränä.](media/TodayReq.png)](media/TodayReq.png)

Suunniteltu tilaus P1 luodaan kuluvalle päivälle nostamaan varastosaatavuus varmuusvarastotason yläpuolelle kyseisenä päivänä. Myyntitilausrivit S1–S3 pienentävät edelleen varastotasoa. Pääsuunnittelu luo suunnitellut tilaukset P2–P4 palauttamaan varastotaso varmuusvarastorajalle kunkin myyntitilaustarpeen jälkeen.

Kun **Tarve**-kattavuuskoodia käytetään, useita suunniteltuja tilauksia luodaan. Usein kysytyille nimikkeille ja materiaaleille kannattaa käyttää joko **Kausi**- tai **Min./Maks.**-kattavuutta luomaan täydennyksen myyntirakenne. Seuraavassa kuvassa on esimerkki **Kausi**-kattavuuskoodista.

[![Kausi. Tämän päivän päivämäärä.](media/TodayPeriod.png)](media/TodayPeriod.png)

Seuraavassa kuvassa on esimerkki **Min./Maks**-kattavuuskoodista.

[![Min./Maks. Tämän päivän päivämäärä.](media/TodayMinMax.png)](media/TodayMinMax.png)

### <a name="todays-date--procurement-time"></a>Tämän päivän päivämäärä + hankinta-aika

Määritetty minimimäärä saavutetaan päivänä, jolloin pääsuunnittelu suoritetaan ja johon on lisätty oston tai tuotannon läpimenoaika. Tämä aika sisältää varmuusmarginaalit. Jos nimikkeeseen liittyy kauppasopimus ja olet valinnut **Pääsuunnittelun parametrit**-sivulla **Etsi kauppasopimukset** -valintaruudun, kauppasopimuksen toimitusläpimenoaikaa ei oteta huomioon. Läpimenoajat haetaan nimikkeen kattavuudesta tai nimikkeestä.

Tämä täyttämistila luo suunnitelmiin vähemmän viiveitä ja suunniteltuja tilauksia nimikkeen kattavuusryhmäasetuksista riippumatta.

Seuraavassa kuvassa on suunnitelman lopputulos, jos kattavuuskoodi on **Tarve** tai **Kausi**.

[![Tarve tai Kausi. Tämän päivän päivämäärä ja läpimenoaika.](media/TodayPLTReq.png)](media/TodayPLTReq.png)

Seuraavassa kuvassa on suunnitelman lopputulos, jos kattavuuskoodi on **Min./Maks**.

[![Min./Maks. Tämän päivän päivämäärä ja läpimenoaika.](media/TodayPLTMinMax.png)](media/TodayPLTMinMax.png)

### <a name="first-issue"></a>Ensimmäinen varasto-otto

Määritetty minimimäärä saavutetaan päivänä, jolloin varastosaatavuus alittaa minimitason, kuten seuraavassa kuvassa. Vaikka varastosaatavuus alittaa minimitason pääsuunnittelun suorituspäivänä, **Ensimmäinen varasto-otto** ei yritä kattaa sitä ennen seuraavan tarpeen saapumista.

Seuraavassa kuvassa on esimerkki **Tarve**-kattavuuskoodista.

[![Tarve-kattavuuskoodia ja Ensimmäinen varasto-otto -täyttämistä käyttävän nimikkeen suunnittelu.](media/FirstIssueReq.png)](media/FirstIssueReq.png)

Seuraavassa kuvassa on esimerkki **Kausi**-kattavuuskoodista.

[![Kausi-kattavuuskoodia ja Ensimmäinen varasto-otto -täyttämistä käyttävän nimikkeen suunnittelu.](media/FirstIssuePeriod.png)](media/FirstIssuePeriod.png)

Seuraavassa kuvassa on esimerkki **Min./Maks**-kattavuuskoodista.

[![MinMax-kattavuuskoodia ja Ensimmäinen varasto-otto -täyttämistä käyttävän nimikkeen suunnittelu.](media/FirstIssueMinMax.png)](media/FirstIssueMinMax.png)

Jos varastosaatavuus alittaa varmuusvarastorajan jo pääsuunnittelun suorituspäivänä, **Tämän päivän päivämäärä** ja **Tämän päivän päivämäärä + hankinta-aika** käynnistävät täydennyksen välittömästi. **Ensimmäinen varasto-otto** odottaa nimikkeen muuta varasto-ottoa, kuten myyntitilauksen ja tuoterakennerivin tarvetta, jonka jälkeen se käynnistää täydennyksen kyseisenä tapahtumapäivänä.

Jos varastosaatavuus alittaa varmuusvarastorajan pääsuunnitelman suorituspäivänä, **Tämän päivän päivämäärä** ja **Ensimmäinen varasto-otto** tuottavat täsmälleen saman tuloksen, kuten seuraavassa kuvassa.

[![Ei alita rajaa.](media/ReqFirstIssue.png)](media/ReqFirstIssue.png)

Jos varastosaatavuus ei alita varmuusvarastorajaa pääsuunnittelun suorituspäivänä, **Tämän päivän päivämäärä + hankinta-aika** tuottaa seuraavan tuloksen, sillä siirtää täyttämisen hankinnan läpimenoajan loppuun.

![Täytäntöönpano lykätään hankinnan läpimenoajan loppuun.](media/ReqTodayLT.png)

### <a name="coverage-time-fence"></a>Kattavuuden aikarajat

Määritetty minimimäärä saavutetaan **Kattavuuden aikarajat** -kentässä määritetyn ajanjakson aikana. Tämä asetus on kätevä silloin, kun pääsuunnittelu ei salli varastosaatavuuden käyttöä todellisissa tilauksissa, kuten myynnissä tai siirroissa, varmuustason ylläpidon vuoksi. Tätä täydennystapaa ei kuitenkaan tarvita tulevissa versioissa ja tämä asetus vanhentuu.

## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>FEFO-nimikkeiden varmuusvaraston täydennyksen suunnittelu

Varmuusvarastossa käytetään aina vanhentumispäivältään viimeisintä varastoonottoa, jotta todellinen kysyntä, kuten myyntirivit tai tuoterakennerivit, voidaan täyttää FEFO-järjestyksessä.

Seuraava skenaario osoittaa, mitä tämä tarkoittaa käytännössä.

[![FEFO-skenaario.](media/FEFOScenario.png)](media/FEFOScenario.png)

Kun suunnittelu suoritetaan, se kattaa ensimmäisen myyntitilauksen käsillä olevasta varastosta ja lisäostotilauksen jäljellä olevalle määrälle.

[![FEFO 1.](media/FEFO1.png)](media/FEFO1.png)

Suunniteltu tilaus luodaan varmistamaan, että varastosaatavuus palautetaan varmuustasolle.

[![FEFO 2.](media/FEFO2.png)](media/FEFO2.png)

Kun toista myyntitilausta suunnitellaan, sen määrä katetaan varmuusvaraston kattavasta aiemmin luodusta suunnitellusta tilauksesta. Näin ollen varmuusvarasto vaihtuu jatkuvasti.

[![FEFO 3.](media/FEFO3.png)](media/FEFO3.png)

Lopuksi luodaan vielä yksi suunniteltu tilaus kattamaan varmuusvarasto.

[![FEFO 4.](media/FEFO4.png)](media/FEFO4.png)

Kaikki erät vanhentuvat vastaavasti ja suunnitellut tilaukset luodaan täyttämään varmuusvarasto vanhentumisen jälkeen.

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>Pääsuunnittelun tapa käsitellä varmuusvaraston rajoitusta

Varmuusvarastoa seurataan järjestelmässä tarvetyyppinä myyntirivien ja tuoterakennetarpeiden tavoin. Varmuusvaraston tarverivi näkyy **Nettotarpeet**-sivulla, jos poistat **Vaatimustyyppi**-sarakkeen oletussuodattimen.

Varmuusvaraston tarvetapahtuman täyttämisen priorisointi poistetaan, jos järjestelmä päättelee sen viivästyttävän todellisen kysynnän, kuten myyntirivien, tuoterakennerivien, siirtotarpeiden tai kysyntäennusterivien, täyttämistä. Muussa tapauksessa sen varmistamisella, että varastosaatavuus ylittää varmuusvaraston määrän, on sama prioriteetti kuin muilla kysyntätyypeillä. Näin varmistetaan, että todellisissa tapahtumissa ei ole viiveitä, sekä autetaan estämään varmuusvaraston liiallinen ja liian aikainen täydennys.

Pääsuunnittelun kattavuusvaiheen aikana varmuusvaraston täydennyksen priorisointia ei enää poisteta. Käytettävissä olevaa varastoa käytetään ennen muista kysyntätyyppejä. Viiveen laskennan aikana uusi logiikka lisätään käsittelemään viivästyneet myyntirivit, tuoterakennerivin tarpeet ja kaikki muut kysyntätyypit. Tällä tavoin selvitetään, voidaanko ne toimittaa ajallaan varmuusvarastoa käyttämällä. Jos järjestelmä havaitsee, että se voi minimoida viiveet varmuusvarastoa käyttämällä, myyntirivit tai tuoterakennerivit korvaavat sitten alkuperäisen kattavuuden varmuusvarastolla ja järjestelmä käynnistää sen sijaan varmuusvaraston täydennyksen.

Jos suunnitelmalle tai nimikkeelle ei ole määritetty viivästyksen laskentaa, varmuusvarastorajoituksella on sama prioriteetti kuin muilla kysyntätyypeillä. Tämä tarkoittaa, että käytössä on käytettävissä olevan varaston ja muun varastosaatavuuden varaus ennen muita kysyntätyyppejä.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
