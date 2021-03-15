---
title: Määritä toimittajan maksulisät
description: Määritä toimittajan toimitusmaksut.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52321851a1aa588a0bbe238e366a28d503665988
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979335"
---
# <a name="define-vendor-payment-fees"></a>Määritä toimittajan maksulisät

[!include [banner](../../includes/banner.md)]

Määritä toimittajan toimitusmaksut. Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry kohtaan Ostoreskontra > Maksun asetukset > Toimitusmaksu.
2. Valitse Uusi.
3. Kirjoita arvo Lisämaksun tunnus -kenttään.
    * Lisämaksun tunnukseksi kannattaa valita lisämaksun käyttötarkoitusta kuvaava tunnus, kuten Sähköisen rahansiirron lisämaksu.  
4. Kirjoita arvo Nimi-kenttään.
5. Kirjoita arvo Lisämaksun kuvaus -kenttään.
    * Määritä lisätietoja lisämaksun käyttämisestä lisäämällä kuvaus.  
6. Valitse Veloitus-kentässä Toimittaja tai Kirjanpito.
    * Kirjanpitoa käytetään, kun lisämaksu veloitetaan organisaatiolta.  Toimittajaa käytetään, kun lisämaksu määritetään toimittajalle.  
7. Syötä päätili, jolta lisämaksu veloitetaan.
    * Tämä vaihtoehto on käytettävissä vain, kun Veloitus-asetukseksi valitaan Kirjanpito.  
8. Valitse kirjauskansio, jossa tätä lisämaksua voidaan käyttää. 
    * Valitse toimittajan toimitusmaksuksi Toimittajan suoritus -kirjauskansio.  
9. Valitse Tallenna.
10. Valitse Toimittajan toimitusmaksun asetukset.
    * Jatka toimitusmaksun asetuksiin ja määritä, milloin lisämaksu on valitsemasi kirjauskansion oletusarvo.  
11. Valitse Taulu, Ryhmä tai Kaikki.
    * Määritä arvoksi Taulu, kun valitset yksittäisen pankkitilin. Valitse Ryhmä, kun valitset pankkiryhmän ja Kaikki, kun näitä lisämaksun asetuksia käytetään kaikissa pankkitileissä.  
12. Valitse pankkiryhmä tai pankkitili.
    * Haussa näkyy pankkiryhmä, jos valittuna on Ryhmä, ja pankkitilit, jos valittuna on Taulu.  
13. Valitse maksutapa, jossa tätä lisämaksua käytetään.
14. Valitse valitun maksutavan maksumääritys.
    * Maksumäärittelyä käytetään sähköisen rahansiirron maksutavoissa.  
15. Määritä, onko lisämaksu prosentti, summa vai väli.
16. Syötä lisämaksun prosentti tai summa.
    * Jos Lisämaksu-kohtaan on valittu Prosentti, syötä prosenttiluku. Jos Lisämaksu-kohtaan on valittu Summa, syötä lisämaksun summa. Jos Lisämaksu-kohtaan on valittu Väli, syötä lisämaksujen tasot Väli-välilehden avulla.  
17. Valitse Lisämaksun valuutta -kentässä valuutta, jossa lisämaksu käsitellään.
    * Tämä valuutta koskee lisämaksua. Maksun valuutan avulla määritetään, milloin lisämaksun sääntöä käytetään maksun valuutan perusteella. Pankki saattaa veloittaa lisämaksun esimerkiksi silloin, kun maksu suoritetaan euroina. Muista maksuista ei tässä tapauksessa veloiteta lisämaksua.  
18. Valitse Tallenna.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]