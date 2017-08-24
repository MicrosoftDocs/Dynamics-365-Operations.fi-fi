--- 
title: Luo myyntitilauksen laskut
description: "Tässä tehtävän ohjauksessa kuvataan myyntitilauksen laskuttaminen sekä laskujen yhdistäminen ja eräkäsittely."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 50c0ee41220461e282aace85f10a0e734a2ab688
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-sales-order-invoices"></a>Luo myyntitilauksen laskut

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävän ohjauksessa kuvataan myyntitilauksen laskuttaminen sekä laskujen yhdistäminen ja eräkäsittely. Näissä toimintaohjeissa käytetään esittely-yritystä USMF.


## <a name="create-an-invoice-from-a-sales-order"></a>Laskun luominen myyntitilauksesta
1. Valitse Myyntireskontra > Tilaukset > Myyntitilaukset, jotka on lähetetty mutta joita ei ole laskutettu.
2. Valitse myyntitilaus luettelosta. 
3. Valitse toimintoruudussa Lasku.
4. Valitse Lasku.
    * Ota huomioon, että tälle myyntitilaukselle on liitetty useita pakkausluetteloita. Näkyvissä on vain sana <multiple> pakkausluetteloiden numeroiden sijaan.  
5. Laajenna Parametrit-osa.
    * Kirjauksen arvoksi on annettava Kyllä, jotta lasku kirjataan. Voit myös ottaa kirjauksen pois päältä ja vain tulostaa laskun. Saat kuitenkin saman tuloksen, kun luot proformalaskun laskun sijaan.  
    * Tätä vaihtoehtoa käytetään komentojonotöissä. Kysely suoritetaan, kun komentojonotyö suoritetaan.    
6. Valitse Tulosta-kentässä Jälkeen.
7. Valitse Tulosta lasku -kohdassa Kyllä.
    * Tulostuksenhallinnan avulla voit tulostaa laskusta useita kopioita ja myös lähettää laskun sähköpostitse PDF-tiedostona.  
8. Valitse Tulosta kulut -kentässä Tee yhteenveto.
9. Valitse Tarkista luottoraja -kentässä Saldo.
10. Valitse Peruuta.

## <a name="combine-orders-into-a-single-invoice"></a>Tilausten yhdistäminen yhdeksi laskuksi
1. Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.
2. Etsi asiakas, jolla on useita avoimia laskuja.
3. Valitse avoin myyntitilaus.
4. Valitse samalta asiakkaalta toinen avoin myyntitilaus.
5. Valitse toimintoruudussa Lasku.
6. Valitse lasku.
7. Laajenna Parametrit-osa.
8. Valitse Määrä-kentässä Kaikki.
    * Ota huomioon, että yhteenveto-osassa näkyy kaksi laskua. Yhdistetään laskut yhdeksi laskuksi.  
9. Valitse Yhteenvedon päivitys -kentässä Laskutustili.
10. Valitse Järjestä, kun haluat yhdistää myyntitilaukset yhdeksi laskuksi.
    * Kaksi myyntitilausta on nyt yhdistetty yhdeksi laskuksi.   
11. Valitse Peruuta.
12. Valitse Kyllä.

## <a name="post-invoices-in-a-batch"></a>Laskujen kirjaaminen eränä
1. Valitse Myyntireskontra > Laskut > Erän laskutus > Lasku.
2. Klikkaa Valitse.
3. Valitse OK.
4. Valitse erä.
5. Valitse Kyllä, jos haluat ottaa eräkäsittelyn käyttöön
6. Valitse Toistuminen.
7. Valitse Päivät
8. Valitse OK.
9. Valitse OK.
10. Valitse Peruuta.
11. Valitse Kyllä.


