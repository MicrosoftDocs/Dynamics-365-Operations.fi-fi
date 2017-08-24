--- 
title: "Vapaatekstilaskumallin määrittäminen asiakkaalle"
description: "Tässä tehtävässä kerrotaan, miten vapaatekstilaskun malli liitetään asiakkaalle."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: af9e5f499e6c162189443d95c90b15c17d910739
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>Vapaatekstilaskumallin määrittäminen asiakkaalle

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävässä kerrotaan, miten vapaatekstilaskun malli liitetään asiakkaalle. Tässä tehtävässä käytetään USMF-esittely-yritystä. Tehtävä on tarkoitettu myyntireskontran laskujen hallinnasta ja käsittelemisestä vastaavalle käyttäjälle.

1. Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Valitse toimintoruudussa Lasku.
4. Valitse Toistuvat laskut.
    * Tällä sivulla liitetään vapaatekstilaskun mallit asiakkaille ja määritetään, miten usein laskut lähetetään asiakkaalle.  
5. Valitse Uusi, kun haluat liittää asiakkaalle uuden mallin.
6. Valitse vapaatekstilaskun malli, jonka haluat liittää asiakkaalle.
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Syötä ensimmäisen laskun luontipäivämäärä.
    * Määritä toiston päättymispäivämäärä.  
    * Valitse jokin seuraavista vaihtoehdoista: Päättymispäivä puuttuu – Laskuja luodaan niin kauan kunnes malli poistetaan asiakkaan tililtä.  Laskutuksen päättymispäivämäärä – Valitse tämä vaihtoehto, kun haluat syöttää laskun luonnille viimeisen päivämäärän.  
    * Suurin mahdollinen kumulatiivinen summa, jonka jälkeen laskujen luominen päättyy.  
    * Syötä suurin mahdollinen kumulatiivinen summa, joka valitun mallin avulla voidaan saavuttaa. Jos esimerkiksi syötät arvioksi 1 000,00, ja kuukauden laskutus on 100,00, laskujen luominen päättyy kymmenennen laskun jälkeen.  
    * Toistuvat laskut luodaan vapaatekstilaskun mallin tai asiakkaan tilin oletusarvojen perusteella.  
    * Valitse käytettäväksi vapaatekstilaskumalli tai asiakastili, kun laskujen luonnin yhteydessä määritetään oletusarvo kielelle, kirjausprofiilille, arvonlisäveroryhmälle, nimikkeen arvonlisäveroryhmälle, luettelokoodille, toimituksen maalle/alueelle, valuutalle, maksuehdoille, maksutavalle, maksumääritykselle, maksuaikataululle, käteisalennukselle, taloushallinnon dimensiolle ja tilisiirtolomakkeelle.  
10. Valitse toistumismalli.
    * Päivittäin – Valitse tämä vaihtoehto ja syötä päivien määrä Per-kenttään. Jos syötät esimerkiksi luvun 15, asiakkaalle luodaan lasku 15 päivän välein.  Viikoittain – Valitse tämä vaihtoehto ja syötä viikkojen määrä Per-kenttään. Jos syötät esimerkiksi luvun 2, asiakkaalle luodaan lasku joka toinen viikko.  Kuukausittain – Valitse tämä vaihtoehto ja syötä kuukausien määrä Per-kenttään. Jos syötät esimerkiksi luvun 6, asiakkaalle luodaan lasku kuuden kuukauden välein.  Vuosittain– Valitse tämä vaihtoehto ja syötä vuosien määrä Per-kenttään. Jos syötät esimerkiksi luvun 2, asiakkaalle luodaan lasku joka toinen vuosi.  
11. Syötä numero Per-kenttään.


