---
title: Kokeen tilan tarkistaminen
description: Tässä ohjeaiheessa käsitellään kokeen tilaa kokeilun elinkaaren aikana Dynamics 365 Commercessa.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: af19a1c2e6a3205cd76c9fe998d1c8268f9077661b96c43b9aa9733286bd32d9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777521"
---
# <a name="review-the-status-of-an-experiment"></a>Kokeen tilan tarkistaminen
Kokeen määrittäminen ja suorittaminen Dynamics 365 Commercessa on monivaiheinen prosessi. Lisätietoja kokeilun elinkaaresta on kohdassa [Kokeilut Dynamics 365 Commercessa](experimentation-overview.md).

Kokeen elinkaaren vaiheen voi tarkistaa Commercen sivustonmuodostimen vasemman siirtymisruudun **Kokeet**-kohdassa. Näkyvissä on koeluettelo sekä kunkin kokeen tila sekä Commercessa että siinä kolmannen osapuolen palvelussa, jossa kokeet luodaan, variaatiot määritetään ja tiedot analysoidaan.

**Commerce-tila**-sarakkeessa on jokin seuraavista arvoista: 
- **Luonnos** – koe on yhdistetty sivuun tai osaan Commercessa ja sitä muokataan.
- **Julkaistu** – Kokeen variaatiot ovat valmiita näytettäviksi sivustossa. Jos koe suoritetaan kolmannen osapuolen palvelussa, sivuston käyttäjät näkevät kolmannen osapuolen palvelun valitseman sivu- tai osavariaation.
- **Julkaisu peruutettu** – Koe ei ole enää käytettävissä sivustossa. Sivuston käyttäjät näkevät vain sivun tai osan oletusversion, vaikka suoritus olisi käynnissä kolmannen osapuolen palvelussa.
- **Valmis** – koe on päättynyt ja variaatio on korotettu live-sivustoon kaikkien sivuston käyttäjien käyttöön.

Vastaavasti **kolmannen osapuolen tilasarakkeessa** seuraavat arvot ilmaisevat, mikä on kolmannen osapuolen palvelussa olevien kokeiden tila.
- **Luonnos** – koe on määritetty kolmannen osapuolen palvelussa, mutta sitä ei ole vielä aloitettu.
- **Suoritetaan** – koe on aloitettu kolmannen osapuolen palvelussa ja kerää tietoja.
- **Keskeytetty** – Koe on keskeytetty eikä kerää tietoja. Koetta on jatkettava, jotta tietoja voidaan taas kerätä.
- **Arkistoitu** – koe on suoritettu loppuun ja se on luetteloitu kolmannen osapuolen palvelussa tulevaa käyttöä varten.

Molemmat tilajoukot ja niiden keskinäinen suhde näkyy seuraavassa kaaviossa.

[ ![Kokeilun tilat.](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)


[!INCLUDE[footer-include](../includes/footer-banner.md)]