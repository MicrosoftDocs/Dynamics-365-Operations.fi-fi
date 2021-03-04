---
title: Indeksikorkojen määrittäminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää indeksikorot. Indeksikorot ovat pakollisia, jos organisaatio liittää maksusummat indeksikorkojoukkoon.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 16b83102aa76f46473138f89ea487e71668a188c
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442965"
---
# <a name="set-up-index-rates"></a>Indeksikorkojen määrittäminen

[!include [banner](../includes/banner.md)]

Jos vuokramaksut riippuvat indeksistä, järjestelmään voidaan lisätä indeksikorkotyypit ja niitä voi ylläpitää siellä. Voit arvostaa vuokrat uudelleen **Indeksikorkotyyppi**-sivulla, jos indeksikoron uudelleenarvostusprosessi käyttää uusinta indeksikorkoa uudelleenarvostuksen päivämäärästä.

Voit lisätä indeksikorkotyyppejä ja indeksikorkoja seuraavasti.

1. Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Indeksikorkotyyppi**.
2. Valitse **Uusi**.
3. Syötä asianmukaisiin kenttiin korkotyyppi ja indeksikoron nimi.
4. Jos haluat lisätä uuden indeksikoron arvon, valitse indeksikorkotyyppi ja valitse sitten **Lisää**.
5. Valitse koron voimassaolon alkamispäivämäärä ja valitse koron arvo.

Sinun on valittava **Indeksikoron arvojen ero**- tai **Indeksikoron arvo** indeksikoron menetelmäksi.

- Valitse **Indeksikoron arvojen ero** -menetelmä, jos haluat laskea uuden vuokran indeksikoron eron perusteella alkupäivämäärän ja uusimman indeksikoron välillä. Indeksikorko määritetään **Indeksikorko (%)** -kentässä.
- Valitse **Indeksikoron arvo** -menetelmä, jos haluat laskea maksun käyttämällä **Indeksikorko (%)** -kentässä määritettyä prosenttilukua.