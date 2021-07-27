---
title: Jäännöspoisto jaon jälkeen
description: Tässä ohjeaiheessa kuvataan menetelmä, jota käytetään resurssissa poiston laskemiseen sen jälkeen, kun resurssi on jaettu käyttämällä jäännöspoistomenetelmää.
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b3a8fe37ae97cf3b14f5121274603cd30de3304b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356772"
---
# <a name="reduce-balance-depreciation-after-a-split"></a>Jäännöspoisto jaon jälkeen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan menetelmä, jota käytetään resurssissa poiston laskemiseen sen jälkeen, kun resurssi on jaettu toiseen resurssiin käyttämällä jäännöspoistomenetelmää. Käyttöomaisuuskirjaan määritetty poistovuosi on tilikausi. Lisätietoja on kohdassa [Jäännöspoisto](reduce-balance-depreciation.md) ja [Käyttöomaisuuserän jakaminen](tasks/split-fixed-asset.md).

Jos jaat resurssin sellaisen tilikauden aikana, joka on myöhempi kuin resurssin hankinnan tilikausi, jäännöspoisto ottaa huomioon resurssin nettokirjanpitoarvon edelliseltä vuodelta. Se myös ottaa huomioon hankinta- ja poistooikaisutapahtumat, jotka on luotu resurssin jakamasta tapahtumasta. Tämä toiminto olettaa, että resurssi on hankittu yhden tilivuoden aikana ja jaettu seuraavan tilivuoden aikana. Summa, joka on poistettava alkuperäisestä resurssista jakamisen jälkeen, vastaa resurssin nettokirjanpitoarvoa ennen resurssin jakamista ja jaolle kirjattua poiston oikaisutapahtumaa.

Esimerkiksi seuraavat ehdot ovat voimassa:

- Tilikausi on 30.6.-1.7.
- Jäännösarvoprosentti on 18 ja resurssi hankitaan kesäkuussa 2019. Hankintahinta on 10 000 $.
- Ensimmäisen tilivuoden poisto on 18 000 $, kuukausittainen poisto on 150 $ ja resurssi on poistettu marraskuussa 2019, summa 738,75 $.
- Marraskuussa 2019 80 prosenttia resurssista jaetaan toiselle käyttöomaisuuserälle.

[![Jäännöspoisto jaon jälkeen.](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)

Alkuperäisen käyttöomaiosuuserän poistettava summa on 1 822,25 $. Tämä summa on sama kuin nettokirjanpitoarvo ennen jakotapahtumaa, kirjattuna (9 111,25 $) lisättynä hankinnan oikaisulla, joka luodaan jakotapahtuman kirjauksen aikana (-8 000 $) lisättynä poiston oikaisulla, joka luodaan jakotapahtuman aikana (711 $). Tämän vuoksi toisen vuoden poisto on (1 822,25 × 18 prosenttia) ÷ 12 = 27,33 $.

Uuden käyttöomaisuudenkäyttöomaisuuserän poistosumma ensimmäisenä vuonna on (8 000 × 18 prosenttia) ÷ 12 = 120 $.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]