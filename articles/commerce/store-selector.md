---
title: Myymälän valitsinmoduuli
description: Tässä ohjeaiheessa käsitellään myymälän valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378205"
---
# <a name="store-selector-module"></a>Myymälän valitsinmoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään myymälän valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskuvaus

Myymälän valitsinmoduulia käytetään "Osta verkosta, nouto myymälässä" (BOPIS) -asiakasskenaariossa. Se näyttää luettelon myymälöistä, joissa tuote on noudettavissa, sekä myymälän aukioloajat ja tuotteen varastosaldon kullekin myymälälle.

Myymälän valitsinmoduuli vaatii tuotteen kontekstin ja hakusijainnin myymälöiden löytämiseksi. Jos hakusijaintia ei ole, oletusarvona käytetään asiakkaan selaimen sijaintia edellyttäen, että asiakas antaa suostumuksensa. Moduulissa on syöttöruutu, jonka avulla asiakas voi kirjoittaa sijainnin (postinumeron tai kaupungin ja osavaltion) lähellä olevien myymälöiden löytämiseksi.

Myymälän valitsinmoduuli on integroitu Bing Maps -geokoodauksen ohjelmointirajapintaan, jota käytetään muuntamaan sijainti leveys- ja pituusasteiksi. Bing Maps -ohjelmointirajapinnan avain on pakollinen, ja se on lisättävä kaupankäynnin yhteiset parametrit -sivulla Dynamics 365 Commercessa.

Myymälän valitsinmoduuli voidaan lisätä tuotteen tietosivun (PDP) ostolaatikkomoduuliin, jossa näkyvät myymälät, joissa tuote on noudettavissa. Se voidaan lisätä myös ostoskoriin. Kun tuote lisätään ostoskorimoduuliin, myymälän valitsinmoduuli näyttää kunkin ostoskorin rivinimikkeen noutovaihtoehdot. Lisäksi mukautetulla koodauksella tämä moduuli voidaan lisätä muille sivuille tai moduuleihin laajennusten ja mukautuksien kautta.

Jotta BOPIS-skenaario toimisi, tuotteet on konfiguroitava Asiakasnouto-toimitustilaan. Muussa tapauksessa moduulia ei näytetä vastaavilla sivuilla. Lisätietoja toimitustilan konfiguroinnista on kohdassa [Toimitustapojen määrittäminen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Seuraavassa kuvassa on esimerkki PDP:n käytössä olevasta myymälän valitsinmoduulista.

![Esimerkki myymälän valitsinmoduulista](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a>Myymälän valitsinmoduulin käyttö sähköisessä kaupankäynnissä

- Myymälän valitsinmoduulia voidaan käyttää tuotteen tietosivulla (PDP), etsimään lähimyymälöitä, joissa tuote on noudettavissa.
- Myymälän valitsinmoduulia voidaan käyttää ostoskorisivulla, etsimään lähimyymälöitä, joissa korissa oleva tuote on noudettavissa.

## <a name="store-selector-module-properties"></a>Myymälän valitsinmoduulin ominaisuudet

| Ominaisuuden nimi             | Arvo                 | kuvaus |
|---------------------------|-----------------------|-------------|
| Hakusäde | Numero | Määrittää myymälöiden hakusäteen maileina. Jos arvoa ei määritetä, käytössä on oletushakusäde 50 mailia.|
|Palveluehdot | URL-osoite    |  Palveluehtojen URL-osoite, joka on pakollinen Bing Maps -palvelussa. |

## <a name="add-a-store-selector-module-to-a-page"></a>Myymälän valitsinmoduulin lisääminen sivulle

Myymälän valitsinmoduuli tarvitsee tuotteen kontekstin, joten sitä voi käyttää vain osto- ja ostoskorimoduuleissa. Myymälän valitsinmoduulit eivät toimi näiden moduulien ulkopuolella.

- Lisätietoja myymälän valitsinmoduulin lisäämisestä ostomoduuliin on kohdassa [Ostomoduuli](add-buy-box.md). 
- Lisätietoja myymälän valitsinmoduulin lisäämisestä ostoskorimoduuliin on kohdassa [Ostoskorimoduuli](add-cart-module.md)

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[PDP:n esittely](quick-tour-pdp.md)

[Ostoskorin ja kassan pikaesittely](quick-tour-cart-checkout.md)

[Määritä toimitustavat](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Organisaationi Bing Mapsin hallinta](dev-itpro/manage-bing-maps.md)
