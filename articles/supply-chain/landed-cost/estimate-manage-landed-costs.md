---
title: Aiheutuneiden kustannusten arviointi ja hallinta
description: Järjestelmä käyttää automaattisten kustannusten asetuksiasi aiheutuneen kustannuksen arvion määrittämiseen. Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää erilaisia skenaarioita tarjotaksesi tarkemman arvion.
author: sherry-zheng
manager: tfehr
ms.date: 01/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMCostTemplateTable, ITM CostEstimateDialog, ITMCostEstimateTable, SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-26
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: cbd652f2b29f7a78ad9e4e1d3dda4a3ef8a9f3f3
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501267"
---
# <a name="estimate-and-manage-landed-costs"></a>Aiheutuneiden kustannusten arviointi ja hallinta

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Järjestelmä käyttää [automaattisten kustannusten asetuksiasi](auto-cost-setup.md) aiheutuneen kustannuksen arvion määrittämiseen. Lisäksi voit määrittää erilaisia skenaarioita tarjotaksesi tarkemman arvion. Nämä skenaariot tallennetaan. Voit siis tarkastella niitä myöhemmin ja verrata niitä raportissa oleviin todellisiin arvoihin. Voit myös päivittää nimikkeen hinnan.

## <a name="set-up-cost-estimates"></a>Kustannusarvioiden määrittäminen

### <a name="set-up-cost-templates"></a>Määritä kustannusmallit

Kustannusmallit määrittävät oletusasetuksia, joita arvion vastaanottavat käyttäjät eivät välttämättä tiedä. Mallit voivat tehdä arviointiprosessista yksinkertaisemman vähentämällä valintoja, joita käyttäjien täytyy tehdä saadakseen tarkan arvion. Jos käytät standardikustannusmallia, voit käyttää kustannusmalleja, kun määrität tavaroiden kustannusta.

Voit määrittää kustannusmalleja valitsemalla **Aiheutunut kustannus \> Kustannuslaskennan asetukset \> Kustannusmallit**. **Kustannusmallit**-sivun vasemmassa laidassa oleva luetteloruutu näyttää kaikki tämänhetkiset kustannusmallit. Voit luoda, poistaa ja muokata malleja käyttämällä toimintoruudun painikkeita.

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin mallille.

| Kenttä | kuvaus |
|---|---|
| Kustannusmalli | Syötä kustannusmallille yksilöivä nimi. Nimi kuvaa yleensä mallin kerrointa tai kustannuskerrointa. |
| kuvaus | Syötä kustannusmallille kuvaus. |
| Kuljetusyritys | Valitse kuljetusyritys, jota käytetään mallin kanssa. |
| Toimitustapa | Valitse toimitustapa, kuten meri- tai lentokuljetus, jota käytetään mallin kanssa. Tämä kenttä auttaa määrittämään tavaroihin liittyvät automaattiset kustannukset kustannusarviossa. |
| Lähetyskontin tyyppi | Valitse lähetyskontin tyyppi, jota käytetään mallin kanssa. Tämä kenttä auttaa määrittämään tavaroihin liittyvät automaattiset kustannukset kustannusarviossa. |
| Tulliasiamies | Tulliasiamies (toimittaja), jota käytetään mallin kanssa. Tämä kenttä auttaa määrittämään kustannusarvioon liitetyt automaattiset kustannukset. |
| Kerroin | Syötä kerroin (prosentteina), jota käytetään automaattisesti kustannusarviossa mallia käytettäessä. Jos haluat lisätä laskettuun kustannusarvioon esimerkiksi 10 prosenttia, syötä arvoksi *1,10*. |

### <a name="create-a-cost-estimate"></a>Kustannusarvion luominen

Käytä **Kustannusarvio**-valintaikkunaa luodaksesi uuden kustannusarvion, joka perustuu valittuun kustannusmalliin, valittuun nimikejoukkoon ja muihin matkan tietoihin. Näitä asetuksia käytetään määrittämään tavaroiden arvioidut aiheutuneet kustannukset. Näitä kustannusarvioita käytetään ensisijaisesti standardikustannusnimikkeiden kanssa. Kun arvioidut aiheutuneet kustannukset lisätään varastossa olevien tavaroiden standardikustannukseen, tapahtumien varianssin tulisi olla pienempi, kun tavarat lisätään merikuljetukseen, koska standardikustannus vastaa kyseisten aiheutuneiden kustannusten arvioita.

