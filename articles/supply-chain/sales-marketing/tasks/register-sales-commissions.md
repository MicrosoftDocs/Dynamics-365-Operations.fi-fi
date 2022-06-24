---
title: Myyntiprovisioiden rekisteröinti
description: Tässä artikkelissa kerrotaan, miten myyntiprovisiot lasketaan ja kirjataan.
author: Henrikan
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b15ca78da14068fd2f3275e7aff04852625db7ee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862508"
---
# <a name="register-sales-commissions"></a>Myyntiprovisioiden rekisteröinti

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten myyntiprovisiot lasketaan ja kirjataan. Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi. Suorita ennen tämän opastuksen aloittamista Määritä myyntikomission säännöt -opastus ja varmista, että sinulla on kaikki tarvittavat komissiolaskelma-asetukset.

Kirjaa muistiin asiakasnumerot ja nimiketunnukset, jotka olevat valinnut provisioprosessiin, ja luo niillä pyydettäessä myyntitilaus tässä opastuksessa.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Laskuta myyntitilaus, josta myyjä saa provision
1. Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset**.
2. Valitse **Uusi**.
3. Valitse **Asiakastili**-kentässä avattavasta valikosta haluamasi tietue.
4. Valitse **OK**.
5. Valitse toimintoruudussa **Asetukset**.
6. Valitse **Vaihda näyttö**.
7. Valitse **Otsikkonäkymä**.
8. Laajenna osa **Asetukset**.

    - **Myyntiryhmä**-kentän arvo vastaa ryhmää, johon on määritetty vähintään yksi myyntiedustaja. Ryhmän jäsenet saavat provisiot ennalta määritettyjen prosenttien ja jaon mukaisesti, kun tilaus lasketaan.   
    - Arvo kopioidaan asiakaskortista, mutta voit vaihtaa sen halutessasi.  
    - Myös myyntiryhmä kopioidaan myyntitilausriville. Voit muuttaa sitä niin, että se poikkeaa otsikon ja/tai rivien välisestä ryhmästä.  
    - **Provisioryhmä**-kentän arvo vastaa ryhmää, jonka olet luonut vähintään yhdelle asiakkaalle provisioiden seurantaa varten.   
    - Arvo kopioidaan asiakaskortista, mutta voit vaihtaa sen halutessasi.   

9. Valitse toimintoruudussa **Asetukset**.
10. Valitse **Vaihda näyttö**.
11. Valitse **Rivinäkymä**.
12. Valitse **Nimiketunnus**-kentän pudotusvalikosta nimike, jonka olet määrittänyt provisioille. 
13. Anna **Määrä**-kentässä numero. Kirjoita rivin nettosumma muistiin. Se vastaa myyntituottoa, joka on tässä esimerkissä provisiolaskelman peruste.  
14. Valitse **Tallenna**.
15. Valitse toimintoruudussa **Lasku**.
16. Valitse **Lasku**.
17. Laajenna **Parametrit**-osa.
18. Valitse **Määrä**-kentässä **Kaikki**.
19. Valitse **Kirjaus**-kentässä **Kyllä**.
20. Valitse **OK** ja valitse sitten seuraavassa ruudussa **OK**. Tapahtuman kirjaaminen kestää noin minuutin. Anna käsittelyn valmistua äläkä sulje sivua.  

## <a name="review-the-registered-sales-commissions"></a>Tarkastele rekisteröityjä myyntiprovisioita
1. Valitse toimintoruudussa **Lasku**, ja valitse sitten jälleen **Lasku**.
2. Valitse toimintoruudussa **Lasku**, ja valitse sitten **Provisiotapahtumat**.

    - **Yhteenveto**-välilehti sisältää rivit, jotka vastaavat laskutettuun myyntitilaukseen liitetyille myyntiedustajille maksettavia provisiosummia. Tarkastellaan tietoja tarkemmin.  
    - Jos määritit **Provisiomyynti**-ryhmän Määritä myyntiprovision säännöt -opastuksessa, kaksi myyjää saa myyntiprovisioita ja provisio jaetaan tasan heidän keskeen.  
    - Tässä esimerkissä provision kokonaismäärä lasketaan myyntituoton prosenttiosuutena (tilausrivin nettosumma).  
3. Sulje sivu.
4. Valitse **Tosite**. Voit tarkastella esimääritetyille provision kulu- ja ostoreskontratileille kirjattujen provisiosummien tositetapahtumia.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]