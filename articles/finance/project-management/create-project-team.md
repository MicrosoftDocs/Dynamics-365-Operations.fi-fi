---
title: Projektiryhmän luominen
description: Tämä ohjeaihe sisältää projektin ryhmien luomista ja hallintaa käsitteleviä tietoja.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760534"
---
# <a name="create-a-project-team"></a>Projektiryhmän luominen

[!include [banner](../includes/banner.md)]

Projektipäällikön täytyy liittää projektin yhteydessä aiemmin määritetyt roolit projektiin, jotta hän voi käyttää niitä. Projektille voidaan määrittää useita rooleja. Nämä roolit nimetään automaattisesti varauksen aikana sekaannusten välttämiseksi. Jos projektipäällikkö tarvitsee esimerkiksi kolme ohjelmistosuunnittelijaa, luodaan automaattisesti kolme ohjelmistosuunnittelijan roolia, joiden nimikkeinä on **ohjelmistosuunnittelija 1**, **ohjelmistosuunnittelija 2** ja **ohjelmistosuunnittelija 3**. Jos roolille on määritetty ominaisuudet jo aiemmin, niitä käytetään suodattimina resurssia haettaessa. Hakua voi tarkentaa lisäämällä muitakin ominaisuuksia tarpeen mukaan.

Myös näyttöasetukset voidaan mukauttaa, jotta resurssien käytettävyys saadaan paremmin näkyviin. Näyttöperusteeksi voi valita käytettävyyden tunnin, päivän, viikon, kuukauden, vuosineljänneksen tai vuoden perusteella. Myös resurssien käytettävissä ja jäljellä olevan kapasiteetin voi suodattaa näkyviin. Tämä vaihtoehto on hyödyllinen ajanhallinnassa, kun arvioit tehtäviin käytettävissä olevaa aikaa tai resurssien käytettävyyttä.

Projektipäällikkö voi valita sivulta haluamansa roolin. Jos vaatimuksia vastaava resurssi on käytettävissä, projektipäällikkö voi valintansa mukaan varata resurssin rooliin. Huomaa, että resursseja ei tarvitse varata tässä suunnitteluvaiheessa. Työrakennetta luodessasi voit korvata roolit projektin henkilöstöllisillä resursseilla. Jos roolit korvataan työrakenteessa henkilöstöllisillä resursseilla, resurssiasetukset päivittävät projektiryhmän luettelon ja aikataulun automaattisesti.

[![Projektiryhmän luettelo, joka sisältää sekä roolit todellinen resurssit](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektipäällikkö voi varata resurssin projektiin eri tavoilla, esimerkiksi valitsemalla **Jäljellä oleva kapasiteetti**, **Koko kapasiteetti**, **Kapasiteettiprosentti** ja **Määritä tunnit**. Nämä varausasetukset voi peruuttaa milloin tahansa, jos resurssimääritykset muuttuvat. Kahta varaustyyppiä tuetaan:

- **Kiinteä varaus** – Resurssivaraus on hyväksytty ja resurssin työskentely sitoumuksessa on vahvistettu tietyksi ajaksi.
- **Alustava varaus** – Resurssivaraus on alustavasti määritetty työskentelemään sitoumuksessa tietyllä ajalla.

Seuraavissa vaiheissa on selostettu, miten projektiryhmä luodaan.

## <a name="create-a-project-team"></a>Projektiryhmän luominen

1. Valitse **Kaikki projektit** -luettelosivulta haluamasi projekti ja valitse sitten **Muokkaa**.
2. Syötä **Projektiryhmän ja ajoitus** -välilehdessä **Ajoita päättymispäivä** -kenttään aikataulun alkamispäivä plus yksi kuukausi. Jos aikataulun alkamispäivä on esimerkiksi 24. kesäkuuta 2017 (24/06/2017), syötä **24/07/2017**.
3. Valitse **Lisää**.
4. Valitse **Lisää roolit projektiin** -ruudun **Rooli**-kentästä **Vastaava projektipäällikkö**.
5. Valitse **Vaaditut osaamisalueet**.
6. Aiemmin vastaavan projektipäällikön roolille määrittämäsi ominaisuudet tulevat oletusarvoisesti valituiksi **Valitse ominaisuudet** -sivulla. Valitse **OK**.
7. Syötä **Lisää roolit projektiin** -sivulla **Resurssien määrä** -kenttään arvoksi **1**.
8. Hakutoiminto näyttää **Resurssi**-kentässä kaikki resurssit, joilla on tarvittavat osaamistiedot. Valitse **Daniel Goldschmidt** ja sitten **Luo**.
9. Valitse **Projekti**-sivulla **Lisää**.
10. Valitse **Lisää roolit projektiin** -ruudun **Rooli**-kentästä **Ryhmän jäsen**. Syötä **Resurssien määrä** -kenttään arvoksi **5**.
11. Valitse **Luo**.
12. Valitse **Projektit**-sivulla **Toteuta resurssi**.

## <a name="monitor-project-teams"></a>Projektiryhmien seuranta
1. Valitse **Kaikki projektit** -sivulla **XYZ-päivitysvaihe 2** -projektin **Projektitunnus**-linkki.
2. Tarkista **Projektiryhmä ja ajoitus** -pikavälilehdessä, että luettelossa näkyvät projektiresurssit ovat oikein.
