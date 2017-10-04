---
title: "Report Designer -ohjelman käyttöliittymä"
description: "Tässä artikkelissa käsitellään Report Designerissa liikkumista ja omia tarpeita vastaamien asetusten käyttämistä."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59041
ms.assetid: 054de5b0-8618-4195-be12-f031b4bb4d74
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: aad8f2617d94e9abc77dafe96cb95f7e191873bd
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="report-designer-interface"></a>Report Designer -ohjelman käyttöliittymä

[!include[banner](../includes/banner.md)]


Tässä artikkelissa käsitellään Report Designerissa liikkumista ja omia tarpeita vastaamien asetusten käyttämistä. 

<a name="report-designer-menu-commands"></a>Report Designer -ohjelman valikkokomennot
-----------------------------

Seuraavassa taulussa kuvataan talousraporttien suunnittelussa käytettävät valikkokomennot ja asetukset. Jotkin valikkokomennot ja asetukset ovat käytettävissä vain tietyissä tilanteissa. Esimerkiksi raportointiyksiköiden ylennysten ja alennusten komennot ovat käytettävissä vain, kun raportointipuun määritystä muokataan.

### <a name="file-menu"></a>Tiedosto-valikko

**Tiedosto**-valikko on kaikkien käyttäjien käytettävissä. Valikon komennot esitellään alla.

| Komento                           | Kuvaus                                                                                                                                                                                      |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Uusi                               | Luo uusi raportin, rivin, sarakkeen, raportointipuun tai raporttiryhmän määritys tai kansio. Lisäasetuksia on käytettävissä käyttäjäroolin mukaan. |
| Avoin                              | Avaa aiemmin luotu rivin, sarakkeen, raportointipuun tai raportin määritys.                                                                                             |
| Sulje                             | Sulje nykyinen rakenneosa.                                                                                                                                                                |
| Sulje kaikki                         | Sulje kaikki rakenneosat.                                                                                                                                                                       |
| Tallenna                              | Tallenna nykyinen rivin, sarakkeen, raportointipuun tai raportin määritys.                                                                                             |
| Tallenna nimellä                           | Tallenna nykyinen rivin, sarakkeen, raportointipuun tai raportin määritys uudella nimellä.                                                                            |
| Ominaisuudet                        | Avaa **Ominaisuudet**-valintaikkuna, jossa voit muuttaa raportin nimen ja kuvauksen.                                                                                                   |
| Luo                          | Luo nykyinen raportti. Tämä komento on käytettävissä raportin määrityksestä.                                                                                                                 |
| Tarkastele raporttia                       | Avaa luodun raportin uusin versio Dynamics 365 for Finance and Operationsissa. Tämä komento on käytettävissä raportin määrityksestä, jos luotuna on vähintään yksi raportti.                                 |
| Viimeisimmät raporttien määritykset         | Näytä äskettäin luotujen tai muokattujen raporttien luettelo. Tämän jälkeen voit valita raportin luettelosta.                                                                                    |
| Viimeisimmät rivien määritykset            | Näytä äskettäin luotujen tai muokattujen rivien määritysten luettelo. Tämän jälkeen voit valita rivin määrityksen luettelosta.                                                                    |
| Viimeisimmät sarakkeiden määritykset         | Näytä äskettäin luotujen tai muokattujen sarakkeiden määritysten luettelo. Tämän jälkeen voit valita sarakkeen määrityksen luettelosta.                                                              |
| Viimeisimmät raportointipuiden määritykset | Näytä äskettäin luotujen tai muokattujen raportointipuiden määritysten luettelo. Tämän jälkeen voit valita raportointipuun määrityksen luettelosta.                                              |
| Lopeta                              | Lopeta Report Designer.                                                                                                                                                                            |

### <a name="edit-menu"></a>Muokkaa-valikko

**Muokkaa**-valikko on niiden käyttäjien käytettävissä, joilla on **suunnittelijan** tai **järjestelmänvalvojan** rooli. Tämä valikko sisältää alla esiteltävät komennot.

