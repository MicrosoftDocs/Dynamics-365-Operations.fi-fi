--- 
title: "Työaikamallien luominen"
description: "Työaikamallit määrittävät koko viikon työtunnit ja niiden avulla luodaan työajat tietylle ajanjaksolle."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ff1978f127a014e75619a4bbbb9b6ff3a3ad7c7a
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-working-time-templates"></a>Työaikamallien luominen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Työaikamallit määrittävät koko viikon työtunnit ja niiden avulla luodaan työajat tietylle ajanjaksolle. Tässä menettelyssä käsitellään, miten työaikamalli määritetään käyttämällä työaikojen aikavälien luokittelun ajoitusominaisuuksia. Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.

1. Siirry kohtaan Kaikki työtilat > Resurssin elinkaaren hallinta.
2. Valitse Työaikamallit.

## <a name="create-working-time-template"></a>Luo työaikamalli
1. Valitse Uusi.
2. Kirjoita Työaikamalli-kenttään arvo.
3. Kirjoita arvo Nimi-kenttään.
4. Laajenna Maanantai-osa.
5. ValitseLisää.
6. Anna aika Alkaen-kentässä.
    * Määritä aika, jolloin työ alkaa aamulla.  
7. Anna aika Asti-kentässä.
    * Määritä työntekijöiden lounastauon aika.  
8. ValitseLisää.
9. Anna aika Alkaen-kentässä.
    * Määritä aika, jolloin työ jatkuu lounaan jälkeen.  
10. Anna aika Asti-kentässä.
    * Määritä, milloin työpäivä päättyy.  

## <a name="replicate-working-times-to-all-week-days"></a>Replikoi työajat kaikkiin viikonpäiviin
1. Valitse Kopioi päivä.
    * Kopioi työaikojen määritykset maanantaista tiistaille.  
2. Valitse OK.
3. Valitse Kopioi päivä.
    * Kopioi työaikojen määritykset maanantaista keskiviikolle.  
4. Valitse vaihtoehto Arkipäivään-kentässä.
5. Valitse OK.
6. Valitse Kopioi päivä.
    * Kopioi työaikojen määritykset maanantaista torstaille.  
7. Valitse vaihtoehto Arkipäivään-kentässä.
8. Valitse OK.
9. Valitse Kopioi päivä.
    * Kopioi työaikojen määritykset maanantaista perjantaille.  
10. Valitse vaihtoehto Arkipäivään-kentässä.
11. Valitse OK.

## <a name="define-time-slots-for-special-operations"></a>Määritä erityistyövaiheiden ajankohdat
1. Laajenna Perjantai-osa.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Anna tai valitse Ominaisuus-kentässä arvo.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Anna tai valitse Ominaisuus-kentässä arvo.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Merkitse viikonlopun päivät noudolta suljetuksi
1. Laajenna Lauantai-osa.
2. Valitse Suljettu noudolta -kentässä Kyllä.
3. Laajenna Sunnuntai-osa.
4. Valitse Suljettu noudolta -kentässä Kyllä.

