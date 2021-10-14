---
title: Rahtikirjan luonti
description: Tässä aiheessa kuvataan, miten luot rahtikirjoja, kun käytät varastonhallintaprosesseja.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b79408e21e9acda12617cf35464007e58ae1b5fe
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573126"
---
# <a name="create-a-bill-of-lading"></a>Rahtikirjan luonti

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten luot rahtikirjoja, kun käytät varastonhallintaprosesseja.  

Rahtikirja on lakisääteinen tosite nimikkeiden lähettäjän ja kuljettajan välillä. Asiakirja liitetään toimitettuihin nimikkeisiin ja se toimii lähetyksen vastaanottokuittina, kun nimikkeet toimitetaan kohteeseen. Jos käytät varastonhallintaa, rahtikirjoja voi luoda kahdella tavalla:

  -   Luo raportti manuaalisesti käyttämällä **Rahtikirja**-sivua.
  -   Luo raportti **Kuormasuunnittelun työtilassa**.

Jos luot rahtikirjan **Kuormasuunnittelun työtilassa**, kuorman tilan on oltava **Toimitettu**. Jos kuormassa on useampi kuin yksi toimitus, rahtikirjan luodaan jokaista toimitusta varten. Rahtikirjan luomisen jälkeen voit tehdä muutoksia siihen **Rahtikirja**-sivulla.

## <a name="master-bill-of-lading"></a>Päärahtikirja
Voit luoda päärahtikirjan, kun kuormassa on useampi kuin yksi lähetys Siinä on sama asettelu ja samat tiedot kuin rahtikirjassa, mutta se sisältää yhteenvedon kaikkien lähetysten sisällöstä. Jos **Luo päärahtikirja, kun kuormassa on useampi kuin yksi lähetys** -asetukseksi on määritetty **Kyllä** **Kuljetustenhallintaparametrit**-sivulla, päärahtikirja luodaan automaattisesti, jos luot rahtikirjan **Kuormasuunnittelun työtilassa** ja lähetyksiä on useampi. Voit ladata myös rahtikirjojen luettelon valitsemalla **Aiheeseen liittyviä tietoja** &gt; **Rahtikirja**. Jos olet luomassa rahtikirjat manuaalisesti, voit luoda päärahtikirjan **Rahtikirja**-sivulla.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]