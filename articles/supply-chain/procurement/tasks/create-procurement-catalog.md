---
title: Luo tuotteiden hankintaluettelo
description: Tässä ohjeaiheessa kerrotaan, miten voit luoda hankintaluettelon.
author: mkirknel
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55bc7479ca9ba3ca86e23b5bee106ef169c40077
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836378"
---
# <a name="create-a-procurement-catalog"></a>Luo tuotteiden hankintaluettelo

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä ohjeaiheessa kerrotaan, miten voit luoda hankintaluettelon. Yleensä hankinta-asiantuntijat suorittavat tämän tehtävän. Opit myös, miten työntekijät voivat käyttää luetteloa ostoehdotuksien luonnissa. Järjestelmässä on oltava hankintaluokkahierarkia ennen luettelon luomista. Hierarkia periytyy uuteen luetteloon, kuten myös kaikki hierarkian tuotteet. Voit käyttää tätä opasta USMF-demoyrityksessä, jossa hankintaluokkahierarkia sekä menettelyn ohjeissa käytetyt esimerkit ovat saatavilla.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Varmista, että hankintaluokkahierarkia on olemassa
1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Hankintaluokat**. Hankintaluokkahierarkia sisältyy USMF-demoyrityksen tietoihin ja tuotteet on lisätty **Toimiston koneet/Tietokoneet** -luokkaan. Jos käytät menettelyä tehtäväoppaana, sinun on ehkä poistettava lukitus, jos haluat selata luokkaa. Jos hierarkia ei ole käytettävissä, voit luoda sen napsauttamalla **Uusi**-painiketta. Tämän voi tehdä vain kerran.  
2. Sulje sivu.

## <a name="create-a-catalog"></a>Luo luettelo
1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Luettelot > Hankintaluettelot**.
2. Avaa valintaikkuna valitsemalla **Uusi tuotteiden hankintaluettelo**.
3. Kirjoita arvo **Nimi**-kenttään.
4. Valitse **OK**.
5. Laajenna puussa **CORP PROCUREMENT CATEGORIES**.
6. Laajenna puussa **OFFICE MACHINES**.
7. Valitse puussa **Tietokoneet**.

  - Hankintaluokan tuotteet näytetään luettelossa. Jos haluat lisätä tuotteen luokkaan, tämä on tehtävä **Hankintaluokkahierarkia**-sivulla tai **Nimiketiedot**-sivulla.  
  - **Oletus**-päivitystyyppi määrittää, ovatko uudet, hankintaluokkahierarkiaan lisätyt tuotteet välittömästi näkyvissä luettelossa. Jos päivityksen tyyppinä on **Dynaaminen**, muutokset näkyvät heti. Jos päivitystyyppi on **Staattinen**, uudet tuotteet näkyvät luettelon käyttäjille vasta, kun se on julkaistu uudelleen. **Julkaise**-toiminto on käytettävissä sivun yläosan toimintoruudussa. Jos tuotteita poistetaan hankintaluokkahierarkiasta, muutos näkyy heti **Oletus**-päivitystyypin kentän arvosta huolimatta.  

8. Valitse toimintoruudussa **Luettelonavigointi** ja varmista, että **Ota käyttöön** on valittuna.
9. Valitse **Aktivoi luettelo**.
10. Sulje sivu.

## <a name="make-the-catalog-visible"></a>Tee luettelosta näkyvä
1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Asetukset > Käytännöt > Ostokäytännöt**.
2. Valitse **hankintakäytäntö USMF**. Sinun on valittava ostokäytäntö yritykselle, johon käyttäjäprofiiliisi liitetty työntekijä saa tilata tuotteita. USMF-demoyrityksen tiedoissa järjestelmänvalvoja on liitetty työntekijään nimeltä **Julia Funderburk**, joka on USMF:n oletustilaaja tuotteille.  
3. Valitse juuri luomasi luettelo.
4. Valitse **OK**.

## <a name="use-the-catalog"></a>Käytä luetteloa
1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Ostoehdotukset > Kaikki ostoehdotukset**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Nimi**-kenttään.
4. Valitse **OK**.
5. Valitse **Lisää tuotteita**.
6. Etsi haluamasi tietue luettelosta ja valitse se. Voit käyttää tuotteiden suodattamiseen luokkahierarkiaa vasemmalla tai luettelon yläosassa olevaa suodatinta.  
7. Valitse **Lisää riveihin**.
8. Valitse **OK**.

