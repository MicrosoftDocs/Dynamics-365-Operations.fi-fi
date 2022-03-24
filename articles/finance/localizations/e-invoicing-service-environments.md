---
title: Palveluympäristöt
description: Tässä ohjeaiheessa on tietoja sähköisen laskutuksen palveluympäristöistä ja siitä, miten ne määritetään.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a8a135098f71e1413cd20ff8ad4003f090ae3407
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371670"
---
# <a name="service-environments"></a>Palveluympäristöt

[!include [banner](../includes/banner.md)]

Palveluympäristöt ovat loogisia osioita, jotka luodaan sähköisen laskutuksen globalisaatio-ominaisuuksien tukemiseksi sekä sähköisessä laskutuspalvelussa käsiteltävien asiakirjojen tukemiseksi. Suojauksen salasanat ja digitaaliset varmenteet sekä käyttöoikeudet (hallinto) on määritettävä palveluympäristön tasolla.

Voit luoda tarvitsemasi määrän palveluympäristöjä. Kaikki luomasi palveluympäristöt ovat toisistaan riippumattomia. Suosittelemme ainakin kahden palveluympäristön luontia parhaan käytännön mukaisesti:

- Yksi ympäristö kehityksen ja oikeellisuustarkistuksen tarkoituksia varten. Tämä ympäristö on tavallisesti käyttäjien hyväksyntätestausta (UAT) varten.
- Yksi ympäristö tuotantotarkoituksia varten. Tämä ympäristö on tavallisesti tuotantoympäristö.

Tämäntyyppinen osiointi auttaa varmistamaan, että sähköisen laskutuksen prosessit tarkistetaan ja niitä mukautetaan eristysympäristössä ennen kuin ne tulevat tuotantoon.

Palveluympäristöt on luotava ja ylläpidettävä Regulatory Configuration Service (RCS) -palvelussa. Kun ne ovat valmiita, ne pitää julkaista sähköiseen laskutuspalveluun. Julkaisuprosessi lähettää palveluympäristön parametrit RCS-instanssista sähköisen laskutuksen palveluun.

Jos julkaisuprosessia ei suoriteta uuden palveluympäristön luomisen tai aiemmin luodun palveluympäristön muokkaamisen (esimerkiksi käyttäjien tai Microsoft Azure Key Vault -salaisuuksien lisääminen tai poistaminen) jälkeen, muutokset eivät tule voimaan. Vain julkaisuja ympäristöjä voi käyttää Dynamics 365 Financesta tai Dynamics 365 Supply Chain Managementista.

## <a name="service-environment-statuses"></a>Palveluympäristön tilat

Palveluympäristöjä voidaan hallita niiden tilojen kautta. Voit tarkastella ympäristön tilaa **Palveluympäristöt**-sivulla. Seuraavat tilat ovat käytettävissä:

- **Ei julkaistu** – Ympäristö on luotu, mutta sitä ei ole vielä julkaistu.
- **Julkaistu** – Ympäristö on julkaistu sähköisen laskutuksen palvelussa.
- **Muutettu** – Julkaistun ympäristön määritteitä on muutettu, mutta muutoksia ei ole vielä julkaistu.

## <a name="users"></a>Käyttäjät

Jokaisessa palveluympäristössä on oltava luettelo käyttäjistä, jotka voivat muodostaa yhteyden sähköiseen laskutukseen Financesta tai Supply Chain Managementista.

## <a name="applications"></a>Hakemukset

Joissakin tilanteissa muiden sovellusten kuin Financen tai Supply Chain Managementin on ehkä oltava yhteydessä sähköiseen laskutuspalveluun sähköisten tiedostojen lähettämistä varten jatkokäsittelyä varten tai esimerkiksi tiedoston lähetystilan hakemiseen. Näissä tilanteissa sovellus on määritettävä sovellusluettelossa. Näin se voi käyttää sähköistä laskutuspalvelua. Sovellus on rekisteröitävä myös sovelluksena Azure Active Directoryssa (Azure AD), ja sen tunnistamisessa on käytettävä objektitunnusta. 

Koska Microsoft edellyttää sovellusten korkeaa suojaustasoa sovelluksille, jotka voivat muodostaa yhteyden sähköiseen laskutuspalveluun, ota yhteyttä Microsoftiin osoitteeseen <DGXRegulatoryservicesengineering@service.microsoft.com> ja anna seuraavat sovelluksesi tiedot:

- Azure AD -vuokraajan tunnus
- Microsoft Dynamics Lifecycle Services (LCS) -ympäristön tunnus
- Sovelluksen tunnus (asiakasohjelman tunnus)
- Objektin tunnus
- Perustelu ja sovelluksen korkean tason kuvaus

