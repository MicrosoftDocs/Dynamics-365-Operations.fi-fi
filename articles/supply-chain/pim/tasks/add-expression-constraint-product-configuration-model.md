---
title: Lisää rajoituslauseke tuotemääritysmalliin
description: Tässä menettelyssä käsitellään, miten uusi rajoituslauseke lisätään tuotemääritysmalliin.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77e8b991a2615a8f5d238acc4655f231edb6ca98
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569646"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Lisää rajoituslauseke tuotemääritysmalliin

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään, miten uusi rajoituslauseke lisätään tuotemääritysmalliin. Se näyttää, miten voit määrätä, että kulmasuojausta on käytettävä kaiuttimessa, jos käyttäjä on valinnut metallin etusäleikköön. Menettely käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -komponenttia.

## <a name="create-an-expression-constraint"></a>Luo lausekerajoitus

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.
3. Etsi haluamasi tietue luettelosta ja valitse se.
    * Tässä esimerkissä käytetään Korkealaatuinen kaiutin -mallia.  
4. Valitse luettelossa valitulla rivillä oleva linkki.
5. Laajenna **Rajoitukset**-osa.
6. Valitse **Lisää**.
7. Valitse **Luo**.
8. Kirjoita arvo **Nimi**-kenttään.

## <a name="enter-expression"></a>Anna lauseke

1. Valitse **Muokkaa lauseketta**.
    * Jos vapautat käyttöliittymän tehtävätallenteen tässä vaiheessa, voit muodostaa rajoituslausekkeen IntelliSensen ja symboliluettelon avulla.  
2. Lisää **ConstraintBody**-kenttään Implies[FrontGrill=="Metal", CornerProtection].
    * Tämän lausekkeen logiikka ilmaisee, että jos etusäleikkö on metallia, sitten kulmasuojausvaihtoehto on valittava.  
3. Valitse **Tarkista**.
    * Vahvistustoiminto suoritetaan rajoitelausekkeessa, jossa se tarkistaa syntaksivirheet.  
4. Valitse **Sulje**.
5. Valitse **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]