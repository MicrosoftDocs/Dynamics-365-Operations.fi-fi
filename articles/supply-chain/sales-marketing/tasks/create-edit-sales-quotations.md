--- 
title: Myyntitarjousten luonti ja muokkaus
description: "Tässä menettelyssä käsitellään, miten myyntitarjous luodaan ja päivitetään."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8e7d2198b4976a6f60f05690d7b6f11f3da55e28
ms.openlocfilehash: 7ffa4fe8d87db5b3f8293ec9dbc042496d09d6e3
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---
# <a name="create-and-edit-sales-quotations"></a>Myyntitarjousten luonti ja muokkaus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään, miten myyntitarjous luodaan ja päivitetään. Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omia tietoja.


## <a name="create-a-sales-quotation"></a>Luo myyntitarjous
1. Valitse Myynti ja markkinointi > Myyntitarjoukset > Kaikki tarjoukset.
2. Valitse Uusi.
3. Valitse Tilityyppi-kentässä Prospekti.
4. Anna tai valitse Prospekti-kentässä arvo.
5. Laajenna Yleiset-osa.
    * Koska valitsit tarjouksen luomisen Myynti ja markkinointi -alueelta, tyypiksi määritettiin automaattisesti Myyntitarjous. Jos haluat luoda projektitarjouksen, tee se Projektinhallinta ja kirjanpito -moduulissa.   
6. Valitse OK.
    * Tarjousrivin kentät ja toiminnot muistuttavat myyntitilausrivin kenttiä ja toimintoja.   Myyntitilausten tavoin tarjoukset voidaan luoda tietylle nimikkeelle tai, jos nimiketunnusta ei tiedetä tai sitä ei ole tarjouksen luontiaikana, ne voidaan luoda myyntiluokalle.  
7. Anna tai valitse Nimike-kentässä arvo.
8. Kirjoita Nimike-kenttään arvo.
9. Sulje sivu.
10. Kirjoita numero Määrä-kenttään.
    * Jos rivillä valitulla nimikkeellä on voimassaolevia sopimuksia, sovellettava hinta ja alennukset kopioidaan automaattisesti tarjousriville. Varmista, että Yksikköhinta-kentässä on arvo. Voit halutessasi antaa myös alennusarvot.  
11. Valitse Tallenna.
12. Valitse toimintoruudussa Myyntitarjous.
13. Valitse Summat.
14. Valitse OK.
15. Valitse myyntitarjousrivi.
16. Valitse Hinnat.
    * Voit kokeilla Suorita hintasimulaatio -sivulla tarjouksen odotetun tuoton tai kannattavuuden säätämistä halutun yksikköhinnan, alennussumman, alennusprosentin, kokonaissumman, marginaalin tai katetuottoprosentin perusteella.   Kun olet tyytyväinen tavoitelukuihin, käytä ehdotusta tarjousrivillä, jolloin sen hintaan liittyvät kentät päivitetään vastaavasti.  
    * Voit luoda niin monta hintasimulointia kuin haluat. Uusi valitset Uusi, nykyisen tarjousrivin hintaehdot kopioidaan sivulle. Voit sitten muokata minkä tahansa hintaan liittyvän kentän arvoja tavoitearvoiksi. Yhden kentän muuttaminen käynnistää kaikkien muiden kenttien uudelleenlaskennan. Jotta järjestelmä voisi laskea myyntikatteen ja katetuottoprosentin, tuotteen yksikkökustannus on tiedettävä. Simuloidut hinnat -välilehdessä on tarkat tiedot alkuperäisistä hinnoista, ehdotetuista muutoksista ja niiden vaikutuksesta tarjouksen summiin.   Yleisesti ottaen järjestelmä laskee arvon uudelleen ja lisää uuden arvon Yksikköhinta-kenttään, kun simulointi määrittää, että tarjousrivillä on käytettävä uutta summaa. Jos simulointi perustuu uuteen marginaaliin tai uuteen katetuottoprosenttiin, vain Nettosumma-kenttä päivitetään ja Yksikköhinta on tyhjä. Kummassakin tapauksessa tarjousrivillä ennen simulointia olleet alennukset poistetaan.  
17. Sulje sivu.
18. Valitse toimintoruudussa Tarjous.
19. Valitse Lähetä tarjous.
20. Valitse Tulosta tarjous -kentässä Kyllä.
21. Valitse OK.
    * Raportin luontiin voi kulua useita minuutteja. Älä sulje sivu, ennen kuin raportti on valmis.  
22. Sulje sivu.

## <a name="update-a-sales-quotation"></a>Päivitä myyntitarjous
1. Valitse toimintoruudussa Seuranta.
2. Valitse Muunna asiakkaaksi.
3. Kirjoita arvo Asiakastili-kenttään.
4. Valitse Tarkista.
    * Varmista, että näyttöön avautuu sanoma, jonka mukaan antamasi tilinumero on vapaa käytettäväksi.  
5. Valitse OK.
    * Järjestelmä on nyt luonut uuden asiakastilin tarjouksen prospektille.  
6. Sulje sivu.
7. Valitse toimintoruudussa Seuranta.
8. Valitse Vahvista.
9. Anna tai valitse Syy-kentässä arvo.
10. Valitse OK.
11. Valitse toimintoruudussa Yleiset.
12. Valitse Myyntitilaukset.
13. Sulje sivu.


