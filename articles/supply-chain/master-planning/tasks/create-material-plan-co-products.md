---
title: Oheistuotteiden materiaalisuunnitelman luominen
description: Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a87935f8f30d909f1a6a62ed7be00c83476a36a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214367"
---
# <a name="create-a-material-plan-for-co-products"></a>Oheistuotteiden materiaalisuunnitelman luominen

[!include [banner](../../includes/banner.md)]

Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita. Tämän menettelyn luomisessa käytetty esittely-yritys on USP2.


## <a name="create-requirement-for-a-co-product"></a>Oheistuotteen tarpeen luominen
1. Siirry oletuskoontinäyttöön.
2. Valitse Myyntitilausten käsittely ja kysely.
3. Valitse Uusi.
4. Valitse Myyntitilaus.
5. Kirjoita arvo Asiakastili-kenttään.
    * Esimerkki: US-001  
6. Valitse OK.
7. Kirjoita arvo Nimiketunnus-kenttään.
    * Esimerkki: P6003  
8. Kirjoita numero Määrä-kenttään.
    * Esimerkki: 50 000  
9. Valitse Tallenna.

## <a name="create-a-material-plan-for-co-products"></a>Rinnakkaistuotteiden materiaalisuunnitelman luominen
1. Sulje sivu.
2. Sulje sivu.
3. Valitse Pääsuunnittelu.
4. Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Esimerkki: MasterPlan  
6. Valitse Suorita.
7. Laajenna tai tiivistä Sisällytettävät tietueet -osa.
8. Valitse Suodatin.
9. Valitse luettelosta rivi Nimiketunnus-kentälle.
10. Kirjoita arvo Ehdot-kenttään.
    * Esimerkki: P6003  
11. Valitse OK.
12. Valitse OK.
13. Valitse Suunnitellut tilaukset.
14. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla P6000.
    * Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.  
15. Merkitse valittu rivi luettelossa.
    * Valitse mikä tahansa suodattimen palauttamista riveistä.  
16. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
17. Laajenna tai tiivistä Tarvekohdistus-osa.
18. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.  
19. Sulje sivu.

## <a name="create-requirement-for-a-co-product"></a>Oheistuotteen tarpeen luominen
1. Siirry oletuskoontinäyttöön.
2. Valitse Myyntitilausten käsittely ja kysely.
3. Valitse Uusi.
4. Valitse Myyntitilaus.
5. Kirjoita arvo Asiakastili-kenttään.
    * Esimerkki: US-001  
6. Valitse OK.
7. Kirjoita arvo Nimiketunnus-kenttään.
    * Esimerkki: P6003  
8. Kirjoita numero Määrä-kenttään.
    * Esimerkki: 50 000  
9. Valitse Tallenna.

## <a name="create-a-material-plan-for-co-products"></a>Rinnakkaistuotteiden materiaalisuunnitelman luominen
1. Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.
2. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Esimerkki: MasterPlan  
3. Valitse Suorita.
4. Laajenna tai tiivistä Sisällytettävät tietueet -osa.
5. Valitse Suodatin.
6. Valitse luettelosta rivi Nimiketunnus-kentälle.
7. Kirjoita arvo Ehdot-kenttään.
    * Esimerkki: P6003  
8. Valitse OK.
9. Valitse OK.
10. Valitse Suunnitellut tilaukset.
11. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla P6000.
    * Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.  
12. Merkitse valittu rivi luettelossa.
    * Valitse mikä tahansa suodattimen palauttamista riveistä.  
13. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
14. Laajenna tai tiivistä Tarvekohdistus-osa.
15. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.  
16. Sulje sivu.
17. Valitse Pääsuunnittelu.
18. Valitse Pääsuunnittelu > Määritys > Pääsuunnittelun parametrit.
19. Valitse Ei-vaihtoehto Poista käytöstä kaikki suunnitteluprosessit -kentässä.
20. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]