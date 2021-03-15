---
title: Varastopaikoitus
description: Tässä ohjeaiheessa on tietoja varastopaikoitusta. Varastopaikoituksen avulla voit konsolidoida kysynnän nimikkeen ja mittayksikön mukaan tilauksista, joiden tila on tilattu, varattu tai vapautettu. Sen avulla varastopäälliköt voivat suunnitella poimintasijainnit älykkäästi, ennen kuin ne vapauttavat tilauksia varastoon ja luovat poimintatöitä.
author: mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fb39daba393944471ee5d412b1eb61754843926f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993750"
---
# <a name="warehouse-slotting"></a>Varastopaikoitus

[!include [banner](../includes/banner.md)]

Käytettävissä on useita varastopaikoitustoimintoja, joiden avulla varastopäälliköt voivat suunnitella poimintasijainnit älykkäästi, ennen kuin he vapauttavat tilauksia varastoon ja luovat poimintatöitä.

*Varastopaikoitustoiminnon* avulla voit konsolidoida kysynnän nimikkeen ja mittayksikön mukaan tilauksista, joiden tila on *tilattu*, *varattu* tai *vapautettu*. Luotua kysyntää voidaan sitten käyttää poimintaan käytettäviin paikkoihin määrän, yksikön, fyysisten dimensioiden, pysyvien sijaintien ja muiden perusteella. Kun poistosuunnitelma on luotu, voidaan luoda täydennystöitä, jotka tuovat sopivan määrän varastoa kuhunkin sijaintiin.

*Siirtotilausten varastopaikoitustoiminnon* avulla varastopäälliköt voivat täydentää keräilysijainteja sellaisten siirtotilausten kysynnän perusteella, joita ei ole vielä vapautettu varastoon. Se varmistaa, että keräilysijainnit sisältävät kaikki nimikkeet, joita tarvitaan siirtotilauksissa, kun ne vapautetaan varastoon. Tämä toiminto edellyttää, että myös *varastopaikoitustoiminto* otetaan käyttöön.

*Varastopaikoituksen kohdistuksen parannustoiminto* lisää asetuksen malliriveille, joita *varaston paikoitustoiminto* käyttää. Tämän asetuksen ansiosta järjestelmä voi ottaa nykyisen käytettävissä olevan varaston huomioon kohdesijainnissa. Tällä tavoin paikoitukselle luodaan ehkä vähemmän täydennyksiä. *Varastopaikoituksen kohdistuksen parannustoiminto* edellyttää, että myös *varaston paikoitustoiminto* otetaan käyttöön. Sitä voidaan valinnaisesti käyttää yhdessä *siirtotilausten varastopaikoitustoiminnon* kanssa.

## <a name="turn-on-the-warehouse-slotting-features"></a>Varastopaikoitustoimintojen ottaminen käyttöön

