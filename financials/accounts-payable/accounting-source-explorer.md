---
title: "Kirjanpitolähteen hallinta"
description: "Tässä artikkelissa on tietoja kirjanpitolähteen hallinnasta, jota voidaan käyttää kirjanpidon kirjauksien lähdetietojen yksityiskohtaisessa analyysissä."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 8913e61285d5d180883471991b659ddcb260afe3
ms.lasthandoff: 03/31/2017


---

# <a name="accounting-source-explorer"></a>Kirjanpitolähteen hallinta

Tässä artikkelissa on tietoja kirjanpitolähteen hallinnasta, jota voidaan käyttää kirjanpidon kirjauksien lähdetietojen yksityiskohtaisessa analyysissä.

"Accounting source explorer" on uusi sivu, joka näyttää lähdetiedot. Voit käyttää kirjanpidon lähde explorer joko erillisenä työkaluna tai analysoida tietoja kirjanpidon kirjaukset takana. Kirjanpidon lähde explorer avulla voit saada eniten yksityiskohtaiset lähdetiedot tasapainon jäljen tasapainossa tai tapahtuman tosite. Sitten voit käyttää Export to MS Excel -toimintoa, jotta voit tutkia tietoja lisää Microsoft Excelissä (esimerkiksi pivot-taulukossa tai pivot-taulukkoraportissa).

Accounting source explorer näyttää aina saman kokonaissumman jokaiselle kirjanpitotilille kuin yleisessä kirjanpidossa näkyy (esimerkiksi pääkirjassa). Kuten pääkirjassa, voit näyttää segmenttejä eri sarakkeissa. Valitse vain haluamasi taloushallinnon dimensiojoukko. 

Parametrien avulla voit määrittää päivämäärävälin analyysia varten. Tämä toiminto muistuttaa myös pääkirjan toimintoja.

Kaikille asiakirjoille, jotka käyttävät lähde tiedoston kehys, kirjanpidon lähde explorer näyttää lisätiedot perustuvat jaot ja, jos mahdollista, projektin kirjanpidolliset jaot. Nämä tiedot sisältävät rahallisen Summalajin, projektin, tehtävän, luokkaa ja rivin ominaisuus. Seuraavassa on esimerkkejä analyysistä, jonka voit tehdä:

-   Ostotilauksien ja toimittajalaskujen väliset varianssit, koska rahasumma tyyppi, esimerkiksi kulujen varianssia, edustaa kutakin varianssia
-   Laskutettavat ja ei-laskutettavat tunnit ja kulut projektissa, liiketoimintayksikössä ja päätilissä

Niille lähdeasiakirjoille, jotka käyttävät lähdeasiakirjojen viitteen käyttäjätietojen käsitettä, "Accounting source explorer" näyttää vielä enemmän tietoja, kuten asiakas, toimittaja, työntekijä, tuote, määrä, yksikkö teksti sekä kuvaukset. Seuraavassa on esimerkkejä analyysistä, jonka voit tehdä:

-   Hotellikulut kunkin yrityksen yksikölle ja tilikauden hotellimerkki, kuluraporttien mukaan
-   Toimittajan, tuotemallin ja osaston mukaiset alennukset

Nämä tiedostot voit löytää myös todellisesta asiakirjan lähteestä "Accounting source explorerista".


