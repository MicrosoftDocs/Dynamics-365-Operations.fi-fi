---
title: Tilirakenteiden luonti
description: Tässä opastuksessa käsitellään tilirakenteen luominen.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed8ce37ab642277ff843e6320a880fac40d41acb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235786"
---
# <a name="create-account-structures"></a>Tilirakenteiden luonti

[!include [banner](../../includes/banner.md)]

Tässä opastuksessa käsitellään tilirakenteen luominen. Vaiheissa käytetään esittely-tietojen USMF-yritystä.

1. Valitse **Siirtymisruutu > Moduulit > Kirjanpito > Tilikartta > Rakenteet > Tilirakenteiden konfigurointi**.
2. Avaa pudotusvalikkoikkuna valitsemalla **toimintoruudussa** **Uusi**.
3. Kirjoita **Tilirakenne**-kenttään nimi, joka kuvailee tilirakenteen tarkoitusta.
4. Kirjoita **Kuvaus**-kenttään kuvaus, joka määrittää tilirakenteen tarkoituksen.
5. Valitse **Luo**.
6. Valitse **Segmentit ja sallitut arvot**-kohdasta **Lisää segmentti.**
7. Valitse dimensioluettelossa tilirakenteeseen lisättävä dimensio.
8. Valitse luettelon lopussa **Lisää segmentti**.
9. Toista vaiheet 6-9 tarpeen mukaan.
10. Voit muokata sallittuja arvoja valitsemalla segmentin **Sallitun arvon tiedot** -osassa.
    Napsauta esimerkiksi **Päätili**-kenttää.  
11. Valitse **Käyttäjä**-kentässä vaihtoehto, kuten on välillä ja sisältää.
12. Kirjoita arvo **Arvo**-kenttään. Esimerkki: 600000.  
13. Kirjoita **kautta**-kenttään arvo. Esimerkki: 699999.  
14. Valitse **Sallitun arvon tiedot** -osassa **Käytä**.
15. Toista vaiheet 10-15 tarpeen mukaan.  
16. Valitse **Sallitun arvon tiedot** -osassa **Lisää uusia kriteerejä**.
17. Valitse Käyttäjä-kentässä vaihtoehto, kuten on välillä ja sisältää.
18. Kirjoita arvo **Arvo**-kenttään. Esimerkki: 033.  
19. Kirjoita **kautta**-kenttään arvo. Esimerkki: 034.  
20. Valitse **Käytä**.
21. Voit muokata sallittuja arvoja valitsemalla ruudukossa segmentin. Esimerkki: Kustannuspaikka.  
22. Kirjoita **CostCenter**-kenttään arvo. Esimerkki: 007..021.  
23. Valitse **Segmentit ja sallitut arvot**-kohdasta **Lisää.**
24. Kirjoita **MainAccount**-kenttään arvo. Esimerkki: 600000..699999  
25. Voit muokata sallittuja arvoja valitsemalla ruudukossa segmentin. Esimerkki: Osasto.  
26. Kirjoita Osasto-kenttään arvo. Esimerkki: 032.  
27. Kirjoita CostCenter-kenttään arvo. Esimerkki: 086.  
28. Valitse **toimintoruudussa** **Vahvista**.
29. Valitse **toimintoruudussa** **Aktivoi**.
30. Valitse **Aktivoi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]