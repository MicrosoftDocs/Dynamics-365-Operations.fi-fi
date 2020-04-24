---
title: Työtilauksien luonti
description: Tässä ohjeaiheessa selitetään, miten työtilaukset luodaan käyttöomaisuuden hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206124"
---
# <a name="creating-work-orders"></a>Työtilauksien luonti

[!include [banner](../../includes/banner.md)]

 

Kun olet ajoittanut ennaltaehkäiseviä kunnossapitotöitä, seuraava vaihe on töiden työtilausten luominen. Sen voi tehdä ylläpitoaikatauluissa. Ylläpitoaikataulun ajoitettujen töiden viitetyypit voivat olla erilaiset:

| Viitetyyppi | Kuvaus                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| Ylläpitosuunnitelmat     | Ennaltaehkäisevät huoltotyöt, jotka perustuvat huoltosuunnitelmatyyppeihin "aika" tai "laskuri".                       |
| Ylläpitokierrokset    | Ennaltaehkäisevät huoltotyöt useille samantyyppistä kunnossapitoa vaativille käyttökohteille.           |
| Ylläpitopyyntö   | Manuaalisesti luotava käyttöomaisuuserän huolto- tai korjauspyyntö, joka voidaan muuntaa työtilaukseksi. |


1. Valitse **Resurssien hallinta** > **Yhteiset** > **Kaikki ylläpitoaikataulut** tai **Avoimet ylläpitoaikataulurivit** tai **Avoimet ylläpitoaikataulupoolit**.

2. Valitse ajoitetut ylläpitotyöt, joille haluat luoda työtilauksen, ja valitse sitten **Työtilaus**. Valittujen rivien ennustetuntien kokonaismäärä näkyy **Luo työtilauksia** - valintaikkunan **Ylläpitoennusteen tunnit** -kentässä.

3. Valitse **Parametrit**-osassa, kuinka monta työtilausta tulee tehdä. Voit luoda yhden työtilauksen ylläpitoaikatauluriviä kohden tai useita työtilauksia, jotka perustuvat **Yksi työtilaus per** -osan valintoihin.

4. Valitse **Työtilaustyyppi**, jota käytetään kaikissa työtilauksissa, jotka luot. Seuraavassa kuvassa on esimerkki **Luo työtilauksia** -valintaikkunasta.

![Kuva 1](media/18-preventive-maintenance.png)

5. Valitse **OK**. Yksi tai monta työtilausta luodaan.

