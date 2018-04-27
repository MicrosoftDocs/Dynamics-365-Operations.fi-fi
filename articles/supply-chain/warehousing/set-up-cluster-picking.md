---
title: "Määritä klusterikeräily"
description: "Tässä ohjeaiheessa käsitellään klusterikeräilyn määrittämistä ja nimikevahvistuksen käyttämistä klusterikeräilyssä."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2ec0890963b2b01407acac8003453faf370894b4
ms.openlocfilehash: 1c23421ddfda8c5f6fa27a31831a00ead6094db9
ms.contentlocale: fi-fi
ms.lasthandoff: 04/11/2018

---

[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a>Määritä klusterikeräily

Tässä ohjeaiheessa kuvataan, kuinka työntekijät voivat käyttää mobiililaitteitaan ryhmittelemään työn keräilyn klustereihin, jotta he voivat keräillä nimikkeet yhdestä sijainnista useille työtilauksille samanaikaisesti. Tätä kutsutaan nimellä *klusterin keräys*.

## <a name="about-cluster-picking"></a>Tietoja klusterin keräilystä

Kun työtilaukset on vapautettu varastoon, työntekijä voi määrittää tilaukset klusteriin mobiililaitteen avulla. Klusteri järjestää keräilytyön työntekijälle. Kun työtilaus liitetään klusteriin, työntekijän on käytettävä klusterikeräilyä kyseisen tilauksen keräilytyöhön. Työntekijä ei voi käyttää muita keräilymenetelmiä. Jos työjärjestys määritetään klusteriin vahingossa, työntekijän on pidettävä tauko rikkoakseen klusterin ja luodakseen sen sitten uudelleen.

Tarvittaessa työntekijä voi siirtää klusterin toiselle työntekijälle. Tämä muuttaa klusterin tilaksi Hyväksytty. Kun työntekijä käyttää mobiililaitetta ja ilmoittaa, että keräily ja hyllytys on valmis, lähetys tai kuorma on vahvistettava Dynamics 365 for Finance and Operations -asiakasohjelmassa.

## <a name="set-up-cluster-picking"></a>Määritä klusterikeräily

Jos haluat ottaa klusterin keräilyn käyttöön, sinun on määritettävä seuraavat:

-   **Klusteriprofiilit** – Määritä, luodaanko klusterin tunnukset, käytettävien sijaintien määrä ja klusterien keskeytyskohta automaattisesti. Määritä myös, miten keräilytyö jaksotetaan ja vahvistetaan.

-   **Työmallit** – Määritä, miten klusterikeräilyn keräilytyö luodaan.

-   **Sijaintidirektiivit** – Määritä, mistä nimikkeet kerätään ja mihin ne laitetaan.

-   **Mobiililaitteen valikkovaihtoehdot** – Määritä mobiililaitteen valikkovaihtoehto käyttämään klusterikeräilyn ohjaamaa työtä. Sinun on lisättävä valikkokohde mobiililaitteen valikkoon, jotta se näkyy mobiililaitteilla.

-   **Varastonhallinnan parametrit** – Määritä numerosarja, jota haluat käyttää klustereiden tunnisteiden luontiin.

## <a name="set-up-a-cluster-profile"></a>Klusteriprofiilin määrittäminen

Määritä klusteriprofiili noudattamalla seuraavia ohjeita:

1.  Valitse **Varastonhallinta** \> **Asetukset** \> **Mobiililaite** \> **Klusteriprofiilit**.

2.  Luo uusi profiili valitsemalla **Uusi**.

3.  Määritä klusterin lajitteluperuste valitsemalla ensin **Luo klusteri** ja sitten **Klusterin lajittelu** -kohdassa **Uusi**. Lajitteluehto hallitsee järjestystä, jonka perusteella työntekijä suorittaa keräilytyön. Voit luoda tarvitsemasi määrän kriteereitä.

4.  Anna **Järjestysnumero**-kentässä numero, joka määrittää lajitteluehtojen käsittelyjärjestyksen.

5.  Valitse **Kentän nimi** -kentässä kenttä, joka määrittää lajitteluun. Esimerkiksi jos valitset **WMSLocationId**-kentän, työ lajitellaan sijainnin mukaan.

6.  Valitse **Lajittelu**-kentässä jokin seuraavista vaihtoehdoista.

| **Vaihtoehto**     | **Kuvaus**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nouseva**  | Keräystyö järjestetään nousevassa järjestyksessä lajitteluehtojen perusteella. Jos käytät **WMSLocationId**-kenttää lajitteluehtona ja sijaintitunnuksesi ovat 1, 2, 3 ja 4, keräät sijainnista 4 ensin. |
| **Laskeva** | Keräystyö järjestetään laskevassa järjestyksessä lajitteluehtojen perusteella. Jos käytät **WMSLocationId**-kenttää lajitteluehtona ja sijaintitunnuksesi ovat 1, 2, 3 ja 4, keräät sijainnista 1 ensin. |

## <a name="item-confirmation"></a>Nimikkeen vahvistus

Kun klusterikeräily on käytössä, nimikkeen vahvistaminen on ehdottoman tärkeää, jotta klustereihin lisättävät nimikkeet voidaan tarkistaa. Voit tarkistaa klusterikeräilyn nimikkeet klusterikeräilyn aikana. Määritys perustuu tuotteen viivakoodin asetuksiin.

### <a name="set-up-item-verification-with-cluster-picking"></a>Nimiketarkistuksen määrittäminen klusterikeräilyssä

1.  Avaa mobiililaitteen valikossa työn vahvistuksen määrityslomake: **Varastonhallinta** \> **Varastonhallinta** \> **Asetukset** \> **Mobiililaite** \> **Mobiililaitteen valikkovaihtoehdot**.

2.  Avaa mobiililaitteen valikossa **Työn vahvistusasetukset**. **Tuotteen vahvistus** -asetuksella voi tarkistaa kunkin varastokappaleen mobiililaitteessa skannauksen yhteydessä.

