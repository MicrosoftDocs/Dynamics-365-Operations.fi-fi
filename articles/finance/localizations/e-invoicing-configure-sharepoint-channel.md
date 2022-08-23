---
title: SharePoint-kanavan konfiguroiminen
description: Tässä artikkelissa kerrotaan, kuinka Microsoft SharePoint -kanava määritetään käsittelemään saapuvat sähköiset laskut.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 92eaa357c6d72cc637d4ce353702e5d41ecf4338
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272301"
---
# <a name="configure-a-sharepoint-channel"></a>SharePoint-kanavan konfiguroiminen

[!include [banner](../includes/banner.md)]

Ennen kuin määrität Microsoft SharePoint -kanavan käsittelemään saapuvat tiedostot, noudata kohdassa [SharePoint-yhteyden konfiguroiminen](e-invoicing-create-sharepoint-connection.md) kuvattuja vaiheita.

Tämän jälkeen voit käyttää SharePoint-kanavaa sähköisten toimittajalaskujen tuomiseen SharePoint-kansioihin tallennetuista tiedostoista.

1. Luo SharePoint-sivustossasi seuraavat kansiot:

    - **Pääkansio** – Kansio, jonka tiedostoja palvelu käsittelee.
    - **Arkistokansio** – Kansio, johon käsitellyt tiedostot tallennetaan.
    - **Virhekansio** – Kansio, johon järjestelmä siirtää tiedostot, jos käsittely epäonnistuu.

2. Valitse Regulatory Configuration Servicesissä (RCS) luomasi sähköisen laskutuksen ominaisuus. Varmista, että valittavan version tila on **Luonnos**.
3. Valitse **Määritykset**-välilehdessä **Lisää**.
4. Valitse avattavan **Toimintoasetusten luonti** -valintaikkunan **Uusi** kenttäryhmässä **Mukautettu määritys** -vaihtoehto.
5. Valitse **Määrityksen tyyppi** -kenttäryhmässä **Tietokanava**-vaihtoehto.
6. Valitse **SharePoint-kansio** **Valitse tietokanava** -kentästä.
7. Valitse **Luo**.
8. Valitse aiemmin luomasi rivi ja valitse sitten **Muokkaa**.
9. Määritä **Tietokanava**-välilehden **Parametrit**-osassa seuraavat pakolliset kentät.

    | Kenttä                 | Kuvaus |
    |-----------------------|-------------|
    | Tietokanava          | Syötä tietokanavan yksilöivä nimi. Nimen enimmäispituus on 10 merkkiä. Siihen viitataan käytettävyyssäännöissä ja liitetyissä sovelluksissa viestintäprosessin aikana. |
    | SharePoint-osoite    | Kirjoita SharePoint URL. Syötä arvoksi esimerkiksi `<domain>.sharepoint.com`. |
    | Sovelluksen tunnus        | Anna sen Azure-avainsäilön salaisen koodi nimi, joka sisältää SharePoint-käyttäjätilin tunnuksen. Salaisen koodin täytyy olla luotu Key Vaultissa ja määritetty palveluympäristössäsi. Arvo on **Sovelluksen (asiakasohjelman) tunnus** -arvo [SharePoint-yhteyden määrittäminen](e-invoicing-create-sharepoint-connection.md) -kohdasta. |
    | Sovelluksen salauskoodi    | Anna sen avainsäilön salaisen koodi nimi, joka sisältää SharePoint-käyttäjätilin salasanan. Arvo on **Sovellusrekisteröinnin salainen koodi** -arvo [SharePoint-yhteyden määrittäminen](e-invoicing-create-sharepoint-connection.md) -kohdasta. |
    | Sivuston nimi             | Anna SharePoint-sivuston nimi. |
    | Asiakirjakirjaston nimi | Syötä SharePoint-tiedostokirjaston nimi. |
    | Aikakatkaisu               | Määritä millisekunteina (ms) enimmäisaika, jonka järjestelmän on odotettava vastausta. Oletusarvo on 10 000 ms (10 sekuntia). |
    | Pääkansio           | Määritä tiedoston tuontilähde tai kansio, josta palvelu käsittelee tiedostot. |
    | Arkistokansio        | Määritä kansio, johon käsitellyt tiedostot tallennetaan. |
    | Virhekansio          | Määritä kansio, johon järjestelmä siirtää tiedostot, jos käsittely epäonnistuu. |
    | Tiedoston enimmäiskoko         | Kirjoita käsiteltävän tiedoston enimmäiskoko tavuina. Oletusarvo on 20 000 000 tavua. |
    | Tiedostojen enimmäismäärä      | Määritä yksittäistä toimintoa varten käsiteltävien tiedostojen enimmäismäärä. Jos et halua rajoittaa tiedostojen määrää, määritä arvoksi **0** (nolla). |
    | Tiedostosuodatin           | Syötä merkkijono, jonka avulla suodatetaan tiedostonimen perusteella. Tämä kenttä ei ole pakollinen. Yksinkertaista muotoa, kuten **\*smth\*.ext**, tuetaan, jossa kukin tähti (\*) edustaa nollaa tai useampaa merkkiä. Määritä esimerkiksi kanava PDF-tiedostojen lukua varten kirjoittamalla **\*.pdf**. |
    | Mukautetun tiedoston nimi      | Anna mukautettu tiedostonimi asiakasohjelmasta. |

10. Tarkista ja päivitä ehdot tarvittaessa **Soveltuvuussäännöt**-välilehdessä. **Kanava**-kentän arvon on oltava sama kuin arvo, jonka olet kirjoittanut **Tietokanava**-kenttään edellisessä vaiheessa.
11. Valitse **Tallenna** ja sulje sivu.
