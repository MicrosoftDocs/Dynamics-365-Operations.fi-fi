---
title: Suunnittelutuotteiden muutostenhallinta
description: Tässä aiheessa on tietoja suunnittelun muutostenhallinnasta. Suunnittelun muutostenhallinnassa on jäsennettyjä prosesseja suunnittelutuotteiden muutostenhallintaan muutosten ehdottamisesta, pyytämisestä ja tekemisestä muutosten tarkistamiseen ja hyväksymiseen sekä niiden vaikutuksen arvioimiseen aiemmin luoduissa tapahtumissa ja muutosten seurantaan.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcmRequestSelection,EngChgEcmRequestProducts,EngChgEcmRequestPriorityChart,EngChgEcmRequestListPage,EngChgEcmRequestFilteredPart,EngChgEcmRequestDetails,EngChgEcmReason,EngChgEcmProjTableInformation,EngChgEcmProductRoute,EngChgEcmProductRelease,EngChgEcmProductPreview, EngChgEcmWhereUsed, EngChgEcmInventTrans,EngChgEcmHeaderSelection,EngChgEcmHeaderPreviewPart,EngChgEcmHeaderFilteredPart,EngChgEcmHeaderDetails, EngChgCaseWhereUsedAnalysis, EngChgCaseValidatorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8ae97d0e6aac1b0961427bd73a37612020231a9f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983797"
---
# <a name="manage-changes-to-engineering-products"></a>Suunnittelutuotteiden muutostenhallinta

[!include [banner](../includes/banner.md)]

Suunnittelun muutostenhallinnassa on jäsennettyjä prosesseja suunnittelutuotteiden muutosten hallintaan. Voit käyttää *suunnittelun muutoksen pyytämisprosessia* muutosten ehdottamiseen ja pyytämiseen ja käyttää sitten *suunnittelun muutoksen tilausprosessia* kyseisten muutosten tekemiseen. Käyttäjät voivat luoda suunnittelun muutospyyntöjä ja suunnittelun muutostilauksia. Tämän jälkeen käytössä on prosessi näiden muutosten tarkistamiseen ja hyväksymiseen, niiden vaikutusten arvioimiseen aiemmin luotuihin tapahtumiin sekä muutosten seurantaan.

## <a name="engineering-change-requests"></a>Suunnittelun muutospyynnöt

Suunnittelun muutoksen pyyntöprosessilla voidaan siepata kaikkien soveltuvien yrityksen osastojen muutospyynnöt. Kuka tahansa voi pyytää muutosta käyttämällä suunnittelun muutospyyntöä riippumatta siitä, onko työpaikka suunnittelu-, valmistus-, hankinta-, varasto- tai myyntiosastolla. Kyseinen muutos voi olla uusi tuoteidea, ongelma, joka löytyi nykyistä tuotetta käytettäessä, nykyisen tuotteen parannusehdotus tai jotain aivan muuta.

Kun joku lähettää muutospyynnön, *tarkistus- ja hyväksyntäprosessia* hallitaan työnkululla, joka määrittää muutoksen hyväksyjän (kuten tuotteen omistajan).

Suunnittelun muutostilausten tai muutospyyntöjen työnkulku määritetään valitsemalla **Suunnittelun muutostenhallinta \> Suunnittelun työnkulut**. Valitse ensin **Uusi** ja sitten käytetäänkö työnkulkua tarkistamaan suunnittelun muutostilauksia vai suunnittelun muutospyyntöjä. Vahvista työnkulku lopuksi.

Lisätietoja työnkulkujen käyttämisestä on kohdassa [Työnkulkujärjestelmän yleiskatsaus](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) Lisätietoja tuotteen omistajista on kohdassa [Tuotteen omistajat](product-owner.md).

### <a name="create-a-new-engineering-change-request"></a>Luo uusi suunnittelun muutospyyntö

Suunnittelun muutospyyntö luodaan jollakin seuraavalla tavalla:

