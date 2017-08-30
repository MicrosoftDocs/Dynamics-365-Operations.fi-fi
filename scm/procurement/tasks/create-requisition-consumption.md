--- 
title: Luo kulutusehdotus
description: "Tässä menettelyssä käsitellään yksityiskohtaisesti ehdotuksen luontiprosessi."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8eb4cd47104e2df1c973e5e508c1da02617b9a1d
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-requisition-for-consumption"></a>Luo kulutusehdotus

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään yksityiskohtaisesti ehdotuksen luontiprosessi. Siinä näytetään erilaisia tapoja hakea tuotteiden hankintaluettelon tuotteita sekä millä tavoin lisätään tuote, jota ei ole luettelossa. Varmista ennen menettelyn aloittamista, että ostokäytäntö on määritetty siten, että ehdotuksen oletustyyppi on Kulutus. Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi. Menettelyn voi suorittaa vain käyttäjäprofiili, joka on määritetty työntekijäksi.  Työntekijä suorittaa yleensä tämän tehtävän. Työntekijän käyttöoikeusroolin ansiosta voit suorittaa tehtävät. Jos käytössä on USMF, voit kirjautua sisään tunnuksella Alicia.


## <a name="create-a-new-requisition"></a>Luo uusi ehdotus
1. Valitse Hankinta > Ostoehdotukset > Itse luodut ostoehdotukset.
2. Valitse Uusi.
3. Kirjoita Nimi-kenttään ehdotuksen nimi.
4. Kirjoita päivämäärä Vaadittu päivämäärä -kenttään.
    * Pyyntöpäivämäärä ja kirjauspäivä kopioidaan oletusarvoisesti ostoehdotusriveille. Niitä voidaan muuttaa rivitasolla. Pyydetty päivämäärä on pyydetty toimituspäivämäärä.  
5. Kirjoita päivämäärä Kirjauspäivä-kenttään.
    * Kirjauspäivämäärää käytetään tiliviennin kirjaamiseen kirjanpitoon ja vahvistamaan, onko budjettirahoitus käytettävissä.  
6. Valitse OK.
7. Avaa haku napsauttamalla Syy-kentässä avattavan valikon painiketta.
    * Oletusarvon mukaan liiketoimintaperusteet, jotka olet valinnut, ilmestyvät ostoehdotusriveille, mutta voit muuttaa niitä rivitasolla.    
8. Etsi haluamasi tietue luettelosta ja valitse se.
9. Valitse syy
10. Kirjoita tietokenttään ehdotuksen peruste

## <a name="add-a-line-to-the-requisition"></a>Lisää rivi ehdotukseen
1. Valitse Lisää rivi.
    * Ostoehdotukseen voi lisätä rivejä kahdella tavalla. Jos tiedät tuotenumeron tai tiedät, ettei pyytämäsi tuotetta ole tuoteluettelossa, voit lisätä rivin suoraan valitsemalla Lisää rivi. Vaihtoehtoisesti voit Lisää tuotteet -asetusta, jota voi käyttää nimikkeiden etsimiseen ja suodattamiseen tuoteluettelossa.    
2. Napsauta juuri luotua riviä.
    * Pyynnön lähettäjä on työntekijä, joka on pyytänyt ehdotusta.   
    * Oletusarvoisesti työntekijä, joka on pyytänyt varasto-ottoehdotuksen, valmistelee sen. Varasto-ottoehdotusrivin valmisteluun toisen työntekijän puolesta tarvitaan lupa. Jos sinulla on tämä käyttöoikeus, toiset työntekijät näkyvät tässä haussa.  
3. Kirjoita arvo Nimiketunnus-kenttään.
    * Ostavan yrityksen luokan käyttöoikeuskäytäntö ja tuotteiden hankintaluettelo rajoittavat, mitä vaihtoehtoja sinulla on käytettävissä.   
4. Kirjoita numero Määrä-kenttään.

## <a name="add-more-products-to-the-requisition"></a>Lisää muita tuotteita ehdotukseen
1. Valitse Lisää tuotteet.
    * Voit hakea tällä asetuksella tuoteluettelon tuotteita.    
2. Kirjoita Etsi hankintaluokan noodi -kenttään etsittävästä luokan nimen alkuosa ja paina sitten Enter-näppäintä.
    * Kirjoita esimerkiksi tiet.  
3. Käytä InvokeDefaultButton-pikavalintaa.
4. Voit suodattaa valitun luokan tuoteluetteloa suodattimella.
5. Valitse ehdotukseen lisättävä tuotekortti.
6. Valitse Lisää riveihin.
7. Syötä Määrä-kenttään numero.
8. Kirjoita Etsi hankintaluokan noodi -kenttään etsittävästä luokan nimen alkuosa ja paina sitten Enter-näppäintä.
    * Kirjoita esimerkiksi alle (alleviivauskynät).  
9. Käytä InvokeDefaultButton-pikavalintaa.
10. Lisää tuote, joka ei ole tuotteiden hankintaluettelossa, valitsemalla Lisää listaamaton tuote riveille.
11. Kirjoita arvo Tuotteen nimi -kenttään.
12. Kirjoita arvo Yksikkö-kenttään.
13. Valitse OK.
14. Lisää tuotekuvaus Nimikkeen kuvaus -kenttään.
15. Kirjoita numero Määrä-kenttään.
16. Syötä Yksikköhinta-kenttään numero.
    * Jos tiedät tietyn (toimittajan tilikentässä valitun) toimittajan hinta, kyseinen hinta voidaan ilmoittaa   
17. Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.
    * Tästä kentästä valittavat vaihtoehdot määräytyvät hankintakäytäntöjen ja toimittajan nykyisen hankintaluokan tilan mukaan. Sen sijaan että toimittaja valittaisiin tässä, voit napsauttaa toimittajan ehdotuspainiketta.    
18. Valitse luettelosta toimittaja, jota haluat käyttää.
19. Kirjoita Ulkoinen nimiketunnus -kenttään arvo.
    * Tämä on tuotteen viitenumero, jonka toimittaja tietää. Se voi olla esimerkiksi tuotteen nimiketunnus toimittajan omassa luettelossa.  
20. Valitse OK.

## <a name="distribute-amounts"></a>Jaa summat
1. Valitse Myyntitiedot.
2. Valitse Jaa summat.
    * Tämä prosessi osoittaa, miten ensimmäisen rivin kustannus jaetaan kahden tilin välillä. Se voidaan tehdä myös myöhemmin, kun varasto-ottoehdotusta arvioidaan.  
3. Luo uusi jakorivi valitsemalla Jako.
4. Valitse Kirjanpitotili-kentässä ensimmäinen kustannuspaikka, johon osa kustannuksesta siirretään.
5. Valitse toinen jakorivi.
6. Määritä toinen kustannuspaikka Kirjanpitotili-kenttään.
7. Valitse Jaa tasaisesti.
8. Sulje sivu.

## <a name="view-line-details"></a>Näytä rivin tiedot
1. Ota käyttöön Rivitiedot-osan laajennus.

## <a name="submit-the-requisition"></a>Lähetä ehdotus
1. Avaa valintaikkuna valitsemalla Työnkulku.
2. Valitse Lähetä.
3. Sulje sivu.
4. Kirjoita ehdotuksen hyväksyjälle huomautus Kommentti-kenttään.
5. Valitse Lähetä.
6. Sulje sivu.
7. Päivitä sivu.

