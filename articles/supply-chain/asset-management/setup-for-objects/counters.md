---
title: Resurssin mittarit
description: Tässä ohjeaiheessa kerrotaan, kuinka resurssin mittarityypit luodaan resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783245"
---
# <a name="asset-measures"></a>Resurssin mittarit

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka resurssin mittarityypit luodaan resurssien hallinnassa. Resurssien mittatyyppejä käytetään resurssien mittausrekisteröintien tekemiseen esimerkiksi tuotantotuntien määrän tai resurssin tuottaman määrän osalta. Resurssityypit liittyvät resurssien mitta tyyppeihin. Tämä tarkoittaa sitä, että resurssi mittaa voidaan käyttää vain, jos resurssin mitta on määritetty resurssiin käytetylle resurssityypille.

Ennen kuin voit tehdä mittauksen rekisteröinnit resursseille, luo ensin ne resurssin mittatyypit, joita haluat käyttää **Laskurit**-kohdassa. Seuraavaksi voit luoda resurssien mittausrekisteröinnit kohdassa **Resurssin mittarit**. 

Resurssin mittareita voidaan käyttää huoltosuunnitelmissa. Huoltosuunnitelman rivin tyyppi voi olla esimerkiksi Laskuri, joka liittyy esim. tuotantotuntien määrään tai tuotettuun määrään. 

Resurssin mittarirekisteröinti voidaan päivittää manuaalisesti tai automaattisesti tuotantotuntien tai tuotetun määrän perusteella. Resurssin mittari voidaan määrittää käyttämään yhtä kolmesta päivitysmenetelmästä (valitaan**Laskurit**-kohdan **Päivitys**-kentässä):
  
- Manuaalinen – Resurssin mittariarvot on rekisteröitävä manuaalisesti.  
- Tuotantotunnit – laskuri päivitetään automaattisesti tuotantotuntien määrän perusteella.  
- Tuotantomäärä – laskuri päivitetään automaattisesti tuotetun määrän perusteella.  

>[!NOTE]
>Jos käytetään tuotettua määrää, *kaikki* rekisteröidyt nimikkeet sisällytetään mittausrekisteröintiin, sekä hyvä määrä että virhemäärä. On aina mahdollista tehdä manuaalisia resurssin mittarirekisteröintejä tarvittaessa.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Luo resurssilaskurien rekisteröintien laskurityypit

1. Valitse **Resurssien hallinta** > **Asetukset** > **Resurssityypit** > **Laskurit**.
2. Luo uusi resurssin mittarityyppi valitsemalla **Uusi**.
3. Lisää tunnus **Laskuri**-kenttään ja laskurin nimi **Nimi**-kenttään.
4. Valitse mittayksikkö **Yleiset**-pikavälilehden **Yksikkö**-kentässä.
5. Valitse **Päivitys**-kentässä resurssin mittarissa käytettävä päivitystapa.
6. Valitse **Peri laskurin arvot** vaihtopainikkeessa Kyllä, jos resurssirakenteen alatason resurssien tulisi periä automaattisesti pääresurssiin tehdyt rekisteröinnit.
7. Valitse **Yhteenlaskettu summa**-kentässä se summausmenetelmä, jota käytetään resurssin mitassa tätä resurssin mittatyyppiä käyttäen. "Summa" on vakio valinta, jota käytetään kirjattujen arvojen jatkuvaan lisäämiseen kokonaisarvoon. "Keskiarvo"-arvoa voidaan käyttää, jos resurssin mitta on määritetty valvomaan esimerkiksi resurssin lämpötilaa, tärinää tai kulumista. 
8. Aseta **Poikkeama yli** -kentässä ylempi taso prosentteina, jonka avulla tarkistetaan, jos manuaaliset resurssin rekisteröinnit ovat odotetun alueen sisällä. Tarkistus perustuu olemassa olevien resurssin rekisteröintien lineaariseen kasvuun.
9. Aseta **Poikkeama alle** -kentässä alempi taso prosentteina, jonka avulla tarkistetaan, jos manuaaliset resurssin rekisteröinnit ovat odotetun alueen sisällä. Tarkistus perustuu olemassa olevien resurssin rekisteröintien lineaariseen vähenemiseen.
10. Valitse **Tyyppi**-kentässä sanomatyyppi (ilmoitus, varoitus, virhe), joka näytetään, jos määritetyn alueen ulkopuoliset poikkeamat toteutuvat, kun teet manuaalisia resurssin mittauksen rekisteröintejä.
11. Lisää **Resurssityypit**-pikavälilehdessä resurssityypit, joiden tulisi voida käyttää resurssin mittaria.
12. Lisää **Liittyvät resurssin mittarit** -pikavälilehdessä resurssin mitat, jotka haluat päivittää automaattisesti, kun tämä resurssin mitta päivitetään.


>[!NOTE]
>Liittyvä resurssin mittari päivitetään automaattisesti vain, jos liittyvällä resurssin mittarilla on resurssityyppi, johon se liittyy, resurssin mittauksen määrityksissä. Esimerkki: Voit määrittää resurssin mittarin Tuotantotunnit ja lisätä resurssityypin Kuorma-auton moottori. Kun tämä resurssin mittari päivitetään, liittyvään laskuriin "Öljy" päivitetään myös samat mittarin arvot. **Laskurit**-asetuksissa on Tunnit-määritys. Myös resurssin mittarille "Öljy" resurssityyppi "Kuorma-auton moottori" pitää lisätä **Resurssityypit**-pikavälilehteen , jotta resurssin mittarin suhde voidaan varmistaa. Alla olevissa näyttökuvissa on esimerkki resurssin mittarien Tunti ja Öljy määrityksistä.

Kun resurssityyppit lisätään resurssin mittarityyppiin kohdassa **Laskurit**, kyseinen resurssin mittari lisätään automaattisesti **Laskurit**-pikavälilehden resurssityyppeihin kohdassa [Resurssitypit](../setup-for-objects/object-types.md).

![Kuva 1](media/071-setup-for-objects.png)


