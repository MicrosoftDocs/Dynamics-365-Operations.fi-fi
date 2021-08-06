---
title: Kirjanpitolähteen hallinta
description: Tässä artikkelissa on tietoja kirjanpitolähteen hallinnasta, jota voidaan käyttää kirjanpidon kirjauksien lähdetietojen yksityiskohtaisessa analyysissä.
author: rcarlson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: roschlom
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1ab7cb7f8f9a42d5f311f8760ff2463055dc178
ms.sourcegitcommit: f2dfec2f4c427e37a574e6acdfaaf150bc92ebb6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/23/2021
ms.locfileid: "6661034"
---
# <a name="accounting-source-explorer"></a>Kirjanpitolähteen hallinta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja kirjanpitolähteen hallinnasta, jota voidaan käyttää kirjanpidon kirjauksien lähdetietojen yksityiskohtaisessa analyysissä.

"Accounting source explorer" on uusi sivu, joka näyttää lähdetiedot. Voit käyttää kirjanpidon lähdehallintaa joko erillisenä työkaluna tai analysoida kirjanpidon kirjauksien tietoja. Kirjanpidon lähdehallinnan avulla voit esimerkiksi saada kaikkein yksityiskohtaisimmat lähdetiedot kirjausketjun saldolle tai tositetapahtumalle. Voit sitten käyttää Export to MS Excel -toimintoa, jotta voit tutkia tietoja lisää Microsoft Excelissä (esimerkiksi pivot-taulukossa tai pivot-taulukkoraportissa).

Accounting source explorer näyttää aina saman kokonaissumman jokaiselle kirjanpitotilille kuin yleisessä kirjanpidossa näkyy (esimerkiksi pääkirjassa). Kuten pääkirjassa, voit näyttää segmenttejä eri sarakkeissa. Valitse vain haluamasi taloushallinnon dimensiojoukko. 

Parametrien avulla voit määrittää päivämäärävälin analyysia varten. Tämä toiminto muistuttaa myös pääkirjan toimintoja.

Kaikille asiakirjoille, jotka käyttävät lähdetiedoston kehystä, kirjanpidon lähdehallinta näyttää lisätiedot, jotka perustuvat kirjanpidollisiin jakoihin ja, jos mahdollista, projektin kirjanpidollisiin jakoihin. Nämä tiedot sisältävät rahasumman tyypin, projektin, tehtävän, luokan ja rivin ominaisuuden. Seuraavassa on esimerkkejä analyysistä, jonka voit tehdä:

-   Ostotilauksien ja toimittajalaskujen väliset varianssit, koska rahasumma tyyppi, esimerkiksi kulujen varianssia, edustaa kutakin varianssia
-   Laskutettavat ja ei-laskutettavat tunnit ja kulut projektissa, liiketoimintayksikössä ja päätilissä

Niille lähdeasiakirjoille, jotka käyttävät lähdeasiakirjojen viitteen käyttäjätietojen käsitettä, "Accounting source explorer" näyttää vielä enemmän tietoja, kuten asiakas, toimittaja, työntekijä, tuote, määrä, yksikkö teksti sekä kuvaukset. Seuraavassa on esimerkkejä analyysistä, jonka voit tehdä:

-   Hotellikulut kunkin yrityksen yksikölle ja tilikauden hotellimerkki, kuluraporttien mukaan
-   Toimittajan, tuotemallin ja osaston mukaiset alennukset

Nämä tiedostot voit löytää myös todellisesta asiakirjan lähteestä "Accounting source explorerista".

> [!NOTE]
> Versiosta 10.0.20 **päivitys** painikkeella on kaksi lisäväliä, jotka rajoittavat tietojen syöttämisen aloituskyselyä sivulla. Nämä lisävälit ovat käytettävissä myös versiossa 10.0.19 palvelupäivityksenä. Lisättiin seuraavat kentät:
>
> - Tositteesta, Tositteeseen
> - Päätilistä, Päätiliin

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