- Valitse ensin **Suunnittelun muutostenhallinta \> Yleinen \> Suunnittelun muutostenhallinta \> Suunnittelun muutospyynnöt** ja valitse toimintoruudussa **Uusi**.
- Avaa aiemmin luodun suunnittelutuotteen **Tuotteen tiedot** -sivu. Valitse sitten toimintoruudussa **Suunnittelu**-välilehden **Suunnittelun muutostenhallinta** -ryhmässä **Suunnittelun muutospyyntö \> Uusi suunnittelun muutospyyntö**.

Uusi muutospyyntö luodaan. Voit määrittää kunkin pikavälilehden asetukset seuraavissa alaosissa kuvatulla tavalla.

#### <a name="general-fasttab"></a>Yleinen-pikavälilehti

**Yleinen**-pikavälilehdessä voi antaa muutospyynnön peruskuvauksen. Seuraavassa taulukossa käsitellään tämän pikavälilehden kentät.

| Kenttä | kuvaus |
|---|---|
| Muutospyyntö | Anna suunnittelun muutospyynnön nimi. |
| Titteli | Kirjoita teksti, joka kuvaa tai määrittää lyhyesti pyynnön muutokset. |
| Prioriteetti | Valitse arvo, joka ilmaisee muutoksen prioriteetin. Voit mukauttaa yrityksen käytettävissä olevia arvoja tarpeen mukaan. (Lisätietoja on kohdassa [Suunnittelun muutostenhallinnan yleisten arvojen luominen](engineering-change-management-setup.md).) |
| Luokka | Valitse arvo, joka kuvaa pyydetyn muutoksen tyyppiä. Voit mukauttaa yrityksen käytettävissä olevia arvoja tarpeen mukaan. (Lisätietoja on kohdassa [Suunnittelun muutostenhallinnan yleisten arvojen luominen](engineering-change-management-setup.md).) |
| Vakavuusaste | Valitse arvo, joka ilmaisee pyynnön toteutuksella korjattavan ongelman vakavuusasteen. Voit mukauttaa yrityksen käytettävissä olevia arvoja tarpeen mukaan. (Lisätietoja on kohdassa [Suunnittelun muutostenhallinnan yleisten arvojen luominen](engineering-change-management-setup.md).) |
| Pyytäjä: | Pyynnön luoneen käyttäjän nimi. |
| Päivämääränä | Pyynnön luontipäivämäärä. |
| Tila | Pyynnön tila. Juuri luodun pyynnön tila on *Luonti*. Kun pyyntö hyväksytään sen tilaksi tulee *Hyväksytty*. Jos pyynnölle on luotu liittyvä muutostilaus, tilaksi tulee *Seurattu*. |
| Muutostilaus | Muutostilauksen numero, jos muutospyyntöä seurasi muutostilaus. |

#### <a name="information-fasttab"></a>Tiedot-pikavälilehti

**Tiedot**-pikavälilehdessä voi antaa pyyntöä koskevia lisätietoja.

Voit lisätä rivin ruudukkoon valitsemalla **Uusi** ruudukon yläpuolella olevalla työkalurivillä ja valitsemalla sitten jonkin seuraavista vaihtoehdoista:

- **Tiedosto** – lataa tiedosto.
- **Kuva** – lataa kuvatiedosto.
- **Huomautus** – kirjoita huomautus suoraan ruudukkoon.
- **URL-osoite** – kirjoita URL-osoite suoraan ruudukkoon.

Seuraavassa taulukossa käsitellään kunkin rivin kenttiä.

