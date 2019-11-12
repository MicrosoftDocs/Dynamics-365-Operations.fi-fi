---
title: Vähittäismyyntitapahtuman yhdenmukaisuuden tarkistuksen sääntöjen käytöstäpoisto
description: Tässä aiheessa kuvataan vähittäismyyntitapahtumien yhdenmukaisuuden tarkistussääntöjen käytöstäpoistotoiminto Microsoft Dynamics 365 Retail -sovelluksessa.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586294"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Vähittäismyyntitapahtuman yhdenmukaisuuden tarkistuksen sääntöjen käytöstäpoisto 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Jälleenmyyjillä voi olla yksilöllisiä liiketoimintaskenaarioita ja -prosesseja. Tämän vuoksi kaikki vähittäismyyntitapahtumien yhdenmukaisuuden tarkistukseen oletusarvoisesti sisältyvät säännöt eivät ole kaikkien jälleenmyyjien käytettävissä. Microsoft Dynamics 365 Retail sisältää myös toiminnon, jonka avulla voi poistaa käytöstä säännöt, jotka eivät ole käytettävissä.

Saat näkyviin ympäristösi vähittäismyyntitapahtuman yhdenmukaisuuden tarkistuksen käytettävissä olevien sääntöjen luettelon ja kunkin säännön tilan siirtymällä kohtaan **Vähittäismyynti \> Pääkonttorin asetukset \> Parametrit \> Vähittäismyynnin parametrit** ja valitsemalla **Tapahtuman tarkistus** -välilehden.

Kunkin säännön tilaksi on oletusarvoisesti määritetty **Käytössä**. Tämän vuoksi kaikkia sääntöjä käytetään tarkistettaessa vähittäismyyntitapahtumat ennen niiden noutamista vähittäismyyntilaskelmiin. Jos haluat poistaa säännön käytöstä, muuta sen tilaksi **Ei käytössä**. Käytöstä poistettuja sääntöjä ei käytetä vähittäismyyntitapahtumien tarkistuksessa laskelman laskentaprosessin aikana.

Jos haluat ohittaa koko tarkistusprosessin käytössä olevista säännöistä huolimatta, siirry kohtaan **Vähittäismyynti \> Pääkonttorin asetukset \> Parametrit \> Vähittäismyynnin parametrit**. Määritä sitten **Tapahtuman tarkistus** -välilehdessä **Poista vähittäismyyntitapahtumien yhdenmukaisuuden tarkistus käytöstä** -asetuksen arvoksi **Kyllä**. Kun tämän asetuksen arvoksi on määritetty **Ei**, arvoksi ei voi enää määrittää **Kyllä** käyttöliittymässä.
