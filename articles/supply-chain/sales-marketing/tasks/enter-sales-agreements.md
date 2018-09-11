--- 
title: Anna myyntisopimukset
description: "Tässä menettelyssä näytetään, miten luodaan myyntisopimus, jossa yksi asiakas sitoutuu ostamaan tuotteen sovitulla summalla tietyn ajan ja saa vastineeksi erikoisalennuksia."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8c11164f7edb8e05b93f3c58b9707c0bf2482228
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="enter-sales-agreements"></a>Anna myyntisopimukset

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä näytetään, miten luodaan myyntisopimus, jossa yksi asiakas sitoutuu ostamaan tuotteen sovitulla summalla

tietyn ajan ja saa vastineeksi erikoisalennuksia. Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.


## <a name="set-up-sales-agreement-header"></a>Määritä myyntisopimuksen otsikko
1. Valitse Myynti ja markkinointi > Myyntisopimukset > Myyntisopimukset.
2. Valitse Uusi.
3. Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Avaa haku napsauttamalla Myyntisopimuksen luokitus -kentässä avattavan valikon painiketta.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Laajenna Yleinen-osa.
9. Valitse Oletussitoumus-kentässä Tuotteen arvoon perustuva sitoumus.
    * Sitoumustyyppi on pakollinen ehto, joka on määritettävä sopimukseen määrittämään, miten sopimus toteutetaan. Voit määrittää neljän esimääritetyn tyypin avulla määränä tai arvona ilmaistavan asiakkaan sitoumuksen tavoitteen. Määräsitoumustyyppiä voidaan käyttää vain määritetyssä tuotteessa, mutta arvoperustaisia tyyppejä voi käyttää sekä määritettyjen että määrittämättömien tuotteiden myyntiin.  
10. Määritä Vanhentumispäivä-kentässä tuleva päivämäärä, jolloin haluat sopimuksen vanhentuvan.
11. Valitse OK.

## <a name="set-up-product-value-commitment-lines"></a>Määritä tuotteen arvon perustuvan sitoumuksen rivit
1. Valitse Lisää rivi.
2. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Sopimukseen valittu sitoumustyyppi vaikuttaa siihen, mitä tietoja sopimusriveillä annetaan. Esimerkiksi arvoperustaisessa sopimuksessa on määritettävä kokonaisnettosumma (sovitussa valuutassa), jolla asiakas sitoutuu ostamaan sinulta tavaroita. Tässä esimerkissä rivin Määrä- ja Yksikkö-kentät eivät ole käytettävissä, koska olet luomassa sopimuksen, jossa asiakas ostaa tuotetta tietyn arvon mukaan.   
5. Anna Nettosumma-kenttään rahasumma, jolla asiakas on sitoutunut ostamaan.
6. Anna Alennusprosentti-kentässä prosenttiarvo, jota käytetään asiakkaan sopimukseen linkitetyillä myyntitilausriveillä.
7. Laajenna Rivin erittely -osa.
8. Valitse Maksimi pakotetaan -kentässä Kyllä.
    * Maksimi pakotetaan -asetuksen valinta tarkoittaa, että kaikkien sitoumuksen erikoishintoja, alennuksia ja/tai maksuehtoja käyttävien myyntitilausrivien yhteissumma ei saa ylittää sitoumuksessa määritettyä summaa.  
    * Vapautuksen vähimmäis- ja enimmäissummat määrittävät arvoalueen, joka on myytävä kussakin valittua sopimusta käyttävässä myyntitilauksessa.   
9. Laajenna Myyntisopimuksen otsikko -osa.
    * Jos sopimuksen tilaksi ei ole valittu Voimassa, myyntitilauksia ei voi liittää sopimukseen eivätkä ne siten osallistu kyseisen sopimuksen täytäntöönpanoon. Voit muuttaa tilan manuaalisesti tässä vaiheessa. Tila kuitenkin muutetaan tavallisesti silloin, kun vahvistat asiakkaan sopimuksen.  
10. Valitse toimintoruudussa Myyntisopimus.
11. Valitse Vahvistus.
    * Varmista, Merkitse sopimus voimassa olevaksi -asetukseksi on valittu Kyllä.  
12. Valitse Tulosta raportti -kentässä Kyllä.
13. Valitse OK.
14. Sulje sivu.
    * Sopimus on nyt voimassa oleva ja voit aloittaa asiakkaan tilausten linkittämisen sopimukseen, jossa ne vastakirjataan sitoumustavoitteeseen.  


