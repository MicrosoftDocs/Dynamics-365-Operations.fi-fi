---
title: Näytä tapahtumat ja kirjauskansiomerkinnät
description: Tässä artikkelissa esitellään kirjauskansiovientien ja -tapahtumien eri tarkastelutavat.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1875911695b1bde0b5ce4f969ad7a0c88717dc6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234138"
---
# <a name="view-journal-entries-and-transactions"></a>Näytä tapahtumat ja kirjauskansiomerkinnät

[!include [banner](../includes/banner.md)]

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


## <a name="additional-resources"></a>Lisäresurssit
- [Kirjanpitotilin saldot](general-ledger-account-balances.md) 
- [Kirjanpitolähteen hallinta](../accounts-payable/accounting-source-explorer.md)
- [Taloushallinnon raportoinnin yleiskatsaus](financial-reporting-getting-started.md)
- [Kirjauskansiovientien tai tapahtumien näyttäminen](tasks/view-journal-entries-or-transactions.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]