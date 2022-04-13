---
title: Toimitusaikataulu
description: Tässä aiheessa on tietoja toimitusaikataulusivusta ja sen ominaisuuksista.
author: t-benebo
ms.date: 9/3/2021
ms.topic: article
ms.search.form: ReqSupplyDemandSchedule, ReqSupplyDemandScheduleFilters, ReqSupplyDemandItemDetails, ReqTransFuturesActionsPart, ReqSupplyDemandOverviewLegendPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 89b8ce96a5c34902187751cfa523ed99a94500b3
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468673"
---
# <a name="supply-schedule"></a>Toimitusaikataulu

[!include [banner](../includes/banner.md)]

**Toimitusaikataulu**-sivu näyttää kattavan yhteenvedon tuotteen tai tuoteperheen toimituksista ja kysynnästä. Tiedot suodatetaan sijainnin, pääsuunnitelman ja kausien mukaan. Sivulla voit myös luoda uusia tilauksia, muokata aiemmin luotuja suunniteltuja tilauksia ja suorittaa pääsuunnittelun.

## <a name="open-the-supply-schedule-page"></a>Toimitusaikataulusivun avaaminen

Voit avata **Toimitusaikataulu**-sivun seuraavilla tavoilla:

- Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Toimitusaikataulu**. Määritä **Muokkaa suodatinta** -valintaikkunassa etsimäsi suunnitelma tai tuote syöttämällä suodatinarvot kenttiin. (Muualla tässä aiheessa lisäämistäsi suodatinarvoista käytetään nimitystä "suodatin" tai "nykyinen suodatin".) Kun olet valmis, valitse **OK**.
- Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**. Valitse tai avaa tuote. Valitse sitten toimintoruudun **Suunnittelu**-välilehden **Näytä**-ryhmässä **Toimitusaikataulu**.
- Avaa **Pääsuunnittelu \> Määritys \> Kysynnän ennuste \> Nimikkeen kohdistustunnukset**. Valitse tuoteperheenä käytettävä nimikkeen kohdistustunnus. Valitse sitten toimintoruudussa **Toimitusaikataulu**.
- Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Suunnitellut tilaukset**. Valitse tai avaa suunniteltu tilaus. Valitse sitten toimintoruudun **Näytä**-välilehden **Näytä**-ryhmässä **Toimitusaikataulu**.

> [!NOTE]
> Kun avaat **Toimitusaikataulu**-sivun tuotteesta, tuoteperheestä tai suunnitellusta tilauksesta, sinun ei tarvitse syöttää suodatinarvoja. Järjestelmä käyttää oletuskausimallia.

## <a name="use-the-supply-schedule-page"></a>Toimitusaikataulusivun käyttäminen

**Toimitusaikataulu**-sivu koostuu yläosasta, **Kauden loppuvarasto** -pikavälilehdestä, toisesta pikavälilehdestä, joka tulee näkyviin yläosassa valitun rivin mukaan, sekä tietoruudusta. (Voit avata tietoruudun ja tarkastella tietoruutua valitsemalla kohdan **Aiheeseen liittyviä tietoja** sivun oikeassa reunassa.)

### <a name="upper-section"></a>Yläosa

Yläosa **Toimitusaikataulu**-sivulla sisältää ruudukon, jossa näkyvät seuraavat tuotteen tai tuoteperheen tiedot. Tiedot on jaotettu kausien mukaan. Kaudet määritetään suodattimesta **Kausimalli**-arvolla.

- **Kauden alkuvarasto** – Tällä rivillä näkyy odotettu varastosaldo kauden alussa, jos kaikki järjestelmän tilaukset tapahtuvat.
- **Kauden loppuvarasto** – Tällä rivillä näkyy odotettu varastosaldo kauden lopussa, jos kaikki järjestelmän tilaukset tapahtuvat.
- **Kauden lopun tarvekohdistettu varasto** – Tällä rivillä näkyy tulevaan kysyntään kohdistettu varaston määrä kauden lopussa.
- **Kauden nettotoimitukset** – Tällä rivillä näkyy kauden toimitusten ja kysynnän välinen ero.
- **Vähimmäisvarasto** – Tämä solmu näyttää tuotteen tai tuoteperheen varmuusvarastot. Laajentaaksesi tai tiivistääksesi tämän solmun valitse se ja valitse sitten **Laajenna** tai **tiivistä** työkaluriviltä. Tämä solmu näkyy vain, jos tuotteessa tai tuoteperheessä on varmuusvarasto.
- **Kysyntä** – Tämä solmu näyttää tuotteen tai tuoteperheen kysynnän. Kysyntä ryhmitellään tapahtumatyypin mukaan. Laajentaaksesi tai tiivistääksesi tämän solmun valitse se ja valitse sitten **Laajenna** tai **tiivistä** työkaluriviltä. Kysynnän tapahtumatyyppejä ovat myynnit, siirrot ja varastokirjauskansiot. Tämä solmu näkyy vain, jos tuotteelle tai tuoteperheelle on kysyntää.
- **Toimitukset** – Tämä solmu näyttää tuotteen tai tuoteperheen toimitukset. Toimitukset ryhmitellään tapahtumatyypin mukaan. Laajentaaksesi tai tiivistääksesi tämän solmun valitse se ja valitse sitten **Laajenna** tai **tiivistä** työkaluriviltä. Toimitusten tapahtumatyyppejä ovat tuotanto, ostot ja siirrot. Tämä solmu näkyy vain, jos tuotteessa tai tuoteperheessä on toimituksia.

