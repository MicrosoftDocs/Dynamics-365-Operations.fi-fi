---
title: Määritä asiakkaan maksulisät
description: Luo asiakkaan toimitusmaksut.
author: ShivamPandey-msft
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7daf2f5b976dbc300458b5cb3efd0c0420c4f5c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822320"
---
# <a name="establish-customer-payment-fees"></a>Määritä asiakkaan maksulisät

[!include [banner](../../includes/banner.md)]

Luo asiakkaan toimitusmaksut.

Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry kohtaan **Siirtymisruutu** > **Moduulit > Myyntireskontra >Maksujen asetukset > Toimitusmaksu**.
2. Valitse **Uusi**.
3. Syötä **Lisämaksun tunnus** -kenttään lisämaksun tunnus. Lisämaksun tunnus näkyy maksukirjauskansioissa, joten määritä käsiteltävää lisämaksua kuvaava tunnus.  
4. Syötä **Nimi**-kenttään lisämaksun nimi.
5. Syötä **Lisämaksun kuvaus** -kenttään lisämaksun kuvaus.
6. Valitse **Veloitus**-kentässä, veloitetaanko lisämaksu asiakas- vai kirjanpitotililtä. Jos lisämaksu koskee asiakasta, valitse Asiakas. Jos organisaatio käsittelee lisämaksun kuluna, valitse Kirjanpito. Tässä tehtävässä valitaan Asiakas.  
7. Valitse **Kirjauskansion tyyppi** -kentässä kirjauskansion tyyppi, joka voi käyttää tätä toimitusmaksua. Jos näitä lisämaksuja käytetään asiakkaan maksuissa, kirjauskansion tyypiksi määritetään todennäköisesti Asiakkaan maksu.  
8. Valitse **Tallenna**.
9. Valitse **Toimitusmaksun asetukset**. Toimitusmaksun asetuksissa määritetään toimitusmaksun käsittelyajankohdan ehdot.  Voit esimerkiksi määrittää, että lisämaksu lasketaan, jos pankkitili on USMF OPER ja maksutapa on sekki.  
10. Valitse **Ryhmittelyt**-kentässä joko Taulu, Ryhmä tai Kaikki, kun määrität tätä lisämaksua käyttävät pankkitilit. Jos valitset Kaikki, tämä lisämaksu koskee kaikkia pankkitilejä.  Jos valitset Taulu, tämä lisämaksu koskee vain valitsemaasi pankkitiliä. Jos valitset Ryhmä, tämä lisämaksu koskee vain valitsemasi pankkiryhmän pankkitilejä.  
11. Valitse **Maksuliikenneyhteys**-kentässä joko pankkiryhmä tai pankkitili. Jos valitset Taulu, pankkitilit näkyvät haussa. Jos valitset Ryhmä, pankkiryhmät näkyvät haussa.  
12. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
13. Valitse **Maksutapa**-kentässä maksutapa, jota varten tämä maksu arvioidaan. Voit määrittää lisämaksun asiakkaille esimerkiksi silloin, kun he lähettävät maksut sekkeinä sähköisten maksujen sijaan.  
14. Etsi haluamasi tietue luettelosta ja valitse se.
15. Jos on tarpeen, syötä **Maksun valuutta** -kenttään maksun valuutta. Maksun valuuttaa käytetään lisäehtona lisämaksun määrittämisessä.  Pankki voi veloittaa lisämaksun esimerkiksi Yhdysvaltojen dollareina saapuneista maksuista, koska yleensä maksutapahtumat suoritetaan euroina.  
16. Määritä, esitetäänkö lisämaksu prosenttina, summana vai välinä.
17. Syötä **Prosenttiosuus/summa**-kenttään maksun prosenttiosuus tai summa. Jos Prosentti/summa-kentän arvo on Prosentti, tähän syötetään prosenttiluku. Jos Prosentti/summa-kentän arvo on Summa, tähän syötetään summa. Jos Prosentti/summa-kenttä on Väli, määritä tasot Väli-välilehden avulla.  
18. Valitse **Lisämaksun valuutta** -kentässä lisämaksun valuutta. Tämä on valuutta, jossa lisämaksu luodaan.  
19. Valitse **Tallenna**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]