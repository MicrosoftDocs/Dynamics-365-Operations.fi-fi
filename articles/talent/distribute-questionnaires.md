---
title: "Kyselylomakkeen jakaminen ja täyttäminen"
description: "Tässä artikkelissa kerrotaan, miten suunnittelemasi kyselylomakkeet jaetaan niin, että ne ovat oikean henkilön tai henkilöryhmän täytettävissä."
author: kherr75
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: kherr75
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9a9883c44202c3fdb963c4dc3ebbb39155a911da
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="distribute-and-complete-a-questionnaire"></a>Kyselylomakkeen jakaminen ja täyttäminen

[!include[banner](includes/banner.md)]


Tässä artikkelissa kerrotaan, miten suunnittelemasi kyselylomakkeet jaetaan niin, että ne ovat oikean henkilön tai henkilöryhmän täytettävissä. 

Kyselylomakkeen voi jakaa seuraavilla tavoilla:

-   Merkitse kyselylomake aktiiviseksi. Tämän jälkeen kyselylomake on kaikkien työntekijöiden käytettävässä, jos kyselylomakeryhmän määrityksissä ei ole valittu toisin.
-   Liitä käyttöoikeudet kyselylomakeryhmään. Tämän jälkeen kyselylomake on valitun ryhmän jokaisen jäsenen käytettävissä.
-   Luo suunniteltuja vastausistuntoja. Näin kyselylomake on vain tietyn henkilön käytettävissä.
-   Luo aikataulu. Näin kyselylomake voi olla useiden henkilöiden käytettävissä.

## <a name="marking-a-questionnaire-as-active"></a>Kyselylomakkeen merkitseminen aktiiviseksi
Kun määrität **Aktiivinen**-kentän arvoksi **Kyllä** **Kyselylomakkeet**-sivulla, voit määrittää kyselylomakkeen kaikkien työntekijöiden käyttöön. Vastaajat voivat täyttää kyselylomakkeen useita kertoja. Tämä toiminto on hyödyllinen, jos haluat kerätä palautetta koko vuoden ajan. Voit luoda esimerkiksi kyselylomakkeen, jonka avulla työntekijät voivat antaa palautetta kahvilan lounaspalvelusta.

## <a name="questionnaire-groups"></a>Kyselylomakeryhmät
Voit määrittää kyselylomakeryhmät ja lisätä vastaajat, joille kyselylomake jaetaan. 

Voit luoda kyselylomakeryhmiä seuraavilta sivuilta:

-   **Kyselylomakeryhmät**– Vain kyselylomakeryhmään kuuluvat henkilöt voivat täyttää valitun kyselylomakkeen. Jos kohdeyleisöksi on määritetty esimerkiksi alihankkijat, voit luoda juuri heille määritetyn kyselylomakeryhmän.
-   **Kyselylomakeryhmän jäsenet** – Voit lisätä kyselylomakeryhmiin henkilöitä.

Liitä kyselylomakeryhmä kyselylomakkeeseen valitsemalla **Kyselylomakkeet**-sivulla **Käyttöoikeudet**. Kun kyselylomake on tallennettu aktiiviseksi, kyselylomakeryhmän jäsenet voivat täyttää kyselylomakkeen. Tämä toiminto on hyödyllinen, jos haluat testata kyselylomakkeen valitulla ryhmällä henkilöitä, ennen kuin se lähetetään suuremmalle ryhmälle, tai jos haluat kohdistaa kyselylomakkeen tietylle yleisölle.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Kyselylomakkeen suunnitellut vastausistunnot
Suunnitellut vastausistunnot ovat vastaajille suunniteltuja ja valittuja kyselylomakkeita. 

> **Huomautus:** Kyselylomake on määritettävä ennen suunniteltujen vastausistuntojen määrittämistä. 

Luo suunniteltu vastausistunto yksittäiselle työntekijälle **Suunniteltu vastausistunto** -sivulla Sivulla oleva luettelo sisältää kaikki suunnitellut kyselylomakkeet. 

Suunniteltuja vastausistuntoja käytetään myös **Kyselylomakkeiden aikataulut** -sivulla, jolla voit suunnitella kyselylomakkeita useille ihmisille. Heitä ovat:

-   Työntekijät
-   Kurssin osallistujat
-   organisaatioyksiköt

Kukin henkilö voi vastata kyselylomakkeeseen vain kerran.

## <a name="scheduling-a-questionnaire"></a>Kyselylomakkeen ajoittaminen
Halutessasi voit aikatauluttaa kyselylomakkeen useille vastaajille.

### <a name="planning-types"></a>Suunnittelutyypit

Suunnittelutyypit ovat pakollisia, jos haluat ajoittaa suunnitellut vastausistunnot useille vastaajille. Suunnittelutyyppejä käytetään kyselylomakkeiden aikataulujen luokittelussa. Voit ajoittaa kyselylomakkeita esimerkiksi seuraavia tarkoituksia varten:

-   Arviointi
-   Kysely
-   Testaaminen

Voit määrittää kyselylomakkeen aikataulun suunnittelutyypit **Kyselylomakkeiden aikataulut** -sivulla.

### <a name="reference-types-for-questionnaire"></a>Kyselylomakkeen viitetyypit

Viitetyyppien avulla voit syöttää vastaajille ehdot, jotka valitsisit kyselylomakkeen ajoittamisen yhteydessä. 

