---
title: Työhönottoprosessien hallinta
description: Tässä artikkelissa kuvataan käsite, jonka avulla rekrytoijat voivat seurata rekrytointiprosessin vaiheita.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: anbichse
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74ff8b081f5c82a089eef47b5cc18bc498a34c21
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752075"
---
# <a name="manage-recruiting-processes"></a>Työhönottoprosessien hallinta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa esitellään konsepti, jonka avulla työhönottajat voivat seurata työhönottoprosessin vaiheita, mukaan lukien avoimia toimien ilmoittaminen ja hakijoiden työhönotto, hakijoiden ja hakemusten tietojen seuranta, hakijoiden haastattelu ja yhden tai useamman ehdokkaan valinta organisaatiossasi avoinna oleviin toimiin.

## <a name="overview"></a>Yleiskuvaus

Työhönottoprojektien avulla voit järjestää yrityksen avoimiin toimiin tarvittavat työhönoton vaiheet. Hakija on henkilö, joka hakee töihin yritykseesi. Hakemus on hakijan osoitus mielenkiinnosta yritykseesi, ja voi olla sidottu työhönottoprojektiin, osoittaen mielenkiinnon tiettyyn toimeen. Yksittäisellä hakijalla voi olla useita avoimia hakemuksia samaan yritykseen tai useampaan organisaatiosi yhtiöön.

## <a name="recruitment-projects"></a>Työhönottoprojektit

Työhönottoprojektien avulla työhönottajat voivat seurata yhden tai useamman avoimen toimen täyttämisen etenemistä. Työhönottoprojektissa tunnistetaan osasto ja työ, jossa on avoinna yksi tai useampi toimi. Työhönottoprojektit seuraavat lisäksi seuraavia tietoja avoimista toimista:

- Avoimien toimien määrä
- Työhön ottava esimies ja vaihtoehtoinen yhteyshenkilö toimelle
- Päivämäärä, jolloin ehdotus hyväksyttiin
- Hakemuksen viimeinen jättöpäivä
- Arvioitu alkamispäivämäärä

Työhönottoprojekti sisältää **työpaikkailmoituksen**, jota käytetään **työntekijän itsepalveluosiossa** avoimen työpaikan ilmoituksena. Näyttääksesi avoimen toimen työntekijöille, työhönottoprojektilla on oltava **työpaikkailmoitus**, sen **Näytä työntekijän itsepalvelussa** -kentän valinta on oltava Kyllä, **hakemuksen viimeisen jättöpäivän** tulee olla tulevaisuudessa, ja työhönottoprojektin **tilana** on oltava Aloitettu. Seuraavassa taulukossa luetellaan mahdolliset työhönottoprojektin tilat ja niiden kuvaukset.

| Tila    | Merkitsee, että...                                                                         |
|-----------|-----------------------------------------------------------------------------------------|
| Ajastettu | Työhönottotoimia valmistellaan. Projektin työhönotto ei ole vielä alkanut. |
| Aloitettu   | Hakemuksia otetaan nyt vastaan projektin avoimille toimille.                   |
| Valmis  | Kaikki projektin toimet on täytetty.                                         |
| Peruutettu  | Projektin työhönotto on peruutettu.                                          |

Työhönottajat voivat myös tallentaa ulkoisissa työpaikkailmoituskanavissa käytettävän **median** sekä seurata projektin tai hakemusten **kehitystuloksia**.

## <a name="applicants"></a>Hakijat

Hakija on henkilö, joka hakee töihin yritykseesi. Hakijat jaetaan kaikkien organisaatiosi yritysten kesken, joten käytettävissä oleva osaajajoukko on suuri. Voit syöttää ja ylläpitää hakijoiden henkilökohtaisia tietoja, osaamisalueita ja erityisjärjestelyjä. Kun hakijatietue on luotu, hakijalle luodaan henkilötietue yleiseen osoitekirjaan. Voit käyttää **Hakija**-sivua päivittääksesi seuraavat tiedot hakijoista yleiseen osoitekirjaan:

- Osoitetiedot
- Yhteystiedot
- Tunnistetiedot
- Nimitiedot
- Henkilökohtaiset tiedot

## <a name="applications"></a>Hakemukset

