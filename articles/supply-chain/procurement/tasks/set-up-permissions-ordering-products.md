---
title: Määritä käyttöoikeudet tuotteiden tilaamiseen jonkun muun puolesta
description: Tässä aiheessa kuvataan, miten myönnät työntekijöille oikeuden valmistella ostoehdotuksia muiden työntekijöiden puolesta.
author: kamaybac
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b46f4c725f8f4fe2952b29a3ccd0d8e3912fd7fb3b6fddda5ac4a436ce9c1c77
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714231"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Määritä käyttöoikeudet tuotteiden tilaamiseen jonkun muun puolesta

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten myönnät työntekijöille oikeuden valmistella ostoehdotuksia muiden työntekijöiden puolesta. Toisin sanoen ostoehdotuksen valmistelija voi luoda ostoehdotuksia toisen pyynnön lähettäjän puolesta. Voit myös myöntää työntekijälle käyttöoikeudet kohteiden ja palveluiden tilaamiseen yhdessä tai useammassa yrityksessä tai toimintayksikössä. Ostopäällikkö tekee yleensä nämä tehtävät. Voit käyttää tätä menettelyä joko USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Myönnä käyttöoikeudet ostoehdotusten kirjoittamiseksi toisen työntekijän puolesta
1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Asetukset > Käytännöt > Ostoehdotuksen käyttöoikeudet**. Varmista, että **Nykyinen näkymä** -kentän arvoksi on asetettu **Valmistelijan mukaan**. Vasemmassa ruudussa on luettelo henkilöistä, jotka voivat saada käyttöoikeuden valmistella ehdotuksia muiden käyttäjien puolesta.  
2. Valitse henkilö, jolle oikeudet myönnetään (valmistelija).
3. Valitse **Lisää**.
4. Etsi ja lisää henkilö pyynnön lähettäjäksi.
    - Ehdottaja on henkilö, jonka puolesta valmistelija voi luoda ostoehdotuksia.  
    - Valitse **Valtuutus**-kentän arvoksi **Yksilöity**, jos valmistelija voi luoda ostoehdotuksia valitun työntekijän puolesta. Valitse arvoksi **Raportointi**, jos valmistelijan pitäisi myös luoda ostoehdotuksia kaikkien työntekijöiden puolesta, jotka raportoivat kyseiselle työntekijälle.  
5. Kirjoita päivämäärä **Voimassa**-kenttään.
6. Syötä päivämäärä **Päättyminen**-kenttään.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Tarkastele valmistelijoita, joilla on oikeus luoda ostoehdotuksia valitulle työntekijälle
1. Valitse **Nykyinen näkymä** -kentän arvoksi **Pyytäjän mukaan**. Tässä näkymässä on luettelo valmistelijoista joille on myönnetty oikeudet luoda ostoehdotuksia valitun työntekijän puolesta.  
2. Etsi pyynnön lähettäjäksi lisäämäsi työntekijä pikasuodattimen avulla.
3. Valitse pyynnön lähettäjä. Valmistelijaluettelossa ovat käyttäjät, joilla on oikeus tilata nimikkeitä vasemmassa ruudussa valitun pyynnön lähettäjän puolesta.  Voit lisätä muita valmistelijoita tässä. Näkymän avulla voit myös antaa pyynnön lähettäjälle oikeuden luoda ostoehdotuksia yrityksissä toimintayksiköissä, jotka eivät ole tämän ensisijainen yritys tai toimintayksikkö.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]