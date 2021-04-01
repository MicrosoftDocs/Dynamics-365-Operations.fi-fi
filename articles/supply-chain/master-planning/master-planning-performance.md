---
title: Pääsuunnittelun suorituskyvyn parantaminen
description: Tässä ohjeaiheessa käsitellään erilaisia asetuksia, joilla voidaan parantaa pääsuunnittelun tai vianmääritysongelmien suorituskykyä.
author: t-benebo
manager: tfehr
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 54f39793b6e8b24a13a4b80b59ba35f10e8f3da5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237470"
---
# <a name="improve-master-planning-performance"></a>Pääsuunnittelun suorituskyvyn parantaminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään erilaisia asetuksia, joilla voidaan parantaa pääsuunnittelun tai vianmääritysongelmien suorituskykyä. Siinä on tietoja parametreista ja asetuksista sekä suositelluista määrityksistä ja toiminnoista. Se sisältää myös yhteenvedon kaikista tärkeistä parametreista, jotka kannattaa ottaa huomioon pitkäkestoisissa pääsuunnittelutöissä.

Tämä ohjeaihe on tarkoitettu järjestelmänvalvojille tai IT-käyttäjille, jotka voivat tehdä vianmääritystä. Se on tarkoitettu myös tuotannon tai toimituksen suunnittelijoille, koska siinä on tietoja liiketoiminnan suunnittelutarpeisiin liittyvistä parametreista. 

## <a name="parameters-related-to-master-planning-performance"></a>Pääsuunnittelun suorituskykyyn liittyvät parametrit

Eri parametrit vaikuttavat pääsuunnittelun ajoaikaan, ja ne onkin otettava huomioon.

### <a name="number-of-threads"></a>Säikeiden määrä

Voit säätää **Säikeiden määrä** -parametrilla pääsuunnitteluprosessia siten, että sen suorituskyky paranee tietyn tietojoukon osalta. Tämä parametri määrittää pääsuunnittelun suorittamiseen käytettävien säikeiden kokonaismäärän. Se aiheuttaa pääsuunnitteluajon rinnakkaisuuden, mikä puolestaan auttaa lyhentämään ajoaikaa. 

Voit määrittää **Säikeiden määrä** -parametrin **Pääsuunnitteluajo**-valintaikkunassa. Voit avata tämän valintaikkunan valitsemalla **Pääsuunnittelu \> Pääsuunnittelu \> Suorita \> Pääsuunnittelu**. Vaihtoehtoisesti voit valita **Suorita** **Pääsuunnittelu**-työtilassa. Parhaan arvon määrittäminen tälle parametrille onnistuu kokeilemalla. Voit kuitenkin laskea ensimmäisen arvon seuraavilla kaavoilla:

- **Valmistusteollisuus:** (säikeiden määrä) = (suunniteltujen tilausten määrä ÷ 1 000)
- **Muut:** (Säikeiden määrä) = (Nimikkeiden määrä ÷ 1 000)

Pääsuunnittelussa käytettävien aputoimintojen määrä on oltava pienempi tai yhtä suuri kuin eräpalvelimessa sallittujen säikeiden enimmäismäärä. Jos aputoimintojen määrä ylittää eräpalvelimen säikeiden määrä, lisäsäikeet eivät tee mitään.

> [!NOTE]
> **Säikeiden määrä** -parametrin asetus **0** (nolla) pidentää pääsuunnittelun ajoaikaa. Tämän vuoksi arvo kannattaa määrittää suuremmaksi kuin 0.

### <a name="number-of-tasks-in-helper-task-bundle"></a>Lisätyöaseman tehtävänipun tehtävien määrä

**Tehtävänipun tehtävien määrä** -asetusta (nipun kokoa) muuttamalla voit ehkä lyhentää ajoaikaa. Tämä asetus määrittää, kuinka monta nimikettä yksi aputoiminto suunnittelee yhdessä.

