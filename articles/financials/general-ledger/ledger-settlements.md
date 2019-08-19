---
title: Tapahtuman selvitykset
description: Tässä ohjeaiheessa käsitellään tapaa, jolla Tapahtuman selvitykset -sivun avulla selvitetään kirjanpitotapahtumia ja tehdään käänteisiä tilityksiä.
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 01764db27eb7061deeddc01997f16a43f9cb00c6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846820"
---
# <a name="ledger-settlements"></a>Tapahtuman selvitykset

[!include [banner](../includes/banner.md)]

Tapahtuman selvitysten avulla täsmäyttää debet- ja kredit-tapahtumat kirjanpidossa ja merkitä ne selvitetyiksi. Tällä tavoin voit varmistaa, että liittyvät tapahtumat on selvitetty. Voit tehdä tarvittaessa myös käänteisiä tilityksiä.

## <a name="enable-advanced-ledger-settlements"></a>Tapahtuman selvitysten lisäasetusten ottaminen käyttöön

Tapahtuman selvitysten lisäasetussivulla on lisää tapahtumien suodatus- ja valintatoimintoja. Ota tapahtuman selvitysten lisäasetussivu käyttöön seuraavien ohjeiden mukaisesti.

1. Valitse **Kirjanpito** \> **Kirjanpidon asetukset** \> **Kirjanpitoparametrit**. 
2. Ota tapahtuman selvityksen lisäasetustoiminto käyttöön valitsemalla **Tapahtuman selvitykset** -välilehdessä **Tapahtuman selvityksen lisäasetukset** -asetukseksi **Kyllä**. **Tapahtuman selvityksen lisäasetukset** -sivua käytetään, kun valitset **Tapahtuman selvitykset** **Kausittaiset tehtävät** -kohdassa. 
3. Jokaiselle tilikartalle on annettava tililuettelo, jota käytetään tapahtuman selvityksissä. Tämän luettelon avulla voi suodattaa **Tapahtuman selvitykset** -sivulla näkyvää tapahtumaluetteloa. Valitse ensin **Tilikartta**-luettelossa tilikartta ja lisää sitten uudet tilit luetteloon valitsemalla **Uusi**.

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a>Tapahtumien selvittäminen tapahtuman selvitysten lisäasetussivulla

Voit selvittää kirjanpitotapahtumia seuraavien ohjeiden avulla.

1. Valitse **Kirjanpito** \> **Kausittaiset tehtävät** \> **Tapahtuman selvitykset**.
2. Määritä sivun yläosassa olevat suodattimet:

    - Valitse päivämääräalue tai täytä päivämääräalue automaattisesti valitsemalla **Päivämäärävälin koodi**.
    - Muuta kirjanpitotasoa tarpeen mukaan.
    - Jos haluat näyttää kirjanpitotiliin ja dimensiot erikseen, valitse taloushallinnon dimensioyhdistelmä

3. Valitse **Näytä tapahtumat**, jos haluat näyttää kaikki määritettyjä suodattimia vastaavat tapahtumat ja tililuettelon, jonka määritit, kun määritit tilikarttaluettelon edellisessä osassa. Jos muutat suodattimia tai dimensioyhdistelmiä, sinun on valittava uudelleen **Näytä tapahtumat**.
4. Valitse vähintään yksi rivi, jonka selvittämistä harkitset. Sivun yläosassa olevan **Valittu summa** -kentän arvo suurenee tai pienenee valittujen rivien kokonaissumman mukaan.
5. Kun olet valinnut tapahtumat, valitse **Merkitse valitut**. Kunkin valitun tapahtuman **Merkitty**-sarakkeeseen tulee valintamerkki. Lisäksi ruudukon yläpuolella olevan **Merkitty summa** -kentän arvo suurenee tai pienenee merkittyjen rivien kokonaissumman mukaan.
6. Kun **Merkitty summa** -arvo on **0** (nolla), valitse **Suorita merkityt tapahtumat**. Merkittyjen tapahtumien tilaksi päivitetään **Selvitetty**.

## <a name="make-transactions-easier-to-find"></a>Tapahtumien löytämisen helpottaminen

**Tapahtuman selvitykset** -sivulla on toimintoja, jotka helpottavat selvitettävän tapahtuman näkemistä.

- **Poista valinta** -painike poistaa valintamerkin kaikkien valittujen rivien **Merkitty**-kentästä.
- **Merkitty**-suodattimella voi suodataa tapahtumia sen perusteella, onko tapahtumien **Merkitty**-kenttä valittu vai valinta tyhjennetty.
- **Tila**-suodattimella voi suodattaa tapahtumia sen perusteella, onko tapahtuman tila **Selvitetty** vai **Selvittämätön**.
- **Järjestä absoluuttisen summan mukaan** -painikkeella summat voi lajitella absoluuttisen arvon mukaan, joten voit ryhmittää yhteen debetit ja kreditit, joilla on sama summa.

## <a name="reverse-a-settlement"></a>Käänteinen tilitys

Voit tehdä tarvittaessa käänteisen tilityksen.

1. Tuo etsimäsi tapahtumat näkyviin suorittamalla kohdan Tapahtumien selvittäminen tapahtuman selvitysten lisäasetussivulla vaiheet 1–3.
2. Valitse **Tila**-suodattimessa **Selvitetty**.
3. Valitse vähintään yksi rivi, jonka käänteistä tilitystä harkitset. Sivun yläosassa olevan **Valittu summa** -kentän arvo suurenee tai pienenee valittujen rivien kokonaissumman mukaan.
4. Kun olet valinnut tapahtumat, valitse **Merkitse valitut**. Kunkin valitun tapahtuman **Merkitty**-sarakkeeseen tulee valintamerkki. Lisäksi sivun yläosassa olevan **Merkitty summa** -kentän arvo suurenee tai pienenee merkittyjen rivien kokonaissumman mukaan.
5. Kun **Merkitty summa** -arvo on **0** (nolla), valitse **Peru merkityt tapahtumat**. Merkittyjen tapahtumien tilaksi päivitetään **Selvittämätön**.

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a>Tapahtumaluetteloon sisältyvän tililuettelon päivittäminen

Valitse **Tapahtumien selvityksen tilit**. Voit muokata avautuvassa valintaikkunassa tapahtumaluetteloon sisältyviä tilejä. Lisää uudet tilit luetteloon valitsemalla **Uusi**. Tämän luettelon avulla voi suodattaa **Tapahtuman selvitykset** -sivulla näkyvää tapahtumaluetteloa.
