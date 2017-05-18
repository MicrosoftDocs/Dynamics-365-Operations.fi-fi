---
title: "Laskusummien täsmäytyksen ristiriitojen täsmäytys"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c947f84e6510073d49045f93af703c16d0ebc1ba
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Laskusummien täsmäytyksen ristiriitojen täsmäytys

[!include[banner](../includes/banner.md)]




Yksi laskujen täsmäytyksen tarkistamisen tyyppi on laskusummien täsmäytys. Määritä järjestelmä suorittamaan laskusummien täsmäytys **Ostoreskontran parametrit** sivun **Laskun oikeellisuustarkistus** -välilehdellä asettamalla **Täsmäytä laskusummat** -vaihtoehdon arvoksi **Kyllä**. 

Voit käyttää laskujen kokonaissummien täsmäytystä varmistamaan, että laskujen kokonaissummien ja odotettujen summien erot ovat hyväksyttävän toleranssin sisällä. Kuutta kokonaissummaa verrataan **Laskusummien täsmäytyksen tiedot** -sivulla. Jos mikään loppusummista eroaa vastaavan ostotilaussumman odotetusta määrästä, merkitään täsmäytysristiriita. 

Voit tarkastella laskua, jolla on loppusumman täsmäytysristiriita, **Toimittajan laskun syöttö** -työtilassa valitsemalla **Odottavat laskut** -ruutu. Valitse sitten Toimintoruudun **Tarkista**-välilehdellä **Täsmäytyksen tiedot**. Jos täsmäytysristiriitoja on havaittu, laskun summan viereen ilmestyy varoituskuvake. Voit tarkastella summia yksityiskohtaisemmin tarkastelemalla laskusummien täsmäytyksen tietoja. 

Kun olet löytänyt ristiriidan, sinun on ehkä otettava yhteys toimittajaan, jos laskun tiedot ovat mielestäsi virheelliset. Suorita sitten jokin seuraavista toimista sen mukaan, millaiseen sopimukseen pääset toimittajan kanssa:

-   Hyväksy hintojen ero ja kirjaa täsmäytysristiriitoja sisältävä lasku. Järjestelmäsi saattaa olla määritetty edellyttämään hyväksynnän ennen laskun kirjaamista, jos sillä on täsmäytysristiriitoja. Tässä tapauksessa sinun on hyväksyttävä täsmäytysristiriita ja valinnaisesti syöttää hyväksyntää koskeva kommentti. Voit sitten valita laskun kirjaamisen.
-   Muuta laskun summa odotetun summan mukaiseksi ja kirjaa lasku.
-   Pyydä toimittajalta täysi hyvitys ja uusi korjattu lasku.





