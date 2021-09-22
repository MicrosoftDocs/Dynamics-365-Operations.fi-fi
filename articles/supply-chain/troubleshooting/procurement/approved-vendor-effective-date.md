---
title: Hyväksytyn toimittajan voimaantulopäivää ei voi muuttaa
description: Tuoteyksikkökohtainen hyväksyttyjen toimittajien luettelo ei salli voimaantulopäivän muuttamista
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: cb6dbd134d63daa163261cabdbd7eceb978877ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476184"
---
# <a name="cant-change-the-effective-date-for-an-approved-vendor"></a>Hyväksytyn toimittajan voimaantulopäivää ei voi muuttaa


## <a name="symptoms"></a>Oireet

Tuotteella on hyväksytty toimittaja, jonka voimaantulopäivä on esimerkiksi 11. tammikuuta 2018 (*01/11/2018*) ja vanhentumispäivä on *Ei koskaan*. Jos yrität muuttaa voimaantulopäivän muotoon 10. tammikuuta 2018 (*01/10/2018*) tai 12. tammikuuta 2018 (*01/12/2018*), näyttöön tulee seuraava virhesanoma:

> Tietuetta ei voi luoda hyväksyttyjen toimittajien luetteloon (PdsApproveVendorList). Vanhentumispäivän arvon on oltava sama tai suurempi kuin voimaantulopäivän arvo.

## <a name="resolution"></a>Ratkaisu

Voit pidentää vain sitä jaksoa, jolle toimittaja on hyväksytty. Seuraavat säännöt pätevät:

- Jos haluat muuttaa voimaantulopäivää siten, että se nimikkeen toimittajan olemassa olevia tietueita (jaksoja) aiemmin, uuden jakson vanhanemispäivän on oltava ennen kaikkia olemassa olevien tietueiden vanhenemispäivää.
- Jos haluat muuttaa vanhenemispäivää siten, että se on myöhempi kuin jokin olemassa oleva jakso, voimaantulopäivämäärän ei saa olla ennen olemassa olevan tietueen vanhenemispäivää.
- Jos haluat pienentää kokonaisaikaa, jolle toimittaja on hyväksytty, sinun on poistettava tai muokattava olemassa olevia tietueia. Vaihtoehtoisesti voit käyttää **katkaisu**-valitsinta tuonnin aikana. Tämä valitsin poistaa kaikki olemassa olevat tietueet nimikekohteisten hyväksyttyjen toimittajien taulukosta.

Esimerkiksi ongelmankuvauksessa kuvattu skenaario, jossa tietueen voimaantulopäivä on *01/11/2018* ja vanhenemispäivä *Ei koskaan*, y voit tuoda uuden tiedoston, jonka voimaantulopäivänä on *01/10/2018* vanhenemispäivänä *Ei koskaan*. Et kuitenkaan voi lyhentää ajanjaksoa niin, että voimaantulopäiväksi päivittyy tiedonhallinnan kautta *01/12/2018*. Tämä muutos on tehtävä käyttöliittymässä.
