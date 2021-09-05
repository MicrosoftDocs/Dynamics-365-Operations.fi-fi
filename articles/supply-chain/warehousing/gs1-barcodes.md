---
title: GS1-viivakoodit ja QR-koodit
description: Tässä aiheessa käsitellään GS1-viivakoodien ja QR-koodien määrittämistä siten, että etiketit voidaan skannata varastossa.
author: Mirzaab
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ef28fcaf308225a78bcbac42f591e6b24b21b1b1
ms.sourcegitcommit: 2b04b5a5c883d216072bb91123f9c7709a41f69a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2021
ms.locfileid: "7384534"
---
# <a name="gs1-bar-codes-and-qr-codes"></a>GS1-viivakoodit ja QR-koodit

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Varastotyöntekijöiden on usein suoritettava useita tehtäviä, kun rekisteröivät nimikkeen, kuormalavan tai kontin liikkeitä mobiililaitteen skannerin avulla. Nämä tehtävät voivat sisältää sekä viivakoodien skannauksen että tietojen antamisen manuaalisesti mobiililaitteessa. Viivakoodeissa käytetään yrityskohtaista muotoa, joka määritetään ja jota hallitaan Microsoft Dynamics 365 Supply Chain Managementissa.

Osoitetarrojen GS1-viivakoodi- ja QR-koodimuodot kehitettiin tarjoamaan yleinen standardi yritysten väliseen tietojen vaihtoon. Tietojen koodaamisen lisäksi GS1-muotojen avulla tietojen merkitys voidaan määrittää käyttämällä esimääritettyä *sovellustunnisteiden* luetteloa. GS1-standardi määritetään tietomuodon ja erilaiset tiedot, joita voidaan koodata sen avulla. Aiemmista viivakoodeista poiketen GS1-viivakoodeissa voi olla useita tietoelementtejä. Niinpä yksi viivakoodiskannaus voi siepata erityyppisiä tuotetietoja, kuten erän ja vanhentumispäivän.

Supply Chain Management GS1-tuki yksinkertaistaa huomattavasti skannausprosessia varastoissa, joissa kuormalavojen ja konttien etiketeissä käytetään GS1-muotoisia koodeja. Varastotyöntekijät saavat kaiken tarvittavan tiedon yhdellä GS1-viivakoodin skannauksella. Koska useita skannauksia ja/tai tietojen manuaalista antamista ei tarvita, GS1-viivakoodit auttavat lyhentämään tehtäviin kuluvaa aikaa. Samalla myös tarkkuus paranee.

Logistiikkapäälliköiden on määritettävä pakollisten sovellustunnisteiden luettelo ja liittää kukin tunniste soveltuviin mobiililaitteen valikkovaihtoehtoon. Sovellustunnisteita voidaan käyttää koko varastossa yleisenä siirto- ja pakkausasetuksena. Näin ollen kaikkien osoitetarrojen muoto on yhtenäinen.

Ellei toisin mainita, *viivakoodi* viittaa tässä aiheessa sekä viivakoodeihin että QR-koodeihin.

## <a name="turn-on-the-gs1-feature"></a>GS1-toiminnon käyttöönotto

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *GS1-viivakoodien skannaus*

## <a name="set-up-global-gs1-options"></a>Yleisten GS1-asetusten määrittäminen

**Varastonhallinnan parametrit** -sivulla on muutamia yleiset GS1-asetukset muodostavia asetuksia.

Yleiset GS1-asetukset määritetään seuraavasti:

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
1. Määritä seuraavat kentät **Viivakoodit**-pikavälilehdessä:

    - **FNC1-merkki** – määritä merkit, jotka on käsiteltävä etuliitteenä viivakoodia jäsennettäessä.
    - **Tietomatriisin merkki** – määritä merkit, jotka on käsiteltävä etuliitteenä tietomatriisia jäsennettäessä.
    - **QR-koodin merkki** – määritä merkit, jotka on käsiteltävä etuliitteenä QR-koodia jäsennettäessä.
    - **Ryhmän erotin** – määritä merkki, joka tunnistaa viiva- tai QR-koodin erilliset osat.
    - **Tunnisteen enimmäispituus** – määritä sovellustunnisteen suurin sallittu merkkimäärä.

