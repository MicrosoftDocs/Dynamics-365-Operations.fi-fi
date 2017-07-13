---
title: "Työhönottoprosessin hallinta"
description: "Tässä artikkelissa esitellään konsepti, jonka avulla työhönottajat voivat seurata työhönottoprosessin vaiheita, mukaan lukien avoimia toimien ilmoittaminen ja hakijoiden työhönotto, hakijoiden ja hakemusten tietojen seuranta, hakijoiden haastattelu ja yhden tai useamman ehdokkaan valinta organisaatiossasi avoinna oleviin toimiin."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 6276655f6e7d09f5bc8862ad456b834d8919e574
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Työhönottoprosessin hallinta
<a id="manage-a-recruiting-process" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Tässä artikkelissa esitellään konsepti, jonka avulla työhönottajat voivat seurata työhönottoprosessin vaiheita, mukaan lukien avoimia toimien ilmoittaminen ja hakijoiden työhönotto, hakijoiden ja hakemusten tietojen seuranta, hakijoiden haastattelu ja yhden tai useamman ehdokkaan valinta organisaatiossasi avoinna oleviin toimiin.

Yleiskuvaus
<a id="overview" class="xliff"></a>
--------

Työhönottoprojektien avulla voit järjestää yrityksen avoimiin toimiin tarvittavat työhönoton vaiheet. Hakija on henkilö, joka hakee töihin yritykseesi.  Hakemus on hakijan osoitus mielenkiinnosta yritykseesi, ja voi olla sidottu työhönottoprojektiin, osoittaen mielenkiinnon tiettyyn toimeen.  Yksittäisellä hakijalla voi olla useita avoimia hakemuksia samaan yritykseen tai useampaan organisaatiosi yhtiöön.

Työhönottoprojektit
<a id="recruitment-projects" class="xliff"></a>
--------------------

Työhönottoprojektien avulla työhönottajat voivat seurata yhden tai useamman avoimen toimen täyttämisen etenemistä.  Työhönottoprojektissa tunnistetaan osasto ja työ, jossa on avoinna yksi tai useampi toimi. Työhönottoprojektit seuraavat lisäksi seuraavia tietoja avoimista toimista:
-   Avoimien toimien määrä
-   Työhön ottava esimies ja vaihtoehtoinen yhteyshenkilö toimelle
-   Päivämäärä, jolloin ehdotus hyväksyttiin
-   Hakemuksen viimeinen jättöpäivä
-   Arvioitu alkamispäivämäärä

Työhönottoprojekti sisältää **työpaikkailmoituksen**, jota käytetään **työntekijän itsepalveluosiossa** avoimen työpaikan ilmoituksena. Näyttääksesi avoimen toimen työntekijöille, työhönottoprojektilla on oltava **työpaikkailmoitus**, sen **Näytä työntekijän itsepalvelussa** -kentän valinta on oltava Kyllä, **hakemuksen viimeisen jättöpäivän** tulee olla tulevaisuudessa, ja työhönottoprojektin **tilana** on oltava Aloitettu. Seuraavassa taulukossa luetellaan mahdolliset työhönottoprojektin tilat ja niiden kuvaukset.

| **Tila**    | **Merkitsee, että...**                                                                  |
|-----------|------------------------------------------------------------------------------------------|
| Ajastettu | Työhönottotoimia valmistellaan.  Projektin työhönotto ei ole vielä alkanut. |
| Aloitettu   | Hakemuksia otetaan nyt vastaan projektin avoimille toimille.                    |
| Valmis  | Kaikki projektin toimet on täytetty.                                          |
| Peruutettu  | Projektin työhönotto on peruutettu.                                           |

Työhönottajat voivat myös tallentaa ulkoisissa työpaikkailmoituskanavissa käytettävän **median** sekä seurata projektin tai hakemusten **kehitystuloksia**.

Hakijat
<a id="applicants" class="xliff"></a>
----------

Hakija on henkilö, joka hakee töihin yritykseesi.  Hakijat jaetaan kaikkien organisaatiosi yritysten kesken, joten käytettävissä oleva osaajajoukko on suuri. Voit syöttää ja ylläpitää hakijoiden henkilökohtaisia tietoja, osaamisalueita ja erityisjärjestelyjä. Kun hakijatietue on luotu, hakijalle luodaan henkilötietue yleiseen osoitekirjaan. Voit käyttää **Hakija**-sivua päivittääksesi seuraavat tiedot hakijoista yleiseen osoitekirjaan:
-   Osoitetiedot
-   Yhteystiedot
-   Tunnistetiedot
-   Nimitiedot
-   Henkilökohtaiset tiedot

