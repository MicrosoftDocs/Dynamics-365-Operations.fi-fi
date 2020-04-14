---
title: Bonuspoiston määrittäminen
description: Tässä menettelyssä kerrotaan, miten erityinen poistovähennys luodaan ja liitetään käyttöomaisuuskirjaan.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91243a4cee44410a221902990d31a10f1805eb08
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138250"
---
# <a name="set-up-bonus-depreciation"></a>Bonuspoiston määrittäminen

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten erityinen poistovähennys luodaan ja liitetään käyttöomaisuuskirjaan. Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.


## <a name="create-a-special-depreciation-allowance"></a>Erityisen poistovähennyksen luominen
1. Siirry kohtaan Käyttöomaisuus > Asetukset > Erityinen poistovähennys.
2. Valitse Uusi.
3. Kirjoita Erityinen poistovähennys -kenttään arvo.
4. Kirjoita arvo Kuvaus-kenttään.
5. Syötä Prosentti-kenttään numero.
    * Määritä summa, jos prosenttia ei ole ilmoitettu.  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a>Erityisen poistovähennyksen liittäminen käyttöomaisuusryhmän kirjaan
1. Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuusryhmät.
2. Valitse luettelosta erityiseen poistovähennykseen liitetty käyttöomaisuusryhmä.
3. Valitse Kirjat.
4. Valitse luettelosta erityiseen poistovähennykseen liitetty kirja.
5. Valitse Erityinen poistovähennys.
6. Valitse Uusi.
7. Kirjoita tai valitse Erityinen poistovähennys -kenttään arvo.
    * Prosentin tai summan oletusarvo saadaan erityisen poistovähennyksen asetuksista.  
8. Syötä numero Prioriteetti-kenttään.