> [!NOTE]
> Etuliitteet ilmaisevat järjestelmälle, että viivakoodi on salattu GS1-standardin mukaisesti. Samanaikaisesti voi käyttää eri tarkoituksiin enintään kolmea etuliitettä (**FNC1-merkki**, **tietomatriisin merkki** ja **QR-koodin merkki**).

## <a name="gs1-application-identifiers"></a>GS1-sovellustunnisteet

Tietojen koodaamisen lisäksi GS1-muotojen avulla tietojen merkitys voidaan määrittää käyttämällä esimääritettyä sovellustunnisteiden luetteloa. Logistiikkapäälliköiden on määritettävä pakollisten sovellustunnisteiden luettelo ja liittää kukin tunniste soveltuviin mobiililaitteen valikkovaihtoehtoon. Tunnisteita voidaan sitten käyttää koko varastossa yleisenä siirto- ja pakkausasetuksena. Näin ollen kaikkien osoitetarrojen muoto on yhtenäinen.

Järjestelmä käyttää tietoja, etenkin esimääritettyjä sovellustunnisteita, sellaisten sääntöjen muodostamiseen, joita on käytettävä soveltuvaan skannattuun tietoon.

Kukin sovellustunniste ilmaisee järjestelmälle, että seuraavat skannatun viivakoodin merkit on katsottava salatuksi tietolohkoksi. Sovellustunnisteiden määritys määrittää, miten järjestelmä tulkitsee viivakoodin ja tallentaa sen arvona järjestelmään.

Logistiikkapäälliköt voivat käyttää kansainvälisiä vakiosovellustunnisteita ja/tai luoda omia tunnisteita.

### <a name="load-the-standard-application-identifiers"></a>Vakiosovellustunnisteiden lataaminen

Alkuun pääsee nopeasti lataamalla yleisten kansainvälisten sovellustunnisteiden luettelon. Luetteloa voi sitten tarvittaessa laajentaa tai muokata myöhemmin.

Vakiosovellustunnisteet ladataan seuraavasti:

1. Valitse **Varastonhallinta \> Määritys \> GS1 \> GS1-sovellustunnisteet**.
1. Valitse toimintoruudussa **Luo oletusasetukset**.

> [!WARNING]
> **Luo oletusasetus** -komento poistaa kaikki tällä hetkellä määritetyt sovellustunnisteet ja korvaa ne vakioluettelolla. Kun oletusasetus on ladattu, luetteloa voi kuitenkin mukauttaa tarpeen mukaan.

### <a name="set-up-custom-application-identifiers"></a>Mukautettujen sovellustunnisteiden määrittäminen

Jos jotkin tai kaikki yrityksen käyttämät sovellustunnisteet poikkeavat vakiotunnisteista, omat koodit voidaan luoda alusta alkaen tai vakiotunnisteita voidaan mukauttaa tarpeen mukaan.

Omat GS1-sovellustunnisteet määritetään tai niitä mukautetaan seuraavasti:

1. Valitse **Varastonhallinta \> Määritys \> GS1 \> GS1-sovellustunnisteet**.
1. Noudata seuraavia ohjeita:

    - Uuden tunnisteen luominen: valitse toimintoruudussa **Uusi**.
    - Aiemmin luodun tunnisteen muokkaaminen: valitse ensin tunniste ja valita sitten toimintoruudussa **Muokkaa**.

