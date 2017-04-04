---
title: "Pankin tiliotteen ja maksun täsmäytyksen yleistä EU: N"
description: "Tässä aiheessa on yleiskatsaus toimintoja, joiden avulla voit täsmäyttää maksutiedot pankeilta, joita käytetään eri Euroopan maissa."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankAccountTable, CustPaymMode, VendPaymMode
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267994
ms.assetid: 2bfb8ecc-e850-43cb-9a96-deb11716a391
ms.search.region: Belgium, Norway, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 22d93d7b3618d4f5931c6a7e39d681173734b0b9
ms.lasthandoff: 03/31/2017


---

# <a name="bank-statement-and-payment-reconciliation-overview-for-the-eu"></a>Pankin tiliotteen ja maksun täsmäytyksen yleistä EU: N

Tässä aiheessa on yleiskatsaus toimintoja, joiden avulla voit täsmäyttää maksutiedot pankeilta, joita käytetään eri Euroopan maissa.

Microsoft Dynamics-365 toimintoja varten voit tuoda tapahtumia pankkien ja olemassa olevien tapahtumien vastaan nämä tapahtumat selvitetään. Euroopassa voit tehdä tämän seuraavissa tapauksissa:

-   Tiliotteet tuodaan.
-   Maksuja tuodaan.
-   Palauta tiedostot tuodaan.

## <a name="bank-statements"></a>Tiliotteet
A *tiliotteen* tai *tilin tiliotteen* on yhteenveto Rahoitustaloustoimia, jotka ovat tapahtuneet rahoituslaitoksen yrityksen pankkitilille tiettynä ajanjaksona. Voit tuoda Dynamics 365 työvaiheiden pankin tiliotteen. On tärkeää olemassa olevien tapahtumien kanssa tuodut tapahtumat selvitetään sekä tarkistaa pankkitilien saldo avaaminen ja päättyy. Seuraavassa luettelossa on Euroopan tuetut tiedostomuodot.

-   Kokeneet pankin täsmäytys Euroopan tiedostomuotoja. Lisätietoja on ohjeaiheessa [Advanced yhteenveto pankkitilin täsmäytyksen](../cash-bank-management/advanced-bank-reconciliation-overview.md).
-   ISO 20022 camt.053 pankin tiliotteen tiedostomuotoa
-   CODA-pankkitilin tiliotteen tiedostomuoto. Lisätietoja on ohjeaiheessa [CODA-tiliote](emea-bel-coda-bank-statement-import.md).

## <a name="customer-and-vendor-payments-import-and-return-messages"></a>Asiakkaan ja toimittajan maksujen tuominen ja palauttaa viestit
Pankin tiliote, lisäksi pankit voivat antaa viestejä, jotka sisältävät tietoja asiakkaiden ja toimittajien maksuille, jotka voidaan tuoda Dynamics 365 operaatioille ja täsmäytetty asiakkaan ja toimittajan tapahtumien kanssa. Kun yritys haluaa vastaanottaa saapuvia maksuja asiakastapahtumien tietoja pankin, tuo muotoja voidaan käyttää. Suoraveloitus ja -tilisiirrolla käyttävät yritykset maksulaitoksen voi vastaanottaa maksuja, jotka on aikaisemmin viety tilan päivittäminen. Tuo muodot ja palautustilausten muodot välinen ero on se, että palauttaa on kohdistettu lähinnä päivittää jo luonut maksukirjauskansion rivit (ne luodaan automaattisesti, kun suora veloitus- tai hyvitystyyppi siirto tehtiin) sen sijaan, että uusia rivejä. Palautuksen tilanteissa voi myös sisältää monimutkaisia tuo joitakin muotoiluja. Seuraavassa esimerkissä näytetään, kuinka tämä jako olisi pantava täytäntöön.

##### <a name="import-formats"></a>Tuo muodot

-   ISO 20022-camt.054 pankki-ilmoitus
-   [Verkot tuo muoto](emea-nor-nets-import-format.md) -Norja maksumuotojen monimutkaisia-ominaisuus
-   Tuo asiakasmaksut ESR
-   Tuo maksumuotojen Ruotsi - BankGirot Max ja BankGirot-OCR-muodot

##### <a name="return-formats"></a>Palauta muoto

-   ISO 20022-pain.002 maksun tila-raportti
-   (DNK) BetalingsserviceBasis-returformat – asiakkaan Betalingsservice vientimuoto Palauta muoto
-   [Tuo maksumuotojen Ruotsi](emea-swe-payment-formats-import.md) -Bankgirot Autogiro palauttaa
-   (SWE) BankGirot Palauta – Palauta toimittajamaksujen muodossa, joka vastaa Bankgirot-vientimuotoa

