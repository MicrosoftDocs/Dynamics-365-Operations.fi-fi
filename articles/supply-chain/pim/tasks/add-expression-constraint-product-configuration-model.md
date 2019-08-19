---
title: Lisää rajoituslauseke tuotemääritysmalliin
description: Tässä menettelyssä käsitellään, miten uusi rajoituslauseke lisätään tuotemääritysmalliin.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f67d912b3349d4b5dd861b97533a7722a2b02fa4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845134"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Lisää rajoituslauseke tuotemääritysmalliin

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään, miten uusi rajoituslauseke lisätään tuotemääritysmalliin. Se näyttää, miten voit määrätä, että kulmasuojausta on käytettävä kaiuttimessa, jos käyttäjä on valinnut metallin etusäleikköön. Menettely käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -komponenttia.


## <a name="create-an-expression-constraint"></a>Luo lausekerajoitus
1. Valitse Tuotevarianttimallin määritys.
2. Valitse Tuotekonfiguraation mallit.
3. Etsi haluamasi tietue luettelosta ja valitse se.
    * Tässä esimerkissä käytetään Korkealaatuinen kaiutin -mallia.  
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Laajenna Rajoitukset-osa.
6. ValitseLisää.
7. Valitse Luo.
8. Kirjoita arvo Nimi-kenttään.

## <a name="enter-expression"></a>Anna lauseke
1. Valitse Muokkaa lauseketta.
    * Jos vapautat käyttöliittymän tehtävätallenteen tässä vaiheessa, voit muodostaa rajoituslausekkeen IntelliSensen ja symboliluettelon avulla.  
2. Lisää ConstraintBody-kenttään Implies[FrontGrill=="Metal", CornerProtection].
    * Tämän lausekkeen logiikka ilmaisee, että jos etusäleikkö on metallia, sitten kulmasuojausvaihtoehto on valittava.  
3. Valitse Vahvista.
    * Vahvistustoiminto suoritetaan rajoitelausekkeessa, jossa se tarkistaa syntaksivirheet.  
4. Valitse Sulje.
5. Valitse OK.