1. Määritä seuraavat uuden tai valitun tunnisteen kentät:

    - **Sovellustunniste** – Anna sovellustunnisteen tunnuskoodi. Tämä on koodi on yleensä kaksinumeroinen kokonaisluku, mutta se voi olla myös pidempi luku. Desimaaliarvoissa viimeinen numero ilmaiseen desimaalien määrän. Lisätietoja on myöhemmin tässä luettelossa **Desimaali**-valintaruudun kuvauksessa.
    - **Kuvaus** – anna tunnisteen lyhyt kuvaus.
    - **Kiinteä pituus** – Valitse tämä valintaruutu, jos tämän sovellustunnisteen avulla skannattavilla arvoilla on kiinteä merkkimäärä. Poista tämän valintaruudun valinta, jos arvojen pituus vaihtelee. Siinä tapauksessa arvon päättyminen on ilmaistava käyttämällä **Varastonhallinnan parametrit** -sivulla määritettyä ryhmän erotinmerkkiä.
    - **Pituus** – Anna suurin merkkimäärä, jota voidaan käyttää tämän sovellustunnisteen avulla skannattavissa arvoissa. Jos **Kiinteä pituus** -valintaruutu on valittu, odotusarvona on juuri kyseinen merkkimäärä.
    - **Tyyppi** – Valitse tämän sovellustunnisteen avulla skannattavan arvon tyyppi (*numeerinen*, *aakkosnumeerinen* tai *päivämäärä*). Päivämäärän muodon odotetaan olevan VVKKPP (ilman välilyöntejä tai välimerkkejä).
    - **Desimaali** – Valitse tämän valintaruutu, jos arvon katsotaan sisältävän desimaalitarkkuuden. Jos tämä ruutu valitaan, järjestelmä määrittää desimaalien määrän sovellustunnisteen viimeisen numeron perusteella. Jos sovellustunniste on esimerkiksi *3205*, arvon viisi oikeanpuolista numeroa tulkitaan olevan desimaalipilkun jälkeen.

> [!NOTE]
> **Varastonhallinnan parametrit** -sivulla määritetty ryhmän erotin on valinnainen, jos sovellustunnistetta edeltävän arvon pituus on kiinteä tai jos sen pituus vastaa enimmäispituutta (eli pituus on sama kuin sovellustunnisteelle määritetty **Pituus**-arvo).

## <a name="establish-the-generic-gs1-setup"></a>Yleisten GS1-asetusten määrittäminen

Yleisillä GS1-asetuksilla muodostetaan yleisten yhdistämismääritysten kokoelma. Nämä yhdistämismääritykset kohdistavat mobiilisovelluksen soveltuvat syöttökentät siihen sovellustunnisteeseen, joka määrittää, miten skannattujen viivakoodien kyseiseen kenttään tallennettuja arvoja tulkitaan. Oletusarvoisesti nämä asetukset koskevat kaikkien mobiililaitteen valikkovaihtoehtojen kaikkia skannauksia. Tietylle valikkovaihtoehdolle määritetty GS1-käytäntö voi kuitenkin korvata ne tietyissä kentissä.

Yleiset GS1-asetukset sallivat vain yhden arvon skannauksen kerralla. Niinpä jos yhdellä skannauksella halutaan ladata useita kentän arvoja, kyseisille valikkovaihtoehdoille on määritettävä GS1-käytäntö.

Lisätietoja GS1-käytännöistä on seuraavassa osassa.

### <a name="load-the-standard-generic-gs1-setup"></a>Yleisten GS1-vakioasetusten lataaminen

**Yleiset GS1-asetukset** -sivulla voi ladata vakiojoukon mobiililaitteen kenttien ja oletusmäärityksen luomien vakiosovellustunnisteiden välisiä yhdistämismäärityksiä.

Määritä yleiset GS1-asetukset valitsemalla **Varastonhallinta \> Määritys \> GS1 \> Yleiset GS1-asetukset**. Valitse sitten **Luo oletusasetus**, jolloin sopiva sovellustunniste määritetään automaattisesti kullekin kentälle, jota mobiililaitteen valikkovaihtoehdot tyypillisesti käyttävät.