| Kenttä | kuvaus |
|---|---|
| Luonnin päivämäärä ja aika | Päivämäärä ja kellonaika, jolloin rivi luotiin. |
| Laji | Tietotyyppi, jolle rivi luotiin (tiedosto, kuva, huomautus tai URL-osoite). |
| kuvaus | Kirjoita rivin kuvaus. |
| Rajoitus | Arvo, joka ilmaisee, lisättiinkö tiedot sisäisestä vai ulkoisesta lähteestä. |
| Liitetty | Valittu valintaruutu ilmaisee, että rivillä on liite (tiedosto tai kuva). Lataa liite valitsemalla rivi ja valitsemalla sitten **Avaa** ruudukon yläpuolella olevalla työkalurivillä. |

#### <a name="products-fasttab"></a>Tuotteet-pikavälilehti

**Tuotteet**-välilehdessä voi mainita jokaisen tuotteen, johon muutospyyntö vaikuttaa. Käytä lisätä tuotteita ruudukkoon tai poistaa niitä ruudukosta työkalurivin painikkeita.

Tämä luettelo on tarkoitettu vain tiedoksi. Tämän vuoksi liittyviä tuotteita voi lisätä tarvittavan määrän. Jos luot muutospyynnön aiemmin luodun tuotteen **Tuotteen tiedot** -sivulla, kyseisen tuotteen pitäisi olla luettelossa **Tuotteet**-pikavälilehdessä pyyntötietueen tallennuksen jälkeen.

#### <a name="source-fasttab"></a>Lähde-pikavälilehti

**Lähde**-pikavälilehdessä voi seurata muutospyynnön alkupistettä. Siitä on hyötyä, jos esimerkiksi haluat nähdä, onko muutospyyntö luotu myyntitilauksesta, kuka sen loi ja missä yrityksessä se luotiin.

### <a name="evaluate-the-business-impact-of-a-change-request"></a>Muutospyynnön liiketoimintavaikutuksen arvioiminen

Muutoksia tarkistettaessa voidaan etsiä riippuvaisuuksia. Tällä tavoin voidaan arvioida pyydetyn muutoksen vaikutus avoimiin tapahtumiin, kuten myyntitilauksiin, tuotantotilauksiin ja käytettävissä olevaan varastoon.

1. Valitse **Suunnittelun muutostenhallinta \> Yleinen \> Suunnittelun muutostenhallinta \> Suunnittelun muutospyynnöt**.
1. Avaa joko aiemmin luotu muutospyyntö tai luo uusi muutospyyntö valitsemalla toimintoruudussa **Uusi**.
1. Valitse toimintoruudun **Muutospyyntö**-välilehden **Liiketoimintavaikutus**-ryhmässä jokin seuraavista painikkeista:

    - **Haku** – Tarkistaa kaikki avoimet tapahtumat ja avaa sitten **Liiketoimintavaikutus avoimiin tapahtumiin** -valintaikkunan. Valintaikkunassa on luettelo kaikista tapahtumista, joihin muutos vaikuttaa.
    - **Näytä edellinen haku** – Avaa **Liiketoimintavaikutus avoimiin tapahtumiin** -valintaikkunan, jossa luettelo edellisen haun tuloksista. (Uutta hakua ei tehdä.)

1. Jos löydetty muutosta edellyttävä ongelma on kriittinen, avoimet tapahtumat voidaan estää tai vastaavalle käyttäjälle voidaan ilmoittaa **Liiketoimintavaikutus avoimiin tapahtumiin** -valintaikkunan työkalurivin painikkeilla.

### <a name="create-a-change-order-from-a-change-request"></a>Muutostilauksen luominen muutospyynnöstä

Suunnittelun muutospyyntöä tarkistava suunnittelija voi luoda suunnittelun muutostilauksen suoraan **Suunnittelun muutospyynnöt** -sivulta. Valitse toimintoruudun **Muutospyyntö**-välilehden **Suunnittelun muutostilaus** -ryhmässä **Kopioi linkki ja tuotteet**.

## <a name="engineering-change-orders"></a>Tekniset muutostilaukset

