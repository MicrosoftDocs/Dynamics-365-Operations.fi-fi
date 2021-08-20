---
title: Mukautetun NF-e-varmenteen vahvistus
description: Tässä ohjeaiheessa on tietoja mukautetun NF-e-varmenteen käyttöönottamisesta ja käyttämisestä.
author: gionoder
ms.date: 07/29/2021
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
ms.openlocfilehash: 8144e16b127bdbe954ef44f52c5ac71689a2036e6085e9a4ccc8bb17f91ae9b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755588"
---
# <a name="nf-e-custom-certificate-validation"></a>Mukautetun NF-e-varmenteen vahvistus

[!include [banner](../includes/banner.md)]

Brasilian varmenteiden päämyöntäjän myöntämien varmenteiden **Palvelimen todentamisen tarkoitus** -ominaisuus on oletusarvoisesti poistettu käytöstä ja on otettava manuaalisesti käyttöön. Joissain tilanteissa automaattinen varmennepäivitys voi poistaa tämän ominaisuuden pois käytöstä. Tämä vaikuttaa TLS-yhteyteen, eikä se ole enää luotettu varmenne. Se vaikuttaa mahdollisuuteen myöntää Brasilian sähköisen laskutuksen veroasiakirjamalli 55 (NF-e) tuotantoympäristöissä Minas Geraisissa (MG) ja Paranássa (PR).

**Mukautetun NF-e-varmenteen vahvistus** -korjaus otetaan käyttöön **ominaisuuksien hallinnassa**. Tämä ominaisuus antaa mahdollisuuden V5- ja V10-varmenteiden vaihtoehtoisille vahvistusratkaisuille sekä sallii luotetun yhteyden verkkopalveluihin, mikä on edellytys NF-e:n turvalliselle lähettämiselle ja SEFAZ-valtuutuksen vastaanottamiselle.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
