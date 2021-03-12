---
title: Rahtikirjan luonti
description: Tässä aiheessa kuvataan, miten luot rahtikirjoja, kun käytät varastonhallintaprosesseja.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b001ef8936e7e35db89163683c023211f79b24c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996460"
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



