---
title: Suunnittelumääritteet ja suunnittelumääritteen haku
description: Tässä aiheessa käsitellään suunnittelun määritteiden käyttämistä määrittämään kaikki muut kuin vakio-ominaisuudet. Näin voidaan varmistaa, että kaikki päätuotetiedot on rekisteröity järjestelmään. Siinä käsitellään myös suunnittelumääritteiden haun käyttämistä tuotteiden etsimiseen kyseisten rekisteröityjen ominaisuuksien perusteella.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2f8803e46ce6f104a5afee64faaf393a2df47a61
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568108"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a>Suunnittelumääritteet ja suunnittelumääritteen haku

[!include [banner](../includes/banner.md)]

Kaikkien päätuotetietojen rekisteröinti järjestelmään voidaan varmistaa määrittämällä kaikki muut kuin vakio-ominaisuudet suunnittelumääritteiden avulla. Sen jälkeen suunnittelumääritteiden haun avulla voi etsiä kätevästi tuotteita kyseisten rekisteröityjen ominaisuuksien perusteella.

## <a name="create-engineering-attributes-and-attribute-types"></a>Suunnittelun määritteiden ja määritetyyppien luominen

Yleensä suunnittelutuotteilla on monenlaisia ominaisuuksia, jotka on siepattava. Vaikka osa ominaisuuksista voidaan rekisteröidä vakiotuotekenttien avulla, tarvittaessa voidaan luoda myös uusia suunnitteluominaisuuksia. Omien *suunnittelun määritteiden* määrittäminen ja niiden käyttäminen tuotemääritelmän osana on mahdollista.

Kunkin suunnittelun määritteen on kuuluttava *määritetyyppiin*. Tätä edellytetään, koska kullakin suunnittelun määritteellä on oltava *tietotyyppi*, jolla määritetään siinä käytettävien tyyppien arvot. Suunnittelun määritetyyppi voi olla vakiotyyppi (kuten vapaateksti, kokonaisluku tai desimaali) tai mukautettu tyyppi (kuten teksti, jossa voi valita tiettyjä arvoja). Voit käyttää kutakin määritetyyppiä rajoittamattomassa määrässä suunnittelun määritteitä.

### <a name="set-up-engineering-attribute-types"></a>Suunnittelun määritetyyppien määrittäminen

Suunnittelun määritetyyppi näytetään, luodaan ja sitä muokataan seuraavasti:

1. Valitse **Suunnittelun muutostenhallinta \> Määritys \> Määritteet \> Määritetyypit**.
1. Valitse luetteloruudussa aiemmin luotu määritetyyppi tai luo uusi määritetyyppi valitsemalla toimintoruudussa **Uusi**.
1. Määritä seuraavat kentät:

    - **Määritetyypin nimi** – anna määritetyypin nimi.
    - **Tyyppi** – valitse vakiotietotyyppi (*Valuutta*, *Päivämäärä ja aika*, *Desimaali*, *Kokonaisluku*, *Teksti*, *Totuusarvo* tai *Viite*).
    - **Kiinteä luettelo** – Tämä vaihtoehto on käytettävissä vain, jos **Tyyppi**-kentän asetuksena on *Teksti*. Määritä tämän tyyppisen määritteen arvot valitsemalla *Kyllä*. Siinä tapauksessa luodaan avattava luettelo. **Arvo**-pikavälilehdessä voi luoda arvoja, joita voi käyttää tässä määritetyypissä. Valitse asetukseksi *Ei*, jos käyttäjä saa antaa minkä tahansa arvon. Siinä tapauksessa luodaan syöttökenttä.
    - **Arvoalue** – Tämä vaihtoehto on käytettävissä vain, jos **Tyyppi**-kentän asetuksena on *Kokonaisluku*, *Desimaali* tai *Valuutta*. Luo tässä määritetyypissä hyväksyttävät vähimmäis- ja enimmäisarvot valitsemalla asetukseksi *Kyllä*. Vähimmäis- ja enimmäisarvot määritetään **Alue**-pikavälilehdessä ja (valuutan osalta) valuutta, joka koskee annettuja rajoja. Määritä asetukseksi *Ei*, jos mikä tahansa arvo hyväksytään. 
    - **Mittayksikkö** – Tämä kenttä on käytettävissä vain, jos **Tyyppi**-kentän asetuksena on *Kokonaisluku* tai *Desimaali*. Valitse tässä määritetyypissä käytettävä mittayksikkö. Jos yksikköä ei tarvita, jätä kenttä tyhjäksi.

