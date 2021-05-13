---
title: Laadunhallinnan nimikeotanta
description: Tässä aiheessa käsitellään nimikeotannan määrittämistä.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956632"
---
# <a name="quality-management-item-sampling"></a>Laadunhallinnan nimikeotanta

Nimikeotantaa käytetään laatuliitoksen osana. Se määrittää nykyisen fyysisen varaston määrän, joka on tarkastettava. Otanta voi perustua kiinteisiin määriin, prosenttiosuuteen tai täyteen rekisterikilpeen.

## <a name="set-up-item-sampling"></a>Nimikeotannan määrittäminen

Voit määrittää nimikeotannan noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Nimikeotanta**.
1. Valitse **Uusi**.
1. Kirjoita arvo **Nimikeotanta**-kenttään.
1. Anna arvo **Kuvaus**-kentässä.
1. Kirjoita numero **Arvo**-kenttään. Tämä arvo liittyy määrän määrityksen arvoon, joka valitaan viereisessä kentässä.
1. Valitse **Prosessi**-osassa **Täysi esto** -valintaruutu, jos koko erä tai tilausrivin määrä estetään, jos testi epäonnistuu. Jos tämän valintaruudun valinta poistetaan, vain laatutilauksen nimikkeet estetään, jos testi epäonnistuu.
1. Valitse **Tallenna**.
1. Sulje sivu.

> [!NOTE]
> *Varastoprosessien laadunhallinta* -toiminto tarjoaa lisää nimikkeen otantatoimintoja. Se lisää käsitteen *Nimikkeen otanta-alueesta* ja mahdollisuuden määrittää täyden rekisterikilven määrä määritykseksi. Jos olet ottanut tämän toiminnon käyttöön, lisätietoja on kohdassa [Varastoprosessien laadunhallinta](quality-management-for-warehouses-processes.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
