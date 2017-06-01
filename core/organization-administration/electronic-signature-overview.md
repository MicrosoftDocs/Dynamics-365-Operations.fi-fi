---
title: "Sähköisten allekirjoitusten yleiskuvaus"
description: "Tässä artikkelissa on yleiskatsaus sähköisistä allekirjoituksista ja niiden käyttämisestä Microsoft Dynamics 365 for Operations -järjestelmässä."
author: maertenm
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5adf45769657e4da81af00b2114a2c1a98655207
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="electronic-signature-overview"></a>Sähköisten allekirjoitusten yleiskuvaus

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on yleiskatsaus sähköisistä allekirjoituksista ja niiden käyttämisestä Microsoft Dynamics 365 for Operations -järjestelmässä.

<a name="what-is-an-electronic-signature"></a>Mikä on sähköinen allekirjoitus?
--------------------------------

Sähköisellä allekirjoituksella vahvistetaan uuden tietojenkäsittelyprosessin aloittavan tai prosessin hyväksynnän aloittavan henkilön henkilöllisyys. Joillakin aloilla sähköinen allekirjoitus on juridisesti yhtä sitova kuin käsin kirjoitettu. Sähköiset allekirjoitukset ovat pakollisia useilla säännöin ja määräyksin säädellyillä aloilla, kuten lääketeollisuudessa, elintarviketeollisuudessa sekä ilmailu- ja maanpuolustusteollisuudessa. Niiden käyttämistä edellyttää myös Yhdysvaltain elintarvike- ja lääkeviranomaisen (FDA) määräys 21 CFR Part 11. **Huomautus:** Sähköinen allekirjoitus ei ole sama kuin digitaalinen allekirjoitus. Sähköinen allekirjoitus on yksinkertaisesti käsin kirjoitetun allekirjoituksen korvike, kun taas digitaalinen allekirjoitus sisältää lisäsuojaustoimenpiteitä. Digitaalisen allekirjoituksen avulla voi tunnistaa, onko toinen käyttäjä tai prosessi peukaloinut tietoja. Digitaalisen allekirjoituksen voi myös vahvistaa, eikä tietojen allekirjoittamiseen käytetyn sertifikaatin omistaja voi kumota tätä vahvistusta. Kuten alla on kuvattu, Microsoft Dynamics 365 for Operations -järjestelmän sähköisissä allekirjoituksissa on sisäinen digitaalisten allekirjoitusten toiminto.

