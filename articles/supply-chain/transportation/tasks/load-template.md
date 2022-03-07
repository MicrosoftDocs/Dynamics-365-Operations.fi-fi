---
title: Kuormituksen mallipohjat
description: Tässä aiheessa käsitellään kuormamallien määrittämistä ja kuormamallin liittämistä uuteen kuormaan.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0a4070a1dd5d53bb502ba2ab0c91dbdc90ded34d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005049"
---
# <a name="load-templates"></a>Kuormituksen mallipohjat

Kun luot uuden kuorman, voi määrittää kuormamallin. Kuormamallissa on tietoja välineistä ja mitoista, kuten kuorman korkeudesta, leveydestä, syvyydestä ja tilavuudesta.

Tässä aiheessa käsitellään kuormamallien määrittämistä ja kuormamallin liittämistä uuteen kuormaan.

## <a name="set-up-a-load-template"></a>Kuormamallien määrittäminen

1. Valitse **Kuljetustenhallinta \> Määritys \> Kuormituksen luonti \> Kuormamalli**.
1. Lisää uusi malli valitsemalla toimintoruudussa **Uusi** tai muokkaa aiemmin luotua mallia valitsemalla **Muokkaa**.
1. Määritä seuraavat kentät uuden tai aiemmin luodun mallin rivillä:

    - **Kuorman mallitunnus** – anna kuormamallin yksilöivä tunnus.
    - **Laite** – valitse laite, jota käytetään kuorman lähettämiseen.
    - **Kuorman korkeus**, **Kuorman leveys** ja **Kuorman syvyys** – anna kuorman dimensiot.
    - **Kuorman suurin sallittu tilavuus** ja **Suurin sallittu kuorman paino** – anna kuorman suurin sallittu tilavuus ja paino.
    - **Suurin sallittu bruttopaino** – Anna kuorman suurin sallittu bruttopaino. Kuorman bruttopaino sisältää sekä sen taarapainon että sen kuormauspainon.
    - **Suurin sallittu rahdin osien määrä** – anna suurin sallittu rahdin osien määrä, joka kuormassa voi olla.
    - **Pinoa kuorma lattialle** – Valitse tämä valintaruutu lattiakuormitusta varten Lattiakuormaskenaariossa laatikot ovat pinossa lattiasta kattoon ja seinästä seinään konttien kapasiteetin maksimoimiseksi.

1. Valitse toimintoruudussa **Tallenna**.

## <a name="associate-a-load-template-with-a-new-load"></a>Kuormamallin liittäminen uuteen kuormaan

1. Valitse **Kuljetustenhallinta \> Suunnittelu \> Kuormasuunnittelun työtila**.
1. Valitse sivun yläosassa jokin seuraavista välilehdistä sen perusteella, minkälaiselle lähdeasiakirjatyypille luodaan kuorma: **lähetykset**, **myyntirivit**, **siirtorivit** tai **ostotilausrivit**. 
1. Valitse tietty asiakirja, jolle kuorma suunnitellaan.
1. Valitse toimintoruudun **Tarjonta ja kysyntä** -välilehden **Lisää**-ryhmässä kohta **Uuteen kuormaan**.
1. Valitse **Kuormamalli**-valintaikkunan **Kuorman mallitunnus** -kentässä käytettävä malli.
1. Käytä mallia valitsemalla **OK**.
