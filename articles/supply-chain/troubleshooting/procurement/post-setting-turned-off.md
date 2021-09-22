---
title: Kirjaa kirjanpidon veloitustilille -asetus ei ole käytössä
description: Tämä ongelma ilmenee, kun ostotilaus laskutetaan ja Kirjaa kirjanpidon veloitustilille -asetus on käytössä Ostoreskontran parametrit -sivun Lasku-välilehdessä.
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
ms.openlocfilehash: 592444958dad4624fdc9098dc58df0a2e49e63de
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476248"
---
# <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Kirjaa kirjanpidon veloitustilille -asetus ei ole käytössä

## <a name="symptoms"></a>Oireet

Tämä ongelma ilmenee, kun ostotilaus laskutetaan ja **Kirjaa kirjanpidon veloitustilille** -asetuksen arvona on *Kyllä* **Ostoreskontran parametrit** -sivun **Lasku**-välilehdessä.

## <a name="reproduce-the-issue"></a>Ongelman toistaminen

Seuraavassa esitetään yksi tapa ongelman toistamiseen.

1. Valitse **Ostoreskontra \> Asetukset \> Ostoreskontran parametrit**.
1. Määritä **Lasku**-välilehden **Kirjaa kirjanpidon veloitustilille** -asetukseksi *Kyllä*.
1. Siirry kohtaan **Varastonhallinta \> Määritys \> Kirjaus \> Kirjaus**.
1. Varmista **Ostotilaus**-välilehdellä, että olet poistanut kaikki tuotteen ostomenojen rivit.
1. Valitse **Ostoreskontra \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Luo ostotilaus. Valitse **Toimittajatili**-kentässä *1001 Acme-toimistotarviketta*.
1. Lisää ostotilausrivi, jossa on seuraavat asetukset:

    - **Nimikenumero:** *D0011 Laserprojektori*
    - **Toimipaikka:** *1*
    - **Varasto**: *11*
    - **Määrä** *4*

1. Valitse toimintoruudun **osta**-välilehden **Toimi**-ryhmässä **Vahvista**.
1. Valitse toimintoruudun **Vastaanota**-välilehden **Luo**-ryhmässä **Tuotteen vastaanotto**.
1. Syötä **Tuotteen vastaanottokirjaus** -valintaikkunan **Tuotteen vastaanotto** -kenttään satunnainen numero ja valitse **OK**.
1. Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.
1. Syötä **Numero**-kenttään satunnainen numero laskunumeroksi.
1. Päivitä täsmäytyksen tila ja kirjaa.
1. Huomaa, näkyviin tulee nyt seuraava virhe, kun luot laskun ostotilauksesta: "Tuotteen ostomenot -tapahtumatyypin tilinumeroa ei ole olemassa".

## <a name="resolution"></a>Ratkaisu

Tämä määräytyy laskujen ja laskuryhmien parametriasetusten perusteella. Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostomenojen kirjaaminen ja varastotilanteen vaihtelut](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
