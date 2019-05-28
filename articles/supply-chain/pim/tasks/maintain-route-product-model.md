---
title: Ylläpidä tuotemallin reititystä
description: Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e793466e021671501570aed06959d684d5e9c15
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567696"
---
# <a name="maintain-route-for-a-product-model"></a>Ylläpidä tuotemallin reititystä

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin. Tämä menetelmä käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -mallia prosessin selittämiseen.


## <a name="add-a-route-operation"></a>Lisää reitityksen työvaihe
1. Valitse Tuotevarianttimallin määritys.
2. Valitse Tuotekonfiguraation mallit.
3. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse tähän harjoitukseen Korkealaatuinen kaiutinmalli.  
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Laajenna Reitityksen työvaihe -osa.
6. ValitseLisää.
7. Kirjoita arvo Nimi-kenttään.
8. Kirjoita arvo Kuvaus-kenttään.
9. Valitse Tallenna.

## <a name="enter-route-operation-details"></a>Anna reitityksen työvaiheen tiedot
1. Valitse Reitityksen työvaiheen tiedot.
2. Anna tai valitse Toiminto-kentässä arvo.
3. Lisää Työvaiheen Nro numero.
    * Työvaihenumerot määrittävät reittijärjestyksen.  
    * Jokainen reitityksen työvaiheen ominaisuus voi saada staattisen arvon tai se voidaan yhdistää määritteeseen. Määritteeseen yhdistettäessä arvo määritetään osana määritystä.  
4. Anna tai valitse arvo Reititysryhmä-kentässä.
    * Reititysryhmä määrittää kustannuslaskennan, kulutuksen ja asetusten tärkeimmät toiminnot.  
5. Valitse Asetukset-välilehti.
6. Valitse Ajat-välilehti.
7. Syötä Prosessimäärä-kenttään numero.
    * Määritä, kuinka monta käsitellään yhdessä työvaiheessa.  
8. Lisää Tunnit/aika-kenttään luku.
    * Lisää aikasuhde.  
9. Valitse Määritä-valintaruutu.
10. Lisää Ajoaika-kenttään numero.
    * Määritä määritetyn määrän käsittelyaika.  
11. Valitse Resurssivaatimukset-välilehti.
12. ValitseLisää.
13. Merkitse valittu rivi luettelossa.
14. Valitse Vaatimustyyppi-kentässä vaihtoehto.
    * Päätä, haluatko määrittää tietyt resurssit vai ominaisuudet, jotka niillä on oltava.  
15. Anna tai valitse Tarve-kentässä arvo.
16. Valitse OK.

