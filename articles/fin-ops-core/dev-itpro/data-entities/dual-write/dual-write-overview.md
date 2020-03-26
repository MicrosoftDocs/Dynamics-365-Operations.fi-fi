---
title: Kaksoiskirjoituksen yleiskatsaus
description: Tämä ohjeaihe sisältää kaksoiskirjoituksen yleiskatsauksen. Kaksoiskirjoitus on infrastruktuuri, joka sisältää lähes reaaliaikaisen vuorovaikutuksen Microsoft Dynamics 365:n mallipohjaisten sovellusten ja Finance and Operations -sovellusten välillä.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c4a643d4981364cea5b549118c201ac8a9798e02
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113871"
---
# <a name="dual-write-overview"></a>Kaksoiskirjoituksen yleiskatsaus

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a>Mikä on kaksoiskirjoitus?

Kaksoiskirjoitus on valmis infrastruktuuri, joka sisältää lähes reaaliaikaisen vuorovaikutuksen Microsoft Dynamics 365:n mallipohjaisten sovellusten ja Finance and Operations -sovellusten välillä. Kun asiakkaiden, tuotteiden, henkilöiden ja toimintojen tiedot siirretään sovellusten ulkopuolelle, kaikki organisaation osastot voivat käyttää niitä.

Kaksoiskirjoitus sisältää tiukasti yhdistetyn kaksisuuntaisen integroinnin Finance and Operations -sovellusten ja Common Data Servicen välillä. Kaikki tietojen muutokset Finance and Operations -sovelluksissa aiheuttavat kaksoiskirjoituksia Common Data Servicessä ja Common Data Servicen tietojen muutokset puolestaan kirjoituksia Finance and Operations -sovelluksissa. Tämä automatisoitu tietovirta tarjoaa integroidun käyttökokemuksen eri sovelluksissa.

![Tietojen suhde sovellusten välillä](media/dual-write-overview.jpg)

Kaksoiskirjoituksissa on eri osaa: *infrastruktuuri* ja *sovellus*.

### <a name="infrastructure"></a>Infrastruktuuri

Kaksoiskirjoituksen infrastruktuuri on laajennettavissa. Se on luotettava infrastruktuuri, joka sisältää seuraavat keskeiset ominaisuudet:

+ Sovellusten välinen synkroninen ja kaksisuuntainen tietovirta
+ Synkronisointi yhdessä toiston, pysäytyksen ja kertymän tilojen kanssa tukee järjestelmää online- ja offline-tilassa sekä asynkronisessa tilassa.
+ Mahdollisuus synkronoida alkuperäiset tiedot sovellusten välillä
+ Yhdistetty näkymä toiminto- ja virhelokeista tietojen järjestelmänvalvojille
+ Mahdollisuus määrittää mukautettuja hälytyksiä ja rajoja sekä tilata ilmoituksia
+ Intuitiivinen käyttöliittymä suodatusta ja muunnoksia varten
+ Mahdollisuus määrittää ja tarkastella entiteetin riippuvuuksia ja suhteita
+ Laajennettavuus sekä vakioentiteeteille että mukautetuille entiteeteille ja määrityksille
+ Luotettava sovelluksen elinkaaren hallinta
+ Uusien asiakkaiden valmis määrityskokemus

### <a name="application"></a>Hakemus

Kaksoiskirjoitus luo vastaavuuden Finance and Operations -sovellusten käsitteiden ja Dynamics 365:n mallipohjaisten sovellusten käsitteiden välille. Tämä integraatio tukee seuraavia skenaarioita:

+ Integroidut asiakkaan päätiedot
+ Asiakkaan kanta-asiakaskorttien ja palkkiopisteiden käyttöoikeus
+ Yhtenäinen tuotteiden hallinnan kokemus
+ Tietoja organisaatiohierarkiasta
+ Integroidut toimittajan päätiedot
+ Talous- ja veroviitetietojen käyttöoikeus
+ Tarvittaessa käytettävän hinnoitteluohjelman käyttökokemus
+ Integroitu prospektista käteiseksi -käyttökokemus
+ Mahdollisuus sekä sisäisten resurssien että asiakkaan resurssien käyttämiseen kentän edustajien kautta
+ Integroitu hankinnasta maksuun -käyttökokemus
+ Asiakastietojen ja asiakirjojen integroidut aktiviteetit ja huomautukset
+ Mahdollisuus etsiä käytettävissä olevan varaston saatavuutta ja tietoja
+ Projektista käteiseksi -käyttökokemus
+ Mahdollisuus käsitellä useita osoitteita ja rooleja osapuolen käsitteen kautta
+ Yhden lähteen hallinta käyttäjille
+ Vähittäiskaupan ja markkinoinnin integroidut kanavat
+ Kampanjoiden ja alennusten näkyvyys
+ Palvelupyyntöjen toiminnot
+ Yksinkertaistetut palvelutoiminnot

