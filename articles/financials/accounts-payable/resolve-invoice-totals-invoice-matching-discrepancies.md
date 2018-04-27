---
title: "Ristiriitojen selvittäminen laskusummien täsmäytyksen aikana"
description: "Voit käyttää laskujen kokonaissummien täsmäytystä varmistamaan, että laskujen kokonaissummien ja odotettujen summien erot ovat hyväksyttävän toleranssin sisällä."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 18250a735d0421daa90b923504aeb94b5003a6a7
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Ristiriitojen selvittäminen laskusummien täsmäytyksen aikana

[!INCLUDE [banner](../includes/banner.md)]

Yksi laskujen täsmäytyksen tarkistamisen tyyppi on laskusummien täsmäytys. Määritä järjestelmä suorittamaan laskusummien täsmäytys **Ostoreskontran parametrit** sivun **Laskun oikeellisuustarkistus** -välilehdellä asettamalla **Täsmäytä laskusummat** -vaihtoehdon arvoksi **Kyllä**. 

Voit käyttää laskujen kokonaissummien täsmäytystä varmistamaan, että laskujen kokonaissummien ja odotettujen summien erot ovat hyväksyttävän toleranssin sisällä. Kuutta kokonaissummaa verrataan **Laskusummien täsmäytyksen tiedot** -sivulla. Jos mikään loppusummista eroaa vastaavan ostotilaussumman odotetusta määrästä, merkitään täsmäytysristiriita. 

Voit tarkastella laskua, jolla on loppusumman täsmäytysristiriita, **Toimittajan laskun syöttö** -työtilassa valitsemalla **Odottavat laskut** -ruutu. Valitse sitten Toimintoruudun **Tarkista**-välilehdellä **Täsmäytyksen tiedot**. Jos täsmäytysristiriitoja on havaittu, laskun summan viereen ilmestyy varoituskuvake. Voit tarkastella summia yksityiskohtaisemmin tarkastelemalla laskusummien täsmäytyksen tietoja. 

Kun olet löytänyt ristiriidan, sinun on ehkä otettava yhteys toimittajaan, jos laskun tiedot ovat mielestäsi virheelliset. Suorita sitten jokin seuraavista toimista sen mukaan, millaiseen sopimukseen pääset toimittajan kanssa:

-   Hyväksy hintojen ero ja kirjaa täsmäytysristiriitoja sisältävä lasku. Järjestelmäsi saattaa olla määritetty edellyttämään hyväksynnän ennen laskun kirjaamista, jos sillä on täsmäytysristiriitoja. Tässä tapauksessa sinun on hyväksyttävä täsmäytysristiriita ja valinnaisesti syöttää hyväksyntää koskeva kommentti. Voit sitten valita laskun kirjaamisen.
-   Muuta laskun summa odotetun summan mukaiseksi ja kirjaa lasku.
-   Pyydä toimittajalta täysi hyvitys ja uusi korjattu lasku.

Lisätietoja on ohjeaiheessa [Poikkeusten tutkiminen ja selvittäminen](tasks/research-resolve-exceptions.md).