Voit määrittää **Tehtävänipun tehtävien määrä** -parametrin **Pääsuunnitelman parametrit** -sivun **Yleiset**-välilehden **Suorituskyky**-osassa (**Pääsuunnittelu \> Asetukset \> Pääsuunnittelun parametrit**). Tämän parametrin paras arvo määräytyy tietojen mukaan. Tämän vuoksi aluksi kannattaa käyttää arvoa **1** ja määrittää sitten kokeilemalla asetukselle paras arvo.

Yleensä tehtävien määrää kannattaa nostaa, kun nimikkeitä on erittäin paljon (satojatuhansia). Muussa tapauksessa tehtävien määrää kannattaa vähentää. Ota seuraavat suositukset huomioon seuraavien toimialojen osalta:

- Vähittäis- ja jakelualoilla, joissa yksittäisiä nimikkeitä on runsaasti, aputoimintoja käytetään runsaasti, koska nimikkeiden välillä ei ole riippuvuutta. 
- Valmistusteollisuudessa, jossa on monia tuoterakenteita ja jaettuja aliosia, käytetään vähemmän aputoimintoja, koska nimikkeiden väliset riippuvuudet voivat aiheuttaa odotusaikoja.

> [!TIP]
> Jos suorituskykyongelmia esiintyy, **Lisätyöaseman tehtävänipun tehtävien määrä** -asetus kannattaa vähentää arvoksi **1**. Voit sitten aloittaa asetuksen parhaan arvon etsimisen kokeilemalla. Yleensä suorituskykyongelmia esiintyy, kun yhden nimikkeen käsittely kestää kauemmin kuin muiden nimikkeiden. Siinä tapauksessa havaitaan, että pääsuunnitteluajon kahden muun tehtävän, joiden tila on **Kattavuus**, ajoaika on merkittävästi erilainen. Äärimmäisissä tapauksissa ero voi olla jopa 30 minuuttia. Voit päätellä tehtävien ajoajan tarkastelemalla kuinkin tehtävän kestoa.

### <a name="use-of-cache"></a>Välimuistin käyttö

Voit säätää **Välimuistin käyttö** -parametrilla pääsuunnitteluprosessia siten, että sen suorituskyky paranee tietyn tietojoukon osalta. Voit säätää sitä esimerkiksi seuraavien tulosten saamiseksi:

- Mitä enemmän välimuistiin tallennetaan, siltä enemmän tietoja kertyy muistiin. Oletuksena on, että tietoja käytetään myöhemmin uudelleen. Jos tiedot ovat muistissa, tietokantapyyntöjä syntyy ehkä enemmän. Jos välimuistitallennuksia tehdään kuitenkin enemmän, muistia tarvitaan lisää.
- Jos välimuistitallennuksia tehdään vähemmän, samat tiedot on ehkä noudattava entistä useammin tietokannasta. Lisäksi AOS-palvelin tallentaa vähän tietoja muistiin koko prosessin aikana.

On vaikea ennakoida, kumpi vaihtoehto on parempi, sillä tietojen lisäksi myös laitteistolla on merkitystä kussakin tapauksessa. Koska esimerkiksi välimuistitallennuksen vähentäminen kuormittaa tietokantapalvelinta enemmän, tätä vaihtoehtoa ei luultavasti kannata valita, jos tietokantapalvelin on jo ylikuormittunut.

Voit määrittää **Välimuistin käyttö** -parametrin **Pääsuunnitelman parametrit** -sivun **Yleiset**-välilehden **Suorituskyky**-osassa (**Pääsuunnittelu \> Asetukset \> Pääsuunnittelun parametrit**). Välimuistin tehokas käyttö määräytyy suuressa määrin asiakastietojen perusteella. Jos välimuistiin tallennettuja tietoja ei koskaan tarvita, muistia käytetään turhaan, jos tiedot tallennetaan ajoitusprosessin päättymiseen saakka. Jos tässä tapauksessa välimuistitallennusmääritystä vähennetään, suorituskyky voi parantua, sillä AOS-palvelin tarvitsee vähemmän muistia ja palvelinresursseja vapautuu muihin tehtäviin.

