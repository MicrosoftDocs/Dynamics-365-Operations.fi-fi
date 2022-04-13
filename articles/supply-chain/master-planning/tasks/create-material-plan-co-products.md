---
title: Oheistuotteiden materiaalisuunnitelman luominen
description: Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27bba54db915b7ccc31fda43a00a8c9435493e07
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469530"
---
# <a name="create-a-material-plan-for-co-products"></a>Oheistuotteiden materiaalisuunnitelman luominen

[!include [banner](../../includes/banner.md)]

Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita. Tämän menettelyn luomisessa käytetty esittely-yritys on USP2.

## <a name="create-requirement-for-a-co-product"></a>Oheistuotteen tarpeen luominen

1. Valitse **Myynti ja markkinointi \> Työtilat \> Myyntitilausten käsittely ja kysely**.
1. Valitse **Uusi**.
1. Valitse **Myyntitilaus**.
1. Kirjoita arvo **Asiakastili**-kenttään.
    * Esimerkki: US-001  
1. Valitse **OK**.
1. Kirjoita arvo **Nimiketunnus**-kenttään.
    * Esimerkki: P6003  
1. Anna **Määrä**-kentässä numero.
    * Esimerkki: 50 000  
1. Valitse **Tallenna**.

## <a name="create-a-material-plan-for-co-products"></a>Rinnakkaistuotteiden materiaalisuunnitelman luominen

1. Sulje sivu.
1. Sulje sivu.
1. Valitse **Pääsuunnittelu**.
1. Avaa haku valitsemalla **Suunnitelma**-kentässä avattavan valikon painike.
1. Valitse luettelossa valitulla rivillä oleva linkki.
    * Esimerkki: MasterPlan  
1. Valitse **Suorita**.
1. Laajenna tai tiivistä **Sisällytettävät tietueet** -osa.
1. Valitse **Suodata**.
1. Valitse luettelosta rivi kohdalle **Kenttä** = *Nimiketunnus*.
1. Kirjoita arvo **Ehdot**-kenttään.
    * Esimerkki: P6003  
1. Valitse **OK**.
1. Valitse **OK**.
1. Valitse **Suunnitellut tilaukset**.
1. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa **Nimiketunnus**-kenttää arvolla P6000.
    * Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.  
1. Merkitse valittu rivi luettelossa.
    * Valitse mikä tahansa suodattimen palauttamista riveistä.  
1. Valitse luettelossa valitulla rivillä oleva linkki.
1. Laajenna **Tarvekohdistus**-osa.
1. Valitse luettelossa valitulla rivillä oleva linkki.
    * Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.  
1. Sulje sivu.

## <a name="create-a-second-requirement-for-a-co-product"></a>Oheistuotteen toisen tarpeen luominen

1. Valitse **Myynti ja markkinointi \> Työtilat \> Myyntitilausten käsittely ja kysely**.
1. Valitse **Uusi**.
1. Valitse **Myyntitilaus**.
1. Kirjoita arvo **Asiakastili**-kenttään.
    * Esimerkki: US-001  
1. Valitse **OK**.
1. Kirjoita arvo **Nimiketunnus**-kenttään.
    * Esimerkki: P6003  
1. Anna **Määrä**-kentässä numero.
    * Esimerkki: 50 000  
1. Valitse **Tallenna**.

## <a name="create-a-second-material-plan-for-co-products"></a>Rinnakkaistuotteiden toisen materiaalisuunnitelman luominen

1. Avaa haku valitsemalla **Suunnitelma**-kentässä avattavan valikon painike.
2. Valitse luettelossa valitulla rivillä oleva linkki.
    * Esimerkki: MasterPlan  
3. Valitse **Suorita**.
4. Laajenna tai tiivistä **Sisällytettävät tietueet** -osa.
5. Valitse **Suodata**.
6. Valitse luettelosta rivi kohdalle **Kenttä** = *Nimiketunnus*.
7. Kirjoita arvo *Ehdot*-kenttään.
    * Esimerkki: P6003  
8. Valitse **OK**.
9. Valitse **OK**.
10. Valitse **Suunnitellut tilaukset**.
11. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa **Nimiketunnus**-kenttää arvolla P6000.
    * Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.  
12. Merkitse valittu rivi luettelossa.
    * Valitse mikä tahansa suodattimen palauttamista riveistä.  
13. Valitse luettelossa valitulla rivillä oleva linkki.
14. Laajenna tai tiivistä **Tarvekohdistus**-osa.
15. Valitse luettelossa valitulla rivillä oleva linkki.
    * Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.  
16. Sulje sivu.
17. Valitse **Pääsuunnittelu**.
18. Valitse **Pääsuunnittelu \> Määritys \> Pääsuunnittelun parametrit**.
19. Valitse *Ei*-vaihtoehto **Poista käytöstä kaikki suunnitteluprosessit** -kentässä.
20. Sulje sivu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]