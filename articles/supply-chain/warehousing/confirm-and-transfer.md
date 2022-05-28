---
title: Vahvista ja siirrä
description: Tässä aiheessa kerrotaan vahvistus- ja siirtotoiminnosta, joiden avulla käyttäjien on mahdollista lähettää kuormia varastosta ennen kuin kaikki kuormiin liittyvät työt on hoidettu.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate,WHSWorkTemplateTable,WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0d34dd1b33467aa1ea3a723e1baaf7f06285c3fa
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675484"
---
# <a name="confirm-and-transfer"></a>Vahvista ja siirrä

[!include [banner](../includes/banner.md)]

*Vahvistus ja siirto* -toiminnon avulla käyttäjien on mahdollista lähettää kuormia varastosta ennen kuin kaikki kuormiin liittyvät työt on hoidettu. Kun lähetys, jonka kuormarivejä ei ole täysin keräilty, saapuu, lähetyksen vahvistajan on joko jaettava jäljelle jäävät määrät uuteen kuormaan tai peruutettava keskeneräiset kuormat.

Järjestelmät, joiden asetuksissa sallitaan kuorman jakaminen, ovat hyödyllisiä tilanteissa, joissa suunnitellut ja osittaiset kuormat on mukautettava uuden tai muuttuneen tilanteen mukaan.

Asiakasohjelma mahdollistaa osittaisten kuormien sulkemisen ja vahvistamisen lähetyksen yhteydessä. Kaikki jäljelle jäävät lähetykset ja kuormarivit (täydet tai keskeneräiset rivimäärät) siirretään uutena luotuun kuormaan ja lähetykseen, jos siirto vaaditaan ja se on sallittu asetuksissa. Uudet lähetykset ja kuormat luodaan automaattisesti lähetysten ja kuormanluonnin alkuperäisasetusten mukaisesti, ja niiden tärkeimmät määritteet pysyvät samana. On myös mahdollista peruuttaa jäljelle jäävät määrät automaattisesti, jos työtilausta ei ole vielä luotu ja peruuttaminen on käyttäjän mielestä tarpeen.

Tämä toiminto sopii tilanteisiin, joissa täysi kuorma ei mahdu yhteen trukkiin tai kuorman tietyn osan on lähdettävä varastosta ennen kuin muu kuorma on valmiina lähetettäväksi. Näissä tilanteissa jäljelle jääneet tuotteet voi siirtää uuteen kuormaan ja siten uuteen trukkiin. Koska tätä toimintoa voidaan käyttää sellaisiin kuormiin, joiden olisi muuten tarkoitus olla lähetettäessä täysiä, lähettämisestä tulee joustavampaa ja esimiehet voivat keskittyä erikoisempien ja yllättävien tilanteiden ratkaisemiseen.

Kun kuorma on jaettu, *Vahvistus ja siirto* -toiminto suorittaa seuraavat tehtävät:

- Uusia kuormia ja lähetyksiä luodaan tarpeen mukaan. Jokaisella kuormalla tai lähetyksellä on melkein kaikki samat määritteet kuin alkuperäisellä kuormalla tai lähetyksellä. Ainoa poikkeus on kuorman tila, joka lasketaan uudelleen työn tilaan perustuen.
- Käyttäjälle ilmoitetaan, että uusi kuorma on luotu. Käyttäjälle ilmoitetaan myös uuden kuorman tunnus.
- Jaettuihin kuormariveihin, työn otsikoihin ja työriveihin päivitetään uudet kuorma- ja lähetystiedot.
- Jos koko lähetys jaetaan, sen tiedot säilytetään ja vain kuorman viitteet päivitetään. Jos lähetys on jaettava, uusi lähetys luodaan.

Kun jäljelle jääneet määrät peruutetaan, kaikki kuormarivin määrät, joita ei ole keräilty ja joihin ei ole liitetty peruuttamatonta työtä, poistetaan kuormasta. Jos työ on kesken, käyttäjä voi vain jakaa kuorman. Jäljelle jääneitä määriä ei voi peruuttaa.

Voit jakaa vain ne kuormat, jotka täyttävät kaikki seuraavat ehdot:

