---
title: Kurssien yleiskatsaus
description: Tässä artikkelissa kerrotaan, miten Human Resources -järjestelmänvalvojat ja -esimiehet voivat käyttää kurssiominaisuuksia ylläpitäessään tietoja työntekijöiden käytettävissä olevista kursseista.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a1fd00fb9feea9ab426f67095770389696452215
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716334"
---
# <a name="courses-overview"></a>Kurssien yleiskatsaus

Microsoft Dynamics 365 Human Resources sisältää ratkaisun organisaation oppimistarpeita varten. Tämä ratkaisu sisältää kaksi oppimisen kurssipolkua: *virtuaalinen* ja *ohjattu* koulutus.

*Virtuaalinen oppiminen* on oppimiskokemus, jota tehostetaan online-resurssien avulla. *Ohjatussa koulutuksessa* opettaja tarjoaa koulutusistunnon työntekijä- tai opiskelijaryhmälle.

Oppimismoduulissa Human Resourcesin ammattilaiset, järjestelmänvalvojat, koulutusesimiehet ja esimiehet voivat luoda oppimisen kurssipolkuja ja delegoida niitä työntekijöille.

> [!NOTE]
> Jos haluat käyttää virtuaalisia kursseja, sinun on otettava se käyttöön **Kurssin parannukset** -ominaisuus Ominaisuuksien hallinta -kohdassa.

## <a name="set-up-virtual-courses"></a>Virtuaalisten kurssien määrittäminen

Jos haluat määrittää virtuaalisia kursseja, sinun on otettava se käyttöön **Kurssin parannukset** -ominaisuus Ominaisuuksien hallinta -kohdassa. Siirry kohtaan **Kurssit \> Uusi** ja määritä **Virtuaalinen**-vaihtoehdon arvoksi **Kyllä**. Kun ominaisuus on otettu käyttöön, tarvitaan kurssilinkki. **Kurssin tila** -kentän arvoksi määritetään **Avoin**. **Salli työntekijän rekisteröityä itse** -vaihtoehdon arvoksi määritetään **Kyllä**. Arvoksi voi myös määrittää **Ei**.

Kun **Kurssin parannukset** -ominaisuus on otettu käyttöön Ominaisuuksien hallinta -kohdassa, tehdään seuraavat muutokset:

- Kurssin tehtävän määräpäivä on määritettävä.
- Kurssilinkki on pakollinen.
- **Työntekijän itsepalvelu** näyttää työntekijän yleiskatsauksen **Kurssit**-kohdassa. Käyttäjä voi tarkastella kursseja, jotka ovat myöhässä, joiden määräpäivä on kohta sekä delegoituja kursseja.
- Työntekijät voivat suorittaa virtuaalikursseja ja arvioida ne itse.

## <a name="set-up-instructor-led-courses"></a>Ohjattujen kurssien määrittäminen

Ohjattuja kursseja ei tarvitse määrittää ennen niiden käyttämistä.

Alla olevat tiedot ovat kursseille haluttaessa määritettäviä tietoja. Jos kursseille syötetään seuraavat tiedot, ne on määritettävä ennen kurssitietueiden luomista:

- Kurssityyppi
- Luokkahuoneryhmät
- Kurssiryhmät
- Kurssipaikat
- Luokkahuoneet
- Opettajat
- Kurssityypit

Voit käyttää *kurssityyppejä* kurssien luokittelemiseen niiden rakenteen tai sisällön perusteella. Sivulla **Kurssityypit** voit luoda kurssityyppejä.

Sivun **Kurssit** pikavälilehdessä **Yleinen** määritetään kurssille rekisteröitävien osallistujien vähimmäis- ja enimmäismäärä.

### <a name="course-setup-type"></a>Kurssin asetustyyppi 

*Määritystyypit* määrittävät kurssin rakenteen. Kursseilla on kolme määritystyyppiä.

| Määritystyyppi | Kuvaus |
|------|--------|
| Vakio | Tämän tyypin kursseilla ei ole päivittäistä työjärjestystä. Tämä on oletusarvoinen asetustyyppi, kun luot uuden kurssin. |
| Työjärjestys | Valitsemalla tämän asetustyypin voit suunnitella useita päiviä kestävän kurssin eri päivien sisällön. |
| Työjärjestys ja istunto | <p>Valitse tämä asetustyyppi monimutkaisille kursseille. Voit esimerkiksi jakaa kurssin ohjelman *edistymissuunnitelmiin* ja *istuntoihin* seuraavalla tavalla:</p><ul><li>*Edistymissuunnitelmat* ovat kurssin erityisiä aihealueita.</li><li>*Istunnot* jaetaan edistymissuunnitelmiin. Ne auttamat tunnistamaan prosesseja tai tekniikkoja, joilla on merkitystä edistymissuunnitelman kannalta.</li></ul> |

### <a name="course-tasks"></a>Kurssin tehtävät

Voit suorittaa jokaiselle kurssille seuraavat tehtävät:

- Rekisteröi osallistujia.
- Määritä rekisteröinnin määräaika.
- Määritä osallistujien vähimmäis- ja enimmäismäärät.
- Määritä kurssin sijainti ja luokkahuone.
- Suosittele kurssin osallistujille hotelleja.
- Luo kurssin kuvaus, joka voidaan julkaista **työntekijän itsepalvelussa**.

> [!NOTE]
> Voit poistaa kurssin vain, jos kukaan ei ole rekisteröitynyt siihen.

### <a name="course-statuses"></a>Kurssin tilat

Seuraavassa taulussa ovat kurssien tilat ja toiminnot, jotka kustakin on suoritettu.

| Tila | Toiminnot |
|------|--------|
| Luontiajankohta | <ul><li>Kirjoita ja muuta kurssin tietoja.</li><li>Muuta kurssin tilaksi **Avoin**, jotta työntekijät voivat rekisteröityä kurssille.</li></ul> | 
| Avaa | <ul><li>Rekisteröi kurssin osallistujat.</li><li>Poista kurssin osallistujia.</li><li>Vahvista kurssin osallistujat</li><li>Muuta kurssin tilaksi **Suljettu** tai **Peruutettu** osallistujille, joiden tila on **Vahvistettu**.</li></ul>|
| Valmis | Voit avata kurssin uudelleen. |
| Peruutettu | Voit avata kurssin uudelleen. |

### <a name="course-participants"></a>Kurssin osallistujat

*Kurssin osallistujat* ovat työntekijöitä, jotka osallistuvat koulutuskurssille tai tapahtumaan. Voit rekisteröidä osallistujia vain avoimille kursseille.

### <a name="workflow"></a>Työnkulku

Työntekijät, jotka ilmoittautuvat kurssille **Työntekijän itsepalvelu** -sivulla, voivat saada ilmoittautumisen reititettyä hyväksynnän työnkulun kautta. Sivun **Kurssit** pikavälilehdessä **Yleinen** voit määrittää kurssille työnkulun.
