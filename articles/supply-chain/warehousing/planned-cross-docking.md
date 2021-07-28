---
title: Suunniteltu cross-docking
description: Tässä ohjeaiheessa kuvataan suunniteltua cross-dockingia, jossa tilauksen edellyttämä varastomäärä ohjataan suoraan vastaanotosta tai luomisesta oikealle lähtevien laiturille tai valmistelualueelle. Saapuvan lähdekoodin koko jäljellä oleva varasto ohjataan oikeaan varastosijaintiin tavallisen hyllytysprosessin kautta.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 9c31b8dd7d69fee40ecefb6c6bc81c9c2dd17ef7
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359074"
---
# <a name="planned-cross-docking"></a>Suunniteltu cross-docking

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan suunnitellun cross-dockingin lisäasetukset. Cross-docking on varastoprosessi, jossa tilauksen edellyttämä varastomäärä ohjataan suoraan vastaanotosta tai luomisesta oikealle lähtevien laiturille tai valmistelualueelle. Saapuvan lähdekoodin koko jäljellä oleva varasto ohjataan oikeaan varastosijaintiin tavallisen hyllytysprosessin kautta.

Cross-dockingin avulla työntekijät ohittavat saapuvan hyllytyksen ja lähtevien nimikkeiden varaston, joka on jo merkitty lähtevälle tilaukselle. Näin ollen varastojen kosketuskertojen määrää vähennetään mahdollisuuksien mukaan. Lisäksi, koska vuorovaikutus järjestelmän kanssa on vähäisempää, fyysisen varastoinnin työn aika- ja tilasäästöt lisääntyvät.

Ennen kuin suoritat cross-dockingin, sinun on konfiguroitava uusi cross-docking-malli, jossa on määritetty toimituslähde ja muut cross-docking-vaatimukset. Kun lähtevä tilaus luodaan, rivi täytyy merkitä saman nimikkeen sisältävään saapuvaan tilaukseen. Voit valita cross docking -mallista direktiivinkoodikentän samalla tavalla kuin täydennys- ja ostotilauksia määritetään.

Saapuvien tilausten vastaanoton yhteydessä cross-docking-asennus määrittää automaattisesti, että cross-docking on tarpeen, ja luo varasto- ja kuormitustyön tarvittavalle määrälle sijaintidirektiivin asetusten mukaisesti.

> [!NOTE]
> Varastotapahtumat *eivät* ole rekisteröimättömiä, kun crossing-dock-työ peruutetaan, vaikka tämän ominaisuuden asetus olisi käytössä varastonhallinnan parametreissa.

## <a name="turn-on-the-planned-cross-docking-features"></a>Suunnitellun cross-docking-toimintojen ottaminen käyttöön

Jos järjestelmäsi ei vielä sisällä tässä aiheessa kuvattuja ominaisuuksia, avaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota seuraavat ominaisuudet käyttöön seuraavassa järjestyksessä:

1. *Suunniteltu cross-docking*
1. *Cross docking -mallit ja sijaintidirektiivit*
    > [!NOTE]
    > Tämän ominaisuuden avulla **direktiivin koodi** kenttä voidaan määrittää cross docking -mallissa samalla tavalla kuin täydennysmallien määrittäminen. Tämän ominaisuuden ottaminen käyttöön estää sinua lisäämästä lopullisen *hyllytys* rivin cross-docking-työmalliriveille direktiivinkoodia. Näin varmistetaan, että työn luonnin aikana voidaan määrittää lopullinen sijainti, ennen kuin otetaan huomioon työmallit.

## <a name="setup"></a>Luo perustiedot

### <a name="regenerate-load-posting-methods"></a>Lataa kirjausmenetelmät uudelleen

Suunniteltu cross-docking toteutetaan kuormituksenkirjausmenetelmänä. Kun olet määrittänyt toiminnon, menetelmät on luotava uudelleen.

1. Valitse **Varastonhallinta \> Asetukset \> Lataa kirjausmenetelmät**.
1. Valitse toimintoruudussa **Luo menetelmät uudelleen**.

    Kun uudelleen luominen on suoritettu, näkyviin tulee menetelmä, jonka **menetelmän nimen** arvo on *planCrossDocking*.

1. Sulje sivu.

### <a name="create-a-cross-docking-template"></a>Luo cross-docking-malli

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Cross-docking-mallit**.
1. Valitse toimintoruudussa **Uusi** ja luo malli.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Järjestys:** *1*

        Tämä kenttä määrittää, missä järjestyksessä mallit arvioidaan.

    - **Cross-docking-mallipohjan tunnus:** *51*
    - **Kuvaus:** *Varasto 51*
    - **Kysynnänvapautuskäytäntö:** *Ennen toimitusvastaanottoa*
    - **Varasto**: *51*

