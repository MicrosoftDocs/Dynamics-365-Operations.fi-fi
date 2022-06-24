---
title: Muiden kuin rahdinkuljettajien toimitustapojen piilotus POS:n lähetysvalinnoissa
description: Tässä artikkelissa kuvataan määritysvaihtoehto, jolla estetään muiden kuin rahdinkuljettajien toimitustapojen valittavuus, kun lähetystilauksia luodaan myyntipistesovelluksessa (POS).
author: hhainesms
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 469e6ebb8afed26a6bf25f4c9c3ab8f7f4ac78ba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897002"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Muiden kuin rahdinkuljettajien toimitustapojen piilotus POS:n lähetysvalinnoissa


[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan määritysvalinta, joka on käytettävissä myyntipistesovelluksessa (POS). Tämä määritysvalinta muuttaa toimintatapaa lähetystavan valinnassa, kun tilauksia luodaan POS:ssä.

Kun käyttäjät luovat mukautettuja lähetystilauksia POS:ssä, he voivat valita lähetykselle toimitustavan. Tämä toiminto on käytettävissä riippumatta siitä, lähetetäänkö koko tilaus vai vain valittuja rivejä.

Oletusarvoisesti toimitustavan valintaikkunassa näkyvät kaikki kanavan, nimikkeen ja toimitusosoitteen yhdistelmälle soveltuvat toimitustavat. Nämä toimitustavat määritetään **Toimitustavat**-sivulla Headquartersissa (**Myynti ja markkinointi \> Asetukset \> Jakelu \> Toimitustavat**). Valintaikkunassa voi näkyä myös muita kuin rahdinkuljettajan toimitustapoja, kuten **Nouto liikkeestä** tai **Nouto**.

Nyt on kuitenkin lisätty toiminto, jolla voit piilottaa valintaikkunassa muut kuin rahdinkuljettajan toimitustavat. Voit ottaa tämän toiminnon käyttöön asettamalla **Asiakastilaukset**-välilehden **Commercen parametrit** -sivun asetuksen **Näytä lähetystilauksissa vain rahdinkuljettajien toimitustavat** arvoksi **Kyllä**. Kun olet ottanut tämän toiminnon käyttöön ja suoritat asianmukaiset jakelutyöt synkronoidaksesi tiedot kanavatietokantaan, muita kuin rahdinkuljettajien toimitustapoja ei enää ole valittavissa, kun lähetystilauksia luodaan POS:ssä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]