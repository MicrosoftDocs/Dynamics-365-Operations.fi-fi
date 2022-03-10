---
title: Laadunhallinnan nimikeotanta
description: Tässä aiheessa käsitellään nimikeotannan määrittämistä.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea749c470ab1d80f1f3974596a2cd4a1f5b7b32d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578485"
---
# <a name="quality-management-item-sampling"></a>Laadunhallinnan nimikeotanta

[!include [banner](../includes/banner.md)]

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
