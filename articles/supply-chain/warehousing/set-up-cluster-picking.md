---
title: Määritä klusterikeräily
description: Tässä ohjeaiheessa käsitellään klusterikeräilyn määrittämistä ja nimikevahvistuksen käyttämistä klusterikeräilyssä.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b3df8cf5e63fe97925f17001e836a41c703dfc9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239227"
---
# <a name="set-up-cluster-picking"></a>Määritä klusterikeräily

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan, kuinka työntekijät voivat käyttää mobiililaitteitaan ryhmittelemään työn keräilyn klustereihin, jotta he voivat keräillä nimikkeet yhdestä sijainnista useille työtilauksille samanaikaisesti. Tätä kutsutaan nimellä *klusterin keräys*.

## <a name="about-cluster-picking"></a>Tietoja klusterin keräilystä

Kun työtilaukset on vapautettu varastoon, työntekijä voi määrittää tilaukset klusteriin mobiililaitteen avulla. Klusteri järjestää keräilytyön työntekijälle. Kun työtilaus liitetään klusteriin, työntekijän on käytettävä klusterikeräilyä kyseisen tilauksen keräilytyöhön. Työntekijä ei voi käyttää muita keräilymenetelmiä. Jos työjärjestys määritetään klusteriin vahingossa, työntekijän on pidettävä tauko rikkoakseen klusterin ja luodakseen sen sitten uudelleen.

Tarvittaessa työntekijä voi siirtää klusterin toiselle työntekijälle. Tämä muuttaa klusterin tilaksi Hyväksytty. Kun hän käyttää kannettavaa laitetta ja ilmoittaa, että keräily ja hyllytys on valmis, lähetys tai kuorma on vahvistettava asiakasohjelmassa.

## <a name="enable-cluster-picking"></a>Klusterikeräilyn ottaminen käyttöön

Jos haluat ottaa klusterin keräilyn käyttöön, sinun on määritettävä seuraavat:

- **Klusteriprofiilit** – Määritä, luodaanko klusterin tunnukset, käytettävien sijaintien määrä ja klusterien keskeytyskohta automaattisesti. Määritä myös, miten keräilytyö jaksotetaan ja vahvistetaan.

- **Työmallit** – Määritä, miten klusterikeräilyn keräilytyö luodaan.

- **Sijaintidirektiivit** – Määritä, mistä nimikkeet kerätään ja mihin ne sijoitetaan.

- **Mobiililaitteen valikkovaihtoehdot** – Määritä mobiililaitteen valikkovaihtoehto käyttämään klusterikeräilyn ohjaamaa työtä. Sinun on lisättävä valikkokohde mobiililaitteen valikkoon, jotta se näkyy mobiililaitteilla.

- **Varastonhallinnan parametrit** – Määritä numerosarja, jota haluat käyttää klustereiden tunnisteiden luontiin.

## <a name="set-up-a-cluster-profile"></a>Klusteriprofiilin määrittäminen

Määritä klusteriprofiili noudattamalla seuraavia ohjeita:

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Mobiililaite** \> **Klusteriprofiilit**.

1. Luo uusi profiili valitsemalla **Uusi**.

1. Määritä klusterin lajitteluperuste valitsemalla ensin **Luo klusteri** ja sitten **Klusterin lajittelu** -kohdassa **Uusi**. Lajitteluehto hallitsee järjestystä, jonka perusteella työntekijä suorittaa keräilytyön. Voit luoda tarvitsemasi määrän kriteereitä.

1. Anna **Järjestysnumero**-kentässä numero, joka määrittää lajitteluehtojen käsittelyjärjestyksen.

1. Valitse **Kentän nimi** -kentässä kenttä, joka määrittää lajitteluun. Esimerkiksi jos valitset **WMSLocationId**-kentän, työ lajitellaan sijainnin mukaan.

1. Valitse **Lajittelu**-kentässä jokin seuraavista vaihtoehdoista.

| **Vaihtoehto**     | **Kuvaus**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nouseva**  | Keräystyö järjestetään nousevassa järjestyksessä lajitteluehtojen perusteella. Jos käytät **WMSLocationId**-kenttää lajitteluehtona ja sijaintitunnuksesi ovat 1, 2, 3 ja 4, keräät sijainnista 4 ensin. |
| **Laskeva** | Keräystyö järjestetään laskevassa järjestyksessä lajitteluehtojen perusteella. Jos käytät **WMSLocationId**-kenttää lajitteluehtona ja sijaintitunnuksesi ovat 1, 2, 3 ja 4, keräät sijainnista 1 ensin. |

## <a name="item-confirmation"></a>Nimikkeen vahvistus

Kun klusterikeräily on käytössä, nimikkeen vahvistaminen on ehdottoman tärkeää, jotta klustereihin lisättävät nimikkeet voidaan tarkistaa. Voit tarkistaa klusterikeräilyn nimikkeet klusterikeräilyn aikana. Määritys perustuu tuotteen viivakoodin asetuksiin.

### <a name="set-up-item-verification-with-cluster-picking"></a>Nimiketarkistuksen määrittäminen klusterikeräilyssä

1. Avaa mobiililaitteen valikossa työn vahvistuksen määrityslomake: **Varastonhallinta** \> **Varastonhallinta** \> **Asetukset** \> **Mobiililaite** \> **Mobiililaitteen valikkovaihtoehdot**.

1. Avaa mobiililaitteen valikossa **Työn vahvistusasetukset**. **Tuotteen vahvistus** -asetuksella voi tarkistaa kunkin varastokappaleen mobiililaitteessa skannauksen yhteydessä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]