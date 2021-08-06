---
title: Tuotteen valmius
description: Tässä aiheessa käsitellään valmiustarkistusten käyttöä varmistamaan, että tuotteen pakolliset päätiedot ovat valmiit, ennen kuin tuotetta käytetään tapahtumissa.
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
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: ecffbfa00aee1dd3197aeeab3b292aba8aafd82f
ms.sourcegitcommit: 908a85987b604a7782407da70fb70ef75c07989f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/19/2021
ms.locfileid: "6641153"
---
# <a name="product-readiness"></a>Tuotteen valmius

[!include [banner](../includes/banner.md)]

Valmiustarkistusten avulla varmistetaan, että tuotteen kaikki pakolliset päätiedot on määritetty, ennen kuin tuotetta käytetään tapahtumissa. Valmiustarkistuksia käytettäessä tietty käyttäjä tai ryhmä vastaa tiettyjen ennaltamääritettyjen tuotteeseen liittyvien tietojen tarkistamisesta. Jos tuotteella on avoin valmiustarkistus, tuotetta ei voi vapauttaa eikä käyttää tapahtumissa.

Suunnittelutuotteen, sen variantin tai version **Aktiivinen**-valintaruutu on käytettävissä vasta, kun kaikki pakolliset tiedot on annettu ja tarkistettu ja kaikki valmistustarkistukset on käsitelty. Tässä vaiheessa tuote, versio tai variantti voidaan vapauttaa muille yrityksille ja sitä voidaan käyttää tapahtumissa. Valmiustarkistuksia voidaan luoda uusille tuotteille, uusille varianteille ja uusille suunnitteluversioille.

Voit myös käyttää valmiustarkistuksia vakiotuotteisiin (ei-tekninen suunnittelu). Lisätietoja on jäljempänä tässä ohjeaiheessa [Standardituotteiden valmiustarkistus](#standard-products) -osassa.

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
> Voit myös määrittää valmiustarkistuksia vakiotuotteille (ei-tekninen suunnittelu). Lisätietoja on jäljempänä tässä ohjeaiheessa [Standardituotteiden valmiustarkistus](#standard-products) -osassa.

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
| Kyselylomake | Valitse tarkistusluettelossa käytettävä kyselylomake. Tarkistusluettelon paikallinen tarkistusluettelo siinä yhtiössä, jossa valmiustarkistus tehdään. Järjestelmän on voitava arvioida kyselylomakkeessa annettujen vastausten oikeellisuus. Tämän vuoksi kyselylomake on määritettävä siten, että arviointi tehdään oikeiden vastausten perusteella. Lisätietoja kyselylomakkeiden luomisesta on kohdassa [Kyselylomakkeiden käyttäminen](/dynamicsax-2012/appuser-itpro/using-questionnaires) ja siihen liittyvissä aiheissa. |
| Automaattinen hyväksyntä | Valmiustarkistustietueissa on **Hyväksytty**-valintaruutu, joka ilmaisee hyväksynnän tilan. Valitse **Automaattinen hyväksyntä** -valintaruutu niissä tarkistuksissa, jotka on määritettävä hyväksytyiksi heti, kun määritetty käyttäjä on suorittanut ne. Poista tämän valintaruudun valinta, jos hyväksyntään tarvitaan erillinen lisävaihe. |
| Pakollinen | Valitse tämä valintaruutu tarkistuksissa, jotka määritetyn käyttäjän on tehtävä. Pakollisia tarkistuksia ei voi ohittaa. |

<a name="assign-policy"></a>

## <a name="assign-readiness-policies-to-standard-and-engineering-products"></a>Vakio- ja suunnittelutuotteiden valmiuskäytäntöjen määrittäminen

Kun luot uuden suunnitteluluokkaan perustuvan tuotteen, luot sekä *vapautetun tuotteen* että liittyvän *jaetun tuotteen*. Se, miten vapautetun tuotteen valmiuskäytännöt ratkaistaan, määräytyy sen mukaan, onko *tuotevalmiuden* tarkistustoiminto otettu käyttöön. (Lisätietoja on jäljempänä tässä ohjeaiheessa [Standardituotteiden valmiustarkistus](#standard-products) -osassa.)

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

### <a name="enable-readiness-checks-on-standard-products"></a>Vakiotuotteiden valmiustarkistusten käyttöönotto

Voit ottaa järjestelmän käyttöön vakiotuotteiden valmiustarkistuksen noudattamalla seuraavia ohjeita.

- Ota käyttöön Suunnittelun muutostenhallinta järjestelmässäsi, niin kuin aiheessa[Suunnittelun muutostenhallinnan yleiskatsaus](product-engineering-overview.md) on kuvattu.
- [Ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) avulla voit ottaa käyttöön toiminnon, jonka nimi on *Tuotevalmiuden tarkistus*.

<!-- KFM: This section requires confirmation before publishing

### How readiness checks are created for standard products

When you create a new non-engineering *released product*, the system determines whether a readiness check policy has been set up for the related shared product. If a policy has been set up, the following events occur:

- Readiness checks are created for the released product, according to the applicable policy.
- The released product is blocked from being used until all checks are marked as completed.

If a new *variant* is created for a product, the system checks whether readiness checks have been set up on the related shared product. If a readiness check has been set up, the following events occur:

- Readiness checks are created for the released product, according to the applicable policy.
- The released product is blocked from being used until all checks are marked as completed.

For engineering products, readiness checks are created in the same way that they are created when the *Product readiness checks* feature is turned off. For more information, see the [How readiness checks are created for a new engineering product, variant, or version](#checks-engineering) section earlier in this topic.

-->

### <a name="create-readiness-policies-for-standard-products"></a>Valmiuskäytäntöjen luominen vakiotuotteille

Luot valmiuskäytännöt vakiotuotteille aivan samoin kuin tuotteiden suunnittelussa. Tietoja on jo käsitelty aiemmin tässä aiheessa.

### <a name="assign-readiness-policies-to-standard-products"></a>Valmiuskäytäntöjen määrittäminen vakiotuotteille

Voit määrittää valmiuskäytännön vakiotuotteelle avaamalla liittyvän jaetun tuotteen ja määrittämällä **tuotteen valmiuskäytännön** kenttään sen käytännön nimen, jota on sovellettava. Lisätietoja on tämän ohjeaiheen aiemmassa kohdassa [Määritä valmiuskäytännöt vakio- ja suunnittelutuotteille](#assign-policy).

### <a name="view-and-process-readiness-checks-on-standard-products"></a>Vakiotuotteiden valmiustarkistusten tarkastelu ja käsittely

Kun tämä ominaisuus on käytössä, voit tarkastella ja käsitellä vakiotuotteiden valmiustarkistuksia aivan samoin kuin suunnittelutuotteessakin. Tietoja on jo käsitelty aiemmin tässä aiheessa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
