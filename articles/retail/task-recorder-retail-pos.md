---
title: "Myyntipisteen tehtävien tallennustoiminto ja ohje"
description: "Tässä ohjeaiheessa kuvataan, miten tehtävien tallennustoimintoa käytetään Retail Modern POS -sovelluksessa ja pilvimyyntipisteessä."
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: e66208ccceb4c248c2704bb7358d77447e032205
ms.openlocfilehash: 43360ea18ccc0fc4622f6da70ff10f2aca8b56c8
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---

# <a name="task-recorder-and-help-for-pos"></a>Myyntipisteen tehtävien tallennustoiminto ja ohje

Tässä ohjeaiheessa kuvataan, miten tehtävien tallennustoimintoa käytetään Retail Modern POS -sovelluksessa ja pilvimyyntipisteessä.

<a name="overview"></a>Yleiskuvaus
--------

Tehtävien tallennustoiminto Retail Modern POS -sovelluksessa on uusi ratkaisu, jonka reagointikyky on suuri. Se sisältää joustavan ohjelmointirajapinnan (API:n), joka mahdollistaa laajennettavuuden ja jonka avulla integrointi liiketoimintaprosessien tallenteiden kuluttajien kanssa on saumatonta. Microsoft Dynamics Lifecycle Servicesin ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) tehtävien tallennustoiminnon integrointia liiketoimintaprosessin mallintajan (BPM) työkalun kanssa on siirretty myöhemmäksi. Tämän vuoksi käyttäjät voivat jatkaa monipuolisten liiketoimintaprosessien kaavioiden tekemistä tallenteista ja analysoida ja suunnitella sovelluksia.

## <a name="architecture"></a>Arkkitehtuuri
Tehtävien tallennustoiminto voi tallentaa käyttäjän toiminnot asiakasohjelmassa erittäin tarkasti. Kukin ohjausobjekti mitataan, ja tehtävien tallennustoiminnolle ilmoitetaan käyttäjän toiminnon suorituksesta. Ohjausobjekti ilmoittaa tehtävien tallennustoiminnolle, että tapahtuma on suoritettu, ja välittää reaaliaikaisesti kaikki vastaavaa käyttäjän toimintoa koskevat asianmukaiset tiedot. Näistä tiedoista tehtävien tallennustoiminto voi tallentaa käyttäjän toiminnon tyypin (kuten painikkeen valinta, arvon syöttö tai siirtyminen) ja käyttäjän toimintoon liittyvät tiedot (kuten syöttötietojen arvon ja tyypin, lomakkeen kontekstin tai tietueen kontekstin). Tehtävien tallennustoiminto säilyttää niin paljon tietoja, että niiden avulla voidaan varmistaa tallenteen toisto juuri niin kuin käyttäjä toiminnon suorittanut tallennuksen hetkellä. (Toistotoimintoa ei ole vielä otettu käyttöön Retail Modern POS -sovelluksessa ja pilvimyyntipisteessä.)

## <a name="basic-configuration"></a>Peruskonfigurointi
Voit ottaa tehtävätallenteen käyttöön myyntipisteessä seuraavasti.

1.  Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Kassakoneet**.
2.  Valitse kassakone, jolle haluat ottaa tehtävätallenteen käyttöön.
3.  Valitse **Kassakone**-välilehden **Yleinen**-pikavälilehden **Ota tehtävän tallennus käyttöön** -vaihtoehdon arvoksi **Kyllä**.
4.  Valitse **Tallenna**.
5.  Siirry kohtaan **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulu**.
6.  Valitse **Kassakoneet (1090)** -työ ja valitse sitten **Suorita nyt**.

## <a name="create-a-recording"></a>Tallenteen luominen
Näiden ohjeiden avulla voit luoda uuden tallenteen tehtävien tallennustoiminnolla.