> [!WARNING]
> Jos jokin yleinen GS1-asetus on määritetty jo aiemmin, **Luo oletusasetus** -komento poistaa sen kokonaan ja lataa vakioasetukset.

### <a name="customize-the-standard-generic-gs1-setup"></a>Yleisten GS1-vakioasetusten mukauttaminen

Yleisiä GS1-asetuksia mukautetaan seuraavasti:

1. Valitse **Varastonhallinta \> Määritys \> GS1 \> Yleiset GS1-asetukset**.
1. Noudata seuraavia ohjeita:

    - Uuden yhdistämismäärityksen luominen: valitse toimintoruudussa **Uusi**.
    - Aiemmin luodun yhdistämismäärityksen muokkaaminen: valitse ensin yhdistämismääritys ja valitse sitten toimintoruudussa **Muokkaa**.

1. Määritä seuraavat uuden tai valitun yhdistämismäärityksen kentät:

    - **Kenttä** – Valitse tai anna mobiilisovelluksen syöttökenttä, johon saapuva arvo on määritettävä. Arvo ei ole työntekijöiden näkemä näyttönimi. Sen sijaan se on sen avaimen nimi, joka on määritetty kenttään taustalla olevassa koodissa. Oletusmääritys sisältää kokoelman todennäköisesti hyödyllisiä kenttiä, ja kullakin kokoelman kentällä on intuitiivinen nimi ja vastaavat ohjelmoidut toiminnot. Omaan toteutukseen sopivista valinnoista kannattaa kuitenkin keskustella kehittäjäkumppanien kanssa.
    - **Sovellustunniste** – Valitse **GS1-sovellustunnisteet**-sivulla määritetty sopiva sovellustunniste. Tunniste määrittää, miten viivakoodia tulkitaan ja miten se tallennetaan nimetyn kentän arvona. Kun sovellustunniste on valittu, **Kuvaus**-kentässä on sen kuvaus.

## <a name="set-up-gs1-policies-that-you-can-assign-to-mobile-device-menu-items"></a>Mobiililaitteen valikkovaihtoehtoihin määritettävien GS1-käytäntöjen määrittäminen

GS1-vakio tarkoitus on antaa työntekijöille mahdollisuus ladata useita arvoja, kun he skannaavat kerran yhden viivakoodin. Jotta tämä olisi mahdollista, logistiikkapäälliköiden on määritettävä GS1-käytännöt ilmoittamaan järjestelmälle, miten useita arvoja sisältäviä viivakoodeja tulkitaan. Myöhemmin mobiililaitteen valikkovaihtoehtoihin voidaan määrittää käytäntöjä ohjaamaan viivakoodin tulkintaa, kun työntekijät skannaavat sen tietyn valikkovaihtoehdon käytön yhteydessä.

Jos valikkovaihtoehdolle ei ole määritetty GS1-käytäntöä, järjestelmä voi siepata vain yhden arvon. Arvoa käytetään siihen mobiilisovelluksen syötteeseen, joka on valittuna, kun työtekijä suorittaa skannauksen yleisten GS1-asetusten määrittämällä tavalla. Jos valikkovaihtoehtoon on määritetty GS1-käytäntö, järjestelmää käyttää edelleen yleisiä GS1-asetuksia ensimmäisen viivakoodin arvon yhdistämiseen valittuun kenttään. Tämän jälkeen se voi kuitenkin siepata lisää kentän arvoja käytettävän käytännön mukaisesti.

### <a name="load-the-standard-specific-gs1-policies"></a>Tiettyjen GS1-vakiokäytäntöjen lataaminen

Alkuun pääsee nopeasti lataamalla GS1-käytäntöjoukon. Käytäntöjä voi sitten tarvittaessa laajentaa tai muokata myöhemmin.

Vakiosovellustunnisteet ladataan seuraavasti:

1. Valitse **Varastonhallinta \> Määritys \> GS1 \> GS1-käytäntö**.
1. Valitse toimintoruudussa **Luo oletusasetukset**.