> [!TIP]
> Yleensä **Välimuistin käyttö** -parametriksi kannattaa määrittää **Maksimi**, koska parametri on tarkoitettu suorituskykyä parantava toiminto. Parametrin arvoksi kannattaa määrittää **Minimi**, jos ajo tehdään paikallisesti ja muistia on rajallisesti (noin 2 gigatavua \[Gt\]).

### <a name="number-of-orders-in-firming-bundle"></a>Vahvistusmyyntirakenteen tilausten määrä

**Vahvistusmyyntirakenteen tilausten määrä** -parametri määrittää, kuinka monta tilausta kukin säie tai erä käsittelee yhteensä kerrallaan. Se aiheuttaa automaattisen vahvistusprosessin rinnakkaisen suorittamisen.

Voit määrittää **Vahvistusmyyntirakenteen tilausten määrä** -parametrin **Pääsuunnitelman parametrit** -sivun **Yleiset**-välilehden **Suorituskyky**-osassa (**Pääsuunnittelu \> Asetukset \> Pääsuunnittelun parametrit**). Automaattinen vahvistusprosessi rinnakkainen suorittaminen perustuu yhdessä käsiteltäviin tilauksiin. Esimerkiksi, jos tämän parametrin arvoksi on määritetty **50**, jokainen säie tai erätehtävä poimii kerralla 50 tilausta ja käsittelee ne yhdessä. Paras arvo kannattaa etsiä kokeilemalla. Voit kuitenkin laskea ensimmäisen arvon seuraavalla kaavalla:

(Tilausten myyntirakennekohtainen määrä) = (kysyntänimikkeiden määrä ÷ säikeiden määrä)

> [!NOTE]
> Jos määrität **Vahvistusmyyntirakenteen tilausten määrä** -parametrin arvoksi **0** (nolla), rinnakkaista automaattista vahvistusprosessia ei tapahdu. Koko prosessi suoritetaan yhtenä erätehtävänä, ja niiden ajoaika on kumulatiivinen. Tämän vuoksi pääsuunnittelun ajoaika pitenee. Tämän vuoksi tämän parametrin arvo kannattaa määrittää suuremmaksi kuin **0** (nolla).

### <a name="time-fences"></a>Aikarajat

Aikarajat määrittävät, kuinka pitkälle tulevaisuuteen pääsuunnittelu laskee laskelmat ja muut tarpeet. Mitä pidempi aikaraja on, sitä kauemmin pääsuunnittelun suorittaminen kestää. Määritä tämän vuoksi aikarajat liiketoimintatarpeiden mukaan. Lisätietoja aikarajasta on kohdassa [Pääsuunnittelun määrittäminen](master-planning-setup.md).

### <a name="actions"></a>Toimenpiteet

Aikarajat sisältävät myös **Toimenpidesanoma**-parametrin. Toimenpidesanomien laskeminen pidentää pääsuunnittelun ajoaikaa. Jos toimenpidesanomia ei analysoida ja käytetä säännöllisesti (kuten päivittäin tai viikoittain), harkitse laskennan poistamista käytöstä pääsuunnitteluajon aikana. Voit poistaa laskennan käytöstä **Pääsuunnitelmat**-sivulla määrittämällä suoritettavan (**Pääsuunnitelman \> Määritys \> Suunnitelmat \> Pääsuunnitelmat**) **Toimenpidesanoman**-aikarajaksi **0** (nolla). Varmista myös, että **Toimenpidesanoma**-asetus on poistettu käytöstä kaikissa kattavuusryhmissä.

### <a name="futures"></a>Viivästyssanomat

Viivästyssanomien laskeminen pidentää pääsuunnittelun ajoaikaa. Jos et suunnittele tuoterakenteita tai jos viivästyksiä ei tarvitse välittää toimituksesta kysyntään suunnitelman aikana, viivästyssanomien laskelmien poistamista käytöstä pääsuunnittelun aikana kannattaa harkita. Voit poistaa laskelmat käytöstä määrittämällä suoritettavan pääsuunnitelman **Viivästyssanomat**-aikarajaksi **0** (nolla). Varmista myös, että **Viivästyssanoma**-asetus on poistettu käytöstä kaikissa kattavuusryhmissä.

