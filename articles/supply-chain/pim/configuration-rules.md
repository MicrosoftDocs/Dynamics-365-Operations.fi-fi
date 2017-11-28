---
title: "Konfiguraatiosäännöt"
description: "Tässä artikkelissa on yleistietoja konfiguraatiosäännöistä. Konfiguraatiosäännöt määrittävät sellaisten tuotteiden tuoterakenteen nimikkeiden väliset suhteet, jotka käyttävät dimensioihin perustuvaa konfiguraatiotekniikkaa."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 37f70d2620023915b23425d41dfb0043ef856492
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="configuration-rules"></a>Konfiguraatiosäännöt

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on yleistietoja konfiguraatiosäännöistä. Konfiguraatiosäännöt määrittävät sellaisten tuotteiden tuoterakenteen nimikkeiden väliset suhteet, jotka käyttävät dimensioihin perustuvaa konfiguraatiotekniikkaa.

Konfiguraatiosääntöjä voi käyttää määritettäessä dimensioihin perustuvia konfiguraatiomalleja. Konfiguraatiosääntöjä käytetään joko tiettyjen nimikeyhdistelmien ottamiseksi käyttöön tai estämiseksi tuoterakenteessa. Kun tuoterakenne on luotu ja sitä vastaavat nimikkeet on määritetty omiin konfiguraatioryhmiinsä, voidaan määrittää yksi tai useampi konfiguraatiosääntö. Jos kaksi nimikettä kuuluu yhteen, sisällytys varmistetaan **Valitse**-operaattorilla. Jos kaksi nimikettä kumoavat toisensa, poissulkeminen varmistetaan **Poista valinta** -operaattorilla.  

**Huomautus:** Nämä tiedot koskevat vain päätuotteita, jotka käyttävät dimensioihin perustuvaa konfiguraatiomääritelmää.  

Konfigurointisääntöjen muutokset eivät vaikuta aiemmin luotuihin konfiguraatioihin. On kuitenkin tärkeää määrittää säännöt ennen uuden konfiguraation määrittämistä tai tarkistaa säännöt, jos ne saattavat olla muuttuneet.  

**Huomautus:** **Valitse**-menetelmä tarkoittaa, että johdettu konfigurointiryhmä, nimiketunnus ja konfiguraatio valitaan automaattisesti. **Poista valinta** -menetelmä tarkoittaa, että johdettua konfigurointiryhmää, nimiketunnusta ja konfiguraatiota ei voi valita.

<a name="see-also"></a>Lisätietoja
--------

[Dimensioon perustuva tuotekonfigurointi](dimension-based-product-configuration.md)




