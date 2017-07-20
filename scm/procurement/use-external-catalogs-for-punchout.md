---
title: "Siirtyminen sähköiseen hankintaan ulkoisten luetteloiden avulla"
description: "Tässä ohjeaiheessa kerrotaan, miten ulkoisen luettelon avulla voit luoda ja lähettää ostoehdotuksia."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 01955aefb27bd18809b35fd025c9dd1b8eb70520
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a>Siirtyminen sähköiseen hankintaan ulkoisten luetteloiden avulla
Käyttämällä ulkoisia luetteloita sähköiseen hankintaan siirryttäessä ei tarvitse ylläpitää toimittajien tuotetietoja omissa päätiedoissa. Sen sijaan toimittajan sivuston ostoskori muunnetaan varasto-ottoehdotusriveiksi, joissa on oikeat tuotetiedot. 

Vältä toimittajien tuotekuvausten ja -hintojen säilyttämistä omissa tuotteen päätiedoissa. Käytä sen sijaan ulkoisia luetteloita siirryttäessä sähköiseen hankintaan Kun työntekijät tämän jälkeen luovat ostoehdotuksia, he voivat siirtyä toimittajan ulkoiseen tuoteluettelosivustoon (toisin sanoen he voivat poistua sinun järjestelmästäsi ja siirtyä toimittajan sivustoon). Tuotteet, jotka on lisätty ostoskoriin toimittajan sivustossa, voidaan muuntaa sitten varasto-ottoehdotusriveiksi. Näin saat oikean tuotetiedot: tuotteen tunnuksen, nimen ja hinnan jne.

Käyttääkseen ulkoisia luetteloita työntekijän on luotava varasto-ottoehdotus **Omat ostoehdotukset** -sivulla.

Työntekijästä, joka luo ehdotuksen, käytetään nimitystä ehdotuksen valmistelija. Valmistelijana voit myös toteuttaa seuraavia tehtäviä.

Käytä **Ulkoiset luettelot** -rivin toimenpidettä sivun avaamiseen, joka sisältää kaikki ulkoiset luettelot, jotka ovat määritetyn ehdottajan, ostavan yrityksen ja vastaanottava toimintayksikön käytettävissä.

Käyttöoikeuksiesi mukaan muuttaa ehdottajaa, ostavaa yritystä ja vastaanottavalle toimintayksikölle. Arvojen muutos voi muuttaa ulkoisia luetteloita, jotka ovat käytettävissä ehdottajalle. Ulkoiset luettelot, jotka ovat käytettävissä, määräytyvät nykyisen aktiivisten ostomenettelyiden perusteella ostavalle yritykselle tai vastaanottavalle toimintayksikölle. Nämä käytännöt voivat sallia tai estää tiettyjen hankintaluokkien käyttöoikeudet. Tämä voi vaikuttaa ulkoisiin luetteloihin, jotka on yhdistetty näihin hankintaluokkiin.

Lisätietoja käytännöistä on kohdassa [Ostokäytännöt](../procurement/purchase-policies.md).

- Voit etsiä tiettyä hankintaluokkaa vastaavia ulkoisia luetteloita kirjoittamalla tekstiä luettelon hakukenttään.
- Lisää tuotteita toimittajan tuoteluettelosta toimittajan sivustossa valitse ulkoinen luettelo. Lisää tuotteita ostoskärryyn ja siirry eteenpäin. Ostoskorin rivit siirretään Microsoft Dynamics 365:een.

Jos hankintaluokille on useita eri vaihtoehtoja, valitse oikea hankintaluokka ennen kuin lisäät rivejä varasto-ottoehdotuksiin.
Kun rivit on lisätty varasto-ottoehdotukseen, voit lisätä lisää rivejä käyttämättä ulkoisia luetteloita. Vaihtoehtoisesti voit edelleen lisätä rivejä ulkoisten luetteloiden avulla.

Kun varasto-ottoehdotus on valmis, käytä **Työnkulku** > **Lähetä** -toimintoa ja lähetä se hyväksyttäväksi.
