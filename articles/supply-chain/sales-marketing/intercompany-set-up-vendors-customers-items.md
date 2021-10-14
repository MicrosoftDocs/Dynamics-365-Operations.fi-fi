---
title: Toimittajien, asiakkaiden ja nimikkeiden määrittäminen konsernin sisäisessä kaupassa
description: Tässä aiheessa käsitellään toimittajien, asiakkaiden ja nimikkeiden määrittämistä konsernin sisäisessä kaupassa
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 062b8fe956fef0f8172d26aac3df54b93e1941ef
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548232"
---
# <a name="set-up-vendors-customers-and-items-for-intercompany-trade"></a>Toimittajien, asiakkaiden ja nimikkeiden määrittäminen konsernin sisäisessä kaupassa

[!include [banner](../../includes/banner.md)]

Organisaation valmistelu konsernin sisäistä kauppaa varten edellyttää, että toimittajat ja asiakkaat, joiden kanssa kauppaa käydään sisäisesti, määritetään. Nämä toimittajat ja asiakkaat on sitten liitettävä ostettaviin tai myytäviin nimikkeisiin.

1. Valitse **Hankinta \> Toimittajat \> Kaikki toimittajat**.
1. Valitse konsernin sisäiseksi toimittajaksi määritettävä toimittaja.
1. Valitse toimintoruudun **Yleiset**-välilehdessä **Konsernin sisäinen**.
1. Määritä toimittajatilin konsernin sisäiset asetusparametrit. Nämä parametrit sisältävät asiakasyrityksen ja -tilin, myyntitilauskäytännöt, ostotilauskäytännöt, arvon yhdistämismäärityksen sekä osto- ja myyntisopimuskäytännöt. Lisäksi voidaan määrittää, käytetäänkö perustietoarvoja toimittajatililtä tai toisen yrityksen asiakastililtä.
1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse **Liittyvät tuotteet** -luettelosivulla toimittajalle määritettävät nimikkeet, jolloin nimikkeet ovat käytettävissä konsernin sisäisessä kaupassa. Avaa kunkin nimikkeen **Vapautetun tuotteen tiedot** -sivu. Kirjoita **Osto**-välilehden **Toimittaja**-kenttään toimittajanumero.
1. Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.
1. Valitse konsernin sisäiseksi asiakkaaksi määritettävä asiakas.
1. Valitse toimintoruudun **Yleiset**-välilehdessä **Konsernin sisäinen**.
1. Määritä asiakastilin konsernin sisäiset asetusparametrit. Nämä parametrit sisältävät toimittajayrityksen ja -tilin, ostotilauskäytännöt, myyntitilauskäytännöt, arvon yhdistämismäärityksen sekä myynti- ja ostosopimuskäytännöt. Lisäksi voidaan määrittää, käytetäänkö perustietoarvoja asiakastililtä tai toisen yrityksen toimittajatililtä.
1. Valitse **Asiakkaat**-sivun **Lasku ja toimitus** -pikavälilehdessä **Luo konsernin sisäiset tilaukset** -valintaruutu. Jos tilaukset halutaan toimittaa suoraan asiakkaille, valitse **Suoratoimitus**-valintaruutu.

    > [!NOTE]
    > Jos yritys varastoi ja toimittaa joitakin nimikkeitä asiakkaille, konsernin sisäisiä tilauksia ei ehkä kannata luoda automaattisesti, vaikka nimikettä olisikin varastossa. Varastossa mahdollisesti joskus olevien nimikkeiden automaattinen luonti poistetaan käytöstä, poistamalla **Luo konsernin sisäiset tilaukset** -valintaruudun valinta.

1. Valitsemalla **Luo epäsuoria tilausrivejä** -valintaruutu voidaan antaa mahdollisuus luoda myyntitilaukseen lisärivejä epäsuorasti. Käyttäjä voi sitten lisätä alkuperäiseen myyntitilaukseen rivejä konsernin sisäisestä myyntitilauksesta.

> [!WARNING]
> Jos myyntitilausten epäsuora luonti sallitaan, kaikki lisäykset konsernin sisäisestä myyntitilauksesta alkuperäiseen myyntitilaukseen sallitaan. Kukin lisäys käsitellään sitten asiakkaaseen ja lisätään tilaukseen ja laskuun. Lisäksi jokainen myyntiin liittyvä asiakirja tulostetaan ja kirjataan automaattisesti. Lisäyksestä ei ilmoiteta käyttäjille.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