1. **Suunnittelu**-pikavälilehden määritys ohjaa mallin toimintaa. Määritä seuraavat arvot:

    - **Tarvevaatimukset:** *Ei mitään*

        Tämä kenttä määrittää kysynnän varaston tarpeet. Jos tarve on linkitetty tarjontaan ennen luovutusta, valitse *Merkintä*. Jos kysynnän on oltava tilaus-varattu toimitusta vasten ennen julkaisua, valitse *Tilauksen varaus*.

    - **Sijaintityyppi:** *Lähetyssijainnit*

        Tässä kentässä määritetään, käyttävätkö cross-docking-työt lähetyksen varastointi-/lataussijainteja vai käytetäänkö sen omia valmistelu-/kuormitussijainteja sijaintidirektiivien avulla.

    - **Työmalli:** Jätä tämä kenttä tyhjäksi.

        Tämä kenttä määrittää työmallin, jota käytetään, kun cross-docking-työtä luodaan.

    - **Tarkista uudelleen toimituskuitissa:** *Ei*

        Tämä vaihtoehto määrittää, tuleeko toimitus vahvistaa uudelleen vastaanoton aikana. Jos tämän asetuksen arvoksi on määritetty *Kyllä*, sekä enimmäisaikaikkuna että vanhenemispäivien alue tarkistetaan.

    - **Direktiivikoodi:** Jätä tämä kenttä tyhjäksi

        Tämä vaihtoehto on käytössä *cross docking -malleilla ja sijaintidirektiivi* -toiminnolla. Järjestelmän käyttää sijaintidirektiivejä parhaan paikan määrittämiseen cross-docking varaston siirtämiselle. Voit määrittää sen määrittämällä jokaiselle asiaankuuluvalle cross-docking-mallille direktiivikoodin. Jos direktiivikoodi on määritetty, järjestelmä etsii sijaintidirektiivit direktiivikoodin perusteella, kun työ luodaan. Näin voit rajata tietyssä cross docking -mallissa käytettävät sijaintiohjeet.

    - **Vahvista aikaikkuna:** *Kyllä*

        Tämä vaihtoehto määrittää, arvioidaanko enimmäisaikaikkuna, kun toimituslähde valitaan. Jos tämän asetuksen arvoksi on määritetty *Kyllä*, järjestelmän enimmäis- ja vähimmäisaikakenttiin liittyvät kentät ovat käytettävissä.

    - **Enimmäisaikaikkuna** *5*

        Tämä kenttä määrittää enimmäisajan, joka on sallittu toimitusten saapumisen ja kysynnän poistumisen välillä.

    - **Enimmäisaikaikkunayksikkö:** *Päivät*
    - **Vähimmäisaikaikkuna** *0*

        Tämä kenttä määrittää vähimmäisajan, joka on sallittu toimitusten saapumisen ja kysynnän poistumisen välillä.

    - **Vähimmäisaikaikkunayksikkö:** *Päivät*
    - **Voimassaolon päättymisalue päivissä** *0*

        *Ensimmäinen päättymispäivä (FEFO) -ehto:* Tässä kentässä määritetään varastossa tällä hetkellä olevan ensimmäisen vanhentumiserän vanhentumispäivämäärän ja vastaanotetun erän välinen päivien enimmäismäärä.

1. **Toimituslähteet**-pikavälilehdessä voit määrittää tämän mallin käytettävissä olevat toimituslajit. Valitse **Uusi** ja määritä sitten seuraavat arvot:

    - **Järjestysnumero:** *1*
    - **Toimituslähde:** *Ostotilaus*

### <a name="create-a-work-class"></a>Työluokan luominen

1. Valitse **Varastonhallinta \> Asetukset \> Työ \> Työluokka**.
1. Valitse toimintoruudussa **Uusi** ja luo työluokka.
1. Määritä seuraavat arvot:

    - **Työluokan tunnus:** *CrossDock*
    - **Kuvaus:** *Cross Dock*
    - **Työtilaus tyyppi:** *Cross docking*

### <a name="create-a-work-template"></a>Luo työmalli

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Aseta **Työtilaustyyppi**-kentän arvoksi *Cross-docking*.
1. Lisää **Yleiskuvaus**-välilehdelle uusi rivi valitsemalla toimintoruudussa **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **Järjestysnumero:** *1*
    - **Työmalli:** *51 Cross Dock*
    - **Työmallin kuvaus:** *51 Cross Dock*

1. Valitse **Tallenna**, jos haluat, että **Työmallin tiedot** -pikavälilehti on käytettävissä.
1. Lisää uusi rivi ruudukkoon **Työmallin tiedot** -pikavälilehdessä **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **Työtyyppi:** *Poiminta*
    - **Työluokan tunnus:** *CrossDock*

