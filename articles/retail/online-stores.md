---
title: Verkkokauppa-yleiskatsaus
description: "Tässä artikkelissa on tietoja vähittäismyynnin verkkokaupoista ja niiden määrittämisestä Microsoft Dynamics 365 for Retailista"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 13d7f99766dabf35b80e7100a3017308033e3da6
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="online-store-overview"></a>Verkkokaupan yleiskatsaus

[!include[banner](includes/banner.md)]


Tässä artikkelissa on tietoja vähittäismyynnin verkkokaupoista ja niiden määrittämisestä Microsoft Dynamics 365 for Retailista

Dynamics 365 for Retail tukee useita vähittäismyyntikanavia. Vähittäismyyntikanavia ovat verkkokaupat, puhelinkeskukset ja vähittäismyymälät (eli kivijalkakaupat). Verkkokaupassa vähittäismyyjät saavat näkyvyyttä Internetissä, ja asiakkaat voivat ostaa tuotteita sekä verkkokaupasta että vähittäismyymälästä. Verkkokaupasta tuotteita ostavat asiakkaat voivat saada tuotteet kotiin toimitettuina tai noutaa ne paikallisesta myymälästä. Luot verkkokaupan Dynamics 365 for Retailin asiakasohjelmassa. Verkkokauppa julkaistaan kolmannen osapuolen verkkokaupassa, joka on yhdistetty Dynamics 365 for Retailiin. Kolmannen osapuolen verkkokauppa toimii verkkokauppasi edustana (käyttöliittymänä), ja voit valita haluamasi asiakkuudenhallintajärjestelmän ja käyttöliittymäominaisuudet. Dynamics 365 for Retailissa on käytettävissä useita tämäntyyppisiä integrointivaihtoehtoja. Verkkokaupalle määritetyt ominaisuudet ohjaavat verkkokaupan toimintoja. Esimerkki: Määrittelet siirtymisluokan hierarkian Dynamics 365 for Retailissa ja määrität sen verkkokaupalle. Kun julkaiset verkkokaupan kolmannen osapuolen verkkokaupassa, siirtymisluokan hierarkia näkyy kaupan verkkoversiossa. Ostajat voivat selata verkkokauppaa ja hakea tuotteita siirtymisluokan hierarkian avulla. Jos haluat luoda verkkokaupan, sinun on määritettävä kaupalle komponentit, jotka mahdollistavat tapahtumien käsittelyn. Sinun täytyy lisätä esimerkiksi valikoimat, määritteet, maksutavat ja toimitustavat. Voit määrittää hinnat, kampanjat, alennukset, alennukset, kauppasopimukset ja lähetyksen ehtoja, jotka liittyvät Internet-kauppa. Kun olet julkaissut verkkokauppasi kolmannen osapuolen verkkokaupassa, voit luoda sille vähittäismyynnin tuoteluetteloita. Luettelon tuotteista tulee verkkokaupassa tuoteluetteloita. Kun asiakas ostaa tuotteita verkkokaupasta, saatavilla oleva varasto päivittyy ja synkronoituu asiakasohjelmassa. Lisäksi ostoille luodaan myyntitilaukset ja ne lähetetään asiakasohjelmaan tilauksen toimitusta ja käsittelyä varten.

## <a name="set-up-an-online-store"></a>Perusta online-kauppa
Kun perustat verkkokauppaa, tee seuraavat tehtävät:

1.  Luo verkkokauppa.
2.  Lisää verkkokauppa sopiviin organisaatiohierarkioihin.
3.  Lisää tuotevalikoimat, joihin kuuluvat verkkokaupassa saatavilla olevat tuotteet.
4.  Määritä tai luo hintaryhmät verkkokauppaa varten.
5.  Määritä verkkokaupassa käytettävissä oleva toimitustavat.
6.  Määritä maksutavat, jotka verkkokauppa hyväksyy.
7.  Jos sallit ostajille tuotteiden Internet-tilaukset ja niiden keräyksen paikallisessa myymälässä, määritä verkkokaupalle toimipaikkapaikannin.
8.  Määritä kanavien, tuotteiden ja myyntitilausten määritteet verkkokaupalle. Kanavamääritteet koskevat koko verkkokauppaa, tuotemääritteet koskevat verkkokaupan tuotteita ja myyntitilauksen määritteet koskevat verkkokaupassa luotuja myyntitilauksia.
9.  Yhdistämällä määritteitä voit määritellä ominaisuuksia, jotka ohjaavat sitä, miten kyseiset määritteet toimivat verkkokaupassa. Määritteet voidaan asettaa esimerkiksi pakollisiksi tai haettaviksi.
10. Julkaise verkkokauppa, jotta voit luoda kaupan rakenteen valitsemaasi kolmannen osapuolen verkkokauppaan. **Tärkeää:** Ennen verkkokaupan julkaisemista sille täytyy määrittää jakelusijainti.

## <a name="retail-channel-navigation-hierarchies"></a>Vähittäismyyntikanavan siirtymishierarkiat
Määritä ennen verkkokaupan luomista siinä käytettävä vähittäismyyntikanavan siirtymishierarkia. Vähittäismyyntikanavan siirtymishierarkia vastaa luokkahierarkiaa, joka näytetään verkkokaupassa kaupan julkaisemisen jälkeen. Kun julkaiset vähittäismyynnin tuoteluetteloita verkkokaupassa, luettelon tuotteet yhdistetään vähittäismyyntikanavan siirtymishierarkian luokkiin. Ostajat voivat siirtyä verkkokaupassa hierarkian avulla.

## <a name="organization-hierarchies"></a>Organisaatiohierarkiat
Organisaatiohierarkioita käytetään vähittäismyyntikanavien rakenteiden määrittelyssä. Organisaatiohierarkiat edustavat liiketoimintasi muodostavien organisaatioiden välisiä suhteita. Kun perustat Internet-kauppoja, voit lisätä ne organisaatiohierarkiaan. Myymälät jakavat sitten valikoimissa, täydennyksissä ja raportoinnissa käytettävät tiedot. Luodessaan organisaatiohierarkian sinun on määritettävä sen tarkoitus. Tarkoitus kuvaa, kuinka hierarkiaa käytetään liiketoimintarakenteessa. Voit luoda yhden organisaatiohierarkian myymälän toimintoihin ja käyttää tätä hierarkiaa valikoimiin, täydennykseen ja raportointia varten. Vaihtoehtoisesti voit luoda erillisen organisaatiohierarkian jokaista käyttötarkoitusta varten. Voit myös luoda useita hierarkioita samaan tarkoitukseen ja määrittää jokaiselle erillisen kanavan. Jos aiot julkaista vähittäismyynnin tuoteluetteloita verkkokaupassa, sinun on vähintään lisättävä verkkokauppa organisaatiohierarkiaan valikoimia varten. Luettelon tuotteet valitaan tuotevalikoimista, jotka on määritetty verkkokauppaan. Kun luettelo on julkaistu, julkaisuprosessi vertaa verkkokauppaan liitetyn valikoiman voimassaolopäiviä luettelossa oleviin tuotteisiin selvittääkseen, mitkä tuotteet tulisi antaa saataville verkkokaupassa.




