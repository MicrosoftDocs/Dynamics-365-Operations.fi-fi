---
title: Täydennys yli sijainnin kapasiteetin
description: Tässä ohjeaiheessa on tietoja Täydennys sijainnin kapasiteetilla -ominaisuudesta. Tämä ominaisuus ottaa käyttöön kaiken täydennystyön, joka vaaditaan luontipäivänä. Se myös hallitsee täydennystyön käytettävyyttä ja varmistaa näin, että varasto ei koskaan lopu keräilysijainnista eikä kapasiteettia ylitetä.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 0c3dedc47558e98f63fb5883e4731bf021b9602b
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677923"
---
# <a name="replenishment-over-location-capacity"></a>Täydennys yli sijainnin kapasiteetin

[!include [banner](../includes/banner.md)]

Joidenkin määrältään suurten tai tilarajoitteisten varastojen on lähetettävä nimikettä suurempia määriä päivässä kuin keräilysijaintiin mahtuu. *Täydennys sijainnin kapasiteetilla* -ominaisuus ottaa käyttöön kaiken täydennystyön, joka vaaditaan luontipäivänä. Se myös hallitsee täydennystyön käytettävyyttä ja varmistaa näin, että varasto ei koskaan lopu keräilysijainnista eikä kapasiteettia ylitetä.

Tämän ominaisuuden avulla on mahdollista luoda enemmän täydennystöitä kuin sijaintiin mahtuu. Tämä estää täydennystyön valmistumisen, kun sijainti on täynnä. Kun keräilysijainnin varasto laskee alle määritetyn rajan, täydennystyötä määritetään lisää käytettäväksi.

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a>Täydennystyö sijainnin kapasiteetilla -ominaisuuden ottaminen käyttöön

Voit käyttää tätä ominaisuutta ottamalla seuraavat ominaisuudet käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (seuraavassa järjestyksessä):

1. Organisaation laajuinen työn esto (Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on pakollinen, joten se on oletusarvoisesti otettu käyttöön eikä sitä poistaa uudelleen käytöstä.)
1. Täydennys yli sijainnin kapasiteetin

## <a name="set-up-the-feature-for-the-example-scenario"></a>Määritä ominaisuus tälle esimerkkiskenaariolle

Tässä ohjeaiheessa on ohjeita ja esimerkki, jossa kerrotaan tämä ominaisuuden määrityksestä ja tässä ohjeaiheessa myöhemmin olevan esimerkkiskenaarion näytetietojen valmistelemisesta.

### <a name="enable-sample-data"></a>Mallitietojen ottaminen käyttöön

