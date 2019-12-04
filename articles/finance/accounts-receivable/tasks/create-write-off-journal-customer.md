---
title: Poiskirjauksen kirjauskansion luominen asiakkaalle
description: Tässä tehtävän ohjauksessa näytetään, miten poiston parametrit määritetään. Ohjauksessa kerrotaan myös, miten Perintä-, Avoimet myyntilaskut- ja Asiakas-sivun poistotapahtumat määritetään.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2422f0a9d168daa76d105099c8b7455c97f92125
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188829"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>Poiskirjauksen kirjauskansion luominen asiakkaalle

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävän ohjauksessa näytetään, miten poiston parametrit määritetään. Ohjauksessa kerrotaan myös, miten Perintä-, Avoimet myyntilaskut- ja Asiakas-sivun poistotapahtumat määritetään. Tässä tehtävässä käytetään esittely-yritystä USMF.


## <a name="set-up-the-write-off-parameters"></a>Poiston parametrien määrittäminen
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Luotonvalvonta > Asetukset > Myyntireskontran parametrit**.
2. Valitse **Perintä**-välilehti.
3. Laajenna tai tiivistä **Poisto**-osa.
    - **Poistojen kirjauskansio** on yleinen kirjauskansio, joka sisältää luomasi poistotapahtumat.  
    - Voit liittää jokaiseen poistoon syykoodin. Voit korvata tämän oletusarvon poiston yhteydessä.  
    - Määritä **Erillinen arvonlisävero** -kohdan arvoksi Kyllä, jos haluat erottaa arvonlisäveron alkuperäisestä tapahtumasta poistossa.  
4. Sulje sivu.
5. Valitse **Luotonvalvonta > Asetukset > Asiakkaan kirjausprofiilit**. Poistotiliä käytetään kulutilinä tai varauksen oikaisuna yleisessä kirjauskansiossa.
6. Sulje sivu.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Asiakkaan saldon poiskirjaus erääntyneiden saldojen sivulla
1. Siirry kohtaan **Luotonvalvonta > Perintä > Erääntyneet saldot**.
2. Merkitse se asiakkaan rivi, jonka haluat poistaa. Merkitse esimerkiksi rivi, jolla on Birch-niminen yritys.
3. Valitse **toimintoruudussa** **Perintä**.
4. Valitse **Poisto**.
5. Valitse **OK**.
6. Sulje sivu.
7. Siirry kohtaan **Siirtymisruutu > Moduulit > kirjanpito > kirjauskansioviennit > Yleiset kirjauskansiot**.
8. Valitse poiston sisältävän kirjauskansion eränumero. Yksi rivi luodaan asiakkaan saldon palauttamiseksi. Yksi tai useita rivejä luodaan poiston kirjaamiseksi poistotilille.  
9. Sulje sivu.
10. Sulje sivu.

## <a name="write-off-transactions-from-the-collections-form"></a>Kirjaa pois tapahtumia perintälomakkeelta.
1. Siirry kohtaan **Luotonvalvonta > Perintä > Erääntyneet saldot**.
2. Valitse sen asiakkaan nimi, jolla on poistettavia tapahtumia. Valitse esimerkiksi Cave Wholesales (US-004).
3. Merkitse rivi ensimmäistä tapahtumaa varten.
4. Merkitse rivi toista tapahtumaa varten.
5. Valitse **Poisto**.
6. Syötä **Syyn kommentti** -kenttään Luottotappio.
7. Valitse **OK**.
8. Sulje sivu.
9. Sulje sivu.
10. Siirry kohtaan **Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot**.
11. Valitse poiston sisältävän kirjauskansion eränumero. Yksi rivi luodaan asiakkaan saldon palauttamiseksi. Yksi tai useita rivejä luodaan poiston kirjaamiseksi poistotilille.  
12. Sulje sivu.
13. Sulje sivu.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Laskun poiskirjaus Avoimet myyntilaskut -sivulta
1. Siirry siirtymisruudussa kohtaan **Moduulit > Myyntireskontra > Laskut > Avoimet asiakaslaskut**.
2. Merkitse laskun rivi. Voit esimerkiksi merkitä kohteen CIV-000667 rivin.
3. Valitse **toimintoruudussa** **Lasku**.
4. Valitse **Poisto**.
5. Valitse **OK**.
6. Sulje sivu.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Asiakkaan saldon poiskirjaus Asiakas-sivulta
1. Siirry kohtaan **Myyntireskontra > Asiakkaat > Kaikki asiakkaat**.
2. Valitse asiakastili. Valitse esimerkiksi US-001 (Contoso Retail San Diego).
3. Valitse **toimintoruudussa** **Perintä**.
4. Valitse **Poisto**.
5. Valitse **OK**.
6. Sulje sivu.