Microsoft arvioi pyynnön ja rekisteröi sovelluksen suojausrekisteriin varmistaakseen, että se voi käyttää sähköistä laskutusta.

## <a name="number-sequences"></a>Numerosarjat

Jos skenaariot edellyttävät numerosarjoja (esimerkiksi tiedostonimissä), voit käyttää tietylle ympäristölle määritettyjä numerosarjoja, mutta niitä voidaan käyttää joko globalisointiominaisuuksien välillä tai tietylle globalisointiominaisuudelle. Kun numerosarja on määritetty, sitä voi käyttää muuttujissa ja käsittelyputkissa. Voit seurata sen käyttöä etsien **Numerosarjat**-sivulla, etsiä **Käytössä**-parametrille **Nykyinen**-arvon.

### <a name="working-with-number-sequences"></a>Numerosarjojen käyttö
**Numerosarjat**-sivulla: 

- Luo numerosarja valitsemalla **Uusi**. Kirjoita sitten nimi ja kuvaus. 
- Valitse **Poista**, jos haluat poistaa numerosarjan, jos sitä ei enää käytetä.
- Muutoksia numerosarjaan ei tarvitse julkaista valitsemalla toimintoruudussa **Julkaise**. Päivitys tehdään automaattisesti.

## <a name="create-a-key-vault-reference"></a>Avainsäilöviitteen luominen

1. Kirjaudu RCS-tilille.
2. Valitse **Globalisaatio-ominaisuudet**-työtilan **Ympäristö**-osassa **Sähköinen laskutus** -ruutu.
3. Valitse **Ympäristön määritys** -sivun toimintoruudusta **Palveluympäristöt**.
4. Valitse **Palveluympäristöt**-sivun toimintoruudusta **Key Vault -parametrit**.
5. Luo **Avainsäilöparametrit**-sivulla avainsäilön viite valitsemalla **Uusi**.
6. Syötä **Nimi**-kenttään avainsäilön viitteen nimi.
7. Syötä **Kuvaus**-kenttään kuvaus.
8. Liitä **Key Vault – URI** -kenttään Key Vault - URI -arvo avainsäilöstä (`https://<your key vault>.vault.azure.net/`). Lisätietoja: [Azure Key Vaultin luominen Azure-portaalissa](e-invoicing-create-azure-key-vault-azure-portal.md).
9. Valitse **Tallenna**.
    
## <a name="create-a-secret-for-the-storage-account-secret-token"></a>Luo salaisuus tallennustilin salaiselle tunnukselle

1. Valitse **Key Vault -parametrit** -sivulla edellisessä menetelmässä luomasi Key Vault -viite, ja valitse sitten **Varmenteet**-osasta **Lisää**.
2. Syötä **Nimi**-kenttään tallennustilin salaisen koodin nimi. Nimen tulisi olla sama kuin avainsäilön salaisuuden, joka sisältää tallennustilan jaetun käyttöoikeuden allekirjoituksen (SAS) tunnuksen. Lisätietoja: [Azure-tallennustilin luominen Azure-portaalissa](e-invoicing-create-azure-storage-account-azure-portal.md). 
3. Syötä **Kuvaus**-kenttään kuvaus.
4. Kirjoita **Tyyppi**-kenttään **Salainen koodi**.
5. Valitse **Tallenna**.
    
## <a name="create-a-service-environment"></a>Palveluympäristön luominen

1. Luo uusi palveluympäristö valitsemalla **Palveluympäristöt**-sivulla **Uusi**.
2. Syötä **Nimi**-kenttään sähköisen laskutuksen ympäristön nimi.
3. Syötä **Kuvaus**-kenttään kuvaus.
4. Valitse **Tallennutilin SAS-tunnuksen salasana** -kentässä sen tallennustilin varmenteen nimi, jota on käytettävä tallennustiliin todentautumisessa.
5. Valitse **Käyttäjät**-osassa **Lisää**, kun haluat lisätä käyttäjän, joka voi lähettää sähköisiä laskuja ympäristön kautta sekä muodostaa yhteyden tallennustiliin.
6. Kirjoita **Käyttäjätunnus**-kenttään käyttäjän alias. 
7. Kirjoita **Sähköpostiosoite**-kenttään käyttäjän sähköpostiosoite.
8. Valitse **Tallenna**.
9. Julkaise ympäristö sähköiseen laskutuspalveluun valitsemalla toimintoruudussa **Julkaise**. Vahvista, että **Tila**-kentän arvoksi tulee **Julkaistu**.