---
title: Toimittajan varmenteen ylläpitäminen
description: Tässä artikkelissa kuvataan vaiheita, joita toimittajat voivat käyttää toimittajien varmenteiden ylläpitoon toimittajien yhteistyötilan avulla.
author: TaylorVH
ms.date: 04/27/2021
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: TaylorVH
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c66952d19cddd9d4a9a102ba59e8d6d97b75ed4d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/22/2022
ms.locfileid: "9583201"
---
# <a name="maintain-vendor-certification"></a>Toimittajan varmenteen ylläpitäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan vaiheita, joita toimittajat voivat käyttää toimittajien varmenteiden ylläpitoon **toimittajien yhteistyötilan** avulla. Esimerkkejä varmenteista voivat olla esimerkiksi Woman Business Enterprise (WBE)- tai Leadership in Energy and Environment Design (LEED) -yritys. Toimittajien täytyy lisätä varmenteen tiedot **Toimittajatiedot**-työtilaan. Siellä toimittajat valitsevat **Lisätietoja** ja sitten **Varmenteet**.

## <a name="turn-on-the-vendor-certification-feature"></a>Toimittajan varmenneominaisuuden ottaminen käyttöön

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sivua ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli** - *Ostoreskontra*
- **Ominaisuuden nimi** - *Ota toimittajan yhteistyövarmenteen hallinta käyttöön*

## <a name="add-a-new-certification"></a>Uuden varmenteen lisääminen

Voit lisätä uuden varmenteen valitsemalla **Lisää**-painikkeen, joka sijaitsee **Varmenne**-ruudun yläpuolella **Toimittajatiedot**-työtilassa. Kirjoita seuraavat tiedot:

- Varmenteen numero
- Varmenteen tyyppi
- Varmenteen myöntäjäorganisaatio
- Todistuksen päivämäärä
- Velkasumma, jos käytettävissä
- Voimassaolon alkamispäivämäärä
- Vanhentumispäivä
- Kommentit, valinnainen

Jos tiettyyn varmenteeseen liittyy asiakirjoja, voit liittää ne valitsemalla **Asiakirja**-painikkeen.

Toimittajiesi tälle sivulle syöttämille varmennuksille määritetään "Toimittaja"-lähde. Voit syöttää varmenteen tiedot toimittajan puolesta toimittajien pankkitilien kohdassa. Tiedot näkyvät tässä, ja lähde näkyy **asiakkaana**.

Toimittajat voivat tarvittaessa muokata tai poistaa varmennuksiaan.

## <a name="vendor-collaboration-generated-certification-records"></a>Toimittajayhteistyöllä luodut varmennetietueet

Kun toimittaja on lisännyt varmennetiedot, tiedot näkyvät **Toimittajayhteistyöllä luodut varmenteet** -sivulla. Voit avata sivun valitsemalla **Ostoreskontra > Kyselyt > Toimittajaraportit > Toimittajayhteistyöllä luodut varmenteet**. Oletusarvon mukaan kaikki uudet tai muokatut varmennetietueet ovat näkyvissä. Ostoreskontran kirjanpitäjä voi tarkastella muutoksia ja vahvistaa tiedot vahvistusprosessinsa kautta. Kun tiedot on vahvistettu, sivulla lueteltu varmennetietue voidaan valita ja merkitä tarkistetuksi. Tietueen merkitseminen tarkistetuksi poistaa tietueen oletusluettelosta.

Kaikki varmennemuutokset näkyvät **Toimittajayhteistyöllä luodut varmenteet** -sivulla. Jos muutosta ei näytetä sivulla, voit tarkastella sitä muokkaamalla toimittajatilin suodattimia, voimaantulopäiväväliä tai valitsemalla, sisällytetäänkö tietoihin tarkistetut varmennemuutokset.

