---
title: Lisää rajoituslauseke tuotemääritysmalliin
description: Tässä menettelyssä käsitellään, miten uusi rajoituslauseke lisätään tuotemääritysmalliin.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81026d8622d3f03b3b87747800f4845cda823569
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256156"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Lisää rajoituslauseke tuotemääritysmalliin

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]