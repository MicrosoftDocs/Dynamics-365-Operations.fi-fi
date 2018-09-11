--- 
title: Vahvista myyntitilaukset
description: "Seuraavassa menettelyssä selvitetään, miten myyntitilaukset vahvistetaan."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cab69222c5004e6a62c632a9e85085403434ffd
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="confirm-sales-orders"></a>Vahvista myyntitilaukset

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavassa menettelyssä selvitetään, miten myyntitilaukset vahvistetaan. Näet, miten yksi tilaus vahvistetaan. Näet myös, miten useita tilauksia voi vahvistaa samanaikaisesti. Yleensä myyntitilauksen käsittelijä tekee nämä tehtävät. Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi. Varmista ennen aloittamista, että samalla asiakkaalla on useita avoimia myyntitilauksia. Jos käytössä on USMF, käytä asiakasta US-027.


## <a name="confirm-a-single-sales-order"></a>Vahvista yksi myyntitilaus
1. Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.
2. Etsi ja valitse luettelosta vahvistettava tilaus.
3. Avaa valittu tilaus napsauttamalla myyntitilauksen numeron linkkiä.
4. Valitse toimintoruudussa Myynti.
5. Valitse Vahvista myyntitilaus.
6. Laajenna tai tiivistä Parametrit-osa.
    * Varmista, että kirjauksen Kyllä-kenttä on aktiivinen.  
7. Valitse Tulosta vahvistus -vaihtoehdoksi Kyllä.
    * Tarkista luottoraja -kenttä määrittää menetelmän, jolla asiakkaan jäljellä oleva luotto lasketaan. Oletusarvoisesti se kopioidaan Myyntireskontran parametrit -sivulta. Jos haluat ohittaa luottorajatarkistuksen tietyn myyntitilauksen vahvistuksessa, valitse Tarkista luottoraja -arvoksi Ei mitään. Muista kuitenkin, että vaikka tämän kentän arvo on Ei mitään, luottorajatarkistus suoritetaan, jos asiakkaan päätiedoissa on valittu Pakollinen luottoraja -vaihtoehto.  
8. Valitse OK.
9. Valitse Kyllä.
10. Sulje sivu.
11. Valitse toimintoruudussa Asetukset.
12. Valitse Vaihda näkymä.
13. Valitse Otsikkonäkymä.
    * Kun tilaus on vahvistettu, asiakirjan tilaksi määritetään Vahvistus.  
14. Valitse toimintoruudussa Myynti.
15. Valitse Myyntitilausvahvistus.
16. Sulje sivu.

## <a name="confirm-multiple-sales-orders-at-once"></a>Vahvista useita myyntitilauksia samanaikaisesti
1. Valitse Myynti ja markkinointi > Myyntitilaukset > Tilausvahvistus > Vahvista myyntitilaus.
2. Klikkaa Valitse.
3. Etsi ja valitse Alueet-välilehdessä tietue, joka viittaa Asiakastili-kenttään.
4. Avaa haku valitsemalla Ehdot-kentässä avattavan valikon painike.
5. Etsi ja valitse luettelosta asiakastili, jossa on useita tilauksia, jotka haluat joukkovahvistaa.
    * Jos käytössä on USMF, voit valita tilin US-027.  
6. Valitse OK.
    * Yhteenveto-välilehdessä on luettelo kyselyehtoja vastaavista tilauksista. Ne sisältyvät vahvistukseen.  
    * Päivitysyhteenveto mille: -kenttä määrittää parametrin, jonka mukaan useista tilauksista tehdään yhteenveto yhteen vahvistusasiakirjaan. Oletusarvoisesti asetus kopioidaan Myyntireskontran parametrit -sivun Päivitysyhteenvedon oletusarvot -asetuksesta.  
7. Valitse Päivitysyhteenveto mille: -kentässä Tilaus.
    * Yhteenvetopäivitysten luontiin tarvitaan ainakin parametrit Laskutustili ja Valuutta. Näin ollen yhteenvetopäivityksiä, joissa on eri laskutustilit ja valuutat, ei sallita. Yhteenvedon päivitysparametrit -sivulla voi määrittää lisäparametreja. Sivun voi avata Myyntireskontran parametrit -sivulta.  
8. Avaa haku napsauttamalla Myyntitilaus-kentässä avattavan valikon painiketta.
9. Valitse luettelossa tilausnumero, jonka haluat yhteenvetotilaukseksi.
10. Valitse Järjestä.
11. Valitse OK.
12. Valitse OK.


