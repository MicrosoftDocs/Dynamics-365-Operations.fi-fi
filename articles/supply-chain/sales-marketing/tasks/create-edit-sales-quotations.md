---
title: Myyntitarjousten luonti ja muokkaus
description: Tässä menettelyssä käsitellään, miten myyntitarjous luodaan ja päivitetään.
author: omulvad
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable, CustQuotationConfirmationJournal, CustQuotationJournal, CustSalesLines, SalesQuotationCopying, SalesQuotationDeleteQuotations, SalesQuotationListPagePreviewPane, SalesQuotationTypeGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 73c15b41a4b0979ec79c8dbd8d88627bffcf6ed3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426879"
---
# <a name="create-and-edit-sales-quotations"></a>Myyntitarjousten luonti ja muokkaus

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään, miten myyntitarjous luodaan ja päivitetään. Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omia tietoja.


## <a name="create-a-sales-quotation"></a>Luo myyntitarjous
1. Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Myyntitarjoukset > Kaikki tarjoukset**.
2. Valitse **Uusi**.
3. Valitse **Tilityyppi**-kentässä Prospekti.
4. Anna tai valitse **Prospekti**-kentässä arvo.
5. Laajenna **Yleiset**-osa. Koska valitsit tarjouksen luomisen Myynti ja markkinointi -alueelta, tyypiksi määritettiin automaattisesti Myyntitarjous. Jos haluat luoda projektitarjouksen, tee se **Projektinhallinta ja kirjanpito** -moduulissa.
6. Valitse **OK**. Tarjousrivin kentät ja toiminnot muistuttavat myyntitilausrivin kenttiä ja toimintoja.   Myyntitilausten tavoin tarjoukset voidaan luoda tietylle nimikkeelle tai, jos nimiketunnusta ei tiedetä tai sitä ei ole tarjouksen luontiaikana, ne voidaan luoda myyntiluokalle.     
7. Anna tai valitse **Nimike**-kentässä arvo.
8. Kirjoita arvo **Toimipaikka**-kenttään.
9. Anna **Määrä**-kentässä numero. Jos rivillä valitulla nimikkeellä on voimassaolevia sopimuksia, sovellettava hinta ja alennukset kopioidaan automaattisesti tarjousriville. Varmista, että Yksikköhinta-kentässä on arvo. Voit halutessasi antaa myös alennusarvot. 
10. Valitse **Tallenna**.
11. Valitse **toimintoruudussa** **Myyntitarjous**.
12. Valitse **Summat**.
13. Valitse **OK**.
14. Valitse myyntitarjousrivi.
15. Valitse **toimintoruudussa** **Tarjous**.
16. Valitse **Hintasimulaatio**.
    - Voit kokeilla **Suorita hintasimulaatio** -sivulla tarjouksen odotetun tuoton tai kannattavuuden säätämistä halutun yksikköhinnan, alennussumman, alennusprosentin, kokonaissumman, marginaalin tai katetuottoprosentin perusteella. Kun olet tyytyväinen tavoitelukuihin, käytä ehdotusta tarjousrivillä, jolloin sen hintaan liittyvät kentät päivitetään vastaavasti.  
    - Voit luoda niin monta hintasimulointia kuin haluat. Uusi valitset **Uusi**, nykyisen tarjousrivin hintaehdot kopioidaan sivulle. Voit sitten muokata minkä tahansa hintaan liittyvän kentän arvoja tavoitearvoiksi. Yhden kentän muuttaminen käynnistää kaikkien muiden kenttien uudelleenlaskennan. Jotta järjestelmä voisi laskea myyntikatteen ja katetuottoprosentin, tuotteen yksikkökustannus on tiedettävä. Simuloidut hinnat -välilehdessä on tarkat tiedot alkuperäisistä hinnoista, ehdotetuista muutoksista ja niiden vaikutuksesta tarjouksen summiin. Yleisesti ottaen järjestelmä laskee arvon uudelleen ja lisää uuden arvon Yksikköhinta-kenttään, kun simulointi määrittää, että tarjousrivillä on käytettävä uutta summaa. Jos simulointi perustuu uuteen marginaaliin tai uuteen katetuottoprosenttiin, vain Nettosumma-kenttä päivitetään ja Yksikköhinta on tyhjä. Kummassakin tapauksessa tarjousrivillä ennen simulointia olleet alennukset poistetaan.
17. Valitse **toimintoruudussa** **Tarjous**.
18. Valitse **Lähetä tarjous**.
19. Valitse **Tulosta tarjous** -kentässä Kyllä.
20. Valitse **OK**. Raportin luontiin voi kulua useita minuutteja. Älä sulje sivu, ennen kuin raportti on valmis.

## <a name="update-a-sales-quotation"></a>Päivitä myyntitarjous
1. Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Myyntitarjoukset > Kaikki tarjoukset**.
2. Valitse **toimintoruudussa** **Seuranta**.
3. Valitse **Muunna asiakkaaksi**.
4. Kirjoita arvo **Asiakastili**-kenttään.
5. Valitse **Tarkista**. Varmista, että näyttöön avautuu sanoma, jonka mukaan antamasi tilinumero on vapaa käytettäväksi.  
6. Valitse **OK**. Järjestelmä on nyt luonut uuden asiakastilin tarjouksen prospektille.  
7. Sulje sivu.
8. Valitse **toimintoruudussa** **Seuranta**.
9. Valitse **Vahvista**.
10. Anna tai valitse **Syy**-kentässä arvo.
11. Valitse **OK**.
12. Valitse **toimintoruudussa** **Yleiset**.
13. Valitse **Myyntitilaukset**.
14. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]