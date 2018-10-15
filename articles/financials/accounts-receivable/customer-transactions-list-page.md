---
title: "Näytä avoimien asiakastapahtumien listaussivu"
description: "Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 for Finance and Operationsin asiakastapahtumien luettelosivusta."
author: mikefalkner
manager: aolson
ms.date: 08/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: 79479f6949c52830918598583ee91dd85d2d7ac3
ms.contentlocale: fi-fi
ms.lasthandoff: 10/01/2018

---

# <a name="customer-transactions-list-page"></a>Näytä avoimien asiakastapahtumien listaussivu

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Näytä tilitykset

Toimintoruudun **Näytä tilitykset** -painikkeen avulla voit käyttää nopeasti tilityshistoriaa ja muita koko tilitystapahtumaa koskevia tietoja. Voit näyttää myös lisätapahtumat, jotka liittyvät valittuihin tapahtumiin joko siksi, että ne sisältyvät samaan tilitykseen, tai siksi, että ne ovat samassa maksukirjauskansiossa luotuja maksuja.

1. Valitse **Myyntireskontra \> Kaikki asiakkaat**.
2. Valitse asiakas, johon liittyy tapahtumia, ja valitse sitten toimintoruudussa **Asiakas**-välilehden **Tapahtumat**.
3. Valitse tutkittava tapahtuma ja valitse sitten toimintoruudussa **Näytä tilitykset**.

    **Näytä tilitykset** -valintaikkuna tulee näkyviin ja näyttää valitun tapahtuman ja kaikki siihen täsmäytetyt asiakirjat. Tämä valintaikkunan muistuttaa tilityshistorianäkymää, mutta se sisältää kaikki liittyvät asiakirjat.

4. Voit valintaikkunassa tehdä erilaisia tehtäviä. Valitse vähintään yksi tosite ja sitten jokin seuraavista painikkeista:

    - **Näytä liittyvät** – Näytä kaikki maksukirjauskansion tapahtumat, jotka luotiin valittuun asiakirjaan liittyvässä maksukirjauskansiossa. Lisäksi näytetään kaikki kyseisiin maksuihin liittyvät tilitykset. Kun tarkastelet liittyviä maksuja, tämän painikkeen otsikko muuttuu muotoon **Näytä tilitykset**. Valitse **Näytä tilitykset**, jos haluat näyttää vain tapahtumat, jotka näytettiin, kun avasit **Näytä tilitykset** -valintaikkunan ensimmäisen kerran.
    - **Näytä historia** – Näytä tositteiden tilityshistoria. Sulje valintaikkuna valitsemalla **Sulje**.
    - **Näytä kirjanpito** – Näytä valittuihin asiakirjoihin liittyvät kaikki tositteet. Sulje valintaikkuna valitsemalla **Sulje**.
    - **Vie** – vie valitus tositteet Microsoft Exceliin.
    - **Tilitä tapahtumat** – Tämä painike ilmestyy vain, jos valittua alkuperäistä asiakirjaa ei ole vielä kokonaan tilitetty. Kun valitset tämän painikkeen, näkyviin tulee **Tilitä tapahtumat** -valintaikkuna, jossa voit valita tilitettävät tapahtumat.
    - **Kumoa tilitykset** – Tämä painike ilmestyy vain, jos valittua alkuperäistä asiakirjaa ei ole vielä kokonaan tilitetty. Kun valitset tämän painikkeen, näkyviin tulee **Kumoa tilitykset** -valintaikkuna, jossa voit kumota tätä asiakirjaa varten tehdyt tilitykset.

## <a name="global-transactions"></a>Yleiset tapahtumat

**Yleiset tapahtumat** -painike on lisätty asiakassivulle. Tämän painikkeen avulla voit tarkastella asiakkaan kaikkia tapahtumia kaikissa yrityksissä. **Asiakastapahtumat**-luettelosivulla näytetään vain niiden yritysten tapahtumat, joihin käyttäjillä on pääsy suojausasetustensa mukaan.

Luettelosivulla näytetään kaikkien niiden asiakkaiden tapahtumat, joilla on sama osapuolen tunnus kuin ensin valitsemallasi asiakkaalla. Esimerkiksi jos yhden yrityksen asiakkaalla US-001 on sama osapuolen tunnus kuin toisen yrityksen asiakkaalla DE-001, näytetään kummankin asiakkaan tunnuksen kaikki tapahtumat.

**Asiakastapahtumat**-luettelosivun valikot vaihtelevat tapahtumaan liittyvän yrityksen mukaan. Esimerkiksi jos toiminto on käytettävissä vain sveitsiläisille yrityksille, tämän toiminnon valikkovaihtoehdot näkyvät vain, kun valitaan sveitsiläinen tapahtuma.

Voit käyttää toimintoa seuraavien ohjeiden mukaisesti.

1. Valitse **Myyntireskontra \> Kaikki asiakkaat**.
2. Valitse asiakas ja valitse sitten **Asiakas**-välilehden **Tapahtumat**-ryhmässä **Yleiset tapahtumat**.

## <a name="more-transaction-filters"></a>Lisää tapahtumasuodattimia 

