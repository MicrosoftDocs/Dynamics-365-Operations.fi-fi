--- 
title: "Lisää rajoituslauseke tuotemääritysmalliin"
description: "Tässä menettelyssä käsitellään, miten uusi rajoituslauseke lisätään tuotemääritysmalliin."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8db46c5b8361c96745b440c0d0684e18c06a6c6f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Lisää rajoituslauseke tuotemääritysmalliin

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

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


