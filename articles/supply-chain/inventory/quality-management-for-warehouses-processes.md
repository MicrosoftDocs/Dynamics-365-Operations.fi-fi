---
title: Laadunhallinta varastoprosesseja varten
description: Tämä artikkeli sisältää tietoja varastoprosessiominaisuuksien laadunhallinnasta. Tämä ominaisuus laajentaa laadunhallinnan ominaisuuksia ja antaa käyttäjien integroida nimikkeen otantakomponentit fyysiseen varastoon vastaanotettaessa käyttämällä varastonhallintaprosesseja (WMS).
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-04-02
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: b4d0b09ea4bee58799a659217e2236fe74102949
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335432"
---
# <a name="quality-management-for-warehouse-processes"></a>Laadunhallinta varastoprosesseja varten

[!include [banner](../includes/banner.md)]

_Varastoprosessien laadunhallinnan ominaisuudet_ -ominaisuus antaa käyttäjien integroida nimikkeen otantakomponentit fyysiseen varastoon vastaanotettaessa käyttämällä varastonhallintaprosesseja (WMS). Varastotyön voi luoda automaattisesti, jotta varasto voidaan siirtää laadunvalvontasijaintiin, joka perustuu prosenttiosuuteen tai kiinteään määrään, tai joka perustuu jokaiseen *n*:teen-rekisterikilpeen. Kun laatutilaus on suoritettu, työt voidaan luoda automaattisesti, jotta varasto siirtyy prosessin seuraavaan sijaintiin laatutulosten mukaan.

_Varastoprosessien laadunhallinta_ -ominaisuus laajentaa peruslaadunhallinnan ominaisuuksia. Se tarjoaa mahdollisuuden luoda laatutilauksia varastolle, joka lähetetään laadunvalvonnan sijaintiin, vaikka laatutilauksia ei aina tarvita. Näin ollen se mahdollistaa kevyen laadunvalvontaprosessin, joka perustuu varastotyöhön.

## <a name="turn-on-the-quality-management-for-warehouse-processes-feature"></a>Ota käyttöön varastoprosessien laadunhallinta -ominaisuus

Ennen kuin voit käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Ominaisuuden nimi:** *Laadunhallinta varastoprosesseja varten*

## <a name="key-benefits"></a>Avainedut

_Varastoprosessien laadunhallinta_ -toiminto luo automaattisesti työn osana vastaanottoprosessia, jotta laadunvalvonnassa tarvittava varastomäärä voidaan siirtää laadunvalvontasijaintiin. Jos vastaanotettu määrä ylittää laadunvalvonnassa vaaditun määrän (nimikkeen otanta-asetusten mukaan), ylimääräinen määrä siirretään sijaintidirektiivin asetusten mukaiseen saapuvaan sijaintiin. Kun laatutilaus on vahvistettu, työ luodaan automaattisesti, jotta laatutilauksen määrä voidaan siirtää uuteen saapuvien tai palautusten sijaintiin oikeellisuustarkistustuloksen ja sijaintidirektiivin asetusten perusteella. Työn automaattinen tuottaminen, jossa on vain määrä, joka on siirrettävä laadunvalvontaan ja siitä pois, tarjoaa integroidun prosessikokemuksen.

> [!NOTE]
> Kun _varastoprosessien laadunhallinta_ -ominaisuus on käytössä, voit silti hyödyntää manuaalista prosessia. Manuaalisessa prosessissa varastonsiirto ja siirto mallin avulla ovat käytössä, kun varastotyöntekijä käynnistää varastotyön luomisen ja siirtää varaston laadunvalvonta sijainnista uuteen sijaintiin. Voit myös edelleen määrittää saapuvan liikenteen sijaintidirektiivin, joka siirtää varaston kokonaisuudessaan vastaanottopaikasta laadunvalvontasijaintiin ottamatta huomioon nimikkeen otantamääritystä.

## <a name="quality-management-and-the-quality-management-for-warehouse-processes-feature"></a>Laadunhallinta ja varastoprosessien laadunhallinta -ominaisuus

Kun _varastoprosessien laadunhallinta_ on otettu käyttöön, se muuttaa tärkeimpien varastonhallinta- ja laadunhallintayksiköiden asetuksia. Seuraavassa kuvassa on yleiskatsaus yksiköistä, jotka mahdollistavat laatutilausten varastoinnin prosesseja varten. Sulkeissa oleva teksti tarkoittaa ehdotettuja toimenpiteitä, kun laadunhallinta on otettu käyttöön ennen kuin _varastonhallintaprosessien laadunhallinta_ -toiminto on käytössä.

![Laadunhallintayksiköt.](media/quality-management-entity-diagram.png "Laadunhallintayksiköt")

## <a name="enablers-the-quality-item-sampling-and-quality-order-work-order-types"></a>Käyttöönotto: laatunimikkeiden otanta- ja laatutilaustyötilaustyypit

_Varastoprosessien laadunhallinta_ -toiminto sisältää kaksi työtilaustyyppiä, jotka mahdollistavat työn luomisprosessin:

- **Laatunimikkeen otanta** – Tätä työtilaustyyppiä käytetään luomaan työ, joka siirtää rekisteröidyn varaston laadunhallintaan.
- **Laatutilaus** – Tämän työtilaustyypin avulla luodaan työ, joka siirtää varaston laadunhallinnasta uuteen sijaintiin sijaintidirektiivin asetusten perusteella.

### <a name="work-classes-location-directives-and-work-templates"></a>Työluokat, sijaintidirektiivit ja työmallit

_Laatunimikkeiden otanta_- ja _laatutilausten_ työtilaustyypit kulutetaan sijaintidirektiiveissä, työluokissa ja työmalleissa.

Ennen kuin varastotyö voidaan luoda automaattisesti, jotta varasto voidaan siirtää laadunhallintaan, järjestelmä on määritettävä noudattamalla näitä ohjeita.

1. Luo erilliset työluokat _laatunimikkeiden otanta_- ja _laatutilauksen_ työtilaustyypeille. Näin varmistat, että asianmukaiset työt voidaan luoda automaattisesti kahden työtilaustyypin perusteella ja että tämä työ voidaan sitten suorittaa käyttämällä varastonhallinnnan mobiilisovellusta.
1. Määritä työmalli kullekin työtilauksen tyypille:

    - Määritä työmalli, joka käyttää _laatunimikkeen otanta_ -työtilaustyyppiä, kun haluat siirtää rekisteröidyn varaston automaattisesti laadunvalvontasijaintiin.
    - Määritä työmalli, joka käyttää _laatutilaus_ -työtilaustyyppiä, kun haluat siirtää rekisteröidyn varaston automaattisesti laadunvalvontasijainnista, kun laatukontrolli on valmis.

1. Määritä kullekin työtilaustyypille sijaintidirektiivit, joissa käytetään oikeita laadunvalvontasijainteja, joihin varasto siirretään. Kun laadunvalvonta on suoritettu, _laatutilauksen_ työtilaustyypin sijaintidirektiivin avulla varmistetaan, että uusi kohdesijainti valitaan siten, että varasto voidaan siirtää laadunvalvontasijainnista.
1. Määritä asianmukaiset mobiililaitteen valikkovaihtoehdot, jotka tukevat vastaanotetun varaston siirtoa laadunvalvonnan sijaintiin, sekä varastonsiirtoa, joka ohittaa laadunvalvonnan sijainnin tai jättää sen uuteen sijaintiin.

