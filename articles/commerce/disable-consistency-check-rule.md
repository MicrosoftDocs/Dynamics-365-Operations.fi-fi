---
title: Tapahtuman tarkistusprosessissa käytettävien sääntöjen käytöstäpoisto
description: Tässä artikkelissa kuvataan tapahtuman tarkistussääntöjen käytöstäpoiston toiminto Microsoft Dynamics 365 Commerce -sovelluksessa.
author: analpert
ms.date: 12/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7d566aa3b829dad281528925a341382f9637fdba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884873"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Tapahtuman tarkistusprosessissa käytettävien sääntöjen käytöstäpoisto

[!include [banner](../includes/banner.md)]

Jälleenmyyjillä voi olla yksilöllisiä liiketoimintaskenaarioita ja -prosesseja. Tämän vuoksi kaikki kauppatapahtumien tarkistusprosessiin sisältyvät säännöt eivät ole kaikkien jälleenmyyjien käytettävissä. Microsoft Dynamics 365 Commerce sisältää myös toiminnon, jonka avulla voi poistaa käytöstä säännöt, jotka eivät ole käytettävissä.

Saat näkyviin ympäristösi tapahtuman tarkistusprosessin käytettävissä olevien sääntöjen luettelon ja kunkin säännön tilan siirtymällä kohtaan **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Commercen parametrit** ja valitsemalla **Tapahtuman tarkistus** -välilehden. Kaikkia käytössä olevia sääntöjä käytetään tapahtumien tarkistuksessa **Tarkista myymälän tapahtumat** -prosessin aikana. Tapahtumat on hyväksyttävä, kerättävä ja kirjattava tapahtumaraporttiin.

Kunkin säännön tilaksi on oletusarvoisesti määritetty **Käytössä**. Tämän vuoksi kaikkia sääntöjä käytetään tarkistettaessa tapahtumat, ennen kuin ne noudetaan kaupankäynnin tapahtumaraportteihin. Jos haluat poistaa säännön käytöstä, muuta sen tilaksi **Ei käytössä**. Käytöstä poistettuja sääntöjä ei käytetä, kun tapahtumat tarkistetaan **Tarkista myymälän tapahtumat** -prosessin aikana.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