Nämä toiminnot otettava käyttöön järjestelmässä, ennen kuin niitä voidaan käyttää. Järjestelmänvalvojat voivat tarkistaa näiden toimintojen tilan ja ottaa ne tarvittaessa käyttöön [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksissa. Ota seuraavat toiminnot käyttöön tarpeen mukaan:

- Varaston osastointiominaisuus
- Siirtotilausten varastopaikoitus

    > [!IMPORTANT]
    > *Varastopaikoitustoiminto* on otettava käyttöön ennen tätä toimintoa.

- Varastopaikoituksen kohdistuksen parannukset

    > [!IMPORTANT]
    > *Varastopaikoitustoiminto* on otettava käyttöön ennen tätä toimintoa.

## <a name="set-up-warehouse-slotting"></a>Varastopaikoituksen käyttöönotto

Varastopaikoitusta voi käyttää sen jälkeen, kun seuraavat elementit on määritetty järjestelmässä:

- Paikoituksen mittayksikkötasot
- Direktiivikoodit
- Paikoitusmallit
- Sijaintidirektiivit

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a>Mittayksikön määrittämistasojen luominen paikoitusta varten

Mittayksikön yksiköt mahdollistavat useiden mittayksiköiden ryhmittelyn paikoitusta varten. Jos esimerkiksi saman ruudun poiminta-alueelta poimitaan useita ruutuja, kullekin koolle voidaan määrittää yksi taso. **Kullekin tasoyksikölle on luotava rivi jokaista mittayksikköä varten.**

1. Siirry kohtaan **Varaston hallinta \> Asetukset \> Täydennys \> Paikoituksen mittayksikkö tasot**.
1. Valitse **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Mittayksikön taso:** *EaBoxPl*
    - **Kuvaus:** *Jokainen laatikkokuormalava*

1. Valitse **Tallenna**.
1. Lisää uusi rivi ruudukkoon **Mittayksiköt**-pikavälilehdessä **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **Yksikkö:** *Laatikko*
    - **Kuvaus:** Jätä tämä kenttä tyhjäksi. Se täytetään automaattisesti, kun tallennat muutokset.
    - **Yksikköluokka:** *Määrä*

1. Valitse **Uusi** lisätäksesi toisen rivin ruudukkoon.
1. Määritä uudelle riville seuraavat arvot:

    - **Yksikkö:** *ea*
    - **Kuvaus:** Jätä tämä kenttä tyhjäksi. Se täytetään automaattisesti, kun tallennat muutokset.
    - **Yksikköluokka:** *Määrä*

1. Valitse **Uusi** lisätäksesi kolmannen rivin ruudukkoon.
1. Määritä uudelle riville seuraavat arvot:

    - **Yksikkö:** *PL*
    - **Kuvaus:** Jätä tämä kenttä tyhjäksi. Se täytetään automaattisesti, kun tallennat muutokset.
    - **Yksikköluokka:** *Määrä*

1. Tallenna taso valitsemalla **Tallenna**.

### <a name="create-a-directive-code-for-slotting"></a>Direktiivikoodin luominen paikoitusta varten

Sinun on valittava malliin liitettävä direktiivikoodi.

1. Valitse **Varastonhallinta \> Asetukset \> Direktiivikoodit**.
1. Valitse toimintoruudussa **Uusi**.
1. Syötä **Direktiivikoodi**-kenttään koodi *Paikoitus*.
1. Syötä **Direktiivin kuvaus** -kenttään koodi *Paikoitus*.

### <a name="set-up-slotting-templates"></a>Paikoituksen mallien käyttöönotto

Kukin paikoitusmalli määrittää, miten varasto määritetään tietyn varaston sijainteihin. Jokaisessa mallissa on oltava rivi kutakin paikoitusmääritystä varten. Tämän osan ohjeiden avulla voit määrittää paikoitusmallien asetukset.

1. Valitse **Varastonhallinta \> Asetukset \> Täydennys \> Paikotusmallit**.
1. Luo malli valitsemalla **Uusi**.

Seuraavaksi on määritettävä mallin ylätunniste, paikoitusmäärittelyt ja paikkadirektiivit, jotka on selitetty seuraavissa alikohdissa. Siirtotilausten paikoituksen määritys muistuttaa myyntitilausten paikoituksen määritystä, mutta **Kysyntätyyppi**-kentän asetus on *Siirtotilaukset* eikä *Myyntilaus*.

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a>Myyntitilauksen paikoitusmallin otsikon määrittäminen

1. Määritä mallin otsikossa seuraavat arvot:

    - **Paikoitusmalli:** _61_
    - **Kuvaus:** _61_
    - **Kysyntätyyppi:** *Myyntitilaus*

        > [!NOTE]
        > Tällä *myyntitilaukset* ja *siirtotilaukset* ovat ainoat tuetut kysyntätyypit. Voit valita *Siirtotilaukset* vain, jos *Siirtotilausten varastopaikoitus* -toiminto on otettu käyttöön.

    - **Kysyntästrategia:** _Tilattu_

        Tässä kentässä käytettävissä ovat seuraavat arvot:

        - **Tilattu** – Myyntitilauksen koko tilatun määrän pitää olla tarpeen.
        - **Varattu** – Ainoastaan ne myyntitilausrivin määrät, jotka on varattu (fyysinen ja tilattu), pitää vaatia.
        - **Vapautettu** – vapautettua määrää on pidettävä kysyntänä.

    - **Varasto**: _61_
    - **Salli aaltokysynnän käyttää varauksettoman määrän:** _Kyllä_

Voit myös määrittää kyselyn, joka rajaa arvioitavan kysynnän laajuuden.

#### <a name="set-up-slotting-specifications-for-each-template"></a>Määritä paikoitusmääritykset kullekin mallille

Voit lisätä kullekin luotavalle myyntitilausmallille rivin kutakin paikoitusmääritystä varten seuraavasti.

1. Lisää uusi mallirivi valitsemalla **Paikoitusmallin tiedot** -pikavälilehdessä **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **Järjestys:** _1_
    - **Kuvaus:** _Kiinteä sijainti_
    - **Vähimmäismäärä:** _1_

        Tämä kenttä määrittää riville vaaditun kysynnän vähimmäismäärän.

    - **Enimmäismäärä** _1000000_

        Tämä kenttä määrittää riville kelvollisen kysynnän enimmäismäärän.

    - **Yksikkö:** Jätä tämä kenttä tyhjäksi.

        Tämä kenttä määrittää mittayksikön, johon vähimmäis- ja enimmäismäärät viittaavat.

    - **Mittayksikön taso:** _EaBoxPl_

        Tämä kenttä määrittää riville kelvolliset kysynnän mittayksiköt. (Lisätietoja on aiemmin tässä ohjeaiheessa olevassa [Määritä paikoituksen mittayksikön tasot](#unit-tiers) -osassa.)

    - **Määritä paikan kriteerit:** _Harkitse määrä_

        Tässä kentässä käytettävissä ovat seuraavat arvot:

        - **Oletetaan tyhjäksi** – Järjestelmä olettaa, että kaikki poiminta-alueen sijainnit ovat tyhjiä, eikä niiden pitäisi tarkistaa varastopaikkoja.
        - **Tarkastele määrää** – Järjestelmän tulisi tarkistaa poiminta-alueen sijainnit varaston varalta ja sen tulisi ohittaa ne sijainnit, jotka eivät ole tyhjiä.
        - **Ota varastosaldo huomioon** – Järjestelmän on tarkistettava, onko missään kohdesijainnissa varaamattomia määriä kysyntärivin nimikettä. Jos määrä on riittävän suuri tyydyttämään aikakin yhden kysyntärivin yksikön, käytettävissä oleva määrä vähennetään luodusta paikoitussuunnitelmatietueesta. Jos kysyntä on esimerkiksi 10 laatikkoa ja varastosaldo on yksi laatikko, etsittävä kysyntä on yhdeksän laatikkoa. Jos kysyntä on 10 laatikkoa ja varastosaldo on yksi kutakin, etsittävä kysyntä on 10 laatikkoa. Tämä arvo on käytettävissä vain, kun *Varastopaikoituksen kohdistuksen parannukset* -toiminto on otettu käyttöön.

    - **Direktiivikoodi:** _Paikoitus_

        Tämä kenttä määrittää sijaintidirektiivin, jota käytetään täydennystyön poimintasijainnin etsimiseen.

    - **Ylivuotosijainti:** Jätä tämä kenttä tyhjäksi.

        Tämä kenttä määrittää sijainnin, johon varasto kohdistetaan, jos määrälle ei löydy sijaintia rivin käsittelyn yhteydessä.

    - **Salli päästää ylös:** _Kyllä_

        Kun tämän vaihtoehdon arvoksi on asetettu *Kyllä*, jos mitään kysyntää ei voi paikoittaa, siirtotyöt luodaan, jotta voidaan ottaa varasto pois sijainneista, joissa on varasto, mutta joissa mitään ei paikoitettu. Malli suoritetaan sitten uudelleen. Tällä kertaa se ohittaa sijaintien varaston. Tämä toiminto toimii parhaiten, kun **Määritä lähtöpaikkakriteerit** -kentän arvoksi on määritetty _Harkitse määrä_.

    - **Kiinteän sijainnin käyttö:** _Vain tuotteen kiinteät sijainnit_

        Tässä kentässä käytettävissä ovat seuraavat arvot:

        - **Kiinteät ja ei-vahvistetut sijainnit** – Järjestelmä ei saa rajoittua käyttämään vain kiinteitä sijainteja.
        - **Vain tuotteen kiinteät sijainnit** – Järjestelmän tulisi paikoittaa vain sellaisia sijainteja, jotka ovat tuotteen kiinteitä sijainteja.
        - **Vain tuotevariantin kiinteät sijainnit** – Järjestelmän tulisi paikoittaa vain sellaisia sijainteja, jotka ovat tuotevariantin kiinteitä sijainteja.

> [!NOTE]
> Jos paikoitusmallissa on ainakin yksi rivi, jossa **Määritä paikan ehdot** -kentän asetuksena on *Ota varastosaldo huomioon*, helpotuksia ei enää sallita millään mallin rivillä.

1. Valitse **Tallenna**.
1. Luo toinen mallirivi valitsemalla **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **Järjestys:** _2_
    - **Kuvaus:** _Muut_
    - **Vähimmäismäärä:** _1_
    - **Enimmäismäärä:** _1000000_
    - **Yksikkö:** Jätä tämä kenttä tyhjäksi.
    - **Mittayksikön taso:** _EaBoxPl_
    - **Määritä paikan kriteerit:** _Harkitse määrä_
    - **Direktiivikoodi:** _Paikoitus_
    - **Ylivuotosijainti:** Jätä tämä kenttä tyhjäksi.
    - **Salli päästää ylös:** _Kyllä_
    - **Käytä kiinteitä sijainteja:** _Kiinteät ja muut kuin kiinteät sijainnit_

    Toisen rivin kyselyssä määritetään nyt ehdot, joiden perusteella voidaan määrittää, mihin sijainteihin kyseisen rivin kysyntä voidaan paikoittaa.

1. Valitse rivi, jonka **Järjestys**-kentän arvoksi on määritetty *2*.
1. Valitse **Muokkaa kyselyä**.
1. Valitse **Alue**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin ruudukkoon.
1. Määritä uudelle riville seuraavat arvot:

    - **Taulu:** *Sijainnit*
    - **Johdettu taulu:** *Sijainnit*
    - **Kenttä:** *Sijaintiprofiilin tunnus*
    - **Ehdot:** *Poiminta-06* (Valitse kentässä kaksinkertainen plusmerkki \[**++**\] laajentaaksesi luettelon ja valitse sitten *Poiminta-06* - *Poimintatoimipaikka 6*.)

1. Valitse **OK**.

#### <a name="set-up-location-directives"></a>Määritä sijaintidirektiivit

On määritettävä vähintään yksi sijaintidirektiivi, joka tukee paikoituksen poimintoja. Tässä osassa olevien ohjeiden avulla voit määrittää uuden *Varastopoimintojen täydennyssijaintidirektiivin*.

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Valitse vasemman ruudun **Työtilaustyyppi**-kentässä *Täydennys*.
1. Valitse toimintoruudussa **Uusi**.
1. Kirjoita uuden sijaintidirektiivin otsikkoon **Nimi**-kenttään *61 paikoituspoiminta*.
1. Hyväksy **Järjestysnumero**-kentässä oletusarvo.

##### <a name="configure-the-location-directives-fasttab"></a>Määritä Sijaintidirektiivit-pikavälilehti

1. Määritä **Sijaintidirektiivit**-pikavälilehdessä seuraavat arvot. Hyväksy oletusarvot kaikille muille kentille.

    - **Työtyyppi:** _Poiminta_
    - **Toimipaikka:** _6_
    - **Varasto**: _61_
    - **Direktiivikoodi:** _Paikoitus_

1. Valitse **Tallenna**, jos haluat, että **Rivit**-pikavälilehti on käytettävissä.

##### <a name="configure-the-lines-fasttab"></a>Määritä Rivit-pikavälilehti

1. Luo uusi rivi valitsemalla **Rivit**-pikavälilehdellä **Uusi**.
1. Määritä uudelle riville seuraavat arvot.

    - **Määrästä:** _0_
    - **Määrälle:** _1000000_

1. Hyväksy jäljellä olevien kenttien oletusarvot.
1. Valitse **Tallenna**, jos haluat, että **Paikkadirektiivitoimenpiteet**-pikavälilehti on käytettävissä.

##### <a name="configure-the-location-directive-actions-fasttab"></a>Määritä Direktiivitoiminnot-pikavälilehti

1. Luo uusi rivi valitsemalla **Sijaintidirektiivin toiminnot** -pikavälilehdessä **Uusi**.
1. Määritä uudelle riville seuraavat arvot. Hyväksy oletusarvot kaikille muille kentille.

    - **Järjestysnumero:** Hyväksy oletusarvo.
    - **Nimi:** _Bulkki_
    - **Strategia:** _Ei mitään_

1. Hyväksy jäljellä olevien kenttien oletusarvot.
1. Valitse **Tallenna**, jos haluat, että **Muokkaa kyselyä** -painike on käytettävissä.

##### <a name="edit-the-query"></a>Muokkaa kyselyä

1. Valitse **Sijaintidirektiivitoiminnot**-pikavälilehdessä **Muokkaa kyselyä**.
1. Valitse **Alue**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin ruudukkoon.
1. Määritä uudelle riville seuraavat arvot:

    - **Taulu:** *Sijainnit*
    - **Johdettu taulu:** *Sijainnit*
    - **Kenttä:** *Alueen tunnus*
    - **Ehdot:** *Bulkki* (Valitse kentässä kaksinkertainen plusmerkki \[**++**\] laajentaaksesi luettelon ja valitse sitten *Bulkki*.)

1. Valitse **OK**.

## <a name="scenario"></a>Skenaario

### <a name="set-up-the-scenario"></a>Määritä skenaario

Tässä skenaariossa voit käyttää valmiita mallitietoja ja luoda tässä osassa kuvatut tiedot.

#### <a name="use-the-usmf-sample-data"></a>Käytä USMF-mallitietoja

Tämän skenaarion käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.

#### <a name="create-demand"></a>Luo kysyntää

Noudattamalla näitä ohjeita voit luoda kysynnän, johon paikoitus kohdistetaan.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Luo uusi myyntitilaus valitsemalla **Uusi**.
1. Valitse **Luo myyntitilaus** -valintaikkunan **Asiakastili**-kentässä _US-007_.
1. Valitse **Varasto**-kentässä _61_.
1. Valitse **OK**.
1. Uusi myyntitilaus avataan. **Myyntitilausrivit**-pikavälilehti sisältää tyhjän rivin. Määritä tälle riville seuraavat arvot:

    - **Nimike:** _L0101_
    - **Määrä** _20_

1. Lisää uusin rivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:

    - **Nimike:** _T0100_
    - **Määrä** _8_

1. Valitse **Tallenna**.
1. Luo toinen myyntitilaus valitsemalla **Uusi**.
1. Valitse **Luo myyntitilaus** -valintaikkunan **Asiakastili**-kentässä _US-008_.
1. Valitse **Varasto**-kentässä _61_.
1. Uusi myyntitilaus avataan. **Myyntitilausrivit**-pikavälilehti sisältää tyhjän rivin. Määritä tälle riville seuraavat arvot:

    - **Nimike:** _T0100_
    - **Määrä** _1_

1. Valitse **Tallenna**.

### <a name="walk-through-a-typical-slotting-scenario"></a>Käy läpi tyypillinen paikoitusskenaario

Kun kaikki vaaditut elementit on määritetty edellisessä osassa kuvatulla tavalla, voit kokeilla toimintoa käyttämällä tässä osiossa kuvattuja harjoituksia.

#### <a name="generate-demand"></a>Luo kysyntä

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Täydennys \> Paikoitusmallit** ja valitse paikoitusmalli, jonka loit aiemmin.
1. Valitse toimintoruudussa **Luo kysyntä**. Tämä komento arvioi kaiken järjestelmässä olevan kysynnän ja joka vastaa paikoitusmallikyselyä. Kaikkien tilausten kokonaiskysyntä yhdistetään sitten yhdelle riville määrää/mittayksikköä kohden. Kun prosessi on päättynyt, näkyviin tulee tietosanoma.

#### <a name="slotting-demand"></a>Paikoituksen kysyntä

*Paikoituskysyntä* näyttää kysynnän luonnin tulokset, jotka perustuvat paikoitusmallin asetuksiin.

- Jos haluat tarkastella **Luo kysyntä** -komennon tuloksia, valitse toimintoruudusta **Paikoituskysyntä**. Paikoituskysynnän rivejä voi muokata. Voit poistaa rivin, lisätä uuden rivin tai muokata rivin tietoja.

> [!NOTE]
> Voit muokata kysyntää manuaalisesti tai voit tuoda sen ulkoisesta järjestelmästä käyttämällä tietojen hallintaa. Mitä paikoituskysynnässä onkaan, sitä käytetään seuraavassa vaiheessa, riippumatta siitä, mistä se on peräisin.

#### <a name="locate-demand"></a>Etsi kysyntä

Kun kysyntä on luotu, sinun on luotava *paikoitussuunnitelma* käyttämällä **Paikanna kysyntä** -komentoa.

- Valitse toimintoruudussa **Etsi kysyntä**. Paikoitusprosessi suoritetaan. Kun prosessi on päättynyt, näkyviin tulee tietosanoma.

#### <a name="slotting-plan"></a>Paikoitussuunnitelma

Paikoitussuunnitelmassa näkyy sijainti, johon kukin nimike/määrä on liitetty, riippumatta siitä, oliko ylivuoto käytössä, onko lisätyötä luotu, ja mitä malliriviä on käytetty. *Kaikki vaatimukset, joita ei ole voitu paikoittaa on korostettu punaisella.*

- Tarkastele tuloksia valitsemalla Toimintoruudussa **Paikoitussuunnitelma**.

> [!NOTE]
> - **Luo kysyntä**-, **Etsi kysyntä**- ja **Suorita täydennykset** -prosessit suoritaan nyt eristysympäristössä. (Nämä prosessit ovat käytettävissä **Paikoitusmallit**-sivun toimintoruudussa.)
> - **Luo kysyntä**-, **Etsi kysyntä**- ja **Suorita täydennykset** -prosessien lukitus varmistaa, että niitä ei käynnistetä samanaikaisesti. Muutoin käytetyt tiedot voitaisiin poistaa.
> - **Luo kysyntä**- ja **Etsi kysyntä** -prosessit näyttävät varoituksen, jos suoritus luonut tietueita tai jos tietueista puuttuu tietoja.
> - Kun **Paikoitussuunnitelma** valitaan, sivun toimintoruudussa ei ole **Uusi**-, **Muokkaa**- tai **Poista**-painikkeita, koska tietolähdettä ei voi muokata.
> - Kun **Suorita täydennykset** valitaan, järjestelmä tarkistaa valitun paikkamallin ja prosessit.

#### <a name="create-replenishment"></a>Luo täydennys

Kun paikoitussuunnitelma on luotu, suunnitelman perusteella on luotava *Täydennystyöt*.

- Valitse toimintoruudussa **Suorita täydennykset**. Kun prosessi on päättynyt, näkyviin tulee tietosanoma. Tämä sanoma ilmaisee työn koontiversiotunnukselle luotujen otsikoiden määrän.

Käytettävät sijaintidirektiivit määritetään kullekin malliriville määritetyn direktiivikoodin perusteella.

## <a name="tips"></a>Vihjeitä

### <a name="set-up-automatic-slotting"></a>Automaattisen paikoituksen käyttöönotto

Kun kaikki vaaditut elementit ovat paikoillaan, voit määrittää tilauksen suoritettavaksi automaattisesti noudattamalla näitä ohjeita.

1. Valitse **Varastonhallinta \> Täydennys \> Suorita paikoitus**.
1. Määritä suoritettavan työn vaiheet. Valitse yksi tai useampi seuraavista paikoitusvaiheista:

    - Luo kysyntä
    - Etsi kysyntä
    - Luo täydennystyö

    > [!NOTE]
    > Paikoitusvaiheet ovat edistyksellisiä. Jos haluat valita *Paikanna kysyntä*, sinun on ensin valittava *Luo kysyntää*.

1. Määritä käytettävä paikoitusmalli.
1. Voit halutessasi määrittää toistuvan ajon automaattisesti.

Jos harjoitteet ovat skenaariossa, **älä** määritä automaattista paikoitusta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]