| Komento                                | Kuvaus                                                                                                                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kumoa                                   | Kumoa viimeisin toiminto.                                                                                                                                                                                              |
| Tee uudelleen                                   | Palauta viimeisin peruutustoiminto.                                                                                                                                                                                      |
| Leikkaa                                    | Poista valittu teksti ja kopioi se leikepöydälle.                                                                                                                                                            |
| Kopioi                                   | Kopioi valittu teksti leikepöydälle.                                                                                                                                                                           |
| Liitä                                  | Lisää viimeisin leikattu tai kopioitu teksti leikepöydältä.                                                                                                                                                    |
| Tyhjennä                                  | Poista valitun rakenneosan solun sisältö.                                                                                                                                                           |
| Etsi                                   | Avaa **Etsi ja korvaa** -valintaikkuna, jossa voit hakea tekstiä näkymäruudussa.                                                                                                                              |
| Korvaa                                | Avaa **Etsi ja korvaa** -valintaikkuna, jossa voit hakea ja korvata tekstiä näkymäruudussa.                                                                                                                  |
| Lisää rivejä dimensioista            | Avaa **Lisää rivejä dimensioista** -valintaikkuna, jossa voi valita rivin määritykseen sisällytettäviä dimensioarvoja. Tämä komento on käytettävissä rivin määrityksestä.                                  |
| Numeroi rivit uudelleen                          | Numeroi kaikki numeeriset rivien koodit uudelleen. Tämä komento on käytettävissä rivin määrityksestä.                                                                                                                                   |
| Rivien linkit                              | Avaa **Rivien linkit** -valintaikkuna, jossa voi määrittää rivien ja raportointipuiden määritysten tietolinkkien lähteet. Tämä komento on käytettävissä rivin määrityksestä.                            |
| Pyöristyksen oikaisu                    | Avaa **Pyöristysten oikaisut** -valintaikkuna, jossa voi määrittää pyöristyksen parametrit. Tämä komento on käytettävissä rivin määrityksestä.                                                                  |
| Hallitse dimensioyhdistelmiä                  | Avaa **Dimensioyhdistelmät**-valintaikkuna, jossa voi luoda ja muokata dimensiojoukkoja. Tämä komento on käytettävissä rivin tai raportointipuun määrityksestä.                                              |
| Lisää rivi                             | Lisää tyhjä rivi rivin määritykseen tai tyhjään otsikkoriviin sarakkeen määrityksestä. Tämä komento on käytettävissä rivin tai sarakkeen määrityksestä.                                               |
| Poista rivi                             | Poista valittu rivi rivin määrityksestä tai valitusta otsikkorivistä sarakkeen määrityksessä. Tämä komento on käytettävissä rivin tai sarakkeen määrityksestä.                                       |
| Lisää sarake                          | Lisää tyhjä sarake sarakkeen määritykseen. Tämä komento on käytettävissä sarakkeen määrityksestä.                                                                                                             |
| Poista sarake                          | Poista valittu sarake sarakkeen määrityksestä. Tämä komento on käytettävissä sarakkeen määrityksestä.                                                                                                         |
| Lisää raportointiyksiköitä dimensioista | Avaa **Lisää raportointiyksiköitä dimensioista** -valintaikkuna, jossa voi valita raportointipuun määritykseen sisällytettäviä dimensioarvoja. Tämä komento on käytettävissä raportointipuun määrityksestä. |
| Tuo dimensioyhdistelmän hierarkia         | Avaa **Dimensioyhdistelmän hierarkia** -valintaikkuna, jossa voit tuoda dimensioyhdistelmän hierarkian taloushallinnon tiedoista. Tämä komento on käytettävissä järjestelmässä raportointipuun määrityksestä ..\financial-dimensions\dimension-based.  |
| Lisää raportointiyksikkö                  | Lisää tyhjä rivi raportointipuun määritykseen. Tämä komento on käytettävissä raportointipuun määrityksestä.                                                                                                |
| Poista raportointiyksikkö                  | Poista valittu raportointiyksikön rivi raportointipuun määrityksestä. Tämä komento on käytettävissä raportointipuun määrityksestä.                                                                             |

