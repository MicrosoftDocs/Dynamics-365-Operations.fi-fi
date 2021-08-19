---
title: Palautettujen nimikkeiden osittaisten toimitusten vastaanottaminen
description: Osatoimitukset määritetään palautustilausrivien, ei palautustilauslähetyksen mukaan.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cff714de8b06142fe4c6911db110d707ba7f86584793c73fa54dddf23498f41
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721220"
---
# <a name="receive-partial-deliveries-of-returned-items"></a>Palautettujen nimikkeiden osittaisten toimitusten vastaanottaminen    

[!include [banner](../includes/banner.md)]


Osatoimitukset määritetään palautustilausrivien, ei palautustilauslähetyksen mukaan.

Se tarkoittaa sitä, että jos vastaanotat yhdellä palautustilausrivillä osoitetun koko määrän, mutta et vastaanota mitään muilla palautustilausriveillä osoitettuja määriä, toimitus ei ole osatoimitus. Jos kuitenkin palautustilausrivi edellyttää palautettavaksi tietyn nimikkeen kymmentä yksikköä ja vastaanotat vain neljä, kyseessä on osatoimitus.

Jos palautuslähetyksen määrä on pienempi kuin palautustilausrivin koko määrä, voit siirtää lähetyksen sivuun ja odottaa määrän loppuosan saapumista. Vaihtoehtoisesti voit rekisteröidä osittaisen määrän ja kirjata sen.

## <a name="register-and-post-a-partial-quantity"></a>Osatoimituksen rekisteröiminen ja kirjaaminen

1.  Kun olet valinnut palautustilauksen saapuvaksi **Saapumisten yhteenveto - Varasto: %1, Laituri: %2, Kirjauskansion nimi: %3** -lomakkeessa, valitse **Aloita saapuminen** luodaksesi saapumisen kirjauskansion ja valitse sitten **Kirjauskansiot** \> **Näytä vastaanottojen saapumiset** avataksesi **Sijainnin kirjauskansio** -lomakkeen.

2.  Valitse kirjauskansion rivi, jota haluat käsitellä. Napsauta sitten **Rivit** avataksesi **Kirjauskansion rivit, sijainnit** -lomakkeen.

3.  Valitse sen nimiketunnuksen rivi, jolle saapui vain osa määrästä. Napsauta sitten **Toiminnot** \> **Jako** avataksesi **Jako**-lomakkeen.

4.  Kirjoita **Jaettava määrä** -kenttään vastaanotettujen nimikkeiden kokonaismäärä. Valitse sitten **OK**.

5.  Valitse **Kirjauskansion rivit, sijainnit**  -lomakkeessa määrän vastaanottaneen nimikkeen rivi. Valitse sitten **Kirjaa**. Voit kirjata lisämäärän rivin nimikkeiden saapumisen jälkeen.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]