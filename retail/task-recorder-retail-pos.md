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
audience: Application User
ms.reviewer: 41
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 007a7e8a34f3f5a2d0d18eb3955822a8fd8bdd0a
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017


---

# Myyntipisteen tehtävien tallennustoiminto ja ohje
<a id="task-recorder-and-help-for-pos" class="xliff"></a>

Tässä ohjeaiheessa kuvataan, miten tehtävien tallennustoimintoa käytetään Retail Modern POS -sovelluksessa ja pilvimyyntipisteessä.

Yleiskuvaus
<a id="overview" class="xliff"></a>
--------

Tehtävien tallennustoiminto Retail Modern POS -sovelluksessa on uusi ratkaisu, jonka reagointikyky on suuri. Se sisältää joustavan ohjelmointirajapinnan (API:n), joka mahdollistaa laajennettavuuden ja jonka avulla integrointi liiketoimintaprosessien tallenteiden kuluttajien kanssa on saumatonta. Microsoft Dynamics Lifecycle Servicesin ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) tehtävien tallennustoiminnon integrointia liiketoimintaprosessin mallintajan (BPM) työkalun kanssa on siirretty myöhemmäksi. Tämän vuoksi käyttäjät voivat jatkaa monipuolisten liiketoimintaprosessien kaavioiden tekemistä tallenteista ja analysoida ja suunnitella sovelluksia.

## Arkkitehtuuri
<a id="architecture" class="xliff"></a>
Tehtävien tallennustoiminto voi tallentaa käyttäjän toiminnot asiakasohjelmassa erittäin tarkasti. Kukin ohjausobjekti mitataan, ja tehtävien tallennustoiminnolle ilmoitetaan käyttäjän toiminnon suorituksesta. Ohjausobjekti ilmoittaa tehtävien tallennustoiminnolle, että tapahtuma on suoritettu, ja välittää reaaliaikaisesti kaikki vastaavaa käyttäjän toimintoa koskevat asianmukaiset tiedot. Näistä tiedoista tehtävien tallennustoiminto voi tallentaa käyttäjän toiminnon tyypin (kuten painikkeen valinta, arvon syöttö tai siirtyminen) ja käyttäjän toimintoon liittyvät tiedot (kuten syöttötietojen arvon ja tyypin, lomakkeen kontekstin tai tietueen kontekstin). Tehtävien tallennustoiminto säilyttää niin paljon tietoja, että niiden avulla voidaan varmistaa tallenteen toisto juuri niin kuin käyttäjä toiminnon suorittanut tallennuksen hetkellä. (Toistotoimintoa ei ole vielä otettu käyttöön Retail Modern POS -sovelluksessa ja pilvimyyntipisteessä.)

## Peruskonfigurointi
<a id="basic-configuration" class="xliff"></a>
Voit ottaa tehtävätallenteen käyttöön myyntipisteessä seuraavasti.

1.  Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Kassakoneet**.
2.  Valitse kassakone, jolle haluat ottaa tehtävätallenteen käyttöön.
3.  Valitse **Kassakone**-välilehden **Yleinen**-pikavälilehden **Ota tehtävän tallennus käyttöön** -vaihtoehdon arvoksi **Kyllä**.
4.  Valitse **Tallenna**.
5.  Siirry kohtaan **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulu**.
6.  Valitse **Kassakoneet (1090)** -työ ja valitse sitten **Suorita nyt**.

## Tallenteen luominen
<a id="create-a-recording" class="xliff"></a>
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