> [!WARNING]
> **Luo oletusasetus** -komento poistaa kaikki tällä hetkellä määritetyt käytännöt ja korvaa ne vakiokäytäntöjoukolla. Kun oletusasetus on ladattu, käytäntöjä voi kuitenkin mukauttaa tarpeen mukaan.

### <a name="set-up-custom-specific-gs1-policies"></a>Tiettyjen GS1-käytäntöjen mukauttaminen

GS1-käytäntöjä määritetään ja mukautetaan seuraavasti:

1. Valitse **Varastonhallinta \> Määritys \> GS1 \> GS1-käytäntö**.
1. Noudata seuraavia ohjeita:

    - Uuden käytännön luominen: valitse toimintoruudussa **Uusi**.
    - Aiemmin luodun käytännön muokkaaminen: valitse käytäntö luetteloruudussa.

1. Määritä uuden tai valitun käytännön otsikossa seuraavat kentät:

    - **Käytännön nimi** – annan käytännön nimi.
    - **Kuvaus** – anna käytännön lyhyt kuvaus.

1. Otsikon alla on pikavälilehti, jossa kentän nimet voidaan yhdistää sovellustunnisteisiin nykyisen käytännön edellyttämällä tavalla. Lisää ja poista rivejä tarpeen mukaan työkalurivin painikkeilla. Määritä kullekin riville seuraavat kentät:

    - **Kenttä** – Valitse tai anna mobiilisovelluksen syöttökenttä, johon saapuva arvo on määritettävä. Arvo ei ole työntekijöiden näkemä näyttönimi. Sen sijaan se on sen avaimen nimi, joka on määritetty kenttään taustalla olevassa koodissa. Oletusmääritys sisältää kokoelman todennäköisesti hyödyllisiä kenttiä, ja kullakin kokoelman kentällä on intuitiivinen nimi ja vastaavat ohjelmoidut toiminnot. Omaan toteutukseen sopivista valinnoista kannattaa kuitenkin keskustella kehittäjäkumppanien kanssa.
    - **Sovellustunniste** – Valitse **GS1-sovellustunnisteet**-sivulla määritetty sopiva sovellustunniste. Tunniste määrittää, miten viivakoodia tulkitaan ja miten se tallennetaan nimetyn kentän arvona. Kun sovellustunniste on valittu, **Kuvaus**-kentässä on sen kuvaus.
    - **Lajittelu** – Kussakin moniarvoisessa viivakoodissa on sovellustunnistesarja, joista kunkin perässä on arvo. Soveltuva GS1-käytäntö määrittää, mikä sovellustunniste määritetään kuhunkin tietokantakenttään. Jos viivakoodi kuitenkin käyttää samaa sovellustunnistetta useita kertoja, järjestelmä yhdistää sovellustunnisteet kenttiin siinä järjestyksessä, jossa ne ovat koodissa. Jos rivit jakavat sovellustunnisteen vähintään yhden muun rivin kanssa, muodosta tämän kentän avulla järjestys, jossa vastaavat rivit käsitellään. Rivi, jonka lajitteluarvo on pienin, käsitellään ensimmäisenä.

> [!NOTE]
> Jos viivakoodissa halutaan käyttää useampaa kuin yhtä samaa sovellustunnistetta, kenttien järjestys *on* muodostettava **Lajittelu**-kentän avulla.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>GS1-käytäntöjen määrittäminen mobiililaitteen valikkovaihtoehtoihin.

Kaikissa mobiililaitteen valikkovaihtoehtoissa on oletusarvoisesti syötekentät, joissa työntekijät voivat skannata yhden arvon yleisten GS1-asetusten mukaisesti. Jos halutaan, että työntekijät voivat skannata useita kentän arvoja yhdellä mobiililaitteen valikkovaihtoehdon skannauksella, GS1-käytäntö on määritettävä seuraavasti:

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Luo tai avaa valikkovaihtoehto.
1. Määritä **Yleinen**-pikavälilehden **GS1-käytäntö**-kentässä käytäntö, jota käytetään valikkovaihtoehdossa.