Avaa **Kustannusarvio**-valintaikkuna valitsemalla **Aiheutunut kustannus \>Kausittaiset tehtävät \> Kustannusarvio**. Määritä sitten seuraavissa osioissa kuvatut kentät. Valitse lopuksi **OK** luodaksesi arvion. **Kustannusarvio**-sivu (**Aiheutunut kustannus \> Kyselyt \> Kustannusarviot**) avautuu ja näyttää sinulle arvion tässä ohjeaiheessa myöhemmin kuvatulla tavalla.

### <a name="settings-on-the-parameters-tab"></a>Parametrit-välilehden asetukset

Seuraavassa taulukossa kuvataan **Kustannusarvio**-valintaikkunan **Parametrit**-välilehdessä käytettävissä olevat kentät.


| Kenttä | kuvaus |
|---|---|
| Kustannusmalli | Valitse kustannusmalli. Valittuun malliin liitettyjä asetuksia käytetään automaattisten kustannusten määrittämiseen. |
| Arviopäivämäärä | Tässä kentässä on oletusarvoisesti tämänhetkinen päivämäärä, mutta voit muuttaa arvoa. Määritettyä päivämäärää käytetään asiaankuuluvien myyntihintojen, ostohintojen, automaattisten kustannusten ja vaihtokurssin valitsemiseen, jos lähetyshintaa käytetään. |
| Mittaus | Kustannukset voivat olla riippuvaisia mitasta. Esimerkiksi lentorahdille voidaan käyttää tilavuuteen perustuvaa hinnoittelua. Jos kustannus on riippuvainen mitasta, syötä mitan arvo. Muussa tapauksessa suosittelemme, että määrität tämän kentän arvoksi *1*, ellet ole varma, ettei arvoa muutetta mitan perusteella. Syötä desimaaliarvo. Yksikkö on sama kuin asiaankuuluvassa automaattisen kustannuksen tietueessa määritetty yksikkö. |
| Matkamalli | Valitse [matkamalli](multi-leg-journey-setup.md). Tämä kenttää määrittää oikeat automaattiset kustannukset, joita tulisi käyttää. |
| Lähtösatama | Satama, jossa nimikkeet lähetetään. Tämä kenttä perustuu valittuun matkamalliin. |
| Satamaan | Satama, johon nimikkeet lähetetään. Tämä kenttä perustuu valittuun matkamalliin. |
| Valuutta | Valitse valuutta, jolla nimikkeet ostetaan. |
| Kontit | Jos käytät tavallisesti useita kontteja, määritä konttien määrä. Järjestelmä käyttää useiden konttien kustannuksia, kun se arvioi kustannuksia. |
| Laskut | Jos käytät tavallisesti useita pakkauksia, syötä niiden määrä. (Määrä on tavallisesti *1*). |
| Toimipaikka | Määritä toimipaikka, johon tavarat toimitetaan. |

### <a name="settings-on-the-items-tab"></a>Nimikkeet-välilehden asetukset

**Nimikkeet**-välilehdessä voit lisätä arvioon niin monta nimikettä kuin tarvitset. Käytä työkaluriviä lisätäksesi nimikkeitä ruudukkoon tai poistaaksesi nimikkeitä. Valitse työkalurivistä **Varasto \> Näytä dimensiot** avataksesi valintaikkunan, josta voit lisätä dimensiosarakkeita ruudukkoon tai poistaa sarakkeita.

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin nimikkeelle.

| Kenttä | kuvaus |
|---|---|
| Nimiketunnus | Valitse nimike, jolle hinta määritetään. (Jos nimikettä ei vielä ole järjestelmässä, luo tyhjä nimike, liitä se halutessasi merikuljetuksen nimikkeiden kustannusryhmään ja jätä sitten hinta tyhjäksi, luo hinta tai muokkaa hintaa). |
| Toimittajanro | Valitse tämän nimikkeen arviossa käytettävä toimittaja. Jos nimikkeelle on määritetty oletustoimittaja, tämä kenttä määritetään automaattisesti. |
| Määrä | Valitse määrä, jonka aiot ostaa. |
| Kustannushinta | Järjestelmä käyttää sen hinnoittelusääntöjä löytääkseen alustavan hinnan, mutta voit korvata hinnan tarvittaessa. |
| Myyntihinta | Syötä tavaroiden odotettu myyntihinta. |
| Mittaus | Syötä desimaaliarvo tavaroiden mitalle. Yksikkö on sama, joka on määritetty asiaankuuluvalle vapautetulle tuotteelle. |
| Päivitä nimikkeen paino/tilavuus | Valitse tämä valintaruutu päivittääksesi vapautetun tuotteen painon tai tilavuuden mitan siten, että se vastaa tälle riville syötettyä **Mittaus**-arvoa. |
| (Muut dimensiot) | Riippuen valitsemastasi dimensiosta, saatat nähdä lisää sarakkeita, jotka sisältävät tietoja kustakin nimikkeestä. |

