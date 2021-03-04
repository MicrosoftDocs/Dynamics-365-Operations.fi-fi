---
title: Tuoterakenteiden vapauttaminen
description: Tässä aiheessa käsitellään täydellisten tuoterakenteiden vapauttamista tuotteiden ja niiden suunnitteluversioiden vapauttamisen ohella. Tällä tavoin voidaan varmistaa, että suunnitteluun liittyviä tuotetietoja voidaan käyttää uudelleen eri yrityksissä.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductReleaseSiteBulkEdit, EngChgProductReleaseSendListPage, EngChgProductReleaseSendDetails,EngChgProductReleaseSelection,EngChgProductReleaseReceiveListPage, EngChgProductReleaseReceiveDetails, EngChgProductReleasePreviewPane, EngChgProductReleasePolicy, EngChgProductReleasePart, EngChgProductReleaseNote
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 68f091cca9c3c2baa03813553127ee41abe6d522
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/29/2020
ms.locfileid: "4427528"
---
# <a name="release-product-structures"></a>Tuoterakenteiden vapauttaminen

[!include [banner](../includes/banner.md)]

Suunnitteluun liittyvien tuotetietojen helppo uudelleenkäyttäminen eri yrityksissä voidaan varmistaa, kun tuotteiden ja niiden suunnitteluversioiden ohella vapautetaan myös täydelliset tuoterakenteet. Tällä tavoin voidaan vapauttaa monitasoisia tuoterakenteita yhdessä päärakenteen kanssa käyttämällä yhtä vapautustoimintona. Tässä tapauksessa vapautetaan myös tuoterakenne ja alatason tuotteet.

Suunnitteluyritys luo ja ylläpitää suunnittelutuotteita siten, että ne vastaavat suunnittelunaikaisia laatuvaatimuksia. Jokainen tuotetta valmistava operatiivinen yritys tarvitsee saman tuotteet ja tuoterakenteen, johon se perustuu. Tuotantolaitos määrittää, luodaanko reitti paikallisesti. Siinä tapauksessa reittiä ei vapauteta yhdessä tuotteen kanssa. Tuoterakenne ei ehkä ole välttämätön yrityksissä, jotka myyvät mutta eivät valmista tuotteita.

Prosessia voi tehostaa vapauttamalla kaikki suunnitteluun liittyvät tiedot muille operatiivisille yrityksille samanaikaisesti. Nämä tiedot sisältävät tuoterakenteen. Vapautusprosessin aikana voidaan valita, mikä osa tuotetiedoista vapautetaan.

Lisätietoja suunnitteluyrityksistä ja operatiivista yrityksistä on kohdassa [Suunnitteluyritykset ja tietojen omistussäännöt](engineering-org-data-ownership-rules.md).

Huomaa, että sekä vakiotuotteita että suunnittelutuotteita voi vapauttaa yhdessä vapautetun tuoterakenteen kanssa. Tämän prosessin aikana voidaan vapauttaa koko tuoterakenne; siis myös tuoterakenne ja reitti yrityksestä, joissa tuotteita vapautetaan.

