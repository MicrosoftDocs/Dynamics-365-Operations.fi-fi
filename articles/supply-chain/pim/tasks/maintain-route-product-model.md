---
title: Ylläpidä tuotemallin reititystä
description: Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 704a6b72c9eb8dc49ba9410ccd3689ba5ccfdd1f03e538b95ad174f6c1ee9796
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746133"
---
# <a name="maintain-route-for-a-product-model"></a>Ylläpidä tuotemallin reititystä

[!include [banner](../../includes/banner.md)]

Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin. Tämä menetelmä käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -mallia prosessin selittämiseen.

## <a name="add-a-route-operation"></a>Lisää reitityksen työvaihe

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.
1. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse tähän harjoitukseen Korkealaatuinen kaiutinmalli.  
1. Valitse luettelossa valitulla rivillä oleva linkki.
1. Laajenna **Reitityksen työvaihe** -osa.
1. Valitse **Lisää**.
1. Kirjoita arvo **Nimi**-kenttään.
1. Kirjoita **Kuvaus**-kenttään arvo.
1. Valitse **Tallenna**.

## <a name="enter-route-operation-details"></a>Anna reitityksen työvaiheen tiedot

1. Valitse **Reitityksen työvaiheen tiedot**.
1. Anna tai valitse **Toiminto**-kentässä arvo.
1. Valitse **Työvaiheen nro** numero.
    * Työvaihenumerot määrittävät reittijärjestyksen.  
    * Jokainen reitityksen työvaiheen ominaisuus voi saada staattisen arvon tai se voidaan yhdistää määritteeseen. Määritteeseen yhdistettäessä arvo määritetään osana määritystä.  
1. Anna tai valitse arvo **Reititysryhmä**-kentässä.
    * Reititysryhmä määrittää kustannuslaskennan, kulutuksen ja asetusten tärkeimmät toiminnot.  
1. Valitse **Määritys**-välilehti.
1. Valitse **Ajat**-välilehti.
1. Syötä **Prosessimäärä**-kenttään numero.
    * Määritä, kuinka monta käsitellään yhdessä työvaiheessa.  
1. Lisää **Tunnit/aika**-kenttään luku.
    * Lisää aikasuhde.  
1. Valitse **Määritä**-valintaruutu.
1. Lisää **Ajoaika**-kenttään numero.
    * Määritä määritetyn määrän käsittelyaika.  
1. Valitse **Resurssivaatimukset**-välilehti.
1. Valitse **Lisää**.
1. Merkitse valittu rivi luettelossa.
1. Valitse **Vaatimustyyppi**-kentässä vaihtoehto.
    * Päätä, haluatko määrittää tietyt resurssit vai ominaisuudet, jotka niillä on oltava.  
1. Anna tai valitse **Tarve**-kentässä arvo.
1. Valitse **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]