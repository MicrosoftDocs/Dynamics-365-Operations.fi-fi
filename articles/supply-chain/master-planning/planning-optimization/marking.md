---
title: Varastomerkintä suunnittelun optimoinnissa
description: Tässä aiheessa on tietoja vahvistettujen tilausten varaston merkintävaihtoehdoista suunnittelun optimointia käytettäessä.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7813f570afb0260e6740507c9504320c3e87be93
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263347"
---
# <a name="inventory-marking-with-planning-optimization"></a>Varastomerkintä suunnittelun optimoinnissa

[!include [banner](../../includes/banner.md)]

Tässä aiheessa on tietoja vahvistettujen tilausten varaston merkintävaihtoehdoista suunnittelun optimointia käytettäessä.

*Merkintää* käytetään linkittämään kysyntä ja tarjonta. Se muistuttaa *tarvekohdistusta*, joka ilmaisee, miten pääsuunnittelun odotetaan kattavan kysynnän. Suunnittelun kannalta suurin ero on siinä, että merkintä on pysyvämpää kuin tarvekohdistus.

Merkintä otettiin käyttöön tukemaan kustannuslaskennan FIFO- ja LIFO-erityisskenaarioita. Sitä käytetään nyt kuitenkin myös joissakin muissa kuin kustannuslaskentaskenaarioissa. Tarjonnan ja kysynnän välinen merkintä on valinnainen ja lähes pysyvä. Käyttäjä voi poistaa merkinnän manuaalisesti tai se voidaan poistaa suorittamalla myyntitilauksen rivin hajotus, jossa **Poista merkintä** -vaihtoehto on valittu.

Tarvekohdistusta ohjataan pääsuunnittelulla kattavuuden aikana, ja sen avulla linkitetään kysyntä tarvittavaan tarjontaan. Tarvekohdistus voidaan päivittää kullekin suunnitteluajolle, jolla optimoidaan kysynnän kattamiseen tarvittava tarjonta. Kun pääsuunnittelu päivittää tarvekohdistustiedot, se noudattaa mahdollista aiemmin luotua merkintää.

Tarvekohdistus alkaa sisällyttämällä liittyvä merkintä, käytettävissä olevan varaston varaukset ja tilauksessa olevan varaston varaukset seuraavassa järjestyksessä:

1. Kysynnän ja tarjonnan välinen merkintä
1. Käytettävissä olevan varaston varaukset
1. Tilauksessa olevan varaston varaukset

Kun vahvistat suunnitellun tilauksen, **Vahvistus**-valintaikkunan **Päivitä merkintä** -kentässä voi määrittää vahvistuksen aikana luotujen tilausten merkintävaihtoehdot. Valitse jokin seuraavista:

- **Ei** – varastomerkintää ei käytetä.
- **Vakio** – varastomerkintä päivitetään tarvekohdistuksen mukaan. Tarvetilaus (kysyntä) merkitään täyttötilauksen (tarjonta) mukaan. Jos täyttötilaukseen jää jäljelle jokin määrä, sitä ei merkitä ja viitetiedot jätetään tyhjäksi. Jos esimerkiksi 100 kappaleen myyntitilaus tarvekohdistetaan 150 kappaleen ostotilaukseen, viitetiedot määritetään vain myyntitilaukseen.
- **Laajennettu** – sekä tarvetilaus (kysyntä) että täyttötilaus (tarjonta) merkitään riippumatta siitä, jääkö täyttötilaukseen jäljelle jokin määrä. Jos esimerkiksi 100 kappaleen myyntitilaus tarvekohdistetaan 150 kappaleen ostotilaukseen, viitetiedot määritetään sekä myyntitilaukseen tai ostotilaukseen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]