---
title: "Näytä tapahtumat ja kirjauskansiomerkinnät"
description: "Tässä artikkelissa esitellään kirjauskansiovientien ja -tapahtumien eri tarkastelutavat."
author: RobinARH
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: a6848ea9c05536ac18a038b1864c9ccb9408964c
ms.lasthandoff: 03/31/2017


---

# <a name="view-journal-entries-and-transactions"></a>Näytä tapahtumat ja kirjauskansiomerkinnät

Tässä artikkelissa esitellään kirjauskansiovientien ja -tapahtumien eri tarkastelutavat. 

Käyttäjillä, jotka haluavat tarkastella kirjauskansioita ja tapahtumia, on monta eri tapaa tarkastella tietoja. He voivat hyödyntää kyselysivuja, joissa on perehtymismahdollisuus tai he voivat käyttää kirjanpidon eri raporttivaihtoehtoja.

## <a name="voucher-transactions"></a>Tositetapahtumat
**Tositetapahtumat** on kysely-sivu, jossa voit valita eri tauluista ja kentistä kriteerit etsimäsi saldon tai tapahtuman valitsemiseksi. Esimerkiksi voit tarkastella kaikkia tietyn päivän tai tilin tapahtumia, tai kaikkia tapahtumia **Käyttöjärjestelmä**-tyypissä, jotka ovat tietyssä kirjanpitotasossa. Oletusarvon mukaan sivulla näkyy kirjauskansionumero, tosite, päivämäärä ja päätili, mutta voit lisätä muita tauluja, kenttiä ja kriteerejä tarkentaakesi hakua.

## <a name="audit-trail"></a>Kirjausketju
**Kirjausketju** on kysely-sivu, jossa näkyvät tapahtumatyypit, kuvaukset, kenen luomia tapahtumat ovet ja milloin ne on luotu. **Kirjausketju** -kyselyn sivulla voit tarkastella tositetapahtumia.

## <a name="financial-reports"></a>Talousraportit
Voit myös selata ja analysoida kirjanpitotapahtumia suorittamalla tilinpäätökset. Koska tilinpäätöksien rakenne voi perustua tileihin, dimensioihin, tililuokkiin tai näiden kolmen yhdistelmään, voit tarkastella tapahtumia siirtymällä eri tavoin. Jos tarvitset lisätietoja kirjanpitoa varten, voit sisällyttää myös useita tapahtuman ominaisuuksia raportin suunnittelun yhteydessä. Lisäksi voit halutessasi tarkastella tapahtumia, jotka muodostavat yleisen kirjanpitosaldon, voit tutkia tilitapahtumia, aivan samoin kuin voit **pääkirjan** luettelosivulta.

## <a name="ledger-reports"></a>Kirjanpitoraportit
Talousraporttien lisäksi voit käyttää seuraavia kirjanpitoraportteja tarkastellaksesi kirjanpidon tapahtumia:

-   **Dimension laskelma** – Tässä raportissa näkyy tapahtumat tilin ja päivän mukaan ja on myös mahdollista näyttää ne ajan ja dimension mukaan.
-   **Kirjanpidon tapahtumaluettelo** – Tämä raportti näyttää tapahtumat tapahtumissa, kirjanpidossa ja tilivaluutan raportoinnin.
-   **Tulosta kirjauskansio** – Tämä raportti esittää kirjatun kirjauskansion tuloksen. Voit suorittaa raportin kirjauskansion eränumeron tai tyypin mukaan, tai lisätä lisäkenttiä.
-   **Kirjatut tapahtumat kirjauskansioittain** -Tässä raportissa näkyvät tapahtumat, jotka on kirjattu kirjauskansioon, tositteen mukaan.
-   **Tapahtumaluettelo päivämäärittäin** – Tämä raportti näyttää kaikki tapahtumat päivämäärittäin, kirjauskansion numeron, tositteen ja kirjanpitotilin kanssa. Se näyttää lisäksi tapahtumat tapahtuman, kirjanpidon ja raportoinnin valuuttana.
-   **Tapahtumalähde** – Tämä tapahtumaraportti näyttää tilin kirjanpidon, tapahtuman ja raportoinnin tilivaluutan. Siinä näkyy myös kirjauskansion jokainen rivi, jota on käytetty osoitteeksi.


Lisätietoja on kohdissa [Kirjanpitotilin saldot](general-ledger-account-balances.md), [Kirjanpitolähteen hallinta](\financials\accounts-payable\accounting-source-explorer) ja [Talousraportointi](financial-reporting-getting-started.md)


