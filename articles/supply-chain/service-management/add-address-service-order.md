---
title: Lisää osoite huoltotilaukseen
description: Tässä ohjeaiheessa kuvataan asiakkaan osoitteen lisääminen huoltotilaukseen.
author: kamaybac
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 055903628b2d72f420415bae5c72d0c7d9d57cba
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573318"
---
# <a name="add-an-address-to-a-service-order"></a>Lisää osoite huoltotilaukseen    

[!include [banner](../includes/banner.md)]


Tässä ohjeaiheessa kuvataan asiakkaan osoitteen lisääminen huoltotilaukseen. Kun luot huoltotilauksen, osoitetiedot siirretään siitä projektista, johon huoltotilaus liittyy. Voit kuitenkin valita vaihtoehtoisen sijainnin osoitteista, jotka on jo määritetty Microsoft Dynamics AX:ssä asiakkaille, toimittajille, sivustoille, varastoille, huoltotilauksille ja projekteille.

Voit myös luoda uuden osoitteen. Oletusarvon mukaan uusi osoite siirretään projektiin. Voit määrittää, että uutta osoitetta käytetään vain tässä palveluesiintymässä. Jos teet niin, uutta osoitetta ei siirretä projektiin.

## <a name="create-a-customer-address-for-a-service-order"></a>Luo asiakkaan osoite palvelutilaukselle

Voit lisätä osoitteen huoltotilaukseen seuraavasti:

1.  Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.

2.  Avaa huoltotilaus, jolle haluat luoda osoitteen.

3.  Napsauta **Toimintoruudussa** **Muokkaa** ja napsauta sitten **Otsikkonäkymä**.

4.  Valitse **Osoite**-pikavälilehdessä **Lisää osoite**.

5.  Valitse **Uusi osoite** -lomakkeessa yksilöivä nimi osoitteelle ja täytä muut kentät. 
    

    > [!WARNING]
    > <P>Jos annat saman nimen olemassa olevana osoitteena, tiedot, jotka kirjoitat muihin kenttiin, korvaavat aiemmat osoitetiedot.</P>


6.  Valitse **OK** kopioidaksesi huoltotilaukseen uuden osoitteen.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Vaihtoehtoisen osoitteen määrittäminen huoltotilaukseen

Voit lisätä vaihtoehtoisen osoitteen huoltotilaukseen seuraavasti:

1.  Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.

2.  Avaa huoltotilaus, jolle haluat kirjoittaa vaihtoehtoisen osoitteen.

3.  Napsauta **Toimintoruudussa** **Muokkaa** ja napsauta sitten **Otsikkonäkymä**.

4.  Valitse **Osoite**-pikavälilehdessä **Muu osoite**.

5.  Valitse **Osoitteen valinta** -lomakkeessa **Tietuetyyppi** -kentässä **Huoltotilaukset**.

6.  Valitse osoite ja napsauta sitten **OK** kopioidaksesi sen huoltotilaukseen.


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]