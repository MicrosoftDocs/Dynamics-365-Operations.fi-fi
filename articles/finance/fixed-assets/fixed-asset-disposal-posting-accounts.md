---
title: Käyttöomaisuuserän luovutuskirjaustilit
description: Tässä ohjeaiheessa kuvataan, kuinka määritetään kirjanpitotilejä käyttöomaisuuden luovuttamista varten.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c82cb8b82f2cc8424675f76c68613a2b5aa76745
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675515"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>Käyttöomaisuuserän luovutuskirjaustilit

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan, kuinka määritetään kirjanpitotilejä käyttöomaisuutta luovutettaessa.

Määritä kirjanpitotilejä käyttöomaisuutta luovuttaessasi valitsemalla **Käyttöomaisuuden kirjausprofiilit** -sivun **Kirjanpitotilit**-pikavälilehdessä **Poistomyynti** ja **Poistohävikki**.

Molempien tapahtumalajien (omaisuuden poisto myymällä tai hävikin kautta) kohdalla kirjanpitotiliä hyvitetään käyttöomaisuuserän luovutusarvolla. Debet kirjataan vastatilille, joka voi olla esimerkiksi pankkitili. Jos käyttöomaisuuserä myydään asiakkaalle, vastatilin asemesta käytetään asiakastiliä. Lisätietoja [Käyttöomaisuuserän poistaminen hävikkinä](dispose-of-a-fixed-asset-as-scrap.md).

Valitse **Poisto**, valitse **Myynti** tai **Hävikki** ja määritä sitten yksityiskohtaiset tilit käyttöomaisuuserän nettokirjanpitoarvon vähentämistä varten. Voit syöttää tietoja myös **Poistoparametrit**-sivun **Kirjausarvo**- ja **Myyntiarvo**-kenttiin. 

Arvoltaan vähäisen käyttöomaisuuden ryhmässä olevan käyttöomaisuuserän poistotapahtuma vähentää arvoltaan vähäisen käyttöomaisuuden ryhmän nettokirjanpitoarvoa vain poistetulla summalla. Jos käyttöomaisuuserän myyntisumma on kuitenkin suurempi kuin arvoltaan vähäisen käyttöomaisuuden ryhmän nettokirjanpitoarvo, nettokirjanpitoarvo vähennetään nollaan.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
