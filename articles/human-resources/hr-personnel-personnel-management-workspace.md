---
title: Henkilöstöhallinto-työtila
description: Tässä ohjeaiheessa kuvataan Henkilöstöhallinto-työtilan käsitteelliset elementit.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.search.scope: Human Resources
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7a83dea308e3e2eec1edebd5d619f9455e1a2268
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066572"
---
# <a name="personnel-management-workspace"></a>Henkilöstöhallinto-työtila


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Henkilöstöhallinto**-työtila sisältää valtavan määrän sisältöä. Se sisältää henkilöstön liikkeet, seuraa työntekijöiden muutoksia, avoimia toimia, osoitemuutoksia, vanhentuvia tietueita ja analyysejä sekä tarjoaa linkkejä tiettyihin tietoihin. Tässä ohjeaiheessa on yksityiskohtaisia tietoja työtilan kustakin osasta.

## <a name="activity-tab"></a>Tehtävä-välilehti

**Tehtävä**-välilehti sisältää osioita, jotka ryhmittelevät työntekijät sen perusteella, missä vaiheessa he ovat työhönottoprosessissa:

- **Palkattavat ehdokkaat**
- **Alkaa pian**
- **Äskettäin palkatut**
- **Lopettaa**
- **Lopettaneet**

Kun työntekijä on jossakin näissä vaiheissa, tietyt toiminnot ovat käytettävissä painikkeena kortissa tai valikossa, joka näytetään, kun valitset oikeasta yläkulmasta kolmen pisteen kuvakkeen (**...**). **Tehtävä**-välilehden osiot ja käytettävissä olevat toiminnot on kuvattu seuraavissa alaosioissa.

### <a name="candidates-to-hire"></a>Palkattavat ehdokkaat

Työtilan **Työhön otettavat hakijat** -osio täytetään useista lähteistä:

- Open Data Protocol (OData) -yksikkö
- LinkedIn-integrointi
- Tuotteeseen manuaalisesti syötetyt tiedot

Kun **Työhön otettavat hakijat** -osiossa näytetään hakijoita, voit suorittaa seuraavat toiminnot valitsemalla kolmen pisteen kuvakkeen ehdokaskortista:

- **Hylkää ehdokas**
- **Älä palkkaa**
- **Palkkaa**

> [!NOTE]
> Jos ehdokasluettelo täytetään Microsoft Dataversesta, kaikissa yrityksissä näytetään samat ehdokkaat, koska ehdokkaaseen ei ole liitetty yritystä.

### <a name="starting-soon"></a>Alkaa pian

**Aloittaa pian** -osiossa näytetään työntekijät, joiden alkamispäivä on tulevaisuudessa. Luettelo on järjestetty alkamispäivän mukaan. Tämänhetkistä päivämäärää lähin alkamisaika näytetään luettelossa ensimmäisenä.

Jos esimiestä ei näytetä kortissa, työntekijälle ei ole kohdistettu toimea.

> [!NOTE] 
> Toimi kannattaa määrittää työntekijälle, ennen tarkistusluettelon käyttämistä. Perehdytystehtäviä määritetään joskus juuri palkatun työntekijän esimiehelle. Jos toimea ei kuitenkaan ole kohdistettu, uuden työntekijän esimiestä ei voi määrittää. Tällöin esimiehelle tarkoitetut perehdytystehtävät kohdistetaan tarkistusluettelon omistajalle sen sijaan.

Kun **Aloittaa pian** -osiossa näytetään työntekijöitä, seuraavat toiminnot ovat heidän käytettävissään:

- Määritä toimi
- Tarkista työsuhde
- Määritä kiinteä kompensaatio
- Määritä muuttuva kompensaatio
- Näytä hierarkiassa
- Käytä tarkistusluetteloa\*\*

\*\* Tämä toiminto on oletustoiminto. Se näytetään kortissa painikkeena.

### <a name="recent-hires"></a>Äskettäin palkatut

**Viimeksi palkatut** -osiossa näytetään työntekijät, joiden alkamisaika on mennyt äskettäin. Luettelo on järjestetty alkamispäivän mukaan. Tämänhetkistä päivämäärää lähin alkamisaika näytetään luettelossa ensimmäisenä.

Luettelossa näytetään oletusarvoisesti työntekijät, jotka palkattiin edellisen seitsemän päivän aikana. Jos haluat muuttaa tätä asetusta, määritä **Viimeksi palkatut** -aikaväli **Henkilöstöhallinnon parametrit** -sivun **Yleiset**-välilehdestä. **Viimeksi palkatut** -osiossa olevat tiedot voidaan näyttää tietyltä päivien, kuukausien tai vuosien ajalta. Jos haluat esimerkiksi nähdä edellisen 14 päivän aikana palkattujen työntekijöiden luettelon, määritä **Kausi**-kentän arvoksi **14** ja **Yksikkö**-kentän arvoksi **Päivät**.

