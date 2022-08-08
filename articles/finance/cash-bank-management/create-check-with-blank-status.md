---
title: Sellaisten sekkien luominen, joiden tila on tyhjä
description: Tässä artikkelissa selitetään, miten pankkitilille luodaan tyhjiä sekkejä.
author: angelad116
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 8d3f3857fe5261c1c95d02f3b7c7aaf9db7c096f
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151577"
---
# <a name="create-checks-that-have-blank-status"></a>Sellaisten sekkien luominen, joiden tila on tyhjä

[!include [banner](../includes/banner.md)]

Tässä artikkelissa selitetään tyhjien sekkien luominen. Tyhjää sekkiä voi käyttää esimerkiksi sellaisen sekin kirjaamiseen, joka on vaurioitunut ja jota ei voi käyttää maksamiseen.

**Sekit**-sivulla suoritetaan sekkien ylläpitotehtäviä. Siellä voidaan esimerkiksi luoda uusia sekkinumeroita ja poistaa sekkejä. Voit myös luoda sekkejä, joiden tila on **Tyhjä**. Kun tyhjiä sekkejä on luotu, niitä ei voi poistaa tai käyttää uudelleen järjestelmässä.

> [!NOTE]
> Tämä toiminto on käytössä **Sekit**-sivulla vain, jos **Luo sekkisivulla sekkejä, joilla on tyhjä tila** -toiminto otetaan käyttöön **Toimintojen hallinta** -sivulla. Jos toiminto ei ole käytössä, sekkejä, joiden tila on **Tyhjä**, voidaan luoda vain **Maksu sekillä** -valintaikkunassa ostoreskontran maksunluontiprosessin aikana.

Avaa **Sekit**-sivu siirtymällä kohtaan **Kassan ja pankkitoiminnan hallinta \> Pankkitilit \> Pankkitilit** ja valitse sitten **Aiheeseen liittyviä tietoja** -ryhmän **Maksujen hallinta**-välilehdellä kohta **Sekit**. Vaihtoehtoisesti voit siirtyä kohtaan **Kassa- ja pankkitoiminnan hallinta \> Kyselyt ja raportit \> Sekit**.

Tämän jälkeen sekkejä, joiden tila on **Tyhjä**, voidaan luoda valitsemalla toimintoruudussa **Luo tyhjiä sekkejä**. Kun järjestelmä luo tyhjiä sekkejä, niihin liittyvä pankkitili on väliaikaisesti pois käytöstä. Tämä toimintatapa vähentää riskiä siitä, että maksuja luodaan samaan aikaan, kun luodaan tyhjiä sekkejä. Kun käsittely on valmis, asianosainen pankkitili aktivoidaan uudelleen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
