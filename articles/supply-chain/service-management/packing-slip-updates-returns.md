---
title: Palautusten pakkausluettelopäivitykset
description: Ennen kuin palautetut nimikkeet voidaan vastaanottaa varastoon, sen tilauksen pakkausluettelo, johon palautetut nimikkeet kuuluvat, on päivitettävä.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6f586537aa2d4cb47b0e55e76e401ea6852e1d60
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580381"
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