Suunnittelun muutostilaukset ovat jäsennetty prosessi muutosten tekemiseen suunnittelutuotteisiin. Muutoksia ehdotetaan käyttämällä suunnitteluun liittyvien tietojen kopiota. Varsinaisiin päätietoihin ei kosketa. Lisätietoja suunnitteluun liittyvistä tiedoista on kohdassa [Suunnitteluversiot ja suunnittelun tuoteluokat](engineering-versions-product-category.md).

Voit luoda hyväksyttyyn suunnittelun muutospyyntöön perustuvan suunnittelun muutostilauksen. Suunnittelijat voivat luoda suunnittelun muutostilauksia myös alusta alkaen. Yhteen suunnittelun muutostilaukseen voidaan sisällyttää useita tuotteita seuraavasti:

- Valitse tuotteet manuaalisesti.
- Sisällytä tuotteen rakenteessa alempana olevia tuotteita (eli alituotteita) tuoterakenteen avulla.
- Sisällytä tuotteen rakenteessa ylempänä olevia tuotteita (eli ylätason tuotteita) missä käytetty -haun avulla.

Kun muutosehdotus on valmis, työnkulku käsittelee tarkistus- ja hyväksymisprosessin. Erilaisia työnkulkuja voidaan määrittää prioriteetin ja vakavuusasteen perusteella.

Suunnittelun muutostilausten tai muutospyyntöjen työnkulku määritetään valitsemalla **Suunnittelun muutostenhallinta \> Suunnittelun työnkulut**. Valitse ensin **Uusi** ja sitten käytetäänkö työnkulkua tarkistamaan suunnittelun muutostilauksia vai suunnittelun muutospyyntöjä. Vahvista työnkulku lopuksi.

