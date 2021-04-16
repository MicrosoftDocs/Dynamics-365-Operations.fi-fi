---
title: Vyöhykkeen rajatäydennys
description: Vyöhykkeeseen perustuva täydennys käyttää minimi/maksimi (min/max) täydennysstrategiaa, mutta se arvioi koko varastovyöhykkeet yksittäisten sijaintien sijaan. Tämän vuoksi varastopäälliköt voivat oppia nopeammin, kun poimintavyöhykkeellä tarvitaan lisävarastoa.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d0a97ed7b01a32e9276433713448a672f83f7d02
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814365"
---
# <a name="zone-threshold-replenishment"></a>Vyöhykkeen rajatäydennys

[!include [banner](../includes/banner.md)]

Vyöhykkeeseen perustuva täydennys käyttää minimi/maksimi (min/max) [täydennys](replenishment.md)-strategiaa, mutta se arvioi koko varastovyöhykkeet yksittäisten sijaintien sijaan. Tämän vuoksi varastopäälliköt voivat oppia nopeammin, kun poimintavyöhykkeellä tarvitaan lisävarastoa.

Tämän ominaisuuden määritys muistuttaa sijaintiin perustuvan täydennyksen asetuksia. Kun määrität mallin min.-/max.-täydennykseen, voit myös määrittää, lasketaanko raja-arvo sijaintia vai vyöhykettä kohden. Jos määrität vyöhykkeisiin perustuvan arvioinnin, vyöhykkeen valintakyselyyn on lisättävä tietyt vyöhykkeet.

Kuten sijaintiin perustuva min.-/max.-täydennys, vyöhykkeeseen perustuva min-/max-täydennys perustuu varaston vähimmäiskynnyksen määritykseen, joka käynnistää valittujen nimikkeiden täydennystöiden luomisen. Tämä täydennystyö kasvattaa varastoa määritetyn vyöhykkeen enimmäisrajan mukaan.

> [!NOTE]
> Nykyisessä versiossa ei tueta tuotevariantin vyöhykkeen täydennysprosesseja.


Toisin kuin sijaintiin perustuvaa min.-/max.-täydennystä, vyöhykkeeseen perustuva min.-/max.-täydennys ei vaadi varastopaikkoja arvioimaan, pitäisikö sijaintien tallentaa tietty nimike. Tämän vuoksi aluevyöhykkeeseen perustuvassa täydennyksessä voit käyttää min.-/max.-täydennystä, vaikka sinulla ei olisikaan varastossa kunkin nimikkeen tai nimikevariantin varastopaikkoja. Kun vyöhykkeen määrä alittaa määritetyn minimirajan, täydennystyö luodaan. Sijaintidirektiivien avulla määritetään, mihin tiettyyn sijaintiin varasto tulisi ottaa.

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a>Vyöhykeraja-arvon täydennysominaisuuden käyttöönotto

Ennen kuin voit käyttää *Vyöhykeraja-arvon täydennys* -toimintoa, sen pitää olla otettu käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Vyöhykeraja-arvon täydennys*

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a>Aseta vyöhykkeeseen perustuva täydennys

Jos haluat määrittää vyöhykkeeseen perustuvan täydennyksen, sinun on konfiguroitava useita järjestelmän osia. Tässä osassa esitellään eri asetukset ja annetaan demoarvot, jotka voit määrittää, jos haluat käsitellä tämän ohjeaiheen lopussa olevaa skenaariota.

### <a name="set-up-directive-codes"></a>Määritä direktiivikoodit

[Direktiivikoodien](control-warehouse-location-directives.md) avulla voit olla tarkempi, kun määrität työmallissa käytettävän sijaintimallin. Kukin koodi muodostaa yhteisen arvon, johon voit viitata, kun määrität kutakin mallityyppiä.

#### <a name="view-and-edit-directive-codes"></a>Direktiivikoodien tarkasteleminen ja muokkaaminen

Jos haluat tarkastella tai muokata direktiivikoodeja, siirry kohtaan **Varaston hallinta \> Määritys \> Direktiivikoodit**.

#### <a name="prepare-demo-data-directive-codes"></a>Demotietodirektiivin koodien valmisteleminen

