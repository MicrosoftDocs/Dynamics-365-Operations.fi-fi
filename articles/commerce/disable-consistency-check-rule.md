---
title: Vähittäismyyntitapahtuman yhdenmukaisuuden tarkistuksen sääntöjen käytöstäpoisto
description: Tässä aiheessa kuvataan tapahtumien yhdenmukaisuuden tarkistussääntöjen käytöstäpoistotoiminto Microsoft Dynamics 365 Commerce -sovelluksessa.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 5eb2af7e3090daabccd338d5d0bc6a6ebc4ea663
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982687"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Vähittäismyyntitapahtuman yhdenmukaisuuden tarkistuksen sääntöjen käytöstäpoisto 

[!include [banner](../includes/banner.md)]

Jälleenmyyjillä voi olla yksilöllisiä liiketoimintaskenaarioita ja -prosesseja. Tämän vuoksi kaikki kauppatapahtumien yhdenmukaisuuden tarkistukseen oletusarvoisesti sisältyvät säännöt eivät ole kaikkien jälleenmyyjien käytettävissä. Microsoft Dynamics 365 Commerce sisältää myös toiminnon, jonka avulla voi poistaa käytöstä säännöt, jotka eivät ole käytettävissä.

Saat näkyviin ympäristösi vähittäismyyntitapahtuman yhdenmukaisuuden tarkistuksen käytettävissä olevien sääntöjen luettelon ja kunkin säännön tilan siirtymällä kohtaan **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Kaupan parametrit** ja valitsemalla **Tapahtuman tarkistus** -välilehden.

Kunkin säännön tilaksi on oletusarvoisesti määritetty **Käytössä**. Tämän vuoksi kaikkia sääntöjä käytetään tarkistettaessa vähittäismyyntitapahtumat ennen niiden noutamista kauppalaskelmiin. Jos haluat poistaa säännön käytöstä, muuta sen tilaksi **Ei käytössä**. Käytöstä poistettuja sääntöjä ei käytetä kauppatapahtumien tarkistuksessa laskelman laskentaprosessin aikana.

Jos haluat ohittaa koko tarkistusprosessin käytössä olevista säännöistä huolimatta, siirry kohtaan **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Kaupan parametrit**. Määritä sitten **Tapahtuman tarkistus** -välilehdessä **Poista kauppatapahtumien yhdenmukaisuuden tarkistus käytöstä** -asetuksen arvoksi **Kyllä**. Kun tämän asetuksen arvoksi on määritetty **Ei**, arvoksi ei voi enää määrittää **Kyllä** käyttöliittymässä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]