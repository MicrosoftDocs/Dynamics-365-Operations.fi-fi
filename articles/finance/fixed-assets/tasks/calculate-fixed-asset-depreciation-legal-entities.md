---
title: Käyttöomaisuuden poistojen laskenta eri yrityksissä
description: Käyttöomaisuuden poisto voidaan suorittaa useille yritykselle yhdellä kertaa.
author: moaamer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ca54a45b81b66fdcdd5e43ad6b8c408cb764fb9
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712115"
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
