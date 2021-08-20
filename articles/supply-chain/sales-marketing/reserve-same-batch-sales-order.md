---
title: Saman erän varaaminen myyntitilausta varten
description: Tässä artikkelissa kerrotaan, miten tuote määritetään, kun varastovaraus sallitaan yhden varastoerän mukaan.
author: omulvad
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9bb3eb067e7e9f8a9108da05602fc6771e7dd12c47be44f989ded53ff7c9d250
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754509"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a>Saman erän varaaminen myyntitilausta varten

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten tuote määritetään, kun varastovaraus sallitaan yhden varastoerän mukaan.

Saman erän varaamisen avulla voit varata myyntitilausriville varaston yhden varastoerän mukaan. Tapettia tilaava asiakas voi esimerkiksi pyytää koko tilauksen samasta erästä saadakseen keskenään samanlaisia tapettirullia. Voit määrittää tuotteen käyttämään saman erän varausta ottamalla käyttöön seuraavat asetukset tuotteeseen liitetyssä nimikemalli-, seurantadimensio- ja varastodimensioryhmässä:

- **Nimikemalliryhmät** – Nimikemalliryhmässä on valittava varastokäytäntöjen **Varaus**-kenttäryhmän **Saman erän valinta**- ja **Konsolidoi tarve** -kenttä.
- **Seurantadimensioryhmät** – Seurantadimensioryhmässä on valittava eränumeron **Kattavuussuunnitelma dimension mukaan** -kenttä.
- **Varastodimensioryhmät** – Varastodimensioryhmässä on valittava **Toimipaikka**- ja **Varasto**-kohdassa **Kattavuussuunnitelma dimension mukaan** -kenttä.

Kun varaat myyntitilausrivin tuotteelle varaston, jolla on määritetty saman erän valinta, järjestelmä yrittää varata tilatun määrän yhdestä varastoerästä. Myös muut erämääritteen vaatimukset otetaan huomioon. Jos määrää ei voida täyttää yhdestä erästä, **Saman erävarauksen ristiriita** -sivu aukeaa. Sivulla kerrotaan ongelmista ja toimenpiteistä, joiden avulla varauksen tekemistä voi jatkaa. Seuraavat tilanteet saattavat estää erän varaamisen:

- Myynnin erän käsittelykoodin **Estä varaaminen** -kohdan arvoksi on merkitty **Estetty**.
- Erä on vanhentunut vanhentumispäivän ja mahdollisten käytettävissä olevien asiakkaan myyntipäivien perusteella. Nimikkeen varausta voidaan silti harkita, jos kyseessä on päivämäärän mukaan ohjatun FEFO-nimikkeen nimikemalliryhmä ja parasta ennen -päivä on valittu keräysehdoksi.
- Erällä ei ole jäljellä riittävästi varastointiaikaa vanhentumispäivän ja parasta ennen -päivän sekä mahdollisten asiakkaan myyntipäivien perusteella.

Jos nimike liittyy varastodimensioryhmään, jossa on otettu käyttöön **Käytä varastonhallintaprosesseja**, voit varata tiettyjä eränumeroita käyttämällä varaushierarkiaa, jossa on sijaintidimension yläpuolella määritetty eränumeron varastodimensio. Tämäntyyppistä varaushierarkiaa kutsutaan myös *erä-yllä\[sijainti\]* -varaushierarkiaksi Myynti- ja siirtotilausrivien **Erän varaus** -sivulla voit myös valita ja varata useita rivejä käytettävissä olevien eränumeroiden perusteella. Katso lisätietoja siitä, mitä tehdä, jos käytät varaushierarkiaa, jolla on varastopaikan alapuolella eränumerodimensio (*erä-alla\[sijainti\]*) kohdasta [Joustava varastotason dimension varauskäytäntö](../warehousing/flexible-warehouse-level-dimension-reservation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
