---
title: Klusterisijainti täynnä
description: Tässä ohjeaiheessa on tietoja Klusterisijainti täynnä -ominaisuudesta. Tämä ominaisuus on vaihtoehto tiukalle työkatkosääntöjen valvonnalle, kun käytössä on klusterikeräily. Tämä johtuu siitä, että ominaisuus mahdollistaa konttien ja kassien tilavuusrajoitteiden aiempaa suuremman virhemarginaalin.
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3610725815b35609ee98b69b367db2945bbf166a
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016168"
---
# <a name="cluster-position-full"></a>Klusterisijainti täynnä

[!include [banner](../includes/banner.md)]

*Klusterisijainti täynnä* -ominaisuus on vaihtoehto tiukalle työkatkosääntöjen valvonnalle, kun käytössä on klusterikeräily. Tämä johtuu siitä, että ominaisuus mahdollistaa konttien ja kassien tilavuusrajoitteiden aiempaa suuremman virhemarginaalin. Yleissä skenaariossa kaikki työtilauksen nimikkeet eivät mahdu valittuun konttiin. Klusterikeräilyä suorittavilla varastotyöntekijöillä on muutama vaihtoehto tässä skenaariossa. He voivat muuttaa suuremman kontin kokoa tai kehittää esimehen kanssa toisenlaisen ratkaisun.

Tämä ominaisuus sisältää mahdollisuuden käyttää **Täysi** -painiketta klusterin yhdessä työyksikössä. Vanhemmissa versioissa tämä vaihtoehto oli käytettävissä vain tavallisissa tilauskeräilyssä, ei klusterikeräilyssä. Tämä ominaisuus eroaa kuitenkin normaalista **Täysi** -painikkeesta siten, että se peruuttaa jäljellä olevan työn. Se ei ehdota käyttäjälle toisen lokeron lisäämistä samaan klusteriin eikä luo automaattisesti uutta työtä.

## <a name="turn-on-the-cluster-position-full-feature"></a>Klusterisijainti täynnä -ominaisuuden ottaminen käyttöön

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Ominaisuuden nimi:** *Klusterisijainti täynnä*

## <a name="setup"></a>Luo perustiedot

Tässä osassa on ohjeita *Klusterisijainti täynnä* -ominaisuuden määrittämiseksi ja käyttämiseksi sekä ominaisuuden esimerkki.

### <a name="make-sample-data-available"></a>Ota mallitiedot käyttöön