Tässä esimerkissä kuvataan, miten direktiivikoodi valmistellaan. Jos aiot käsitellä tämän ohjeaiheen lopussa olevaa skenaariota, käytä tässä annettuja demoarvoja. Muussa tapauksessa käytä omia arvoja.

1. Valitse **USMF**-yritys, joka käyttää demotietoja.
1. Valitse **Varastonhallinta \> Asetukset \> Direktiivikoodit**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.
1. Aseta uudelle riville seuraavat arvot:

    - **Direktiivikoodi:** _Vyöhykkeen täyd_
    - **Direktiivin kuvaus:** _Vyöhykkeen täydennys_

1. Tallenna uusi koodi valitsemalla **Tallenna**.

### <a name="set-up-replenishment-templates"></a>Määritä täydennysmallit

[Vähimmäis- tai enimmäistäydennysmallit](tasks/set-up-min-max-replenishment-process.md) ovat ensisijainen mekanismi optimaalisten tasojen ylläpitämiseksi poimintasijainneissa. Näissä malleissa on määritettävä säännöt, joita käytetään varaston täydentämiseen varastossa. Täydennys, johon malleja voidaan käyttää, sisältää vyöhykkeeseen perustuvan täydennyksen.

#### <a name="view-and-edit-replenishment-templates"></a>Tarkastele ja muokkaa täydennysmalleja

Täydennysmalli on sääntöjoukko, joka määrittää, milloin ja miten sijaintia täydennetään. Voit valita mallin, jolla ohjataan, milloin ja miten täydennys tehdään. Siirry kohtaan **Varastonhallinta \> Asetukset \> Täydennys \> Täydennysmallit** tarkastellaksesi tai muokataksesi täydennysmallejasi.

#### <a name="prepare-a-demo-data-replenishment-template"></a>Demotietojen täydennysmallin valmisteleminen

Tässä esimerkissä kuvataan, miten täydennysmalli valmistellaan. Jos aiot käsitellä tämän ohjeaiheen lopussa olevaa skenaariota, käytä tässä annettuja demoarvoja. Muussa tapauksessa käytä omia arvoja.

1. Valitse **USMF**-yritys, joka käyttää demotietoja.
1. Valitse **Varastonhallinta \> Asetukset \> Täydennys \> Täydennysmallit**.
1. Valitse **Muokkaa**, jotta saat sivun muokkaustilaan.
1. Lisää **Yleiskatsaus**-ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.
1. Aseta uudelle riville seuraavat arvot. Hyväksy oletusarvot kaikille muille kentille.

    - **Täydennysmalli:** _Vyöhyke min./max. täyd_
    - **Kuvaus:** _Vyöhykkeen min./max. täydennys_
    - **Täydennystyyppi:** _Vähimmäis- tai enimmäisarvo_

1. Valitse **Tallenna**.
1. Kun uusi rivi on yhä valittuna **Yhteenveto**-ruudukossa, lisää juuri luomaasi *Vyöhyke min.-/max. täyd.*-täydennysmalli valitsemalla **Täydennysmallin tiedot**-ruudukon yläpuolella oleva **Uusi**-valintaruutu.
1. Aseta uudelle riville seuraavat arvot:

    - **Järjestysnumero:** Syötä _1_.
    - **Kuvaus:** Syötä _Poimintavyöhykkeen täydennys_.
    - **Täydennysyksikkö:** Valitse _kpl_.
    - **Pyyntötyyppi:** Jätä tämä kenttä tyhjäksi.
    - **Direktiivikoodi:** Tämä kenttä linkittää täydennysmallin sijaintidirektiiviin. Valitse aiemmin luomasi demotietodirektiivin koodi (_Vyöhyketäyd._).
    - **Työmalli:** Jätä tämä kenttä tyhjäksi.
    - **Minimimäärä:** Tämä kenttä määrittää määrän, jonka täydennys käynnistyy. Syötä _50_.
    - **Enimmäismäärä:** Tämä kenttä määrittää nimikkeen enimmäismäärän, joka voidaan esittää vyöhykkeessä. Luotu täydennystyö lisää varaston määrää tähän määrään. Syötä _150_.
    - **Yksikkö:** Tässä kentässä määritetään vähimmäis- ja enimmäisarvojen yksikkö. Valitse _kpl_.
    - **Kysynnän lisäys:** Valitse _Pyöristä ylöspäin_.
    - **Täydennä tyhjät kiinteät sijainnit:** Valitse tämä valintaruutu.
    - **Täydennä vain kiinteät sijainnit:** Tyhjennä tämä valintaruutu.
    - **Tuotekyselytila:** Valitse _tuotekysely_.
    - **Täydennyksen raja-alue:** Tässä kentässä määritetään, arvioiko malli alueen vai määritetyn sijainnin mukaan. Valitse _Vyöhyke_.
    - **Varasto:** Valitse _61_.

