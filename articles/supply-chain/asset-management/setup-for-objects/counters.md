---
title: Resurssin mittarit
description: Tässä ohjeaiheessa kerrotaan, kuinka resurssin mittarityypit luodaan resurssien hallinnassa.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 47fd386875e3000d579890ae58a462b643ef1876
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360919"
---
# <a name="counters"></a>Laskurit

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka resurssienhallinnassa luodaan laskurityyppejä. Laskurityyppejä käytetään resurssien laskurirekisteröintien tekemiseen esimerkiksi tuotantotuntien määrän tai resurssin tuottaman määrän osalta. Resurssityypit liittyvät laskurityyppeihin. Tämä tarkoittaa sitä, että laskuria voidaan käyttää resurssin vain, jos laskuri on määritetty resurssiin käytetylle resurssityypille.

Ennen kuin voit tehdä laskurirekisteröintejä resursseille, luo ensin ne laskurityypit, joita haluat käyttää **Laskurit**-kohdassa. Seuraavaksi voit luoda laskurirekisteröintejä kohdassa **Laskurit**. 

Laskureita voidaan käyttää ylläpitosuunnitelmissa. Huoltosuunnitelman rivin tyyppi voi olla esimerkiksi Laskuri, joka liittyy esim. tuotantotuntien määrään tai tuotettuun määrään. 

Laskurirekisteröinti voidaan päivittää manuaalisesti tai automaattisesti tuotantotuntien tai tuotetun määrän perusteella. Laskuri voidaan määrittää käyttämään yhtä kolmesta päivitysmenetelmästä (valitaan **Laskurit**-kohdan **Päivitys**-kentässä):
  
- Manuaalinen – Laskuriarvot on rekisteröitävä manuaalisesti.  
- Tuotantotunnit – laskuri päivitetään automaattisesti tuotantotuntien määrän perusteella.  
- Tuotantomäärä – laskuri päivitetään automaattisesti tuotetun määrän perusteella.  

>[!NOTE]
>Jos käytetään tuotettua määrää, *kaikki* rekisteröidyt nimikkeet sisällytetään laskurirekisteröintiin, sekä hyvä määrä että virhemäärä. On aina mahdollista tehdä manuaalisia laskurirekisteröintejä tarvittaessa.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Luo resurssilaskurien rekisteröintien laskurityypit

1. Valitse **Resurssien hallinta** > **Asetukset** > **Resurssityypit** > **Laskurit**.
2. Luo uusi laskurityyppi valitsemalla **Uusi**.
3. Lisää tunnus **Laskuri**-kenttään ja laskurin nimi **Nimi**-kenttään.
4. Valitse laskuriyksikkö **Yleiset**-pikavälilehden **Yksikkö**-kentässä.
5. Valitse **Päivitys**-kentässä laskurissa käytettävä päivitystapa.
6. Valitse **Peri laskurin arvot** vaihtopainikkeessa Kyllä, jos resurssirakenteen alatason resurssien tulisi periä automaattisesti pääresurssiin tehdyt laskurirekisteröinnit.
7. Valitse **Yhteenlaskettu summa**-kentässä se summausmenetelmä, jota käytetään laskurissa tätä laskurityyppiä käyttäen. "Summa" on vakio valinta, jota käytetään kirjattujen arvojen jatkuvaan lisäämiseen kokonaisarvoon. "Keskiarvo"-arvoa voidaan käyttää, jos laskuri on määritetty valvomaan esimerkiksi resurssin lämpötilaa, tärinää tai kulumista. 
8. Aseta **Poikkeama yli** -kentässä ylempi taso prosentteina, jonka avulla tarkistetaan, jos manuaaliset laskurirekisteröinnit ovat odotetun alueen sisällä. Tarkistus perustuu olemassa olevien laskurirekisteröintien lineaariseen kasvuun.
9. Aseta **Poikkeama ali** -kentässä alempi taso prosentteina, jonka avulla tarkistetaan, jos manuaaliset laskurirekisteröinnit ovat odotetun alueen sisällä. Tarkistus perustuu olemassa olevien laskurirekisteröintien lineaariseen pienenemiseen.
10. Valitse **Tyyppi**-kentässä sanomatyyppi (ilmoitus, varoitus, virhe), joka näytetään, jos määritetyn alueen ulkopuoliset poikkeamat toteutuvat, kun teet manuaalisia laskurirekisteröintejä.
11. Lisää **Resurssityypit**-pikavälilehdessä resurssityypit, joiden tulisi voida käyttää laskuria.
12. Lisää **Liittyvät resurssilaskurit** -pikavälilehdessä laskuri, jota haluat päivittää automaattisesti, kun tämä laskuri päivitetään.


>[!NOTE]
>Liittyvä laskuri päivitetään automaattisesti vain, jos liittyvällä laskurilla on resurssityyppi, johon se liittyy, laskurin määrityksissä. Esimerkki: Voit määrittää laskurin Tuotantotunnit ja lisätä resurssityypin Kuorma-auton moottori. Kun tämä laskuri päivitetään, liittyvään laskuriin "Öljy" päivitetään myös samat laskuriarvot. **Laskurit**-asetuksissa on Tunnit-määritys. Myös laskurille "Öljy" resurssityyppi "Kuorma-auton moottori" pitää lisätä **Resurssityypit**-pikavälilehteen , jotta laskurisuhde voidaan varmistaa. Alla olevissa näyttökuvissa on esimerkki laskureiden Tunti ja Öljy määrityksistä.

Kun resurssityypit lisätään laskurityyppiin kohdassa **Laskurit**, kyseinen laskuri lisätään automaattisesti **Laskurit**-pikavälilehden resurssityyppeihin kohdassa [Resurssitypit](../setup-for-objects/object-types.md).

![Kuva 1.](media/071-setup-for-objects.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]