### <a name="set-up-engineering-attributes"></a>Suunnittelun määritteiden määrittäminen

Suunnittelun määrite näytetään, luodaan ja sitä muokataan seuraavasti:

1. Valitse **Suunnittelun muutostenhallinta \> Määritys \> Määritteet \> Suunnittelun määritteet**.
1. Valitse luetteloruudussa aiemmin luotu määrite tai luo uusi määrite valitsemalla toimintoruudussa **Uusi**.
1. Määritä seuraavat kentät:

    - **Nimi** – Anna määritteen nimi. Tämä nimi näkyy vain **Suunnittelun määritteet** -sivulla. Muualla järjestelmässä määrite tunnistetaan näyttämällä **Kutsumanimi**-kentän arvo.
    - **Määritetyyppi** – valitse edellisessä osassa määritetty määritetyyppi.
    - **Kutsumanimi** – anna nimi, jolla määrite tunnistetaan järjestelmässä (**Suunnittelun määritteet** -sivua lukuun ottamatta). 
    - **Kuvaus** – anna määritteen kuvaus.
    - **Ohjeteksti** – anna ohjeteksti, joka ilmaisee muille käyttäjille määritteen tarkoituksen.
    - **Oletusarvo** – Anna määritteen oletusarvo. Esillä olevat vaihtoehdot määräytyvät valitun määritetyypin mukaan.
    - **Valuutta** – jos valittu määritetyyppi on valuutta, valitse valuutta, jonka määrite hyväksyy ja jossa arvot näytetään.

1. Jos valittu määritetyyppi on kokonaisluku tai desimaali, **Alue**-pikavälilehti on näkyvissä. Määritä seuraavat kentät tarvittaessa tässä välilehdessä:

    - **Toleranssitoimenpide** – Valitse, miten järjestelmä reagoi, jos käyttäjä antaa annetun arvon ulkopuolisen arvon. Jos valitset *Varoitus*, varoitus näytetään mutta käyttäjä voi tallentaa arvon. Jos valitset *Ei sallittu*, varoitus näytetään eikä arvoa voi tallentaa, ennen kuin käyttäjä korjaa sen.
    - **Minimi** – anna pienin suositeltu tai hyväksytty arvo.
    - **Maksimi** – anna suurin suositeltu tai hyväksytty arvo.

### <a name="engineering-attribute-inheritance"></a>Määritteiden periytymisen suunnittelu

Tuoterakenteissa, kuten tuotantorakenteita tai resepteissä, valittuja määritteitä voidaan välittää alinimikkeistä päänimikkeeseen. Tämän prosessin voi ajatella olevan käänteisenä periytymisenä.

#### <a name="turn-on-this-feature-for-your-system"></a>Tämän ominaisuuden ottaminen käyttöön järjestelmällesi

