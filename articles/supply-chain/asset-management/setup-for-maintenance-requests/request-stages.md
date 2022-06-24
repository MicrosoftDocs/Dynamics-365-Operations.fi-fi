---
title: Ylläpitopyynnön elinkaaren tilat
description: Tässä artikkelissa kuvataan, kuinka ylläpitopitopyynnön elinkaaren tilat määritetään resurssien hallinnassa.
author: johanhoffmann
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81b30820adf11f0239ea8ff9d1886b5738e38162
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862711"
---
# <a name="maintenance-request-lifecycle-states"></a>Ylläpitopyynnön elinkaaritilat

[!include [banner](../../includes/banner.md)]

 


Huoltopyynnön elinkaaritilat määrittävät vaiheet, jotka pyyntö voi käydä läpi. Esimerkkejä ovat **Luotu**, **Aktiivinen** ja **Päättynyt**. Kun ylläpitopyyntö muunnetaan työtilaukseksi, kunnossapitopyynnön elinkaaren tilaksi päivitetään **Päättynyt** tai **Suljettu**, mikä osoittaa, että ylläpitopyyntö ei ole enää aktiivinen. **Kaikki ylläpitopyynnöt** -luettelosivulla näkyvät kaikki ylläpitopyynnöt niiden elinkaaritilasta riippumatta.

## <a name="set-up-maintenance-request-lifecycle-states"></a>Ylläpitopyynnön elinkaaren tilojen määritys

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Ylläpitopyynnöt** \> **Elinkaaren tilat**.
2. Luo ylläpitopyynnön elinkaaren tila valitsemalla **Uusi**.
3. Kirjoita **Elinkaaren tila** -kenttään elinkaaren tilan tunnus.
4. Anna nimi **Nimi**-kenttään.

    **Tiedot**-pikavälilehden **Elinkaarimallit**-kentässä näkyy niiden ylläpitopyyntöjen elinkaarimallien määrä, jotka käyttävät tätä elinkaaritilaa.

5. Määritä **Yleiset**-pikavälilehdessä **Aktiivinen**-asetukseksi **Kyllä**, jos ylläpitopyynnön pitäisi olla aktiivinen, kun se on tässä elinkaaren tilassa.
6. Määritä, **Määritä todellinen lopetus** -asetukseksi **Kyllä**, jos todellinen päättymispäivä ja-aika tulee automaattisesti syöttää ylläpitopyyntöön, joka on tässä elinkaaren tilassa.
7. Määritä **luo työtilaus** -asetukseksi **Kyllä**, jos työtilauksen voi luoda ylläpitopyynnöstä, joka on tässä elinkaaren tilassa.
8. Määritä **Poista**-asetukseksi **Kyllä**, jos ylläpitopyyntö voidaan poistaa, kun se on tässä elinkaaren tilassa.
9. **Päivitä**-pikavälilehdessä **käyttöomaisuus**-osan **saapuvat** ja **lähtevät** asetukset ovat olennaisia, jos käytät varaston korjausta. Määritä sopiva vaihtoehto **Kyllä**, jos ylläpitopyynnössä valittujen käyttöomaisuuserien elinkaaren tila päivitetään automaattisesti **saapuvaan** tai **lähtevään** tilaan, kun ylläpitopyynnön elinkaaritilaksi määritetään **saapuva** tai **lähtevä**.

Seuraavassa kuvassa on esimerkki **Ylläpitopyynnön elinkaaren tilat** -sivusta.

![Ylläpitopyynnön elinkaaritilasivu.](media/02-setup-for-requests.png)

> [!NOTE]
> Huoltopyynnön elinkaaritilat, elinkaaren tilaryhmät ja -tyypit liittyvät toisiinsa ja niitä käytetään samalla tavalla kuin työtilauksen elinkaaritiloja, elinkaaren tilaryhmiä ja -tyyppejä. 

## <a name="set-up-maintenance-request-lifecycle-models"></a>Ylläpitopyynnön elinkaarimallien määritys

Kun olet luonut kunnossapitopyynnöille tarvittavat elinkaaritilat, ne voidaan jakaa elinkaaren tilaryhmiin tai elinkaarimalleihin. Huoltopyynnön elinkaarimallien avulla luodaan työnkulku, jota voidaan käyttää erityyppisissä ylläpitopyynnöissä. Vähintään yksi ylläpitopyynnön vakioelinkaarimalli on luotava.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Ylläpitopyynnöt** \> **Elinkaarimallit**.
2. Luo ylläpitopyynnön elinkaarimalli valitsemalla **Uusi**.
3. Kirjoita **Elinkaarimalli** -kenttään elinkaarimallin tunnus.
4. Anna nimi **Nimi**-kenttään.

    **Tiedot**-välilehden **Elinkaaren tilat**-kentässä näkyy niiden elinkaaren tilojen määrä, jotka on valittu tässä elinkaarimallissa. **Ylläpitopyynnön tyypit**-kentässä näkyy tätä elinkaarimallia käyttävien ylläpitopyynnön tyyppien määrä.

5. Valitse **Elinkaaren tilat** -pikavälilehdessä ne elinkaaren tilat, jotka sisällytetään elinkaarimalliin.

    - Jos haluat sisällyttää elinkaaren tilan elinkaarimalliin, valitse se **Jäljellä olevat elinkaaren tilat** -osiosta ja valitse sitten oikealle osoittava nuolipainike ![Oikea nuoli.](media/03-setup-for-requests.png) siirtääksesi sen **Valitut elinkaaren tilat** -osioon.
    - Jos haluat lisätä kaikki käytettävissä olevat elinkaaritilat elinkaarimalliin, valitse **Valitse kaikki käytettävissä olevat tilat** -painike ![Valitse kaikki käytettävissä olevat tilat.](media/04-setup-for-requests.png). Kaikki elinkaaritilat siirretään **Valitut elinkaaren tilat** -osioon.
    - Jos haluat poistaa elinkaaren tilan elinkaarimallista, valitse se **Valitut elinkaaren tilat** -osiosta ja valitse sitten vasemmalle osoittava nuolipainike ![Vasen nuoli.](media/05-setup-for-requests.png) siirtääksesi sen **Jäljellä olevat elinkaaren tilat** -osioon.

6. **Yleiset**-pikavälilehden **Päivitykset**-osion kentät ovat merkityksellisiä, jos käytät varastokorjausta.

    - Valitse **Vastaanotetun resurssin elinkaaren tila** -kentässä resurssin elinkaaren tila, johon ylläpitopyynnössä valitut resurssit päivitetään automaattisesti, kun ne vastaanotetaan varastokorjausta varten.
    - Valitse **Toimitetun resurssin elinkaaren tila** -kentässä resurssin elinkaaren tila, johon ylläpitopyynnössä valitut resurssit päivitetään automaattisesti, kun ne palautetaan korjauksen jälkeen.

Seuraavassa kuvassa on esimerkki **Ylläpitopyynnön elinkaarimallit** -sivusta.

![Ylläpitopyynnön elinkaarimallit -sivu.](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]