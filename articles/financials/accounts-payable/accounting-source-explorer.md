---
title: "Kirjanpitolähteen hallinta"
description: "Tässä artikkelissa on tietoja kirjanpitolähteen hallinnasta, jota voidaan käyttää kirjanpidon kirjauksien lähdetietojen yksityiskohtaisessa analyysissä."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: df97cad657164866b83fa0ca8f10091317f92a88
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="accounting-source-explorer"></a>Kirjanpitolähteen hallinta

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on tietoja kirjanpitolähteen hallinnasta, jota voidaan käyttää kirjanpidon kirjauksien lähdetietojen yksityiskohtaisessa analyysissä.

"Accounting source explorer" on uusi sivu, joka näyttää lähdetiedot. Voit käyttää kirjanpidon lähdehallintaa joko erillisenä työkaluna tai analysoida kirjanpidon kirjauksien tietoja. Kirjanpidon lähdehallinnan avulla voit esimerkiksi saada kaikkein yksityiskohtaisimmat lähdetiedot kirjausketjun saldolle tai tositetapahtumalle. Sitten voit käyttää Export to MS Excel -toimintoa, jotta voit tutkia tietoja lisää Microsoft Excelissä (esimerkiksi pivot-taulukossa tai pivot-taulukkoraportissa).

Accounting source explorer näyttää aina saman kokonaissumman jokaiselle kirjanpitotilille kuin yleisessä kirjanpidossa näkyy (esimerkiksi pääkirjassa). Kuten pääkirjassa, voit näyttää segmenttejä eri sarakkeissa. Valitse vain haluamasi taloushallinnon dimensiojoukko. 

Parametrien avulla voit määrittää päivämäärävälin analyysia varten. Tämä toiminto muistuttaa myös pääkirjan toimintoja.

Kaikille asiakirjoille, jotka käyttävät lähdetiedoston kehystä, kirjanpidon lähdehallinta näyttää lisätiedot, jotka perustuvat kirjanpidollisiin jakoihin ja, jos mahdollista, projektin kirjanpidollisiin jakoihin. Nämä tiedot sisältävät rahasumman tyypin, projektin, tehtävän, luokan ja rivin ominaisuuden. Seuraavassa on esimerkkejä analyysistä, jonka voit tehdä:

-   Ostotilauksien ja toimittajalaskujen väliset varianssit, koska rahasumma tyyppi, esimerkiksi kulujen varianssia, edustaa kutakin varianssia
-   Laskutettavat ja ei-laskutettavat tunnit ja kulut projektissa, liiketoimintayksikössä ja päätilissä

Niille lähdeasiakirjoille, jotka käyttävät lähdeasiakirjojen viitteen käyttäjätietojen käsitettä, "Accounting source explorer" näyttää vielä enemmän tietoja, kuten asiakas, toimittaja, työntekijä, tuote, määrä, yksikkö teksti sekä kuvaukset. Seuraavassa on esimerkkejä analyysistä, jonka voit tehdä:

-   Hotellikulut kunkin yrityksen yksikölle ja tilikauden hotellimerkki, kuluraporttien mukaan
-   Toimittajan, tuotemallin ja osaston mukaiset alennukset

Nämä tiedostot voit löytää myös todellisesta asiakirjan lähteestä "Accounting source explorerista".



