---
title: Suunnittelutuotteiden muutostenhallinta
description: Tässä artikkelissa on tietoja suunnittelun muutostenhallinnasta. Suunnittelun muutostenhallinnassa on jäsennettyjä prosesseja suunnittelutuotteiden muutostenhallintaan muutosten ehdottamisesta, pyytämisestä ja tekemisestä muutosten tarkistamiseen ja hyväksymiseen sekä niiden vaikutuksen arvioimiseen aiemmin luoduissa tapahtumissa ja muutosten seurantaan.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcmRequestSelection,EngChgEcmRequestProducts,EngChgEcmRequestPriorityChart,EngChgEcmRequestListPage,EngChgEcmRequestFilteredPart,EngChgEcmRequestDetails,EngChgEcmReason,EngChgEcmProjTableInformation,EngChgEcmProductRoute,EngChgEcmProductRelease,EngChgEcmProductPreview, EngChgEcmWhereUsed, EngChgEcmInventTrans,EngChgEcmHeaderSelection,EngChgEcmHeaderPreviewPart,EngChgEcmHeaderFilteredPart,EngChgEcmHeaderDetails, EngChgCaseWhereUsedAnalysis, EngChgCaseValidatorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6c578609a64c21a33f10b64a1d77f006b45bac41
ms.sourcegitcommit: 229ea085cf35579a2631ea1e5fc2c602fa47e3f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/24/2022
ms.locfileid: "9714733"
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

### <a name="evaluate-the-business-impact-of-a-change-request-and-send-notifications"></a>Muutospyynnön ja ilmoitusten lähettämisen liiketoimintavaikutuksen arvioiminen

Muutoksia tarkistettaessa voidaan etsiä riippuvaisuuksia. Tällä tavoin voidaan arvioida pyydetyn muutoksen vaikutus avoimiin tapahtumiin, kuten myyntitilauksiin, tuotantotilauksiin ja käytettävissä olevaan varastoon. Kun tarkastelet muutospyyntöjä, voit lähettää ilmoitukset ihmisille, jotka vastaavat erilaisten tilausten täyttämisestä.

#### <a name="review-affected-transactions-block-selected-transactions-and-send-notifications"></a>Tarkastele tapahtumia, joihin vaikutus ulottuu, estä valitut tapahtumat ja lähetä ilmoituksia

Voit tarkastella tapahtumia, joihin vaikutus ulottuu, estää valitut tapahtumat ja lähettää niihin liittyviä ilmoituksia seuraavasti.

1. Valitse **Suunnittelun muutostenhallinta \> Yleinen \> Suunnittelun muutostenhallinta \> Suunnittelun muutospyynnöt**.
1. Avaa joko aiemmin luotu muutospyyntö tai luo uusi muutospyyntö valitsemalla toimintoruudussa **Uusi**.
1. Valitse toimintoruudun **Muutospyyntö**-välilehden **Liiketoimintavaikutus**-ryhmässä jokin seuraavista painikkeista:

    - **Haku** – Tarkistaa kaikki avoimet tapahtumat ja avaa sitten **Liiketoimintavaikutus avoimiin tapahtumiin** -valintaikkunan. Valintaikkunassa on luettelo kaikista tapahtumista, joihin muutos vaikuttaa.
    - **Näytä edellinen haku** – Avaa **Liiketoimintavaikutus avoimiin tapahtumiin** -valintaikkunan, jossa luettelo edellisen haun tuloksista. (Uutta hakua ei tehdä.)

