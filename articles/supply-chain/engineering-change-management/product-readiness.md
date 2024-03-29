---
title: Tuotteen valmius
description: Tässä artikkelissa käsitellään valmiustarkistusten käyttöä varmistamaan, että tuotteen pakolliset päätiedot ovat valmiit, ennen kuin tuotetta käytetään tapahtumissa.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a8e76d5fc786b6f4cac7cd0430399ca3ad13a7bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856219"
---
# <a name="product-readiness"></a>Tuotteen valmius

[!include [banner](../includes/banner.md)]

Valmiustarkistusten avulla varmistetaan, että tuotteen kaikki pakolliset päätiedot on määritetty, ennen kuin tuotetta käytetään tapahtumissa. Valmiustarkistuksia käytettäessä tietty käyttäjä tai ryhmä vastaa tiettyjen ennaltamääritettyjen tuotteeseen liittyvien tietojen tarkistamisesta.

Voit merkitä suunnittelutuotteen, sen variantin tai version **Aktiivinen**-valintaruudun, kun kaikki pakolliset tiedot on annettu ja tarkistettu ja kaikki valmistustarkistukset on käsitelty. Jos vähintään yksi tarkistus on tekemättä tuotteelle, sen versiolle tai sen variantille, yrittäessäsi merkitä **Aktiivinen**-valintaruutua tulee näkyviin kehote, joka varoittaa siitä, ettei kaikkia tarkistuksia ole tehty.

