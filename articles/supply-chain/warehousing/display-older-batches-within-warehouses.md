---
title: Varaston vanhojen erien näyttämisen määrittäminen mobiililaitteessa
description: Tässä artikkelissa kerrotaan, miten mobiililaite määritetään näyttämään luettelon sijainneista, joissa on työrivin nykyistä sijaintia vanhempia eriä.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5788b42483f2c3046b0d20f45115b98d62cce213
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900532"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Varaston vanhojen erien näyttämisen määrittäminen mobiililaitteessa

[!include [banner](../includes/banner.md)]

**Näytä varaston vanhat erät** -määrityksellä saadaan näkyviin luettelo sijainnista, joissa on vanhempia eriä kuin työrivin nykyinen sijainti. Näkyvässä sijaintiluettelossa on tietoja sijainnin vanhoista eristä, erien erääntymispäivä ja kunkin erän fyysinen varasto. Voit valita keräilyn uudesta sijainnista tai jatkaa keräilyä nykyisestä sijainnista. 
- Kerää uudesta sijainnista – Jos valitse keräilyn uudesta sijainnista, nykyinen työrivi päivitetään käyttämään uutta sijaintia ja työ jatkuu entiseen tapaan uudessa sijainnissa. Uusi sijainti kelpaa, kun sen käytettävissä oleva määrä kattaa koko työrivin. Jos vaadittu määrä ei ole käytettävissä, työriviä ei päivitetään ja luettelo on näkyvissä. 
- Jatka keräilyä nykyisestä sijainnista – Jos jatkat työrivin nykyisessä sijainnissa, työrivin määrien keräilyä jatketaan alkuperäisestä sijainnista.

## <a name="where-it-applies"></a>Käyttö
Näytä varaston vanhat erät määritetään mobiililaitteen valikkovaihtoehdoissa ja se vaikuttaa erän alempien nimikkeiden keräilyyn.

## <a name="set-up-display-older-batches-within-warehouse"></a>Varaston vanhojen erien näyttämisen määrittäminen
**Näytä varaston vanhat erät** -määritys on valittavissa mobiililaitteen valikossa, kun **Valitse vanhin erä** -asetukseksi on määritetty **Varoitus**.

- Valitse ensin **Varastonhallinta** > **Asetukset** > **Mobiililaite** > **Mobiililaitteen valikkovaihtoehdot**, valitse sitten **Käytä nykyistä työtä** -arvoksi **Kyllä** ja valitse lopuksi **Varoitus** **Valitse vanhin erä** -kentässä. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]