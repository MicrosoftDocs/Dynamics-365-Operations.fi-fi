---
title: Taloushallinnon dimensiot
description: "Tässä ohjeaiheessa kerrotaan erityyppisistä taloushallinnon dimensioista ja niiden määrittämisestä."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3e9f00fdc32feda0a62f71a92e503a677dce35cc
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="financial-dimensions"></a>Taloushallinnon dimensiot

[!INCLUDE [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään erityyppisiä taloushallinnon dimensioita ja niiden määrittämistä.

Luo **Taloushallinnon dimensiot** -sivun avulla tilikartan tilisegmentteinä käytettäviä taloushallinnon dimensioita. Taloushallinnon dimensioita on kahdenlaisia: mukautettuja ja yksikön tukemia dimensioita. Mukautetut dimensiot jaetaan yritysten välillä, ja käyttäjät vastaavat arvojen antamisesta ja ylläpidosta. Yksikön tukemien dimensioiden arvot määritellään muualla järjestelmässä, esimerkiksi Asiakkaat- tai Myymälät-yksiköissä. Jotkin yksikön tukemat dimensiot jaetaan yritysten välillä, kun taas toiset yksikön tukemat dimensiot ovat yrityskohtaisia. 

Kun taloushallinnon dimensiot on luotu, voit liittää jokaiselle taloushallinnon dimensiolle lisää ominaisuuksia **Taloushallinnon dimension arvot** -sivulla. 

Voit käyttää taloushallinnon dimensiota yritysten esittämiseen. Yrityksiä ei tarvitse luoda Microsoft Dynamics 365 for Finance and Operationsissa. Taloushallinnon dimensioita ei kuitenkaan ole suunniteltu käsittelemään yritysten operatiivisia tai liiketoiminnan tarpeita. Finance and Operationsin yksiköiden välisen kirjanpidon toiminnallisuus on suunniteltu käsittelemään vain jokaisen tapahtuman luomat kirjanpitomerkinnät. 

Ennen kuin määrität taloushallinnon dimensiot yrityksiksi, arvioi liiketoimintaprosessisi seuraavilla alueilla ja selvitä, voiko tätä asetusta käyttää organisaatiossasi:

- Varasto
- Myynnit ja ostot taloushallinnon dimensioiden ja yritysten välillä
- Arvonlisäveron laskenta ja ilmoittaminen
- Toiminnan raportointi

Seuraavassa on joitakin rajoituksia:

- Voit käyttää arvonlisäverotoimintoa ainoastaan yritysten kanssa, et taloushallinnon dimensioiden.
- Jotkin raportit eivät sisällä taloushallinnon dimensioita. Tämän vuoksi raportteja on ehkä muokattava taloushallinnon dimension mukaista raportointia varten.

## <a name="custom-dimensions"></a>Mukautetut dimensiot

Voit luoda käyttäjän määrittämän taloushallinnon dimension valitsemalla luoda **Käytä arvoja kohteesta** -kentässä **&lt; Mukautettu dimensio &gt;**. Voit määrittää myös tilipeitteen rajoittamaan dimensioarvoille annettavaa summaa ja tietojen tyyppiä. Voit antaa jokaisessa dimensioarvossa samana pysyviä arvoja, kuten kirjaimia tai yhdysviivan (-). Voit myös antaa numeromerkkejä (\#) ja et-merkkejä (&) kirjaimien ja numerojen paikkamerkkeinä, jotka muuttuvat aina, kun dimensioarvo luodaan. Käytä numeromerkkiä (\#) numeron paikkamerkkinä ja et-merkkiä (&) kirjaimen paikkamerkkinä. Muotoilupeitteen kenttä on käytettävissä vain, kun valitset **&lt; Mukautettu dimensio &gt;** **Käytä arvoja** -kentässä.

**Esimerkki**

Jos haluat rajoittaa dimensioarvon kirjaimiin CC ja kolmeen numeroon, anna muotoilupeitteeksi **CC-\#\#\#**.

## <a name="entity-backed-dimensions"></a>Yksikön tukemat dimensiot

Voit luoda yksikön tukeman taloushallinnon dimension valitsemalla **Käytä arvojaa** -kenttään järjestelmän määrittämä yksikkö, johon taloushallinnon dimensio perustuu. Taloushallinnon dimensioarvot luodaan sitten tästä yksiköstä. Voit esimerkiksi luoda projektien dimensioarvot valitsemalla **Projektit**. Jokaiselle projektin nimelle luodaan sitten dimensioarvo. Yksikön arvot näkyvät **Taloushallinnon dimension arvot** -sivulla. Jos nämä arvot ovat yrityskohtaisia, myös yritys näkyy sivulla.

## <a name="activating-dimensions"></a>Dimensioiden aktivointi

Kun aktivoit taloushallinnon dimension, taulu päivitetään sisältämään taloushallinnon dimension nimen. Poistetut dimensiot poistetaan. Voit antaa dimensioarvot ennen taloushallinnon dimension aktivointia. Taloushallinnon dimensiota ei voi kuitenkaan kuluttaa missään, ennen kuin se on aktivoitu. Et voi esimerkiksi lisätä taloushallinnon dimensiota tilirakenteeseen ennen dimension aktivointia. Kun valitset **Aktivoi**, kaikki dimensiot päivitetään ja niiden tilan näytetään muuttuneen. 

## <a name="translations"></a>Käännökset

Voit kirjoittaa valitun taloushallinnon dimension **Tekstin käännös** -sivulla erikielistä tekstiä. Voit kirjoittaa päätilille erikielistä tekstiä **Päätilin käännös** -sivulla. 

## <a name="legal-entity-overrides"></a>Yrityksen ohitukset

Kaikkia dimensioita ei voi käyttää kaikissa yrityksissä. Lisäksi jotkin dimensiot voivat liittyä vain tiettyyn jaksoon. Näissä tapauksissa voit määrittää **Yrityksen ohitukset** -osassa yritykset, joissa dimension käyttö pitäisi keskeyttää, omistaja sekä ajanjakso, jolloin dimensio on aktiivinen.

## <a name="deleting-financial-dimensions"></a>Taloushallinnon dimensioiden poistaminen

Tietojen viitteiden eheyden varmistamiseksi taloushallinnon dimensiot voi vain harvoin poistaa. Jos yrität poistaa taloushallinnon dimension, seuraavat ehdot arvioidaan:

- Onko taloushallinnon dimensiota käytetty missään kirjatussa tai kirjaamattomassa tapahtumassa tai jossain dimensioarvoyhdistelmässä?
- Onko taloushallinnon dimensiota käytettä missään aktiivisessa tilirakenteessa, lisäasetuksia käyttävässä sääntörakenteessa tai taloushallinnon dimensiojoukossa?
- Onko taloushallinnon dimensio osa oletusarvoista taloushallinnon dimension integrointimuotoa?
- Onko taloushallinnon dimensio määritetty oletusdimensioksi?

Jos jokin ehdoista täyttyy, et voi poistaa taloushallinnon dimensiota.


Lisätietoja on seuraavissa aiheissa:
- [Määritä taloushallinnon dimensiot](tasks/define-financial-dimensions.md)
- [Ylläpidä taloushallinnon dimension oletusmalleja](tasks/maintain-financial-dimension-default-templates.md)

