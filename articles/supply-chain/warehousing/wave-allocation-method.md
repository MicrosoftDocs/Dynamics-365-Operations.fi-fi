---
title: Aallon kohdistus
description: Tässä aiheessa kuvataan, miten voit määrittää aallon kohdistusvaiheen. Tässä aiheessa kuvataan myös, miten sen rinnakkaiskäsittely otetaan käyttöön.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 9c534f5e10f5797543d56ff4a5a7ada937edcb017228ebe395ae8a45efa10886
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781318"
---
# <a name="wave-allocation"></a>Aallon kohdistus

[!include [banner](../includes/banner.md)]

Aallon käsittelyssä voi kulua kauan, ja suurin osa käsittelyajasta kuluu kohdistusvaiheessa ja työn luontivaiheessa.

Kaikki nämä vaiheet on nyt mahdollista suorittaa rinnakkain, mikä voi parantaa aallon käsittelyn suorituskykyä ja mahdollistaa suuremman määrän aaltojen samassa varastossa. Tässä aiheessa kerrotaan, miten voit määrittää aallon kohdistusmenetelmän, joka suoritetaan rinnakkain. Lisätietoja siitä, miten työn luonti määritetään samanaikaista ajoa varten, on kohdassa [Aikatauluta työn luonti aallon aikana](configure-wave-schedule-work-creation.md).

Aiemmin varastossa voi kohdistaa vain yhden aallon kerrallaan. Tämä rajoitus on poistettu ja korvattu uudella rajoituksella, joka lukitsee vain ne nimikkeet ja dimensiot, jotka ovat varaushierarkiassa yläpuolella. Sijainnin yläpuolella olevat dimensiot sisältävät aina tuotedimensioita. Jos nimike on määritetty esimerkiksi *Väri*-määrityksen avulla, *punaisen*, *sinisen* ja *keltaisen* variantin voi kunkin käsitellä rinnakkain.

Tämä tarkoittaa, että jos sama nimike, jolla on samat dimensiot sijainnin yläpuolella, kohdistetaan yhteen aaltoon, muiden aaltojen on odotettava lukitusta samalle nimikkeelle ja dimensioille. Jos lukitusta ei voi hankkia ajoissa, tulee virhe ja aallon käsittely epäonnistuu.

Rinnakkaiskäsittelyn hyödyntäminen edellyttää, että aalto on suoritettava erätyönä.

## <a name="performance-improvements"></a>Suorituskykyä koskevat parannukset

Rinnakkaiskäsittelyn suorituskykyedut kuuluvat kahteen luokkaan:

- **Parannettu siirtomäärä** – Aaltojen siirtomäärä parantuu yleensä, vaikka rinnakkaiskäsittelyä ei ole määritetty, erityisesti tilanteissa, joissa nimikkeillä ei ole päällekkäisyyksiä aaltojen sisällä.
- **Yksittäisen aallon kohdistuksen parannus** – Testaaminen asiakastiedoilla on osoittanut, että suorituskyky parani lähes 50 prosenttia sen jälkeen, kun siirryttiin rinnakkaisiin kohdistuksiin. Rinnakkaiskäsittely tehdään sijainnin yläpuolella olevien nimikkeiden ja dimensioiden mukaan, joten parannukset määräytyvät sen mukaan, montako eri nimikettä aalto sisältää, mikä on käytettävissä oleva infrastruktuuri sekä mikä on kohdistuksen kesto verrattuna työn luonnin kestoon.

## <a name="configure-parallel-allocation"></a>Rinnakkaisen kohdistuksen määrittäminen

### <a name="warehouse-management-parameters"></a>Varastonhallinnan parametrit

Jos haluat käyttää rinnakkaista kohdistuskäsittelyä, siirry kohtaan **Varastonhallinta > Asetukset > Varastonhallinnan parametrit**, avaa **AAllon käsittely** -välilehti ja tee seuraavat asetukset:

- **Aallon käsittelyn eräryhmä** – Valitse eräryhmä, jota aaltojen alkukäsittelyn tulisi käyttää. Kohdistuksen käsittely tämän jälkeen voidaan tehdä käyttämällä eri eräryhmiä.
- **Käsittele aallot erinä** – Määritä arvoksi *Kyllä*, jos haluat käyttää rinnakkaiskäsittelyä.
- **Odota lukitusta (ms)** – Kirjoita millisekunteina aika, jonka kohdistusvaihe odottaa järjestelmäresurssia, joka on toisen kohdistusvaiheen lukitsema. Kun tämä aika ylitetään, aaltoa ei käsitellä ja virhesanoma tulee näkyviin. Yhden loogisen yksikön kohdistukselle on suositeltavaa sallia vähintään muutaman sekunnin aika.