> [!NOTE]
> **Henkilöstöhallinnon parametrit** -sivulla olevat asetukset ovat yrityskohtaisia. Tästä johtuen aikaväli, jolta tarkastelet viimeksi palkattuja työntekijöitä, voi vaihdella yrityksittäin. Saatat esimerkiksi haluta nähdä kaikki USMF-yrityksen edellisen seitsemän päivän aikana palkkaamat työntekijät. Toisaalta saatat haluta nähdä kaikki USSI-yrityksen edellisen 14 päivän aikana palkkaamat työntekijät. Siinä tapauksessa avataan kunkin yrityksen **Henkilöstöhallinnan parametrit** -sivu ja määritetään tarvittavat parametrit.

Jos esimiestä ei näytetä kortissa, työntekijälle ei ole kohdistettu toimea.

Kun **Viimeksi palkatut** -osiossa näytetään työntekijöitä, seuraavat toiminnot ovat heidän käytettävissään:

- Määritä toimi
- Tarkista työsuhde
- Kiinteä kompensaatio
- Määritä muuttuva kompensaatio
- Näytä hierarkiassa
- Käytä tarkistusluetteloa\*\*

\*\* Tämä toiminto on oletustoiminto. Se näytetään kortissa painikkeena.

### <a name="exiting"></a>Lopettaa

**Lopettavat**-osiossa näytetään työntekijät, joiden työsuhteen loppumispäivä on tulevaisuudessa. Luettelo on järjestetty työsuhteen loppumispäivän mukaan. Tämänhetkistä päivämäärää lähin työsuhteen loppumispäivä näytetään luettelossa ensimmäisenä. 

Luettelossa näytetään oletusarvoisesti työntekijät, joiden työsuhteen loppumispäivä on seuraavan seitsemän päivän kuluessa. Jos haluat muuttaa tätä asetusta, määritä **Näytä lopettavat työntekijät** -aikaväli **Henkilöstöhallinnon parametrit** -sivun **Yleiset**-välilehdestä. **Lopettavat**-osiossa olevat tiedot voidaan näyttää tietyltä päivien, kuukausien tai vuosien ajalta. Jos haluat esimerkiksi nähdä seuraavan 14 päivän lopettavien työntekijöiden luettelon, määritä **Kausi**-kentän arvoksi **14** ja **Yksikkö**-kentän arvoksi **Päivät**.

Kun **Lopettavat**-osiossa näytetään työntekijöitä, seuraavat toiminnot ovat heidän käytettävissään:

- Käytä tarkistusluetteloa\*\*
- Tarkista työsuhde
- Näytä hierarkiassa

\*\* Tämä toiminto on oletustoiminto. Se näytetään kortissa painikkeena.

### <a name="exited"></a>Lopettaneet

**Lopettaneet**-osiossa näytetään työntekijät, joiden työsuhteen loppumispäivä on mennyt äskettäin. Luettelo on järjestetty työsuhteen loppumispäivän mukaan. Tämänhetkistä päivämäärää lähin työsuhteen loppumispäivä näytetään luettelossa ensimmäisenä.

Luettelossa näytetään oletusarvoisesti työntekijät, joiden työsuhde on päättynyt edellisen seitsemän päivän aikana. Jos haluat muuttaa tätä asetusta, määritä **Näytä lopettaneet työntekijät** -aikaväli **Henkilöstöhallinnon parametrit** -sivun **Yleiset**-välilehdestä. **Lopettaneet**-osiossa olevat tiedot voidaan näyttää tietyltä päivien, kuukausien tai vuosien ajalta. Jos haluat esimerkiksi nähdä edellisen 14 päivän aikana lopettaneiden työntekijöiden luettelon, määritä **Kausi**-kentän arvoksi **14** ja **Yksikkö**-kentän arvoksi **Päivät**.

Kun **Lopettaneet**-osiossa näytetään työntekijöitä, seuraavat toiminnot ovat heidän käytettävissään:

- Käytä tarkistusluetteloa\*\*
- Tarkista työsuhde
- Näytä hierarkiassa

\*\* Tämä toiminto on oletustoiminto. Se näytetään kortissa painikkeena.

## <a name="employee-changes-tab"></a>Työntekijöiden muutokset -välilehti

**Työntekijöiden muutokset** -välilehdessä näytetään kaikkien työntekijöihin liittyvien henkilöstötoimintojen luettelo. Tämä luettelo ei ole oletusarvoisesti käytettävissä. Jos haluat ottaa tämän ominaisuuden käyttöön, valitse **Henkilöstöhallinnon jaetut parametrit** -sivun **Henkilöstötoiminnot**-välilehdestä **Ota käyttöön työntekijätoiminnot** -asetukseksi **Kyllä**.

## <a name="position-changes-tab"></a>Toimien muutokset -välilehti

**Toimien muutokset** -välilehdessä näytetään kaikkien toimiin liittyvien henkilöstötoimintojen luettelo. Tämä luettelo ei ole oletusarvoisesti käytettävissä. Jos haluat ottaa tämän ominaisuuden käyttöön, valitse **Henkilöstöhallinnon jaetut parametrit** -sivun **Henkilöstötoiminnot**-välilehdestä **Ota käyttöön toimen toiminnot** -asetukseksi **Kyllä**.

