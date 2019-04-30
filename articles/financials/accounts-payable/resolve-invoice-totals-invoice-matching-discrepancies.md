---
title: Ristiriitojen selvittäminen laskusummien täsmäytyksen aikana
description: Voit käyttää laskujen kokonaissummien täsmäytystä varmistamaan, että laskujen kokonaissummien ja odotettujen summien erot ovat hyväksyttävän toleranssin sisällä.
author: abruer
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63f4747c13d70d45404069a200124336d6f54947
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/25/2019
ms.locfileid: "896347"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Ristiriitojen selvittäminen laskusummien täsmäytyksen aikana

[!include [banner](../includes/banner.md)]

Yksi laskujen täsmäytyksen tarkistamisen tyyppi on laskusummien täsmäytys. Määritä järjestelmä suorittamaan laskusummien täsmäytys **Ostoreskontran parametrit** sivun **Laskun oikeellisuustarkistus** -välilehdellä asettamalla **Täsmäytä laskusummat** -vaihtoehdon arvoksi **Kyllä**. 

Voit käyttää laskujen kokonaissummien täsmäytystä varmistamaan, että laskujen kokonaissummien ja odotettujen summien erot ovat hyväksyttävän toleranssin sisällä. Kuutta kokonaissummaa verrataan **Laskusummien täsmäytyksen tiedot** -sivulla. Jos mikään loppusummista eroaa vastaavan ostotilaussumman odotetusta määrästä, merkitään täsmäytysristiriita. 

Voit tarkastella laskua, jolla on loppusumman täsmäytysristiriita, **Toimittajan laskun syöttö** -työtilassa valitsemalla **Odottavat laskut** -ruutu. Valitse sitten Toimintoruudun **Tarkista**-välilehdellä **Täsmäytyksen tiedot**. Jos täsmäytysristiriitoja on havaittu, laskun summan viereen ilmestyy varoituskuvake. Voit tarkastella summia yksityiskohtaisemmin tarkastelemalla laskusummien täsmäytyksen tietoja. 

Kun olet löytänyt ristiriidan, sinun on ehkä otettava yhteys toimittajaan, jos laskun tiedot ovat mielestäsi virheelliset. Suorita sitten jokin seuraavista toimista sen mukaan, millaiseen sopimukseen pääset toimittajan kanssa:

-   Hyväksy hintojen ero ja kirjaa täsmäytysristiriitoja sisältävä lasku. Järjestelmäsi saattaa olla määritetty edellyttämään hyväksynnän ennen laskun kirjaamista, jos sillä on täsmäytysristiriitoja. Tässä tapauksessa sinun on hyväksyttävä täsmäytysristiriita ja valinnaisesti syöttää hyväksyntää koskeva kommentti. Voit sitten valita laskun kirjaamisen.
-   Muuta laskun summa odotetun summan mukaiseksi ja kirjaa lasku.
-   Pyydä toimittajalta täysi hyvitys ja uusi korjattu lasku.

Lisätietoja on ohjeaiheessa [Poikkeusten tutkiminen ja selvittäminen](tasks/research-resolve-exceptions.md).


