---
title: Ristiriitojen selvittäminen laskusummien täsmäytyksen aikana – yleiskatsaus
description: Voit käyttää laskujen kokonaissummien täsmäytystä varmistamaan, että laskujen kokonaissummien ja odotettujen summien erot ovat hyväksyttävän toleranssin sisällä.
author: abruer
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 63413,  ""intro-internal
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.form: VendTotalPriceTolerance
ms.openlocfilehash: fa248622a21b0571b08c97eff507ee1035daa7f9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268584"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a>Ristiriitojen selvittäminen laskusummien täsmäytyksen aikana – yleiskatsaus

[!include [banner](../includes/banner.md)]

Yksi laskujen täsmäytyksen tarkistamisen tyyppi on laskusummien täsmäytys. Määritä järjestelmä suorittamaan laskusummien täsmäytys **Ostoreskontran parametrit** sivun **Laskun oikeellisuustarkistus** -välilehdellä asettamalla **Täsmäytä laskusummat** -vaihtoehdon arvoksi **Kyllä**. 

Voit käyttää laskujen kokonaissummien täsmäytystä varmistamaan, että laskujen kokonaissummien ja odotettujen summien erot ovat hyväksyttävän toleranssin sisällä. Kuutta kokonaissummaa verrataan **Laskusummien täsmäytyksen tiedot** -sivulla. Jos mikään loppusummista eroaa vastaavan ostotilaussumman odotetusta määrästä, merkitään täsmäytysristiriita. 

Voit tarkastella laskua, jolla on loppusumman täsmäytysristiriita, **Toimittajan laskun syöttö** -työtilassa valitsemalla **Odottavat laskut** -ruutu. Valitse sitten Toimintoruudun **Tarkista**-välilehdellä **Täsmäytyksen tiedot**. Jos täsmäytysristiriitoja on havaittu, laskun summan viereen ilmestyy varoituskuvake. Voit tarkastella summia yksityiskohtaisemmin tarkastelemalla laskusummien täsmäytyksen tietoja. 

Kun olet löytänyt ristiriidan, sinun on ehkä otettava yhteys toimittajaan, jos laskun tiedot ovat mielestäsi virheelliset. Suorita sitten jokin seuraavista toimista sen mukaan, millaiseen sopimukseen pääset toimittajan kanssa:

-   Hyväksy hintojen ero ja kirjaa täsmäytysristiriitoja sisältävä lasku. Järjestelmäsi saattaa olla määritetty edellyttämään hyväksynnän ennen laskun kirjaamista, jos sillä on täsmäytysristiriitoja. Tässä tapauksessa sinun on hyväksyttävä täsmäytysristiriita ja valinnaisesti syöttää hyväksyntää koskeva kommentti. Voit sitten valita laskun kirjaamisen.
-   Muuta laskun summa odotetun summan mukaiseksi ja kirjaa lasku.
-   Pyydä toimittajalta täysi hyvitys ja uusi korjattu lasku.

Lisätietoja on kohdassa [Poikkeusten tutkiminen ja selvittäminen](tasks/research-resolve-exceptions.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
