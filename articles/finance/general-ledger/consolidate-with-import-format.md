---
title: Tuontimuoto konsolidointia varten
description: Tässä artikkelissa on yksityiskohtaisia tietoja tuontimuodosta, jota käytetään konsolidoitaessa useiden yritysten taloustietoja.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 0aee830f8fbfa384c86dc16465b202be36f07b73
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871301"
---
# <a name="import-format-for-consolidation"></a>Tuontimuoto konsolidointia varten

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yksityiskohtaisia tietoja tuontimuodosta, jota käytetään konsolidoitaessa useiden yritysten taloustietoja. Tuontimuoto on tallennettava tekstitiedostona (.txt).

## <a name="import-format"></a>Tuontimuoto

Seuraavassa taulukossa luetellaan tuontimuoto, jota on käytettävä, kun teet konsolidoinnin tuonnin aikana.

| Tietuetaulu | Muoto | Muistiinpanot |
|--------------|---------|-------|
| 1            | 170150, Goodwill, 4 | <ul><li>Tietuetaulu</li><li>Lähteen päätilin tunnus</li><li>Päätilin rivi</li><li>Päätilin tyyppi</li></ul> |
| 2            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Päätilin tunnus</li><li>Tapahtuman päivä</li><li>Kirjanpitokauden tyyppi (**0** = Avaaminen, **1** = Käytössä ja **2** = Sulkeminen)</li><li>Tapahtuman valuutta</li><li>Debet tai kredit (**0** = Debet ja **1** = Kredit)</li><li>Kirjanpitotaso</li><li>Tapahtumasummat</li><li>Määrä</li><li>Paikallinen RecID (moniselitteinen, yksilöivä int64-arvo tapahtumalle)</li></ul> |
| 3            | USMF0000009, 2017/01/01, FY2017, 1, 2017,01,01, 602200, USD, 6053.6.0 | <ul><li>Merkintänumero (budjettiotsikon tapahtumanumero)</li><li>Budjettiotsikon oletuspäivämäärä</li><li>Budjettimallin tunnus</li><li>Budjettityyppi (**1** - Alkuperäinen budjetti, **2** - SIirto, **3** - Tarkistusversio, **4** - Varaus, **5** - Ennakkovaraus, **6** - Siirrettävä budjetti, **7** - Projekti, **8** - käyttöomaisuus, **9** - kysyntäennuste, **10** - tarjontaennuste, **11** - Jaot, **12** -Alustava budjetti.)</li><li>Rivin päivämäärä</li><li>Rivin päätilin tunnus</li><li>Rivin valuuttakoodi</li><li>Rivin summa tapahtuman valuuttana</li><li>Rivin budjettityypin (kulu tai tuotto) valintalistan kokonaislukuarvo.</li></ul> |
| 4            | DEMF | RecordCompany on lähdeyritys. |
| 5            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Päätilin tunnus</li><li>Tapahtuman päivämäärä</li><li>Kirjanpitokauden tyyppi (0 Avaaminen, 1 Käytössä ja 2 Sulkeminen)</li><li>Tapahtumavaluutta</li><li>Debet tai kredit (0 on Debet ja 1 on Kredit)</li><li>Kirjanpitotaso</li><li>Tapahtuman summa</li><li>Määrä</li><li>Paikallinen RecID (moniselitteinen, yksilöivä int64-arvo tapahtumalle)</li></ul>  |
| 6            | BusinessUnit, 1 Osasto, 2 | Taloushallinnon dimension määritteet määritetään segmenttijärjestyksessä.<p>**Vienti**-sivulla voit tarkistaa, miten määritteet on määritetty.</p> |
| 7            | 002,1,658 | <ul><li>Taloushallinnon dimension arvo</li><li>Taloushallinnon dimensio RecordDimensions-dimensioiden indeksinä.</li><li>Moniselitteinen, yksilöivä tietuetunnus, joka liittyy RecordTrans- tai RecordTrans2-kohteen yksilöivään tietuetunnukseen</li></ul> |
| 8            | 002,1,1 | <ul><li>RecordBudget-kohteesta tapahtumaan liittyvät dimensioarvot</li><li>Taloushallinnon dimensio RecordDimensions-dimensioiden indeksinä.</li><li>Moniselitteinen rivitietueen tunnus, joka on kohdistettu tiedoston tapahtumarivien järjestyksen mukaan.</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