### <a name="view-menu"></a>Näytä-valikko

**Näytä**-valikko on kaikkien käyttäjien käytettävissä. Valikon komennot esitellään alla.

| Komento         | Kuvaus                                                            |
|-----------------|------------------------------------------------------------------------|
| Siirtymisruutu | Näytä tai piilota siirtymisruutu.                                      |
| Työkalurivit        | Valitse näkyvissä olevat työkalurivit.                                  |
| Tilarivi      | Näytä tai piilota **Report Designer** -ikkunan tilatiedot. |
| Tervetulo-sivu    | Avaa **Tervetuloa**-sivu.                                             |

### <a name="format-menu"></a>Muotoilu-valikko

**Muotoilu**-valikko on niiden käyttäjien käytettävissä, joilla on **suunnittelijan** tai **järjestelmänvalvojan** rooli. Tämä valikko sisältää alla esiteltävät komennot.

| Komento               | Kuvaus                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tyylit ja muotoilu | Avaa **Tyyli ja muotoilu** -valintaikkuna, jossa voi luoda ja muokata rivien ja sarakkeiden määritysten tekstin tyyliä. Tämä komento on käytettävissä rivin tai sarakkeen määrityksestä. |
| Sarakkeen leveys          | Avaa **Sarakkeen leveys** -valintaikkuna, jossa voi määrittää valitun sarakkeen leveyden. Tämä komento on käytettävissä rivin, sarakkeen tai raportointipuun määrityksestä.                      |
| Piilota                  | Piilota valittu sarake. Tämä komento on käytettävissä rivin, sarakkeen tai raportointipuun määrityksestä.                                                                                        |
| Tuo esiin                | Tuo esiin valittujen sarakkeiden välissä olevat piilotetut sarakkeet. Tämä komento on käytettävissä rivin, sarakkeen tai raportointipuun määrityksestä.                                                      |

### <a name="company-menu"></a>Yritys-valikko

**Yritys**-valikko on niiden käyttäjien käytettävissä, joilla on **suunnittelijan** tai **järjestelmänvalvojan** rooli. Tämä valikko sisältää alla esiteltävät komennot.

| Komento               | Kuvaus                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Yritykset             | Avaa **Yritykset**-valintaikkuna, jossa voi luoda ja muokata yrityksiä.                                          |
| Rakenneosaryhmät | Avaa **Rakenneosaryhmät**-valintaikkuna, jossa voi luoda, muokata, tuoda ja viedä rakenneosaryhmiä. |

### <a name="go-menu"></a>Siirry-valikko

**Siirry**-valikko on kaikkien käyttäjien käytettävissä. Valikon komennot esitellään alla. **Huomautus:** Näiden komentojen vaikutus ei ole näkyvä, jos siirtymisruutu ei ole näkyvissä.

| Komennot                   | Kuvaus                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| Raporttien määritykset         | Näytä raporttien määritykset siirtymisruudussa.                                    |
| Rivien määritykset            | Näytä rivien määritykset siirtymisruudussa.                                       |
| Sarakkeiden määritykset         | Näytä sarakkeiden määritykset siirtymisruudussa.                                    |
| Raportointipuiden määritykset | Näytä raportointipuiden määritykset siirtymisruudussa.                            |
| Suojaus                   | Näyttää käyttäjien, ryhmien ja yritysten suojaustiedot siirtymisruudussa. |

### <a name="tools-menu"></a>Työkalut-valikko

**Työkalut**-valikko on kaikkien käyttäjien käytettävissä, mutta joidenkin komentojen käytettävyyttä on rajoitettu. Tämä valikko sisältää alla esiteltävät komennot.

