---
title: Kustannusobjektin vastuuhenkilön käyttöoikeuksien määrittäminen
description: Tämän menettelyn avulla määritetään kustannusobjektin vastuuhenkilön käyttöoikeudet.
author: kfend
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17615ff70c15789ac30223464b20ccd61a1bad55
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710627"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>Kustannusobjektin vastuuhenkilön käyttöoikeuksien määrittäminen

[!include [banner](../../includes/banner.md)]

Tämän menettelyn avulla määritetään kustannusobjektin vastuuhenkilön käyttöoikeudet. Tämä tallenne käyttää esittelytietojen USP2-yritystä.


## <a name="assign-the-cost-object-controller-role"></a>Kustannusobjektin vastuuhenkilön roolin delegoiminen
1. Valitse Järjestelmänhallinta > Käyttäjät > Käyttäjät.
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Käyttäjän nimi -kenttää arvolla "alicia".
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse Määritä rooleja.
5. Etsi haluamasi tietue luettelosta ja valitse se.
6. Valitse OK.

## <a name="enable-access-list-security"></a>Käyttöoikeusluettelon suojauksen ottaminen käyttöön
1. Valitse Kustannuslaskenta > Dimensiot > Dimensiohierarkiat.
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse Organisaatio.  
3. Valitse Muokkaa.
4. Valitse Käyttöoikeusluettelohierarkia-kentässä Kyllä.
5. Valitse Näytä hierarkia.

## <a name="assign-access-rights-to-user"></a>Käyttöoikeuksien delegoiminen käyttäjälle
1. Valitse Uusi.
2. Merkitse valittu rivi luettelossa.
3. Syötä tai valitse arvo Käyttäjätunnus-kentässä.
    * Valitse Järjestelmänvalvoja.  
4. Valitse puussa Organization\CEO\CFO\FIM.
5. Valitse Uusi.
6. Merkitse valittu rivi luettelossa.
7. Syötä tai valitse arvo Käyttäjätunnus-kentässä.
    * Valitse Alicia.  
8. Valitse Tallenna.

## <a name="enable-access-rights-in-cost-accounting"></a>Käyttöoikeuksien ottaminen käyttöön kustannuslaskennassa
1. Valitse Kustannuslaskenta > Asetukset > Parametrit.
2. Valitse Yleiset-välilehti.
3. Valitse Ota käyttöön katseluoikeus kustannusobjektin dimension jäsenille -kentässä Kyllä.
4. Valitse Tallenna.
5. Sulje sivu.
6. Valitse Kustannuslaskenta > Asetukset > Kustannusseurannan työtilan konfiguraatio.
7. Valitse Muokkaa.
8. Valitse Julkaistu-kentässä Kyllä.
    * Jos valitset Kyllä, käyttäjä, jolle on delegoitu jokin seuraavista neljästä roolista, näkee raportit kustannusseurannan työtilassa: kustannuslaskennan hallinta, kustannuslaskija, kustannuslaskijan apulainen tai kustannusobjektin vastuuhenkilö. Jos valitset Ei, vain käyttäjä, jolle on delegoitu jokin seuraavista rooleista, näkee raportit: kustannuslaskennan hallinta, kustannuslaskija tai kustannuslaskijan apulainen.    
9. Valitse Tallenna.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