1. Valitse **Täydennysmallin tiedot** -ruudukon yläpuolelta **Valitse tuotteet**.
1. Lisää ruudukkoon rivi valitsemalla **Tuotekysely**-valintaruudun **Alue**-välilehdessä **Lisää**.
1. Aseta uudelle riville seuraavat arvot:

    - **Taulukko:** _Nimikkeet_
    - **Johdettu taulu:** _Nimikkeet_
    - **Kenttä:** _Nimiketunnus_
    - **Kriteerit:** _A0001_

1. Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.
1. Valitse **Täydennysmallin tiedot** -ruudukon yläpuolelta **Valitse täydennettävät vyöhykkeet**.
1. Lisää ruudukkoon rivi **Vyöhykekysely** -valintaruudun **Alue**-välilehdessä.
1. Aseta uudelle riville seuraavat arvot:

    - **Taulu:** _Varastovyöhyke_
    - **Johdettu taulu:** _Varastovyöhyke_
    - **Kenttä:** _Alueen tunnus_
    - **Kriteerit:** _LATTIA_

1. Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.

### <a name="set-up-location-directives"></a>Määritä sijaintidirektiivit

Toisin kuin sijaintiin perustuva min.-/max.-täydennys, vyöhykkeisiin perustuva min./max.-täydennys edellyttää, että määrität sekä keräilysijaintidirektiivit että varastopaikkadirektiivit, koska järjestelmä laskee koko vyöhykkeen sen sijaan, että se olisi vain lähtevien töiden poimintasijainti.

#### <a name="view-and-edit-location-directives"></a>Sijaintidirektiivien tarkasteleminen ja muokkaaminen

Jos haluat tarkastella tai muokata sijaintidirektiivejä, siirry kohtaan **Varaston hallinta \> Määritys \> Sijaintidirektiivit**.

Seuraavassa osassa on esimerkkejä siitä, miten voit luoda tarvittavat poimintasijaintidirektiivit ja sijoittaa sijaintidirektiivejä asetusten avulla.

#### <a name="prepare-demo-data-location-directives"></a>Demotietosijaintidirektiivien valmisteleminen

Jos haluat valmistella demotietoja, jotta sitä voidaan käyttää tämän ohjeaiheen lopussa olevassa skenaariossa, sinun on luotava kaksi sijaintidirektiiviä: yksi poimintaa ja yksi hyllytystä varten.

##### <a name="create-a-replenishment-pick-directive"></a>Luo täydennyspoimintadirektiivi

1. Valitse **USMF**-yritys, joka käyttää demotietoja.
1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Aseta vasemmassa ruudussa **Työtilaustyyppi**-kentän arvoksi _Täydennys_.
1. Valitse toimintoruudussa **Uusi** luodaksesi uuden direktiivin.
1. Määritä seuraavat arvot:

    - **Järjestysnumero:** Hyväksy oletusarvo.
    - **Nimi:** Syötä _vyöhykkeen poiminta_.
    - **Työtyyppi:** Valitse _Poiminta_.
    - **Toimipaikka:** Valitse _6_.
    - **Varasto:** Valitse _61_.
    - **Direktiivikoodi:** Jätä tämä kenttä tyhjäksi.
    - **Useita varastointiyksiköitä:** Määritä tämän vaihtoehdon arvoksi _Ei_.