| Komento                       | Kuvaus                                                                                                                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Suojaa                       | Käytä valittuna olevassa rakenneosassa salasanaa. Tämä komento on **suunnittelijan** tai **järjestelmänvalvojan** roolin omaavien käyttäjien käytettävissä.                                                                           |
| Raportin jonon tila           | Avaa **Raportin jonon tila** -valintaikkuna, jossa näkyvät kaikki uusimmat luodut raportit ja kunkin raportin tiedot.                                                                                    |
| Lähdejärjestelmän tiedot     | Näytä Microsoft Dynamics ERP -järjestelmän asetukset. Tämä komento on **suunnittelijan** tai **järjestelmänvalvojan** roolin omaavien käyttäjien käytettävissä.                                                                 |
| Uloskuitatut kohteet             | Näytä avoinna olevat rivien, sarakkeiden, raportointipuiden ja raporttien määritykset. Tämä komento on **suunnittelijan** tai **järjestelmänvalvojan** roolin omaavien käyttäjien käytettävissä. |
| Päivitä välimuistiin tallennetut taloushallinnon tiedot | Päivitä taloushallinnon dimensioiden sarakkeen tiedot.                                                                                                                                                               |
| Optiot                       | Avaa **Asetukset**-valintaikkuna, jossa voi muokata Report Designer -ohjelman käyttäjän asetuksia.                                                                                                                       |

### <a name="window-menu"></a>Ikkuna-valikko

**Ikkuna**-valikko on kaikkien käyttäjien käytettävissä. Valikon komennot esitellään alla.

| Komento              | Kuvaus                                                                                                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Järjestä vierekkäin    | Näytä kaikki avoimet ikkunat vierekkäin.                                                                                                                                                     |
| Järjestä allekkain      | Näytä kaikki avoimet ikkunat allekkain.                                                                                                                                               |
| Limittäin              | Asettele kaikki avoimet ikkunat niin, että kunkin ikkunan otsikkorivi on näkyvissä.                                                                                                                      |
| Lukitse vaakasuunnassa    | Lukitse valittu rivi niin, että rivi näkyy ikkunassa myös silloin, kun ikkunaa vieritetään. Tämä komento on **suunnittelijan** tai **järjestelmänvalvojan** roolin omaavien käyttäjien käytettävissä.       |
| Lukitse pystysuunnassa      | Lukitse valittu sarake niin, että sarake näkyy ikkunassa myös silloin, kun ikkunaa vieritetään. Tämä komento on **suunnittelijan** tai **järjestelmänvalvojan** roolin omaavien käyttäjien käytettävissä. |
| Avointen ikkunoiden luettelo | Näytä avointen ikkunoiden luettelo. Valitse näkyville tuotava ikkuna.                                                                                                               |

### <a name="help-menu"></a>Ohje-valikko

**Ohje**-valikko on kaikkien käyttäjien käytettävissä. Valikon komennot esitellään alla.

| Komento | kuvaus                                                  |
|---------|--------------------------------------------------------------|
| Ohje    | Avaa Dynamics 365 for Finance and Operationsin ohjeen talousraportoinnin aihesivu. |
|         |                                                              |

## <a name="report-designer-toolbar-buttons"></a>Report Designer -ohjelman työkalurivin painikkeet
Seuraavassa taulukossa esitellään raporttien suunnittelussa käytettävissä olevat työkalurivin painikkeet. Jotkin työkalurivin painikkeet ovat käytettävissä vain tietyissä tilanteissa. Esimerkiksi raportointiyksiköiden ylennysten ja alennusten painikkeet ovat käytettävissä vain, kun raportointipuun määritystä muokataan.

### <a name="standard-toolbar"></a>Vakiotyökalurivi

Vakiotyökalurivi mahdollistaa tiedostojen ja muokkauskomentojen nopean käyttämisen. Tämä työkalurivi sisältää seuraavat painikkeet.

