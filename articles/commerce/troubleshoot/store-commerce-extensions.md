---
title: Store Commerce -laajennusten vianmääritys
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Commerce Store Commerce -sovelluksen laajennusten vianmäärityksestä.
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1a2d6a68b7556d8b4d05529efd90f9e66f0c5925
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269778"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Store Commerce -laajennusten vianmääritys

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja Microsoft Dynamics 365 Commerce Store Commerce -sovelluksen laajennusten vianmäärityksestä.

## <a name="extensions-packages-arent-loaded"></a>Laajennuspaketteja ei ladata

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>Laajennuspaketit eivät näy myyntipisteen \> Asetukset-sivulla

Commerce Runtime (CRT) -käynnistimiä ei ehkä ole päivitetty niin, että ne sisältävät laajennuspaketin, tai niitä ei ole otettu käyttöön. Lisätietoja on kohdassa [Commerce runtime (CRT) laajennettavuus ja käynnistimet](../dev-itpro/commerce-runtime-extensibility-trigger.md).

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>Laajennuspaketit näkyvät myyntipisteen \> Asetukset-sivulla, mutta luetteloa ei ole ladattu.

Vahvista, että laajennuspaketit ovat **C:\\Program Files\\Microsoft Dynamics 365\\10.0\\Store Commerce\\Extensions** -kansiossa. Jos paketit ovat olemassa, siellä pitäisi olla **Myyntipiste**-kansio, joka sisältää luettelon.

Jos **Myyntipiste**-kansiota ei ole, vahvista, että Store commerce -projekti viittaa oikein myyntipisteen laajennusprojektiin. Tarkista projektiviitepolku ja varmista, että se on olemassa. 

Seuraavassa esimerkissä asennusohjelmaprojektissa on ongelmia viitatussa laajennusprojektissa.

![Store Commerce -asennusohjelman projektiviite ei kelpaa.](media/ReferenceNotValid.png)

Jos laajennusprojektin viite on lisätty oikein, asennusohjelmaprojektissa ei ole varoitusta eikä riippuvuusongelmaa, kuten seuraavassa esimerkissä on esitetty.

![Store Commerce -asennusohjelman projektiviite kelpaa.](media/ReferenceValid.png)
