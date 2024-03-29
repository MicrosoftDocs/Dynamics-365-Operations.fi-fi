---
title: Määritä pankkitilin täsmäytyksen lisätoimintojen tuontiprosessi
description: Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Microsoft Dynamics 365 Financessa. Tässä artikkelissa käsitellään tiliotteiden tuontitoimintoa.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60195962e50817b4d85840a2464848db6e666f46
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716015"
---
# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Määritä pankkitilin täsmäytyksen lisätoimintojen tuontiprosessi

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Tämä toiminto vanhentuu syyskuussa 2022, joten uusien käyttäjien kannattaa käyttää sähköistä raportointia. Lisätietoa on kohdassa [Pankkitilin täsmäytyksen tuonnin lisätoimintojen määrittäminen sähköisen raportoinnin avulla](../accounts-payable/import-bai2-er.md).


Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Dynamics 365 Financessa. Tässä artikkelissa käsitellään tiliotteiden tuontitoimintoa. 

Tiliotteen tuontiasetukset vaihtelevat sähköisen tiliotteen muodon mukaan. Finance tukee heti kolmea tiliotemuotoa, jotka ovat ISO20022, MT940 ja BAI2.

## <a name="set-time-zone-preference"></a>Aikavyöhykeasetuksen määrittäminen
Kun määrität tiliotteiden tuontiasetukset, voi olla tärkeää ottaa päivämäärä/aika-tietojen aikavyöhyke huomioon tuotavissa tiliotetiedostoissa. Kaikkien päivämäärä- ja aika-arvojen oletetaan oletusarvoisesti olevan Coordinated Universal Time (UTC) -aikavyöhykkeen mukaisia, joten aikavyöhykettä ei muuteta, kun tuot tietoja. 

Käytettävissä on vaihtoehto, jolla voit määrittää tietojen tuonnissa käytettävän aikavyöhykkeen. Tämä vaihtoehto on käytettävissä **Aikavyöhykeasetus**-kentässä kaikilla **lähdetietojen muotojen tietojen** sivuilla (**Tietojen hallinnan työtila > Määritä tietolähteet > Valitse tietojen muoto > Alueasetukset**-pikavälilehti). Syöttämäsi aikavyöhykeasetus koskee kaikkia tuonteja, jotka käyttävät kyseistä lähdetietojen muotoa. Voit luoda niin monta tietolähteen muotoa kuin tarvitset tietojen tuomiseen useista aikavyöhykkeistä.  

Tämä aikavyöhyke ei välttämättä ole sama kuin käyttäjän tai yrityksen aikavyöhyke, joten muista selvittää, mitä aikavyöhykettä päivämäärä- ja aikatiedot käyttävät. Suosittelemme ottamaan huomioon seuraavat seikat, kun määrität aikavyöhykeasetuksia. 

 - Aikavyöhykeasetus koskee kaikkia tuonteja, jotka käyttävät kyseistä lähdetietojen muotoa. Voit luoda niin monta tietolähteen muotoa kuin tarvitset tietojen tuonnin käsittelemiseen useista aikavyöhykkeistä. 
 
 - Aikavyöhykeasetuksen tulisi olla tuontitiedostossa olevien päivämäärä- ja aikatietojen paikallinen aikavyöhyke. 
 
 - Päivämäärä- ja aikatietojen aikavyöhyke ei välttämättä ole sama kuin käyttäjän tai yrityksen aikavyöhyke.
 
 - Käyttäjät voivat muokata omaa aikavyöhykettään **Käyttäjän asetukset** -sivultaan.

Huomaa, että seuraavat toimenpiteet voivat auttaa vähentämään päivämäärien ja aikojen ristiriitoja, kun tuot tiliotteita. 

 - Vältä sellaisten pankkitilien aikavyöhykeasetusten muuttamista, joihin on jo tuotu tiliotteita. Aikavyöhykeasetuksen muuttaminen voi vaikuttaa uusien tiliotteiden järjestykseen suhteessa olemassa oleviin tiliotteisiin aikavyöhykkeen säädön vuoksi. 
 
 - Tarkasta kaikki tuonnit, jotka käyttävät valittua tietolähteen muotoa. Muodolle määritetty aikavyöhykeasetus koskee kaikkia tuontiprojekteja, jotka käyttävät kyseistä muotoa. Varmista, että aikavyöhykeasetus on määritetty oikein kaikille tuontiprojekteille, jotka käyttävät kyseistä muotoa.

