---
title: Vapaatekstilaskumallin määrittäminen asiakkaalle
description: Tässä tehtävässä kerrotaan, miten vapaatekstilaskun malli liitetään asiakkaalle.
author: ShivamPandey-msft
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49074c11659ae30fd2decdb93b4721441edff2c5
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780524"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>Vapaatekstilaskumallin määrittäminen asiakkaalle

[!include [banner](../../includes/banner.md)]

Tässä tehtävässä kerrotaan, miten vapaatekstilaskun malli liitetään asiakkaalle. Tässä tehtävässä käytetään USMF-esittely-yritystä. Tehtävä on tarkoitettu myyntireskontran laskujen hallinnasta ja käsittelemisestä vastaavalle käyttäjälle.

1. Siirry **siirtymisruudussa** kohtaan **Moduulit > Myyntireskontra > Asiakkaat > Kaikki asiakkaat**.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Valitse **toimintoruudussa** **Lasku**.
4. Valitse **Toistuvat laskut**. Tällä sivulla liitetään vapaatekstilaskun mallit asiakkaille ja määritetään, miten usein laskut lähetetään asiakkaalle.  
5. Valitse **Uusi**, kun haluat liittää asiakkaalle uuden mallin.
6. Valitse **Malli**-kentässä vapaatekstilaskun malli, jonka haluat liittää asiakkaalle.
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Syötä **Laskutuksen aloituspäivämäärä** -kenttään ensimmäisen laskun luontipäivämäärä.
10. Määritä **Toisto päättyy** -osassa toiston päättymispäivämäärä.  
    Valitse jokin seuraavista: 
    - **Päättymispäivä puuttuu** – Laskuja luodaan niin kauan kunnes malli poistetaan asiakkaan tililtä.
    - **Laskutuksen päättymispäivä** – Valitse tämä vaihtoehto, kun haluat syöttää laskun luonnille viimeisen päivämäärän.  
11. Syötä **Kumulatiivinen enimmäissumma** -kenttään suurin kumulatiivinen summa, jonka jälkeen laskun luonti pysähtyy. Syötä suurin mahdollinen kumulatiivinen summa, joka valitun mallin avulla voidaan saavuttaa. Jos esimerkiksi syötät arvioksi 1 000,00, ja kuukauden laskutus on 100,00, laskujen luominen päättyy kymmenennen laskun jälkeen.  
12. Valitse **Luo toistuvia laskuja käyttämällä oletusarvoja** -osassa vapaatekstilaskun malli tai asiakastili. Valitse käytettäväksi vapaatekstilaskumalli tai asiakastili, kun laskujen luonnin yhteydessä määritetään oletusarvo kielelle, kirjausprofiilille, arvonlisäveroryhmälle, nimikkeen arvonlisäveroryhmälle, luettelokoodille, toimituksen maalle/alueelle, valuutalle, maksuehdoille, maksutavalle, maksumääritykselle, maksuaikataululle, käteisalennukselle, taloushallinnon dimensiolle ja tilisiirtolomakkeelle.  
13. Valitse **Toistumisen kuvio** -kentässä toistumisen kuvio.
    - **Päivittäin** – Valitse tämä vaihtoehto ja syötä päivien määrä Per-kenttään. Jos syötät esimerkiksi luvun 15, asiakkaalle luodaan lasku 15 päivän välein.
    - **Viikoittain** – Valitse tämä vaihtoehto ja syötä viikkojen määrä Per-kenttään. Jos syötät esimerkiksi luvun 2, asiakkaalle luodaan lasku joka toinen viikko.
    - **Kuukausittain** – Valitse tämä vaihtoehto ja syötä kuukausien määrä Per-kenttään. Jos syötät esimerkiksi luvun 6, asiakkaalle luodaan lasku kuuden kuukauden välein.
    - **Vuosittain** – Valitse tämä vaihtoehto ja syötä vuosien määrä Per-kenttään. Jos syötät esimerkiksi luvun 2, asiakkaalle luodaan lasku joka toinen vuosi.  
14. Syötä numero **Per**-kenttään.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