Määritä kyselylomakkeen viitetyypit **Viitetyypit**-sivulla. Kukin viitetyyppi vastaa Microsoft Dynamics 365 for Finance and Operationsin taulua. Voit määrittää kyselylomakkeen aikataulujen luomisen yhteydessä yksittäisiä tietueita tauluun tai tietuealueen. Tietueet tai tietuealue liitetään kyselylomakkeeseen. 

Esimerkiksi Kurssit-taulussa voit määrittää kurssin, jota kyselylomake koskee. Kun määrität Kurssit-taulun viitteen, osa **Kurssit**-sivun kentistä ja painikkeista ovat käytettävissä.

### <a name="questionnaire-schedules"></a>Kyselylomakkeiden aikataulut

Voit käyttää kyselylomakkeen ajoituksia luodessasi useita suunniteltuja vastausistuntoja käyttäjäryhmälle viitetyypin perusteella. Luo aikataulu **Kyselylomakkeiden aikataulut** -sivulla. Luokittele aikataulu valitsemalla suunnittelutyyppi ja valitse myös viitetyyppi, jota käytetään suoritettaessa järjestelmäkysely tiettyjen käyttäjien osalta. Jos määrität Kurssit-taulun arvoksi Viitetyyppi, voit valita tietyn kurssin **Viite**-kentässä. 

Valitse kyselylomake ja muut ehdot valitsemalla **Asetuksen tiedot**. Määritä ehdoksi esimerkiksi opettajan nimi, jos kyselylomake koskee opettajan arviointia. Kun asetuksen tiedot on syötetty, järjestelmä luo kyselyyn kuuluville käyttäjille suunnitellut vastausistunnot. 

Voit tarkastella aikataulun vastausistuntoja **Suunnitellut vastausistunnot** -kohdassa. Tämän jälkeen voit luoda lisää suunniteltuja vastausistuntoja manuaalisesti tai poistaa istuntoja, joihin ei ole vastattu. 

Ota kyselylomake käyttöön liittyvien suunniteltujen vastausistuntojen käyttäjille valitsemalla **Toiminnot** &gt; **Käynnistä**. Voit tarkastella kyselylomakkeen vastauksia **Vastaukset**-kohdassa. Voit myös kopioida kyselylomakkeen aikataulun asetuksia, suunniteltuja vastausistuntoja ja vastauksia uutta kyselylomakkeen aikataulua varten.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Käytettävissä olevista kyselylomakkeista ilmoittaminen vastaajille
Kun jaat kyselylomakkeen, sinun on ilmoitettava vastaajille, että kyselylomakkeet ovat heidän saatavillaan. 

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Suunnitellusta vastausistunnosta ilmoittaminen vastaajille

Jos käytössä on suunniteltu vastausistunto, henkilölle on ilmoitettava suoraan esimerkiksi puhelimitse tai sähköpostitse.

### <a name="notifying-respondents-about-a-scheduling"></a>Aikataulusta ilmoittaminen vastaajille

**Kyselylomakkeiden aikataulut** -sivulla voidaan luoda ja lähettää sähköpostiviesti kaikille kyselylomakkeen vastaajille. Syötä sähköpostiviestin teksti **Työntekijän itsepalvelun sähköpostiosoite** -välilehdessä. Kun ajoitus on aloitettu, luo ja lähetä sähköposti vastaajille valitsemalla **Toiminnot** &gt; **Lähetä sähköposti**. Vastaajat voivat sitten kirjautua sivustoon ja täyttää kyselylomakkeen. 

> **Huomautus:** IT-järjestelmänvalvojan on annettava sähköpostiasetukset **Sähköpostiparametrit**-sivulla, ennen kuin tämä toiminto otetaan käyttöön.

## <a name="ending-a-scheduled-questionnaire"></a>Ajoitetun kyselyn päättäminen
Voit lopettaa aikataulutetun kyselylomakkeen, kun kaikki vastaajat ovat tehneet vastausistuntonsa loppuun. Kun ajoitettu kyselylomake lopetetaan, asetuksia ei enää voi kopioida uuteen aikatauluun. 

> **Huomautus:** Jos vähintään yksi vastaaja ei ole täyttänyt vastauslomaketta, mutta haluat siitä huolimatta lopettaa aikataulutuksen, poista vastaajat **Suunniteltu vastausistunto** -sivun luettelosta. Sen jälkeen voit lopettaa aikataulun.

## <a name="completing-questionnaires"></a>Kyselylomakkeiden täyttäminen
Kun kyselylomake on suunniteltu ja jaettu, valitut vastaajat voivat täyttää sen. Voit täyttää kyselylomakkeita kahdesta käytettävissäsi olevasta sijainnista:

-   Valitse siirtymisruudussa **Kyselylomakkeet** &gt; **Jaa** &gt; **Täydennä kyselylomake**.
-   Valitse työntekijän itsepalvelussa **Täytettävät kyselylomakkeet**.

Kyselylomakkeet voidaan määrittää tietyille käyttäjille tai käyttäjäryhmille tai kaikille verkon käyttäjille.

<a name="see-also"></a>Lisätietoja
--------

[Kyselylomakkeiden suunnitteleminen](design-questionnaires.md)

[Kyselylomakkeiden käyttäminen](questionnaires.md)

[Kyselylomakkeen tulosten tarkasteleminen ja arvioiminen](evaluate-questionnaire-results.md)