Lisätietoja näistä ja muista aallon käsittelyvaihtoehdoista **Varastonhallinnan parametrit** -sivulla on kohdassa [Varastonhallinnan parametrit aaltojen käsittelylle](wave-warehouse-parameters.md).

## <a name="wave-process-methods"></a>Aallon käsittelymenetelmät

Rinnakkaiskäsittelyn voi määrittää seuraavasti:

1. Valitse **Varastonhallinta > Asetukset > Aallot A Aallon käsittelymenetelmät**.
1. Valitse ruudukossa `allocateWave`-menetelmä.
1. Valitse toimintoruudussa **Tehtävän määritys**.
1. **Aallon jälkeisen menetelmän tehtävän määritys** -sivu avautuu. Tässä ruudukossa luetellaan kaikki varastot, joissa olet konfiguroinut `allocateWave`-menetelmän. Rinnakkaiskäsittelyä käytetään vain luettelon varastoissa. Toimintoruudun painikkeiden avulla voit tarvittaessa lisätä varastoja ruudukkoon tai poistaa niitä ruudukosta. 
1. Tee kullekin varastolle seuraavat asetukset:
    - **Erätehtävien enimmäismäärä** – Määritä erätehtävien määrä, jota valitun varaston kohdistukssa on käytettävä. Erätehtävien optimaalinen määrä riippuu käytettävissä olevasta infrastruktuurista ja palvelimessa käsiteltävästä erätyöstä. Kokonaan aaltojen käsittelyyn määritetyllä neljän ytimen ympäristöllä tehdyt testit osoittivat, että kahdeksan tehtävän käyttö tuotti hyviä tuloksia.
    - **Aallon käsittelyn eräryhmä** – Tiettyjä eräryhmiä voidaan käyttää eri varastoille, jotta kohdistuskäsittely voidaan skaalata varastokohtaisesti.

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a>Rinnakkaisuuden ottaminen käyttöön ja poistaminen käytöstä kaikissa yrityksissä

Suosittelemme, että määrität `allocateWave`-menetelmän, joka suoritetaan rinnakkain kaikissa yritysyksiköissä, koska tämä parantaa aaltokäsittelyn suorituskykyä. Alkaen Supply Chain Management -versiosta 10.0.17 *Aaltojen rinnakkaisuus Allocate Wave -menetelmälle* -ominaisuus on oletusarvon mukaan käytössä kaikissa uusissa ja päivitetyissä asennuksissa, eikä sitä voi enää poistaa käytöstä. Kun tämä ominaisuus on otettu käyttöön, tapahtuu seuraavaa:

- `allocateWave`-menetelmä päivitetään niin, että se sisältää tehtävän konfiguraation asetuksen, jonka avulla voit **Aallon käsittelymenetelmät** -sivulla määrittää samalla kertaa suoritettavien tehtävien määrän, joka vastaa rinnakkaisten prosessien määrää. Tästä seuraa, että aallon kohdistusvaiheissa käytetty aika (joka on tavallisesti 30 – 60 % käsittelyn kokonaisajasta) vähenee tehtävien määrää vastaavalla kertoimella. Voit myös valita erän, joka määritetään näiden tehtävien suorittamista varten. On tärkeää muistaa, että kaikki yritykset on konfiguroitu käsittelemään aaltoja erissä. Käytössä olevat konfiguraatiot säilytetään niiden varastojen varastoissa, jotka on jo konfiguroitu käsittelemään aaltoja erätyönä, ja varastoissa, jotka on jo määritetty käyttämään `allocateWave`-menetelmää rinnakkain.
- Oletusarvon mukaan kaikki uudet yritykset on määritetty käsittelemään aaltoja erissä. Kaikissa uusissa varastoissa, joiden **Varastonhallintaprosessit**-asetus on käytössä, `allocateWave`-menetelmä on määritetty suoritettavaksi oletusarvon mukaan rinnakkain.
- **Varastonhallinnan parametrit** -sivulla **Käsittele aallot erinä** -arvona on *Kyllä* ja **Odota lukitusta  (ms)** -arvoksi asetetaan 15 sekunnin oletusarvo. Tämä tarkoittaa, että kaikki aallot suoritetaan erinä. Kun aaltoa suoritetaan, se hankkii nimikkeeseen ja sen ylätason sijainnin dimensioiden lukituksen kohdistusvaiheen aikana. Kun toinen aallon käsittelytehtävä yrittää hankkia saman lukituksen samalle tietueelle, se estetään, kunnes nykyinen käsittely on valmis. **Odota lukitusta (ms)** -asetus määrittää enimmäisajan, jonka järjestelmä odottaa ennen lukituksen vapauttamista.