Jos järjestelmäsi ei vielä sisällä tässä aiheessa osassa ominaisuuksia, avaa [Ominaisuuksienhallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota *Muutostenhallinnan suunnittelun parannettu määritteiden periytyminen* -ominaisuus käyttöön.

#### <a name="attribute-inheritance-example"></a>Esimerkki määritteiden periytymisestä

Porkkanakakun kaltaisen elintarviketuotteen osalta järjestelmän on tallennettava jokainen tuotteen sisältämä allergeeni. Porkkanakakku voidaan mallintaa järjestelmässä suunnittelutuotteena, jolla on resepti. Tämä resepti sisältää porkkanakakun ainesosat, kuten jauhot, maidon, porkkanat ja pähkinät. Tässä esimerkissä yrityksellä on kaksi porkkanakakun mallia: yksi laktoosia sisältävä ja yksi laktoositon.

Laktoosia sisältävällä kakulla on ainesosatasolla seuraavat määritteet:

- Ainesosa "jauho": määrite "gluteeni" = kyllä
- Ainesosa "maito": määrite "laktoosi" = kyllä
- Ainesosa "pähkinät": määrite "pähkinää" = kyllä

Laktoosittomassa kakussa käytetään laktoositonta maitoa, ja sillä on ainesosatasolla seuraavat määritteet:

- Ainesosa "jauho": määrite "gluteeni" = kyllä
- Ainesosa "maito": määrite "laktoosi" = ei
- Ainesosa "pähkinät": määrite "pähkinää" = kyllä

Koska tuotteet ovat pääosin samanlaisia, näiden määritteiden välittäminen aliversiolta (mainitut kaksi versiota) päätuotteeseen (perustason porkkanakakku). Tämän "käänteisen periytymisen" toteuttamiseen voi käyttää *Määritteen periytyminen* -ominaisuutta. Tämä toiminto määritetään kullekin [suunnitteluversiolle](engineering-versions-product-category.md).

## <a name="connect-engineering-attributes-to-an-engineering-product-category"></a>Suunnittelun määritteiden yhdistäminen suunnittelun tuoteluokkaan

Joitakin suunnittelun määritteitä käytetään kaikissa tuotteissa, kun taas toiset koskevat yksittäisiä tuotteita tai tuoteluokkia. Esimerkiksi sähkömääritteitä ei tarvita mekaanisissa tuotteissa. Tämän vuoksi voidaan määrittää *suunnittelun tuoteluokkia*. Suunnittelun tuoteluokka määrittää suunnittelun määritekokoelman, jonka on oltava kyseiseen luokkaan kuuluvien tuotteiden määritelmää. Voit määrittää myös, mitkä suunnittelun määritteet ovat pakollisia, ja mahdollisen oletusarvon.

Lisätietoja suunnittelun tuoteluokkien käyttämisestä sekä tietoja määritteiden yhdistämisestä luokkiin on kohdassa [Suunnitteluversiot ja suunnittelun tuoteluokat](engineering-versions-product-category.md).

## <a name="set-attribute-values-for-engineering-attributes"></a>Suunnittelun määritteiden määritearvojen määrittäminen

Suunnittelun tuoteluokkaan yhdistetyt suunnittelun määritteet ovat esillä, kun kyseiseen luokaan perustuva uusi suunnittelutuote luodaan. Tässä vaiheessa voidaan määrittää määritteiden arvot: Myöhemmin näitä arvoja voidaan muuttaa **Suunnitteluversio**-sivulla tai osana suunnittelun muutostenhallintaan suunnittelun muutostilauksessa. Lisätietoja on kohdassa [Suunnittelutuotteiden muutosten hallinta](engineering-change-management.md).

## <a name="create-an-engineering-product"></a>Suunnittelutuotteen luominen

Luo suunnittelutuote avaamalla **Vapautetut tuotteet** -sivu. Valitse sitten toimintoruudun **Tuote**-välilehden **Uusi**-ryhmässä **Suunnittelutuote**.

Suunnitteluluokka, johon tuote kuuluu, on määritettävä. Luokkaa määrittää kaikki tuotteen oletusarvot ja ominaisuudet. Se määrittää myös tuotteessa käytettävät määritteet. Kun luokka on valittu, määritteiden arvot määritetään. Näitä arvoja voi sitten muokata.

## <a name="search-for-products-by-using-engineering-attribute-values"></a>Tuotteiden haku suunnittelumääritteiden arvojen avulla

Suunnittelun määritehaulla voi etsiä tuotteita hakemalla niiden suunnittelumääritteiden arvoja. Tällä tavoin suunnittelutuotteita on helppo hakea ominaisuuksien perusteella. Haku voi kohdistua suunnittelun tuoteluokkaan kuuluviin tuotteisiin tai haku voi koskea kaikki suunnittelutuotteita.

Haku on käytettävissä päätuotetietosivuilla ja järjestelmän tapahtumanimikkeissä, kuten myyntitilauksissa. Tapahtumanimikkeessä tuotetta voi hakea **Tuotteen määritehaku** -sivulla. Voit sitten lisätä tuotteen myyntilauksen riveille käyttämällä **Lisää uutena rivinä** -painikkeella. Hakutulosten tuotteita voidaan lisätä tilaukseen myös suoraan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
