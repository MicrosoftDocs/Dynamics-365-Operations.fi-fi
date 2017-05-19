---
title: "Käyttöomaisuuden poistojen kirjaustilit"
description: "Tässä artikkelissa kuvataan, kuinka määritetään kirjanpitotilejä käyttöomaisuuden luovuttamista varten."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 111ff7ec677b699b8455b3a46a2866bd98970527
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="fixed-asset-disposal-posting-accounts"></a>Käyttöomaisuuden poistojen kirjaustilit

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan, kuinka määritetään kirjanpitotilejä käyttöomaisuuden luovuttamista varten.

Määritä kirjanpitoon kirjaukset valitsemalla Käyttöomaisuuden kirjausprofiilit -sivulla Poistomyynti tai Poistohävikki.

Molempien tapahtumalajien kohdalla kirjanpitotiliä hyvitetään käyttöomaisuuserän luovutusarvolla. Debet kirjataan vastatilille, joka voi olla esimerkiksi pankkitili. Jos käyttöomaisuuserä myydään asiakkaalle, vastatilin asemesta käytetään asiakastiliä.

Valitse Luovutus, valitse Myynti tai Hävikki ja määritä sitten yksityiskohtaiset tilit käyttöomaisuuserän nettokirjanpitoarvon vähentämistä varten. Voit syöttää tietoja myös Luovutusparametrit-sivun Kirjausarvo- ja Myyntiarvo-kenttiin. 

Arvoltaan vähäisen käyttöomaisuuden ryhmässä olevan käyttöomaisuuserän poistotapahtuma vähentää arvoltaan vähäisen käyttöomaisuuden ryhmän nettokirjanpitoarvoa vain poistetulla summalla. Jos käyttöomaisuuserän myyntisumma on kuitenkin suurempi kuin arvoltaan vähäisen käyttöomaisuuden ryhmän nettokirjanpitoarvo, nettokirjanpitoarvo vähennetään nollaan.






