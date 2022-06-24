---
title: Tilausten lähetys toisesta myymälästä käyttämällä Veloita lähetys -toimintoa
description: Tässä artikkelissa kuvataan Veloita lähetys -toiminto.
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
ms.openlocfilehash: d73a21bfe9a284bd6e222e73bb0250648912b230
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863510"
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