1. Valitse **Tallenna**, jos haluat luoda direktiivin, jossa on tähän mennessä määritetyt asetukset.
1. Lisää uusi rivi ruudukkoon **Rivit**-pikavälilehdessä **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **Järjestysnumero:** Syötä _1_.
    - **Määrästä:** Syötä _0_.
    - **Määrään:** Syötä _10000000_.
    - **Yksikkö:** Jätä tämä kenttä tyhjäksi.
    - **Etsi määrä:** Valitse _ei mitään_.
    - **Rajoita yksikön mukaan:** Tyhjennä tämä valintaruutu.
    - **Pyöristä ylös yksikköön:** Tyhjennä tämä valintaruutu.
    - **Etsi pakkausmäärä:** Tyhjennä tämä valintaruutu.
    - **Salli jakaminen:** Valitse tämä valintaruutu.

1. Tallenna uusi rivi valitsemalla **Tallenna**.
1. Kun uusi rivi on edelleen valittuna **Rivit**-ruudukossa, lisää rivi ruudukkoon valitsemalla **Sijaintidirektiivin toimenpiteet** -pikavälilehdessä **Uusi**.
1. Aseta uudelle riville seuraavat arvot:

    - **Järjestysnumero:** Syötä _1_.
    - **Nimi:** Syötä _Poiminta bulkkina_.
    - **Kiinteän sijainnin käyttö:** Valitse _Kiinteät ja muut kuin kiinteät sijainnit_.
    - **Salli negatiivinen varasto:** Tyhjennä tämä valintaruutu.
    - **Erä käytössä:** Tyhjennä tämä valinta ruutu.
    - **Strategia:** Valitse _Ei mitään_.

1. Tallenna uusi toiminto valitsemalla **Tallenna**.
1. Kun uusi toiminto on edelleen valittuna, valitse **Sijaintidirektiivin toiminnot** -ruudukon yläpuolella oleva **Muokkaa kyselyä**.
1. Näyttöön tulee kyselyvalintaikkuna, jossa voit valita varastopaikat, joita haluat täydentää. Valitse **Alue**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin ruudukkoon.
1. Aseta uudelle riville seuraavat arvot:

    - **Taulu:** _Sijainnit_
    - **Johdettu taulu:** _Sijainnit_
    - **Kenttä:** _Alueen tunnus_
    - **Kriteerit:** _BULK_

1. Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.
1. Tallenna sijaintidirektiivi valitsemalla **Tallenna**.

##### <a name="create-a-replenishment-put-directive"></a>Luo täydennyshyllytysdirektiivi

1. Varmista **Sijaintidirektiivit**-sivun vasemmasta ruudusta, että **Työtilauksen tyyppi** -kentän arvoksi on edelleen määritetty _Täydennys_.
1. Valitse toimintoruudussa **Uusi** luodaksesi toisen uuden direktiivin.
1. Määritä seuraavat arvot:

    - **Järjestysnumero:** Hyväksy oletusarvo.
    - **Nimi:** Syötä _vyöhykkeen hyllytys_.
    - **Työtilauksen tyyppi:** Valitse _Hyllytys_.
    - **Toimipaikka:** Valitse _6_.
    - **Varasto:** Valitse _61_.
    - **Direktiivin koodi:** Valitse _Vyöhykkeen täyd_, jos haluat linkittää tämän sijaintidirektiivin aiemmin luomaasi täydennysmalliin käyttämällä aiemmin luomaasi koodia.
    - **Useita varastointiyksiköitä:** Määritä tämän vaihtoehdon arvoksi _Ei_.

1. Valitse **Tallenna**, jos haluat luoda direktiivin, jossa on tähän mennessä määritetyt asetukset.
1. Lisää uusi rivi ruudukkoon **Rivit**-pikavälilehdessä **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **Järjestysnumero:** Syötä _1_.
    - **Määrästä:** Syötä _0_.
    - **Määrään:** Syötä _10000000_.
    - **Yksikkö:** Jätä tämä kenttä tyhjäksi.
    - **Etsi määrä:** Valitse _ei mitään_.
    - **Rajoita yksikön mukaan:** Tyhjennä tämä valintaruutu.
    - **Pyöristä ylös yksikköön:** Tyhjennä tämä valintaruutu.
    - **Etsi pakkausmäärä:** Tyhjennä tämä valintaruutu.
    - **Salli jakaminen:** Valitse tämä valintaruutu.