Rinnakkainen kohdistuksen käsittely edellyttää, että aallon käsittely suoritetaan erätyönä. Sen vuoksi aaltojen käsittelyteho pienenenee, jos poistat **Käsittele aallot erinä** -määrityksen käytöstä, erityisesti jos aallon käsittely käyttää rinnakkaista prosessia, joka on määritetty asiaankuuluvien aaltomenetelmien tehtäväkonfiguraatiossa.

Voit tarvittaessa kumota kaikki asetukset, jotka on tehty oletusarvoisesti, kun *Aaltojen rinnakkaisuus Allocate Wave -menetelmälle* -ominaisuus on automaattisesti otettu käyttöön esiintymässä. Toimi seuraavasti:

- Valitse **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**. Käytä **Aallon käsittely** -välilehdessä haluamiasi arvoja **Käsittele aallot erinä**- ja **Odota lukitusta (ms)** -asetuksille.
- Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon käsittelymenetelmät**. Valitse `allocateWave`-menetelmä. Valitse toimintoruudusta **Tehtävän määritys** avataksesi sivun, jolla luetellaan kaikki varastot, joissa menetelmä on määritetty suoritettavaksi rinnakkain. Muokkaa tai poista erätehtävien määrää ja määritettyä aaltoryhmää kullekin luettelossa olevalle varastolle tarpeen mukaan.

## <a name="troubleshooting"></a>Vianmääritys

### <a name="troubleshoot-using-the-infolog"></a>Vianmääritys infolokin avulla

Koska käytetään eräkehystä, aaltojen käsittelyssä esiintyvät virheet siepataan erätöiden infolokien osana. Voit lukea aaltoon liittyvät erätyöt seuraavasti:

1. Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.
1. Valitse tarkastettava aalto.
1. Avaa toimintoruudussa **Aalto**-välilehti ja valitse **Aalto** -ryhmässä **Erätyöt**.

Aaltojen käsittely itsensä korjaavaa, joten kaikki käsittelyn aikana havainnut virheet on raportoitava infolokin avulla.

Rinnakkaiskäsittelyyn liittyvä tyypillinen virhe voi olla se, että kaksi aaltoa yrittää kohdistaa saman nimikkeen samanaikaisesti, eikä yksi niistä ole valmis, jotta toinen ei voi hankkia lukitusta määritettynä aikana. Jos näin tapahtuu, erätöiden loki sisältää tiedot, joiden mukaan nimikkeen lukitusta ei voitu hankkia. Tällöin epäonnistunut aalto on käsiteltävä uudelleen.

Koska käsittely on rinnakkaista, tiedot on ylläpidettävä eri taulukoissa käsittelyn tilan seuraamista varten. Tämä tarkoittaa, että erätöiden lokit voivat sisältää virheitä, kuten avainten kaksoiskappaleiden virheitä.

Erätehtävien virheet kuuluvat myös erätöiden lokiin. Tärkeimmät tiedot ovat yleensä alaosassa.

Muutamista harvinaisissa tapauksissa, jos esimerkiksi SQL-yhteys päätettiin, voidaan aallon käsittely lopettaa epäyhtenäisessä tilassa, jossa erätyö näyttää olevan käynnissä, mutta käsittely on pysäytetty. Aalto ei voi käsitellä tällaisia virheitä, joten epäonnistuneita aaltoja yritetään puhdistaa, kun seuraava aalto suoritetaan. Voit myös tehdä seuraavat toimet, jos nykyinen aalto on epäyhtenäisessä tilassa:

1. Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.
1. Valitse aalto, jonka haluat siivota.
1. Avaa toimintoruudussa **Aalto**-välilehti ja valitse **Aalto** -ryhmässä **Tyhjennä aallon tiedot**.

### <a name="troubleshoot-using-the-wave-progress-log"></a>Vianmääritys aallon etenemislokin avulla

Jos **Varastonhallinnan parametrit** -sivulla on otettu käyttöön **Luo aallon etenemisloki** -asetus, lokitietue luodaan aina, kun nimikkeen ja sen dimensioiden aikakohdistukset alkavat ja päättyvät. Ota tämä loki käyttöön vain silloin, kun tarvitset sitä, esimerkiksi alkutestauksen tai vianmäärityksen aikana. Kun tämä asetus on käytössä, voit tarkastella lokia seuraavasti:

1. Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.
1. Valitse tarkastettava aalto.
1. Valitse toimintoruudun **Aalto**-välilehden **Aalto**-ryhmässä **Edistyminen**.
