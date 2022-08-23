---
title: Sähköpostikanavan konfiguroiminen
description: Tässä artikkelissa kerrotaan, kuinka sähköpostikanava määritetään vastaanottamaan sähköiset laskut.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 19339cbcc59e93289609690363b0dd9195a66f6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279867"
---
# <a name="configure-an-email-channel"></a>Sähköpostikanavan konfiguroiminen

[!include [banner](../includes/banner.md)]

Määritä sähköpostitilikanava, jos luotu sähköinen laskutusominaisuus tuo toimittajan sähköisiä laskuja sähköpostiin vastaanotetuista liitetiedostoista.

1. Valitse Regulatory Configuration Servicesissä (RCS) luomasi sähköisen laskutuksen ominaisuus. Varmista, että valittavan version tila on **Luonnos**.
2. Valitse **Määritykset**-välilehdessä **Lisää**.
3. Valitse avattavan **Toimintoasetusten luonti** -valintaikkunan **Uusi** kenttäryhmässä **Mukautettu määritys** -vaihtoehto.
4. Valitse **Määrityksen tyyppi** -kenttäryhmässä **Tietokanava**-vaihtoehto.
5. Kirjoita **Saapuva sähköposti** **Valitse tietokanava** -kenttään.
6. Valitse **Luo**.
7. Valitse aiemmin luomasi rivi ja valitse sitten **Muokkaa**.
8. Määritä **Tietokanava**-välilehden **Parametrit**-osassa seuraavat pakolliset kentät.

    | Kenttä                | Kuvaus |
    |----------------------|-------------|
    | Tietokanava         | Syötä tietokanavan yksilöivä nimi. Nimen enimmäispituus on 10 merkkiä. Siihen viitataan käytettävyyssäännöissä ja liitetyissä sovelluksissa viestintäprosessin aikana. |
    | Palvelimen osoite       | Kirjoita sähköpostitilin tarjoajan palvelimen osoite. Esimerkiksi palvelun `https://outlook.live.com` palvelinosoite on imap-mail.outlook.com. |
    | Palvelimen portti          | Kirjoita sähköpostipalveluntarjoajan käyttämän portin numero. Esimerkiksi palvelun `https://outlook.live.com` palvelimen portti on 993. |
    | Käyttäjänimen salainen koodi     | Anna sen Microsoft Azure -avainsäilön salaisen koodi nimi, joka sisältää sähköpostikäyttäjätilin tunnuksen. Salaisen koodin täytyy olla luotu Key Vaultissa ja määritetty palveluympäristössäsi. |
    | Käyttäjän salasanan salainen koodi | Anna sen avainsäilön salaisen koodi nimi, joka sisältää sähköpostikäyttäjätilin salasanan. |
    | Aikakatkaisu              | Millisekunteina (ms) enimmäisaika, jonka järjestelmän on odotettava vastausta. Oletusarvo on 10 000 ms (10 sekuntia). |
    | Pääkansio          | Määritä sähköpostin tuontilähde tai kansio, josta palvelu käsittelee sähköpostit. |
    | Arkistokansio       | Määritä kansio, johon käsitellyt sähköpostit tallennetaan. Jos et määritä tätä kansiota, järjestelmä luo sen automaattisesti. |
    | Virhekansio         | Määritä kansio, johon järjestelmä siirtää sähköpostit, jos käsittely epäonnistuu. Jos et määritä tätä kansiota, järjestelmä luo sen automaattisesti. |
    | Viestin enimmäiskoko     | Kirjoita yhden käsiteltävän viestin enimmäiskoko tavuina. Oletusarvo on 20 000 000 tavua. |
    | Viestien enimmäismäärä   | Määritä yksittäistä toimintoa varten käsiteltävien viestien enimmäismäärä. Jos et halua rajoittaa viestien määrää, määritä arvoksi **0** (nolla). |
    | Lähettäjäsuodatin          | Syötä merkkijono, jonka avulla suodatetaan lähettäjän osoitteen perusteella. Vain sähköpostiviestit, joissa lähettäjän osoite vastaa suodatinta, käsitellään. Tämä kenttä ei ole pakollinen. Jos haluat määrittää useita lähettäjän osoitteita, käytä puolipisteitä (;) erottimena. |
    | Aihesuodatin       | Syötä merkkijono, jonka avulla suodatetaan aiheen perusteella. Vain sähköpostiviestit, joissa aihe vastaa suodatinta, käsitellään. Tämä kenttä ei ole pakollinen. Yksinkertaista muotoa, kuten **\*smth\*.ext**, tuetaan, jossa kukin tähti (\*) edustaa nollaa tai useampaa merkkiä. |
    | Päivämääräsuodatin          | Määritä päivä, joka määrittää käsiteltyjen sanomien ikärajan päivinä. Tämä kenttä ei ole pakollinen. Oletusarvo on 30 päivää. |
    | Käsittelytila      | <p>Valitse jokin seuraavista vaihtoehdoista sen mukaan, voidaanko kaikki sähköpostiviestin liitteet käsitellä yhdessä vai käsitelläänkö jokainen liite erikseen:</p><ul><li><b>Liitekohtaisesti</b> – Kullekin sähköpostiviestin liitteelle luodaan uusi sähköinen tiedosto. Jos esimerkiksi yhdessä sähköpostiviestissä on useita tiedostoja, jotka sisältävät laskutietoja, kutakin tiedostoa käsitellään järjestelmässä uutena sähköisenä laskuna.</li><li><b>Sähköpostikohtaisesti</b> – Yhtä liitettä käsitellään perusliitteenä, ja järjestelmään luodaan yksi sähköinen lasku. Muita liitteitä voidaan käyttää tukitiedostoina.</li></ul> |

9. Lisää tiedostojen suodatustiedot **Liitesuodatin**-osassa. Vain määritetyn suodattimen täyttävät liitteet käsitellään. Esimerkiksi **\*.xml** suodattaa liitteet, joissa on tiedostonimen tunniste .xml. Liitteen nimeä käytetään määrityksen aikana Dynamics 365 Financessa tai Dynamics 365 Supply Chain Managementissa.

    - Jos määrität **Käsittelytila**-kentän arvoksi edellisessä vaiheessa **Sähköpostikohtaisesti**, voit lisätä tähän useita suodattimia. Tietty tiedosto tunnistetaan nimestä.
    - Jos määrität **Käsittelytila**-kentän arvoksi **Liitekohtaisesti**, voit lisätä vain yhden suodattimen.

10. Tarkista ja päivitä ehdot tarvittaessa **Soveltuvuussäännöt**-välilehdessä. **Kanava**-kentän arvon on oltava sama kuin arvo, jonka olet kirjoittanut **Tietokanava**-kenttään vaiheessa 8.
11. Valitse **Tallenna** ja sulje sivu.
