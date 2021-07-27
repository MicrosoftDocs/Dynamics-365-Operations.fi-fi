---
title: Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi
description: Tässä ohjeaiheessa käsitellään, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi luoda konfigurointilpalvelun.
author: NickSelin
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9428ff1f53928f104df4736911ce34756128da44
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359432"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa käsitellään tapaa, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi luoda konfigurointilähteen sähköiselle raportoinnille (ER). Kunkin ER-konfiguraation tekijänä pidetään lähdettä. Tässä esimerkissä luodaan konfiguraation lähde malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraation lähteet.

## <a name="create-a-provider"></a>Luo lähde
1. Valitse **siirtymisruutu** vasemmassa yläkulmassa ja valitsemalla **Organisaation hallinto**.
2. Valitse **Työtilat > Sähköinen raportointi**.
3. Valitse **Liittyvät linkit > Konfiguraation lähteet**.
4. Valitse **Uusi**.
    - Lähdetietueella on yksilöivä nimi ja URL-osoite. Tarkista tämän sivun sisältö ja ohita tämä menettely, jos Litware, Inc. (https://www.litware.com) on jo luotu.  
5. Syötä Nimi-kenttään `Litware, Inc.`.
6. Kirjoita Internet-osoite-kenttään `https://www.litware.com`.
7. Valitse **Tallenna**.
8. Sulje sivu.

## <a name="select-as-an-active-provider"></a>Valitse aktiiviseksi lähteeksi
1. Valitse lähteeksi Litware, Inc.
2. Valitse **Määritä aktiivinen**.

![Sähköisen raportoinnin työtilan sivu.](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]