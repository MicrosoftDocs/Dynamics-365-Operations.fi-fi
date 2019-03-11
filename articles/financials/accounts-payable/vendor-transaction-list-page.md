---
title: Näytä avoimien toimittajatapahtumien listaussivu
description: Tässä aiheessa on tietoja Microsoft Dynamics 365 for Finance and Operationsin toimittajatapahtumien luettelosivusta.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 99a169bd51e14f15c085f7547ec240b2787258cc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "341738"
---
# <a name="vendor-transactions-list-page"></a>Näytä avoimien toimittajatapahtumien listaussivu

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Näytä tilitykset

Toimintoruudun **Näytä tilitykset** -painikkeen avulla voit käyttää nopeasti tilityshistoriaa ja muita tilitystapahtumaa koskevia tietoja. Voit näyttää myös lisätapahtumat, jotka liittyvät valittuihin tapahtumiin joko siksi, että ne sisältyvät samaan tilitykseen, tai siksi, että ne ovat samassa maksukirjauskansiossa luotuja maksuja.

1. Valitse **Ostoreskontra \> Kaikki toimittajat**.
2. Valitse toimittaja, johon liittyy tapahtumia, ja valitse sitten toimintoruudussa **Toimittaja**-välilehden **Tapahtumat**.
3. Valitse tutkittava tapahtuma ja valitse sitten toimintoruudussa **Näytä tilitykset**.

    **Näytä tilitykset** -valintaikkuna tulee näkyviin ja näyttää valitun tapahtuman ja kaikki siihen täsmäytetyt asiakirjat. Tämä valintaikkunan muistuttaa tilityshistorianäkymää, mutta se sisältää kaikki liittyvät asiakirjat.

4. Voit valintaikkunassa tehdä erilaisia tehtäviä. Valitse vähintään yksi tosite ja sitten jokin seuraavista painikkeista:

    - **Näytä asiaan liittyvät** – Näytä kaikki toimittajan maksukirjauskansion ja yleisen kirjauskansion tapahtumat, jotka luotiin niissä kirjauskansioissa, joissa luettelossa näkyvät asiakirjat luotiin. Jos esimerkiksi maksu näytetään, silloin näytetään myös kaikki sen maksukirjauskansion maksut, jossa se luotiin. Jos lasku tai maksu näytetään ja jos se oli luotu yleisessä kirjauskansiossa, sitten kaikki sen yleisen kirjauskansion asiakirjat näytetään, jos se luotiin. Lisäksi näytetään kaikki kyseiseen asiakirjaluetteloon liittyvät tilitykset. Kun tarkastelet liittyviä maksuja, tämän painikkeen otsikko muuttuu muotoon **Näytä tilitykset**. Valitse **Näytä tilitykset**, jos haluat näyttää vain tapahtumat, jotka näytettiin, kun avasit **Näytä tilitykset** -valintaikkunan ensimmäisen kerran.
    - **Näytä historia** – Näytä tositteiden tilityshistoria. Sulje valintaikkuna valitsemalla **Sulje**.
    - **Näytä kirjanpito** – Näytä valittuihin asiakirjoihin liittyvät kaikki tositteet. Sulje valintaikkuna valitsemalla **Sulje**.
    - **Vie** – vie valitus tositteet Microsoft Exceliin.
    - **Tilitä tapahtumat** – Tämä painike ilmestyy vain, jos valittua alkuperäistä asiakirjaa ei ole vielä kokonaan tilitetty. Kun valitset tämän painikkeen, näkyviin tulee **Tilitä tapahtumat** -valintaikkuna, jossa voit valita tilitettävät tapahtumat.
    - **Kumoa tilitykset** – Tämä painike ilmestyy vain, jos valittua alkuperäistä asiakirjaa ei ole vielä kokonaan tilitetty. Kun valitset tämän painikkeen, näkyviin tulee **Kumoa tilitykset** -valintaikkuna, jossa voit kumota tätä asiakirjaa varten tehdyt tilitykset.

## <a name="global-transactions"></a>Yleiset tapahtumat

**Yleiset tapahtumat** -painike näkyy myös **Toimittajatapahtumat**-luettelosivulla. Tämän painikkeen avulla voit tarkastella toimittajan kaikkia tapahtumia kaikissa yrityksissä. **Toimittajatapahtumat**-luettelosivulla näytetään vain niiden yritysten tapahtumat, joihin käyttäjillä on pääsy suojausasetustensa mukaan.

Luettelosivulla näytetään kaikkien niiden toimittajien tapahtumat, joilla on sama osapuolen tunnus kuin ensin valitsemallasi toimittajalla. Esimerkiksi jos yhden yrityksen toimittajalla US-001 on sama osapuolen tunnus kuin toisen yrityksen toimittajalla DE-001, näytetään kummankin toimittajan tunnuksen kaikki tapahtumat.

**Toimittajatapahtumat**-luettelosivun valikot vaihtelevat tapahtumaan liittyvän yrityksen mukaan. Esimerkiksi jos toiminto on käytettävissä vain sveitsiläisille yrityksille, tämän toiminnon valikkovaihtoehdot näkyvät vain, kun valitaan sveitsiläinen tapahtuma.

Voit käyttää toimintoa seuraavien ohjeiden mukaisesti.

