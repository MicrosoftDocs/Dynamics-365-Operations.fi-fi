---
title: ISO20022-tiedostojen tuominen
description: "Tässä ohjeaiheessa kerrotaan, miten ISO 20022 - maksutiedostojen camt.054- ja pain.002-muodot tuodaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin."
author: neserovleo
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Italy, Latvia, Lithuania, Norway, Poland, Spain, Sweden, Switzerland, United Kingdom
ms.author: v-lenest
ms.search.validFrom: 2017-06-01T00:00:00.000Z
ms.dyn365.ops.version: Enterprise edition, July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 48e280bf0a6c5db237bd389fe448c9d698d3ae12
ms.openlocfilehash: acf6ed5f503d77f372d802a51a71cec062c2b24b
ms.contentlocale: fi-fi
ms.lasthandoff: 07/25/2017

---

# <a name="import-iso20022-files"></a>ISO20022-tiedostojen tuominen

## <a name="overview"></a>Yleiskuvaus
Voit tuoda maksutiedostoja seuraavissa muodoissa:

 - **ISO20022 camt.054 -hyvitysilmoitus** – tuo saapuvat maksut tiedostosta tässä muodossa asiakkaan maksukirjauskansioon.
 - **ISO20022 pain.002 -tilapalautus** ja **ISO20022 camt.054 -veloitusilmoitus** – tuo palautustiedostot näissä muodoissa ostoreskontran maksujen siirtokirjauskansioon.

## <a name="prerequisites-for-importing-the-camt054-credit-advice-file"></a>camt.054-hyvitysilmoitustiedoston tuontiedellytykset
Pankki-ilmoitussanomien tuonti camt.054.001.002-muodossa asiakkaan maksukirjauskansioon edellyttää seuraavien toimien suorittamista.

1. Tuo sähköinen **ISO20022 camt.054** -raportointimääritys Microsoft Dynamics Lifecycle Servicesistä (LCS). Valitse sitten kyseinen määritys **Asiakkaan maksutapa** -sivun **Tuo muotokonfiguraatio** -kentässä. Lisätietoja on ohjeaiheessa [Maksutapojen tiedostomuodot](emea-select-file-formats-for-the-method-of-payments.md).
2. Anna **Kaikki asiakkaat** -sivulla kunkin asiakkaan nimi ja organisaatiotunnus.
3. Määritä **Asiakkaan pankkitili** -sivulla asiakkaan pankkitilitietue antamalla seuraavat tiedot: IBAN-numero tai pankkitilin numero sekä SWIFT-koodi tai reititysnumero.
4. Määritä **Pankkitilit** -sivulla yrityksen pankkitilit antamalla seuraavat tiedot: IBAN-numero tai pankkitilin numero, SWIFT-koodi tai reititysnumero, valuutta ja osoite.

    > [!NOTE]
    > Jos aiot käyttää pankkitilin täsmäytyksen lisätoimintoja, valitse **Täsmäytys**-pikavälilehdessä **Pankkitilin täsmäytyksen lisätoiminnot** -asetukseksi **Kyllä**. Jos aiot täsmäyttää kirjaamattomat tuodut maksut, valitset **Käytä tiliotteita sähköisten maksujen vahvistuksena** -asetukseksi **Kyllä**.

5. Valinnainen: Määritä **Tapahtumakoodin määritys** -sivulla tiedostossa olevien pankin tapahtumakoodien ja pankin tapahtumatyyppien välinen määritys.
6. Jos tiedostossa on tapahtumakuluja, jotka haluat kirjata yhdessä saapuvan maksun kanssa, luo maksulisä **Asiakkaan maksulisä** -sivulla. Liitä maksulisä sitten maksulisän asetusten **Maksutavat** -sivulla pankkitiliin.
7. Jos ESR-maksut tuodaan ja jos niissä on ISR-viitteitä (koskee sveitsiläisiä yrityksiä), tee seuraavat määritykset:

    - Anna **Asiakkaan maksut, tilin pituus** -kentässä ISR-viitteissä tai asiakkaan automaattisessa tunnistuksessa käytettävän asiakaskoodin pituus.
    - Varmista, että asiakkaan ja laskun numerossa (numerosarjassa) käytetään vain numeroita. Muiden merkkien käyttö ei ole sallittua. Laskunumerossa ei saa olla alkunollia.
    - Anna yrityksen pankkitilin ESR-, BESR- ja reititysnumero. Lisätietoja on [vanhassa ESR-ominaisuudessa](emea-che-esr-customer-payments-import.md), koska tarvittavat asetukset ovat vastaavanlaisia.
    
