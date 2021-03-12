---
title: Valmiiksi ilmoittaminen rekisterikilpiohjaamattomaan sijaintiin (Sovellus, Toukokuu 2016)
description: Tässä tehtäväoppaassa näytetään esimerkki valmiiksi ilmoittamisesta sijaintiin, jota ei ohjata rekisterikilvellä.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 180035668d9c8a03b83f669af7459725eecc8def
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981178"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>Valmiiksi ilmoittaminen rekisterikilpiohjaamattomaan sijaintiin (Sovellus, Toukokuu 2016)

[!include [banner](../../includes/banner.md)]

Tässä tehtäväoppaassa näytetään esimerkki valmiiksi ilmoittamisesta sijaintiin, jota ei ohjata rekisterikilvellä. Tehtävä edellyttää käytettävää työkäytäntöä. Työkäytännön määrittäminen on esitelty edellisessä tehtäväoppaassa. Tämä tehtäväopas vaatii Dynamics AX -sovelluksen version 7.0.1 tai sitä uudemman.




## <a name="set-up-an-output-location"></a>Määritä tulostussijainti
1. Valitse Organisaation hallinto > Resurssit > Resurssiryhmät.
2. Valitse luettelosta resurssiryhmä 5102.
3. Valitse Muokkaa.
4. Kirjoita Tulostusvarasto-kenttään arvo 51.
5. Kirjoita Tulostussijainti-kenttään arvo 001.
    * Sijainti 001 ei ole rekisterikilven mukaan ohjattu sijainti. Voit määrittää rekisterikilven mukaan ohjaamattoman sijainnin ainoastaan, jos sijainnille on olemassa soveltuva työkäytäntö.  

## <a name="create-a-production-order-and-report-it-as-finished"></a>Luo tuotantotilaus ja ilmoita se valmiiksi
1. Sulje sivu.
2. Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.
3. Valitse Uusi tuotantotilaus.
4. Kirjoita Nimiketunnus-kenttään arvo L0101.
5. Valitse Luo.
6. Valitse toimintoruudussa Tuotantotilaus.
7. Valitse Arvio.
8. Valitse OK.
9. Valitse Käynnistys.
10. Valitse Yleiset-välilehti.
11. Valitse Automaattinen tuoterakennekulutus -kentässä Ei koskaan.
12. Valitse OK.
13. Valitse Ilmoita valmiiksi.
14. Valitse Yleiset-välilehti.
15. Valitse Hyväksy virhe -kentässä Kyllä.
16. Valitse OK.
17. Valitse toimintoruudussa Varasto.
18. Valitse Työn tiedot.
    * Kun tuotantotilaus on raportoitu päättyneeksi, poispanotöitä ei luotu. Tämä johtuu siitä, että määritettynä on työn käytäntö, joka estää töiden luonnin, kun tuote L0101 ilmoitetaan valmiiksi sijaintiin 001.  

