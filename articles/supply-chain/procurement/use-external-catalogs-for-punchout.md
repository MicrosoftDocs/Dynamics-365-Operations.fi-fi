---
title: Siirtyminen sähköiseen hankintaan ulkoisten luetteloiden avulla
description: Tässä ohjeaiheessa kerrotaan, miten ulkoisen luettelon avulla voit luoda ja lähettää ostoehdotuksia.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests, CatExternalCatalogBasketWizard, CatExternalCatalogPunchoutDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e360204bdb71dca35337e1b95bdf1837a16a25caa00e979f70876dd5ffd9139
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774051"
---
# <a name="use-external-catalogs-for-punchout-e-procurement"></a>Siirtyminen sähköiseen hankintaan ulkoisten luetteloiden avulla

[!include [banner](../includes/banner.md)]

Käyttämällä ulkoisia luetteloita sähköiseen hankintaan siirryttäessä ei tarvitse ylläpitää toimittajien tuotetietoja omissa päätiedoissa. Sen sijaan toimittajan sivuston ostoskori muunnetaan varasto-ottoehdotusriveiksi, joissa on oikeat tuotetiedot. 

Vältä toimittajien tuotekuvausten ja -hintojen säilyttämistä omissa tuotteen päätiedoissa. Käytä sen sijaan ulkoisia luetteloita siirryttäessä sähköiseen hankintaan Kun työntekijät tämän jälkeen luovat ostoehdotuksia, he voivat siirtyä toimittajan ulkoiseen tuoteluettelosivustoon (toisin sanoen he voivat poistua sinun järjestelmästäsi ja siirtyä toimittajan sivustoon). Tuotteet, jotka on lisätty ostoskoriin toimittajan sivustossa, voidaan muuntaa sitten varasto-ottoehdotusriveiksi. Näin saat oikean tuotetiedot: tuotteen tunnuksen, nimen ja hinnan jne.

Käyttääkseen ulkoisia luetteloita työntekijän on luotava varasto-ottoehdotus **Omat ostoehdotukset** -sivulla.

Työntekijästä, joka luo ehdotuksen, käytetään nimitystä ehdotuksen valmistelija. Valmistelijana voit myös toteuttaa seuraavia tehtäviä.

Käytä **Ulkoiset luettelot** -rivin toimenpidettä sivun avaamiseen, joka sisältää kaikki ulkoiset luettelot, jotka ovat määritetyn ehdottajan, ostavan yrityksen ja vastaanottava toimintayksikön käytettävissä.

Käyttöoikeuksiesi mukaan muuttaa ehdottajaa, ostavaa yritystä ja vastaanottavalle toimintayksikölle. Arvojen muutos voi muuttaa ulkoisia luetteloita, jotka ovat käytettävissä ehdottajalle. Ulkoiset luettelot, jotka ovat käytettävissä, määräytyvät nykyisen aktiivisten ostomenettelyiden perusteella ostavalle yritykselle tai vastaanottavalle toimintayksikölle. Nämä käytännöt voivat sallia tai estää tiettyjen hankintaluokkien käyttöoikeudet. Tämä voi vaikuttaa ulkoisiin luetteloihin, jotka on yhdistetty näihin hankintaluokkiin.

Lisätietoja käytännöistä on kohdassa [Ostokäytäntöjen yleiskatsaus](../procurement/purchase-policies.md).

- Voit etsiä tiettyä hankintaluokkaa vastaavia ulkoisia luetteloita kirjoittamalla tekstiä luettelon hakukenttään.
- Lisää tuotteita toimittajan tuoteluettelosta toimittajan sivustossa valitse ulkoinen luettelo. Lisää tuotteita ostoskärryyn ja siirry eteenpäin. Ostoskorin rivit siirretään Microsoft Dynamics 365:een.

Jos hankintaluokille on useita eri vaihtoehtoja, valitse oikea hankintaluokka ennen kuin lisäät rivejä varasto-ottoehdotuksiin.
Kun rivit on lisätty varasto-ottoehdotukseen, voit lisätä lisää rivejä käyttämättä ulkoisia luetteloita. Vaihtoehtoisesti voit edelleen lisätä rivejä ulkoisten luetteloiden avulla.

Kun varasto-ottoehdotus on valmis, käytä **Työnkulku** > **Lähetä** -toimintoa ja lähetä se hyväksyttäväksi.

### <a name="additional-resources"></a>Lisäresurssit

- [Sähköiseen hankintaan siirtymisessä käytettyjen ulkoisten luetteloiden määrittäminen](set-up-external-catalog-for-punchout.md)
- [Ostojen cXML-parannukset](purchasing-cxml-enhancements.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]