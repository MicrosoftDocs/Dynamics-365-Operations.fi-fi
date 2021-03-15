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
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f13e8b8229bbd9e174e5bde7858a468048ba309b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990083"
---
# <a name="nf-e-custom-certificate-validation"></a>Mukautetun NF-e-varmenteen vahvistus

[!include [banner](../includes/banner.md)]

Kun mukautetun NF-e-varmenteen tarkistusominaisuus otetaan käyttöön, mukautettu vahvistus sallii yhteyden muodostamisen verkkopalveluihin. Tämä yhteys on pakollinen, jotta NF-e voidaan lähettää ja vastaanottaa SEFAZ-valtuutus.

Varmenteen V5 **Palvelimen todentamisen tarkoitus** -ominaisuuden myöntäjä on Brasilian varmenteiden päämyöntäjä. Tämä ominaisuus on oletusarvoisesti poistettu käytöstä ja se on otettava manuaalisesti käyttöön. Joissain tilanteissa automaattinen varmennepäivitys voi poistaa tämän ominaisuuden pois käytöstä. Tämä vaikuttaa TLS-yhteyteen, eikä se ole enää luotettu varmenne. Se vaikuttaa myös mahdollisuuteen myöntää NF-e tuotantoympäristöissä Minas Geraisin (MG) ja Paranán (PR) osavaltioissa.

Tämä päivitys antaa vaihtoehtoisen varmenteen vahvistusratkaisun, jolla voi muodostaa turvallisen yhteyden.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]