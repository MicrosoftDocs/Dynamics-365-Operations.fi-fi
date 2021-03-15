---
title: USMCA-alkuperätodistus
description: Tämän toiminnon avulla voidaan tulostaa USMCA (United States-Mexico-Canada) -sopimuksen edellyttämät alkuperätodistusasiakirjat.
author: Henrikan
manager: tfehr
ms.date: 10/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-23
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: de0917f6734d81248f8aa588bd0c5dec7d056219
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006413"
---
# <a name="usmca-certification-of-origin"></a>USMCA-alkuperätodistus

[!include [banner](../includes/banner.md)]

Tämän toiminnon avulla voidaan tulostaa USMCA (United States-Mexico-Canada) -sopimuksen edellyttämät alkuperätodistusasiakirjat.

*USMCA-alkuperätodistusasiakirja* sisältää ilmoituksessa vähintään tarvittavat tietoelementit. Jotkin tietoelementit voidaan täyttää valmiiksi ennen tulostamista, kun taas toiset on täytettävä manuaalisesti tulostamisen jälkeen. Tullietuuskohtelun saaminen edellyttää, että asiakirja on täytetty ja maahantuojan hallussa ilmoitusta tehtäessä. Asiakirjan voi täyttää maahantuoja, viejä tai valmistaja.

Asiakirjan voi tulostaa yhtä lähetystä varten **Kaikki lähetykset** -luettelosivulla tai **Lähetyksen tiedot** -sivulla.

Asiakirjaa voi käyttää vain, jos yrityksen ensisijainen osoite on Yhdysvalloissa.

Asiakirjan tulostusvalinnan mukaan asiakirjaan voidaan täyttää valmiiksi järjestelmässä olevia tietoja. Tulostetun asiakirjan tietoja voidaan vaihtaa tai niitä voidaan lisätä viemällä tulostettu asiakirja muokattavassa muodossa, kuten Microsoft Word -asiakirjana. Viennin jälkeen tarvittavat muutokset voidaan tehdä ennen ilmoituksen tekemistä.

## <a name="turn-on-the-usmca-feature"></a>USMCA-toiminnon ottaminen käyttöön

Ennen kuin USMCA-toimintoa voidaan käyttää, se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Kuljetustenhallinta*
- **Toiminnon nimi:** *USMCA-alkuperätodistusasiakirja*

## <a name="document-content"></a>Asiakirjan sisältö

USMCA-alkuperätodistusasiakirja sisältää seuraavat tietoelementit:

- Osoite-elementit
- Sertifioinnin myöntävän osapuolen rooli
- Yksittäinen lähetys
- Laskut
- Valittu kausi
- Nimikkeen tiedot
- Sertifioijan allekirjoitus
- Sivujen määrä

Lisätietoja kustakin elementistä ja niiden arvoista on tämän aiheen jäljempänä olevissa osissa.

## <a name="print-a-usmca-certification-of-origin-document"></a>USMCA-alkuperätodistusasiakirjan tulostaminen

Lähetyksen USMCA-alkuperätodistusasiakirja tulostetaan seuraavasti:

1. Tee jompikumpi seuraavista toimista:
    - Valitse ensin **Kuljetustenhallinta > Lähetykset > Kaikki lähetykset** ja valitse sitten lähetys, jolle haluat tulostaa asiakirjan.
    - Avaa sen lähetyksen **Lähetyksen tiedot** -sivu, jolle haluat tulostaa asiakirjan. (Sen voi tehdä monella eri tavalla esimerkiksi **Kaikki lähetykset** -sivulta.)
1. Avaa toimintoruudussa **Lähetykset**-välilehti ja valitse **Tulosta**-ryhmässä **USMCA-alkuperätodistus**.
1. **Alkuperätodistus**-valintaikkuna avautuu. Määritä seuraavissa aliosissa kuvatut asetukset ja luo asiakirja sitten valitsemalla **OK**.
1. Asiakirjan esikatselu avautuu. Tulosta tai vie asiakirja tarpeen mukaan käyttämällä toimintoruudun komentoja.

### <a name="certifying-party"></a>Todistuksen antaja

Määritä avattavassa **Todistuksen antama** -luettelossa asiakirjan tulostavan osapuolen tyyppi. Määritä, onko todistuksen antaja *viejä*, *viejä ja valmistaja*, *valmistaja* vai *maahantuoja* tai jätä se tyhjäksi, jos todistuksen antaja ei ole mikään niistä. Valittu vaihtoehto määrittää, mitä tulostetaan asiakirjan osoiteosiin.

