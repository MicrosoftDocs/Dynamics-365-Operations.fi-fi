---
title: Pakkausmateriaalit ja maksut
description: Pakkausmateriaalimaksuja maksetaan kierrätysyritykselle säännöllisin väliajoin. Maksuna peritään tietty summa kunkin pakkausyksikköön kuuluvan materiaalin painoyksikköä kohden. Pakkausmateriaalimaksut lasketaan ja raportoidaan, mutta niistä ei kirjata kirjanpitotapahtumia, koska niitä ei käsitellä viranomaiselle maksettavana verona.
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c188651fe8ba3fe3f9678f36ab11ae886ef6f1cf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "312298"
---
# <a name="packing-materials-and-fees"></a>Pakkausmateriaalit ja maksut

[!include [banner](../includes/banner.md)]

Pakkausmateriaalimaksuja maksetaan kierrätysyritykselle säännöllisin väliajoin. Maksuna peritään tietty summa kunkin pakkausyksikköön kuuluvan materiaalin painoyksikköä kohden. Pakkausmateriaalimaksut lasketaan ja raportoidaan, mutta niistä ei kirjata kirjanpitotapahtumia, koska niitä ei käsitellä viranomaiselle maksettavana verona.

Pakkausmateriaalin painot ja maksut lasketaan sekä osto- että myyntitilausriveille.

Nimikkeelle, nimikkeiden pakkausryhmälle tai kaikille nimikkeille määritetään vähintään yksi pakkausyksikkö. Pakkausyksikköön kuuluvat pakkausmateriaalit, niiden paino ja pakkausyksikköön pakattavien nimikkeiden määrä. Pakkausmateriaalikoodi määritetään kullekin määritetylle pakkausmateriaalityypille. Voit määrittää pakkausmateriaalikoodin perusteella hinnan tietyksi ajaksi. Pakkausmateriaalimaksu lasketaan näiden tietojen perusteella.

| **Huomautus**                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vaikka yritys ei maksaisi pakkausmateriaalimaksuja, toimintoa voi käyttää pakkausmateriaalien painoon perustuvien tilastojen laskemiseen. |

## <a name="setup-requirements-for-packing-material-fees"></a>Pakkausmateriaalimaksuvaatimusten määrittäminen
Seuraavat perustiedot on luotava ennen pakkausmateriaalin painojen tai pakkausmateriaalimaksujen tai molempien laskemista:

-   Pakkausryhmät – luo nimikkeisiin määritettävä pakkausryhmät.
-   Pakkausmateriaalikoodit – luo pakkausmateriaalikoodit jokaiselle määritetylle pakkausmateriaalityypille.
-   Pakkausyksiköt – Määritä nimikkeen, pakkausryhmän tai kaikkien nimikkeiden pakkausyksikkö. Määritä kullekin pakkausyksikölle sisällytettävät pakkausmateriaalit, määritä painot ja anna Pakkausyksikkökerroin-kentässä muuntokerroin varastoyksiköstä.
-   Pakkausmateriaalimaksu – Määritä kunkin pakkausmateriaalikoodin pakkausmateriaalimaksu. Määritä jokaiselle materiaalityypille voimassaoloaika, materiaalikohtainen hinta, valuutta ja yksikkö.

## <a name="packing-units-on-sales-order-lines"></a>Myyntitilausrivien pakkausyksiköt
Kun myyntitilausrivi luodaan, järjestelmä tarkistaa, onko nimikkeelle määritetty pakkausyksikköjä. Jos pakkausyksiköitä on määritetty, järjestelmä päivittää määritetyn pakkausyksikön ja pakkausyksikön määrän myyntitilausriville. Pakkausyksikön määrä perustuu tilattuun määrään, joka on jaettu valitun pakkausyksikön nimikkeiden määrällä. Jos pakkausyksikköä ei ole määritetty, pakkausyksikön ja pakkausyksikön määrän voi lisätä myyntitilausriville manuaalisesti. Pakkausyksikköä ja pakkausyksikön määrää voi muuttaa myös myyntitilausrivin kirjauksen yhteydessä. Tämä voi olla tarpeen, jos myyntitilausrivi toimitetaan tai laskutetaan vain osittain. Pakkausmateriaalitapahtumat luodaan, kun myyntitilaus laskutetaan. Pakkausmateriaalitapahtumat sisältävät myyntirivin pakkausmateriaalien painon. Tapahtumia voi myös muokata laskutuksen jälkeen, jonka jälkeen voi luoda uusia tapahtumia.

## <a name="packing-units-on-purchase-order-lines"></a>Ostotilausrivien pakkausyksiköt
Järjestelmä ei luo ostotilausrivin pakkausmateriaalitapahtumia. Voit luoda laskutettuja ostontilausrivien tapahtumia manuaalisesti **Pakkausmateriaalitapahtumat**-sivulla.

## <a name="set-up-customer-packaging-material-fee-license-numbers"></a>Asiakkaan pakkausmateriaalimaksun lupanumeroiden määrittäminen
Jos asiakkaat maksavat pakkausmateriaalimaksuja, määritä asiakkaan pakkausmateriaalimaksun lupanumerot **Asiakkaat**-sivulla. Kun asiakkaan lupanumero on määritetty, pakkausmateriaalimaksujen laskeminen tapahtuu automaattisesti myyntitilausten laskutuksen yhteydessä. Laskutuksen jälkeen **Pakkausmateriaalitapahtumat**-sivun **Laske maksu** -valintaruudun valinta poistetaan, koska raporttia ei tarvitse laskea eikä tulostaa. Voit tulostaa pakkausmateriaalin painon laskuun ja ilmoittaa asiakkaille, että he maksavat maksut. 

Jos työnantajasi maksaa pakkausmateriaalimaksut, älä määritä asiakkaiden lupanumeroita. Laskutuksen jälkeen **Laske maksu** -valintaruutu valitaan **Pakkausmateriaalitapahtumat**-sivulla. Tämä ilmaisee, että maksut lasketaan, kun raportti luodaan. Voit tulostaa painot laskuun ja ilmoittaa, että yrityksesi maksaa palkkiot.

## <a name="print-packaging-material-weights-on-invoices"></a>Pakkausmateriaalien painon tulostaminen laskuihin
Voit tulostaa pakkausmateriaalien painon laskuun ja ilmaista, kuka maksaa pakkausmateriaalimaksun. Painojen yhteenlaskeminen tapahtuu pakkauskoodeittain.





