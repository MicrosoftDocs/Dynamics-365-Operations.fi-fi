---
title: Sellaisten sekkien luominen, joiden tila on tyhjä
description: Tässä ohjeaiheessa selitetään, miten pankkitilille luodaan tyhjiä sekkejä sekkisivulla.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: aa1c4c33b977c0173da98aee409389b9242980fb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976446"
---
# <a name="create-checks-that-have-blank-status"></a>Sellaisten sekkien luominen, joiden tila on tyhjä

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa selitetään tyhjien sekkien luominen. Tyhjää sekkiä voi käyttää esimerkiksi sellaisen sekin kirjaamiseen, joka on vaurioitunut ja jota ei voi käyttää maksamiseen.

**Sekit**-sivulla suoritetaan sekkien ylläpitotehtäviä. Siellä voidaan esimerkiksi luoda uusia sekkinumeroita ja poistaa sekkejä. Voit myös luoda sekkejä, joiden tila on **Tyhjä**. Kun tyhjiä sekkejä on luotu, niitä ei voi poistaa tai käyttää uudelleen järjestelmässä.

> [!NOTE]
> Tämä toiminto on käytössä **Sekit**-sivulla vain, jos **Luo sekkisivulla sekkejä, joilla on tyhjä tila** -toiminto otetaan käyttöön **Toimintojen hallinta** -sivulla. Jos toiminto ei ole käytössä, sekkejä, joiden tila on **Tyhjä**, voidaan luoda vain **Maksu sekillä** -valintaikkunassa ostoreskontran maksunluontiprosessin aikana.

Avaa **Sekit**-sivu siirtymällä kohtaan **Kassan ja pankkitoiminnan hallinta \> Pankkitilit \> Pankkitilit** ja valitse sitten **Aiheeseen liittyviä tietoja** -ryhmän **Maksujen hallinta**-välilehdellä kohta **Sekit**. Vaihtoehtoisesti voit siirtyä kohtaan **Kassa- ja pankkitoiminnan hallinta \> Kyselyt ja raportit \> Sekit**.

Tämän jälkeen sekkejä, joiden tila on **Tyhjä**, voidaan luoda valitsemalla toimintoruudussa **Luo tyhjiä sekkejä**. Kun järjestelmä luo tyhjiä sekkejä, niihin liittyvä pankkitili on väliaikaisesti pois käytöstä. Tämä toimintatapa vähentää riskiä siitä, että maksuja luodaan samaan aikaan, kun luodaan tyhjiä sekkejä. Kun käsittely on valmis, asianosainen pankkitili aktivoidaan uudelleen.
