---
title: Ehdota käyttöomaisuuden hankintaa
description: Tässä artikkelissa kerrotaan, miten voit hankkia käyttöomaisuutta käyttöomaisuuden kirjauskansion hankintaehdotuksen avulla.
author: moaamer
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35d2171dc828cb0227f310e81be1d3e3359f41c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909066"
---
# <a name="propose-fixed-asset-acquisitions"></a>Ehdota käyttöomaisuuden hankintaa

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten voit hankkia käyttöomaisuutta käyttöomaisuuden kirjauskansion hankintaehdotuksen avulla. Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja. Jos aiot hankkia käyttöomaisuuden käyttöomaisuuden ehdotuskirjauskansion avulla, ensin on luotava käyttöomaisuustietue ja sitten määritettävä hankintahinta käyttöomaisuuskirjassa.

## <a name="create-an-asset-acquisition-proposal"></a>Käyttöomaisuuden hankintaehdotuksen luominen

Luo käyttöomaisuuden hankintaehdotus seuraavasti. 

1. Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio**.
2. Valitse **Uusi**.
3. Anna tai valitse arvo **Nimi**-kentässä.
4. Valitse toimintoruudussa **Rivit**.
5. Valitse **Ehdotukset**.
6. Valitse **Hankintaehdotus**.
7. Valitse **Suodata**. Tyhjennä aiemmat arvot valitsemalla **Palauta**.
8. Valitse **Käyttöomaisuuserän numero** -rivi.
9. Anna tai valitse arvo **Ehdot**-kentässä. Määritä muut ehdot käyttöomaisuuserille, jotka haluat hakea tämän ehdotuksen avulla.  
10. Poistu ruudusta valitsemalla **OK** kahdesti.
- Tarkista, että tapahtumarivit on luotu.  
- Hankintaehdotukseen sisällytetään vain se käyttöomaisuuserä, jonka hankintapäivämäärä ja -hinta on määritetty kirjassa.  
11. Valitse sivulla **Kirjat**-välilehti.
12. Valitse **Kirjaa**.

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a>Sisällytä taloushallinnon oletusdimensiot hankintaehdotukseen

Hankintatapahtuma voidaan luoda Excel-apuohjelman avulla valitsemalla **Käyttöomaisuus > Kirjauskansioviennit > Käyttöomaisuuserän kirjauskansio**. Luo uusi kirjauskansio, siirry sivun **Rivit**-osaan, valitse Excel-kuvake ja valitse sitten käyttöomaisuuspäiväkirjan rivi. Järjestelmä luo ja avaa kirjauskansiorivejä edustavan Excel-mallin. Voit lisätä malliin päiväkirjarivien lisättävät tiedot ja julkaista tiedot sitten takaisin järjestelmään. 

Jos valitulle käyttöomaisuuskirjalle ja vastaaville Excel-malliin syötetyille käyttöomaisuuserille on määritetty oletusdimensiot, taloushallinnon oletusdimensioita kutsutaan käyttöomaisuuskirjan päätiedoista, kun kirjauskansio julkaistaan Excelistä järjestelmään. Jos haluat sisällyttää taloushallinnon dimensiot käyttöomaisuuskirjaan automaattisesti, kun julkaiset käyttöomaisuuskirjauskansion Excel-apuohjelmasta, oletusdimensiot on määritettävä etukäteen.  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