[Esimerkkiskenaarion](#example-scenario) käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon [vakiodemotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.

### <a name="location-profile"></a>Sijaintiprofiili

Ota käyttöön Täydennys kapasiteetilla -ominaisuus sijaintiprofiilissa.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintien profiilit**.
1. Valitse vasemmasta ruudusta **POIMINTA-06**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Määritä **Täydennys**-pikavälilehdessä seuraavat arvot:

    - **Ylittää sijaintikapasiteetin:** *Kyllä*

        Kun otettu käyttöön, täydennystyö saa ylittää sijainnin enimmäiskapasiteetin. Tämä ottaa käyttöön myös muut **Täydennys**-pikavälilehden kentät.

    - **Työn käytettävyyden rajatyyppi:** *Määrä*

        Tämä kenttä määrittää menetelmän, jota käytetään lisätyön vapauttamisen määrittämisessä. Vapautus voidaan tehdä määrän tai prosenttiosuuden mukaan seuraavasti:

        - *Prosenttiosuus* – Valitse tämä vaihtoehto, jos haluat käyttää prosenttiosuuden kapasiteettia, joka perustuu varastointirajoituksiin tai tilavuustietoihin. Tämän vaihtoehdon avulla voidaan ottaa käyttöön **Ylivuotoprosentti**-kenttä. Se poistaa käytöstä kaksi määrään liittyvää kenttää, jotka ovat **Ylivuotomäärä** ja **Ylivuotoyksikkö**.

            Voit käyttää tätä vaihtoehtoa, jos keräilysijainneissa on käytössä tilavuustiedot.

            Jos tämä vaihtoehto on valittuna, määritä **Ylivuotoprosentti**-kentän arvoksi prosenttiluku, jonka yhteydessä määritetään lisää täydennystyötä käytettäväksi.

        - *Määrä* – Valitse tämä vaihtoehto, jos haluat käyttää tiettyä määräarvoa. Tämän vaihtoehdon avulla poistaa käytöstä **Ylivuotoprosentti**-kenttä. Se ottaa käyttöön **Ylivuotomäärä**- ja **Ylivuotoyksikkö**-kentät.

            Käytä tätä vaihtoehtoa, jos et käytä tilavuustietoja täydennettäville sijainneille, tai jos sinulla on yhdenmukaisia määriä, joista haluat tuoda lisää varastoa sijaintiin.

           Jos tämä vaihtoehto on valittuna, määritä sen määrän ja yksikön **Ylivuotomäärä**- ja **Ylivuotoyksikkö**-kentät, jolle määritetään lisää täydennystyötä käytettäväksi.

    - **Ylivuotomäärä:** *0,65*

        Tämä kenttä määrittää määrän, jolloin sijainnissa on ylivuoto.

        Työ on käytettävissä aina, kun sijainnin varastosaldon ja työn määrien summa alittaa tämän arvon. Mahdollinen täydennystyö, joka on yli tämän arvon, estetään, ja se on vapautettava manuaalisesti.

        Sijainnin varastointirajoitukset otetaan huomioon, kun työmäärää lasketaan.

    - **Ylivuotoyksikkö:** *KL*

        Tässä kentässä määritetään ylivuotomäärään liittyvä yksikkö.

        Tässä tapauksessa käytettävissä on enemmän täydennystyötä, kun sijainnissa on alle 0,65 kuormalavaa (KL).

    - **Ylivuotoprosentti**

        Tämä kenttä määrittää prosenttiosuuden, jolloin sijainnissa on ylivuoto.

        Työ on käytettävissä aina, kun sijainnin varastosaldon ja työn määrien summa alittaa tämän prosenttiosuuden. Mahdollinen täydennystyön määräprosentti, joka on yli tämän arvon, estetään, ja se on vapautettava manuaalisesti.

        Sijainnin varastointirajoitukset otetaan huomioon, kun työmäärän prosenttiosuutta lasketaan. Jos sijainnin varastointirajoituksia ei ole määritetty, työmääräprosentti lasketaan tilavuuden mukaan, jos tilavuusrajoitteita on määritetty sijaintiprofiilissa.

> [!IMPORTANT]
> Jos käytössä ovat **USMF**-yrityksen esittelytiedot ja aiemmin käyttöönotettu *Sijainnin rekisterikilven paikannus* -ominaisuus, poista **Ota käyttöön rekisterikilven paikannus** -asetus käytöstä **BULKKI-06**-sijaintiprofiilissa ja tee mobiilisovelluksen vaiheet valmiiksi esimerkkiskenaariossa.

### <a name="wave-step-code"></a>Aallon vaihekoodi

> [!NOTE]
> Jos haluat määrittää aallon vaihekoodin tässä määritetyllä tavalla, ensin on ehkä käytettävä [ominaisuuksien hallintaa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja otettava käyttöön ominaisuus, jonka nimi on *Organisaationlaajuinen aallon vaihekoodi*.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Aallot \> Aallon vaihekoodit**.
1. Valitse **Uusi** ja määritä seuraavat arvot:

    - **Aallon vaihekoodi:** *Täydennä*
    - **Aallon vaihekuvaus:** *Täydennys*
    - **Aalto vaihetyyppi:** *Täydennys*

1. Valitse **Tallenna**.

### <a name="replenishment-template"></a>Täydennysmalli

Täydennysmallit ovat sääntöjoukko, joka määrittää, milloin ja miten sijaintia täydennetään.

1. Valitse **Varastonhallinta \> Asetukset \> Täydennys \> Täydennysmallit**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse **Yleiskatsaus**-osassa rivi, jolla **Täydennysmalli**-kentän arvoksi on määritetty *Vaadi täydennystä*.
1. Määritä seuraavat arvot:

    - **Aallon vaihekoodi:** *Täydennä*
    - **Salli aaltokysynnän käyttää varauksettoman määrän:** *Kyllä*

1. Valitse **Tallenna**.

### <a name="wave-template"></a>Aaltomalli

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.
1. Aseta vasemmassa ruudussa **Aaltomallityyppi**-kentän arvoksi *Lähetys*.
1. Valitse luettelosta **61 - lähetys** -malli.
1. Valitse toimintoruudussa **Muokkaa**.
1. Määritä **Yleiset**-pikavälilehden **Automatisoi täydennystyön vapautus** -asetukseksi *Kyllä*.

    Jos määrität tämän vaihtoehdon arvoksi *Kyllä*, voit luoda täydennystyön tarpeen mukaan ja vapauttaa sen automaattisesti. Sinun on lisättävä täydennyksen aaltomenetelmä aaltomalliin ja luotava täydennysmalli, jonka tyyppi on **Aallon kysyntä**. Määritä täydennysmalli **Täydennysmallit**-sivulla. Jos haluat määrittää täydennysmallin, lisää täydennysmenetelmä aaltomalliin.

1. Etsi **Menetelmät**-välilehden **Valitut menetelmät**-sarakkeesta seuraava rivi:

    - **Menetelmän nimi:** *täydennä*
    - **Nimi:** *Täydennys*

1. Määritä **Aallon vaihekoodi** -kentän arvoksi tälle riville *Täydennä*.
1. Valitse **Tallenna**.

## <a name="example-scenario"></a>Esimerkkiskenaario

Kun olet tehnyt kaikki edellä mainitut näytetiedot käytettäviksi ja määrittänyt ne, voit käyttää tätä skenaariota ja kokeilla *Täydennys sijainnin kapasiteetilla* -toimintoa. Tämän skenaarion arvoissa oletetaan, että käsittelet vakionäytetietoja, valittuna on **USMF**-yritys ja että aiemmin tässä ohjeaiheessa kuvatut näytetietueet on valmisteltu. Tämä skenaario on myös esimerkki siitä, miten ominaisuutta voidaan käyttää tuotannon määrityksessä.

### <a name="create-replenishment-work"></a>Luo täydennystyö

#### <a name="create-sales-order-1"></a>Luo myyntitilaus 1

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi** ja avaa valintaikkuna luodaksesi uuden myyntitilauksen.
1. Lisää valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-007*
    - **Varasto**: *61*

1. Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.
1. Uusi myyntitilaus avataan. **Myyntitilausrivit**-pikavälilehti sisältää uuden, tyhjän rivin. Määritä tälle riville seuraavat arvot:

    - **Nimiketunnus:** *T0100*
    - **Määrä** *40*

1. Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Varaus**.
1. Valitse **Varaus**-sivun kohta **Varaa erä**.
1. Sulje sivu.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.

    Näyttöön tulevat tietosanomat ilmaisevat luodun aallon ja lähetyksen tunnukset. Myös täydennysaalto luodaan.

    Näyttöön tulee myös seuraava varoitussanoma: "Työtä, jonka tunnus on XXXX, ei voi vapauttaa, koska sillä on keskeneräistä täydennystyötä.

#### <a name="create-sales-order-2"></a>Luo myyntitilaus 2

1. Valitse **Kaikki myyntitilaukset** -sivun toimintoruudussa **Uusi**, jos haluat avata valintaikkunan ja luoda uuden myyntitilauksen.
1. Lisää valintaikkunassa seuraava arvo:

    - **Asiakastili:** *US-001*
    - **Varasto**: *61*

1. Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.
1. Uusi myyntitilaus avataan. **Myyntitilausrivit**-pikavälilehti sisältää uuden, tyhjän rivin. Määritä tälle riville seuraavat arvot:

    - **Nimiketunnus:** *T0100*
    - **Määrä** *60*

1. Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Varaus**.
1. Valitse **Varaus**-sivun kohta **Varaa erä**.
1. Sulje sivu.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.

    Näyttöön tulevat tietosanomat ilmaisevat luodun aallon ja lähetyksen tunnukset. Myös täydennysaalto luodaan.

    Näyttöön tulee myös seuraava varoitussanoma: "Työtä, jonka tunnus on XXXX, ei voi vapauttaa, koska sillä on keskeneräistä täydennystyötä.

#### <a name="create-sales-order-3"></a>Luo myyntitilaus 3

1. Valitse **Kaikki myyntitilaukset** -sivun toimintoruudussa **Uusi**, jos haluat avata valintaikkunan ja luoda uuden myyntitilauksen.
1. Lisää valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-004*
    - **Varasto**: *61*

1. Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.
1. Uusi myyntitilaus avataan. **Myyntitilausrivit**-pikavälilehti sisältää uuden, tyhjän rivin. Määritä tälle riville seuraavat arvot:

    - **Nimiketunnus:** *T0100*
    - **Määrä** *30*

1. Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Varaus**.
1. Valitse **Varaus**-sivun kohta **Varaa erä**.
1. Sulje sivu.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.

    Näyttöön tulevat tietosanomat ilmaisevat luodun aallon ja lähetyksen tunnukset. Myös täydennysaalto luodaan.

    Näyttöön tulee myös seuraava varoitussanoma: "Työtä, jonka tunnus on XXXX, ei voi vapauttaa, koska sillä on keskeneräistä täydennystyötä.

#### <a name="view-work-details"></a>Näytä työn tiedot

1. Valitse **Varastonhallinta \> Työ \> Työn tiedot**.
1. Suodata **Yleiskatsaus**-osassa **Varasto**-sarake varastolle *61*.
1. Näkyvissä pitäisi olla tieto siitä, että kolmelle kysynnän myyntitilaukselle luotiin seitsemän työtunnusta.

    - Kolmella seitsemästä työtunnuksesta on **Työtilaustyyppi**-kohdan arvona *Täydennys* ja neljällä **Työtilaustyyppi**-kohdan arvona *Myyntitilaukset*.
    - Kaikilla kolmella työtilauksella, joiden **Työtilaustyyppi**-kohdan arvo on *Täydennys*, on sama *keräily*- ja *hyllytyssijainti* **Rivit osassa**.

        - **Keräily:** *02A01R5S1B*
        - **Hyllytys:** *06A01R2S1B*

    - Myyntitilaukselle 1 on luotu kaksi työtunnusta.

1. Merkitse kaikkien myyntitilausten työtunnukset muistiin.

Käytettävissä olevista määristä riippuen luodut työmäärät voivat olla hieman erilaisia. Yleisesti luotujen työotsikoiden tulisi kuitenkin vastata tämän skenaarion esimerkkiä.

#### <a name="on-hand-inventory-license-plate-id"></a>Käytettävissä olevan varaston rekisterikilven tunnus

Myöhemmin tässä skenaariossa käytetään varastonhallinnan mobiilisovellusta (tai emulaattoria), jossa sinun on tunnistettava rekisterikilpi keräilyn ja täydennyksen skenaarioiden viimeistelemistä varten.

Voit etsiä myöhemmin tarvittavat rekisterikilven tunnukset alla olevien vaiheiden avulla.

1. Siirry kohtaan **Varastonhallinta \> Kyselyt ja raportit \> Käytettävissä olevien luettelo**.
1. Avaa suodatinruutu valitsemalla **Näytä suodattimet** -painike.
1. Anna seuraavat suodatusehdot, jos haluat hakea skenaarion rekisterikilvet. Käytä *alkaa*-suodatinta.

    - **Nimiketunnus:** *T0100*
    - **Varasto**: *61*

1. Valitse **Käytä**.
1. Valitse toimintoruudussa **Dimensiot**.
1. Valitse **Dimensioiden näyttö** -valintaruudussa **Tallennusdimensiot**-osassa kaikki arvot.
1. Valitse **Tapahtumat**-osassa **nimikenumeroksi** ja **määräksi \<\> 0**.
1. Kun olet valmis, sulje valintaikkuna valitsemalla **OK**.
1. **Käytettävissä oleva** -ruudukossa on rekisterikilpien numerot nimikkeelle *T0100* kaikissa sijainneissa. Merkitse muistiin kussakin sijainnissa oleva rekisterikilpi, koska tarvitset näitä tietoja myöhemmin.
1. Sulje sivu.

### <a name="process-steps"></a>Prosessivaiheet

Suorita varastosijainnin täydennys kahdelle ensimmäiselle työtunnukselle. Kolmannen täydennystyön työ estetään siihen asti, kunnes varastotaso keräilysijainnissa on alle rajan.

#### <a name="replenishment"></a>Täydennys

1. Kirjaudu varastonhallinnan mobiilisovellukseen käyttäjänä varastossa *61*. (Anna käyttäjätunnukseksi *61* ja salasanaksi *1*.)
1. Siirry kohtaan **Varasto \> Täydennys**.

    Sinua pyydetään suorittamaan ensimmäinen täydennystyö. Näkyvissä ovat nimiketunnus, määrä ja keräilysijainti.

1. Anna **RK**-kenttään sen nimikkeen rekisterinumero, jonka sijainti näytetään.
1. Valitse **OK**-painike (valintamerkkisymboli).

    Järjestelmä luo kohderekisterinumeron keräiltävän nimikkeen uudelle rekisterikilvelle.

1. Vahvista arvo valitsemalla **OK**.

    Näkyviin tulee työ, joka kehottaa käyttäjää asettamaan kohderekisterikilven täydennyssijaintiin. *Keräilysijainnin* on oltava **06A01R2S1B**.

1. Vahvista keräilyn tiedot ja valitse **OK**.

    Näyttöön tulee Työ valmis -sanoma ja seuraavan täydennyskeräilytehtävän tiedot: nimikenumero, määrä ja keräilysijainti. Keräilysijainti on sama kuin ensimmäinen täydennyssijainti. Tämän vuoksi rekisterikilvellä on sama rekisterikilven tunnus, jota käytettiin ensimmäisessä täydennystyötehtävässä.

1. Suorita toisen työtehtävän täydennystyöt toistamalla edellä kuvatut vaiheet. Määrä- ja kohderekisterikilpi eroavat ensimmäisen työtehtävän määrä- ja kohderekisterikilvestä.

Kun toinen täydennystyö on valmis, näyttöön tulee Työ valmis -sanoma. Mobiililaite ilmoittaa myös, jos työtä ei ole saatavissa, vaikka täydennystyötä olisi jäljellä. Tämä johtuu siitä, että täydennystyön saatavuuden tila on *Pidossa* ja sen vuoksi se saa merkinnän **Estetty**.

*Pidossa*-tila käynnistettiin, koska sen keräilysijaintiin liitetyn työn sijaintiprofiilin **Ylivuotomäärä**-kohdan arvo on *0,65 KL*. Kaksi edellistä täydennystyötehtävää täyttivät nimikkeen *T0100* lähes ylivuotorajaan asti. (Nimikkeen yksikkömuunnos on *1 KL = 100 kpl*.) Tämän vuoksi jäljellä oleva täydennystyö voi aiheuttaa sijainnin ylivuotorajan ylityksen.

Tämä täydennystyö pysyy estettynä niin kauan, kunnes sijainnista kerätään tarpeeksi varastoa ja mobiililaitteen valikkovaihtoehdon työn vapautuksen raja alittuu.

#### <a name="sales-order-pick"></a>Myyntitilauksen keräily

Ennen kuin jäljellä oleva täydennystyötehtävä voidaan viimeistellä, keräilysijainnin varaston tason on oltava niin alhainen, että jäljellä oleva täydennystyö voidaan vapauttaa. Toisin sanoen käytettävissä olevan varaston kokonaismäärä sijainnissa ja täydennysmäärä eivät saa ylittää **ylivuotomäärän** arvoa. Kun tämä summa on pienempi kuin ylivuotomäärä, jäljelle jäävä täydennystyö vapautetaan.

1. Kirjaudu varastonhallinnan mobiilisovellukseen käyttäjänä varastossa *61*. (Anna käyttäjätunnukseksi *61* ja salasanaksi *1*.)
1. Siirry kohtaan **Lähtevät \> Myynnin keräily**.
1. Anna myyntitilauksen 1 ensimmäinen työtunnus.

    Katso **Työn tiedot** -sivulta niiden myyntitilausten työtunnukset, jotka kirjoitit muistiin aiemmin. Tässä annettava työtunnus luo keräilytyön 10 kappaleen määrälle kahdessa eri sijainnissa.

1. Valitse **OK**.

    **Myyntitilaukset: Keräily** -tehtävän sivulla ovat nimikenumero, määrä ja ensimmäisen sijainnin keräilysijainti.

1. Anna **RK**-kenttään sen nimikkeen rekisterinumero, jonka sijainti näytetään.
1. Valitse **OK**-painike (valintamerkkisymboli).

    **Myyntitilaukset: Keräily** -tehtävän sivulla ovat nimikenumero, määrä ja seuraavan sijainnin keräilysijainti.

1. Anna **RK**-kenttään sen nimikkeen rekisterinumero, jonka sijainti näytetään.
1. Valitse **OK**-painike (valintamerkkisymboli).

    **Myyntitilaukset: Hyllytys** -sivulla on ohjeita molempien valmiiden keräilytöiden hyllytyksestä lähtevien väliaikaiseen sijaintiin.

1. Valitse **OK**.

    Näyttöön tulee Työ valmis -sanoma.

1. Anna myyntitilauksen 1 toinen työtunnus.

    Tällä työtunnuksella on vain yksi keräilytehtävä.

1. Valitse **OK**.

    **Myyntitilaukset: Keräily** -tehtävän sivulla ovat nimikenumero, määrä ja keräilysijainti.

1. Anna **RK**-kenttään sen nimikkeen rekisterinumero, jonka sijainti näytetään.

    Määritettävä rekisterikilpi tulee olemaan eräs järjestelmän luomista rekisterikilvistä täydennystyötehtävissä. Voit varmistaa, että tallennat oikean rekisterikilven tunnuksen, tarkistamalla varaston **Käytettävissä olevien luettelo** -sivulla nimikkeen, sijainnin ja määrän osalta.

1. Valitse **OK**-painike (valintamerkkisymboli).
1. Vahvista hyllytystehtävän ohjeet lähtevien väliaikaisessa sijainnissa.
1. Valitse **OK**.

    Näyttöön tulee Työ valmis -sanoma.

Myyntitilauksen 2 keräily on estetty, koska linkitettyä täydennystyötä ei ole viimeistelty. Tällä hetkellä keräilysijainnissa on yhä 30 kappaleen määrä, ja myyntitilauksen 2 täydennysmäärä on 60 kpl. Käytettävissä olevan varaston summa ja täydennysvarasto (90 kpl) ylittää ylivuotomäärän 0,65 KL (tai 65 kpl). Myyntitilaus 3 on keräiltävä, ennen kuin täydennystyö voidaan viimeistellä.

1. Anna myyntitilauksen 3 työtunnus.

    Tällä työtunnuksella on vain yksi keräilytehtävä.

1. Valitse **OK**.

    **Myyntitilaukset: Keräily** -tehtävän sivulla ovat nimikenumero, määrä ja keräilysijainti.

1. Anna **RK**-kenttään sen nimikkeen rekisterinumero, jonka sijainti näytetään.

    Määritettävä rekisterikilpi tulee olemaan eräs järjestelmän luomista rekisterikilvistä täydennystyötehtävissä. Voit varmistaa, että tallennat oikean rekisterikilven tunnuksen, tarkistamalla varaston **Käytettävissä olevien luettelo** -sivulla nimikkeen, sijainnin ja määrän osalta.

1. Valitse **OK**-painike (valintamerkkisymboli).
1. Vahvista hyllytystehtävän ohjeet lähtevien väliaikaisessa sijainnissa.
1. Valitse **OK**.

    Näyttöön tulee Työ valmis -sanoma.

Heti, kun käytettävissä olevan varaston summa keräilysijainnissa ja täydennysmäärä ovat alle rajan, voit käsitellä jäljellä olevan täydennystyön.

Palaa **Työn tiedot** -sivulla ja ota huomioon, että täydennystyön käytettävyys täydennyksen viimeisessä osassa (myyntitilaukselle 2) on *Avoin*, koska sijainnissa on nyt tarpeeksi tilaa täydennyksen hyväksymiseksi.

Voit nyt käsitellä täydennystyötä mobiililaitteen kautta.

1. Siirry kohtaan **Varasto \> Täydennys**.

    Sinua pyydetään suorittamaan jäljellä oleva täydennystyö. Näkyvissä ovat nimiketunnus, määrä ja keräilysijainti.

1. Anna **RK**-kenttään sen nimikkeen rekisterinumero, jonka sijainti näytetään.
1. Valitse **OK**-painike (valintamerkkisymboli).

    Järjestelmä luo kohderekisterinumeron keräiltävän nimikkeen uudelle rekisterikilvelle.

1. Vahvista arvo valitsemalla **OK**.

    Näkyviin tulee työ, joka kehottaa käyttäjää asettamaan kohderekisterikilven täydennyssijaintiin. *Keräilysijainnin* on oltava **06A01R2S1B**.

1. Vahvista keräilyn tiedot ja valitse **OK**.

    Näyttöön tulee Työ valmis- ja Työtä ei saatavissa -viestit.

Seuraavaksi voit kerätä myyntitilauksen 2. Se vapautettiin, kun myyntitilaukseen linkitetty täydennystyö viimeisteltiin.

1. Anna myyntitilauksen 2 työtunnus.

    Tällä työtunnuksella on vain yksi keräilytehtävä.

1. Valitse **OK**.

    **Myyntitilaukset: Keräily** -tehtävän sivulla ovat nimikenumero, määrä ja keräilysijainti.

1. Anna **RK**-kenttään sen nimikkeen rekisterinumero, jonka sijainti näytetään.

    Määritettävä rekisterikilpi tulee olemaan järjestelmän luoma rekisterikilpi täydennystyötehtävässä. Voit varmistaa, että tallennat oikean rekisterikilven tunnuksen, tarkistamalla varaston **Käytettävissä olevien luettelo** -sivulla nimikkeen, sijainnin ja määrän osalta.

1. Valitse **OK**-painike (valintamerkkisymboli).
1. Vahvista hyllytystehtävän ohjeet lähtevien väliaikaisessa sijainnissa.
1. Valitse **OK**.

    Näyttöön tulee Työ valmis -sanoma.

## <a name="notes-and-tips"></a>Huomautuksia ja vihjeitä

- Tätä toimintoa voi käyttää kaikissa täydennystyypeissä, esimerkiksi aallon kysynnässä, vähimmäis- tai enimmäistäydennyksessä, kuorman kysynnässä ja paikoituksessa.
- Voit ohittaa halutessasi täydennystyön saatavuuden manuaalisesti jokaisen työotsikon kohdalla **Työn tiedot** -sivulla.
- Kun järjestelmä määrittää täydennystyön saatavuuden, se ottaa huomioon varaston, joka on jo sijainnissa ennen töiden valmistumista.
- Jokainen myyntitilaustyö on linkitetty tiettyyn täydennystyöhön. Vastaavaa myyntityön saatavuuden toimintoa ei ole.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]