Avoimet tapahtumat näyttävä suodatin on korvattu uudella suodattimella, joka näyttää useampia tapahtumien yhdistelmiä. Seuraavat vaihtoehdot ovat käytettävissä **Näytä**-kentässä:

- **Kaikki** – Näytä valittujen asiakkaiden kaikki tapahtumat (avoimet ja suljetut).
- **Suljettu** – Näytä vain tapahtumat, jotka on kokonaan tilitetty ja suljettu.
- **Avoin** – Näytä vain tapahtumat, joita ei ole kokonaan tilitetty.
- **Avaa alkaen** – Näytä vain tapahtumat, joita ei ole kokonaantilitetty määrittämänäsi päivämääränä. Kun valitset tämän vaihtoehdon, voit muuttaa suodattimen vieressä näkyvää päivämäärää. Tapahtumat, joilla on **Viimeisin tilityspäivämäärä** -arvo määrittämäsi päivämäärän jälkeen, näkyvät luettelossa, vaikka nämä tapahtumat on kokonaan tilitetty nykyisenä päivämääränä. Saldo edustaa kuitenkin nykyisen päivämäärän saldoja, ei valitun päivämäärän saldoja.

Mukaan on myös lisätty suodatin, jonkaavulla voit piilottaa valuutan muuntamisen tapahtumat. Valitse vain **Piilota valuutan uudelleenarvostukset** -valintaruutu.

## <a name="more-easily-modify-due-dates-and-discount-dates"></a>Muokkaa helpommin eräpäiviä ja alennuksen päivämääriä

Voit päivittää avointen asiakastapahtumien eräpäivät ja alennuksen päivämäärät. Kokemusta on parannettu versiossa 8.1. Voit nyt lisätä eräpäivät **Asiakastapahtumat**-luettelosivulle. Napsauttamalla eräpäivää **Asiakastapahtumat**-luettelosivulla, voit myös muuttaa eräpäiviä, alennuksen päivämääriä, maksuehtoja ja käteisalennuksen ehtoja **Päivitä eräpäivää ja käteisalennuksen päivämääriä** -valintaikkunassa.

### <a name="activate-the-feature"></a>Toiminnon aktivoiminen

Voit lisätä eräpäiviä **Asiakastapahtumat**-luettelosivulle ja muuttaa tapahtuman maksuasetuksia **Päivitä eräpäivää ja käteisalennuksen päivämääriä** -valintaikkunan avulla seuraavien ohjeiden mukaisesti.

1. Valitse **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.
2. Määritä **Tilitykset**-välilehdessä **Näytä eräpäivä ja salli muokkaus** -vaihtoehdon arvoksi **Kyllä**.
3. Jotta toiminto voidaan ottaa käyttöön, asiakastapahtumiin on lisätty uusia kenttiä. Nämä kentät täytetään, kun uusi tapahtuma on valmis. Ne myös täytetään, kun avaat **Päivitä eräpäivää ja käteisalennuksen päivämääriä** -valintaikkunan. Kun määrität **Näytä eräpäivä ja salli muokkaus** -vaihtoehdoksi **Kyllä**, näyttöön tulee **Päivitä maksutiedot** -valintaikkuna.  Voit päivittää nykyiset tapahtumat heti valitsemalla **Päivitä kaikki nykyiset tapahtumat**. Vaihtoehtoisesti voit täyttää vain uusien tapahtumien kentätä valitsemalla **Jatka ilman päivitystä**.

Eräpäivä lisätään nyt **Asiakastapahtumat**-luettelosivulle ja voit helpommin muokata tapahtumien eräpäivää ja käteisalennuksen päivämääriä.

### <a name="modify-the-payment-settings"></a>Maksuasetusten muuttaminen

**Asiakastapahtumat**-luettelosivu näyttää asiakkaan kaikki tapahtumat. Kun valitset tapahtuman eräpäivän, näkyviin tulee **Päivitä eräpäivää ja käteisalennuksen päivämääriä** -valintaikkuna. Tämä valintaikkuna näyttää eräpäivän peruspäivämäärän ja alennuslaskelmat, eräpäivän, maksuehdot, käteisalennuksen ehdot ja käteisalennuksen päivämäärät.

Kukin kenttä vaikuttaa eri tavalla tapahtumaan, kun muokkaat sitä:

- **Muokkaa peruspäivämäärää:** Eräpäivää ja alennuspäivämääriä muutetaan siten, että peruspäivämäärä on asiakirjan päivämäärä.
- **Muokkaa eräpäivää:** Vain eräpäivää muutetaan.
- **Muokkaa alennuksen päivämääriä:** Vain alennuksen päivämääriä muutetaan.
- **Muokkaa maksuehtoja:** Eräpäivää muutetaan peruspäivämäärän ja maksuehtojen perusteella.
- **Muokkaa käteisalennuksen ehtoja:** Käteisalennuksia muutetaan peruspäivämäärän ja käteisalennuksen ehtojen perusteella.

Kun olet muokannut maksuasetuksia, tallenna muutokset valitsemalla **Sulje**.
