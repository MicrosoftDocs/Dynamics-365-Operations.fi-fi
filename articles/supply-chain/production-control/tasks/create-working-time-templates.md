---
title: Työaikamallien luominen
description: Työaikamallit määrittävät koko viikon työtunnit ja niiden avulla luodaan työajat tietylle ajanjaksolle.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ef913777c8e2aa14af21e28ed56362e31b3d70a1a52e988a90ad94f59b77b70
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741258"
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