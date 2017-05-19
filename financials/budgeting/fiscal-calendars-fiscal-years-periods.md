---
title: Kirjanpidon kalenterit, tilikaudet ja kaudet
description: "Tässä artikkelissa käsitellään kirjanpidon vuosikalentereita ja tilikausia sekä sitä, miten niitä käytetään yrityksissä, käyttöomaisuudessa ja budjetoinnissa."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FiscalCalendars
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25851
ms.assetid: a968a5e5-585e-4389-aa4e-c885a7e23413
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 373c30904604c73271b6a25ee6523b278b5ec861
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="fiscal-calendars-fiscal-years-and-periods"></a>Kirjanpidon kalenterit, tilikaudet ja kaudet

[!include[banner](../includes/banner.md)]


Tässä artikkelissa käsitellään kirjanpidon vuosikalentereita ja tilikausia sekä sitä, miten niitä käytetään yrityksissä, käyttöomaisuudessa ja budjetoinnissa.

Kirjanpidon kalenterit tarjoavat kehyksen organisaation taloudelliselle toiminnalle. Jokainen kirjanpidon vuosikalenteri sisältää yhden tai useamman tilikauden ja jokainen tilikausi sisältää useita kausia. Kirjanpidon kalenterit voivat perustua kalenterivuoteen välille 1.1.-31.12 tai mille tahansa valitsemillesi päivämäärille. Valitse esimerkiksi joissakin organisaatioissa vuosikalenteri, joka alkaa 1. kesäkuuta yhtenä vuotena ja päättyy 30. kesäkuuta seuraavana vuonna. 

Luotavien kirjanpidon vuosikalentereiden määrää tai kirjanpidon vuosikalenteriin luotavien tilikausien määrää ei ole rajoitettu. Jokainen vuosikalenteri on riippumaton organisaatiostasi ja useat organisaation yritykset voivat käyttää sitä. Organisaatiolla on esimerkiksi kahdeksan osastoa ja jokainen osasto on erillinen yritys. Viisi niistä jakavat saman kirjanpidon vuosikalenterin ja kolme käyttävät erilaisia kirjanpidon vuosikalentereita. Voit luoda yhden kirjanpidon vuosikalenterin 5 yritykselle, jotka käyttävät samaa vuosikalenteria, ja sitten luoda erillinen kirjanpidon vuosikalenteri muille yrityksille.

## <a name="create-fiscal-calendars-fiscal-years-and-periods"></a>Luo tilikauden kalentereita, tilikausia ja jaksoja
Voit luoda ja poistaa kirjanpidon kalentereita, tilikausia ja kausia Kirjanpidon kalenterit -sivulla. Voit jakaa aiemmin luotuja kausia ja luoda lopetuskausia, jonka avulla voidaan sulkea tilikauden. 

Päätöskautta käytetään erottamaan pääkirjanpidon tapahtumat, jotka luodaan, kun tilikausi on suljettu. Kun sulkevat tapahtumat ovat yhdessä kirjanpitokaudessa, on helpompi luoda raportteja, jotka joko sisältävät tai eivät sisällä erilaisia tilinpäätöstapahtumia. Jos tilikausi on jaettu 12 kauteen, päätöskausi on yleensä kolmastoista kausi. Lopetuskausi voidaan kuitenkin luoda mistä tahansa jaksosta, jonka tila on Avoin. 

Luodessasi lopetuskauden valitse kausi, jonka tila on Avoin ja jonka päivämääriä haluat käyttää. Uusi päätöskausi kopioi aloitus- ja lopetuspäivämäärät nykyisestä kaudesta. Alkuperäinen kausi on edelleen olemassa. Valitse esimerkiksi kausi 12, joka on tilikauden viimeisen kausi ja jonka päivämäärät ovat 1.-31.8. Voit nimetä sulkemiskauden esim. nimellä Sulje. Kun olet luonut uuden päätöskauden, sinulla on nyt alkuperäinen kausi ja päätöskausi. Molemmissa on päivämäärät, jotka alkavat 1.8. ja päättyvät 31.8.

## <a name="select-fiscal-calendars-for-ledgers-fixed-assets-and-budget-cycles"></a>Valitse kirjanpidon, käyttöomaisuuden ja budjettijaksojen tilikauden kalenterit
Kirjanpidon kalentereita käytetään käyttöomaisuuden poistojen, kirjanpitotapahtumien ja budjettijaksojen kanssa. Kirjanpidon vuosikalenterin luodessasi voit käyttää sitä useita tarkoituksia varten. Voit valita kirjanpidon vuosikalenterin arvomallille tai poistokirjalle tehdäksesi riitä käyttöomaisuuskalenterin. Voit valita kirjanpidolle budjettijaksolle ja tehdä siitä budjettikalenterin. Voit valita budjettijaksolle kirjanpidon vuosikalenterin ja tehdä siitä budjettikalenterin. Voit käyttää samaa kirjanpidon vuosikalenteria näille kaikille.

### <a name="select-a-fiscal-calendar-for-your-legal-entity"></a>Valitse oikeushenkilöllesi kirjanpidon vuosikalenteri

Valitse Kirjanpito-lomakkeessa kirjanpidon kalenteri, jota haluat käyttää yrityksesi kirjanpitoon. Kirjanpidon kalenteri on valittava Kirjanpito-sivulla jokaiselle yritykselle. Kun kirjanpidon kalenteri on valittu, voit määrittää kausien tilat ja oikeudet Kirjanpitokalenteri-sivulla kaikille kausille, jotka ovat osa tilikautta.

### <a name="select-a-fiscal-calendar-for-fixed-assets"></a>Valitse verovuosi käyttöomaisuudelle

Voit valita kirjanpidon vuosikalenterin arvomallille tai poistokirjalle, ja tätä vuosikalenteria käytetään käyttöomaisuuteen, joka käyttää valittua arvomallia tai poistokirjaa. Voit valita kaikista kirjanpidon kalentereista, jotka on määritetty Kirjanpidon kalenterit -sivulla.

### <a name="define-budget-cycle-time-spans"></a>Määritä budjettijakson aikavälit

Budjettijaksoja ovat ajat, jolloin budjetointia käytetään. Budjettijaksoja voivat olla tilikauden osat tai useat tilikaudet, esimerkiksi kaksi tai kolme vuotta. Budjettijakson aikaväli määrittää budjettijaksoon sisällytettävien kausien määrän. Voit määrittää budjettijakson aikavälin Budjettijakson aikavälit -sivulla.

## <a name="maintain-periods-for-your-organization"></a>Ylläpidä organisaation jaksoja
Voit käyttää Kirjanpitokalenteri-sivua organisaatiosi käyttämän kirjanpidon kalenterin, tilikausien ja jaksojen tarkastelemiseen. Voit myös muuttaa kausien tilaa ja valita käyttäjät, jotka voivat kirjata kirjanpidon tapahtumia kausille. Esimerkiksi uuden jakson alussa voit ehkä haluta, että jokin käyttäjäryhmä lopettaa kirjanpitotapahtumien kirjaamisen edelliseen jaksoon, kun taas muut ryhmät tekevät kirjauksia vain uuteen jaksoon.