## <a name="top-reasons-to-use-dual-write"></a>Yleisimmät syyt kaksoiskirjoittamisen käyttämiseksi

Kaksoiskirjoitus mahdollistaa tietojen integroinnin Microsoft Dynamics 365 -sovelluksissa Tämä luotettava kehys linkittää ympäristöt ja mahdollistaa erilaisten liiketoimintasovellusten käyttämisen yhdessä. Seuraavassa kerrotaan tärkeimmät syyt kaksoiskirjoituksen käyttämiseksi:

+ Kaksoiskirjoitus mahdollistaa tiiviisti yhdistetyn ja lähes reaaliaikaisen kaksisuuntaisen integroinnin Finance and Operations -sovellusten ja Dynamics 365:n mallipohjaisten sovellusten välillä. Tämä integraatio tekee Microsoft Dynamics 365:stä yhden pysähdyksen kaupan kaikille liiketoimintasovelluksille. Asiakkaat, jotka käyttävät Dynamics 365 Finance- ja Dynamics 365 Supply Chain Management -sovellusta, mutta jotka käyttävät asiakkuudenhallintaan (CRM) jotain muuta kuin Microsoftin ratkaisua, siirtyvät kohti Dynamics 365:ttä sen kaksoiskirjoitustuen vuoksi.
+ Asiakkaiden, tuotteiden, toimintojen, projektien ja esineiden internetin tiedot siirtyvät automaattisesti Common Data Serviceen kaksoiskirjoituksen kautta. Tämä yhteys on erittäin hyödyllinen yrityksille, jotka ovat kiinnostuneita Microsoft Power Platform -laajennuksista.
+ Kaksoiskirjoitusinfrastruktuuri noudattaa kooditonta / vähäisen koodin periaatetta. Vakiomuotoisten taulukosta taulukkoon -määritysten ja mukautettujen määritysten laajentamisessa ei tarvita paljon kehitystyötä.
+ Kaksoiskirjoitus tukee sekä online- että offline-tilaa. Microsoft on ainoa yritys, joka tarjoaa tukea online-ja offline-tilassa.

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a>Mitä kaksoiskirjoituds tarkoittaa CRM-tuotteiden käyttäjille ja suunnittelijoille?

Kaksoiskirjoitus automatisoi tietovirran Finance and Operations -sovellusten ja Common Data Servicen välillä. Tulevissa versioissa Dynamics 365:n mallipohjaisten sovellusten käsitteet (esimerkiksi asiakas, yhteyshenkilö, tarjous ja tilaus) skaalataan keskisuurten ja suurten markkinoiden asiakkaille.

Ensimmäisessä versiossa kaksoiskirjoitusratkaisut käsittelevät suurinta osaa automaatiosta. Tulevissa versioissa näistä ratkaisuista tulee osa Common Data Servicea. Common Data Servicen tulevien muutosten ymmärtäminen helpottaa työtä jatkossa. Tässä esitellään joitakin tärkeitä muutoksia:

+ Common Data Service sisältää uusia käsitteitä, kuten yritys ja osapuoli. Nämä käsitteet vaikuttavat kaikkiin Common Data Servicen avulla muodostettuihin sovelluksiin, kuten Dynamics 365 Sales-, Dynamics 365 Marketing-, Dynamics 365 Customer Service- ja Dynamics 365 Field Service -sovellukseen.
+ Toiminnot ja huomautukset ovat yhtenäisiä ja laajenevat tukemaan sekä C1 (järjestelmän käyttäjät)- että C2 (järjestelmän asiakkaat) -kohteita.
+ Tässä esitellään joitakin Common Data Servicen tärkeitä muutoksia:

    - Desimaalitietotyyppi korvaa raha-tietotyypin.
    - Voimassaolopäivä tukee mennyttä, nykyistä ja tulevaa päivämäärää samassa paikassa.
    - Valuutta- ja vaihtokursseja tuetaan aiempaa enemmän ja **Vaihtokurssi**-ohjelmointirajapintaa muutetaan.
    - Yksikkömuunnoksia tuetaan.

Lisätietoja tulevista muutoksista on kohdassa [Common Data Servicen tiedot – vaihe 1 ja 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).
