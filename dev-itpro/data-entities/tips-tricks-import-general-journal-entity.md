---
title: "Parhaat käytännöt tuodaan käyttämällä yleisen kirjauskansion tositteet"
description: "Tässä aiheessa vihjeitä tuoda tietoja yleisen päiväkirjan avulla yleinen kirjauskansio-kohteen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 81a52acd1d9baa12fcfe9d848441901894fa5682
ms.lasthandoff: 03/31/2017


---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>Parhaat käytännöt tuodaan käyttämällä yleisen kirjauskansion tositteet

Tässä aiheessa vihjeitä tuoda tietoja yleisen päiväkirjan avulla yleinen kirjauskansio-kohteen.  

Kirjauskansio-kohteen avulla voit tuoda tositteet, joiden tilinä vai vastatilinä tilityyppi on **pääkirjanpidon, asiakkaan, toimittajan tai pankin**. Tosite voidaan lisätä yhdelle riville sekä **tilin** kenttä ja **vastatili** kenttään, tai usean rivin tosite, jos vain **tilin** kenttää käytetään (ja **vastatili** on tyhjä rivin kunkin). Kirjauskansion kohde ei tue jokaisen tilin tyyppi. Sen sijaan on olemassa muita yksiköitä sellaisiin tilanteisiin, joissa on käytettävä tilityyppien yhdistelmiä. Käyttää esimerkiksi tuomaan projektitapahtuman projektin kulujen kirjauskansio kohteen. Kullakin entiteetillä on suunniteltu tukemaan tiettyjä tilanteita, mikä tarkoittaa Lisää kenttiä voi olla käytettävissä yksiköiden tapauksissa, mutta ei kohteita eri skenaarion.

## <a name="setup"></a>Luo perustiedot
Ennen kuin tuot kohteen yleisen päiväkirjan avulla, tarkista seuraavat asetukset:

-   **Erän kirjauskansion numeron numerosarjan asetukset** - kun tuot numerosarjasta, joka määritetään kirjanpidon parametrit käyttämällä yleinen päiväkirja-yksikön päiväkirjan erän numero käyttää oletusarvoisesti. Jos määrität kirjauskansion eränumeron numerosarjaksi **Manuaalinen**, oletusnumeroa ei käytetä. Tätä asetusta ei tueta.
-   **Taloushallinnon dimension konfiguraation** -jokaisen organisaation on määritettävä haluamasi järjestys taloushallinnon dimensioiden käytettäessä kohteet haluat tuoda tapahtumat. Tilaus on määritetty **kirjanpidon dimensiot integrointi** muodossa, osoitteessa **kirjanpidon**&gt;**tilikartan**&gt;**mitat**&gt;**sovellusten integrointi taloushallinnon dimension konfiguraatio**&gt;**Valitse entiteettien tietojen**. Tuodun kirjanpitotilin segmenttien on oltava samassa järjestyksessä. Muussa tapauksessa tapahtuu tuontivirhe.

## <a name="general-journal-entity-setup"></a>Kirjauskansioyksikön asetukset
Kaksi asetukset, tietojen hallinta vaikuttaa oletus-kirjauskansion eränumero tai tositteen numeron käyttäminen:

-   **Set-pohjaisen käsittelyn** (Valitse tiedot-kohde)
-   **Automaattisesti luotu** (-kentän yhdistäminen)

Seuraavissa osissa käsitellään näiden asetusten vaikutusta ja selvitetään, miten kirjauskansion eränumerot ja tositenumerot luodaan.

### <a name="journal-batch-number"></a>Kirjauskansion eränumero

-   Kirjauskansioyksikön **Joukkoon perustuva käsittely** -asetus ei vaikuta tapaan, jolla kirjauskansion eränumerot luodaan.
-   Jos **Kirjauskansion eränumero** -kentässä on valittu **Luotu automaattisesti**, jokaiselle tuodulle riville luodaan uusi kirjauskansion eränumero. Tämä menettelyä ei suositella. **Luotu automaattisesti** -asetus sijaitsee tuontiprojektin **Yhdistämistiedot**-välilehden kohdassa **Näytä yhdistämismääritykset**.
-   Jos **Kirjauskansion eränumero** -kentässä ei ole valittu **Luotu automaattisesti**, kirjauskansion eränumero luodaan seuraavasti:
    -   Jos olemassa, kirjaamaton kirjauskansio työvaiheiden Microsoft Dynamics-365-vastaa päiväkirjan erän numero, joka on määritetty tuodun tiedoston, kaikki rivit, joilla on vastaavia kirjauskansion eränumero tuoda olemassa olevaan kirjauskansioon. Rivejä ei koskaan tuoda kirjattuun kirjauskansion eränumeroon. Sen sijaan luodaan uusi numero.
    -   Jos päiväkirjan erän numero, joka on määritetty tuotavassa tiedostossa ei vastaa olemassa, kirjaamaton kirjauskansio työvaiheiden 365 Dynamics-, kaikki rivit, joilla on saman päiväkirjan erä on ryhmitelty uuteen kirjauskansioon. Esimerkiksi kaikki rivit, joiden kirjauskansion eränumero on 1, tuodaan uuteen kirjauskansioon, ja kaikki rivit, joiden kirjauskansion eränumero on 2, tuodaan toiseen uuteen kirjauskansioon. Kirjauskansion eränumero luodaan käyttämällä kirjanpidon parametreissa määritettyä numerosarjaa.

