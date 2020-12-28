---
title: Myy ja palauta tuotteet, jotka eivät kuulu myymälän on valikoimaan
description: Dynamics 365 Commerceissa voi myydä ja palauttaa valikoiman ulkopuolisia tuotteita.
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 86c6ecf9ef67ca3ac4ed3c44d930acaa965112b6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412052"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a>Myy ja palauta tuotteet, jotka eivät kuulu myymälän on valikoimaan

[!include [banner](includes/banner.md)]

Jälleenmyyjän yleinen skenaario on tuotteiden myyminen asiakkaalle tai palautusten hyväksyminen asiakkaalta, vaikka tiettyjä tuotteita ei olisi liikkeessä (tuotevalikoimaa ei siis ole myymälässä).

Seuraavassa on joitakin tyypillisiä skenaarioita:

+ Jälleenmyyjällä ei ole kaikkia tuotteita tietyssä kaupassa. Muut tuotteet säilytetään varastossa. Myymälätyöntekijä voi auttaa asiakasta haussa tai varaston tuotteiden selaamisessa, lisätä tuotteet ostoskoriin ja valmistella tilauksen jättämisen valitsemalla toimitustavan, kuten lähetys asiakkaan osoitteeseen tai asiakkaan suorittama tuotekeräily tästä tai toisesta myymälästä.
+ Jälleenmyyjällä ei ole tiettyjä tuotteita myymälässä tai varastossa, mutta tuotteita on muissa myymälöissä. Myymäläpäällikkö voi auttaa asiakasta tuotteiden haussa tai selaamisessa toisessa myymälässä, lisätä ne ostoskoriin ja jättää tilauksen valitsemalla toimitusmenetelmän.
+ Jälleenmyyjällä on useita myymälöitä ja tietyssä kaupungissa tai postinumeroalueella eikä halua pakottaa asiakkaita palauttamaan tuotteita samaan myymälään josta ne ostettiin. Sen sijaan asiakkaat voivat palauttaa tuotteet mihin tahansa myymälään.

Nämä yleiset skenaariot ovat jälleenmyyjien käytettävissä Commercessa. Commercen ominaisuudet:

+ Tuotteiden haku tai selaaminen toisissa myymälöissä
+ Kaikkien julkaistujen tuotteiden haku tai selaaminen.
+ Luo itsepalvelutukkutapahtumia tai asiakastilauksia.
+ Valitse asiakastilausten toimitukset.
+ Nouda nykyisen myymälän tai toisen myymälän tuotteita.
+ Peruuta nykyisen myymälän tai toisen myymälän tuotteiden tilaus.
+ Tilauksen palauttaminen kuitin kanssa tai ilman nykyiseen tai toiseen myymälään.
