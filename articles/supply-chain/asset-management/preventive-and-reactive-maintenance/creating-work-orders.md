---
title: Työtilauksien luonti
description: Tässä ohjeaiheessa selitetään, miten työtilaukset luodaan käyttöomaisuuden hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b23ed3251b2f6cf4f34b423ce2f85301d6ab31a1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875625"
---
# <a name="creating-work-orders"></a>Työtilauksien luonti


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Kun olet ajoittanut ennaltaehkäiseviä kunnossapitotöitä, seuraava vaihe on töiden työtilausten luominen. Sen voi tehdä ylläpitoaikatauluissa. Ylläpitoaikataulun ajoitettujen töiden viitetyypit voivat olla erilaiset:

| Viitetyyppi | Kuvaus                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| Ylläpitosuunnitelmat     | Ennaltaehkäisevät huoltotyöt, jotka perustuvat huoltosuunnitelmatyyppeihin "aika" tai "laskuri".                       |
| Ylläpitokierrokset    | Ennaltaehkäisevät huoltotyöt useille samantyyppistä kunnossapitoa vaativille käyttökohteille.           |
| Ylläpitopyyntö   | Manuaalisesti luotava käyttöomaisuuserän huolto- tai korjauspyyntö, joka voidaan muuntaa työtilaukseksi. |


1. Valitse **Resurssien hallinta** > **Yhteiset** > **Kaikki ylläpitoaikataulut** tai **Avoimet ylläpitoaikataulurivit** tai **Avoimet ylläpitoaikataulupoolit**.

2. Valitse ajoitetut ylläpitotyöt, joille haluat luoda työtilauksen, ja valitse sitten **Työtilaus**. Valittujen rivien ennustetuntien kokonaismäärä näkyy **Ylläpitoennusteen tunnit** -kentässä.

3. Valitse **Parametrit**-osassa, kuinka monta työtilausta tulee tehdä. Voit luoda yhden työtilauksen ylläpitoaikatauluriviä kohden tai useita työtilauksia, jotka perustuvat **Yksi työtilaus per** -osan valintoihin.

4. Valitse **Työtilaustyyppi**, jota käytetään kaikissa työtilauksissa, jotka luot.

5. Valitse **OK**. Yksi tai monta työtilausta luodaan.

![Kuva 1](media/18-preventive-maintenance.png)