## <a name="one-heavy-routine-at-a-time"></a>Yksi kuormittava rutiini kerrallaan

Kun ajoitat pääsuunnittelua, älä ajoita samaan aikaan muita erätöitä. Vältä etenkin muiden kuormittavien rutiinien samanaikaista ajoittamista. Tällainen on esimerkiksi varaston sulkeminen.

## <a name="review-the-session-log"></a>Istuntolokin tarkasteleminen

Järjestelmä voi kerätä lisätietoja pääsuunnittelun aikana suoritettavista tehtävistä, Jos haluat järjestelmän keräävän näitä tietoja, ota **Seuraa käsittelyaikaa** -asetus käyttöön **Pääsuunnitteluajo**-valintaikkunassa. Kerätyt tiedot voivat auttaa etsimään ajon pullonkauloja. Kun esimerkiksi **Lisätyöaseman tehtävänipun tehtävien määrä** -parametrin asetukseksi on määritetty **1**, voit tunnistaa nimikkeen, jonka ajoaika on pisin. Voit myös verrata sellaisten erilaisten säikeiden ajoaikoja, joilla on **Kattavuus**-tila, ja verrata kunkin tehtävän kestoa.

Voit tarkastella järjestelmän pääsuunnitteluajoja käyttämällä jompaakumpaa seuraavaa ohjetta.

- Valitse **Pääsuunnittelu**-työtilassa työtila avattavassa kentässä ja valitse sitten **Pääsuunnittelu**-ruudussa **Historia**. Valitse ensin työ, sitten **Kyselyt** pikavälilehdessä ja sitten **Käsittelytehtävän kesto**.
- Valitse **Pääsuunnitelmat**-sivulla vasemmassa ruudussa suunnitelma ja valitse sitten **Historia** pikavälilehdessä. Valitse ensin työ, sitten **Kyselyt** pikavälilehdessä ja sitten **Käsittelytehtävän kesto**.

Ota seuraavat seikat huomioon, kun tarkastelet istuntolokia:

- **Päivityksen** ei pitäisi kestää kauan (yleensä se kestää noin 30 minuuttia). Se on kuitenkin yksisäikeinen.
- **Suunnitelman kopioinnin** ei pitäisi kestään kauan (sen pitäisi kestää noin minuutin).
- **Automaattinen vahvistaminen** kestää yleensä noin 30 minuuttia. Se voi kuitenkin kestää useita tunteja tilausten määrän ja nimikkeiden monimutkaisuuden mukaan.
- **Automaattisen vahvistuksen** pitäisi kestää lyhyemmän ajan kuin **Kattavuus**.
- **Kattavuuden** keston pitäisi olla pidempi kuin muiden asetusten keston.
- **Toiminto-** ja **viivästyssanoma** voi kestään pitkään tietojen ja tuoterakenteiden määrän mukaan.

## <a name="filtering-of-items"></a>Nimikkeiden suodattaminen

**Pääsuunnitteluajo**-valintaikkunassa käytetyt suodattimet vaikuttavat pääsuunnitteluajon kestoon. Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Suorita \> Pääsuunnittelu**. Vaihtoehtoisesti voit valita **Suorita** **Pääsuunnittelu**-työtilassa. Jos haluat jättää nimikkeet ajon ulkopuolelle, suodatus kannattaa tehdä nimikkeen elinkaaren tilan (eikä nimikenumeroiden) perusteella. Kun suodatusperusteena käytetään elinkaaren tilaan, päivitysprosessi kestää vähemmän aikaa kuin nimikenumeroiden mukaan suodatettaessa.

## <a name="automatically-filter-by-items-with-direct-demand"></a>Suodata automaattisesti suoran kysynnän nimikkeiden mukaan