## <a name="gs1-setup-example"></a>GS1-määritysesimerkki

Tämä esimerkki koskee järjestelmää, jossa GS1-asetukset on määritetty seuraavasti:

- **Varastonhallinnan parametrit** -sivulla on määritetty seuraavat yleiset asetukset:

  - **FNC1-merkki:** *\]C1*
  - **Ryhmäerotin:** *\~*

- Seuraavat sovellustunnisteet koskevat tätä esimerkkiä **GS1-sovellustunnisteet**-sivulla:

    | Sovellustunniste | kuvaus | Kiinteä pituus | Pituus | Laji | Desimaali |
    |---|---|---|---|---|---|
    | 01 | GTIN | Valittu | 14 | Numeerinen | Selvitetyt |
    | 10 | Eränumero | Selvitetyt | 20 | Aakkosnumeerinen | Selvitetyt |
    | 17 | Erääntymispäivä | Valittu | 6 | Päivämäärä | Selvitetyt |
    | 30 | Vastaanottava määrä | Selvitetyt | 8 | Numeerinen | Selvitetyt |

- Seuraavat **Yleiset GS1-asetukset** -sivun yleisen GS1-käytännön asetukset koskevat tätä esimerkkiä.

    | Kenttä | Sovellustunniste | kuvaus |
    |---|---|---|
    | ItemId | 01 | GTIN |

- **GS1-käytäntö**-sivulla on käytäntö, jossa **Käytännön nimi** -kentän määrityksenä on *Ostojen vastaanotto*. Tämä käytäntö sisältää seuraavat rivit:

    | Kenttä | Sovellustunniste | kuvaus | Lajittelu |
    |---|---|---|---|
    | ExpDate | 17 | Erääntymispäivä | 0 |
    | InventBatchId | 10 | Eränumero | 0 |
    | Määrä | 30 | Vastaanottava määrä | 0 |

- **Mobiililaitteen valikkovaihtoehdot** -sivulla on valikkovaihtoehto, jonka nimi on *Ostojen vastaanotto*. **GS1-käytäntö**-kentän määrityksenä on *Ostojen vastaanotto*.

Kun ostotilauksen tavarat saapuvat varastoon, työntekijä toimii seuraavasti:

1. Valitse mobiililaitteessa **Ostojen vastaanotto** -valikkovaihtoehto.
1. Anna ostotilauksen numero.
1. Valitse **Nimike**-kenttä ja skannaa seuraava viivakoodi: *\]C10100000012345678\~3030\~10b1\~17220215*.

Tätä esimerkkiä varten muodostettujen asetusten perusteella järjestelmä jäsentää skannatun viivakoodin seuraavasti:

| Kentän avain | Sovelluksen tunnus | Arvo | Seteli |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Koska työntekijä skannasi **Kohde**-kenttään, viivakoodin ensin arvo yhdistetään kyseiseen kenttään. Tämä yhdistämismääritys haetaan yleisistä GS1-asetuksista. |
| Määrä | 30 | 30 | Koska yhdellä skannauksella siepataan useita kentän arvoja, tämä yhdistämismääritys ja kaikki jäljellä olevat yhdistämismääritykset haetaan GS1-käytännöstä, joka on määritetty **Ostojen vastaanotto** -valikkovaihtoehtoon. Tämä arvo on vastaanotettu määrä. |
| InventBatchId | 10 | b1 | Tämä arvo on erän tunnus. |
| ExpDate | 17 | 220215 | Päivämäärän muoto on VVKKPP. Vanhenemispäivämäärä onkin sen vuoksi 15. helmikuuta 2022. |

Vastaanotto rekisteröidään sitten, ja soveltuvat tietokanta-arvot annetaan yhden skannauksen jälkeen.
