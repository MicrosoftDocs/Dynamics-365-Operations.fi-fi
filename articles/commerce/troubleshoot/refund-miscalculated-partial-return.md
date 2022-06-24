---
title: Hyvitettävät veloitukset lasketaan väärin palautetun määrän perusteella
description: Tämä artikkeli antaa ohjeita vianmääritykseen, kun kassat näkevät palautetun nimikemäärän virheelliset, palautuskelpoiset maksut myyntipisteessä.
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 7a84207f587a826b9acdfd818c64220c5327bde1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890240"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>Hyvitettävät veloitukset lasketaan väärin palautetun määrän perusteella

[!include [banner](../../includes/banner.md)]

Tämä artikkeli antaa ohjeita vianmääritykseen, kun kassat näkevät palautetun nimikemäärän virheelliset, palautuskelpoiset maksut myyntipisteessä.

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
