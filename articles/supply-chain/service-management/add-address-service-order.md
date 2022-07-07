---
title: Lisää osoite huoltotilaukseen
description: Tässä artikkelissa kuvataan asiakkaan osoitteen lisääminen huoltotilaukseen.
author: sorenva
ms.date: 06/15/2020
ms.topic: article
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c485c50bab7c2e945aa0f0fc0601008dcebd3328
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015722"
---
# <a name="add-an-address-to-a-service-order"></a>Lisää osoite huoltotilaukseen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan asiakkaan osoitteen lisääminen huoltotilaukseen. Kun luot huoltotilauksen, osoitetiedot siirretään siitä projektista, johon huoltotilaus liittyy. Voit kuitenkin valita vaihtoehtoisen sijainnin osoitteista, jotka on jo määritetty Microsoft Dynamics AX:ssä asiakkaille, toimittajille, sivustoille, varastoille, huoltotilauksille ja projekteille.

Voit myös luoda uuden osoitteen. Oletusarvon mukaan uusi osoite siirretään projektiin. Voit määrittää, että uutta osoitetta käytetään vain tässä palveluesiintymässä. Jos teet niin, uutta osoitetta ei siirretä projektiin.

## <a name="create-a-customer-address-for-a-service-order"></a>Luo asiakkaan osoite palvelutilaukselle

Voit lisätä osoitteen huoltotilaukseen seuraavasti:

1. Siirry kohtaan **Palveluiden hallinta** \> **Huoltotilaukset** \> **Huoltotilaukset**.

1. Avaa huoltotilaus, jolle haluat luoda osoitteen.

1. Avaa **Otsikko**-välilehti.

1. Laajenna **Osoite**-pikavälilehti ja valitse pikavälilehden työkaluriviltä **Lisää osoite** -kohta.

1. Valitse **Uusi osoite** -valintaikkunassa yksilöivä nimi osoitteelle ja täytä muut kentät. 

    > [!WARNING]
    > Jos annat saman nimen olemassa olevana osoitteena, tiedot, jotka kirjoitat muihin kenttiin, korvaavat aiemmat osoitetiedot.

1. Valitse **OK** kopioidaksesi huoltotilaukseen uuden osoitteen.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Vaihtoehtoisen osoitteen määrittäminen huoltotilaukseen

Voit lisätä vaihtoehtoisen osoitteen huoltotilaukseen seuraavasti:

1. Siirry kohtaan **Palveluiden hallinta** \> **Huoltotilaukset** \> **Huoltotilaukset**.

1. Avaa huoltotilaus, jolle haluat kirjoittaa vaihtoehtoisen osoitteen.

1. Avaa **Otsikko**-välilehti.

1. Laajenna **Osoite**-pikavälilehti ja valitse pikavälilehden työkaluriviltä **Muu osoite** -kohta.

1. Valitse **Osoitteen valinta** -valintaikkunassa **Huoltotilaukset** ruudukon yläpuolella olevasta avattavasta luettelosta.

1. Valitse osoite ja valitse sitten **OK** kopioidaksesi sen huoltotilaukseen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]