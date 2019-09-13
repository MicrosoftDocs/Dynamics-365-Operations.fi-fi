---
title: Myyntisopimusten syöttäminen
description: Tässä aiheessa kerrotaan, miten luodaan myyntisopimus, jossa yksi asiakas sitoutuu ostamaan tuotteen sovitulla summalla tietyn ajan ja saa vastineeksi erikoisalennuksia.
author: omulvad
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7699f426c102b4ae2610db0851ddd127e514b652
ms.sourcegitcommit: 6545bef4584d72dd7789f2d3935cf00ac8f489b0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2019
ms.locfileid: "1871026"
---
# <a name="enter-sales-agreements"></a>Myyntisopimusten syöttäminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä aiheessa kerrotaan, miten luodaan myyntisopimus, jossa yksi asiakas sitoutuu ostamaan tuotteen sovitulla summalla tietyn ajan ja saa vastineeksi erikoisalennuksia. Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.


## <a name="set-up-sales-agreement-header"></a>Määritä myyntisopimuksen otsikko
1. Siirry siirtymisruudussa kohtaan **Moduulit > Myynti ja markkinointi > Myyntisopimukset > Myyntisopimukset**.
2. Valitse **Uusi**.
3. Valitse **Asiakastili**-kentässä avattavasta valikosta haluamasi tietue.
4. Valitse **Myyntisopimuksen luokittelu**-kentässä avattavasta valikosta haluamasi tietue.
5. Laajenna **Yleiset**-osa.
6. Valitse **Oletussitoumus**-kentässä **Tuotteen arvoon perustuva sitoumus**. Sitoumustyyppi on pakollinen ehto, joka on määritettävä sopimukseen määrittämään, miten sopimus toteutetaan. Voit määrittää neljän esimääritetyn tyypin avulla määränä tai arvona ilmaistavan asiakkaan sitoumuksen tavoitteen. Määräsitoumustyyppiä voidaan käyttää vain määritetyssä tuotteessa, mutta arvoperustaisia tyyppejä voi käyttää sekä määritettyjen että määrittämättömien tuotteiden myyntiin.  
7. Määritä **Vanhentumispäivä**-kentässä tuleva päivämäärä, jolloin haluat sopimuksen vanhentuvan.
8. Valitse **OK**.

## <a name="set-up-product-value-commitment-lines"></a>Määritä tuotteen arvon perustuvan sitoumuksen rivit
1. Valitse **Lisää rivi**.
2. Valitse **Nimiketunnus**-kentässä avattavasta valikosta haluttu tietue. Sopimukseen valittu sitoumustyyppi vaikuttaa siihen, mitä tietoja sopimusriveillä annetaan. Esimerkiksi arvoperustaisessa sopimuksessa on määritettävä kokonaisnettosumma (sovitussa valuutassa), jolla asiakas sitoutuu ostamaan sinulta tavaroita. Tässä esimerkissä rivin **Määrä**- ja **Yksikkö**-kentät eivät ole käytettävissä, koska olet luomassa sopimuksen, jossa asiakas ostaa tuotetta tietyn arvon mukaan.   
3. Anna **Nettosumma**-kenttään rahasumma, jolla asiakas on sitoutunut ostamaan.
4. Anna **Alennusprosentti**-kentässä prosenttiarvo, jota käytetään asiakkaan sopimukseen linkitetyillä myyntitilausriveillä.
5. Laajenna **Rivin erittely** -osa.
6. Valitse **Maksimi pakotetaan** -kentässä **Kyllä**.
    - **Maksimi pakotetaan** -asetuksen valinta tarkoittaa, että kaikkien sitoumuksen erikoishintoja, alennuksia ja/tai maksuehtoja käyttävien myyntitilausrivien yhteissumma ei saa ylittää sitoumuksessa määritettyä summaa.  
    - Vapautuksen vähimmäis- ja enimmäissummat määrittävät arvoalueen, joka on myytävä kussakin valittua sopimusta käyttävässä myyntitilauksessa.   
7. Laajenna **Myyntisopimuksen otsikko** -osa. Jos sopimuksen tilaksi ei ole valittu **Voimassa**, myyntitilauksia ei voi liittää sopimukseen eivätkä ne siten osallistu kyseisen sopimuksen täytäntöönpanoon. Voit muuttaa tilan manuaalisesti tässä vaiheessa. Tila kuitenkin muutetaan tavallisesti silloin, kun vahvistat asiakkaan sopimuksen.  
8. Valitse toimintoruudussa **Myyntisopimus**.
9. Valitse **Vahvistus**. Varmista, että **Merkitse sopimus voimassa olevaksi** -asetukseksi on valittu **Kyllä**.  
10. Valitse **Tulosta raportti** -kentässä **Kyllä**.
11. Valitse **OK**.
12. Sulje sivu. Sopimus on nyt voimassa. Voit aloittaa asiakkaan tilausten linkittämisen sopimukseen, jossa ne vastakirjataan sitoumustavoitteeseen.  