Valittu **todistuksen antaja** sisällytetään tulostettuun asiakirjaan.

Asiakirja voidaan tulostaa sekä saapuville että lähteville lähetyksille. Valitse saapuvissa lähetyksissä *maahantuoja* **todistuksen antajaksi**.

Seuraavassa taulukossa käsitellään tietotyyppejä, jotka sisällytetään asiakirjaan valitun **todistuksen antajan** perusteella.

| Todistuksen&nbsp;antaja | kuvaus |
|---|---|
| *\[Tyhjä\]* | Lisää seuraavat tiedot asiakirjaan:<ul><li>**Sertifioijan tiedot**: Käyttää lähetysvaraston osoitteen tietoja, jos ne ovat käytettävissä. Muussa tapauksessa käytetään lähetyspaikan osoitetta, jos se on käytettävissä. Muutoin käytetään yrityksen Supply Chain Managementissa valittua osoitetta.</li><li>**Viejän tiedot**: tyhjä</li><li>**Valmistajan tiedot**: tyhjä</li><li>**Maahantuojan tiedot**: tyhjä</li><ul>|
| *Viejä* | Lisää seuraavat tiedot asiakirjaan:<ul><li>**Sertifioijan tiedot**: Käyttää lähetysvaraston osoitteen tietoja, jos ne ovat käytettävissä. Muussa tapauksessa käytetään lähetyspaikan osoitetta, jos se on käytettävissä. Muutoin käytetään yrityksen Supply Chain Managementissa valittua osoitetta.</li><li>**Viejän tiedot**: käyttää yrityksen osoitetietoja.</li><li>**Valmistajan tiedot**: tyhjä</li><li>**Maahantuojan tiedot**: käyttää liittyvän myyntitilauksen laskutustiliä.</li><ul>|
| *Viejä ja valmistaja* | Lisää seuraavat tiedot asiakirjaan:<ul><li>**Sertifioijan tiedot**: Käyttää lähetysvaraston osoitteen tietoja, jos ne ovat käytettävissä. Muussa tapauksessa käytetään lähetyspaikan osoitetta, jos se on käytettävissä. Muutoin käytetään yrityksen Supply Chain Managementissa valittua osoitetta.</li><li>**Viejän tiedot**: käyttää yrityksen osoitetietoja.</li><li>**Valmistajan tiedot**: käyttää yrityksen osoitetietoja.</li><li>**Maahantuojan tiedot**: käyttää liittyvän myyntitilauksen laskutustiliä.</li><ul>|
| *Tuoja* | Lisää seuraavat tiedot asiakirjaan:<ul><li>**Sertifioijan tiedot**: Käyttää lähetysvaraston osoitteen tietoja, jos ne ovat käytettävissä. Muussa tapauksessa käytetään lähetyspaikan osoitetta, jos se on käytettävissä. Muutoin käytetään yrityksen Supply Chain Managementissa valittua osoitetta.</li><li>**Viejän tiedot**: tyhjä</li><li>**Valmistajan tiedot**: tyhjä</li><li>**Maahantuojan tiedot**: käyttää yrityksen osoitetietoja.</li><ul>|
| *Tuottaja* | Lisää seuraavat tiedot asiakirjaan:<ul><li>**Sertifioijan tiedot**: Käyttää lähetysvaraston osoitteen tietoja, jos ne ovat käytettävissä. Muussa tapauksessa käytetään lähetyspaikan osoitetta, jos se on käytettävissä. Muutoin käytetään yrityksen Supply Chain Managementissa valittua osoitetta.</li><li>**Viejän tiedot**: tyhjä</li><li>**Valmistajan tiedot**: käyttää yrityksen osoitetietoja.</li><li>**Maahantuojan tiedot**: tyhjä</li><ul>|

### <a name="has-various-producers"></a>Sisältää useita tuottajia

Avattava **Todistuksen antaja** -luettelo hallitsee tekstiä, jota käytetään asiakirjan valmistajan tietoja. Valitse yksi seuraavista:

- *Useita tuottajia* – tulostaa tekstini Useita tuottajan tietoihin.
- *Saatavana pyydettäessä* – tulostaa tuottajan tietoihin tekstin Saatavana maahantuojaviranomaisten pyytäessä.