Esimerkki tuotteen vapauttamisesta on kohdassa [Suunnittelutuotteen vapauttaminen paikalliseen yritykseen](engineering-scenarios.md#release)

## <a name="released-data-for-a-product-when-the-release-product-structure-is-used"></a>Tuotteen vapautetut tiedot käytettäessä vapautettua tuoterakennetta

Suunnittelun tietojen vapautus sisältää seuraavat tiedot:

- **Tuotetiedot** – uusi vapautettu tuote luodaan.
- **Suunnitteluversion tiedot** – Suunnitteluversio ja sen tiedot luodaan tai päivitetään. Huomaa, että jos sama suunnitteluversio vapautetaan uudelleen operatiiviseen yritykseen, suunnittelun tiedot korvataan.
- **Suunnittelumääritteet** – suunnittelumääritteet ja niiden arvot luodaan tai päivitetään.
- **Suunnittelun tuoterakenne** – Suunnittelun tuoterakenne ja sen rivit voidaan luoda tai päivittää. Lisätietoja tuotteen omistuksesta on kohdassa [Tuotteen omistajat](product-owner.md).
- **Suunnittelureitit** – Suunnittelureitit ja niiden toiminnot voidaan luoda tai päivittää. Lisätietoja tuotteen omistuksesta on kohdassa [Tuotteen omistajat](product-owner.md).
- **Suunnitteluasiakirjat** – luotuun tai päivitettävään suunnitteluversioon liittyvät suunnitteluasiakirjat.

Kun suunnittelun muutostenhallinta otetaan järjestelmässä käyttöön, vapautettu tuoterakenne on käytettävissä. Vapautettavat vakiotuotteet sisältävät lisäksi tuoterakenteet ja reitit.

## <a name="product-acceptance"></a>Tuotteen hyväksyntä

**Tuotteen hyväksyntä** on keskeinen vapautusprosessiin vaikuttava parametri. Tämä parametri voidaan määrittää kullekin yritykselle valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Suunnittelun muutostenhallinnan parametrit**. Lisätietoja on kohdassa [Suunnittelun muutostenhallinnan parametrit](engineering-parameters.md).

### <a name="automatic-product-acceptance"></a>Automaattinen tuotteen hyväksyntä

Jokainen suunnittelutuotteiden vapautus alkaa sillä, että joku suunnitteluyrityksessä valitse vapautettavan tuotteen. Kun **Tuotteen hyväksyntä** -parametrina on *Automaattinen*, käyttäjä päättää suunnitteluyrityksessä, mitkä suunnittelutiedot vapautetaan automaattisesti operatiivisille yrityksille. Tuote vapautetaan sitten automaattisesti ohjatussa vapautustoiminnossa valituille yrityksille.

### <a name="manual-product-acceptance"></a>Manuaalinen tuotteen hyväksyntä

Jokainen suunnittelutuotteiden vapautus alkaa sillä, että joku suunnitteluyrityksessä valitse vapautettavan tuotteen. Kun **Tuotteen hyväksyntä** -parametrina on *Manuaalinen*, käyttäjä päättää suunnitteluyrityksessä, mitkä suunnittelutiedot vapautetaan operatiivisille yrityksille. Käyttäjä tarkistaa sitten kussakin operatiivisessa yrityksessä tuotteen tiedot ja päättää, hyväksytäänkö vapautus. Operatiivisen yrityksen käyttäjä voi määrittää seuraavat asetukset, kun tiedot vastaanotetaan:

- Jos tuotteet (päivitykset) eivät liity operatiiviseen yritykseen, käyttäjä voi päättää olla hyväksymättä vapautusta.
- Käyttäjä voi muuttaa uusien tuotteiden nimikemallia.
- Käyttäjä voi valita, vapautetaanko tuote yhdessä tuoterakenteen ja/tai reittien kanssa sekä vapautetaanko se hyväksyttynä ja aktiivisena.
- Käyttäjä voi muuttaa tuotteiden voimassaolon alkamispäivämääriä.

Esimerkki tuotteen hyväksymisestä on kohdassa [Tuotteen tarkistaminen ja hyväksyminen ennen vapauttamista paikalliselle yhtiölle](engineering-scenarios.md#accept).

> [!NOTE]
> Vakiotuotteet voidaan vapauttaa mistä tahansa yrityksestä mihin tahansa muuhun yritykseen. Suunnittelutuotteen voi vapauttaa vain suunnitteluyrityksestä.

## <a name="release-policies"></a>Vapautuskäytännöt

Kaikki operatiiviset yritykset eivät tarvitse samoja tuotetietoja. Yleisesti ottaen suunnittelutuotteita valmistavat operatiiviset yritykset tarvitsevat tuoterakenteen, kun taas suunnittelutuotteita ainoastaan myyvät operatiiviset yritykset eivät tarvitse tuoterakennetta. Voit muodostaa vapautuskäytäntöjen avulla parametreja, joita käytetään tuotteiden vapauttamisessa.

Suunnittelutuotteiden vapautuskäytäntö määritetään suunnittelun tuoteluokassa, ja kenttä on pakollinen. Vakiotuotteiden osalta käytäntö määritetään jaettuun tuotteeseen, ja kenttä on valinnainen.

Lisätietoja suunnittelun tuoteluokista on kohdassa [Suunnitteluversiot ja suunnittelun tuoteluokat](engineering-versions-product-category.md).

Asetuksia voi muokata vapautusprosessin aikana.

## <a name="create-and-manage-product-release-policies"></a>Tuotteen vapautuskäytäntöjen luominen ja hallinta

Voit käyttää tuotteen vapautuskäytäntöjä valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Tuotteen vapautuskäytännöt**. Tee sitten jokin seuraavista:

- Luo uusi käytäntö valitsemalla toimintoruudussa **Uusi** ja määritä sitten kentät seuraavissa alaosissa kuvatulla tavalla.
- Muokkaa aiemmin luotua käytäntöä valitsemalla se luetteloruudussa ja sitten valitsemalla toimintoruudussa **Muokkaa**. Määritä sitten kentät seuraavissa alaosissa kuvatulla tavalla.
- Poista aiemmin luotu käytäntö valitsemalla se luetteloruudussa, valitsemalla toimintoruudussa **Muokkaa** ja varmistamalla sitten **Yleiset**-pikavälilehdessä, että **Aktiivinen**-asetuksena on *Ei*. Valitse lopuksi toimintoruudussa **Poista**.

### <a name="header"></a>Otsikko

Määritä seuraavat kentät tuotteen vapautuskäytännön otsikossa.

| Kenttä | kuvaus |
|---|---|
| Nimi | Anna käytännön nimi. |
| kuvaus | Anna käytännön kuvaus. |

### <a name="general-fasttab"></a>Yleinen-pikavälilehti

Määritä seuraavat kentät tuotteen vapautuskäytännön **Yleiset**-pikavälilehdessä.

| Kenttä | kuvaus |
|---|---|
| Tuotetyyppi | Valitse, käytetäänkö käytäntöä *Nimike*- vai *Palvelu*-tyypin tuotteissa. Tätä asetusta ei voi muuttaa tietueen tallentamisen jälkeen. |
| Käytä malleja | Määritä jollakin seuraavalla asetuksella, käytetäänkö tuotevapautusmalleja ja miten niitä käytetään, kun käytäntö on käytössä:<ul><li>**Aina** – Mallivapautustuote, jota on aina käytettävä vapautuksessa. Jos valitset tämän asetuksen, määritä **Kaikki tuotteet** -pikavälilehdessä malli, jota käytetään kussakin yrityksessä, johon vapautus tehdään. Jos kullekin **Kaikki tuotteet** -pikavälilehden luettelossa olevalle yritykselle ei määritetä mallia, käytäntöä tallennettaessa saadaan virhe.</li><li>**Valinnainen** – Jos mallivapautustuote määritetään **Kaikki tuotteet** -pikavälilehden luettelossa olevalle yritykselle, kyseistä mallia käytetään, kun vapautus tehdään kyseiseen yritykseen. Muussa tapauksessa mallia ei käytetä. Jos valitse tämän asetuksen, voit tallentaa käytännön ilman, että mallit määritetään kaikille yrityksille. (Varoitusta ei näytetä.)</li><li>**Ei koskaan** – Mallivapautustuotetta ei käytetä missään yrityksessä, johon vapautus tehdään, vaikka malli olisi määritetty **Kaikki tuotteet** -pikavälilehden luettelossa oleville yrityksille. Mallisarakkeet eivät ole käytettävissä.</li></ul> |
| Aktiiviset | Tämän asetuksen avulla voi ylläpitää vapautuskäytäntöjä. Valitse *Kyllä* kaikille niille vapautuskäytännöille, joita käytät. Valitse *Ei* ilmaisemaan, että vapautuskäytäntö on passiivinen, kun sitä ei käytetä. Huomaa, että suunnittelun tuoteluokalle määritettyä vapautuskäytäntöä ei voi merkitä passiiviseksi ja että vain passiivisia vapautuskäytäntöjä voidaan poistaa. |

### <a name="all-products-fasttab"></a>Kaikki tuotteet -pikavälilehti

Lisää **Kaikki tuotteet** -pikavälilehdessä riville kullekin operatiiviselle yritykselle, johon vapauttamiseen haluat käyttää tätä käytäntöä. Lisää ja poista rivejä tarpeen mukaan **Kaikki tuotteet** -pikavälilehden painikkeilla. Määritä seuraavat kentät jokaiselle lisättävälle riville.

> [!NOTE]
> **Kaikki tuotteet** -pikavälilehden asetukset koskevat sekä suunnittelu- että vakiotuotteita.

| Kenttä | kuvaus |
|---|---|
| Yrityksen tilien tunnus | Valitse yritys, jota rivi koskee. Rivin parametreja käytetään, kun tuotteet vapautetaan tähän yritykseen. |
| Vapautettu mallituote | Lisää tuotteen malli. |
| Kopioi tuoterakenteen hyväksyntä | Kopioi tuoterakenteen hyväksynnän tilan vastaanottavaan yritykseen valitsemalla tämä valintaruutu. |
| Kopioi tuoterakenteen aktivointi | Kopioi tuoterakenteen aktivoinnin tilan vastaanottavaan yritykseen valitsemalla tämä valintaruutu. |
| Kopioi reitin hyväksyntä | Kopioi reitin hyväksynnän tilan vastaanottavaan yritykseen valitsemalla tämä valintaruutu.|
| Kopioi reitityksen aktivointi | Kopioi reitin aktivoinnin tilan vastaanottavaan yritykseen valitsemalla tämä valintaruutu. |

### <a name="option-parameters-for-engineering-products-fasttab"></a>Suunnittelutuotteiden asetuksen parametrit -pikavälilehti

Aina kun **Kaikki tuotteet** -pikavälilehteen lisätään rivi, myös **Suunnittelutuotteiden asetuksen parametrit** -pikavälilehteen luodaan rivi, jolla on vastaava **Yritystilien tunnus** -arvo. Jos **Kaikki tuotteet** -pikavälilehdestä sitten poistetaan rivi, myös **Suunnittelutuotteiden asetuksen parametrit** -pikavälilehdestä poistetaan rivi, jolla on vastaava **Yritystilien tunnus** -arvo.

Määritä jokaiselle **Suunnittelutuotteiden asetuksen parametrit** -pikavälilehdessä näkyvälle riville seuraavat kentät.

> [!NOTE]
> **Suunnittelutuotteiden asetuksen parametrit** -pikavälilehden asetukset koskevat vain suunnittelutuotteita.

| Kenttä | kuvaus |
|---|---|
| Mallituoterakenne | Kun tuoterakenteen sisältävä tuote vapautetaan, määrityn mallituoterakenteen rivit lisätään. Tämä kenttä on kätevä lisättäessä paikallisia osia, kuten paikallista kieltä käyttävä pakkaus tai ohjeet. |
| Mallin reitti | Kun reitin sisältävä tuote vapautetaan, määrityn mallin rivit lisätään. |
| Kopioi voimassaolo | Valitse, kopioidaanko voimassaolopäivät suunnitteluyrityksestä toiminnalliseen yritykseen tuotteiden vapautuksen yhteydessä. |
| Lisää automaattisesti vapautusehdotukseen | Valitse tämä valintaruutu suunnittelun muutostilauksessa tuotteille, jotka on vapautettava automaattisesti. Tällä tavoin tuotteet, jotka kuuluvat tätä vapautuskäytäntöä käyttäviin suunnittelun tuoteluokkiin, voidaan vapauttaa automaattisesti operatiivisiin yrityksiin, joissa tämä asetus on määritetty. (Lisätietoja on kohdassa [Suunnittelutuotteiden muutosten hallinta](engineering-change-management.md).)

### <a name="review-each-product-when-you-release-it"></a>Jokaisen tuotteen tarkistaminen vapautuksen yhteydessä

Kun tuoterakenteita tai reittejä sisältävät suunnittelutuotteet vapautetaan, parametrit määritetään oletusarvoiksi vapautuskäytännön mukaisesti. Käyttäjä voi vaikuttaa tähän toimintaan vapauttavana osapuolena, kun käytössä on tuoterakenteen vapauttaminen.

Suunnittelutuotteet vapautetaan valitsemalla **Vapautetut tuotteet** -sivulla ensin vapautettava tuote ja avaamalla sitten ohjattu vapautus toiminto valitsemalla **Vapauta tuoterakenne**. Tuotteet näkyvät **Valitse vapautettavat suunnittelutuotteet** -sivulla. Valitse yksi tuote ja tarkista sitten kyseisen tuotteen vapautustiedot valitsemalla **Vapautuksen tiedot**.

Voit muuttaa **Vapautuksen tiedot** -sivulla **Vastaanoton tuoterakenne**-, **Kopioi tuoterakenteen hyväksyntä**-, **Kopioi tuoterakenteen aktivointi**-, **Vastaanoton tuoterakenne**-, **Kopioi reitin hyväksyntä**- ja **Kopioi reitin aktivointi** -kenttien arvon. Vuorovaiheskenaariossa samojen kenttien arvon voi muuttaa vastaanoton puolella, mikäli tuoterakenne ja reitti on vapautettu.

## <a name="product-owners-and-product-releases"></a>Tuotteen omistajat ja tuotteen vapautukset

Koska tuotteen omistajat tietävät, mitkä yritykset tarvitsevat heidän tuotteitaan, vain kyseisen tuotteen tuotteen omistajaryhmän jäsenet voivat vapauttaa tuotteen. Muut käyttäjät eivät voi vapauttaa tuotteita, joita he eivät omista.

Tämä toiminta on käytössä vain, kun tuote valitaan suoraan vapautukseen. Muut kuin omistajakäyttävät *voivat* vapauttaa tuotteet, jotka ovat osa toisen tuotteen rakennetta tuoterakenteen kautta, kun päätuote vapautetaan. Tämä on mahdollisista siinä tapauksessa, että he omistavat päätuotteen.

Tuote X on esimerkiksi määritetty *Design-kaiuttimet*-tuotteen omistajaryhmään. Tuote X on myös tuotteen Y tuoterakenteen osa, ja tuote Y on määritetty *Design-kaiuttimet*-tuotteen omistajaryhmään. Jos *Design-kaiuttimet*-tuotteen omistajaryhmä vapauttaa tuotteen Y ja sen tuoterakenteen, tuote X vapautetaan yhdessä tuotteen Y kanssa.

Lisätietoja on kohdassa [Tuotteen omistajat](product-owner.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]