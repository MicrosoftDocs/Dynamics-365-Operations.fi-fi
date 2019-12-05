---
title: Parhaat käytännöt kirjauskansioyksikön avulla tapahtuvaan tositteiden tuontiin
description: Tässä ohjeaiheessa on vihjeitä tietojen tuomisesta kirjauskansioon käyttämällä kirjauskansioyksikköä.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 23a4cff85bb5c9d119f9ec47e8421aa1964a3d4f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769607"
---
# <a name="best-practices-for-importing-vouchers-by-using-the-general-journal-entity"></a>Parhaat käytännöt kirjauskansioyksikön avulla tapahtuvaan tositteiden tuontiin

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on vihjeitä tietojen tuomisesta kirjauskansioon käyttämällä kirjauskansioyksikköä.

Voit tuoda kirjauskansioyksiköllä vain tositteita, joiden tili- tai vastatilityyppinä on **Kirjanpito, Asiakas, Toimittaja tai Pankki**. Tosite voidaan lisätä yhtenä rivinä, käyttäen sekä **Tili**- että **Vastatili**-kenttiä, tai monirivisenä tositteena, jossa käytetään vain **Tili**-kenttää (**Vastatili**-kenttä jätetään tyhjäksi jokaisella rivillä). Kirjauskansioyksikkö ei tue kaikkia tilityyppejä. Sen sijaan on olemassa muita yksiköitä sellaisiin tilanteisiin, joissa on käytettävä tilityyppien yhdistelmiä. Jos haluat esimerkiksi tuoda projektitapahtuman, voit käyttää projektin kulukirjausyksikköä. Kukin yksikkö on suunniteltu tukemaan tiettyjä tilanteita, joka tarkoittaa, että kyseisiä tilanteita varten luoduissa yksiköissä voi olla lisäkenttiä, joita ei ole muita tilanteita koskevissa yksiköissä.

## <a name="setup"></a>Luo perustiedot
Tarkista ennen kirjauskansioyksikköä käyttävää tuontia seuraavat asetukset:

- **Kirjauskansion eränumeron numerosarja-asetukset** – Kun käytät tuontiin kirjanpitoyksikköä, kirjauskansion eränumero käyttää oletusarvoisesti kirjanpitoparametreissa määritettyä numerosarjaa. Jos määrität kirjauskansion eränumeron numerosarjaksi **Manuaalinen**, oletusnumeroa ei käytetä. Tätä asetusta ei tueta.
- **Taloushallinnon dimension määritykset** – Jokaisen organisaation on määritettävä taloushallinnon dimensioiden järjestys, kun tapahtumien tuontiin käytetään yksiköitä. Järjestys määritetään **Kirjanpidon dimensioiden integrointi** -muodolle valitsemalla **Kirjanpito** &gt; **Tilikartta** &gt; **Dimensiot** &gt; **Integrointisovellusten taloushallinnon dimension määritykset** &gt; **Valitse tietoyksiköt**. Tuodun kirjanpitotilin segmenttien on oltava samassa järjestyksessä. Muussa tapauksessa tapahtuu tuontivirhe.

## <a name="general-journal-entity-setup"></a>Kirjauskansioyksikön asetukset
Kaksi tietojen hallinnan asetusta vaikuttaa siihen, miten oletuskirjauskansion eränumeroa tai tositenumero käytetään:

- **Joukkoon perustuva käsittely** (tietoyksikössä)
- **Luotu automaattisesti** (kentän yhdistämismäärityksessä)

Seuraavissa osissa käsitellään näiden asetusten vaikutusta ja selvitetään, miten kirjauskansion eränumerot ja tositenumerot luodaan.

### <a name="journal-batch-number"></a>Kirjauskansion eränumero