### <a name="voucher-number"></a>Tositenumero

-   Kun käytät kirjauskansioyksikössä **Joukkoon perustuva käsittely** -asetusta, tuodun tiedoston on annettava tositenumero. Jokaiselle kirjauskansion tapahtumalle määritetään tuodusta tiedostosta saatu tositenumero, vaikka tositetta ei olisi täsmäytetty. Jos haluat käyttää joukko tapahtuva käsittely, mutta myös käytettävä numerosarja on määritetty tosite numeroille Dynamics 365 operaatioille, korjaustiedosto on annettu helmikuu 2016 julkaistavaksi. Hotfix-korjauksen numero on 3170316, ja sen voi ladata Lifecycle Services (LCS) -palvelusta. Lisätietoja on artikkelissa [Hotfix-korjausten lataaminen Lifecycle Servicesistä](..\migration-upgrade\download-hotfix-lcs.md).
    -   Jos haluat ottaa käyttöön Kirjauskansionimi, jota käytetään tuonnin Dynamics 365 toimintoja, nämä toiminnot **numero kohdistus kirjauksen yhteydessä**, **Kyllä**.
    -   Tositenumero on määritettävä edelleen tuodussa tiedostossa. Kuitenkin tämä luku on väliaikainen ja korvaavat Dynamics-365 toimintojen tositenumeroa varten, kun kirjauskansio kirjataan. Varmista, että väliaikainen tositenumero ryhmittää kirjauskansion rivit oikein. Esimerkiksi kirjauksen aikana kolme riviä ehdoista, joilla väliaikainen tositenumero 1. Kaikki kolme riviä väliaikainen tositenumero korvataan seuraavan numeron numerosarjasta. Jos nämä kolme riviä eivät ole täsmätty vienti, tositetta ei kirjata. Jos seuraavaksi havaitaan rivejä, joiden väliaikainen tositenumero on 2, tämä numero korvataan seuraavalla numerosarjan tositenumerolla ja niin edelleen.

<!-- -->

-   Kun et käytä **joukko tapahtuva käsittely** määrittäminen, sinun ei tarvitse Anna tositenumero tuotavan tiedoston. Tositenumerot luodaan tuonnin aikana kirjauskansion asetusten mukaan (**Vain yksi tosite**, **Kun tosite täsmää**ja niin edelleen). Jos kirjauskansion asetukseksi on esimerkiksi määritetty **Kun tosite täsmää**, ensimmäinen rivi saa uuden oletusarvoisen tositenumeron. Järjestelmä sitten arvioi rivin ja määrittää, vastaavatko debet-arvot kredit-arvoja. Jos rivillä on vastatili, seuraava tuotavarivi saa uuden tositenumeron. Jos vastatiliä ei ole, järjestelmä arvioi, vastaavatko debet-arvot kredit-arvoja uutta riviä tuotaessa.
-   Jos **Tositenumero**-kentän arvoksi on valittu **Luotu automaattisesti**, tuonti epäonnistuu. **Tositenumero**-kentän **Luotu automaattisesti** -asetusta ei tueta.

Kirjauskansioyksikkö käyttää oletusarvoisesti joukkoon perustuvaa käsittelyä. Kun olet arvioinut organisaation liiketoimintatavoitteet, voit muuttaa **Joukkoon perustuva käsittely** -asetusta valitsemalla **Tietoyksiköt** **Tietojen hallinta** -työtilassa. Joukkoon perustuvaa käsittelyä käytetään nopeuttamaan tuontiprosessia. Jos et käytä joukkoon perustuvaa käsittelyä, kirjauskansioyksikköä käyttävä tuonti tapahtuu hitaammin.