1. Tallenna uusi rivi valitsemalla **Tallenna**.
1. Kun uusi rivi on edelleen valittuna **Rivit**-ruudukossa, lisää rivi ruudukkoon valitsemalla **Sijaintidirektiivin toimenpiteet** -pikavälilehdessä **Uusi**.
1. Aseta uudelle riville seuraavat arvot:

    - **Järjestysnumero:** Syötä _1_.
    - **Nimi:** Syötä _vyöhykkeen hyllytys_.
    - **Kiinteän sijainnin käyttö:** Valitse _Kiinteät ja muut kuin kiinteät sijainnit_.
    - **Salli negatiivinen varasto:** Tyhjennä tämä valintaruutu.
    - **Erä käytössä:** Tyhjennä tämä valinta ruutu.
    - **Strategia:** Valitse _Konsolidoi_.

1. Tallenna uusi toiminto valitsemalla **Tallenna**.
1. Kun uusi toiminto on edelleen valittuna, valitse **Sijaintidirektiivin toiminnot** -ruudukon yläpuolella oleva **Muokkaa kyselyä**.
1. Näyttöön tulee kyselyvalintaikkuna, jossa voit valita vyöhykkeet, joita haluat täydentää. Tämän vyöhykkeen tulee olla sama alue, joka on määritetty täydennysmallissa. Valitse **Alue**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin ruudukkoon.
1. Aseta uudelle riville seuraavat arvot:

    - **Taulu:** _Sijainnit_
    - **Johdettu taulu:** _Sijainnit_
    - **Kenttä:** _Alueen tunnus_
    - **Kriteerit:** _LATTIA_

1. Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.
1. Tallenna sijaintidirektiivi valitsemalla **Tallenna**.

## <a name="scenario"></a>Skenaario

Tässä osassa on esimerkkiskenaario, jossa kerrotaan, kuinka toimintoa käytetään.

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a>Esimerkkiskenaarion mukaisten esimerkkiskenaarioiden valmisteleminen

Ennen kuin aloitat skenaarion käsittelyn, sinun on aktivoitava mallitiedot ja määritettävä ominaisuus tässä osassa ja aiemmissa tämän ohjeaiheen osissa kuvatulla tavalla.

#### <a name="use-the-usmf-legal-entity"></a>Käytä USFM-yritystä

Tämän skenaarion käyttäminen määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.

#### <a name="prepare-additional-sample-data"></a>Lisä mallitietojen valmisteleminen

