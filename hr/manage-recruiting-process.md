---
title: "Työhönottoprosessin hallinta"
description: "Tässä artikkelissa esitellään konsepti, jonka avulla työhönottajat voivat seurata työhönottoprosessin vaiheita, mukaan lukien avoimia toimien ilmoittaminen ja hakijoiden työhönotto, hakijoiden ja hakemusten tietojen seuranta, hakijoiden haastattelu ja yhden tai useamman ehdokkaan valinta organisaatiossasi avoinna oleviin toimiin."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: 551e15ed31953d6e5fc99a1177c1310194ea95d0
ms.lasthandoff: 03/31/2017


---

# <a name="manage-a-recruiting-process"></a>Työhönottoprosessin hallinta

Tässä aiheessa kuvataan käsite, rekrytoijille avulla voit seurata ohjeita työhönoton prosessi, mainostaa avoimia toimia ja rekrytoidaan hakijoiden pyrittävä etsimään hakijalle ja hakemuksen tietoja interviewing hakijoiden ja valitsemalla yksi tai useampi ehdokkaita täyttämään avoimia työpaikkoja yrityksessäsi.

<a name="overview"></a>Yleiskuvaus
--------

Työhönottoprojektien avulla voit järjestää yrityksen avoimiin toimiin tarvittavat työhönoton vaiheet. Hakija on henkilö, joka koskee työllisyyden yrityksen.  Hakemus on sellaisen yrityksen palveluksessa etua hakijan ja voi liittää työhönottoprojektin nimenomaisesti tiettyjä avattaessa etua.  Yksittäisen hakijan voi olla useita sovelluksia samalle oikeushenkilölle tai eri yritysten organisaatiossa.

<a name="recruitment-projects"></a>Työhönottoprojektit
--------------------

Työhönottoprojektien avulla rekrytoijille, voit seurata edistymistä täyttää avoimia toimia vastaan.  Työhönottoprojektin tunnistaa osasto ja työn, jotka ovat avoimia toimia. Työhönottoprojektit seuraavat lisäksi seuraavia tietoja avoimista toimista:
-   Avoimien toimien määrä
-   Työhön ottava esimies ja vaihtoehtoinen yhteyshenkilö toimelle
-   Päivämäärä, jolloin ehdotus hyväksyttiin
-   Hakemuksen viimeinen jättöpäivä
-   Arvioitu alkamispäivämäärä

Työhönottoprojekti sisältää **työpaikkailmoituksen**, jota käytetään **työntekijän itsepalveluosiossa** avoimen työpaikan ilmoituksena. Näyttääksesi avoimen toimen työntekijöille, työhönottoprojektilla on oltava **työpaikkailmoitus**, sen **Näytä työntekijän itsepalvelussa** -kentän valinta on oltava Kyllä, **hakemuksen viimeisen jättöpäivän** tulee olla tulevaisuudessa, ja työhönottoprojektin **tilana** on oltava Aloitettu. Seuraavassa taulukossa on lueteltu mahdollinen rekrytointi projektin tilat ja niiden kuvaukset.

| **Status**    | **Indicates that…**                                                                  |
|-----------|------------------------------------------------------------------------------------------|
| Ajastettu | Työhönoton pyrkimyksiä valmistetaan.  Työhönotosta vastaavan ei ole vielä alkanut tämän projektin. |
| Aloitettu   | Hakemuksia otetaan nyt vastaan projektin avoimille toimille.                    |
| Valmis  | Kaikki projektin toimet on täytetty.                                          |
| Peruutettu  | Projektin työhönotto on peruutettu.                                           |

Työhönottajat voivat myös tallentaa ulkoisissa työpaikkailmoituskanavissa käytettävän **median** sekä seurata projektin tai hakemusten **kehitystuloksia**.

<a name="applicants"></a>Hakijat
----------

Hakija on henkilö, joka koskee yrityksen projektille.  Hakijat jaetaan kaikkien oikeussubjektien välillä organisaatiossa, joka antaa suuren joukon etsiä kyvykkyys. Voit syöttää ja ylläpitää hakijoiden henkilökohtaisia tietoja, osaamisalueita ja erityisjärjestelyjä. Kun hakijatietue on luotu, hakijalle luodaan henkilötietue yleiseen osoitekirjaan. Voit käyttää **Hakija**-sivua päivittääksesi seuraavat tiedot hakijoista yleiseen osoitekirjaan:
-   Osoitetiedot
-   Yhteystiedot
-   Tunnistetiedot
-   Nimitiedot
-   Henkilökohtaiset tiedot

## <a name="applications"></a>Hakemukset
Vastaanotettujen työhakemusten tietoja voi taltioida **Hakemus**-sivulle. Sovellus on hakijan etua avaamisen organisaation työ.  Jos haluat luoda sovelluksen, hakijan tulee olla hakija tai henkilö järjestelmään.
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

**Hakemuksen** vastaustoimenpide määrittää asiakirjan tai sähköpostiviestin mallin, jota käytetään viestinnässä hakemuksen lähettäneen henkilön kanssa. Voit liittää **hakemuksen kirjanmerkit** kanssa, jotta voit käyttää arvoja sovelluksesta vastaustoimenpidettä hakijan haastattelu ja rekrytointi-projektin sivut viestintää hakijoiden kanssa.  **Sähköpostimallit** voi luoda nopeasti lähettää sähköpostia hakijoita, joilla on sovelluksen käyttäen tiettyjä tila ja kirjeenvaihto toiminto vastaustoimenpidettä. Esimerkiksi kaikkien sovellusten kanssa voi lähettää vahvistuksen sähköpostitse **tila** on vastaanotettu ja **vastaavuus-toiminto** on vastaanotettu.  Sähköpostin lähettämisen jälkeen voit halutessasi päivittää automaattisesti sovellusten tilan.

## <a name="application-routing"></a>Hakemusten reititys

Jos useiden työntekijöiden täytyy tarkistaa hakemus, voit hallita tätä prosessia luomalla kiertolistan **Hakemusten reititys** -sivulla.

## <a name="interviews"></a>Haastattelut

**Hakijoiden haastattelut** on ajoitettu **sovelluksia** sivulla.  Käytä **lähettää kokouksen tietoja** painike lähettää hakijalle ja Haastattelijan kalenteritiedosto, joka haastattelun tietoja.

## <a name="skill-mapping"></a>Osaamisaluekartoitus

**Osaamisaluekartoitusta** ja **osaamisaluekartoituksen profiileja** voidaan käyttää tunnistamaan hakijat, jotka ovat mahdollisesti päteviä toimeen.

## <a name="hiring-applicants"></a>Hakijoiden ottaminen palvelukseen

Käytä **Hakemukset**-sivua ottaaksesi hakija palvelukseen. Kun hakija palkataan, hakemustietueen tilaksi merkitään **Palkattu** ja hakijan yleisessä osoitekirjassa olevat tiedot liitetään uuteen työntekijätietueeseen. Yleiseen osoitekirjan tietoihin tehdyt muutokset uuden työntekijätietueen kautta näkyvät myös hakijatietueessa. Tämä vähentää tietojen syöttäminen Jos uusi työntekijä soveltaa joskus johonkin muuhun työtehtävään yrityksen sisällä.  Valitsemalla aiemmin luodun työntekijän palkkaa uusi paikalleen, **vaihtaa paikkaa** - **hakemuksen tila** pudota alas initiate siirtoprosessi.




