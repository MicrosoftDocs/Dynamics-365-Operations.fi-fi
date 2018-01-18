---
title: Valikoiman ulkopuolisten tuotteiden myyminen ja palauttaminen
description: "Dynamics 365 for Retaililla voit myydä ja palauttaa valikoiman ulkopuolisia tuotteita."
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fd00da1242964dddda5c19d46e61da33997e6d02
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="sell-and-return-products-outside-of-an-assortment"></a>Valikoiman ulkopuolisten tuotteiden myyminen ja palauttaminen
Jälleenmyyjän yleinen skenaario on tuotteiden myyminen asiakkaalle tai palautusten hyväksyminen asiakkaalta, vaikka tiettyjä tuotteita ei olisi liikkeessä (ts. tuotevalikoimaa ei ole myymälässä).
Seuraavassa on joitakin tyypillisiä skenaarioita:

+ Jälleenmyyjällä ei ole kaikkia tuotteita tietyssä kaupassa. Muut tuotteet säilytetään varastossa. Myymälätyöntekijä voi auttaa asiakasta haussa tai varaston tuotteiden selaamisessa, lisätä tuotteet ostoskoriin ja valmistella tilauksen jättämisen valitsemalla toimitustavan, kuten lähetys asiakkaan osoitteeseen tai asiakkaan suorittama tuotekeräily tästä tai toisesta myymälästä.
+ Jälleenmyyjällä ei ole tiettyjä tuotteita myymälässä tai varastossa, mutta tuotteita on muissa myymälöissä. Myymäläpäällikkö voi auttaa asiakasta tuotteiden haussa tai selaamisessa toisessa myymälässä, lisätä ne ostoskoriin ja jättää tilauksen valitsemalla toimitusmenetelmän.
+ Jälleenmyyjällä on useita myymälöitä ja tietyssä kaupungissa tai postinumeroalueella eikä halua pakottaa asiakkaita palauttamaan tuotteita samaan myymälään josta ne ostettiin. Sen sijaan asiakkaat voivat palauttaa tuotteet mihin tahansa myymälään.


Nämä yleiset skenaariota ovat jälleenmyyjien käytössä Dynamics 365 for Retailissa. Retailin ominaisuudet:
+ Tuotteiden haku tai selaaminen toisissa myymälöissä
+ Kaikkien julkaistujen tuotteiden haku tai selaaminen.
+ Luo itsepalvelutukkutapahtumia tai asiakastilauksia.
+ Valitse asiakastilausten toimitukset.
+ Nouda nykyisen myymälän tai toisen myymälän tuotteita.
+ Peruuta nykyisen myymälän tai toisen myymälän tuotteiden tilaus.
+ Tilauksen palauttaminen kuitin kanssa tai ilman nykyiseen tai toiseen myymälään.