Valmiustarkistuksia voidaan luoda uusille suunnittelutuotteille, varianteille ja uusille versioille. Voit tehdä valmisutarkistuksia myös vakiotuotteille eli muille kuin suunnittelutuotteille (katso myös [Vakiotuotteiden valmiustarkistukset](#standard-products)). 

Voit käyttää vakiotuotteita tapahtumissa, vaikka kaikki valmiustarkistukset eivät olisi valmiit. Jos haluat estää tuotteen käytön tapahtumissa, käytä sen elinkaaren tilaa. Voit määrittää elinkaaren tilan, joka estää tuotteen käyttämisen tapahtumissa ja sitten, kun valmiustarkistukset ovat valmiit, määrittää uuden elinkaaren tilan, joka sallii tarvittavat tapahtumat.

## <a name="types-of-readiness-checks"></a>Valmiustarkistustyypit

Valmiustarkistuksia on kolme on eri tyyppiä:

- **Järjestelmätarkistus** – Järjestelmä tarkistaa, onko käytössä kelvollinen tietue. Tällainen tietue voi olla esimerkiksi aktiivinen tuoterakenne.
- **Manuaalinen tarkistus** – Käyttäjä tarkistaa tietueen kelpoisuuden. Valmiustarkistus voi esimerkiksi edellyttää tilauksen oletusasetusten vahvistamista. Joissakin tapauksissa tilauksen oletusasetuksia edellytetä. Tämä koskee esimerkiksi tilannetta, jossa tuotetta vielä suunnitellaan eikä sitä voi sen vuoksi olla varastossa. Tilauksen oletusasetuksia voidaan kuitenkin edellyttää toiselta samantyyppiseltä tuotteella, koska kyseistä tuotetta voidaan säilyttää varastossa. On käyttäjän vastuulla tietää, on valmiustarkistus pakollinen.
- **Tarkistusluettelo** – Käyttäjä vastaa tarkistusluettelon kysymyksiin ja järjestelmää määrittää, ovatko vastaukset odotetunkaltaisia. Tarkistusluettelon aiheita ei ole rajoitettu. Sen avulla voidaan esimerkiksi päätellä, onko markkinointimateriaali tai tuoteohjeistus valmis.

<a name="checks-engineering"></a>

## <a name="how-readiness-checks-are-created-for-a-new-engineering-product-variant-or-version"></a>Uuden teknisen tuotteen, variantin tai version valmiustarkistusten luominen

Valmiustarkistuskäytäntöjä voidaan käyttää vapautetun tuotteen tasolla, vapautetun variantin tasolla ja suunnitteluversion tasolla.

Kun luot uuden *suunnittelutuotteen*, järjestelmä määrittää, onko [valmiustarkistuskäytäntö käytössä](#assign-policy). Jos käytössä on valmiustarkistuskäytäntö, seuraavat tapahtumat tapahtuvat:

- Tuotteelle luodaan käytettävän käytännön mukaiset valmiustarkistukset.
- Suunnitteluversio määritetään passiiviseksi, mikä estää tuotteen käytön. Kaikki tuotteen suunnitteluversiot on määritetty passiivisiksi.

Jos tuotteelle luodaan uusi *muuttuja*, järjestelmä tarkistaa, koskeeko valmiustarkistuskäytäntö tuotetta. (Valmiustarkistuksia voidaan käyttää vapautetun variantin tasolla ja suunnitteluversion tasolla.) Jos käytäntö koskee sitä, tuloksena on seuraavat tapahtumat:

- Tuotteelle luodaan käytettävän käytännön mukaiset valmiustarkistukset.
- Suunnitteluversio ja variantti määritetään passiiviseksi, mikä estää tuotteen käytön.

Jos suunnittelutuotteelle luodaan uusi *versio*, järjestelmä tarkistaa, koskeeko valmiustarkistuskäytäntö tuotetta. (Valmiustarkistuksia voidaan käyttää suunnitteluversion tasolla.) Jos käytäntö koskee sitä, tuloksena on seuraavat tapahtumat:

- Tuotteelle luodaan käytettävän käytännön mukaiset valmiustarkistukset.
- Suunnitteluversio määritetään passiiviseksi, mikä estää tuotteen käytön.

> [!NOTE]
> Voit myös määrittää valmiustarkistuksia vakiotuotteille (ei-tekninen suunnittelu). Lisätietoja on jäljempänä tässä artikkelissa [Standardituotteiden valmiustarkistus](#standard-products) -osassa.

## <a name="view-readiness-checks"></a>Valmiustarkistusten näyttäminen

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Tuotteen tai tuoteversion avoimien valmiustarkistusten näyttäminen

Etsi tuotteet avoimet valmiustarkistukset avaamalla **Vapautettujen tuotteiden tiedot** -sivu. Valitse sitten toimintoruudun **Tuote**-välilehden **Valmiustarkistukset**-ryhmässä **Valmiustarkistukset**.

Etsi tuoteversion avoimet valmiustarkistukset avaamalla vapatuetun tuotteen **Suunnitteluversiot**-sivu ja valitsemalla versio. Valitse sitten toimintoruudun **Tuote**-välilehden **Tarkistusluettelo**-ryhmässä **Valmiustarkistukset**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Sinulle määritettyjen avoimien valmiustarkistusten näyttäminen

Voit tarkastella sinulle määritettyjä avoimia valmiustarkistuksia jommallakummalla tavalla:

- Valitse **Suunnittelun muutostenhallinta \> Yleinen \> Tuotteen valmius \> Omat avoimet valmiustarkistukset**.
- Valitse **Tuotetietojen hallinta \> Työtilat \> Erillisen valmistuksen tuotteen valmius**.

Määritys, joka määrittää, kenelle valmiustarkistus määritetään, tehdään valmiuskäytäntöön. Valmiustarkistukset voidaan määrittää henkilölle tai ryhmälle. Jos valmiustarkistus määritetään ryhmällä, yhden ryhmän henkilön on käsiteltävä valmiustarkistus.

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

Tuotteen valmiuskäytäntöjen avulla voi hallita tuotteessa käytettäviä valmiustarkistuksia. Kussakin valmiuskäytännössä on joukko valmiustarkistuksia. Kun valmiuskäytäntö määritetään suunnittelun tuoteluokalle tai jaetulle tuotteelle, kaikilla kyseiseen luokkaan tai jaettuihin tuotteisiin liittyvillä tuotteilla on valmiustarkastukset, jotka sisältyvät valmiuskäytäntöön.

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
| Aktiiviset | Tämän asetuksen avulla voi ylläpitää valmiuskäytäntöjä. Valitse *Kyllä* kaikille niille valmiuskäytännöille, joita käytät. Valitse *Ei* ilmaisemaan, että valmiuskäytäntö on passiivinen, kun sitä ei käytetä. Huomaa, että suunnittelun tuoteluokalle tai jaetulle tuotteelle määritettyä valmiuskäytäntöä ei voi merkitä passiiviseksi ja että vain passiivisia vapautuskäytäntöjä voidaan poistaa. |

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
| Kyselylomake | Valitse tarkistusluettelossa käytettävä kyselylomake. Tarkistusluettelon paikallinen tarkistusluettelo siinä yhtiössä, jossa valmiustarkistus tehdään. Järjestelmän on voitava arvioida kyselylomakkeessa annettujen vastausten oikeellisuus. Tämän vuoksi kyselylomake on määritettävä siten, että arviointi tehdään oikeiden vastausten perusteella. Lisätietoja kyselylomakkeiden luomisesta on kohdassa [Kyselylomakkeiden käyttäminen](/dynamicsax-2012/appuser-itpro/using-questionnaires) ja siihen liittyvissä artikkeleissa. |
| Automaattinen hyväksyntä | Valmiustarkistustietueissa on **Hyväksytty**-valintaruutu, joka ilmaisee hyväksynnän tilan. Valitse **Automaattinen hyväksyntä** -valintaruutu niissä tarkistuksissa, jotka on määritettävä hyväksytyiksi heti, kun määritetty käyttäjä on suorittanut ne. Poista tämän valintaruudun valinta, jos hyväksyntään tarvitaan erillinen lisävaihe. |
| Pakollinen | Valitse tämä valintaruutu tarkistuksissa, jotka määritetyn käyttäjän on tehtävä. Pakollisia tarkistuksia ei voi ohittaa. |

<a name="assign-policy"></a>

## <a name="assign-readiness-policies-to-standard-and-engineering-products"></a>Vakio- ja suunnittelutuotteiden valmiuskäytäntöjen määrittäminen

Kun luot uuden suunnitteluluokkaan perustuvan tuotteen, luot sekä *vapautetun tuotteen* että liittyvän *jaetun tuotteen*. Tapa, jolla valmiuskäytännöt ratkaistaan vapautetun tuotteen osalta, määräytyy sen mukaan, onko *Tuotteen valmiustarkistukset* -toiminto käytössä järjestelmässäsi (katso osasta [Vakiotuotteiden valmiustarkistukset](#standard-products) jäljempänä tässä artikkelissa tietoja tästä toiminnosta ja siitä, miten se otetaan käyttöön ja poistetaan käytöstä).

- Kun *tuotevalmiuden tarkistus* -toiminto on *poistettu käytöstä* järjestelmässä, valmiuskäytäntö määritetään ja näkyy vain [suunnitteluluokan](engineering-versions-product-category.md) tietueissa. Jos haluat tietää, mitä menettelyä vapautettavaan tuotteeseen liittyy, järjestelmä tarkistaa liittyvän suunnitteluluokan **Tuotevalmiuskäytäntö**-kentän. Voit muuttaa olemassa olevan tuotteen valmiuskäytäntöä muokkaamalla siihen liittyvää suunnitteluluokkaa (ei jaettua tuotetta).
- Kun *tuotevalmiuden tarkistus* -toiminto on *käytössä*, se lisää **tuotevalmiuskäytännön** kentän **tuote**-sivulle (jossa yhteiset tuotteet on määritetty) ja **vapautetun tuotteen** sivulle (jossa arvo on vain luku ja otetaan liittyvästä jaetusta tuotteesta). Järjestelmä löytää vapautetun tuotteen valmiuskäytännön tarkistamalla liittyvän jaetun tuotteen. Kun luot uuden suunnittelutuotteen käyttämällä suunnitteluluokkaa, järjestelmä luo sekä jaetun tuotteen että vapautetun tuotteen sekä kopioi uuteen jaettuun tuotteeseen suunnitteluluokan **tuotevalmiuden käytäntö** -asetuksen. Voit sitten muuttaa olemassa olevan tuotteen valmiuskäytäntöä muokkaamalla siihen liittyvää jaettua tuotetta (ei vapautettua suunnitteluluokkaa).

Valmiuskäytäntö määritetään jaetulle tuotteelle seuraavasti:

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotteet**.
1. Avaa tai luo tuote, jolle haluat määrittää valmiuskäytännön.
1. Määritä **Yleiset**-pikavälilehdessä **Tuotteen valmius -käytäntö** -kenttään tuotteeseen sovellettavan käytännön nimi.

Valmiuskäytäntö määritetään tuotesuunnitteluluokalle seuraavasti:

1. Valitse **Suunnittelun muutostenhallinta \> Määritys \> Suunnittelun tuoteluokan tiedot**.
1. Avaa tai luo suunnittelun tuoteluokka, jolle haluat määrittää valmiuskäytännön.
1. Määritä **Tuotteen valmiuskäytäntö**-pikavälilehdessä **Tuotteen valmiuskäytäntö** -kenttään suunnittelutuoteluokkaan sovellettavan käytännön nimi.

<a name="standard-products"></a>

## <a name="readiness-checks-on-standard-products"></a>Vakiotuotteiden valmiustarkistukset

Voit ottaa käyttöön tuotteiden valmiustarkistukset vakiotuotteille (ei-suunnittelu) ottamalla *tuotevalmiuden tarkistukset* -ominaisuus käyttöön toiminnonhallinnassa. Tämän ominaisuuden avulla valmiustarkistusjärjestelmään tehdään muutamia muutoksia, jotta se tukee vakiotuotteita.

### <a name="enable-or-disable-readiness-checks-on-standard-products"></a>Vakiotuotteiden valmiustarkistusten käyttöönotto tai käytöstä poistaminen

Tämä toiminto edellyttää, että toiminnot *Suunnittelun muutosten hallinta* ja *Tuotteen valmiustarkistukset* ovat käytössä järjestelmässäsi. Tietoja näiden toimintojen ottamisesta käyttöön tai pois käytöstä: [Suunnittelun muutostenhallinnan yleiskuvaus](product-engineering-overview.md).

### <a name="create-readiness-policies-for-standard-products"></a>Valmiuskäytäntöjen luominen vakiotuotteille

Luot valmiuskäytännöt vakiotuotteille aivan samoin kuin tuotteiden suunnittelussa. Tietoja on jo käsitelty aiemmin tässä artikkelissa.

### <a name="assign-readiness-policies-to-standard-products"></a>Valmiuskäytäntöjen määrittäminen vakiotuotteille

Voit määrittää valmiuskäytännön vakiotuotteelle avaamalla liittyvän jaetun tuotteen ja määrittämällä **tuotteen valmiuskäytännön** kenttään sen käytännön nimen, jota on sovellettava. Lisätietoja on tämän artikkelin aiemmassa kohdassa [Määritä valmiuskäytännöt vakio- ja suunnittelutuotteille](#assign-policy).

### <a name="view-and-process-readiness-checks-on-standard-products"></a>Vakiotuotteiden valmiustarkistusten tarkastelu ja käsittely

Kun tämä ominaisuus on käytössä, voit tarkastella ja käsitellä vakiotuotteiden valmiustarkistuksia aivan samoin kuin suunnittelutuotteessakin. Tietoja on jo käsitelty aiemmin tässä artikkelissa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
