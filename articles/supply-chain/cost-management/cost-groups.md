---
title: Kustannusryhmät
description: Kustannusryhmät muodostavat pohjan valmistetun nimikkeen laskettujen kustannusten kustannusosuuksien, kuten materiaali- ja työkustannusten osuuksien sekä yleiskustannusten osuuden, segmentoinnille ja analysoinnille. Kustannusryhmän segmentoinnilla on valmistusympäristöissä useita synonyymejä, kuten kustannuserittely, kustannusten hajottaminen ja kustannusluokittelu.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCostGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 50871
ms.assetid: 1855f744-f73f-4fa8-8290-a7ee126d368b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dee8e40de43480cd010b5acc41a3d87611c2ab6
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981605"
---
# <a name="cost-groups"></a>Kustannusryhmät

[!include [banner](../includes/banner.md)]

Kustannusryhmät muodostavat pohjan valmistetun nimikkeen laskettujen kustannusten kustannusosuuksien, kuten materiaali- ja työkustannusten osuuksien sekä yleiskustannusten osuuden, segmentoinnille ja analysoinnille. Kustannusryhmän segmentoinnilla on valmistusympäristöissä useita synonyymejä, kuten kustannuserittely, kustannusten hajottaminen ja kustannusluokittelu. 

Kustannusryhmän segmentoinnilla on valmistusympäristöissä useita synonyymejä, kuten kustannuserittely, kustannusten hajottaminen ja kustannusluokittelu. Kustannusryhmien segmentoinnista on monenlaista hyötyä. Seuraavassa on muutamia esimerkkejä:

-   Se voi segmentoida erityyppisten materiaalien, kuten säilyketuotteen valmistusaineiden ja pakkausmateriaalien, kustannukset. Ne perustuvat nimikkeille määritettyihin kustannusryhmiin.
-   Se voi segmentoida erityyppisten operatiivisten resurssien, kuten erityyppisen työvoiman tai erilaisten koneiden, kustannukset. Ne perustuvat kustannusryhmiin, jotka on määritetty operatiivisten resurssien ja reitityksen työvaiheisiin liittyville kustannusluokille.
-   Se voi segmentoida reitityksen työvaiheiden määritysten ja suoritusajan kustannukset. Ne perustuvat kustannusryhmiin, jotka on määritetty reitityksen työvaiheisiin liittyville kustannusluokille.
-   Se voi segmentoida erityyppisten yleiskustannusten, kuten työhön ja koneisiin liittyvien yleiskustannusten, kustannukset. Ne perustuvat kustannusryhmiin, jotka on määritetty kustannuslaskennan määrityksessä epäsuorille kustannuksille.
-   Se voi toimia pohjana erityyppisten valmistuksen yleiskustannusten laskennalle kustannuslaskennan määrityksessä. Tämä voi sisältää erilaisia yleiskustannuksia, jotka liittyvät operatiivisten resurssien reititystietoihin tai asetus- ja suoritusajan tietoihin. Valmistuksen yleiskustannusten ja komponentin materiaalikustannusten osuuden välillä voi myös olla yhteys. Se on merkki Lean-valmistusfilosofiasta, jossa reititystietoja ei tarvita.

Kustannusryhmän segmentointi koskee valmistetun nimikkeen laskettuja kustannuksia huolimatta siitä, perustuvatko ne standardikustannuksiin vai suunniteltuihin kustannuksiin. Segmentointi näkyy **Yhteenveto**-sivulla kustannusryhmän, tason tai molempien mukaan. 

Kustannusryhmän segmentoinnin säilyttämistä eri tasoilla kutsutaan *jakamiseksi*. Jakaminen koskee vain valmistettuja nimikkeitä, joissa käytetään Standardikustannus-varastomallia. Jos jakamista ei käytetä, valmistetun komponentin kustannuksia käsitellään materiaalikustannusten osuutena. Alareskontran varastoparametri kustannuserittelylle osoittaa, että kustannusryhmän segmentointi säilytetään usealla tasolla standardikustannuslaskelmissa. Toisaalta taas jos käytännöllä ei ole tasoja, kustannusryhmän segmentointi koskee vain yhden tason laskelmia. Esimerkiksi **Kustannusten koonti kustannusryhmien mukaan** -sivulla standardikustannusnimikkeiden kustannusryhmän segmentointi esitetään usealla eri tasolla. 

Kustannusryhmien segmentointi voi koskea myös standardikustannusnimikkeen variansseja. Toinen varastoparametri määrittää, tunnistetaanko varianssit kustannusryhmän mukaan vai esitetäänkö ne pelkkänä yhteenvetona. 

Kustannusryhmälle voi määrittää kustannusryhmän tyypin sekä käyttäytymisen lisäsegmentointia varten.

-   **Kustannusryhmän tyyppi** − Kullekin kustannusryhmälle täytyy määrittää kustannusryhmätyyppi, joka osoittaa, että se koskee suoraa materiaalia, suoraa valmistusta tai suoraa ulkoistusta, tai se täytyy määrittää epäsuoraksi tai määrittämättömäksi. Suoraksi materiaaliksi määritetyn kustannusryhmän voi liittää nimikkeisiin. Suoran tuotannon kustannusryhmän voi liittää kustannusluokkiin. Suoran ulkoistuksen kustannusryhmän voi määrittää palvelun tuotetyypille niin, että voit luokitella palvelun ostamiseen liittyvät kulut alihankinnaksi. Välillisten kustannusten ryhmän voi määrittää lisämaksujen tai osuuksien välillisille kustannuksille. Määrittelemättömäksi osoitetun kustannusryhmän voi määrittää nimikkeille, kustannusluokille tai välillisille kustannuksille. Kustannusryhmätyypin määrittäminen palvelee useita tarkoituksia. Se rajoittaa ensinnäkin kustannusryhmän määrittämistä ja sovellettavien kustannusryhmien luettelon tarkastelemista. Toinen sisältää lisäsegmentointia raportointia varten. Kolmanneksi sitä voidaan käyttää kirjanpitotilien määrittämiseksi variansseille.
-   **Toiminta** − Kullekin kustannusryhmälle voi tarvittaessa määrittää toiminnan. Se määrittää, että kustannusryhmä koskee kiinteitä tai muuttuvia kustannuksia. Kustannusryhmää, jolla ei ole käyttäytymisarvoa, käsitellään muuttuvana kustannuksena. Toiminnan määritystä käytetään vain raportoinnissa. Kustannukset voidaan esittää esimerkiksi kustannuslaskentalomakkeella segmentoituina kiinteiksi ja muuttuviksi kustannuksiksi sekä **Kustannusten koonti kustannusryhmien mukaan** -sivulla. Jos määrität kullekin kustannusryhmälle tuottovaatimusprosentin, tuoterakennelaskenta tarjoaa ehdotetun myyntihinnan hinta+hinnankorotus-mallin perusteella.




