---
title: "Nimikkeen tai raaka-aineen jäljittäminen"
description: "Tässä menettelyssä käsitellään, miten nimikkeen seurannalla voidaan selvittää, miten nimikkeitä tai raaka-aineita on käytetty tai ollaan käyttämässä."
author: pjacobse
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: c4b093af672b2d4e1a2c91cd55470f9072d992c3
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="trace-an-item-or-raw-material"></a>Nimikkeen tai raaka-aineen jäljittäminen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään, miten nimikkeen seurannalla voidaan selvittää, miten nimikkeitä tai raaka-aineita on käytetty tai ollaan käyttämässä. Tämän menettelyn avulla voit tunnistaa nimikkeen sekä seurata sitä takaisin lähteeseen ja sitten tuotannon ja myynnin kautta lopulliseen tuotteeseen. Prosessilla voit selvittää esimerkiksi, mitä asiakkaita tai myyntitilauksia se koski. Menettely käyttää USP2-yrityksen demotietoja.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Jäljitä nimike taaksepäin tiedossa olevaan eränumeroon
1. Valitse Inventoinnin- ja varastonhallinta > Kyselyt ja raportit > Seurantadimensiot > Nimikkeen seuranta.
2. Valitse Nimiketunnus-kenttään P9100.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse Eteen- tai taaksepäin -kentässä Taaksepäin.
5. Valitse Eränumero-kentässä as 12-344-01.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Valitse OK.

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Tunnista nimike, seuraa sitä eteenpäin ja analysoi
    * Puun ylin solmu vastaa valitun nimikkeen ja erän käytettävissä olevaa määrää. Laajenna puun nimike, jotta voit paikantaa nimikkeen, jolle seuranta tulisi suorittaa.   
1. Laajenna puussa "alla kuvatut solmut ja valitse sitten viimeinen solmu".
    * Laajenna: P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101 ja valitse sitten kyseinen solmu.     
2. Laajenna puussa "alla kuvattu solmu ja valitse sitten kyseinen solmu".
    * Laajenna valitusta solmusta lähtien "M9103 ● Tuotantorivi B-000050 ● 12/9/2015 ●-160.00 lb ● Koko=70,Väri=OK, Toimipaikka=1, Varasto=10, Eränumero=App01" ja valitse sitten kyseinen solmu.  
3. Valitse Seuraa solmusta.
4. Valitse Eteenpäin.
5. Valitse toimintoruudussa Jäljitys.
    * Seurantavaihtoehtoja on useita; ne tarjoavat tietoja asiakkaista, joihin seurattava nimike vaikuttaa sekä myyntitilauksista, jotka liittyvät nimikkeeseen, oli niitä lähetetty tai ei.   
6. Valitse Asiakkaat.
7. Sulje sivu.
8. Valitse toimintoruudussa Jäljitys.
9. Valitse Lähetetyt myyntitilaukset.
10. Sulje sivu.
