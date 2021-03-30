---
title: Siirtotilausten varastojen määrittäminen
description: Tässä ohjeaiheessa käsitellään siirtotilausten varastojen määrittämistä.
author: Mirzaab
manager: tfehr
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e01629982bb383078e90ff3dad0592371f44bd1b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206844"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>Siirtotilausten varastojen määrittäminen 

[!include [banner](../includes/banner.md)]

Varastotasoja käyttämällä voidaan luoda hierarkia, joka tukee varastojen välisiä siirtotilauksia. Tämän määrityksen mukaan pääajoitus laskee nimikkeiden tarpeen kullakin varastotasolla ja täyttää tarpeet luomalla suunnitellut siirtotilaukset, joiden mukaan siirtäminen tapahtuu varastojen välillä.

1.  Valitse **Varastonhallinta > Asetukset > Inventaarioanalyysi > Varastot**.

2.  Valitse varasto, jota haluat täydentää.

3.  Valitse **Pääsuunnittelu**-pikavälilehdessä **Uudelleentäyttö**-valintaruutu.

4.  Valitse **Päävarasto**-kentässä varasto, jota haluat käyttää täydennysvarastona. Pääajoitus laskee valittua varastoa koskevan siirtovaatimuksen ja luo suunnitellun siirtotilauksen, jonka mukaan siirto tapahtuu määritetystä **päävarastosta**.
   
    > [!NOTE]
    > <P>Jos tyhjennät <STRONG>Uudelleentäyttö</STRONG>-valintaruudun, valitulle varastolle määritetään <STRONG>päävarastoa</STRONG> koskeva varastotaso, mutta <STRONG>päävarastoa</STRONG> ei määritetä täydennysvarastoksi.</P>

5.  Valitse sivu, joilla uusia asetuksia käytetään.


> [!TIP]
> <P>Jos haluat määrittää varaston täydennystä varten, määritä varasto ensin varastodimensioksi <STRONG>Varastodimensioryhmät</STRONG>-sivulla. Valitse tällä sivulla <STRONG>Aktiivinen</STRONG>-kenttä ja varaston <STRONG>Kattavuussuunnitelma dimension mukaan</STRONG> -kenttä.</P>

## <a name="set-up-transport-lead-time"></a>Kuljetusajan määrittäminen

Määritä myös varastojen välinen kuljetusaika **Kuljetusvuorokaudet**-sivulla. 
1. Valitse **Inventoinnin- ja varastonhallinta > Asetukset > Toimitus > Kuljetusvuorokaudet**.
2. Valitse **Vastaanottopiste**-kentässä **varasto**.
3. Valitse **Lähetysvarasto**, **Vastaanottovarasto** ja **Kuljetusvuorokaudet**. 
4. (Valinnainen) Voit määrittää myös kuljetusajan toimitustavan mukaan **Kuljetuspäivät toimitustavan mukaan** -välilehdessä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]