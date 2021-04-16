---
title: Osittaisten vapautusten ja osalähetysten vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun osittaisia vapautuksia ja osittaisia lähetyksiä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5534099f81a97a1dcf4908784fd71dd03cf94eaf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828151"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>Osittaisten vapautusten ja osalähetysten vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun osittaisia vapautuksia ja osittaisia lähetyksiä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Myyntitilauksen vapautustilaksi jää Osittain vapautettu myös myyntitilauksen laskutuksen jälkeen.

### <a name="issue-description"></a>Ongelman kuvaus

Myyntilaus on toimitustilaus, mutta ainakin yhdellä nimikkeellä on erilainen toimitustila. Kun tilaus on laskutettu, sen vapautustila on edelleen *Osittain vapautettu*.

Esimerkiksi myyntitilauksessa on kaksi nimikettä: yksi toimitusta varten ja toinen noutoa varten. Sekä toimitus että nouto ovat valmiita. Tämän vuoksi molemmat rivit on laskutettu. Vapautustilana on kuitenkin edelleen *Osittain vapautettu*, mikä on harhaanjohtavaa.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Vapautustila koskee vain tilausrivejä, joiden nimikkeissä varastonhallinta on otettu käyttöön. Tämän vuoksi vapautustilaksi jää *Osittain vapautettu* tässä skenaariossa. Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus. Laajennus voitaisiin lisätä pakkausluettelon ja laskutusprosessin osana päivittämään vapautustila.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]