1. Lisää toinen rivi valitsemalla **Uusi** ja määritä sille seuraavat arvot:

    - **Työtyyppi:** *Aseta*
    - **Työluokan tunnus:** *CrossDock*

1. Valitse **Tallenna** ja vahvista, että *51 Cross Dock* -mallille on valittu **Kelvollinen**-valintaruutu .

> [!NOTE]
> *Poiminta*- ja *Hhyllytys*-työtyyppien työluokkien tunnusten on oltava samat.

### <a name="create-location-directives"></a>Luo toimipaikkadirektiivit

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Aseta vasemmassa ruudussa **Työtilaustyyppi**-kentän arvoksi *Cross-docking*.
1. Valitse toimintoruudussa **Uusi** ja määritä seuraavat arvot:

    - **Järjestysnumero:** *1*
    - **Nimi:** *51 Cross Dock Put*
    - **Työtyyppi:** *Aseta*
    - **Toimipaikka:** *5*
    - **Varasto**: *51*

1. Valitse **Tallenna**, jos haluat, että **Rivit**-pikavälilehti on käytettävissä.
1. Lisää uusi rivi ruudukkoon **Rivit**-pikavälilehdessä **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **Määrästä:** *1*
    - **Määrälle:** *1000000*

1. Valitse **Tallenna**, jos haluat, että **Paikkadirektiivitoimenpiteet**-pikavälilehti on käytettävissä.
1. Lisää uusi rivi ruudukkoon **Sijaintidirektiivin toiminnot** -pikavälilehdessä **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **Nimi:** *Baydoor*
    - **Kiinteän sijainnin käyttö:** *Kiinteät ja muut kuin kiinteät sijainnit*

1. Valitse **Tallenna**, jos haluat, että **Sijaintidirektiivin toiminnot** -työkalurivin **Muokkaa kyselyä** -painike on käytettävissä.
1. Avaa kyselyeditori valitsemalla **Muokkaa kyselyä**.
1. Varmista **Alue** -välilehdessä, että seuraavat kaksi riviä on konfiguroitu:

    - Rivi 1:

        - **Taulu:** *Sijainnit*
        - **Johdettu taulu:** *Sijainnit*
        - **Kenttä:** *Varasto*
        - **Ehdot:** *51*

    - Rivi 2:

        - **Taulu:** *Sijainnit*
        - **Johdettu taulu:** *Sijainnit*
        - **Kenttä:** *Sijainti*
        - **Kriteerit:** *Baydoor*

1. Valitse **OK** sulkeaksesi kyselyeditorin.

### <a name="create-a-mobile-device-menu-item"></a>Luo mobiililaitteen valikkovaihtoehto

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse vasemmanpuoleisen ruudun valikkovaihtoehtojen luettelosta **Oston hyllytys**.
1. Valitse **Muokkaa**.
1. Lisää uusi rivi ruudukkoon **Työlajit**-pikavälilehdessä **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **Työluokan tunnus:** *CrossDock*
    - **Työtilaus tyyppi:** *Cross docking*

1. Valitse **Tallenna**.

## <a name="scenario"></a>Skenaario

### <a name="create-a-purchase-order"></a>Ostotilauksen luominen

Noudattamalla näitä ohjeita voit luoda ostotilauksen toimituslähteeksi.

1. Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta **Luo ostotilaus** -valintaikkunassa seuraavat arvot:

    - **Toimittajan tili:** *104*
    - **Varasto**: *51*

1. Valitse **OK** ja kirjoita tilausnumero muistiin.
1. **Ostotilausrivit**-pikavälilehdelle lisätään uusi rivi. Määritä tälle riville seuraavat arvot:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *5*

### <a name="create-a-sales-order"></a>Luo myyntitilaus

Noudattamalla näitä ohjeita voit luoda myyntitilauksen kysynnän lähteeksi.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-002*
    - **Varasto**: *51*

1. Valitse **OK**.
1. **Myyntitilausrivit**-pikavälilehdelle lisätään uusi rivi. Määritä tälle riville seuraavat arvot:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *3*

### <a name="create-planned-cross-docking"></a>Luo suunniteltu cross-docking

Seuraavien vaiheiden avulla voit luoda suunnitellun cross-dockingin myyntitilauksesta.

1. Valitse juuri luomasi myynti tilauksen **Myyntitilaustiedot** -sivulta toimenpideruudun **Varasto**-välilehden **Toiminnot**-ryhmästä **Vapauta varastoon**.

    Vapauta varastoon -toiminto luo myyntitilausriville lähetys- ja kuormitusrivin sekä yrittää kohdistaa varaston.
    
    Näyttöön avautuu tietosanoma. Näyttöön tulee myös seuraava varoitussanoma: "Aallolle XXXX ei luotu työtä. Lisätietoja on työn luonnin historialokissa." Tämä toiminta on odotettavissa, koska varastossa ei ole varastoa.

