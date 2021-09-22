---
title: Päivitysristiriita, kun varaston arvostusmenetelmä on vakiokustannus tai liukuva keskiarvo
description: Päivitysristiriita tapahtuu, kun varaston arvostusmenetelmä on joko standardikustannus tai liukuva keskiarvo
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 920d20d19843ce0cac678c5426c00ec99aa61c61
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476258"
---
# <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Päivitysristiriita tapahtuu, kun varaston arvostusmenetelmä on joko standardikustannus tai liukuva keskiarvo

## <a name="symptoms"></a>Oireet

Kun asiakirjoja, kuten varastokirjauskansioita, ostotilauslaskuja tai myyntitilauslaskuja, kirjataan rinnakkain skaalautuvuuden ja suorituskyvyn vuoksi, tuloksena voi olla virhesanoma päivitysristiriidasta eikä kaikkia asiakirjoja ehkä kirjata. Tämä ongelma voi tapahtua, kun varaston arvostusmenetelmä on joko *standardikustannus* tai *liukuva keskiarvo*. Kumpikin menetelmä on jatkuva kustannuslaskentamenetelmä. Lopullinen kustannus määritetään siis kirjauksen aikana.

Jos käytössä on *Liukuva keskiarvo* -menetelmä, virhesanoma muistuttaa seuraavaa esimerkkiä:

> Varaston arvoa xx.xx ei odoteta suhteellisen kululaskelman jälkeen

Jos käytössä on *Standardikustannus* -menetelmä, virhesanoma muistuttaa seuraavaa esimerkkiä:

> Standardikustannus ei vastaa kirjanpitovaraston arvoa päivityksen jälkeen. Arvo = xx.xx, Määrä = yy.yy, Vakiokustannus = zz.zz

## <a name="workaround"></a>Ongelman kiertäminen

Nämä virheet voidaan välttää tai niitä voidaan vähentää käyttämällä seuraavia kiertotapoja siihen saakka, kunnes Microsoft julkaisee ongelman korjaavan ratkaisun:

- Kirjaa epäonnistuneet asiakirjat uudelleen.
- Luo asiakirjoja, joissa on vähemmän rivejä.
- Vältä desimaaliarvojen käyttämistä standardikustannuksissa. Yritä määrittää vakiokustannus siten, että **Hintamäärä**-kentän arvoksi on määritetty *1*. Jos **Hintamäärä**-arvoksi on määritettävä arvo, joka on suurempi kuin *1*, yritä käyttää yksikön standardikustannuksessa mahdollisimman vähän desimaaleja. (Parhaassa tapauksessa desimaaleja on vähemmän kuin kaksi.) Yritä välttää standardikustannuksen asetuksina esimerkiksi seuraavia: **Hinta** = *10* ja **Hintamäärä** = *3*. Tässä tapauksessa yksikön vakiokustannukseksi tulee nimittäin 3,333333 (jossa desimaaliarvo toistuu).
- Useimmissa asiakirjoissa kannattaa välttää sama tuotannon ja varaston taloushallinnon dimensioyhdistelmän käyttämistä useilla riveillä.
- Vähennä rinnakkaisuutta. (Tässä tapauksessa järjestelmä voi nopeutua, koska päivitysristiriitoja ja uudelleenyrityksiä on vähemmän.)
