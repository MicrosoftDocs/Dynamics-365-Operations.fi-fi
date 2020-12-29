---
title: Tuotteen valmius
description: Tässä aiheessa käsitellään valmiustarkistusten käyttöä varmistamaan, että tuotteen pakolliset päätiedot ovat valmiit, ennen kuin tuotetta käytetään tapahtumissa.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 58b5a35800ab464f25868c6756b16f25d14d8d78
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/29/2020
ms.locfileid: "4427529"
---
# <a name="product-readiness"></a>Tuotteen valmius

[!include [banner](../includes/banner.md)]

Valmiustarkistusten avulla varmistetaan, että tuotteen kaikki pakolliset päätiedot on määritetty, ennen kuin tuotetta käytetään tapahtumissa. Valmiustarkistuksia käytettäessä tietty käyttäjä tai ryhmä vastaa tiettyjen ennaltamääritettyjen tuotteeseen liittyvien tietojen tarkistamisesta. Jos tuotteella on avoin valmiustarkistus, tuotetta ei voi vapauttaa eikä käyttää tapahtumissa.

Suunnittelutuotteen, sen variantin tai version **Aktiivinen**-valintaruutu on käytettävissä vasta, kun kaikki pakolliset tiedot on annettu ja tarkistettu ja kaikki valmistustarkistukset on käsitelty. Tässä vaiheessa tuote, versio tai variantti voidaan vapauttaa muille yrityksille ja sitä voidaan käyttää tapahtumissa. Valmiustarkistuksia voidaan luoda uusille tuotteille, uusille varianteille ja uusille suunnitteluversioille.

## <a name="types-of-readiness-checks"></a>Valmiustarkistustyypit

Valmiustarkistuksia on kolme on eri tyyppiä:

- **Järjestelmätarkistus** – Järjestelmä tarkistaa, onko käytössä kelvollinen tietue. Tällainen tietue voi olla esimerkiksi aktiivinen tuoterakenne.
- **Manuaalinen tarkistus** – Käyttäjä tarkistaa tietueen kelpoisuuden. Valmiustarkistus voi esimerkiksi edellyttää tilauksen oletusasetusten vahvistamista. Joissakin tapauksissa tilauksen oletusasetuksia edellytetä. Tämä koskee esimerkiksi tilannetta, jossa tuotetta vielä suunnitellaan eikä sitä voi sen vuoksi olla varastossa. Tilauksen oletusasetuksia voidaan kuitenkin edellyttää toiselta samantyyppiseltä tuotteella, koska kyseistä tuotetta voidaan säilyttää varastossa. On käyttäjän vastuulla tietää, on valmiustarkistus pakollinen.
- **Tarkistusluettelo** – Käyttäjä vastaa tarkistusluettelon kysymyksiin ja järjestelmää määrittää, ovatko vastaukset odotetunkaltaisia. Tarkistusluettelon aiheita ei ole rajoitettu. Sen avulla voidaan esimerkiksi päätellä, onko markkinointimateriaali tai tuoteohjeistus valmis.

## <a name="how-readiness-checks-are-created-for-a-new-product-variant-or-version"></a>Uuden tuotteen, variantin tai version valmiustarkistusten luominen

Kun uutta suunnittelun **tuotetta** luodaan, järjestelmää selvittää, onko suunnittelun tuoteluokalle määritetty valmiustarkistuskäytäntö. (Valmiustarkistuskäytäntöjä voidaan käyttää vapautetun tuotteen tasolla, vapautetun variantin tasolla ja suunnitteluversion tasolla.) Jos käytäntö on määritetty, tuloksena on seuraavat tapahtumat:

- Tuotteelle luodaan käytettävän käytännön mukaiset valmiustarkistukset.
- Suunnitteluversio määritetään passiiviseksi, mikä estää tuotteen käytön. Kaikki kyseessä olevan tuotteen versiot määritetään passiivisiksi.

Jos tuotteelle luodaan uusi **variantti**, järjestelmä tarkistaa, onko suunnittelun tuoteluokassa määritetty valmiustarkistuksia. (Valmiustarkistuksia voidaan käyttää vapautetun variantin tasolla ja suunnitteluversion tasolla.) Jos valmiustarkistus on määritetty, tuloksena on seuraavat tapahtumat:

