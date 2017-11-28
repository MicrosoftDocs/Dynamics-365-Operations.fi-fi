---
title: "Tilaustenkäsittelyprosessin määrittäminen"
description: "Tämän ohjeaihe antaa tietoja siitä, kuinka puhelukeskusten tilauksia käsitellään Dynamics 365 for Retailin avulla."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 144bee2102b8d1901d1b4964f6c92501c1cd573d
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-order-processing-options"></a>Tilaustenkäsittelyasetusten määrittäminen

[!include[banner](includes/banner.md)]


Tämän ohjeaihe antaa tietoja siitä, kuinka puhelukeskusten tilauksia käsitellään Dynamics 365 for Retailin avulla. 

Retail tukee useita vähittäismyynnin kanavia, kuten verkkokauppoja, verkon kauppapaikkoja, perinteisiä liikkeitä ja puhelinmyyntiä. Puhelinpalvelukeskuksissa työntekijät ottavat vastaan asiakastilauksia puhelimitse ja luovat myyntitilauksia. Tässä ohjeaiheessa kuvataan, kuinka puhelinkeskus luodaan ja miten puhelinkeskuksen asetukset määritetään. Jokaisella puhelinkeskuksella voi olla omat käyttäjät, maksutavat, hintaryhmät, taloushallinnon dimensiot ja toimitustavat. Voit määrittää nämä asetukset puhelinkeskusta luotaessa. **Tärkeää:** Ennen kuin puhelukeskuksen työnkulkuja voidaan käyttää, kun käyttäjä luo myyntitilauksia, käyttäjän on oltava määritetty puhelukeskuksen käyttäjäksi. Voit ottaa käyttöön tai poistaa käytöstä vain puhelinpalvelukeskuksille ominaiset ryhmät tai toiminnot **Puhelukeskus**-sivulla. Seuraavat ominaisuusryhmät voidaan ottaa käyttöön:

-   **Tilauksen viimeistely** – Tämä ryhmä sisältää ominaisuuksia, jotka liittyvät maksuihin ja tilausten viimeistelyyn **Myyntitilaus**-sivulla.
-   **Ohjattu myynti** – Tämä ryhmä sisältää ominaisuuksia, jotka liittyvät lähdekoodeihin, komentosarjoihin ja luettelopyyntöihin.

Kun otat nämä toiminnot käyttöön puhelukeskuksen asetuksissa, ne ovat **Myyntitilaus**-sivulla puhelukeskukseen liittyvien käyttäjien käytettävissä. Useimmat näistä ominaisuuksista vaativat lisäasetuksia ennen käyttöä. Kuvat ja käsikirjoitukset ovat käytössä osana tietyn puhelukeskuksen ohjatun myynnin asetuksia. Jos nämä ominaisuudet ovat käytössä, käsikirjoitukset ja tuotekuvat näytetään **Myyntitilaus** -sivun tietoruudussa. Näyttöön tulee tuotteelle asetettu oletuskuva. Käsikirjoituksia voidaan määrittää nimikkeelle, luettelolle, asiakkaalle, tai nimikkeelle luettelokontekstissa. Puhelukeskustilauksilla voi näkyä lisätietoja siitä, miten määrätyn tilausrivin hinta on muotoutunut. Tilaukset näyttävät esimerkiksi, mitä alennuksia on sovellettu. Voit ottaa tämän toiminnon käyttöön kohdassa **Myyntireskontra** &gt; **Asetukset** &gt; **Myyntireskontran parametrit** &gt; **Hinnat** &gt; **Hintatiedot**. Pääset **Hintatiedot**-sivulle **Myyntitilausrivi**-avattavasta luettelosta. Voit käyttää tilaustapahtuman seurantaa tarkistaaksesi tilaukselle tilauksen elinkaaren aikana suoritetut toiminnot tai seurataksesi tietyn käyttäjän toimintoja. Voit esimerkiksi tallentaa toiminnon aina, kun käyttäjä luo myyntitilauksen, asettaa tilauksen pitoon, ohittaa veloituksen tai päivittää tilausrivin. Voit määrittää tilaustapahtumat seuraamaan tietyn käyttäjän, käyttäjäryhmän tai kaikkien käyttäjien toimenpiteitä tiettynä aikajaksona. Voit tarkastella asiakirjassa suoritettuja toimenpiteitä avaamalla **Tilaustapahtumat** -sivun kyseisen asiakirjan sivulla olevasta Toimintoruudusta. Voit määrittää tilaustapahtumia kohdassa **Myynti ja markkinointi** &gt; **Asetukset** &gt; **Tapahtumat** &gt; **Myyntitapahtumat**. Jos asiakkaan tilausta ei voida lähettää ajoissa, yritys voi lähettää asiakkaalle automaattisen ilmoituksen sähköpostitse, jossa kerrotaan tilauksen tila ja annetaan asiakkaalle mahdollisuus peruuttaa tilaus. Jos viive ylittää määritetyn raja-arvon, tilaus voidaan peruuttaa automaattisesti. Korkeintaan kolme sähköpostiviestiä voidaan lähettää määrättyjen aikavälien kuluttua:

1.  **Ensimmäisen peruutusilmoitus** – Asiakas voi peruuttaa tilauksen.
2.  **Toinen peruutusilmoitus** – Asiakas voi peruuttaa tilauksen.
3.  **Lopullinen peruutusilmoitus** – Järjestelmä peruuttaa tilauksen ja asiakkaalle ilmoitetaan peruutuksesta.

Voit vapauttaa yksittäiset asiakkaat ja tuotteet automaattisesta ilmoitus- ja peruutusprosessista. Marginaalihälytys laukeaa, kun lisään nimikkeen tilaukseen. Hälytys sisältää tärkeitä tietoja nimikkeestä, kuten hintamarginaalin ja nimikkeen kannattavuuden. Näiden tietojen avulla voit määrittää, onko hinnan ohitus oikea, kun lisäät nimikkeen myyntitilauksen. Voit esimerkiksi asettaa rajoja kauppojen katteelle määrittämään, että 40 prosenttia tai enemmän kustannukset ylittävä hinta on tuotteelle hyväksyttävä, mutta 20-39 prosentilla kustannukset ylittävä hinta on kyseenalainen. Tässä tapauksessa nimike, jolla on 20-39 prosentin raja, aiheuttaa varoituksen. Nimikettä, jolla on alle 20 prosenttia kustannukset ylittävä raja, ei voida myydä, ja nimikkeen hintaa ei voida muokata. Voit määrittää marginaalihälytyksiä kohdassa **Myyntireskontra** &gt; **Asetukset** &gt; **Myyntireskontran parametrit** &gt; **Marginaalihälytykset**. Kun määrität arvonlisäveronäärityksen oletussääntöjen perusteella, voit määrittää vastaavan prioriteetin osoite-elementeille. Voit esimerkiksi määrittää, että arvonlisäveroryhmän täsmäämisellä postinumeron mukaan on suurempi prioriteetti kuin arvonlisäveroryhmän täsmäämisellä osavaltion mukaan. Kun lisäät uusia asiakkaan osoitetietueita, arvonlisäveroryhmä määritetään automaattisesti sen mukaan, kuinka asiakkaan osoite vastaa määrittämiäsi oletussääntöjä ja prioriteettivastaavuutta. Voit määrittää tämän toiminnon **Kirjanpitoparametrit**-sivulla.




