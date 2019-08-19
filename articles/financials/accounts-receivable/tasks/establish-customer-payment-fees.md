---
title: Määritä asiakkaan maksulisät
description: Luo asiakkaan toimitusmaksut.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f18b88cfdeef2e66003cd4411ace4b4c49e42f6f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834436"
---
# <a name="establish-customer-payment-fees"></a>Määritä asiakkaan maksulisät

[!include [task guide banner](../../includes/task-guide-banner.md)]

Luo asiakkaan toimitusmaksut.

Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry kohtaan Myyntireskontra > Maksujen asetukset > Toimitusmaksu.
2. Valitse Uusi.
3. Syötä Lisämaksun tunnus -kenttään lisämaksun tunnus.
    * Lisämaksun tunnus näkyy maksukirjauskansioissa, joten määritä käsiteltävää lisämaksua kuvaava tunnus.  
4. Syötä Nimi-kenttään lisämaksun nimi.
5. Syötä Lisämaksun kuvaus -kenttään lisämaksun kuvaus.
6. Määritä, veloitetaanko lisämaksu asiakkaalta vai kirjanpitotililtä.
    * Jos lisämaksu koskee asiakasta, valitse Asiakas. Jos organisaatio käsittelee lisämaksun kuluna, valitse Kirjanpito. Tässä tehtävässä valitaan Asiakas.  
7. Valitse sen kirjauskansion tyyppi, joka voi käyttää tätä toimitusmaksua.
    * Jos näitä lisämaksuja käytetään asiakkaan maksuissa, kirjauskansion tyypiksi määritetään todennäköisesti Asiakkaan maksu.  
8. Valitse Tallenna.
9. Valitse Toimittajan toimitusmaksun asetukset.
    * Toimitusmaksun asetuksissa määritetään toimitusmaksun käsittelyajankohdan ehdot.  Voit esimerkiksi määrittää, että lisämaksu lasketaan, jos pankkitili on USMF OPER ja maksutapa on sekki.  
10. Valitse joko Taulu, Ryhmä tai Kaikki, kun määrität tätä lisämaksua käyttävät pankkitilit.
    * Jos valitset Kaikki, tämä lisämaksu koskee kaikkia pankkitilejä.  Jos valitset Taulu, tämä lisämaksu koskee vain valitsemaasi pankkitiliä. Jos valitset Ryhmä, tämä lisämaksu koskee vain valitsemasi pankkiryhmän pankkitilejä.  
11. Valitse pankkiryhmä tai pankkitili.
    * Jos valitset Taulu, pankkitilit näkyvät haussa. Jos valitset Ryhmä, pankkiryhmät näkyvät haussa.  
12. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
13. Valitse maksutapa, jossa tätä lisämaksua käytetään.
    * Voit määrittää lisämaksun asiakkaille esimerkiksi silloin, kun he lähettävät maksut sekkeinä sähköisten maksujen sijaan.  
14. Etsi haluamasi tietue luettelosta ja valitse se.
15. Syötä tarvittaessa maksun valuutta.
    * Maksun valuuttaa käytetään lisäehtona lisämaksun määrittämisessä.  Pankki voi veloittaa lisämaksun esimerkiksi Yhdysvaltojen dollareina saapuneista maksuista, koska yleensä maksutapahtumat suoritetaan euroina.  
16. Määritä, esitetäänkö lisämaksu prosenttina, summana vai välinä.
17. Syötä lisämaksun prosentti tai summa.
    * Jos Prosentti/summa-kentän arvo on Prosentti, tähän syötetään prosenttiluku. Jos Prosentti/summa-kentän arvo on Summa, tähän syötetään summa. Jos Prosentti/summa-kenttä on Väli, määritä tasot Väli-välilehden avulla.  
18. Valitse Lisämaksun valuutta -kentässä lisämaksun valuutta.
    * Tämä on valuutta, jossa lisämaksu luodaan.  
19. Valitse Tallenna.

