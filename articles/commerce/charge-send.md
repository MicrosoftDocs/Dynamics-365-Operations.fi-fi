---
title: Tilausten lähetys toisesta myymälästä käyttämällä Veloita lähetys -toimintoa
description: Tässä ohjeaiheessa kuvataan Veloita lähetys -toiminto.
author: ashishmsft
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: b9e0c4f55fd823bf7471edfe6ce1d424b0179d21
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800468"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Tilausten lähetys toisesta myymälästä käyttämällä Veloita lähetys -toimintoa

[!include [banner](includes/banner.md)]

Commercen Veloita lähetys -toiminnon avulla asiakastilaukset voidaan tehdä yhdessä myymälässä ja lähettää toisesta myymälästä.

Myyntipisteasiakasohjelmien asiakastilaukset tukevat useita toteutusvaihtoehtoja. Seuraavassa esitellään joitakin toteutusvaihtoehtoja:

- Noudo samasta myymälästä eri päivänä.
- Nouto samasta myymälästä eri päivänä.
- Lähetys myymälään liitetystä oletuslähetysvarastosta ja toimitus tiettynä päivänä.

Veloita lähetys -toiminto käyttää seuraavia myyntipisteen toimintoja: Lähetä kaikki tuotteet ja Lähetä valitut tuotteet. Näin myymälänhoitaja voi valita lähetyssijainnin, josta tilaus tai tilausrivi voidaan toteuttaa. Oletusarvoisesti lähetyssijainti on myymälään liitetty lähetysvarasto. Myymälänhoitaja voi kuitenkin muuttaa tätä sijaintia ja valita minkä tahansa myymälän, joka on määritetty myymälälle liitettyyn myymälän paikanninryhmään.

Lähetysosoitteen valintavaihtoehdot säilyvät ennallaan.

Tilausrivin toteuttamisessa käytettävät toimitustavat perustuvat tuotteiden ja osoitteiden sallittujen toimitustilojen konfiguraatioon. Koska sallittujen toimitustilojen sääntöjä ylläpidetään Headquarters-palvelussa, myyntipisteen asiakasohjelma hakee lähetysrivin sallitut toimitustavat reaaliaikaisesti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]