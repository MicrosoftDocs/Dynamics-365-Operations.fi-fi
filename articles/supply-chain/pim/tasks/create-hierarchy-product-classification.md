---
title: Tuotteiden luokitteluhierarkian luominen
description: Tässä menettelyssä selvitetään, miten uusi luokkahierarkia luodaan, ja määritetään kauppatavarahierarkian tyyppi.
author: ShylaThompson
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74be72ac5787273e13692abdb9db18be4c5ccc08
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966952"
---
# <a name="create-a-hierarchy-of-product-classification"></a>Tuotteiden luokitteluhierarkian luominen

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä selvitetään, miten uusi luokkahierarkia luodaan, ja määritetään kauppatavarahierarkian tyyppi. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu luokkapäällikölle.


## <a name="create-the-new-category-hierarchy"></a>Luo uusi luokkahierarkia
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Asetukset > Luokat ja määritteet > Luokkahierarkiat**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Nimi**-kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Luo**.

## <a name="build-the-hierarchy"></a>Luo hierarkia
1. Valitse **Uusi** luokkasolmu.
2. Kirjoita arvo **Nimi**-kenttään.
3. Kirjoita **Koodi**-kenttään arvo.
4. Kirjoita **Kutsumanimi**-kenttään arvo.
5. Valitse **Uusi** luokkasolmu.
6. Kirjoita arvo **Nimi**-kenttään.
7. Kirjoita **Koodi**-kenttään arvo.
8. Kirjoita **Kutsumanimi**-kenttään arvo.
9. Valitse **Uusi** luokkasolmu.
10. Kirjoita arvo **Nimi**-kenttään.
11. Kirjoita **Koodi**-kenttään arvo.
12. Kirjoita **Kutsumanimi**-kenttään arvo.
13. Valitse **Uusi** luokkasolmu.
14. Kirjoita arvo **Nimi**-kenttään.
15. Kirjoita **Koodi**-kenttään arvo.
16. Kirjoita **Kutsumanimi**-kenttään arvo.
17. Sulje sivu.

## <a name="classify-the-hierarchy"></a>Luokittele hierarkia
1. Etsi haluamasi tietue luettelosta ja valitse se.
2. Valitse **toimintoruudussa** **Luokkahierarkia**.
3. Valitse **Liitä hierarkiatyyppi**.
4. Valitse **Uusi**.
5. Valitse **Luokkahierarkian tyyppi** -kentässä vaihtoehto. Valitse **Tuoteluokituksen luokkahierarkian tyypin kauppatavarakoodi**.  
6. Avaa haku napsauttamalla **Luokkahierarkia**-kentässä avattavan valikon painiketta.
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]