1.  Käynnistä Retail Modern POS tai pilvimyyntipiste ja kirjaudu sisään.
2.  Valitse **Asetukset**-sivun **Tehtävien tallennustoiminto** -osassa **Avaa tehtävien tallennustoiminto**. **Tehtävien tallennustoiminto** -ruutu avautuu. Valitse oikeassa yläkulmassa oleva **Sulje**-painike (**X**), kun haluat sulkea **Tehtävien tallennustoiminto** -ruudun ennen uuden tallenteen aloittamista. Voit avata ruudun uudelleen toistamalla vaiheen 2.
[![Tehtävien tallennustoiminto -ruutu](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3.  Kirjoita tallenteen nimi ja kuvaus ja valitse sitten **Aloita**. Tallennusistunto alkaa heti, kun valitset **Aloita**.

**Huomautus:** Jos valitset oikeassa yläkulmassa olevan **Sulje**-painikkeen (**X**) tallennuksen ollessa käynnissä, **Tehtävien tallennustoiminto** -ruutu suljetaan, mutta tallennusistuntoa ei päätetä. Voit avata Tehtävien tallennustoiminto -ruudun uudelleen valitsemalla näytön yläosassa olevan **Ohje**-painikkeen (kysymysmerkki). 

[![Kysymysmerkki](./media/help.jpg)](./media/help.jpg)

4.  Kun valitset **Aloita**, tehtävien tallennustoiminto siirtyy tallennustilaan. **Tehtävien tallennustoiminto** -ruutu näyttää tallennusprosessiin liittyvät tiedot ja ohjausobjektit.
5.  Suorita toimintoja, joita haluat suorittaa Retail Modern POS -sovelluksen tai pilvimyyntipisteen käyttöliittymässä.
6.  Kun lopetat tallennusistunnon, valitse **Lopeta**.

## <a name="download-options"></a>Latausvalinnat
Tallennusistunnon loputtua näkyvissä on useita vaihtoehtoja, joiden avulla tallenteen voi ladata. 
[![Latausvalinnat](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>Tallenna tälle tietokoneelle

Tallennepaketin avulla voi toistaa tehtäväoppaan, ylläpitää tallennetta ja muokata tallenteen huomautuksia. (Tätä toimintoa ei ole vielä otettu käyttöön Retail Modern POS -sovelluksessa ja pilvimyyntipisteessä.)

### <a name="export-as-word-document"></a>Vie Word-tiedostona

Tallenteen voi tallentaa Microsoft Word -asiakirjana. Asiakirja sisältää tallennetut vaiheet ja näyttökuvat.

### <a name="save-as-developer-recording"></a>Tallenna kehittäjien tallenteena

Kehittäjät voivat käyttää käsittelemätöntä tallennetiedostoa moniin tarkoituksiin, esimerkiksi testikoodin muodostamiseen. (Tätä toimintoa ei ole vielä otettu käyttöön.)

## <a name="recording-controls"></a>Tallennuksen säätimet
### <a name="recording-controlsmediacontrolsjpgmediacontrolsjpg"></a>[![Tallennuksen säätimet](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>P&ysäytä

Valitse **Lopeta**, kun haluat lopettaa tallennusistunnon. Huomaa, että lopettamisen jälkeen et voi käynnistää istuntoa uudelleen. Tämän vuoksi kannattaa varmistaa, että tallenne on valmis, ennen kuin se lopetetaan.

### <a name="pause"></a>Keskeytä

Valitse **Keskeytä**, kun haluat pysäyttää tallennusistunnon väliaikaisesti ja jatkaa toimintoa. **Keskeytä**-painikkeen valinnan jälkeen suoritettuja vaiheita ei tallenneta.

### <a name="continue"></a>Jatka

Voit jatkaa tallennusistuntoa keskeytyksen jälkeen, kun valitset **Jatka**.

### <a name="capture-screenshots"></a>Tallenna näyttökuvia

Tehtävien tallennustoiminto voi tallentaa Retail Modern POS -käyttöliittymän näyttökuvia liiketoimintaprosessin tallennuksen aikana. Voit ottaa näyttökuvatoiminnon käyttöön määrittämällä **Tallenna näyttökuvia** -asetukseksi **Kyllä** ja tekemällä tallenteen. Kun tallenne on valmis, valitse **Pysäytä** ja lataa Word-asiakirja. Asiakirja sisältää vaiheet ja liittyvät näyttökuvat.

#### <a name="note"></a>Seteli
> Näyttökuvien tallennustoimintoa ei tueta Modern POS -versiossa.

### <a name="start-task-and-end-task"></a>Tehtävän aloittaminen ja lopettaminen

Voit määrittää ryhmiteltyjen vaiheiden joukon aloituksen ja lopetuksen **Aloita tehtävä**- ja **Lopeta** **tehtävä** -painikkeen avulla. Lisää Aloita tehtävä -vaihe valitsemalla **Aloita tehtävä**. Suorita sitten vaiheet, jotka lisätään ryhmään. Kun ryhmän vaiheet on suoritettu, valitse **Lopeta tehtävä**. Tehtävien avulla menettelyiden järjestäminen on helpompaa. Tehtävät voivat olla sisäkkäisiä muiden tehtävien kanssa. Näin myös pitkien ja monimutkaisten liiketoimintaprosessien järjestäminen onnistuu paremmin.

## <a name="adding-annotations"></a>Huomautusten lisääminen
Huomautus on lisäteksti, joka lisätään vaiheeseen tallennuksen aikana. Huomautusten avulla voidaan esimerkiksi antaa käyttäjille lisätietoja tai ohjeita. Huomautuksia voi lisätä vaiheen edelle ja sen jälkeen. Huomautuksia voi lisätä mihin tahansa vaiheeseen **Muokkaa**-painikkeen avulla (kynäsymboli), joka löytyy vaiheen oikealta puolelta. 

[![Vaiheen Muokkaa-painike](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>Tekstit ja muistiinpanot

**Tekstit**- ja **Muistiinpanot**-kenttien avulla voi lisätä tekstiä, jotka liitetään tehtäväoppaan vaiheeseen.
[![Teksti- ja Muistiinpanot-kenttä](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>Teksti

**Teksti**-kenttään syötetty kenttä näkyy tehtäväoppaan vaiheen tekstin *yläpuolella*. Tämä sijainti on sopiva tekstille, joka on tarkoitettu käyttäjän luettavaksi ennen vaiheen suoritusta.

#### <a name="notes"></a>Muistiinpanot

**Muistiinpanot**-kenttään syötetty kenttä näkyy tehtäväoppaan vaiheen tekstin *alapuolella*. Käyttäjän on laajennettava vaiheen teksti ponnahdusikkunassa, jotta sen voi lukea. Tämä sijainti on sopiva valinnaisesti luettavalle materiaalille tai muille tiedoille, jotka voivat olla hyödyllisiä, mutta joita ei vaadita toiminnon suorittamista varten.

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a>Retail Modern POS -sovelluksen ja pilvimyyntipisteen ohje
Voit näyttää omat mukautetut tehtävätallenteet Retail Modern POS -sovelluksen ja pilvimyyntipisteen ohjeruudussa niin, että niitä voidaan tarkastella tekstinä, kun tallennat tehtävätallenteet ensin omaan BPM-kirjastoon ja päivität sitten ohjejärjestelmän parametrit niin, että ne osoittavat BPM-kirjastoon. Lisätietoja on kohdassa [Yhteyden muodostaminen ohjejärjestelmään.](../fin-and-ops/get-started/help-connect.md). Retail Modern POS -sovelluksen ja pilvimyyntipisteen ohje tekee haut LCS-palvelusta reaaliaikaisesti. Se tekee haun kaikista BPM-kirjastoista, jotka on valittu Microsoft Dynamics 365 for Retailin ohjejärjestelmän parametreissa, ja näyttää hakua vastaavat tulokset. Voit käyttää **Ohje**-valikkoa valitsemalla näytön yläosassa olevan **Ohje**-painikkeen (kysymysmerkki) kirjoittamalla hakuruutuun prosessin nimen ja painamalla hakupainiketta. 

[![Ohje-painike](./media/help.jpg)](./media/help.jpg) 

Kun valitset hakutuloksista tehtäväoppaan, voit tarkastella vaiheita ohjeaiheena tai viedä ne Word-asiakirjaan. 
#### <a name="note"></a>Seteli
> Retail Modern POS -sovelluksen ja pilvimyyntipisteen ohje ei anna tehtäväohjeita sen mukaan, mikä lomake tai tehtävä on käsiteltävänä. Kirjoita hakukenttään prosessin nimi ja valitse sitten on **Haku**.