Voit tarkastella tai muokata nimikkeen tilavuus- ja/tai painotietoja valitsemalla nimikkeen ruudukosta ja käyttämällä sitten sivun alalaidassa olevia kenttiä.

## <a name="manage-estimated-costs"></a>Arvioitujen kustannusten hallinta

Voit tarkastella ja muokata luomiasi kustannusarvioita valitsemalla **Aiheutunut kustannus \> Kyselyt \> Kustannusarviot**. **Kustannusarviot**-sivun vasemmassa laidassa oleva luetteloruutu näyttää kaikki tämänhetkiset kustannusarviot. Voit käsitellä valittua arviointia toimintoruudun painikkeiden avulla. Huomaa, ettet voi luoda uutta kustannusarviota **Kustannusarviot**-sivulta. Käytä sen sijaan **Kustannusarvio**-valintaikkunaa (**Aiheutunut kustannus \> Kausittaiset tehtävät \> Kustannusarvio**) aiemmin tässä ohjeaiheessa kuvatulla tavalla.

**Kustannusarviot**-sivulla näytetään, miten jokainen arvioitu kustannus on laskettu. Se näyttää myös kunkin nimikkeen arvioidun aiheutuneen kustannuksen. Voit muokata kustannusarviota muuttamalla eri tavaroihin liitettyä kustannushintaa ja/tai valuuttaa. Voit myös muokata asiaankuuluvia merikuljetuksen kustannuksia merikuljetuksen ja kontin tasolla. Kun muokkaat kustannuksia tältä sivulta, sinua pyydetään laskemaan arvioidut kustannukset uudelleen kustannusarvioon sisältyville nimikkeille. Kun olet valmis, voit käyttää arvioita päivittääksesi kustannusmalliin sisältyvien nimikkeiden kustannushinnan.

### <a name="information-on-the-header"></a>Ylätunnisteessa olevat tiedot

**Kustannusarviot**-sivun ylälaidassa näytetään asetukset, joita käytettiin valitun kustannusarvion luomiseen, niin kuin edellisessä osassa on kuvattu. 

### <a name="settings-and-buttons-on-the-lines-fasttab"></a>Rivit-pikavälilehden asetukset ja painikkeet

**Rivit**-pikavälilehdessä näytetään kaikkien tämänhetkiseen arvioon sisältyvien nimikkeiden luettelo. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin riville.

| Kenttä | kuvaus |
|---|---|
| Toimittajanro | Nimikkeeseen liitetty toimittajatili. |
| Nimiketunnus | Nimikkeen numero. |
| Määrä | Kustannuksen määrittämiseen käytettyjen nimikkeiden määrä. |
| Kustannushinta | Kauppasopimuksen mukainen kustannushinta. Tämä arvo näytetään paikallisena valuuttana. |
| Mittaus | Yksittäinen mitta. Yksikkö on sama, joka on määritetty asiaankuuluvalle vapautetulle tuotteelle. |
| Arvioitu aiheutuva kustannus | Kokonaismäärän arvioitu aiheutunut kustannus. |
| Yksikköä kohden | Arvioitu aiheutunut kustannus jaettuna määrällä. |
| (Muut dimensiot) | Riippuen valitsemastasi dimensiosta, saatat nähdä lisää sarakkeita, jotka sisältävät tietoja kustakin nimikkeestä. |

Seuraavassa taulukossa kuvataan painikkeet, jotka ovat käytettävissä **Rivit**-pikavälilehden työkalurivissä.

| Painike | kuvaus |
|---|---|
| Lisää | Lisää nimikkeitä kustannusarvioon. Kun olet lisännyt nimikkeitä, sinun täytyy valita toimintoruudusta **Laske uudelleen**. |
| Poista | Poista nimikkeitä kustannusarviosta. Kun olet poistanut nimikkeitä, sinun täytyy valita toimintoruudusta **Laske uudelleen**. |
| Matkan kustannukset | Avaa sivu, josta voit tarkastella ja muokata nimikkeen erityyppisiä merikuljetuksen kustannuksia. |
| Varasto \> Näytä dimensiot | Avaa valintaikkuna, josta voit lisätä ruudukkoon dimensiosarakkeita tai poistaa sarakkeita. |

### <a name="settings-on-the-general-fasttab"></a>Yleinen-pikavälilehden asetukset