## Latausvalinnat
<a id="download-options" class="xliff"></a>
Tallennusistunnon loputtua näkyvissä on useita vaihtoehtoja, joiden avulla tallenteen voi ladata. 
[![Latausvalinnat](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### Tallenna tälle tietokoneelle
<a id="save-to-this-pc" class="xliff"></a>

Tallennepaketin avulla voi toistaa tehtäväoppaan, ylläpitää tallennetta ja muokata tallenteen huomautuksia. (Tätä toimintoa ei ole vielä otettu käyttöön Retail Modern POS -sovelluksessa ja pilvimyyntipisteessä.)

### Vie Word-tiedostona
<a id="export-as-word-document" class="xliff"></a>

Tallenteen voi tallentaa Microsoft Word -asiakirjana. Asiakirja sisältää tallennetut vaiheet ja näyttökuvat.

### Tallenna kehittäjien tallenteena
<a id="save-as-developer-recording" class="xliff"></a>

Kehittäjät voivat käyttää käsittelemätöntä tallennetiedostoa moniin tarkoituksiin, esimerkiksi testikoodin muodostamiseen. (Tätä toimintoa ei ole vielä otettu käyttöön.)

## Tallennuksen säätimet
<a id="recording-controls" class="xliff"></a>
### [![Tallennuksen säätimet](./media/controls.jpg)](./media/controls.jpg)
<a id="recording-controlsmediacontrolsjpgmediacontrolsjpg" class="xliff"></a>

### P&ysäytä
<a id="stop" class="xliff"></a>

Valitse **Lopeta**, kun haluat lopettaa tallennusistunnon. Huomaa, että lopettamisen jälkeen et voi käynnistää istuntoa uudelleen. Tämän vuoksi kannattaa varmistaa, että tallenne on valmis, ennen kuin se lopetetaan.

### Keskeytä
<a id="pause" class="xliff"></a>

Valitse **Keskeytä**, kun haluat pysäyttää tallennusistunnon väliaikaisesti ja jatkaa toimintoa. **Keskeytä**-painikkeen valinnan jälkeen suoritettuja vaiheita ei tallenneta.

### Jatka
<a id="continue" class="xliff"></a>

Voit jatkaa tallennusistuntoa keskeytyksen jälkeen, kun valitset **Jatka**.

### Tallenna näyttökuvia
<a id="capture-screenshots" class="xliff"></a>

Tehtävien tallennustoiminto voi tallentaa Retail Modern POS -käyttöliittymän näyttökuvia liiketoimintaprosessin tallennuksen aikana. Tehtävien tallennustoiminto käyttää näyttökuvia, kun lataat tallenteen Word-asiakirjana. Voit ottaa näyttökuvatoiminnon käyttöön määrittämällä **Tallenna näyttökuvia** -vaihtoehdon arvoksi **Kyllä**. 

#### Seteli
<a id="note" class="xliff"></a>
> Näyttökuvien tallennustoimintoa ei tueta pilvimyyntipisteessä.

### Tehtävän aloittaminen ja lopettaminen
<a id="start-task-and-end-task" class="xliff"></a>

Voit määrittää ryhmiteltyjen vaiheiden joukon aloituksen ja lopetuksen **Aloita tehtävä**- ja **Lopeta** **tehtävä** -painikkeen avulla. Lisää Aloita tehtävä -vaihe valitsemalla **Aloita tehtävä**. Suorita sitten vaiheet, jotka lisätään ryhmään. Kun ryhmän vaiheet on suoritettu, valitse **Lopeta tehtävä**. Tehtävien avulla menettelyiden järjestäminen on helpompaa. Tehtävät voivat olla sisäkkäisiä muiden tehtävien kanssa. Näin myös pitkien ja monimutkaisten liiketoimintaprosessien järjestäminen onnistuu paremmin.

## Huomautusten lisääminen
<a id="adding-annotations" class="xliff"></a>
Huomautus on lisäteksti, joka lisätään vaiheeseen tallennuksen aikana. Huomautusten avulla voidaan esimerkiksi antaa käyttäjille lisätietoja tai ohjeita. Huomautuksia voi lisätä vaiheen edelle ja sen jälkeen. Huomautuksia voi lisätä mihin tahansa vaiheeseen **Muokkaa**-painikkeen avulla (kynäsymboli), joka löytyy vaiheen oikealta puolelta. 

[![Vaiheen Muokkaa-painike](./media/annotate.jpg)](./media/annotate.jpg)

### Tekstit ja muistiinpanot
<a id="texts-and-notes" class="xliff"></a>

**Tekstit**- ja **Muistiinpanot**-kenttien avulla voi lisätä tekstiä, jotka liitetään tehtäväoppaan vaiheeseen.
[![Teksti- ja Muistiinpanot-kenttä](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### Teksti
<a id="text" class="xliff"></a>

**Teksti**-kenttään syötetty kenttä näkyy tehtäväoppaan vaiheen tekstin *yläpuolella*. Tämä sijainti on sopiva tekstille, joka on tarkoitettu käyttäjän luettavaksi ennen vaiheen suoritusta.

#### Muistiinpanot
<a id="notes" class="xliff"></a>

**Muistiinpanot**-kenttään syötetty kenttä näkyy tehtäväoppaan vaiheen tekstin *alapuolella*. Käyttäjän on laajennettava vaiheen teksti ponnahdusikkunassa, jotta sen voi lukea. Tämä sijainti on sopiva valinnaisesti luettavalle materiaalille tai muille tiedoille, jotka voivat olla hyödyllisiä, mutta joita ei vaadita toiminnon suorittamista varten.

## Retail Modern POS -sovelluksen ja pilvimyyntipisteen ohje
<a id="help-in-retail-modern-pos-and-cloud-pos" class="xliff"></a>
Voit näyttää omat mukautetut tehtävätallenteet Retail Modern POS -sovelluksen ja pilvimyyntipisteen ohjeruudussa niin, että niitä voidaan tarkastella tekstinä, kun tallennat tehtävätallenteet ensin omaan BPM-kirjastoon ja päivität sitten ohjejärjestelmän parametrit niin, että ne osoittavat BPM-kirjastoon. Lisätietoja on kohdassa [Yhteyden muodostaminen ohjejärjestelmään.](/dynamics365/unified-operations/dev-itpro/get-started/help-connect). Retail Modern POS -sovelluksen ja pilvimyyntipisteen ohje tekee haut LCS-palvelusta reaaliaikaisesti. Se tekee haun kaikista BPM-kirjastoista, jotka on valittu Microsoft Dynamics 365 for Retailin ohjejärjestelmän parametreissa, ja näyttää hakua vastaavat tulokset. Voit käyttää **Ohje**-valikkoa valitsemalla näytön yläosassa olevan **Ohje**-painikkeen (kysymysmerkki) kirjoittamalla hakuruutuun prosessin nimen ja painamalla hakupainiketta. 

[![Ohje-painike](./media/help.jpg)](./media/help.jpg) 

Kun valitset hakutuloksista tehtäväoppaan, voit tarkastella vaiheita ohjeaiheena tai viedä ne Word-asiakirjaan. 
#### Seteli
<a id="note" class="xliff"></a>
> Retail Modern POS -sovelluksen ja pilvimyyntipisteen ohje ei anna tehtäväohjeita sen mukaan, mikä lomake tai tehtävä on käsiteltävänä. Kirjoita hakukenttään prosessin nimi ja valitse sitten on **Haku**.