Voit parantaa pääsuunnittelun ajoaikaa valitsemalla vain ne nimikkeet, joilla on suora kysyntä. Tätä suodatinta voi käyttää vain täydellisessä pääsuunnittelun ajossa, jossa ei ole muita suodattimia **Sisällytettävät tietueet** -kenttään. Suodattimien kanssa suoritettava pääsuunnittelu ohittaa **Suodata automaattisesti kohteet, joilla on suora kysyntä** -asetus.

**Suodata automaattisesti kohteilla, joilla on suora kysyntä** -kenttä, löytyy **Pääsuunnittelun parametrit** -sivulta, ja sitä voidaan käyttää sekä esikäsittely- että jälkikäsittelyasetuksilla.

### <a name="pre-processing"></a>Esikäsittely
**Esikäsittely: Suodata automaattisesti kohteiden mukaan suoraan kysynnän** parametrilla varmistaa, että pääsuunnittelun esikäsittelyvaihe sisältää vain kohteet, jotka täyttävät vähintään yhden seuraavista ehdoista:
  - Nimikkeellä on odotettu vastaanotto tai asia, kuten ostotilaus, myyntitilaus, tarjous, siirtotilaus tai tuotantotilaus. 
  - Nimikkeellä on nimikekattavuus ja varmuusvarasto (pienin käytettävissä oleva varasto).
  - Ennusteen kysyntä on tämän päivän jälkeen olemassa nimikkeelle.
  - Ennusteen tarjonta on tämän päivän jälkeen olemassa nimikkeelle.
  - Nimike sisältää vielä luotavan puhelinkeskusmoduulin jatkuvuusrivit.

> [!NOTE]
> Nimikkeellä, jolla on fyysisesti käytettävissä oleva varasto, ei näy tarvetapahtumaa, koska nimikkeelle ei ole kysyntää.

### <a name="post-processing"></a>Jälkikäsittely
**Jälkikäsittely: Suodata automaattisesti kohteilla, joilla on suora kysyntä** -asetus on merkityksellinen vain, jos määrität **Tuoterakenne version vaatimuksen** kattavuusryhmiin. Muussa tapauksessa parametria ei tarvitse ottaa käyttöön. 

Ennen kattavuusvaihetta otetaan käyttöön esikattavuusvaihe, jonka aikana nimikkeet, joilla on kattavuus asetuksen **tuoterakenneversion vaatimus**, käsitellään uudelleen. Tämä tehdään sen varmistamiseksi, että vaaditun tuoterakenneversion nimikkeet suunnitellaan. Nimikkeille, joilla katsotaan olevan kysyntää esikäsittelyn aikana ei enää ole kysyntää ja siksi olisi jätettävä pois suunnitteluajosta.

## <a name="performance-checklist-summary"></a>Suorituskyvyn tarkistusluettelon yhteenveto

- **Säikeiden määrä** – määritä arvo suuremmaksi kuin **0** (nolla).
- **Lisätyöaseman tehtävänipun tehtävien määrä** – Määritä arvo suuremmaksi kuin **0** (nolla). (Käytä aiemmin tässä ohjeaiheessa annettuja kaavoja.)
- **Välimuistin käyttö** – määritä arvoksi **Maksimi**, ellei järjestelmän muisti on vähissä.
- **Vahvistusmyyntirakenteen tilausten määrä** – Määritä arvo suuremmaksi kuin **0** (nolla). (Käytä aiemmin tässä ohjeaiheessa annettu kaava.)
- **Aikarajat** – säädä liiketoimintatarpeiden mukaan.
- **Toiminnot ja viivästykset** – poista toiminnot ja viivästykset, jos et käytä niitä.
- **Yksi kuormittava rutiini kerrallaan** – älä suorita pääsuunnittelu yhdessä muiden kuormittavien rutiinien kanssa.
- **Tarkista istuntoloki.**
- **Nimikkeiden suodatus** – Jätä nimikkeitä pääsuunnitteluajon ulkopuolelle elinkaaren tilan avulla. (Älä käytä nimikenumeroita.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]