## <a name="open-positions-tab"></a>Avoimet toimet -välilehti

**Avoimet toimet** -välilehdessä näytetään kaikkien avoimien toimien luettelo. Jotta toimet näytettäisiin luettelossa, niiden aktivointipäivän on oltava tänään tai aiemmin, eikä niille voi olla kohdistettu työntekijää.

> [!NOTE]
> Luettelo huomioi työntekijöiden tehtävät tästä päivästä alkaen. Luettelossa näytetään edelleen kaikki toimet, joille on määritetty tulevaisuudessa tapahtuva työntekijän kohdistus. Toimi kuitenkin poistetaan luettelosta, kun työntekijän kohdistuksen voimaantulopäivä on saavutettu.

## <a name="expiring-records-tab"></a>Vanhentuvat tietueet -välilehti

**Vanhentuvat tietueet** -välilehdessä näytetään luettelo kaikista nimikkeistä, jotka ovat vanhentuneet tai jotka vanhentuvat työntekijöille yrityksessä, johon käyttäjä on kirjautunut. Luettelossa näytetään seuraavat nimikkeet:

- **Sertifikaatit**
- **Tunnus**
- **Koeajat**
- **Seulonnat**
- **Testit**

Jos haluat määrittää, näytetäänkö luettelossa vanhentuneet vai vanhentuvat tietueet, määritä **Henkilöstöhallinnon parametrit** -sivun **Yleiset**-välilehdestä aikaväli **Vanhentuvat tietueet**- tai **Vanhentuvat tietueet** -vaihtoehdoille. **Vanhentuvat tietueet** -välilehden tiedot voidaan näyttää tietyltä määrältä päiviä. Jos haluat nähdä esimerkiksi seuraavan 14 päivän aikana vanhentuvien tietueiden luettelon, määritä **Päivien määrä** -kentän arvoksi **14**.

> [!NOTE] 
> Jos määrität **Vanhentuneet tietueet**- tai **Vanhentuvat tietueet** -asetuksen aikaväliksi **0** **Henkilöstöhallinnon parametrit** -sivulla, luettelossa ei näytetä yhtään tietuetta.

## <a name="employees-tile"></a>Työntekijät-ruutu

**Työntekijät**-ruutu näyttää kaikkien niiden työntekijöiden määrän, jotka työskentelevät yrityksessä, johon käyttäjä on tällä hetkellä kirjautunut. Kun valitset **Työntekijät**-ruudun, uudella sivulla näytetään työntekijöiden tiedot.

## <a name="contractors-tile"></a>Alihankkijat-ruutu

**Alihankkijat**-ruutu näyttää kaikkien niiden alihankkijoiden määrän, jotka työskentelevät yrityksessä, johon käyttäjä on tällä hetkellä kirjautunut. Kun valitset **Alihankkijat**-ruudun, uudella sivulla näytetään alihankkijoiden tiedot.

## <a name="open-positions-tile"></a>Avoimet toimet -ruutu

**Avoimet toimet** -ruutu näyttää kaikkien avointen toimien määrän. Kun valitset **Avoimet toimet** -ruudun, uudella sivulla näytetään avoimien toimien tiedot. Jotta toimet sisällytettäisiin tähän määrään, niiden aktivointipäivän on oltava tänään tai aiemmin, eikä niille voi olla kohdistettu työntekijää.

> [!NOTE]
> Ruutu huomioi työntekijöiden tehtävät tästä päivästä alkaen. Määrän lasketaan edelleen kaikki toimet, joille on määritetty tulevaisuudessa tapahtuva työntekijän kohdistus. Toimi kuitenkin jätetään pois määrästä, kun työntekijän kohdistuksen voimaantulopäivä on saavutettu.

## <a name="approvals-tile"></a>Hyväksynnät-ruutu

**Hyväksynnät**-ruutu näyttää kaikkien sellaisten työnkulkunimikkeiden määrän, jotka odottavat tämänhetkisen käyttäjän hyväksyntää. Kun valitset **Hyväksynnät**-ruudun, uudella sivulla näytetään sinun hyväksyntääsi odottavien työnkulkunimikkeiden tiedot.

## <a name="address-changes-tile"></a>Osoitemuutokset-ruutu

**Osoitemuutokset**-ruutu näyttää **Henkilöstöhallinnon parametrit** -sivulla määritetyn aikavälin aikana tapahtuneiden osoitemuutosten määrän. Kun valitset **Osoitemuutokset**-ruudun, uudella sivulla näytetään kaikkien osoitemuutosten tiedot. Voit valita sivun oikeasta yläkulmasta **Sisällytä tulevat osoitemuutokset** -vaihtoehdon nähdäksesi osoitemuutokset, joiden päivämäärä on tulevaisuudessa.

Lisätietoja osoitemuutosten tarkasteleminen ja hallitsemisesta on kohdassa [Osoitemuutosten tarkasteleminen ja hallinta](hr-personnel-view-address-changes.md).
