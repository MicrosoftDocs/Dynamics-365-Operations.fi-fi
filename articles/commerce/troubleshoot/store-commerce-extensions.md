---
title: Store Commerce -laajennusten vianmääritys
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Commerce Store Commerce -sovelluksen laajennusten vianmäärityksestä.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: ff26bb76e04c60a9cb975e106456fd781f9300c4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870515"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Store Commerce -laajennusten vianmääritys

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

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
