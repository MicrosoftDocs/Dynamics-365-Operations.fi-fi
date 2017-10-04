---
title: "Varaston vanhojen erien näyttämisen määrittäminen mobiililaitteessa"
description: "Tässä ohjeaiheessa kerrotaan, miten mobiililaite määritetään näyttämään luettelon sijainneista, joissa on työrivin nykyistä sijaintia vanhempia eriä."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 3e9386f6da7b8bdc1cbb817a78f72c225cbaa9bc
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---

# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Varaston vanhojen erien näyttämisen määrittäminen mobiililaitteessa

[!include[banner](../includes/banner.md)]

**Näytä varaston vanhat erät** -määrityksellä saadaan näkyviin luettelo sijainnista, joissa on vanhempia eriä kuin työrivin nykyinen sijainti. Näkyvässä sijaintiluettelossa on tietoja sijainnin vanhoista eristä, erien erääntymispäivä ja kunkin erän fyysinen varasto. Voit valita keräilyn uudesta sijainnista tai jatkaa keräilyä nykyisestä sijainnista. 
- Kerää uudesta sijainnista – Jos valitse keräilyn uudesta sijainnista, nykyinen työrivi päivitetään käyttämään uutta sijaintia ja työ jatkuu entiseen tapaan uudessa sijainnissa. Uusi sijainti kelpaa, kun sen käytettävissä oleva määrä kattaa koko työrivin. Jos vaadittu määrä ei ole käytettävissä, työriviä ei päivitetään ja luettelo on näkyvissä. 
- Jatka keräilyä nykyisestä sijainnista – Jos jatkat työrivin nykyisessä sijainnissa, työrivin määrien keräilyä jatketaan alkuperäisestä sijainnista.

## <a name="where-it-applies"></a>Käyttö
Näytä varaston vanhat erät määritetään mobiililaitteen valikkovaihtoehdoissa ja se vaikuttaa erän alempien nimikkeiden keräilyyn.

## <a name="set-up-display-older-batches-within-warehouse"></a>Varaston vanhojen erien näyttämisen määrittäminen
**Näytä varaston vanhat erät** -määritys on valittavissa mobiililaitteen valikossa, kun **Valitse vanhin erä** -asetukseksi on määritetty **Varoitus**.

- Valitse ensin **Varastonhallinta** > **Asetukset** > **Mobiililaite** > **Mobiililaitteen valikkovaihtoehdot**, valitse sitten **Käytä nykyistä työtä** -arvoksi **Kyllä** ja valitse lopuksi **Varoitus** **Valitse vanhin erä** -kentässä. 

