---
title: Nimikkeen tai raaka-aineen jäljittäminen
description: Tässä menettelyssä käsitellään, miten nimikkeen seurannalla voidaan selvittää, miten nimikkeitä tai raaka-aineita on käytetty tai ollaan käyttämässä.
author: pjacobse
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 044b098b24d8cdf8008824b7ed1359f2b0566a8f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961484"
---
# <a name="trace-an-item-or-raw-material"></a>Nimikkeen tai raaka-aineen jäljittäminen

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään, miten nimikkeen seurannalla voidaan selvittää, miten nimikkeitä tai raaka-aineita on käytetty tai ollaan käyttämässä. Tämän menettelyn avulla voit tunnistaa nimikkeen sekä seurata sitä takaisin lähteeseen ja sitten tuotannon ja myynnin kautta lopulliseen tuotteeseen. Prosessilla voit selvittää esimerkiksi, mitä asiakkaita tai myyntitilauksia se koski. Menettely käyttää USP2-yrityksen demotietoja.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Jäljitä nimike taaksepäin tiedossa olevaan eränumeroon
1. Valitse **siirtymisruudussa** **Moduulit > Inventoinnin- ja varastonhallinta > Kyselyt ja raportit > Seurantadimensiot > Nimikkeen seuranta**.
2. Valitse **Nimiketunnus**-kenttään "P9100".
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse **Eteen- tai taaksepäin** -kentässä "Taaksepäin".
5. Valitse **Eränumero**-kentässä 12-344-01.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Valitse **OK**.

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Tunnista nimike, seuraa sitä eteenpäin ja analysoi

Puun ylin solmu vastaa valitun nimikkeen ja erän käytettävissä olevaa määrää. Laajenna puun nimike, jotta voit paikantaa nimikkeen, jolle seuranta tulisi suorittaa.   
1. Laajenna puussa "alla kuvatut solmut ja valitse sitten viimeinen solmu".
    
    Laajenna: P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101 ja valitse sitten kyseinen solmu.     
2. Laajenna puussa "alla kuvattu solmu ja valitse sitten kyseinen solmu".
    
    Laajenna valitusta solmusta lähtien "M9103 ● Tuotantorivi B-000050 ● 12/9/2015 ●-160.00 lb ● Koko=70,Väri=OK, Toimipaikka=1, Varasto=10, Eränumero=App01" ja valitse sitten kyseinen solmu.  
3. Valitse **Seuraa solmusta**.
4. Valitse **Eteenpäin**.
5. Valitse **toimintoruudussa** **Jäljitys**.
    
    Seurantavaihtoehtoja on useita; ne tarjoavat tietoja asiakkaista, joihin seurattava nimike vaikuttaa sekä myyntitilauksista, jotka liittyvät nimikkeeseen, oli niitä lähetetty tai ei.   
6. Valitse **Asiakkaat**.
7. Sulje sivu.
8. Valitse **toimintoruudussa** **Jäljitys**.
9. Valitse **Lähetetyt myyntitilaukset**.
10. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]