- Tuotteelle luodaan valmiustarkistukset.
- Suunnitteluversio määritetään passiiviseksi, mikä estää tuotteen käytön.

Jos tuotteelle luodaan uusi suunnittelun **versio**, järjestelmä tarkistaa, onko suunnittelun tuoteluokassa määritetty valmiustarkistuksia. (Valmiustarkistuksia voidaan käyttää suunnitteluversion tasolla.) Jos valmiustarkistus on määritetty, tuloksena on seuraavat tapahtumat:

- Tuotteelle luodaan valmiustarkistukset.
- Suunnitteluversio määritetään passiiviseksi, mikä estää tuotteen käytön.

## <a name="view-readiness-checks"></a>Valmiustarkistusten näyttäminen

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Tuotteen tai tuoteversion avoimien valmiustarkistusten näyttäminen

Etsi tuotteet avoimet valmiustarkistukset avaamalla **Vapautettujen tuotteiden tiedot** -sivu. Valitse sitten toimintoruudun **Tuote**-välilehden **Valmiustarkistukset**-ryhmässä **Valmiustarkistukset**.

Etsi tuoteversion avoimet valmiustarkistukset avaamalla vapatuetun tuotteen **Suunnitteluversiot**-sivu ja valitsemalla versio. Valitse sitten toimintoruudun **Tuote**-välilehden **Tarkistusluettelo**-ryhmässä **Valmiustarkistukset**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Sinulle määritettyjen avoimien valmiustarkistusten näyttäminen

Voit tarkastella sinulle määritettyjä avoimia valmiustarkistuksia jommallakummalla tavalla:

- Valitse **Suunnittelun muutostenhallinta \> Yleinen \> Tuotteen valmius \> Omat avoimet valmiustarkistukset**.
- Valitse **Tuotetietojen hallinta \> Työtilat \> Erillisen valmistuksen tuotteen valmius**.

Määritys, joka määrittää, kenelle valmiustarkistus määritetään, tehdään suunnittelun tuoteluokassa. Valmiustarkistukset voidaan määrittää henkilölle tai ryhmälle. Jos valmiustarkistus määritetään ryhmällä, yhden ryhmän henkilön on käsiteltävä valmiustarkistus. Lisätietoja on kohdassa [Suunnitteluversiot ja suunnittelun tuoteluokat](engineering-versions-product-category.md).

## <a name="process-open-readiness-checks"></a>Avoimien valmiustarkistusten käsitteleminen

### <a name="process-system-and-manual-readiness-checks"></a>Järjestelmän ja manuaalisten valmiustarkistusten käsitteleminen

Voit tarkastella avatulla **Valmiustarkistukset**-sivulla järjestelmän ja manuaalisten valmiustarkistuksen aiheita valitsemalla toimintoruudussa **Näytä liittyvät tiedot**. Voit sitten täydentää ja/tai tarkistaa valmiustarkistuksen tiedot. Avoimien valmiustarkistusten **Tila**-arvo on *Odottaa*. Tämä tila ilmaisee, että valmiustarkistus on vielä käsiteltävä. Voit käsitellä valmiustarkistuksen jommallakummalla tavalla:

- Tarkista ja suorita valmiustarkistus valitsemalla toimintoruudussa **Tarkista/suorita**. Kun olet valmis, **Tila**-kenttään päivittyy *Hyväksytty*.
- Valitse toimintoruudussa **Ohita**, jos haluat ohittaa valmiustarkistuksen, joka ei ole pakollinen. Esimerkki: Hintalaskelmille on määritetty valmiustarkistus. Päätät kuitenkin ohittaa tämän vaiheen, kun tuote on vielä suunnitteluvaiheessa. Tässä tapauksessa **Tila**-kenttään päivittyy *Ohitettu*.

Valmiuskäytännön määritysten mukaan valmiustarkistuksen **Tila**-kentän *Hyväksytty*-päivityksen jälkeen voidaan tarvitaan vielä erillinen valmiustarkistuksen hyväksymisvaihe. Valitse siinä tapauksessa valmiustarkistuksen lopuksi **Hyväksyntä**. Tämä hyväksyntävaihe on aina pakollinen, kun valmiustarkistus ohitetaan.

