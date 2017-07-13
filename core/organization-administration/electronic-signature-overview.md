---
title: "Sähköisten allekirjoitusten yleiskuvaus"
description: "Tässä artikkelissa on yleiskatsaus sähköisistä allekirjoituksista ja niiden käyttämisestä Microsoft Dynamics 365 for Finance and Operationsissa."
author: maertenm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 0cebd30a560ff033efab89c2055827b62cf31576
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017


---

# Sähköisten allekirjoitusten yleiskuvaus
<a id="electronic-signature-overview" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on yleiskatsaus sähköisistä allekirjoituksista ja niiden käyttämisestä Microsoft Dynamics 365 for Finance and Operationsissa.

Mikä on sähköinen allekirjoitus?
<a id="what-is-an-electronic-signature" class="xliff"></a>
--------------------------------

Sähköisellä allekirjoituksella vahvistetaan uuden tietojenkäsittelyprosessin aloittavan tai prosessin hyväksynnän aloittavan henkilön henkilöllisyys. Joillakin aloilla sähköinen allekirjoitus on juridisesti yhtä sitova kuin käsin kirjoitettu. Sähköiset allekirjoitukset ovat pakollisia useilla säännöin ja määräyksin säädellyillä aloilla, kuten lääketeollisuudessa, elintarviketeollisuudessa sekä ilmailu- ja maanpuolustusteollisuudessa. Niiden käyttämistä edellyttää myös Yhdysvaltain elintarvike- ja lääkeviranomaisen (FDA) määräys 21 CFR Part 11. **Huomautus:** Sähköinen allekirjoitus ei ole sama kuin digitaalinen allekirjoitus. Sähköinen allekirjoitus on yksinkertaisesti käsin kirjoitetun allekirjoituksen korvike, kun taas digitaalinen allekirjoitus sisältää lisäsuojaustoimenpiteitä. Digitaalisen allekirjoituksen avulla voi tunnistaa, onko toinen käyttäjä tai prosessi peukaloinut tietoja. Digitaalisen allekirjoituksen voi myös vahvistaa, eikä tietojen allekirjoittamiseen käytetyn sertifikaatin omistaja voi kumota tätä vahvistusta. Kuten alla on kuvattu, Microsoft Dynamics 365 for Finance and Operationsin sähköisissä allekirjoituksissa on sisäinen digitaalisten allekirjoitusten toiminto.

