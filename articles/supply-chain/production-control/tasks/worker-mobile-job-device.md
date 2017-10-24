--- 
title: "Määritä työssä mobiililaitetta käyttävä työntekijä"
description: "Tässä menettelyssä näytetään, miten työntekijän käyttäjätilille määritetään oikeat roolit, ja annetaan sitten työntekijälle mahdollisuus tehdä työnohjauksen rekisteröintejä."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d56f861dbbf579e44fcd3fc4d8b45c24029acecc
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Määritä työssä mobiililaitetta käyttävä työntekijä

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä näytetään, miten työntekijän käyttäjätilille määritetään oikeat roolit, ja annetaan sitten työntekijälle mahdollisuus tehdä työnohjauksen rekisteröintejä.


## <a name="assign-roles-to-user-account"></a>Määritä rooleja käyttäjätilille
1. Valitse Järjestelmänhallinta > Käyttäjät > Käyttäjät.
2. Suodata pikasuodatuksella työntekijä, jonka käyttäjätili on liitetty koneenkäyttäjän rooliin. Mallitiedoissa nimenä on Shannon.
3. Valitse käyttäjätilitietue.
4. Avaa käyttäjätilin tiedot napsauttamalla luettelossa valitulla rivillä Nimi-linkkiä.
5. Valitse puussa Roolit\Koneenkäyttäjä.
6. Sulje käyttäjätietojen tietosivu.
7. Sulje sivu.

## <a name="configure-worker-account"></a>Määritä työntekijän tili.
1. Valitse Henkilöstöhallinto > Työntekijät > Työntekijät.
2. Suodata pikasuodatuksella työntekijä, jonka käyttäjätili on liitetty koneenkäyttäjän rooliin. Mallitiedoissa nimenä on Shannon.
3. Valitse käyttäjätilitietue.
4. Avaa käyttäjätilin tiedot napsauttamalla luettelossa valitulla rivillä Nimi-linkkiä.
5. Valitse Työsuhde-välilehti.
6. Laajenna Aikarekisteröinti-pikavälilehti ja valitse Aktivoi rekisteröintipäätteissä.
7. Valitse Aktivoi rekisteröintipäätteissä.
8. Anna tai valitse Laskentaryhmä-kentässä arvo.
9. Anna tai valitse Oletuslaskentaryhmä-kentässä arvo.
10. Anna tai valitse Hyväksyntäryhmä-kentässä arvo.
11. Anna tai valitse Vakioprofiili-kentässä arvo.
12. Anna tai valitse Profiiliryhmä-kentässä arvo.
13. Valitse OK.
14. Anna uuden aikarekisteröinnin työntekijän nimilapun numero valitsemalla Muokkaa.
15. Kirjoita Nimilapun tunnus -kenttään arvo.
16. Valitse Tallenna.
17. Käytä SaveRecord-pikavalintaa.
18. Sulje työntekijän tietosivu.
19. Sulje sivu.

## <a name="assign-worker-to-device-group"></a>Määritä työntekijä laiteryhmään.
1. Valitse Tuotannonhallinta > Asetukset > Tuotannonohjaus > Konfiguroi työkortti laitteita varten.
2. ValitseLisää.
3. Merkitse valittu rivi luettelossa.
4. Valitse OK.
5. Valitse Muokkaa.
6. Voit määrittää Tuotantoyksikkö-kentässä työntekijän oletussuodattimen. Tämä varmistaa, että vain valittujen tuotantoyksiköiden tuotantotyöt näytetään, kun työntekijä kirjautuu laitteeseen.
7. Sulje sivu.


