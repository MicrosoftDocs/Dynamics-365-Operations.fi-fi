---
title: "Tilausten lähetys toisesta myymälästä käyttämällä Veloita lähetys -toimintoa"
description: "Tässä ohjeaiheessa kuvataan Veloita lähetys -toiminto."
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: e5351086c56d13ef98937aec066be00cdf88fd37
ms.contentlocale: fi-fi
ms.lasthandoff: 01/04/2019

---

# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Tilausten lähetys toisesta myymälästä käyttämällä Veloita lähetys -toimintoa

[!include [banner](includes/banner.md)]

Dynamics 365 for Retail -sovelluksen Veloita lähetys -toiminnon avulla asiakastilaukset voidaan tehdä yhdessä myymälässä ja lähettää toisesta myymälästä.

Myyntipisteasiakasohjelmien asiakastilaukset tukevat useita toteutusvaihtoehtoja. Seuraavassa esitellään joitakin toteutusvaihtoehtoja:

- Noudo samasta myymälästä eri päivänä.
- Nouto samasta myymälästä eri päivänä.
- Lähetys myymälään liitetystä oletuslähetysvarastosta ja toimitus tiettynä päivänä.

Veloita lähetys -toiminto käyttää seuraavia myyntipisteen toimintoja: Lähetä kaikki tuotteet ja Lähetä valitut tuotteet. Näin myymälänhoitaja voi valita lähetyssijainnin, josta tilaus tai tilausrivi voidaan toteuttaa. Oletusarvoisesti lähetyssijainti on myymälään liitetty lähetysvarasto. Myymälänhoitaja voi kuitenkin muuttaa tätä sijaintia ja valita minkä tahansa myymälän, joka on määritetty myymälälle liitettyyn myymälän paikanninryhmään.

Lähetysosoitteen valintavaihtoehdot säilyvät ennallaan.

Tilausrivin toteuttamisessa käytettävät toimitustavat perustuvat tuotteiden ja osoitteiden sallittujen toimitustilojen konfiguraatioon. Koska sallittujen toimitustilojen sääntöjä ylläpidetään Retail Headquarters -palvelussa, myyntipisteen asiakasohjelma hakee lähetysrivin sallitut toimitustavat reaaliaikaisesti.