- Yhdellä tai useammalla kuormarivillä on keräiltyjä tuotteita.
- Kuorman tila on pienempi kuin kuorman todellinen määrä.
- Kuormarivin tietoja ei ole. (Nämä tiedot luodaan rekisterikilven konsolidoinnin avulla väliaikaisessa sijainnissa, ja Vahvistus ja siirto -toiminto ei tue rekisterikilven konsolidointia.)
- Pakkaussijainnissa ei ole pakkaamista odottavaa varastoa. (*Vahvista ja siirrä* -ominaisuus ei tue varastoa, joka on kerätty pakkausasemalle mutta jota ei ole pakattu ellei pakattuja kontteja ole sijoitettu väliaikaisiin sijainteihin ja ellei niille ole luotu lataustyötä.)

> [!NOTE]
> Tämä toiminto eroaa kuljetuskuormatoiminnosta, jota käytetään sellaisissa varastoissa, joissa kuormia ei koskaan voida suunnitella ja luoda ennen keräilyä, vaan joissa vapaa kuljetustila kuormataan, kun keräily on saatu valmiiksi.
>
> Käytä *Vahvistus ja siirto* -toimintoa tilanteissa, joissa kuormat ovat tavallisesti suunniteltuja ja etukäteen luotuja, mutta joiden kanssa joskus käy niin, että kuorma ei mahdu käytettävissä olevaan kuljetukseen (esim. trukkiin).

## <a name="turn-the-confirm-and-transfer-feature-on-or-off"></a>Vahvista ja siirrä -toiminnon käyttöönotto tai käytöstä poisto

Tässä aiheessa kuvatun toiminnon käyttäminen edellyttää, että *Vahvista ja siirrä* -toiminto on käytössä järjestelmässäsi. Supply Chain Managementin versiosta 10.0.25 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä. Jos käytät vanhempaa versiota kuin 10.0.25, järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Vahvista ja siirrä* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

## <a name="set-up-confirm-and-transfer"></a>Vahvistuksen ja siirron määrittäminen

Jos haluat käyttää *Vahvistus ja siirto* -toimintoa, sinun on otettava se käyttöön kaikissa olennaisissa kuormamalleissa. Voit myös tarpeen mukaan valmistella toimintoon kanssa yhteensopivia työmalleja. Jos haluat kokeilla tässä aiheessa myöhemmin esiteltävää esimerkkitilannetta, määritä järjestelmäsi tämän osion ohjeiden mukaan. (Esimerkkitilanne perustuu **USMF**-esittelytietoihin.)

### <a name="prepare-your-load-templates"></a>Kuormamallien valmisteleminen

