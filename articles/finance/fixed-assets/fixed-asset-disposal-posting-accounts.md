---
title: Käyttöomaisuuserän luovutuskirjaustilit
description: Tässä artikkelissa kuvataan, kuinka määritetään kirjanpitotilejä käyttöomaisuuden luovuttamista varten.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: kfend
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1272cdb16396d24b5495f023e7b9fe3dee341507
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871330"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>Käyttöomaisuuserän luovutuskirjaustilit

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka määritetään kirjanpitotilejä käyttöomaisuutta luovutettaessa.

Määritä kirjanpitotilejä käyttöomaisuutta luovuttaessasi valitsemalla **Käyttöomaisuuden kirjausprofiilit** -sivun **Kirjanpitotilit**-pikavälilehdessä **Poistomyynti** ja **Poistohävikki**.

Molempien tapahtumalajien (omaisuuden poisto myymällä tai hävikin kautta) kohdalla kirjanpitotiliä hyvitetään käyttöomaisuuserän luovutusarvolla. Debet kirjataan vastatilille, joka voi olla esimerkiksi pankkitili. Jos käyttöomaisuuserä myydään asiakkaalle, vastatilin asemesta käytetään asiakastiliä. Lisätietoja [Käyttöomaisuuserän poistaminen hävikkinä](dispose-of-a-fixed-asset-as-scrap.md).

Valitse **Poisto**, valitse **Myynti** tai **Hävikki** ja määritä sitten yksityiskohtaiset tilit käyttöomaisuuserän nettokirjanpitoarvon vähentämistä varten. Voit syöttää tietoja myös **Poistoparametrit**-sivun **Kirjausarvo**- ja **Myyntiarvo**-kenttiin. 

Arvoltaan vähäisen käyttöomaisuuden ryhmässä olevan käyttöomaisuuserän poistotapahtuma vähentää arvoltaan vähäisen käyttöomaisuuden ryhmän nettokirjanpitoarvoa vain poistetulla summalla. Jos käyttöomaisuuserän myyntisumma on kuitenkin suurempi kuin arvoltaan vähäisen käyttöomaisuuden ryhmän nettokirjanpitoarvo, nettokirjanpitoarvo vähennetään nollaan.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
