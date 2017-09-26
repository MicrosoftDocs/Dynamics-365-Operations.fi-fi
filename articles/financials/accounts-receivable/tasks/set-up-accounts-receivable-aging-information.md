--- 
title: "Määritä ja luo myyntireskontran erääntymistiedot"
description: "Tämän ohjauksen avulla opit määrittämään erääntymiskauden ja asiakkaiden saldojen erääntymisen sekä tarkastelemaan erääntyneiden saldojen luettelon saldoja ja Perintä-sivua."
author: mikefalkner
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
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ed23bcfed4e256ecc16264a181161c7119cd9bb3
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Määritä ja luo myyntireskontran erääntymistiedot

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tämän ohjauksen avulla opit määrittämään erääntymiskauden ja asiakkaiden saldojen erääntymisen sekä tarkastelemaan erääntyneiden saldojen luettelon saldoja ja Perintä-sivua. Tässä tallenteessa käytetään esittely-yritystä USMF.


## <a name="create-an-aging-period-definition"></a>Luo erääntymiskausien määritys.
1. Siirry kohtaan Luotonvalvonta > Asetukset > Erääntymiskausien määritykset.
2. Valitse Uusi.
3. Kirjoita arvo Erääntymiskauden määritys -kenttään.
4. Kirjoita Kuvaus-kenttään arvo.
5. Lisää uusi erääntymiskausi valitsemalla alla oleva Lisää.
6. Syötä Kausi-kenttään erääntymisraporteissa näkyvä kuvaus.
7. Syötä Yksikkö-kenttään numero.
8. Valitse vaihtoehto Aikaväli-kentässä.
    * Kirjanpitokausi on sama kuin kirjanpitokalenterin kausi. Päivä, viikko, kuukausi, neljännesvuosi ja vuodet määrittävät aikavälin koon päivämäärätyypin mukaan. Jos valittuna on Rajoittamaton, kaikki edellistä kautta aiemmat tai edellisen kauden jälkeiset tapahtumat valitaan sen perusteella, onko kyseessä ensimmäinen vai viimeinen kausi.  
9. Valitse vaihtoehto Erääntymisen ilmaisin -kentässä.
10. Valitse kausi ruudukon yläosassa. Päivitä kuvaukseen erääntymiskauden määrityksen vanhimman kauden kuvaus.
11. Syötä Kausi-kenttään erääntymiskauden uusi kuvaus.
12. Sulje sivu.

## <a name="age-the-balances"></a>Saldojen erääntyminen
1. Siirry kohtaan Luotonvalvonta > Kausittaiset tehtävät > Eräännytä asiakkaan saldot.
2. Valitse Erääntymiskauden määritys -kentässä luomasi erääntymiskauden määritys.
    * Kullakin erääntymiskauden määrityksellä voi olla yksi aktiviinen tilannevedos.  
    * Kaikki asiakkaat käsitellään oletusarvoisesti. Voit laskea yksittäisten perintöjen asiakasjoukon tämän valinnan perusteella.  
    * Valitse sen tapahtuman päivämäärä, jota haluat käyttää erääntymisessä.  
    * Valitse erääntymiselle alkaen-päivämäärä. Oletusarvo on tänään. Voit kuitenkin muuttaa kentän arvoksi Valittu päivämäärä, jolloin voit valita haluamasi päivämäärän. Käytä eräkäsittelyssä kuluvaa päivämäärää.  
3. Laajenna yritysalue. Voit valita yrityksiä tilannevedokseen. Nykyinen yritys on valittuna oletusarvoisesti.
4. Aloita tilannevedoksen käsittely valitsemalla OK. Tähän kuluu jonkin aikaa, joten odota, kunnes liukusäädin katoaa. Tarkista sitten viestikeskuksen viestit.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>Saldojen tarkasteleminen erääntyneiden saldojen luettelossa ja Perintä-sivulla
1. Siirry kohtaan Luotonvalvonta > Perintä > Erääntyneet saldot.
    * Luettelosivulla näkyvät asiakkaan saldot. Erääntymiskuvake osoittaa vanhimman tapahtuman erääntymiskauden.  
2. Valitse asiakas, jolla on saldo.
3. Laajenna Erääntyminen-tietoruutua niin, että erääntyvät saldot näkyvät.
    * Tietokentän erääntymiskauden määritys saadaan parametreissa määritetystä erääntymiskauden oletusmäärityksestä. Arvon voi muuttaa keräysvalikon avulla.  