Lisätietoja työnkulkujen käyttämisestä on kohdassa [Työnkulkujärjestelmän yleiskatsaus](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

Seuraavat sidosryhmät voivat tyypillisesti hyväksyä suunnittelun muutostilauksen:

- **Tuotteen omistajat** – lisätietoja tuotteen omistajista on kohdassa [Tuotteen omistajat](product-owner.md).
- **Vastaava ryhmän johtaja** – Suunnittelun muutostilauksen **Otsikko**-näkymän **Suunnittele**-kentässä on sen suunnittelijan nimi, joka loi suunnittelun muutostilauksen. Jos suunnittelija on järjestelmässä määritetyn ryhmän jäsen, **Vastuunhenkilö**-kentässä on kyseisen ryhmän johtajan nimi.
- **Talousosasto** – talousosaston on ehkä tarkistettava palvelupyynnöt, jossa muutoksen kustannukset ovat suuret.

Voit valita, käsitelläänkö suunnittelun muutostilaus suoraan hyväksymisen jälkeen työnkulun osana vai käsitelläänkö se myöhemmin manuaalisena vaiheena. Suunnittelun muutostilauksen käsittelyn aikana varsinaisen tuotteen suunnittelutiedot päivitetään.

Kun tarkistat muutospyyntöä valitse toimintoruudun **Muutospyyntö**-välilehden **Liiketoimintavaikutus**-ryhmässä **Haku**. Voit sitten arvioida ehdotetun muutoksen vaikutuksen avoimiin tapahtumiin, kuten myyntitilauksiin, tuotantotilauksiin ja käytettävissä olevaan varastoon. Tulokset näkyvät **Liiketoimintavaikutus avoimiin tapahtumiin** -valintaikkunassa, jossa voi valita tapahtumia, joihin vaikutus kohdistuu, sekä tarkastella lisätietoja, ilmoittaa vastuukäyttäjälle tai estää tapahtuma työkalurivin komennoilla.

### <a name="engineering-change-orders-in-engineering-or-operational-companies"></a>Suunnitteluyritysten tai operatiivisten yritysten suunnittelun muutostilaukset

Kuten kohdassa [Suunnitteluyritykset ja tietojen omistussäännöt](engineering-org-data-ownership-rules.md) on kuvattu, muokattavat tuotetiedot vaihtelevat sen mukaan, minkälainen yritys on käytössä (suunnitteluyritys vai operatiivinen yritys). Tietojen omistussääntöjä käytetään myös suunnittelun muutostilauksissa. Niinpä yritystyyppi, jossa suunnittelun muutostilaus luotiin, määrittää minkälaisia muutoksia voidaan tehdä. Seuraavassa on muutamia esimerkkejä:

- **Suunnitteluyrityksen** suunnittelun muutostilauksissa voidaan tehdä perusmuutoksia suunnittelutietoihin. Voit esimerkiksi luoda uusia versioita tuotteesta, muuttaa tuotteen rakennetta tuoterakenteen avulla ja muuttaa suunnittelumääritteen arvoja. Valitse kunkin sellaisen tuotteen osalta, johon muutos vaikuttaa, seuraavat arvot **Vaikutus**-kentässä:

    - **Ei mitään** – päivitä aiemmin luotu tuoteversio (version päivitys).
    - **Uusi versio** – luo uusi valittuun tuoteversioon perustuva versio.
    - **Uusi tuote** – luo täysin uusi tuote tai tuotevariantti, joka perustuu valittuun tuoteversioon.

- **Operatiivisen yrityksen** suunnittelun muutostilauksissa voi muuttaa tuotteen logistisia tietoja. Voit esimerkiksi rikastaa aiemmin luotua tuoterakennetta hankinnan asetuksia, lisätä paikallisia reittejä tai paikallisia tuoterakenteita ja jopa rikastaa tuoterakennetta lisäämällä uusia tuoterakennerivejä paikallisia pakkausmateriaaleja, voiteluaineita tai paikallisella kielellä annettavia ohjeita varten. Käyttäjien operatiivisessa yrityksessä tekemät rikastukset säilytetään, kun uudet päivitykset lähetetään suunnitteluyrityksestä. Lisätietoja on kohdassa [Suunnitteluyritykset ja tietojen omistussäännöt](engineering-org-data-ownership-rules.md).

    Kun suunnittelun muutostilauksia käsitellään suunnitteluyrityksessä, tuotteet luodaan ja/tai päivitetään suunnitteluyrityksessä. Niinpä jos myös tuotteen päätiedot päivitetään, tuotteet on vapautettava myös operatiivisiin yrityksiin.

- Voit vapauttaa tuotteita suoraan suunnittelun muutostilauksista. Avaa muutostilaus ja valitse sitten toimintoruudun **Muutostilaus**-välilehden **Tuotevapautukset**-ryhmässä **Vapauta tuotteen rakenne**. Prosessi toimii samalla tavoin kuin vapautettaessa tuotteita **Vapautetut tuotteet** -sivulta. Lisätietoja on kohdassa [Tuoterakenteiden vapauttaminen](release-product-structure.md).
- Tuotteet voidaan vapauttaa automaattisesti suunnittelun muutostilauksista seuraavien seikkojen perusteella:

    - Vapauttaminen uudelleen yrityksiin, joissa tuotteita vapautettiin aiemmin. Tarkista kaikki aiemmat vapautukset valitsemalla **Haku** ja näytä sitten tulokset valitsemalla **Näytä**. Edelliset tuotevapautukset näkyvät **Näytä**-sivulla, ja voit valita, mitkä tuotteet haluat vapauttaa uudelleen. Sulje sitten **Näytä**-sivu ja vapauta valitut tuotteet uudelleen valitsemalla **Käsittele**.
    - Suunnittelun tuoteluokan vapautuksen hallinnan automaattiset vapautusasetukset. Tämä vapautus voidaan tehdä työnkulun osana. Kun **vapautusehdotuksen keräämisen** estoa käytetään, vapautusehdotus täytetään vapauttamalla ehdotukset uudelleen (katso edellinen luettelokohta) ja tuotteet vapautetaan yrityksille, jos **Automaattinen vapautus** -valintaruutu valitaan suunnittelun tuoteluokan vapautuksen hallinnassa. Voit näyttää tulokset valitsemalla **Näytä** edellisessä luettelokohdassa kuvatulla tavalla. Tuotteet vapautetaan myös, kun **vapautusehdotuksen käsittelyn** estoa käytetään. Jos valitset vain vapautusehdotuksen keräämisen työnkulun osana, voit käynnistää vapautuksen manuaalisesti valitsemalla **Käsittele** edellisessä luettelokohdassa kuvatulla tavalla.

## <a name="follow-up-on-an-engineering-change-request-via-an-engineering-change-order"></a>Suunnittelun muutospyynnön seuranta suunnittelun muutostilauksen avulla

Heti kun suunnittelun muutospyyntö on hyväksytty, seuraava toimi voi olla suunnittelun muutostilaus. Voit yhdistää useita suunnittelun muutospyyntöjä yhteen suunnittelun muutostilaukseen. Yhdessä suunnittelun muutostilauksessa voi myös olla useita tuotteita. (Tätä menetelmää käytetään yleensä, kun sama muutos on tehtävä useisiin tuotteisiin.) Useita suunnittelun muutostilauksia ei voi luoda yhdestä suunnittelun muutospyynnöstä.

Voit tehdä muutospyynnön jälkeen muutostilakusen avaamalla muutospyynnön ja valitsemalla sitten toimintoruudun **Muutostilaus**-välilehden **Suunnittelun muutostilaus** -ryhmässä **Kopioi linkki ja tuotteet**. Voit sitten valita aiemmin luodun suunnitelman, johon muutostilaus yhdistetään, tai voit luoda uuden suunnitelman muutostilauksen kyseiselle pyynnölle.

## <a name="engineering-change-order-report"></a>Suunnittelun muutostilausraportti

Suunnittelun muutostilauksen raporteissa käsitellään suunnittelun muutostilaukseen tehtyjä muutoksia. Niistä on hyötyä sekä tarkistus- ja hyväksymisprosessin aikana ja sen jälkeen.

Voit tarkastella suunnitelman muutostilauksen raporttia avaamalla kyseisen muutostilauksen ja valitsemalla sitten toimintoruudun **Muutostilaus**-välilehden **Näytä**-ryhmässä **Suunnitelman muutostilauksen raportti**.

## <a name="fields-on-an-engineering-change-order"></a>Suunnittelun muutostilauksen kentät

Useimmat suunnitelman muutostilausten kentät ovat samoja kuin vapautettujen tuotteiden, suunnitelmaversioiden, asiakirjojen, tuoterakenteiden (rivien) ja reittien (toimintojen) kentät. Seuraavassa taulukossa olevat kentät ovat kuitenkin vain muutostilauksissa.

| Kenttä | kuvaus |
|---|---|
| Suunnittelun muutoksen syyt | Valitse syy, miksi tuotetta, joka vaikutus koskee, muutettiin. |
| Muutoksen kuvaus | Anna muutoksen kuvaus. |
| Vaaditut erikoistyökalut | Määritä, tarvitaanko muutoksen tekemiseen erikoistyökaluja. |
| Suunnittelun materiaalikäsittely | Valitse materiaalin käsittelykoodi jätteelle, jota tuotetaan muutosta käytettäessä. |
| Asiakkaan hyväksyntä vaaditaan | Määritä, onko asiakkaan hyväksyntä pakollinen ennen muutoksen käyttämistä. |
| Asiakkaan hyväksyntä saatu | Määritä asiakkaan hyväksynnän tila. |
| Ympäristön terveellisyys ja turvallisuus | Määritä, käytetäänkö ympäristön terveellisyys- ja turvallisuussääntöjä muutokseen. Jos niitä käytetään, voit valita käytettävät säännöt. |

Voit kopioida muutoksen tietoja niiden tuotteiden välillä, joita muutos koskee, käyttämällä **Ylläpidä tai kopioi muutostietoja** -painiketta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]