Kun kaikki uuden tuotteen, variantin tai version avoimet valmiustarkistukset on käsitelty ja tarvittaessa hyväksytty, nimike muuttuu automaattisesti aktiiviseksi ja on siten myös käytettävissä.

### <a name="process-checklist-readiness-checks"></a>Tarkistusluettelon valmiustarkistusten käsitteleminen

Avaa tarkistusluettelo avaamalla **Valmiustarkistukset**-sivu ja valitsemalla sitten toimintoruudussa **Käynnistä tarkistusluettelo**. Kun tarkistusluettelo on valmis, järjestelmä tarkistaa kyselylomakkeen asetusten perusteella, onko valmiustarkistus hyväksytty. Jos tarkistus hyväksytään, **Tila**-kenttään päivittyy *Hyväksytty*. Jos valmiustarkistus ei ole pakollinen, voit ohittaa sen. Tässä tapauksessa **Tila**-kenttään päivittyy *Ohitettu*.

Valmiuskäytännön määritysten mukaan valmiustarkistuksen **Tila**-kentän *Hyväksytty*-päivityksen jälkeen voidaan tarvitaan vielä erillinen valmiustarkistuksen hyväksymisvaihe. Valitse siinä tapauksessa valmiustarkistuksen lopuksi **Hyväksyntä**. Tämä hyväksyntävaihe on aina pakollinen, kun valmiustarkistus ohitetaan.

Kun kaikki uuden tuotteen, variantin tai version avoimet valmiustarkistukset on käsitelty ja tarvittaessa hyväksytty, nimike muuttuu automaattisesti aktiiviseksi ja on siten myös käytettävissä.

## <a name="create-and-manage-product-readiness-policies"></a>Tuotteen valmiuskäytäntöjen luominen ja hallinta

Tuotteen valmiuskäytäntöjen avulla voi hallita tuotteessa käytettäviä valmiustarkistuksia. Koska valmiuskäytäntö määritetään suunnittelun luokalle, kaikkia valmiuskäytännön tarkistuksia käytetään kaikissa suunnittelun luokkaan perustuvissa suunnittelutuotteissa. Lisätietoja on kohdassa [Suunnitteluversiot ja suunnittelun tuoteluokat](engineering-versions-product-category.md).

Kussakin valmiuskäytännössä on joukko valmiustarkistuksia. Kun valmiuskäytäntö määritetään suunnittelun tuoteluokalle, kaikissa suunnittelun tuoteluokasta luoduissa tuotteissa on valmiuskäytännössä ilmoitetut valmiustarkistukset.

Voit käyttää tuotteen valmiuskäytäntöjä valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Tuotteen valmiuskäytännöt**. Tee sitten jokin seuraavista:

- Luo uusi käytäntö valitsemalla toimintoruudussa **Uusi** ja määritä sitten kentät seuraavissa alaosissa kuvatulla tavalla.
- Muokkaa aiemmin luotua käytäntöä valitsemalla se luetteloruudussa ja sitten valitsemalla toimintoruudussa **Muokkaa**. Määritä sitten kentät seuraavissa alaosissa kuvatulla tavalla.
- Poista aiemmin luotu käytäntö valitsemalla se luetteloruudussa, valitsemalla toimintoruudussa **Muokkaa** ja varmistamalla sitten **Yleiset**-pikavälilehdessä, että **Aktiivinen**-asetuksena on *Ei*. Valitse lopuksi toimintoruudussa **Poista**.

### <a name="header"></a>Otsikko

Määritä seuraavat kentät suunnittelun valmiuskäytännön otsikossa.

| Kenttä | kuvaus |
|---|---|
| Nimi | Anna käytännön nimi. |
| kuvaus | Anna käytännön kuvaus. |

### <a name="general-fasttab"></a>Yleinen-pikavälilehti

Määritä seuraavat kentät suunnittelun valmiuskäytännön **Yleiset**-pikavälilehdessä.

| Kenttä | kuvaus |
|---|---|
| Tuotetyyppi | Valitse, käytetäänkö käytäntöä *Nimike*- vai *Palvelu*-tyypin tuotteissa. Tätä asetusta ei voi muuttaa tietueen tallentamisen jälkeen. |
| Aktiiviset | Tämän asetuksen avulla voi ylläpitää valmiuskäytäntöjä. Valitse *Kyllä* kaikille niille valmiuskäytännöille, joita käytät. Valitse *Ei* ilmaisemaan, että valmiuskäytäntö on passiivinen, kun sitä ei käytetä. Huomaa, että suunnittelun tuoteluokalle määritettyä valmiuskäytäntöä ei voi merkitä passiiviseksi ja että vain passiivisia vapautuskäytäntöjä voidaan poistaa. |

