---
title: Sellaisten sekkien luominen, joiden tila on tyhjä
description: Tässä artikkelissa selitetään, miten pankkitilille luodaan tyhjiä sekkejä.
author: angelad116
ms.date: 10/24/2022
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
ms.openlocfilehash: 86020d9088d8135c83716128a77090608536a78f
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804015"
---
# <a name="create-checks-that-have-blank-status"></a>Sellaisten sekkien luominen, joiden tila on tyhjä

[!include [banner](../includes/banner.md)]

Tässä artikkelissa selitetään tyhjien sekkien luominen. Tyhjää sekkiä voi käyttää esimerkiksi sellaisen sekin kirjaamiseen, joka on vaurioitunut ja jota ei voi käyttää maksamiseen.

**Sekit**-sivulla suoritetaan sekkien ylläpitotehtäviä. Siellä voidaan esimerkiksi luoda uusia sekkinumeroita ja poistaa sekkejä. Voit myös luoda sekkejä, joiden tila on **Tyhjä**. Kun tyhjiä sekkejä on luotu, niitä ei voi poistaa tai käyttää uudelleen järjestelmässä.

> [!NOTE]
> Tämä toiminto on käytössä **Sekit**-sivulla vain, jos **Luo sekkisivulla sekkejä, joilla on tyhjä tila** -toiminto otetaan käyttöön **Toimintojen hallinta** -sivulla. Jos toiminto ei ole käytössä, sekkejä, joiden tila on **Tyhjä**, voidaan luoda vain **Maksu sekillä** -valintaikkunassa ostoreskontran maksunluontiprosessin aikana.

Avaa **Sekit**-sivu siirtymällä kohtaan **Kassan ja pankkitoiminnan hallinta \> Pankkitilit \> Pankkitilit** ja valitse sitten **Aiheeseen liittyviä tietoja** -ryhmän **Maksujen hallinta**-välilehdellä kohta **Sekit**. Vaihtoehtoisesti voit siirtyä kohtaan **Kassa- ja pankkitoiminnan hallinta \> Kyselyt ja raportit \> Sekit**.

Tämän jälkeen sekkejä, joiden tila on **Tyhjä**, voidaan luoda valitsemalla toimintoruudussa **Luo tyhjiä sekkejä**. Kun luodaan tyhjiä sekkejä, niihin liittyvä pankkitili on väliaikaisesti pois käytöstä. Tämä toimintatapa vähentää riskiä siitä, että maksuja luodaan samaan aikaan, kun luodaan tyhjiä sekkejä. Kun käsittely on valmis, asianosainen pankkitili aktivoidaan uudelleen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
