---
title: Vapaatekstilaskun mallin määrittäminen asiakkaalle
description: Tässä tehtävässä kerrotaan, miten vapaatekstilaskun malli liitetään asiakkaalle.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53bff33083a78c0bb1c7d243fe9965fb264d209e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843046"
---
# <a name="assign-free-text-invoice-template-to-a-customer"></a>Vapaatekstilaskun mallin määrittäminen asiakkaalle

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

