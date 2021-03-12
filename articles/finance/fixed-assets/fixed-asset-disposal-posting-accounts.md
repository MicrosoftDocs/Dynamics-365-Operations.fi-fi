---
title: Käyttöomaisuuserän luovutuskirjaustilit
description: Tässä ohjeaiheessa kuvataan, kuinka määritetään kirjanpitotilejä käyttöomaisuuden luovuttamista varten.
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
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d9c386b5da90918226e8b1a224bf628c65702b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988999"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>Käyttöomaisuuserän luovutuskirjaustilit

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan, kuinka määritetään kirjanpitotilejä käyttöomaisuuden luovuttamista varten.

Määritä kirjanpitoon kirjaukset valitsemalla Käyttöomaisuuden kirjausprofiilit -sivulla Poistomyynti tai Poistohävikki.

Molempien tapahtumalajien kohdalla kirjanpitotiliä hyvitetään käyttöomaisuuserän luovutusarvolla. Debet kirjataan vastatilille, joka voi olla esimerkiksi pankkitili. Jos käyttöomaisuuserä myydään asiakkaalle, vastatilin asemesta käytetään asiakastiliä.

Valitse Luovutus, valitse Myynti tai Hävikki ja määritä sitten yksityiskohtaiset tilit käyttöomaisuuserän nettokirjanpitoarvon vähentämistä varten. Voit syöttää tietoja myös Luovutusparametrit-sivun Kirjausarvo- ja Myyntiarvo-kenttiin. 

Arvoltaan vähäisen käyttöomaisuuden ryhmässä olevan käyttöomaisuuserän poistotapahtuma vähentää arvoltaan vähäisen käyttöomaisuuden ryhmän nettokirjanpitoarvoa vain poistetulla summalla. Jos käyttöomaisuuserän myyntisumma on kuitenkin suurempi kuin arvoltaan vähäisen käyttöomaisuuden ryhmän nettokirjanpitoarvo, nettokirjanpitoarvo vähennetään nollaan.