## Microsoft 365 for Finance and Operationsin sähköiset allekirjoitukset
<a id="electronic-signatures-in-dynamics-365-for-finance-and-operations" class="xliff"></a>
Voit käyttää Finance and Operationsissa sähköisiä allekirjoituksia tärkeissä liiketoimintaprosesseissa. Joissakin prosesseissa on sisäinen sähköisten allekirjoitusten toiminto. Voit myös luoda mukautettuja allekirjoitusvaatimuksia mille tahansa tietokannan taululle ja kentälle. Sähköisissä allekirjoituksissa on sisäinen digitaalisten allekirjoitusten toiminto. Jokaisen tiedostoja allekirjoittavan käyttäjän on hankittava voimassa oleva salaussertifikaatti. Kun tiedosto allekirjoitetaan, tähän sertifikaattiin liittyvä yksityinen avain vahvistetaan. Finance and Operations kirjaa sähköisten allekirjoitusten tiedot lokiin kirjausketjua varten. Lisätietoja sähköisistä allekirjoituksista on artikkelissa [Määritä sähköiset allekirjoitukset (ohjattu tehtävä)](http://ax.help.dynamics.com/en/wiki/set-up-electronic-signatures/).

## Käyttäjät, joiden on voitava käyttää sähköisiä allekirjoituksia
<a id="users-who-require-access-to-electronic-signatures" class="xliff"></a>
Kolmenlaiset käyttäjät tarvitsevat tavallisesti pääsyn sähköisiin allekirjoituksiin: sähköisten allekirjoitusten järjestelmänvalvojat, allekirjoittajat ja sähköisten allekirjoitusten tarkastajat.

### Sähköisten allekirjoitusten järjestelmänvalvoja
<a id="electronic-signature-administrator" class="xliff"></a>

Sähköisten allekirjoitusten järjestelmänvalvoja määrittää allekirjoitusvaatimukset, yleisparametrit ja hyväksyjät sekä saa hälytyksiä, kun allekirjoituksia ei voida vahvistaa. Oletusarvon mukaan **Tietotekniikkapäällikkö**-käyttöoikeusrooliin kuuluvalla käyttäjällä on sähköisten allekirjoitusten hallintaoikeudet.

### Allekirjoittaja
<a id="signer" class="xliff"></a>

Allekirjoittaja antaa sähköisiä allekirjoituksia tiedostoihin ja prosesseihin, joissa allekirjoituksia vaaditaan. Oletusarvon mukaan **Järjestelmän käyttäjä** -käyttöoikeusrooliin kuuluvalla käyttäjällä on oikeus allekirjoittaa asiakirjoja sähköisesti. **Huomautus:** Allekirjoittaja saattaa tarvita lisäkäyttöoikeuksia, ennen kuin hänelle myönnetään allekirjoitettavaan tiedoston tai prosessiin liittyvien tietojen käyttöoikeus. Käyttäjällä, joka tekee muutoksia tietoihin ja jonka on sitten allekirjoitettava nämä muutokset, on oltava oikeus muuttaa tietoja. Käyttäjä, joka allekirjoittaa toisen käyttäjän puolesta, ei ehkä tarvitse pääsyä tietoihin. Esimerkki tällaisesta käyttäjästä on esimies, joka allekirjoittaa työntekijän muutokset.

### Sähköisten allekirjoitusten tarkastaja
<a id="electronic-signature-auditor" class="xliff"></a>

Sähköisten allekirjoitusten tarkastaja tarkistaa tietokantalokin sekä allekirjoituksen tarkistuslokin, jota voi käyttää tietokantalokista. Oletusarvon mukaan **Tietotekniikkapäällikkö**-käyttöoikeusrooliin kuuluvalla käyttäjällä on sähköisten allekirjoitusten tarkistusoikeudet. Jos käytät muuta kuin **Tietotekniikkapäällikkö**-roolia, varmista, että roolille on määritelty seuraavat oikeudet:

-   Tarkastele sähköisen allekirjoituksen virheitä
-   Tarkastele tietokantalokia

## Asiakirjojen allekirjoittaminen sähköisesti
<a id="signing-documents-electronically" class="xliff"></a>
### Sertifikaatin hakeminen
<a id="get-a-certificate" class="xliff"></a>

Sinun on pyydettävä sertifikaatti ennen tiedostojen sähköistä allekirjoitusta Finance and Operationsissa. **Huomautus:** Finance and Operations käyttää Microsoft SQL Serverin ominaisuuksia sertifikaattien luomiseen ja sähköisten allekirjoitusten käyttöönottoon. Muuta sertifikaattia tai julkisen avaimen infrastruktuuria ei tarvita. Kun pyydät sertifikaattia, sinulle luodaan julkinen avain ja yksityinen avain Finance and Operations -tietokantaan. Yksityinen avain salataan vain sinun tuntemallasi salasanalla. Kun allekirjoitat tiedoston sähköisesti, henkilöllisyytesi tarkistetaan kirjoittaessasi salasanan. Pyydä sertifikaatti valitsemalla **Asetukset**-sivun **Tilit**-välilehdessä **Hanki sertifikaatti**. Kirjoita ja vahvista salasana, jota käytät allekirjoittamiseen. Salasanalla suojataan yksityistä avaintasi ja hyväksytään sertifikaattisi käyttö. Tätä salasanaa ei tallenneta tietokantaan eikä se ole kenenkään muun käytettävissä – ei edes Finance and Operations -järjestelmänvalvojan käytössä. Jos unohdat sertifikaattiisi liittyvän salasanan, sertifikaatti on vaihdettava. Jos vaihdat sertifikaatin, se ei vaikuta aiemmalla sertifikaatilla allekirjoitettuihin asiakirjoihin. Voit vaihtaa sertifikaatin valitsemalla **Asetukset** -sivulla **Palauta sertifikaatti**.

### Asiakirjan allekirjoittaminen sähköisesti
<a id="sign-a-document-electronically" class="xliff"></a>

**Allekirjoita tiedosto** -sivu avautuu, kun teet sähköistä allekirjoitusta edellyttävän muutoksen.

1.  Tarkista tiedoston muutokset valitsemalla **Allekirjoita tiedosto** -sivulla **Tiedosto**-välilehti.
2.  Valitse syykoodi **Allekirjoitus**-välilehdestä.
3.  Kirjoita kommentti, jos se on pakollinen.
4.  Jos käyttäjätunnuksesi ei näy **Allekirjoittaja**-kentässä, valitse se luettelossa.
5.  Anna sijaintisi, jos tämä tieto on pakollinen.
6.  Napsauta **OK**.

### Kirjaa toisen käyttäjän muutokset
<a id="sign-for-another-users-changes" class="xliff"></a>

Joskus voi olla tarpeen, että käyttäjä allekirjoittaa toisen käyttäjän muutokset. Esimerkiksi esimiehen on joskus allekirjoitettava työntekijän tuoterakenteeseen tekemät muutokset. Tällä menetelmällä voit määrittää Finance and Operations -käyttäjän allekirjoittajaksi, joka tekee allekirjoitukset toisen käyttäjän puolesta. **Huomautukset:** Kun käyttäjä allekirjoittaa toisen käyttäjän muutoksen, allekirjoitus on tehtävä muutoksen tehneen käyttäjän työasemassa. Käyttäjä ei voi tallentaa muutosta, ennen kuin allekirjoitus on annettu. Määritä hyväksyjät seuraavasti.

1.  Valitse **Asetukset**-sivun **Tilit**-välilehdessä **Määritä hyväksyjä**.
2.  Valitse sen käyttäjän tunnus, jonka on allekirjoitettava toisen käyttäjän muutokset **Hyväksyjän käyttäjätunnus** -kentässä.
3.  Valitse sen käyttäjän tunnus, jonka muutokset on allekirjoitettava **Käyttäjätunnus, jonka puolesta allekirjoitetaan** -kentässä.





