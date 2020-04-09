---
title: ER Tuo kokoonpano Lifecycle Services -palvelusta
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi tuoda uuden sähköisen raportoinnin (ER) konfiguraation version Microsoft Lifecycle Services (LCS) -palvelusta.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67e09e3187ac49e12727116f55066b64a386e2de
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142383"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a>ER Tuo kokoonpano Lifecycle Services -palvelusta

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi tuoda uuden sähköisen raportoinnin (ER) konfiguraation version Microsoft Lifecycle Services (LCS) -palvelusta.

Tässä esimerkissä valitaan sopiva ER-konfiguraatio ja tuodaan se malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraatiot. Lataa ER-kokoonpano Lifecycle Services -palveluun -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista. Näiden vaiheiden suorittamiseen tarvitaan myös LCS:n käyttöoikeudet.

1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
2. Valitse Konfiguraatiot.

## <a name="delete-a-shared-version-of-data-model-configuration"></a>Poista tietomallin konfiguraation jaettu versio
1. Valitse puussa solmu Mallikonfiguraation esimerkki.
    * Ensimmäinen mallikonfiguraation esimerkkiversio on luotu ja julkaistu LCS:ään "Lataa ER-kokoonpano Lifecycle Services -palveluun" -menettelyn aikana. Tässä menettelyssä poistetaan kyseinen ER-konfiguraation versio. Tämä tietomallin konfiguraation esimerkkiversio tuodaan LCS:stä myöhemmin.  
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse tämän konfiguraation versio, jonka tila on "Jaettu". Tämä tila ilmaisee, että konfiguraatio on julkaistu LCS:ään.  
3. Voit muuttaa tilaa valitsemalla Muuta.
4. Napsauta Lopeta.
    * Muuta valitun version tila jaetusta lopetetuksi, jotta se on poistettavissa.  
5. Valitse OK.
6. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse tämän konfiguraation versio, jonka tila on "Lopetettu".  
7. Valitse Poista.
8. Valitse Kyllä.
    * Huomaa, että vain valitun tietomallin konfiguraation luonnosversio 2 on käytettävissä.  
9. Sulje sivu.

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a>Tuo tietomallin konfiguraation jaettu versio LCS:stä
1. Merkitse valittu rivi luettelossa.
    * Avaa Litware, Inc:n säilöluettelo. -konfiguraation lähteestä.  
2. Valitse Säilöt.
3. Valitse Avaa.
    * Valitse LCS-säilö ja avaa se.  
4. Merkitse valittu rivi luettelossa.
    * Valitse versioluettelosta ensimmäinen mallikonfiguraation esimerkkiversio.  
5. Valitse Tuo.
6. Valitse Kyllä.
    * Vahvista valitun version tuonti LCS:stä.  
    * Huomaa, että valitun version tuonnin onnistuminen ilmaistaan tiedotuksella (lomakkeen yllä).  
7. Sulje sivu.
8. Sulje sivu.
9. Valitse Konfiguraatiot.
10. Valitse puussa solmu Mallikonfiguraation esimerkki.
11. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse tämän konfiguraation versio, jonka tila on "Jaettu".  
    * Huomaa, että valitun tietomallin konfiguraation jaettu versio 1 on nyt myös käytettävissä.  

