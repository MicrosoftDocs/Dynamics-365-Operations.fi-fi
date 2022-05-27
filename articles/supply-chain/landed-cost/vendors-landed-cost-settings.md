---
title: Aiheutuneelle kustannukselle lisätyt toimittaja-asetukset
description: Tässä aiheessa kuvataan uudet kentät, jotka lisätään olemassa olevalle Toimittajat-sivulle, kun Aiheutunut kustannus -moduuli otetaan käyttöön. Näiden kenttien avulla määritetään ne toimittajat, joita käytetään yhdessä Aiheutunut kustannus -toimintojen kanssa.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b4e02397f7a4cdeaa21b451268b16e4fbe773612
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690523"
---
# <a name="vendor-settings-added-for-landed-cost"></a>Aiheutuneelle kustannukselle lisätyt toimittaja-asetukset

[!include [banner](../../includes/banner.md)]

Kun otat **Aiheutunut kustannus** -moduulin käyttöön, olemassa olevalle **Toimittajat**-sivulle lisätään useita uusia kenttiä. Näiden kenttien avulla määritetään ne toimittajat, joita käytetään yhdessä Aiheutunut kustannus -toimintojen kanssa.

Voit määrittää tarvittavat kentät valitsemalla **Hankinta \> Toimittajat \> Kaikki toimittajat**. Avaa olemassa oleva toimittaja tai luo uusi toimittaja ja valitse sitten **Muut tiedot** -pikavälilehti. Kaikki uudet **Aiheutunut kustannus** -moduulin lisäämät kentät tulevat näkyviin **Matkat**-otsikon alle. Kentät käsitellään seuraavassa taulukossa.

| Kenttä | kuvaus |
|---|---|
| Lähetystyyppi | <p>Valitse toimittajan rooli suhteessa aiheutuneeseen kustannukseen:</p><ul><li>**Ei mitään** – Toimittajalla ei ole tiettyä aiheutuneeseen kustannukseen liittyvää roolia. Tämä arvo on oletusarvo, koska useimmilla toimittajilla ei todennäköisesti ole tiettyä roolia.</li><li>**Rahdinkuljettaja** – Toimittaja on rahdinkuljettaja. Toimittajat, joilla on tämä lähetystyyppi, voidaan valita **Matkat**-sivun **Rahdinkuljettaja**-kentässä.</li><li>**Tulliasioitsija** – Toimittaja on tulliasioitsija. Toimittajat, joilla on tämä lähetystyyppi, voidaan valita **Pakkaus**-sivun **Tulliasioitsija**-kentässä.</li><li>**Agentti** – Toimittaja on agentti. Toimittajat, joilla on tämä lähetystyyppi, voidaan valita **Toimittajat**-sivun ja **Ostotilaukset**-sivun **Agentti**-kentässä.</li></ul> |
| Kustannustyyppiryhmä | Liitä toimittaja kustannuslajiryhmään [automaattisten kustannusten](auto-cost-setup.md) valitsemista varten. |
| Lähtösatama | Valitse matkan lähtösatama. |
| Agentti | Oletusagentti, kun toimittajalta tehdään hankintoja. |
| Tuonnin kustannuslaskennan toimittaja | <p>Määritä, onko toimittaja aiheutuneen kustannuksen toimittaja.</p><p>**Vihje:** Voit käyttää tätä kenttää yhdessä tietuetason turvan kanssa matkan luonnin yhteydessä näkyvien ostotilausten rajoittamiseksi.</p> |
| Kuljetusyritys | Valitse oletusarvoinen rahdinkuljettaja, jota käytetään, kun toimittajalle luodaan ostotilauksia. |
| Palvelujen tarjoaja | Määritä, onko toimittaja palveluntarjoaja. |
| Ylitys- ja alitustoleranssiryhmä | Valitse toimittajalle oletusarvoinen ylitys- ja alitustoleranssiryhmä. |