## <a name="sample-files"></a>Mallitiedostot
Tarvitset kaikkia kolmea muotoa varten tiedostot, jotka kääntävät sähköisen tiliotteen alkuperäisestä muodosta muotoon, jota Finance voi käyttää. Tarvittavat resurssitiedostot sijaitsevat Microsoft Visual Studion Application Explorerin **Resurssit**-solmussa. Kun olet löytänyt tiedot, kopioi ne yhteen tunnettuun sijaintiin, sillä silloin ne on helpompi ladata palvelimeen määritysprosessin aikana.

| Resurssin nimi                                           | Tiedostonimi                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_to\_Composite\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Esimerkkejä tiliotteiden muodoista ja teknisistä asetteluista
Alla on esimerkkejä tuonnin lisäasetuksia pankkitilin täsmäytystietojen tuontitiedoston teknisistä asettelumäärityksistä sekä kolme esimerkkitiliotetiedostoa: [Tuontitiedoston esimerkit](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Tekninen asettelumääritys                             | Esimerkkitiliotetiedosto          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |



## <a name="set-up-the-import-of-iso20022-bank-statements"></a>Määritä ISO20022-tiliotteiden tuonti
Määritä ensin ISO20022-tiliotteiden tiliotemuodon käsittelyryhmä käyttämällä tietoyksikkökehystä.

1.  Valitse **Työtilat** &gt; **Tietojen hallinta**.
2.  Valitse **Tuo**.
3.  Anna muodolle nimi, kuten **ISO20022**.
4.  Valitse **Lähdetietojen muoto**-kenttään **XML-elementti**.
5.  Valitse **Yksikön nimi** -kenttään **Tiliotteet**.
6.  Voit ladata tuontitiedostot valitsemalla **Lataa palvelimeen** ja siirtymällä sitten aiemmin tallentamaasi **SampleBankCompositeEntity.xml**-tiedostoon.
7.  Kun Tiliotteet-yksikkö on ladattu ja yhdistämismääritykset ovat valmiit, valitse yksikölle **Näytä yhdistämismääritykset** -toiminto.
8.  Tiliotteet-yksikkö on neljästä eri yksiköstä koostuva yhdistelmäyksikkö. Valitse luettelossa ensin **BankStatementDocumentEntity** ja sitten **Näytä yhdistämismääritykset** -toiminto.
9.  Valitse **Muunnokset**-välilehdessä **Uusi**.
10. Valitse järjestysnumerolle 1 ensin **Lataa tiedosto palvelimeen** ja sitten aiemmin tallentamasi **ISO20022XML-to-Reconciliation.xslt**-tiedosto. **Huomautus:** Muunnostiedostot ovat vakiomuotoisia. Koska pankit poikkeavat usein tästä muodosta, sinun on päivitettävä tiliotemuotoon yhdistämismääritettävä muunnostiedosto. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. Valitse **Uusi**.
12. Valitse järjestysnumerolle 2 ensin **Lataa tiedosto palvelimeen** ja sitten aiemmin tallentamasi **BankReconciliation-to-Composite.xslt**-tiedosto.
13. Valitse **Käytä muunnoksia**.

Kun muodon käsittelyryhmä on määritetty, seuraavana vaiheena on ISO20022-tiliotteiden tiliotemuodon sääntöjen määrittäminen.

1.  Valitse **Maksuliikenteen hallinta** &gt; **Asetukset** &gt; **Pankkitilin täsmäytyksen lisätoimintojen asetukset** &gt; **Tiliotteen muotoilu**.
2.  Valitse **Uusi**.
3.  Määritä tiliotteen muotoilu, kuten **ISO20022**.
4.  Kirjoita muotoilun nimi.
5.  Määritä **Käsittelyryhmä**-kenttä aiemmin määrittämällesi ryhmälle, kuten **ISO20022**.
6.  Valitse **XML-tiedosto**-valintaruutu.

Viimeinen vaihe on pankkitilin täsmäytyksen lisätoimintojen ottaminen käyttöön ja määritä pankkitilin tiliotteen muotoilu.

1.  Siirry kohtaan **Maksuliikenteen hallinta** &gt; **Pankkitilit**.
2.  Valitse pankkitili ja avaa se, jolloin tiedot tulevat näkyviin.
3.  Valitse **Täsmäytys**-välilehdessä **Pankkitilin täsmäytyksen lisätoiminnot**-asetukseksi **Kyllä**.
4.  Määritä **Tiliotteen muotoilu**-kenttä aiemmin luomallesi muotoilulle, kuten **ISO20022**.

## <a name="set-up-the-import-of-mt940-bank-statements"></a>Määritä MT940-tiliotteiden tuonti
Määritä ensin MT940-tiliotteiden tiliotemuodon käsittelyryhmä käyttämällä tietoyksikkökehystä.

1.  Valitse **Työtilat** &gt; **Tietojen hallinta**.
2.  Valitse **Tuo**.
3.  Anna muodolle nimi, kuten **MT940**.
4.  Valitse **Lähdetietojen muoto** -kenttään **XML-elementti**.
5.  Valitse **Yksikön nimi** -kenttään **Tiliotteet**.
6.  Voit ladata tuontitiedostot valitsemalla **Lataa palvelimeen** ja siirtymällä sitten aiemmin tallentamaasi **SampleBankCompositeEntity.xml**-tiedostoon.
7.  Kun Tiliotteet-yksikkö on ladattu ja yhdistämismääritykset ovat valmiit, valitse yksikölle **Näytä yhdistämismääritykset** -toiminto.
8.  Tiliotteet-yksikkö on neljästä eri yksiköstä koostuva yhdistelmäyksikkö. Valitse luettelossa ensin **BankStatementDocumentEntity** ja sitten **Näytä yhdistämismääritykset** -toiminto.
9.  Valitse **Muunnokset**-välilehdessä **Uusi**.
10. Valitse järjestysnumerolle 1 ensin **Lataa tiedosto palvelimeen** ja sitten aiemmin tallentamasi **MT940TXT-to-MT940XML.xslt**-tiedosto.
11. Valitse **Uusi**.
12. Valitse järjestysnumerolle 2 ensin **Lataa tiedosto palvelimeen** ja sitten aiemmin tallentamasi **MT940XML-to-Reconciliation.xslt**-tiedosto. **Huomautus:** Muunnostiedostot ovat vakiomuotoisia. Koska pankit poikkeavat usein tästä muodosta, sinun on päivitettävä tiliotemuotoon yhdistämismääritettävä muunnostiedosto. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. Valitse **Uusi**.
14. Valitse järjestysnumerolle 3 ensin **Lataa tiedosto palvelimeen** ja sitten aiemmin tallentamasi **BankReconciliation-to-Composite.xslt**-tiedosto.
15. Valitse **Käytä muunnoksia**.

Kun muodon käsittelyryhmä on määritetty, seuraavana vaiheena on MT940-tiliotteiden tiliotemuodon sääntöjen määrittäminen.

1.  Valitse **Maksuliikenteen hallinta** &gt; **Asetukset** &gt; **Pankkitilin täsmäytyksen lisätoimintojen asetukset** &gt; **Tiliotteen muotoilu**.
2.  Valitse **Uusi**.
3.  Määritä tiliotteen muotoilu, kuten **MT940**.
4.  Kirjoita muotoilun nimi.
5.  Määritä **Käsittelyryhmä**-kenttä aiemmin määrittämällesi ryhmälle, kuten **MT940**.
6.  Valitse **Tiedostotyyppi** -kenttään **txt**.

Viimeinen vaihe on pankkitilin täsmäytyksen lisätoimintojen ottaminen käyttöön ja määritä pankkitilin tiliotteen muotoilu.

1.  Siirry kohtaan **Maksuliikenteen hallinta** &gt; **Pankkitilit**.
2.  Valitse pankkitili ja avaa se, jolloin tiedot tulevat näkyviin.
3.  Valitse **Täsmäytys**-välilehdessä **Pankkitilin täsmäytyksen lisätoiminnot** -asetukseksi **Kyllä**.
4.  Kun sinua pyydetään vahvistamaan valintasi ja ottamaan Pankkitilin täsmäytyksen lisätoiminto käyttöön, valitse **OK**.
5.  Määritä **Tiliotteen muotoilu** -kenttä aiemmin luomallesi muotoilulle, kuten **MT940**.

## <a name="set-up-the-import-of-bai2-bank-statements"></a>Määritä BAI2-tiliotteiden tuonti
Määritä ensin BAI2-tiliotteiden tiliotemuodon käsittelyryhmä käyttämällä tietoyksikkökehystä.

1.  Valitse **Työtilat** &gt; **Tietojen hallinta**.
2.  Valitse **Tuo**.
3.  Anna muodolle nimi, kuten **BAI2**.
4.  Valitse **Lähdetietojen muoto** -kenttään **XML-elementti**.
5.  Valitse **Yksikön nimi** -kenttään **Tiliotteet**.
6.  Voit ladata tuontitiedostot valitsemalla **Lataa palvelimeen** ja siirtymällä sitten aiemmin tallentamaasi **SampleBankCompositeEntity.xml**-tiedostoon.
7.  Kun Tiliotteet-yksikkö on ladattu ja yhdistämismääritykset ovat valmiit, valitse yksikölle **Näytä yhdistämismääritykset** -toiminto.
8.  Tiliotteet-yksikkö on neljästä eri yksiköstä koostuva yhdistelmäyksikkö. Valitse luettelossa ensin **BankStatementDocumentEntity** ja sitten **Näytä yhdistämismääritykset** -toiminto.
9.  Valitse **Muunnokset**-välilehdessä **Uusi**.
10. Valitse järjestysnumerolle 1 ensin **Lataa tiedosto palvelimeen** ja sitten aiemmin tallentamasi **BAI2CSV-to-BAI2XML.xslt**-tiedosto.
11. Valitse **Uusi**.
12. Valitse järjestysnumerolle 2 ensin **Lataa tiedosto palvelimeen** ja sitten aiemmin tallentamasi **BAI2XML-to-Reconciliation.xslt**-tiedosto. **Huomautus:** Muunnostiedostot ovat vakiomuotoisia. Koska pankit poikkeavat usein tästä muodosta, sinun on päivitettävä tiliotemuotoon yhdistämismääritettävä muunnostiedosto. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. Valitse **Uusi**.
14. Valitse järjestysnumerolle 3 ensin **Lataa tiedosto palvelimeen** ja sitten aiemmin tallentamasi **BankReconciliation-to-Composite.xslt**-tiedosto.
15. Valitse **Käytä muunnoksia**.

Kun muodon käsittelyryhmä on määritetty, seuraavana vaiheena on BAI2-tiliotteiden tiliotemuodon sääntöjen määrittäminen.

1.  Valitse **Maksuliikenteen hallinta** &gt; **Asetukset** &gt; **Pankkitilin täsmäytyksen lisätoimintojen asetukset** &gt; **Tiliotteen muotoilu**.
2.  Valitse **Uusi**.
3.  Määritä tiliotteen muotoilu, kuten **BAI2**.
4.  Kirjoita muotoilun nimi.
5.  Määritä **Käsittelyryhmä**-kenttä aiemmin määrittämällesi ryhmälle, kuten **BAI2**.
6.  Valitse **Tiedostotyyppi** -kenttään **txt**.

Viimeinen vaihe on pankkitilin täsmäytyksen lisätoimintojen ottaminen käyttöön ja määritä pankkitilin tiliotteen muotoilu.

1.  Siirry kohtaan **Maksuliikenteen hallinta** &gt; **Pankkitilit**.
2.  Valitse pankkitili ja avaa se, jolloin tiedot tulevat näkyviin.
3.  Valitse **Täsmäytys**-välilehdessä **Pankkitilin täsmäytyksen lisätoiminnot** -asetukseksi **Kyllä**.
4.  Kun sinua pyydetään vahvistamaan valintasi ja ottamaan Pankkitilin täsmäytyksen lisätoiminto käyttöön, valitse **OK**.
5.  Määritä **Tiliotteen muotoilu** -kenttä aiemmin luomallesi muotoilulle, kuten **BAI2**.

## <a name="test-the-bank-statement-import"></a>Testaa tiliotteen tuonti
Viimeisessä vaiheessa testataan, että tiliotteen tuonti onnistuu.

1.  Siirry kohtaan **Maksuliikenteen hallinta** &gt; **Pankkitilit**.
2.  Valitse pankkitili, jolle Pankkitilin täsmäytyksen lisätoiminnot on otettu käyttöön.
3.  Valitse **Täsmäytä**-välilehdessä **Tiliotteet**.
4.  Valitse **Tiliotteet**-sivulla **Tuo tiliote**.
5.  Määritä **Pankkitili**-kenttä valitulle pankkitilille. **Tiliotteen muotoilu** -kenttä määritetään asetetaan automaattisesti pankkitilin asetuksen perusteella.
6.  Valitse ensin **Selaa** ja sitten sähköinen tiliotetiedosto.
7.  Valitse **Lataa palvelimeen**.
8.  Napsauta **OK**.

Jos tuonti onnistuu, avautuva sanoma ilmoittaa, että tiliote on tuotu. Jos tuonti epäonnistuu, etsi työ **Tietojen hallinta** -työtilan **Työhistoria**-kohdasta. Avaa **Suorituksen yhteenveto** -sivu valitsemalla työn **Suorituksen tiedot** ja tuo tuontivirheet näkyviin valitsemalla **Näytä suoritusloki**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