## <a name="import-the-camt054-credit-advice-file-into-the-customer-payment-journal"></a>camt.054-hyvitysilmoitustiedoston tuominen asiakkaan maksukirjauskansioon
1. Valitse **Asiakkaan maksukirjauskansion rivit** -sivulla **Toiminnot** > **Viitesuoritusten luku**.
2. Valitse maksutapa, jossa on ISO20022 camt.054-muodon edellyttämät asetukset.
3. Määritä tarvittavat parametrit ja tiedoston polku. Valitse sitten **OK**.

Tiedosto tuodaan.

## <a name="prerequisites-for-importing-files-in-the-pain002-status-return-and-camt054-debit-advice-formats-into-the-ap-payment-transfer-journal"></a>pain.002 -tilapalautusmuodossa ja camt.054 -veloitusilmoitusmuodossa ostoreskontran maksujen siirtokirjauskansioon tuotavien tietojen edellytykset
Seuraavat edellytykset on suoritettava, jotta pankkisanomat voidaan tuoda seuraavissa ISO20022-muodoissa **Toimittajan maksujen siirto** -sivulle: pain.002.001.003 -tilapalautussanomat ja camt.054.001.002-veloitusilmoitus.

1. Tuo ER-määritykset **ISO20022 camt.054** ja **ISO20022 pain.002** LCS:stä.
2. Valitse **Toimittajan maksutapa** -sivun **Palautusmuodon määritys**- ja **Palautusmuodon toissijainen määritys** -kentissä tuomasi ER-määritykset. Valitun maksutavan yleinen sähköinen palautusmuoto on aktivoitava.
3. Määritä **Palautusmuodon tilan yhdistämismääritys** -sivulla tilakoodin yhdistämismääritys pain.002-tilojen ja toimittajan maksukirjauskansion tilojen välille.

    Esimerkki tilamäärityksistä.

    Palautustila | Maksun tila
    --------------|---------------
    RJCT          | Hylätty
    ACCP          | Hyv.
    ACSP          | Vastaanotettu

4. Määritä **Palautusmuodon virhekoodit** -sivulla pain.002-virhekoodit ja kuvaukset ulkoisten ISO20022-tilan syykoodien mukaisesti.

    Esimerkki osasta virhekoodimääritystä:

    Koodi | Nimi
    -----|-----
    AC01 | IncorrectAccountNumber
    AC02 | InvalidDebtorAccountNumber
    AC03 | InvalidCreditorAccountNumber
    AC04 | ClosedAccountNumber
    AC05 | ClosedDebtorAccountNumber
    AC06 | BlockedAccount

5. Jos camt.054-tiedostossa on tapahtumakuluja, jotka haluat kirjata yhdessä saapuvan maksun kanssa, luo maksulisä **Toimittajan maksulisä** -sivulla. Liitä maksulisä sitten maksulisän asetusten **Maksutavat** -sivulla pankkitiliin.

## <a name="import-the-pain002-status-return-or-camt054-debit-advice-files-into-the-vendor-payment-journal"></a>pain.002-tilapalautus- tai camt.054-veloitusilmoitustiedostojen tuominen toimittajan maksukirjauskansioon
1. Avaa **Maksusiirrot**-sivu Ostoreskontra-valikossa.
2. Valitse **Maksusiirrot**-sivulla **Palautustiedosto - Toimittaja**.
3. Valitse maksutapa, jossa on ISO20022-tiedostojen edellyttämät asetukset, ja valitse **OK**.
4. Valitse ensin tuotava tiedostomuoto ja sitten **OK**.
5. Määritä tarvittavat parametrit ja tiedoston polku. Valitse sitten **OK**.

Jos olet tuomassa pain.002-tiedostoa, toimittajan maksurivien tila päivitetään tuodun tiedoston tietojen perusteella.

Jos olet tuomassa camt.054-tiedoston, määritä seuraavat lisäparametrit:

- **Maksutunnus** – Anna maksutunnus, joka määrittää uudet maksulisärivit. Nämä rivit luodaan toimittajan maksukirjauskansion rivillä, jos veloituksen summa sisältyy camt.054-tiedostoon.
- **Uusi kirjauskansio nimi** ja **Uuden kirjauskansion kuvaus** – Anna sen kirjauskansion nimi ja kuvaus, johon käsitellyt tapahtumat siirretään. Siirron jälkeen uudet tositenumerot pitäisi määrittää uudessa kirjauskansiossa.
- **Tuo suoraveloitustapahtumat** – valitse asetukseksi **Kyllä**, jos lähtevät suoraveloitukset on tuotava toimittajan maksukirjauskansioon.
- **Kirjauskansion nimi** – määritä tuotujen suoraveloitustapahtumien kirjauskansiolle uusi nimi.
- **Selvitä tapahtumat** – valitse asetukseksi **Kyllä**, jos tuodut toimittajan maksut on selvitettävä järjestelmästä löytyvien laskujen kanssa.

Voit tarkastella tuotuja tietoja **Maksutapahtumat**-sivulla. 

