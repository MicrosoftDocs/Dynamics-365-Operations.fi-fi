---
title: Muiden kuin rahdinkuljettajien toimitustapojen piilotus POS:n lähetysvalinnoissa
description: Tässä aiheessa kuvataan määritysvaihtoehto, jolla estetään muiden kuin rahdinkuljettajien toimitustapojen valittavuus, kun lähetystilauksia luodaan myyntipistesovelluksessa (POS).
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 09ea83b3336b208f8af0a91025c2e6c50d64c385
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/24/2019
ms.locfileid: "2659018"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Muiden kuin rahdinkuljettajien toimitustapojen piilotus POS:n lähetysvalinnoissa

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä aiheessa kuvataan määritysvalinta, joka on käytettävissä myyntipistesovelluksessa (POS). Tämä määritysvalinta muuttaa toimintatapaa lähetystavan valinnassa, kun tilauksia luodaan POS:ssä.

Kun käyttäjät luovat mukautettuja lähetystilauksia POS:ssä, he voivat valita lähetykselle toimitustavan. Tämä toiminto on käytettävissä riippumatta siitä, lähetetäänkö koko tilaus vai vain valittuja rivejä.

Oletusarvoisesti toimitustavan valintaikkunassa näkyvät kaikki kanavan, nimikkeen ja toimitusosoitteen yhdistelmälle soveltuvat toimitustavat. Nämä toimitustavat määritetään **Toimitustavat**-sivulla Retail Headquartersissa (**Myynti ja markkinointi \> Asetukset \> Jakelu \> Toimitustavat**). Valintaikkunassa voi näkyä myös muita kuin rahdinkuljettajan toimitustapoja, kuten **Nouto liikkeestä** tai **Nouto**.

Nyt on kuitenkin lisätty toiminto, jolla voit piilottaa valintaikkunassa muut kuin rahdinkuljettajan toimitustavat. Voit ottaa tämän toiminnon käyttöön asettamalla **Asiakastilaukset**-välilehden **Vähittäismyynnin parametrit** -sivun asetuksen **Näytä lähetystilauksissa vain rahdinkuljettajien toimitustavat** arvoksi **Kyllä**. Kun olet ottanut tämän toiminnon käyttöön ja suoritat asianmukaiset jakelutyöt synkronoidaksesi tiedot kanavatietokantaan, muita kuin rahdinkuljettajien toimitustapoja ei enää ole valittavissa, kun lähetystilauksia luodaan POS:ssä.
