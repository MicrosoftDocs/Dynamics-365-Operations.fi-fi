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
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 01752bfc9bab662064baf30635ae6879358c5bbe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830073"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a>Suunnittelumääritteet ja suunnittelumääritteen haku

[!include [banner](../includes/banner.md)]

Kaikkien päätuotetietojen rekisteröinti järjestelmään voidaan varmistaa määrittämällä kaikki muut kuin vakio-ominaisuudet suunnittelumääritteiden avulla. Sen jälkeen suunnittelumääritteiden haun avulla voi etsiä kätevästi tuotteita kyseisten rekisteröityjen ominaisuuksien perusteella.

## <a name="engineering-attributes"></a>Suunnittelun määritteet

Yleensä suunnittelutuotteilla on monenlaisia ominaisuuksia, jotka on siepattava. Vaikka osa ominaisuuksista voidaan rekisteröidä vakiotuotekenttien avulla, tarvittaessa voidaan luoda myös uusia suunnitteluominaisuuksia. Omien *suunnittelun määritteiden* määrittäminen ja niiden käyttäminen tuotemääritelmän osana on mahdollista.

### <a name="create-engineering-attributes-and-attribute-types"></a>Suunnittelun määritteiden ja määritetyyppien luominen

Kunkin suunnittelun määritteen on kuuluttava *määritetyyppiin*. Tätä edellytetään, koska kullakin suunnittelun määritteellä on oltava *tietotyyppi*, jolla määritetään siinä käytettävien tyyppien arvot. Suunnittelun määritetyyppi voi olla vakiotyyppi (kuten vapaateksti, kokonaisluku tai desimaali) tai mukautettu tyyppi (kuten teksti, jossa voi valita tiettyjä arvoja). Voit käyttää kutakin määritetyyppiä rajoittamattomassa määrässä suunnittelun määritteitä.

#### <a name="set-up-engineering-attribute-types"></a>Suunnittelun määritetyyppien määrittäminen

Suunnittelun määritetyyppi näytetään, luodaan ja sitä muokataan seuraavasti:

1. Valitse **Suunnittelun muutostenhallinta \> Määritys \> Määritteet \> Määritetyypit**.
1. Valitse luetteloruudussa aiemmin luotu määritetyyppi tai luo uusi määritetyyppi valitsemalla toimintoruudussa **Uusi**.
1. Määritä seuraavat kentät:

    - **Määritetyypin nimi** – anna määritetyypin nimi.
    - **Tyyppi** – valitse vakiotietotyyppi (*Valuutta*, *Päivämäärä ja aika*, *Desimaali*, *Kokonaisluku*, *Teksti*, *Totuusarvo* tai *Viite*).
    - **Kiinteä luettelo** – Tämä vaihtoehto on käytettävissä vain, jos **Tyyppi**-kentän asetuksena on *Teksti*. Määritä tämän tyyppisen määritteen arvot valitsemalla *Kyllä*. Siinä tapauksessa luodaan avattava luettelo. **Arvo**-pikavälilehdessä voi luoda arvoja, joita voi käyttää tässä määritetyypissä. Valitse asetukseksi *Ei*, jos käyttäjä saa antaa minkä tahansa arvon. Siinä tapauksessa luodaan syöttökenttä.
    - **Arvoalue** – Tämä vaihtoehto on käytettävissä vain, jos **Tyyppi**-kentän asetuksena on *Kokonaisluku*, *Desimaali* tai *Valuutta*. Luo tässä määritetyypissä hyväksyttävät vähimmäis- ja enimmäisarvot valitsemalla asetukseksi *Kyllä*. Vähimmäis- ja enimmäisarvot määritetään **Alue**-pikavälilehdessä ja (valuutan osalta) valuutta, joka koskee annettuja rajoja. Määritä asetukseksi *Ei*, jos mikä tahansa arvo hyväksytään. 
    - **Mittayksikkö** – Tämä kenttä on käytettävissä vain, jos **Tyyppi**-kentän asetuksena on *Kokonaisluku* tai *Desimaali*. Valitse tässä määritetyypissä käytettävä mittayksikkö. Jos yksikköä ei tarvita, jätä kenttä tyhjäksi.

#### <a name="set-up-engineering-attributes"></a>Suunnittelun määritteiden määrittäminen

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

### <a name="connect-engineering-attributes-to-an-engineering-product-category"></a>Suunnittelun määritteiden yhdistäminen suunnittelun tuoteluokkaan

Joitakin suunnittelun määritteitä käytetään kaikissa tuotteissa, kun taas toiset koskevat yksittäisiä tuotteita tai tuoteluokkia. Esimerkiksi sähkömääritteitä ei tarvita mekaanisissa tuotteissa. Tämän vuoksi voidaan määrittää *suunnittelun tuoteluokkia*. Suunnittelun tuoteluokka määrittää suunnittelun määritekokoelman, jonka on oltava kyseiseen luokkaan kuuluvien tuotteiden määritelmää. Voit määrittää myös, mitkä suunnittelun määritteet ovat pakollisia, ja mahdollisen oletusarvon.

Lisätietoja suunnittelun tuoteluokkien käyttämisestä sekä tietoja määritteiden yhdistämisestä luokkiin on kohdassa [Suunnitteluversiot ja suunnittelun tuoteluokat](engineering-versions-product-category.md).

### <a name="set-values-for-engineering-attributes"></a>Suunnittelun määritteiden arvojen määrittäminen

Suunnittelun tuoteluokkaan yhdistetyt suunnittelun määritteet ovat esillä, kun kyseiseen luokaan perustuva uusi suunnittelutuote luodaan. Tässä vaiheessa voidaan määrittää määritteiden arvot: Myöhemmin näitä arvoja voidaan muuttaa **Suunnitteluversio**-sivulla tai osana suunnittelun muutostenhallintaan suunnittelun muutostilauksessa. Lisätietoja on kohdassa [Suunnittelutuotteiden muutosten hallinta](engineering-change-management.md).

### <a name="create-an-engineering-product"></a>Suunnittelutuotteen luominen

Luo suunnittelutuote avaamalla **Vapautetut tuotteet** -sivu. Valitse sitten toimintoruudun **Tuote**-välilehden **Uusi**-ryhmässä **Suunnittelutuote**.

Suunnitteluluokka, johon tuote kuuluu, on määritettävä. Luokkaa määrittää kaikki tuotteen oletusarvot ja ominaisuudet. Se määrittää myös tuotteessa käytettävät määritteet. Kun luokka on valittu, määritteiden arvot määritetään. Näitä arvoja voi sitten muokata.

## <a name="search-for-products-by-using-engineering-attribute-values"></a>Tuotteiden haku suunnittelumääritteiden arvojen avulla

Suunnittelun määritehaulla voi etsiä tuotteita hakemalla niiden suunnittelumääritteiden arvoja. Tällä tavoin suunnittelutuotteita on helppo hakea ominaisuuksien perusteella. Haku voi kohdistua suunnittelun tuoteluokkaan kuuluviin tuotteisiin tai haku voi koskea kaikki suunnittelutuotteita.

Haku on käytettävissä päätuotetietosivuilla ja järjestelmän tapahtumanimikkeissä, kuten myyntitilauksissa. Tapahtumanimikkeessä tuotetta voi hakea **Tuotteen määritehaku** -sivulla. Voit sitten lisätä tuotteen myyntilauksen riveille käyttämällä **Lisää uutena rivinä** -painikkeella. Hakutulosten tuotteita voidaan lisätä tilaukseen myös suoraan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]