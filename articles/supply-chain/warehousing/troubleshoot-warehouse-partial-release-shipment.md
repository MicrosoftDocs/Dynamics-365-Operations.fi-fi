---
title: Osittaisten vapautusten ja osalähetysten vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun osittaisia vapautuksia ja osittaisia lähetyksiä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 1c9246376505e163a4a41bf141a98deed0fd511f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263225"
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