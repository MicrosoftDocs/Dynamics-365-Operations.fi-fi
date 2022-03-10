---
title: Työaikamallien luominen
description: Työaikamallit määrittävät koko viikon työtunnit ja niiden avulla luodaan työajat tietylle ajanjaksolle.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 130a21d08e4e720f8bf803a5d4b03d315cefc26f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580669"
---
# <a name="create-working-time-templates"></a>Työaikamallien luominen

[!include [banner](../../includes/banner.md)]

Työaikamallit määrittävät koko viikon työtunnit ja niiden avulla luodaan työajat tietylle ajanjaksolle. Tässä menettelyssä käsitellään, miten työaikamalli määritetään käyttämällä työaikojen aikavälien luokittelun ajoitusominaisuuksia. Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.

1. Siirry kohtaan **Työtilat > Resurssin elinkaaren hallinta**.
1. Valitse **Työaikamallit**.

## <a name="create-working-time-template"></a>Luo työaikamalli

1. Valitse **Uusi**.
1. Kirjoita **Työaikamalli**-kenttään arvo.
1. Kirjoita arvo **Nimi**-kenttään.
1. Laajenna **Maanantai**-osa.
1. Valitse **Lisää**.
1. Anna aika **Alkaen**-kentässä.
    * Määritä aika, jolloin työ alkaa aamulla.  
1. Anna aika **Asti**-kentässä.
    * Määritä työntekijöiden lounastauon aika.  
1. Valitse **Lisää**.
1. Anna aika **Alkaen**-kentässä.
    * Määritä aika, jolloin työ jatkuu lounaan jälkeen.  
1. Anna aika **Asti**-kentässä.
    * Määritä, milloin työpäivä päättyy.  

## <a name="replicate-working-times-to-all-week-days"></a>Replikoi työajat kaikkiin viikonpäiviin

1. Valitse **Kopioi päivä**.
    * Kopioi työaikojen määritykset maanantaista tiistaille.  
1. Valitse **OK**.
1. Valitse **Kopioi päivä**.
    * Kopioi työaikojen määritykset maanantaista keskiviikolle.  
1. Valitse vaihtoehto **Arkipäivään**-kentässä.
1. Valitse **OK**.
1. Valitse **Kopioi päivä**.
    * Kopioi työaikojen määritykset maanantaista torstaille.  
1. Valitse vaihtoehto **Arkipäivään**-kentässä.
1. Valitse **OK**.
1. Valitse **Kopioi päivä**.
    * Kopioi työaikojen määritykset maanantaista perjantaille.  
1. Valitse vaihtoehto **Arkipäivään**-kentässä.
1. Valitse **OK**.

## <a name="define-time-slots-for-special-operations"></a>Määritä erityistyövaiheiden ajankohdat

1. Laajenna **Perjantai**-osa.
1. Etsi haluamasi tietue luettelosta ja valitse se.
1. Anna tai valitse **Ominaisuus**-kentässä arvo.
1. Etsi haluamasi tietue luettelosta ja valitse se.
1. Anna tai valitse **Ominaisuus**-kentässä arvo.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Merkitse viikonlopun päivät noudolta suljetuksi

1. Laajenna **Lauantai**-osa.
1. Valitse **Suljettu noudolta** -kentässä *Kyllä* .
1. Laajenna **Sunnuntai**-osa.
1. Valitse **Suljettu noudolta** -kentässä *Kyllä* .


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]