Vastaanotettujen työhakemusten tietoja voi taltioida **Hakemus**-sivulle. Hakemus on hakijan osoitus mielenkiinnosta organisaatiossasi avoinna olevaa työtä kohtaan. Luodakseen hakemuksen, hakija on rekisteröitävä hakijaksi tai henkilöksi järjestelmääsi.

Internetin välityksellä toimitetut sähköiset työhakemukset ovat joko ilmoituksiin perustuvia hakemuksia, jotka on lähetetty vastauksena työpaikkailmoitukseen, tai avoimia hakemuksia. Ilmoituksiin perustuvat hakemukset liitetään automaattisesti työhönottoprojektiin, josta ilmoitus on luotu. Avoimet hakemukset liitetään työhönottoprojektiin, joka on määritetty **Henkilöstöhallintoparametrit**-sivun **Työhönotto**-alueella.

### <a name="application-status"></a>Hakemuksen tila

Hakemuksen tila ilmaisee, missä vaiheessa työhönottoprosessia hakemus on. Seuraavassa taulukossa luetellaan mahdolliset työhakemusten tilat ja niiden kuvaukset.

| Tila    | Merkitsee, että...                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| Vastaanotettu  | Hakemus on otettu vastaan.                                                             |
| Vahvistettu | Hakijalle voi lähettää vahvistuksen hakemuksen vastaanottamisesta.            |
| Haastattelu | Hakijalle voi lähettää kutsun haastatteluun.                                     |
| Hylkääminen | Hakijalle voi lähettää hylkäyskirjeen.                                          |
| Peruutettu  | Hakijalle voi lähettää peruuttamista koskevan vahvistuksen. Tämä tila määritetään manuaalisesti. |
| Toimessa  | Hakijalle voi lähettää työtarjouksen.                                         |

### <a name="correspondence-actions"></a>Vastaustoimenpiteet

**Hakemuksen** vastaustoimenpide määrittää asiakirjan tai sähköpostiviestin mallin, jota käytetään viestinnässä hakemuksen lähettäneen henkilön kanssa. Voit liittää **hakemuksen kirjanmerkkejä** vastaustoimenpiteisiin käyttääksesi Hakemus-, Hakija-, Haastattelu- ja Työhönottoprojekti-sivujen arvoja viestinnässä hakijoiden kanssa. Vastaustoimenpiteille voi luoda **sähköpostimalleja**, joiden avulla hakijoille, joiden hakemuksella on tietyn tilan ja vastaustoimenpiteen yhdistelmä, voi lähettää nopeasti sähköpostiviestejä. Voit esimerkiksi lähettää vahvistussähköpostin kaikille hakemuksille, joiden **tila** on Vastaanotettu ja **vastaustoimenpide** on Vastaanotettu. Viestien lähettämisen jälkeen voit päivittää hakemusten tilan automaattisesti.

## <a name="application-routing"></a>Hakemusten reititys

Jos useiden työntekijöiden täytyy tarkistaa hakemus, voit hallita tätä prosessia luomalla kiertolistan **Hakemusten reititys** -sivulla.

## <a name="interviews"></a>Haastattelut

**Työhönottohaastattelut** voi ajoittaa **Hakemukset**-sivulta. Käytä **Lähetä tapaamistiedot** -painiketta lähettääksesi haastatteluaikataulun kalenteritiedostona hakijalle ja haastattelijalle.

## <a name="skill-mapping"></a>Osaamisaluekartoitus

**Osaamisaluekartoitusta** ja **osaamisaluekartoituksen profiileja** voidaan käyttää tunnistamaan hakijat, jotka ovat mahdollisesti päteviä toimeen.

## <a name="hiring-applicants"></a>Hakijoiden ottaminen palvelukseen

Käytä **Hakemukset**-sivua ottaaksesi hakija palvelukseen. Kun hakija palkataan, hakemustietueen tilaksi merkitään **Palkattu** ja hakijan yleisessä osoitekirjassa olevat tiedot liitetään uuteen työntekijätietueeseen. Yleiseen osoitekirjan tietoihin tehdyt muutokset uuden työntekijätietueen kautta näkyvät myös hakijatietueessa. Tämä voi vähentää tietokirjausten määrää, jos uusi työntekijäsi hakee koskaan yrityksen sisällä uutta työtä. Vanhan työntekijän palkkaamisen uuteen toimeen voit tehdä napsauttamalla **Hakemuksen tila** -valikosta **Muuta toimea**, joka aloittaa siirtoprosessin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]