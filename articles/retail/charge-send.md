---
title: "Tilauksen toimittaminen eri myymälästä"
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
ms.sourcegitcommit: 797058bdbbdb63a08eb35034ffe3c913307f38df
ms.openlocfilehash: 41434614b01f9a00f2b8a56765ecb90ee07e3d90
ms.contentlocale: fi-fi
ms.lasthandoff: 03/05/2018

---

# <a name="ship-an-order-from-a-different-store"></a>Tilauksen toimittaminen eri myymälästä

[!include [banner](includes/banner.md)]

Dynamics 365 for Retail -sovelluksen Veloita lähetys -toiminnon avulla asiakastilaukset voidaan tehdä yhdessä myymälässä ja lähettää toisesta myymälästä. Myyntipisteasiakasohjelmien asiakastilaukset tukevat useita toteutusvaihtoehtoja. Seuraavassa esitellään joitakin toteutusvaihtoehtoja:
-   Noudo samasta myymälästä eri päivänä.
-   Nouto samasta myymälästä eri päivänä.
-   Lähetys myymälään liitetystä oletuslähetysvarastosta ja toimitus tiettynä päivänä.

Veloita lähetys -toiminto käyttää seuraavia myyntipisteen toimintoja: Lähetä kaikki tuotteet ja Lähetä valitut tuotteet. Näin myymälänhoitaja voi valita lähetyssijainnin, josta tilaus tai tilausrivi voidaan toteuttaa. Oletusarvoisesti lähetyssijainti on myymälään liitetty lähetysvarasto. Myymälänhoitaja voi kuitenkin muuttaa tätä sijaintia ja valita minkä tahansa myymälän, joka on määritetty myymälälle liitettyyn myymälän paikanninryhmään. 

Lähetysosoitteen valintavaihtoehdot säilyvät ennallaan. 

Tilausrivin toteuttamisessa käytettävät toimitustavat perustuvat tuotteiden ja osoitteiden sallittujen toimitustilojen konfiguraatioon. Koska sallittujen toimitustilojen sääntöjä ylläpidetään Retail Headquarters -palvelussa, myyntipisteen asiakasohjelma hakee lähetysrivin sallitut toimitustavat reaaliaikaisesti. 


