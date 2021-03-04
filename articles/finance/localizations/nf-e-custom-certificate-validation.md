---
title: Mukautetun NF-e-varmenteen vahvistus
description: Tässä ohjeaiheessa on tietoja mukautetun NF-e-varmenteen käyttöönottamisesta ja käyttämisestä.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 26ffed1f49d9087ca767aab1b8cac41b099f73cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442703"
---
# <a name="nf-e-custom-certificate-validation"></a>Mukautetun NF-e-varmenteen vahvistus

[!include [banner](../includes/banner.md)]

Kun mukautetun NF-e-varmenteen tarkistusominaisuus otetaan käyttöön, mukautettu vahvistus sallii yhteyden muodostamisen verkkopalveluihin. Tämä yhteys on pakollinen, jotta NF-e voidaan lähettää ja vastaanottaa SEFAZ-valtuutus.

Varmenteen V5 **Palvelimen todentamisen tarkoitus** -ominaisuuden myöntäjä on Brasilian varmenteiden päämyöntäjä. Tämä ominaisuus on oletusarvoisesti poistettu käytöstä ja se on otettava manuaalisesti käyttöön. Joissain tilanteissa automaattinen varmennepäivitys voi poistaa tämän ominaisuuden pois käytöstä. Tämä vaikuttaa TLS-yhteyteen, eikä se ole enää luotettu varmenne. Se vaikuttaa myös mahdollisuuteen myöntää NF-e tuotantoympäristöissä Minas Geraisin (MG) ja Paranán (PR) osavaltioissa.

Tämä päivitys antaa vaihtoehtoisen varmenteen vahvistusratkaisun, jolla voi muodostaa turvallisen yhteyden.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]