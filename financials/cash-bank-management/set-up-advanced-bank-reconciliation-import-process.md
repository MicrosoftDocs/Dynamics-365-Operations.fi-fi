---
title: "Määritä pankkitilin täsmäytyksen lisätoimintojen tuontiprosessi"
description: "Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Microsoft Dynamics 365 for Operations -järjestelmässä. Tässä artikkelissa käsitellään tiliotteiden tuontitoimintoa."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eab840b2974f4e9e8cf542c146482ba8e4239079
ms.openlocfilehash: acf7bacf6e95725024ff0a542a059349593d01a0
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Määritä pankkitilin täsmäytyksen lisätoimintojen tuontiprosessi

[!include[banner](../includes/banner.md)]


Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Microsoft Dynamics 365 for Operations -järjestelmässä. Tässä artikkelissa käsitellään tiliotteiden tuontitoimintoa. 

Tiliotteen tuontiasetukset vaihtelevat sähköisen tiliotteen muodon mukaan. Microsoft Dynamics 365 for Operations tukee heti kolmea tiliotemuotoa, jotka ovat ISO20022, MT940 ja BAI2.

## <a name="sample-files"></a>Mallitiedostot
Tarvitset kaikkia kolmea muotoa varten tiedostot, jotka kääntävät sähköisen tiliotteen alkuperäisestä muodosta muotoon, jota Dynamics 365 for Operations voi käyttää. Tarvittavat resurssitiedostot sijaitsevat Microsoft Visual Studion Application Explorerin **Resurssit**-solmussa. Kun olet löytänyt tiedot, kopioi ne yhteen tunnettuun sijaintiin, sillä silloin ne on helpompi ladata palvelimeen määritysprosessin aikana.

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
Alla on esimerkkejä tuonnin lisäasetuksia pankkitilin täsmäytystietojen tuontitiedoston teknisistä asettelumäärityksistä sekä kolme esimerkkitiliotetiedostoa: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  

| Tekninen asettelumääritys                             | Esimerkkitiliotetiedosto          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |

 

## <a name="set-up-the-import-of-iso20022-bank-statements"></a>Määritä ISO20022-tiliotteiden tuonti
Määritä ensin ISO20022-tiliotteiden tiliotemuodon käsittelyryhmä käyttämällä tietoyksikkökehystä.

1.  Valitse **Työtilat** &gt; **Tietojen hallinta**.
2.  Valitse **Tuo**.
3.  Anna muodolle nimi, kuten **ISO20022**.
4.  Valitse **Lähdetietojen muoto **-kenttään **XML-elementti**.
5.  Valitse **Yksikön nimi** -kenttään **Tiliotteet**.
6.  Voit ladata tuontitiedostot valitsemalla **Lataa palvelimeen** ja siirtymällä sitten aiemmin tallentamaasi **SampleBankCompositeEntity.xml**-tiedostoon.
7.  Kun Tiliotteet-yksikkö on ladattu ja yhdistämismääritykset ovat valmiit, valitse yksikölle **Näytä yhdistämismääritykset** -toiminto.
8.  Tiliotteet-yksikkö on neljästä eri yksiköstä koostuva yhdistelmäyksikkö. Valitse luettelossa ensin **BankStatementDocumentEntity** ja sitten **Näytä yhdistämismääritykset** -toiminto.
9.  Valitse **Muunnokset**-välilehdessä **Uusi**.
10. Valitse järjestysnumerolle 1 ensin **Lataa tiedosto palvelimeen** ja sitten aiemmin tallentamasi** ISO20022XML-to-Reconciliation.xslt**-tiedosto. **Huomautus:** Dynamics 365 for Operationsin muunnostiedostot ovat vakiomuotoisia. Koska pankit poikkeavat usein tästä muodosta, sinun on päivitettävä tiliotemuotoon yhdistämismääritettävä muunnostiedosto. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
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
3.  Valitse **Täsmäytys**-välilehdessä **Pankkitilin täsmäytyksen lisätoiminnot **-asetukseksi **Kyllä**.
4.  Määritä **Tiliotteen muotoilu **-kenttä aiemmin luomallesi muotoilulle, kuten **ISO20022**.

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
12. Valitse järjestysnumerolle 2 ensin **Lataa tiedosto palvelimeen** ja sitten aiemmin tallentamasi **MT940XML-to-Reconciliation.xslt**-tiedosto. **Huomautus:** Dynamics 365 for Operationsin muunnostiedostot ovat vakiomuotoisia. Koska pankit poikkeavat usein tästä muodosta, sinun on päivitettävä tiliotemuotoon yhdistämismääritettävä muunnostiedosto. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
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
12. Valitse järjestysnumerolle 2 ensin **Lataa tiedosto palvelimeen** ja sitten aiemmin tallentamasi **BAI2XML-to-Reconciliation.xslt**-tiedosto. **Huomautus:** Dynamics 365 for Operationsin muunnostiedostot ovat vakiomuotoisia. Koska pankit poikkeavat usein tästä muodosta, sinun on päivitettävä tiliotemuotoon yhdistämismääritettävä muunnostiedosto. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
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




