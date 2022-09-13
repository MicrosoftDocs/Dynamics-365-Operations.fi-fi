---
title: Kirjanpitoa odottavat asiakirjat
description: Tässä artikkelissa kerrotaan, miten Kirjanpitoa odottavat asiakirjat ‑sivun toimintoja käytetään.
author: ryanCCarlson2
ms.date: 09/02/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: e915c248abd1c842f8f01490a49db9b824644a29
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2022
ms.locfileid: "9424363"
---
# <a name="documents-pending-accounting"></a>Kirjanpitoa odottavat asiakirjat

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Tässä artikkelissa kerrotaan, miten **Kirjanpitoa odottavat asiakirjat** ‑sivun toimintoja käytetään.

Versiossa Microsoft Dynamics 365 Finance 10.0.30 on käytettävissä **Parempi lähdeasiakirjan kirjanpitokehyksen suorituskyky** ‑ominaisuus. Tämä ominaisuus parantaa lähdeasiakirjaa käyttävien asiakirjakirjausten kirjausprosesseja alkaen vapaatekstilaskujen kirjausprosessista.

Kun tämä ominaisuus on käytössä, alareskontra-asiakirjan kirjaaminen tapahtuu erillään kirjanpidon luomisesta tai *kirjausprosessista*, joka luo täydet kirjanpitoon siirrettävät kirjanpitotiedot. Esimerkiksi vapaatekstilaskun kirjausprosessissa **Myyntireskontra**-moduulissa oleva myyntilasku kirjataan ennen täyden kirjanpidon luomista. Tämä parannetun suorituskyvyn ominaisuus mahdollistaa myyntilaskujen kirjaamisen nopeammin ja kirjanpidon luonnin viivästämisen.

Seuraavat painikkeet ovat käytettävissä **Kirjanpitoa odottavat asiakirjat** ‑sivulla.

- **Luo kirjanpito** – lähetä asiakirja, joka parhaillaan odottaa tilien luomista kirjausta varten.
- **Näytä jakaumat** – näytä valitun luettelossa olevan asiakirjan kirjanpidolliset jaot.
- **Näytä virheloki** – näytä virheiden tiedot, kun asiakirjan kirjanpidon tila osoittaa, että kirjanpidossa on virheitä. Voit tarkastella samoja virhesanomatietoja valitsemalla **Virheloki**-linkin asiakirjan rivillä.

Kirjanpidon luomisen tekee prosessin automatisoinnin taustaprosessi nimeltä **Kirjanpitokehyksen käsittelijä**. Lisätietoja kaikkien prosessien automatisointien asetuksista ja konfiguroinnista on ohjeaiheessa [Prosessien automatisointi](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
