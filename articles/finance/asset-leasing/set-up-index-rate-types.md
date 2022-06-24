---
title: Indeksikorkojen määrittäminen
description: Tässä artikkelissa kerrotaan, kuinka voit määrittää indeksikorot. Indeksikorot ovat pakollisia, jos organisaatio liittää maksusummat indeksikorkojoukkoon.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRateType
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e700c6c0c66b855a3e329302ac27681f4d0144a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883384"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