[Esimerkkiskenaarion](#example-scenario) käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon [vakiodemotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu. Sinun on myös valittava **USMF** -yritys ennen kuin aloitat.

Voit hyödyntää esimerkkiskenaariota myös ohjeena, kun käytät tätä ominaisuutta tuotantojärjestelmässä. Siinä tapauksessa tässä kuvattujen asetusten omat arvot on korvattava.

### <a name="cluster-profiles"></a>Klusteriprofiilit

Määritä, milloin klustereiden tunnukset luodaan automaattisesti, miten monta sijaintia käytetään, milloin klusterit rikotaan ja miten keräilytyö järjestetään ja tarkistetaan.

1. Valitse **Varastonhallinta \> Asetukset \> Mobiililaite \> Klusteriprofiilit**.
1. Valitse luetteloruudusta **Luo klusteri** -tietue.
1. Tarkista **Yleiset** -pikavälilehdessä seuraavat arvot:

    - **Luo klusterin tunnus:** *Kyllä*
    - **Aktivoi sijainnit:** *Kyllä*
    - **Sijaintien määrä:** *2*
    - **Sijainnin nimi:** *Numeerinen*
    - **Hajota klusteri:** *Hyllytys*
    - **Lajittelun tarkistuksen tyyppi:** *Sijainnin tarkistus*

1. **Klusterin lajittelu** -pikavälilehdessä. Ruudukon on oltava tyhjä (se ei saa sisältää rivejä).

### <a name="work-templates"></a>Työmallit

Määritä, miten keräilytyö luodaan klusterin keräilyä varten.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Määritä sivun yläosassa **Työtilauksen tyyppi** -kentän arvoksi *Myyntitilaukset*.
1. Varmista, että seuraavat esittelytietojen työmallit on luetteloitu. Jos ne eivät ole käytettävissä, et voi suorittaa skenaariota loppuun.

    - 61 MT:n vaihe
    - 61 MT:n klusterin keräily

### <a name="location-directives"></a>Sijaintidirektiivit

Sinun on määritettävä, mistä nimikkeet kerätään ja mihin ne sijoitetaan.

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Määritä luettelon otsikossa **Työtilaustyyppi** -kentän arvoksi *Myyntitilaukset*.
1. Varmista, että seuraavat esittelytietojen myyntitilausdirektiivit on luetteloitu. Jos ne eivät ole käytettävissä, et voi suorittaa skenaariota loppuun.

    - 61 Klusterin keräily
    - 61 MT:n keräilyjärjestys

### <a name="mobile-device-menu-items"></a>Mobiililaitteen valikkovaihtoehdot

Määritä mobiililaitteen valikkovaihtoehto käyttämään klusterikeräilyn ohjaamaa työtä. Klusterikeräilyn mobiililaitteen valikon vaihtoehdon **Salli työn jakaminen** -parametri on otettava käyttöön ja *Myyntitilauksen keräily* -työluokka on lisättävä.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse luetteloruudusta **Klusterikeräilyn luominen** -tietue.
1. Valitse toimintoruudussa **Muokkaa**.
1. Määritä **Yleiset** -pikavälilehdessä seuraavat arvot:

    - **Ohjaaja:** *Klusterikeräily*
    - **Luo rekisterikilpi:** *Kyllä*
    - **Salli työn jakaminen:** *Kyllä*
    - **Klusteriprofiilin tunnus:** *Luo klusteri*

    Hyväksy oletusarvot kaikille muille kentille.

1. Lisää **Työluokat** -pikavälilehdessä seuraavat kaksi riviä tarvittaessa:

    - Rivi 1 (yleensä ovat esittelytiedoissa):

        - **Työluokan tunnus:** *Myynti* 
        - **Työtilauksen tyyppi:** *Myyntitilaukset*

    - Rivi 2 (todennäköisesti eivät ole esittelytiedoissa):

        - **Työluokan tunnus:** *Myyntitilauksen keräily*
        - **Työtilauksen tyyppi:** *Myyntitilaukset*

1. Siirry toimintoruudun **Työn vahvistusasetukset** -kohtaan.
1. Valitse **Muokkaa**.
1. Anna ruudukon riville seuraavat arvot.
    - **Työtyyppi** - *Keräily*
    - **Tuotteen vahvistus** - *Valitse valintaruutu*

1. Valitse toimintoruudussa **Tallenna** ja sulje sivu.

## <a name="create-picking-work"></a>Luo keräystyö

Ennen kuin voit aloittaa klusterikeräilyn, sinun on luotava lähtevä työ. Aiemmin luomasi klusteriprofiili määrittää kaksi klusteripositiota. Näin ollen myyntitilauksen keräilylle on luotava vähintään kaksi työtunnusta. Tämän skenaarion tapahtumat ovat varastossa *61* ja tapahtumissa käytetään nimikkeitä *L0101* ja *T0100*. Esittelytiedoissa on oltava riittävästi käytettävissä olevaa varastoa näille nimikkeille. Varmista, että sinulla on riittävästi varastoa tapahtumien suorittamista varten.

### <a name="create-sales-order-1"></a>Luo myyntitilaus 1

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Luo myyntitilaus 1 valitsemalla **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-010*
    - **Varasto** : *61*

1. Valitse **OK**.
1. Uusi myyntitilaus avataan. Lisää **Myyntitilausrivit** -pikavälilehdessä rivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *T0100*
    - **Määrä** *5*

1. Anna **Toimitus** -välilehden **Rivin tiedot** -pikavälilehden **Vahvistettu lähetyspäivämäärä** -kenttään kuluvan päivän päivämäärä.
1. Lisää **Myyntitilausrivit** -pikavälilehdessä toinen rivi, jonka asetukset ovat seuraavat:

    - **Nimiketunnus:** *L0101*
    - **Määrä** *20*

1. Anna **Toimitus** -välilehden **Rivin tiedot** -pikavälilehden **Vahvistettu lähetyspäivämäärä** -kenttään kuluvan päivän päivämäärä.
1. Varaa varastoa jokaiselle lisätylle riville seuraavasti:

    1. Valitse varattava rivi.
    2. Valitse **Myyntitilausrivit** -pikavälilehdessä **Varasto \> Varaus**.
    3. Varaa varasto **Varaus** -sivun toimintoruudussa valitsemalla **Varaa erä**.
    4. Sulje **Varaus** -sivu.

1. Valitse toimintoruudussa **Varasto** -välilehdellä **Vapauta varastoon**.

    Kun vapautus on tehty, näkyviin tulee tietosanomia, jotka sisältävät luodun aallon ja luodut kuormatunnukset.

### <a name="create-sales-order-2"></a>Luo myyntitilaus 2

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Luo myyntitilaus 2 valitsemalla **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-011*
    - **Varasto** : *61*

1. Valitse **OK**.
1. Uusi myyntitilaus avataan. Lisää **Myyntitilausrivit** -pikavälilehdessä rivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *L0101*
    - **Määrä** *20*

1. Anna **Toimitus** -välilehden **Rivin tiedot** -pikavälilehden **Vahvistettu lähetyspäivämäärä** -kenttään kuluvan päivän päivämäärä.
1. Lisää **Myyntitilausrivit** -pikavälilehdessä toinen rivi, jonka asetukset ovat seuraavat:

    - **Nimiketunnus:** *T0100*
    - **Määrä** *2*

1. Anna **Toimitus** -välilehden **Rivin tiedot** -pikavälilehden **Vahvistettu lähetyspäivämäärä** -kenttään kuluvan päivän päivämäärä.
1. Varaa varastoa jokaiselle lisätylle riville seuraavasti:

    1. Valitse varattava rivi.
    2. Valitse **Myyntitilausrivit** -pikavälilehdessä **Varasto \> Varaus**.
    3. Varaa varasto **Varaus** -sivun toimintoruudussa valitsemalla **Varaa erä**.
    4. Sulje **Varaus** -sivu.

1. Valitse toimintoruudussa **Varasto** -välilehdellä **Vapauta varastoon**.

    Kun vapautus on tehty, näkyviin tulee tietosanomia, jotka sisältävät luodun aallon ja luodut kuormatunnukset.

### <a name="get-work-ids-and-license-plate-numbers"></a>Työtunnusten ja rekisterinumeroiden haku

Luotuna on nyt kaksi työtunnusta. Molemmilla tunnuksilla on kaksi keräilyriviä. Etsi työtunnukset ja rekisterikilpien toimeksiannot alla olevien ohjeiden avulla.

1. Valitse **Varastonhallinta \> Työ \> Työn tiedot**.
1. Hae **Yleiskatsaus** -ruudukosta kahden juuri luodun myyntitilauksen **Tilausnumero** -sarake. Merkitse muistiin kunkin myyntitilauksen vastaava työtunnus.
1. Valitse kunkin myyntitilauksen rivi, jos haluat nähdä **Rivit** -ruudukon liittyvät tiedot. Merkitse muistiin kunkin nimikkeen keräyssijainti.
1. Siirry kohtaan **Varastonhallinta \> Kyselyt ja raportit \> Käytettävissä olevien luettelo**.
1. Valitse toimintoruudussa **Dimensiot** ja avaa **Dimension näyttö** -valintaikkuna.
1. Varmista, että **Rekisterikilpi** -, **Varasto** - ja **Nimikenumero** -valintaruudut on valittu. Valitse sitten **OK**.
1. Määritä **Suodatin** -ruudussa seuraavat suodattimet:

    - **Nimiketunnus** – **on** *L0101* tai *T100*
    - **Varasto** – **alkaa numerolla** - *61*

1. Kirjoita muistiin näkyvissä olevat **rekisterikilven** arvot.

## <a name="example-scenario"></a><a name="example-scenario"></a>Esimerkkiskenaario

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a>Mobiililaitteen työnkulun suoritus – Tuotteen työn vahvistuksen määritys

1. Kirjaudu varastosovellukseen käyttäjänä varastossa *61*.
1. Siirry kohtaan **Lähtevät \> Klusterikeräilyn luominen**.

    Näkyviin tulee **TEHTÄVÄ: Liitä työ klusteriin** -sivu.

1. Anna myyntitilaukselle 1 työtunnus ja liitä se klusterisijaintiin 1.
1. Valitse **OK** (valintamerkkisymboli).
1. Anna myyntitilaukselle 2 työtunnus ja liitä se klusterisijaintiin 2.
1. Valitse **OK** (valintamerkkisymboli).

    Näkyviin tulee **TEHTÄVÄ: Klusterikeräilyn luominen: Keräily** -sivu, joka sisältää *Nimike L0101 2 PL* -kohdan.

Koska klusteriprofiili määrittää sijaintien numeroksi 2, järjestelmä ohjaa käyttäjän automaattisesti ensimmäiseen konsolidoituun keräilyyn. Se on nimikkeen *L0101* kaksi kuormalavaa.

Kun noudatat seuraavia ohjeita, voit missä tahansa vaiheessa valita **Tiedot** -välilehden ja katsoa tehtävän lisätietoja, kuten keräilysijainnin.

1. Määritä **NIMIKE** -kentän arvoksi *L0101*. Tämä vahvistaa nimikenumeron, joka vaaditaan tälle valikon vaihtoehdolle (se määritettiin aiemmin valitsemalla **Työn vahvistuksen määritys** **Mobiililaitteen valikon vaihtoehto** -sivulla tämän valikon vaihtoehdon luomisen yhteydessä).
1. Anna rekisterikilpinumero, joka liittyy keräiltävässä sijainnissa olevaan nimikkeeseen. Keräile kaksi kuormalavaa.
1. Määritä **RK** -kentän arvoksi *LP\_PICK\_01*.
1. Valitse **OK** (valintamerkkisymboli).

    **TEHTÄVÄ: Lajittelu: Klusterikeräilyn luominen** -sivu avautuu. Tässä voit lajitella kaksi keräiltyä kuormalavaa keräilysijaintiin. Tämä sijainti voi olla kassi tai kontti, jota käytetään keräillyn varaston erottelussa myyntitilauksen mukaan.

1. Tarkastele nimikkeelle ( *L0101* ) ja määrälle ( *20* kpl) näytettäviä tietoja. Ne lajitellaan sijaintiin (myyntitilaukselle 1).
1. Määritä **SIJAINTI NA** -kentän arvoksi *1*.
1. Valitse **OK** (valintamerkkisymboli).
1. Tarkastele nimikkeelle ( *L0101* ) ja määrälle ( *20* kpl) näytettäviä tietoja. Ne lajitellaan sijaintiin 2 (myyntitilaukselle 2).
1. Määritä **SIJAINTI NA** -kentän arvoksi *2*.
1. Valitse **OK** (valintamerkkisymboli).

    Näkyviin tulee **TEHTÄVÄ: Klusterikeräilyn luominen: Keräily** -sivu, joka sisältää *Nimike T0100 7 kpl* -kohdan.

Tässä skenaariossa sijainti 1 ei voi hyväksyä myyntitilauksen 1 täyttämiseksi keräiltävien nimikkeiden täyttä määrää. Sijainti on merkittävä täydeksi. Tässä skenaariossa tehdään toisen nimikkeen osittainen keräily. Toinen nimike keräillään osittain sijaintiin 1. Luodaan uusi ty, joka keräilee jäljellä olevan nimikkeen tilauksen täyttämiseksi.

1. Valitse valikkopainike (jossa on allekkain useita viivoja) ja lopeta Oikaisu sisään -tehtävä valitsemalla **Sijainti täynnä**.
1. Määritä täynnä oleva sijainti ja valitse *1*.
1. Valitse **OK** (valintamerkkisymboli).
1. Anna keräilymäärä, joka on yhä keräiltävissä sijaintiin 1. Järjestelmä voi määrittää, mitä nimiketunnusta kerätään.
1. Syötä *2*.
1. Valitse **OK** (valintamerkkisymboli).
1. Vahvista nimiketunnus, jotta jäljellä olevan nimikkeen keräily voidaan viimeistellä sijaintiin 2.
1. Määritä **NIMIKE** -kentän arvoksi *T0100*.
1. Valitse **OK** (valintamerkkisymboli).
1. Anna rekisterikilpi, josta nimike keräillään, määrittämällä **RK** -kentän arvoksi *LPREPL04*.
1. Valitse **OK** (valintamerkkisymboli).
1. Tarkastele nimikkeelle ( *T0100* ) ja määrälle ( *2* kpl) näytettäviä tietoja. Ne lajitellaan sijaintiin 2 (myyntitilaukselle 2).
1. Määritä **SIJAINTI NA** -kentän arvoksi *2*.
1. Valitse **OK** (valintamerkkisymboli).
1. Tarkastele nimikkeelle ( *T0100* ) ja määrälle ( *2* kpl) näytettäviä tietoja. Ne lajitellaan sijaintiin 1 (myyntitilaukselle 1).
1. Määritä **SIJAINTI NA** -kentän arvoksi *1*.
1. Valitse **OK** (valintamerkkisymboli).

    **TEHTÄVÄ: Klusterikeräilyn luominen: Hyllytys** -sivu avautuu.

Tässä skenaariossa klusterikeräily on valmis, ja käyttäjä ohjataan hyllyttämään keräillyt nimikkeet sijainnista 1 ja 2 väliaikaiseen sijaintiin *STAGE01*.

1. Tarkista sivun tiedot. Se osoittaa, että väliaikaiseen sijaintiin hyllytettävä määrä on yhteensä *44*.
1. Valitse **OK** (valintamerkkisymboli).

    Näyttöön tulee Klusteri on valmis -sanoma.

Voit nyt käyttää valikon **Myynnin keräily** -vaihtoehtoa jäljellä olevan määrän keräilemiseksi. Voit sitten käyttää valikon **Myynnin kuormaus** -vaihtoehtoa ja siirtää nimikkeet väliaikaisesta sijainnista lastauslaituriin.
