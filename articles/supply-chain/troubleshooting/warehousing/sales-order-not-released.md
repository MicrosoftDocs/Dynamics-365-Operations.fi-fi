---
title: Myyntitilausta ei voitu vapauttaa lähtevien varaston työvaiheissa
description: Myyntitilauksen vapautuksen epäonnistumista koskevaan virhesanomaan voi olla useita syitä. Tällä sivulla selitetään, mistä se johtuu ja miten ongelma korjataan.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fca5ee1bc97545ea4de56d940fdedd320a6cfe84
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476243"
---
# <a name="sales-order-could-not-be-released-with-outbound-warehouse-operations"></a>Myyntitilausta ei voitu vapauttaa lähtevien varaston työvaiheissa

## <a name="symptoms"></a>Oireet

Kun käytät lähteviä varastotoimintoja, voit saada seuraavan virhesanoman:

> Myyntitilausta ei voitu vapauttaa.

## <a name="cause"></a>Syy

Tämä ongelman esiintymiseen voi olla useita syitä. Tilaus on esimerkiksi luotonhallinnan pidossa eikä lähetyksiä voi luoda, ennen kuin kaikille tilaukseen liitetyille myyntiriveille on annettu kelvollinen postiosoite. Vaihtoehtoisesti kyse voi olla tilauksen pidosta, joka on käsiteltävä, ennen kuin tilaus voidaan vapauttaa varastoon. Kyseinen pito voi olla tilauskohtainen ja se voi olla asiakastilissä.

## <a name="resolution"></a>Ratkaisu

Lisää tai päivitä myyntitilauksen tai myyntitilausten osoite ja vapauta tilaus sitten varastoon. Tilaukset voidaan vapauttaa varastoon vain, jos niissä on kelvollinen toimitusosoite (**Organisaation hallinto** -moduulissa määritetyn osoitemuodon mukaisesti).

Selvitä tilauksen pito ja käsittele ongelmat. Poista sitten pito tilauksesta tai asiakkaasta ja vapauta tilaus varastoon.
