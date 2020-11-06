---
title: Asiakkaiden hyvittäminen
description: Tässä artikkelissa kerrotaan, miten hyvitystapahtumat luodaan asiakasryhmälle. Jos asiakkaalla on maksettavien saldo, voit hyvittää asiakkaalle saldon summan.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bceeaf99437f6ef66bd3b4e1710b469c262e693e
ms.sourcegitcommit: 9e7ceb5604472f3088f611aa0360bd6a716db32b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022540"
---
# <a name="reimburse-customers"></a>Asiakkaiden hyvittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten hyvitystapahtumat luodaan asiakasryhmälle. Jos asiakkaalla on maksettavien saldo, voit hyvittää asiakkaalle saldon summan. 

Seuraavassa taulukossa esitellään edellytykset, joiden on täytyttävä ennen aloittamista.

| Edellytys                                                            | Kuvaus                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Määritä vähimmäishyvityksen määrä yritykselle.          | **Myyntireskontran parametrit** -sivulla **Yleiset** -alueella **Vähimmäissumma** -kentässä, syötä vähimmäissumma, joka voidaan korvata asiakkaan liikamaksuista. |
| Valinnainen: Lisää toimittajatili jokaiselle asiakkaalle, jolle voidaan hyvittää. | **Asiakkaiden** sivulla **Muut tiedot** -pikavälilehdessä **Toimittajatili** -kentässä, valitse toimittajatili asiakkaalle.                                           |

Luodessasi hyvitystapahtumia toimittajalasku luodaan maksettavan saldon määrälle. Takaisinmaksuprosessi poistaa asiakastilin luottosaldon ja luo toimittajatilille erääntyvän saldon, joka vastaa asiakasta.

1.  Myyntireskontrassa suorita **Hyvitys** -prosessi.
2.  Noudata seuraavia ohjeita:
    -   Jos haluat hyvittää tiettyjä asiakasnumeroita, klikkaa **Valitse**  ja määritä kyselyn asiakastilit.
    -   Voit hyvittää kaikkia asiakasnumeroita valitsemalla **OK**.

    Hyvityssummat siirretään asiakkaiden toimittajanumeroille. Ne käsitellään tavallisina maksuina. Jos asiakkaalla ei ole toimittajatiliä, ohjelma luo asiakkaalle automaattisesti kertatoimittajatilin.
3.  Tarkastellaksesi luotuja hyvitystapahtumia, käytä **Hyvitys** -sivua.
4.  Ostoreskontrassa, luo maksu toimittajan laskuille, jotka luotiin hyvitysprosessiin maksun luomisessa.