Monet käytettävissä olevista työkalurivin painikkeista, tietoruudut ja pikavälilehdet määräytyvät yläosan valintojen mukaan. Yleensä tapahtumalaji valitaan valitsemalla jokin riveistä **Toimitukset** tai **Kysyntä**-solmussa. Tämän jälkeen voit valita kauden valitsemalla tietyn sarakkeen valitulle riville.

Työkalurivi yläosan ruudukon yläpuolella **Toimitusaikataulu**-sivulla näyttää seuraavat painikkeet:

- **Laajenna/Tiivistä** – Laajenna tai tiivistä valittu solmu, kuten **Kysyntä**-solmu, **Toimitukset**-solmu tai niiden alisolmu. (Solmut näyttävät etuliitteen **\[+\]** tai **\[-\]** sen merkiksi, ovatko ne tiivistettyinä tai laajennettuina.)
- **Uusi** – Avaa valikon, jossa jokainen komento puolestaan avaa valintaikkunan tai sivun, jonka avulla voit lisätä valintaasi tietyntyyppisen nimikkeen. Käytettävissä olevia komentoja ovat **Ennustetoimitus**, **Suunniteltu tilaus**, **Ajoitettu kanban**, **Uusi tuotantotilaus**, **Ostotilaus** ja **Siirtotilaus**.
- **Pääsuunnittelu** – Suorita pääsuunnittelu. Näyttöön tulee valintaikkuna, jossa voit määrittää suoritettavan suunnitelman. Oletusarvoisesti **Pääsuunnitelma**-kenttä määritetään vastaamaan nykyistä suodatinta.
- **Ilmoita valmiiksi -kirjausten enimmäismäärä** – Avaa **Ilmoita valmiiksi -kirjausten enimmäismäärä** -sivun tuotteelle, joka on määritetty nykyisessä suodattimessa.
- **Päivitä suunnitellut tilaukset** – Avaaa **Suunnitellut tilaukset** -sivun, jossa näkyvät nykyisessä suodattimessa määritetyn tuotteen tai tuoteperheen suunnitellut tilaukset.
- **Taso** – Jaa suunnitellut tilaukset näyttöön tulevan valintaikkunan asetusten mukaan.
- **Sijaintikohtainen materiaalisuunnitelman käytäntö** – Avaa **Nimikkeen kattavuus** -sivu tuotteelle, joka on määritetty nykyisessä suodattimessa.
- **Kanban-sääntö** – Avaa **Kanban-säännöt**-sivu tuotteelle, joka on määritetty nykyisessä suodattimessa.

### <a name="fasttabs"></a>Pikavälilehdet

**Toimitusaikataulu**-sivu voi sisältää seuraavat pikavälilehdet:

- **Kauden loppuvarasto** – Tämä pikavälilehti näyttää kauden loppuvaraston tiedot graafisessa muodossa.
- **Toimitusprofiili** – Tämä pikavälilehti näyttää toimitustiedot graafisessa muodossa. Se tulee näkyviin, kun valitset **Toimitus**-solmun tai sen alla olevan rivin sivun yläosassa.
- **Yhteenveto** – Tässä pikavälilehdessä näkyy yhteenvetotietoja, jotka liittyvät yläosassa valitsemaasi tapahtumatyyppiin. Esimerkiksi, jos valitset **Myynti**-kohdan **Kysyntä**-solmussa, tämä pikavälilehti näyttää kentät, jotka liittyvät myyntitilauksiin, kuten **Pyydetyt myyntitilausrivit** tai **Kokonaismäärä**. Jos valitset **Tuotantotilaukset** **Tuotanto**-alisolmussa **Toimitus**-solmussa, tämä pikavälilehti näyttää kentät, jotka liittyvät tuotantotilauksiin, kuten **Ajoitetut tuotantotilaukset** tai **Ajoitettu yhteensä**. Kenttäarvot määräytyvät yläosassa valitsemasi kauden mukaan. 
- **\[Tapahtumatyyppi\] - \[Kausi\]** – Tämä pikavälilehti näyttää yläosassa valitsemasi tapahtumatyypin ja kauden tilaukset. Pikavälilehden nimi vastaa näitä valintoja. Nimi voi olla esimerkiksi **Myyntitilauukset - keskeneräiset työt** tai **Tuotantotilaukset - viikko 37**.

### <a name="action-pane"></a>Toimintoruutu

Toimintoruudussa ovat käytettävissä seuraavat painikkeet:

- **Muokkaa suodatinta** – Avaa **Muokkaa suodatinta** -valintaruudun, jossa voit päivittää suodatinarvot ja avata sitten uudelleen **Toimitusaikataulu**-sivun, joka näyttää päivitetyt suodatinasetukset.
- **Näytä viivästykset** – Korosta ylemmässä osassa olennaiset rivit, jos tapahtumatyyppiä vastaava tilaus on viivästynyt.

### <a name="factbox-pane"></a>Tietoruutu

Voit avata tietoruudun ja tarkastella tietoruutua valitsemalla kohdan **Aiheeseen liittyviä tietoja** sivun oikeassa reunassa. Seuraavat tietoruudut ovat käytössä **Toimitusaikataulu**-sivulla:

- **Nimikkeen tiedot** – Tämä tietoruutu sisältää nykyisessä suodattimessa määritetyn tuotteen perustiedot. Se on tyhjä, jos olet määrittänyt suodattimessa tuoteperheen.
- **Toiminnot** – Tämä pikavälilehti näyttää yläosassa valitsemasi tapahtumatyypin tilausten toiminnot.
- **Viivästykset** – Tämä pikavälilehti näyttää yläosassa valitsemasi tapahtumatyypin tilausten viivästykset.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
