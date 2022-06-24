---
title: Laskujen TDS-laskenta
description: Tämä artikkeli sisältää viitteen tapahtumille, joissa Vero vähennettynä lähteissä (TDS) lasketaan laskutasolla.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: efc12e0839fe87e9db435f481ce1fd733c286d6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855360"
---
# <a name="tds-calculation-on-invoices"></a>Laskujen TDS-laskenta

[!include [banner](../includes/banner.md)]

Tämä artikkeli sisältää viitteen tapahtumille, joissa Vero vähennettynä lähteissä (TDS) lasketaan laskutasolla.

| Sarjanumero | Tapahtumatyyppi                                 | Tapahtuman summa | Sivun nimi ja valintapolku                                 | Tilin tyyppi ja vastatilin tyyppi                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Toimittajalta tehdyt ostot / kulujen kirjaaminen   | Debet tai Kredit  | Kirjauskansiot-sivu (Kirjanpito > Kirjauskansiomerkinnät > Yleiset kirjauskansiot), Laskun hyväksymiskirjauskansio -sivu (Ostoreskontra > Laskut > Laskun hyväksyminen), Laskukirjauskansio-sivu (Ostoreskontra > Laskut > Laskukirjauskansio) | Kirjanpito (Dr.) Toimittaja (Cr.).  Ennakonpidätys lasketaan toimittaja- ja kirjanpitoyhdistelmälle vain, jos kirjanpitotilin kirjaustyyppi on **Osto** **käteinen**. |
| 2.            | Asiakkaalta tehdyt ostot / kulujen kirjaaminen | Debet tai Kredit  | Kirjauskansiot-sivu (Kirjanpito > Kirjauskansiomerkinnät > Yleiset kirjauskansiot), Laskukirjauskansio-sivu (Ostoreskontra > Laskut > Laskukirjauskansio) | Kirjanpito (Dr.) Asiakas (Cr.)                                 |
| 3.            | Käyttöomaisuuserän ostaminen toimittajalta              | Debet tai Kredit  | Kirjauskansiot-sivu (Kirjanpito > Kirjauskansiomerkinnät > Yleiset kirjauskansiot), Laskurekisterikirjauskansio-sivu (Ostoreskontra > Laskut > Laskurekisteri), Laskukirjauskansio-sivu (Ostoreskontra > Laskut > Laskukirjauskansio) | Käyttöomaisuuserät (Dr.) Toimittaja (Cr.)                             |
| 4.            | Käyttöomaisuuserän ostaminen asiakkaalta            | Debet tai Kredit  | Kirjauskansiot-sivu (Kirjanpito > Kirjauskansiomerkinnät > Yleiset kirjauskansiot), Laskukirjauskansio-sivu (Ostoreskontra > Laskut > Laskukirjauskansio) | Käyttöomaisuuserät (Dr.) Asiakas (Cr.)                           |
| 5.            | Ostolasku (TDS-ostoreskontra)                  |                    | Ostotilaus-sivu (Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset) |                                                              |
| 6.            | Myyntilasku (TDS-myyntireskontra)                  |                    | Myyntitilaussivu (Myyntireskontra > Tilaukset > Kaikki myyntitilaukset), Vapaatekstilasku-sivu (Myyntireskontra > Laskut > Kaikki vapaatekstilaskut) |                                                              |