| Painike                                                                                                                                                                                   | Kuvaus                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![Uusi painike](./media/rowc130389.png)](./media/rowc130389.png)                              | Luo uusi (tyhjä) raportin, rivin, sarakkeen tai raportointipuun määritys.                                                                               |
| [![Avaa-painike](./media/openfolderc130389.png)](./media/openfolderc130389.png)               | Avaa aiemmin luotu rivin, sarakkeen, raportointipuun tai raportin määritys.                                                                                   |
| [![Tallenna-painike](./media/savec130389.png)](./media/savec130389.png)                           | Tallenna nykyinen rivin, sarakkeen, raportointipuun tai raportin määritys.                                                                                   |
| [![Kopioi-painike](./media/copyc130389.png)](./media/copyc130389.png)                           | Kopioi valittu teksti leikepöydälle.                                                                                                                                               |
| [![Leikkaa-painike](./media/cutc130389.png)](./media/cutc130389.png)                              | Poista valittu teksti ja kopioi se leikepöydälle.                                                                                                                                |
| [![Liitä-painike](./media/pastec130389.png)](./media/pastec130389.png)                        | Lisää teksti leikepöydältä.                                                                                                                                                    |
| [![Kumoa-painike](./media/undoc130389.png)](./media/undoc130389.png)                           | Kumoa viimeisin toiminto.                                                                                                                                                                  |
| [![Tee uudelleen -painike](./media/redoc130389.png)](./media/redoc130389.png)                           | Palauta viimeisin peruutustoiminto.                                                                                                                                                          |
| [![Etsi-painike](./media/findc130389.png)](./media/findc130389.png)                           | Avaa **Etsi ja korvaa** -valintaikkuna, jossa voit hakea ja korvata tekstiä aktiivisesta ikkunasta.                                                                                  |
| [![Lisää rivi -painike](./media/insertrowc130389.png)](./media/insertrowc130389.png)           | Lisää tyhjä rivi rivin määritykseen tai tyhjään otsikkoriviin sarakkeen määrityksestä. Tämä painike on käytettävissä rivin tai sarakkeen määrityksestä.                    |
| [![Lisää sarake -painike](./media/insertcolumnc130389.png)](./media/insertcolumnc130389.png)  | Lisää tyhjä sarake sarakkeen määritykseen. Tämä painike on käytettävissä sarakkeen määrityksestä.                                                                                  |
| [![Lukitse-painike](./media/lockc130389.png)](./media/lockc130389.png)                           | Käytä valittuna olevassa rakenneosassa salasanaa. Tämä painike on **suunnittelijan** tai **järjestelmänvalvojan** roolin omaavien käyttäjien käytettävissä.                                                 |
| [![Rivin linkki -painike](./media/rowlinkc130389.png)](./media/rowlinkc130389.png)                 | Avaa **Rivien linkit** -valintaikkuna, jossa voi määrittää rivien ja raportointipuiden määritysten tietolinkkien lähteet. Tämä painike on käytettävissä rivin määrityksestä. |
| [![Ylennä-painike](./media/promotec130389.png)](./media/promotec130389.png)                  | Ylennä raportointipuun määrityksen yksikkö. Kun valitset aliyksikön ja sen jälkeen **Ylennä**-painikkeen, aliyksikkö siirretään samalle tasolle kuin sen pääyksikkö.                |
| [![Alenna-painike](./media/demotec130389.png)](./media/demotec130389.png)                     | Alenna raportointipuun määrityksen yksikkö. Kun valitset yksikön ja sen jälkeen **Alenna**-painikkeen yksiköstä tulee sitä edeltävän yksikön aliyksikkö.                               |
| [![Laajenna-painike](./media/expandtreebuttonc130389.png)](./media/expandtreebuttonc130389.png) | Laajenna kaikki raportointipuun määrityksen yksiköt valitun yksikön tasolla.                                                                                                   |
| [![Tiivistä-painike](./media/collapsec130389.png)](./media/collapsec130389.png)               | Tiivistä raportointipuu.                                                                                                                                                           |
| [![Ohje-painike](./media/helpc130389.png)](./media/helpc130389.png)                           | Avaa Ohje.                                                                                                                                                                             |

