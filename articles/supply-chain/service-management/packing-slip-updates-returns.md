---
title: Palautusten pakkausluettelopäivitykset
description: Ennen kuin palautetut nimikkeet voidaan vastaanottaa varastoon, sen tilauksen pakkausluettelo, johon palautetut nimikkeet kuuluvat, on päivitettävä.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87dfad2247c84f8e85074739cfff4a2d1b9f8567
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259695"
---
# <a name="packing-slip-updates-for-returns"></a>Palautusten pakkausluettelopäivitykset  

[!include [banner](../includes/banner.md)]


Ennen kuin palautetut nimikkeet voidaan vastaanottaa varastoon, sen tilauksen pakkausluettelo, johon palautetut nimikkeet kuuluvat, on päivitettävä. Samalla tavoin kuin laskun päivitysprosessi kirjanpitotapahtumaksi pakkausluettelon päivitysprosessi on varastotietueen fyysinen päivitys eli se vahvistaa muutokset varastoon. Kun kyseessä on palautus, käsittelytoimenpiteen vaiheet toteutetaan pakkausluettelon päivityksen aikana.

Pakkausluettelon päivitys voidaan käsitellä joko nimikkeen saapumisen kirjauskansiossa tai palautustilauksessa.

Pakkausluetteloiden kirjaamisprosessin osana on mahdollista liittää pakkausluettelon viitenumero asiakkaan toimitusasiakirjoista tilausriveille. Tämä liitos on valinnainen ja se on tarkoitettu vain tiedoksi. Se ei luo mitään tapahtumaan liittyviä päivityksiä.

Jos kaikki odotetut palautetut nimikkeet eivät ole vielä saapuneet, sisällytä vain vastaanotettu määrä pakkausluettelon päivitykseen. Puuttuvat nimikkeet jätetään tilaukseen siihen saakka, kunnes loput palautuksesta on saapunut.

Pakkausluettelo on päivitettävä, jos nimike lähetetään takaisin karanteenista lähetys- ja vastaanotto-osastolle esimerkiksi tilanteessa, jossa karanteenitarkastaja ei tiedä, mihin nimike varastoidaan. Näin voidaan varmistaa oikeanlainen rekisteröinti sekä karanteenin tuloksena määritettyyn käsittelykoodiin liittyvä toimenpide.

Kun päivität myyntisopimukseen kuuluvan palautetun nimikkeen pakkausluettelon, kyseisen nimikkeen myyntisopimuksen sitoumus päivitetään automaattisesti määrän tai summan muutoksen mukaan. 

## <a name="see-also"></a>Lisätietoja

[Laskun päivitysten suorittaminen palautuksille](perform-invoice-updates-for-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]