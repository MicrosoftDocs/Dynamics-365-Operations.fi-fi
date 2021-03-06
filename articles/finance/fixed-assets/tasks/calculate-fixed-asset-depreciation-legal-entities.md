---
title: Käyttöomaisuuden poistojen laskenta eri yrityksissä
description: Käyttöomaisuuden poisto voidaan suorittaa useille yritykselle yhdellä kertaa.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85a1e71967fb126be29a76a8a29ea5e4ae2b2199
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818461"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Käyttöomaisuuden poistojen laskenta eri yrityksissä

[!include [banner](../../includes/banner.md)]

Käyttöomaisuuden poisto voidaan suorittaa useille yritykselle yhdellä kertaa. Näissä ohjeissa kerrotaan, miten prosessi määritetään ja suoritetaan useille yrityksille. Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.


## <a name="set-up-cross-company-depreciation-run-journals"></a>Yritysten välisten poistoajon kirjauskansioiden määrittäminen
1. Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuuden parametrit.
2. Laajenna Käyttöomaisuuden ehdotukset -osa.
3. ValitseLisää.
4. Syötä tai valitse arvo Kirjanpitotaso-kenttään.
5. Syötä tai valitse arvo Kirjauskansion nimi -kentässä.
    * Toista kirjauskansion asetukset kunkin yrityksen Käyttöomaisuuden parametrit -sivulla.  

## <a name="depreciation-run"></a>Poiston suorittaminen
1. Siirry kohtaan Käyttöomaisuus > Kirjauskansioviennit > Luo poistoehdotus.
2. Syötä tai valitse arvo Kirjanpitotaso-kenttään.
    * Kirjauskansion nimen oletusarvo saadaan käyttömaisuuden parametreista. Nykyisen yrityksen kirjauskansion nimi voidaan vaihtaa tässä.  
3. Kirjoita päivämäärä Päivämäärään-kenttään.
    * Valitse poistoajoon sisällytettävät yritykset.  
    * Luettelo sisältää vain yritykset, joiden kirjauskansiot on määritetty Käyttöomaisuuden parametrit -sivun Käyttöomaisuuden ehdotukset -osassa.  
4. Valitse Kirjaa kirjauskansiot -kentässä Kyllä.
    * Kenttien suodattaminen sisältää kaiken yrityksen käyttöomaisuuden ja kaikki yrityksen ryhmät ja kirjat, jotka on valittu tähän poistoajoon.  
    * Eräkäsittely-vaihtoehto on käytössä oletusarvoisesti. Kun tämä vaihtoehto on käytössä, poistokirjauskansion luominen ja kirjaaminen suoritetaan taustalla.  
5. Valitse Luo kirjauskansio.
6. Valitse Käyttöomaisuus > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]