## <a name="electronic-signatures-in-dynamics-365-for-operations"></a>Sähköiset allekirjoitukset Microsoft 365 for Operations -järjestelmässä
Microsoft Dynamics 365 for Operations -järjestelmässä voit käyttää sähköisiä allekirjoituksia tärkeissä liiketoimintaprosesseissa. Joissakin prosesseissa on sisäinen sähköisten allekirjoitusten toiminto. Voit myös luoda mukautettuja allekirjoitusvaatimuksia mille tahansa tietokannan taululle ja kentälle. Sähköisissä allekirjoituksissa on sisäinen digitaalisten allekirjoitusten toiminto. Jokaisen tiedostoja allekirjoittavan käyttäjän on hankittava voimassa oleva salaussertifikaatti. Kun tiedosto allekirjoitetaan, tähän sertifikaattiin liittyvä yksityinen avain vahvistetaan. Dynamics 365 for Operations kirjaa sähköisten allekirjoitusten tiedot lokiin kirjausketjua varten. Lisätietoja sähköisistä allekirjoituksista on artikkelissa [Määritä sähköiset allekirjoitukset (ohjattu tehtävä)](http://ax.help.dynamics.com/en/wiki/set-up-electronic-signatures/).

## <a name="users-who-require-access-to-electronic-signatures"></a>Käyttäjät, joiden on voitava käyttää sähköisiä allekirjoituksia
Kolmenlaiset käyttäjät tarvitsevat tavallisesti pääsyn sähköisiin allekirjoituksiin: sähköisten allekirjoitusten järjestelmänvalvojat, allekirjoittajat ja sähköisten allekirjoitusten tarkastajat.

### <a name="electronic-signature-administrator"></a>Sähköisten allekirjoitusten järjestelmänvalvoja

Sähköisten allekirjoitusten järjestelmänvalvoja määrittää allekirjoitusvaatimukset, yleisparametrit ja hyväksyjät sekä saa hälytyksiä, kun allekirjoituksia ei voida vahvistaa. Oletusarvon mukaan **Tietotekniikkapäällikkö**-käyttöoikeusrooliin kuuluvalla käyttäjällä on sähköisten allekirjoitusten hallintaoikeudet.

### <a name="signer"></a>Allekirjoittaja

Allekirjoittaja antaa sähköisiä allekirjoituksia tiedostoihin ja prosesseihin, joissa allekirjoituksia vaaditaan. Oletusarvon mukaan **Järjestelmän käyttäjä** -käyttöoikeusrooliin kuuluvalla käyttäjällä on oikeus allekirjoittaa asiakirjoja sähköisesti. **Huomautus:** Allekirjoittaja saattaa tarvita lisäkäyttöoikeuksia, ennen kuin hänelle myönnetään allekirjoitettavaan tiedoston tai prosessiin liittyvien tietojen käyttöoikeus. Käyttäjällä, joka tekee muutoksia tietoihin ja jonka on sitten allekirjoitettava nämä muutokset, on oltava oikeus muuttaa tietoja. Käyttäjä, joka allekirjoittaa toisen käyttäjän puolesta, ei ehkä tarvitse pääsyä tietoihin. Esimerkki tällaisesta käyttäjästä on esimies, joka allekirjoittaa työntekijän muutokset.

### <a name="electronic-signature-auditor"></a>Sähköisten allekirjoitusten tarkastaja

Sähköisten allekirjoitusten tarkastaja tarkistaa tietokantalokin sekä allekirjoituksen tarkistuslokin, jota voi käyttää tietokantalokista. Oletusarvon mukaan **Tietotekniikkapäällikkö**-käyttöoikeusrooliin kuuluvalla käyttäjällä on sähköisten allekirjoitusten tarkistusoikeudet. Jos käytät muuta kuin **Tietotekniikkapäällikkö**-roolia, varmista, että roolille on määritelty seuraavat oikeudet:

-   Tarkastele sähköisen allekirjoituksen virheitä
-   Tarkastele tietokantalokia

## <a name="signing-documents-electronically"></a>Asiakirjojen allekirjoittaminen sähköisesti
### <a name="get-a-certificate"></a>Sertifikaatin hakeminen

Sinun on pyydettävä sertifikaatti ennen tiedostojen sähköistä allekirjoitusta Dynamics 365 for Operations -järjestelmässä. **Huomautus:** Dynamics 365 for Operations käyttää Microsoft SQL Serverin ominaisuuksia sertifikaattien luomiseen ja sähköisten allekirjoitusten käyttöönottoon. Muuta sertifikaattia tai julkisen avaimen infrastruktuuria ei tarvita. Kun pyydät sertifikaattia, sinulle luodaan julkinen avain ja yksityinen avain Dynamics 365 for Operations .
-tietokantaan. Yksityinen avain salataan vain sinun tuntemallasi salasanalla. Kun allekirjoitat tiedoston sähköisesti, henkilöllisyytesi tarkistetaan kirjoittaessasi salasanan. Pyydä sertifikaatti valitsemalla **Asetukset**-sivun **Tilit**-välilehdessä **Hanki sertifikaatti**. Kirjoita ja vahvista salasana, jota käytät allekirjoittamiseen. Salasanalla suojataan yksityistä avaintasi ja hyväksytään sertifikaattisi käyttö. Tätä salasanaa ei tallenneta tietokantaan eikä se ole kenenkään muun käytettävissä – ei edes Dynamics 365 for Operations -järjestelmänvalvojan. Jos unohdat sertifikaattiisi liittyvän salasanan, sertifikaatti on vaihdettava. Jos vaihdat sertifikaatin, se ei vaikuta aiemmalla sertifikaatilla allekirjoitettuihin asiakirjoihin. Voit vaihtaa sertifikaatin valitsemalla **Asetukset** -sivulla **Palauta sertifikaatti**.

### <a name="sign-a-document-electronically"></a>Asiakirjan allekirjoittaminen sähköisesti

**Allekirjoita tiedosto** -sivu avautuu, kun teet sähköistä allekirjoitusta edellyttävän muutoksen.

1.  Tarkista tiedoston muutokset valitsemalla **Allekirjoita tiedosto** -sivulla **Tiedosto**-välilehti.
2.  Valitse syykoodi **Allekirjoitus**-välilehdestä.
3.  Kirjoita kommentti, jos se on pakollinen.
4.  Jos käyttäjätunnuksesi ei näy **Allekirjoittaja**-kentässä, valitse se luettelossa.
5.  Anna sijaintisi, jos tämä tieto on pakollinen.
6.  Napsauta **OK**.

### <a name="sign-for-another-users-changes"></a>Kirjaa toisen käyttäjän muutokset

Joskus voi olla tarpeen, että käyttäjä allekirjoittaa toisen käyttäjän muutokset. Esimerkiksi esimiehen on joskus allekirjoitettava työntekijän tuoterakenteeseen tekemät muutokset. Tällä menetelmällä voit määrittää Dynamics 365 for Operations -käyttäjän allekirjoittajaksi, joka tekee allekirjoitukset toisen käyttäjän puolesta. **Huomautukset:** Kun käyttäjä allekirjoittaa toisen käyttäjän muutoksen, allekirjoitus on tehtävä muutoksen tehneen käyttäjän työasemassa. Käyttäjä ei voi tallentaa muutosta, ennen kuin allekirjoitus on annettu. Määritä hyväksyjät seuraavasti.

1.  Valitse **Asetukset**-sivun **Tilit**-välilehdessä **Määritä hyväksyjä**.
2.  Valitse sen käyttäjän tunnus, jonka on allekirjoitettava toisen käyttäjän muutokset **Hyväksyjän käyttäjätunnus** -kentässä.
3.  Valitse sen käyttäjän tunnus, jonka muutokset on allekirjoitettava **Käyttäjätunnus, jonka puolesta allekirjoitetaan** -kentässä.





