---
title: Varaston merkintä
description: Tässä artikkelissa on tietoja vahvistettujen tilausten varaston merkintävaihtoehdoista.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c86db6a670d7d0f7bfe74b7466b9bce766e4a08d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740573"
---
# <a name="inventory-marking"></a>Varaston merkintä

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa on tietoja vahvistettujen tilausten varaston merkintävaihtoehdoista.

*Merkintää* käytetään linkittämään kysyntä ja tarjonta. Se muistuttaa *tarvekohdistusta*, joka ilmaisee, miten pääsuunnittelun odotetaan kattavan kysynnän. Suunnittelun kannalta suurin ero on siinä, että merkintä on pysyvämpää kuin tarvekohdistus.

Merkintä otettiin käyttöön tukemaan kustannuslaskennan FIFO- ja LIFO-erityisskenaarioita. Sitä käytetään nyt kuitenkin myös joissakin muissa kuin kustannuslaskentaskenaarioissa. Tarjonnan ja kysynnän välinen merkintä on valinnainen ja lähes pysyvä. Käyttäjä voi poistaa merkinnän manuaalisesti tai se voidaan poistaa suorittamalla myyntitilauksen rivin hajotus, jossa **Poista merkintä** -vaihtoehto on valittu.

Tarvekohdistusta ohjataan pääsuunnittelulla kattavuuden aikana, ja sen avulla linkitetään kysyntä tarvittavaan tarjontaan. Tarvekohdistus voidaan päivittää kullekin suunnitteluajolle, jolla optimoidaan kysynnän kattamiseen tarvittava tarjonta. Kun pääsuunnittelu päivittää tarvekohdistustiedot, se noudattaa mahdollista aiemmin luotua merkintää.

Tarvekohdistus alkaa sisällyttämällä liittyvä merkintä, käytettävissä olevan varaston varaukset ja tilauksessa olevan varaston varaukset seuraavassa järjestyksessä:

1. Kysynnän ja tarjonnan välinen merkintä
1. Käytettävissä olevan varaston varaukset
1. Tilauksessa olevan varaston varaukset

Kun vahvistat suunnitellun tilauksen, **Vahvistus**-valintaikkunan **Päivitä merkintä** -kentässä voi määrittää vahvistuksen aikana luotujen tilausten merkintävaihtoehdot. Valitse jokin seuraavista:

- *Ei* – varastomerkintää ei käytetä.
- *Vakio* – varastomerkintä päivitetään tarvekohdistuksen mukaan. Tarvetilaus (kysyntä) merkitään täyttötilauksen (tarjonta) mukaan. Jos täyttötilaukseen jää jäljelle jokin määrä, sitä ei merkitä ja viitetiedot jätetään tyhjäksi. Jos esimerkiksi 100 kappaleen myyntitilaus tarvekohdistetaan 150 kappaleen ostotilaukseen, viitetiedot määritetään vain myyntitilaukseen.
- *Laajennettu* – sekä tarvetilaus (kysyntä) että täyttötilaus (tarjonta) merkitään riippumatta siitä, jääkö täyttötilaukseen jäljelle jokin määrä. Jos esimerkiksi 100 kappaleen myyntitilaus tarvekohdistetaan 150 kappaleen ostotilaukseen, viitetiedot määritetään sekä myyntitilaukseen tai ostotilaukseen.
- *Yksitasoinen vakio* – Käytetään yksitasoista merkintää. Yksitasoinen merkintä merkitsee vain päänimikkeen, ei sen tuoterakennekomponentteja (BOM). Näin ollen voit pitää tuotantotilausten komponenttien määrityksen joustavana vahvistuksen jälkeen. Yksitasoinen merkintä sallii järjestelmän optimoida viime hetken muutokset kysynnässä. Kun yksitasoisen merkinnän tyyppi on *vakio*, tarvetilaukset merkitään niiden täyttämistilausten mukaan, mutta täyttämistilauksia ei merkitä, jos niillä on jäljellä oleva määrä.
- *Yksitasoinen laajennettu* – Käytetään yksitasoista merkintää. Kun yksitasoisen merkinnän tyyppi on *laajennettu*, tarvetilaukset merkitään niiden täyttämistilausten mukaan ja täyttämistilaukset merkitään aina riippumatta jäljellä olevasta määrästä.

Jos haluat määrittää järjestelmäsi oletusarvoisen merkintävaihtoehdon, siirry kohtaan **Pääsuunnittelu \> Asetukset \> Pääsuunnittelun parametrit**. Valitse sitten haluamasi vaihtoehto **Vakiopäivitys**-välilehden **Päivitä merkintä** -kentästä.

> [!NOTE]
> *Yksitasoinen vakio*- ja *Yksitasoinen laajennettu* -vaihtoehdot ovat käytettävissä vain, jos *Tilauksesta valmistukseen -tarjonnan automatisointi* -ominaisuus on käytössä järjestelmässäsi. Lisätietoja tästä ominaisuudesta ja sen ottamisesta käyttöön on kohdassa [Tilauksesta valmistukseen -tarjonnan automatisointi](../make-to-order-supply-automation.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