1. **Liiketoiminnan vaikutus avoimiin tapahtumiin** -valintaikkuna sisältää joukon välilehtiä, joista jokaisella on luettelo tietyn tyyppisistä tapahtumista, joihin vaikutus ulottuu (**myyntitilaukset**, **ostotilaukset**, **tuotantotilaukset**, **varasto** ja niin edelleen). Kussakin välilehdessä näkyy myös numero, joka ilmaisee tyypin tapahtumien määrän, johon vaikutus ulottuu. Valitse välilehti, jos haluat tarkastella luetteloa.
1. Jos haluat käyttää tapahtumaa luettelossa, valitse tapahtuma ja valitse sitten työkaluriviltä jokin seuraavista painikkeista:

    - **Näytä tapahtuma** – Avaa valittu tapahtumatietue.
    - **Estä tilaus** – Tämä painike on käytettävissä vain **Myyntitilaukset**-välilehdessä. Valitse tämä, jos haluat estää valitun myyntitilauksen.
    - **Estä rivi** – Tämä painike on käytettävissä vain **Ostotilaukset**-välilehdessä. Valitse tämä, jos haluat estää valitun ostotilausrivin.
    - **Ilmoita vastuuhenkilölle** – Tämä painike on käytettävissä vain **Myyntitilaukset**-välilehdessä. Valitsemalla tämän painikkeen voit lähettää muutosilmoituksen käyttäjälle, joka on määritetty vastuuhenkilöksi valitulle myyntitilaukselle. Lisätietoja siitä, kuka voi nähdä ilmoitukset ja miten ilmoituksen näytetään, on kohdassa [Tapahtumien muutosilmoitusten tarkasteleminen ja käsitteleminen](#review-notifications).
    - **Ilmoita tilaajalle** – Tämä painike on käytettävissä vain **Ostotilaukset**-välilehdessä. Valitsemalla tämän painikkeen voit lähettää muutosilmoituksen tilaajalle, joka on määritetty tilaajaksi valitulle ostotilaukselle. Lisätietoja siitä, kuka voi nähdä ilmoitukset ja miten ilmoituksen näytetään, on kohdassa [Tapahtumien muutosilmoitusten tarkasteleminen ja käsitteleminen](#review-notifications).
    - **Ilmoita tuotannolle** – Tämä painike on käytettävissä vain **Tuotantotilaukset**-välilehdessä. Toisin kuin myynti- ja ostotilauksissa, tuotantotilauksilla ei ole yksittäistä käyttäjää, joka on määritetty vastuulliseksi niistä alusta loppuun. Sen sijaan eri valvojat tai suunnittelijat yleensä omistavat omistajuuden tietyn sivuston tai tietyn tuotannon osan osalta (esimerkiksi tietyille resursseille tai resurssiryhmille). Kun valitset tämän painikkeen, kaikki valittuun tuotantotilaukseen liittyvästä resurssista vastuussa olevat käyttäjät saavat muutosilmoituksen. Lisätietoja siitä, kuka voi nähdä ilmoitukset ja miten ilmoituksen näytetään, on kohdassa [Tapahtumien muutosilmoitusten tarkasteleminen ja käsitteleminen](#review-notifications).
    - **Ilmoita valmistelijalle** – Tämä painike on käytettävissä vain **Ostoehdotus**-välilehdessä. Valitsemalla tämän painikkeen voit lähettää muutosilmoituksen valmistelijalle, joka on määritetty valistelijaksi valitulle ostoehdotukselle. Lisätietoja siitä, kuka voi nähdä ilmoitukset ja miten ilmoituksen näytetään, on kohdassa [Tapahtumien muutosilmoitusten tarkasteleminen ja käsitteleminen](#review-notifications).
    - **Ilmoita myynnin vastuuhenkilölle** – Tämä painike on käytettävissä vain **Tarjoukset**-välilehdessä. Valitsemalla tämän painikkeen voit lähettää muutosilmoituksen käyttäjälle, joka on määritetty vastuuhenkilöksi valitulle tarjoukselle. Lisätietoja siitä, kuka voi nähdä ilmoitukset ja miten ilmoituksen näytetään, on kohdassa [Tapahtumien muutosilmoitusten tarkasteleminen ja käsitteleminen](#review-notifications).
    - **Hävikki** – Tämä painike on käytettävissä vain **Varasto**-välilehdessä. Valitse tämä, kun haluat hävikkiin valitun varaston.
    - **Näytä historia** – Avaa valittuun tapahtumaan liittyvät toimenpiteet käyttämällä **Liiketoimintavaikutukset avoimiin tapahtumiin** -valintaikkunaa. (Historiassa näkyy esimerkiksi, onko ilmoitukset lähetetty vai onko tapahtumia estetty.) 
    - **Tarkastele kaikkia tapahtumia** – Avaa kaikkien tapahtumien koko luettelo, ei vain avoimia tapahtumia.

> [!IMPORTANT]
> **Ilmoita tuotantoon** -painike on käytettävissä vain, jos *Suunnitteluilmoitukset tuotannolle* -ominaisuus on käytössä järjestelmässä. Ohjeita tämän toiminnon ja sen edellytysten käyttöönottoon ja käytöstä poistamiseen: [Suunnittelun muutostenhallinnan yleiskuvaus](product-engineering-overview.md).

#### <a name="review-and-process-change-notifications-for-transactions"></a><a name="review-notifications"></a>Tapahtumien muutosilmoitusten tarkasteleminen ja käsitteleminen

Voit lukea ja käsitellä muutosilmoitukset seuraavasti:

- Tuotantotilauksia lukuun ottamatta toimintokeskuksessa näkyvät niiden tapahtumien ilmoitukset, joista olet vastuussa. Siirtymispalkin oikeassa sivussa oleva **Näytä viestit** -painike (kellosymboli) ilmaisee, milloin sanoma on käytettävissäsi toimintokeskuksessa. Avaa toimintokeskus ja tarkastele viestejä valitsemalla **Näytä viestit** -painike.
- Voit tarkastella kaikkia tuotantotilauksia, joista on lähetetty tekninen suunnitteluilmoitus, kohdassa **Tuotantotilaukset \> Tuotantotilaukset \> Kaikki tuotantotilaukset**. Sitten toimintoruudun **Tuotantotilaus**-välilehden **Tuotannon muutospyyntö** -ryhmässä valitse **Tuotannon ilmoitukset** avataksesi **Tuotannon ilmoitukset** -sivun.
- Tuotantotilauksia varten voit tarkistaa vain hallitsemaani tuotantoresursseihin liittyvät muutosilmoitukset. Valitse **tuotannonhallinnan** työtilan toimintoruudusta **Määritä työtila** ja suodata sivu siten, että siinä näkyvät tiedot vain hallitsemistasi tuotantoyksiköistä, ryhmistä ja/tai resursseista. **Yhteenveto**-osassa ruudussa, jonka nimi on **Tuotantotilaukset, joissa on muutettuja tuotteita**, näkyy suodatusasetuksiasi vastaavat ilmoitukset. Valitse tämä ruutu, kun haluat avata **Suunnitteluilmoitukset**-sivun, joka sisältää suodatuksen ehdot täyttävien tapahtumien luettelon.

Kun tarkastelet tuotantotilauksen ilmoituksia **Suunnitteluilmoitukset**-sivulla, voit seurata linkkejä niihin liittyviin muutostilauksiin tai tuotantotilauksiin valitsemalla sarakearvot tai käyttämällä toimintoruudussa olevia komentoja. Kun olet lopettanut muutoksen arvioinnin, voit merkitä ilmoituksen ratkaistuksi, kun olet peruuttanut tai muokannut tuotantotilauksia tarpeen mukaan. Valitse ilmoitus ja valitse sitten toimintoruudusta **Ratkaise**. Ilmoitus poistetaan kaikkien käyttäjien näkymistä.

> [!IMPORTANT]
> Tuotantotilauksia koskevien ilmoitusten lähettäminen edellyttää, että *Suunnitteluilmoitukset tuotannolle* -ominaisuus on käytössä järjestelmässä. Ohjeita tämän toiminnon ja sen edellytysten käyttöönottoon ja käytöstä poistamiseen: [Suunnittelun muutostenhallinnan yleiskuvaus](product-engineering-overview.md).

### <a name="create-a-change-order-from-a-change-request"></a>Muutostilauksen luominen muutospyynnöstä

Suunnittelun muutospyyntöä tarkistava suunnittelija voi luoda suunnittelun muutostilauksen suoraan **Suunnittelun muutospyynnöt** -sivulta. Valitse toimintoruudun **Muutospyyntö**-välilehden **Suunnittelun muutostilaus** -ryhmässä **Kopioi linkki ja tuotteet**.

Varmista, että valitset oikean yrityksen uutta suunnittelun muutostilausta varten. Jos muutostilauksentuloksena suunnittelutuote itsessään muuttuu (uusi versio, uusi tuote tai uusi variantti), muutostilaus on liitettävä suunnitteluyritykseen. Jos tarvitaan vain paikallinen muutos (**Vaikutus**-kohdan arvoksi on määritetty *Ei mitään*), muutostilaus voidaan liittää paikalliseen yritykseen ja muutokset otetaan käyttöön nykyisessä tuotteessa.

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

- *Suunnitteluyrityksen* suunnittelun muutostilauksissa voidaan tehdä perusmuutoksia suunnittelutietoihin. Voit esimerkiksi luoda uusia versioita tuotteesta, muuttaa tuotteen rakennetta tuoterakenteen avulla ja muuttaa suunnittelumääritteen arvoja. Valitse kunkin sellaisen tuotteen osalta, johon muutos vaikuttaa, seuraavat arvot **Vaikutus**-kentässä:

    - **Ei mitään** – päivitä aiemmin luotu tuoteversio (version päivitys).
    - **Uusi versio** – luo uusi valittuun tuoteversioon perustuva versio.
    - **Uusi tuote** – luo täysin uusi tuote, joka perustuu valittuun tuoteversioon.
    - **Uusi variantti** – luo uusi valittuun tuoteversioon perustuva variantti. Sen tuoterakenteen ja reitin tiedot kopioidaan.

- *Operatiivisen yrityksen* suunnittelun muutostilauksissa voi muuttaa tuotteen logistisia tietoja. Voit esimerkiksi rikastaa aiemmin luotua tuoterakennetta hankinnan asetuksia, lisätä paikallisia reittejä tai paikallisia tuoterakenteita ja jopa rikastaa tuoterakennetta lisäämällä uusia tuoterakennerivejä paikallisia pakkausmateriaaleja, voiteluaineita tai paikallisella kielellä annettavia ohjeita varten. Käyttäjien operatiivisessa yrityksessä tekemät rikastukset säilytetään, kun uudet päivitykset lähetetään suunnitteluyrityksestä. Lisätietoja on kohdassa [Suunnitteluyritykset ja tietojen omistussäännöt](engineering-org-data-ownership-rules.md).

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

## <a name="use-electronic-signatures-to-approve-and-active-boms-and-routes"></a>Sähköisten allekirjoitusten avulla voit hyväksyä ja aktivoida tuoterakenteita ja reitityksiä.

Sähköisten allekirjoitusten avulla voit hyväksyä ja/tai aktivoida tuoterakenteen ja/ tai reititysmuutoksia siirtymällä kohtaan **Organisaation hallinto \> Asetukset \> Sähköinen allekirjoitus \> Sähköisen allekirjoituksen vaatimukset**. Varmista sitten, että kullakin seuraavista nimikkeistä on **Allekirjoitus pakollinen** -asetuksen arvona *Kyllä*:

- Aktivoi suunnittelun muutostilauksen tuotteen tuoterakenne
- Aktivoi suunnittelun muutostilauksen tuotteen reititys
- Hyväksy suunnittelun muutostilauksen tuotteen tuoterakenne
- Hyväksy suunnittelun muutostilauksen tuotteen reititys
- Hyväksy suunnitteluversion tuoterakenne ja tuoterakenneversiot
- Hyväksy suunnitteluversio ja reititysversio

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
