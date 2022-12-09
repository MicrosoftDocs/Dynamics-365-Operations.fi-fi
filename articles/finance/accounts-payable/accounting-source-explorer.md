---
title: Kirjanpitolähteen hallinta
description: Tässä artikkelissa on tietoja kirjanpitolähteen hallintasivusta, jota voidaan käyttää kirjanpidon kirjauksien lähdetietojen yksityiskohtaisessa analyysissä.
author: RyanCCarlson2
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: kfend
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd5580dc0be37ec89e6c7934b47c7d5593d8716
ms.sourcegitcommit: 5f8f042f3f7c3aee1a7303652ea66e40d34216e3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806430"
---
# <a name="accounting-source-explorer"></a>Kirjanpitolähteen hallinta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja **kirjanpitolähteen hallintasivusta**, jota voidaan käyttää kirjanpidon kirjauksien lähdetietojen yksityiskohtaisessa analyysissä.

**Kirjanpitolähteen hallinta** on uusi sivu, joka näyttää lähdetiedot. Voit käyttää sitä joko erillisenä työkaluna tai analysoida kirjanpidon kirjauksien tietoja. Sivun avulla voit esimerkiksi saada kaikkein yksityiskohtaisimmat lähdetiedot kirjausketjun saldolle tai tositetapahtumalle. Voit sitten käyttää **Vie MS Exceliin** -toimintoa, jotta voit tutkia tietoja lisää Microsoft Excelissä (esimerkiksi pivot-taulukossa tai pivot-taulukkoraportissa).

**Kirjanpitolähteen hallinta** -sivu näyttää aina saman kokonaissumman jokaiselle kirjanpitotilille kuin yleisessä kirjanpidossa näkyy (esimerkiksi pääkirjassa). Kuten pääkirjassa, voit näyttää segmenttejä eri sarakkeissa. Valitse vain haluamasi taloushallinnon dimensiojoukko. 

Parametrien avulla voit määrittää päivämäärävälin analyysia varten. Tämä toiminto muistuttaa myös pääkirjan toimintoja.

Kaikille asiakirjoille, jotka käyttävät lähdetiedoston kehystä, **kirjanpidon lähdehallinta** -sivu näyttää lisätiedot, jotka perustuvat kirjanpidollisiin jakoihin ja, jos mahdollista, projektin kirjanpidollisiin jakoihin. Nämä tiedot sisältävät **rahasumman tyypin**, **projektin**, **tehtävän**, **luokan** ja **rivin ominaisuuden** arvot. Seuraavassa on esimerkkejä analyysistä, jonka voit tehdä:

- Ostotilauksien ja toimittajalaskujen väliset varianssit, koska rahasumma tyyppi, esimerkiksi kulujen varianssia, edustaa kutakin varianssia
- Laskutettavat ja ei-laskutettavat tunnit ja kulut projektissa, liiketoimintayksikössä ja päätilissä

Niille lähdeasiakirjoille, jotka käyttävät lähdeasiakirjojen viitteen käyttäjätietojen käsitettä, **kirjanpidon lähdehallinta** -sivu näyttää vielä enemmän tietoja, kuten **asiakkaan**, **toimittajan**, **työntekijän**, **tuotteen**, **määrän**, **yksikkötekstin** ja **kuvauksen** arvot. Seuraavassa on esimerkkejä analyysistä, jonka voit tehdä:

- Hotellikulut kunkin yrityksen yksikölle ja tilikauden hotellimerkki, kuluraporttien mukaan
- Toimittajan, tuotemallin ja osaston mukaiset alennukset

Nämä tiedostot voit löytää myös todellisesta asiakirjan lähteestä **kirjanpidon lähdehallinta** -sivulta.

> [!NOTE]
> Versiosta 10.0.31 lähtien uusi **kirjanpidon lähdehallinnan edistynyt suodattaminen** -ominaisuus on käytettävissä Toimintojen hallinnassa. Tämä ominaisuus korvaa **Päivitä**-painikkeen, joka tarjoaa kehittyneen ja aiempaa vakaamman kyselykokemuksen. Se muistuttaa kokemusta, joka on käytössä **Tositetapahtumat**-sivulla. Kehittynyt suodatin sallii suodattamisen eri kenttien mukaan. Kentät vastaavat **Tositetapahtumien kysely** -sivun kenttiä kuten **Kirjanpitotili**, **Liiketoimintayksikkö**, **Kustannuspaikka** ja **Osasto**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