## Hakemukset
<a id="applications" class="xliff"></a>
Vastaanotettujen työhakemusten tietoja voi taltioida **Hakemus**-sivulle. Hakemus on hakijan osoitus mielenkiinnosta organisaatiossasi avoinna olevaa työtä kohtaan.  Luodakseen hakemuksen, hakija on rekisteröitävä hakijaksi tai henkilöksi järjestelmääsi.
Internetin välityksellä toimitetut sähköiset työhakemukset ovat joko ilmoituksiin perustuvia hakemuksia, jotka on lähetetty vastauksena työpaikkailmoitukseen, tai avoimia hakemuksia. Ilmoituksiin perustuvat hakemukset liitetään automaattisesti työhönottoprojektiin, josta ilmoitus on luotu. Avoimet hakemukset liitetään työhönottoprojektiin, joka on määritetty **Henkilöstöhallintoparametrit**-sivun **Työhönotto**-alueella.
### Hakemuksen tila
<a id="application-status" class="xliff"></a>

Hakemuksen tila ilmaisee, missä vaiheessa työhönottoprosessia hakemus on. Seuraavassa taulukossa luetellaan mahdolliset työhakemusten tilat ja niiden kuvaukset.

| Tila    | Merkitsee, että...                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| Vastaanotettu  | Hakemus on otettu vastaan.                                                             |
| Vahvistettu | Hakijalle voi lähettää vahvistuksen hakemuksen vastaanottamisesta.            |
| Haastattelu | Hakijalle voi lähettää kutsun haastatteluun.                                     |
| Hylkääminen | Hakijalle voi lähettää hylkäyskirjeen.                                          |
| Peruutettu  | Hakijalle voi lähettää peruuttamista koskevan vahvistuksen. Tämä tila määritetään manuaalisesti. |
| Toimessa  | Hakijalle voi lähettää työtarjouksen.                                         |

### Vastaustoimenpiteet
<a id="correspondence-actions" class="xliff"></a>

**Hakemuksen** vastaustoimenpide määrittää asiakirjan tai sähköpostiviestin mallin, jota käytetään viestinnässä hakemuksen lähettäneen henkilön kanssa. Voit liittää **hakemuksen kirjanmerkkejä** vastaustoimenpiteisiin käyttääksesi Hakemus-, Hakija-, Haastattelu- ja Työhönottoprojekti-sivujen arvoja viestinnässä hakijoiden kanssa.  Vastaustoimenpiteille voi luoda **sähköpostimalleja**, joiden avulla hakijoille, joiden hakemuksella on tietyn tilan ja vastaustoimenpiteen yhdistelmä, voi lähettää nopeasti sähköpostiviestejä. Voit esimerkiksi lähettää vahvistussähköpostin kaikille hakemuksille, joiden **tila** on Vastaanotettu ja **vastaustoimenpide** on Vastaanotettu.  Viestien lähettämisen jälkeen voit päivittää hakemusten tilan automaattisesti.

## Hakemusten reititys
<a id="application-routing" class="xliff"></a>

Jos useiden työntekijöiden täytyy tarkistaa hakemus, voit hallita tätä prosessia luomalla kiertolistan **Hakemusten reititys** -sivulla.

## Haastattelut
<a id="interviews" class="xliff"></a>

**Työhönottohaastattelut** voi ajoittaa **Hakemukset**-sivulta.  Käytä **Lähetä tapaamistiedot** -painiketta lähettääksesi haastatteluaikataulun kalenteritiedostona hakijalle ja haastattelijalle.

## Osaamisaluekartoitus
<a id="skill-mapping" class="xliff"></a>

**Osaamisaluekartoitusta** ja **osaamisaluekartoituksen profiileja** voidaan käyttää tunnistamaan hakijat, jotka ovat mahdollisesti päteviä toimeen.

## Hakijoiden ottaminen palvelukseen
<a id="hiring-applicants" class="xliff"></a>

Käytä **Hakemukset**-sivua ottaaksesi hakija palvelukseen. Kun hakija palkataan, hakemustietueen tilaksi merkitään **Palkattu** ja hakijan yleisessä osoitekirjassa olevat tiedot liitetään uuteen työntekijätietueeseen. Yleiseen osoitekirjan tietoihin tehdyt muutokset uuden työntekijätietueen kautta näkyvät myös hakijatietueessa. Tämä voi vähentää tietokirjausten määrää, jos uusi työntekijäsi hakee koskaan yrityksen sisällä uutta työtä.  Vanhan työntekijän palkkaamisen uuteen toimeen voit tehdä napsauttamalla **Hakemuksen tila** -valikosta **Muuta toimea**, joka aloittaa siirtoprosessin.






