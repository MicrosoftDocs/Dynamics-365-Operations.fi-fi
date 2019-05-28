---
title: Rekisteröi myyntiprovisiot
description: Tässä menettelyssä käsitellään, miten myyntiprovisiot lasketaan ja rekisteröidään.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c39b2fcf521106dfb58466bc45a316c0b506345
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560709"
---
# <a name="register-sales-commissions"></a>Rekisteröi myyntiprovisiot

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään, miten myyntiprovisiot lasketaan ja rekisteröidään. Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi. Suorita ennen tämän opastuksen aloittamista Määritä myyntikomission säännöt -opastus ja varmista, että sinulla on kaikki tarvittavat komissiolaskelma-asetukset.

Kirjaa muistiin asiakasnumerot ja nimiketunnukset, jotka olevat valinnut provisioprosessiin, ja luo niillä pyydettäessä myyntitilaus tässä opastuksessa.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Laskuta myyntitilaus, josta myyjä saa provision
1. Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.
2. Valitse Uusi.
3. Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse OK.
7. Valitse toimintoruudussa Asetukset.
8. Valitse Vaihda näkymä.
9. Valitse Otsikkonäkymä.
10. Laajenna osa Asetukset.
    * Myyntiryhmä-kentän arvo vastaa ryhmää, johon on määritetty vähintään yksi myyntiedustaja. Ryhmän jäsenet saavat provisiot ennalta määritettyjen prosenttien ja jaon mukaisesti, kun tilaus lasketaan.   Arvo kopioidaan asiakaskortista, mutta voit vaihtaa sen halutessasi.  Myös myyntiryhmä kopioidaan myyntitilausriville. Voit muuttaa sitä niin, että se poikkeaa otsikon ja/tai rivien välisestä ryhmästä.  
    * Provisioryhmä-kentän arvo vastaa ryhmää, jonka olet luonut vähintään yhdelle asiakkaille provisioiden seurantaa varten.   Arvo kopioidaan asiakaskortista, mutta voit vaihtaa sen halutessasi.   
11. Valitse toimintoruudussa Asetukset.
12. Valitse Vaihda näkymä.
13. Valitse Rivinäkymä.
14. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
15. Valitse luettelosta provisioille määritetty nimike. 
16. Kirjoita numero Määrä-kenttään.
    * Kirjoita rivin nettosumma muistiin. Se vastaa myyntituottoa, joka on tässä esimerkissä provisiolaskelman peruste.  
17. Valitse Tallenna.
18. Valitse toimintoruudussa Lasku.
19. Valitse Lasku.
20. Laajenna Parametrit-osa.
21. Valitse Määrä-kentässä Kaikki.
22. Valitse Kirjaus-kentässä Kyllä.
23. Valitse OK.
24. Valitse OK.
    * Tapahtuman kirjaaminen kestää noin minuutin. Anna käsittelyn valmistua äläkä sulje sivua.  

## <a name="review-the-registered-sales-commissions"></a>Tarkastele rekisteröityjä myyntiprovisioita
1. Valitse toimintoruudussa Lasku.
2. Valitse Lasku.
3. Valitse toimintoruudussa Lasku.
4. Valitse Provisiotapahtumat.
    * Yhteenveto-välilehti sisältää rivit, jotka vastaavat laskutettuun myyntitilaukseen liitetyille myyntiedustajille maksettavia provisiosummia. Tarkastellaan tietoja tarkemmin.     
    * Jos määritit Provisiomyynti-ryhmän Määritä myyntiprovision säännöt -opastuksessa, kaksi myyjää saa myyntiprovisioita ja provisio jaetaan tasan heidän keskeen.  
    * Tässä esimerkissä provision kokonaismäärä lasketaan myyntituoton prosenttiosuutena (tilausrivin nettosumma).   
5. Sulje sivu.
6. Valitse Tosite.
    * Voit tarkastella esimääritetyille provision kulu- ja ostoreskontratileille kirjattujen provisiosummien tositetapahtumia.  

