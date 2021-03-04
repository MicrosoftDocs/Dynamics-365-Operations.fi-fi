---
title: Käyttöomaisuuden hankintojen kirjaustilit
description: Tässä artikkelissa kuvataan, kuinka määritetään kirjanpitotilejä käyttöomaisuuden hankkimista varten.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8fea6b1cd79b5536341a7cb50e5592ea38a7392d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442705"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a>Käyttöomaisuuden hankintojen kirjaustilit

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka määritetään kirjanpitotilejä käyttöomaisuuden hankkimista varten.

Käyttöomaisuuden hankintojen kirjaamiseen käytetyt tilit voivat vaihdella sen mukaan, millä tavalla käyttöomaisuus hankitaan. Valitsemalla Käyttöomaisuuserän kirjausprofiili -sivun Kirjanpitotilit -välilehdessä Hankinta ja Hankintaoikaisu voit määrittää käyttöomaisuustilit kirjanpitoon kirjaamista varten. 

Kirjanpitotili on kirjauskansioissa ja ostotilauksissa yleensä tasetili, jota hyvitetään uuden käyttöomaisuuserän hankinta-arvolla. Tätä tiliä ei näytetä kirjauskansiossa, eikä sitä voi korvata tapahtumissa. 

Myös vastatili on tasetili. Kirjauskansiossa ja käyttöomaisuuskirjauskansiossa tämä tili on usein pankkitili, jota käytetään käyttöomaisuuserän hankintahinnan maksamiseen. Vastatili on kirjauskansioissa ehdotettava oletustili. Se voidaan vaihtaa kirjauskansiossa toiseksi tilikartan tiliksi tai toimittajatiliksi, jos käyttöomaisuuserä oli osto toimittajalta. 

Käytettäessä ostoreskontran Laskukirjauskansio- tai Ostotilaukset-toimintoa käyttöomaisuuden hankintaan, käyttöomaisuustapahtuman vastatili korvataan tapahtumalle valitulla toimittajatilillä.

Kirjanpito-osan Siirto varastosta käyttöomaisuuteen -kirjauskansion avulla kirjattavien hankintojen osalta käyttöomaisuuserää ei osteta ulkoisesta lähteestä, vaan se siirretään yrityksen omasta varastosta. Tämän vuoksi vastatili on varasto-ottotili varastonimikkeelle varastonhallinnassa.

Lisätietoja on ohjeaiheessa [Hankkia omaisuuseriä hankintojen kautta](acquire-assets-procurement.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]