Jos haluat vaiheittaisen esimerkin, joka ilmaisee, miten nämä määritykset on suoritettava, katso [esimerkkiskenaario](#example-scenario) tämän artikkelin lopussa.

## <a name="enable-a-warehouse-for-quality-management"></a>Ota käyttöön varastoprosessien laadunhallinta

Ennen kuin _Varastoprosessien laadunhallinta_ -toimintoa voidaan käyttää tietyssä varastossa, sinun on tehtävä nämä toimet, jotta varasto on käytettävissä.

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Varastot**.
1. Valitse varasto ottaaksesi käyttöön laadunhallinnan.
1. Määritä **varasto**-pikavälilehdessä **Ota käyttöön laatutilaus varastoprosesseja varten** -asetukseksi _Kyllä_. (Huomaa, että tämän vaihtoehdon arvoksi voidaan määrittää _Kyllä_ vain varastoille, joissa käytetään varastonhallintaprosesseja (WMS).)

Kun **Ota käyttöön laatutilaus varastoprosesseja varten** -asetus on _Kyllä_, laatuliitosasetukset määrittävät, sovelletaanko _laadunhallinta varastoprosesseja varten_ -ominaisuutta valittuun varastoon. Voit muuttaa vaihtoehdon asetukseksi _Ei_ milloin tahansa. Tällöin toiminto ei enää koske varastoa laatuliitoksen asetuksista riippumatta.

## <a name="quality-control"></a>Laadunvalvonta

_Varastoprosessien laadunhallinta_ -toiminto ohjaa useita laatuliitosten ja nimikeotannan avainasetuksia.

### <a name="quality-associations"></a>Laatuliitokset

Jokaisessa [laatuliitostietueessa](enable-quality-management.md) määritetään myös joukko testejä, hyväksyttävän laadun taso ja otantasuunnitelma, joita käytetään laatutilauksissa, jotka luodaan. Voit määrittää laatuliitostietueen noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Laatuliitokset**.
1. Luo tai valitse laatuliitosmääritys sille nimikkeelle tai ryhmälle, jota käsittelet, tai kaikille nimikkeille.
1. Määritä **Ehdot**-pikavälilehdessä **Sovellettava varastotyyppi** -kentälle joku seuraavista arvoista:

    - **Vain varastoprosessien laadunhallinta** – Aktivoi _Varastoprosessien laadunhallinta_ -ominaisuus. Voit valita tämän arvon vain, jos viitetyyppinä on joko *Osto* tai *Tuotanto*.
    - **Kaikki** - Poista käytöstä _Varastoprosessien laadunhallinta_ -ominaisuus. Valitse tämä arvo kaikille viitetyypeille lukuun ottamatta *Ostoa* ja *Tuotantoa*.

> [!NOTE]
> _Varastoprosessien laadunhallinta_ -ominaisuus tulee voimaan vain, jos lähdeasiakirjan rivillä oleva nimike käyttää varastonhallintaprosesseja (WMS) ja jos **Ota käyttöön laatutilaus varastoprosesseja varten** -asetukseksi on valittu _Kyllä_, kun kyseessä on lähdeasiakirjan rivillä oleva varasto.

Kun jokainen nimike on rekisteröity (tai ilmoitettu valmiiksi), järjestelmä määrittää, mitä laatuliitoksia siihen sovelletaan.

Kun _varastoprosessien laadunhallinta_ on käytössä, sovellettava varastotyyppi lisätään loogisesti laatuliitoksen hakuhierarkian neljänteen hakuryhmään. Seuraavassa taulukossa on looginen esitys hakuhierarkiasta.

| Hakuryhmä | kuvaus |
|---|---|
| Ryhmä 1 | Tarkista kunkin laatuliitoksen **viitetyyppi**-, **tapahtumatyyppi**- ja **suorituksen täsmäytys** -arvot suhteessa nimikkeeseen. Jos lähdeasiakirjan riviä vasten on vastineita, siirry ryhmään 2. |
| Ryhmä 2 | Tarkista kunkin laatuliitoksen **Nimikekoodin** arvo (_taulu_, _ryhmä_ tai _kaikki_) nimikettä vasten. _Taulu_ on tarkempi kuin _ryhmä_, ja _ryhmä_ on tarkempi kuin _kaikki_. Jos _taulussa_ (tietty nimike) on vastineita, siirry ryhmään 3. Jos _taululle_ ei ole vastinetta, etsi vastinetta _ryhmää_ varten. Jos _ryhmälle_ ei ole vastinetta, _kaikki_ on voimassa. Jos kyseessä on vastine, siirry ryhmään 3. |
| Ryhmä 3 | Tarkista kullekin laatuliitokselle **tilikoodin** ja **resurssikoodin** arvot nimikettä vasten. Käytettävä logiikka muistuttaa **nimikekoodi** -arvolle sovellettavaa logiikkaa. |
| Ryhmä 4 | Tarkista kunkin laatuliitoksen osalta **sovellettava varastotyypin** arvo (_vain varastoprosessien laadunhallinta_ tai _kaikki_) nimikettä vasten. Jos **ota laatutilaus käyttöön varastoprosesseissa** -asetuksen arvoksi on määritetty lähdeasiakirjan varastoasetuksessa _Kyllä_ ja lähdeasiakirjan rivillä olevan nimikkeen määrite on _käytä varastonhallintaprosesseja_, molemmat liitokset, joissa on _vain varastoprosessien laadunhallinnan vastineita_, ja liitokset, joissa on vastine _kaikille_, ovat käytettävissä rinnakkain, jos molemmat ovat olemassa. Jos **Ota käyttöön laatutilaus varastoprosesseja varten** -asetukseksi on valittu _Ei_ lähdeasiakirjan varastolle ja lähdeasiakirjarivillä on asetettu _Käytä varastohallintaprosesseja_, vain laadunhallintaa sovelletaan. |

Olet esimerkiksi määrittänyt varaston, jossa **Ota laatutilaus käyttöön varastoprosesseille** -vaihtoehdon arvoksi on määritetty _kyllä_ ja *osto*-viitetyypille on määritetty kaksi laatuliitosta: yksi kaikille nimikkeille ja yksi *rekisteröinti*-tapahtumatyypille. Ainoa ero kahden laatuliitoksen välillä on **sovellettavan varastotyypin** arvo: sen arvoksi on määritetty _kaikki_ yhdelle laatuliitokselle ja _laadunhallinta vain varastoprosesseille_ muille . Tässä tapauksessa molemmat laatuliitokset ovat yhtä täsmällisiä, ja molemmat ovat sovellettavissa.

Laatuliitosten **testiryhmä**-kentän arvo on myös kerroin. Tässä kentässä määritetään käytettävä testimenetelmä. Jos **testiryhmä**-arvo on sama molemmille liitoksille, luodaan vain yksi laatutilaus laatuliitokselle, jossa **Sovellettava varastotyyppi** -arvo on _laadunhallinta vain varastoprosesseille_. Jos molempien liitosten **testiryhmä**-arvo ei ole sama, luodaan kaksi laatutilausta. Ensimmäinen laatutilaus luodaan laatuliitokselle, jossa **sovellettava varastotyyppi** -arvo on _vain varastoprosessien laadunhallinta_. Toinen laatutilaus luodaan laatuliitokselle, jossa **sovellettava varastotyyppi** -arvo on _Kaikki_.

> [!NOTE]
> _Vain varastoprosessien laadunhallinta_ -arvoa pidetään tarkempana kuin _Kaikki_-arvoa, kun ryhmien 1 ja 2 laatu kytkentöjen kriteerit ovat samat ja kun testiryhmä on sama. Kaksi laatutilausta luodaan vain, kun testiryhmät eroavat toisistaan.

#### <a name="reference-types"></a>Viitetyypit

Kun **viitetyypin** arvo on _osto_ ja **sovellettavan varastotyypin** arvo on _vain varastoprosessien laadunhallinta_, **tapahtumatyyppi** -kentän arvoksi **Prosessi**-pikavälilehdellä on asetettava _Rekisteröinti_. _Rekisteröinti_ on ainoa tuettu tapahtumatyyppi _osto_-viitetyypille, kun käytät _varastoprosessien laadunhallinta_ -ominaisuutta varten.

#### <a name="quality-processing-policy"></a>Laadun prosessointikäytäntö

_Varastoprosessien laadunhallinta_ -toiminto mahdollistaa töiden luomisen vain nimikeotannan perusteella. Siksi se mahdollistaa kevyen prosessin. Työn luonnin yhteydessä käytettävä varasto määräytyy laatuliitokseen liittyvän nimikeotannan mukaan. Kun käytetään kevyttä prosessia, kun työntekijä on luonut määrän laadunvalvonnan sijaintiin, laatuosasto voi luoda laatutilauksen manuaalisesti, jos laatutilaus on pakollinen.

**Laatuprosessikäytäntö**- kenttä **laatutilausprosessi**-pikavälilehdellä määrittää, luodaanko laatutilaus myös silloin, kun luodaan työ, jonka avulla nimike siirretään laadunvalvontasijaintiin. Tämä kenttä voidaan määrittää _luomaan laatutilaus_ tai _luomaan vain työ_. Oletusarvo on _Luo laatutilaus_.

> [!NOTE]
> Riippumatta siitä, luotko laatutilauksia manuaalisesti vai automaattisesti, järjestelmä luo automaattisesti työn, joka siirtää nimikkeet pois laadunvalvontasijainnista, kun laatutilaus merkitään vahvistetuksi.

Laatutilaustöiden luominen ei liity laatuliitoksen asetuksiin. Jos on olemassa työmalli , jolla on *Laatutilauksen* **Työtilauksen tyyppi** -arvo ja jos kyselyn ehdot täyttyvät kyseisessä työmallissa, laatutilauksen oikeellisuustarkistus käynnistää laatutilaustyön luomisen.

#### <a name="referenced-item-sampling"></a>Viitatun nimikkeen otanta

Jokaisella laatuliitoksella on viitattava nimikkeen otantaan. Nimikkeen otanta määrittää laadunvalvonnalla lähetettävän määrän. Se voidaan määrittää niin, että se koskee vain laatuliitoksia, joissa **sovellettava varastotyyppi** -arvo on _vain varastoprosessien laadunhallinta_. Jos **Nimikeotanta**-arvo on _kuormitus_ tai _toimitus_ tai **määrän määrityksen** arvo on _täysi rekisterikilpi_, nimikkeen otantaan voi viitata vain laatuliitoksilla, joissa **sovellettava varastotyypin** arvo on _vain varastoprosessien laadunhallinta_.

Jos määrität nimikkeen otannan, joka käyttää käytettävissä olevaa _vain varastoprosessien laadunhallinta_ -varastotyyppiä, näyttöön tulee virhesanoma, jos yrität viitata siihen laatuliitosta, joka ei käytä _laadunhallinta fyysisen varastoinnin prosessi_ -ominaisuutta.

> [!NOTE]
> Täyttä estoa käyttävää nimikeotantaa ei tueta laatuliitoksissa, joissa **Sovellettava varastotyyppi** -kentän arvo on _vain varastoprosessien laadunhallinta_.

### <a name="item-sampling"></a>Nimikeotanta

Nimikeotanta määrittää, kuinka usein nimikkeet lähetetään laadunvalvontaan. _Varastoprosessien laadunhallinta_ -ominaisuus sisältää _nimikkeen otanta-alueen käsitteen_. Järjestelmä käyttää nimikeotanta-aluetta, kun se arvioi, luodaanko laatutilaukset ja/tai laatunimikkeen otantatyöt ja laatutilaustyöt.

Voit määrittää nimikeotannan siirtymällä kohtaan **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Nimikkeen otanta** ja määrittämällä **Näytteenottoalue**-kentän arvoksi jonkin seuraavista arvoista:

- **Tilaus** – Lähdeasiakirjariviä käytetään perustana, kun arvioidaan luodaanko laatutilaukset ja/tai laatunimikeotantatyöt ja laatutilaustyöt. Tämä arvo on oletusarvo, ja kun se valitaan, järjestelmä toimii samalla tavalla kuin se toimii, kun _Varastoprosessien laadunhallinta_ -ominaisuus ei ole käytössä.
- **Kuormitus** – Kuormituksia käytetään perustana arvioitaessa, luodaanko laatutilaus ja/tai -työ. Tämä arvo on käytettävissä vain, kun _Varastoprosessien laadunhallinta_ on käytössä.
- **Lähetys** – Lähetyksiä käytetään perustana arvioitaessa, luodaanko laatutilaus ja/tai -työ. Tämä arvo on käytettävissä vain, kun _Varastoprosessien laadunhallinta_ on käytössä.

> [!NOTE]
> Kun **Otanta-alue**-kentän arvoksi on määritetty *Kuormitus* tai *Toimitus*, kuormitus- ja lähetysyksiköitä käytetään, jos ne ovat käytettävissä. Jos ne eivät ole käytettävissä, tilausyksikköä käytetään.

_Varastoprosessien laadunhallinta_ -ominaisuus sisältää myös *Täysi rekisterikilpi* -arvon **Määrän määritys** -kentälle. Tämä arvo tukee laatutilaustöiden ja laatunimikkeiden otantatöiden luomista rekisterikilpien perusteella. Kun valitset tämän arvon, tapahtuu seuraavat muutokset:

- **Jako kohteen mukaan** -vaihtoehto ja **Per n:s-rekisteri kilpi** -kenttä **Prosessi** -pikavälilehdellä ovat käytettävissä.
- **Otantamäärä**-pikavälilehden **Arvo**-kenttä ei ole käytettävissä.
- **Päivitysmäärä**-, **sijainti**-ja **rekisteri**-asetuksien arvoksi on määritetty *Kyllä* eikä asetuksia voi muuttaa.

**Taukomäärä nimikkeittäin** -vaihtoehto määrittää, arvioidaanko rekisterikilpimäärä nimikkeittäin vai kaikkien otantanimikkeiden välillä. Tuotevariantteja käsitellään samalla nimikkeellä. Tämä vaihtoehto myös määrittää, nollataanko kunkin nimikkeen rekisterikilven määrä.

**Per n:s rekisterikilpi** -kentän arvo määrittää, kuinka usein laatutilaukset luodaan suhteessa rekisteröitävien nimikkeiden määrään. Esimerkiksi arvo *3* lähettää jokaisen kolmannen nimikkeen laadunhallintaan aloittaen ensimmäisestä nimikkeestä. Arvon on oltava suurempi kuin 0 (nolla).

Kun työntekijät vastaanottavat nimikkeitä varastonhallinnnan mobiilisovelluksen avulla, järjestelmä tarkistaa, onko kullekin saapuvalle nimikkeelle määritetty laatuliitos. Jos laatuliitos on määritetty, järjestelmä käyttää kyseiselle laatuliitokselle määritetyn nimikkeen otantatietuetta määrittääkseen, miten se luo laatutilauksia, laatunimikkeiden otantatyötä ja ostotilaustyötä.

> [!NOTE]
> Kun vastaanoton rekisteröiminen tehdään WWW-asiakasohjelmassa (käyttämällä pientä rekisteröitymissivua tai nimikkeen saapumisen kirjauskansiota ostotilausriveille), laatunimikkeen otanta- tai ostotilaustyötä ei luoda asetuksista riippumatta. Laatuliitoksesta vastaavien nimikkeiden osalta viitatun nimikkeen otantaa käytetään vain laatutilausten luonnin ohjaamiseen.

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Esimerkkejä laatutilausten automaattisesta luomisesta

Seuraavissa esimerkeissä havainnollistetaan, miten laatuliitoksen ja siihen liittyvän nimikeotannan asetukset vaikuttavat laatutilausten luontiin, kun **Sovellettava varastotyyppi** -kentän arvo on _Vain varastoprosessien laadunhallinta_.

Kun **Määrämäärityksen** arvo on _Täysi rekisterikilpi_, **Per n:s rekisterikilpi** -kenttä määrittää, mikä rekisterikilven laatunimikkeiden otantatyö luodaan. Ensimmäinen rekisterikilpi menee aina laadunvalvontaan, ja sitten tämän kentän arvo määrittää, että jokaisen *n*:nnen rekisterikilven tämän rekisterikilven jälkeen pitäisi myös mennä.

Seuraavien esimerkkien **Viitetyypin** arvo on _Osto_- ja **Tapahtumatyypin** arvo on *Rekisteröinti*.

| Otanta-alue | Määrän määritys | Päivitettyä määrää kohden | Varastodimension mukaan | Katkomäärä nimikkeittäin | Per n:s rekisterikilpi | Tulos |
|---|---|---|---|---|---|---|
| Tilaus | Koko rekisterikilpi | Kyllä _(lukittu/ei muokattavissa)_ | <p>Paikka: Kyllä</p><p>Rekisterikilpi: Kyllä _(lukittu/ei muokattavissa)_</p> | Ei | 3 | <p>**Tilausrivin määrä: 100 EA**</p><ol><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 20 EA, LP1<p>Laatunimikkeen otantatyötä 20 EA:lle</p><p>Laatutilaus 1 20 EA:lle</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 20 EA, LP2<p>Ostotilaustyö 20 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 20 EA, LP3<p>Ostotilaustyö 20 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 20 EA, LP4<p>Laatunimikkeen otantatyötä 20 EA:lle</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 20 EA, LP5<p>Ostotilaustyö 20 EA:lle (hyllytys)</p></li></ol> |
| Tilaus | Kiinteä määrä = 1 | Kyllä | <p>Paikka: Kyllä</p><p>Rekisterikilpi: Kyllä</p> | Ei | Ei käytettävissä | <p>**Tilausrivin määrä: 100**</p><ol><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 20 EA, LP1<p>Laatunimikkeen otantatyötä 1 EA:lle</p><p>Laatutilaus 1 1 EA:lle</p><p>Ostotilaustyö 19 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 20 EA, LP2<p>Laatunimikkeen otantatyötä 1 EA:lle</p><p>Laatutilaus 1 1 EA:lle</p><p>Ostotilaustyö 19:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 20 EA, LP3<p>Laatunimikkeen otantatyötä 1 EA:lle</p><p>Laatutilaus 1 1 EA:lle</p><p>Ostotilaustyö 19 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 20 EA, LP4<p>Laatunimikkeen otantatyötä 1 EA:lle</p><p>Laatutilaus 1 1 EA:lle</p><p>Ostotilaustyö 19 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 20 EA, LP5<p>Laatunimikkeen otantatyötä 1 EA:lle</p><p>Laatutilaus 1 1 EA:lle</p><p>Ostotilaustyö 19 EA:lle (hyllytys)</p></li></ol> |
| Tilaus | Prosentti = 10 | Ei | <p>Sijainti: Ei</p><p>Rekisterikilpi: Ei</p> | Ei | Ei käytettävissä | <p>**Tilausrivin määrä: 100 EA**</p><ol><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 50 EA, LP1<p>Laatunimikkeen otantatyötä 10 EA:lle</p><p>Laatutilaus 1 10 EA:lle</p><p>Ostotilaustyö 40 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 50 EA, LP2<p>Ostotilaustyö 50 EA:lle (hyllytys)</p></li></ol> |
| Lastaa | Prosentti = 5 | Kyllä _(lukittu/ei muokattavissa)_ | <p>Sijainti: Ei</p><p>Rekisterikilpi: Ei</p> | Ei | Ei käytettävissä | <p>**Tilausrivin määrä: 500 EA**</p><p>**Kaksi kuormitusta: ensimmäinen kuorma 200 EA, toinen kuorma 300 EA**</p><ol><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa ensimmäiselle kuormitukselle 100 EA<p>Laatunimikkeen otantatyötä 5 EA:lle</p><p>Laatutilaus 1 5 EA:lle</p><p>Ostotilaustyö 95 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa ensimmäiselle kuormitukselle 100 EA<p>Laatunimikkeen otantatyötä 5 EA:lle</p><p>Laatutilaus 1 5 EA:lle</p><p>Ostotilaustyö 95 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa toiselle kuormitukselle 300 EA<p>Laatunimikkeen otantatyötä 15 EA:lle</p><p>Laatutilaus 1 15 EA:lle</p><p>Ostotilaustyö 285 EA:lle (hyllytys)</p></li></ol> |
| Järjestys | Prosentti = 10 | Kyllä | <p>Paikka: Kyllä</p><p>Rekisterikilpi: Kyllä</p> | Ei | Ei käytettävissä | <p>**Tilausrivin määrä: 100**</p><ol><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 50 EA, LP1<p>Laatunimikkeen otantatyötä 5 EA:lle</p><p>Laatutilaus 1 5 EA:lle</p><p>Ostotilaustyö 45 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 50 EA, LP2<p>Laatunimikkeen otantatyötä 5 EA:lle</p><p>Laatutilaus 1 5 EA:lle</p><p>Ostotilaustyö 45:lle (hyllytys)</p></li></ol> |
| Kuorma | Koko rekisterikilpi | Kyllä _(lukittu/ei muokattavissa)_ | <p>Paikka: Kyllä</p><p>Rekisterikilpi: Kyllä _(lukittu/ei muokattavissa)_</p> | Ei | 3 | <p>**Kaksi nimikettä:**</p><ul><li>**Nimikkeen A tilausrivien määrä: 120 EA (4 kuormalavaa)**</li><li>**Nimikkeen B tilausrivien määrä: 90 EA (3 kuormalavaa)**</li></ul><p>**Yksi kuormitus, kaksi kuormaviivaa ja tilausrivi**</p><ol><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa nimikkeelle A, 30 EA, LP1<p>Laatunimikkeen otantatyötä 30 EA:lle</p><p>Laatutilaus 1 30 EA:lle</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa nimikkeelle A, 30 EA, LP2<p>Ostotilaustyö 30 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa nimikkeelle A, 30 EA, LP3<p>Ostotilaustyö 30 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa nimikkeelle A, 30 EA, LP4<p>Laatunimikkeen otantatyötä 30 EA:lle</p><p>Laatutilaus 1 30 EA:lle</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa nimikkeelle B, 30 EA, LP5<p>Ostotilaustyö 30 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa nimikkeelle B, 30 EA, LP6<p>Ostotilaustyö 30 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa nimikkeelle A, 30 EA, LP7<p>Laatunimikkeen otantatyötä 30 EA:lle</p><p>Laatutilaus 1 30 EA:lle</p></li></ol> |
| Kuorma | Koko rekisterikilpi | Kyllä _(lukittu/ei muokattavissa)_ | <p>Paikka: Kyllä</p><p>Rekisterikilpi: Kyllä _(lukittu/ei muokattavissa)_</p> | Kyllä | 3 | <p>**Kaksi nimikettä:**</p><ul><li>**Nimikkeen A tilausrivien määrä: 120 EA (4 kuormalavaa)**</li><li>**Nimikkeen B tilausrivien määrä: 90 EA (3 kuormalavaa)**</li></ul><p>**Yksi kuormitus, kaksi kuormaviivaa ja tilausrivi**</p><ol><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa nimikkeelle A, 30 EA, LP1<p>Laatunimikkeen otantatyötä 30 EA:lle</p><p>Laatutilaus 1 30 EA:lle</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa nimikkeelle A, 30 EA, LP2<p>Ostotilaustyö 30 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa nimikkeelle A, 30 EA, LP3<p>Ostotilaustyö 30 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa nimikkeelle A, 30 EA, LP4<p>Laatunimikkeen otantatyötä 30 EA:lle</p><p>Laatutilaus 1 30 EA:lle</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa nimikkeelle B, 30 EA, LP5<p>Laatunimikkeen otantatyötä 30 EA:lle</p><p>Laatutilaus 1 30 EA:lle</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa nimikkeelle B, 30 EA, LP6<p>Ostotilaustyö 30 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa nimikkeelle A, 30 EA, LP7<p>Ostotilaustyö 30 EA:lle (hyllytys)</p></li></ol> |
| Kuorma | Prosentti = 10 | Kyllä _(lukittu/ei muokattavissa)_ | <p>Sijainti: Ei</p><p>Rekisterikilpi: Ei</p> | Ei | Ei käytettävissä | <p>**Tilausrivin määrä: 100 EA**</p><p>**Kuormituksia ei ole luotu. Tilauksen laajuutta käytetään.**</p><ol><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 50 EA, LP1<p>Laatunimikkeen otantatyötä 5 EA:lle</p><p>Laatutilaus 1 5 EA:lle</p><p>Ostotilaustyö 45 EA:lle (hyllytys)</p></li><li>Rekisteröintikuitti varastonhallinnnan mobiilisovelluksessa kohteelle 50 EA, LP2<p>Laatunimikkeen otantatyötä 5 EA:lle</p><p>Laatutilaus 1 5 EA:lle</p><p>Ostotilaustyö 45 EA:lle (hyllytys)</p></li></ol> |

Kun työntekijä vahvistaa jonkin edellisessä taulussa näytetyistä laatutilauksista, järjestelmä luo automaattisesti laatutilaustyön, jonka avulla varasto siirretään laadunhallintasijainnista sijaintiin, joka on määritetty _laatutilauksen_ työtilaustyypin sijaintidirektiivissä. Voit määrittää tähän tarkoitukseen minkä tahansa sijaintipaikan, kuten palautuksen tai varastopaikan, laatutilauksen testituloksen mukaan. Esimerkki tästä asennuksesta on tämän artikkelin lopussa olevassa [esimerkkiskenaariossa](#example-scenario).

Voit avata uudelleen laatutilauksen, joka on jo vahvistettu. Jos laatutilauksen työ, joka liittyy varaston siirtämiseen laadunvalvontasijainnista, ei ole *suljetun* tai *käynnissä olevan* **työn tilan** arvo.

## <a name="process-insights-when-multiple-quality-associations-coexist"></a>Käsittele kävijätietoja, kun useita laatuliitoksia on rinnakkain

Samaan lähdeasiakirjan riviin voidaan määrittää useita laatuliitoksia, ja **Käytettävissä oleva varastotyyppi** -kentän arvoksi voidaan määrittää _Vain varastoprosessien laadunhallinta_ joillekin laatuliitoksille ja _Kaikki_ muille.

Seuraavassa esimerkissä **Viitetyypin** arvo on _Osto_.

1. Ensimmäinen laatuliitos määritetään seuraavalla tavalla:

    - **Sovellettava varastotyyppi:** *Vain varastoprosessien laadunhallinta*
    - **Nimikekoodi:** *A0001*
    - **Tilikoodi:** *Kaikki*
    - **Testiryhmä:** *Kehys*
    - **Nimikeotanta:** *5 kpl*

1. Toinen laatuliitos määritetään seuraavalla tavalla:

    - **Sovellettava varastotyyppi:** *Kaikki*
    - **Nimikekoodi:** *Kaikki*
    - **Tilikoodi:** *Kaikki*
    - **Testiryhmä:** *Kehys*
    - **Nimikeotanta:** *1 kpl*

1. Kolmas laatuliitos määritetään seuraavalla tavalla:

    - **Sovellettava varastotyyppi:** *Vain varastoprosessien laadunhallinta*
    - **Nimikekoodi:** *Kaikki*
    - **Tilikoodi:** *104*
    - **Testiryhmä:** *Impedanssi*
    - **Nimikeotanta:** *Joka toinen rekisterikilpi* (Tämä asetus tarkoittaa, että ensimmäinen, kolmas, viides ja niin edelleen vastaanotettu rekisterikilpi luo laatutilauksen.)

1. Neljäs laatuliitos määritetään seuraavalla tavalla:

    - **Sovellettava varastotyyppi:** *Kaikki*
    - **Nimikekoodi:** *Kaikki*
    - **Tilikoodi:** *Kaikki*
    - **Testiryhmä:** *Impedanssi*
    - **Nimikeotanta:** *5 kpl*

1. Viides laatuliitos määritetään seuraavalla tavalla:

    - **Sovellettava varastotyyppi:** *Kaikki*
    - **Nimikekoodi:** *Kaikki*
    - **Tilikoodi:** *Kaikki*
    - **Testiryhmä:** *Kartio*
    - **Nimikeotanta:** *10 %*

Toimittajalle 104 luodaan nyt ostotilaus, jonka määrä on 10 A0001-nimikettä. Tämän jälkeen ostotilausrivi, jonka määrä on 10, rekisteröidään yhteen rekisterikilpeen käyttämällä varastonhallinnnan mobiilisovellusta. Tulos näyttää tältä:

- *Kehys*-testiryhmän ensimmäisestä laatuliitoksesta on yksi laatutilaus. Määrä on 5. Toisesta laatuliitoksesta ei ole laatutilausta, koska ensimmäisen laatuliitoksen kriteerit ovat tarkempia suhteessa *Kehys*-testiryhmään.
- *Impedanssi*-testiryhmän kolmannesta laatuliitoksesta on yksi laatutilaus. Määrä on 10. Neljännestä laatuliitoksesta ei ole laatutilausta, koska ensimmäisen laatuliitoksen kriteerit ovat tarkempia suhteessa *Impedanssi*-testiryhmään.
- *Kartio*-testiryhmän viidennestä laatuliitoksesta on yksi laatutilaus. Määrä on 1.

Laatunimikkeen otantatyö luodaan myös, kun luodaan kullekin kolmelle laatuliitokselle yksi laatutilaus. Rekisteröity määrä on vain 10. Nimikkeen otanta-asetusten vuoksi laatutilausmäärien summa, joka luodaan *vain varastoprosessien laadunhallintaa* varten, koskee vain varastotyyppiä 16, joka ylittää fyysisen rekisteröidyn määrän 10. Tämän vuoksi työtä ei tehdä kaikille laatutilausmäärille (16), sillä vain 10 on fyysisesti käytettävissä laadunvalvontasijaintiin siirtämistä varten. Laatunimikkeiden otantatyön luonnissa käytettävä prioriteetti seuraa laatutilauksen luonnin järjestystä:

- **Ensimmäinen laatutilaus (määrä = 5):** Laatunimikkeen otantatyöt luodaan 5:lle. Jäljellä oleva määrä on nyt 5 (10 – 5) laadullisten esineiden otantatöiden luomiseksi.
- **Toinen laatutilaus (määrä = 10):** Laatunimikkeen otantatyöt luodaan 5:lle. Jäljellä oleva määrä on nyt 0 (nolla) laadullisten esineiden otantatöiden luomiseksi.
- **Kolmas laatutilaus (määrä = 1):** Laatunimikkeiden otantatöitä ei luoda.

Laatutilausten luonnin yhteydessä luodaan varastoesto, jonka määrä on 10. Tämä varastoesto viitataan kolmeen laatutilaukseen. Laatutilausmäärien summa on 16.

Kun laatutilaukset tarkistetaan, järjestelmä yrittää luoda laatutilaustyön kullekin vahvistettavalle laatutilaukselle. Koska laatutilausmäärien summa ylittää tosiasiallisesti estetyn määrän ja on näin ollen käytettävissä myös työn luonnissa, laatutilauksia ei voi luoda koko laatutilausmäärälle, kuten tässä on esitetty. (Tämä esimerkki jatkaa edellistä esimerkkiä.)

1. **Tarkista toinen luotava laatutilaus (määrä = 10). Laatutilaustyöt luodaan määrälle 4.**

    Laatutilaustyön luonti perustuu varastoestomäärän muutokseen. Koska laatutilausmäärien summa oli 16, määrän 10 vahvistus aiheuttaa jäljellä olevien laatutilausmäärien vahvistamisen yhtä suureksi kuin 6. Varastoestomäärä vähennetään 10:stä 6:een. Alennettu määrä 4 on varattu laatutilauksen työn luomiseen.

2. **Tarkista ensimmäinen luotava laatutilaus (määrä = 5). Laatutilaustyöt luodaan määrälle 5.**

    Laatutilaustyön luonti perustuu varastoestomäärän muutokseen. Koska laatutilausmäärien summa oli 6, määrän 5 vahvistus aiheuttaa jäljellä olevien laatutilausmäärien vahvistamisen yhtä suureksi kuin 1. Varastoestomäärä vähennetään 6:stä 1:een. Alennettu määrä 5 on varattu laatutilauksen työn luomiseen.

3. **Tarkista kolmas luotava laatutilaus (määrä = 1). Laatutilaustyöt luodaan määrälle 1.**

    Laatutilaustyön luonti perustuu varastoestomäärän muutokseen. Koska laatutilausmäärien summa oli 1, määrän 1 vahvistus aiheuttaa jäljellä olevien laatutilausmäärien vahvistamisen yhtä suureksi kuin 0 (nolla). Varastoesto poistetaan (eli varastoestomäärä vähennetään 1:stä 0:an). Alennettu määrä 1 on varattu laatutilauksen työn luomiseen.

> [!NOTE]
> Laatutilaustöiden luonti riippuu varastoestomäärästä, johon viitataan vähintään yhdessä laatutilauksessa. Jos laatutilausmäärien summa ylittää viitatun varastoestomäärän, laatutilausten luonnin tilauksen oikeellisuustarkistus määrittää laatutilaustyön luomisen.

## <a name="canceling-quality-item-sampling-work"></a>Laatunimikkeen otantatyön peruuttaminen

Voit peruuttaa laatunimikkeiden otantaa varten luodun työn. Voit määrittää, mitä tapahtuu, kun tämä työ peruutetaan, noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
1. Määritä **Yleinen**-välilehden **Työ**-pikavälilehden **Poista kuitti, kun työ peruutetaan** -asetus on jokin seuraavista arvoista:

    - **Kyllä** – Kun laatunimikkeiden otantatyöt peruutetaan, siihen liittyvä laatutilaus poistetaan ja varasto ei ole rekisteröity.
    - **Ei** – Kun laatunimikkeiden otantatyöt peruutetaan, siihen liittyvää laatutilausta ei poisteta ja varaston rekisteröintiä ei poisteta.

## <a name="cross-docking"></a>Cross-docking

Voit määrittää laatuliitosmäärityksen, joka luo nimikkeen otantatyöt. Kun cross-docking-vaihtoehto on olemassa ja laatuliitos luo laatunimikkeiden otantatyöt, jos määrä on riittävä vain cross-dockingin tyydyttämiseksi, vain nimikkeen otantatyöt luodaan. Sellaisissa tapauksissa, joissa **Ota käyttöön laatutilaus varastoprosesseissa** -asetuksen arvoksi vastaanottavalle varastolle on määritetty _Kyllä_ ja **käytettävissä olevan varaston tyyppi** -kentän arvoksi on määritetty _Vain varastoprosessien laadunhallinta_ laatukytkentää varten, laatunimikkeiden otantatöiden luominen ohittaa cross-docking-työn luomisen. Jos määrä on suurempi kuin cross-dockingin tarve, järjestelmä luo edelleen vain nimikkeiden otantatyöt.

## <a name="destructive-testing"></a>Destruktiivinen testaus

Voit määrittää testiryhmän, joka suorittaa destruktiivisen testauksen. Destruktiivisen testin tapauksessa oletetaan, että testattavan nimikkeen määrä tuhotaan testin yhteydessä riippumatta siitä, mikä on testin tulos. Tapa, jolla _laadunhallinta varastoprosesseissa_ -toiminto tukee destruktiivista testausta, muistuttaa tapaa, jolla laadunhallinta tukee sitä, kun ominaisuutta ei ole otettu käyttöön. Ennen kuin laatutilaus voidaan vahvistaa, laatupäällikön on määritettävä tuhoutuneen määrän keräilysijainti. Voit rekisteröidä keräilyn laatutilaussivulta valitsemalla toimintoruudusta **Varasto \> Keräily**. Kun laatutilauksen määrän poiminta on rekisteröity, oikeellisuustarkistus voidaan suorittaa.

## <a name="example-scenario"></a>Esimerkkiskenaario

### <a name="prepare-the-scenario"></a>Skenaarion valmisteleminen

Jos haluat käsitellä tätä skenaariota, sinun on valmisteltava järjestelmä seuraavalla tavalla:

- Varmista, että demotiedot on asennettu järjestelmään, ja valitse **USFM**-yritys.
- Ota käyttöön _Varastoprosessien laadunhallinta_ -ominaisuus kohdassa [ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Määritä varasto 51, jos haluat käyttää _Laadunhallintaa varastoprosesseja varten_ seuraavasti:

    1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Varastot**.
    1. Valitse varasto 51.
    1. Määritä **varasto**-pikavälilehdessä **Ota käyttöön laatutilaus varastoprosesseja varten** -asetukseksi *Kyllä*.

### <a name="quality-in-setup--move-to-the-quality-control-location"></a>Laatuasetusten määrittäminen – Siirry laadunvalvontasijaintiin

Tämän jälkeen sinun on valmisteltava perusmääritys, jonka avulla järjestelmä voi tukea varaston 51 _laadunhallintavarastoprosessi_-ominaisuuksia varten. (Demotiedot määrittävät laadunhallintasijainnin, jonka nimi on *QMS*. Tähän sijaintiin viitataan useaan kertaan tässä skenaariossa.) Seuraavat elementit valmistellaan tämän osan alakohdissa kuvatulla tavalla:

- Työluokka
- Työmalli
- Sijaintidirektiivi
- Nimikeotanta
- Laatuliitos
- Mobiililaitteen valikkovaihtoehdot

#### <a name="work-class-for-quality-in"></a>Laatuluokan työluokka

1. Valitse **Varastonhallinta \> Asetukset \> Työ \> Työluokka**.
1. Luo työluokka ja määritä seuraavat arvot:

    - **Työluokan tunnus:** _QualityIn_
    - **Kuvaus:** _Laatunimikkeen otanta_
    - **Työtilauksen tyyppi:** _Laatunimikkeen otanta_

#### <a name="work-template"></a>Työmalli

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Valitse **Työtilaustyyppi** -kentässä _Laatunimikkeen otanta_.
1. Luo työmalli ja määritä seuraavat arvot:

    - **Työmalli:** _51 laatu_
    - **Työmallin kuvaus:** _51 laatu_

1. Lisää rivi työmalliin ja määritä seuraavat arvot:

    - **Työtyyppi:** _Poiminta_
    - **Työluokan tunnus:** _QualityIn_

1. Lisää toinen rivi työmalliin ja määritä seuraavat arvot:

    - **Työtyyppi:** _Aseta_
    - **Työluokan tunnus:** _QualityIn_

#### <a name="location-directive"></a>Sijaintidirektiivi

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Valitse **Työtilaustyyppi** -kentässä _Laatunimikkeen otanta_.
1. Luo sijaintidirektiivi ja määritä seuraavat arvot:

    - **Nimi:** _51 laatuun_
    - **Työtyyppi:** _Aseta_
    - **Toimipaikka:** 5
    - **Varasto**: _51_

1. Lisää rivi sijaintidirektiiville ja määritä seuraavat arvot:

    - **Määrästä:** _1_
    - **Määrälle:** _1000000_

1. Luo sijaintidirektiivitoiminto ja määritä seuraava arvo:

    - **Nimi:** _Laatu_

1. Valitse uusi sijaintidirektiivitoiminto kohdasta **Muokkaa kyselyä** ja määritä **Alue**-tietue, jolla on seuraavat arvot:

    - **Taulu:** *Sijainnit*
    - **Kenttä:** _Sijaintiprofiilin tunnus_
    - **Kriteerit:** *QMS*

1. Tallenna kysely valitsemalla **OK** ja tallenna uusi sijaintidirektiivi.

Seuraavaksi sinun on muutettava aiemmin luodun ostotilauksen sijaintidirektiivien järjestystä varastolle 51. Demotiedot sisältävät kaksi sijaintidirektiiviä, joiden _osto_-arvo on **Työtilaustyyppi**: toisen nimi on _51 QMS_ ja toisen nimi on _51 PO Direct_. Varmista, että _51 QMS_ -sijaintidirektiiviä ei käytetä varmistamalla, että varaston 51 *varastoprosessien laatuhallinta* -toiminto on käytössä. Sen sijaan, että poistaisit kyseisen sijaintidirektiivin (koska haluat ehkä käyttää sitä tulevaisuudessa), voit vain muuttaa järjestystä.

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Aseta **Työtilaustyyppi**-kentän arvoksi _Ostotilaus_.
1. Valitse järjestysluettelosta järjestysnumero 5 _51 PO Direct_ -toimipaikkadirektiiville.
1. Siirrä valittu järjestys järjestysnumeron 4 mukaan.
1. Tarkista, että _51 QMS_ -sijaintidirektiivin järjestysnumero on nyt vähintään 5.

#### <a name="item-sampling"></a>Nimikeotanta

_Varastoprosessien laadunhallinta_ -toiminto lisää uusia nimikkeen otantatoimintoja. **Otanta-alueen** arvo voi nyt olla _Tilaus_, _Lähetys_ tai _Kuormitus_ ja **Otantamäärä**-arvo voi nyt olla _Täysi rekisterikilpi_.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Nimikeotanta**.
1. Luo nimikeotantatietue ja määritä seuraavat arvot:

    - **Nimikeotanta:** _kolmas LP_
    - **Kuvaus:** _Joka kolmas rekisterikilpi_
    - **Otanta-alue:** _Tilaus_

1. Aseta **määrämääritys**-kentän arvoksi _täysi rekisterikilpi_ **otantamäärä**-pikavälilehdessä.
1. Määritä **Prosessi**-pikavälilehden **Per n:s rekisterikilpi** -kentän arvoksi _3_.
1. Ota **per varastodimensio**-osassa käyttöön sekä **varasto** että **varaston tila**.

#### <a name="quality-associations"></a>Laatuliitokset

Luo laatuliitos, joka käyttää uutta nimikeotantaa.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Laatuliitokset**.
1. Luo laatuliitostietue ja määritä seuraavat arvot:

    - **Viitetyyppi:** _Osto_
    - **Nimikekoodi:** _Taulu_
    - **Nimike:** _M9201_
    - **Toimipaikka:** _5_

1. Määritä **Prosessi**-pikavälilehden **Tapahtumatyyppi**-kentän arvoksi *Rekisteröinti*.
1. Määritä **Ehdot**-pikavälilehdessä **Käytettävä varastotyyppi** -kentän arvoksi *Vain varastoprosessien laadunhallinta*.
1. Määritä **Laatutilausprosessi**-pikavälilehdellä **Laatukäsittelykäytäntö**-kentän arvoksi _Luo laatutilaus_.
1. Napsauta **Määritykset**- pikavälilehden **Testiryhmä**-kenttää hiiren kakkospainikkeella ja avaa sitten **Testiryhmät**-sivu valitsemalla **Näytä tiedot**.
1. Luo **Testiryhmät**-sivun yläruudukon **Yhteenveto**-välilehdessä koeryhmä ja määritä seuraavat arvot:

    - **Testiryhmä:** _QMS_
    - **Kuvaus:** _QMS-testi_
    - **Hyväksyttävä määrä:** _100_
    - **Nimikeotanta:** _kolmas LP_ (Valitse)

1. Lisää yhden testin tietue alemman ruudukon **Yhteenveto**-välilehdessä ja määritä seuraavat arvot:

    - **Järjestys:** *1*
    - **Testi:** *Kehyksen mittaus*

1. Määritä alemman ruudukon **Testi**-välilehdessä seuraavat arvot:

    - **Testimuuttujat:** *Hyväksytty/Hylätty*
    - **Oletustulos:** *Hyväksytty*

1. Tallenna uusi testiryhmä ja sulje **Testiryhmät**-sivu.
1. Palaa **Laatukytkennät**-sivulle, valitse **Testiryhmä**-kentässä **QMS**.
1. Tallenna tietue.

#### <a name="mobile-device-menu-items-for-quality-in"></a>Mobiililaitteen valikkovaihtoehdot laadun mukaan

Jotta voit siirtää tavarat laatuvalvonnan sijaintiin, määritä laatunimikkeen otantatoiminto käytettäväksi mobiililaitteen valikkovaihtoehdon avulla.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse **Oston hyllytys** -mobiililaitevalikkovaihtoehto.
1. Lisää **Työluokat**-pikavälilehden työluokan tunnus kohtaan *QualityIn*.

#### <a name="summary-your-setup-to-move-goods-to-quality-control"></a>Yhteenveto: määrityksesi siirtää tavarat laadunvalvontaan

Olet nyt määrittänyt laatuliitoksen, joka käynnistää laatutilauksen luomisen käyttämällä *Laadunhallinta varastoprosesseja varten* -toimintoa. Olet määrittänyt varaston 51 työ- ja sijaintitiedot sen varmistamiseksi, että tietty työ luodaan, kun nimikkeelle M9201 tehdään ostokirjaus. Tämä asetus varmistaa, että joka kolmas rekisteröity rekisterikilpi siirretään laatusijaintiin (_QMS_) ja että rekisterikilven määrälle luodaan laatutilaus. Kaikki muu siirretään hyllytykseen laadunvalvonnan sijainnin asemesta.

### <a name="process-quality-management-work"></a>Prosessin laadunhallintatyö

1. Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Luo ostotilaus ja määritä seuraavat arvot:

    - **Määritä toimittajatili:** *104*
    - **Varasto**: *51*

1. Lisää ostotilausrivi ja määritä seuraavat arvot:

    - **Nimike:** *M9201*
    - **Määrä** *20*
    - **UoM:** *ea*
    - **Varasto**: *51*

1. Kirjoita ostotilauksen numero muistiin, jotta voit käyttää sitä myöhemmin.
1. Siirry mobiililaitteeseen tai emulaattorille, joka käyttää varastonhallinnnan mobiilisovellusta, ja kirjaudu varastoon 51 käyttämällä lukua *51* käyttäjätunnuksena ja lukua *1* salasanana.
1. Siirry kohtaan **Saapuva \> Oston vastaanotto** ja syötä seuraavat arvot:

    - **PONum:** Kirjoita juuri luomasi ostotilauksen numero
    - **Määrä:** *5*
    - **Yksikkö:** *ea*

1. Jatka vastaanottamista linjaa vastaan *5 ea* kerrallaan, kunnes rivi on täysin vastaanotettu. (Yhteensä neljä rekisterikilpeä luodaan.)
1. Kirjaudu ulos varastonhallinnan mobiilisovelluksesta.
1. Siirry WWW-asiakasohjelmassa kohtaan **Hankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Etsi ja avaa ostotilaus.
1. Valitse **Ostotilausrivit**-osassa nimiketunnuksen *M9201* rivi ja valitse sitten **Ostotilausrivit \> Työtiedot**.
1. Huomaa, että luodut toisen ja kolmannen työn otsikot ovat tavallisia hyllytystöitä, kun taas ensimmäisen ja neljännen työn otsikot ovat laatunimikkeiden otantatöitä. Tämä tulos on yhdenmukainen nimikkeen otantamäärityksen kanssa, joka on määritetty ottamaan otokseen joka kolmas rekisterikilpi.

#### <a name="move-to-the-quality-control-location"></a>Siirry laadunvalvonnan sijaintiin

Voit nyt siirtää rekisterikilvet niiden nimetyille paikoille. Ensimmäinen ja neljäs rekisterikilpi menee laadunvalvontapaikkaan, kun taas toinen ja kolmas rekisterikilpi siirtyy suoraan varastoon.

1. Siirry mobiililaitteeseen tai emulaattorille, joka käyttää varastonhallinnnan mobiilisovellusta, ja kirjaudu varastoon 51 käyttämällä lukua *51* käyttäjätunnuksena ja lukua *1* salasanana.
1. Siirry kohtaan **Saapuva \> Oston hyllytys** ja siirrä kukin rekisterikilpi edellisestä menettelystä, kunnes olet sulkenut kaikki työt.

#### <a name="summary-process-quality-management-work"></a>Yhteenveto: Prosessin laadunhallintatyö

Olet nyt suorittanut ensimmäisen ja neljännen rekisterikilven laatunimikkeiden otantatyöt siirtämällä ne laadunvalvontasijaintiin. Olet myös hyllyttänyt toisen ja kolmannen rekisterikilven. Seuraava vaihe on laatutilauksen testauksen ja hallinnan testaaminen.

### <a name="quality-out-setup-move-from-the-quality-control-location-to-storage-or-return"></a>Lähtevä laatumääritys: Siirry laadunvalvontasijainnista varastoon tai palaa

Kun työntekijät raportoivat laatutilauksen tuloksista, järjestelmä luo automaattisesti työn.

Seuraavaksi jatkat työluokan, työmallin ja sijaintidirektiivin tarvittavia perusasetuksia, jotta voit ottaa laadunhallinnan käyttöön varastoprosesseissa. Näin voidaan luoda tarvittava työ, jotta laatutilauksen määrä voidaan siirtää laadunvalvontasijainnista nimettyyn varastopaikkaan.

#### <a name="work-class-for-quality-out"></a>Lähtevä laatutyöluokka

1. Valitse **Varastonhallinta \> Asetukset \> Työ \> Työluokka**.
1. Luo työluokka ja määritä seuraavat arvot:

    - **Työluokan tunnus:** *QualityOut*
    - **Kuvaus:** *Lähtevä laatu*
    - **Työtilauksen tyyppi:** *Laatutilaus*

#### <a name="work-templates"></a>Työmallit

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Muuta **Työtilauksen tyypin** arvoksi *Laatutilaus*.
1. Luo työmalli ja määritä seuraavat arvot:

    - **Työmalli:** *51 lähtevä laatu*
    - **Työmallin kuvaus:** *51 lähtevä laatu*

1. Lisää rivi ja määritä seuraavat arvot:

    - **Työtyyppi:** *Poiminta*
    - **Työluokan tunnus:** **QualityOut**

1. Lisää toinen rivi ja määritä seuraavat arvot:

    - **Työtyyppi:** *Aseta*
    - **Työluokan tunnus:** *QualityOut*

#### <a name="location-directives"></a>Sijaintidirektiivit

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Muuta **Työtilauksen tyypin** arvoksi *Laatutilaus*.
1. Luo sijaintidirektiivi ja määritä seuraavat arvot:

    - **Nimi:** *51 Hyväksytty*
    - **Työtyyppi:** *Aseta*
    - **Toimipaikka:** *5*
    - **Varasto**: *51*

1. Valitse toimintoruudussa **Muokkaa kyselyä**, jotta voit avata kyselyeditori-valintaikkunan.
1. Määritä **Arvojoukko**-välilehdessä seuraavat arvot:

    - **Taulu:** *Laatutilaukset*
    - **Kenttä:** *Tila*
    - **Kriteerit:** *Hyväksytty*

1. Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.
1. Lisää **Rivit**-pikavälilehdellä rivi ja määritä seuraavat arvot:

    - **Määrästä:** *1*
    - **Määrälle:** *1000000*

1. Lisää rivi **Sijaintidirektiivin toimenpiteet** -pikavälilehdessä ja määritä seuraava arvo:

    - **Nimi:** *Hyväksytty*

1. Valitse **Sijaintidirektiivin toiminto** -pikavälilehdessä **Muokkaa kyselyä**, jotta voit avata kyselyeditori-valintaikkunan.
1. Määritä **Arvojoukko**-välilehdessä seuraavat arvot:

    - **Taulu:** *Sijainnit*
    - **Kenttä:** *Alueen tunnus*
    - **Kriteerit:** *Bulkki*

1. Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.
1. Valitse toimintoruudussa **Tallenna** tallentaaksesi uuden sijaintidirektiivin.
1. Luo toinen sijaintidirektiivi ja määritä seuraavat arvot:

    - **Nimi:** *51 Hylätty*
    - **Työtyyppi:** *Aseta*
    - **Toimipaikka:** *5*
    - **Varasto**: *51*

1. Valitse toimintoruudussa **Muokkaa kyselyä**, jotta voit avata kyselyeditori-valintaikkunan.
1. Määritä **Arvojoukko**-välilehdessä seuraavat arvot:

    - **Taulu:** *Laatutilaukset*
    - **Kenttä:** *Tila*
    - **Kriteerit:** *Hylätty*

1. Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.
1. Lisää **Rivit**-pikavälilehdellä rivi ja määritä seuraavat arvot:

    - **Määrästä:** *1*
    - **Määrälle:** *1000000*

1. Lisää rivi **Sijaintidirektiivin toimenpiteet** -pikavälilehdessä ja määritä seuraava arvo:

    - **Nimi:** *Hylätty*

1. Valitse **Sijaintidirektiivin toiminto** -pikavälilehdessä **Muokkaa kyselyä**, jotta voit avata kyselyeditori-valintaikkunan.
1. Määritä **Arvojoukko**-välilehdessä seuraavat arvot:

    - **Taulu:** *Sijainnit*
    - **Kenttä:** *Alueen tunnus*
    - **Kriteerit:** *Palaa*

1. Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.
1. Valitse toimintoruudussa **Tallenna** tallentaaksesi uuden sijaintidirektiivin.

#### <a name="mobile-device-menu-items-for-quality-out"></a>Mobiililaitteen valikkovaihtoehdot lähtevän laadun mukaan

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse **QMS-hyllytys**-mobiililaitevalikkovaihtoehto.
1. Lisää **Työluokat**-pikavälilehden työluokan tunnus kohtaan *QualityPut*.

Varastotyöntekijät voivat nyt poimia laatutilaustyötä **QMS-hyllytys**-valikkovaihtoehdon avulla. Tuotteet, joiden laadunvalvonta on epäonnistunut, voidaan ottaa käyttöön palautettaessa, ja tuotteet, jotka on ohitettu, voidaan sijoittaa Bulk-001-sijaintiin.

#### <a name="summary-your-setup-to-move-goods-from-quality-control"></a>Yhteenveto: määrityksesi siirtää tavarat laadunvalvonnasta

Olet määrittänyt varaston 51 työ- ja sijaintitiedot sen varmistamiseksi, että tietty työ luodaan automaattisesti, kun laatutilaukset ovat valmiita. Tämä asetus varmistaa, että jokainen laadunvalvonnassa oleva rekisterikilpi siirretään joko bulkkisijaintiin tai palautussijaintiin.

### <a name="process-quality-management-work"></a>Prosessin laadunhallintatyö

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Laatutilaukset**.
1. Valitse ensimmäinen laatutilaus rekisteröitäville määrille.
1. Valitse **Tarkista**. Tapaamisen tilaksi päivitetään *Hylätty*.
1. Siirry kohtaan **Varastonhallinta \> Kaikki työt**.
1. Avaa juuri luomasi työ ja huomaa, että **Työtilaustyypin** arvo on *Laatutilaus*. Työhön sisältyy rivi, jolla varastopaikka *palautetaan* ja tila on *hylätty*. (Jos laatutilauksen tila on *hyväksytty*, hyllytyssijainti olisi sen sijaan *Bulkki*.)
1. Siirry takaisin kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Laatutilaukset**.
1. Valitse toinen laatutilaus rekisteröitäville nimikkeille.
1. Valitse alemman ruudukon yläpuolella olevat **tulokset**. Päivitä **tulosmäärän** arvoksi *5* ja tarkista, että **Testin tulos** -arvo muuttuu valintamerkiksi.
1. Valitse **Vahvista** ja sulje sivu.
1. Palaa **Laatutilaukset**-sivulle, valitse **Vahvista** ja tee oikeellisuustarkistus. Tilaksi päivitetään *Hyväksytty*.

    > [!NOTE]
    > Vahvistustapahtuma käynnistää laatutilaustyön luomisen, jotta määrä voidaan siirtää laadunvalvontasijainnista uuteen sijaintiin.

1. Siirry kohtaan **Varastonhallinta \> Kaikki työt**.
1. Valitse juuri luotu työ ja huomaa, että on luotu toinen laatutilauksen työotsikko, jossa hyllytyksen sijainti on *Bulk-001*.
1. Siirry mobiililaitteeseen tai emulaattorille, joka käyttää varastonhallinnnan mobiilisovellusta, ja kirjaudu varastoon 51 käyttämällä lukua *51* käyttäjätunnuksena ja lukua *1* salasanana.
1. Siirry kohtaan **Laatu \> Hyllytys QMS:stä** ja käsittele molempiin töihin liittyvät molemmat rekisterikilvet siten, että kaikki työt suljetaan.

> [!NOTE]
> Harkitse laatumerkinnän lisäämistä mobiililaitteen valikkokohteeseen, jossa tehtäväkoodi on *Näytä avoin työluettelo*. Katso esimerkiksi matkaviestimen valikkovaihtoehto, jonka nimi on demotietojen **Työluettelo**. Lisää ensin *Laatutilauksen* työluokka käyttäjän ohjattuun valikkokohteeseen, koska työluokka on pakollinen, jotta työ voidaan näyttää työluettelossa. Lisää sitten *Laatutilauksen* työluokka **Työluettelo**-valikkonimikkeeseen. Käyttäjät, joilla on työluettelon käyttöoikeus, voivat tällöin poimia ja käsitellä työn, joka luodaan automaattisesti laatutilauksen vahvistuksen avulla.

## <a name="additional-resources"></a>Lisäresurssit

- [Laadun ja määrityksistä poikkeamisen hallinnan yleiskatsaus](quality-management-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]