- Kirjauskansioyksikön **Joukkoon perustuva käsittely** -asetus ei vaikuta tapaan, jolla kirjauskansion eränumerot luodaan.
- Jos **Kirjauskansion eränumero** -kentässä on valittu **Luotu automaattisesti**, jokaiselle tuodulle riville luodaan uusi kirjauskansion eränumero. Tämä menettelyä ei suositella. **Luotu automaattisesti** -asetus sijaitsee tuontiprojektin **Yhdistämistiedot**-välilehden kohdassa **Näytä yhdistämismääritykset**.
- Jos **Kirjauskansion eränumero** -kentässä ei ole valittu **Luotu automaattisesti**, kirjauskansion eränumero luodaan seuraavasti:

    - Jos tuodussa tiedostossa määritetty kirjauskansion eränumero vastaa aiemmin luotua kirjaamatonta kirjauskansiota, kaikki rivit, joilla on sama kirjauskansion eränumero, tuodaan aiemmin luotuun kirjauskansioon. Rivejä ei koskaan tuoda kirjattuun kirjauskansion eränumeroon. Sen sijaan luodaan uusi numero.
    - Jos tuodussa tiedostossa määritetty kirjauskansion eränumero ei vastaa aiemmin luotua kirjaamatonta kirjauskansiota, kaikki rivit, joilla on sama kirjauskansion eränumero, ryhmitetään uuteen kirjauskansioon. Esimerkiksi kaikki rivit, joiden kirjauskansion eränumero on 1, tuodaan uuteen kirjauskansioon, ja kaikki rivit, joiden kirjauskansion eränumero on 2, tuodaan toiseen uuteen kirjauskansioon. Kirjauskansion eränumero luodaan käyttämällä kirjanpidon parametreissa määritettyä numerosarjaa.

### <a name="voucher-number"></a>Tositenumero

- Kun käytät kirjauskansioyksikössä **Joukkoon perustuva käsittely** -asetusta, tuodun tiedoston on annettava tositenumero. Jokaiselle kirjauskansion tapahtumalle määritetään tuodusta tiedostosta saatu tositenumero, vaikka tositetta ei olisi täsmäytetty. Jos haluat käyttää joukkoon perustuvaa käsittelyä mutta haluat käyttää myös tositenumeroille määritettyä numerosarjaa, helmikuun 2016 versiossa on tätä varten hotfix-korjaus. Hotfix-korjauksen numero on 3170316, ja sen voi ladata Lifecycle Services (LCS) -palvelusta. Lisätietoja on kohdassa [Päivitysten lataaminen Lifecycle Servicesistä (LCS)](../migration-upgrade/download-hotfix-lcs.md).

    - Voit ottaa tämän toiminnon käyttöön valitsemalla siinä kirjauskansiossa, jota käytetään tuontiin, **Numeroiden kohdistus kirjauksen yhteydessä** -asetukseksi **Kyllä**.
    - Tositenumero on määritettävä edelleen tuodussa tiedostossa. Tämä numero on kuitenkin väliaikainen ja tositenumero korvaa sen, kun kirjauskansio kirjataan. Varmista, että väliaikainen tositenumero ryhmittää kirjauskansion rivit oikein. Kirjauksen aikana havaitaan esimerkiksi kolme riviä, joilla on väliaikainen tositenumero 1. Kaikkien kolmen rivin väliaikeinen tositenumero korvataan numerosarjan seuraavalla numerolla. Jos nämä kolme riviä eivät ole täsmätty vienti, tositetta ei kirjata. Jos seuraavaksi havaitaan rivejä, joiden väliaikainen tositenumero on 2, tämä numero korvataan seuraavalla numerosarjan tositenumerolla ja niin edelleen.

- Jos et käytä kirjauskansioyksikössä **Joukkoon perustuva käsittely** -asetusta, tuodussa tiedostossa ei tarvitse antaa tositenumeroa. Tositenumerot luodaan tuonnin aikana kirjauskansion asetusten mukaan (**Vain yksi tosite**, **Kun tosite täsmää** ja niin edelleen). Jos kirjauskansion asetukseksi on esimerkiksi määritetty **Kun tosite täsmää**, ensimmäinen rivi saa uuden oletusarvoisen tositenumeron. Järjestelmä sitten arvioi rivin ja määrittää, vastaavatko debet-arvot kredit-arvoja. Jos rivillä on vastatili, seuraava tuotavarivi saa uuden tositenumeron. Jos vastatiliä ei ole, järjestelmä arvioi, vastaavatko debet-arvot kredit-arvoja uutta riviä tuotaessa.
- Jos **Tositenumero**-kentän arvoksi on valittu **Luotu automaattisesti**, tuonti epäonnistuu. **Tositenumero**-kentän **Luotu automaattisesti** -asetusta ei tueta.

Kirjauskansioyksikkö käyttää oletusarvoisesti joukkoon perustuvaa käsittelyä. Kun olet arvioinut organisaation liiketoimintatavoitteet, voit muuttaa **Joukkoon perustuva käsittely** -asetusta valitsemalla **Tietoyksiköt** **Tietojen hallinta** -työtilassa. Joukkoon perustuvaa käsittelyä käytetään nopeuttamaan tuontiprosessia. Jos et käytä joukkoon perustuvaa käsittelyä, kirjauskansioyksikköä käyttävä tuonti tapahtuu hitaammin.