Kun **Todistuksen antaja** -asetukseksi on määritetty *Viejä ja valmistaja* tai *Valmistaja*, **On useita valmistajia** -asetus ohitetaan ja valmistajan osoitetiedot ovat samat kuin sertifioijan.

### <a name="blanket-period"></a>Valittu kausi

Luo puitekausi käyttämällä **Puitekausi alkaa**- ja **Puitekausi päättyy** -asetuksia. Tämän puitekauden aikana asiakirja kattaa useita samanlaisten tuotteiden lähetyksiä, vaikka asiakirja tulostetaan vain yhdelle lähetykselle. Puitekauden päivämäärät voidaan määrittää ilman rajoituksia, ja se lisätään asiakirjaan. Nämä asetukset voidaan jättää myös tyhjäksi tai määrittää menneisyyteen.

### <a name="is-single-shipment"></a>On yksittäinen lähetys

Määritä **Todistuksen antaja** -valintaikkunassa **On yksittäinen lähetys** -asetukseksi jokin seuraavista:

- *Kyllä* – lisää Yksittäinen lähetys: kyllä laskutusnumeron viereen.
- *Ei* – mitään ei lisätä.

## <a name="other-information-included-in-the-document"></a>Muut asiakirjaan sisällytettävät tiedot

Valinnaisten **Alkuperätodistus**-valintaikkunassa valittavien elementtien lisäksi USMCA-alkuperätodistusasiakirja sisältää tietoja ja mukautettuja kenttiä, joiden yhteenveto on seuraavissa aliosissa. Osa näistä tiedoista on annettava manuaalisesti asiakirjan luonnin jälkeen.

### <a name="invoice-number"></a>Laskun numero

Toimituksiin liittyvien myyntilaskujen tunnukset tulostetaan asiakirjaan puitekaudesta riippumatta. Laskun numerot tulostetaan **On yksittäinen toimitus** -valinnasta riippumatta.

### <a name="item-details"></a>Nimikkeen tiedot

Asiakirjassa on useita osia, joissa on seuraavat nimikkeen tiedot:

- **SKU-numero**: tulostaa vapautetun tuotteen nimiketunnuksen.

- **Kuvaus**: Tulostaa joko vapautetun tuotteen kuvauksen tai nimen. Jos käyttäjänkielinen kuvaus on olemassa, se tulostetaan. Jos tällaista kuvausta ei ole, tulostetaan käyttäjänkielinen nimi. Jos nimeä ei ole, nimikkeen nimi tulostetaan.

- **Yhtenäistetyn tariffiluokittelujärjestelmä**: Tulostaa tuotteeseen liitetyn yhtenäistetyn tariffinimikkeistön. Nämä nimikkeistöt voidaan määrittää valitsemalla **Kuljetustenhallinta \> Määritys \> Kuljetusstandardi \> Harmonisoitu tariffiaikataulu**.

- **Alkuperäehto:** tämän osan tiedot on annettava, kun asiakirja vapautetaan ensimmäisen kerran.

- **Alkuperämaa:** Tulostaa alkuperämaan, joka otetaan käyttöön valitsemalla **Tuotetietojen hallinta \> Määritys \> Tuotteen yhteensopivuus \> Alkuperämaa** (katso myös [Alkuperämaa](../pim/country-of-origin.md)). Alkuperämaan ISO-koodi tulostetaan lähetyksen toimitusosoitteen ja nimikkeen kohdemaan tai -alueen perusteella. Jos alkuperämaata ei määritetä, tämä arvo palautuu asetukseen, joka on kohdassa **Vapautettu tuote \> Ulkomaankauppa \> Alkuperä**. Jos alkuperämaan tietoja ei edelläänkään löydy, alkuperämaa on annettava manuaalisesti asiakirjan luonnin jälkeen.

### <a name="certifier-signature-and-date"></a>Sertifioijan allekirjoitus ja päiväys

Tämä on annettava manuaalisesti asiakirjan luomisen jälkeen.

### <a name="consists-of-number-of-pages"></a>Sivujen määrä

Todistuksen allekirjoittavan käyttäjän on annettava manuaalisesti sivujen määrä (varmistusta varten) asiakirjojen luonnin jälkeen.

### <a name="page-numbers"></a>Sivunumerot

Asiakirjan alareunaan tulostettu käytössä oleva sivu ja sivujen määrä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]