1. Valitse **Ostoreskontra** \> **Kaikki toimittajat**.
2. Valitse toimittaja ja valitse sitten **Toimittaja**-välilehden **Tapahtumat**-ryhmässä **Yleiset tapahtumat**.

## <a name="more-transaction-filters"></a>Lisää tapahtumasuodattimia

Avoimet tapahtumat näyttävä suodatin on korvattu uudella suodattimella, joka näyttää useampia tapahtumien yhdistelmiä. Seuraavat vaihtoehdot ovat käytettävissä **Näytä**-kentässä:

- **Kaikkil** – Näytä valitujen toimittajien kaikki tapahtumat (avoimet ja suljetut).
- **Suljettu** – Näytä vain tapahtumat, jotka on kokonaan tilitetty ja suljettu.
- **Avoin** – Näytä vain tapahtumat, joita ei ole kokonaan tilitetty.
- **Avoimet sisältäen tällä päivämäärällä tai sen jälkeen suljetut** – Näytä vain tapahtumat, joita ei ole kokonaan tilitetty tai jotka on tilitetty määritetyn päivämäärän jälkeen. Kun valitset tämän vaihtoehdon, voit muuttaa suodattimen vieressä näkyvää päivämäärää. Tapahtumat, joilla on **Viimeisin tilityspäivämäärä** -arvo määritettynä päivänä tai sen jälkeen, näkyvät luettelossa, vaikka nämä tapahtumat on kokonaan tilitetty nykyisenä päivämääränä. Saldo edustaa kuitenkin nykyisen päivämäärän saldoja, ei valitun päivämäärän saldoja.

Piilota valuutan muuntotapahtumat valitsemalla **Piilota valuuttojen revalvaatiot** -valintaruutu.

## <a name="modify-due-dates-and-discount-dates"></a>Eräpäivien ja alennuspäivämäärien muokkaaminen

Voit päivittää avointen asiakastapahtumien eräpäivät ja alennuksen päivämäärät. Voit lisätä versiossa 8.1. eräpäivät **Toimittajatapahtumat**-luettelosivulle. Napsauttamalla eräpäivää **Toimittajatapahtumat**-luettelosivulla, voit myös muuttaa eräpäiviä, alennuksen päivämääriä, maksuehtoja ja käteisalennuksen ehtoja **Päivitä eräpäivää ja käteisalennuksen päivämääriä** -valintaikkuna.

### <a name="activate-the-feature"></a>Toiminnon aktivoiminen

Voit lisätä eräpäiviä **Toimittajatapahtumat**-luettelosivulle ja muuttaa tapahtuman maksuasetuksia **Päivitä eräpäivää ja käteisalennuksen päivämääriä** -valintaikkunan avulla seuraavien ohjeiden mukaisesti.

1. Valitse **Ostoreskontra \> Asetukset \> Ostoreskontran parametrit**.
2. Määritä **Tilitykset**-välilehdessä **Näytä eräpäivä ja salli muokkaus** -vaihtoehdon arvoksi **Kyllä**.
3. Jotta toiminto voidaan ottaa käyttöön, toimittajatapahtumiin on lisätty uusia kenttiä. Nämä kentät täytetään, kun uusi tapahtuma on valmis. Ne myös täytetään, kun avaat **Päivitä eräpäivää ja käteisalennuksen päivämääriä** -valintaikkunan. Kun määrität **Näytä eräpäivä ja salli muokkaus** -vaihtoehdoksi **Kyllä**, näyttöön tulee **Päivitä maksutiedot** -valintaikkuna.  Voit päivittää nykyiset tapahtumat heti valitsemalla **Päivitä kaikki nykyiset tapahtumat**. Vaihtoehtoisesti voit täyttää vain uusien tapahtumien kentätä valitsemalla **Jatka ilman päivitystä**.

Eräpäivä lisätään nyt **Toimittajatapahtumat**-luettelosivulle, joten tapahtumien eräpäivän ja käteisalennuksen päivämäärien muokkaus helpottuu.

### <a name="modify-the-payment-settings"></a>Maksuasetusten muuttaminen

**Toimittajatapahtumat**-luettelosivu näyttää toimittajan kaikki tapahtumat. Kun valitset tapahtuman eräpäivän, näyttöön tulee valintaikkuna. Tämä valintaikkuna näyttää eräpäivän peruspäivämäärän ja alennuslaskelmat, eräpäivän, maksuehdot, käteisalennuksen ehdot ja käteisalennuksen päivämäärät.

Kukin kenttä vaikuttaa eri tavalla tapahtumaan, kun muokkaat sitä:

- **Muokkaa peruspäivämäärää** – Eräpäivää ja alennuspäivämääriä muutetaan siten, että peruspäivämäärä on asiakirjan päivämäärä.
- **Muokkaa eräpäivää** – Vain eräpäivä muuttuu.
- **Muokkaa alennuksen päivämääriä** – Vain alennuksen päivämääriä muutetaan.
- **Muokkaa maksuehtoja** – Eräpäivää muutetaan peruspäivämäärän ja maksuehtojen perusteella.
- **Muokkaa käteisalennuksen ehtoja** – Käteisalennuksia muutetaan peruspäivämäärän ja käteisalennuksen ehtojen perusteella.

Kun olet muokannut maksuasetuksia, tallenna muutokset valitsemalla **Sulje**.
