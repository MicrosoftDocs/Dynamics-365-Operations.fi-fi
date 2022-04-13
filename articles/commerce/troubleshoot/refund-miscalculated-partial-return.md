---
title: Hyvitettävät veloitukset lasketaan väärin palautetun määrän perusteella
description: Tämä ohjeaihe antaa ohjeita vianmääritykseen, kun kassat näkevät palautetun nimikemäärän virheelliset, palautuskelpoiset maksut myyntipisteessä.
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c8ecaa0cb73d06ac66b57cce815264e841a2259b
ms.sourcegitcommit: 94ebdaae6dc996b205ac78ed546e38f91f4f46ed
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/28/2022
ms.locfileid: "8490212"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>Hyvitettävät veloitukset lasketaan väärin palautetun määrän perusteella

[!include [banner](../../includes/banner.md)]

Tämä ohjeaihe antaa ohjeita vianmääritykseen, kun kassat näkevät palautetun nimikemäärän virheelliset, palautuskelpoiset maksut myyntipisteessä.

## <a name="description"></a>Kuvaus

Asiakas palauttaa osan nimikkeistä, jotka on ostettu myyntitilaukseen, jossa on rivitason palautuskelpoisia kuluja. Osahyvityksen näyttämisen asemesta POS näyttää kaikki kulut, jotka voidaan hyvittää.

Asiakas esimerkiksi ostaa viisi nimikettä 5 dollarilla per nimike, jolloin kokonaiskulut ovat 25 $. Asiakas palauttaa tämän jälkeen kolme viidestä nimikkeestä. Kassanhoitajalle näytetään kuitenkin 25 dollarin palautusmaksu POS:ssa odotetun 15 dollarin hyvitettävän maksun sijaan kolmesta palautetusta tuotteesta.

## <a name="resolution"></a>Ratkaisu

### <a name="turn-on-the-enable-refunding-charges-based-on-the-refunded-quantity-feature"></a>Ota käyttöön Ota käyttöön palautuskulut palautetun määrän perusteella -ominaisuus

Microsoft Dynamics 365 Commercen versiosta 10.0.26 alkaen **Ota hyvitysmaksut käyttöön palautetun määrän perusteella** -ominaisuus mahdollistaa rivitason hyvitettävien maksujen laskemisen palautettavien tuotteiden määrän perusteella.

Ota **Käyttöön palautusten hyvityskulut, jotka perustuvat hyvitettyihin määriin** -ominaisuus käyttöön Commerce headquartersissa, noudattamalla seuraavia ohjeita.

1. Avaa **Ominaisuuksien hallinta** -työtila (**Järjestelmänvalvoja \> Työtilat\> Ominaisuuksien hallinta**).
1. Etsi käytettävissä olevien ominaisuuksien luettelosta ja valitse **Ota palautuskulut käyttöön palautetulle määrälle** -ominaisuus.
1. Valitse oikeanpuoleisesta ruudusta **Ota käyttöön nyt**.