1. Valitse **Varastonhallinta \> Asetukset \> Kuorma \> Kuormamallit**.
1. Valitse toimintoruudussa **Muokkaa**, jotta saat sivun muokkaustilaan.
1. Valitse **Salli kuorman jakaminen lähetyksen vahvistamisen aikana** -valintaruutu kaikissa aiemmin luoduissa malleissa, joissa haluat ottaa toiminnon käyttöön. Vaihtoehtoisesti voit valita kohdan **Uusi**, luoda uuden mallin ja määrittää sen haluamallasi tavalla. Kaikki tämän mallin avulla luodut kuormat perivät tämän toiminnon. (Jos hyödynnät **USMF**-esittelytietoja, ota toiminto käyttöön **20' Kontti** -kuormamallia varten.)

### <a name="prepare-your-work-templates"></a>Työmallien valmisteleminen

Tätä asetusta ei vaadita kaikissa tilanteissa. Tässä näytetyn esimerkin avulla taataan, että työ voidaan jakaa lähetyksen mukaan, mikä tukee myöhemmin tässä aiheessa esiteltävää esimerkkitilannetta. Tähän lopputulokseen voi päätyä myös muilla tavoilla.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Valitse sivun yläosan ruudukossa aiemmin luotu työmalli, jota varten haluat määrittää *Vahvistus ja siirto* -toiminnon. (Jos hyödynnät **USMF**-esittelytietoja, valitse kohta **51 Poiminta** -työmalli.) Voit myös luoda uuden työmallin.
1. Valitse toimintoruudussa **Muokkaa kyselyä**, jotta voit avata **Myynti**-valintaikkunan.
1. Lisää ruudukkoon rivi valitsemalla **Myynti**-valintaruudun **Lajittelu**-välilehdessä **Lisää**.
1. Aseta uudelle riville seuraavat arvot:

    - **Taulukko:** *Väliaikaiset työtapahtumat*
    - **Johdettu taulukko:** *Väliaikaiset työtapahtumat*
    - **Kenttä:** *Lähetyksen tunnus*
    - **Hakusuunta:** *Laskeva*

1. Valitse **OK**, tallenna asetuksesi ja sulje **Myynti**-valintaikkuna.
1. Jos näyttöön tulee sanoma, jossa ilmoitetaan ryhmittelyn nollauksesta, valitse **Kyllä** ja jatka.
1. Valitse **Työmallit**-sivun yläosan ruudukossa malli, jota juuri muokkasit, ja valitse sitten toimintoruudussa kohta **Työn otsikoiden jakaminen**.
1. Valitse toimintoruudussa **Muokkaa**, jotta saat sivun muokkaustilaan.
1. Aseta ruudukkoon seuraavat arvot:

    - **Taulukon nimi:** *Väliaikaiset työtapahtumat*
    - **Kentän nimi:** *Lähetyksen tunnus*
    - **Ryhmittele tämän kentän mukaan:** Valitse tämä valintaruutu.

1. Valitse toimintoruudussa **Tallenna**.
1. Sulje sivu.

## <a name="scenario"></a>Skenaario

Tässä tilanteessa näkyy esimerkki siitä, kun keräilyprosessi ei vielä ole valmis, mutta jo keräillyt nimikkeet on kuormattava trukkiin ja lähetettävä joka tapauksessa. Siksi käyttäjä voi jakaa keräilemättömät kuormarivit uuteen kuormaan. Kaikki tietosuhteet päivitetään sitten automaattisesti.

> [!NOTE]
> Tässä tilanteessa kuvatut tietyt arvot perustuvat **USMF**-esittelytietoihin. Suosittelemme, että käytät näitä esittelytietoja, kun esittelet tai opettelet toiminnon käyttöä. Jos et käytä **USMF**-esittelytietoja, korvaa omat arvosi vaaditun mukaisiksi.

### <a name="step-1-create-a-load-that-has-multiple-load-lines"></a>Vaihe 1: Useita kuormarivejä sisältävän kuorman luominen

Ennen kuin voit käyttää tätä toimintoa, sinulla on oltava useita kuormarivejä sisältävä kuorma. Sinun on myös varmistettava, että keräilysijainneissa on tarpeeksi varastoa luomiesi myyntitilausten kaikille nimikkeille. Tarkista sijaintidirektiivin asetukset (**Varastonhallinta \> Asetukset \> Sijaintidirektiivit**) ja huomioi keräilysijainnit, joita käytetään myyntitilauksen keräilyssä. Jos sinun on muokattava varastoa, voit luoda manuaalisia siirtoja tai hyödyntää täydennystä tai mitä tahansa muuta virtausta tarpeen mukaan.

Aloita hyväksyttävän kuorman luonti luomalla kolme myyntitilausta näiden vaiheiden mukaisesti.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi** ja avaa **Luo myyntitilaus**-valintaikkuna.
1. Aseta **Luo myyntitilaus** -valintaikkunassa (vähintään) seuraavat arvot:

    - Aseta **Asiakas**-pikavälilehdessä **Asiakastili**-kentän arvoksi *US-004* (*Cave Wholesales*).
    - Aseta **Yleinen**-pikavälilehden **Varasto**-kentässä arvoksi *51*.

1. Valitse **OK** luodaksesi uuden myyntitilauksen ja sulje **Luo myyntitilaus** -valintaikkuna.
1. Uusi myyntitilauksesi avataan. Lisää **Myyntitilausrivit**-ruudukossa rivi, jossa on seuraavat arvot:

    - **Nimiketunnus:** *M9200*
    - **Määrä** *40*
    - **Yksikkö:** *ea*

1. Valitse ruudukon yläpuolella olevasta **Varasto**-valikosta kohta **Varaus**.
1. Valitse toimintoruudussa kohta **Varaa erä** ja avaa **Varaus**-sivu.
1. Varaa varasto myyntirivillä ja sulje **Varaus**-sivu.
1. Toista vaiheet 1–4 ja lisää toinen myyntitilaus samalle asiakkaalle ja varastolle.
1. Lisää kaksi myyntiriviä, joilla on seuraavat arvot. Kun olet lisännyt uuden rivin, varaa sille varasto vaiheissa 6–8 kuvattujen ohjeiden mukaan.

    - **Rivi 1:** Aseta **Nimiketunnus**-kentän arvoksi *M9200*, **Määrä**-kentän arvoksi *30* ja **Yksikkö**-kentän arvoksi *kpl*.
    - **Rivi 2:** Aseta **Nimiketunnus**-kentän arvoksi *M9201*, **Määrä**-kentän arvoksi *20* ja **Yksikkö**-kentän arvoksi *kpl*.

1. Toista vaiheet 1–4 ja lisää kolmas myyntitilaus samalle asiakkaalle ja varastolle.
1. Lisää kaksi myyntiriviä, joilla on seuraavat arvot. Kun olet lisännyt uuden rivin, varaa sille varasto vaiheissa 6–8 kuvattujen ohjeiden mukaan.

    - **Rivi 1:** Aseta **Nimiketunnus**-kentän arvoksi *M9201*, **Määrä**-kentän arvoksi *20* ja **Yksikkö**-kentän arvoksi *kpl*.
    - **Rivi 2:** Aseta **Nimiketunnus**-kentän arvoksi *M9202*, **Määrä**-kentän arvoksi *60* ja **Yksikkö**-kentän arvoksi *kpl*.

#### <a name="load-planning-workbench"></a>Kuormasuunnittelun työtila

Kuormasuunnittelun työtila kokoaa lähetykset ja vapauttaa myyntitilausrivit varastoon kuormamallin tunnuksen avulla.

1. Valitse **Varastonhallinta \> Kuormat \> Kuormasuunnittelun työtila**.
1. Valitse **Varasto**-kentässä *51*.

    Voit nyt koota kuorman juuri luomillesi myyntitilauksille.

1. Valitse **Myyntirivit**-välilehden ruudukossa uusien myyntitilausten myyntirivit.
1. Valitse toimintoruudun **Tarjonta ja kysyntä** -välilehden **Lisää**-ryhmässä kohta **Uuteen kuormaan**.
1. Valitse **Lataa mallin määritys** -valintaikkunan **Lataa mallin tunnus** -kentässä kohta *20' Kontti*.
1. Valitse **OK**.
1. Etsi **Kuormasuunnittelun työtila** -sivun **Kuormat**-osan ruudukosta varastolle *51* juuri luotu kuorman tunnus. Vieritä oikealle, kunnes näet **Salli kuorman jakaminen lähetyksen vahvistamisen aikana** -sarakkeen. Valintaruudun on oltava valittuna kuormasi kohdalla.
1. Valitse kuorma.
1. Luo työ valitsemalla ruudukon yläpuolella olevasta **Vapauta**-valikosta kohta **Vapauta varastoon**.
1. Varmista **Vapauta kuorma varastoon** -valintaikkunassa, että **Sisällytettävät tietueet** -pikavälilehdessä näkyy kuormasi tunnus.
1. Valitse **OK**.

    Näyttöön saattaa tulla Käsitellään toimintoa -sanoma, kun järjestelmä luo lähetyksiä ja työtä.

1. Kuormasi tilan pitäisi nyt olla *Aalto*-tilassa **Kuormasuunnittelun työtila** -sivun **Kuormat**-osassa. Valitse kuorma ja sitten ruudukon yläpuolella olevasta **Aiheeseen liittyviä tietoja** -valikosta kohta **Aallon tiedot**, jotta näet luodut lähetystunnukset. Kun olet valmis, sulje **Aalto**-sivu.
1. Valitse kuorma **Kuormasuunnittelun työtila** -sivun **Kuormat**-osasta ja valitse sitten ruudukon yläpuolella olevasta **Aiheeseen liittyviä tietoja** -valikosta kohta **Työn tiedot**, jotta voit nähdä myyntitilauksille luodun työn.
1. Huomioi luodut työtunnukset. Sinun on ehkä vieritettävä näyttöä oikealle, jotta näet työtunnukseen liittyvän myyntitilauksen numeron ja lähetystunnuksen.

### <a name="step-2-set-up-the-execution-flow-for-mobile-devices"></a>Vaihe 2: Suorittamisen työnkulun määrittäminen mobiililaitteille

Mobiililaitteilla suoritettavat tehtävät vaativat käyttäjän syöttämiä tietoja, kuten työtunnusta tai rekisterikilven tunnusta. Kentissä nämä tiedot annetaan varaston käyttäjille yleensä dokumentaatioon, pakkaamiseen tai hyllytykseen liittyvien viivakoodien avulla. Jotta voit viimeistellä tilanteiden mobiililaitevaiheet, varmista, että olet tunnistanut tapahtumien työtunnukset ja tapahtumiin kuuluvien nimikkeen ja sijainnin rekisterikilven tunnukset.

1. Kirjaudu sisään mobiililaitteeseen varaston *51* käyttäjätunnuksella ja salasanalla.
1. Valitse kohta **Lähtevät**.
1. Valitse kohta **Myynnin keräily**.
1. Voit syöttää työtunnuksen tai rekisterikilven tunnuksen. Kirjoita työtunnus ensimmäisen myyntitilauksen yhteyteen ja valitse sitten **Syötä**.
1. Syötä **Sij.**-kenttään sijainti, joka näytetään keräilysijaintia vahvistettaessa. Valitse sitten **Syötä**.
1. Syötä **RK**-kenttään rekisterikilven tunnus. Rekisterikilven tunnuksen on vastattava nimikettä, varastoa ja valitusta sijainnista keräiltävän nimikkeen sijaintia. Kun olet valmis, valitse **Syötä**.
1. Syötä nimikkeen numero **Nimike**-kenttään, vahvista keräiltävä nimike ja valitse **Syötä**.
1. Syötä keräiltävän nimikkeen määrä **Lkm.**-kenttään ja valitse sitten kohta **Syötä**.
1. Syötä **Kohde-RK**-kenttään kohderekisterikilven tunnus. Kohderekisterikilvet ovat käyttäjän määrittämiä. Varmista, että muistat syöttämäsi rekisterikilven tunnuksen. Suosittelemme, että valitset tunnuksen muodoksi nykyisen päivämäärän ja jatkat sitä kahdella numerolla (VVKKPP\#\#), esimerkiksi *19112301*. Kun olet valmis, valitse **Syötä**.
1. Tarkista näytettävät tiedot. Nämä tiedot ovat *Keräily*-tietoja, joista tulee määritystapahtuman *Määritys*-tietoja. Kun olet valmis, valitse **Syötä**.

    - Näyttöön tulee **Työ valmis** -sanoma.

1. Toista vaiheet 4–10 toisen myyntitilauksen työtunnukselle.

Seuraavassa vaiheessa kaksi keräiltyä rekisterikilpeä kuormataan trukkiin.

1. Kirjaudu sisään mobiililaitteeseen varaston *51* käyttäjätunnuksella ja salasanalla.
1. Valitse kohta **Lähtevät**.
1. Valitse kohta **Myynnin kuormaaminen**.
1. Syötä käyttäjän määrittämä kohderekisterikilven tunnus, joka luotiin ensimmäiselle työtunnukselle edellisessä menettelyssä. Valitse sitten kohta **Syötä** ja aseta kohderekisterikilpi **LAVA**-sijaintiin.
1. Syötä kohderekisterikilven tunnus uudelleen ja aseta rekisterikilpi **LASTAUSOVI**-sijaintiin valitsemalla **Syötä**.
1. Toista vaiheet 4–5 toiselle työtunnukselle luomallesi kohderekisterikilven tunnukselle.

Nyt nämä kaksi työtunnusta suljetaan (kuormataan).

### <a name="step-3-confirm-the-outbound-shipment"></a>Vaihe 3: Lähtevän lähetyksen vahvistaminen

Tässä vaiheessa vahvistat kaksi myyntitilausta ja työtä, joiden kuormaus on valmis, lähetät kuorman keräillyt nimikkeet ja luot uuden kuorman keräilemättömille nimikkeille. Lähtevän lähetyksen vahvistus on tehtävä **Kuorman tiedot** -sivulla.

1. Valitse **Varastonhallinta \> Kuormat \> Kuormasuunnittelun työtila**.
1. Valitse **Kuormat**-osan ruudukossa rivi luomallesi kuorman tunnukselle.
1. Valitse kuorman tunnus -linkki ja avaa **Kuorman tiedot** -sivu.
1. Valitse **Kuorman tiedot** -sivun toimintoruudun **Lähetä ja vastaanota** -välilehden **Vahvista**-ryhmässä kohta **Lähtevä lähetys**, jotta vahvistus aloitetaan.
1. Valitse **Lähetyksen vahvistus** -valintaikkunan **Kuormanjakomenetelmä lähetyksen vahvistuksen aikana** -kentässä kohta *Uuteen kuormaan jaettava määrä*.
1. Valitse **OK**.

    Näyttöön saattaa tulla Käsitellään toimintoa -sanoma.

    Näyttöön tulee tietosanomia, joissa ilmoitetaan kuormasi lähetyksen vahvistamisesta ja uuden kuorman luomisesta jaettavalle määrälle.

Päivitä **Kuormasuunnittelun työtila** -sivu, josta näet juuri luodun kuorman.

Voit myös vahvistaa, että tapahtuman suhteet on päivitetty seuraavasti:

- Jäljelle jääneisiin (käsittelemättömiin) lähetyksiin ja lähetysriveihin on päivitetty uuden kuorman tunnus.
- Myyntitilaus on liitetty uuden kuorman tunnukseen.
- Alkuperäisessä kuormassa ei ole jäljelle jääneitä kuormarivejä.
- Jäljelle jääneeseen työhön on päivitetty uuden kuorman tunnus.
- Aalto pysyy samana.
- Uuden kuorman tila on päivitetty oikein. (Jos työn tila on _Kesken_, kuorman tilan on myös oltava _Kesken_.)

## <a name="notes-and-tips"></a>Huomautuksia ja vihjeitä

- Voit myös ottaa käyttöön **Salli kuorman jakaminen lähetyksen vahvistamisen aikana** -parametrin sen jälkeen, kun kuorma on luotu ilman **Kuormamalli**-parametria, mutta ennen kuin kuormausprosessi on alkanut. Siirry haluamaasi kuormaan ja ota parametri käyttöön otsikkonäkymässä.
- **Uuteen kuormaan jaettava määrä** -vaihtoehto toimii myös silloin, kun osa jäljelle jääneistä työn otsikoista on *Kesken*-tilassa. Tämän vuoksi voit käyttää toimintoa, vaikka työntekijät ovat jo aloittaneet tilausten keräilyn.
- Jos valitset kohdan **Peruuta täyttämätön määrä** silloin, kun jäljelle jääneen työn tila on *Auki* tai *Kesken*, näytölle tulee seuraava virhesanoma: Jäljelle jäänyttä kuormamäärää ei voi peruuttaa. Työ on tarkoitettu kuormalle.
- Jos valitset kohdan **Peruuta täyttämätön määrä** silloin, kun jäljelle jäänyttä työtä ei ole, mutta kuormassa on vapauttamattomia kuormarivejä, näytölle tulee seuraava virhesanoma: Kuorman lähetystä ei voitu vahvistaa, koska nimikkeen määrä ylittää alitoimitukselle määritetyn prosenttiosuuden. Voit välttää tämän virhesanoman asettamalla vapauttamattoman kuormarivin **Alitoimitus**-prosenttiosuuden 100 prosenttiin. Vapauttamattomia rivejä ei siirretä uuteen kuormaan, mutta nykyinen kuorma vahvistetaan alitoimituksen yhteydessä. Tällöin et voi vapauttaa alkuperäistä tilausta uudelleen. Siksi sinun on hoidettava se jollakin muulla tavalla.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]