---
title: Asiakkaiden hyvittäminen
description: Tässä artikkelissa kerrotaan, miten hyvitystapahtumat luodaan asiakasryhmälle. Jos asiakkaalla on maksettavien saldo, voit hyvittää asiakkaalle saldon summan.
author: JodiChristiansen
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd8b32e04743fdde3cc339e1535f8ae58c518aed
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816289"
---
# <a name="reimburse-customers"></a>Asiakkaiden hyvittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten hyvitystapahtumat luodaan asiakasryhmälle. Jos asiakkaalla on maksettavien saldo, voit hyvittää asiakkaalle saldon summan. 

Seuraavassa taulukossa esitellään edellytykset, joiden on täytyttävä ennen aloittamista.

| Edellytys                                                            | Kuvaus |
|-------------------------------------------------------------------------|-------------|
| Määritä vähimmäishyvityksen määrä yritykselle.          | **Myyntireskontran parametrit** -sivulla **Yleiset**-alueella **Vähimmäissumma**-kentässä, syötä vähimmäissumma, joka voidaan korvata asiakkaan liikamaksuista. |
| Valinnainen: Lisää toimittajatili jokaiselle asiakkaalle, jolle voidaan hyvittää. | **Asiakkaiden** sivulla **Muut tiedot** -pikavälilehdessä **Toimittajatili**-kentässä, valitse toimittajatili asiakkaalle. |

Luodessasi hyvitystapahtumia toimittajalasku luodaan maksettavan saldon määrälle. Takaisinmaksuprosessi poistaa asiakastilin luottosaldon ja luo toimittajatilille erääntyvän saldon, joka vastaa asiakasta.

1. Suorita myyntireskontrassa **Hyvitys**-prosessi (**Myyntireskontra \> Kausittaiset tehtävät \> Hyvitys**).
2. Jos haluat ryhmitellä kaikki tapahtumat kirjauskansion dimensioista huolimatta, määritä **Asiakasyhteenveto**-vaihtoehdon arvoksi **Kyllä**. Voit ryhmitellä vain sellaisia tapahtumia, joilla on samanlaiset kirjanpitodimensiot, määrittämällä arvoksi **Ei**.
3. Valitse **Sisällytä asiakkaat, joilla on avoimia veloitustapahtumia**, jos haluat valita asiakkaat, joilla on selvittämättömiä veloitussummia.
4. Jos haluat hyvittää tiettyjä asiakastilejä, valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** ja määritä sitten asiakastilit kyselyssä.

    Hyvityssummat siirretään asiakkaiden toimittajanumeroille. Ne käsitellään tavallisina maksuina. Jos asiakkaalla ei ole toimittajatiliä, ohjelma luo asiakkaalle automaattisesti kertatoimittajatilin.

5. Voit tarkastella luotuja hyvitystapahtumia käyttämällä **Hyvitys**-raporttia (**Myyntireskontra \> Kyselyt ja raportit \> Hyvitys-raportti**).
6. Ostoreskontrassa, luo maksu toimittajan laskuille, jotka luotiin hyvitysprosessiin maksun luomisessa. Lisätietoja toimittajille maksamisesta on kohdassa [Toimittajan maksun yhteenveto](../accounts-payable/Vendor-payments-workspace.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]