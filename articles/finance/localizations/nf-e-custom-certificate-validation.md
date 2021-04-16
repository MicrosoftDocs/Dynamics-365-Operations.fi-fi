---
title: Mukautetun NF-e-varmenteen vahvistus
description: Tässä ohjeaiheessa on tietoja mukautetun NF-e-varmenteen käyttöönottamisesta ja käyttämisestä.
author: gionoder
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 895513f51798a797ebf59f8a5be4f5cde006726d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813965"
---
# <a name="nf-e-custom-certificate-validation"></a>Mukautetun NF-e-varmenteen vahvistus

[!include [banner](../includes/banner.md)]

Kun mukautetun NF-e-varmenteen tarkistusominaisuus otetaan käyttöön, mukautettu vahvistus sallii yhteyden muodostamisen verkkopalveluihin. Tämä yhteys on pakollinen, jotta NF-e voidaan lähettää ja vastaanottaa SEFAZ-valtuutus.

Varmenteen V5 **Palvelimen todentamisen tarkoitus** -ominaisuuden myöntäjä on Brasilian varmenteiden päämyöntäjä. Tämä ominaisuus on oletusarvoisesti poistettu käytöstä ja se on otettava manuaalisesti käyttöön. Joissain tilanteissa automaattinen varmennepäivitys voi poistaa tämän ominaisuuden pois käytöstä. Tämä vaikuttaa TLS-yhteyteen, eikä se ole enää luotettu varmenne. Se vaikuttaa myös mahdollisuuteen myöntää NF-e tuotantoympäristöissä Minas Geraisin (MG) ja Paranán (PR) osavaltioissa.

Tämä päivitys antaa vaihtoehtoisen varmenteen vahvistusratkaisun, jolla voi muodostaa turvallisen yhteyden.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]