**Yleinen**-pikavälilehdessä näytetään tietoja nimikkeestä, joka on valittuna tällä hetkellä **Rivit**-pikavälilehdessä. Suuri osa näistä tiedoista saadaan suoraan **Rivit**-pikavälilehdestä, eikä niitä voida muokata kummastakaan sijainnista. Näet kuitenkin myös lisätietoja. Lisäkenttien arvot perustuvat asiaankuuluvan vapautetun tuotteen asetuksiin.

### <a name="settings-on-the-dimension-fasttab"></a>Dimensio-pikavälilehden asetukset

**Dimensio**-välilehti näyttää **Rivit**-välilehdessä valittuna olevan nimikkeen kaikkien käytettävissä olevien varastodimensioiden arvot riippumatta siitä, mitkä dimensiot olet valinnut näkymään tässä välilehdessä. Kaikki näytetyt arvot saadaan asiaankuuluvasta kustannusarviomallista. Ne ovat valinnaisia kustannusarviomallissa.

### <a name="buttons-on-the-action-pane"></a>Toimintoruudun painikkeet

Voit työstää valittua kustannusarviota käyttämällä **Kustannusarviot**-sivun toimintoruudun painikkeita. Seuraava taulukko kuvaa käytettävissä olevat painikkeet.

| Toimenpide | kuvaus |
|---|---|
| Kustannuskysely | Tarkasta merikuljetuksen kaikki kustannukset. Voit tarkastella kustannuksia yksittäisen nimikkeen tasolla tarvittaessa. |
| Päivitä vakiokustannus | <p>Päivitä standardikustannus käyttämällä kustannuslaskennan oletusversiota, joka on määritetty **Aiheutuneen kustannuksen parametrit** -sivulla. Voit korvata tämän version.</p><p>**Huomaa:** Jos nimikkeellä on useita nimikedimensioita (esimerkiksi eri kokoja, värejä ja konfiguraatioita), mutta näitä dimensioita ei ole valittu arviota varten, järjestelmä luo jokaiselle yhdistelmälle odottavan hinnan.</p><p>**Tärkeää:** Hintaerittely luodaan ja sitä käytetään määrittämään standardikustannusvarianssi per arvioitu kustannus.</p> |
| Matkan kustannukset | Tarkastele ja muokkaa lähetyksen kaikkien tavaroiden merikuljetuskustannuksia. |
| Laske uudelleen | Päivitä arvioidut aiheutuneet kustannukset, kun merikuljetuskustannuksia päivitetään, lisätään tai poistetaan. |
| Lukitse | Lukitse kustannusarviotietue, jotta siihen ei voi tehdä enää muutoksia. |

## <a name="item-cost-price-update"></a>Nimikkeen kustannushinnan päivitys

Kausittainen **Nimikkeen kustannushinnan päivitys** -tehtävä päivittää kaikki kustannusarviot, jotka vastaavat tehtävän suorittamisen aikana määrittämiäsi suodattimia. Se toimii samalla tavalla kuin **Päivitä vakiokustannus** -vaihtoehdon valitseminen toimintoruudusta yksittäiselle arviolle. Tässä tapauksessa päivitys koskee kuitenkin kaikkia vastaavia arvioita.

Suorita kausittainen tehtävä noudattamalla seuraavia ohjeita.

1. Valitse **Aiheutunut kustannus \> Kausittaiset tehtävät \> Nimikkeen kustannushinnan päivitys**.
1. Määritä **Päivitä kustannushinta arviosta** -valintaikkunassa seuraavat kentät päivityksen laajuuden rajoittamiseksi:

    - **Versio** – Päivitä vain arviot, jotka käyttävät määritettyä kustannuslaskennan versiota.
    - **Toimipaikka** – Päivitä vain arviot, jotka käyttävät määritettyä toimipaikkaa.
    - **Kustannusmalli** – Päivitä vain arviot, jotka käyttävät määritettyä mallia.
    - **Kohdesatama** – Päivitä vain arviot, jotka käyttävät määritettyä kohdesatamaa.
    - **Arviopäivämäärä** – Päivitä vain arviot, joilla on määritetty päivämäärä.

1. Määritä **Sisällytettävät tietueet**- ja **Suorita taustalla** -pikavälilehtien vaihtoehdot tavallisen tapaan kausittaisille tehtäville.
1. Valitse **OK** suorittaaksesi tehtävän.

> [!NOTE]
> Tämä kausittainen tehtävä suoritetaan onnistuneesti vain, jos seuraavat tiedot ovat käytettävissä:
>
> - Kaikilla asiaankuuluvilla tuotteilla täytyy olla **Bruttosyvyys**-, **Bruttoleveys**- ja **Bruttokorkeus**-arvot määritettynä.
> - Kaikilla asiaankuuluvilla toimittajilla täytyy olla **Lähtösatama**-arvo määritettynä.