1. Valitse **Myyntitilausrivit**-pikavälilehdellä **Varasto**-valikosta **Lähetyksen tiedot**.

    Näkyviin tulee **Lähetyksen tiedot** -sivu, jossa näkyy myyntitilaukselle luotu lähetys.

1. Huomaa, että **Suunniteltu cross-docking-määrä** -kentän arvo on *3* **Lataa rivit** -pikavälilehdessä. Koska varastossa ei ollut käytettävissä varastoa, mutta voimassa oleva toimituslähde saapuu cross-docking-mallissa määritettyyn aikaikkunaan, cross-docking-määrä on luotu.
1. Voit tarkastella luotuja cross-docking-tietoja valitsemalla **Lataa rivit** -pikavälilehdessä **Suunniteltu cross-docking**.

## <a name="process-the-cross-docking"></a>Prossessoi cross-docking

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a>Ostotilauksen vastaanotto varastoinnin mobiilisovelluksessa

Järjestelmä vastaanottaa ostotilauksesta viiden määrän vastaanottosijaintiin ja luo kaksi työkappaletta.

Ensimmäisen luotavan työtunnuksen **Työtilaustyypin** arvo on *Cross docking* ja se on linkitetty myyntitilaukseen. Sen määrä on 3 ja se ohjataan lopulliseen lähetyssijaintiin, jotta se voidaan lähettää heti.

Toisen luotavan työtunnuksen **Työtilaustyypin** arvo on *Ostotilaukset* ja se on linkitetty ostotilaukseen. Sen jäljellä oleva määrä on 2, se ei ollut cross-dockattu ja se ohjataan hyllytyksen varastointiin.

1. Kirjaudu kannettavaan laitteeseen käyttäjänä varastossa *51*.
1. Siirry kohtaan **Saapuva \> Oston vastaanotto**.
1. Syötä **PONum**-kenttään ostotilauksen numero.
1. Kirjoita **Määrä**-kenttään *5*.
1. Valitse **OK**.
1. Määritä seuraavalla sivulla **Nimike**-kentän arvoksi *A0001*.
1. Valitse **OK**.
1. Vahvista seuraavalla sivulla **PONum**-, **Nimike**- ja **Määrä**-arvot valitsemalla **OK**.

    Näyttöön tulee Työ valmis -sanoma.

1. Valitse **Peruuta**, jos haluat poistua.

### <a name="put-away-to-cross-docking-and-bulk"></a>Hyllytys cross-dockingiin ja irtotavaraan

Tällä hetkellä molemmilla työtunnuksilla on sama kohderekisterikilpi. Jotta voit suorittaa seuraavat vaiheet, sinun on saatava työtunnus ja kohderekisterikilpitunnus. Voit saada nämä tiedot ostotilausrivin ja myyntitilausrivin työtiedoista. Vaihtoehtoisesti voit siirtyä kohtaan **Varastonhallinta \> Työ \> Työtiedot** ja suodattaa työt, joissa **Varasto**-arvo on *51*.

1. Siirry mobiililaitteen **Saapuva \> Ostohyllytys**-kohtaan ja kirjoita työn kohderekisterikilpi.
1. Kirjoita **Tunnus**-kenttään työtietojen kohderekisteritunnus.

    Cross-docking-keräyssivulla näkyy keräilysijainti (*RECV*), kohderekisterikilpi (*rekisterikilpi*), nimike (*A0001*) ja määrä (*3*).

1. Valitse **OK**.
1. Kirjoita **Kohde-RK**-kenttään sen rekisterikilven tunnus, joka on tarkoitus sijoittaa (cross-dockata) lähetyssijaintiin. Voit valita haluamasi rekisterikilven tunnuksen.
1. Valitse **OK**.
1. Kirjoita seuraavalla sivulla **Tunnus**-kenttään kohderekisteritunnus.
1. Valitse **OK**.
1. Vahvista jäljellä olevan määrän 2 poimintatyö ja valitse **OK**.
1. Valitse seuraavalla sivulla **Valmis**, kun haluat lopettaa poimintaprosessin ja aloittaa hyllytysprosessin.

    Mobiilisovellus esittää sinulle sijainnin ja rekisterikilven, johon kohde sijoitetaan.

1. Vahvista irtotavaran **Hyllytys** valitsemalla **OK**.
1. Varmista seuraavalla sivulla, että cross-dockingin **Hyllytys** on käytössä valitsemalla **OK**.

    Näyttöön tulee Työ valmis -sanoma.

1. Valitse **Peruuta**, jos haluat poistua.

Seuraavassa kuvassa näkyy, miten tehty cross-docking-työ saattaa näkyä Microsoft Dynamics 365 Supply Chain Managementissa.

![Cross-docking-työ päättynyt.](media/PlannedCrossDockingWork.png "Cross-docking-työ päättynyt")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]