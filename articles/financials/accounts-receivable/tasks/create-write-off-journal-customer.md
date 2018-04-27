--- 
title: Poiskirjauksen kirjauskansion luominen asiakkaalle
description: "Tässä tehtävän ohjauksessa näytetään, miten poiston parametrit määritetään. Ohjauksessa kerrotaan myös, miten Perintä-, Avoimet myyntilaskut- ja Asiakas-sivun poistotapahtumat määritetään."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 19a816f04283ce4f200de7396617313e45e057db
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-write-off-journal-for-a-customer"></a>Poiskirjauksen kirjauskansion luominen asiakkaalle

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävän ohjauksessa näytetään, miten poiston parametrit määritetään. Ohjauksessa kerrotaan myös, miten Perintä-, Avoimet myyntilaskut- ja Asiakas-sivun poistotapahtumat määritetään. Tässä tehtävässä käytetään esittely-yritystä USMF.


## <a name="set-up-the-write-off-parameters"></a>Poiston parametrien määrittäminen
1. Siirry kohtaan Luotonvalvonta > Asetukset > Myyntireskontran parametrit.
2. Valitse Perintä-välilehti.
3. Laajenna tai tiivistä Poisto-osa.
    * Poiston kirjauskansio on yleinen kirjauskansio, joka sisältää luomasi poistotapahtumat.  
    * Voit liittää jokaiseen poistoon syykoodin. Voit korvata tämän oletusarvon poiston yhteydessä.  
    * Määritä tämän kohdan arvoksi Kyllä, jos haluat erottaa arvonlisäveron alkuperäisestä tapahtumasta poistossa.  
4. Sulje sivu.
5. Siirry kohtaan Luotonvalvonta > Asetukset > Asiakkaan kirjausprofiilit.
    * Poistotiliä käytetään kulutilinä tai varauksen oikaisuna yleisessä kirjauskansiossa   
6. Sulje sivu.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Asiakkaan saldon poiskirjaus erääntyneiden saldojen sivulla
1. Siirry kohtaan Luotonvalvonta > Perintä > Erääntyneet saldot.
2. Merkitse se asiakkaan rivi, jonka haluat poistaa. Merkitse esimerkiksi rivi, jolla on Birch-niminen yritys.
3. Valitse toimintoruudussa Perintä.
4. Valitse Poisto.
5. Valitse OK.
6. Sulje sivu.
7. Siirry kohtaan Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot.
8. Valitse poiston sisältävän kirjauskansion eränumero.
    * Yksi rivi luodaan asiakkaan saldon palauttamiseksi. Yksi tai useita rivejä luodaan poiston kirjaamiseksi poistotilille.  
9. Sulje sivu.
10. Sulje sivu.

## <a name="write-off-transactions-from-the-collections-form"></a>Kirjaa pois tapahtumia perintälomakkeelta.
1. Siirry kohtaan Luotonvalvonta > Perintä > Erääntyneet saldot.
2. Valitse sen asiakkaan nimi, jolla on poistettavia tapahtumia. Valitse esimerkiksi Cave Wholesales (US-004).
3. Merkitse rivi ensimmäistä tapahtumaa varten.
4. Merkitse rivi toista tapahtumaa varten.
5. Valitse Poisto.
6. Syötä Syyn kommentti -kenttään Luottotappio.
7. Valitse OK.
8. Sulje sivu.
9. Sulje sivu.
10. Siirry kohtaan Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot.
11. Valitse poiston sisältävän kirjauskansion eränumero.
    * Yksi rivi luodaan asiakkaan saldon palauttamiseksi. Yksi tai useita rivejä luodaan poiston kirjaamiseksi poistotilille.  
12. Sulje sivu.
13. Sulje sivu.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Laskun poiskirjaus Avoimet myyntilaskut -sivulta
1. Siirry kohtaan Myyntireskontra > Laskut > Avoimet myyntilaskut.
2. Merkitse laskun rivi. Voit esimerkiksi merkitä kohteen CIV-000667 rivin.
3. Valitse toimintoruudussa Lasku.
4. Valitse Poisto.
5. Valitse OK.
6. Sulje sivu.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Asiakkaan saldon poiskirjaus Asiakas-sivulta
1. Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.
2. Valitse asiakastili. Valitse esimerkiksi US-001 (Contoso Retail San Diego).
3. Valitse toimintoruudussa Perintä.
4. Valitse Poisto.
5. Valitse OK.
6. Sulje sivu.


