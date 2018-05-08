---
title: "Käyttöomaisuuserän arvomallin ja poistokirjan yhdistäminen"
description: "Aiemmissa julkaisuversioissa oli kaksi käyttöomaisuuserien arviointikäsitettä: arvomallit ja poistokirjat. Microsoft Dynamics 365 for Operations (1611) -julkaisussa arvomallin toiminnot ja poistokirjatoiminnot on yhdistetty yhdeksi käsitteeksi, jota kutsutaan kirjaksi."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ef31b63dd253ab5b436a65385e248c4753abf1e
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Käyttöomaisuuserän arvomallin ja poistokirjan yhdistäminen

[!include [banner](../includes/banner.md)]

Aiemmissa julkaisuversioissa oli kaksi käyttöomaisuuserien arviointikäsitettä: arvomallit ja poistokirjat. Microsoft Dynamics 365 for Operations (1611) -julkaisussa arvomallin toiminnot ja poistokirjatoiminnot on yhdistetty yhdeksi käsitteeksi, jota kutsutaan kirjaksi.

Uusi kirja-toiminto perustuu aiempaan arvomalli-toimintoon, mutta sisältää myös kaikki aiemmin pelkästään poistokirjoihin sisältyvät toiminnot. [![Kirja arvomallin yhdistämisenä ja poistokirjan toiminnot](./media/fixed-assets.png)](./media/fixed-assets.png) Yhdistämisen ansiosta voi nyt käyttää samaa sivu-, kysely- ja raporttisarjaa kaikille käyttöomaisuusprosesseille. Tämän aiheen taulukoissa kuvataan aiempia arvomallien ja poistokirjojen toimintoja verrattuina uusien kirjojen toimintoihin.

## <a name="setup"></a>Luo perustiedot
Kirjat suorittavat oletusarvoisesti kirjauksia sekä kirjanpitoon (GL) että käyttöomaisuuserän alareskontraan. Kirjoissa on uusi **Kirjaa kirjanpitoon** -asetus, joka mahdollistaa Kirjataan kirjanpitoon- ja Kirjaa vain käyttöomaisuuserän alareskontraan -toimintojen poistamisen käytöstä. Tämä toiminto muistuttaa aiempaa poistokirjojen kirjaustapaa. Kirjauskansioiden nimien asetuksissa on uusi kirjanpitotaso "Ei mitään". Tämä kirjanpitotaso lisättiin erityisesti käyttöomaisuustapahtumia varten. Kirjoissa, jotka eivät kirjaa tapahtumia kirjanpitoon, on käytettävä kirjaamiseen kirjauskansionimeä, joka on määritetty kirjanpitotasolle **Ei mitään**.

|                                                  |                                 |                                 |                                                         |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
|                                                  | Poistokirja               | Arvomalli                     | Kirja (uusi)                                              |
| Kirjaa kirjanpitoon                                   | En koskaan                           | Aina                          | Kirjanpitoon kirjaamisen vaihtoehto                                |
| Kirjanpitotasot                                   | Ei käytettävissä                  | 3: Nykyinen, Liiketoiminnot, Verot | 11: Nykyinen, Liiketoiminnot, Vero, 7 mukautettua tasoa, Ei mitään |
| Kirjauskansioiden nimet                                    | Poistokirjan kirjauskansioiden nimet | Kirjanpito - Kirjauskansioiden nimet              | Kirjanpito - Kirjauskansioiden nimet                                      |
| Johdetut kirjat                                    | Ei sallittu                     | Sallittu                         | Sallittu                                                 |
| Poistoprofiili ohittaa käyttöomaisuustasolla | Sallittu                         | Ei sallittu                     | Sallittu                                                 |

## <a name="processes"></a>Prosessit
Prosessit käyttävät yhteistä sivua. Jotkin prosessit ovat sallittuja vain, jos **Kirjaa kirjanpitoon** -asetus on **ei** kirjan asetuksissa.

|                                |                           |                     |                                          |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
|                                | Poistokirja         | Arvomalli         | Kirja (uusi)                               |
| Tapahtuman syöttäminen              | Poistokirjan kirjauskansio | Käyttöomaisuuserän kirjauskansio | Käyttöomaisuuserän kirjauskansio                      |
| Bonuspoisto             | Sallittu                   | Ei sallittu         | Sallittu                                  |
| Poista aiemmat tapahtumat | Sallittu                   | Ei sallittu         | Sallittu, ellet ole kirjaamassa kirjanpitoon |
| Joukkopäivitys                    | Sallittu                   | Ei sallittu         | Sallittu, ellet ole kirjaamassa kirjanpitoon |

## <a name="inquiries-and-reports"></a>Kyselyt ja raportit
Kyselyt ja raportit tukevat kaikkia kirjoja. Raportit, jotka eivät sisälly seuraavaan taulukkoon, tukivat aiemmin sekä poistokirjoja että arvomalleja, ja ne tukevat jatkossa kaikkia kirjatyyppejä. **Kirjaustaso**-kenttä myös lisätty raportteihin niin, että tapahtuman kirjaukset voidaan helposti tunnistaa.

|                                       |                                |                          |                          |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
|                                       | Poistokirja              | Arvomalli              | Kirja (uusi)               |
| Kyselyt                             | Poistokirjan tapahtumat | Käyttöomaisuustapahtumat | Käyttöomaisuustapahtumat |
| Käyttöomaisuuserittely kohteittain                 | Ei sallittu                    | Sallittu                  | Sallittu                  |
| Käyttöomaisuuserän peruste                     | Sallittu                        | Ei sallittu              | Sallittu                  |
| Käyttöomaisuuserän käytettävyys vuosineljänneksen puolivälissä | Sallittu                        | Ei sallittu              | Sallittu                  |

## <a name="upgrade"></a>Päivitä
Päivitysprosessi siirtää aiemmin määritetyt asetukset ja kaikki olemassa olevat tapahtumat uuden kirjan rakenteeseen. Arvomallit säilyvät nykyisellään, kirjana joka tekee kirjauksia kirjanpitoon. Poistokirjat sen sijaan siirretään kirjaan, jonka **Kirjaa kirjanpitoon** -asetus on **Ei**. Poistokirjan kirjauskansioiden nimet siirretään kirjanpidon kirjauskansion nimeen, jonka kirjanpitotasoksi on määritetty **Ei mitään**.