### <a name="readiness-control-fasttab"></a>Valmiuden hallinnan pikavälilehti

Lisää kullekin käytäntöön sisällytettävälle valmiustarkistustyypille rivi **Valmiuden hallinta** -pikavälilehteen. Lisää ja poista rivejä tarpeen mukaan seuraavilla pikavälilehden työkalurivin painikkeilla:

- **Lisää tarkistus** – Lisää vakiovalmiustarkistus käytäntöön. Kun valitset tämän painikkeen, **Lisää tarkistus** -valintaikkuna avautuu. Voit tehdä ikkunassa valinnat käytettävissä olevien tarkistusten luettelossa.
- **Lisää aiemmin luotu kyselylomake** – Lisää tyhjä rivi ruudukkoon. Voit sitten määrittää aiemmin luodun kyselylomakkeen määrittämällä seuraavassa taulukossa olevat kentät.
- **Kopioi** – lisää valitun rivin kopio ruudukkoon.
- **Poista** – poista valittu rivi ruudukosta.

Määritä seuraavat kentät jokaiselle lisättävälle riville.

| Kenttä | kuvaus |
| --- | --- |
| Prosessialue | Valitse alue, johon tarkistus liittyy. |
| Laji | Valitse, onko kyseessä järjestelmän tarkistus, manuaalinen tarkistus vai tarkistusluettelo (kyselylomake). |
| Nimi | Jos tarkistus on valintaluettelo, anna nimi. Tämä kenttä määritetään automaattisesti, jos kyse on järjestelmän tarkistuksesta tai manuaalisesta tarkistuksesta. |
| kuvaus | Jos tarkistus on valintaluettelo, anna kuvaus. Tämä kenttä määritetään automaattisesti, jos kyse on järjestelmän tarkistuksesta tai manuaalisesta tarkistuksesta, ja kuvaus selittää, mitä tarkistetaan. |
| Tarkistusten käyttökohde | Valitse, luoko rivi valmiustarkistuksia uudelle vapautetulle tuotteelle, vapautetulle variantille vai vapautetulle versiolle. |
| Suorita kohteessa | Valitse, käytetäänkö rivin luomia valmiustarkistuksia kaikissa yhtiöissä vai yhdessä yhtiössä. |
| Yhtiö | Jos **Suoritetaan kohteessa** -kentän asetuksena on *Yksi yhtiö*, valitse yhtiö. |
| Omistajan tyyppi | Valitse, määritetäänkö rivin luomat valmiustarkistukset henkilölle vain ryhmälle. |
| Omistaja | Valitse henkilö tai ryhmä, jolle rivin luomat valmiustarkistukset määritetään. |
| Kyselylomake | Valitse tarkistusluettelossa käytettävä kyselylomake. Tarkistusluettelon paikallinen tarkistusluettelo siinä yhtiössä, jossa valmiustarkistus tehdään. Järjestelmän on voitava arvioida kyselylomakkeessa annettujen vastausten oikeellisuus. Tämän vuoksi kyselylomake on määritettävä siten, että arviointi tehdään oikeiden vastausten perusteella. Lisätietoja kyselylomakkeiden luomisesta on kohdassa [Kyselylomakkeiden käyttäminen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/using-questionnaires) ja siihen liittyvissä aiheissa. |
| Automaattinen hyväksyntä | Valmiustarkistustietueissa on **Hyväksytty**-valintaruutu, joka ilmaisee hyväksynnän tilan. Valitse **Automaattinen hyväksyntä** -valintaruutu niissä tarkistuksissa, jotka on määritettävä hyväksytyiksi heti, kun määritetty käyttäjä on suorittanut ne. Poista tämän valintaruudun valinta, jos hyväksyntään tarvitaan erillinen lisävaihe. |
| Pakollinen | Valitse tämä valintaruutu tarkistuksissa, jotka määritetyn käyttäjän on tehtävä. Pakollisia tarkistuksia ei voi ohittaa. |