Kun olet valinnut **USMF**-yrityksen, lisää tarvittavat näytetiedot, jotka on kuvattu aiemmin tämän ohjeaiheen kohdassa [Määritä vyöhykkeeseen perustuva täydennys](#setup) -osa.

#### <a name="check-your-on-hand-inventory"></a>Tarkista käytettävissä olevat varastosi

Seuraavien vaiheiden avulla voit varmistaa, että järjestelmä sisältää riittävän varaston, joka tukee esimerkkiskenaariota.

1. Varmista, että nimike *A0001* on käytettävissä oleva varasto kahdessa eri paikassa täydennysmallissa määritetyssä poimintavyöhykkeessä (*LATTIA*). Kokonaisvaraston on kuitenkin oltava pienempi kuin vaadittu vähimmäismäärä (*50*), joka on määritetty täydennysmallissa. Näin voit simuloida, miten laskeminen tapahtuu koko vyöhykkeelle yhden ainoan sijainnin asemesta. **Voit muuttaa varastoa tarpeen mukaan käyttämällä mitä tahansa varastoprosessia.**
1. Varmista, että nimikkeelle *A0001* on riittävästi varastoa varastopaikan keräilysijaintidirektiivissä määritetyssä bulkkisijainnissa, jossa täydennystyön tulisi poimia nimikkeet vyöhykkeen tunnuksesta *BULKKI*. Kokonaisvaraston on oltava suurempi kuin vaadittu enimmäismäärä (*150*), joka on määritetty täydennysmallissa.
1. Valinnainen mutta suositeltava: Luo varaston oikaisukirjauskansio noudattamalla seuraavia ohjeita:

    1. Valitse **Varastonhallinta \> Kirjauskansioviennit \> Nimikkeet \> Varaston oikaisu**.
    1. Valitse **Uusi**.
    1. Valitse **Luo varastokirjauskansio** -valintaikkunan **Varasto**-kentässä *61*.
    1. Valitse **OK**.
    1. Lisää ruudukkoon kolme riviä käyttämällä **Uusi**-painiketta **Kirjauskansion rivit**-pikavälilehdessä ja määritä seuraavat arvot. Kun olet määrittänyt jokaisen rivin, valitse **Tallenna**.

        - **Rivi 1:**

            - **Nimiketunnus:** *A0001*
            - **Toimipaikka:** *6*
            - **Varasto**: *61*
            - **Sijainti:** *02A01R1S1B*
            - **Rekisterikilpi:** Valitse luettelosta aiemmin luotu rekisterikilpi tai luo uusi rekisterikilpi.
            - **Määrä** *1000*

        - **Rivi 2:**

            - **Nimiketunnus:** *A0001*
            - **Toimipaikka:** *6*
            - **Varasto**: *61*
            - **Sijainti:** *07A01R2S1B*
            - **Rekisterikilpi:** Valitse luettelosta aiemmin luotu rekisterikilpi tai luo uusi rekisterikilpi.
            - **Määrä** *15*

        - **Rivi 3:**

            - **Nimiketunnus:** *A0001*
            - **Toimipaikka:** *6*
            - **Varasto**: *61*
            - **Sijainti:** *07A01R1S1B*
            - **Rekisterikilpi:** Valitse luettelosta aiemmin luotu rekisterikilpi tai luo uusi rekisterikilpi.
            - **Määrä** *10*

    1. Valitse toimintoruudussa **Validoi**. Voit korjata mahdolliset virheet, jotka löytyvät ennen seuraavaan vaiheeseen siirtymistä.
    1. Vahvista varaston kirjaus valitsemalla toimintoruudussa **Kirjaa**.

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a>Esimerkkiskenaario: Suorita vyöhykkeeseen perustuva min.-/max.-täydennys

Kun kaikki vaaditut mallitiedot on luotu, voit käynnistää täydennyksen noudattamalla näitä ohjeita.

1. Valitse **Varastonhallinta \> Täydennys \> Täydennykset**.
1. Avaa **Täydennys**-valintaikkuna valitsemalla **Sisällytettävät tietueet** -pikavälilehdessä **Suodatus**.
1. Muokkaa oletustaulukon riviä **Kysely**-valintaikkunan **Alue**-välilehdessä seuraavalla tavalla:

    - **Taulu:** Valitse _Täydennysmallit_.
    - **Johdettu taulu:** Valitse _Täydennysmallit_.
    - **Kenttä:** Valitse _Täydennysmalli_.
    - **Ehdot:** Valitse _Vyöhykkeen min./max. täyd_. Tämä täydennysmalli on täydennysmalli, jonka loit tämän skenaarion demotietojen valmistelun aikana.

1. Tallenna kysely ja palaa **Täydennys**-valintaikkunaan valitsemalla **OK**.
1. Suorita täydennysmalli valitsemalla **OK**.

Täydennystyöt luodaan nyt, kun varasto kerätään *BULKKI*-vyöhykkeestä ja se lisätään *LATTIA*-vyöhykkeeseen.

## <a name="notes-and-tips"></a>Huomautuksia ja vihjeitä

Seuraavassa on muutamia huomautuksia ja vihjeitä toiminnon käyttämisestä:

- Jos haluat määrittää täydennystyöt, jotka menevät haluamallesi vyöhykkeelle, voit linkittää täydennysmallin rivit ja sijaintidirektiivit jommallakummalla seuraavista tavoista:

    - Muokkaa sijaintidirektiivin otsikkokyselyä ja suodata valittuja täydennysmallin rivejä.
    - Käytä täydennysmallirivillä direktiivikoodia ja vastaa sitä hyllytyssijaintidirektiiviin.

- Jos käytät dynaamisia sijainteja, täydennystyöt luodaan joko ensimmäiselle käytettävissä olevalle sijainnille tai sijainnille, joissa on jo varasto, jos sijaintidirektiivitoimenpide on määritetty käyttämään **Konsolidoi**-strategiaa.
- Jos käytät paikkoja, joissa käytetään vyöhykkeitä, käytä [normaalia min.-/max.-täydennystä](tasks/set-up-min-max-replenishment-process.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]