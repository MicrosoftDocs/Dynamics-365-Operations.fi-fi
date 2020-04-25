---
title: Myyntisopimusten syöttäminen
description: Tässä aiheessa kerrotaan, miten luodaan myyntisopimus, jossa yksi asiakas sitoutuu ostamaan tuotteen sovitulla summalla tietyn ajan ja saa vastineeksi erikoisalennuksia.
author: omulvad
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 723621f61a237d4b390271e65bce204c44ee4fc2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204329"
---
# <a name="enter-sales-agreements"></a>Myyntisopimusten syöttäminen

[!include [banner](../../includes/banner.md)]

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

