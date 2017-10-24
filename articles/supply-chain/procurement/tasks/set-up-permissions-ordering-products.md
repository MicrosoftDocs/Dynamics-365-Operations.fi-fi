--- 
title: "Määritä käyttöoikeudet tuotteiden tilaamiseen jonkun muun puolesta"
description: "Seuraavassa menettelyssä kuvataan, miten myönnät työntekijöille oikeuden valmistella ostoehdotuksia muiden työntekijöiden puolesta."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9e003f953c05facd5516e2bfa6d1c83ba6381c15
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Määritä käyttöoikeudet tuotteiden tilaamiseen jonkun muun puolesta

[!include[task guide banner](../../includes/task-guide-banner.md)]

Seuraavassa menettelyssä kuvataan, miten myönnät työntekijöille oikeuden valmistella ostoehdotuksia muiden työntekijöiden puolesta. Toisin sanoen ostoehdotuksen valmistelija voi luoda ostoehdotuksia toisen pyynnön lähettäjän puolesta. Voit myös myöntää työntekijälle käyttöoikeudet kohteiden ja palveluiden tilaamiseen yhdessä tai useammassa yrityksessä tai toimintayksikössä. Ostopäällikkö tekee yleensä nämä tehtävät. Voit käyttää tätä menettelyä joko USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Myönnä käyttöoikeudet ostoehdotusten kirjoittamiseksi toisen työntekijän puolesta
1. Siirry kohtaan Hankinnat > Asetukset > Käytännöt > Ostoehdotuksen käyttöoikeudet.
    * Varmista, että Nykyinen näkymä -kentän arvoksi on asetettu Valmistelijan mukaan.  Vasemmassa ruudussa on luettelo henkilöistä, jotka voivat saada käyttöoikeuden valmistella ehdotuksia muiden käyttäjien puolesta.  
2. Valitse henkilö, jolle oikeudet myönnetään (valmistelija).
3. ValitseLisää.
4. Etsi ja lisää henkilö pyynnön lähettäjäksi.
    * Ehdottaja on henkilö, jonka puolesta valmistelija voi luoda ostoehdotuksia.  
    * Valitse Valtuutus-kentän arvoksi Yksilöity, jos valmistelija voi luoda ostoehdotuksia valitun työntekijän puolesta. Valitse arvoksi Raportointi, jos valmistelijan pitäisi myös luoda ostoehdotuksia kaikkien työntekijöiden puolesta, jotka raportoivat kyseiselle työntekijälle.  
5. Kirjoita päivämäärä Voimassa-kenttään.
6. Syötä päivämäärä Päättyminen-kenttään.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Tarkastele valmistelijoita, joilla on oikeus luoda ostoehdotuksia valitulle työntekijälle
1. Valitse Nykyinen näkymä -kentän arvoksi "Pyytäjän mukaan".
    * Tässä näkymässä on luettelo valmistelijoista joille on myönnetty oikeudet luoda ostoehdotuksia valitun työntekijän puolesta.  
2. Etsi pyynnön lähettäjäksi lisäämäsi työntekijä pikasuodattimen avulla.
3. Valitse pyynnön lähettäjä.
    * Valmistelijaluettelossa ovat käyttäjät, joilla on oikeus tilata nimikkeitä vasemmassa ruudussa valitun pyynnön lähettäjän puolesta.   Voit lisätä muita valmistelijoita tässä.   Näkymän avulla voit myös antaa pyynnön lähettäjälle oikeuden luoda ostoehdotuksia yrityksissä toimintayksiköissä, jotka eivät ole tämän ensisijainen yritys tai toimintayksikkö.  