### <a name="formatting-toolbar"></a>Muotoilutyökalurivi

Muotoilutyökalurivin avulla tyylikomennot on helppo ottaa käyttöön. Tämä työkalurivi sisältää seuraavat painikkeet.

| Painike                                                                                                                                                                                                   | Kuvaus                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [![Fonttityyli-painike](./media/formattingc130389.png)](./media/formattingc130389.png)                         | Ota valittu fonttityyli käyttöön nykyisessä tekstissä.      |
| [![Fontti-painike](./media/fonttype.png)](./media/fonttype.png)                                                 | Määritä nykyinen teksti valitulla fontilla.              |
| [![Fonttikoko-painike](./media/fontsize.png)](./media/fontsize.png)                                            | Määritä nykyinen teksti valitulla fonttikoolla (pisteinä). |
| [![Lihavoi-painike](./media/boldc130389.png)](./media/boldc130389.png)                                           | Lihavoi nykyinen teksti.                             |
| [![Kursivoi-painike](./media/italicsc130389.png)](./media/italicsc130389.png)                                   | Kursivoi nykyinen teksti.                           |
| [![Alleviivaa-painike](./media/underlinec130389.png)](./media/underlinec130389.png)                            | Alleviivaa nykyinen teksti.                             |
| [![Pienennä sisennystä -painike](./media/outdentlsc130389.png)](./media/outdentlsc130389.png)                      | Pienennä nykyisen tekstin sisennystä.                |
| [![Suurenna sisennystä -painike](./media/indentlsc130389.png)](./media/indentlsc130389.png)                        | Suurenna nykyisen tekstin sisennystä.                |
| [![Taustaväri-painike](./media/fillbackgroundcolorc130389.png)](./media/fillbackgroundcolorc130389.png) | Muuta nykyisen solun taustaväriä.        |
| [![Fontin väri -painike](./media/fontcolorc130389.png)](./media/fontcolorc130389.png)                           | Muuta nykyisen tekstin väriä.                   |

### <a name="report-designer-toolbar"></a>Report Designer -työkalurivi

Reporter Designer -työkaluriviltä voi käyttää nopeasti Report Designerin siirtymiskomentoja. Tämä työkalurivi sisältää seuraavat painikkeet.

| Painike                                                                                                                                                                                          | Kuvaus                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![Raportin määritys -painike](./media/reportc130389.png)](./media/reportc130389.png)                 | Näytä **Ikkuna**-valikossa näkyvä raportin määritys.                                                                                                            |
| [![Rivin määritys -painike](./media/rowc130389.png)](./media/rowc130389.png)                          | Näyttää aktiivisen raportin määritykseen liitetyn rivin määrityksen.                                                                                                    |
| [![Sarakkeen määritys -painike](./media/columnc130389.png)](./media/columnc130389.png)                 | Näyttää aktiivisen raportin määritykseen liitetyn sarakkeen määrityksen.                                                                                                 |
| [![Raportointipuun määritys -painike](./media/treec130389.png)](./media/treec130389.png)             | Näyttää aktiivisen raportin määritykseen liitetyn raportointipuun määrityksen.                                                                                         |
| [![Report Viewer -painike](./media/reportviewerc130389.png)](./media/reportviewerc130389.png)         | Käynnistä Report Viewer ja näytä luodun raportin uusin versio. Tämä painike on käytettävissä raportin määrityksestä, jos luotuna on vähintään yksi raportti. |
| [![Luo raportti -painike](./media/generate-to-ddvc130389.png)](./media/generate-to-ddvc130389.png) | Luo raportin aktiivisen raportin määrityksestä. Tämä painike on käytettävissä raportin määrityksestä.                                                                      |



<a name="see-also"></a>Lisätietoja
--------

[Taloushallinnan raportointi](financial-reporting-intro.md)

[Raportin luominen](generate-financial-report.md)



